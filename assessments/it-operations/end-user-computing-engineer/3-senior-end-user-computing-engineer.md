# Senior End User Computing Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a senior end user computing engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills and workplace judgement that predict success in a role. For a senior end user computing engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the materials you genuinely handle — team queues and rotas, incident and problem records, change impact assessments, performance statistics, capacity forecasts, test plans, and stakeholder reports — and the decisions you genuinely make, such as co-ordinating and prioritising your team's work to resolve technical incidents quickly, deciding which repeat issues to escalate to the lead engineer, the incident or problem manager, or software developers, and working closely with infrastructure, capacity and availability managers to fix underlying faults.

Why do these assessments matter at your level in particular? You occupy the pivot point of your team: still close enough to the tools to diagnose the hard faults yourself, but now responsible for how the whole queue moves — who does what, in which order, and which patterns deserve investigation rather than another round of individual fixes. That dual responsibility rests on a distinctive mix of mental skills: recognising trends across weeks of incident data, reasoning about causes and impacts before approving changes, checking reports and registers whose errors would now mislead a whole team, prioritising other people's work as well as your own, interpreting data sets and communicating them credibly to stakeholders, reading specifications and policies with precision, and making judgement calls where technical facts, team dynamics and service pressures collide. Psychometric assessments sample exactly these demands, which is why practising them sharpens both your test performance and your professional craft.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The four sections cover:

1. A **cognitive assessment** — pattern recognition across incident and performance data, logical deduction about causes and changes, error checking of team artefacts, prioritisation of competing demands, and applied problem solving.
2. A **numeric reasoning assessment** — percentages, rates, weighted figures, trends and forecasts, built on the ticket volumes, SLA statistics, capacity data and resource plans you actually handle.
3. A **verbal reasoning assessment** — precise comprehension of specifications, policies, vendor advisories, stakeholder correspondence and reports, with true/false/cannot-say discipline.
4. A **situational judgement assessment** — realistic dilemmas about team co-ordination, escalation, specialist consultation, preventative action and stakeholder communication.

To get the most from this guide: work through one section at a time; commit to an answer before reading each explanation; and treat every explanation as a mini-lesson, even when you answered correctly. At your level there is a second use, too — the worked reasoning in these pages is the kind you increasingly narrate to the engineers you manage, so consider each explanation a rehearsal for the coaching conversations your team needs from you.

You prioritise, diagnose and communicate for a living. Let's put that to work.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. For a senior engineer, the materials shift upward from single tickets toward the artefacts of co-ordination: multi-week incident trends, change impact assessments, team schedules, performance statistics, test conditions, and escalation decisions.

The typical format is an online, timed test lasting 15 to 30 minutes, with 15 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group; many platforms adapt difficulty to your performance and report speed and accuracy separately, so working both quickly and carefully matters. Short ungraded practice questions usually precede the real test.

For your role, cognitive assessment is particularly relevant because your professional value now lies in structured thinking applied at two levels simultaneously. At the incident level, you still diagnose and prioritise: investigating causes and finding resolutions is a named part of your incident management skill. At the team and service level, you initiate and monitor actions to investigate patterns and trends, assess the impact of proposed changes before actioning them, and decide what to escalate — to the lead engineer, the problem manager, or software developers — and what to resolve in place. Both levels are exercises in hypothesis, evidence and inference under time pressure, which is precisely what a well-designed cognitive test simulates. And because your conclusions now direct other people's work, an error costs more than your own time — which is why employers weight these skills heavily at senior level.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Problem management** skill: initiating and monitoring actions to investigate patterns and trends to resolve problems begins with seeing the trend at all — the model-specific fault signature, the step change after a release, the repeat issue hiding across three engineers' queues.
- **Logical deduction** maps to your **Change management** and **Incident management** skills: analysing and assessing the impact of change means reasoning from a proposed alteration to its consequences across services and users; diagnosing incidents means reasoning backward from symptoms to causes.
- **Error checking** maps to your **IT service reporting** and **Asset and configuration management** skills: producing relevant reports in an appropriate format and maintaining accurate configuration information both fail at the same point — the unnoticed inconsistency — and at your level the reports carry your team's credibility with stakeholders.
- **Prioritisation** maps to your core duty to **manage, co-ordinate and prioritise tasks** to resolve technical incidents as quickly as possible: the queue you sequence is now the team's, and mis-sequencing multiplies across engineers.
- **Applied problem solving** maps to your **Technical specialism** skill — using logical schemata to investigate problems, collecting performance statistics, optimising performance and forecasting resource needs — and to your **Testing** skill of reviewing requirements and defining test conditions: both are structured decomposition of messy situations into checkable parts.

### Practice questions

**Question 1 (easy) — Pattern recognition in a weekly trend**

Your team's "laptop battery failure" counts over eight weeks: 2, 3, 2, 3, 2, 9, 10, 11. Procurement confirms a new battery supplier was introduced in week 5's laptop builds. Which statement best characterises the data?

- A) The counts fluctuate randomly throughout.
- B) A stable baseline of 2–3 failures per week shifts to a sustained level around 9–11 from week 6 — a step change consistent with a cause introduced around week 5, making the supplier change the leading hypothesis to test.
- C) The supplier change is proven to be the cause.
- D) Failures always rise in the second month of a quarter.

**Correct answer: B**

**Explanation:** Characterise the shape first: weeks 1–5 oscillate in a tight 2–3 band; weeks 6–8 sit at 9–11 — roughly four times the baseline, sustained for three weeks. That is a step change, not noise (ruling out A), and its timing sits one build-cycle after the supplier switch, which makes the new batteries the leading hypothesis. But hypothesis is the operative word: option C converts correlation into proof, which the data cannot do — confirmation needs the next investigative step, such as checking whether the failing units actually contain the new supplier's batteries. Option D invents a seasonal pattern from a single period. This question is your problem management skill in miniature: pattern first (the step change), hypothesis second (the supplier), evidence third (the component check) — and only then escalation, with the trend data attached, to procurement and the lead engineer. Assessments reward the answer that claims exactly as much as the evidence supports, and no more.

**Question 2 (easy) — Deduction from a change impact rule**

Your change policy states: "Any change to a shared driver package must be impact-assessed against every laptop model in the estate that uses the package. A change may proceed only when every affected model has either passed testing or been explicitly excluded from the rollout." The estate has four models using the package: P, Q, R and S. Testing has passed on P and Q; R has failed testing; S has not yet been tested. The proposed rollout excludes R. May the change proceed?

- A) Yes — the failing model has been excluded.
- B) No — model S has neither passed testing nor been excluded.
- C) Yes — a majority of models have passed.
- D) No — a change may never proceed while any model has failed testing.

**Correct answer: B**

**Explanation:** The rule imposes a universal condition: every affected model must be in one of two states — passed, or excluded. Walk the four models: P passed; Q passed; R failed but is excluded, which the rule explicitly permits; S has neither passed nor been excluded — the condition fails on S, so the change may not proceed: answer B. Option A checks only the model that drew attention (the failure) and forgets the one that drew none — the classic audit gap, since untested is easier to overlook than failed. Option C imports a majority principle the rule does not contain; universal conditions are not votes. Option D over-reads the rule: exclusion is a legitimate route for a failing model, and the policy says so. Analysing and assessing the impact of change — your named change management skill — is largely the discipline of universal quantifiers: "every model", "all affected services", "each user group". In assessments and change boards alike, the question is never "is the known problem handled?" but "is every case accounted for?"

**Question 3 (easy) — Error checking a team rota against rules**

Your cover rules: (i) the walk-up desk needs exactly two engineers every day; (ii) no engineer works the desk more than two days in a week; (iii) at least one of the two daily desk engineers must be senior-qualified (marked *). The draft rota reads:

- Mon: Amir*, Beth
- Tue: Beth, Chen
- Wed: Chen, Dana*
- Thu: Beth, Amir*
- Fri: Dana*, Chen

Which rule is broken, and by whom?

- A) Rule (i) on Wednesday
- B) Rule (ii) by Beth and Chen
- C) Rule (iii) on Tuesday only
- D) Rules (ii) and (iii): Beth and Chen each work three days, and Tuesday has no senior-qualified engineer

**Correct answer: D**

**Explanation:** Audit each rule across the whole week. Rule (i): every day lists exactly two engineers — satisfied. Rule (ii): count appearances — Amir 2, Beth 3 (Mon, Tue, Thu), Chen 3 (Tue, Wed, Fri), Dana 2 — so Beth and Chen both breach the two-day limit. Rule (iii): scan for the asterisk day by day — Mon has Amir*, Wed has Dana*, Thu has Amir*, Fri has Dana*, but Tuesday pairs Beth with Chen, neither senior-qualified — breach. Two rules are broken, so D is the complete answer; options B and C are each half-right, and half-right findings are the danger in real audits because they end the check early. The method that scales — here, in asset registers, in test results — is one rule at a time across all cases, never one case at a time against whichever rule comes to mind. Rota-checking may look administrative, but it is the same verification skill your reporting and configuration duties depend on, and the Tuesday gap is exactly the kind of quiet failure that surfaces as a badly-handled incident three weeks later.

**Question 4 (moderate) — Prioritising the team's morning**

At 08:55 you have four engineers available and five demands:

1. A P1: the case-management service is down for an entire 200-person directorate; infrastructure suspects a network component and asks for a desk-side engineer to run local diagnostics at the affected site.
2. Two P3 tickets promised for completion today, each about an hour's work.
3. A change window 10:00–12:00 for a pre-approved software rollout to thirty machines, prepared last week.
4. An associate asks for help with a diagnosis they have been stuck on since yesterday afternoon.
5. Your monthly performance report to the service desk manager, due at 17:00.

What is the strongest allocation?

- A) All four engineers to the P1 to show urgency; everything else waits.
- B) One strong diagnostician to the P1 site immediately; one engineer to the change window as planned; one engineer to the two P3 promises; you take fifteen minutes to unstick the associate, then draft the report between interruptions.
- C) You go to the P1 site yourself; the rest of the team continues as scheduled without briefing.
- D) One engineer to the P1; three engineers to the change rollout to finish it early; the P3 promises, the associate and the report wait until afternoon.

**Correct answer: B**

**Explanation:** The P1 is the top priority, but priority means right resource, not all resources: infrastructure needs one capable local diagnostician, and four engineers at one site would idle three while promises break elsewhere — option A confuses visible effort with effectiveness. Option B covers the full portfolio in impact order: the P1 gets immediate expert attention; the change window — a hard external constraint agreed with users — proceeds as planned; the two same-day promises are kept, protecting the team's credibility in small things; the stuck associate gets fifteen minutes that unlock a day of their capacity (a high-leverage use of senior time, and note they have been stuck since yesterday — a signal to address, gently, about asking earlier); the report, deadline 17:00, absorbs the slack. Option C removes the co-ordinator during the day's biggest incident and leaves the team unbriefed — at your level, going hands-on is sometimes right, but never silently. Option D over-resources a pre-prepared routine rollout while promised work and a blocked colleague wait. The senior pattern: match resource to need, protect commitments, spend your own time where it multiplies.

**Question 5 (moderate) — Deduction about a capacity symptom**

The virtual desktop service slows every weekday from 11:45 to 13:15. You gather: (i) user session counts peak 09:00–10:00, not midday; (ii) the backup job runs 02:00–04:00; (iii) an automated inventory scan of all endpoints runs 11:30–13:30; (iv) the slowdown began three weeks ago, the same week the scan was extended from servers-only to all endpoints. What is the strongest next step?

- A) Move the backup job to the weekend.
- B) Add session capacity to handle the midday peak.
- C) Test the inventory-scan hypothesis — its window brackets the slowdown and its scope changed exactly when the symptom began — for example by rescheduling or narrowing one day's scan and observing the effect.
- D) Ask users to avoid the service at lunchtime.

**Correct answer: C**

