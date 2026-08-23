# Lead Technical Writer - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a lead technical writer in the UK Government Digital and Data profession — an expert practitioner who directs a team of technical writers and assures the quality of technical writing across teams and its alignment to strategy. Your role description adds that you standardise tools, ways of communicating and processes; work closely with service managers, technology leaders and senior stakeholders to resource teams and resolve problems; promote the discipline of technical writing; engage with the cross-government community; and keep up to date with industry changes.

That is a role in which most of what you achieve happens through other people, in a discipline that is chronically under-resourced because its value is hard to demonstrate. Both facts shape this guide.

You may be facing a formal assessment as part of a selection process, or you may want to re-examine reasoning that has become fluent enough to be worth checking. At your level the risk is not gaps in technique but that technique has become automatic, automatic reasoning feels certain, and few people around you are positioned to catch you.

Three features of the role shape everything that follows. First, you assure writing you did not produce, on systems you have not integrated with, judged from a document rather than from the thing it describes — which makes reading an output for the shape of the work behind it a core competence. Second, you standardise: tools, templates, processes and ways of working. A decision at that level is paid for many times, and a template that omits a field produces the same gap in every document that uses it. Third, you argue for resource in a discipline whose absence is invisible until an integration fails, which puts unusual weight on your ability to express documentation value in numbers other people already use.

The document has four main sections: a cognitive assessment, a numeric reasoning assessment, a verbal reasoning assessment, and a situational judgement assessment. Each provides an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Commit before reading, and attend particularly where you were quick and sure.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands, presented through practical materials rather than abstract puzzles. At lead level the materials are documentation sets you did not write, analytics across a portal, support data, team output, and standards applied unevenly.

The format is typically an online test of fifteen to thirty minutes covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group of comparable seniority.

Three things distinguish this section at your level.

The first is reasoning at a distance. You judge documentation from the document rather than from using it, which makes the absence of information as informative as its presence — a reference with no error codes tells you what the writer had access to as much as what the endpoint returns.

The second is that the interesting problems are systemic. Documentation defects recur because something produces them: a template without a field for error codes, a release process that does not involve writers, an engineering culture where nobody is asked, or a tooling gap that makes samples untestable. Fixing documents leaves the mechanism intact.

The third is the maintenance calculus. Your team's capacity is fixed and your documentation set is not, and a substantial part of your judgement concerns what should not exist — content nobody maintains is a liability, and choosing to retire or automate is frequently a stronger recommendation than choosing to write.

### How this assessment maps to your role

The cognitive dimensions map onto the skills named in your role summary:

- **Auditing at a distance** maps to assuring the quality of technical writing across teams.
- **Systemic diagnosis** maps to standardising tools, ways of communicating and processes.
- **Life cycle reasoning** maps to **User-centred content design**, where you direct the approach to content life cycle management.
- **Strategic prioritisation** maps to **Strategic thinking**, where you lead the design and implementation of strategy.
- **Capability diagnosis** maps to **User-centred content design**, where you identify gaps in skills and capability and help teams grow.
- **Reasoning about positions** maps to **Stakeholder relationship management**, where you influence and negotiate with senior stakeholders.

### Practice questions

**Question 1 (easy) — Reading an output for what is missing**

A reference page documents an endpoint's method, parameters, response schema and a code sample. It lists no error codes. What is the most important observation?

- A) The page is nearly complete.
- B) An absent error section usually means the writer documented what the endpoint returns on success — which is what a specification and a happy-path test show — and had no source for the failure modes, so the gap is about their access to information rather than their thoroughness.
- C) The error codes should be added.
- D) The sample should be tested.

**Correct answer: B**

**Explanation:** Option C states the remedy and B states the diagnosis, and at your level the diagnosis is the useful output. Error codes are the section most often missing in API documentation, and almost never because the writer forgot: success behaviour is visible in a specification and in any working call, while the set of failures an endpoint can produce usually exists only in the code or in an engineer's head. A writer without that access produces exactly this page. Option B identifies that, which points at the fix — a template field that must be filled, and a route to the information — rather than at one page. Option A treats a missing section as a rounding error when it is the section integrators need to write resilient clients.

**Question 2 (easy) — Deduction from a versioning policy**

A policy states: "Breaking changes may only be released in a new major version, unless the affected endpoint has been formally deprecated for at least six months." A team reports changing a response format last week with no major version bump. Which must be true?

- A) The policy was breached.
- B) The endpoint had been deprecated for six months.
- C) Either the endpoint had been deprecated for at least six months, or the policy was breached — and separately, whether the change was breaking has not been established.
- D) The change was not breaking.

**Correct answer: C**

**Explanation:** A conditional with a stated exception, plus facts silent on the exception, licenses only the disjunction — and this item has a second layer. The policy governs *breaking* changes, and "changed the response format" does not establish that: adding an optional field changes the format and breaks nothing, while renaming or removing one breaks every client parsing it. So two things are undetermined and option C names both. At your level the practical consequence is what your team documents — an addition is a release note, a rename is a migration guide with a communication plan — and establishing which before your writers start is part of resolving problems with technology leaders rather than after.

**Question 3 (moderate) — Diagnosing recurring defects**

Across four teams' documentation you find the same three gaps: missing error codes, untested code samples, and no statement of which version the documentation describes. What is the strongest diagnosis?

- A) Four teams need training.
- B) Three specific gaps recurring across four independent teams indicates a shared cause — most plausibly a template lacking those fields, or a process where writers are engaged after release rather than during — and the three named have a common character: each requires information or access a writer only gets by being present when the thing is built.
- C) Documentation quality is generally low.
- D) Reviews should be more frequent.

**Correct answer: B**

**Explanation:** Three specific gaps across four independent teams is not four coincidences, and the observation that makes option B strong is what the three have in common: error codes, tested samples and version identification all require the writer to have access to a running system and to the engineers building it. A writer handed a specification after the fact can produce everything else and none of these. That points at engagement timing and at tooling rather than at skill, which is a completely different remedy from training. Option A is the default and weakest response. Option C is a diagnosis so general it suggests no action. Option D increases detection without reducing occurrence and consumes your own capacity permanently.

**Question 4 (moderate) — Strategic prioritisation**

You can direct substantial capacity to one of four things this quarter:

1. Generating reference documentation automatically from API specifications across the estate.
2. Auditing the documentation for twelve services not reviewed in two years.
3. Writing a style guide for engineering-authored content.
4. Rewriting the top twenty highest-traffic pages.

Which is strongest, and why?

- A) Item 4, because it affects the most readers.
- B) Item 1, because generated reference cannot drift from the source of truth — it removes a whole class of decay permanently across the estate, whereas the others improve, detect or inform a set that will decay again.
- C) Item 2, because unreviewed documentation is unknown risk.
- D) Item 3, because it scales through others.

**Correct answer: B**

**Explanation:** The four options are prevention, detection, capability and repair, and only one changes the rate at which documentation goes wrong. Reference documentation generated from a specification is not a separate artefact that can fall out of step; it is a view of the source of truth, so the commonest and most damaging failure — documentation describing an interface that has changed — becomes structurally impossible for everything it covers. Option A repairs twenty pages that will decay again. Option C produces a list. Option D is genuinely good and third-best, because a style guide raises quality and does nothing about accuracy. Note that option 1 does not cover everything — guides, tutorials and conceptual material still need writing — which is exactly why it is worth doing: it frees your team for the work that cannot be generated.

