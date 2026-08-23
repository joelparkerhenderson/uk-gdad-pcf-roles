# Technical Writer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a technical writer in the UK Government Digital and Data profession — an expert practitioner with a deep understanding of technology and the needs of technologists. Your role description says you take a user-centred approach to explaining how to use government products and services to a technical audience, focusing on specialist content and software documentation, write blog posts for or on behalf of the technical community, and engage with the cross-government technical writing and content design communities.

That combination is unusual, and it is worth naming what makes it so. You write for readers who are frequently more expert than you in the subject and less expert in what they need to know, which inverts the usual content design relationship. A developer reading your API documentation does not need concepts explained; they need to find the one parameter that is behaving unexpectedly, at speed, while something is broken. Your users arrive impatient, competent and mid-task, and they will abandon your documentation for a search engine within seconds if it does not answer them. Almost everything in this guide is downstream of that.

You may be preparing for a formal assessment as part of a recruitment or promotion process, or you may want to sharpen the reasoning your job depends on. Psychometric assessment at this level is not an intelligence test and not a knowledge quiz. It is a standardised sample of the thinking a role demands, and for an expert practitioner that thinking has a particular character: you are rarely choosing between right and wrong and usually choosing between defensible options under incomplete information.

Three features of your role shape the questions here. First, your role names deep technical understanding — you are expected to read code, understand architecture and hold your own with engineers, which means several items assume technical reasoning rather than only editorial judgement. Second, you take responsibility for assuring the quality of more junior colleagues' content and for coaching them, so you will be asked to diagnose somebody else's work rather than only produce your own. Third, you are expected to think strategically about content life cycle: documentation that is correct today and unmaintained is a liability rather than an asset, and knowing which is which is a judgement your role requires.

The document has four main sections: a cognitive assessment, a numeric reasoning assessment, a verbal reasoning assessment, and a situational judgement assessment. Each provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Commit before reading each explanation. The explanations spend most of their words on why the near-miss options fail.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role genuinely uses, presented through practical materials rather than abstract puzzles. At your level the materials are documentation sets, API references, release notes, support tickets, analytics on developer portals, and content produced by colleagues you are coaching.

The format is typically an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group at a comparable level.

Three things distinguish this section for a technical writer.

The first is that your reasoning is frequently about a system rather than a text. A support ticket, a search log and an error message are evidence about where documentation is failing, and reading them well is closer to diagnosis than to editing.

The second is that correctness has a hard edge in your discipline. Content for a general audience can be imprecise and still helpful; a code sample with a wrong parameter name costs a developer twenty minutes and costs your documentation their trust permanently. Several items turn on the difference between content that is unclear and content that is wrong.

The third is maintenance. Documentation decays because the thing it describes changes, and a technical writer who does not think about that ships liabilities. Several questions ask you to weigh whether something should exist at all, given who will keep it current.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Diagnosing where documentation fails** maps to **User-centred content design**, where you show deep understanding of end-to-end journeys and identify where journey fixes or content improvements are needed.
- **Technical reasoning** maps to **Technical understanding (user-centred design)**, where you demonstrate knowledge of the technologies used to build and operate digital services.
- **Error checking** maps to **User-centred content design**, where you assure the quality of content from more junior colleagues.
- **Prioritisation** maps to **Agile working**, where you help teams prioritise work and adhere to agreed scope.
- **Life cycle reasoning** maps to **User-centred content design**, where you ensure content is regularly reviewed and evaluated.
- **Reasoning about audiences and positions** maps to **Stakeholder relationship management** and **User focus**.

### Practice questions

**Question 1 (easy) — Error checking a code sample**

A colleague's documentation includes: "Send a POST request to /v2/users with the header `Content-Type: application/json`. The response returns a `user_id` field." The API reference states the endpoint returns `userId`. What is the most important issue?

- A) The prose could be more concise.
- B) The field name in the documentation does not match the API — a developer copying `user_id` into their code will get an undefined value and will spend time debugging their own code before suspecting the documentation, which is the most expensive kind of documentation error.
- C) The header should be in a code block.
- D) The version number should be confirmed.

**Correct answer: B**

**Explanation:** A wrong field name is a different order of problem from an unclear sentence, and the reason is what happens next: the developer's code fails silently or returns undefined, they assume they have made a mistake, and they debug their own work for twenty minutes before considering that the documentation might be wrong. That sequence is what destroys trust in a documentation set, and once a developer has been burned they check the API response directly and stop reading you. Option B names this. Option D is a legitimate check and secondary. Options A and C are formatting improvements on a page containing a factual error, and prioritising them is the characteristic mistake of reviewing technical content as though it were prose.

**Question 2 (easy) — Deduction from a versioning rule**

A policy states: "Breaking changes may only be released in a new major version, unless the affected endpoint has been formally deprecated for at least six months." A team says: "We changed the response format of /v1/orders last week without a major version bump." Which must be true?

- A) The policy was breached.
- B) The endpoint had been deprecated for six months.
- C) Either the endpoint had been formally deprecated for at least six months, or the policy was breached — and separately, whether the change is breaking has not been established.
- D) The change was not breaking.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction — but this item has a second layer worth catching. The policy governs *breaking* changes, and "changed the response format" does not establish that the change was breaking: adding an optional field to a response is a format change and is not breaking, while removing or renaming one is. So two things are undetermined, and option C names both. Options A and B each assume a branch of the first question while taking the second for granted. Option D assumes the opposite. As a technical writer this distinction matters directly, because you will be asked to document the change and the answer determines whether it belongs in release notes as a note or as a migration guide.

**Question 3 (moderate) — Diagnosing from support tickets**

The top three support tickets for a developer API are: "How do I authenticate?", "What does error 429 mean?" and "Why is my request timing out?" All three are documented. What is the strongest analysis?

- A) Developers are not reading the documentation.
- B) Three heavily documented topics generating the most tickets suggests the documentation exists but is not findable at the moment of need, or is present but does not answer the specific question asked — so the diagnostic step is to look at what the tickets actually say and where the developers had been looking.
- C) The documentation should be rewritten.
- D) Support should point people to the documentation.

**Correct answer: B**

**Explanation:** "It is documented" and "developers can find and use it" are different claims, and the gap between them is where most technical documentation fails. The three topics named have a common character worth noticing: all are things a developer hits mid-task, under time pressure, usually in the middle of an integration — which means the documentation may be perfectly good and located somewhere nobody reaches from an error message. Option B names the two realistic causes and the cheap diagnostic. Option A blames users, which is both unhelpful and usually wrong. Option C rewrites content that may be correct. Option D treats the symptom, and doing so permanently obscures the problem because tickets stop being visible without the underlying difficulty stopping.

**Question 4 (moderate) — Prioritising documentation work**

You have capacity for one substantial piece of work this quarter:

1. A new API goes to public beta next month with no reference documentation.
2. An existing guide is out of date in three places, generating occasional confusion.
3. A tutorial for a deprecated feature needs rewriting.
4. The team wants a style guide for engineering-authored content.

Which is strongest, and why?

- A) Item 2, because inaccurate documentation actively misleads.
- B) Item 1, because an API going to public beta without reference documentation is unusable by its intended audience, and the window to produce it before external developers form an impression closes next month.
- C) Item 4, because it would improve everything.
- D) Item 3, because tutorials are high-value.

**Correct answer: B**