**Explanation:** Score each candidate cause against two tests: does its footprint match the symptom's timing, and does its history match the symptom's onset? The backup job (option A) fails the timing test by eight hours. Session load (option B) fails it too — the user peak is 09:00–10:00, yet the service is fine then and slow at 11:45; adding capacity would spend money on a disproven hypothesis. The inventory scan passes both tests: its 11:30–13:30 window brackets the 11:45–13:15 slowdown, and its scope expansion three weeks ago coincides with the symptom's appearance. Option C then does what a senior engineer's method requires — it tests rather than concludes, using a cheap, reversible experiment (one day's rescheduled scan) whose result will be decisive either way. Option D manages users around a fault instead of fixing it. This is your technical specialism working as designed: collect performance statistics, use logical schemata — here, the footprint-matching schema — and consult the relevant specialists (the scan's owners, infrastructure) with a tested finding rather than a guess. In assessments, the "strongest next step" is almost always the cheapest action that discriminates between hypotheses.

**Question 6 (moderate) — Error checking a change request document**

You are reviewing an engineer's change request before submission. The template requires: description, affected services, risk assessment, rollback plan, and test evidence. The draft reads: "Description: update wireless drivers on all 300 estate laptops to v9.2. Affected services: none — this is a client-side change. Risk: low; v9.2 is vendor-recommended. Rollback: reinstall v9.1 from the deployment tool. Test evidence: v9.2 ran on 10 pilot laptops for two weeks, zero wireless incidents."

Which element most needs challenge before submission?

- A) The rollback plan — reinstalling v9.1 may not be possible.
- B) The "affected services: none" claim — a wireless driver change on 300 laptops affects every service those users reach over wireless; the field confuses "no server-side components changed" with "no service impact."
- C) The test evidence — ten laptops is too small a pilot to mention.
- D) The description — it should name the vendor.

**Correct answer: B**

**Explanation:** The document's load-bearing error is a category confusion. "Affected services: none" is true only in the narrow sense that no server-side component is being altered — but the field exists to drive impact assessment, and the honest answer is that wireless connectivity itself, and therefore every service reached over it by 300 users, is in the blast radius of a bad driver. Writing "none" suppresses exactly the scrutiny (scheduling, communication, phased rollout) the change deserves; if v9.2 misbehaves on some hardware variant the pilot missed, the impact is estate-wide loss of connectivity — the same class of error as calling a foundation repair "no impact on the building" because only the basement is touched. Option A raises a fair verification question (is v9.1 still packaged and deployable?) but the draft at least states a plausible plan. Option C undervalues a genuinely useful pilot — ten machines for two weeks is modest but meaningful evidence, worth strengthening with hardware-variant coverage rather than dismissing. Option D is cosmetic. Reviewing documents for the claim that hides the risk — rather than the field that merely looks thin — is what analysing and assessing the impact of change means at review time, and it is a skill assessments probe hard at senior level.

**Question 7 (moderate) — Defining test conditions from a requirement**

A requirement reads: "The new self-service password reset must complete within two minutes for a typical user, work on both corporate laptops and personal phones, and lock after three failed identity checks." You must define test conditions. Which set most completely covers the requirement?

- A) Time a reset on a corporate laptop; confirm it completes within two minutes.
- B) Time resets on a corporate laptop and a personal phone; confirm both complete within two minutes; attempt three failed identity checks and confirm lockout occurs; attempt two failed checks then a successful one and confirm no lockout.
- C) Attempt three failed identity checks and confirm lockout; test on a personal phone.
- D) Time resets on both device types; confirm lockout after five failed checks.

**Correct answer: B**

**Explanation:** Decompose the requirement into its testable claims: (1) completion within two minutes; (2) on corporate laptops; (3) on personal phones; (4) lockout after three failed checks. Option B tests all four — and adds the boundary condition that separates adequate testing from good testing: two failures followed by success must not lock the account, because a lockout rule's most common defect is firing early and locking out legitimate users who mistyped twice. Option A covers half of one claim-pair; option C ignores the timing requirement entirely; option D tests lockout against the wrong threshold — five, not the specified three — which would pass a non-compliant build. This is your testing skill exactly as your role summary states it: review requirements and specifications, and define test conditions — where "define" means translating each clause, including its boundaries, into a checkable case. The habit that generalises: for every threshold in a specification (three failures, two minutes), test at the threshold, just below it, and the negative case. Requirements name the happy path; defects live at the edges.

**Question 8 (moderate) — Prioritisation of escalations**

Four items are candidates for escalation this week. Given limited attention from the parties above you, which one most needs escalation beyond your team — and to whom?

1. A one-off laptop fault an engineer resolved yesterday after four hours' struggle.
2. Login failures recurring every Monday morning for three weeks across all directorates, each time self-resolving by 09:40; your team's diagnostics point to an authentication component your team cannot see inside.
3. An associate's persistent lateness with ticket updates.
4. A stock shortfall of loan laptops projected in six weeks.

- A) Item 1, to the problem manager — four hours is too long for one fault.
- B) Item 2, to the problem manager and the infrastructure/availability specialists who own the authentication component — a recurring, estate-wide, self-resolving pattern your team cannot investigate further is precisely what the escalation route exists for.
- C) Item 3, to the service desk manager as a formal performance concern.
- D) Item 4, to procurement as an emergency order.

**Correct answer: B**

**Explanation:** Apply the escalation test: is the issue recurring or high-impact, and has it exceeded your team's authority or visibility? Item 2 scores on every axis — three consecutive weeks (recurring), all directorates (broad impact), and a root cause inside a component your team cannot see (beyond your reach). Its self-resolving nature makes it more escalation-worthy, not less: nothing in your span will change, so Monday's disruption will repeat indefinitely until the component's owners investigate — and your role summary names exactly this duty: identify and escalate repeat issues to the incident or problem manager and the relevant specialists. Item 1 is resolved and singular — a candidate for a knowledge article, not escalation. Item 3 is a line-management matter to address yourself first; escalating it unaddressed exports your own job. Item 4 needs action — a routine order placed now — but six weeks of runway makes it planning, not emergency escalation; save the emergency channel for emergencies or it stops working. The senior discipline: escalate patterns and blocked investigations upward with evidence; handle events, people and plannable logistics within your span.

**Question 9 (challenging) — Multi-constraint incident allocation**

At 14:00, three incidents arrive simultaneously: (X) the directorate print service is down — resolution requires server-side access that only engineers with elevated rights hold; (Y) a P2 on the deputy director's laptop — she is presenting externally at 15:30; (Z) a walk-in reports their laptop was possibly left on a train — your security procedure requires immediate remote-wipe initiation and an incident report to the security team. Available: you (elevated rights, senior), engineer E1 (elevated rights, currently mid-way through a promised P3), and engineer E2 (no elevated rights, free now, strong desk-side diagnostician).

Which allocation works best?

- A) You take X; E2 takes Y; you also initiate Z's remote-wipe immediately before starting X, as it takes minutes and is time-critical; E1 continues the promised P3.
- B) E1 abandons the P3 for X; you take Y personally because of the seniority of the user; E2 handles Z.
- C) E2 takes X; you take Z; E1 takes Y after finishing the P3.
- D) You take Y; E1 takes Z; X waits until someone with rights is free.

**Correct answer: A**

**Explanation:** Constraint-match before allocating. X requires elevated rights — held only by you and E1. Z's remote-wipe is genuinely time-critical (data exposure grows by the minute) but short: initiating a wipe and logging the security report takes minutes, and procedure permits any engineer to trigger it — though in option A you do it yourself precisely because it is quick and you are already context-switching. Y needs strong desk-side diagnosis against a hard 15:30 deadline — E2's exact profile, and no elevated rights are needed. That leaves X with you (E1's promised P3 survives, protecting a commitment) — the print service gets elevated-rights attention within minutes of the wipe being triggered. Option B breaks a promise unnecessarily and mis-assigns you to Y for seniority-of-user reasons — user rank does not require engineer rank; it requires competence and urgency-matching. Option C gives X to the one engineer who cannot touch it — an allocation that fails on a hard constraint, however sensible it looks otherwise. Option D leaves a directorate-wide service down while its only qualified resolvers do other work, and delays the wipe behind E1's P3 wrap-up. The method: list each task's hard constraints (rights, deadline, duration), then allocate scarce capabilities to the tasks that require them, and protect promises with whatever remains.

**Question 10 (challenging) — Reasoning about a misleading aggregate**

Your quarterly report shows first-time fix (FTF) improving: 68% → 71% → 74% across three months. A stakeholder proposes citing your team as the model for others. Before accepting the praise, you disaggregate: password-and-access tickets (FTF steady at 92%) have grown from 30% to 55% of total volume after a directorate onboarding; hardware tickets' FTF actually fell from 61% to 54%. What is the honest characterisation?

- A) The improvement is real and the team should be the model.
- B) The headline rise is a mix effect: an influx of high-FTF password tickets lifted the average while underlying hardware performance declined — the report should present both strands, celebrate neither, and investigate the hardware decline.
- C) The figures contradict each other, so the data is unreliable.
- D) Hardware FTF fell, so the team is actually performing worse overall.

**Correct answer: B**

**Explanation:** This is composition shift — the aggregate moved because the mix moved, not because performance improved. Password tickets fix first-time 92% of the time; when their share of volume nearly doubles, the blended average rises mechanically even while every underlying category stagnates or declines. The disaggregation reveals the true picture: one category steady, one deteriorating (61% → 54% is a seven-point fall worth investigating — new hardware? lost expertise? part shortages?). Option B states exactly this, and its reporting posture matters as much as its arithmetic: presenting both strands is what interpreting a data set and communicating it to others means when the honest story is less flattering than the headline — stakeholder trust in your reports is a service asset you protect by correcting favourable errors as energetically as unfavourable ones. Option A accepts credit the data does not support, and invites other teams to copy a mirage. Option C mistakes explainable structure for unreliability — the figures cohere perfectly once decomposed. Option D overcorrects: the password stream's performance is genuinely strong and its growth genuinely absorbed; "worse overall" is as unsupported as "better overall." When any aggregate moves, your first question is now permanent: did performance change, or did the mix?

**Question 11 (challenging) — Preventative measure selection**

Investigation of a quarter's laptop-damage incidents (60 total) shows: 32 are cracked screens from laptops carried unprotected between buildings; 15 are liquid damage at desks; 8 are drops during badge-access door transits while juggling equipment; 5 are miscellaneous. Budget allows one primary preventative measure this quarter. Which choice reflects the strongest reasoning?

- A) A poster campaign about general laptop care — it addresses all four categories at once.
- B) Issue protective sleeves to the staff who regularly move between buildings — it targets the largest single cause (53% of damage), addresses the mechanism directly (unprotected transit), and its effect can be measured in next quarter's category counts.
- C) Ban drinks at desks — liquid damage is the most preventable category.
- D) Fund whichever measure the most recently damaged user's directorate requests.

**Correct answer: B**

**Explanation:** Preventative investment is a targeting problem: rank causes by magnitude, match the measure to the mechanism, and build in a way to verify effect. The category data does the ranking for you — transit screen damage is 32 of 60 incidents (53%), more than double the next category — and sleeves address its mechanism physically rather than exhortatively. The measurability clause matters: because the intervention maps to one category, next quarter's counts will show whether it worked, turning spend into evidence — determining preventative measures, as your problem management skill puts it, includes determining whether they prevented anything. Option A spreads effort across everything and concentrates it on nothing; awareness campaigns fade in weeks and their effect is unmeasurable against any single mechanism. Option C asserts "most preventable" without evidence and targets a category half the size of the leader — and desk-drink bans have compliance costs posters never show. Option D allocates by recency and noise rather than data. The senior habit under test: when incident data is categorised, the biggest bar in the chart — not the most recent, most vivid, or most requested item — is where prevention money goes first, with a measurement plan attached.

**Question 12 (challenging) — Diagnosing across team boundaries**

Users report that large file transfers to a partner organisation fail intermittently. Your desk-side checks clear the laptops: failures occur across models, buildings and both wired and wireless. Infrastructure's monitoring shows their network links healthy. The partner's IT reports "no issues our side." The failures cluster between 15:00 and 17:00 daily and affect only files above roughly 500 MB. What is the strongest next move?

- A) Accept the three "all clear" reports and close the investigation as unreproducible.
- B) Convene the specialists across the boundary — infrastructure, and through agreed channels the partner's network team — around the two discriminating facts (time-of-day clustering, size threshold), and propose a joint test: schedule controlled large-file transfers inside and outside the window while both sides capture diagnostics simultaneously.
- C) Advise users to split all files below 500 MB permanently and close the ticket as workaround-resolved.
- D) Escalate to the lead engineer that the partner organisation is at fault, since your side has been cleared twice.

**Correct answer: B**