**Question 5 (moderate) — What should not exist**

Your set contains a twelve-page guide to working around a limitation that engineering will remove in two months. What is the strongest recommendation?

- A) Keep it; users need it now.
- B) Keep it with a prominent dated note and a scheduled retirement — because an undated workaround guide outlives its problem and then leads people into unnecessary and usually fragile constructions, which is worse than having no page.
- C) Remove it now.
- D) Shorten it.

**Correct answer: B**

**Explanation:** Workaround documentation has a characteristic failure mode: written under pressure, genuinely useful, and then orphaned when the problem is fixed. Two years later somebody follows twelve pages of workaround for a limitation that no longer exists, which costs them a day and leaves unnecessary complexity in their codebase. Option B keeps it useful now and builds in the retirement, which is what your role means by directing content life cycle management. The scheduling is the part that distinguishes a lead's answer: a note saying the workaround will become unnecessary is good, and a note plus a calendar entry is what actually results in the page being retired. Option A ignores the life cycle. Option C removes something currently needed. Option D improves prose on a page whose problem is temporal.

**Question 6 (moderate) — Assuring a writer's work**

A writer in your team produces a guide that is well written, clearly structured, and describes a configuration process that changed three months ago. What is the most useful response?

- A) Correct the error.
- B) Establish how they verified the process — because a well-written guide describing something that no longer works usually means writing from an existing source rather than performing the steps, and the method matters more than the instance since every guide they produce carries the same risk.
- C) Correct it and note it in their review.
- D) Add a verification step to the team's process.

**Correct answer: B**

**Explanation:** The diagnostic combination is well written, well structured and wrong, which almost always means the writer worked from an older document rather than following the process. Option B addresses the method with the individual, which is where it should start. Option D is the systemic version and is the right *second* move — if more than one writer has the habit, or if the reason is that nobody has an environment to test in, the fix belongs in the team process rather than in a conversation. Doing D without B risks adding a process step to solve one person's habit; doing B without D risks fixing one person while the same gap persists. Option A fixes the instance. Option C converts a coachable habit into a performance note before anyone has discussed it.

**Question 7 (moderate) — Standardising tools**

Your four writers use three different documentation tools, inherited from the teams they sit with. What is the strongest approach?

- A) Standardise on one tool immediately.
- B) Establish what the differences actually cost — whether it is reviewer confusion, inability to share components, duplicated effort on templates, or nothing much — because standardising has real costs in migration and in fighting the teams whose toolchains these are, and it is worth doing only where the fragmentation is causing something.
- C) Let each writer keep their tool.
- D) Standardise on the most popular one.

**Correct answer: B**

**Explanation:** Standardisation is named in your role and is not automatically correct, and the discipline is to establish the cost before paying one. Sometimes the fragmentation is genuinely expensive — writers cannot cover for each other, templates are maintained three times, and a change to shared style means three implementations. Sometimes it costs almost nothing because the tools output similar things and the writers rarely overlap. Option B distinguishes them. The second clause matters too: documentation tooling is usually chosen by the engineering team a writer sits with, so standardising means asking three teams to change something they own, which is a substantial ask requiring a substantial reason. Option A pays the cost without establishing it. Option D picks by popularity rather than by need.

**Question 8 (harder) — Scoping a flaw in an audit**

A documentation audit you commissioned was conducted by reading pages rather than by using them. Four findings: (i) 23 pages have inconsistent heading structure; (ii) code samples appear correct; (iii) terminology is inconsistent across four guides; (iv) navigation is clear. Which findings are most compromised?

- A) All four.
- B) None; reading is a valid audit method.
- C) Findings (ii) and (iv) are most compromised, because whether samples work and whether navigation is clear can only be established by running the samples and by trying to find something — while heading structure and terminology consistency are genuinely assessable by reading.
- D) Only (ii).

**Correct answer: C**

**Explanation:** The distinction is between properties visible on the page and properties that only appear in use. Heading structure and terminology consistency are textual and a careful reader can assess them. Whether a code sample works requires executing it, and "appears correct" means the reviewer read it and saw nothing obviously wrong — which will not catch a deprecated parameter, a renamed field or a sample that was correct for a previous version. Whether navigation is clear requires trying to find something you do not already know the location of, which a reader working through pages sequentially never does. Option C says this. Option A discards two sound findings. Option B accepts two findings the method cannot support, and those are the two most likely to be quoted as reassurance.

**Question 9 (harder) — Reading portal analytics**

A developer portal shows high traffic to getting-started, low traffic to conceptual material, very high traffic to one error-code page, and a high internal search volume for "webhook". What is the strongest interpretation?

- A) The conceptual material should be promoted.
- B) The overall shape is normal for a developer audience, and two signals stand out for different reasons: concentrated traffic to one error code means either that error is common or its page is unhelpful, and high internal search for a topic means people cannot reach it by navigation — so one is a content or product question and the other is a findability question.
- C) More content is needed on webhooks.
- D) The error page is performing well.

**Correct answer: B**

**Explanation:** Three readings are needed and option B supplies them. The overall pattern — heavy getting-started, light concepts, heavy error reference — is what a working developer audience produces and should not be treated as a defect. The error concentration has two possible causes with different owners: a common error points at the product, an unhelpful page points at your team. And search volume measures navigation failure rather than interest, so "webhook" being searched heavily suggests the content exists somewhere unreachable rather than that it is missing. Option C assumes absence when the likelier answer is findability, which is a cheaper fix. Option D reads high traffic to an error page as success, which is backwards. Option A treats a normal pattern as a problem.

**Question 10 (harder) — A capability gap**

Two of your four writers produce consistently accurate technical content; two produce well-written content with recurring factual errors. All four are experienced writers. What is the strongest inference?

- A) The two need technical training.
- B) The difference is more likely access than knowledge — the accurate two probably have working environments, engineer relationships or code access the others lack — so establish what the first two actually do to verify, and give the others the same access before assuming a skills gap.
- C) Reassign technical content to the accurate two.
- D) Review all four writers' output.

**Correct answer: B**

**Explanation:** All four are experienced writers, which makes a straightforward skills explanation less likely than an access one, and the distinction is worth being careful about because the remedies are entirely different and one of them is insulting. A writer with a local environment, a friendly engineer and read access to the repository can verify everything; a writer with a specification and a shared inbox cannot, however capable. Option B goes and establishes what the accurate two do, which is the step almost everyone skips. Option A may be right and is the assumption to test rather than act on. Option C concentrates the work and permanently limits two people. Option D makes you the bottleneck and does not address why the errors occur.

**Question 11 (harder) — Aligning to strategy**

Your organisation's technology strategy commits to an API-first approach. Your team spends most of its time on internal process documentation. What is the strongest response?

- A) Continue; internal documentation is needed.
- B) Establish whether the mismatch is a misallocation or a signal — if the organisation is genuinely moving to API-first, your team's effort should follow, and if internal process documentation is consuming the capacity because nobody else will write it, that is a different problem to raise rather than absorb.
- C) Redirect the team to API documentation.
- D) Ask for more writers.

**Correct answer: B**

