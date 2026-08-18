# Solution Architect (Associate Solution Architect) - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as an associate solution architect working within the UK Government Digital and Data profession. Whether you are preparing for a formal assessment, exploring a promotion opportunity, or simply want to sharpen the thinking skills you use every day, this document is here to help you practise, reflect, and build your confidence.

Psychometric assessments are structured exercises that measure the mental skills and judgement you bring to your work. They are widely used across the UK public sector, both in recruitment and in professional development, because they give a fair, consistent picture of how someone thinks, rather than relying only on interviews or CVs. For an associate solution architect, these assessments matter because your role sits at the meeting point of technology, people, and organisational goals. You help frame problems, support the design of solutions, communicate with technical and non-technical stakeholders, and learn how decisions are made and governed. All of that depends on clear reasoning, careful reading, comfort with numbers, and sound judgement in tricky situations.

This document is organised into four main assessment sections, each matched to your role and level:

1. **Workplace job-specific cognitive assessment** - practises pattern recognition, logical deduction, error checking, and prioritisation using the kinds of artefacts you handle, such as architecture diagrams, design documents, and technology roadmaps.
2. **Workplace job-specific numeric reasoning assessment** - practises working with budgets, capacity figures, licensing costs, and performance metrics that appear in real solution design work.
3. **Workplace job-specific verbal reasoning assessment** - practises reading dense material carefully, such as government standards, governance policies, and stakeholder emails, and drawing only the conclusions the text supports.
4. **Workplace job-specific situational judgement assessment** - practises choosing effective actions in realistic workplace dilemmas involving supervisors, stakeholders, and multidisciplinary teams.

Each section explains what the assessment measures, maps it to the specific skills in your role profile, gives you a generous set of practice questions with full worked explanations, and finishes with preparation tips and common pitfalls to avoid.

Here is the best way to use this guide. First, read each "About this assessment" section so you understand the format. Then attempt the practice questions honestly, without peeking at the answers. Check your reasoning against the explanations, not just whether you got the right letter. Where you went wrong, ask yourself why, and note the pattern. Finally, revisit the preparation tips a few days before any real assessment. Remember: as an associate, you are at the start of your architecture journey, and nobody expects perfection. These exercises are about growth. Take your time, be kind to yourself, and enjoy the practice.

## Advisory

"This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff."

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment is a targeted psychometric test that measures the exact mental processes needed for your role, rather than abstract intelligence. Instead of puzzles about shapes or dictionary words, it uses practical scenarios and data drawn from the everyday work of an associate solution architect: architecture diagrams, design documents, standards checklists, technology roadmaps, and stakeholder requirements. The aim is simple - to predict how well you can spot patterns, follow logical chains, catch errors, prioritise tasks, and solve problems in the situations you actually face at work.

These assessments are usually delivered online, timed, and last between 15 and 30 minutes. You will typically see multiple-choice questions, and your results are compared against a benchmark group rather than judged in isolation. Many platforms give you a short set of ungraded practice questions first so you can get used to the interface, and some adapt the difficulty of questions based on your previous answers. Employers usually receive a breakdown of your speed versus your accuracy rather than a single raw score, so working carefully matters just as much as working quickly.

Because you are at associate level, questions calibrated for you will focus on well-understood technology, managed levels of complexity, and situations where you work with the support of more experienced architects. You are not expected to make enterprise-wide strategic calls; you are expected to reason clearly, notice details, and support your team well. That is exactly what this practice section helps you build.

### What it measures for your role

Each cognitive dimension maps directly onto skills named in your role profile:

- **Pattern recognition** supports your skill in **Technical design throughout the life cycle**, where you "work with well-understood technology and identify appropriate patterns". Spotting that a new problem resembles a known integration pattern, or that three services share the same failure mode, is core architecture thinking.
- **Logical deduction** supports **Making architectural decisions**, where you "describe the reasoning behind architectural design decisions" and "gather information to inform decisions". If A depends on B, and B is being decommissioned, what follows for A? Architects reason like this constantly.
- **Error checking** supports **Architecture communication** and compliance with standards and governance. You will review design documents, diagrams, and decision records, and you need to notice when a document contradicts itself or a diagram does not match its description.
- **Prioritisation** supports **Problem definition and shaping**, where you "help to frame a problem characterised by managed levels of complexity, complication, or risk". Deciding which constraint matters most, or which task to do first under supervision, is a daily judgement.
- **Problem solving** supports **Architect for the whole context**, where you "identify relevant information that can inform your architectural work, such as strategies, roadmaps, policies and technical trends", and combine those inputs into sensible options.

The questions below use artefacts you genuinely handle: solution options papers, environment diagrams, decision logs, technology roadmaps, and governance checklists, all set in a UK government digital context.

### Practice questions

**Question 1 (easy) - Pattern recognition in environments**

Your team manages four environments for a citizen-facing licensing service. The deployment sequence so far has been: Development, then Test, then Staging, then Production. A release note says version 2.4 has passed Development and Test. According to the established pattern, which environment should version 2.4 be deployed to next?

- A) Production
- B) Staging
- C) Development
- D) Test

**Correct answer: B) Staging.**

**Explanation:** The sequence follows a fixed progression: Development, Test, Staging, Production. Version 2.4 has completed the first two stages, so the next stage in the pattern is Staging. Option A skips a stage, which would break the governance pattern your team complies with. Options C and D are stages already completed. In real work, recognising and respecting release patterns is part of complying with standards and governance - deployments that skip Staging are a classic source of production incidents, and an associate who spots a skipped stage adds real value.

**Question 2 (easy) - Logical deduction from constraints**

A senior architect tells you: "All services that store citizen personal data must complete a Data Protection Impact Assessment (DPIA) before go-live. The appointment-booking service stores citizen personal data." Which conclusion must be true?

- A) The appointment-booking service has already completed a DPIA
- B) The appointment-booking service must complete a DPIA before go-live
- C) The appointment-booking service cannot go live
- D) All services must complete a DPIA before go-live

**Correct answer: B.**

**Explanation:** This is a straightforward logical syllogism. The rule applies to all services storing citizen personal data; the appointment-booking service is one of those; therefore the rule applies to it. Option A confuses "must complete" with "has completed" - we know the obligation exists, not whether it has been met. Option C goes too far: the service can go live once the DPIA is done. Option D overgeneralises: the rule stated applies only to services storing citizen personal data, not to all services. Careful deduction like this underpins your skill in describing the reasoning behind architectural decisions.

**Question 3 (moderate) - Error checking a design document**

You are proofreading a solution design document before it goes to the architecture review board. The document states:

1. "Section 2: The solution will use the department's approved cloud platform and managed PostgreSQL database service."
2. "Section 4: All data will be stored in the on-premises Oracle database to minimise change."
3. "Section 5: Database backups will use the cloud platform's automated snapshot feature."

Which pair of statements is inconsistent?

- A) Sections 2 and 4
- B) Sections 2 and 5
- C) Sections 4 and 5
- D) Both A and C

**Correct answer: D) Both A and C.**

**Explanation:** Section 2 says data lives in a cloud-managed PostgreSQL database, while Section 4 says all data lives in an on-premises Oracle database - a direct contradiction (pair A). Section 5 then relies on cloud snapshot features, which contradicts Section 4's on-premises claim (pair C). Sections 2 and 5 are consistent with each other, so pair B is fine. Catching contradictions before a governance review saves your team embarrassment and rework, and it is exactly the kind of supporting contribution expected of an associate: you help your team achieve its objectives by making documents watertight before they reach assurance gates.

**Question 4 (moderate) - Prioritisation under supervision**

It is Monday morning. Your supervising solution architect is in workshops all day. You have four tasks:

1. Finish the diagram for Thursday's architecture review board submission (deadline: Wednesday noon for the pack)
2. Respond to a developer's question blocking their work today on which messaging pattern to use
3. Read a new technology trends briefing circulated for general awareness
4. Book a room for next month's community of practice session

What is the most sensible order to tackle them?

- A) 1, 2, 3, 4
- B) 2, 1, 4, 3
- C) 3, 2, 1, 4
- D) 2, 4, 1, 3

**Correct answer: B) 2, 1, 4, 3.**

**Explanation:** The developer's question is blocking someone's work right now, so unblocking them first has the greatest immediate impact on the team - and if the question is beyond your confidence level, your first action is still to engage with it, even if that means gathering the details to escalate. The review board diagram has a hard deadline of Wednesday, so it comes next with plenty of margin. Booking a room is quick and time-sensitive only loosely, so it beats the trends briefing, which is important for staying up to date on technology trends but has no deadline. Option A delays an actively blocked colleague; option C puts general reading before urgent work; option D leaves the deadline-bound diagram too late relative to a trivial admin task. Prioritisation questions reward thinking about impact and deadlines together.

**Question 5 (moderate) - Pattern recognition in incident data**

You review a log of incidents affecting three services over four weeks:

- Week 1: Service A timeout, Service B normal, Service C timeout
- Week 2: Service A normal, Service B normal, Service C timeout
- Week 3: Service A timeout, Service B normal, Service C timeout
- Week 4: Service A normal, Service B normal, Service C timeout

Services A and C both call the same legacy address-lookup API; Service B does not. Which statement best fits the pattern?

- A) Service B is the root cause of the timeouts
- B) Service C has an issue every week, and Service A intermittently; the shared legacy API is a plausible common factor worth investigating
- C) The legacy API is definitely the root cause
- D) The timeouts are random and show no pattern

**Correct answer: B.**

**Explanation:** The data shows Service C failing all four weeks and Service A failing alternate weeks, while Service B - the only service not using the legacy API - never fails. That correlation makes the shared API a plausible common factor, which is precisely how an architect frames a hypothesis. Option C overstates the evidence: correlation is a lead, not proof, and saying "definitely" skips the investigation step. Option A contradicts the data - Service B never failed. Option D ignores the clear regularity. Notice the careful wording of B: "plausible" and "worth investigating". Gathering information to inform decisions, rather than jumping to conclusions, is a named behaviour in your Making architectural decisions skill.

**Question 6 (moderate) - Logical deduction with roadmaps**

The department's technology roadmap states: "The legacy document store will be decommissioned in Q3 next year. Any solution going live after Q1 next year must not create new dependencies on the legacy document store." Your team's new casework solution is scheduled to go live in Q2 next year, and one design option uses the legacy document store for file storage. What follows?