**Explanation:** The right frame is what your input can still change and what happens if it does not. An API released to public beta without reference documentation is not partially usable — an external developer cannot integrate without knowing the endpoints, parameters and error codes, so the release is effectively blocked for its audience while appearing to have happened. The window matters too: first impressions of a developer product are formed at first contact and are expensive to change. Item 2 is genuinely harmful and generating occasional confusion rather than blocking anyone, so it goes next. Item 3 is documentation for a deprecated feature, which raises whether it should be rewritten at all rather than marked deprecated and left. Item 4 has real leverage and no deadline. Option A ranks harm correctly and misses that item 1 is a total barrier rather than a partial one.

**Question 5 (moderate) — Content that should not exist**

A twelve-page tutorial explains how to work around a known limitation in a service. Engineering plans to remove the limitation in two months. What is the strongest recommendation?

- A) Keep the tutorial; users need it now.
- B) Keep it with a prominent, dated note that the limitation is being removed and the workaround will become unnecessary, and plan its retirement — because an undated workaround guide outlives the problem it solves and then actively misleads people into doing something unnecessary and probably harmful.
- C) Remove it now.
- D) Rewrite it more concisely.

**Correct answer: B**

**Explanation:** Workaround documentation has a specific failure mode: it is written under pressure, it solves a real problem, and then the problem goes away and nobody remembers the page exists. Two years later a developer follows a twelve-page workaround for a limitation that was fixed, which is worse than having no documentation because it costs them a day and produces code containing an unnecessary and probably fragile construction. Option B keeps it useful now and builds in the retirement, which is what your role means by ensuring content is regularly reviewed and contributing to continuous improvement. Option A ignores the life cycle entirely. Option C removes something people currently need. Option D improves the prose of a page whose real problem is temporal.

**Question 6 (moderate) — Assuring a colleague's work**

A junior colleague's guide is well written, clearly structured, and describes a configuration process that you know changed three months ago. What is the most useful feedback?

- A) Note the factual error and ask them to correct it.
- B) Note the error, and use it to establish how they verified the process — because a well-written guide describing something that no longer works suggests they wrote from an existing source rather than performing the steps, and the habit matters far more than this instance.
- C) Correct it yourself.
- D) Praise the structure and mention the error briefly.

**Correct answer: B**

**Explanation:** The instructive feature is the combination: well written, well structured, and wrong. That combination almost always means the writer worked from an older document or a colleague's description rather than following the process themselves — and if that is the habit, every guide they produce carries the same risk regardless of how carefully they write. Option B addresses the habit, which is what your role means by coaching and guiding junior colleagues to improve rather than correcting their output. The remedy is simple to state and hard to skip once named: follow the steps yourself, on a real system, before publishing. Option A fixes the instance. Option C removes the learning entirely and makes you a permanent checker. Option D softens the point until it is not made.

**Question 7 (moderate) — Writing for a technical audience**

You are documenting an authentication flow. Which approach best serves a developer audience?

- A) A prose explanation of the concepts, followed by examples.
- B) A working code sample first, with the minimum necessary explanation around it and links to conceptual detail — because a developer arriving at authentication documentation almost always wants to make a request work, and will read the concepts afterwards if at all.
- C) A comprehensive conceptual guide covering all authentication options.
- D) A step-by-step tutorial with screenshots.

**Correct answer: B**

**Explanation:** The audience inversion is what decides this. A general-audience reader needs orientation before instruction; a developer arriving at authentication documentation is mid-integration, has a specific goal, and is measuring your page against the time cost of just reading the source. A working sample they can copy, run and modify serves that directly, and the conceptual material is genuinely useful to the smaller number who need it — after they have something working. Option B also reflects how developers actually learn a new API, which is by making one call succeed and then expanding. Option A inverts the order for this audience. Option C is the comprehensive guide that gets skimmed for a code block. Option D uses a format suited to interface walkthroughs rather than to code.

**Question 8 (harder) — A technically ambiguous instruction**

Documentation states: "Set the timeout value appropriately for your use case." What is wrong, and what should it say?

- A) Nothing; timeout values are context-dependent.
- B) It transfers a decision to the reader without giving them what they need to make it — the useful version states the default, the units, the practical range, what happens at each extreme, and a recommendation for the common case, since "appropriately" is only meaningful to somebody who already knows the answer.
- C) It should specify a value.
- D) It should link to the configuration reference.

**Correct answer: B**

**Explanation:** "Appropriately" is the characteristic failure of technical documentation written by somebody who knows the system: it is true, it is unfalsifiable, and it helps only readers who did not need the sentence. Option B names what a reader actually requires to make the decision, and the list matters — units are omitted surprisingly often and cause real errors, and describing what happens at each extreme is what converts a number into a judgement the reader can make. Option A defends the sentence on the grounds that make it useless, since context-dependence is precisely why the reader needs the parameters of the decision. Option C over-corrects: a single prescribed value would be wrong for many readers. Option D sends the reader elsewhere for information the sentence should carry.

**Question 9 (harder) — Reading analytics for a documentation site**

A developer documentation site shows: high traffic to the getting-started page, low traffic to the conceptual overview, and very high traffic to a single error-code reference page. What is the strongest interpretation?

- A) The conceptual overview should be promoted.
- B) The pattern is what you would expect from a working developer audience — they start with getting-started, skip concepts, and arrive at the error reference when something breaks — but very high traffic to one error code specifically suggests either that error is unusually common or its documentation is unusually unhelpful, and that is the page worth investigating.
- C) The conceptual overview should be removed.
- D) The error page is working well.

**Correct answer: B**

**Explanation:** Two readings are combined here and both matter. The overall shape is normal and should not be treated as a problem: developers genuinely do skip conceptual material and arrive at error references under duress, and low traffic to concepts is not evidence that they are badly written. But traffic concentrated on one error code within that pattern is a signal, and it has two possible causes with different remedies — a common error, which points at the product, or an inadequate explanation, which points at the page and is often visible in whether people leave the page and search again. Option B holds both. Option D reads high traffic as success, which for an error page is exactly backwards. Options A and C both treat a normal pattern as a defect.

**Question 10 (harder) — Documentation and a product decision**

Engineering proposes an API change that would be simpler to implement but would require every existing integrator to change their code. You are asked only to document it. What is the strongest response?

- A) Document it as asked.
- B) Document it, and separately flag that the change requires action from every existing integrator — which makes it a breaking change with migration, deprecation-period and communication implications beyond documentation, and is worth confirming has been considered rather than assuming it has.
- C) Refuse to document it until the decision is reviewed.
- D) Document it with a warning to readers.

**Correct answer: B**

**Explanation:** You have noticed something with consequences beyond your task, and the useful contribution is to surface it without overstepping. A change requiring every integrator to alter their code is a breaking change whatever it is called internally, and breaking changes carry obligations — a deprecation period, a migration path, direct communication to known integrators — that documentation cannot substitute for. Option B raises it as a question rather than an objection, which is both accurate to your position and far more likely to be heard. It is entirely possible the team has considered all of this; it is also common for the person writing the documentation to be the first to think about the reader. Option A is a legitimate reading of the instruction and misses the contribution. Option C exceeds your remit. Option D warns users about a decision that could still be changed.

**Question 11 (harder) — Content life cycle**

Your documentation set contains 340 pages. Analytics show 40 pages account for 85% of traffic, and 120 pages have had no visits in a year. What is the strongest recommendation?