**Explanation:** A mismatch between where a team's effort goes and where the organisation says it is heading has two very different explanations, and acting before establishing which is how leads waste a year. If the strategy is real and your team is misallocated, redirecting is correct and overdue. If the team is absorbing internal process documentation because no other function will produce it, then redirecting will simply leave that work undone and somebody will notice — so the useful move is to surface it as a resourcing question rather than to solve it silently. Option B distinguishes them, which is what your role means by directing the evaluation of strategies to ensure business requirements are being met. Option C acts on one reading. Option A accepts a misalignment your role exists to notice. Option D asks for resource before establishing what the current resource should be doing.

**Question 12 (harder) — A flaw in something you standardised**

Six months ago you introduced a documentation template now used across the organisation. You realise it has no field for error codes, and error documentation has become patchier since. What should you do?

- A) Add the field to the template.
- B) Add the field, tell the teams using the template that documentation produced with it may be missing error codes, identify which pages need retrofitting, and ask why the template review did not catch a missing section that is among the most important in API documentation.
- C) Add the field quietly.
- D) Note it for the next template review.

**Correct answer: B**

**Explanation:** A template used across an organisation propagates its gaps into everything produced with it, so this is not one omission but every document written in six months. Option B does the four things that matter: fixes the template, tells the people whose documentation is affected — which they cannot know otherwise — identifies the remediation scope, and asks the question specific to your level, which is why the review process did not catch it. That last part is the only element that prevents the next omission, and the answer is usually that the template was reviewed by writers against style rather than against the completeness requirements of the content type. Option C fixes the template and leaves six months of incomplete documentation undiscovered. Option A does the same more openly. Option D defers a compounding problem.

### Preparation tips

- **Read an output for what its author had access to.** A missing error section is usually an access problem.
- **Ask what several teams' identical gaps have in common.** Often it is information a writer only gets by being present.
- **Prefer generation to writing where a source of truth exists.** Generated reference cannot drift.
- **Establish the cost of fragmentation before standardising.** Standardisation is not free and is not always warranted.
- **Distinguish properties visible on a page from properties only visible in use.**
- **Read search volume as navigation failure.**
- **Test access before assuming a skills gap.** Experienced writers producing errors usually lack verification routes.
- **Ask why a review process missed something before adding another review.**

### Common pitfalls to avoid

- **Treating a missing error section as thoroughness rather than access.**
- **Reaching for training as the answer to a systemic gap.**
- **Repairing high-traffic pages that will decay again.**
- **Standardising without establishing the cost of not doing so.**
- **Accepting audit findings a reading-based method cannot support.**
- **Assuming absent content when the likelier answer is findability.**
- **Concentrating technical work on the writers who can already do it.**
- **Fixing a template without telling the people whose documents used the broken version.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A numeric reasoning assessment measures how accurately you handle quantitative material. At lead level the emphasis shifts from calculating to interrogating, and the material becomes consequential in a specific way: technical writing is chronically under-resourced because its value is invisible until an integration fails, and the only reliable remedy is figures.

That is worth stating plainly. A lead technical writer arguing for a fourth writer on the grounds that documentation is important will lose to almost any competing bid. One who can say that integration support tickets cost the organisation a quantified amount, that a documented class of them fell by a measured proportion after a specific intervention, and that the remaining volume implies a particular saving, is making an argument in the currency the decision is taken in. Your role names working with technology leaders and senior stakeholders to resource teams, and that conversation happens in numbers.

The format is typically a timed online test of fifteen to thirty minutes, each item presenting a table, chart or paragraph of figures with a multiple-choice question. Calculators are usually provided.

Four habits carry the load. Establish what the question asks before looking at the data. Identify the denominator and the population it represents. Estimate, calculate, compare. And sanity-check against the world.

### How this assessment maps to your role

The numerical skills tested map onto your named skills:

- **Quantifying documentation value** maps to **Stakeholder relationship management**, where you resource teams and negotiate with senior stakeholders.
- **Reading portal and support analytics** maps to **User-centred content design**, where you direct content life cycle management.
- **Weighted aggregation across teams** maps to assuring quality across teams.
- **Estimating effort** maps to **Agile working**, where you help teams prioritise and adhere to scope.
- **Evaluating interventions** maps to **Strategic thinking**, where you direct the evaluation of strategies.
- **Detecting misleading metrics** maps to your accountability for what your function reports.

### Practice questions

**Question 1 (easy) — Support ticket proportion**

Of 8,400 support tickets a year, 2,100 are integration questions answerable from documentation. What proportion?

- A) 20%
- B) 25%
- C) 30%
- D) 40%

**Correct answer: B**

**Explanation:** 2,100 ÷ 8,400 = 0.25, so 25%, giving B. Estimate first: 2,100 of 8,400 is a quarter. The figure is the beginning of a resourcing argument rather than the end of one, and the qualifier "answerable from documentation" is doing essential work — it is the subset your function could plausibly affect, and quoting total ticket volume instead would overstate your case and invite a correction that undermines the rest.

**Question 2 (easy) — Annualising and costing**

Integration tickets run at 175 a month. If the organisation's cost per supported ticket is £18, what is the annual cost?

- A) £3,150
- B) £37,800
- C) £315,000
- D) £2,100

**Correct answer: B**

**Explanation:** 175 × 12 = 2,100 tickets a year, and 2,100 × £18 = £37,800, giving B. Option A stops at the monthly cost, which is the commonest error because the first calculation feels complete. The annualised figure is the one that competes in a resourcing conversation: £3,150 a month is a rounding error in most budgets, and £37,800 a year against the cost of a writer is an argument. Note the honesty required — this is the cost of the tickets, not the saving from a writer, and claiming the second would be overstating. The defensible version says that a measured proportion of these tickets is documentation-addressable and estimates the saving from that share.

**Question 3 (easy) — Weighted aggregation across teams**

Four teams' documentation sets have defect rates per hundred pages of 4 on 300 pages, 10 on 100, 6 on 200, and 5 on 400. What is the overall rate?

- A) 5.4
- B) 6.25
- C) 5.0
- D) 7.0

**Correct answer: A**

**Explanation:** Convert to counts. 4 per hundred on 300 = 12 defects. 10 per hundred on 100 = 10. 6 per hundred on 200 = 12. 5 per hundred on 400 = 20. Total 54 across 1,000 pages, so 5.4 per hundred, giving A. Option B is the unweighted mean of 4, 10, 6 and 5, which is 6.25 and over-weights the 100-page team against the 400-page one. The organisational point matters more than the arithmetic: the unweighted figure describes the average *team*, while the weighted figure describes the average *page* — and only the second describes what a reader encounters, which is the figure that belongs in a report you sign.

**Question 4 (easy) — Reading a distribution**

Of 340 pages, 40 account for 85% of traffic and 120 have had no visits in a year. What is the strongest reading?

- A) The 120 should be archived.
- B) The distribution is normal for technical documentation, and zero traffic is ambiguous — genuinely obsolete content, rarely-needed critical content such as recovery or migration guides, and content nobody can find all look identical in the figures, so the number identifies candidates for investigation rather than for deletion.
- C) Maintenance should focus on the 40.
- D) The set should be reduced to 40 pages.

**Correct answer: B**

**Explanation:** Zero traffic is the most misread statistic in documentation management, because it is ambiguous in a way that makes acting on it directly hazardous, and the three cases have opposite remedies. Obsolete content should go. A migration guide for a version some integrators are still on is *supposed* to have almost no traffic and is catastrophic to lose. And unfindable content looks identical to unwanted content in the figures while needing promotion. Option B distinguishes them. Option A treats a recovery procedure as dead weight, which is the error discovered during a recovery. Option C is a sensible maintenance allocation answering a different question. Option D is A with more conviction.

