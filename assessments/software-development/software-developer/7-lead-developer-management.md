# Lead Developer (Management) - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a lead developer in the management track of the UK Government Digital and Data profession. You lead development across one or a small number of related project teams, and your role summary names responsibilities that distinguish this variant from its technical counterpart: leading and developing a team of experts, analysing current processes and implementing opportunities to optimise them, ensuring the correct implementation of availability and capacity management standards, and setting policy and standards.

That is a different centre of gravity. The technical lead maintains hands-on responsibility across the stages of a project; you are responsible for the people who do, for the processes they work within, and for the standards that govern both. The work is still technical — you cannot set a standard you do not understand, and a process optimisation proposed by someone who has not done the work is usually wrong — but the leverage has moved. Your best day changes how thirty people work, not what one component does.

You may be preparing for a formal assessment as part of a selection process, or you may simply want to test reasoning that has become fluent. At this level the specific risk is that management judgement is harder to check than technical judgement. A wrong architectural decision produces an outage; a wrong process decision produces a slow accumulation of friction that nobody attributes to it.

Three features of the role run through everything here. First, you make decisions about people whose consequences are slow, personal, and largely unmeasurable. Second, you set policy, and policy applies to everyone including the cases you did not imagine. Third, you are accountable for outcomes produced by people you do not directly control, which makes the quality of your delegation the main determinant of the quality of the output.

The document contains a cognitive assessment, a numeric reasoning assessment, a verbal reasoning assessment and a situational judgement assessment. Each has an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips, and common pitfalls.

Answer each question before reading its explanation, and pay attention where you were fast.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands using material drawn from the role itself. For a lead developer on the management track that means process data, team performance information, standards proposals, capacity plans and resourcing decisions.

The format is typically fifteen to thirty minutes online, covering deduction, pattern recognition, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group of comparable seniority, and many platforms report speed and accuracy separately.

Three things distinguish this section at your level.

The first is that process problems are usually system problems. When a team is slow, the cause is rarely that people are working slowly; it is queueing, handoffs, rework, or waiting on something. The instinct to look for effort is almost always the wrong instinct.

The second is that policy has a blast radius. A rule written to fix one case applies to every case, including the ones where it makes no sense, and the discipline of imagining the badly-fitting case before publishing is what separates workable policy from the kind teams quietly ignore.

The third is that you reason about people through weak evidence. Performance signals are noisy, sparse, and heavily confounded by circumstance, and treating them as clean data produces confident wrong conclusions about individuals.

### How this assessment maps to your role

- **Systemic process diagnosis** maps to **Development process optimisation**, where you analyse current processes and implement improvements.
- **Policy reasoning** maps to your responsibility for setting policy and standards, and to **Modern development standards**.
- **Capacity reasoning** maps to **Availability and capacity management**, where you ensure standards are correctly implemented.
- **Prioritisation across teams** maps to leading development across related project teams.
- **Reasoning under weak evidence** maps to leading and developing a team of experts.
- **Risk and security judgement** maps to **Information security**.

### Practice questions

**Question 1 (easy) — Deduction from a policy**

Your policy states: "All production changes require an approved change record, except changes classified as standard changes, which are pre-approved." A change went to production without an approved change record. Which must be true?

- A) The policy was breached.
- B) It was a standard change.
- C) Either it was a standard change, or the policy was breached.
- D) The change should be reversed.

**Correct answer: C**

**Explanation:** A rule with an exception, plus a fact silent on the exception, licenses only the disjunction. Options A and B each pick a branch on no evidence. Option D prescribes an action, and the question asks what must be true. There is a practical point behind the logic: if standard changes are invisible in your records, your policy cannot be audited, and that is a defect in the policy you wrote rather than in anyone's compliance.

**Question 2 (easy) — Where the time goes**

A team reports that a typical change takes 11 days from starting work to reaching production. Coding takes 2 days, review 0.5 days, testing 1 day, and deployment 0.5 days. What is the strongest observation?

- A) The team should code faster.
- B) Four days of work is spread across 11 days, so roughly 7 days are spent waiting rather than working — which means process improvement should target the queues, not the activities.
- C) Testing should be automated.
- D) The estimate is probably wrong.

**Correct answer: B**

**Explanation:** 2 + 0.5 + 1 + 0.5 = 4 days of activity inside an 11-day elapsed time, so nearly two-thirds is waiting: for a reviewer, for a test environment, for a release window, for an approval. This is the single most useful calculation in process optimisation and it is nearly always ignored, because the visible work is the activity and the invisible cost is the queue. Halving coding time saves one day; removing a three-day wait for a test environment saves three. Options A and C optimise activities that together account for less than a third of the elapsed time.

**Question 3 (moderate) — A recurring problem across teams**

Three of the four teams you lead have each missed a delivery commitment this quarter, for apparently different reasons: a dependency, an illness, and a scope change. What is the strongest reading?

- A) Three different causes; nothing systemic.
- B) Three teams missing commitments with three different proximate causes suggests the commitments themselves may be the issue — specifically that they are being made with no allowance for the ordinary disruptions that always occur — so the question is how the commitments are set rather than what went wrong in each case.
- C) The teams need better planning.
- D) Dependencies should be managed more tightly.

**Correct answer: B**

**Explanation:** The apparent diversity of causes is what makes option A tempting and what actually points at a systemic cause. Dependencies slipping, people falling ill and scope changing are not unusual events; they are the normal background of delivery, and a commitment process that assumes none of them will happen will be missed by whichever one shows up. Option B reframes from "what went wrong three times" to "what does our commitment process assume", which is the question that produces a fix. Option C is a conclusion without a mechanism. Option D addresses one of the three.

**Question 4 (moderate) — Writing a policy**

You are drafting a policy requiring that all services have automated deployment. One of your teams maintains a legacy system where this would be disproportionately expensive. What is the strongest approach?

- A) Write the policy without exceptions; exceptions weaken policy.
- B) Write the policy with an explicit, narrow exception process — a named approver, a stated justification, and a review date — because a policy with no route for the genuine hard case is either broken by the team quietly or complied with at absurd cost, and both outcomes are worse than a recorded exception.
- C) Exempt the legacy system by name in the policy.
- D) Do not write the policy.

**Correct answer: B**

**Explanation:** Option A produces the failure mode that undermines most internal policy: teams facing an unreasonable requirement do not escalate, they quietly do not comply, and you lose visibility of who is compliant. An exception process with a named approver and a review date keeps the hard cases visible and time-bound. Option C hard-codes today's known case and leaves you with the same problem the next time a different one appears. Option D abandons a worthwhile standard because of one case. The review date is the part most often omitted and it is what stops an exception becoming permanent.