- A) Archive the 120 unvisited pages.
- B) Investigate before acting: some unvisited pages are genuinely obsolete, some are findable only by people who need them rarely and urgently — a disaster recovery procedure, say — and some are unvisited because they cannot be found, so the traffic figure alone does not distinguish content nobody needs from content nobody can reach.
- C) Focus maintenance effort on the 40 high-traffic pages.
- D) Keep everything; storage is free.

**Correct answer: B**

**Explanation:** Zero traffic is ambiguous in a way that makes acting on it directly hazardous, and the three cases have opposite remedies. Genuinely obsolete content should be archived. Rarely-needed critical content — recovery procedures, incident runbooks, migration guides for old versions — is *supposed* to have low traffic and is catastrophic to lose. And content nobody can find looks identical in the analytics to content nobody wants, while needing promotion rather than deletion. Option B distinguishes them. Option A treats a low-traffic disaster recovery page as dead weight, which is the error that gets discovered during a disaster. Option C is a sensible allocation of maintenance effort and answers a different question. Option D ignores that unmaintained content is a liability rather than a neutral.

**Question 12 (harder) — A flaw in your own work**

You realise that a code sample you published two months ago contains a parameter that works but is deprecated, and will stop working in the next major release. What should you do?

- A) Update it in the next review cycle.
- B) Update it now, and check whether the same deprecated parameter appears in other samples across the documentation set — because a pattern you used once you have probably used repeatedly, and every integrator who copied it will break at the same moment.
- C) Update it quietly.
- D) Add a note that the parameter is deprecated.

**Correct answer: B**

**Explanation:** Code samples are copied, which is what makes an error in one different from an error in prose: developers do not read your sample and paraphrase it, they paste it, so a deprecated parameter in a published sample is now in an unknown number of production codebases with a scheduled failure date. Option B fixes it and asks the question that matters at your level — a writer who used a parameter once has usually used it consistently, so the exposure is probably larger than the single page. Option D is a reasonable addition and leaves the sample propagating the problem to anyone who copies before reading. Option A defers something with a known failure date. Option C corrects the page and leaves the pattern unexamined.

### Preparation tips

- **Distinguish unclear from wrong.** A wrong field name costs a developer their trust in the whole set.
- **Follow the steps yourself before publishing.** Well-written and wrong usually means written from a source.
- **Read support tickets and search logs as evidence about findability, not about readers.**
- **Ask who will keep this current.** Documentation nobody maintains is a liability.
- **Lead with the working example for a developer audience.** Concepts come after something works.
- **Replace "appropriately" with the parameters of the decision.** Default, units, range, consequences, recommendation.
- **Treat zero traffic as ambiguous.** Obsolete, rarely-needed and unfindable look identical.
- **Check whether an error in one sample appears in others.** Samples get copied.

### Common pitfalls to avoid

- **Reviewing technical content as prose.** Formatting comments on a page with a factual error.
- **Reading "changed the format" as "breaking change".** Additions are not breaking.
- **Blaming readers for not finding documentation.**
- **Rewriting content whose problem is findability.**
- **Treating high traffic to an error page as success.**
- **Archiving low-traffic content without asking why it is low.**
- **Leaving workaround guides undated.** They outlive the problem and then mislead.
- **Correcting a junior colleague's instance rather than their method.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle the quantitative material your role produces and consumes. For a technical writer that material is unusually varied: documentation analytics, search logs, support ticket volumes, API usage figures, error rates, and the numbers inside the content itself — rate limits, timeouts, payload sizes, version numbers and retention periods.

That last category deserves emphasis, because it is where numerical care in your discipline differs from most. A number in your documentation is not a summary or an argument; it is an instruction somebody will implement. A rate limit stated as 100 requests per minute when it is 100 per hour will cause every integrator who reads it to build something that fails in production, and unlike a vague sentence it will fail silently until it does not.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a table, chart or paragraph of figures with a multiple-choice question. Calculators are usually provided.

Four habits carry the load. Establish what the question asks before looking at the data. Identify the denominator and the population it represents. Estimate, calculate, compare. And sanity-check against the world — which for you includes checking whether a documented figure is physically plausible.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Accuracy with figures in content** maps to **Technical understanding (user-centred design)**, where knowledge of the technologies is what lets you notice an implausible value.
- **Reading documentation analytics** maps to **User-centred content design**, where you ensure content is reviewed and evaluated.
- **Rate and limit arithmetic** maps to **Technical understanding**, since documenting a system means representing its constraints correctly.
- **Prioritising by impact** maps to **Agile working**, where you help teams prioritise and adhere to scope.
- **Presenting figures to stakeholders** maps to **Stakeholder relationship management**.
- **Evaluating content performance** maps to **Strategic thinking**, where directing evaluation of strategies means knowing what the numbers can support.

### Practice questions

**Question 1 (easy) — Rate limit arithmetic**

An API allows 5,000 requests per hour. A client sends requests at a steady rate. What is the maximum sustainable rate per minute?

- A) 50
- B) 83
- C) 300
- D) 500

**Correct answer: B**

**Explanation:** 5,000 ÷ 60 = 83.3, so about 83 requests per minute, giving B. Option A divides by 100; option C multiplies incorrectly. The reason to be careful is what you would write: documenting the limit as "about 83 per minute" is helpful, and documenting it as "83 per minute" invites an integrator to build a client sending exactly 83 every minute, which will exceed 5,000 in an hour by 20 requests and get rate-limited intermittently in a way that is genuinely hard to debug. The honest documentation states the actual limit and its window — 5,000 per hour — and notes the per-minute figure as approximate guidance, because the limit is enforced on the hour and not on the minute.

**Question 2 (easy) — Percentage of traffic**

A documentation site has 340 pages. Forty pages account for 68,000 of 80,000 monthly visits. What proportion of traffic do those pages carry?

- A) 68%
- B) 75%
- C) 85%
- D) 12%

**Correct answer: C**

**Explanation:** 68,000 ÷ 80,000 = 0.85, so 85%, giving C. Option A misreads the raw figure as a percentage. The distribution is worth registering: 12% of pages carrying 85% of traffic is a normal and steep pattern for technical documentation, and it has a direct implication for how you spend maintenance effort. It also has a less obvious one — the long tail is not automatically waste, because a rarely-read migration guide may be critical to the few who need it, so the distribution tells you where to focus attention rather than what to delete.

**Question 3 (easy) — Support ticket reduction**

Before a documentation change, a topic generated 240 support tickets a month. After, it generates 180. What is the reduction, and what should you check?

- A) 25% reduction, and check whether ticket volume overall fell in the same period
- B) 33% reduction
- C) 60 tickets, which is the meaningful figure
- D) 25% reduction, demonstrating the change worked

**Correct answer: A**

**Explanation:** The difference is 60, and 60 ÷ 240 = 0.25, a 25% reduction — so B miscalculates by dividing by the new figure. Between A and D the check decides it, and it is the right one: if total ticket volume fell 25% across all topics in the same period, your documentation change explains nothing and something else did, perhaps a quieter month or a change in how tickets are categorised. Establishing that takes one query and is the difference between a claim you can defend and one that collapses the first time somebody looks. Option C is the raw figure without the comparison that makes it interpretable.

**Question 4 (easy) — Payload size**

Documentation states a maximum request payload of 2 MB. A developer asks how many records of approximately 4 KB they can send in one request. What is the best answer?

- A) About 500
- B) About 500, with the caveat that the limit applies to the encoded request including overhead, so the practical figure is somewhat lower and they should not design for the maximum
- C) About 2,000
- D) About 50

**Correct answer: B**