- A) The option is acceptable because the store still exists in Q2
- B) The option conflicts with the roadmap rule and needs to change or be justified as an exception
- C) The casework solution must be delayed until Q3
- D) The roadmap must be wrong

**Correct answer: B.**

**Explanation:** The rule covers any solution going live after Q1 next year; Q2 is after Q1; therefore the rule applies, and the design option that creates a new dependency on the legacy store conflicts with it. Option A confuses physical availability with policy compliance - the store existing does not make new dependencies permissible. Option C invents a remedy the rule does not require; the sensible response is to change the design or seek a formally governed exception. Option D is not a deduction at all. This is a classic example of your Architect for the whole context skill: roadmaps are exactly the "relevant information that can inform your architectural work", and spotting a conflict early is far cheaper than discovering it at a governance review.

**Question 7 (moderate) - Error checking a diagram against its description**

A context diagram shows: Citizen -> Web Frontend -> API Gateway -> Booking Service -> Payments Provider. The accompanying text says: "The citizen interacts with the web frontend, which calls the booking service directly. The booking service then calls the payments provider through the API gateway." How many discrepancies are there between the diagram and the text?

- A) None
- B) One
- C) Two
- D) Three

**Correct answer: C) Two.**

**Explanation:** Compare each hop. Discrepancy one: the diagram routes the frontend through the API gateway to the booking service, but the text says the frontend calls the booking service "directly". Discrepancy two: the diagram shows the booking service calling the payments provider directly, but the text says that call goes "through the API gateway". The citizen-to-frontend hop matches in both. Diagram-versus-text mismatches are among the most common defects in architecture documents, and they cause real confusion for delivery teams. Your Architecture communication skill includes creating and using different architecture representations - and those representations must agree with each other, or stakeholders will trust neither.

**Question 8 (hard) - Multi-step problem solving**

Your team must choose a file-scanning approach for citizen document uploads. Constraints gathered so far:

1. Security policy: all uploads must be virus-scanned before being stored in the case system.
2. Performance requirement: citizens must receive upload confirmation within 5 seconds.
3. The approved scanning service takes 8-20 seconds per file.
4. The case system rejects unscanned files.

Which design option satisfies all constraints?

- A) Scan the file synchronously, then confirm the upload once scanning completes
- B) Store the file directly in the case system and scan it afterwards
- C) Confirm receipt into a quarantine area within 5 seconds, scan asynchronously, then move the file into the case system only after a clean scan
- D) Ask the security team to waive the scanning requirement

**Correct answer: C.**

**Explanation:** Work through the constraints. Option A fails constraint 2: scanning takes 8-20 seconds, so synchronous confirmation cannot happen within 5 seconds. Option B fails constraints 1 and 4: the file would enter the case system unscanned, which policy forbids and the system rejects. Option D is not a design solution and abandons a legitimate security control. Option C separates "we have received your file" from "your file is accepted", using a quarantine-then-promote pattern: the citizen gets fast confirmation, scanning happens asynchronously, and only clean files reach the case system. This is a well-understood pattern for exactly this problem - identifying appropriate patterns for well-understood technology is a named behaviour at your level. Notice how the right answer satisfies every constraint rather than trading one off silently.

**Question 9 (hard) - Deduction across multiple rules**

Three governance rules apply to your solution:

1. If a service handles payments, it must complete a security review.
2. If a service completes a security review, it must have a named technical owner.
3. Services without a named technical owner cannot be deployed to production.

Your service handles payments and currently has no named technical owner. Which statement must be true?

- A) The service can be deployed to production once the security review is complete
- B) The service cannot currently be deployed to production, and it must both complete a security review and gain a named technical owner
- C) The security review is optional because there is no technical owner
- D) The service does not handle payments if it has no technical owner

**Correct answer: B.**

**Explanation:** Chain the rules. Rule 1: payments means a security review is required. Rule 3: no named technical owner means no production deployment - which applies right now. Rule 2 tells us the review itself requires a named owner, reinforcing that the owner must be appointed. So the service is currently blocked from production and needs both the review and the owner - exactly option B. Option A ignores the owner requirement. Option C reverses the logic of rule 2: the review requiring an owner does not make the review optional. Option D is a non sequitur. Multi-rule deduction like this mirrors real architectural governance, where several policies interact and the architect must state clearly what is required and why - the heart of describing the reasoning behind decisions.

**Question 10 (hard) - Prioritising risks**

Your supervising architect asks you to list which of four identified risks should be raised first at the weekly risk review. The risks are:

1. A third-party API your solution depends on will retire its current version in 18 months
2. The solution's single database instance has no failover, and the service goes live to the public in 3 weeks
3. A junior developer prefers a different code formatting style to the team standard
4. The project wiki contains some out-of-date diagrams

Which risk should be raised first?

- A) Risk 1
- B) Risk 2
- C) Risk 3
- D) Risk 4

**Correct answer: B) Risk 2.**

**Explanation:** Prioritise by combining impact and urgency. Risk 2 combines high impact (a public service failing with no failover affects citizens directly) with high urgency (go-live in 3 weeks leaves little time to fix it). Risk 1 is genuinely important but has an 18-month horizon, so it is raised and tracked, not urgent. Risk 3 is a team-working preference, not an architectural risk - it belongs in a team retrospective, not a risk review. Risk 4 matters for communication quality but has low immediate impact. Managing risks "in a transparent way" is in your role description: transparency means raising the right risks at the right forum with honest severity, not burying the serious one among trivia.

**Question 11 (moderate) - Spotting the odd one out**

Your team catalogues integration approaches used across the department. Which of the following is NOT an integration pattern?

- A) Publish-subscribe messaging
- B) Request-response API call
- C) Batch file transfer
- D) Quarterly budget review

**Correct answer: D) Quarterly budget review.**

**Explanation:** Publish-subscribe, request-response, and batch file transfer are all recognised ways for systems to exchange data - classic integration patterns you will meet constantly when working with well-understood technology. A quarterly budget review is a financial governance activity, not a way systems communicate. This question looks simple, but classification skills matter: architects constantly sort information into categories (pattern versus principle, requirement versus constraint, risk versus issue), and muddled categories lead to muddled documents. If you found this easy, excellent - it means your mental filing system for architecture concepts is forming well.

**Question 12 (hard) - Working backwards from an outcome**

A design review found that a proposed solution fails the department's accessibility standard because a document-preview feature relies on a third-party viewer that does not support screen readers. The team has three weeks before the review board reconvenes. Which sequence of steps is the most logical way to resolve this?

- A) Remove the accessibility requirement from the solution scope
- B) Identify alternative viewers or native rendering approaches that meet the standard, assess them against the other constraints, recommend one with reasons, and update the design
- C) Keep the current viewer and add a note saying accessibility will be fixed later
- D) Escalate to the review board that the standard is too strict

**Correct answer: B.**

**Explanation:** The failure is specific (the viewer lacks screen reader support), so the logical response is to generate options that fix that specific failure, evaluate them against all constraints (not just accessibility), and document the reasoning - which is literally your Problem definition and shaping skill: "help to create options for solving problems at an appropriate level of detail". Option A abandons a mandatory standard; accessibility is a legal requirement for UK public sector services, not an optional scope item. Option C defers a known compliance failure, which governance boards rightly reject. Option D challenges the standard rather than the design, without any evidence the standard is at fault. The disciplined move - options, assessment, recommendation, updated design - is the pattern to internalise.

**Question 13 (easy) - Sequence completion**

Your supervising architect describes the standard lifecycle your documents follow: Draft, then Peer review, then Architecture review, then Approved, then Published. A document has just completed Peer review. What is its next stage?

- A) Published
- B) Draft
- C) Architecture review
- D) Approved

**Correct answer: C) Architecture review.**

**Explanation:** The lifecycle is a fixed sequence, and the stage after Peer review is Architecture review. Options A and D skip stages, and option B moves backwards. Simple sequence questions like this check that you can hold a process in mind and apply it accurately - the same mental habit you use when complying with standards and governance. In timed assessments, bank easy questions like this quickly and accurately to leave more time for the harder ones.

**Question 14 (moderate) - Combining information sources**

You are helping shape options for replacing a paper-based grant application process. You have gathered: the departmental digital strategy (which mandates "digital by default" services), a policy requiring assisted-digital support for users who cannot use online services, and a technical trends briefing noting the department's growing use of its existing forms platform. Which option best reflects all three inputs?

- A) An online application built on the existing forms platform, with a telephone-assisted route for users who need support
- B) An online-only application built on a brand-new custom platform
- C) Keeping the paper process but scanning the forms into a document store
- D) A telephone-only service, since some users cannot get online

**Correct answer: A.**

**Explanation:** The skill being tested is synthesis: combining strategy, policy, and technical trend information into one coherent option - the essence of "identify relevant information that can inform your architectural work". Option A honours the digital-by-default strategy (online application), the assisted-digital policy (telephone-assisted route), and the technical trend (reuse of the existing forms platform). Option B ignores both the assisted-digital policy and the reuse trend, adding cost and excluding users. Option C is not digital by default - scanning paper digitises storage, not the service. Option D inverts the strategy entirely, serving the exception case as the only case. When several legitimate inputs all point somewhere, the strongest option is usually the one that needs no input to be quietly ignored.

### Preparation tips

- **Practise with real artefacts.** Re-read a recent design document or decision log from your team and actively hunt for inconsistencies, just as Question 3 and Question 7 did. This builds error-checking instincts faster than abstract puzzles.
- **Verbalise your deductions.** When you decide something follows from a rule, say the chain out loud: "the rule covers X; this is an X; therefore...". This is also excellent practice for describing the reasoning behind decisions, a named skill at your level.
- **Do a timed warm-up.** Because these tests run to 15-30 minutes, practise a set of 10 questions in 15 minutes so the pace feels familiar. Accuracy under mild time pressure is a trainable skill.
- **Bank the easy marks.** Answer quick questions decisively and flag the hard multi-step ones to revisit. A blocked question costs you two others.
- **Rest and set up well.** Sleep properly the night before, use a quiet room, and complete any ungraded practice questions the platform offers so the interface holds no surprises. As an associate, remember the benchmark reflects your level - you are not being compared to principal architects.

### Common pitfalls

