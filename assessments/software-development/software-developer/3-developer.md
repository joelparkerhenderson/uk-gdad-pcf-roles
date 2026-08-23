# Developer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a developer in the UK Government Digital and Data profession — someone who delivers software components that form part of a product, develops software to meet user needs, follows best practice guidelines and helps to improve them, and writes clean, secure and well-tested code. The role description adds two things that shape the whole discipline in government: you work test-first, and you create code that is open by default and easy for others to reuse.

You may be preparing for a formal assessment as part of a recruitment or promotion process, or you may want to sharpen the reasoning your job depends on. Either way, it is worth being clear about what psychometric assessment is and is not. It is not a coding test — nobody will ask you to implement a linked list — and it is not a knowledge quiz about frameworks. It is a standardised sample of the thinking a role demands, and a good deal of what makes a developer effective is not typing speed or language knowledge but reasoning: deducing what a bug report actually implies, working out which of two explanations the evidence supports, judging what a test proves, deciding what to do first when three things are broken, and reading a specification precisely enough to build the right thing.

Three features of your role shape the questions here. First, you write code others will read, reuse and maintain — code that is open by default is code somebody outside your team will depend on, which raises the cost of a poor interface or an unclear name. Second, you work in a team with shared standards, so several items concern reviewing somebody else's work or explaining your own. Third, government software runs in production for a long time, serves people who have no alternative, and handles data that matters. That combination puts unusual weight on security, resilience and the honest assessment of risk.

The document has four main sections: a cognitive assessment, a numeric reasoning assessment, a verbal reasoning assessment, and a situational judgement assessment. Each provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Commit to an answer before reading each explanation. The explanations spend most of their words on why the near-miss options fail.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role genuinely uses, presented through practical workplace materials rather than abstract puzzles. Instead of number sequences you will meet bug reports, log extracts, test results, code review situations, deployment decisions and specifications.

The format is typically an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group at a comparable level. Many platforms are adaptive, so a test that feels hard is usually one you are doing well on, and acuity reports distinguishing speed from accuracy reward precision.

Three things characterise this section for a developer.

The first is that debugging is deduction, and the assessment format is unusually close to it. A bug report plus a log extract plus what you know about the system is a set of premises, and the skill is drawing only the conclusion they support — which is precisely what the logic items test, and precisely what separates a developer who fixes the cause from one who fixes the symptom.

The second is that evidence about software is frequently negative and frequently misread. A passing test proves that one path works, not that the code is correct; an absence of errors in a log may mean nothing went wrong or may mean nothing was logged. Several items turn on what a piece of evidence can and cannot establish.

The third is proportionality under pressure. When something is broken in production, the reasoning that matters is about consequence and reversibility, not about which fix is most elegant.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Logical deduction** maps to **Programming and build (software engineering)** and to debugging generally, where reasoning from symptoms to causes is the daily work.
- **Error checking** maps to **Modern development standards**, where writing and reviewing clean, well-tested code depends on systematic checking.
- **Pattern recognition** maps to **Service support**, where recurring incidents point at a cause, and to **Systems integration**.
- **Prioritisation** maps to **Service support** and **Availability and capacity management**, where what you do first under incident conditions is a reasoning task.
- **Applied problem solving** maps to **Systems design** and **Prototyping**, where you explore an approach before committing.
- **Reasoning about security** maps to **Information security**, where the relevant question is usually what an attacker could do rather than what a user will.

### Practice questions

**Question 1 (easy) — Deduction from a deployment rule**

Your team's rule states: "A change may only be deployed to production if it has passed the full test suite, unless it is a rollback to a previously deployed version." A colleague says: "I deployed at 3pm and the full suite had not passed." Which must be true?

- A) The rule was broken.
- B) The deployment was a rollback.
- C) Either the deployment was a rollback to a previously deployed version, or the rule was broken.
- D) The deployment caused a problem.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction. Options A and B each assume a branch without evidence. Option D introduces a consequence nothing supports — a deployment outside the rule may work perfectly, which is exactly why the rule needs enforcing rather than relying on outcomes. Only C holds. The workplace version matters: during an incident, rollbacks legitimately bypass the suite, so "the suite had not passed" is entirely consistent with correct behaviour, and asking which route was taken gets you an answer where an accusation gets you a defensive colleague.

**Question 2 (easy) — What a passing test proves**

A function that parses dates has 100% line coverage and all tests pass. A bug report says it returns the wrong value for 29 February 2024. What is the strongest inference?

- A) The bug report is wrong; coverage is complete.
- B) Line coverage measures which lines executed, not which inputs were tried — so complete coverage is entirely consistent with a leap-year bug, because the tests may have executed every line without ever passing a leap day.
- C) The tests are badly written.
- D) The function needs rewriting.

**Correct answer: B**

**Explanation:** This is the most consequential misunderstanding about test coverage, and it is worth being precise about. Coverage tells you that a line ran during the test suite; it says nothing about whether the inputs that ran it were the interesting ones. A date parser can achieve 100% line coverage with two test cases and still mishandle leap years, month boundaries, time zones and the epoch. Option B says this. Option A treats a coverage figure as a correctness proof, which is the error the metric invites. Option C is a reasonable inference and premature — the tests may be well written for the cases somebody thought of, and thinking of leap days is exactly what is hard. Option D leaps to a remedy before the diagnosis; the fix here is probably three lines and a test.

**Question 3 (moderate) — Reasoning from a log**

A service returns 500 errors for about 2% of requests. The application log shows no errors. What is the strongest analysis?

- A) The 500s are not coming from this service.
- B) An absence of logged errors is consistent with several things — the errors occur before the application code runs, such as in a proxy or load balancer; or they occur in a path with no logging; or the logging itself is failing — so the absence is a clue about where to look rather than evidence that the service is fine.
- C) The monitoring is wrong.
- D) The log level should be increased.

**Correct answer: B**

**Explanation:** The instructive feature is that a negative observation is being treated as information, and it is — just not the information it appears to be. Errors reaching the client but not the application log means something is producing them outside the code that logs, and the three candidates in option B are the realistic ones, each pointing somewhere different: infrastructure, an unlogged code path, or the logging pipeline. Option A is one of those possibilities stated as a conclusion. Option D is a sensible next action and does not follow from the reasoning if the errors never reach the application. Option C dismisses the observation that started the investigation, which is almost always the wrong first move — the monitoring is usually right and inconveniently so.

**Question 4 (moderate) — Prioritising during an incident**

At 10am four things are true. (i) A payment endpoint is returning errors for about 5% of requests. (ii) A scheduled batch job failed overnight and needs rerunning before 6pm. (iii) A colleague is blocked waiting for your code review. (iv) Your own feature is due for demo tomorrow. What should you do first?

- A) The code review, since it unblocks someone and takes ten minutes.
- B) The payment errors, because users are losing money or being unable to pay right now, and the failure rate means the problem is ongoing rather than historical.
- C) The batch job, because it has a hard deadline.
- D) Your feature, since the demo is soonest.

**Correct answer: B**

**Explanation:** Prioritisation under incident conditions ranks by ongoing harm and reversibility. The payment errors are happening now, to real users, with money involved, and every minute of delay adds affected people — which makes it the only item on the list where waiting increases the cost. The batch job has a hard deadline eight hours away and is a known quantity, so it is next and can be started once the payment issue is understood. The review takes ten minutes and can slot in. Your feature has until tomorrow. Option A is tempting because it is quick and helps a colleague, and quick-and-helpful is exactly the trap in incident triage. Option C ranks by deadline rather than by whether harm is accumulating.