**Explanation:** 2 MB is roughly 2,000 KB, and 2,000 ÷ 4 = 500 records — so the arithmetic gives A and the useful answer is B. The caveat is what makes it good documentation: the limit applies to the whole encoded request, which includes headers, JSON structural characters, field names repeated per record and any encoding expansion, so a client designed to send exactly 500 will intermittently exceed the limit as record sizes vary. Advising against designing for the maximum is the kind of practical guidance that distinguishes documentation written by somebody who has integrated with an API from documentation written by somebody transcribing a specification.

**Question 5 (moderate) — Comparing documentation versions**

Version A of a guide had 12,000 visits with 3,600 users reaching the next step. Version B had 8,000 visits with 3,200 reaching the next step. Which performed better?

- A) Version A, with more users progressing.
- B) Version B, with a 40% progression rate against Version A's 30%.
- C) They are equivalent.
- D) Version A, with more traffic.

**Correct answer: B**

**Explanation:** Convert to rates because the traffic differs. Version A: 3,600 ÷ 12,000 = 30%. Version B: 3,200 ÷ 8,000 = 40%. Version B performs better per reader, giving B. Options A and D compare raw counts across different-sized groups, which is the standard error. Worth noting a genuine complication in the interpretation: the traffic difference is itself interesting, and if Version B has lower traffic because it is harder to find, then a better page is reaching fewer people — which would make the right action promoting it rather than congratulating yourself. Rate is the right comparison and it is not the whole answer.

**Question 6 (moderate) — Estimating documentation effort**

An API has 40 endpoints. A colleague estimates 90 minutes each for reference documentation, giving 60 hours. What is the most useful thing to establish?

- A) Whether 90 minutes is realistic.
- B) Whether the endpoints share request and response structures — because if 30 of the 40 follow two or three common patterns, the work is closer to documenting the patterns plus 40 short variations, which is a different and much smaller job than 40 independent efforts.
- C) The total, which is 60 hours.
- D) Whether the colleague has done this before.

**Correct answer: B**

**Explanation:** The estimate treats endpoints as independent, and REST APIs almost never are: a well-designed one has a handful of resource patterns with consistent authentication, pagination, filtering and error behaviour, so the substantial work is documenting those once and then the specifics of each endpoint briefly. Option B establishes that, and it can move the estimate by more than half in either direction — an API with forty genuinely idiosyncratic endpoints is a much bigger job and a much worse API. Option A asks about the rate rather than the structure, which is the less consequential half. Option C computes what the estimate implies without questioning its basis.

**Question 7 (moderate) — Percentage change**

Monthly visits to a getting-started guide rose from 4,800 to 6,000 after it was linked from the API console. What is the increase?

- A) 20%
- B) 25%
- C) 80%
- D) 125%

**Correct answer: B**

**Explanation:** The difference is 1,200, and 1,200 ÷ 4,800 = 0.25, a 25% increase, giving B. Option A is 1,200 ÷ 6,000, dividing by the new figure — the most common error and one that under-reports every improvement. Option D expresses the new figure as a proportion of the old. The rule: for percentage change, the denominator is where you started. This particular figure is also worth interpreting rather than only reporting: a 25% rise from adding one link suggests findability was the constraint rather than the content, which is a useful thing to know about the rest of the documentation set.

**Question 8 (moderate) — Reading a search log**

The top five internal searches on a developer portal are: "authentication" 1,400; "rate limit" 900; "webhook" 700; "error 429" 600; "sandbox" 400. What is the strongest interpretation?

- A) These are the five most important topics.
- B) Internal search is where people go when navigation failed, so these are the five topics developers most often cannot find by browsing — and the presence of "error 429" alongside "rate limit" suggests they are the same underlying need arriving by two routes, which is a case for linking them or merging them.
- C) The site search is working well.
- D) These topics need more content.

**Correct answer: B**

**Explanation:** Search volume measures navigation failure rather than importance, which inverts the naive reading. Option B says so and adds the observation that makes the data actionable: 429 *is* the rate limit error, so 1,500 searches are arriving at one topic by two different vocabularies — one from people who know the concept and one from people who have hit the error and are searching the number. Documentation that does not connect the two leaves half of them searching again. Option A reads the log as a popularity ranking. Option C treats search volume as a success measure. Option D assumes the content is missing when it is more likely unfindable, which is a different and cheaper fix.

**Question 9 (moderate) — Timeout arithmetic**

A service has a 30-second timeout. A retry policy uses exponential backoff starting at 1 second and doubling. How many retries fit within the timeout?

- A) 3
- B) 4
- C) 5
- D) 6

**Correct answer: B**

**Explanation:** The waits are 1, 2, 4, 8 and 16 seconds. Cumulatively: after one retry 1 second, after two 3, after three 7, after four 15, after five 31 — which exceeds 30. So four retries fit within the timeout and the fifth does not, giving B. The arithmetic matters because this is exactly the sort of thing documentation gets wrong: stating "retry up to five times with exponential backoff" alongside a 30-second timeout describes a policy that cannot complete, and every developer implementing it will hit the timeout on the last retry and file a ticket. Being able to check that the numbers in a document are mutually consistent is a distinctively technical-writing skill and it catches real errors.

**Question 10 (harder) — A metric that misleads**

A documentation site reports "average time on page: 4 minutes" and a colleague reads this as good engagement. What is the strongest observation?

- A) Four minutes is good.
- B) Time on page has no direction for technical documentation — a developer who finds the answer in ten seconds and leaves is a success, and one who spends four minutes because the page is confusing is a failure, so a high average is as consistent with difficulty as with engagement, and the useful measures are whether people progress, search again, or file tickets.
- C) The pages should be shorter.
- D) The figure should be broken down by page.

**Correct answer: B**

**Explanation:** Time on page is misleading everywhere and especially here, because the ideal interaction with reference documentation is brief. A developer who lands on your error-code page, reads one line and returns to their editor has had a perfect experience, and it registers as a bounce with low dwell. Option B names the ambiguity and identifies measures with direction — progression to the next step, repeat searching, and ticket volume all move in an interpretable way. Option D is a real improvement and reports the same directionless quantity more granularly. Option C acts on one interpretation. At your level the useful move is to say this before the metric becomes the target, because a documentation team optimising for dwell time will make things worse very efficiently.

**Question 11 (harder) — Percentage points and relative change**

The proportion of developers completing an integration within a day rose from 40% to 52% after a documentation change. Which statement is accurate?

- A) A 12% increase.
- B) A 12 percentage point increase, equivalent to a 30% relative increase.
- C) A 30 percentage point increase.
- D) A 23% increase.

**Correct answer: B**

**Explanation:** The arithmetic gap is 52 − 40 = 12 percentage points. The relative increase is 12 ÷ 40 = 0.3, or 30%. Option B labels both. Option A is ambiguous and generally read as relative. Option C misapplies the label. Option D divides by the new value. This matters for you specifically because technical writers are frequently asked to demonstrate the value of documentation work, and the temptation to report the larger-sounding figure is real. Giving both is the honest practice and the safer one — a stakeholder who later notices the flattering figure was selected will discount your next claim, and documentation value claims are already treated with more scepticism than most.

**Question 12 (harder) — A figure in the content**

A draft states: "The endpoint returns up to 1,000 results per page, with a maximum of 50 pages." A colleague asks whether that means 50,000 results. What should you check?