**Question 5 (moderate) — Evaluating an intervention**

After introducing generated reference documentation, integration tickets fell from 175 to 130 a month. What is the change, and what should you check?

- A) 26% reduction, demonstrating the intervention worked
- B) 26% reduction, and the check is whether the fall is concentrated in the ticket categories generated reference addresses — parameter names, response fields, endpoint behaviour — because a fall spread evenly across categories suggests something else changed
- C) 35% reduction
- D) 45 tickets, which is the meaningful figure

**Correct answer: B**

**Explanation:** The difference is 45, and 45 ÷ 175 = 0.257, about 26%, so option C miscalculates by dividing by the new figure. Between A and B the check decides it, and it is a specific and answerable one: generated reference fixes a defined class of question — what a field is called, what an endpoint returns, which parameters exist — so attribution holds if the fall is concentrated there and does not if tickets fell uniformly, which would suggest a quieter period or a change in how tickets are logged. At your level you will be asked whether the investment worked, and a claim you have not tested is one that collapses when next year's figures move the other way.

**Question 6 (moderate) — Estimating team capacity**

Your four writers each have about 120 productive days a year. An API programme estimates needing 200 writer-days. What proportion of your team's annual capacity is that, and what should you note?

- A) 42%, and the note is that this leaves 280 days for everything else including maintenance of an existing 340-page set
- B) 42%
- C) 50%
- D) 200 days is manageable across four writers

**Correct answer: A**

**Explanation:** Total capacity is 4 × 120 = 480 days, and 200 ÷ 480 = 0.417, about 42% — so the arithmetic gives A and B equally, and the note decides it. The note is the substantive part at your level: a request for 42% of annual capacity is not obviously unreasonable, and it becomes a decision rather than an acceptance once the remaining 280 days are set against the maintenance load of an existing set plus every other team's requests. Stating that turns "can you do this?" into "here is what we would not do", which is the only form in which a capacity conversation is honest. Option D accepts without establishing the trade.

**Question 7 (moderate) — Percentage change**

Monthly visits to a getting-started guide rose from 5,600 to 7,000 after it was linked from the API console. What is the increase, and what does it suggest?

- A) 20%
- B) 25%, suggesting findability rather than content was the constraint — which is worth testing elsewhere in the set
- C) 80%
- D) 25%

**Correct answer: B**

**Explanation:** The difference is 1,400, and 1,400 ÷ 5,600 = 0.25, a 25% increase, so option A divides by the new figure. Between B and D the interpretation decides it, and it generalises: a quarter more readers from adding one link means the content was adequate and unreachable, which raises the obvious question of how much else in a 340-page set is in the same position. That is a cheap and high-yield line of investigation, and noticing it is the difference between reporting a number and directing work with it.

**Question 8 (moderate) — Comparing two documentation approaches**

Version A of a guide had 14,000 visits with 4,200 users progressing. Version B had 9,000 visits with 3,600 progressing. Which performed better, and what else should you ask?

- A) Version A, with more users progressing.
- B) Version B, at 40% against 30% — and the question is why B has lower traffic, since a better page reaching fewer people may need promotion rather than congratulation.
- C) They are equivalent.
- D) Version A, with more traffic.

**Correct answer: B**

**Explanation:** Convert to rates: A is 4,200 ÷ 14,000 = 30%, B is 3,600 ÷ 9,000 = 40%. B performs better per reader, so options A and D compare raw counts across different-sized groups. The second clause is what makes B the complete answer: a page converting better while reaching fewer people is a partial success, and if the traffic difference reflects findability then promoting B would deliver more than the rewrite did. Rate is the right comparison and it is not the whole picture, and at your level noticing the second half is what turns an evaluation into a decision.

**Question 9 (moderate) — Estimating documentation effort**

An API has 60 endpoints. A writer estimates 90 minutes each, giving 90 hours. What is the most useful thing to establish?

- A) Whether 90 minutes is realistic.
- B) Whether the endpoints share request, response and error patterns — because a well-designed API has a handful of patterns with consistent authentication, pagination and error behaviour, making the work closer to documenting the patterns once plus 60 short variations, which is a much smaller job.
- C) The total, which is 90 hours.
- D) Whether the writer has documented an API before.

**Correct answer: B**

**Explanation:** The estimate treats endpoints as independent, and REST APIs rarely are. Option B establishes the structure, which can move the estimate by more than half — and the direction of the finding is informative either way: an API with sixty genuinely idiosyncratic endpoints is a much larger documentation job and also a much worse API, which is worth saying to the technology lead before either of you commits. Option A asks about the rate rather than the structure, the less consequential half. Option C computes what the estimate implies without questioning its basis, which is how documentation programmes get scoped at twice their real size and then descoped in a way that removes the wrong things.

**Question 10 (harder) — A directionless metric**

Your portal reports average time on page as 4 minutes, and a stakeholder reads this as strong engagement. What is the strongest response?

- A) Agree.
- B) Time on page has no direction for reference documentation — a developer finding an answer in ten seconds is a success and one spending four minutes on a confusing page is a failure — so the figure supports neither reading, and the measures with direction are progression, repeat searching and ticket volume.
- C) The pages should be shorter.
- D) Break it down by page.

**Correct answer: B**

**Explanation:** Time on page is misleading everywhere and inverted here, because the ideal interaction with a reference page is brief. Option B names the ambiguity and supplies measures that move interpretably. The stakes at your level are higher than being right: a stakeholder who has accepted dwell time as an engagement measure will eventually ask your team to improve it, and a documentation team optimising for time on page will make things worse extremely efficiently. Saying so before the metric becomes a target is the intervention. Option D reports the same directionless quantity more granularly. Option C acts on one interpretation.

**Question 11 (harder) — Percentage points and relative change**

The proportion of integrations completed within a day rose from 45% to 57% after a documentation programme. Which statement is accurate?

- A) A 12% increase.
- B) A 12 percentage point increase, equivalent to a 27% relative increase.
- C) A 27 percentage point increase.
- D) A 21% increase.

**Correct answer: B**

**Explanation:** The gap is 57 − 45 = 12 percentage points; the relative increase is 12 ÷ 45 = 0.267, about 27%. Option B labels both. Option A is ambiguous and generally read as relative. Option C misapplies the label. Option D divides by the new value. For you the stake is specific: technical writing value claims already attract scepticism, and a lead who reports the larger-sounding figure and is later found to have chosen it will find every subsequent claim discounted. Making both figures a standing convention in your team's reporting removes the temptation and the suspicion together, and costs nothing.

**Question 12 (harder) — A figure in a business case**

A business case for two additional writers claims a saving of £240,000 a year. Integration tickets number 2,100 a year at £18 each. What should you check?

- A) Nothing; the case is made.
- B) The arithmetic does not reconcile: eliminating every integration ticket would save about £37,800, so a £240,000 claim must rest on something else — developer time, delayed integrations, or abandoned onboarding — and unless that basis is stated and defensible the case will not survive scrutiny.
- C) Whether £18 per ticket is right.
- D) Whether two writers is the right number.

**Correct answer: B**