**Question 5 (moderate) — Competing explanations**

After a deploy, response times rise from 200ms to 900ms. The deploy contained a database query change and a dependency upgrade. What is the strongest approach?

- A) Revert the query change, since queries cause slowness.
- B) Revert the whole deploy first to restore service, then reproduce in a non-production environment to establish which change is responsible — because with two candidate causes, guessing has a 50% chance of leaving the problem in place while appearing to have acted.
- C) Add an index to the query.
- D) Profile the running production system.

**Correct answer: B**

**Explanation:** Two changes went out together and either could be responsible, which makes this a question about sequencing rather than diagnosis. Option B separates the two goals correctly: restoring service is urgent and reverting achieves it with certainty, while identifying the cause is important and can be done safely afterwards. Reverting first also preserves the ability to reproduce, since the deployed artefact still exists. Option A guesses, and the guess is plausible enough to be dangerous — a dependency upgrade can easily add latency through a changed default, a new retry policy or altered connection pooling. Option C adds a change during an incident on an unconfirmed diagnosis. Option D is a legitimate technique and leaves users on a degraded service while you investigate.

**Question 6 (moderate) — Reviewing a colleague's code**

A pull request adds a feature. The code is clear and well structured. It also constructs a database query by concatenating a user-supplied string. What is the most important review comment?

- A) The code is well structured; approve with minor comments.
- B) The string concatenation is a SQL injection vulnerability regardless of how clean the surrounding code is, and it needs a parameterised query — this is a blocking comment rather than a suggestion, because the consequence is arbitrary data access rather than a maintainability cost.
- C) Suggest extracting the query into a repository class.
- D) Ask for a test covering the new feature.

**Correct answer: B**

**Explanation:** The instructive combination is clean, well-structured code containing a serious vulnerability, and the point is that the two are independent — readability tells you nothing about safety, and a well-written injection is still an injection. Option B names it, states the fix, and — importantly — categorises it as blocking, because review comments that read as suggestions get deferred. Options C and D are legitimate comments on a page containing a vulnerability, and raising them alongside without distinguishing severity is the review equivalent of a bug list with no ordering. Option A is the failure mode this question exists to catch: a review that assesses style and misses security is the review that lets it through.

**Question 7 (moderate) — What an intermittent failure implies**

A test fails about one run in twenty, always in the same test, always with a timeout. What is the strongest analysis?

- A) The test is flaky and should be retried automatically.
- B) An intermittent timeout usually indicates a real dependency on something non-deterministic — timing, ordering, shared state, or an external call — and each has a different fix, so the useful step is to establish which rather than to suppress the symptom.
- C) The timeout should be increased.
- D) The test should be deleted.

**Correct answer: B**

**Explanation:** "Flaky" is a description rather than a diagnosis, and treating it as one is how test suites become untrustworthy. An intermittent timeout has a small number of realistic causes: a race between the test and something asynchronous, an ordering dependency exposed when tests run in a different sequence, shared state leaking between tests, or a genuine external dependency. Each has a specific and different fix. Option B says this. Options A and C suppress the symptom, and the reason that matters is not purity: a suite with automatic retries and generous timeouts eventually stops failing for real reasons too, and the intermittent failure may be telling you about a race that will also occur in production. Option D discards coverage.

**Question 8 (harder) — Scoping the impact of a bug**

You find that a function has been rounding currency values with floating-point arithmetic. It has been in production for six months. Which is the strongest first step?

- A) Fix the function.
- B) Fix it, and establish the blast radius before anything else is decided — which values were affected, by how much, whether the errors accumulate or cancel, whether anything downstream has been stored or reported, and whether anyone has been over- or undercharged.
- C) Change to a decimal type and redeploy.
- D) Raise it with your lead.

**Correct answer: B**

**Explanation:** The fix is the easy part and the smallest part. Floating-point currency errors are typically fractions of a penny per operation, which sounds negligible and is not, because the question is what happened to those fractions over six months: whether they accumulated in a stored balance, whether they were reported in figures somebody relied on, and whether any individual was materially over- or undercharged. Option B establishes that, and the reason it matters is that the answer determines whether this is a code fix, a data remediation, or something with financial and possibly regulatory consequences. Option D is a reasonable and incomplete action — you should tell your lead, and telling them "I found a rounding bug" is far less useful than telling them what it did. Options A and C fix forward and leave six months of consequences unexamined.

**Question 9 (harder) — A security judgement**

A feature needs to display a user's own reference number. A colleague proposes reading the reference number from a URL parameter, since the user's own reference is already in their session. What is the strongest analysis?

- A) It is fine; the user only sees their own reference.
- B) Taking the reference from the URL means the server is trusting a value the user controls, so anyone can change it to another reference and see somebody else's data unless the server independently checks that the reference belongs to the session — the fix is to derive it from the session rather than to validate the parameter.
- C) The parameter should be encrypted.
- D) The reference should be obfuscated.

**Correct answer: B**

**Explanation:** This is the most common access control vulnerability in web applications, and the reasoning that catches it is a habit rather than a piece of knowledge: ask what an attacker controls. A URL parameter is under the user's complete control, so a server acting on it is acting on attacker input, and the fact that the legitimate user would only ever see their own reference is irrelevant to what a curious or malicious one can do. Option B names both the vulnerability and the correct fix, and the distinction in that fix matters — deriving the value from the session removes the attack surface entirely, whereas validating the parameter leaves a check somebody can later forget to apply. Options C and D obscure the value rather than protecting the resource, which is security through obscurity and fails as soon as somebody guesses a pattern.

**Question 10 (harder) — Systems integration reasoning**

Your service calls an external API that has started returning responses more slowly, occasionally taking 30 seconds. Your service has no timeout configured. What is the most important consequence?

- A) Some requests will be slow.
- B) Without a timeout, slow upstream responses hold your service's connections and threads open, so a slow dependency can exhaust your resources and take your service down entirely — the failure mode is not slowness but total unavailability, and it affects users who never touch that dependency.
- C) The external API should be asked to improve.
- D) Responses should be cached.

**Correct answer: B**

**Explanation:** The key insight is that the failure propagates and amplifies. A request waiting 30 seconds on an upstream call is holding a connection, a thread or an event-loop slot for 30 seconds, and if requests arrive faster than they complete, the pool exhausts and every request fails — including requests to endpoints that never call the external API. That turns a partial degradation in somebody else's system into a total outage in yours, which is why timeouts, and usually circuit breakers, are not optimisations but structural requirements when integrating with anything you do not control. Option A describes the visible symptom and misses the mechanism. Option C is worth doing and does not protect you. Option D helps for cacheable responses and does nothing for the resource exhaustion.

**Question 11 (harder) — Reading a specification precisely**

A specification states: "The service must reject applications submitted more than 28 days after the qualifying event, unless the applicant has been granted an extension." You are implementing the check. What must you establish before writing it?

- A) Nothing; the rule is clear.
- B) At least three things the specification does not settle — whether 28 days means calendar or working days, whether the boundary is inclusive so that day 28 is accepted, and how the system knows an extension has been granted — because each changes the code and getting any of them wrong produces wrongly rejected applications.
- C) Whether the extension is 14 days.
- D) What error message to show.