- A) Nothing; the arithmetic is straightforward.
- B) Whether the 50-page maximum is a hard cap on total retrievable results or a pagination limit that resets — because those give completely different answers to "can I retrieve my 80,000 records", and the documentation as written does not distinguish them.
- C) Whether 1,000 is the default or the maximum.
- D) Whether the pages are zero-indexed.

**Correct answer: B**

**Explanation:** The arithmetic is trivial and the semantics are not, which is the point. If the 50-page limit is a hard cap, the maximum retrievable set is 50,000 records and a developer with 80,000 cannot get them all through this endpoint — a substantial constraint they need to know about before designing anything. If pagination resets with a cursor or a filter, the cap is per query and the full set is retrievable in batches. Those are opposite answers to the only question a developer actually has, and the sentence as drafted supports both. Option C is a real ambiguity and a smaller one. Option D matters for the first request and not for the capability question. Option A treats a semantic ambiguity as an arithmetic one, which is the characteristic error when technical content is reviewed for correctness of numbers rather than correctness of meaning.

### Preparation tips

- **Check that numbers in a document are mutually consistent.** Retry policies and timeouts frequently contradict each other.
- **State limits in the units they are enforced in.** Converting a per-hour limit to per-minute invites intermittent failures.
- **Warn against designing for the maximum.** Encoded overhead makes the stated limit optimistic.
- **Read search volume as navigation failure, not importance.**
- **Look for two vocabularies for one need.** "Rate limit" and "error 429" are the same question.
- **Compare versions by rate, and then ask why the traffic differed.**
- **Distrust time on page.** For reference documentation, brief is the goal.
- **Ask whether endpoints share structure before accepting an estimate.**

### Common pitfalls to avoid

- **Dividing by the new figure in percentage change.**
- **Comparing raw counts across pages with different traffic.**
- **Reading a search log as a popularity ranking.**
- **Treating high dwell time as engagement.**
- **Claiming a documentation improvement without checking the baseline moved.**
- **Estimating endpoint documentation as independent units.**
- **Reviewing numbers for arithmetic and missing the semantic ambiguity.**
- **Reporting only the flattering framing.** Documentation value claims already attract scepticism.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. For your discipline it is close to the job itself: you spend your working life reading specifications, RFCs, engineering tickets, code comments and API contracts, and turning them into something a reader can act on. Getting that wrong in either direction is serious — understate a constraint and integrators build something that breaks; overstate one and they build defensively around a limit that does not exist.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. True means the statement follows necessarily. False means the passage contradicts it. Cannot Say means the passage neither establishes nor excludes it. Alongside these come comprehension items, main-point items, and questions asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone. Your professional knowledge must be set aside, and this is harder for you than for most: you know how these systems usually work, and the temptation to supply the behaviour you would expect rather than the one described is exactly what produces documentation asserting things the specification never said.

Cannot Say deserves particular attention. Technical writers avoid it because a reader asking "does this endpoint support filtering?" wants an answer, and "the specification does not say" feels like a failure. In practice it is frequently the correct and most useful answer, because it identifies a gap somebody needs to close before you document it.

Small words carry the load. "May" and "must" have specific force in specification prose. "Should" means something between them. "Or" offers alternatives. And a specification's silence is not permission.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading specifications precisely** maps to **Technical understanding (user-centred design)**.
- **Separating statement from inference** maps to **User-centred content design**, where content must be traceable to what a source actually says.
- **Identifying the main point** maps to your core task of turning specification prose into something usable.
- **Handling qualified language** maps to **Technical understanding**, where "may" and "must" carry defined weight in technical documents.
- **Reading for absence** maps to **User-centred content design**, where noticing a specification never states an error condition is what stops you inventing one.
- **Reading stakeholder correspondence** maps to **Stakeholder relationship management**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Clients must include an Authorization header on all requests to protected endpoints. Clients may include an Idempotency-Key header on POST requests; where present, the server will return the original response for any repeated request with the same key within 24 hours. Servers must reject requests exceeding 2 MB with a 413 response. Clients should implement exponential backoff on 429 responses."

**Question 1 (easy)** — Statement: "Clients must include an Idempotency-Key header on POST requests." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says clients *may* include the header — it is optional. The statement's "must" contradicts that, so False. In specification prose "may", "should" and "must" are terms of art with defined force, and this passage uses all three deliberately: the Authorization header is mandatory, idempotency keys are optional, and backoff is recommended. A technical writer who flattens those into a single register produces documentation that either over-constrains integrators or under-warns them, and both cost trust. Reading them exactly is the foundational skill of the discipline.

**Question 2 (easy)** — Statement: "A repeated POST with the same Idempotency-Key after 30 hours will return the original response." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage guarantees the original response for repeats *within 24 hours*. Thirty hours falls outside that window, so the guarantee does not apply and the statement is contradicted. False. Note what the passage does not say: it does not state what happens after 24 hours, so the request might be processed as new, might be rejected, or might behave in some other way. That is worth registering because it is exactly the sort of thing you would need to establish before documenting, and the honest draft says the guarantee holds for 24 hours rather than inventing the behaviour beyond it.

**Question 3 (moderate)** — Statement: "A client that does not implement exponential backoff is non-compliant." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says clients *should* implement exponential backoff. In specification usage "should" indicates a strong recommendation that may be departed from for good reason, not a requirement — so a client without it is not compliant with the recommendation and is not non-compliant with the specification. The statement asserts non-compliance, which the passage does not support, so False. This distinction is one integrators care about, because "should" tells them the behaviour is expected and they will not be rejected for omitting it, while "must" tells them their client will break. Documentation that renders both as "you need to" removes information the reader needs.

**Question 4 (harder)** — Statement: "A 1.9 MB request will be accepted." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage requires servers to reject requests *exceeding* 2 MB, so a 1.9 MB request is not rejected on size grounds. But acceptance depends on everything else — authorisation, validity, rate limits, and any condition the passage does not mention — and the passage establishes only that one particular rejection does not apply. Cannot Say. This is the distinction between "will not be rejected for this reason" and "will be accepted", and it matters in documentation because writing "requests under 2 MB are accepted" makes a promise the specification does not, which an integrator will believe until a valid-sized request fails validation and they conclude your documentation is unreliable.

*Passage B — for Questions 5 to 8*

"The review of the developer portal found that teams publishing reference documentation alongside code releases reported fewer integration support tickets than teams publishing separately. The review notes that the teams publishing alongside releases were also those with dedicated technical writers. The review did not assess documentation accuracy. It recommends that the portal team consider whether alongside-release publishing should be standard."

**Question 5 (easy)** — Statement: "Teams publishing documentation alongside releases reported fewer integration tickets." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence states this directly and the statement restates it without addition. True. Note the passage's careful "reported fewer" rather than "had fewer", and the statement respects it. Answer quickly and bank the time for harder items.

**Question 6 (moderate)** — Statement: "Publishing alongside releases reduces support tickets." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports an association and then flags that the same teams had dedicated technical writers — which is a substantial confound, since a team with a dedicated writer would be expected to produce better documentation regardless of when it publishes. So the fall in tickets may be attributable to the writer, the timing, both, or something else the review did not name. Cannot Say. This is the trap for someone in your position, because "publishing alongside releases reduces tickets" is a claim you would like to be true and would cite when arguing for the practice. The stronger argument is available and honest: documentation published after a release is documentation integrators did not have when they needed it, which is a reason on its own without needing the ticket data to carry it.