- **Overreaching beyond the evidence.** As in Question 5, choosing "definitely the root cause" when the data supports only "plausible factor". Assessments deliberately include overconfident options.
- **Confusing obligation with completion.** "Must complete a DPIA" does not mean one has been completed. Read modal verbs (must, may, should) with care.
- **Skipping stages in patterns.** When a sequence or lifecycle is given, the answer respects every stage. Options that jump ahead are traps.
- **Losing time on one hard question.** The spec for these assessments notes that speed and accuracy are reported separately, but a single ten-minute struggle still starves every other question of time. Move on and return.
- **Answering from your own workplace instead of the question.** Your department's real release process may differ from the one described. Use only the rules the question gives you.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates how well you analyse, interpret, and make logical decisions using numerical data. It deliberately mimics the data-handling demands of your actual role, focusing on practical business mathematics rather than abstract formulas. For an associate solution architect, that means the numbers architects genuinely meet: hosting and licensing costs, capacity and performance figures, user volumes, project budgets, and comparisons between solution options.

Do not worry if maths is not your favourite subject. These assessments rarely go beyond percentages, ratios, averages, simple cost comparisons, and reading values accurately from tables and charts. Most platforms allow or provide an on-screen calculator, because the real skill being measured is interpretation - extracting the right numbers, applying the right operation, and sanity-checking the result - not mental arithmetic. What makes the tests challenging is the time limit: you typically face strict pacing, so quick and accurate data extraction matters.

Question inputs usually look like the tables in this section: cost comparisons between cloud options, monthly transaction volumes, performance dashboards, or licence pricing tiers. As an associate, the numbers you handle in real life often support a senior architect's options paper - "which option is cheaper over three years?", "will this capacity handle peak demand?" - so the practice below is built around exactly those situations. Being confident with this kind of arithmetic makes you noticeably more useful in design discussions, because you can check claims on the spot rather than taking them on trust.

### What it measures for your role

Numeric reasoning connects to your role profile in specific, practical ways:

- **Commercial perspective** asks you to "show an awareness of government commercial processes". Comparing supplier quotes, understanding total cost of ownership, and spotting when a discount changes a ranking are all numeric skills wrapped in commercial awareness.
- **Making architectural decisions** requires you to "gather information to inform decisions". Much of that information is numeric: latency figures, error rates, storage growth, cost per transaction. An option paper without numbers is opinion; with numbers it is evidence.
- **Problem definition and shaping** includes helping to "create options for solving problems at an appropriate level of detail". Costing options at the right level of precision - not spuriously exact, not hopelessly vague - is a numeric judgement.
- **Working within business and technical constraints** (from your role description) often means working within a budget or a capacity ceiling, both of which are numbers.
- **Technical design throughout the life cycle** involves designs with "managed levels of risk, impact, and complexity" - and sizing that risk and impact frequently involves volumes, percentages, and growth rates.

Every practice question below uses data an associate solution architect in a UK government department could plausibly meet this month.

### Practice questions

**Question 1 (easy) - Reading a cost table**

Your team compares monthly hosting costs for a citizen appointments service across three options:

| Option | Compute | Storage | Support |
|---|---|---|---|
| Cloud A | £1,200 | £300 | £250 |
| Cloud B | £1,050 | £450 | £300 |
| On-premises | £900 | £500 | £600 |

Which option has the lowest total monthly cost?

- A) Cloud A
- B) Cloud B
- C) On-premises
- D) They are all equal

**Correct answer: A) Cloud A.**

**Explanation:** Add each row. Cloud A: 1,200 + 300 + 250 = £1,750. Cloud B: 1,050 + 450 + 300 = £1,800. On-premises: 900 + 500 + 600 = £2,000. Cloud A is cheapest at £1,750. The trap here is anchoring on a single column: On-premises has the cheapest compute (£900), and a rushed reader might pick it. Always total the whole row before comparing - partial costs mislead. This mirrors real options papers, where a headline figure often hides support or storage costs that change the ranking.

**Question 2 (easy) - Percentage increase**

A licensing service handled 40,000 applications last quarter. This quarter it handled 46,000. What is the percentage increase?

- A) 6%
- B) 13%
- C) 15%
- D) 17%

**Correct answer: C) 15%.**

**Explanation:** Percentage increase = (new - old) / old x 100. That is (46,000 - 40,000) / 40,000 x 100 = 6,000 / 40,000 x 100 = 15%. Option A confuses the absolute increase (6,000) with a percentage. Option B comes from dividing by the new figure (6,000 / 46,000 is about 13%) - a very common error; always divide by the original value. Growth figures like this feed directly into capacity planning: if applications grow 15% a quarter, an architect must ask whether the current design can absorb compound growth.

**Question 3 (moderate) - Ratios in team capacity**

Your delivery team has 3 developers for every 1 tester. The programme is scaling the team to 24 developers while keeping the same ratio. How many testers will there be?

- A) 6
- B) 8
- C) 12
- D) 21

**Correct answer: B) 8.**

**Explanation:** The ratio of developers to testers is 3:1, so testers = developers / 3 = 24 / 3 = 8. Option A might come from misreading the ratio as 4:1. Option C halves the developers instead of dividing by three. Option D subtracts 3 rather than dividing. Ratio questions reward writing the relationship down before calculating. In practice, architects meet ratios constantly: requests per instance, records per batch, environments per service - and a design that assumes the wrong ratio fails at scale.

**Question 4 (moderate) - Three-year cost comparison**

Two options for a document-processing capability:

- Option X: £25,000 one-off implementation, then £2,000 per month running costs.
- Option Y: £5,000 one-off implementation, then £2,750 per month running costs.

Over a full three-year period, which option costs less, and by how much?

- A) Option X, by £7,000
- B) Option Y, by £7,000
- C) Option X, by £2,000
- D) Option Y, by £2,000

**Correct answer: A) Option X, by £7,000.**

**Explanation:** Three years is 36 months. Option X: 25,000 + (2,000 x 36) = 25,000 + 72,000 = £97,000. Option Y: 5,000 + (2,750 x 36) = 5,000 + 99,000 = £104,000. Option X is cheaper by 104,000 - 97,000 = £7,000. The commercial lesson: a lower up-front cost (Option Y) can be the more expensive choice once running costs compound - the essence of total cost of ownership, a core idea in government commercial awareness. Spending programmes are usually assessed over multiple years precisely to catch this.

**Question 5 (moderate) - Capacity headroom**

A booking API is provisioned to handle 500 requests per second. Current peak load is 320 requests per second, and the service team forecasts peak load will grow by 25% next year. Will next year's forecast peak fit within current capacity, and what is the forecast figure?

- A) Yes - forecast peak is 400 requests per second
- B) No - forecast peak is 525 requests per second
- C) Yes - forecast peak is 345 requests per second
- D) No - forecast peak is 640 requests per second

**Correct answer: A) Yes - forecast peak is 400 requests per second.**

**Explanation:** Growth of 25% on 320 = 320 x 1.25 = 400 requests per second, which is below the 500 capacity, leaving 100 requests per second of headroom (20% of capacity). Option C adds 25 requests rather than 25%. Option D doubles incorrectly (320 x 2 = 640). Option B mistakenly grows the capacity figure (500 x 1.05) or simply misapplies the numbers. Capacity questions are bread-and-butter for solution architects: the arithmetic is easy, but choosing the right base figure (current peak, not average, not capacity) is where care is needed.

**Question 6 (moderate) - Licence tier pricing**

A software supplier prices user licences in tiers:

| Tier | Users covered | Price per user per year |
|---|---|---|
| 1 | First 100 users | £120 |
| 2 | Next 200 users (101-300) | £90 |
| 3 | Users above 300 | £60 |

Your service needs licences for 350 users. What is the total annual cost?

- A) £21,000
- B) £30,000
- C) £33,000
- D) £42,000

**Correct answer: C) £33,000.**

**Explanation:** Tiered pricing applies each rate only to the users in that band. Tier 1: 100 x £120 = £12,000. Tier 2: 200 x £90 = £18,000. Tier 3: the remaining 50 users x £60 = £3,000. Total: 12,000 + 18,000 + 3,000 = £33,000. Option A applies the cheapest rate to everyone (350 x £60). Option D applies the most expensive rate to everyone (350 x £120). Option B uses a flat middle rate. Tiered (marginal) pricing is extremely common in government software agreements, and misreading it as flat pricing is one of the most frequent commercial errors - worth mastering now, because you will see this table shape again and again.

**Question 7 (moderate) - Reading a performance dashboard**

A monthly service dashboard shows:

| Metric | April | May | June |
|---|---|---|---|
| Uptime | 99.5% | 99.9% | 99.0% |
| Average response time | 420 ms | 380 ms | 510 ms |
| Failed transactions | 1,200 | 800 | 2,100 |
| Total transactions | 600,000 | 640,000 | 700,000 |

Which month had the highest failure rate as a percentage of total transactions?

- A) April
- B) May
- C) June
- D) All months are equal

**Correct answer: C) June.**

**Explanation:** Compute failure rates. April: 1,200 / 600,000 = 0.20%. May: 800 / 640,000 = 0.125%. June: 2,100 / 700,000 = 0.30%. June has the highest rate. The trap is reading only the absolute failure count - June is also highest in absolute terms here, but assessments often reverse that, so always normalise by volume. Notice how the dashboard tells one consistent story: June's uptime dipped and response time rose alongside failures. Reading several metrics together, rather than one in isolation, is exactly how architects gather information to inform decisions about where a design needs strengthening.

**Question 8 (hard) - Cost per transaction**

Using the table in Question 7, and given that the platform's total running cost was £42,000 in April and £49,000 in June, which statement is correct about cost per successful transaction (to three decimal places)?

- A) April cost more per successful transaction than June
- B) June cost more per successful transaction than April
- C) Both months cost the same per successful transaction
- D) It cannot be calculated from the data given

**Correct answer: C) Both months cost the same per successful transaction.**

**Explanation:** Successful transactions = total minus failed. April: 600,000 - 1,200 = 598,800; cost per successful transaction = 42,000 / 598,800 = £0.070 (to three decimal places). June: 700,000 - 2,100 = 697,900; 49,000 / 697,900 = £0.070 (to three decimal places). At the stated precision they are equal. This question rewards following the definition exactly (successful, not total, transactions) and carrying the division through carefully. It also mirrors a genuinely useful architectural metric: unit cost per transaction is how many government platforms judge whether scaling is economical, and an associate who can compute it correctly earns trust fast.

**Question 9 (hard) - Budget allocation with constraints**

A project has a £120,000 budget for its discovery and alpha phases. Rules: discovery may use at most 30% of the budget; at least £10,000 must be held as contingency; the remainder goes to alpha. If discovery uses its full allowance and the minimum contingency is held, how much is available for alpha?