**Correct answer: B**

**Explanation:** The rule reads as clear and is not implementable as written, which is the characteristic situation. Calendar versus working days changes the answer by up to four days. Boundary inclusivity decides whether somebody applying on day 28 succeeds, and specifications are almost never explicit about it. And "has been granted an extension" describes a state the code must be able to check, which means there is a data question — a flag, a record, a date — that somebody must answer. Option B identifies all three. Option D is a real question and much less consequential. Option A is the answer that produces a plausible implementation and a rejected application from somebody who applied in time, which is the kind of defect that surfaces as a complaint rather than an error.

**Question 12 (harder) — A test that proves less than it appears**

A colleague adds a test asserting that a function returns successfully when called with valid input, and cites it as evidence the function is correct. What is the strongest observation?

- A) The test is a reasonable start.
- B) The test establishes that one valid input does not error, which is the weakest thing that could be tested — it says nothing about whether the returned value is right, what happens with invalid input, or what happens at boundaries, and a function returning a wrong answer confidently would pass it.
- C) More test cases are needed.
- D) The test should assert on the return value.

**Correct answer: B**

**Explanation:** The specific weakness is worth naming precisely rather than generally, and option B does: a test asserting only that a call completes will pass for a function that returns the wrong answer, returns nothing, or silently swallows an error. That makes it worse than no test in one respect, because it creates the appearance of coverage. Options C and D each identify one part of the gap — more cases, and asserting on the value — and B names both plus the boundary question, which is where defects actually live. Option A is charitable and misses the point of the review. The useful framing for a colleague is not that the test is bad but that it does not yet test the thing they care about, which is what the function returns.

### Preparation tips

- **Ask what evidence can and cannot establish.** Coverage, passing tests and empty logs all prove less than they appear.
- **Ask what an attacker controls.** It is the habit that catches most access control bugs.
- **Separate restoring service from finding the cause.** Revert first, diagnose after.
- **Treat "flaky" as a description, not a diagnosis.**
- **Establish blast radius before deciding what a fix is.**
- **Read a rule for what it does not settle.** Boundaries, units and state are where specifications are silent.
- **Rank by accumulating harm during an incident.** Quick and helpful is a trap.
- **Distinguish blocking review comments from suggestions.** Severity that is not stated is not heard.

### Common pitfalls to avoid

- **Treating line coverage as a correctness measure.**
- **Reading an empty error log as evidence nothing is wrong.**
- **Guessing between two candidate causes during an incident.**
- **Suppressing an intermittent failure with retries or longer timeouts.**
- **Reviewing for style and missing a vulnerability.**
- **Validating attacker-controlled input rather than not trusting it.**
- **Integrating without a timeout.** Slow upstreams cause total outages, not slow responses.
- **Implementing a rule that reads clearly but is not implementable as written.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle the quantitative material your role produces. Developers sometimes assume this section is beneath them because they work with numbers constantly, and that assumption is worth examining: the numbers in this section are not arithmetic problems but operational ones — error rates, latency percentiles, capacity headroom, throughput, storage growth and the figures in a performance report — and the errors people make with them are errors of interpretation rather than calculation.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a table, chart or paragraph of figures with a multiple-choice question. Calculators are usually provided and the arithmetic is deliberately tractable. Time per item is tight, so the operative skill is locating what matters and disregarding what does not.

Four habits carry the load. Establish what the question asks before looking at the data. Identify the denominator and the population it represents. Estimate, calculate, compare. And sanity-check against the world — which for you means asking whether a figure is physically plausible given what you know about the system.

One warning about the options. Distractors are built from predictable errors: dividing by the wrong total, confusing a percentage with a percentage point, using the new value as the base in a percentage change, and — specific to this domain — reading an average where a percentile is the meaningful measure.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Rates and error budgets** map to **Availability and capacity management**, where service levels are numerical commitments.
- **Percentiles and distributions** map to **Availability and capacity management** and **Service support**, where averages routinely conceal the experience being complained about.
- **Capacity arithmetic** maps to **Availability and capacity management**, where headroom and growth determine when something breaks.
- **Interpreting monitoring data** maps to **Service support**, where the numbers are the first evidence in an incident.
- **Comparing before and after** maps to **Development process optimisation**, where knowing whether a change helped requires the right comparison.
- **Sizing and estimation** maps to **Systems design**, where a design decision usually rests on an order-of-magnitude judgement.

### Practice questions

**Question 1 (easy) — Error rate**

Of 240,000 requests in a day, 6,000 returned errors. What is the error rate?

- A) 2.0%
- B) 2.5%
- C) 4.0%
- D) 25%

**Correct answer: B**

**Explanation:** 6,000 ÷ 240,000 = 0.025, so 2.5%, giving B. Estimate first: 6,000 of 240,000 is one fortieth, and one fortieth is 2.5%. Option A comes from dividing by 300,000. The figure is worth putting in context, which is the habit that matters more than the arithmetic: 2.5% sounds small and means 6,000 failed requests, and whether that is a crisis depends entirely on what failed — 6,000 failed health checks are noise, 6,000 failed payments are not.

**Question 2 (easy) — Availability arithmetic**

A service commits to 99.9% availability. How much downtime does that permit in a 30-day month?

- A) About 43 minutes
- B) About 4 hours
- C) About 7 hours
- D) About 3 minutes

**Correct answer: A**

**Explanation:** A 30-day month contains 43,200 minutes, and 0.1% of that is 43.2 minutes, giving A. The figure is worth knowing by heart because it recurs constantly: three nines is roughly 43 minutes a month, four nines is roughly four minutes, and two nines is roughly seven hours. Option C is the two-nines figure and option D is roughly four nines, so the distractors are the adjacent commitments — which is the real-world confusion, since the difference between 99.9% and 99.99% is one character in a document and an order of magnitude in what it requires operationally.

**Question 3 (easy) — Percentile versus average**

Response times are reported as: mean 180ms, 50th percentile 120ms, 95th percentile 800ms, 99th percentile 4,200ms. Users complain the service is slow. Which figure best explains the complaints?

- A) The mean, at 180ms.
- B) The 99th percentile at 4,200ms — one request in a hundred taking over four seconds means a user making several requests in a session will very likely hit at least one, and a page assembling ten calls will hit one most of the time.
- C) The median, at 120ms.
- D) None; the service is fast.

**Correct answer: B**

**Explanation:** This is the most important numerical concept in operating a service, and the arithmetic behind it is what makes it persuasive. A 1% chance of a slow request sounds negligible per request and is not per session: a page making ten backend calls has roughly a 1 − 0.99¹⁰ chance of hitting at least one, which is about 10%, and a user making thirty requests across a session will hit one more often than not. Option B says this. Options A and C report figures that are true and describe the requests nobody complains about. Option D is the conclusion somebody reaches from the mean, and it is why tail latency is reported separately — averages are dominated by the fast majority and hide exactly the experience generating the tickets.

**Question 4 (easy) — Storage growth**

A database grows by 4 GB a month and currently holds 120 GB. The disk is 200 GB. How long until it is full?

- A) 10 months
- B) 20 months
- C) 30 months
- D) 50 months

**Correct answer: B**