**Question 7 (moderate)** — Statement: "The documentation produced alongside releases was more accurate." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage says explicitly that the review did not assess accuracy. Declared silence establishes nothing, so Cannot Say. The distinction matters in your field more than in most: documentation published under release pressure could plausibly be *less* accurate while generating fewer tickets, if it arrives in time to prevent the confused questions that a later and better document would have answered. Fewer tickets and better documentation are different things, and a review that measured one and not the other has told you about one.

**Question 8 (harder)** — Statement: "The review recommends making alongside-release publishing standard." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The review recommends that the portal team *consider whether* it should be standard — a recommendation to evaluate, including the possibility of deciding against. The statement asserts a recommendation to adopt, which was not made, so False rather than Cannot Say: the passage tells you what was recommended and it was something different. This pervades review prose, and technical writers are unusually likely to be the person who writes the record of what a review said — which makes reading it precisely a professional obligation rather than a test technique.

*Passage C — for Questions 9 to 12*

"Documentation for a public API must state the endpoint, method, required and optional parameters with types, the response schema, and all error codes the endpoint can return. Where an endpoint is deprecated, the documentation must state the deprecation date and the recommended alternative. Code samples must be executable as written against the documented version. Documentation must be reviewed whenever the endpoint changes, and at least annually."

**Question 9 (easy)** — Statement: "Documentation must list all error codes an endpoint can return." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence requires all error codes the endpoint can return. The statement restates that, so True. Answer quickly. It is worth noting why the requirement is stated so strongly: an undocumented error code is one an integrator cannot handle, and the failure mode is a client that works in testing and falls over in production when an unanticipated response arrives. This is among the most commonly incomplete sections of API documentation, usually because the writer documents the errors they encountered rather than the ones the endpoint can produce.

**Question 10 (moderate)** — Statement: "A code sample that works against the current version but not the documented version satisfies the requirement." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The requirement is that samples are executable as written *against the documented version*. A sample working only against a different version fails that, so the statement is contradicted. False. The scenario is realistic and worth recognising: documentation for version 2 gets updated with samples tested against version 3 because that is what the writer had running locally, and every integrator still on version 2 — which is the audience for that documentation — finds the sample fails. The requirement names the documented version specifically because this is the error it exists to prevent.

**Question 11 (harder)** — Statement: "Documentation reviewed eleven months ago, with no endpoint changes since, is compliant." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The requirement has two limbs: review whenever the endpoint changes, and at least annually. With no changes, the first limb is not triggered, and eleven months is within the annual requirement, so both are satisfied and the statement follows. True. Contrast this with the structure that produces a Cannot Say — if the passage had not told you whether the endpoint had changed, the case would be undetermined. Here the stem supplies both facts, so the compound condition can be fully evaluated. Reading which facts you have been given, rather than assuming a compound condition is always indeterminate, is what the item tests.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) Documentation must list all error codes.
- B) API documentation must be complete, executable and current — specifying the interface fully including errors, giving deprecation dates and alternatives, containing samples that actually run against the version documented, and being reviewed on change and at least annually.
- C) Code samples must be executable.
- D) Documentation must be reviewed annually.

**Correct answer: B**

**Explanation:** The main point must cover the whole passage while adding nothing. Options A, C and D are each true of one provision and silent on the rest, and D also drops the change-triggered review. Option B captures the four requirements and names the logic joining them: an integrator relies on the documentation as a contract, so it must describe the interface fully, work when followed, and not describe a system that no longer exists. Note that B preserves "against the version documented" and both review triggers — a summary dropping either is one a colleague could act on and still fail the requirement.

### Preparation tips

- **Read "may", "should" and "must" as terms of art.** Flattening them removes information integrators need.
- **Distinguish "will not be rejected for this reason" from "will be accepted".**
- **Treat a specification's silence as a gap to close, not a behaviour to infer.**
- **Trust Cannot Say.** It identifies the question somebody needs to answer before you document.
- **Watch compound conditions and check which facts you have.** Not every compound is indeterminate.
- **Separate "consider whether X" from "recommend X".** You may be writing the record.
- **Keep version qualifiers in summaries.** "Executable" and "executable against the documented version" differ.
- **Notice when an argument you want to make rests on a confounded finding.** The honest argument is usually available.

### Common pitfalls to avoid

- **Supplying the behaviour you would expect rather than the one described.** The characteristic technical writer's error.
- **Rendering "should" as a requirement.**
- **Documenting behaviour outside a stated window.**
- **Promising acceptance when a passage only rules out one rejection.**
- **Marking True on a claim that would support a practice you favour.**
- **Treating a proxy outcome as the thing itself.** Fewer tickets is not better documentation.
- **Testing samples against the version you happen to be running.**
- **Documenting the errors you encountered rather than the ones the endpoint returns.**

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to parse and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures whether your judgement matches what the profession considers good practice at your level. Your role description places you as an expert practitioner with deep technical understanding, writing for technologists, assuring the quality of more junior colleagues' content, coaching them, delivering through others, and engaging with the cross-government community.

Four principles carry most scenarios, and two are specific to your discipline.

Your readers are experts under time pressure. They arrive mid-task, competent, and impatient, and they will leave for the source code or a search engine within seconds. Options that respect that — leading with the working thing, answering the question asked — beat options that are thorough.

Accuracy is not negotiable in the way clarity is. A confusing sentence costs a reader a minute; a wrong parameter costs them twenty and costs your documentation their trust permanently. When those two pull against each other, accuracy wins.

Work through engineers rather than around them. You depend on people who have the knowledge and rarely the time, and almost every scenario in this section is really about how you get information out of somebody who would rather be coding.

Think about who maintains it. Documentation you write and nobody updates becomes a liability, and choosing not to write something is sometimes the strongest recommendation available.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Working with engineers** maps to **Technical understanding (user-centred design)**, where you collaborate closely with colleagues in different digital disciplines.
- **Assuring and coaching** maps to **User-centred content design**, where you take responsibility for the quality of junior colleagues' content and deliver through others.
- **Influencing stakeholders** maps to **Stakeholder relationship management**.
- **Prioritising and scoping** maps to **Agile working**.
- **Life cycle thinking** maps to **User-centred content design**, where content is regularly reviewed and evaluated.
- **Community contribution** maps to your role level's named engagement with cross-government communities.

### Practice questions

**Question 1 (easy) — Getting information from an engineer**

You need to document a new endpoint. The engineer who built it is busy and their written answers are terse and incomplete. What is the most effective approach?

- A) Keep asking follow-up questions by message until you have enough.
- B) Write a draft from the code and the specification, get it wrong in places, and ask them to correct it — because reviewing a wrong draft takes an engineer five minutes and generates more accurate detail than answering open questions takes them thirty.
- C) Ask for a meeting.
- D) Document what you can and mark the gaps.

**Correct answer: B. Least effective: A**

**Explanation:** This is the single most useful working technique in technical writing and it exploits a real asymmetry: answering "how does authentication work here?" requires an engineer to construct an explanation from scratch, which is slow and produces terse answers, while reading a draft that says something slightly wrong triggers an immediate and detailed correction. People find it much easier to fix a wrong thing than to produce a right one. Option B also puts the effort where your time is cheaper than theirs. Option A is least effective, extending a low-yield exchange over days and consuming exactly the goodwill you will need for the next endpoint. Option C is reasonable and expensive, and works far better once you have a draft to review in it. Option D leaves the reader with the gaps.

**Question 2 (easy) — A factual error in published documentation**

A developer reports that a documented parameter name is wrong. You verify it. What is the most effective response?