**Question 5 (moderate) — Capacity standards**

You are responsible for ensuring capacity management standards are correctly implemented. A team reports that its service is "comfortably within capacity" at 50% average CPU. What is the strongest response?

- A) Accept it; 50% is comfortable.
- B) Ask for peak figures and failure headroom rather than averages — what the utilisation is at peak, and what it becomes if an instance is lost during peak — since average utilisation is close to uninformative about whether a service can survive its worst moment.
- C) Ask them to reduce it to 30%.
- D) Ask for the last three months of data.

**Correct answer: B**

**Explanation:** Average CPU is the number teams report because it is the easy one, and it conceals exactly the situation that causes outages. A service at 50% average with a peak factor of 2 is at 100% at peak with no failure headroom at all. Option B asks the two questions that matter and does so in a way that is diagnostic rather than prescriptive. Option C sets a number without knowing the shape of the load. Option D gathers more of the wrong metric. This is the specific way capacity standards are complied with in letter and missed in substance.

**Question 6 (moderate) — Prioritising across teams**

Four teams have each asked for your time this week: one on a design decision, one on a conflict between two developers, one on a stakeholder escalation, and one on a hiring decision. What is the strongest basis for prioritising?

- A) Deal with them in the order received.
- B) Prioritise by what deteriorates if delayed and what only you can do — an interpersonal conflict worsens materially over a week and cannot be delegated, while a design decision can often be unblocked by naming who decides rather than by deciding it yourself.
- C) Prioritise the stakeholder escalation; stakeholders are most visible.
- D) Delegate all four.

**Correct answer: B**

**Explanation:** The two criteria in option B are the useful ones and they are different: urgency by deterioration, and irreducibility. Conflicts harden, and each day of silence makes them harder to resolve. Design decisions frequently need a decision-maker named rather than a decision made, which takes two minutes. Option C prioritises by visibility, which is the default failure of a lead's calendar and reliably starves the invisible work that matters more. Option A ignores all information. Option D includes things that are genuinely yours, and a conflict between two of your people is one of them.

**Question 7 (moderate) — Interpreting a team health signal**

An anonymous team survey shows one of your four teams scoring markedly lower on "I can raise concerns". What is the strongest first step?

- A) Ask the team lead what is going on.
- B) Treat the signal as real and find out how, carefully — the score says people do not feel able to speak, so a route that requires them to speak to their lead or to you will not produce reliable information, and an approach through a neutral party or through what you can observe is more likely to work.
- C) Discuss it with the team openly.
- D) Wait for the next survey to see if it persists.

**Correct answer: B**

**Explanation:** The finding is self-referential and that is the whole difficulty: the measurement says people cannot raise concerns, so any method that involves raising concerns is compromised. Option B recognises this and looks for routes that do not depend on it. Option C is well-intentioned and asks people who have said they do not feel safe speaking to speak, in a group, to the person above their lead. Option A may be exactly the wrong door if the lead is part of the cause, though it is not automatically wrong. Option D defers a signal about psychological safety for a quarter, which is the one signal least safe to defer.

**Question 8 (harder) — An optimisation that shifts a cost**

A proposed change would cut the team's code review turnaround from two days to four hours by allowing single-reviewer approval instead of two. What is the strongest analysis?

- A) Adopt it; the time saving is substantial.
- B) The saving is real and the change moves risk rather than removing it, so the question is what the second reviewer was catching — if the data shows second reviewers rarely add findings, the change is nearly free, and if they catch a meaningful share of defects, you are trading two days of latency for defects reaching production.
- C) Reject it; two reviewers is a control.
- D) Adopt it for low-risk changes only.

**Correct answer: B**

**Explanation:** The change is plausible and its cost is invisible in the proposal, which is the shape of most process optimisations that go wrong. Option B asks the question that settles it and it is empirically answerable — review data will show how often the second reviewer added a finding the first did not. If the answer is rarely, the control is theatre and removing it is a clear win. Option D is a decent instinct and requires a definition of low-risk that will itself need maintaining, so it belongs after the data. Option A takes the benefit without pricing the risk; option C defends the control without asking what it does.

**Question 9 (harder) — Reading performance evidence**

A developer who performed strongly for two years has had a weak quarter. What is the strongest inference?

- A) Their performance has declined.
- B) A single weak quarter against two strong years is far more likely to reflect circumstance than a change in capability — a difficult project, a change at home, a poor fit with the current work, or a team dynamic — so the reasonable prior is that something has changed around them, and the useful action is to find out what.
- C) They need performance management.
- D) It is normal variation; ignore it.

**Correct answer: B**

**Explanation:** This is base-rate reasoning applied to people. Two years of strong evidence is a substantial prior, and one quarter of contrary evidence is a weak signal against it — capability does not usually change abruptly, whereas circumstances do, constantly. Option B holds the prior and prescribes the correct action, which is inquiry. Option C reaches for a formal process on a single data point, which damages a strong performer and frequently causes the departure it was meant to prevent. Option D is closer to right than C and still wrong, because a strong performer having a bad quarter usually has a reason worth knowing about.

**Question 10 (harder) — A metric that will be gamed**

You are considering measuring teams on the number of production incidents, with a target of reducing them. What is the strongest observation?

- A) It is a good measure; fewer incidents is better.
- B) Counting incidents creates an incentive to classify fewer events as incidents, which is easier than preventing them — so the measure will improve while reliability does not, and a measure less easy to redefine, such as user-visible unavailability, is a better target if you want the behaviour rather than the number.
- C) It should be combined with other measures.
- D) Targets should not be set on incidents at all.

**Correct answer: B**

**Explanation:** Any measure used as a target creates pressure on whatever is cheapest to change, and for incident counts the cheapest thing is the classification threshold rather than the underlying reliability. Option B names the mechanism and proposes the remedy, which is to measure something the team does not control the definition of — minutes of user-visible unavailability is defined by users rather than by the team's judgement. Option C is generically sensible and does not fix a measure with a specific gaming route. Option D over-corrects; reliability targets are legitimate and the choice of measure is what matters.

**Question 11 (harder) — Standard versus autonomy**

Two of your four teams use different testing frameworks. Standardising would simplify tooling and shared support. What is the strongest analysis?