**Explanation:** 2,100 tickets at £18 is £37,800, so the claimed saving exceeds the entire ticket cost by a factor of more than six — which means either the case rests on a different and unstated benefit, or somebody has produced a number they cannot defend. Option B identifies the gap and names the plausible alternative bases, all of which are legitimate: integrator time is real, delayed integrations have costs, and abandoned onboarding is expensive. The point is that they must be stated. A business case whose headline figure cannot be reconciled with its own supporting data will be taken apart by finance, and the damage extends beyond the bid — it will be remembered the next time your function asks for anything. Option C is a fair secondary check on a much smaller discrepancy.

### Preparation tips

- **Annualise and cost before arguing for resource.** Monthly figures do not compete.
- **Quote the addressable subset, not the total.** It is more defensible and harder to dismiss.
- **Return to counts before combining rates.** The weighted figure describes what readers encounter.
- **Treat zero traffic as ambiguous.** Obsolete, rarely-needed and unfindable look identical.
- **Test attribution before claiming an intervention worked.**
- **State what would not be done when accepting a capacity request.**
- **Distrust time on page, and say so before it becomes a target.**
- **Reconcile a business case against its own supporting figures.**

### Common pitfalls to avoid

- **Stopping at a monthly figure.**
- **Claiming ticket cost as saving.** They are not the same.
- **Averaging team-level rates without weighting.**
- **Archiving low-traffic content without asking why it is low.**
- **Comparing raw counts across pages with different traffic.**
- **Accepting an endpoint estimate as independent units.**
- **Letting dwell time be reported as engagement.**
- **Signing a business case whose headline exceeds its own evidence.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A verbal reasoning assessment measures how accurately you read. For your discipline it is close to the job: your team's work consists of reading specifications, tickets, code comments and API contracts and turning them into something a reader can act on, and you assure the result. Getting it wrong in either direction is serious — understate a constraint and integrators build something that breaks, overstate one and they build defensively around a limit that does not exist.

The classic format presents a short passage of dense workplace prose, typically three to six sentences, followed by statements to classify as True, False or Cannot Say. Alongside these come comprehension items, main-point items, and questions asking which of four summaries is most accurate.

The governing rule is that you answer from the passage alone, and the part specific to your level is this: expertise costs marks. You know how these systems usually behave, and supplying the expected behaviour rather than the described one is exactly the error that produces documentation asserting things a specification never said. Candidates at your level underperform on verbal reasoning at rates that surprise them.

Cannot Say is the answer experienced practitioners avoid, and in your discipline it has a specific value: identifying that a specification does not determine something is how you find the question somebody must answer before your team documents it.

Small words carry the load. "May", "should" and "must" have defined force in specification prose. "Or" offers alternatives. And silence is a gap, not permission.

### How this assessment maps to your role

The verbal skills tested map onto your named skills:

- **Reading specifications precisely** maps to **Technical understanding (user-centred design)**.
- **Separating statement from inference** maps to being accountable for the production of high quality content.
- **Identifying the main point** maps to your team's core task, which you assure.
- **Handling qualified language** maps to **Technical understanding**, where "may" and "must" carry defined weight.
- **Reading for absence** maps to **User-centred content design**, where identifying gaps is named.
- **Reading governance and review prose** maps to **Stakeholder relationship management**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Clients must include an Authorization header on all requests to protected endpoints. Clients may include an Idempotency-Key header on POST requests; where present, the server will return the original response for any repeated request with the same key within 24 hours. Servers must reject requests exceeding 2 MB with a 413 response. Clients should implement exponential backoff on 429 responses."

**Question 1 (easy)** — Statement: "Clients must include an Idempotency-Key on POST requests." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says clients *may* include it — optional. The statement's "must" contradicts that, so False. The passage uses all three modal terms deliberately: Authorization is mandatory, idempotency keys optional, backoff recommended. A documentation set that flattens those into one register either over-constrains integrators or under-warns them, and at your level the useful output is a house convention on how each is rendered — because four writers left to their own instincts will produce four treatments of the same distinction.

**Question 2 (easy)** — Statement: "A repeated POST with the same key after 30 hours returns the original response." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The guarantee applies to repeats *within 24 hours*, and 30 hours falls outside it, so the statement is contradicted. False. Note what the passage does not establish: what happens after 24 hours is unstated — the request might be processed as new, rejected, or something else — so an honest draft documents the guarantee and its window and does not invent the behaviour beyond it. That gap is exactly the sort of thing worth flagging to engineering before publication rather than resolving by assumption.

**Question 3 (moderate)** — Statement: "A client without exponential backoff is non-compliant." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The passage says clients *should* implement backoff. In specification usage "should" indicates a strong recommendation that may be departed from for good reason, not a requirement — so a client without it departs from a recommendation and is not non-compliant. False. The distinction matters to integrators because it tells them whether omitting the behaviour will get their client rejected or merely leave it less well behaved, and documentation rendering both as "you need to" removes information they use to prioritise. At your level this is a review criterion worth naming explicitly.

**Question 4 (harder)** — Statement: "A 1.9 MB request will be accepted." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage requires servers to reject requests *exceeding* 2 MB, so a 1.9 MB request is not rejected on size. But acceptance depends on authorisation, validity, rate limits and anything the passage does not mention, and the passage establishes only that one rejection does not apply. Cannot Say. The distinction between "will not be rejected for this reason" and "will be accepted" is one your reviewers should be catching in drafts, because writing "requests under 2 MB are accepted" makes a promise the specification does not, and the integrator who believes it and then sees a valid-sized request fail validation concludes your documentation is unreliable.

*Passage B — for Questions 5 to 8*

"The review of the developer portal found that teams publishing reference documentation alongside code releases reported fewer integration support tickets than teams publishing separately. The review notes that the teams publishing alongside releases were also those with dedicated technical writers. The review did not assess documentation accuracy. It recommends that the portal team consider whether alongside-release publishing should be standard."

**Question 5 (easy)** — Statement: "Teams publishing alongside releases reported fewer integration tickets." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence states this directly and the statement restates it without addition. True. Note the careful "reported fewer" rather than "had fewer" — a distinction the statement respects, and one worth preserving whenever your team writes up findings, because reported and actual volumes diverge for reasons that have nothing to do with the thing being measured.

**Question 6 (moderate)** — Statement: "Publishing alongside releases reduces support tickets." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage reports an association and flags that the same teams had dedicated technical writers, which is a substantial confound — a team with a dedicated writer would be expected to produce better documentation whenever it published. So the fall may be attributable to the writer, the timing, both, or something unnamed. Cannot Say. This is the specific trap for someone in your position, because "publishing alongside releases reduces tickets" is a claim you would like to be true and would cite when standardising the process. The stronger and honest argument is available: documentation published after a release is documentation integrators did not have when they needed it, which stands on its own without needing the ticket data.

**Question 7 (moderate)** — Statement: "The documentation published alongside releases was more accurate." True, False or Cannot Say?

**Correct answer: Cannot Say**

**Explanation:** The passage says explicitly that accuracy was not assessed. Declared silence establishes nothing, so Cannot Say. The possibility worth registering is that documentation written under release pressure might be *less* accurate while generating fewer tickets, if it arrives in time to prevent confused questions that a later and better document would have answered. Fewer tickets and better documentation are different outcomes, and a review measuring one has told you about one — which matters if you are about to standardise a process on the strength of it.