- A) Fix the page.
- B) Fix it immediately, thank them, and check whether the same parameter appears in other pages and samples — because a name you got wrong once you probably got wrong consistently, and anyone who copied it has broken code.
- C) Add it to the backlog.
- D) Fix it and add a note about the change.

**Correct answer: B. Least effective: C**

**Explanation:** A wrong parameter name in documentation is live and propagating: developers copy samples, so the error is now in an unknown number of codebases. Option B fixes it fast, acknowledges the reporter — which matters more than it sounds, since a developer who reports a documentation error and hears nothing does not report the next one — and asks the question that distinguishes a writer from a proofreader, because errors of this kind are almost never isolated. Option C is least effective, treating a live factual error that is actively breaking integrations as backlog work. Option A fixes one instance. Option D adds a changelog entry to a correction, which is reasonable and secondary to finding the other instances.

**Question 3 (easy) — A junior colleague's guide**

A junior colleague's guide is well written and describes a process that changed three months ago. What is the most useful response?

- A) Note the error and ask them to fix it.
- B) Note the error, and establish how they verified the process — because a well-written guide describing something that no longer works usually means they wrote from an existing document rather than following the steps, and the habit matters more than this instance.
- C) Fix it yourself.
- D) Praise the writing and mention the error.

**Correct answer: B. Least effective: C**

**Explanation:** The combination is diagnostic: well written, clearly structured, and wrong. That pattern almost always means the writer worked from an older source rather than performing the process, and if that is the method then every guide they produce carries the same risk however carefully they write. Option B addresses the method, which is what your role means by coaching and guiding junior colleagues rather than correcting their output. Option C is least effective, removing the learning and making you a permanent checker of work that will keep containing the same class of error. Option A fixes the instance. Option D softens the point past the level at which it registers.

**Question 4 (moderate) — Pressure to document rather than fix**

An engineering team asks you to document a workaround for a confusing error message rather than change the message, because changing it requires a release. What is the most effective response?

- A) Document the workaround.
- B) Document it as an interim measure, and raise that a confusing error message generates documentation, support tickets and integrator time indefinitely while a message change is bounded work — so the documentation should carry a dated note and the message change should be on the backlog with the ticket volume attached.
- C) Refuse until the message is fixed.
- D) Document it without comment.

**Correct answer: B. Least effective: D**

**Explanation:** The team's constraint is real and their solution transfers a bounded cost into an unbounded one: a message change costs one release, while documentation of a confusing message costs every developer who hits it, forever, plus the support tickets from those who do not find the page. Option B serves the immediate need and makes the trade visible with the evidence attached, which is what turns "the writer would prefer we fixed it" into a prioritisation case. The dated note matters too, since workaround documentation outlives the problem otherwise. Option D is least effective, absorbing the problem silently and guaranteeing it persists — and establishing that documentation is where product defects go. Option A does the same with slightly more awareness. Option C refuses a legitimate interim need.

**Question 5 (moderate) — Content nobody will maintain**

A team asks you to write a detailed guide to an internal tool that changes frequently and has no owner. What is the most effective response?

- A) Write it as asked.
- B) Establish who will keep it current before writing it — because a detailed guide to a frequently changing tool with no owner will be wrong within months and will then mislead people who trust it, which is worse than the current situation where they ask somebody.
- C) Refuse.
- D) Write a shorter version.

**Correct answer: B. Least effective: A**

**Explanation:** Documentation has a maintenance cost that is invisible at the moment of writing and inevitable afterwards, and a detailed guide to a fast-changing tool with no owner is a liability being requested in good faith. Option B asks the question that determines whether writing it is a service or a disservice, and it is a question the requesting team has usually not considered. The comparison it names is the persuasive part: people currently ask a colleague and get a correct answer, and after your guide they will follow it and get a wrong one. Option A is least effective, producing something that will actively mislead. Option D reduces the maintenance burden and is a genuine partial answer — a short guide covering the stable parts ages better than a detailed one — but it still needs an owner. Option C declines without diagnosing.

**Question 6 (moderate) — A disagreement with an engineer**

An engineer objects to your description of an error condition, saying it "basically never happens". Your reading of the code says it can. What is the most effective response?

- A) Defer to the engineer.
- B) Ask what would have to be true for it to occur, since "basically never" describes frequency rather than possibility — and if it can occur, an integrator who has not handled it has a production failure waiting, however rare.
- C) Document it anyway without discussion.
- D) Escalate.

**Correct answer: B. Least effective: A**

**Explanation:** The engineer and you are answering different questions. They are describing how often the condition arises in practice, which is useful information; you are documenting what a client must handle, and rarity is close to irrelevant to that — an unhandled error path fails in production, usually at the worst moment, and rarity means it will not be caught in testing. Option B establishes the conditions, which resolves the disagreement in either direction and produces material worth documenting: "returned when the upstream service is unavailable, which is rare" is a better line than either party started with. Option A is least effective, dropping a documented error path because somebody said it was uncommon. Option C wins the point and forgoes the detail. Option D escalates a technical question with a technical answer.

**Question 7 (moderate) — Writing for the wrong audience**

A stakeholder asks you to make the API reference "more accessible to non-technical readers". What is the most effective response?

- A) Simplify the reference.
- B) Establish who the non-technical readers are and what they need — because if they need to understand what the API does, that is an overview or a product page rather than a reference, and simplifying the reference would degrade it for the developers it exists for while still not serving the new audience.
- C) Refuse; references are for developers.
- D) Add a glossary.

**Correct answer: B. Least effective: A**

**Explanation:** The request conflates two audiences with incompatible needs, and the productive move is to separate them. A developer reading a reference wants precision and density; a non-technical reader wants to know what the thing is for. Simplifying the reference produces something too vague for the first and still impenetrable for the second, which is the worst available outcome and the one option A delivers. Option B asks what the new audience actually needs, and the answer is usually a short overview page that costs a day and serves them properly. Option C is right about the reference and refuses a legitimate need. Option D is a reasonable addition that does not address whether the reference is the right artefact.

**Question 8 (harder) — A breaking change presented as a small one**

Engineering describes a change as minor: a response field is being renamed. You know every integrator parsing that field will break. What is the most effective response?

- A) Document the rename in the release notes.
- B) Document it, and flag that a field rename breaks every client parsing that field — which makes it a breaking change with migration, deprecation and communication implications beyond documentation, and is worth confirming has been considered.
- C) Refuse to document it as minor.
- D) Add a prominent warning to the documentation.

**Correct answer: B. Least effective: A**

**Explanation:** You have noticed something with consequences beyond your task. A renamed response field is breaking by any reasonable definition: existing clients reading the old name get nothing, usually without an error, which produces silent data loss rather than a clean failure. That carries obligations documentation cannot substitute for — a deprecation period, both fields returned during transition, and direct notice to known integrators. Option B raises it as a question rather than a challenge, which is accurate to your position and far more likely to be heard; the team may well have considered it, and it is also common for the person writing the release notes to be the first to think about the reader. Option A is least effective, documenting a breaking change as routine and leaving integrators to discover it. Option D warns readers who may never see the note. Option C makes it a fight about labels.

**Question 9 (harder) — Documentation debt**

Your documentation set has grown to 340 pages, maintained by two writers, and accuracy is slipping. What is the strongest response?

- A) Ask for more writers.
- B) Reduce the surface area: identify content that is obsolete, duplicated or better replaced by generated reference from the source of truth, and retire or automate it — because a set two people cannot maintain will keep decaying whatever effort goes in, and accuracy is a function of size as much as of care.
- C) Introduce a review schedule.
- D) Prioritise the highest-traffic pages.