**Explanation:** Three teams have each checked their own component and found it healthy — yet the failure exists, which means it almost certainly lives between components (a shared path, an intermediate device, a time-varying load) where nobody's individual monitoring looks. The two discriminating facts are diagnostic gold: a daily 15:00–17:00 window implies a load- or schedule-correlated factor; a 500 MB threshold implies a duration- or session-size-sensitive mechanism. Option B does what your role summary specifies — effectively consult specialists where required, working closely with infrastructure — and shapes the consultation around a designed joint observation, because simultaneous capture during controlled transfers is the cheapest experiment that can see across the boundary. Option A mistakes three partial all-clears for a global one; "each part is healthy" does not sum to "the whole is healthy." Option C converts a useful interim workaround into a permanent service degradation and closes the ticket on an undiagnosed fault that will surface elsewhere. Option D escalates blame without evidence — being cleared twice localises nothing when the failure sits on a shared path, and accusations poison exactly the cross-organisation co-operation the diagnosis needs. The pattern for boundary faults: stop re-checking components, start observing the whole path, and make the discriminating facts drive the experimental design.

### Preparation tips

- **Practise on your team's real data.** Take a month of ticket statistics and interrogate them: which trends are steps, which are noise, which aggregates hide mix effects? The instincts these questions build are the assessment's exact target.
- **Adopt the footprint test.** For every suspected cause, ask whether its footprint — timing, location, scope, onset — matches the symptom's. Most wrong hypotheses die in ten seconds under this test, in assessments and investigations alike.
- **Audit one rule at a time.** Whether checking rotas, registers, change documents or test results, sweep each rule across all cases rather than each case against remembered rules. Completeness comes from method, not concentration.
- **Rank before you spend.** In prioritisation and prevention questions, force yourself to write the magnitude ranking first — biggest impact, largest category, hardest constraint — then match resources to it. Options that serve vividness over magnitude are planted traps.
- **Design the discriminating step.** When a question asks for the "next step," look for the cheapest reversible action that separates the surviving hypotheses. That is the answer more often than any repair, replacement or escalation.
- **Time-box and move.** Ninety seconds of honest effort per question, best answer chosen, flagged, moved on. Senior queues and senior assessments reward the same thing: throughput with judgement.

### Common pitfalls to avoid

- **Claiming more than the evidence supports.** Step changes suggest causes; they do not prove them. Options asserting proof from correlation are wrong even when the hypothesis is right.
- **Auditing only where attention falls.** The failed test case is checked; the untested one is forgotten. Universal conditions fail at their quietest member — check every case, especially the boring ones.
- **All resources to the loudest incident.** Flooding the P1 while promises break elsewhere reads as urgency and scores as mis-allocation. Match resource to need; protect commitments with the remainder.
- **Trusting aggregates.** Any average that moved may be a mix effect. Disaggregate before celebrating — or citing — a trend.
- **Treating workarounds as resolutions.** Splitting the files, avoiding the lunchtime slowdown, rebooting every Monday — options that manage around an undiagnosed fault leave it growing. Interim relief yes; closure no.
- **Escalating blame instead of evidence.** "Their side must be at fault" advances nothing. Escalations carry discriminating facts and proposed next steps, or they carry noise.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your role genuinely produces and consumes: SLA percentages, incident trends, capacity and utilisation figures, cost comparisons, forecast calculations, and the statistics behind the reports you produce for stakeholders.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions, each presenting a table, chart or described dataset. A calculator and rough paper are normally allowed; the test measures selection of the right figures, choice of the right method, and sense-checking of results — under time pressure. Scoring is objective against a norm group, often reporting accuracy and speed separately.

At senior level, numeric fluency carries a double weight. First, you produce numbers: your IT service reporting skill requires you to produce relevant reports in an appropriate format and agreed timeframe, and to interpret a data set and communicate it to others — which means every percentage, average and trend you publish is one you should be able to defend line by line. Second, you consume numbers to decide: co-ordinating and prioritising the team's work means reading demand data; your technical specialism includes collecting performance statistics, optimising performance and forecasting resource needs; and working with capacity and availability managers means holding your own in conversations built entirely on utilisation figures, growth rates and thresholds. An error in your arithmetic now propagates into rotas, orders, escalations and stakeholder confidence.

The mathematics remains practical — percentages, rates, weighted averages, trends, and forecasting — but the questions at this level lean harder on interpretation: spotting the mix effect, the wrong base, the misleading average, and the forecast built on the wrong growth model.

### How this assessment maps to your role

- **Rates, percentages and weighted figures** map to your **IT service reporting** skill: producing reports and discussing changes in reporting processes with stakeholders requires computing SLA attainment, first-time-fix and reopen rates exactly as defined — and recognising when a blended figure misleads.
- **Trend analysis** maps to your **Problem management** skill: initiating and monitoring actions to investigate patterns and trends starts from the arithmetic of trends — distinguishing steps from drift, additive from multiplicative growth.
- **Capacity and utilisation calculations** map to your **Technical specialism** skill (optimise performance and forecast resource needs) and your duty to work closely with **capacity and availability managers**: thresholds, headroom and run-out dates are shared vocabulary in those conversations.
- **Workload arithmetic** maps to your duty to **manage, co-ordinate and prioritise tasks**: rota maths, demand-versus-capacity comparisons and backlog projections are how a queue is steered by evidence rather than feel.
- **Comparative analysis** maps to your **Change management** skill: analysing and assessing the impact of change often reduces to before/after comparisons that must be computed on fair bases.
- **Test metrics** map to your **Testing** skill: analysing and reporting test activities and results means summarising pass rates, defect densities and coverage honestly.

### Practice questions

**Question 1 (easy) — Team SLA attainment**

Your team closed 320 incidents last month; 272 were within SLA. What was the SLA attainment percentage?

- A) 82%
- B) 85%
- C) 88%
- D) 90%

**Correct answer: B**

**Explanation:** Attainment = within-SLA ÷ total closed × 100. Step 1: 272 ÷ 320 = 0.85. Step 2: × 100 = 85% — answer B. Sense-check by complement: 320 − 272 = 48 breaches; 48 ÷ 320 = 0.15 = 15%, and 100 − 15 = 85 — consistent. At senior level the habit worth adding is exactly that complement check: breaches are usually the small number, easier to verify at a glance, and stakeholders often ask about them first. A figure you have verified two ways is a figure you can defend in a stakeholder meeting without reaching for the source data.

**Question 2 (easy) — Utilisation against a threshold**

The capacity manager flags any file store running above 80% utilisation. Store A holds 1.2 TB of a 1.6 TB allocation; Store B holds 3.4 TB of 4.0 TB. Which stores breach the threshold?

- A) Neither
- B) Store A only
- C) Store B only
- D) Both

**Correct answer: C**

**Explanation:** Compute each utilisation. Store A: 1.2 ÷ 1.6 = 0.75 = 75% — below the 80% threshold. Store B: 3.4 ÷ 4.0 = 0.85 = 85% — above it. Answer C. The trap is judging by absolute headroom: Store A has 0.4 TB free and Store B has 0.6 TB free, so B "has more space" — but thresholds are set on proportions because growth consumes proportionally, and B's larger free space serves a larger demand. When you talk to capacity managers, per-store percentages are the shared language; absolute gigabytes mislead the moment stores differ in size. Divide first, compare second.

**Question 3 (easy) — Average handling time for a rota decision**

Yesterday's twelve walk-up visits took (minutes): 5, 10, 15, 5, 20, 10, 5, 30, 10, 15, 5, 50. What are the mean and median handling times?

- A) Mean 15, median 10
- B) Mean 14, median 12
- C) Mean 15, median 12.5
- D) Mean 12.5, median 15

**Correct answer: A**

**Explanation:** Mean: total ÷ count. Sum stepwise: 5+10=15; +15=30; +5=35; +20=55; +10=65; +5=70; +30=100; +10=110; +15=125; +5=130; +50=180. Mean = 180 ÷ 12 = 15 minutes. Median: sort the values — 5, 5, 5, 5 (positions 1–4), 10, 10, 10 (positions 5–7), 15, 15 (8–9), 20 (10), 30 (11), 50 (12). With twelve values, the median is the average of the 6th and 7th values: (10 + 10) ÷ 2 = 10 minutes. So mean 15, median 10 — answer A. Position-counting is where median calculations go wrong, so write the sorted list out and number the positions rather than eyeballing it. The operational reading matters for your rota decision: the mean (15) sits fifty percent above the median (10) because one 50-minute visit drags it upward; the median tells you the typical visit a desk engineer experiences, while mean × volume still gives true total workload. Use both, knowing what each is for — a rota built on the mean alone would overstaff the typical hour, and one built on the median alone would underprovide for the long-visit tail.

**Question 4 (moderate) — Percentage change with the right base**

Incident volume: June 400, July 500, August 450. A colleague reports: "+25% in July, then −10% in August, so we're +15% overall." Which is correct?

- A) The monthly changes are right and the overall is +15%.
- B) The monthly changes are right (+25%, −10%), but the overall change June→August is +12.5%, because the −10% applies to July's larger base.
- C) The monthly changes are wrong.
- D) Overall change cannot be computed from these figures.

**Correct answer: B**

**Explanation:** Verify each step. July: (500−400) ÷ 400 = +25% ✓. August: (450−500) ÷ 500 = −10% ✓. Overall: (450−400) ÷ 400 = 50 ÷ 400 = +12.5% — not +15%. Percentage changes do not add, because each applies to a different base: +25% then −10% compounds as 1.25 × 0.90 = 1.125, i.e. +12.5%. The colleague's arithmetic error is three points — small enough to survive review, large enough to misstate a quarter's demand trend to stakeholders. When you produce reports, compute period-over-period changes from the raw endpoint values, never by summing intermediate percentages; when you review others' reports, this is one of the first checks to run. Answer B.

**Question 5 (moderate) — Weighted SLA across priorities**

Last month: P1 incidents — 10 closed, 90% in SLA; P2 — 40 closed, 85% in SLA; P3 — 150 closed, 92% in SLA. What is the overall in-SLA percentage across all incidents?

- A) 89%
- B) 90.5%
- C) 91%
- D) 92%

**Correct answer: B**

**Explanation:** Convert percentages to counts before combining. P1: 90% of 10 = 9. P2: 85% of 40 = 34. P3: 92% of 150 = 138. Total in SLA: 9 + 34 + 138 = 181. Total closed: 10 + 40 + 150 = 200. Overall: 181 ÷ 200 = 0.905 = 90.5% — answer B. A straight average of the three percentages ((90+85+92) ÷ 3 = 89%) undercounts because it ignores that P3, the best-performing category, dominates the volume. Notice also the reporting nuance for stakeholder conversations: the blended 90.5% conceals that P2 — often the priority stakeholders feel most — runs at 85%. Producing the overall figure and the per-priority breakdown together is what interpreting a data set for others honestly looks like.

**Question 6 (moderate) — Capacity forecast to a threshold**

A shared storage volume is at 60% utilisation today and has grown by 3 percentage points per month, steadily, for a year. The capacity manager's escalation threshold is 85%, and expanding the volume takes two months from decision to delivery. When must the expansion decision be made, at the latest, to stay below threshold?

- A) Month 6 — the threshold is crossed around month 8, and delivery takes two months
- B) Month 8
- C) Immediately
- D) Month 4

**Correct answer: A**

**Explanation:** Project the growth as a simple linear model: utilisation = 60 + 3m, where m is months from now. Find the threshold crossing: 60 + 3m = 85 → 3m = 25 → m ≈ 8.3, so the volume crosses 85% early in month 8–9. Step back by the two-month delivery time: the decision must be made by roughly month 6.3, so month 6 is the latest whole-month decision point — decide in month 6, delivery lands in month 8, just ahead of the crossing. Answer A. Option B decides at the crossing itself, guaranteeing two months above threshold; option D is earlier than the question's "at the latest" asks for; option C overreacts to a deadline eight months out. Having computed the answer, note the professional postscript you would add in the real meeting: month 6 is the mathematical deadline with zero margin for delivery slippage, demand spikes, or slow approval cycles — so the recommendation to your capacity manager would be a decision by month 4 or 5, with the buffer stated explicitly as insurance on the lead time. Forecasting resource needs, as your technical specialism puts it, means computing the deadline exactly — and then choosing not to live on it.