**Explanation:** Remaining capacity is 200 − 120 = 80 GB, and 80 ÷ 4 = 20 months, giving B. Option D divides the total by the growth rate rather than the remaining space. The practical point is that 20 months is not the number that matters: databases degrade well before a disk is full, indexes and temporary space need headroom, and the growth rate is unlikely to be constant. The useful figure is when you reach a threshold you have chosen — typically 80%, which here is 160 GB and arrives in 10 months — and that is what an alert should be set against, because arriving at a full disk is an incident while arriving at 80% is a planning conversation.

**Question 5 (moderate) — Throughput and concurrency**

A service handles requests taking on average 200ms and runs 8 worker threads. What is the theoretical maximum throughput?

- A) 8 requests per second
- B) 40 requests per second
- C) 1,600 requests per second
- D) 400 requests per second

**Correct answer: B**

**Explanation:** Each worker completes 1 ÷ 0.2 = 5 requests per second, and 8 workers give 40 per second, so B. Option A ignores the request duration; option C multiplies by milliseconds. The word "theoretical" is carrying weight and the practical implication is worth stating: real throughput is lower because of contention, garbage collection, connection limits and the fact that average duration hides a tail, and a service designed to run at its theoretical maximum has no headroom for a slow dependency or a traffic spike. A common rule of thumb is to plan for well below the theoretical ceiling, and knowing where that ceiling is remains the starting point for the conversation.

**Question 6 (moderate) — Comparing before and after**

Before a change, 480 of 6,000 daily requests errored. After, 300 of 7,500 errored. Did the error rate improve, and by how much in percentage points?

- A) Yes, by 180 requests
- B) Yes, by 4 percentage points
- C) Yes, by 3 percentage points
- D) No, it worsened

**Correct answer: B**

**Explanation:** Convert to rates because the volumes differ. Before: 480 ÷ 6,000 = 8%. After: 300 ÷ 7,500 = 4%. The improvement is 4 percentage points, giving B — and it is also a halving, which is the more striking way to say it. Option A compares raw counts across different traffic levels, and note the direction of the distortion: traffic rose, so the raw fall of 180 understates the improvement considerably. That is worth registering because the usual warning about raw counts assumes they flatter, and here they conceal a genuine win, which is a good reason to convert every time rather than only when suspicious.

**Question 7 (moderate) — Percentage change**

Median response time rose from 120ms to 150ms after a deploy. What is the increase?

- A) 20%
- B) 25%
- C) 30ms, which is the meaningful figure
- D) 80%

**Correct answer: B**

**Explanation:** The difference is 30ms, and 30 ÷ 120 = 0.25, a 25% increase, giving B. Option A divides by the new figure, the most common error in this question type. Option C is a true statement and answers a different question, though it is worth noting that in latency work the absolute figure is often the one that matters — 30ms added to 120ms is a 25% regression and is imperceptible to a user, while 30ms added to a 20ms call is a 150% regression and still imperceptible. Percentages on latency need their absolute context, which is why good reporting gives both.

**Question 8 (moderate) — Reading an error budget**

A service with a 99.9% availability target has used 32 minutes of its 43-minute monthly budget by day 10. What is the strongest observation?

- A) There is budget remaining.
- B) At this rate the budget will be exhausted around day 13 of a 30-day month, so the useful action is to establish what consumed 32 minutes in ten days rather than to note that some remains — an error budget is a signal about trajectory rather than a quota to spend down.
- C) The target should be lowered.
- D) 32 minutes is acceptable for a month.

**Correct answer: B**

**Explanation:** The arithmetic is the point: 32 minutes in 10 days is 3.2 minutes a day, and the remaining 11 minutes lasts about three and a half more days. Option B does that calculation and draws the right conclusion, which is about trajectory rather than remainder — an error budget consumed early is a signal that something is systematically wrong, and the useful response is diagnostic rather than administrative. Option A is literally true and is the reading that produces a surprised incident review at the end of the month. Option D confuses the monthly total with the current position. Option C responds to a signal by removing the instrument.

**Question 9 (moderate) — Sizing a decision**

A proposed cache would serve 85% of requests from memory. Cached responses take 5ms; uncached take 200ms. What is the expected average response time?

- A) 25ms
- B) 34ms
- C) 100ms
- D) 170ms

**Correct answer: B**

**Explanation:** Weight each outcome by its probability: 0.85 × 5 = 4.25ms, plus 0.15 × 200 = 30ms, giving 34.25ms, so B. Option A ignores the uncached contribution; option C averages the two times without weighting. The calculation is worth being able to do quickly because it is how cache decisions get justified, and it is also worth noticing what it conceals: an average of 34ms is dominated by the 15% of requests still taking 200ms, so the tail is unchanged and users hitting cache misses see no improvement at all. A cache improves the average dramatically and the 95th percentile barely, which is the opposite of what a summary figure suggests.

**Question 10 (harder) — A metric that misleads**

A dashboard shows average CPU utilisation across a cluster at 40%, and a colleague concludes there is ample headroom. What is the strongest observation?

- A) 40% is comfortable.
- B) An average across a cluster conceals distribution — one instance at 95% and four at 26% averages to 40%, and the hot instance is the one that will fail — so the useful figures are per-instance utilisation and the maximum, not the mean.
- C) More instances should be added.
- D) CPU is the wrong metric.

**Correct answer: B**

**Explanation:** Averaging across instances is one of the most reliably misleading things a dashboard does, because failures are local: a cluster does not fall over at its average utilisation, it falls over when one member is saturated, and uneven load distribution is extremely common — caused by sticky sessions, uneven partitioning, one instance holding a long-running job, or a load balancer that is not balancing. Option B names this and states what to look at instead. Option A reads the mean as the position. Option C acts on the misleading figure and may add capacity that receives no traffic. Option D is a reasonable secondary point, since CPU may not be the constraint, and it does not address the averaging error which would apply equally to memory or connections.

**Question 11 (harder) — Percentage points and relative change**

A service's success rate rose from 96% to 98%. Which statement is most useful?

- A) A 2% improvement.
- B) A 2 percentage point improvement, and — more usefully for a service at this level — the failure rate halved from 4% to 2%, which is the framing that shows the size of the change.
- C) A 2.08% relative improvement.
- D) A 50% improvement.

**Correct answer: B**

**Explanation:** All three arithmetic descriptions are defensible: 2 percentage points, a 2.08% relative increase in success, and a 50% reduction in failure. The point of the item is that they are not equally informative. At high success rates the interesting quantity is the failure rate, because that is what users experience and what work is required to reduce — improving 96% to 98% means eliminating half of all failures, which is substantial and is completely obscured by "a 2% improvement". Option B says this. Option D states the halving without labelling it, which is how misleading claims get made honestly. Option A is ambiguous and understates. The general habit: as a rate approaches 100%, report the complement.

**Question 12 (harder) — A plausibility check**

A report states that a batch job processed 2.4 million records in 90 seconds. Your service writes each record to a database with an average write latency of 3ms. What is the strongest observation?

- A) The job is well optimised.
- B) The figures do not reconcile with sequential writes — 2.4 million writes at 3ms each is 7,200 seconds, so either the writes are batched or parallelised by a factor of about eighty, or the record count or the timing is wrong, and establishing which matters before anyone plans capacity on this figure.
- C) The database is fast.
- D) The latency figure must be wrong.

**Correct answer: B**