**Question 8 (harder)** — Statement: "The review recommends making alongside-release publishing standard." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The review recommends that the portal team *consider whether* it should be standard — a recommendation to evaluate, including deciding against. The statement asserts a recommendation to adopt, which was not made, so False rather than Cannot Say. At your level you are likely to be both a recipient of this and the person who writes what the organisation did about it, so misreading commits you to standardising something nobody asked for and then reporting delivery against it — which is how processes acquire the appearance of a mandate they never had.

*Passage C — for Questions 9 to 12*

"Documentation for a public API must state the endpoint, method, required and optional parameters with types, the response schema, and all error codes the endpoint can return. Where an endpoint is deprecated, documentation must state the deprecation date and the recommended alternative. Code samples must be executable as written against the documented version. Documentation must be reviewed whenever the endpoint changes, and at least annually."

**Question 9 (easy)** — Statement: "Documentation must list all error codes an endpoint can return." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The first sentence requires all error codes the endpoint can return, and the statement restates it. True. Worth noting why the requirement is absolute: an undocumented error code is one an integrator cannot handle, producing clients that work in testing and fail in production when an unanticipated response arrives. It is also the section most commonly incomplete, usually because a writer documents the errors they encountered rather than the ones the endpoint can produce — which is a template and access problem for you rather than a diligence problem for them.

**Question 10 (moderate)** — Statement: "A sample working against the current version but not the documented version satisfies the requirement." True, False or Cannot Say?

**Correct answer: False**

**Explanation:** The requirement is that samples are executable *against the documented version*. A sample working only against a different version fails that. False. The scenario is entirely realistic: documentation for version 2 gets samples tested against version 3, because that is what the writer had running, and every integrator still on version 2 — the audience for that documentation — finds the sample fails. The requirement names the version specifically because this is the error it exists to prevent, and it is one your review process should be checking rather than assuming.

**Question 11 (harder)** — Statement: "Documentation reviewed eleven months ago, with no endpoint changes since, is compliant." True, False or Cannot Say?

**Correct answer: True**

**Explanation:** The requirement has two limbs — review on change, and at least annually. With no changes the first is not triggered, and eleven months is within the annual limit, so both are satisfied and the statement follows. True. Contrast the structure that produces a Cannot Say: had the passage not told you whether the endpoint changed, the case would be undetermined. Here both facts are supplied, so the compound condition can be fully evaluated. Reading which facts you have, rather than treating every compound condition as indeterminate, is what the item tests.

**Question 12 (harder) — Main point**

Which best captures the main point of Passage C?

- A) Documentation must list all error codes.
- B) API documentation must be complete, executable and current — specifying the interface fully including errors, giving deprecation dates and alternatives, containing samples that run against the version documented, and being reviewed on change and at least annually.
- C) Code samples must be executable.
- D) Documentation must be reviewed annually.

**Correct answer: B**

**Explanation:** The main point must cover the whole passage while adding nothing. Options A, C and D are each true of one provision, and D drops the change-triggered review. Option B captures the four requirements and names the logic joining them: an integrator relies on documentation as a contract, so it must describe the interface fully, work when followed, and not describe a system that no longer exists. Note that B preserves "against the version documented" and both review triggers — a summary dropping either is one your team could follow and still fail the requirement, which is the test of whether a summary is usable.

### Preparation tips

- **Read "may", "should" and "must" as terms of art, and set a house convention for rendering them.**
- **Distinguish "will not be rejected for this reason" from "will be accepted".**
- **Treat a specification's silence as a gap to raise, not a behaviour to infer.**
- **Trust Cannot Say.** It identifies what somebody must answer before your team writes.
- **Check which facts a compound condition supplies.** Not every compound is indeterminate.
- **Separate "consider whether X" from "recommend X".** You may be writing the record and the process.
- **Keep version qualifiers in summaries.**
- **Notice when the argument you want rests on a confounded finding.** The honest one is usually available.

### Common pitfalls to avoid

- **Supplying the behaviour you would expect.** The characteristic error of an experienced writer.
- **Rendering "should" as a requirement.**
- **Documenting behaviour outside a stated window.**
- **Promising acceptance when a passage rules out one rejection.**
- **Marking True on a claim that would support a process you favour.**
- **Treating a proxy outcome as the thing itself.** Fewer tickets is not better documentation.
- **Letting samples be tested against whatever version is running.**
- **Dropping a review trigger when summarising a requirement.**

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks what you would do. There is no passage to parse and no arithmetic. You get a dilemma of the kind your role produces, four or five candidate responses, and a question asking which is most effective and often which is least.

This section measures whether your judgement matches what the profession considers good practice at your level. Your role places you as an expert practitioner directing a team of technical writers, assuring quality across teams, standardising tools and processes, working with technology leaders and senior stakeholders to resource teams and resolve problems, and promoting the discipline.

Three features distinguish your level.

Most of what you achieve happens through other people. An option solving a problem through your personal intervention is usually second-best, because it does not survive your absence and does not scale past your calendar.

Your function is chronically under-resourced because its absence is invisible. Documentation that does not exist produces support tickets, integrator delay and abandoned onboarding, and none of those arrive labelled as a documentation problem. That makes options bringing evidence in other people's currencies systematically stronger than options asserting importance.

You absorb pressure downwards. When a technology lead tells a writer their documentation is blocking a release, the writer should not be holding that line.

Four principles carry most scenarios. Accuracy is not negotiable in the way clarity is. Work through engineers rather than around them. Ask who maintains it. And fix the mechanism rather than the document.

### How this assessment maps to your role

The judgement dimensions map onto your named skills:

- **Directing a team** maps to **User-centred content design**, where you oversee teams' work and are accountable for high quality content.
- **Standardising** maps to your role level's named standardisation of tools, ways of communicating and processes.
- **Resourcing and resolving problems** maps to **Stakeholder relationship management**, where you influence and negotiate with senior stakeholders.
- **Capability development** maps to **User-centred content design**, where you identify gaps in skills and help teams grow.
- **Promoting the discipline** maps to your role level's named promotion and community engagement.
- **Strategic alignment** maps to **Strategic thinking**.

### Practice questions

**Question 1 (easy) — A writer under pressure**

A writer tells you a technology lead is insisting documentation ships with a release despite an unverified process, and has implied the writer is blocking it. What is the most effective response?

- A) Tell the writer to hold the line.
- B) Establish with them what can be verified in the time available and what cannot, then take the conversation with the technology lead yourself — offering to publish the verified parts with the unverified section marked and dated rather than presenting it as all or nothing.
- C) Escalate.
- D) Approve publication.

**Correct answer: B. Least effective: D**

**Explanation:** Two things must happen: unverified content does not ship as verified, and the writer is not left in a standoff with a technology lead. Option B does both, and the partial-publication offer is what makes it succeed — the lead's real need is that something ships with the release, and "here is what we can stand behind, and here is what is marked as unverified" usually satisfies it while an all-or-nothing refusal does not. Taking the conversation yourself is your job. Option D is least effective, publishing unverified process documentation, which is the specific failure that costs a documentation set its credibility permanently. Option A leaves a writer refusing a technology lead by proxy. Option C escalates before attempting a resolution available to you.

**Question 2 (easy) — A standard nobody follows**

You introduced a documentation template a year ago. Teams do not use it, describing it as too heavy. What is the strongest approach?

- A) Reissue it with a message.
- B) Review recent documentation with the teams to establish which sections are genuinely unnecessary for their content type and which are being skipped because the information is hard to get, then cut the first and solve the second — since a template that requires information nobody can obtain will be abandoned whatever its merits.
- C) Mandate its use.
- D) Run training on the template.