- A) Standardise; consistency is worth it.
- B) Price the migration against the benefit honestly — one team rewrites its test suite, which is weeks of work producing no user value and some risk of losing coverage, against a saving in tooling and support that is real but modest — and be clear that the strongest case for standardising is usually about future teams and mobility rather than about these two.
- C) Leave it; team autonomy matters.
- D) Standardise for new services only.

**Correct answer: B**

**Explanation:** Standardisation decisions are often made on an aesthetic preference for consistency, and the cost lands entirely on whichever team has to move. Option B insists on pricing it and identifies where the real benefit usually lies, which is not in the present state but in onboarding, mobility between teams, and not maintaining two sets of tooling indefinitely. Option D is frequently the right resolution — it captures most of the benefit at almost no cost — and it belongs after the analysis, since if the benefit is genuinely modest it may not be worth doing at all. Options A and C are positions rather than analyses.

**Question 12 (harder) — Delegation and accountability**

You delegated a technical decision to a senior developer. They made a choice you would not have made. It is defensible but not what you would have chosen. What is the strongest response?

- A) Overturn it; you are accountable.
- B) Support the decision and let it stand, because a defensible decision made by the person you delegated to is a good outcome even when it differs from yours — and overturning it teaches them, and everyone watching, that delegation here means guessing what you would have done.
- C) Support it publicly and discuss your reservations privately.
- D) Ask them to reconsider.

**Correct answer: B**

**Explanation:** "Defensible but different" is the normal and desired result of real delegation; if delegated decisions always matched yours, either you are delegating to a mirror or nobody is actually deciding. Option B accepts that. Option C is close and is the answer most people pick, and it is right when the reservations are substantive information the person lacks — but as a habit it becomes a way of overturning decisions quietly, and the person learns that your public support is not real. If your reservations amount to preference, the honest thing is to keep them. Option A destroys the delegation. Option D is a softer version of A and reads exactly the same from the other side.

### Preparation tips

- **Compute elapsed time against activity time.** The gap is where the improvement is.
- **Read diverse proximate causes across teams as one systemic cause.**
- **Build a narrow exception route with a review date into every policy.**
- **Ask for peak and failure headroom whenever someone reports an average.**
- **Prioritise by deterioration rate and by what only you can do.**
- **Ask what a control catches before removing it.**
- **Hold the prior when one quarter contradicts two years.**
- **Ask how a measure would be gamed before adopting it as a target.**

### Common pitfalls to avoid

- **Optimising activities that occupy a third of the elapsed time.**
- **Writing policy with no route for the genuine hard case.**
- **Accepting average utilisation as evidence of capacity headroom.**
- **Prioritising by visibility.**
- **Investigating a psychological safety finding through channels it says are blocked.**
- **Treating a single weak quarter as a capability signal.**
- **Standardising on a preference for consistency without pricing the migration.**
- **Overturning a defensible delegated decision.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can reach a defensible conclusion from operational data under time pressure. On the management track the data is team throughput, cycle time, cost, capacity, headcount, defect rates and the business cases you are asked to support or challenge.

The format is typically fifteen to twenty-five minutes with a calculator, presenting tables and charts followed by multiple-choice items. Some items are computational and some ask what the data supports, and the second kind carries more weight at senior levels because the risk you present to an organisation is a confident conclusion the numbers do not carry.

Three habits matter particularly.

The first is that you are usually the person in the room best placed to notice when a number is wrong by an order of magnitude, and the order-of-magnitude check is worth more than the precise answer.

The second is that people numbers do not behave linearly. Adding people to a team does not add throughput proportionally, and any business case that assumes it does is wrong before it starts.

The third is that improvement percentages need their base. A 50% reduction in something that costs two days a month is not worth a fortnight of work, however good the percentage looks.

### How this assessment maps to your role

- **Cycle time and flow arithmetic** maps to **Development process optimisation**.
- **Capacity and utilisation** map to **Availability and capacity management**.
- **Cost and business case reasoning** map to setting policy and standards, and to resource decisions.
- **Team throughput and resourcing** map to leading and developing a team of experts.
- **Defect and quality metrics** map to **Modern development standards**.
- **Volumetrics** map to **Systems integration** and **Systems design**.

### Practice questions

*Table 1 — Delivery metrics for four teams, last quarter*

| Team | People | Changes delivered | Mean cycle time (days) | Production incidents |
|---|---|---|---|---|
| Alpha | 6 | 84 | 6.2 | 3 |
| Bravo | 8 | 96 | 9.1 | 7 |
| Charlie | 5 | 55 | 5.4 | 1 |
| Delta | 9 | 72 | 14.3 | 11 |

**Question 1 (easy) — Reading a table**

Which team delivered the most changes per person?

- A) Alpha
- B) Bravo
- C) Charlie
- D) Delta

**Correct answer: A**

**Explanation:** Alpha 84/6 = 14.0; Bravo 96/8 = 12.0; Charlie 55/5 = 11.0; Delta 72/9 = 8.0. Alpha leads. Note before drawing any conclusion that "changes" are not a standardised unit — a team splitting work into smaller changes will score higher without delivering more, which is worth holding in mind for the next few questions.

**Question 2 (easy) — Total and share**

What percentage of the quarter's production incidents came from Delta?

- A) About 32%
- B) About 50%
- C) About 41%
- D) About 25%

**Correct answer: B**

**Explanation:** Total incidents: 3 + 7 + 1 + 11 = 22. Delta's share: 11/22 = 50%. Half the incidents came from one of four teams, which is a substantial concentration and the most striking single fact in the table. Delta also has the longest cycle time and the lowest per-person delivery, and those three facts together are more informative than any of them alone.

**Question 3 (easy) — Cycle time comparison**

Delta's mean cycle time is approximately how many times Charlie's?

- A) About 1.8
- B) About 2.6
- C) About 3.4
- D) About 2.0

**Correct answer: B**

**Explanation:** 14.3 / 5.4 = 2.65, so about 2.6 times. A change takes more than two and a half times as long to get through Delta as through Charlie. Whether that reflects the work, the process or the system Delta maintains is not determinable from this table, and the magnitude is large enough to be worth investigating rather than attributing.

**Question 4 (moderate) — What the data supports**

Based on Table 1, what is the strongest conclusion about Delta?

- A) Delta is underperforming and needs intervention.
- B) Delta shows the worst figures on all three measures, which makes it the clearest candidate for investigation — but the table contains no information about what each team works on, and a team maintaining an old high-risk system would produce exactly this pattern without anyone underperforming.
- C) Delta has too many people for its output.
- D) Delta's incidents are causing its long cycle time.

**Correct answer: B**