**Explanation:** The sanity check is the skill: 2,400,000 × 0.003 seconds = 7,200 seconds, which is two hours rather than 90 seconds, so the reported figures are inconsistent with the naive model by a factor of eighty. That does not mean the report is wrong — batched inserts, bulk loading and parallel writers all achieve exactly this kind of speedup, and any of them would explain it. But it does mean somebody should say which, because the difference matters for capacity planning, for whether the pattern is reusable, and for whether the 3ms figure applies at all. Option D picks one resolution arbitrarily. Options A and C accept an unexplained figure. The habit of multiplying out a claimed throughput against a known per-unit cost catches a surprising number of misunderstandings.

### Preparation tips

- **Learn the availability figures by heart.** 99.9% is about 43 minutes a month; 99.99% is about four.
- **Ask for percentiles, not averages.** The complaint is almost always in the tail.
- **Compute session-level probability from per-request rates.** A 1% slow rate is a 10% slow page at ten calls.
- **Set thresholds, not endpoints.** When you reach 80% is the planning date; when you reach 100% is the incident.
- **Convert rates before comparing before and after.** Traffic changes conceal improvements as well as inflating them.
- **Report the complement at high success rates.** 96% to 98% is a halving of failures.
- **Distrust averages across instances.** Failures are local.
- **Multiply out claimed throughput against known per-unit cost.** It catches inconsistencies fast.

### Common pitfalls to avoid

- **Reading a mean where a percentile is the meaningful measure.**
- **Comparing raw counts across different traffic volumes.**
- **Dividing by the new value in percentage change.**
- **Treating an error budget as a quota rather than a trajectory.**
- **Averaging utilisation across instances.**
- **Reporting a cache's effect on the average and implying it helped the tail.**
- **Planning capacity to a disk-full date rather than a threshold.**
- **Accepting a throughput figure that does not reconcile with per-unit costs.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. Developers sometimes expect this to be the least relevant section and it is arguably the most: you build from specifications, tickets, standards and API contracts, and the gap between what a document says and what you assume it says is where a substantial proportion of defects originate. A misread requirement produces working software that does the wrong thing, which is more expensive than software that does not work, because nobody notices for months.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. True means the statement follows necessarily. False means the passage contradicts it. Cannot Say means the passage neither establishes nor excludes it. Alongside these come comprehension items, main-point items, and questions asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone. Your knowledge of how systems usually work must be set aside — and this is the specific hazard for a developer, because you know what a sensible system would do, and supplying that rather than what the specification says is exactly how requirements get implemented as the developer imagined them.

Cannot Say deserves particular attention. Developers avoid it because a ticket demanding an answer is not satisfied by "the specification does not say". In practice that answer is frequently correct and is the most valuable thing you can produce, because it identifies a decision somebody must make before you write code that assumes one.

Small words carry the load. "May", "should" and "must" have defined force in technical documents. "Or" is inclusive unless stated otherwise. And silence is a gap, not permission.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading specifications precisely** maps to **Programming and build (software engineering)**, where you use agreed specifications to design and code.
- **Separating statement from inference** maps to **Systems design**, where an assumption you did not notice becomes a design decision nobody agreed.
- **Identifying the main point** maps to **User focus**, where understanding what a requirement is for shapes what you build.
- **Handling qualified language** maps to **Modern development standards**, where knowing what a standard requires and what it recommends tells you where judgement applies.
- **Reading for absence** maps to **Information security**, where an unstated error condition or unspecified default is where vulnerabilities live.
- **Reading contracts and interfaces accurately** maps to **Systems integration**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Clients must include an Authorization header on all requests to protected endpoints. Clients may include an Idempotency-Key header on POST requests; where present, the server returns the original response for any repeated request with the same key within 24 hours. Servers must reject requests exceeding 2 MB with a 413 response. Clients should implement exponential backoff on 429 responses."

**Question 1 (easy)** — Statement: "Clients must include an Idempotency-Key on POST requests." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says clients *may* include it — optional. The statement's "must" contradicts that, so False. The passage uses three modal terms deliberately, and the distinction is operational rather than pedantic: Authorization is mandatory so a client without it fails, idempotency keys are optional so a client without one works but loses replay protection, and backoff is recommended so a client without it works and behaves badly under load. Implementing all three as mandatory produces unnecessary work; implementing all three as optional produces a client that fails.

**Question 2 (easy)** — Statement: "A repeated POST with the same key after 30 hours returns the original response." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The guarantee applies within 24 hours, and 30 falls outside it, so the statement is contradicted. False. Note what the passage does not establish: what happens after 24 hours is unstated, so the repeat might be processed as a new request, rejected, or something else. If you were implementing a client that retries after a long delay, that is a question you would need answered rather than assumed — and assuming it is safe because it was safe within the window is exactly how duplicate payments happen.

**Question 3 (moderate)** — Statement: "A client that does not implement exponential backoff violates the specification." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says clients *should* implement backoff. In specification usage "should" indicates a strong recommendation that may be departed from with good reason, not a requirement — so a client without it departs from a recommendation and does not violate the specification. False. The practical distinction matters: "must" tells you your client will be rejected, while "should" tells you it will work and will hammer a struggling service, which is a reason to implement it and not a compliance question. Reading the two as equivalent removes information you use to prioritise.

**Question 4 (harder)** — Statement: "A 1.9 MB request will be accepted." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage requires servers to reject requests *exceeding* 2 MB, so 1.9 MB is not rejected on size. But acceptance depends on authorisation, validity, rate limits and anything unmentioned, and the passage establishes only that one particular rejection does not apply. Cannot Say. The distinction between "will not be rejected for this reason" and "will be accepted" is one that matters when you are writing client code, because a client built on the second assumption has no handling for the other failure modes and will behave unpredictably the first time one occurs.

*Passage B — for Questions 5 to 8*

"The review of the platform found that teams using the shared deployment pipeline reported fewer failed releases than teams with bespoke pipelines. The review notes that teams on the shared pipeline were generally newer services with simpler architectures. The review did not assess whether failed releases were more severe in either group. It recommends that the platform team consider whether shared pipeline use should be mandatory."

**Question 5 (easy)** — Statement: "Teams using the shared pipeline reported fewer failed releases." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence states this directly and the statement restates it without addition. True. Note the passage's "reported fewer" rather than "had fewer", and the statement respects it. Answer quickly and bank the time for harder items.

**Question 6 (moderate)** — Statement: "The shared pipeline reduces failed releases." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports an association and then flags a substantial confound: the shared-pipeline teams were newer services with simpler architectures, which would be expected to have fewer failed releases whatever pipeline they used. So the difference may be attributable to the pipeline, to the simplicity, or to both. Cannot Say. This is the shape of most infrastructure comparisons and it is worth recognising, because the argument for a shared pipeline does not need this finding — reduced duplication and consistent security controls stand on their own — and resting the case on a confounded number invites somebody to dismantle it.

**Question 7 (moderate)** — Statement: "Failed releases on bespoke pipelines were more severe." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage says explicitly that severity was not assessed. Declared silence establishes nothing, so Cannot Say. The possibility is worth registering because it could run either way: teams with bespoke pipelines may have more failures that are trivially rolled back, or fewer that are catastrophic, and a count of failures without severity is a metric that could rank two very different situations identically. A review measuring frequency and not severity has told you about frequency.

**Question 8 (harder)** — Statement: "The review recommends making the shared pipeline mandatory." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The review recommends that the platform team *consider whether* it should be mandatory — a recommendation to evaluate, including deciding against. The statement asserts a recommendation to mandate, which was not made, so False rather than Cannot Say: the passage tells you what was recommended and it was something different. This distinction pervades review documents, and misreading it produces the familiar sequence in which a recommendation to consider becomes an item on a delivery plan that somebody then reports against.