- A) £74,000
- B) £84,000
- C) £96,000
- D) £110,000

**Correct answer: A) £74,000.**

**Explanation:** Discovery maximum: 30% of 120,000 = £36,000. Contingency: £10,000. Alpha = 120,000 - 36,000 - 10,000 = £74,000. Option B forgets the contingency. Option C computes 80% of the budget. Option D subtracts only the contingency. Multi-constraint budget questions reward a systematic layout: list each deduction, subtract in turn, and check the parts sum back to the whole (36,000 + 10,000 + 74,000 = 120,000 - it does). Discovery and alpha phase budgeting is a real feature of UK government agile delivery, so this arithmetic pattern will serve you in genuine planning sessions.

**Question 10 (hard) - Storage growth projection**

A case management system currently stores 2.0 TB of documents. Storage grows by 20% each year, compounding. Approximately how much storage will be needed after three years?

- A) 3.2 TB
- B) 3.5 TB
- C) 2.6 TB
- D) 6.0 TB

**Correct answer: B) 3.5 TB (approximately).**

**Explanation:** Compound growth multiplies each year: 2.0 x 1.2 = 2.4 TB after year one; 2.4 x 1.2 = 2.88 TB after year two; 2.88 x 1.2 = 3.456 TB after year three, which rounds to about 3.5 TB. Option A uses simple (non-compounding) growth: 2.0 + (3 x 0.4) = 3.2 TB - the most common error. Option C stops after one and a half years of growth. Option D triples the base. The architectural point: designs sized on simple growth quietly under-provision, and the gap widens every year. When you see "compounding" or "each year" in a question, multiply repeatedly rather than adding.

**Question 11 (easy) - Averages for reporting**

Response times for five test runs of a new integration were: 210 ms, 190 ms, 250 ms, 230 ms, 220 ms. What is the mean response time?

- A) 210 ms
- B) 220 ms
- C) 225 ms
- D) 230 ms

**Correct answer: B) 220 ms.**

**Explanation:** Sum the values: 210 + 190 + 250 + 230 + 220 = 1,100 ms. Divide by the number of runs: 1,100 / 5 = 220 ms. Option A picks the first value, option D picks a middle-looking value, and option C is a near-miss arithmetic slip. When you report test results to your team, being able to compute and sanity-check a mean quickly keeps discussions grounded. Bonus habit: also glance at the spread (here 190-250 ms) - a mean alone can hide worrying variability, which is why performance requirements often specify percentiles as well as averages.

**Question 12 (hard) - Comparing supplier quotes with discounts**

Two suppliers quote for an API management product for 3 years:

- Supplier P: £40,000 per year, with a 10% discount on the total if all 3 years are paid up front.
- Supplier Q: £35,000 for year one, then £38,000 for each of years two and three, no discount.

Your department will pay up front if it saves money overall. Which is the cheapest arrangement?

- A) Supplier P paid annually - £120,000
- B) Supplier P paid up front - £108,000
- C) Supplier Q - £111,000
- D) Supplier Q - £105,000

**Correct answer: B) Supplier P paid up front - £108,000.**

**Explanation:** Supplier P annually: 40,000 x 3 = £120,000. Supplier P up front: 120,000 x 0.90 = £108,000. Supplier Q: 35,000 + 38,000 + 38,000 = £111,000 (option D miscalculates this). Comparing the true candidates: £108,000 beats £111,000, so Supplier P up front is cheapest. The commercial nuance: without the up-front discount, Supplier Q would win, so payment terms - not just headline prices - decide the outcome. Government commercial processes frequently involve exactly this trade-off, and an associate who can lay the arithmetic out clearly supports the commercial team as well as the architecture.

**Question 13 (moderate) - Proportions of user needs**

User research for a permit service found that of 1,500 research participants, 63% completed the online journey unaided, 24% needed some assistance, and the remainder could not complete it online at all. How many participants could not complete the journey online?

- A) 195
- B) 360
- C) 130
- D) 945

**Correct answer: A) 195.**

**Explanation:** The remainder percentage is 100% - 63% - 24% = 13%. Then 13% of 1,500 = 0.13 x 1,500 = 195 participants. Option B is the "needed assistance" group (24% = 360). Option D is the unaided group (63% = 945). Option C is a decimal slip. Two habits help here: first, always derive the missing percentage before calculating; second, check the parts sum to the whole (945 + 360 + 195 = 1,500 - correct). Numbers like these drive assisted-digital design decisions, so handling them accurately links directly to designing inclusive services - a serious obligation for UK public sector work.

**Question 14 (hard) - Multi-step migration estimate**

A legacy system holds 1.2 million records. A migration tool processes records in batches of 5,000, and each batch takes 12 minutes including validation. The migration can run for at most 10 hours per night. How many nights does the full migration need?

- A) 4 nights
- B) 5 nights
- C) 6 nights
- D) 48 nights

**Correct answer: B) 5 nights.**

**Explanation:** Step one: number of batches = 1,200,000 / 5,000 = 240 batches. Step two: total processing time = 240 x 12 = 2,880 minutes = 48 hours. Step three: nights needed = 48 / 10 = 4.8, which must round up to 5 nights, because 4 nights gives only 40 hours - not enough. Option A rounds down, a classic error: partial nights are not available, so always round up when dividing work into fixed windows. Option D confuses hours (48) with nights. Migration window arithmetic exactly like this appears in real cutover plans, and getting it wrong by one night can mean a missed go-live or an overrunning outage - so senior architects will love you for checking it.

**Question 15 (moderate) - Percentage of budget consumed**

A solution workstream has an annual budget of £250,000. At the end of month 8, it has spent £180,000. Is spending ahead of or behind a straight-line budget profile, and by how much?

- A) Ahead of profile by £13,333
- B) Behind profile by £13,333
- C) Ahead of profile by £30,000
- D) Exactly on profile

**Correct answer: A) Ahead of profile by £13,333.**

**Explanation:** A straight-line profile spends the budget evenly across 12 months: 250,000 / 12 = £20,833.33 per month. By month 8, profiled spend = 8 x 20,833.33 = £166,666.67. Actual spend is £180,000, so the workstream is ahead of (over) profile by 180,000 - 166,666.67 = £13,333 (to the nearest pound). Option C incorrectly profiles two-thirds of the year as £150,000 (that would be month 7.2, not month 8). Option B has the right magnitude but the wrong direction - a sign error that careful labelling ("actual minus profile") prevents. Budget-versus-profile arithmetic appears in nearly every programme board pack in government, and understanding it helps you see the financial constraints your designs must respect.

**Question 16 (hard) - Interpreting availability percentages**

A service level agreement promises 99.5% monthly uptime. In a 30-day month, approximately how many hours of downtime does that allow, and did a service with 5 hours of downtime that month meet the SLA?

- A) Allows about 3.6 hours; the service missed the SLA
- B) Allows about 3.6 hours; the service met the SLA
- C) Allows about 7.2 hours; the service met the SLA
- D) Allows about 36 hours; the service met the SLA

**Correct answer: A) Allows about 3.6 hours; the service missed the SLA.**

**Explanation:** A 30-day month has 30 x 24 = 720 hours. Allowed downtime = 0.5% of 720 = 0.005 x 720 = 3.6 hours. The service was down for 5 hours, which exceeds 3.6, so it missed the SLA. Option C doubles the allowance (using 1%), and option D slips a decimal place (5%). The deeper lesson is how deceptively small the gap between availability figures is: 99.5% allows 3.6 hours a month, while 99.9% allows only about 43 minutes. When a stakeholder casually asks for "another nine" of availability, the cost implications multiply - and an associate who can translate percentages into hours brings instant clarity to that conversation.

**Question 17 (easy) - Sense-checking a claim**

A colleague's draft options paper claims: "Moving to Option B reduces monthly hosting costs from £8,000 to £6,000, a saving of 33%." You are proofreading before it goes to your supervising architect. Is the percentage correct?

- A) Yes - 33% is correct
- B) No - the saving is 25%
- C) No - the saving is 20%
- D) It cannot be checked from the figures given

**Correct answer: B) No - the saving is 25%.**

**Explanation:** A saving is measured against the original cost: (8,000 - 6,000) / 8,000 x 100 = 2,000 / 8,000 x 100 = 25%. The paper's 33% comes from dividing the saving by the new cost (2,000 / 6,000), which answers a different question ("how much more expensive is the old option than the new?"). Both numbers describe the same £2,000, but only 25% is "a saving of" the current cost. This asymmetry - percentages differ depending on the base - is why reviewers should always recompute headline percentages before papers reach governance. Catching this before your supervisor did would be a quiet, genuinely valuable associate contribution: wrong percentages in an options paper undermine confidence in everything else the paper says.

### Preparation tips

- **Rebuild your percentage toolkit.** Percentage change, percentage of a total, and reverse percentages cover most questions. Ten minutes of daily practice for a week makes these automatic.
- **Always identify the base figure first.** Ask "percentage of what?" before touching the calculator. Dividing by the wrong base is the single most common numeric error, as Question 2 showed.
- **Use the calculator, but estimate first.** A rough mental estimate ("about £100k") catches keying errors instantly. This double-check habit costs seconds and saves marks.
- **Practise with tables, not just sums.** Most errors come from extracting the wrong number, not calculating badly. Cover a table with paper, reveal it, and give yourself 20 seconds to find a specific value.
- **Check totals when parts are given.** Where percentages or allocations should sum to a whole, verify they do - it is a free correctness check, used in Questions 9 and 13.
- **Be gentle with yourself about pace.** At associate level, steady accuracy beats rushed brilliance. If a multi-stage question (like Question 14) looks heavy, flag it, bank the quicker ones, and return.

### Common pitfalls

- **Misreading chart and table labels.** Confusing monthly with annual figures, or missing qualifiers like "in thousands", flips an answer from right to wrong. Read headers and units before the numbers.
- **Over-calculating.** Performing precise multi-decimal arithmetic when rounding would reveal the answer faster. If options are far apart (£74,000 versus £96,000), estimation alone often decides it.
- **Time-sink questions.** Spending five minutes stuck on one multi-stage problem instead of banking three easier ones. Skip and return - the marks are equal.
- **Applying flat rates to tiered pricing.** As Question 6 showed, tiered tables must be computed band by band. Multiplying every unit by one rate is the trap the question is built around.
- **Simple growth instead of compound growth.** When something grows "by X% each year", multiply year on year. Adding the same amount each year under-provisions, as Question 10 demonstrated.
- **Forgetting to round up for fixed windows.** Work divided into nights, sprints, or batches must round up: 4.8 nights means 5 nights, as Question 14 showed.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written information. It mirrors the exact reading demands of your role: dense passages built from the kinds of documents an associate solution architect reads every week - technology standards, governance policies, architecture decision records, stakeholder emails, and service assessments.