**Correct answer: B. Least effective: A**

**Explanation:** A template nobody uses has already failed, and reissuing changes only the date. Option B treats the objection as data and distinguishes two causes with different remedies: sections that are genuinely superfluous for a content type should be cut, and sections skipped because the information is unavailable — error codes being the usual example — need an access fix rather than a template change. Getting that distinction wrong means either cutting a field that matters or leaving a requirement people cannot meet. Option A is least effective, the purest form of appearing to act. Option C mandates something people have told you is unworkable, producing completed-and-empty sections. Option D is useful and insufficient alone.

**Question 3 (easy) — Conditions for the team**

Your four writers are each embedded with a different engineering team, spend most of their time on reactive requests, have no shared review practice, and one has left in six months. What is the strongest response?

- A) Discuss workload with each engineering team.
- B) Treat it as structural: establish a shared review routine so writers see each other's work, protect time for planned rather than reactive work, and change how they are deployed if single embedding means nobody has a peer.
- C) Recruit a replacement.
- D) Introduce a wellbeing initiative.

**Correct answer: B. Least effective: C**

**Explanation:** Writers embedded singly with no shared practice is a structural pattern with two distinct costs: the people have nobody to learn from, and the work has nobody checking it — and in technical writing peer review catches a specific and important class of error, since a second writer reading a draft asks the questions an integrator would ask. Option B addresses both. Option C is least effective, recruiting into conditions that produced the departure and, in a small discipline, into a role whose reputation travels. Option A addresses symptoms individually and leaves each writer negotiating alone with the team they depend on. Option D treats a design-of-work problem as morale.

**Question 4 (moderate) — Assuring across teams**

A team you do not manage has published API documentation with a wrong parameter name. Integrators are copying it. What is most effective?

- A) Correct it yourself if you can.
- B) Contact the writer and their lead immediately with the specific error, agree who corrects it and when, and ask whether the same parameter appears elsewhere in their set — while making clear that a wrong name in a copied sample is now in integrators' codebases.
- C) Raise it at the writing community.
- D) Report it to the technology lead.

**Correct answer: B. Least effective: C**

**Explanation:** A wrong parameter name in a published sample is live and propagating, because developers paste samples rather than reading them. Option B moves fast, goes to the people who can fix it, and asks the question that distinguishes a lead's response — errors of this kind are rarely isolated, since a writer who used a wrong name once has probably used it consistently. Option C is least effective, deferring a live error to a scheduled forum and broadcasting a team's mistake before they can fix it, which costs their cooperation. Option A bypasses the people responsible and may exceed your permissions. Option D escalates before asking.

**Question 5 (moderate) — Making the resourcing case**

You need a fourth writer. Your technology director believes engineers can write their own documentation. What is most effective?

- A) Explain what technical writers do.
- B) Lead with evidence in their currency — integration ticket volume and cost, the measured fall after a specific documentation intervention, and the engineer time currently spent answering questions your team could absorb — then set out what a fourth writer would take on and what you would stop doing without one.
- C) Point to the service standard.
- D) Show examples of poor engineer-authored documentation.

**Correct answer: B. Least effective: D**

**Explanation:** A director who believes engineers can write documentation has already discounted the premise, and explaining the discipline confirms their view that this is a preference. Option B inverts the order: establish the cost in figures they already use, then price the ask, and — the part that makes it credible — name what you would stop doing, since a lead who claims everything is essential is not making a trade-off, they are making a demand. The engineer-time element is particularly effective with a technology director, because it converts your bid into a saving in a resource they care about more than yours. Option D is least effective, criticising the work of the director's own engineers, which makes the conversation about their team's competence and guarantees resistance. Option C invokes compliance, which wins a minimum and never wins resource.

**Question 6 (moderate) — A recurring gap across teams**

Documentation across five teams consistently omits error codes. Each writer says engineering does not give them the information. What is most effective?

- A) Remind writers that error codes are required.
- B) Accept the diagnosis they have given you: five writers reporting the same access problem means the information route is the issue, so negotiate once with technology leadership for a way writers can obtain error behaviour — access to the code, a required field in the API specification, or a standing question in release planning.
- C) Add error codes to the review checklist.
- D) Have writers document the errors they can find.

**Correct answer: B. Least effective: A**

**Explanation:** Five writers giving the same explanation is good diagnostic information, and it is an access problem rather than a diligence one. Option B does the thing only you can: negotiating once with technology leadership on all five writers' behalf, rather than leaving five people to have the same losing conversation separately. The three routes it names are worth knowing because one of them is usually easy — error responses are frequently already in the API specification and simply not surfaced to writers. Option A is least effective, telling five writers a requirement they know and cannot meet, which also teaches them that reporting a blocker gets them a reminder. Option D institutionalises incomplete error documentation, which is worse than none because it looks complete. Option C adds a check for a gap the system creates.

**Question 7 (moderate) — Standardising tools**

Your writers use three documentation tools inherited from their engineering teams. What is most effective?

- A) Standardise on one immediately.
- B) Establish what the fragmentation actually costs — whether writers can cover for each other, whether templates are maintained three times, whether shared style changes need three implementations — and standardise only if the cost is real, since the tools belong to engineering teams and changing them is a substantial ask.
- C) Leave it.
- D) Standardise on the most popular.

**Correct answer: B. Least effective: A**

**Explanation:** Standardisation is named in your role and is not automatically correct, and this case has a specific complication: documentation tooling is usually part of an engineering team's own toolchain, so standardising means asking three teams to change something they own and maintain. That requires a reason proportionate to the ask. Option B establishes whether one exists, and the tests it names are the right ones — cover, duplicated maintenance and change cost are where fragmentation actually hurts. Option A is least effective, paying a substantial political cost without establishing the benefit, and it is the kind of early initiative that consumes the goodwill a new lead needs. Option D picks by popularity rather than need. Option C forgoes the question.

**Question 8 (harder) — Documentation nobody will maintain**

A programme asks your team to produce detailed documentation for an internal platform that changes weekly and has no product owner. What is most effective?

- A) Produce it as asked.
- B) Establish who will keep it current before committing — and if nobody will, propose the alternative that survives: a short overview that ages slowly plus generated reference from the platform's own configuration, rather than a detailed guide that will be wrong within two months and will then mislead people who trust it.
- C) Decline.
- D) Produce a shorter version.

**Correct answer: B. Least effective: A**

**Explanation:** Documentation has a maintenance cost invisible at the moment of writing and inevitable afterwards, and detailed documentation of a weekly-changing platform with no owner is a liability being requested in good faith. Option B asks the determining question and — crucially — offers the alternative that works, because declining without one gets you overruled or resented. Short conceptual material ages slowly, and generated reference cannot drift, so the combination delivers most of the value with a fraction of the decay. Option A is least effective, committing your team's capacity to producing something that will actively mislead. Option D reduces the burden without addressing ownership. Option C declines a legitimate need without a route.

**Question 9 (harder) — Promoting the discipline**

You are asked to explain to a technology leadership group why technical writing is a distinct discipline rather than something any good communicator can do. What is most effective?

- A) Explain the skills involved.
- B) Show it: take a real page from their own estate, show what an integrator hits, and show the version that answers the question they actually arrive with — then name what the writer had to know and have access to in order to produce it.
- C) Cite industry practice.
- D) Present the ticket data.