**Explanation:** The pattern is consistent and real, and the confound is enormous: the table has no column for what the teams do. A team maintaining a fifteen-year-old system with poor test coverage will have long cycle times, frequent incidents and low throughput regardless of who is on it, and moving people or applying performance pressure would make things worse. Option B states the finding and the limit. Option A jumps to a conclusion about people from data about a system. Option C infers overstaffing from output alone. Option D asserts a causal direction that is at least as plausible reversed.

**Question 5 (moderate) — Adding people**

Bravo asks for two more developers, projecting a proportional increase in delivery from 96 to 120 changes. What is the strongest assessment?

- A) Reasonable; 8 people deliver 96, so 10 should deliver 120.
- B) The projection assumes throughput scales linearly with headcount, which it does not — new people take months to become productive, absorb existing team members' time while doing so, and increase coordination overhead — so a realistic near-term expectation is a dip followed by a gain well short of 25%.
- C) Unreasonable; adding people never helps.
- D) The projection is too conservative.

**Correct answer: B**

**Explanation:** The linear projection is the standard form of a resourcing business case and it is wrong in a predictable direction. Three effects work against it: onboarding time, the productivity cost to existing members who do the onboarding, and coordination overhead that grows faster than headcount. In the first quarter the team may deliver less than it does now. Option B says this without claiming that hiring is futile — option C overstates in the other direction, and adding capacity does work over a longer horizon. The useful contribution you can make to a business case like this is to reset the timescale, not to block it.

**Question 6 (moderate) — Percentage of a base**

A proposed tooling change would reduce build times by 40%. Builds currently consume 30 minutes per developer per day across a team of 8. The change would take about 3 weeks of one developer's time to implement. Roughly how long until it pays back?

- A) About 3 months
- B) About 6 weeks
- C) About 5 months
- D) About 2 weeks

**Correct answer: A**

**Explanation:** Convert both sides to hours. Saving: 40% of 30 minutes = 12 minutes per developer per day, × 8 developers = 96 minutes/day = 1.6 hours/day. Cost: 3 weeks × 5 days × 7.5 hours = 112.5 hours. Payback: 112.5 / 1.6 = about 70 working days, which is roughly 14 weeks or a little over 3 months. The discipline that matters is putting both sides in the same unit before dividing, and the reason to do the calculation at all is that a 40% improvement sounds compelling and a three-month payback invites a fair question about whether something with a shorter one should come first.

**Question 7 (moderate) — Capacity headroom**

A service runs on 6 instances at 55% average CPU. Peak is 1.9 times average. What is the approximate CPU per instance at peak if one instance is unavailable?

- A) About 105%
- B) About 125%
- C) About 88%
- D) About 95%

**Correct answer: B**

**Explanation:** Total work at average: 6 × 55% = 330 percentage-points. At peak: 330 × 1.9 = 627. Across 5 remaining instances: 627 / 5 = 125.4%. The service cannot survive an instance loss at peak. Note also that peak across all 6 is 627/6 = 104.5%, already over capacity — so this service is under-provisioned even without a failure, and 55% average CPU is the number that made it look fine. This is precisely the substance behind "ensure correct implementation of capacity management standards".

**Question 8 (harder) — Comparing rates fairly**

Using Table 1, which team has the highest incident rate per change delivered?

- A) Bravo
- B) Delta
- C) Alpha
- D) Charlie

**Correct answer: B**

**Explanation:** Alpha 3/84 = 3.6%; Bravo 7/96 = 7.3%; Charlie 1/55 = 1.8%; Delta 11/72 = 15.3%. Delta is highest by a wide margin — more than four times Alpha and more than eight times Charlie. Normalising by changes rather than comparing raw counts is the right move, because a team delivering more changes will have more incidents at the same quality level. The caution from Question 4 still applies: this normalisation controls for volume, not for the risk profile of the systems involved.

**Question 9 (harder) — A business case**

A supplier proposes a platform costing £240,000 a year, claiming it will save each of your 28 developers 45 minutes a day. Assume a fully loaded cost of £70,000 per developer per year and 220 working days. Is the case credible?

- A) Yes — the time saved is worth far more than the cost.
- B) The arithmetic supports it and the assumption does not: 45 minutes is 10% of a 7.5-hour day, worth about £7,000 per developer or £196,000 across 28, which is less than the £240,000 cost — and any claim that a tool saves every developer three-quarters of an hour every day should be treated as a sales figure until measured.
- C) No; the cost is too high.
- D) There is not enough information.

**Correct answer: B**

**Explanation:** 45 minutes of a 7.5-hour day is 10%; at £70,000 fully loaded that is £7,000 per developer, or £196,000 across 28 — close to but below the £240,000 cost, and that is before noting that saved minutes scattered through a day do not convert into delivered work at anything like face value. Option B reaches the right conclusion by the right route and names the real problem, which is the unmeasured 45-minute claim. Option A does the multiplication and skips the comparison. Option C reaches a defensible conclusion without reasoning. Option D declines a calculation the question supplies everything for.

**Question 10 (harder) — Trend versus noise**

Monthly production incidents across your four teams: 18, 22, 19, 25, 21, 24. A stakeholder asks whether reliability is getting worse. What is the strongest answer?

- A) Yes; the trend is upward.
- B) The series moves between 18 and 25 with no clear direction — the apparent rise depends entirely on which months you compare, and six points with this much month-to-month variation cannot distinguish a trend from noise, so the honest answer is that reliability is roughly flat and a longer series or a different measure is needed to say more.
- C) No; reliability is stable.
- D) Not enough information to comment.

**Correct answer: B**

**Explanation:** First to last (18 to 24) suggests a rise; months two to five (22 to 21) suggest nothing; the mean of the first three is 19.7 and of the last three 23.3, which looks like an increase and sits comfortably within the observed variation. Option B gives the stakeholder what they need, which is that the data does not answer their question and what would. Option C overstates in the safe direction — "stable" is a claim too, and this data barely supports it. Option D is unhelpful when you can characterise the variation. Reading noise as a trend and then explaining it is one of the more expensive habits in management reporting.

**Question 11 (harder) — Little's Law in practice**

A team has 14 items in progress and completes on average 7 items per week. What is the expected average cycle time?

- A) 1 week
- B) 2 weeks
- C) 3.5 weeks
- D) 0.5 weeks

**Correct answer: B**