**Correct answer: B. Least effective: C**

**Explanation:** Accuracy slipping across 340 pages maintained by two people is an arithmetic problem before it is a discipline problem, and effort cannot solve it — any schedule that reviews everything will review each page rarely, and any schedule that does not review everything leaves the rest decaying while claiming coverage. Option B attacks the size, and the third route it names is the strongest available in technical writing: reference documentation generated from the source of truth cannot drift, because it is not a separate artefact. Option C is least effective, adding process to a workload that does not fit, which produces a schedule that slips and a false sense of coverage. Option D is a sensible interim allocation and does not stop the tail decaying. Option A may be justified and is a much easier ask once the set has been rationalised.

**Question 10 (harder) — Community contribution**

You have solved a documentation problem — a clear pattern for documenting authentication flows — that other departments plainly share. What is the most effective response?

- A) Use it and move on.
- B) Share it through the cross-government community with the reasoning and an honest note on where it did not work, and offer to help anyone adapting it — accepting that others may improve it, which is the point.
- C) Publish it as a standard.
- D) Mention it to writers you know.

**Correct answer: B. Least effective: A**

**Explanation:** Your role names engaging with and contributing to the cross-government technical writing and content design communities, and this is where that becomes concrete: authentication is documented badly in most places, and one tested pattern is worth more than several departments each arriving at their own. Option B shares it well, and the honest note about where it did not work is what prevents the pattern being adopted into contexts it does not fit — a pattern that suits token-based flows may be wrong for certificate-based ones, and saying so is what makes it usable rather than merely available. Option A is least effective, keeping a solution while others repeat the work. Option C publishes as a standard something one department has tested. Option D helps a few people and bypasses the mechanism built for this.

**Question 11 (harder) — A flaw in your own work**

You realise a published code sample uses a parameter that works now but is deprecated and will stop working in the next major release. What should you do?

- A) Update it in the next review.
- B) Update it now, and check whether the same parameter appears in other samples — because a pattern you used once you have probably used repeatedly, and every integrator who copied it will break at the same moment.
- C) Update it quietly.
- D) Add a deprecation note to the sample.

**Correct answer: B. Least effective: A**

**Explanation:** Code samples are copied rather than read, which is what makes an error in one categorically different from an error in prose: the deprecated parameter is now in an unknown number of production codebases with a scheduled failure date. Option B fixes it and asks the question that matters — a writer who used a parameter once has usually used it consistently, so the exposure is larger than the page. Option A is least effective, deferring something with a known deadline attached, and the deadline is not yours to move. Option D leaves the sample propagating the problem to anyone who copies before reading, which is most people. Option C corrects the page and leaves the pattern unexamined.

**Question 12 (harder) — Delivering through others**

Engineers in your organisation write a lot of internal documentation, and its quality varies widely. You cannot review it all. What is the strongest response?

- A) Review what you can and accept the rest.
- B) Give them the smallest useful thing that raises the floor without your involvement — a short template with the sections that matter, a handful of worked examples from documentation that works, and a rule of thumb they can apply themselves — and reserve your review for what matters most.
- C) Require all engineering documentation to be reviewed by a writer.
- D) Deliver training to all engineering teams.

**Correct answer: B. Least effective: C**

**Explanation:** You cannot review everything, and any answer depending on you reviewing everything fails on arithmetic. Option B raises the baseline without your involvement, and the specific ingredients matter: a template supplies structure to people who know the content and not the shape, worked examples teach faster than rules, and a rule of thumb — for instance, that a page should let a reader complete one task — travels in a way a style guide does not. Option C is least effective, creating a bottleneck that will either be ignored or will stop documentation being written, and engineering documentation that does not exist is worse than engineering documentation that is uneven. Option D is a real intervention that mostly does not persist unattached to an artefact people use. Option A accepts a variable floor you could raise cheaply.

### Preparation tips

- **Draft it wrong and ask for corrections.** Reviewing beats answering for a busy engineer.
- **Check whether an error appears in other samples.** Samples are copied, not read.
- **Ask who will maintain it before writing it.**
- **Separate audiences rather than compromising between them.**
- **Distinguish "rarely happens" from "cannot happen".** Integrators must handle the second regardless of the first.
- **Attach evidence to a prioritisation case.** Ticket volume turns a preference into an argument.
- **Reduce surface area before adding process.** Accuracy is a function of size.
- **Raise the floor with a template and examples rather than with review.**

### Common pitfalls to avoid

- **Extending a low-yield question exchange with a busy engineer.**
- **Treating a live factual error as backlog work.**
- **Correcting a junior colleague's instance rather than their method.**
- **Absorbing a product defect into documentation silently.**
- **Writing detailed documentation for something with no owner.**
- **Simplifying a reference to serve a second audience.** It serves neither.
- **Documenting a field rename as a minor change.**
- **Adding a review schedule to a set that is too large to review.**

## Conclusion

You have reached the end, and it is worth pausing over what that involved: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a substantial piece of professional preparation and rather more than most people do.

Look back at the ground. In the cognitive section you distinguished a wrong field name from an unclear sentence, read a support ticket pattern as evidence about findability, recognised a workaround guide that would outlive its problem, replaced "appropriately" with the parameters of a decision, and treated zero traffic as ambiguous rather than as permission to delete. In the numeric section you converted a rate limit without inviting intermittent failures, warned against designing for a maximum, read a search log as navigation failure, spotted a retry policy that could not complete inside its own timeout, and found the semantic ambiguity behind a trivial piece of arithmetic. In the verbal section you read "may", "should" and "must" as terms of art, declined to promise acceptance when a passage only ruled out one rejection, treated a specification's silence as a gap rather than a behaviour, and refused to mark True on a confounded finding that would have supported a practice you favour. And in the situational judgement section you drafted something wrong to get it corrected, asked who would maintain a guide before writing it, separated two audiences rather than compromising between them, and raised a documentation floor with a template rather than a review queue.

Two threads run through it. The first is that accuracy in your discipline has a hard edge that most content work does not: your readers copy what you write into systems that then fail or do not, and a wrong parameter is a different kind of error from an unclear sentence. The second is that your effectiveness depends almost entirely on people who have the knowledge and not the time, which is why so many of the strongest answers here are about how you extract information, transfer capability, or decline to create something nobody will maintain.

A word about your level. Being an expert practitioner in this discipline means you are frequently the only person in the room thinking about the reader — the engineers know how it works, the product people know why it exists, and nobody but you is asking what somebody encountering it for the first time at two in the morning needs to see first. That is a genuinely valuable position and it is easy to spend it badly, on formatting arguments and style debates. Spend it on accuracy, on findability, and on the things that should not be documented at all.

If you want to build on this, a few things repay effort more than rereading. Integrate with your own API using only your documentation, on a clean machine, and note every point where you had to look at the source. Read a month of support tickets and find the pages that should have answered them. Ask an engineer to talk you through the code path behind an endpoint you have documented. Look at your search log for two vocabularies describing one need. And take the ten pages you are proudest of and ask who will notice when they go out of date.

Finally, for the day itself. An assessment samples your reasoning on one morning under artificial conditions. It is not a verdict on your judgement or your career. Read the stem twice, read "should" as "should", find the denominator, trust Cannot Say, and remember that the strongest answer is usually the one that is exactly right about a fact and honest about what is not yet known.

Good luck. Go carefully, verify by doing, and keep asking who will maintain it.