**Question 7 (moderate) — Before/after comparison on a fair base**

You deployed a preventative fix at the end of March. Reopened-ticket counts: January 30, February 28, March 32, April 18, May 16. Ticket volumes were stable across all five months. What is the fairest statement of the fix's effect?

- A) Reopens fell by 14 from March to April — a 44% reduction against the pre-fix average of 30, sustained into May; with stable volumes, the timing and persistence support (but do not prove) the fix as cause.
- B) Reopens fell 44% in April, proving the fix worked.
- C) The reduction is within normal variation.
- D) Reopens will reach zero by August if the trend continues.

**Correct answer: A**

**Explanation:** Establish the baseline: January–March average = (30+28+32) ÷ 3 = 30, oscillating in a tight 28–32 band. Post-fix: April 18, May 16 — a drop to roughly 55% of baseline ((30−17) ÷ 30 ≈ 43–44% reduction using the two-month post average of 17), sustained rather than momentary, with volumes stable (removing the most common confounder). Option A states the arithmetic and calibrates the claim: "support but do not prove" — other March-end changes could exist. Option B's arithmetic is right and its epistemology wrong: proof needs elimination of alternatives, not one favourable comparison. Option C ignores that 18 and 16 sit far outside the 28–32 band that defined normal variation for three months. Option D extrapolates a two-point trend linearly to an absurd conclusion; preventative fixes remove their targeted cause, and the remaining reopens likely have different causes the fix never addressed. This is the measurement half of determining preventative measures: quantify baseline, quantify after, hold conditions constant, claim proportionately.

**Question 8 (moderate) — Cost comparison for a recommendation**

Two options for replacing 60 ageing laptops. Option 1: buy new at £700 per unit, with a three-year warranty included. Option 2: refurbish at £250 per unit now, but refurbished units carry an expected 20% annual failure rate requiring £150 average repair each failure, versus 5% for new units (repairs under warranty: £0). Over three years, which option costs less, and by roughly how much?

- A) Refurbishment, by about £10,000
- B) New purchase, by about £3,000
- C) Refurbishment, by about £21,600
- D) They cost about the same

**Correct answer: C**

**Explanation:** Cost each option over the full three years — purchase plus the expected repair stream. Option 1 (new): 60 × £700 = £42,000 to buy; the 5% annual failures are repaired under warranty at £0, so the three-year total is £42,000. Option 2 (refurbished): 60 × £250 = £15,000 to buy; failures run at 20% of 60 = 12 units per year, costing 12 × £150 = £1,800 per year, so £1,800 × 3 = £5,400 in repairs; three-year total £15,000 + £5,400 = £20,400. Difference: £42,000 − £20,400 = £21,600 in refurbishment's favour — answer C. The structural insight: refurbishment wins despite quadruple the failure rate because the purchase gap (£27,000) dwarfs the repair stream (£5,400) — a pattern common in total-cost comparisons, where the headline risk (failures) is real but small next to the quiet certainty of unit price. In a real recommendation, though, the spreadsheet is not the whole answer: 12 failures a year means 36 user-disruption events over three years that the cost table never shows, plus engineer time per repair — worth explicit sentences in any report a stakeholder will act on, because the cheapest option on paper is only the best option when its non-cost burdens have been priced honestly too.

**Question 9 (challenging) — Backlog projection under demand growth**

Your team resolves 150 tickets per week at full strength. Demand has grown 4% per month for six months and now stands at 140 per week. The current backlog is 60 tickets. Two engineers (of eight) leave next month, cutting resolution capacity by 25% for the eight weeks it takes to recruit and induct replacements. Roughly what backlog should you expect at the end of those eight weeks, assuming demand growth continues?

- A) About 60 — inflow and outflow roughly balance
- B) About 300 — capacity falls to ~112/week while demand runs at ~141–148/week, adding roughly 28–32 tickets weekly for eight weeks on top of the existing 60
- C) About 120 — the backlog doubles
- D) Backlogs cannot be projected from these figures

**Correct answer: B**

**Explanation:** Model inflow minus outflow. Capacity during the gap: 150 × 0.75 ≈ 112 per week. Demand: starts at 140 and grows 4% per month (roughly 1% per week), so over eight weeks it runs from about 141 up to about 148, averaging ≈ 144. Weekly shortfall: 144 − 112 ≈ 32 at the average, or 28 if you conservatively hold demand flat at 140. Eight weeks × 28–32 ≈ 225–255 tickets added; plus the existing 60 gives roughly 285–315 — call it about 300, answer B. Options A and C are wishful (they require shortfalls the arithmetic rules out); D is defeatist — the figures support a perfectly serviceable projection. The precision lesson: backlog projections are sensitivity ranges, not point values — quote "roughly 280–320" with your assumptions stated. The operational lesson is why this calculation matters: performed before the engineers leave, it converts "we'll cope" into a quantified case for interim cover, overtime, or demand triage — exactly the resource forecasting your technical specialism names, and exactly the evidenced escalation your lead engineer and service desk manager need from you.

**Question 10 (challenging) — Test results summary**

Acceptance testing of a new build ran 240 test cases: 210 passed, 18 failed, 12 blocked (could not run because an environment dependency was down). The vendor's summary reports "92.6% pass rate" and recommends release. Assess the claim.

- A) The figure is correct: 210 ÷ (210 + 18) = 92.1%... approximately 92.6% — accept it.
- B) The vendor computed 210 ÷ 227 or similar; the honest headline is 210 ÷ 240 = 87.5% executed-and-passed, with 18 failures (7.5%) and 12 blocked cases (5%) that represent untested functionality — the blocked cases must be run, and the failures assessed for severity, before any release recommendation.
- C) 92.6% exceeds 90%, so release is justified.
- D) Pass rates are meaningless in acceptance testing.

**Correct answer: B**

**Explanation:** Recompute every candidate denominator. Against all cases: 210 ÷ 240 = 87.5%. Against executed cases only: 210 ÷ 228 = 92.1%. The vendor's 92.6% ≈ 210 ÷ 227 — close to the executed-only basis (the odd case perhaps reclassified). The arithmetic sleight is the denominator: excluding the 12 blocked cases treats untested functionality as if it did not exist, inflating the headline by five points. Option B names both the fair figure and the decision logic: blocked ≠ passed — those 12 cases are unknown territory, and 18 failures need severity assessment (one critical failure outweighs seventeen cosmetic ones; a raw pass rate cannot say which you have). Option A accepts the vendor's denominator without checking it. Option C applies a threshold to an inflated figure — thresholds are only as good as the arithmetic beneath them. Option D overcorrects into nihilism. This is your testing skill as the role defines it — analyse and report test activities and results — plus the senior addition: when someone else's summary supports their own recommendation, recompute the denominator first. Managing supplier-adjacent test claims honestly is also groundwork for the vendor management your next role level will formalise.

**Question 11 (challenging) — Interpreting a distribution for a staffing case**

Resolution times for the team's 200 incidents last month: median 45 minutes; mean 95 minutes; 90th percentile 240 minutes; the ten longest incidents averaged 14 hours each and were all hardware faults requiring parts. The service desk manager, seeing the mean, proposes an efficiency review of the team. What is the strongest evidence-based response?

- A) Accept the review — a 95-minute mean against a 45-minute median suggests general slowness.
- B) Show the decomposition: the median and 90th percentile describe a team resolving typical incidents in 45 minutes and 90% within four hours; the mean is inflated by ten parts-dependent hardware incidents (14-hour average) whose duration is set by parts logistics, not engineer efficiency — so the actionable target is the parts pipeline (stock levels, supplier lead times), not team working speed.
- C) Exclude the ten worst incidents from future reports so the mean looks better.
- D) Argue that means should never be reported.

**Correct answer: B**

**Explanation:** A mean double the median announces a right-skewed distribution: most work is quick, a tail is very slow. Quantify the tail's pull: the ten longest incidents contribute 10 × 840 = 8,400 minutes; the other 190 incidents contribute 200 × 95 − 8,400 = 19,000 − 8,400 = 10,600 minutes, averaging 10,600 ÷ 190 ≈ 56 minutes — the team's true typical performance, coherent with the 45-minute median. Option B turns this decomposition into the right management conversation: the tail's cause is identified (parts dependency), so the improvement lever is stock and supplier lead time, not engineer pace — a review of working speed would investigate the 190 incidents that are already fine. Option A accepts a diagnosis the data contradicts. Option C is the integrity failure: excluding inconvenient data to flatter a metric corrupts the very reporting stakeholders rely on — the legitimate version is reporting mean and median with the tail explained, which is exactly B. Option D discards a useful statistic instead of contextualising it. Interpreting a data set and communicating it to others — your reporting skill verbatim — is at its most valuable precisely here, where the wrong reading of a summary statistic was about to misdirect a month of management attention.

### Preparation tips

- **Recompute the denominator first.** Whenever a percentage arrives with a recommendation attached — vendor pass rates, supplier SLAs, your own team's headline — identify what was divided by what before engaging with the conclusion. Most misleading figures are denominator choices, not arithmetic errors.
- **Keep the four models distinct.** Simple percentage, percentage change (original base), weighted combination (counts first), and compound change (multiply factors). Label which one a question needs before calculating; mislabelling is the root of most errors.
- **Decompose every suspicious average.** Mean far from median means a tail; a moving aggregate means a possible mix effect. Practise splitting your own team's figures until decomposition is reflex.
- **Project with stated assumptions.** Backlogs, capacity crossings and cost comparisons are models: write the assumptions (growth rate, failure rate, lead time) beside the result, and sanity-check by varying one. Ranges with assumptions beat points without.
- **Rehearse the stakeholder translation.** For each practice answer, draft the one-sentence version you would give a service desk manager or capacity manager. If the sentence needs the arithmetic's caveats, include them — that translation is the skill your reports are judged on.
- **Verify by a second route.** Complement checks, re-adding in reverse, recomputing from raw endpoints — every figure you can confirm two ways is one you can defend under questioning.

### Common pitfalls to avoid

- **Adding percentage changes.** +25% then −10% is +12.5%, not +15%. Compound by multiplying factors, or recompute from endpoints.
- **Averaging averages.** Percentages from different-sized groups combine by counts, never by simple averaging — the error always biases toward the smaller group.
- **Accepting favourable denominators.** Blocked test cases, excluded reopens, "executed-only" bases: the omitted category is usually where the risk lives. Ask what fell out of the denominator and why.
- **Letting one number speak for a distribution.** A mean without its median (or a percentile) invites exactly the misdiagnosis the efficiency-review question dramatised. Report pairs, not points.
- **Planning to the arithmetic deadline.** The month-6 decision that leaves zero slack is technically correct and operationally reckless. Compute the deadline exactly; recommend the buffer explicitly.
- **Forcing your arithmetic to match an offered figure.** In assessments and vendor meetings alike, when careful recomputation disagrees with a stated number, the discipline is to re-derive and stand by the method — not to bend your working toward the answer in front of you.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret and draw conclusions from written material — using documents a senior end user computing engineer genuinely works with: vendor advisories, change and release documentation, service policies, escalation correspondence, test specifications, stakeholder emails, and the reports your own team produces.

The typical format is an online, timed test of 15 to 25 minutes. You are shown a passage and asked structured questions. The dominant style is **true / false / cannot say** — deciding whether a statement is guaranteed by the passage, contradicted by it, or simply not addressed. Other styles include selecting the best summary, judging which draft communicates most effectively, and reasoning across two related documents. The governing rule never changes: answer from the text alone, however much your technical experience wants to fill the gaps.

At senior level, reading precision carries multiplied consequences. You are the person who interprets a vendor's carefully-hedged advisory and decides what your team does about it. You review change requests where a single mis-read clause becomes an estate-wide incident. You read between organisations — infrastructure's monitoring summaries, a partner's "no issues our side," a supplier's test report — where each author's wording choices carry meaning about confidence and accountability. And you write for stakeholders: producing reports in an appropriate format, discussing changes in reporting processes, and communicating interpreted data are named duties, and every one of them is reading's twin skill. Meanwhile the engineers you manage learn their reading standards largely from yours — the precision you demand in handovers and ticket notes is the precision you model.

The assessment rewards disciplined extraction — what does this text state, exclude, and leave open — plus, at this level, sensitivity to hedged language: "should," "may," "recommended," "we believe" and "no issues detected" all mean less than they seem, and noticing that is frequently the tested skill.