**Explanation:** Cycle time = work in progress / throughput = 14 / 7 = 2 weeks. This relationship is worth knowing by name because it has a direct management implication: with throughput roughly fixed, cycle time is proportional to work in progress, so the fastest available way to reduce cycle time is to start fewer things at once. That is counter-intuitive to teams under delivery pressure, whose instinct is to start more, and being able to state the relationship is what makes the argument winnable.

**Question 12 (harder) — Cost of a delay**

A service generates £45,000 a month in avoided manual processing cost. A three-month delay to its launch is proposed to add a feature. What is the strongest framing?

- A) The delay costs £135,000 in foregone savings, which should be weighed against what the feature is worth — and the relevant question is whether the feature could be added after launch, since that would capture the savings and the feature rather than trading one for the other.
- B) The delay costs £135,000; reject it.
- C) The feature should be assessed on its merits.
- D) £45,000 a month is a projection and may not materialise.

**Correct answer: A**

**Explanation:** 3 × £45,000 = £135,000 of foregone benefit, which is the number the conversation needs and which nobody has usually computed. Option A supplies it and then asks the question that frequently dissolves the trade-off: most features can be added after launch, and the choice between launching now and launching with the feature is often a false one created by treating launch as a single event. Option B computes correctly and forecloses. Option D raises a fair caution and offers nothing. Option C is true and empty without the number.

### Preparation tips

- **Convert both sides of a payback calculation to the same unit before dividing.**
- **Normalise counts by volume before comparing teams.**
- **Reject linear headcount-to-throughput projections.**
- **Ask for peak and failure headroom, not average utilisation.**
- **Know Little's Law.** Cycle time = WIP / throughput.
- **Check whether a percentage improvement has a base worth improving.**
- **Compute the cost of delay before discussing a delay.**
- **Distinguish a trend from variation before reporting one.**

### Common pitfalls to avoid

- **Comparing raw incident counts across teams of different sizes.**
- **Reading team metrics as evidence about people rather than systems.**
- **Accepting a vendor's per-person time saving without measurement.**
- **Treating six noisy data points as a trend.**
- **Assuming two more developers means 25% more delivery.**
- **Reporting average CPU as capacity headroom.**
- **Discussing a launch delay without pricing it.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what written material establishes. On the management track the material is policy, contracts, HR guidance, standards, supplier agreements and reports written to be relied on.

The commonest format gives a passage and asks you to mark statements True, False or Cannot Say. True means the passage establishes it, False means the passage contradicts it, and Cannot Say means the passage does neither — regardless of what you know from experience. Your knowledge is the main hazard, because you will frequently know the answer while the passage is silent.

Three specifics matter at your level.

The first is that policy prose uses "must", "should" and "may" as distinct obligations, and reading them loosely is how a lead ends up enforcing something optional or waiving something mandatory.

The second is that authority language is precise. "May approve", "must consult", "is responsible for" and "in consultation with" describe genuinely different arrangements, and confusing them means acting outside your remit or failing to act within it.

The third is that HR and employment material is written carefully because it has to be, and reading in the ordinary practice rather than the stated rule is a common and consequential error.

### How this assessment maps to your role

- **Reading normative language** maps to setting policy and standards.
- **Reading authority and delegation** maps to leading teams and to your accountability boundaries.
- **Reading employment guidance** maps to leading and developing a team of experts.
- **Reading contracts and supplier terms** maps to resource and supplier decisions.
- **Reading service commitments** maps to **Availability and capacity management**.
- **Distinguishing evidence from inference** maps to **Development process optimisation**.

### Practice questions

*Passage A — for Questions 1 to 4*

"A lead developer may approve a deviation from the departmental coding standard for a single project, provided the deviation is recorded in the project's decision log and reviewed within six months. Deviations affecting more than one project must be approved by the head of engineering. Deviations relating to security controls must be approved by the head of engineering in consultation with the departmental security lead, regardless of scope. A recorded deviation that has not been reviewed within the stated period lapses, and the standard applies in full from that date. Lapsed deviations may be reinstated through the original approval route."

**Question 1 (easy)**

Statement: A lead developer can approve a single-project deviation from the coding standard.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly in the first sentence, with two conditions attached — recording and review — that do not affect who may approve it. The baseline item.

**Question 2 (moderate)**

Statement: A lead developer can approve a single-project deviation relating to a security control.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: security deviations "must be approved by the head of engineering in consultation with the departmental security lead, regardless of scope". The phrase "regardless of scope" exists specifically to close the single-project route, and this is exactly the kind of authority boundary worth reading precisely, since exceeding it is not a technical error but a governance one.

**Question 3 (moderate)**

Statement: If a deviation is not reviewed within six months, it must be re-approved by the head of engineering before it can be reinstated.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage says lapsed deviations "may be reinstated through the original approval route" — and for a single-project non-security deviation, the original route was the lead developer. So head of engineering approval is not required for that case, and the statement asserts it universally. The word doing the work is "original", which sends you back to whichever route applied first rather than escalating.

**Question 4 (harder)**

Statement: The departmental security lead can approve a security-related deviation.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage assigns approval to the head of engineering and gives the security lead a consultation role — "approved by the head of engineering in consultation with the departmental security lead". Consultation is not approval, and the distinction is the point of the item. The passage does not merely omit the security lead's approval power; it allocates the approval elsewhere, which contradicts the statement rather than leaving it open.

*Passage B — for Questions 5 to 8*

"The team charter states that development work is prioritised by the product owner, and that technical work necessary to maintain the service may be scheduled by the lead developer up to a limit of 20% of team capacity in any sprint. Technical work exceeding this limit requires the product owner's agreement. Where the lead developer judges that unaddressed technical risk threatens service availability, they may exceed the limit without prior agreement, and must inform the product owner and record the decision within one working day. The charter is reviewed annually. Since its introduction eighteen months ago, the limit has been exceeded on four occasions."

**Question 5 (easy)**

Statement: The product owner prioritises development work.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated in the first clause. Note that the passage immediately qualifies it with the lead developer's 20% allocation, so "prioritises development work" is true as stated and not the whole picture — which is how charters usually read.

**Question 6 (moderate)**

Statement: The lead developer must obtain the product owner's agreement before scheduling technical work above 20% of capacity.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts the "must, before" framing by supplying an exception: where unaddressed technical risk threatens availability, the lead may exceed the limit without prior agreement and inform afterwards. So prior agreement is the default and not an absolute requirement. Reading only the second sentence and stopping produces True, and the third sentence is there precisely to qualify it.

**Question 7 (moderate)**