The format is distinctive and worth understanding before you start. You are given a passage, then a series of statements. For each statement you answer **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot Say** (the passage gives insufficient information either way). The golden rule is that you answer based strictly on the text provided, ignoring your outside knowledge. Even if you know from experience that something is generally true in government IT, if the passage does not say it, the answer is Cannot Say. Some assessments also include multiple-choice comprehension questions asking for the best summary, the main obligation, or the correct application of a rule.

These tests are time-pressured - often less than a minute per question - to simulate workplace deadlines. That sounds daunting, but the passages are short, and with practice you will learn to scan for the sentence that decides each statement rather than re-reading everything.

For your role, this skill is not academic. Solution architects live and die by precise reading: a misread standard becomes a non-compliant design; a misread email becomes a stakeholder misunderstanding; a misread policy becomes a governance failure. Practising careful, evidence-based reading directly improves the quality of your architectural work.

### What it measures for your role

- **Architecture communication** asks you to "listen to the needs of technical and business stakeholders" and achieve agreement with technical and non-technical audiences. Reading is listening in written form: extracting what a stakeholder actually said, rather than what you expected them to say, is the foundation of that skill.
- **Commercial perspective** requires "awareness of legal and compliance rules". Legal and commercial text is dense and precise; the difference between "must", "should", and "may" changes your obligations entirely. Verbal reasoning trains exactly that sensitivity.
- **Architect for the whole context** asks you to "identify relevant information" in strategies, roadmaps, and policies. Those documents are long; the relevant sentence is usually one among hundreds. Fast, accurate extraction is the measured skill.
- **Making architectural decisions** includes understanding "architectural governance and assurance relevant to your work" - which arrives as written terms of reference, review criteria, and standards you must interpret correctly.
- **Problem definition and shaping** begins with reading problem statements, user research findings, and requirement documents accurately, so the problem you frame is the one that actually exists.

### Practice questions

**Passage A (for Questions 1-4): Extract from a departmental technology standard**

"All new digital services must be hosted on the department's approved cloud platform unless an exemption is granted by the Architecture Review Board. Exemptions will be considered only where a service has a demonstrable technical dependency that the approved platform cannot meet, or where the total cost of migration exceeds the projected five-year benefit. Services granted an exemption must be reviewed annually. Legacy services already in operation before January 2025 are not required to migrate, but any major change to a legacy service triggers a hosting review. The Architecture Review Board meets monthly and publishes its decisions on the departmental intranet."

**Question 1 (easy) - True / False / Cannot Say**

Statement: "New digital services must use the approved cloud platform unless the Architecture Review Board grants an exemption."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A) True.**

**Explanation:** This is a near-restatement of the first sentence: "All new digital services must be hosted on the department's approved cloud platform unless an exemption is granted by the Architecture Review Board." Every element of the statement - the obligation, its scope (new services), and the exemption route - appears explicitly in the text. Easy verification questions like this reward reading the statement first and then scanning for the matching sentence, rather than reading the whole passage repeatedly. Bank marks like this quickly in a timed test.

**Question 2 (moderate) - True / False / Cannot Say**

Statement: "A legacy service in operation since 2023 that undergoes a major change must migrate to the approved cloud platform."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C) Cannot Say.**

**Explanation:** Read the legacy clause precisely: "any major change to a legacy service triggers a hosting review". A review is triggered - but the passage never says the review's outcome is mandatory migration. The review could conclude migration, an exemption, or something else; the text is silent. Answering True imports an assumption the text does not make - the single most common verbal reasoning error. Answering False would also overreach, because the passage does not rule migration out either. When the text specifies a process (a review) but the statement claims an outcome (must migrate), Cannot Say is usually the answer. This distinction between process and outcome is exactly the kind of precision architectural governance demands.

**Question 3 (moderate) - True / False / Cannot Say**

Statement: "An exemption can be granted where migration costs exceed the projected five-year benefit."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A) True.**

**Explanation:** The passage lists two grounds for exemption: a demonstrable technical dependency the platform cannot meet, "or where the total cost of migration exceeds the projected five-year benefit". The statement matches the second ground almost word for word. Note the small vocabulary shift - the statement says "migration costs" while the passage says "total cost of migration" - assessments routinely paraphrase, and your job is to judge whether the meaning is preserved (here, it is). Contrast this with Question 2, where the paraphrase changed the meaning. Sensitivity to meaning-preserving versus meaning-changing paraphrase is precisely what you use when checking that a design document faithfully reflects a standard.

**Question 4 (hard) - Multiple choice comprehension**

According to Passage A, which of the following services definitely requires no action today?

- A) A new service planning to host outside the approved platform without an exemption
- B) A legacy service from 2020 with no changes planned
- C) A service granted an exemption fourteen months ago and not reviewed since
- D) A new service with a technical dependency the platform cannot meet

**Correct answer: B.**

**Explanation:** Work through each option against the text. Option A breaches the first sentence - new services must use the platform or hold an exemption, so action is required. Option C breaches the annual review requirement: "Services granted an exemption must be reviewed annually", and fourteen months exceeds a year, so a review is overdue. Option D is a service that may qualify for an exemption, but it must still apply for one - qualifying grounds do not grant themselves, so action is required. Option B fits the legacy clause: services operating before January 2025 "are not required to migrate", and with no major change planned, no hosting review is triggered. Nothing in the passage requires anything of it today. This question rewards systematic elimination - the same discipline you use when checking which governance requirements apply to a design.

**Passage B (for Questions 5-8): Email from a service owner to the architecture team**

"Thanks for the draft options paper. I have concerns about Option 2. Our contact centre staff already juggle three systems, and adding a fourth screen will slow them down during peak periods, when call volumes can double. I would support Option 2 only if the new case view can be embedded inside the existing agent desktop. Option 1 avoids this problem but, as your paper notes, it requires the data-cleansing work to finish first, and my team cannot commit resource to that before April. Please also remember that whichever option we choose must be signed off by the Service Assessment panel before private beta. I would like to discuss at Thursday's session."

**Question 5 (easy) - True / False / Cannot Say**

Statement: "The service owner has concerns about Option 2."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A) True.**

**Explanation:** The second sentence says directly: "I have concerns about Option 2." This is stated in plain terms with no hedging. Notice, though, what the statement does not claim - it does not say the service owner rejects Option 2. In fact, the email later sets a condition under which they would support it. Verbal reasoning passages built from emails often test whether you can separate a concern from a refusal, because in real stakeholder work the difference matters enormously: a concern invites design work (embedding the case view), while a refusal closes the option down.

**Question 6 (moderate) - True / False / Cannot Say**

Statement: "The service owner will support Option 2 if the new case view is embedded inside the existing agent desktop."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A) True.**

**Explanation:** The email states: "I would support Option 2 only if the new case view can be embedded inside the existing agent desktop." The statement mirrors this condition. A subtle point for the alert reader: "only if" strictly expresses a necessary condition, and the email's plain reading is that embedding would secure the owner's support - which the statement captures. Assessments at associate level treat conversational English at face value; the answer is True. The workplace skill here is recognising a stakeholder's stated condition and carrying it accurately into the design discussion - misquote it as a preference rather than a condition, and Thursday's session goes badly.

**Question 7 (moderate) - True / False / Cannot Say**

Statement: "The data-cleansing work will be finished by April."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C) Cannot Say.**

**Explanation:** The email says Option 1 "requires the data-cleansing work to finish first, and my team cannot commit resource to that before April". This tells you when the service owner's team could start contributing resource - it says nothing about when the work will finish, who else might resource it, or whether it is already underway elsewhere. Concluding "it will be finished by April" invents a completion date; concluding "it will not be finished" (False) equally goes beyond the text. The passage constrains one input to the work, not the work's end date. Timeline statements are favourite Cannot Say territory: check whether the text gives a date for the same event the statement describes - here it does not.

**Question 8 (hard) - Multiple choice comprehension**

Which of the following best summarises the service owner's overall position?

- A) They reject both options and want new ones developed
- B) They prefer Option 1 unconditionally and want it approved on Thursday
- C) They see obstacles with both options - a usability condition on Option 2 and a resourcing constraint affecting Option 1 - and want to discuss before deciding
- D) They believe the Service Assessment panel should choose the option

**Correct answer: C.**

**Explanation:** The email raises a concern about Option 2 with a condition that would resolve it (embedding in the agent desktop), notes that Option 1 depends on data-cleansing work their team cannot resource before April, reminds everyone of the assessment gate, and asks to discuss on Thursday. Option C captures all of that without exaggeration. Option A overstates - nothing is rejected. Option B invents a preference and an approval request the email never makes; the owner merely says Option 1 "avoids this problem", which is not unconditional support. Option D distorts the panel's role: sign-off is a governance step the owner flags, not a delegation of the choice. Summary questions reward the option that is entirely supported and complete - discard any option containing even one unsupported claim.

**Passage C (for Questions 9-12): Extract from architecture governance terms of reference**

"The purpose of architectural assurance is to confirm that solution designs comply with departmental standards before significant build investment is made. Design documents should be submitted to the review board at least five working days before the meeting. Submissions received later than this may be deferred to the following month at the chair's discretion. Each submission must include a completed standards checklist, a risk summary, and a record of the architectural decisions taken to date, including the reasoning behind them. Associate architects may present designs they have contributed to, provided a supervising architect attends the same session. The board does not approve budgets; financial approval follows a separate process owned by the finance committee."

**Question 9 (easy) - True / False / Cannot Say**

Statement: "The review board approves project budgets."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B) False.**

**Explanation:** The final sentence states plainly: "The board does not approve budgets; financial approval follows a separate process owned by the finance committee." The statement directly contradicts this, so the answer is False - not Cannot Say. Distinguish the two: Cannot Say applies when the text is silent; False applies when the text asserts the opposite, as here. Candidates who have learned to be cautious sometimes over-use Cannot Say - remember that an explicit contradiction earns a confident False. Knowing which forum owns which decision is also genuine governance knowledge for your role: taking a budget question to an architecture board wastes everyone's time.

**Question 10 (moderate) - True / False / Cannot Say**

Statement: "A submission received three working days before the meeting will be deferred to the following month."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C) Cannot Say.**