### How this assessment maps to your role

- **Comprehension of technical and policy documents** maps to your **Change management** skill: analysing and assessing the impact of change, and documenting change requests, requires exact reading of scope clauses, preconditions and exclusions — and writing them so others cannot misread.
- **True/false/cannot-say discipline** maps to your **Problem management** skill: initiating and monitoring investigations fairly means keeping the evidence's actual claims separate from your hypotheses — and from other teams' confident-sounding non-claims.
- **Reading hedged and qualified language** maps to your duty to **consult specialists effectively** and work with **infrastructure, capacity and availability managers**: vendor advisories and cross-team reports communicate as much through their qualifications as their assertions.
- **Summary and clarity judgement** maps to your **IT service reporting** skill: producing relevant reports in an appropriate format, and interpreting a data set and communicating it to others, is summarisation under an accuracy constraint — every dropped qualifier is a potential misdecision downstream.
- **Reading requirements precisely** maps to your **Testing** skill: reviewing requirements and specifications and defining test conditions begins with extracting exactly what a specification promises, at its boundaries.
- **User-facing clarity** maps to your **User focus** skill: turning quantitative and qualitative user evidence into outcomes requires writing that users and stakeholders actually understand — and the judgement to know when a draft fails that test.

### Practice questions

**Question 1 (easy) — Reading a vendor advisory**

An advisory reads: "Firmware v4.2 resolves the intermittent display flicker reported on Model K laptops. Devices on v4.0 or earlier should upgrade directly to v4.2. Devices on v4.1 must first roll back to v4.0 before applying v4.2, as direct upgrade from v4.1 can corrupt display settings. v4.2 has not been tested on Model J."

Statement: "A Model K laptop on v4.1 can be safely upgraded directly to v4.2."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The advisory addresses this exact path: devices on v4.1 "must first roll back to v4.0" because direct upgrade "can corrupt display settings." The statement claims the direct path is safe; the passage contradicts it — false, not cannot-say. Note the asymmetry a fast reader misses: the safe path depends on the starting version, so a single instruction ("upgrade to v4.2") sent to a mixed estate would corrupt exactly the v4.1 subset. This is why senior review of upgrade instructions checks the from-state, not just the to-state — and why the advisory's final sentence (v4.2 untested on Model J) is a separate landmine: untested is not "unsafe," but it is also not "safe," a distinction the cannot-say discipline exists to protect. Before any team-wide instruction goes out, the version-conditional structure of documents like this must survive the paraphrase.

**Question 2 (easy) — What a monitoring summary does and does not claim**

Infrastructure's summary reads: "Network monitoring for Building D detected no packet loss or latency threshold breaches between 09:00 and 17:00. Monitoring covers the wired network to the floor-switch level. Wireless access points in Building D are not currently within monitoring scope."

Statement: "The summary shows that Building D users experienced no network problems during working hours."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Separate what was measured from what is claimed. The summary asserts: no threshold breaches, on the wired network, to floor-switch level, 09:00–17:00. The statement generalises to "no network problems for users" — but users in Building D may connect wirelessly, and the passage explicitly places wireless outside monitoring scope; problems there would be invisible to this summary, not absent. Equally, nothing in the passage demonstrates that problems did occur — so the statement is neither guaranteed (true) nor contradicted (false): cannot say. This is the reading skill your cross-team investigations live on: "no issues detected" is a claim about the detector's coverage as much as about the network, and the scope sentence — often the last, least-read line — is where the coverage lives. When three teams each report "all clear," a senior engineer's first question is what each team's instruments can actually see.

**Question 3 (easy) — Following release documentation**

Release notes state: "This release must be deployed in sequence: database schema update first, then application server packages, then client updates. Client updates deployed before the schema update will fail silently, leaving clients on the old version while reporting success. The schema update requires a 30-minute service outage and must therefore occur outside business hours."

Statement: "If a client update reports success, the client is running the new version."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage constructs the exact counter-case: a client update deployed out of sequence "will fail silently, leaving clients on the old version while reporting success." A reported success is therefore compatible with a stale client — the statement's inference (success report → new version) is broken by the passage itself, making it false. The operational sting is real: silent failure modes invert the meaning of your deployment dashboard, so verification must use a signal independent of the installer's own report — an actual version check against inventory. For your testing skill, this is the pattern that "define test conditions" exists to catch: any specification containing the words "reports success" deserves a test that distinguishes reported success from actual success. And for change documentation, the sequencing constraint plus its failure mode is precisely what your team briefing must carry forward — a summary that drops the "silently" drops the whole danger.

**Question 4 (moderate) — Stacked conditions in a security policy**

Policy extract: "(1) Remote-access tokens are issued only to staff with a completed security induction. (2) Contractors may hold tokens only while their engagement letter is current, and must additionally be sponsored by a permanent staff member at grade 7 or above. (3) Token renewals follow the same rules as issuance. (4) During a declared security incident, all contractor tokens are suspended irrespective of sponsorship and engagement status."

A contractor with a completed security induction, a current engagement letter, and a grade 6 permanent sponsor requests token renewal. No security incident is declared. What does the policy require?

- A) Renew — induction and engagement letter are both in order.
- B) Refuse — renewal requires a sponsor at grade 7 or above, which a grade 6 sponsor does not satisfy.
- C) Renew, but flag for review at the next declared incident.
- D) Refuse — contractors may never hold tokens.

**Correct answer: B**

**Explanation:** Trace every applicable rule to its end. Rule 1: induction complete ✓. Rule 2 has two conjoined conditions for contractors: current engagement letter ✓, and a sponsor at grade 7 or above — the sponsor is grade 6 ✗. Rule 3 imports issuance rules into renewal, so the failed sponsorship condition applies now, at renewal, not just at first issue. Rule 4 is dormant (no incident declared) and irrelevant to the decision. The renewal must be refused until a qualifying sponsor is secured — answer B. Option A checks the two conditions that pass and stops counting — conjunctions ("and must additionally") fail on their weakest member, not their average. Option C invents a conditional-renewal category the policy does not contain; policies are not menus for improvisation. Option D over-reads rule 2's restrictions into a prohibition the rule explicitly does not make. The senior relevance is double: you apply such policies, and you write documents with this structure — change requests, procedures, standards — where a reader who stops mid-sentence inherits a security gap. Write conjunctions so they cannot be half-read; read them as if someone else wrote them carelessly.

**Question 5 (moderate) — Inference from escalation correspondence**

An email from the problem manager reads: "Thanks for the Monday-morning login failure evidence — the time clustering and the clean authentication logs were exactly what we needed. We've reproduced the failure in the test environment and traced it to a token cache that expires over weekends under a specific configuration. A fix is being tested; assuming it passes, release is targeted for the 14th. Until then, the Tuesday-to-Friday pattern should hold, but we can't rule out a similar failure after bank holiday weekends, for the same underlying reason."

Statement: "The problem manager expects that the failure could also occur on the morning after a bank holiday, before the fix is released."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Map the statement onto the passage's final sentence: "we can't rule out a similar failure after bank holiday weekends, for the same underlying reason." The mechanism explains why: the cache expires "over weekends," and a bank holiday extends the weekend — so the caveat is a reasoned expectation of possibility, which is exactly what the statement claims ("could also occur"). True. The subtlety worth noticing is the modal calibration on both sides: the statement says "could," not "will" — had it said "will occur after every bank holiday," the answer would be cannot-say, since the passage claims possibility, not certainty. Reading professionals' hedges at their intended strength — "can't rule out" = live possibility; "targeted for the 14th" = intention, not commitment; "assuming it passes" = an explicit dependency — is the difference between accurate downstream planning and manufactured promises. Your team briefing from this email should carry the bank-holiday warning and the conditional release date, at their stated strength: that is what faithful transmission means, and it is a senior engineer's daily act of translation.

**Question 6 (moderate) — Choosing the best stakeholder summary**

Your team's monthly data shows: incidents up 12% (driven by a directorate onboarding); SLA attainment steady at 91%; hardware repair backlog up from 15 to 24 due to a supplier recall consuming engineer time; the recall itself 80% complete and on track to finish next month. The service desk manager wants a four-line summary for the directorate heads. Which draft is best?

- A) "Another strong month: SLA steady at 91% despite 12% more incidents. Some hardware delays due to external factors beyond our control. Normal service continues."
- B) "Incidents rose 12%, absorbed without SLA impact (steady at 91%) — the rise tracks the Directorate F onboarding. Hardware repairs are slower than usual: the supplier recall is consuming engineer time, and the repair backlog has grown from 15 to 24. The recall is 80% complete; we expect it finished, and the backlog recovering, next month. No action needed from directorates, but hardware-dependent users should expect longer repair times until then."
- C) "Incident volumes have increased and the hardware backlog has grown, indicating rising pressure on the service. Escalation of resource concerns is recommended."
- D) "SLA 91%. Incidents +12%. Backlog 15→24. Recall 80%."

**Correct answer: B**

**Explanation:** Judge each draft against what directorate heads need: what changed, why, what happens next, and what (if anything) they should do. Option B delivers all four in four lines — each movement paired with its cause (onboarding; recall), a dated expectation (next month), and the one consequence readers should plan around (longer repair times). It reports the unflattering backlog number plainly, which is what keeps your reports trusted. Option A spins: "external factors beyond our control" hides the backlog figure and converts information into reassurance — readers discover the 24-repair queue when it touches them, and remember who smoothed it away. Option C reads the same data pessimistically, promoting an explained, ending pressure into a resourcing escalation — distortion in the opposite direction. Option D is data without interpretation: accurate, and useless to a reader who cannot tell whether 15→24 is a crisis or a footnote. This question is your reporting skill verbatim — produce relevant reports in an appropriate format; interpret and communicate — and its scoring rule generalises: the best summary is the one a reader could act on correctly without access to the underlying data.

**Question 7 (moderate) — Precise reading of an SLA definition**

Contract extract: "Priority 2 incidents: response within 1 working hour, resolution within 8 working hours. The resolution clock pauses while an incident awaits information requested from the customer, and while an agreed workaround is in place pending permanent fix. Incidents resolved by workaround are reported as 'resolved (workaround)' and count toward SLA resolution targets only when the workaround fully restores service functionality."

Statement: "An incident where an agreed workaround partially restores service counts toward the SLA resolution target."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The final clause sets the condition: workaround resolutions count "only when the workaround fully restores service functionality." A partial restoration fails the "fully" test, so it does not count toward the target — the statement is contradicted: false. Two words carry the whole meaning: "only when" (a necessary condition — no full restoration, no SLA credit) and "fully" (the threshold). Notice what the definition simultaneously does elsewhere: the clock pauses while an agreed workaround is in place, so a partial workaround stops the clock without earning the credit — a structure that could tempt a team to park incidents in workaround-pause indefinitely. Reading that incentive out of the definition is senior-level contract literacy: when you discuss reporting processes with stakeholders, definitions like this one are where reported performance and user experience quietly diverge, and the engineer who can point to the exact clause is the one who can fix the metric before it distorts behaviour.

**Question 8 (moderate) — Reconciling two documents**

Document 1 (your team's runbook, updated January): "USB storage devices are blocked on all estate laptops. Exceptions require a business case approved by the security team, reviewed annually."
Document 2 (security bulletin, dated last week): "Following the data-handling review, all existing USB storage exceptions are revoked with immediate effect. New exception requests are suspended pending publication of the revised removable-media policy, expected within eight weeks."

A user with a January-approved exception asks whether they can still use their USB drive, and when they can reapply. What is the accurate answer?

- A) Yes — their exception was approved and is valid until its annual review.
- B) No — their exception is revoked; and they cannot yet reapply, because new requests are suspended until the revised policy is published, expected within eight weeks.
- C) No — their exception is revoked, but they can reapply immediately under the runbook process.
- D) Yes — bulletins cannot override runbooks.

**Correct answer: B**

**Explanation:** Sequence and scope decide the reconciliation. The bulletin is later (last week versus January) and explicitly targets the runbook's exception regime: "all existing... exceptions are revoked with immediate effect" extinguishes the user's January approval regardless of its annual-review date — so the answer's first half is no. The second half is where option C fails: the bulletin also suspends new requests "pending publication of the revised policy," so the runbook's application route is closed until that publication, expected within eight weeks — the user cannot reapply yet, and B states both halves accurately, including the "expected" hedge on the timeline. Option A reads only the older document; option D inverts the precedence of a later, specific instruction over an earlier, general one. The housekeeping instinct this should trigger is also senior work: the runbook is now misleading and needs an urgent annotation, because every engineer who reads only Document 1 will give users answer A in good faith. Documents age at different rates; the reader who checks dates — and the maintainer who reconciles them — prevent the confidently wrong answer from propagating.