*Passage C — for Questions 9 to 12*

"All code must be reviewed by at least one other developer before merging to the main branch, unless the change is a documentation-only change. Code containing changes to authentication or authorisation must be reviewed by two developers, at least one of whom is not on the authoring team. All merges to main must pass the automated test suite. Emergency fixes may be merged with a single review provided a second review is completed within one working day."

**Question 9 (easy)** — Statement: "All changes require review before merging to main." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage exempts documentation-only changes. The statement's "all" contradicts that, so False. The exemption is narrow and worth reading precisely — "documentation-only" means a change touching no code, so a change updating a comment and a variable name is not exempt. That is the kind of distinction people get wrong in the permissive direction under time pressure, and it is why the exemption is drafted with "only" rather than "documentation changes".

**Question 10 (moderate)** — Statement: "An emergency fix merged with one review, with a second review completed three days later, complies." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The emergency provision permits a single review *provided a second review is completed within one working day*. Three days exceeds that, so the condition fails and the merge does not comply. False. Note the structure: the emergency route is not an exemption from two reviews but a deferral of one, which is a different thing — and the practical consequence is that an emergency fix creates an obligation for the following day that is easy to forget once the incident is over, which is exactly when it gets forgotten.

**Question 11 (harder)** — Statement: "An authentication change reviewed by two developers from the authoring team complies." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The requirement for authentication and authorisation changes has two limbs: two reviewers, and at least one from outside the authoring team. Two reviewers from the authoring team satisfies the first and fails the second, so the statement is contradicted. False. The second limb exists for a specific reason worth understanding rather than merely complying with: a team that has designed an access control model shares its assumptions, and the reviewer most likely to notice that the model is wrong is the one who does not already believe it. Reading the requirement as "two reviewers" and satisfying it internally is compliance with the letter and defeat of the purpose.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) All code must be reviewed before merging.
- B) Changes reaching main must be independently checked in proportion to their risk — one reviewer normally, two including an outsider for access control changes, automated tests always, and a deferred rather than waived second review in emergencies.
- C) Authentication changes need two reviewers.
- D) Emergency fixes may be merged with one review.

**Correct answer: B**

**Explanation:** The main point must cover the whole passage while adding nothing. Option A drops the exemption and three provisions. Options C and D are each true of one clause, and D drops the condition that makes it a deferral rather than a waiver. Option B captures all four and names the logic joining them, which is proportionality: the review burden scales with the risk of the change, and the emergency route bends the timing without removing the requirement. Note that B preserves the "deferred rather than waived" distinction — a summary saying emergency fixes need only one review would be one a colleague could follow and still be in breach.

### Preparation tips

- **Read "may", "should" and "must" as terms of art.** They tell you whether your client fails, misbehaves or is merely suboptimal.
- **Distinguish "will not be rejected for this reason" from "will be accepted".**
- **Treat silence as a question to ask, not a default to assume.**
- **Trust Cannot Say.** It identifies the decision somebody must make before you write the code.
- **Read exemptions for their limiting words.** "Documentation-only" is narrower than "documentation".
- **Notice deferrals dressed as exemptions.** An emergency route usually creates an obligation for tomorrow.
- **Ask what a two-limbed requirement is for.** Satisfying one limb and defeating the purpose is the common failure.
- **Separate "consider whether X" from "recommend X".**

### Common pitfalls to avoid

- **Supplying the behaviour a sensible system would have.** The characteristic developer's misreading.
- **Rendering "should" as a requirement, or as optional.**
- **Assuming behaviour outside a stated window.**
- **Marking True on a claim that would support an approach you favour.**
- **Reading a proxy outcome as the thing itself.** Fewer failures is not less severe failures.
- **Widening an exemption under time pressure.**
- **Treating an emergency provision as a waiver.**
- **Satisfying a requirement's letter while defeating its purpose.**

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to parse and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures whether your judgement matches what the profession considers good practice at your level. Your role description places you as somebody who delivers software components forming part of a product, writes clean, secure, well-tested code, follows best practice guidelines and helps improve them, and produces code that is open by default and reusable. The strongest answers involve exercising real technical judgement, raising things through the right channel, and knowing which decisions belong to somebody else.

Four principles carry most scenarios, and two are specific to this discipline.

Users of government services usually have no alternative. Somebody who cannot complete a benefits application cannot take their custom elsewhere, which is why an outage or a data error carries weight that the same defect would not carry in a commercial product, and why "we can fix it next sprint" is a weaker answer here than it sounds.

Say what you know and what you do not. Software work runs on estimates, diagnoses and assurances, and the most damaging habit in the discipline is expressing a guess with the confidence of a measurement. Options that distinguish "I have verified this" from "I believe this" are consistently stronger.

Raise things early and through the right route. A concern raised before a decision is information; the same concern raised afterwards is criticism.

Leave the codebase better than you found it, within reason. Your role names helping to improve best practice guidelines, and that mostly happens through small consistent acts rather than initiatives.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Security judgement** maps to **Information security**.
- **Code review and standards** map to **Modern development standards**, where you help improve guidelines as well as follow them.
- **Incident behaviour** maps to **Service support** and **Availability and capacity management**.
- **Working with others' code and constraints** maps to **Systems integration** and **Programming and build**.
- **Improving how the team works** maps to **Development process optimisation**.
- **Keeping the user in view** maps to **User focus**.

### Practice questions

**Question 1 (easy) — A security issue in a colleague's code**

Reviewing a pull request, you find a query built by string concatenation from user input. The author is more senior than you. What is the most effective response?

- A) Approve it; they are more experienced and may have a reason.
- B) Comment specifically — that concatenating user input into a query allows SQL injection and a parameterised query fixes it — and mark the review as requesting changes, since the severity warrants blocking rather than a suggestion.
- C) Mention it in passing and approve.
- D) Raise it with your lead rather than the author.

**Correct answer: B. Least effective: A**

**Explanation:** Seniority is not a reason to approve a vulnerability, and the framing that makes this easy is that you are not judging the author, you are reporting a fact about the code — the query accepts arbitrary input into its structure. Option B states the issue, states the fix, and blocks, which matters because a comment that reads as a suggestion gets deferred and a vulnerability that gets deferred ships. Option A is least effective and is the failure mode the question exists to catch: deference in code review is how serious defects reach production, and a senior developer will almost always thank you. Option C raises it without weight. Option D bypasses somebody who has had no chance to respond, and treats a routine technical comment as a matter needing escalation.

**Question 2 (easy) — An estimate you are unsure about**

Your delivery manager asks how long a piece of work will take. You genuinely do not know, because it depends on how a third-party API behaves. What is the most effective response?

- A) Give your best guess as a number.
- B) Say what the estimate depends on and offer to timebox an investigation — a day spent establishing how the API behaves will produce an estimate worth having, whereas a number given now is a guess that will be treated as a commitment.
- C) Say you cannot estimate it.
- D) Give a wide range.

**Correct answer: B. Least effective: A**