**Explanation:** The passage says late submissions "may be deferred to the following month at the chair's discretion". "May" plus "at the chair's discretion" means deferral is possible, not automatic. The statement claims it "will be deferred" - a certainty the text does not support. But the text does not guarantee acceptance either, so False would also overreach; the outcome genuinely cannot be determined. This is the classic modal-verb trap: must/will express certainty, may/might express possibility, and should expresses expectation. Train yourself to underline modal verbs as you read - in assessments and in real standards documents alike, because misreading "may" as "must" in a compliance context creates non-existent obligations in your designs.

**Question 11 (moderate) - True / False / Cannot Say**

Statement: "An associate architect may present a design they contributed to if a supervising architect attends the session."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A) True.**

**Explanation:** The passage states: "Associate architects may present designs they have contributed to, provided a supervising architect attends the same session." The statement reproduces both the permission and its condition faithfully. This clause should also be personally encouraging: governance frameworks expect associates to present at review boards, with support present. If the statement had dropped the condition ("An associate architect may present any design"), the answer would change, because the permission is conditional and scoped to designs they contributed to. Conditions attached to permissions are part of the meaning - carry them with you, in tests and in practice.

**Question 12 (hard) - Multiple choice comprehension**

A design document is submitted on time but includes only the standards checklist and a risk summary. According to Passage C, what is missing, and why does it matter to the board's purpose?

- A) Nothing is missing; two documents are sufficient
- B) The record of architectural decisions and their reasoning is missing; without it the board cannot fully confirm the design's compliance journey before build investment
- C) The budget approval form is missing; the board cannot proceed without finance sign-off
- D) The supervising architect's signature is missing; all submissions require one

**Correct answer: B.**

**Explanation:** The passage requires three items: "a completed standards checklist, a risk summary, and a record of the architectural decisions taken to date, including the reasoning behind them". The submission includes two, so the decision record with reasoning is missing - and the board's stated purpose is confirming compliance "before significant build investment is made", which the reasoning record supports. Option A miscounts the requirements. Option C imports budget approval, which the passage explicitly assigns elsewhere. Option D invents a signature requirement; the supervising architect condition concerns presenting, not submitting. Notice how the correct answer connects a factual gap to the stated purpose - the passage itself links assurance to protecting build investment, and staying within what the passage links is what makes B fully supported. Recording decisions with reasoning is also literally one of your named skills, so let this question double as a professional reminder.

**Question 13 (moderate) - True / False / Cannot Say**

Passage D (for Question 13): "The department's API standard requires all new APIs to be documented in the developer portal within one month of go-live. A recent internal audit sampled twenty new APIs and found that seventeen were documented on time. The audit report recommended automated reminders for API owners, and the standards team has accepted the recommendation."

Statement: "Three of the sampled APIs were not documented within one month of go-live."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A) True.**

**Explanation:** The audit sampled twenty APIs and found seventeen documented on time. Simple subtraction: 20 - 17 = 3 were not documented on time - which is exactly what the statement says. This shows that verbal reasoning sometimes includes light arithmetic inference; deriving "three" from "twenty minus seventeen" stays firmly within the text, unlike importing outside knowledge, which never does. Be careful not to over-extend, though: the passage would not support "three API owners ignored the standard" (we know nothing about reasons) or "15% of all departmental APIs are undocumented" (the sample is twenty APIs, not the whole estate). Inference is allowed exactly as far as the numbers given - and no further.

**Question 14 (hard) - Multiple choice comprehension**

Passage E (for Question 14): "Following the spending review, the programme board has asked all workstreams to identify designs that reuse existing departmental platforms before proposing new builds. Proposals for new components will require a reuse assessment demonstrating that no existing platform meets the need at reasonable cost. The board recognises that reuse is not always feasible, particularly where legacy platforms carry unsupported dependencies, and it does not intend the policy to delay fixes to live service incidents."

Which action best complies with the policy in Passage E?

- A) Proposing a new notification component without checking the department's existing notification platform
- B) Delaying an urgent live incident fix until a reuse assessment is completed
- C) Completing a reuse assessment that shows the existing forms platform cannot meet the need at reasonable cost, then proposing a new build
- D) Rejecting all new builds permanently because reuse is now mandatory

**Correct answer: C.**

**Explanation:** The policy requires a reuse assessment before proposing new components, and permits new builds where the assessment demonstrates no existing platform meets the need at reasonable cost - which is exactly option C's sequence. Option A skips the required assessment. Option B contradicts the passage's explicit carve-out: the board "does not intend the policy to delay fixes to live service incidents". Option D overstates the policy: reuse is the first consideration, not an absolute mandate, and the passage openly recognises reuse "is not always feasible". Policy-application questions reward matching each option against every clause, including exceptions - the same skill you will use when checking a design against a spending control or technology standard, where the exceptions are as binding as the rule.

**Question 15 (moderate) - True / False / Cannot Say**

Passage F (for Question 15): "The architecture community of practice meets fortnightly and is open to all members of the digital, data and technology profession in the department. Sessions alternate between show-and-tell presentations and open discussion of current design challenges. Attendance is voluntary, although architects presenting a design at an upcoming review board are encouraged to rehearse at a community session first. Recordings of presentations are stored on the shared drive for staff who cannot attend."

Statement: "Architects presenting at an upcoming review board are required to rehearse at a community session first."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B) False.**

**Explanation:** The passage says such architects "are encouraged to rehearse" - and, crucially, it also states "attendance is voluntary". "Encouraged" expresses a recommendation, while the statement claims a requirement ("are required"). Because the passage explicitly frames attendance as voluntary and rehearsal as encouragement, the statement's claim of obligation contradicts the text, making the answer False rather than Cannot Say. This mirrors Question 10's modal-verb lesson from the other direction: there, "may" could not support "will" (Cannot Say, because the outcome was undetermined); here, "voluntary plus encouraged" actively contradicts "required" (False). Reading recommendation and obligation accurately matters in your community collaboration too - knowing what your team genuinely expects of you, versus what is simply good practice, keeps your workload and your promises realistic.

### Preparation tips

- **Read the statement first, then hunt.** For True/False/Cannot Say questions, read the statement before the passage, then scan for the deciding sentence. It is faster and keeps you anchored to the text.
- **Underline modal verbs.** Must, will, may, should, can - each carries different force. Half of all Cannot Say answers hinge on a modal verb, as Questions 2 and 10 showed.
- **Practise the discipline of ignorance.** Deliberately answer using only the passage, even when you know the real-world answer. Try practising with passages about unfamiliar domains, where you have no outside knowledge to resist.
- **Learn the False/Cannot Say boundary.** False needs an explicit contradiction in the text; silence means Cannot Say. Rehearse this distinction until it is instant - it is the most commonly confused pair.
- **Read governance documents actively at work.** Your department's standards, decision records, and terms of reference are free practice material - and reading them closely doubles as genuine professional development for your Making architectural decisions skill.
- **Keep calm about pace.** Aim for steady progress at roughly a minute per question. If a passage feels impenetrable, answer what you can, flag the rest, and return.

### Common pitfalls

- **Making assumptions.** Bringing personal or professional knowledge into the answer instead of relying only on the provided text. The test measures reading, not experience - your experience will shine elsewhere.
- **Confusing likelihood with fact.** A passage saying an outcome is "likely" or "possible" never supports a statement that it "will" happen. Match the strength of the claim, as Question 10 demonstrated.
- **Treating a process as an outcome.** "Triggers a review" does not mean "must migrate" (Question 2). When the statement claims a result the text only sets in motion, choose Cannot Say.
- **Over-using Cannot Say.** Caution is good, but explicit contradictions deserve a confident False (Question 9). Cannot Say is for silence, not for hesitation.
- **Poor time management.** Reading every passage exhaustively before looking at the questions burns your minutes. Scan for keywords from the statement instead.
- **Dropping conditions from permissions.** "May present, provided a supervisor attends" is not "may present" (Question 11). Conditions are part of the rule - in assessments and in governance alike.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct. Unlike the logic and numeracy tests earlier in this guide, it presents realistic workplace dilemmas - conflicts, ethical grey areas, competing priorities - and asks how you would respond. There is usually no single objectively right answer in the mathematical sense; several responses may seem reasonable, but one aligns best with the organisation's values and the demands of your role.

The response formats vary. Most commonly you are asked to pick the **most effective** and **least effective** actions from a set, or to **rank** all the options from best to worst. These assessments are usually untimed or generously timed, because they measure natural judgement rather than speed. Take that as an invitation to think each scenario through properly.

For an associate solution architect in UK government, "effective" has a particular flavour. The public sector values that shape good answers include: putting user needs first, transparency and honesty (especially about risks and mistakes), collaboration across disciplines, accessibility and inclusion, and responsible use of public money. Your level matters too: as an associate you usually work under supervision, so effective answers often involve engaging your supervising architect at the right moment - neither hiding problems from them nor escalating every tiny decision. The strongest responses are active (they engage the problem), honest (they surface rather than bury difficulties), and proportionate (they match the response to the size of the issue).

The scenarios below are drawn directly from your role's real duties: supporting design work with stakeholders, communicating architecture to mixed audiences, complying with governance, managing risks transparently, and helping your team achieve its objectives.

### What it measures for your role

- **Community collaboration** - "understand the work of others and the importance of team dynamics, collaboration and feedback". Many scenarios test whether you strengthen or strain team relationships under pressure.
- **Architecture communication** - "listen to the needs of technical and business stakeholders" and support "discussions about architectural topics within a multidisciplinary team". Scenarios probe how you handle disagreement, confusion, and difficult messages.
- **Making architectural decisions** - "describe the reasoning behind architectural design decisions" and "understand architectural governance and assurance". Scenarios test transparency about decisions and respect for governance routes.
- **Problem definition and shaping** - several dilemmas hinge on whether you address the real problem or a symptom.
- **Commercial perspective** - awareness of "government commercial processes" and "legal and compliance rules" appears in scenarios involving suppliers and data.
- Your role description's commitments to "manage risks and decisions in a transparent way" and "communicate and work effectively with stakeholders" run through every scenario, as does your level's emphasis on working under supervision and helping your team achieve its objectives.

### Practice questions

**Question 1 (easy) - The mistake in your published diagram**

You discover that a context diagram you produced, already circulated to the delivery team, contains an error: it shows a direct connection between the case system and the payments provider that does not exist. Development work based on the diagram starts next week. What do you do?