Statement: On each of the four occasions the limit was exceeded, the lead developer judged that service availability was threatened.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage records that the limit was exceeded four times and says nothing about the route by which each exceedance was authorised. Some may have been agreed with the product owner in advance, which is a permitted route requiring no availability judgement at all. The statement assumes one of two available mechanisms was used every time.

**Question 8 (harder)**

Statement: The charter has been reviewed at least once since its introduction.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The charter "is reviewed annually" and was introduced eighteen months ago, which means a review was due at twelve months — and the passage states the intention, not the fact. Policies specify annual reviews that do not always happen, and the passage gives no evidence about whether this one did. Marking True treats a stated cadence as an event record, which is the specific error the item is built around, and it is a real one: assuming a scheduled review occurred is how out-of-date policy stays in force.

*Passage C — for Questions 9 to 12*

"Where a period of sustained underperformance is identified, the line manager should first address it informally, setting out the specific concerns and the improvement expected, and agreeing a period in which improvement will be assessed. Formal capability procedures should be initiated only where informal measures have not produced sufficient improvement, or where the nature of the underperformance makes informal measures inappropriate. Before initiating formal procedures the line manager must consult the human resources business partner. Where underperformance may be connected to a disability or a health condition, the line manager must seek advice from occupational health before taking any action, whether formal or informal."

**Question 9 (moderate)**

Statement: A line manager must always attempt informal measures before initiating formal capability procedures.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts "always": formal procedures may be initiated where informal measures have not worked "or where the nature of the underperformance makes informal measures inappropriate". The second limb is an independent route. Note also that the informal step is a "should" rather than a "must", which independently defeats "always".

**Question 10 (moderate)**

Statement: A line manager must consult human resources before initiating formal capability procedures.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly with "must": "Before initiating formal procedures the line manager must consult the human resources business partner." Worth contrasting with the surrounding sentences, which use "should" for the informal-first approach — the passage is deliberate about which obligations are absolute, and this is one of them.

**Question 11 (harder)**

Statement: Where underperformance may be connected to a health condition, the line manager can hold an informal conversation before seeking occupational health advice.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: occupational health advice must be sought "before taking any action, whether formal or informal". The final clause exists specifically to prevent the reading that informal action is exempt, and the word "any" leaves no room. This is the item where professional instinct pulls hardest in the wrong direction, because having a quiet supportive conversation feels obviously right and the guidance sequences it deliberately.

**Question 12 (harder)**

Statement: The passage requires that an improvement period be agreed with the individual.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says the manager should be "agreeing a period in which improvement will be assessed", which sits inside a sentence governed by "should" rather than "must" — so it is a recommendation rather than a requirement, and the statement's word "requires" does not hold. Marking True is the natural reading and skips the modal verb governing the whole clause. Note the answer is Cannot Say rather than False because the passage does recommend it and does not state that it is unnecessary; nothing in the text contradicts the practice, only the characterisation of it as required.

### Preparation tips

- **Read must, should and may as distinct obligations.**
- **Distinguish consultation from approval.**
- **Trace "the original route" back rather than escalating.**
- **Read a stated review cadence as an intention, not a record.**
- **Check whether a rule has a second independent limb.**
- **Watch for "any", "regardless of" and "in all cases" — they close inferences.**
- **Ask whether a statement's modal verb matches the passage's.**
- **Check that a claim about every occasion is supported for every occasion.**

### Common pitfalls to avoid

- **Reading a consultee as an approver.**
- **Treating "should" as mandatory in the statement while the passage says "should".**
- **Assuming a scheduled annual review took place.**
- **Stopping before the sentence that supplies the exception.**
- **Assuming the availability route was used every time a limit was exceeded.**
- **Exempting informal action from a "before any action" requirement.**
- **Answering from HR experience rather than from the passage.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. On the management track the scenarios involve people, standards, competing demands from teams you lead, and the recurring problem of being accountable for work you did not do.

The commonest formats ask for the most and least effective response, or for a rating of each. Scoring is against a key derived from experienced practitioners at comparable levels, so you are aiming at professional consensus rather than personal style.

Three patterns run through the strong answers.

The first is that you establish the cause before selecting the response. Almost every people problem has several possible causes with entirely different remedies, and acting on the first plausible one is the commonest management error.

The second is that you protect the team's ability to tell you things. A lead who reacts badly to bad news gets less of it, and the news does not stop happening.

The third is that policy you set applies to you. Every exemption you take is a public statement about what the policy is actually worth.

### How this assessment maps to your role

- **Leading and developing people** maps to leading a team of experts.
- **Setting and holding standards** maps to setting policy and standards.
- **Process change** maps to **Development process optimisation**.
- **Capacity and reliability decisions** map to **Availability and capacity management**.
- **Stakeholder management** maps to working with client functions and to **User focus**.
- **Security judgement** maps to **Information security**.

### Practice questions

**Question 1 (easy) — Bad news arrives late**

A developer tells you on Thursday that work due Friday will not be ready, and admits they knew on Monday. What is the most effective response?

- A) Explain that this should have been raised on Monday, then deal with the delivery.
- B) Deal with the delivery consequence first, then find out why it took until Thursday — whether they hoped to recover it, expected a bad reaction, or did not think it mattered — because the answer determines whether the fix is about expectations, about how you respond to bad news, or about them.
- C) Tell them clearly that late notice is unacceptable.
- D) Handle the delivery and say nothing about the delay in telling you.

**Correct answer: B**

**Explanation:** The three-day gap is the more important problem and it has several possible causes with different remedies. If they were trying to recover it, that is normal optimism and easily addressed. If they anticipated a bad reaction, the problem is you. If they did not think it mattered, the problem is expectations. Option B finds out and, importantly, deals with the delivery first so the conversation is not conducted under time pressure. Options A and C both correct before understanding, and option C in particular is the response most likely to make the next disclosure later still. Option D leaves the pattern in place.

**Question 2 (easy) — A team wants to change a process**

A team proposes dropping the daily stand-up, which they find low-value. What is the most effective response?

- A) Agree; if it is low-value, drop it.
- B) Ask what the stand-up was meant to achieve and how they will achieve it otherwise — the coordination need is usually real even when the ceremony is not — and let them run the change as an experiment with a date to review it.
- C) Explain why stand-ups are valuable.
- D) Keep it; consistency across teams matters.

**Correct answer: B**

**Explanation:** Option B separates the ceremony from the need it serves, which is the useful distinction: if the team has a better way to surface blockers, dropping the meeting is straightforwardly good, and if they have not thought about that, the question prompts it without overruling them. Framing it as a reviewable experiment makes the change cheap and reversible. Option A skips the question. Option C defends a practice to a team who do it every day and have concluded otherwise. Option D subordinates a team's working practice to cross-team uniformity, which is rarely worth it for something this local.