**Explanation:** The distinction the question turns on is between an estimate and a guess, and the reason it matters is what happens to the number: a figure given in a planning meeting is recorded, communicated onward and becomes a commitment, and the uncertainty attached to it does not travel with it. Option B addresses the actual problem, which is a missing piece of information, and proposes the cheapest way to get it. A timeboxed spike is a normal and well-understood answer that delivery managers accept readily. Option A is least effective, converting uncertainty into a false commitment. Option C is honest and unhelpful, leaving the delivery manager with nothing. Option D is better than A and still supplies a number rather than resolving the unknown.

**Question 3 (easy) — Finding a bug in your own released code**

You discover that code you released last week has been silently writing an incorrect value to a record. What should you do?

- A) Fix it in the next release.
- B) Tell your team immediately, establish how many records are affected and whether anything downstream has consumed them, and treat the data remediation as a separate question from the code fix.
- C) Fix it quietly and correct the data.
- D) Fix the code and monitor.

**Correct answer: B. Least effective: C**

**Explanation:** Two problems exist and they are different: the code writes wrong values, and a week of wrong values exists in the database and possibly beyond it. The second is usually the larger one, because data flows — into reports, into downstream systems, into decisions somebody has already made — and a fix to the code does nothing about any of it. Option B separates them and establishes the scope, which is the information anybody deciding what to do next needs. Option C is least effective, and the concealment is the part that matters: a colleague who later discovers that data was silently corrected will trust nothing you say about your own code. Option D fixes forward and leaves the existing records wrong. Option A leaves the code writing wrong values.

**Question 4 (moderate) — Pressure to skip tests**

With a deadline tomorrow, a colleague suggests merging without tests and adding them next sprint. What is the most effective response?

- A) Agree; the deadline is real.
- B) Ask what specifically will not fit, since writing tests for the paths that matter is usually less work than it appears and the sprint after next is where untested code stays — and if something genuinely has to give, propose that it is scope rather than tests, and say so to whoever owns the deadline.
- C) Refuse and cite the standard.
- D) Merge without tests and write them yourself later.

**Correct answer: B. Least effective: D**

**Explanation:** The colleague has a real constraint and has proposed relieving it by taking on a debt the team will not repay — "next sprint" for tests is one of the least reliable commitments in software, not through bad faith but because the next sprint has its own deadline. Option B does three useful things: it questions the premise, since the test writing is often smaller than the anxiety about it; it proposes an alternative sacrifice, which is scope; and it puts the trade to the person who owns the deadline rather than resolving it between two developers. Option D is least effective, taking personal responsibility for a team commitment, which means the debt exists and nobody but you knows. Option A accepts the debt. Option C cites a rule without engaging with the constraint.

**Question 5 (moderate) — A third-party dependency with a vulnerability**

An automated scan flags a critical vulnerability in a library your service uses. The library is three major versions behind and upgrading looks substantial. What is the most effective first step?

- A) Start the upgrade.
- B) Establish whether your service is actually exposed — whether the vulnerable code path is one you call, and whether the conditions for exploitation apply in your deployment — because that determines whether this is an emergency, a scheduled upgrade, or a false positive, and the three warrant very different responses.
- C) Report it as a critical incident.
- D) Suppress the alert and schedule the upgrade.

**Correct answer: B. Least effective: D**

**Explanation:** Scanners report vulnerabilities in libraries, not in your service, and the two frequently differ: a critical flaw in a code path you never invoke, or one requiring a configuration you do not use, may not expose you at all. Establishing that is a couple of hours' work and determines everything that follows — genuine exposure justifies dropping other work, while no exposure turns a three-version upgrade into a planned piece of maintenance. Option B does the assessment first. Option D is least effective: suppressing an alert makes the finding invisible, and if the assessment is never done, nobody knows whether the scheduled upgrade is urgent. Option A commits substantial effort before establishing need. Option C escalates before knowing whether there is anything to escalate.

**Question 6 (moderate) — Disagreement about an approach**

You believe a colleague's design will not scale. They disagree and have more experience with the system. What is the most effective response?

- A) Defer to their experience.
- B) State your specific concern with the numbers behind it — the expected volume, the operation you think becomes a bottleneck, and why — and ask what you are missing, since a concrete concern either gets answered or turns out to be right, while a general worry gets dismissed.
- C) Escalate to the lead developer.
- D) Implement it and see.

**Correct answer: B. Least effective: A**

**Explanation:** The move that resolves this is making the concern specific enough to be checked. "I don't think this will scale" is an opinion and invites an opinion in return; "at 4,000 records this does a query per record, which is 4,000 queries at 3ms each" is a claim with an answer, and their answer is either that the volume is lower than you think, that the query is cached, or that you are right. Option B also asks what you are missing, which is honest — they may well know something — and makes the exchange collaborative rather than adversarial. Option A is least effective, deferring on experience rather than reasoning, which is how known problems get built. Option C escalates a technical disagreement that has a technical resolution. Option D is the most expensive way to find out.

**Question 7 (moderate) — Code that is open by default**

You are writing a component that will be published in a public repository. A colleague suggests hard-coding an internal hostname to save time, since it is not secret. What is the most effective response?

- A) Agree; it is not sensitive.
- B) Point out that a hard-coded internal hostname in a public repository reveals internal infrastructure to anyone reading it and makes the component unusable by anyone else — which defeats the purpose of publishing — so it belongs in configuration regardless of whether it counts as secret.
- C) Agree and add a note that it should be configurable later.
- D) Refuse to publish the repository.

**Correct answer: B. Least effective: C**

**Explanation:** Two separate objections apply and both are worth making. The security one is modest and real: internal hostnames are reconnaissance material even when they are not credentials, and a public repository is indexed. The reusability one is stronger and is the point of coding in the open — a component with somebody's internal hostname baked in cannot be used by anybody else, so publishing it achieves nothing beyond exposure. Option B names both. Option C is least effective, because "make it configurable later" in a published repository means the hostname is public now and probably permanently, since it will remain in the commit history even after a fix. Option A accepts both problems. Option D over-corrects by abandoning the publication rather than the hard-coding.

**Question 8 (harder) — An incident with an unclear cause**

A service is failing intermittently. You have a plausible theory but have not confirmed it. Your lead asks what is wrong. What is the most effective response?

- A) State your theory as the cause.
- B) State what you have established, state the theory as a theory, and say what would confirm or eliminate it — because during an incident a confidently stated guess sends people down one path and the cost of being wrong is measured in outage minutes.
- C) Say you do not know yet.
- D) Say you are investigating.

**Correct answer: B. Least effective: A**

**Explanation:** This is the discipline that most distinguishes reliable engineers under pressure. During an incident, information propagates fast and is acted on: a theory stated as a fact reaches a stakeholder update within minutes and becomes the organisation's understanding, and people stop looking elsewhere. Option B gives your lead everything they need — what is known, what is suspected, and what would settle it — which lets them decide whether to wait, parallelise or escalate. Option A is least effective and is genuinely tempting, because "I think it's the cache" sounds more useful than a hedge and is the kind of thing that gets repeated without the hedge. Options C and D are honest and withhold the theory, which is useful information provided it is labelled.

**Question 9 (harder) — A requirement that will harm users**

A requirement asks you to time out a user's session after five minutes of inactivity on a long benefits form. You believe many users will lose their work. What is the most effective response?

- A) Implement it as specified.
- B) Raise it before implementing, with the specific consequence — that a form taking most users longer than five minutes to complete will discard the work of anyone who pauses to find a document — and propose alternatives such as a longer timeout, a warning, or saving progress, while accepting that there may be a security reason you do not know about.
- C) Implement a longer timeout.
- D) Refuse to implement it.