- A) Quietly correct the diagram in the repository and say nothing, hoping nobody noticed
- B) Tell your supervising architect about the error, correct the diagram, and send the delivery team a short note explaining what changed and why
- C) Wait to see whether the developers spot it, since they may not use that part of the diagram
- D) Mention it verbally to one developer you trust and ask them to spread the word

**Most effective: B. Least effective: C.**

**Explanation:** Option B is honest, prompt, and complete: the error is fixed, your supervisor is informed (appropriate at associate level), and everyone who received the wrong version learns about the correction before work begins - transparency in exactly the sense your role description requires. Option A fixes the artefact but not the misunderstanding already in circulation; silent corrections erode trust when discovered. Option D relies on informal, unreliable channels for a formal artefact. Option C is least effective because it is passive: it knowingly lets a defect flow toward a costly outcome, gambling with the team's time. A useful general rule for situational judgement: options that surface problems early and communicate corrections openly nearly always outrank options that conceal, delay, or delegate the honesty.

**Question 2 (easy) - The jargon-heavy presentation**

You are helping prepare a presentation about a proposed solution for an audience including the service owner, a policy lead, and two content designers - none of them deeply technical. The draft slides, written by a developer, are full of terms like "idempotent consumers" and "circuit breakers". Your supervising architect asks you to improve the deck. What is the most effective approach?

- A) Leave the terms in - stakeholders should learn the vocabulary of the systems they own
- B) Delete all the technical content so nobody gets confused
- C) Reframe each point around what it means for the service and its users - reliability, error recovery, cost - keeping a short technical annex for those who want depth
- D) Replace the slides with a live demo of the prototype

**Most effective: C. Least effective: A.**

**Explanation:** Your Architecture communication skill is explicitly about using "different architecture representations to communicate effectively, achieving agreement with technical and non-technical stakeholders". Option C does precisely that: it translates technical patterns into service outcomes stakeholders care about, while the annex respects readers who want detail. Option B throws away substance - non-technical stakeholders still need to understand the trade-offs, just in accessible language. Option D changes the medium without solving the translation problem, and a demo of a prototype cannot convey architectural choices like resilience patterns. Option A is least effective because it pushes the communication burden onto the audience; expecting stakeholders to decode jargon is the opposite of listening to their needs, and it typically loses the room - and the agreement you were seeking.

**Question 3 (moderate) - The tempting shortcut**

A delivery manager under deadline pressure asks you to skip the architecture review for a "small" change: connecting the booking service to a new SMS provider. You know the department's governance requires review for any new external integration. The delivery manager says: "It is only notifications - can you just say the architects are happy?" What do you do?

- A) Agree - it genuinely is a small change, and you want a good relationship with the delivery manager
- B) Refuse bluntly and remind them that rules are rules
- C) Explain that a new external integration does need review, and offer to help make it fast - preparing the submission yourself and asking your supervising architect whether an expedited or lightweight review is possible
- D) Tell them to raise it with the review board themselves and step away

**Most effective: C. Least effective: A.**

**Explanation:** Option C upholds governance while genuinely helping with the underlying problem - the deadline. It reflects understanding of "architectural governance and assurance relevant to your work", offers practical support (very much the associate's contribution), and keeps the relationship collaborative. Option A is least effective: saying "the architects are happy" without review misrepresents assurance, sets a precedent that governance is negotiable under pressure, and puts you personally in an untenable position - a new external integration carries real security, commercial, and data protection considerations. Option B protects the rule but damages the relationship and ignores the schedule pressure, which will simply resurface. Option D is technically correct but unhelpfully passive - it misses the chance to collaborate and leaves a frustrated colleague to navigate governance alone. Notice the pattern: the best options serve both the value at stake and the person in difficulty.

**Question 4 (moderate) - Conflicting stakeholder requirements**

During discovery for a grants service, the finance stakeholder insists all applications must be checked manually before payment, while the service owner wants fully automated processing to hit a two-day turnaround target. Both tell you, separately, that their requirement is non-negotiable. You are supporting the lead architect on this work. What do you do first?

- A) Design for the finance stakeholder, since financial controls always take priority
- B) Design for the service owner, since user needs come first in government services
- C) Record both requirements and the conflict, brief the lead architect, and suggest a joint session to explore what each stakeholder is really trying to achieve - for example, risk-based checking that automates low-value applications
- D) Design a compromise yourself and present it to both stakeholders as the answer

**Most effective: C. Least effective: D.**

**Explanation:** The conflict is real and above your pay grade to resolve unilaterally - but surfacing it clearly, and bringing an idea, is squarely your job. Option C listens to both stakeholders, makes the conflict transparent, engages your lead appropriately, and starts moving from stated positions ("manual checks", "full automation") to underlying needs (fraud control, turnaround speed) - the essence of problem definition and shaping. The risk-based suggestion shows how apparently opposed requirements often dissolve once reframed. Options A and B each pick a side prematurely, guaranteeing a collision later; neither "always" claim is true, and choosing between stakeholders is not an associate's solo call. Option D is least effective: designing the compromise alone and presenting it as "the answer" bypasses your lead, denies stakeholders a voice in the trade-off, and stakes the outcome on your guess about two sets of needs you have not yet explored. First understand, then design - with your team.

**Question 5 (moderate) - The struggling teammate**

A developer on your team seems to be struggling with the integration design you helped document. In stand-ups they say everything is fine, but their tasks keep slipping, and yesterday they implemented something that contradicts the documented design. You suspect they have not fully understood it. What do you do?

- A) Raise their underperformance with the delivery manager so it is dealt with formally
- B) Have a friendly one-to-one chat: ask how they are finding the integration work, walk through the design together, and ask for their feedback on where the documentation could be clearer
- C) Rewrite their code yourself to match the design, since you know what it should look like
- D) Announce at the next stand-up that the implementation does not match the design and needs redoing

**Most effective: B. Least effective: D.**

**Explanation:** Option B embodies your Community collaboration skill - "the importance of team dynamics, collaboration and feedback". It approaches a colleague with curiosity rather than blame, tests your hypothesis (misunderstanding) before acting on it, and treats their difficulty as feedback on your documentation - which it may well be. This is also how designs are supported "throughout the life cycle": guidance and support to the teams using them. Option A escalates a possible communication gap into a performance issue, skipping the obvious human step. Option C fixes one symptom, leaves the misunderstanding intact, and quietly undermines the developer. Option D is least effective because public criticism at a stand-up humiliates a colleague who may already be struggling to admit difficulty - it damages psychological safety, making it even less likely that they, or anyone else watching, will ask for help next time. Strong situational judgement answers protect both the work and the person.

**Question 6 (moderate) - Out of your depth in a meeting**

Your supervising architect is off sick, and you are asked to represent architecture at a stakeholder meeting about the casework solution. Mid-meeting, the programme director asks you directly: "Can we commit to switching off the legacy system by March?" You genuinely do not know - decommissioning depends on analysis you have not seen. What do you do?

- A) Say yes - March sounds plausible, and you can check the details afterwards
- B) Say no - it is safer to refuse commitments you are unsure about
- C) Say you cannot give a reliable answer today, explain it depends on the migration analysis, and commit to getting a definitive answer from the lead architect within two days
- D) Deflect the question by talking in detail about the technical migration approach until the agenda moves on

**Most effective: C. Least effective: A.**

**Explanation:** Option C is honest about the limits of your knowledge - a strength, not a weakness, at any level and especially under supervision - while remaining useful: it names what the answer depends on and commits to a specific, dated follow-up. That is transparent management of decisions in action, and stakeholders consistently prefer a reliable "I will find out" to a shaky "yes". Option A is least effective: an unfounded "yes" from someone representing architecture becomes a planning assumption the moment it is spoken, and unwinding it later costs credibility and possibly money. Option B is dishonest in the opposite direction - an unfounded "no" may derail plans needlessly. Option D wastes the stakeholders' time and dodges a legitimate question; people notice. The professional habit to build: distinguish clearly between what you know, what you believe, and what you must check - and say which is which.

**Question 7 (hard) - The supplier demonstration**

At a supplier demonstration of a case management product, the sales team shows a feature your programme needs and says: "We can have you live in eight weeks." Afterwards, the supplier's account manager emails you personally, offering to "help draft the requirements" for the upcoming procurement. You are aware the department will run a formal procurement process. How do you respond?

- A) Accept the help - their product knowledge would make the requirements sharper, and it saves the team time
- B) Politely decline, tell your supervising architect and the commercial team about the offer, and ensure any requirements are drafted independently so the procurement stays fair
- C) Ignore the email entirely
- D) Accept the help but keep it informal and unwritten so it cannot influence the official documents

**Most effective: B. Least effective: D.**

**Explanation:** A supplier drafting the requirements for a procurement they intend to bid in is a serious fairness problem: it risks skewing the specification toward their product, could invalidate the procurement, and may breach procurement regulations - exactly the "government commercial processes" and "legal and compliance rules" your Commercial perspective skill covers. Option B declines cleanly, makes the contact transparent to the right people (supervisor and commercial colleagues), and protects the process. Option D is least effective - worse even than naive option A - because it adds concealment to the impropriety: "informal and unwritten" shows awareness that the influence is improper, plus intent to hide it. Option A is a genuine but naive error an associate might make; the assessment distinguishes naivety from bad faith, and so do real organisations. Option C avoids personal risk but leaves the commercial team blind to a supplier behaving inappropriately - transparency means reporting, not just abstaining. When in doubt commercially: decline, disclose, and ask.

**Question 8 (hard) - The risk nobody wants on the register**

While documenting the solution design, you realise the chosen approach depends on a single specialist engineer - if they leave, nobody else understands the integration layer. You draft a risk entry. A senior colleague (not your supervisor) says: "Do not log that - it will make the team look bad, and anyway he is not going anywhere." What do you do?

- A) Follow the senior colleague's advice - they are more experienced and know the politics
- B) Log the risk anyway without telling anyone, and let the register speak for itself
- C) Explain to the colleague why you believe it should be logged, and discuss it with your supervising architect before adding it, together with sensible mitigations like documentation and pairing
- D) Post the concern in the programme-wide channel so it cannot be suppressed

**Most effective: C. Least effective: A.**