**Question 3 (moderate) — Two of your teams in conflict**

Two teams you lead are in dispute about the ownership of a shared component, and it has become personal. What is the most effective response?

- A) Assign ownership to one team and move on.
- B) Get both leads in a room and settle ownership explicitly, because an unowned shared component generates this dispute continuously and the personal element is a symptom of an unresolved structural question — and then deal separately with the conduct, which does not become acceptable because the underlying issue was real.
- C) Ask them to resolve it between themselves.
- D) Address the personal conflict first.

**Correct answer: B**

**Explanation:** There are two problems and option B is the only response that treats both. The structural one is that nobody owns the component, which will keep producing friction until it is settled. The behavioural one is that it became personal, which needs addressing on its own terms rather than being excused by the structural cause. Option A resolves ownership by fiat, which may work and leaves the conduct unaddressed. Option D inverts the order and attempts a personal resolution while the cause is still live. Option C returns a problem to people who have demonstrated they cannot resolve it and who both report to you.

**Question 4 (moderate) — A policy you set is inconvenient for you**

You set a policy that all changes require a peer review. You need to push an urgent fix at 22:00 and nobody is available. What is the most effective response?

- A) Push the fix; it is urgent and you set the policy.
- B) Follow whatever emergency route the policy provides, and if it does not have one, push the fix, record it, and add an emergency route the next morning — because the policy has just been shown to be missing something, and the exemption you take without documenting it is the one the team will remember.
- C) Wait until someone is available.
- D) Wake a colleague for the review.

**Correct answer: B**

**Explanation:** The situation is real and the policy is deficient if it has no answer for it. Option B does the right operational thing and then fixes the gap, which is precisely the difference between an exception and an erosion. The recording matters more than it seems: an undocumented exemption taken by the policy's author is the single most effective way to communicate that the policy is optional. Option A does the same thing without the record. Option D is reasonable for a genuine emergency and is a heavier cost than option B's route. Option C may be right if the fix is not truly urgent, and the scenario states that it is.

**Question 5 (moderate) — A capacity warning nobody wants**

Your capacity analysis shows a service will exhaust headroom in about four months. The service owner says there is no budget for more capacity this year. What is the most effective response?

- A) Note the risk and move on; the budget decision is theirs.
- B) Put the consequence and the timeline in writing to the service owner and their accountable superior, with the options — additional capacity, reducing load, or accepting a degradation risk from roughly a stated date — so the decision is made explicitly by someone able to make it rather than by default.
- C) Escalate immediately to senior management.
- D) Find efficiencies to defer the problem.

**Correct answer: B**

**Explanation:** The service owner may not have the budget and may not be the person who can make this decision, which is why option B routes it upward while keeping them in it rather than going round them. The written record and the specific date are what turn a warning into a decision. Option A treats a foreseeable outage as somebody else's problem, and it will not be seen that way afterwards. Option C goes over the service owner's head without giving them the chance to act. Option D is worth doing alongside and is dangerous alone, because efficiency work that defers the wall by two months removes the urgency without removing the problem.

**Question 6 (moderate) — A high performer wants to leave**

An excellent developer tells you privately that they are considering leaving because there is no progression route in your team. What is the most effective response?

- A) Offer a promotion if you can.
- B) Take it seriously and be honest about what is and is not available — including whether a progression route genuinely exists here — because promising something you cannot deliver buys a few months and costs the relationship, and if the honest answer is that the route is elsewhere in the organisation, helping them find it keeps them in it.
- C) Explain that progression takes time.
- D) Accept it; people leave.

**Correct answer: B**

**Explanation:** They have given you information at some personal cost and the response that keeps them longest is honesty, including honesty that is unwelcome. Option B also names the outcome most people miss: retaining someone in the organisation is a much better result than losing them entirely, and a lead who helps a strong person move internally builds a reputation that pays back repeatedly. Option A is the reflex and is only right if it is real and deliverable. Option C is the standard deflection and confirms exactly what they suspect. Option D wastes an opportunity they created.

**Question 7 (harder) — Pressure to move a date**

A senior stakeholder asks you to commit to a delivery date your teams' data suggests is unrealistic. They note that the previous lead would have committed. What is the most effective response?

- A) Commit; refusing damages the relationship.
- B) Decline to commit to that date and say why with the evidence — recent comparable delivery times, what is on the critical path — and offer what you can commit to, including a reduced scope by their date if that helps, because a commitment you expect to miss damages the relationship far more than a difficult conversation now.
- C) Commit with heavy caveats.
- D) Say you will get back to them.

**Correct answer: B**

**Explanation:** The comparison to your predecessor is pressure rather than information, and it is worth noticing that a predecessor who committed to unrealistic dates is not a favourable comparison. Option B substitutes evidence for assertion and, crucially, offers an alternative — a stakeholder who needs something by a date can usually work with reduced scope, and a flat no invites a fight while a scoped yes invites a conversation. Option C is the worst of both, since caveats are not heard and the date is. Option A defers the damage and multiplies it. Option D is acceptable briefly and evasive as a final answer when you already have the data.

**Question 8 (harder) — A process change that failed**

You introduced a change to the release process three months ago. It has not delivered the improvement you expected and the teams find it burdensome. What is the most effective response?

- A) Give it more time; changes take time to bed in.
- B) Say plainly that it has not worked and reverse it, unless there is specific evidence that the benefit is arriving slowly — because a change that costs the teams daily and delivers nothing measurable should be withdrawn, and withdrawing your own initiative visibly is what makes teams willing to try the next one.
- C) Modify it to reduce the burden.
- D) Ask the teams what they would prefer.

**Correct answer: B**

**Explanation:** The hardest part is that it was your idea, and the signal sent by reversing it is worth more than the process itself. A team that has watched a lead abandon their own failed initiative will engage genuinely with the next experiment; a team that has watched one defended past its evidence will comply and disengage. Option B leaves the correct opening for evidence that benefits are lagging, which does happen. Option A is the default and converts a three-month cost into a permanent one. Option C is reasonable if the change is fundamentally sound and here there is no evidence it is. Option D is a good input and does not answer whether this change should stand.

**Question 9 (harder) — Conflicting demands from two teams**

Two of your teams need the same specialist for the next sprint, and both have credible reasons. What is the most effective response?