**Question 9 (challenging) — A specification's boundary conditions**

Specification extract: "The device-encryption compliance report runs nightly at 02:00 and lists all laptops whose last successful encryption check is older than 72 hours. Laptops offline for more than 14 consecutive days are moved to the 'dormant' register and excluded from the compliance report until they next connect. On connection, a dormant laptop is checked within 15 minutes and, if the check fails or cannot complete, appears on the next compliance report."

Statement: "A laptop that has been offline for 10 days will appear on tonight's compliance report."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Walk the two rules with the laptop's numbers. Dormancy requires more than 14 consecutive days offline; at 10 days, the laptop is not dormant, so the exclusion does not apply. The report's inclusion test is a last successful check older than 72 hours; a laptop offline for 10 days cannot have completed a successful check in the last 72 hours (checks require connection), so its last success is at least 10 days old — well past the threshold. Both conditions resolve determinately: included — true. The tempting wobble is cannot-say, reasoning "perhaps offline laptops are invisible to the report" — but that imports an assumption the passage explicitly handles otherwise: the specification's whole design is that non-dormant offline laptops do appear (that is what the 72-hour rule catches), while only 14-plus-day dormancy excludes. Reading specifications means letting their stated mechanics answer the question rather than your intuitions about how such systems usually work. This is also a compliance-literacy point with real audit consequences: the 10-day-offline laptop showing as non-compliant is the system working as specified — and the senior engineer who can explain that distinction saves their team from "fixing" correct behaviour.

**Question 10 (challenging) — Evaluating an argument in a proposal**

A proposal from a software developer team reads: "Since the desktop team's remote-support tool was deployed, average incident resolution time has fallen 18%. Deploying the same tool to the field-engineering team will therefore reduce their resolution times by a similar amount. Field engineering's incidents are largely connectivity-related and occur at sites without reliable network access."

Statement: "The proposal's own final sentence undermines its central argument."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Reconstruct the argument: the tool improved desktop resolution times; therefore it will similarly improve field engineering's. The inference assumes the two contexts are relevantly similar — and the final sentence supplies the dissimilarity that matters most: a remote-support tool requires network access to function, and field engineering's incidents "occur at sites without reliable network access" and are themselves "largely connectivity-related." The tool would be least available precisely when needed — its mechanism of benefit is disabled by the target environment. The proposal thus documents the defeater of its own generalisation: true. This question models a reading skill assessments increasingly test at senior level: evaluating arguments, not just extracting facts — locating the load-bearing assumption ("similar contexts") and checking whether the text itself strains it. It is also your daily cross-team reality: proposals, vendor pitches and business cases routinely generalise from favourable pilots, and the reviewing engineer's contribution is exactly this — not cynicism, but the question "does the mechanism that produced the benefit exist in the new context?" Often the fix is scoped adoption (sites with connectivity) rather than rejection; but only the reader who caught the tension can propose it.

**Question 11 (challenging) — Judging a difficult communication**

A change your team implemented last night failed partially: 30 of 200 laptops did not receive a security patch and are temporarily blocked from the network by policy, stranding their users this morning. The cause was an expired deployment certificate your team should have renewed. You must email the affected users' managers. Which draft is best?

- A) "Due to a certificate anomaly in the deployment infrastructure, a subset of devices was unable to complete the scheduled update and has been isolated per security policy. Remediation is in progress."
- B) "Last night's security patch failed on 30 laptops because a deployment certificate expired — a renewal our team should have made and missed. Security policy has automatically blocked those laptops this morning; the affected users are listed below. We expect all 30 restored by 12:00. Affected users can work immediately via the loan pool or browser-based email — reply and we'll arrange either within the hour. We're adding certificate expiry to our monitored checks so this cannot recur silently. I'll confirm completion by 12:30."
- C) "A small number of devices missed last night's patch and were blocked by policy. This is a routine occurrence in large estates and no cause for concern. Normal service will resume shortly."
- D) "30 laptops are blocked following a failed patch. The security policy that blocks unpatched devices is set centrally, not by this team. Users should contact the service desk for workarounds."

**Correct answer: B**

**Explanation:** The situation contains four communication duties: honest cause, concrete scope and timeline, immediate mitigation, and prevention — and option B is the only draft carrying all four. Its accountability is exact ("a renewal our team should have made and missed") without self-flagellation; its scope is usable (a list of affected users — managers' first question); its mitigation is actionable within the hour; its prevention line ("monitored checks so this cannot recur silently") converts the failure into evidence of a team that learns; and it closes the loop with a confirmation time. Option A is the anonymous passive voice at its worst — "a certificate anomaly" describes your team's missed renewal as if weather had occurred; readers eventually learn the truth, and then re-read the evasion. Option C minimises ("routine," "no cause for concern") to an audience of managers whose staff are visibly unable to work — reassurance that contradicts the reader's own experience destroys credibility instantly. Option D is technically accurate blame-deflection: true sentences arranged to point away from the missed renewal, ending with the burden pushed onto users. The scoring key's deep pattern, which your ownership skill states as owning an issue until resolved: when your team caused it, the strongest possible message names the cause, bounds the damage, mitigates now, and shows the fix that outlives the incident.

### Preparation tips

- **Read scope sentences first, or at least always.** Monitoring summaries, advisories and reports quietly define what they can see — coverage clauses, model exclusions, "to the floor-switch level." The last line of the passage is disproportionately often the line the question turns on.
- **Calibrate hedges at their stated strength.** Build a personal glossary: "targeted" (intention), "should" (expectation), "can't rule out" (possibility), "only when" (necessary condition), "must additionally" (conjunction). Transmitting hedges faithfully — up to stakeholders and down to your team — is the skill under test.
- **Check document dates before reconciling.** When two texts conflict, sequence and specificity usually decide precedence. Practise on your own runbooks against recent bulletins — and fix the stale ones you find.
- **Test inferences against stated mechanisms.** "Reports success" versus "is updated"; "no breaches detected" versus "no problems"; "improved there" versus "will improve here." The gap between a text's claim and the offered conclusion is where most questions live.
- **Draft the summary, then audit it.** Take a real month of team data and write the four-line stakeholder version; then check: is every movement paired with its cause? Is the unflattering number present? Could the reader act correctly without the source data? That audit is the assessment's clarity questions, self-administered.
- **Read one argument critically each week.** Proposals, vendor claims, business cases: find the generalising assumption and ask whether the mechanism of benefit survives the new context. Ten minutes weekly builds the evaluation reflex the hardest questions require.

### Common pitfalls to avoid

- **Treating "no issues detected" as "no issues."** Every detection claim inherits its instrument's coverage. The confident cross-team all-clear is the most expensive misreading in service operations.
- **Half-reading conjunctions and exceptions.** "And must additionally," "only when," "except" — conditions fail on their weakest member, and exceptions frequently invert the sentence they end. Read rules to the full stop.
- **Importing your operational intuition.** You know how deployments usually behave; the passage defines how this one behaves. When text and instinct conflict, the text is the exam — and, with vendor advisories, usually the safer guide at work too.
- **Letting older documents answer newer questions.** January's runbook cannot survive last week's bulletin. Date-check before you answer, in tests and at the desk.
- **Choosing summaries that spin or panic.** Wrong drafts hide the unflattering figure, or promote explained pressure into crisis. The scoring key rewards cause-paired, actionable, unspun accuracy — in both directions.
- **Mistaking modality.** "Could occur" is not "will occur"; "expected within eight weeks" is not a commitment. Statements that harden a hedge (or soften a rule) are the true/false/cannot-say questions' favourite trap.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of possible responses — choosing the **most effective**, the **least effective**, or rating each option on a scale. The material is the human side of your role: team members under pressure, escalations that stall, stakeholders with conflicting demands, specialists who disagree, and the recurring collision between speed, process and people.

The typical format is 10 to 20 scenarios, untimed or generously timed. Scoring compares your choices with the pooled judgement of experienced professionals and the organisation's values. For UK government digital roles, the scored behaviours are recognisable: user focus, ownership, honesty, collaboration, proportionate escalation, inclusion — and at senior level, two more come into focus: developing the people you manage, and protecting the service's interests across team boundaries.

Why do employers weight SJTs heavily for senior engineers? Because your role summary is largely made of judgement calls. Managing, co-ordinating and prioritising the team's tasks means deciding between competing goods, not right and wrong. Identifying and escalating repeat issues means judging when evidence is strong enough, and which of several routes — lead engineer, incident manager, problem manager, software developers — fits the issue. Working closely with infrastructure, capacity and availability managers means influence without authority. Owning issues until they are resolved or properly handed over means calibrated persistence. And the line-management thread running through it all — workload, development, mistakes, morale — is judgement from start to finish. Technical skill determines whether you can fix things; judgement determines what your team fixes, in what order, at what cost. SJTs sample the second.

A calibration note for your level: scoring keys expect you to resolve within your span what belongs in your span (people, priorities, team process), to escalate with evidence what exceeds it (systemic causes, cross-team blockers, resourcing), and to develop rather than absorb — the senior who does everything personally scores as poorly as the one who delegates everything upward.

### How this assessment maps to your role

- **Team co-ordination judgement** maps to your duty to **manage, co-ordinate and prioritise tasks**: scenarios test allocation under scarcity, protection of commitments, and the discipline of matching resource to need rather than to noise.
- **Escalation calibration** maps to your duty to **identify and escalate repeat issues** to the lead engineer, incident or problem managers, and software developers: the tested judgement is when, to whom, and with what evidence — under-escalation buries systemic faults; over-escalation devalues the channel.
- **Cross-team influence** maps to your duty to **work closely with infrastructure, capacity and availability managers** and to **effectively consult specialists**: scenarios probe persistence, evidence-led disagreement, and maintaining relationships across boundaries you do not control.
- **Developing engineers** maps to your team-management responsibility and your **Ownership** skill: coaching versus absorbing, addressing performance early and privately, and building the team's capability rather than its dependence on you.
- **Preventative instinct** maps to your **Problem management** skill — determining preventative measures — and your **Service focus**: strong options fix the instance and the system that produced it.
- **Honest stakeholder communication** maps to your **IT service reporting** skill and **User focus**: scenarios reward accurate, unspun, actionable communication, especially when the news is bad and the cause is yours.

### Practice questions

**Question 1 (easy) — The engineer who hides a struggle**

Reviewing the queue, you notice one of your engineers has quietly held a P3 ticket for six days — the team norm is two — re-dating the expected-resolution field twice without notes. The engineer is capable, well liked, and has never needed chasing before.

Which response is most effective?

- A) Reassign the ticket to a faster engineer and say nothing — the queue matters most.
- B) Raise the six-day ticket at the team stand-up so everyone learns the standard.
- C) Speak privately: ask what is happening with the ticket, listen first — the uncharacteristic pattern suggests a blocker, a knowledge gap, or something personal — then agree a path for the ticket and whatever support the actual cause needs.
- D) Send a written reminder of the two-day norm with the ticket reference attached.

**Correct answer: C**

**Explanation:** Read the signal before choosing the instrument. A reliable engineer breaking pattern — silently, with re-dated fields — is more likely struggling than slacking: a technical dead-end they are embarrassed to admit, an unfamiliar system, or pressure outside work. Option C investigates before acting, privately, and with listening ahead of judgement; whatever the cause, the conversation resolves the ticket (help, reassignment, or escalation) and addresses the source, while teaching something more valuable than the two-day norm: that surfacing a struggle early is safe. Option A fixes the ticket and abandons the engineer — the same silent struggle recurs on the next hard ticket, still hidden. Option B converts a private difficulty into public example-making; the lesson everyone actually learns is to hide struggles better. Option D applies a rule to a person without asking which one needs the attention; process reminders answer questions nobody asked. The senior pattern: uncharacteristic behaviour is data — investigate privately, support first, and keep the standard by making it safe to fall short of it out loud.

**Question 2 (easy) — Credit flows upward**