**Explanation:** Key-person dependency is a textbook architectural risk, and "manage risks and decisions in a transparent way" is in your role description - so the risk belongs on the register, framed constructively with mitigations (knowledge sharing, documentation, pairing) rather than as an accusation. Option C does this while treating the dissenting colleague with respect (you explain your reasoning - a Making architectural decisions behaviour) and using your proper support line, your supervising architect. Option A is least effective: suppressing a genuine risk because it "looks bad" is precisely the culture failure that turns manageable risks into crises, and seniority is not a reason to abandon transparency. Option B gets the risk logged but dodges the conversation, leaving the colleague to discover it and feel ambushed - collaboration matters even when you disagree. Option D escalates a team-level risk into a public drama before trying proportionate routes, damaging trust unnecessarily. Transparent does not mean theatrical; it means honest, through the right channels.

**Question 9 (moderate) - The accessibility objection**

In a design discussion, a developer proposes a slick document-upload flow that relies on drag-and-drop only. A content designer points out this will fail users who rely on keyboards or screen readers. The developer replies: "That is an edge case - we can sort accessibility after private beta." The room looks to you as the architecture representative. What is the most effective contribution?

- A) Stay neutral - accessibility is the content designer's specialism, not architecture's
- B) Support the developer - velocity matters, and retrofitting is a valid strategy
- C) Back the accessibility concern: explain that accessibility is a legal requirement and a design constraint from day one, and suggest the flow support both drag-and-drop and a standard file picker
- D) Suggest a vote among the team to settle it democratically

**Most effective: C. Least effective: B.**

**Explanation:** Accessibility for public sector services is a legal obligation and a core government service standard - it is a constraint architecture must design within, not a feature to bolt on. Option C brings that constraint into the decision clearly, supports a colleague who has raised a legitimate need, and - importantly - offers a constructive both/and design (drag-and-drop plus file picker) rather than simply blocking the developer's idea. That is supporting "discussions about architectural topics within a multidisciplinary team" at its best. Option B is least effective: "retrofit accessibility later" reliably becomes "never", excludes real users - who are citizens, not edge cases - and stores up expensive rework and legal exposure. Option A dodges: constraints like accessibility are absolutely architecture's business, because they shape the solution. Option D treats a legal requirement as a matter of preference; teams do not get to vote away compliance. Inclusion is a value the assessment - and the profession - expects you to defend.

**Question 10 (hard) - Ranking under deadline pressure**

It is 16:00 on Wednesday. The architecture review board pack (due at 17:00) is missing one diagram you promised to finish. Meanwhile: your supervising architect has asked for comments on a strategy paper by Friday; a tester has found what they think is a design flaw and wants ten minutes; and a stakeholder has emailed asking to move tomorrow's walkthrough. Rank these actions from first to last:

1. Finish and submit the review board diagram
2. Spend ten minutes with the tester on the suspected design flaw
3. Reply to the stakeholder about tomorrow's walkthrough
4. Start commenting on the strategy paper

- A) 1, 2, 3, 4
- B) 2, 1, 3, 4
- C) 1, 3, 2, 4
- D) 3, 4, 1, 2

**Best ranking: A) 1, 2, 3, 4.**

**Explanation:** The diagram has an immovable deadline sixty minutes away, and missing it may defer the whole submission a month (recall the governance terms in the verbal section) - it comes first. The tester comes next: a suspected design flaw carries real risk, ten minutes is a small cost, and hearing it today might even matter to the review pack - but with only an hour before the deadline, it cannot pre-empt the submission unless the tester's news directly affects it, which you can establish with one quick question while you work. The stakeholder email is important but tomorrow's walkthrough can be rearranged this evening without harm. The strategy paper has two days of slack, so it is last - though "last" means "scheduled for tomorrow", not forgotten. Ranking B risks the hard deadline for a conversation that could wait forty minutes; C leaves a colleague with a live risk waiting behind routine correspondence; D inverts urgency entirely. Deadline-driven ranking questions reward comparing each task's deadline, impact, and cost of delay - out loud, if it helps.

**Question 11 (moderate) - The feedback that stings**

Your supervising architect reviews your first solo options paper and returns it covered in tracked changes, with a comment that the options "read as technology choices, not answers to the business problem". You worked hard on it and feel deflated. What is the most effective response?

- A) Rewrite it exactly as the tracked changes suggest and move on quickly
- B) Ask for a short conversation to understand the feedback properly - especially what "answering the business problem" looks like - then rewrite, and ask for a second look
- C) Defend the paper: the technology analysis was thorough and the criticism feels subjective
- D) Ask a different senior architect for a second opinion without mentioning the first review

**Most effective: B. Least effective: D.**

**Explanation:** Option B treats feedback as the development opportunity it is - your Community collaboration skill explicitly values feedback, and at associate level, learning from supervision is the core of your growth. The specific question in B matters: the reviewer's comment is about framing options around the business problem, which is your Problem definition and shaping skill maturing - understanding that lesson deeply is worth far more than mechanically accepting edits (option A), which fixes the paper but not the author. Option C converts feedback into conflict before understanding it; there may be points worth discussing, but understanding comes first. Option D is least effective because it quietly shops for a friendlier verdict, undermining trust with your supervisor if discovered, and wastes the second architect's time by hiding the context. Feeling deflated is human and fine; the professional move is to turn the sting into a conversation, and the conversation into skill.

**Question 12 (hard) - The strategic misalignment you spotted**

Reading the department's newly published data strategy, you notice that your project's design - agreed by the lead architect before the strategy was published - stores citizen documents in a way that conflicts with the strategy's new "store once, reference everywhere" principle. Delivery is mid-build. Nobody else seems to have noticed. What do you do?

- A) Say nothing - the design was legitimately agreed before the strategy existed, so it is grandfathered in
- B) Raise it with your lead architect: summarise the specific conflict, its practical impact, and rough options (continue with a documented exception, adapt now, adapt later), so the team can decide transparently
- C) Email the data strategy team to report your own project's non-compliance
- D) Quietly redesign the storage approach and give the updated design to the developers

**Most effective: B. Least effective: D.**

**Explanation:** This scenario rewards exactly the behaviours your role profile names: identifying "relevant information that can inform your architectural work, such as strategies" (you did - by reading the strategy), and adapting "a technical design if needed during delivery" (the question is whether and how). Option B surfaces the conflict to the right person with analysis and options rather than alarm - a decision made transparently, with reasoning, at the right level. Note that "continue with a documented exception" is a legitimate option: strategies routinely include transition arrangements, and mid-build changes have real costs; the point is that the decision must be conscious and recorded, not accidental. Option A assumes grandfathering without checking - silence makes the non-alignment invisible rather than managed. Option C escalates outside the team before your own lead has heard the news; loyalty to transparency does not mean bypassing your team. Option D is least effective: an associate unilaterally changing an agreed design mid-delivery - without the lead architect, without the delivery team's planning, without governance - creates chaos regardless of good intentions. Spotting the issue was excellent; the judgement lies in what you do next.

### Preparation tips

- **Learn the values, not scripted answers.** UK public sector judgement scenarios consistently reward user needs, transparency, collaboration, accessibility and inclusion, and care with public money. Understand why each matters and your instincts will generalise to scenarios no practice guide covers.
- **Think "active, honest, proportionate".** Before choosing, test each option: does it engage the problem or dodge it? Does it surface the truth or manage appearances? Is the response sized to the issue? The strongest option usually passes all three.
- **Use your level deliberately.** At associate level, involving your supervising architect at the right moment is a strength the assessment expects to see. The judgement being tested is when to handle, when to consult, and when to escalate - not whether you can do everything alone.
- **Read every option before judging any.** The most and least effective options often differ by one clause - "and tell your supervisor" versus "and say nothing". Compare options against each other, not just against your first instinct.
- **Rehearse with real memories.** Recall recent workplace moments - a disagreement in refinement, an awkward stakeholder email - and ask what the most effective response would have been. This builds the reflective habit the assessment measures, and it is free professional development.
- **Do not rush.** These assessments are usually untimed or generous. Reread the scenario, notice who is affected, and take a breath before answering. Considered judgement is precisely what is being measured.

### Common pitfalls

- **Answering idealistically instead of practically.** Choosing what sounds noble ("immediately escalate to the director") over what is practically effective in a real workplace. Effective answers solve the problem at the lowest sensible level.
- **Selecting passive options.** Options that delay action, pass the problem to someone else, or wait to see what happens are almost always weak - as Question 1's "wait and see" showed. Passivity is the most common least-effective answer.
- **Ignoring the organisation's values.** In UK government scenarios, options that compromise accessibility, transparency, or fair procurement lose - however efficient they look. Question 7's "informal and unwritten" option is efficient and disqualifying.
- **Confusing loyalty with silence.** Protecting a colleague or the team's image by suppressing risks or errors (Question 8) reads as a values failure, not as loyalty. Transparency through the right channel is the loyal act.
- **Over-escalating.** Broadcasting every concern to the widest audience (Question 8's option D) signals poor proportionality. Escalation is a ladder: try the nearest appropriate rung first.
- **Forgetting the people in the scenario.** Options that are technically correct but humiliate, ambush, or bypass colleagues (Question 5's stand-up announcement) score poorly. The assessment measures how you treat people while solving the problem - and so does your career.

## Conclusion

Well done for working through this guide - it represents a genuinely thorough piece of preparation, and the fact that you have engaged with it says good things about your commitment to your development as an associate solution architect.

You have now practised the four kinds of thinking that psychometric assessments measure, each mapped to your real work. In the cognitive section, you exercised pattern recognition, logical deduction, error checking, and prioritisation on the artefacts architects actually handle - designs, roadmaps, decision logs, and governance rules. In the numeric section, you worked with the budgets, capacity figures, licence tiers, and performance metrics that turn architectural opinion into evidence. In the verbal section, you sharpened the precise, evidence-only reading that standards, policies, and stakeholder emails demand - including the discipline of Cannot Say. And in the situational judgement section, you rehearsed the honest, active, proportionate choices that build trust with teams and stakeholders.

A few encouragements as you move forward. First, remember that these are trainable skills: every practice session genuinely moves you forward, and the explanations you studied matter more than the scores you got. Second, your daily work is the best practice ground there is - every design document you proofread, every percentage you check in an options paper, every standard you read closely, and every tricky conversation you handle thoughtfully is assessment preparation and professional growth at the same time. Third, use the people around you: your supervising architect, your architecture community of practice, and your multidisciplinary teammates are all part of how associates grow into architects.

If you have a real assessment coming up, revisit the preparation tips a few days beforehand, sleep well, and go in knowing you have prepared properly. Whatever the outcome, you will have strengthened exactly the skills your role profile asks of you. Good luck - and enjoy the journey from supporting solutions to designing them.