- A) Split the specialist's time between them.
- B) Decide it yourself on the relative consequence of delay to each, tell both leads the reasoning, and treat the single point of dependency as the actual problem to fix — because this will recur every sprint until more than one person can do the work.
- C) Let the two leads negotiate.
- D) Give priority to the team with the earlier deadline.

**Correct answer: B**

**Explanation:** Option B does the immediate allocation and names the structural issue, which is that you have one person who can do something two teams need. Explaining the reasoning matters because the team that loses needs to see the basis, not just the outcome. Option A is the instinct to be fair and is usually the worst option, since a specialist split across two contexts serves both badly and loses time to switching. Option D uses one input as if it were the whole question, and an earlier deadline may matter less than a later one with larger consequences. Option C makes a decision that is yours into a negotiation between peers, and the more assertive lead wins regardless of merit.

**Question 10 (harder) — A security concern raised by a junior**

A junior developer raises a security concern about a design your most senior developer produced. You are not certain the concern is well-founded. What is the most effective response?

- A) Ask the senior developer to look at it.
- B) Have the concern examined properly and visibly, whether by the two of them together or by a security specialist — because the cost of investigating a concern that turns out to be unfounded is an hour, and the cost of a team learning that junior challenges to senior work get quietly dropped is every future concern.
- C) Ask the junior developer to write it up first.
- D) Investigate it yourself.

**Correct answer: B**

**Explanation:** The asymmetry decides this. If the concern is wrong, you spend an hour and a junior developer learns something. If it is right and you dropped it, you have a vulnerability and a team that has learned when to stay quiet. Option B also handles it visibly, which is what makes the lesson land for everyone watching rather than only the two involved. Option A is the efficient route and asks the author of the design to adjudicate a challenge to it, which is a poor setup regardless of the senior developer's integrity. Option C adds a hurdle that reads as a brush-off. Option D is fine if you have the expertise, and the scenario says you are uncertain.

**Question 11 (harder) — An unpopular organisational decision**

Your organisation has mandated a change your teams strongly dislike, and you were not consulted. Your teams ask you what you think. What is the most effective response?

- A) Support the decision publicly regardless of your view.
- B) Be honest that you were not consulted and that you have reservations, name them specifically, and be equally clear that the decision stands and you expect the team to implement it properly — because teams can tell when a lead is performing enthusiasm, and the credibility you keep by being straight is what lets you ask them to get on with it.
- C) Tell them you disagree and will push back.
- D) Say it is not your decision.

**Correct answer: B**

**Explanation:** The two halves of option B are both necessary. Honesty about your view preserves the credibility that makes everything else you say worth listening to, and a lead who visibly performs enthusiasm they do not feel is trusted less on everything afterwards. Clarity that the decision stands prevents honesty from becoming licence. Option A is the conventional answer and fails because it is transparent. Option C promises advocacy on a settled decision and sets up a second disappointment. Option D is technically true and abdicates, leaving the team to conclude you either agree and will not say so or disagree and will not help.

**Question 12 (harder) — Evidence that contradicts your own initiative**

You championed a technology adoption last year. New data suggests it has increased incident rates rather than reducing them. What is the most effective response?

- A) Examine the data carefully before acting; correlation is not causation.
- B) Present the data yourself, including the part that reflects badly on your decision, and propose how to establish whether the adoption caused the increase — because you are the person best placed to see it, the least suspected of motivated reasoning if you raise it, and the most damaged if someone else does.
- C) Investigate quietly and act if it holds up.
- D) Note the increase but point out the other benefits.

**Correct answer: B**

**Explanation:** Option A is genuinely correct methodologically and incomplete as a response, because it is also exactly what someone protecting a decision would say — and the difference between rigour and defensiveness is visible only in whether you raise the data or wait to be shown it. Option B does the same analysis in the open. The reputational point is real and secondary: the primary reason is that a decision-maker who suppresses contrary evidence about their own decision cannot be trusted with the next one. Option C is the tempting middle and looks exactly like concealment if the quiet investigation is discovered. Option D changes the subject.

### Preparation tips

- **Establish the cause before choosing the response.**
- **Deal with the delivery consequence first, then the disclosure pattern.**
- **Separate the ceremony from the need it serves.**
- **Record every exemption you take from your own policy.**
- **Turn a capacity warning into a written decision with a date.**
- **Be honest about progression rather than promising what you cannot deliver.**
- **Reverse your own failed initiatives visibly.**
- **Raise contrary evidence about your own decisions yourself.**

### Common pitfalls to avoid

- **Correcting late disclosure in a way that makes the next one later.**
- **Splitting a specialist between two teams to be fair.**
- **Asking a design's author to adjudicate a challenge to it.**
- **Committing to a date you expect to miss, with caveats.**
- **Defending a process change past its evidence.**
- **Performing enthusiasm for a decision you disagree with.**
- **Investigating awkward evidence quietly.**
- **Resolving a conflict between your own teams by asking them to sort it out.**

## Conclusion

You have worked through four assessments pitched at the management track of lead developer, and what they test is worth naming.

The cognitive section kept returning to systems rather than individuals. Four days of activity inside eleven days of elapsed time means the improvement is in the queues. Three teams missing commitments for three different reasons means the commitment process assumes nothing will go wrong. A standard nobody follows is a defect in the standard. And policy without a route for the genuine hard case is not enforced, it is quietly ignored — which is worse, because you lose the visibility.

The numeric section was the arithmetic of your decisions: peak headroom rather than average utilisation, incident rates normalised by volume, payback periods with both sides in the same unit, Little's Law, and the cost of delay computed before the delay is discussed. The recurring caution was against treating team metrics as evidence about people, when the systems those teams maintain explain most of the variation.

The verbal section was about reading the documents that define your authority. Consultation is not approval. "The original route" sends you back rather than up. A stated annual review is an intention rather than a record. And an obligation to seek advice "before any action" includes the informal supportive conversation that feels obviously right.

The situational judgement section circled the particular difficulty of managing technical people: you are accountable for outcomes you do not produce, through people who will only tell you things if you make it safe to. The strong answers established causes before responses, treated the structural and behavioural problems as two problems, recorded exemptions, and were honest in the places where performing confidence would have been easier.

If one thing is worth carrying away, it is the pattern in the last two questions of the judgement section: the strongest response to your own failed initiative, and to evidence against your own decision, was to raise it yourself. That is not primarily about integrity. It is that a team which has seen you do it will bring you problems early, and everything else in this role gets easier when they do.

Good luck. This is a role where the good decisions are mostly invisible and the compounding is real, and the time you have put into this is well spent.