At a service review with your service desk manager and other team leads, the manager praises last month's sharp drop in repeat incidents — an improvement produced by a preventative fix that one of your engineers designed and drove almost entirely alone. The manager congratulates you personally.

Which response is most effective, and which is least effective?

- A) Accept the praise gracefully — as their manager, the team's results are yours to represent.
- B) In the meeting, redirect the credit specifically: name the engineer, state what they designed, and note you will pass on the recognition — then do so, and mention it in their next development conversation.
- C) Say nothing in the meeting, but privately thank the engineer afterwards.
- D) Explain modestly that the improvement was mostly luck and the trend may not hold.

**Correct answer: most effective B; least effective D**

**Explanation:** Attribution moments are development infrastructure. Option B costs one sentence and buys three outcomes: the engineer's work becomes visible to the seniority that decides progression (visibility they cannot create for themselves from inside the queue); your team learns that good work travels upward with names attached — a stronger motivator than any away-day; and your own credibility rises, because managers who name their people read as leaders while managers who absorb credit read as ceilings. Option A is the quiet ceiling: technically defensible, and it teaches your best people that their work becomes yours at the meeting-room door. Option C preserves private fairness while wasting the public moment — the thank-you matters, but the room where progression is discussed has already moved on. Option D is least effective and deserves its own autopsy: false modesty erases the engineer's work entirely — worse than absorbing credit, it converts a designed, driven improvement into noise, undermining the case for future preventative investment and the engineer in one move. Truthfulness about causes is a reporting virtue everywhere else; it applies to successes too.

**Question 3 (easy) — The specialist who talks past you**

Investigating recurring virtual-desktop slowness, you consult an infrastructure specialist. Their reply is a wall of subsystem jargon concluding "everything's green our side," which does not address the time-clustered evidence you sent. You suspect they skimmed it. The slowness continues, users are complaining daily, and the specialist is known to be prickly with non-infrastructure people.

Which response is most effective?

- A) Accept the all-clear and tell users the fault cannot be found.
- B) Re-engage concretely: restate the two discriminating facts in one short message — the 11:45–13:15 daily window and the three-week-old onset — ask directly what their monitoring covers during that specific window, and propose a fifteen-minute joint look at the data; if it stalls again, escalate the impasse with the evidence trail to the lead engineer.
- C) Escalate immediately to the specialist's manager, attaching the dismissive reply.
- D) Work around them: ask a friendlier infrastructure contact to run checks informally.

**Correct answer: B**

**Explanation:** Effectively consulting specialists — your role summary's phrase — includes the harder half: re-consulting when the first pass fails. Option B applies the craft: compress the evidence to its two discriminating facts (walls of context invite skimming; two sharp facts are hard to wave away), convert the vague all-clear into a specific coverage question ("what does your monitoring see 11:45–13:15?" — which, as the verbal section showed, is where all-clears hide their gaps), and lower the cost of engagement to fifteen shared minutes. Most cross-team impasses dissolve under this treatment because the first reply was skimming, not stonewalling. The escalation clause matters too: prepared, evidenced, and second, not first. Option A abandons users to a fault nobody has actually ruled out. Option C escalates before attempting a competent second pass — spending relationship capital the investigation will need later, and inviting "did you ask about the window?" from the manager. Option D gets checks run while corroding the official channel: the prickly specialist eventually discovers the bypass, and every future consultation starts colder. The pattern: sharpen the evidence, shrink the ask, question the coverage — then escalate the impasse, not the person.

**Question 4 (moderate) — The rota favour with a pattern**

An engineer asks to swap out of next week's Monday walk-up desk shift — the third consecutive Monday request, each with a plausible individual reason. Covering the swaps has quietly fallen to the same two colleagues, one of whom mentions it to you with studied casualness. Monday is the desk's heaviest day.

Which response is most effective?

- A) Approve this swap — each request has had a valid reason — and keep monitoring.
- B) Refuse this and future Monday swaps — fairness requires everyone taking equal Mondays.
- C) Approve or hold this swap on its stated merits, but address the pattern directly: a private conversation with the engineer about the three-Monday run and what is behind it, and a look at whether the swap-covering burden has become unfair to the two colleagues absorbing it.
- D) Redesign the whole rota so Mondays rotate automatically and swaps need your written approval.

**Correct answer: C**

**Explanation:** Two things are true simultaneously: each individual request was plausible, and the pattern is now data — three consecutive Mondays, the heaviest day, with the cost quietly concentrating on two colleagues whose "studied casualness" is how tolerant people first signal unfairness. Option C treats both truths at their own level. The current swap gets judged on its merits (the engineer may have a genuine recurring Monday constraint — caring responsibilities, a course — which, surfaced, might justify a deliberate rota adjustment everyone can see, rather than serial informal swaps nobody agreed to). The pattern gets its own conversation: not an accusation, an inquiry — "three Mondays running; what's going on?" — plus explicit attention to the colleagues carrying the cover. Option A extends a drift that is already taxing two people and lets "monitoring" substitute for managing. Option B swings to rule-enforcement without asking the question whose answer might change everything; fairness includes hearing reasons. Option D reaches for structural machinery to avoid one direct conversation — process as conflict-avoidance, and the paperwork burden lands on everyone. The senior habit: patterns in small requests are managed in conversation before they are managed in systems — and the quiet absorbers of unfairness are watching what you do.

**Question 5 (moderate) — Pressure to bless a risky change**

The service desk manager wants a driver update pushed to all 300 estate laptops this week, citing vendor security guidance. Your impact assessment is incomplete: the pilot covered only two of the estate's four hardware variants, and one untested variant had serious problems with the previous driver generation. The manager says: "Security trumps process — push it estate-wide, I'll own the risk."

Which response is most effective?

- A) Push estate-wide as instructed — the manager has explicitly accepted the risk.
- B) Refuse until the full pilot completes in three weeks — process is process.
- C) Propose the risk-managed middle: push now to the two tested variants (about 70% of the estate, capturing most of the security benefit immediately), fast-track a 48-hour pilot on the remaining variants — prioritising the one with the bad driver history — and stage their rollout on its results; put this plan and its rationale to the manager in writing.
- D) Push estate-wide but keep rollback packages ready.

**Correct answer: C**

**Explanation:** The manager's framing — security versus process — is false, and the strongest response dissolves it rather than picking a side. Option C delivers most of the security benefit at the speed the manager wants (70% of the estate this week) while confining the untested risk to a 48-hour, prioritised pilot; if the historically-troublesome variant misbehaves, the damage is a pilot group, not 90 laptops mid-fault estate-wide. Writing the plan down is not defensive paperwork — it is how a change decision with a risk trade-off should exist, visible to the change process and fair to everyone including the manager. Option A misreads what "I'll own the risk" can do: accountability for a bad outcome is not transferable by sentence, and — more practically — the users on the untested variant own the actual downtime regardless of who owns the risk on paper. Your change management skill (analyse and assess impact) exists precisely for the moment someone senior waves it aside. Option B hands the manager a three-week security exposure to defend a process whose purpose — risk control — option C achieves faster. Option D does the reckless thing carefully: rollback readiness mitigates but does not justify skipping the assessment, and a fleet-wide driver failure with rollback is still a fleet-wide incident. The scored pattern: when speed and safety are framed as enemies, design the sequence that delivers both, and put it in writing.

**Question 6 (moderate) — The repeat issue nobody owns**

For a month, your team has logged intermittent failures in the expenses application — a dozen tickets, real user impact, clear evidence. You escalated to the application's software development team twice; both times the tickets were closed as "cannot reproduce." Your engineers have started telling users "known issue, nothing we can do," and the users have started believing them.

Which response is most effective?

- A) Accept the developers' finding — if they cannot reproduce it, it cannot be progressed.
- B) Rebuild the escalation as evidence they cannot close: aggregate the twelve tickets into one problem record with the reproduction-relevant pattern (timing, user actions, error text, affected versions), ask your engineers to capture diagnostics at the next occurrences, then take the package through the problem manager — the route designed for exactly this — rather than as a third ticket-to-ticket escalation; and reset your team's user script from "nothing we can do" to "actively under investigation, here's the workaround."
- C) Tell users to raise complaints so the application team feels the pressure.
- D) Instruct your team to stop logging tickets for it, since they only get closed.

**Correct answer: B**

**Explanation:** "Cannot reproduce" is a statement about the evidence that reached the developers, and twice through the ticket channel, the evidence arrived shaped as isolated incidents — easy to test briefly and close honestly. Option B changes what arrives: a problem record aggregating twelve occurrences with the pattern data that makes reproduction possible (timing, actions, error text, versions — the discriminating facts), enriched by diagnostics your engineers capture at the next failures, routed through the problem manager, whose process exists to hold open exactly the recurring, hard-to-reproduce faults that ticket-by-ticket handling closes. This is your role summary executing itself: initiate and monitor actions to investigate patterns; escalate repeat issues to the problem manager and software developers. The user-script reset matters equally: "nothing we can do" is corrosive learned helplessness — false (you are doing something) and trust-destroying. Option A treats a channel failure as a technical verdict. Option C weaponises users to do your escalation for you — it may generate pressure, but it spends user trust and poisons the developer relationship the fix will need. Option D stops collecting the evidence the case depends on, guaranteeing permanent unfixability while the impact continues. The pattern: when escalation fails twice, upgrade the evidence and change the route — do not repeat the failed method louder, and never let your team narrate defeat to users.

**Question 7 (moderate) — Two managers, one engineer, Friday afternoon**

At 15:30 Friday, the capacity manager asks you to keep an engineer late for urgent storage remediation ("tonight or we breach thresholds over the weekend"), while the availability manager separately insists the same engineer — your only specialist in the relevant system — completes failover testing tonight ahead of Monday's DR audit. The engineer, who has flagged childcare constraints on late notice before, has not yet been asked. Both managers say their task cannot slip.

Which response is most effective?

- A) Give the engineer both tasks and let them prioritise — they know the systems best.
- B) Take the conflict off the engineer entirely: get the two managers to rank the tasks against each other (asking each what "cannot slip" concretely means and what a 24-hour slip actually costs); in parallel, establish real options — can either task be done by you or another engineer with the specialist advising, can either genuinely wait — and only then discuss late working with the engineer, as a request with their constraints respected, not a fait accompli.
- C) Side with the availability manager — audits outrank thresholds.
- D) Tell both managers that late working is impossible due to the engineer's circumstances and the tasks must wait until Monday.

**Correct answer: B**

**Explanation:** Three failures hide in the easy answers. Option A exports a management conflict to the person least able to resolve it — the engineer cannot rank two managers' "cannot slip" claims and ends up owning whichever breach occurs, plus a ruined evening they were never actually asked about. Option C adjudicates on category ("audits outrank thresholds") without interrogating either claim — yet "cannot slip" statements, pressed for specifics, frequently soften into "would be awkward"; the manager whose claim survives concrete questioning is the one with the real constraint. Option D protects the engineer by unilaterally sacrificing both tasks — advocacy without problem-solving, and it makes the engineer the named reason for two teams' Friday failures. Option B does the senior job in the right order: force the prioritisation conversation between the demand owners (where it belongs), widen the option space (the specialist advising while another pair of hands executes converts "only X can do it" into "X can enable it" — often true and rarely volunteered), and approach the engineer last, with a genuine request that honours previously-flagged constraints. Note the deep structure, which recurs throughout senior work: when two authorities both claim priority over your resource, your job is to make them rank against each other — not to guess, and never to make your engineer guess.

**Question 8 (moderate) — The report that would embarrass a colleague**

Preparing your monthly report, you find that a spike in failed changes traces to one engineer's three consecutive failed implementations — all from skipping the pre-implementation checklist. Your report goes to the service desk manager and is discussed in a forum where teams' figures are compared. You have not yet spoken to the engineer about the failures.

Which response is most effective?

- A) Report the spike with the engineer named — transparency requires full attribution.
- B) Omit the three failures from the figures to protect the engineer, and handle it privately.
- C) Report the spike accurately with its process cause ("three failed changes traced to pre-implementation checks being skipped; corrective actions under way") without naming the engineer — and hold the direct, developmental conversation with the engineer before the report lands, so the corrective actions are real and they hear it from you first.
- D) Delay the report a month to see whether the trend self-corrects.

**Correct answer: C**