**Correct answer: B. Least effective: C**

**Explanation:** You have noticed a real consequence and the requirement may still be correct, since session timeouts on services handling personal data are often set by security policy for reasons that are not visible in a ticket. Option B raises it before the work is done, which is when the observation is cheap to act on, states the consequence concretely rather than as a preference, offers alternatives — saving progress usually resolves the tension entirely — and acknowledges what you do not know. Option C is least effective: silently implementing something other than what was specified means the security requirement is unmet and nobody knows, which is worse than either honest option. Option A builds something that will discard people's work. Option D refuses a requirement that may be legitimate.

**Question 10 (harder) — Improving how the team works**

You notice the team spends about an hour a day on merge conflicts caused by long-lived branches. What is the most effective response?

- A) Manage your own branches better.
- B) Raise it in a retrospective with the observation and a specific proposal — smaller, shorter-lived branches, or merging main into feature branches daily — since an hour a day across the team is a substantial cost and a retrospective is the forum where the team can agree a change.
- C) Suggest a different branching strategy to the lead.
- D) Accept it; merge conflicts are normal.

**Correct answer: B. Least effective: D**

**Explanation:** Your role names helping to improve best practice guidelines, and this is what that looks like at your level: noticing a recurring cost, quantifying it, and taking it to the forum designed for exactly this. The quantification matters — "we lose about an hour a day to conflicts" is an argument where "branches are getting messy" is a grumble — and the specific proposal matters, because a retrospective item without one produces a discussion and no change. Option D is least effective, treating a measurable and fixable cost as a fact of life. Option A fixes your own contribution to a team problem. Option C is a reasonable route and skips the team, which for a change to shared working practice means it arrives as an instruction rather than an agreement.

**Question 11 (harder) — Reusing versus writing**

You need functionality that an existing internal library provides, but the library is poorly documented and you are not sure it does exactly what you need. Writing your own would take two days. What is the most effective approach?

- A) Write your own; two days is not long.
- B) Spend an hour establishing what the library actually does, since if it fits you save two days and avoid maintaining a second implementation — and if it does not, you have learned that cheaply and can write your own knowing why.
- C) Use the library and adapt around its behaviour.
- D) Ask the library's maintainers.

**Correct answer: B. Least effective: A**

**Explanation:** The asymmetry decides it: an hour of investigation either saves two days or costs an hour, which is a good bet in almost any circumstance. Option B also names the cost that developers systematically underestimate — a second implementation of something is not a two-day cost but a permanent one, since it must be maintained, tested and understood by everyone who encounters it, and internal duplication is how codebases become hard to change. Option A is least effective, taking the two-day cost and the permanent one without checking whether either was necessary. Option D is a good idea and usually slower than reading the code, which is available to you. Option C commits to the library before establishing that it fits, which risks adapting your design around behaviour you do not want.

**Question 12 (harder) — A shortcut nobody will see**

Under time pressure you implement something in a way you know is poor but that works. Nobody has noticed in review. What is the most effective response?

- A) Leave it; it works and was reviewed.
- B) Flag it yourself — in a comment, a ticket, or to the team — because you are the only person who knows, and the cost of a known shortcut is manageable while the cost of an unknown one is paid by whoever meets it next without context.
- C) Fix it now regardless of the deadline.
- D) Mention it if somebody asks.

**Correct answer: B. Least effective: A**

**Explanation:** The asymmetry here is about knowledge rather than quality: shortcuts under deadline are a normal part of the work and are not the problem. The problem is a shortcut only one person knows about, because the next developer meets code that looks deliberate, assumes there was a reason, and either works around it or replicates the pattern. Option B removes that asymmetry at almost no cost, and a comment saying "this does X the slow way because Y; see ticket Z" turns an invisible liability into a managed one. Option A is least effective, and "it was reviewed" is not the defence it appears to be, since review did not catch what only you know. Option C may be right if the shortcut is serious and treats a deadline as negotiable without asking. Option D leaves the disclosure to chance.

### Preparation tips

- **Report facts about code rather than judgements about authors.** It makes seniority irrelevant in review.
- **Distinguish an estimate from a guess, and propose a spike when it is a guess.**
- **Separate the code fix from the data remediation.** The second is usually larger.
- **Assess exposure before responding to a vulnerability report.**
- **Make a technical concern specific enough to be checked.** Numbers turn an opinion into a claim.
- **Label a theory as a theory during an incident.** It will be repeated without your hedge otherwise.
- **Quantify a recurring cost before proposing a change.**
- **Flag your own shortcuts.** A known one is manageable; an unknown one is not.

### Common pitfalls to avoid

- **Deferring to seniority in code review.**
- **Giving a number when you mean a guess.**
- **Fixing forward and leaving corrupted data.**
- **Accepting "tests next sprint".**
- **Suppressing a vulnerability alert before assessing exposure.**
- **Implementing something other than what was specified without saying so.**
- **Stating a theory as a cause during an incident.**
- **Writing your own version of something without spending an hour checking what exists.**

## Conclusion

You have reached the end, and it is worth pausing over what that involved: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a substantial piece of professional preparation and rather more than most people do.

Look back at the ground. In the cognitive section you established what a coverage figure does and does not prove, read an empty error log as a clue about where to look, reverted before diagnosing during an incident, treated "flaky" as a description rather than a diagnosis, and asked what an attacker controls. In the numeric section you learned what 99.9% costs in minutes, worked out why a 1% slow rate produces a 10% slow page, distrusted an average across instances, reported the complement at a high success rate, and multiplied a claimed throughput against a per-unit cost to find that it did not reconcile. In the verbal section you read "may", "should" and "must" as terms of art, declined to promise acceptance when a passage ruled out one rejection, spotted a deferral dressed as an exemption, and refused to mark True on a confounded finding. And in the situational judgement section you blocked a pull request from somebody senior, proposed a spike instead of a guess, assessed exposure before reacting to a scanner, and flagged your own shortcut because you were the only person who knew.

Two threads run through all of it. The first is about the limits of evidence: passing tests, empty logs, high coverage, clean scans and confident theories all say less than they appear to, and knowing exactly how much less is most of what makes debugging and design reliable. The second is about honest reporting of uncertainty — separating what you have verified from what you believe, an estimate from a guess, a theory from a cause. Neither is a coding skill and both are what distinguish developers whose judgement people rely on.

A word about where you are. Delivering components that form part of a product means somebody else builds on what you write, and code that is open by default means that somebody may be outside your organisation entirely. That raises the value of the unglamorous things — a clear interface, a name that means what it says, a comment explaining why rather than what, a test that would catch the regression. Those are the parts of the craft that compound.

If you want to build on this, a few things repay effort more than reading about them. Take a bug you fixed recently and write down what evidence you actually had at each step, and where you guessed. Look at a service's latency percentiles rather than its average and see whether the story changes. Read a specification you have implemented and count the things it did not settle that you decided silently. Pick a library your team wrote in-house and find out whether something existing would have done. And next time you take a shortcut, write the comment.

Finally, for the day itself. An assessment samples your reasoning on one morning under artificial conditions. It is not a verdict on your ability or your career. Read the stem twice, ask what the evidence can support, find the denominator, trust Cannot Say, and remember that the strongest answer is usually the one that is honest about what is not yet known.

Good luck. Go carefully, verify before you assert, and label the guesses.