**Correct answer: B. Least effective: A**

**Explanation:** An audience that believes any good communicator can do this has never seen the difference demonstrated, and demonstration works where explanation does not — particularly with a technology audience, who will recognise the failure mode immediately once it is in front of them in their own documentation. Option B also names the part that is genuinely hard and invisible: the writer had to read the code, know what an integrator does at that moment, and have an environment to verify in. Option A is least effective for the reason it feels natural, because a list of skills is exactly what somebody who thinks writing is easy will discount. Option D is strong and is the resourcing argument rather than the discipline argument; it establishes that documentation matters without establishing that it needs specialists.

**Question 10 (harder) — A strategic misalignment**

Your organisation is moving to an API-first model. Your team spends most of its capacity on internal process documentation because no other function will write it. What is most effective?

- A) Continue; the work is needed.
- B) Surface it as a resourcing question rather than absorbing it: set out what proportion of capacity goes on internal process documentation, what will not be done for the API programme as a result, and ask where the organisation wants the capacity — because silently absorbing work nobody owns means the misalignment is invisible and permanent.
- C) Redirect the team to API documentation.
- D) Ask for more writers.

**Correct answer: B. Least effective: A**

**Explanation:** Your team has become the place unowned documentation lands, which is a common fate for a small competent function and is invisible until somebody counts. Option B makes the trade explicit and puts the decision where it belongs, and the framing matters — this is not a complaint but a capacity allocation question, and presenting it with the proportions attached makes it answerable. Option A is least effective, absorbing the work silently, which guarantees the misalignment persists and that your team is later criticised for not supporting the strategy. Option C redirects unilaterally and leaves internal documentation undone, which somebody will notice in a way that reflects on you. Option D asks for resource before establishing what the current resource should do.

**Question 11 (harder) — A flaw in something you standardised**

Six months ago you introduced a template now used across the organisation. You realise it has no field for error codes, and error documentation has become patchier since. What should you do?

- A) Add the field.
- B) Add the field, tell the teams that documentation produced with the template may be missing error codes, identify which pages need retrofitting, and ask why the template review did not catch a missing section that is among the most important in API documentation.
- C) Add it quietly.
- D) Note it for the next template review.

**Correct answer: B. Least effective: C**

**Explanation:** A template used across an organisation propagates its gaps into everything produced with it, so this is not one omission but six months of documentation. Option B does the four things that matter: fixes it, tells the people whose documentation is affected since they cannot know otherwise, scopes the retrofit, and asks the question specific to your level. That last part is the only element preventing recurrence, and the answer is usually that the template was reviewed by writers against style rather than against the completeness requirements of the content type — which is a review criterion you can change. Option C is least effective, leaving six months of incomplete documentation undiscovered while creating a record suggesting the problem was handled. Option A does the same more openly. Option D defers a compounding problem.

**Question 12 (harder) — Cross-government contribution**

Your team has developed an approach to documenting authentication flows that works well. You know other departments face the same problem. What is most effective?

- A) Use it internally.
- B) Share it through the cross-government community with the reasoning, the evidence, and an honest note on where it did not work — and offer to help anyone adapting it, accepting that others may improve it.
- C) Publish it as a cross-government standard.
- D) Mention it to writers you know in other departments.

**Correct answer: B. Least effective: A**

**Explanation:** Your role names promoting the discipline and engaging with the cross-government community, and authentication is documented badly nearly everywhere, so one tested approach is worth considerably more than several departments arriving at their own. Option B shares it well, and the honest note about where it did not work is what prevents the approach being adopted into contexts it does not fit — a pattern suited to token-based flows may be wrong for certificate-based ones, and saying so is what makes it usable rather than merely available. Option A is least effective, keeping a solution while other departments repeat the work. Option C publishes as a standard something one team has tested. Option D helps a few people and bypasses the mechanism built for exactly this.

### Preparation tips

- **Offer partial publication rather than all or nothing.** It usually satisfies the real need.
- **Distinguish template sections that are unnecessary from ones people cannot fill.**
- **Negotiate once on the whole team's behalf.** Five writers having the same losing conversation is a leadership failure.
- **Establish the cost of fragmentation before standardising something you do not own.**
- **Ask who maintains it, and offer the alternative that survives.**
- **Demonstrate rather than explain when the audience discounts the premise.**
- **Surface absorbed work as a capacity question.** Silently absorbing it makes it permanent.
- **Name what you would stop doing when asking for resource.**

### Common pitfalls to avoid

- **Publishing unverified content under release pressure.**
- **Reissuing a template teams have told you is unworkable.**
- **Reminding writers of a requirement they cannot meet.**
- **Criticising engineers' documentation to a technology director.**
- **Standardising a toolchain you do not own without a proportionate reason.**
- **Committing capacity to documentation nobody will maintain.**
- **Absorbing unowned work silently.**
- **Fixing a template without telling the teams whose documents used the broken version.**

## Conclusion

You have reached the end, and it is worth registering the scale: forty-eight questions across four assessment types, with the reasoning worked through on each. That is a substantial piece of professional preparation and more than most people at your level undertake.

Look back at the ground. In the cognitive section you read a missing error section as an access problem rather than a diligence one, found what three recurring gaps had in common, preferred generation to writing where a source of truth existed, established the cost of tool fragmentation before standardising, and scoped an audit's findings to what its method could support. In the numeric section you annualised and costed before arguing for resource, quoted the addressable subset rather than the total, treated zero traffic as ambiguous, tested attribution before claiming an intervention worked, and refused to sign a business case whose headline exceeded its own evidence. In the verbal section you read "may", "should" and "must" as terms of art, declined to promise acceptance when a passage ruled out one rejection, treated silence as a gap to raise, and refused to mark True on a confounded finding that would have supported a process you favour. And in the situational judgement section you offered partial publication under release pressure, negotiated once with technology leadership on five writers' behalf, demonstrated the discipline rather than explaining it, and surfaced absorbed work as a capacity question.

Two threads run through it. The first is that accuracy in your discipline has a hard edge: readers copy what your team writes into systems that then work or do not, and a wrong parameter is a different order of error from an unclear sentence. The second is that your function's value is invisible by construction — documentation that works produces no ticket, no complaint and no evidence of itself — which is why so many of the strongest answers here involve converting an invisible cost into a number somebody else already uses.

A word about your level. Directing a small function in a discipline most people believe they could do themselves means you spend more time than you would like establishing that the work is work. The way through is not advocacy but evidence and demonstration: ticket volumes, measured falls, and a real page from somebody's own estate shown alongside the version that answers the question integrators actually arrive with. Those change minds; explanations of the discipline do not.

If you want to build on this, a few things repay effort more than rereading. Integrate with one of your organisation's APIs using only its documentation, on a clean machine, and note every point where you had to read source. Read a month of integration tickets and find the pages that should have answered them. Ask each of your writers what they cannot verify and why. Look at what your most accurate writer does that the others do not, before assuming it is skill. And take your ten most-used pages and ask who will notice when they go out of date.

Finally, for the day itself. An assessment samples your reasoning on one morning under artificial conditions. It is not a verdict on your judgement or your career. Read the stem twice, read "should" as "should", find the denominator, trust Cannot Say, and remember that at your level the strongest answer is usually the one that fixes the mechanism and can be defended with a figure.

Good luck. Go carefully, verify by doing, and keep asking who will maintain it.