**Explanation:** Two duties collide — honest reporting and fair management — and option C discovers they do not actually conflict. The report stays true: the spike appears, its cause is stated at the level stakeholders need (a process failure: checks skipped), and corrective action is claimed because, by sequencing the conversation first, it exists. The engineer is managed properly: performance conversations happen in private, before the numbers circulate, so they are never ambushed by a forum discussion of their own failures — and the conversation itself follows Question 1's pattern: uncharacteristic or not, ask why the checklist got skipped (time pressure? checklist rot? overconfidence?) before prescribing. Names are withheld from the report not as concealment but as level-matching: the forum needs the cause and the fix; individual attribution adds shame, not information, and teaches every engineer that honest figures are personally dangerous. Option A converts reporting into public discipline — accuracy weaponised. Option B corrupts the data: this month's omission becomes next month's unexplained baseline shift, and your reports stop being trustworthy the day the omission surfaces. Option D trades a month of stakeholder blindness for the hope of avoiding one conversation — and failed changes are exactly what stakeholders most need to see promptly. The pattern: report causes publicly, manage people privately, and sequence so both are true when the report lands.

**Question 9 (challenging) — Your improvement made things worse**

Three weeks ago you redesigned the team's ticket-triage process to speed up allocation — your initiative, announced with some fanfare. The data now shows allocation is faster, but misrouted tickets have doubled, and two engineers privately say the new categories are confusing. The old process could be restored in a day. Your monthly review with the service desk manager, where you presented the redesign, is tomorrow.

Which response is most effective, and which is least effective?

- A) Present the allocation-speed improvement tomorrow and hold back the misrouting data while you quietly fix the categories.
- B) Restore the old process today and describe the episode tomorrow as a trial that ran its course.
- C) Bring the full picture tomorrow: the speed gain, the doubled misrouting, the engineers' feedback — and a decision made with the team today on the evidence, whether that is fixing the confusing categories quickly or reverting while a better design is worked up; presented plainly as "the redesign achieved X, cost Y, and here is what we're doing about it."
- D) Keep the new process unchanged for another month to give it a fair chance before judging.

**Correct answer: most effective C; least effective A**

**Explanation:** The scenario tests whether your evidence standards survive your own authorship. Option C applies to your initiative exactly the discipline you would apply to anyone else's: both metrics on the table (speed improved, accuracy halved — and misrouting is the costlier failure, since a misrouted ticket loses more time than fast allocation saves), the practitioners' feedback taken as data, and a decision — fix-forward or revert — made on evidence with the people who work the process, then reported without spin. Whichever technical choice the evidence supports, the presentation pattern "achieved X, cost Y, doing Z" converts a mixed result into demonstrated judgement; managers trust more, not less, after a leader reports their own initiative's costs unprompted. Option A is least effective and compounding: selective presentation of your own project's data is precisely the reporting corruption Question 8 warned about, now with a personal motive — and misrouting data circulates in ticket systems where the manager can find it, after which every future report from you gets re-checked. Option B reverts sensibly but launders the story ("a trial that ran its course" — it was announced as an improvement, and it doubled misrouting); the half-truth costs more than the failure. Option D extends a known cost for another month to protect the possibility of being right — sunk-cost persistence dressed as fairness. The senior pattern, and the one your team is watching for: your initiatives get the same evidence standards, the same honest reporting, and the same willingness to revert as anyone else's.

**Question 10 (challenging) — Inclusion versus the delivery deadline**

Your team is two days from completing a directorate-wide laptop migration with a published deadline. An engineer flags that one team of six caseworkers includes two users of specialist assistive technology whose configurations the standard migration process will wipe; rebuilding them properly needs the assistive-technology specialist, who is unavailable until three days after the deadline. Pushing those two users through the standard process would hit the deadline but leave them without their tools for at least three days. The directorate head "expects 100% completion by Friday."

Which response is most effective?

- A) Migrate everyone by Friday — 100% was promised, and the two users can be supported with workarounds for three days.
- B) Defer the whole six-person team until the specialist is available, keeping teams together.
- C) Migrate the four standard users on schedule; explicitly defer the two assistive-technology users until the specialist can rebuild their configurations — treating their working setup as a completion requirement, not an optional extra; tell the directorate head today: 98% Friday, the final two properly done three days later, with the reason stated plainly.
- D) Ask the two users to choose between migrating on time with temporary workarounds or waiting for the specialist.

**Correct answer: C**

**Explanation:** Reframe what "completion" means and the answer clarifies: a migration that leaves two disabled users unable to work is not complete for them — it has converted their equipment into an obstacle. Option A treats their access as a rounding error on a percentage; "workarounds for three days" for assistive-technology users typically means dependence on colleagues or effective exclusion from work, a cost no deadline symbolism justifies — and one the two users have seen before, which is why how this decision lands matters beyond this migration. Option C delivers everything the deadline actually protects (96 of 98 users... precisely: four of the six, plus the rest of the directorate, on time), defers exactly the two migrations that would cause harm, and — the senior half — communicates the exception today, proactively, with its reason: directorate heads absorb "98% Friday, final two done properly Tuesday because their assistive technology needs specialist rebuild" far better than they absorb discovering excluded staff the following week. Expectations are managed by information delivered early, not by silent 100%s with hidden casualties. Option B over-corrects: four standard users' migrations carry no risk, and deferring them serves symmetry, not need. Option D outsources an accessibility judgement to the affected users as a forced choice between bad options — choice architecture masquerading as respect; the organisation's duty is to provide the option where they lose nothing. The scored behaviours: inclusion as a completion criterion, proportionate exception-making, and proactive stakeholder honesty.

**Question 11 (challenging) — The quiet capability gap**

A key monitoring system your team depends on is understood deeply by exactly one engineer, who built most of your team's tooling around it. They are excellent, overloaded, visibly proud of being indispensable — and have just been shortlisted for a promotion elsewhere in the organisation. Documentation is thin; two other engineers have separately mentioned they "wouldn't know where to start" if the specialist were away.

Which response is most effective?

- A) Hope the promotion falls through; the team works well as it is.
- B) Instruct the specialist to write full documentation before any move is confirmed.
- C) Start deliberate knowledge transfer now, framed as investment in the specialist rather than insurance against them: pair the two interested engineers with the specialist on real tickets, make documentation a byproduct of the pairing (they write it, the specialist corrects it), recognise the specialist's teaching visibly — and say plainly that setting the team up to survive their promotion is part of making the promotion possible.
- D) Quietly commission an external contractor to reverse-engineer the tooling as a contingency.

**Correct answer: C**

**Explanation:** The single-point-of-knowledge is a problem-management pattern applied to people: a predictable failure mode, identified before it fires — and your role's preventative-measures duty applies to team capability as much as to hardware. Option C is the only response that treats every party's interests as aligned, because they genuinely are: the specialist's promotion prospects improve when their systems survive their departure ("irreplaceable" reads as "cannot be released" to promotion panels — saying this plainly converts knowledge transfer from threat to gift); the two interested engineers get the development they have implicitly asked for; and the mechanics are chosen to work — pairing on real tickets transfers judgment, not just facts, and documentation written by the learners and corrected by the expert is both cheaper for the specialist and better calibrated to what a non-expert actually needs. The pride dynamic is handled by visible recognition of teaching, redirecting the identity from "only I know this" to "I built the team that knows this." Option A is a plan with a single point of failure about a single point of failure. Option B extracts documentation as a toll on someone's career move — resented, rushed, and written by the one person who cannot see what beginners don't know. Option D spends money to avoid a developmental conversation, produces outsider documentation of insider tooling, and — when discovered — tells the specialist you planned around them behind their back. The senior pattern: capability risks are managed like any other risk — early, openly, and in a way that leaves the people involved better off than the risk found them.

### Preparation tips

- **Run options through the three-lens check, plus one.** User outcome, process integrity, relationship health — and at your level, add: what does this choice teach my team? Options identical on the first three often separate on the fourth.
- **Rank the claims before adjudicating.** When multiple parties insist their need "cannot slip," the strong answers make claimants rank against each other with concrete costs, rather than guessing or deferring to rank. Practise asking "what does a 24-hour slip actually cost?" — it resolves most manufactured urgency.
- **Sequence conversations before documents.** Report causes publicly, manage people privately, and order events so both are honest: the development conversation precedes the report; the stakeholder hears the exception before the deadline, not after.
- **Apply your standards to your own work first.** The hardest scored behaviour at senior level is subjecting your own initiatives to the evidence, reversal and reporting discipline you expect of others. Rehearse the sentence "it achieved X, cost Y, here's what I'm doing" until it is available under pressure.
- **Treat patterns as the unit of action.** Single events get handled; repeating ones — swap requests, closed escalations, one-person knowledge — get investigated and re-designed. Before answering, ask whether the scenario is showing you an instance or a pattern.
- **Debrief real dilemmas with peers.** Other team leads' reasoning about escalation, credit, and difficult managers is the norm group SJTs score against. A monthly coffee spent on "what would you have done?" is targeted preparation.

### Common pitfalls to avoid

- **Absorbing instead of developing.** Taking the hard tickets yourself, covering gaps silently, staying indispensable — heroic absorption reads as dedication and scores as a team kept dependent. The senior answer builds capability that outlasts the incident.
- **Escalating people-problems past yourself.** Performance, fairness and pattern conversations inside your team are yours; sending them upward unaddressed exports your role. Conversely, keeping systemic cross-team faults to yourself buries them — know which side of the line a problem sits on.
- **Accepting transferred risk on someone's say-so.** "I'll own the risk" transfers nothing operationally: users still bear the outage, and you still bear the professional duty of assessment. Strong options redesign the plan; weak ones accept the sentence.
- **Letting reports and truth diverge.** Omitting your team's bad figures, your own project's costs, or an engineer's failure-spike corrupts the instrument stakeholders steer by. Every spin option in an SJT is a planted trap — including the flattering ones.
- **Adjudicating by category or rank.** "Audits beat thresholds," "directors outrank caseworkers," "face-to-face beats chat" — categorical rules feel decisive and skip the actual claims. Interrogate concreteness: the real constraint survives specific questioning.
- **Managing patterns with machinery.** Reaching for rota redesigns, written policies and approval workflows to avoid one direct conversation is process as conflict-avoidance. The conversation usually resolves it; the machinery usually taxes everyone else.

## Conclusion

Well done — you have worked through a substantial set of practice materials covering all four assessment types you are likely to meet as a senior end user computing engineer: cognitive ability, numeric reasoning, verbal reasoning, and situational judgement.

Along the way, you have practised far more than test technique. You have distinguished step changes from noise and mix effects from improvements, audited rotas, change requests and test claims one rule at a time, computed weighted SLAs, backlog projections, capacity deadlines and total costs of ownership with the bases stated, read vendor advisories, monitoring summaries and conflicting policies at their exact strength, and weighed the judgement calls that define your level — allocating scarce engineers, calibrating escalations, confronting your own initiative's costs, protecting assistive-technology users against a deadline, and dissolving a single point of knowledge without damaging the person who holds it. Every exercise maps directly to the skills your role names: incident management, problem management, change management, asset and configuration management, IT service reporting, technical specialism, testing, service focus, ownership, user focus, and the service management framework knowledge underneath them all.

A few encouragements as you move forward. First, assessment performance is a skill that responds to practice: if particular question types caught you out, revisit their explanations in a week and try similar items — the recurring methods are few and learnable. Notice how often the same disciplines returned: match the footprint of cause to symptom; recompute the denominator; read the rule to its end; rank claims by concrete cost; report causes publicly and manage people privately. Second, treat these pages as management material as much as test preparation — the worked explanations are rehearsals for the coaching conversations, escalation summaries and stakeholder translations your week is already made of, and every technique you internalise is one you can now teach. Third, be confident in what you already bring: you prioritise a team's work under pressure, hold your own with specialists and managers across boundaries, and turn incident data into investigations every working day. These assessments sample, in miniature, judgement you already exercise at full scale.

If you are preparing for a real assessment, find out the format, timing and provider in advance, complete any official practice tests offered, and look after the basics — rest, a quiet environment, rough paper, a steady pace. And whatever the outcome, keep investing in your development: seek feedback from the lead engineers and managers you work with, keep sharpening the evidence behind your escalations, and keep building engineers who can one day do your job — which is, quietly, the strongest evidence of having done it well.

Good luck — you are better prepared than you were when you started reading. Keep going.
