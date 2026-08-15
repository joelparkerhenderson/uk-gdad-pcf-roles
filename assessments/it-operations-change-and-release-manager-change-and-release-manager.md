# Change and Release Manager - Psychometric Assessment Resources

## Introduction

Welcome. This guide has been prepared specifically for you as a change and release manager working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, pursuing your next post, benchmarking your own capability, or simply curious about how psychometric assessment maps onto the realities of your role, this document is designed to help you practise deliberately and arrive confident.

Psychometric assessments are structured, standardised exercises that measure the cognitive capabilities and professional behaviours known to predict success in a role. For a change and release manager, that means considerably more than abstract reasoning puzzles. The assessments described here are job-specific: they draw on the artefacts you genuinely own — forward schedules of change, Change Advisory Board (CAB) papers, risk assessments, release calendars, configuration management data, availability and capacity KPIs, and post-implementation reviews — and the decisions you genuinely make: whether a contested change proceeds, how interdependent releases are sequenced, when an escalation demands your personal ownership, and how a change process itself should be improved.

Why does this matter for your role in particular? You sit at the point where delivery pressure meets operational risk. You chair the CAB, ensuring every technical change is adequately assessed for impact, prioritised, scheduled, authorised, and implemented in line with process. You are the escalation point when things go wrong, the decision-maker for all technical changes, and the coordinator of releases and their interdependencies. Each of the four assessment types in this guide measures a capability that work depends on directly: cognitive ability (spotting the conflict buried in a forward schedule, reasoning through dependency chains), numerical reasoning (reading KPI tables accurately, converting availability targets into real minutes, building the quantified case for process improvement), verbal reasoning (extracting precisely what a policy, audit finding, or incident report does and does not establish), and situational judgement (holding the line under senior pressure, coordinating without commanding, and improving processes without losing the people who must follow them).

The document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and how it is typically administered, a mapping of its dimensions to the specific skills named in your role's capability framework, a substantial set of practice questions with fully worked explanations, practical preparation tips, and common pitfalls to avoid. Questions progress from easy through moderate to challenging, and the challenging questions are genuinely challenging — they reflect the ambiguity and competing pressures of the role at your level.

To get the most from the guide: read each "About this assessment" section first so the formats hold no surprises; attempt every question and commit to an answer before reading the explanation; and treat each explanation as a short masterclass — even where you answer correctly, the walkthroughs are written to sharpen technique and to connect it back to the judgement your role exercises daily. Many of the scenarios will feel familiar. That is deliberate. The best preparation for a job-specific assessment is structured reflection on the job itself, and you will find that practising for these assessments doubles as a review of your own operating discipline: how you assess risk, how you weigh evidence, how you communicate decisions, and how you develop the teams and processes around you.

Take your time, work honestly, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the mental processes your role demands, using practical scenarios rather than abstract puzzles. For a change and release manager, that means questions built from the materials of change governance: forward schedules, risk classifications, dependency maps, CAB submissions, release calendars, freeze periods, and post-implementation evidence.

The typical format is an online, timed test of 15 to 30 minutes, with 15 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group at a comparable level; most modern platforms adapt question difficulty to your performance, and employers typically receive accuracy and speed as separate measures rather than a single score. Short ungraded practice questions are normally offered before the timed section begins.

For your role, cognitive assessment is particularly relevant because structured reasoning under time pressure is the substance of the job. Chairing a CAB well means holding a dozen changes in mind simultaneously — their risk levels, their dependencies, their windows, their requesters' track records — and noticing the conflict nobody has declared: two changes touching the same configuration item on the same night, a release scheduled inside a freeze, an impact assessment whose logic does not survive contact with the dependency map. Coordinating releases and interdependencies is constraint-satisfaction reasoning; diagnosing and prioritising incidents is deduction from incomplete evidence; improving change processes is pattern recognition across months of outcome data. A well-designed cognitive assessment rehearses each of these in miniature, which is why the practice below should feel less like test preparation and more like a compressed week in the role.

A note on approach: these tests are constructed so that most candidates do not finish. Sustained accuracy outscores rushed coverage on nearly every platform. Work briskly, but let your standard for "checked" stay high — the same standard you would apply before authorising a change to production.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your capability framework:

- **Pattern recognition** maps to your **Problem management** skill: initiating and monitoring actions to investigate patterns and trends is literally the skill's wording. Spotting that emergency changes cluster around one team's release cycle, or that failed changes share a common window, is how trend investigation starts. It also serves your **Availability and capacity management** duty to manage service components against KPIs — KPI drift is a pattern before it is a problem.
- **Logical deduction** maps to your **Change management** skill and your duty to make decisions for all technical changes: reasoning from policy, risk classification, and dependency data to what must follow — which changes conflict, which sequence is forced, what a piece of evidence does and does not establish — is the daily logic of authorisation.
- **Error checking** maps to your **Asset and configuration management** skill: ensuring that changes to assets are recorded and controlled appropriately means finding the schedule conflict, the stale record, and the impact assessment that contradicts the configuration data — before implementation does it for you.
- **Prioritisation** maps to your role as escalation point and to your **Incident management** skill: diagnosing and prioritising incidents, and choosing what deserves your personal attention first when several things are burning, is impact-and-urgency reasoning performed continuously.
- **Applied problem solving** maps to your **Service focus** skill — taking inputs and establishing coherent frameworks that work — and to your duty to actively improve and optimise change processes: decomposing a failing process into causes and redesigning it is problem solving at the process level, not just the incident level.

### Practice questions

**Question 1 (easy) — Pattern recognition in risk classification**

Your change policy classifies risk by two factors: service criticality (Gold, Silver, Bronze) and change type (routine, non-routine). The classification rule produces: Gold + non-routine = High risk; Gold + routine = Medium; Silver + non-routine = Medium; Silver + routine = Low; Bronze + non-routine = Low; Bronze + routine = Low. A CAB submission lists four changes with their claimed classifications:

1. Payments service (Gold), non-routine — High
2. Intranet (Bronze), non-routine — Medium
3. Case management (Gold), routine — Medium
4. Reporting service (Silver), routine — Low

Which change is misclassified?

- A) Change 1
- B) Change 2
- C) Change 3
- D) Change 4

**Correct answer: B**

**Explanation:** Apply the rule table mechanically to each row. Change 1: Gold + non-routine = High — correct. Change 2: Bronze + non-routine = Low by the table, but the submission claims Medium — misclassified. Change 3: Gold + routine = Medium — correct. Change 4: Silver + routine = Low — correct. The interesting feature is the direction of the error: change 2 is over-classified, not under-classified. Over-classification looks harmless — surely more caution never hurts? — but it has real costs: it consumes CAB scrutiny time that High-risk changes need, it trains requesters that classifications are decorative, and it erodes the data you use to tune the process (if Medium-risk changes "never fail", perhaps that is because half of them were really Low). When you audit classification quality as part of improving your change process, both directions of error matter. In the test, the technique is simple discipline: check every row against the rule, including the ones that look plausible.

**Question 2 (easy) — Deduction from delegated authority rules**

Your change policy states: "Standard changes are pre-authorised. Normal changes with Low or Medium risk may be authorised by the change and release manager. Normal changes with High risk require CAB authorisation. Emergency changes may be authorised by the change and release manager or, in their absence, the designated deputy, and must be reviewed at the next CAB." Last Tuesday — a day you were at work — a High-risk normal change was implemented. Which one of the following must be true, if the policy was followed?

- A) You personally authorised the change.
- B) The CAB authorised the change.
- C) The change was reviewed retrospectively at the next CAB.
- D) The deputy authorised the change.

**Correct answer: B**

**Explanation:** The policy assigns exactly one authorisation route to each category. The change in question is a High-risk normal change, and the policy is explicit: such changes "require CAB authorisation". If the policy was followed, the CAB authorised it — option B. Option A confuses your general decision-making role with this specific category: the policy delegates Low and Medium normal changes to you, but explicitly reserves High risk for the board you chair — chairing the CAB is not the same as being the CAB. Option C applies the retrospective-review rule, which belongs to emergency changes, not normal ones. Option D invokes the deputy, who features only in the emergency route, and only in your absence — and you were present. The discipline being tested is one your role exercises constantly: keeping authorisation routes crisply separated in your mind, because blurring them — treating "the change manager decides everything" as a summary of the policy — is precisely how governance drifts in real organisations. The policy's structure distributes authority deliberately; reading it deductively is how you keep it that way.

**Question 3 (easy) — Error checking a release calendar against constraints**

Your constraints for March: (i) a company-wide change freeze covers the first full week (Monday 2nd to Friday 6th); (ii) payments service releases may only occur on Tuesdays or Thursdays; (iii) no two releases may share the same day. A draft calendar proposes: Release A (HR system) — Wednesday 4th; Release B (payments) — Thursday 12th; Release C (payments) — Tuesday 17th; Release D (intranet) — Thursday 12th. How many constraint violations does the draft contain?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Check each constraint across the whole calendar. Freeze: Release A sits on Wednesday 4th, inside the 2nd–6th freeze — violation one. Payments days: Release B (Thursday) and Release C (Tuesday) both use permitted days — no violation. One-release-per-day: Releases B and D share Thursday 12th — violation two. Total: 2. Note the counting discipline: the shared day is one violation of one constraint, not two (each release is not separately guilty; the collision is the fault), and Release A's freeze breach is complete in itself regardless of what kind of service HR is, because the freeze is company-wide. Miscounting conflicts — double-counting collisions, or missing breaches because the individual entries each look innocent — is exactly how draft calendars pass review with problems intact. In your role, this check is the weekly bread of maintaining a forward schedule of change: constraints live in different documents (freeze notices, service-specific windows, capacity rules), and the conflicts only become visible when someone systematically applies all of them to the same draft. That someone is you, or the process you build.

**Question 4 (moderate) — Prioritisation as the escalation point**

It is 10:00 on Wednesday. Four items compete for your immediate attention:

1. A P2 incident is in progress; the incident manager reports the leading suspect is last night's change to the document service, and asks you to confirm whether an emergency back-out should be considered.
2. The CAB you chair convenes at 11:00; you have not yet read the two High-risk submissions on the agenda.
3. A programme director has emailed asking why their team's change was deferred last week and wants a call "this morning".
4. Your monthly change performance report to the service management board is due by close of play.

Which sequencing is most defensible?

- A) 2, 1, 3, 4 — the CAB is your chair's duty and is closest in time
- B) 1, 2, 3, 4 — support the live incident decision, then prepare for CAB, then the director, then the report
- C) 3, 1, 2, 4 — senior stakeholders should never wait
- D) 1, 3, 2, 4 — incident first, then the director before they escalate further

**Correct answer: B**

**Explanation:** Rank by impact-weighted urgency. Item 1 is a live service degradation with a decision pending that only you are positioned to make quickly: the back-out judgement needs the change context you own (what the change did, its back-out plan's state, what reversal risks). Minutes matter, and your input unblocks the incident team — it comes first, and note that "support the decision" may take ten focused minutes, not the morning. Item 2 is next: an 11:00 CAB with unread High-risk submissions is a governance failure in the making — chairing unprepared means either rubber-stamping or deferring, both of which damage the board's credibility; your preparation time is protected by handling it second. Item 3 is a relationship that matters, but "this morning" is the director's preference, not an operational deadline; a two-line holding reply ("in a live incident and pre-CAB; can I call you at 12:30?") manages the expectation honestly and costs ninety seconds — the full conversation follows the CAB. Item 4 has an end-of-day deadline and flexes around the rest. Option A puts meeting preparation ahead of a live incident; option C converts seniority into urgency, which is exactly the confusion your escalation-point role exists to resist; option D lets the director's impatience outrank your governance duty. The deeper pattern: as escalation point, your scarcest resource is focused attention, and the test — like the job — rewards spending it where your unique contribution is largest, while cheap communications (the holding reply) keep the queue orderly behind you.

**Question 5 (moderate) — Deduction through an interdependency chain**

Three releases are planned: the API gateway upgrade (G), the mobile app release (M), and the identity service update (I). Constraints: (i) M requires the new gateway features, so G must complete before M; (ii) the identity update changes an authentication interface that the current gateway cannot handle, but the upgraded gateway can — so I must not go live while the current gateway is in service; (iii) the mobile release team needs at least five working days of testing against the live upgraded gateway before M releases; (iv) I and G cannot be deployed in the same maintenance window, and windows occur weekly. If G deploys in window 1, what is the earliest window in which M can release, and where can I go?

- A) M in window 2; I in window 2
- B) M in window 2; I anywhere from window 2 onward
- C) M in window 3; I anywhere from window 2 onward
- D) M in window 3; I must wait until after M

**Correct answer: C**

**Explanation:** Work each constraint. G deploys in window 1. Constraint (iii): M needs at least five working days of testing against the live upgraded gateway — testing can begin after window 1, and five working days is a full working week, which consumes the gap between windows 1 and 2 entirely; M therefore cannot make window 2 and lands in window 3 at the earliest. Constraint (ii): I requires the upgraded gateway to be in service, which is true from window 1's completion onward; constraint (iv) only forbids I sharing a window with G — so I is free from window 2 onward. Nothing ties I to M in either direction: option D invents a dependency the constraints do not contain, and options A and B compress M's testing week to nothing. So M in window 3, I from window 2 onward — option C. Two professional observations: first, the reasoning is exactly your duty to coordinate releases and interdependencies, and the discipline of asking "which constraints actually bind, and which dependencies am I assuming?" is what separates a defensible sequence from a cautious guess — option D's phantom dependency is the kind that quietly adds weeks to real plans. Second, notice that I in window 2 puts two significant changes in consecutive weeks; the constraints permit it, but a good coordinator would also weigh support capacity across those weeks — the test asks what is possible; the role asks, additionally, what is wise.

**Question 6 (moderate) — Error checking a forward schedule of change**

Reviewing next week's forward schedule, you see four approved changes:

| Change | Configuration items affected | Window | Back-out duration |
|---|---|---|---|
| CHG-201 | Database cluster DB-A | Tuesday 20:00–23:00 | 45 min |
| CHG-202 | Web tier, load balancer LB-1 | Tuesday 20:00–23:00 | 30 min |
| CHG-203 | Database cluster DB-A | Tuesday 21:00–22:00 | 20 min |
| CHG-204 | Load balancer LB-1 firmware | Wednesday 02:00–04:00 | 90 min |

Policy: changes affecting the same configuration item must not have overlapping windows; a change's window must be long enough to contain its implementation and, in the worst case, its back-out. Which pair of changes presents the clearest policy conflict?

- A) CHG-201 and CHG-202
- B) CHG-201 and CHG-203
- C) CHG-202 and CHG-204
- D) CHG-203 and CHG-204

**Correct answer: B**

**Explanation:** Scan for shared configuration items first, then test windows. CHG-201 and CHG-203 both touch database cluster DB-A, and their windows overlap: 21:00–22:00 sits wholly inside 20:00–23:00 — a direct breach of the same-CI rule, and a genuinely dangerous one: two teams modifying one cluster simultaneously means neither team's testing validates the combined state, and a mid-window failure becomes unattributable — if the cluster misbehaves at 21:30, which change do you back out? Option A pairs changes on different CIs (database versus web tier and load balancer) in the same window, which the policy as stated permits — same-window is not the violation; same-CI-overlapping-window is. Option C shares LB-1 across CHG-202 and CHG-204, but their windows (Tuesday evening, Wednesday small hours) do not overlap — sequential changes to one CI are the normal rhythm of maintenance, though a thoughtful reviewer might note that CHG-204's team should know LB-1 changed the previous evening. Option D shares nothing. The transferable habit: conflict detection is a join across two dimensions — what is touched, and when — and schedules that look clean in either dimension alone can still collide in the intersection. Building this check into your schedule review (or automating it against CMDB relationship data) is exactly the kind of process hardening your change management skill's "actively improving and optimising" clause has in mind.

**Question 7 (moderate) — Pattern recognition in change outcome data**

Analysing six months of change data, you tabulate emergency changes by requesting team and month:

| Team | Jan | Feb | Mar | Apr | May | Jun |
|---|---|---|---|---|---|---|
| Platform | 2 | 1 | 2 | 2 | 1 | 2 |
| Payments dev | 1 | 6 | 1 | 7 | 1 | 6 |
| Service desk | 1 | 1 | 2 | 1 | 1 | 1 |

The payments development team releases on a two-month cycle, with major releases landing in February, April, and June. Which interpretation best fits the data?

- A) The payments team's emergency changes spike in its release months, suggesting its releases are going out with defects that then require emergency fixes.
- B) The payments team is simply busier than other teams, so more emergencies are expected.
- C) Emergency change volumes are random; no pattern is present.
- D) The service desk causes the payments team's emergencies.

**Correct answer: A**

**Explanation:** Read the table against the known cycle. Payments dev shows 6, 7, and 6 emergency changes in exactly the release months (February, April, June) and 1 in every other month — a six-to-sevenfold swing locked to the release calendar across three full cycles. The other teams sit flat at 1–2 throughout, which rules out any organisation-wide seasonal cause. Option A names the mechanism the correlation most plausibly indicates: releases shipping with defects that surface immediately and get patched under emergency procedures — a hypothesis, but one with three cycles of consistent evidence and an obvious next test (do the emergency changes' descriptions reference the release's components?). Option B fails because "busier" would elevate the baseline, not create a two-month sawtooth synchronised to releases. Option C ignores a pattern as clean as operational data ever produces. Option D has no support whatsoever in the data. This is your problem management skill executed exactly as your framework words it — initiate and monitor actions to investigate patterns and trends to resolve problems — and the follow-through matters as much as the detection: the finding points at preventative measures (release testing quality, staged rollout, post-release monitoring) rather than at tightening emergency change scrutiny, because the emergencies are a symptom. The mature move is to take the pattern to the payments team as a shared problem to investigate, consulting specialists where required — not as an accusation. Data opens that conversation; how you open it determines whether it produces improvement or defensiveness.

**Question 8 (moderate) — Applied problem solving: a CAB drowning in volume**

Your weekly CAB reviews every normal change, currently around 40 per week. Meetings overrun by an hour, scrutiny of genuinely risky changes is rushed, and delivery teams complain of a two-week authorisation queue. Analysis shows 70% of submissions are low-risk, repeatable changes with a 99.5% success rate; 25% are medium-risk with 97% success; 5% are high-risk with 88% success. Which redesign most improves the process?

- A) Extend the CAB meeting by an hour so everything gets proper scrutiny.
- B) Reclassify the recurring low-risk changes as standard (pre-authorised) via documented templates, delegate medium-risk authorisation to the change manager with periodic sampling review, and focus the CAB on high-risk changes and on reviewing the delegation's outcome data.
- C) Split the CAB into two weekly meetings, halving each agenda.
- D) Require all submissions two weeks earlier so papers can be read in advance.

**Correct answer: B**

**Explanation:** Diagnose before designing: the CAB's scarce resource is collective scrutiny, and the data shows it being spent almost entirely where it adds least — 70% of the agenda carries a 0.5% failure rate, while the 5% that fails one time in eight gets rushed. The principle is risk-proportionate governance, and option B applies it at each tier: recurring low-risk changes become standard changes — pre-authorised through documented templates, which is exactly what the standard-change mechanism exists for — removing 28 items from the agenda while keeping them recorded and controlled; medium-risk moves to your delegated authority (squarely within a change manager's remit) with sampling review, so the delegation remains evidenced rather than trusted; and the CAB's recovered time concentrates on the high-risk 5% plus oversight of the new tiers' outcome data — governance of the system, not just the items. Options A and C treat the symptom (meeting length) while preserving the misallocation: the same low-value scrutiny, spread across more hours or more meetings, and the queue persists. Option D improves preparation while lengthening the very queue teams are complaining about — thoroughness purchased with the currency you are shortest of. Note also what B does culturally: it converts the CAB from a bottleneck delivery teams route around into a board whose attention signals genuine risk — which is how your service focus skill's "coherent frameworks that work" looks in change governance, and why "actively improving and optimising processes" is written into your change management skill rather than left as an occasional project.

**Question 9 (challenging) — Multi-constraint release coordination**

Four releases must be scheduled across four weekly windows (W1-W4): Finance (F), Portal (P), Data platform (D), and Security patch (S). Constraints: (i) D must precede P, because the portal release consumes the data platform's new API; (ii) P requires at least two full windows' gap after D for phased integration testing — so D in W1 permits P in W4 at the earliest; (iii) S must be deployed within the first two windows under security policy; (iv) the finance team is unavailable in W2, so F cannot be scheduled there; (v) exactly one release per window. Which schedule satisfies every constraint?

- A) W1: D, W2: S, W3: P, W4: F
- B) W1: S, W2: D, W3: F, W4: P
- C) W1: D, W2: S, W3: F, W4: P
- D) W1: F, W2: S, W3: D, W4: P

**Correct answer: C**

**Explanation:** Start with the tightest constraint and let it force the rest. Constraint (ii) demands two full windows between D and P: within four windows, the only placement that achieves it is D in W1 and P in W4, with W2 and W3 as the testing gap. That single deduction fixes half the schedule. Now place S: constraint (iii) confines it to W1 or W2, and W1 is taken by D, so S goes in W2. F takes the only remaining window, W3 — which also satisfies constraint (iv), since W3 is not W2. The schedule is forced at every step: D, S, F, P — option C, and no alternative survives. Confirm by eliminating the others: option A puts P in W3 with only one clear window (W2) after D, breaching (ii); option B puts D in W2 and P in W4, again leaving only one window's gap (W3); option D opens with F in W1, pushing D to W3 — from which (ii) would require P in W6, two windows beyond the calendar — and for good measure it schedules P immediately after D. The solving technique is the professional lesson: identify the constraint with the fewest satisfying placements, commit it first, and watch the remaining freedom collapse — the same order of operations that makes real release calendars tractable, where the two-month integration dependency gets pinned before anyone argues about who prefers which Tuesday. Its converse is equally practical: when a stakeholder asks you to move one release "just a week", the answer is rarely local — trace which binding constraint the move breaks, and you can show them the cost rather than assert it. Coordinating releases and interdependencies, as your role requires, is exactly this: making the constraint structure explicit enough that the schedule defends itself.

**Question 10 (challenging) — Deduction from post-incident evidence**

At 03:10 the payments API began returning errors. Three changes completed earlier that night: CHG-301 (02:00, database index rebuild on the payments database), CHG-302 (02:30, TLS certificate renewal on the API gateway), CHG-303 (02:45, logging configuration change on an unrelated HR service). Evidence: the payments database's query times have been normal all night; the API gateway logs show successful TLS handshakes until 03:05, then handshake failures from external clients only — internal clients continue to succeed; the certificate deployed by CHG-302 included the server certificate but the accompanying intermediate certificate bundle was replaced with an incomplete one; external clients validate the full chain, while internal clients trust the server certificate directly. What is the best-supported conclusion?

- A) CHG-301 caused the failure — the database is the payments system's core.
- B) CHG-302 caused the failure — the incomplete intermediate bundle breaks chain validation for external clients, matching the observed internal/external split.
- C) CHG-303 caused the failure — it was the last change before the errors.
- D) The failure is external to all three changes, since handshakes succeeded until 03:05, after all changes completed.

**Correct answer: B**

**Explanation:** Reason from the failure's signature, not from proximity or importance. The discriminating observation is the split: external clients fail, internal clients succeed, simultaneously, on the same gateway. Work each hypothesis against it. CHG-301: database trouble would degrade responses for all callers equally once requests reached the database — and the evidence directly clears it (query times normal all night). Option A substitutes the component's importance for evidence, a persistent bias in incident rooms. CHG-303 touched an unrelated service; "last change before the errors" is pure temporal proximity — post hoc reasoning with no mechanism, and the 25-minute gap to 03:10 is anyway shorter than CHG-302's 40 minutes only if one ignores that certificate changes commonly bite when sessions expire and renegotiate, not at deployment. That also dissolves option D's argument: successful handshakes until 03:05 do not exonerate a 02:30 certificate change, because existing sessions continue on the old handshake until renegotiation — the delay is the mechanism's signature, not its alibi. Option B fits every observation: an incomplete intermediate bundle breaks chain validation, which is exactly the validation external clients perform and internal clients (trusting the server certificate directly) skip — reproducing the split precisely — and the deployment detail (bundle replaced with an incomplete one) supplies the defect directly. This is your incident management skill as your framework states it — diagnose, investigate causes, find resolutions — and the transferable techniques are two: first, the differential signature (who fails and who does not) eliminates faster than any timeline; second, ask of each candidate change "by what mechanism, and on what delay, would this produce exactly this failure?" — changes without a mechanism are noise, whatever their timing. The resolution follows from the diagnosis: redeploy the complete bundle, and feed the packaging gap into problem management as a preventative measure — certificate deployments should validate the full chain as a post-implementation check.

**Question 11 (challenging) — Reasoning about a risk assessment's logic**

A CAB submission assesses a change as follows: "Likelihood of failure: Low, because this upgrade has been performed successfully in the test environment and by two other government departments. Impact if failed: Low, because the change window is overnight and the service has few users at that hour. Overall risk: Low. Recommended approval route: expedited." Which is the most serious flaw in this assessment's reasoning?

- A) The likelihood assessment relies on evidence from environments that may not match production.
- B) The impact assessment measures the impact of a failure detected and contained within the window, but ignores the impact of a failure that persists or emerges into business hours — impact must be assessed on the credible worst case, not the convenient case.
- C) Two other departments is too small a sample to establish anything.
- D) Overnight windows are riskier because fewer staff are available.

**Correct answer: B**

**Explanation:** All four options contain something arguable; the question asks for the most serious flaw, which means finding the one that breaks the assessment's structure rather than merely weakening an input. Option B does: the submission's impact logic quietly substitutes "impact of a failure at the moment of implementation" for "impact of this change failing". A failed overnight change whose effects surface at 09:00 — data corrupted silently, a service that starts refusing logins under morning load, a back-out that itself fails — lands on the full business day, and the overnight window's emptiness is irrelevant to that scenario. Since risk = likelihood × impact, an impact score assessed on the best-case failure mode understates overall risk by construction, and the error then propagates into the approval route: "expedited" scrutiny is being recommended on the strength of the very corner the assessment cut. Option A is a fair challenge but a weaker one — test environments and other departments' experience are legitimate likelihood evidence, merely imperfect; the assessment's likelihood reasoning is incomplete, not structurally wrong. Option C overstates: two independent successful deployments is meaningful (if modest) evidence, not nothing. Option D is a reasonable operational observation that cuts against the impact claim but is itself situational. The chairing skill this rehearses is precise: your CAB's quality depends less on rejecting bad submissions than on asking the question that exposes structural optimism — "walk me through the worst credible failure mode and its business-hours impact" — and teaching requesters, through repetition, that impact means worst credible case. Assessments improve fastest when the chair's questions are predictable; that, too, is process improvement.

**Question 12 (challenging) — Integrated reasoning before a major go-live**

Three days before a major release, three artefacts land on your desk. The readiness report says all 214 test cases passed, but a footnote records that the performance test ran against a dataset one-tenth of production size "due to environment constraints". The service desk forecast, based on the last three major releases, predicts a 30–40% call spike in week one and notes the desk is already at 92% capacity. An email from the programme director states the go-live date is contractually committed, that the release has passed all tests, and that they expect confirmation of go-live at tomorrow's board. Which position best reflects sound reasoning across all three artefacts?

- A) Confirm go-live: 214 of 214 tests passed, and the contractual commitment settles the matter.
- B) Refuse go-live until performance testing is repeated at production scale, whatever the contractual position.
- C) Take to the board a conditional position: the functional evidence is strong, but the performance evidence does not cover production load and the support capacity forecast shows week one absorbing a 30–40% spike into an 8% margin — so present the residual risks with mitigation options (production-scale performance test in the remaining days, staged rollout or throttled onboarding, temporary desk reinforcement, a defined rollback trigger) and let the board decide with the risk visible.
- D) Confirm go-live but privately brief the service desk to expect a difficult week.

**Correct answer: C**

**Explanation:** Integrate what each artefact actually establishes. The readiness report's headline (214/214) is functional evidence — real and strong — but its footnote quietly voids the performance claim: a test at one-tenth scale establishes behaviour at one-tenth scale, and the phrase "all tests passed" in the director's email is therefore true in letter and misleading in substance; whoever confirms go-live on it adopts that gap as their own. The desk forecast converts a vague worry into arithmetic: a 30–40% spike arriving into 8% headroom is an overload forecast, not a caution. The director's email, finally, is a fact about consequences (contractual commitment) and a preference about process (confirm tomorrow) — it changes the cost of delay, which is genuine decision input, but it changes nothing about the technical evidence. Option C is the only position that lets every artefact keep its true weight: it neither suppresses the risk (A confirms on the misleading headline and lets the contractual pressure do the reasoning; D confirms while whispering the risk to the people who will absorb it — informing the desk is not mitigating the overload) nor absolutises it (B treats one residual risk as a veto, ignoring that the remaining three days might close it and that go/no-go on contractually committed releases is a board-level trade-off, not a unilateral one). Note what C preserves that A, B and D all surrender: the decision-maker's sight of the risk. Your role's authority — decisions for all technical changes — is exercised here precisely by refusing to launder uncertainty into a clean "confirmed": you certify what the evidence supports, present what it does not, price the mitigations, and put the residual trade-off where it belongs. Boards forgive risks they were shown and accepted; they do not forgive risks that were footnotes. Reading the footnote — literally and habitually — is the whole discipline of this question, and a fair summary of change governance.

### Preparation tips

- **Practise on your own governance artefacts.** Take a recent forward schedule, CAB pack, or post-implementation review and interrogate it: which constraints bind, which classifications would survive re-derivation from the rule, which footnotes change the headline? Real artefacts train the exact muscles the test measures.
- **Draw the structure before reasoning about it.** Dependency chains, windows, and constraint sets belong on scrap paper, not in working memory. The two minutes spent sketching repays itself in every multi-constraint question.
- **Check every option against every rule.** Plausible-looking rows and schedules are where errors hide. The mechanical pass — each item against each constraint — is slower per question and faster per correct answer.
- **Reason from mechanisms, not proximity.** For evidence questions, ask of each candidate cause: by what mechanism, and on what delay, would it produce exactly this signature? Timing correlations without mechanisms are the test's favourite distractor and the incident room's favourite trap.
- **Assess impact on the credible worst case.** Wherever a scenario offers a convenient framing (overnight window, small sample, headline pass rate), practise asking what the inconvenient framing would show.
- **When two options both seem right, a constraint is under-read.** Return to the exact wording; the intended reading is the one under which a single option survives. Cultivate the same precision with your own policies.
- **Manage the clock like a change window.** Time-box hard questions, bank the accessible marks, and return if time allows. Sustained accuracy across the paper outscores heroics on any single item.

### Common pitfalls to avoid

- **Letting importance substitute for evidence.** The critical component is not automatically the failed one, and the senior stakeholder's request is not automatically the urgent one. Both confusions appear in tests because both appear in operations.
- **Double-counting or under-counting conflicts.** A collision is one violation; a breach is complete regardless of intent. Count against the constraint, not against your sense of severity.
- **Accepting headline numbers without their footnotes.** "All tests passed" and "99.5% success" are claims with scopes. The scope is where the question — and the risk — lives.
- **Inventing dependencies.** Constraint questions punish assumed orderings the rules never state, and real release plans lose weeks to them. Distinguish "must precede" from "usually precedes" ruthlessly.
- **Treating over-classification as harmless.** Inflated risk ratings and padded schedules feel safe but degrade the signal your governance runs on. The test rewards noticing errors in both directions.
- **Exonerating changes by deployment time.** Failures follow mechanisms and delays — session renewals, cache expiries, morning load. "It worked at deployment" clears nothing by itself.
- **Rushing the reading to save time for the reasoning.** Most wrong answers at this level are misread constraints, not failed logic. Read once well; it is faster than reasoning twice.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the quantitative material your role produces and consumes: change volumes and success rates, availability KPIs, incident metrics, capacity utilisation, trend data, and the business cases that justify process investment. It is not a mathematics examination — nothing beyond percentages, ratios, averages, rates, and disciplined table reading is required. What it measures is the quality of your quantitative judgement: selecting the right figures, applying the right operation, and understanding what the result does and does not mean.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions, each presenting a table, chart, or short data scenario with four or five answer options. An on-screen calculator is normally permitted and should be used. Scoring is against a norm group at a comparable level; adaptive difficulty is common; and accuracy is typically weighted more heavily than coverage.

For a change and release manager, numeric reasoning is not adjacent to the role — it is the evidence layer of it. Your authorisation decisions rest on failure rates and their scopes; your duty to manage service components against KPIs means converting targets like 99.9% into the minutes they actually permit, and knowing when a month has breached them; your process improvements live or die by whether you can quantify the case — what the current failure load costs, what the redesign saves, when it pays back. And as the person who reports change performance to boards, you are the last check between a misleading number and a decision made on it: a success rate computed on the wrong base, a "20% improvement" that is really 20 percentage points, an average that hides the tail. The questions below rehearse precisely these situations, and every worked answer shows the arithmetic step by step.

One orientation note: at your level, the test's harder questions are rarely hard because the calculation is complex. They are hard because the scenario offers a plausible wrong number — the convenient base, the flattering comparison, the headline without its denominator. The discipline being measured is the one your role practises daily: interrogate the number before you use it.

### How this assessment maps to your role

The numeric skills tested map directly to the named skills in your capability framework:

- **Percentages, rates, and their bases** map to your **Change management** skill and your authorisation duty: success and failure rates by category, month, and team are the core evidence of change performance, and computing them on the correct base is what makes your CAB reporting and your delegation decisions defensible.
- **Availability arithmetic** maps to your **Availability and capacity management** skill: managing service components to meet business needs and KPIs requires fluent conversion between availability percentages and downtime minutes, and correct judgement about when a target has been breached and by how much.
- **Weighted averages and aggregation** map to your reporting duties and your **Service focus** skill: combining figures across teams, categories, and periods without distortion is what makes a coherent framework's metrics trustworthy rather than merely tidy.
- **Trend analysis and projection** maps to your **Problem management** skill — investigating patterns and trends — and to capacity planning for the change process itself: forecasting when CAB load exceeds capacity, or whether an improvement trajectory will reach its target, is simple arithmetic with governance consequences.
- **Cost-benefit and payback reasoning** maps to your duty to actively improve and optimise change processes: process investment competes for funding, and the manager who can quantify failure cost, saving, and payback period is the one whose improvements get approved.
- **Reading data about users and services** maps to your **User focus** skill: using quantitative and qualitative data about users to turn user focus into outcomes starts with reading the quantitative part correctly.

### Practice questions

**Question 1 (easy) — Quarterly change success rate**

Last quarter, 480 changes were implemented. 456 succeeded; the rest failed or were backed out. What was the quarterly change success rate?

- A) 92%
- B) 94%
- C) 95%
- D) 96%

**Correct answer: C**

**Explanation:** Success rate = successful ÷ total × 100. Step 1: 456 ÷ 480 = 0.95. Step 2: 0.95 × 100 = 95%. Cross-check from the failure side: failures = 480 − 456 = 24, and 24 ÷ 480 = 5%; 100% − 5% = 95% — two routes, one answer. Worth internalising at your level: the complement (the 5%, i.e. 24 failed changes) is usually the more informative number for governance purposes, because improvement work targets failures, not successes, and 24 is a countable population you can categorise by cause, team, and change type. Headline success rates reassure boards; failure counts drive problem management. Report both.

**Question 2 (easy) — Average CAB throughput**

Over four consecutive weekly CAB meetings, the board considered 38, 42, 35, and 45 changes. What was the average number of changes considered per meeting?

- A) 39
- B) 40
- C) 41
- D) 42

**Correct answer: B**

**Explanation:** Mean = total ÷ number of meetings. Step 1: 38 + 42 = 80; 80 + 35 = 115; 115 + 45 = 160. Step 2: 160 ÷ 4 = 40. Sense-check: the values span 35 to 45, and 40 sits centrally — a mean outside the data's range always indicates an arithmetic slip. The managerial layer: a four-week average of 40 items per meeting is itself a finding. If each item deserving scrutiny needs even three minutes, that is two hours of pure item time before any discussion — an average like this is the quantitative predicate for the process redesigns you weigh as chair (standard-change reclassification, delegated tiers). Averages are not just summaries; at your level they are the opening sentences of business cases.

**Question 3 (easy) — Change mix ratio**

Last month's 400 changes split across standard, normal, and emergency categories in the ratio 12 : 7 : 1. How many emergency changes were there?

- A) 16
- B) 20
- C) 24
- D) 28

**Correct answer: B**

**Explanation:** Step 1: total parts = 12 + 7 + 1 = 20. Step 2: one part = 400 ÷ 20 = 20 changes. Step 3: emergency = 1 part = 20. Verify the full split: standard = 240, normal = 140, emergency = 20; total 400 — consistent. The ratio's governance meaning deserves as much attention as its arithmetic: emergencies at 5% of volume (20 in 400) is a figure worth tracking as a KPI in its own right, because the emergency route bypasses forward planning and full assessment — it is a pressure valve, and a rising ratio means either genuine instability or teams discovering the valve is easier than the process. Either way, the trend triggers investigation. Ratios turn raw volumes into comparable shapes across months of different sizes; that is why your monthly report should carry the mix, not just the totals.

**Question 4 (moderate) — Availability target in minutes**

A service has a 99.9% monthly availability KPI. Using a 30-day month (43,200 minutes), how many minutes of downtime does the KPI permit, and did a month containing 65 minutes of downtime breach it?

- A) 43.2 minutes permitted; 65 minutes breached the KPI
- B) 432 minutes permitted; 65 minutes met the KPI
- C) 43.2 minutes permitted; 65 minutes met the KPI
- D) 4.3 minutes permitted; 65 minutes breached the KPI

**Correct answer: A**

**Explanation:** Step 1: the permitted unavailability is 100% − 99.9% = 0.1% of the month. Step 2: 0.1% of 43,200 = 0.001 × 43,200 = 43.2 minutes. Step 3: compare: 65 > 43.2, so the month breached the KPI, by 65 − 43.2 = 21.8 minutes. Option B misplaces the decimal (432 minutes corresponds to 99%), and option D overshoots the other way (4.3 minutes corresponds to 99.99%) — decimal placement is the entire difficulty of "nines" arithmetic, and misplacing it changes the service's obligations tenfold. This conversion should be reflexive for you, in both directions, because it prices your decisions: a change window that takes a 99.9% service down for 30 minutes has consumed 69% of the month's entire error budget before any unplanned incident occurs. That framing — planned downtime and incidents drawing on the same 43.2-minute budget — is often the sharpest way to explain to a delivery team why their preferred deployment approach needs a zero-downtime design, and it is exactly what managing service components against KPIs means in practice.

**Question 5 (moderate) — Percentage points versus percent**

The change success rate rose from 92% in Q1 to 95% in Q2. Which statement describes the improvement accurately?

- A) Success improved by 3%.
- B) Success improved by 3 percentage points, which is a relative improvement of about 3.3% — and a reduction in the failure rate of 37.5%.
- C) Success improved by 3 percentage points, which is the same thing as 3%.
- D) The failure rate fell by 3%.

**Correct answer: B**

**Explanation:** Work the three different quantities. The absolute change is 95 − 92 = 3 percentage points. The relative change in the success rate is 3 ÷ 92 = 0.0326 ≈ 3.3%. And the failure rate fell from 8% to 5%: a fall of 3 percentage points, but a relative reduction of 3 ÷ 8 = 37.5%. Option B states all three correctly and, crucially, keeps them distinct. Options A and C blur points with percent — a conflation that is nearly harmless here (3 points ≈ 3.3%) but wildly misleading at other bases, and habitual precision is what stops the misleading cases slipping through. Option D commits the blur in its most consequential direction: "the failure rate fell by 3%" would mean 8% dropping to 7.76%, a barely visible improvement, when the truth is a 37.5% collapse in failures — the most impressive true statement available about this quarter. The reporting lesson runs both ways: know which framing is honest and know that audiences will hear whichever you say. "Failures down 37.5%" and "success up 3.3%" describe the same quarter; a manager reporting to a board should say "3 percentage points, which means failures fell by more than a third" — precise, and precisely understood. This distinction appears in numeric tests at every senior level because getting it wrong in a real report is both common and quietly reputation-damaging.

**Question 6 (moderate) — Failure rates from a mixed table**

Last quarter's changes by category:

| Category | Changes implemented | Failed |
|---|---|---|
| Standard | 300 | 3 |
| Normal | 150 | 9 |
| Emergency | 30 | 6 |

Which category had the highest failure rate, and what was it?

- A) Normal — 6%
- B) Emergency — 20%
- C) Standard — 1%
- D) Emergency — 6%

**Correct answer: B**

**Explanation:** Compute each rate on its own base. Standard: 3 ÷ 300 = 1%. Normal: 9 ÷ 150 = 6%. Emergency: 6 ÷ 30 = 20%. Emergency's rate is highest at 20% — one failure in every five — even though normal changes produced the most failures in absolute terms (9). The distractor structure is instructive: option A rewards the eye drawn to the biggest failure count; option D pairs the right category with a rate computed on someone else's base. Rates and counts answer different questions — "where is the risk concentrated per change?" versus "where does the failure volume come from?" — and your governance needs both: the 20% emergency failure rate is an argument about the emergency route itself (rushed assessment produces one-in-five failure; are all these emergencies genuine?), while the 9 normal-change failures are the larger workload for post-implementation review. Note also the arithmetic fragility of small bases: emergency's 20% rests on 6 failures in 30 changes, so a single change flips the rate by 3.3 points — quote small-base rates with their counts ("6 of 30") so readers can weigh them properly. That habit is what separates KPI reporting from KPI theatre.

**Question 7 (moderate) — Combining success rates across quarters**

In Q1, 400 changes were implemented with a 92% success rate. In Q2, 600 changes were implemented with a 95% success rate. What was the success rate across the half-year?

- A) 93.5%
- B) 93.8%
- C) 94.0%
- D) 94.2%

**Correct answer: B**

**Explanation:** Do not average 92% and 95% — the quarters differ in size, so weight by volume. Step 1: Q1 successes = 0.92 × 400 = 368. Step 2: Q2 successes = 0.95 × 600 = 570. Step 3: total successes = 368 + 570 = 938. Step 4: total changes = 400 + 600 = 1,000. Step 5: combined rate = 938 ÷ 1,000 = 93.8%. The unweighted average (93.5%, option A) understates performance because it gives the smaller, weaker quarter equal say. The convenient round total (1,000) makes this example transparent, but the principle scales to every aggregation your reporting performs: across teams, services, months, and categories, percentages combine only through their raw counts. At your level there is also a directional caution worth naming: whichever way the unweighted error happens to point, someone will have an interest in preferring it — the flattering version for the annual report, the alarming version for the funding bid. The manager whose aggregates always reconcile to raw counts is immune to both temptations, and visibly so, which is what makes their numbers quotable upward without checking. That reputation is an asset; weighted arithmetic is how it is earned.

**Question 8 (moderate) — Release window capacity**

Your organisation runs four release windows per month, and operational policy caps each window at three releases. Next month's demand is 14 releases. What is the position?

- A) Capacity is 12 releases; demand exceeds it by 2, so either 2 releases must move to the following month or an additional window must be agreed.
- B) Capacity is 12 releases; at 14 demanded, utilisation is 86%, which is acceptable.
- C) Capacity is 16 releases; demand fits with 2 spare.
- D) Windows can each take a fourth release, so demand fits exactly.

**Correct answer: A**

**Explanation:** Step 1: monthly capacity = 4 windows × 3 releases = 12. Step 2: demand versus capacity: 14 − 12 = 2 releases over. The position is a genuine overflow with exactly two resolutions inside your gift as coordinator: defer two releases (which two, and by what priority logic, is the real decision) or expand capacity through an agreed exception (an additional window, with the support and risk implications that carries). Option B miscomputes utilisation — 14 ÷ 12 = 117%, not 86% (that is 12 ÷ 14, the ratio inverted) — and utilisation above 100% is not a percentage nuance; it is a scheduling impossibility wearing a percentage. Option C multiplies wrongly. Option D simply repeals the policy under demand pressure — and note how naturally it phrases itself ("can each take a fourth"): capacity caps exist because of support coverage, back-out headroom, and cumulative risk per window, and a cap that yields whenever demand exceeds it was never a cap. The professional shape of the answer matters: "demand exceeds capacity by 2" is not a problem statement to escalate raw — your role is to arrive with the prioritisation proposal attached: which two releases have the least date-sensitivity, what the deferral costs, and whether the overflow is a spike or the start of a trend requiring a structural fifth window. Capacity arithmetic is trivial; capacity judgement is the job.

**Question 9 (challenging) — Payback period for process automation**

Your organisation implements 200 changes per quarter with a 5% failure rate. Each failed change costs an average of £2,500 in investigation, rework, and lost productivity. A proposed automated testing and deployment pipeline costs £120,000 and is credibly projected to reduce the failure rate to 2%. Ignoring other benefits, what is the payback period?

- A) 4 quarters
- B) 6 quarters
- C) 8 quarters
- D) 10 quarters

**Correct answer: C**

**Explanation:** Step 1: current failures = 5% of 200 = 10 per quarter, costing 10 × £2,500 = £25,000. Step 2: projected failures = 2% of 200 = 4 per quarter, costing 4 × £2,500 = £10,000. Step 3: quarterly saving = £25,000 − £10,000 = £15,000. Step 4: payback = £120,000 ÷ £15,000 = 8 quarters — two years. That is the arithmetic; the judgement around it is what your level adds. First, stress-test the sensitive assumption: the case rests on the failure rate genuinely falling to 2% — if it only reaches 3.5%, the saving drops to £7,500 a quarter and payback doubles to four years; a business case worth signing shows this sensitivity rather than hiding it. Second, notice what "ignoring other benefits" excludes: faster authorisation cycles, released CAB capacity, and the unmeasurable cost of the failures' service impact on users — a two-year payback on failure cost alone usually understates the true case, which strengthens rather than weakens your proposal, and saying so explicitly ("payback is eight quarters on the narrowest benefit measure alone") is the honest way to present it. Third, the framing habit: converting a failure rate into pounds per quarter is the single most persuasive move available to a manager arguing for process investment, because it moves the conversation from "quality is important" to "this leak costs £100,000 a year and here is the £120,000 tap washer". Your duty to actively improve and optimise processes competes for funding; this is the arithmetic that wins it.

**Question 10 (challenging) — Projecting CAB load against capacity**

CAB submissions have grown linearly for six months and now stand at 40 per week, rising by a steady 6 submissions per month. The board's effective capacity for proper scrutiny is 70 submissions per week. If the trend continues and nothing changes, in how many months will weekly submissions first exceed the board's capacity?

- A) 4 months
- B) 5 months
- C) 6 months
- D) 8 months

**Correct answer: C**

**Explanation:** Submissions after n months = 40 + 6n. The board is exceeded when 40 + 6n > 70, so 6n > 30, so n > 5: the first whole month satisfying the inequality is n = 6. Verify by stepping: month 5 gives 40 + 30 = 70 — at capacity, not over it — and month 6 gives 76, the first breach. Option B is the off-by-one error the wording is built to catch: "exceed" means strictly greater, and 70 equals 70. The projection technique is elementary; the managerial content is in what you do with a six-month runway. First, month 5's "at capacity" is the real deadline — a board running at 100% scrutinises nothing properly and has no headroom for the emergency spike, so the intervention date is earlier than the breach date. Second, linear trends in demand are usually symptoms with causes you can inspect: is the growth new services onboarding (structural — capacity must change), or is it low-risk repeat changes that belong in the standard category (misclassification — demand can be reshaped, as in the cognitive section's CAB redesign)? The projection tells you when the wall arrives; the decomposition tells you whether to move the wall or redirect the traffic. Third, this is your own process's capacity management — the same KPI discipline you apply to service components, applied reflexively to the governance you run. Boards that watch their services' capacity but not their own are a pattern; be the counterexample.

**Question 11 (challenging) — Recovering an SLA mid-quarter**

Your target: 85% of change-related P2 incidents resolved within four hours. So far this quarter, 45 such incidents have occurred, 36 resolved within four hours. If incidents keep occurring, what is the minimum number of consecutive future incidents that must all be resolved within four hours to bring the quarterly figure to at least 85%?

- A) 3
- B) 9
- C) 12
- D) 15

**Correct answer: D**

**Explanation:** Current position: 36 ÷ 45 = 80% — five points short. Let n be the number of future incidents, all resolved within target. The quarterly figure becomes (36 + n) ÷ (45 + n), and you need (36 + n) ÷ (45 + n) ≥ 0.85. Solve: 36 + n ≥ 0.85 × (45 + n) = 38.25 + 0.85n, so 0.15n ≥ 2.25, so n ≥ 15. Check n = 15: (36 + 15) ÷ (45 + 15) = 51 ÷ 60 = 85% exactly — target met at the boundary. The intuitive guesses fail instructively: option A treats the gap as "3 more of the original 45" (39 ÷ 45 = 86.7%), forgetting that future incidents enlarge the denominator too — every new incident you resolve in time pulls the average up by less than the one before, because it also dilutes itself. That denominator drag is why recovering a ratio mid-period is always harder than the raw gap suggests, and why the honest management insight here is uncomfortable arithmetic: you need a fifteen-incident perfect streak, with zero misses — a single failure during the streak resets the requirement higher. Two professional conclusions follow. First, report the recovery requirement, not just the current 80%: "we need 15 consecutive in-target resolutions to recover the quarter" tells the board the true probability of recovery in a way "five points behind" does not. Second, the calculation is an argument for early-quarter vigilance in every ratio-based KPI you own — misses banked early are nearly irrecoverable later, so the time to escalate a slipping SLA is at the first miss pattern, not at the quarter's death. Managers who understand denominator drag escalate in month one; managers who do not write explanatory paragraphs in month three.

**Question 12 (challenging) — Compound reduction toward a target**

Your improvement programme aims to reduce emergency changes by 20% per quarter, compounding, from a current level of 50 per quarter. The target is to reach 25 or fewer per quarter. If the programme achieves exactly 20% reduction each quarter, during which quarter's result will the target first be met?

- A) The 2nd quarter
- B) The 3rd quarter
- C) The 4th quarter
- D) The 5th quarter

**Correct answer: C**

**Explanation:** Compound each quarter at 80% of the previous level. Quarter 1: 50 × 0.8 = 40. Quarter 2: 40 × 0.8 = 32. Quarter 3: 32 × 0.8 = 25.6. Quarter 4: 25.6 × 0.8 = 20.48 — the first result at or below 25. So the target is met in the fourth quarter's result — option C. The tempting error is linear thinking: "20% of 50 is 10 per quarter, so 50 → 40 → 30 → 20, done in quarter 3" — but percentage reductions compound on a shrinking base, so each quarter removes fewer changes than the last (10, then 8, then 6.4, then 5.1). Quarter 3's 25.6 is agonisingly close to the target and does not meet it; "25 or fewer" is a boundary, and 25.6 sits outside it — precision at boundaries is a repeated theme in numeric tests because it is a repeated failure in real reporting, where 25.6 becomes "about 25, basically there" in a slide deck. Two management notes. First, the decelerating trajectory is a feature to anticipate in your communications: stakeholders who cheered the ten-change reduction in quarter one will ask why quarter four only managed five; the honest answer — the same 20% of an improving base — should be in the programme's expectations from the start. Second, compounding percentage targets embed an assumption worth challenging in real programmes: early reductions harvest the easy causes (misclassified emergencies, one team's bad release cycle), and holding 20% per quarter gets harder as the remaining emergencies become the genuinely irreducible ones. A fixed-percentage glide path that ignores this will be met for two quarters and missed thereafter — set the trajectory with a floor, and revisit it as the mix changes. Targets, like changes, deserve impact assessment before they are authorised.

### Preparation tips

- **Drill the conversions your KPIs use.** Availability percentages to minutes (both directions, all the common "nines"), rates to counts, points to percent. These should be reflexes before the test and are professional necessities after it.
- **Name the base aloud before dividing.** Out of which changes, which incidents, which quarter, which window? Base selection errors produce fluent, confident, wrong answers — the most dangerous kind at reporting level.
- **Aggregate only through raw counts.** Any question (or report) combining two percentages is testing whether you return to the underlying numbers first. Always do.
- **Watch for denominator effects.** Ratios recovered mid-period, rates on growing populations, utilisation over 100% — where the denominator moves, intuition fails and arithmetic must lead.
- **Respect boundaries exactly.** "Exceed", "at least", "25 or fewer": test wording is contractual, and so are your SLAs. 70 does not exceed 70; 25.6 is not 25.
- **Compound what compounds.** Percentage growth and reduction work on the current base, not the original. Step through the quarters explicitly rather than multiplying a linear guess.
- **Practise with your own reporting pack.** Recompute last quarter's headline figures from the raw data. It is ideal test preparation, and any discrepancy you find is worth more than the practice.

### Common pitfalls to avoid

- **Averaging percentages across unequal groups.** The unweighted mean is almost never right and always available as a distractor — in tests and in slide decks.
- **Conflating percentage points with percent.** A 3-point rise and a 3% rise are different claims; the failure-rate version of the same change can be a 37.5% story. Precision here is credibility.
- **Reading counts as rates.** The category with the most failures and the category with the worst failure rate are usually different. Check which the question — or the board — is actually asking about.
- **Misplacing the decimal in availability arithmetic.** Each "nine" moves the permitted downtime tenfold. Write the subtraction (100% − target) explicitly before multiplying.
- **Linear thinking about compound processes.** Reductions shrink their own base; recoveries dilute their own numerator. Step through the periods; do not extrapolate the first step.
- **Accepting the flattering computation.** Inverted utilisation, convenient bases, "about 25": when a result pleasingly supports the easy conclusion, recompute it before trusting it — the test plants these deliberately, and so does organisational life.
- **Presenting arithmetic without its sensitivity.** For business-case questions, the right answer often includes what the number depends on. Cultivate the habit; assessments at your level increasingly probe it, and boards always do.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret, and reason about the written material your role runs on: change and release policies, audit findings, major incident reviews, service standards, board papers, and correspondence from stakeholders at every level. The dominant question format presents a short passage and a statement, asking whether the statement is **True** (supported by the passage), **False** (contradicted by it), or **Cannot say** (the passage provides insufficient information either way). Complementary formats test inference, identification of unstated assumptions, recognition of a passage's main point, and judgement about clear, audience-appropriate writing.

The typical format is an online, timed test of 15 to 25 minutes with 15 to 30 questions. The governing discipline: answer from the passage alone. Your operational knowledge will frequently tell you that a statement is true in your organisation; if this passage does not establish it, the answer is "Cannot say". The test is measuring exactly that separation — between what a text states and what its reader imports — because that separation is where policy misreadings, audit disputes, and governance failures begin.

For a change and release manager, the stakes of precise reading are unusually concrete. The authority you exercise is written authority: what the policy delegates to you, what it reserves to the CAB, what an emergency provision permits and what it merely defers. The evidence you weigh is written evidence: an impact assessment's actual claims versus its hopeful implications, an incident review's established causes versus its plausible narrative. And the words you produce carry governance weight: authorisation records, deferral rationales, board reports, and the policy text itself — which others will read with exactly the literalness these tests train, especially when something has gone wrong and the question is what the process required. A manager who reads "should" as "must", or "reviewed" as "approved", does not merely lose test marks; they misstate their own authority.

At your level, expect the harder questions to turn on scope, modality, and attribution: who exactly a rule covers, how strong an obligation actually is, and whether a claim is the passage's assertion or a quoted party's opinion. These are the same three edges on which real policy arguments turn, which is why the practice below doubles as governance discipline.

### How this assessment maps to your role

The verbal skills tested map directly to the named skills in your capability framework:

- **Precise comprehension of policy and delegation** maps to your **Change management** skill and your authorisation duty: implementing change management processes — and improving them — begins with reading exactly what current process text requires, permits, and reserves, and for whom.
- **True/False/Cannot-say discipline** maps to your **Asset and configuration management** advocacy and your evidence-weighing duties: distinguishing verified fact from plausible assumption is the same act whether the object is a CMDB record, an audit assertion, or a statement in a test.
- **Inference and assumption identification** maps to your **Problem management** skill: incident reviews and trend analyses argue from evidence to causes and remedies; consulting specialists effectively and determining appropriate resolutions requires seeing which steps in those arguments are established and which are assumed.
- **Main-point and audience judgement** maps to your **Community collaboration** skill — adapting feedback so it is effective and lasting — and to your reporting duties: a board paper, a CAB decision note, and a message to a delivery team may describe the same event, but each succeeds only if written for its reader.
- **Reading user evidence accurately** maps to your **User focus** skill: using quantitative and qualitative data about users to turn user focus into outcomes depends on reading research findings for what they establish, at their stated scope, without inflation.
- **Reading standards vocabulary precisely** maps to your **Service focus** and **Continuity management** knowledge: coherent frameworks are built from must, should, and may used deliberately — and read the same way.

### Practice questions

For each True/False/Cannot-say question, judge the statement strictly against the passage.

**Passage 1 (for Questions 1–3)**

*Extract from the departmental change policy:* "The change and release manager may authorise normal changes assessed as Low or Medium risk. High-risk normal changes require authorisation by the Change Advisory Board, which is quorate when at least four voting members are present, including a representative of service operations. The change and release manager chairs the Board but does not hold a vote, except that in the event of a tied vote the chair holds the casting vote. Where a change affects services subject to the financial services code, the Board must additionally receive written risk acceptance from the relevant service owner before authorisation."

**Question 1 (easy) — True/False/Cannot say**

Statement: "The change and release manager may authorise a Medium-risk normal change without the Board."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage's first sentence grants exactly this: the change and release manager "may authorise normal changes assessed as Low or Medium risk". Nothing elsewhere qualifies the grant for ordinary cases — the financial-services condition attaches to Board authorisation of affected services, and the statement claims nothing about those. When a statement restates a granted permission at or below its stated scope, the answer is True. The professional mirror: fluency in your own delegation's exact boundaries is what lets you act quickly inside them and decline confidently outside them — and both speeds matter. Note also the reading habit the question rewards: you verified the claim against the operative sentence rather than against a general sense that "managers can approve things", which is precisely how policy should be cited in a dispute — by its words.

**Question 2 (easy) — True/False/Cannot say**

Statement: "The change and release manager votes on High-risk changes only when the Board's vote is tied."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage states the chair "does not hold a vote, except that in the event of a tied vote the chair holds the casting vote". The statement expresses the same rule from the other direction: no vote ordinarily, a vote only on a tie. Exception clauses reward double reading — a skimmer who catches "does not hold a vote" answers False; a skimmer who catches "holds the casting vote" answers True for the wrong reason, and would then misstate the rule in a real meeting. The full sentence, held together, is the rule. Governance texts are dense with exactly this structure (general rule, tail exception), and the chair who can quote their own casting-vote provision precisely — including its precondition — is the chair whose tied meetings end cleanly rather than contentiously. Read exceptions as part of the sentence they modify, never as separate facts.

**Question 3 (easy) — True/False/Cannot say**

Statement: "A Board meeting with five voting members present is quorate."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Quoracy has two conditions: "at least four voting members" and "including a representative of service operations". Five members satisfies the first condition — but the statement says nothing about whether service operations is represented among the five, and the passage cannot supply that fact. Since the meeting might or might not include the required representative, the statement is neither supported nor contradicted: Cannot say. This is the compound-condition trap in its purest form — a statement that satisfies the memorable numeric condition while remaining silent on the qualitative one — and it is worth noticing how naturally the mind treats "five is more than four" as settling the matter. Real quoracy disputes turn on exactly this: a well-attended meeting that lacked the mandated role. As chair, you own quoracy; counting heads is the easy half, and the checklist in your head should have both entries.

**Passage 2 (for Questions 4–5)**

*Extract from a major incident review:* "The incident began at 09:14 when the case management service became unresponsive. The service had received a database change the previous evening, authorised through the emergency route after a capacity alert. The review found that the change itself was implemented as specified. However, the post-implementation verification checked only that the database restarted successfully; it did not include the application-level checks specified in the service's runbook, which would likely have detected the misconfigured connection pool before business hours. The review also notes that this is the third incident in four months in which post-implementation verification was incomplete. The incident manager has stated her view that verification steps are routinely skipped when changes complete late at night."

**Question 4 (moderate) — True/False/Cannot say**

Statement: "The review established that verification steps are routinely skipped when changes complete late at night."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Track attribution — the question's entire cargo. The passage attributes the "routinely skipped" claim to the incident manager as "her view", stated to the review; the review itself establishes narrower facts: this verification was incomplete, and it is the third such case in four months. Three instances in four months is consistent with the incident manager's view but does not establish "routinely", and a stated view reported by a review is not a review finding. The statement claims the review established it — the passage neither supports that (it labels the claim as opinion) nor contradicts it (the review might have investigated further; the passage is silent). Cannot say. The distinction is anything but pedantic in your role: incident reviews are quoted in governance forums, and the difference between "the review found X" and "the incident manager believes X" determines what action the evidence licenses — a finding supports process change directly; a view supports investigating whether the view is correct. Managers who launder opinions into findings get faster agreement and worse decisions. When you write reviews, label the two ruthlessly; when you read them, track the labels.

**Question 5 (moderate) — Inference from the passage**

Based on Passage 2, which is the safest inference?

- A) The emergency change should not have been authorised.
- B) Had the runbook's application-level checks been performed, the misconfiguration would probably have been found before business hours.
- C) The database administrator was negligent.
- D) The emergency change caused the capacity alert.

**Correct answer: B**

**Explanation:** Option B restates, almost verbatim, what the review itself concluded with appropriate hedging: the runbook checks "would likely have detected the misconfigured connection pool before business hours". Adopting a passage's own carefully hedged causal claim, hedged to the same degree ("probably"), is the safest inference available — you are inferring nothing the text has not already weighed. Option A attacks the authorisation, but the passage supports the opposite lean: the change responded to a genuine capacity alert and "was implemented as specified" — the failure lay in verification, not authorisation, and conflating the two would misdirect the remedy. Option C names an individual and a culpability standard the passage never approaches; reviews that find process gaps ("verification was incomplete") are precisely not findings of personal negligence, and the three-in-four-months pattern points at systemic causes — late-night conditions, runbook usability, absent enforcement — rather than individual fault. Option D inverts the timeline: the alert preceded and prompted the change. The skill here is proportion: strong inference tracks the evidence's own weight and direction. In problem management terms, the passage hands you the actionable pattern (incomplete verification, recurring, with a hypothesised mechanism awaiting confirmation) — the correct next act is a preventative measure around verification completion, and perhaps a test of the incident manager's hypothesis, not a blame exercise or an authorisation clampdown.

**Question 6 (moderate) — Must, should, and may in a release standard**

Your release standard states: (i) "Releases to production **must** have a documented and tested back-out plan." (ii) "Releases **should** be deployed using the automated pipeline; teams deploying manually **must** record the justification in the change record." (iii) "Teams **may** bundle related low-risk changes into a single release." A team deployed manually with a tested, documented back-out plan, bundling three related low-risk changes, and recorded no justification for the manual deployment. Which requirements were breached?

- A) (i) and (ii)
- B) (ii) only — specifically its second clause
- C) (ii) and (iii)
- D) None — manual deployment is permitted, so no justification was needed

**Correct answer: B**

**Explanation:** Parse clause by clause. (i): back-out plan documented and tested — satisfied. (iii): bundling is a permission ("may"); using it breaches nothing. (ii) is the interesting clause because it is compound: a "should" (prefer the pipeline) followed by a conditional "must" (manual deployment triggers a mandatory justification record). The team's manual deployment is not itself a breach — "should" tolerates justified exceptions — but the missing justification record breaches the conditional must exactly. Option B. Option D's logic ("manual is permitted, so no justification needed") deletes the very mechanism that makes the permission safe: the standard permits deviation and prices it at one recorded justification, which is how a well-drafted should-clause keeps exceptions visible, auditable, and honest. This drafting pattern — recommendation plus mandatory record on deviation — is one you should recognise and reuse when you improve process text, because it outperforms both rigid musts (which get ignored under pressure, invisibly) and bare shoulds (which decay into optional). Reading modality precisely is the test's skill; drafting it deliberately is your role's — the two are one competence, examined from opposite sides.

**Question 7 (moderate) — Audience-appropriate writing**

A High-risk change was deferred by the CAB pending a revised impact assessment. You must now inform the delivery team's programme manager, who is not a technical specialist and is anxious about the date. Which message is best?

- A) "The Board resolved pursuant to paragraph 4.2 of the change policy that the submission be remitted to the originating team for elaboration of the impact assessment artefacts, whereafter resubmission may be entertained."
- B) "Your change was rejected because the impact assessment wasn't good enough. Resubmit when it meets the standard."
- C) "The Board deferred the change — it isn't rejected. We need one thing before approving it: the impact assessment doesn't yet cover the effect on the payments interface, and for a High-risk change we can't approve without that. If your team can add that analysis, we can take it at next Wednesday's Board — which still supports your go-live window. Sasha on my team can walk your analysts through what's needed."
- D) "Following rigorous multilateral risk-based deliberations, the change governance forum has determined that additional assurance artefacts are required to derisk the submission trajectory going forward."

**Correct answer: C**

**Explanation:** Measure each option against what this reader needs: the decision's actual meaning, the reason, the path forward, and the date implication — in plain language. Option C delivers all four and adds the two moves that distinguish governance communication from governance correspondence: it corrects the reader's worst fear explicitly ("deferred — not rejected", addressing the anxiety you know she has), and it converts the gap into a concrete, resourced next step (what is missing, why it is non-negotiable at this risk level, when the Board can retake it, who will help). Note that C is also the only option that preserves the date hope honestly — "still supports your go-live window" is information the anxious reader needs and the others withhold. Option A is legalese that transmits procedure instead of meaning; the reader learns a paragraph number and nothing about her date. Option B is accurate, brutal, and unhelpful in equal measure — "wasn't good enough" assigns failure without direction, and "rejected" is factually wrong in a way that maximises alarm. Option D is management fog: fifteen abstractions, zero information, and the fog is not neutral — vagueness from a governance body reads as evasion and breeds the resentment that gets change processes routed around. The pattern to keep: decision, reason, path, date, help — in the reader's vocabulary. Your community collaboration skill's phrase "adapt feedback to ensure it's effective and lasting" is a writing instruction as much as a coaching one, and deferral messages are where chairs earn either partners or adversaries.

**Passage 3 (for Questions 8–9)**

*Extract from a user research summary attached to a CAB submission:* "We interviewed 12 caseworkers and observed 8 processing sessions across two regional offices. Participants consistently described the current release communications as 'arriving too late to plan around'. Seven of the twelve interviewees said they had missed at least one release notice entirely in the past year. Observed workarounds included teams maintaining their own unofficial release calendars compiled from corridor conversations. We recommend release notices be published at least ten working days before implementation, and that a single authoritative release calendar be made available to service teams. We note our sample was drawn from the two offices with the highest caseloads, and results may not generalise to smaller sites."

**Question 8 (moderate) — True/False/Cannot say**

Statement: "A majority of the interviewed caseworkers reported missing at least one release notice in the past year."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Seven of twelve interviewees reported missing at least one notice; seven is a majority of twelve. The statement quantifies exactly what the passage quantifies, at the same scope — the interviewed caseworkers, not caseworkers generally — so it is True. Both restrictions matter and both are where near-miss versions of this statement would fail: "a majority of caseworkers miss release notices" (dropping the sample scope) would be Cannot say, especially given the passage's own caution that the high-caseload sample "may not generalise"; and "most caseworkers missed notices" as a present-tense general claim would inflate a twelve-person, one-year recall finding into an organisational fact. The research summary models the honesty the test rewards — it states its numbers, its scope, and its limits — and your user focus skill is the professional application: using data about users to turn user focus into outcomes requires carrying the data's limits along with its findings, because a CAB that hears "users miss notices" makes a different (and worse-calibrated) decision than one that hears "seven of twelve interviewed, in our two busiest offices". Precision is not hedging; it is the finding.

**Question 9 (challenging) — Identifying the unstated assumption**

The research's recommendation moves from "notices arrive too late to plan around" to "publish notices at least ten working days before implementation". Which unstated assumption does the recommendation most depend on?

- A) Ten working days is enough lead time for teams to plan around a release.
- B) Caseworkers dislike change communications in general.
- C) Smaller sites do not need release notices.
- D) The unofficial calendars are more accurate than official communications.

**Correct answer: A**

**Explanation:** The evidence establishes a problem of insufficient lead time; the recommendation prescribes a specific quantity of lead time. The bridge the argument crosses without stating is that the prescribed quantity solves the established problem — that ten working days is actually enough for the planning caseworkers need to do. Nothing in the findings derives the number: no interviewee is quoted specifying a sufficient horizon, no observed workflow is timed. If planning around a release genuinely requires four weeks (rota cycles, training bookings), the recommendation could be implemented perfectly and the complaint would survive intact. Option A names this dependency. Option B contradicts the evidence's texture — caseworkers who build unofficial calendars from corridor conversations are demonstrating demand for release information, not aversion. Option C misreads the generalisation caveat, which limits what the sample supports rather than claiming smaller sites differ. Option D is a distractor about a detail: the workarounds evidence unmet need; their accuracy is beside the argument. The chairing application is direct: recommendations arriving at your Board frequently contain exactly this structure — evidenced problem, specific remedy, unexamined bridge — and the highest-value question a chair asks is the bridge question: "what tells us ten days is the right number?" Often the honest answer is "it is a defensible starting point, to be validated" — which is fine, and materially different from "the research established it". Your user focus skill's phrase "understand and define research that fits user needs" includes noticing when the research stops and the assumption begins.

**Question 10 (challenging) — Reconciling policy with an audit finding**

Document 1, the change policy: "Emergency changes must be reviewed retrospectively at the next CAB meeting following implementation." Document 2, an internal audit report: "Of 24 emergency changes sampled from the past year, 21 were recorded as reviewed at a subsequent CAB. In 9 of those 21 cases, the review occurred two or more CAB meetings after implementation. Three changes had no recorded review." Which statement do the two documents, taken together, best support?

- A) The retrospective review requirement was met in 21 of 24 sampled cases.
- B) The requirement was fully met in at most 12 of the 24 sampled cases, since reviews later than the next meeting do not satisfy "at the next CAB meeting", and three had no review at all.
- C) The policy's review requirement is impractical and should be relaxed.
- D) The nine late reviews were caused by CAB agenda overload.

**Correct answer: B**

**Explanation:** The reconciliation turns on reading the policy's requirement at its actual strictness. "Reviewed retrospectively at the next CAB meeting" is a deadline, not merely an event: a review occurring two or more meetings later happened, but did not happen when the policy requires. Now count against that standard: 24 sampled; 3 never reviewed — clear breaches; 9 reviewed two or more meetings late — breaches of the timing requirement; leaving 12 whose reviews were not identified as late. Whether all 12 truly met the "next meeting" deadline the audit does not explicitly confirm — it reports lateness where found, not punctuality where not — so the defensible ceiling is "at most 12 of 24 fully compliant", which is exactly how option B phrases it. Option A is the audit-reading error the question is built around: it adopts "reviewed at a subsequent CAB" — the audit's deliberately looser recording category — as if it satisfied the policy's stricter "next CAB" requirement, a substitution of the measured proxy for the actual rule. Options C and D leap past the evidence: C to a policy recommendation the documents nowhere argue (widespread breach might equally indicate an enforcement or scheduling fix), and D to a cause the audit never investigates. The professional core: compliance counting must use the rule's own wording as the measuring stick, and audits often measure what is recordable rather than what the rule requires — the gap between those two is where a chair reading their own compliance figures needs to look first. "21 of 24 reviewed" and "at most 12 of 24 compliant" are both true sentences about the same year; only one of them answers the governance question.

**Question 11 (challenging) — Main point of a passage**

*Extract from a service management board paper:* "Change volume has doubled in eighteen months as legacy services migrate to continuous delivery practices. The change process, designed for a monthly release rhythm, now processes daily submissions through weekly governance. Success rates remain high at 96%, but authorisation lead time has become the top complaint in delivery team surveys, and two programmes have documented instances of batching unrelated changes into single submissions to reduce governance overhead — a practice that increases the blast radius of any failure. We propose a differentiated model: automated pre-authorisation for changes meeting defined low-risk criteria with full audit logging, retained board scrutiny for high-risk changes, and quarterly review of the criteria themselves against outcome data. The alternative — scaling the current process by adding meetings — addresses throughput but not the underlying mismatch between governance rhythm and delivery rhythm."

Which sentence best expresses the paper's main point?

- A) Change success rates remain high, so the current process is working and complaints about lead time are secondary.
- B) Delivery teams are behaving badly by batching changes and should be corrected.
- C) The change process's rhythm no longer matches the delivery rhythm it governs, and the remedy is risk-differentiated governance rather than more of the current governance.
- D) Continuous delivery practices are incompatible with change governance.

**Correct answer: C**

**Explanation:** The paper's architecture: cause (delivery rhythm transformed), symptom set (lead-time complaints, and batching — presented as a rational response to overhead that worsens risk, not as misconduct), the trap reading dismissed (high success rate as evidence of health), the proposal (differentiated model with its three components), and the explicit rejection of the scaling alternative for a stated reason ("addresses throughput but not the underlying mismatch"). Option C captures the diagnosis-plus-remedy spine, including the crucial "rather than more of the same" clause that the paper's final sentence exists to establish. Option A adopts precisely the reading the paper pre-empts: the 96% success rate is real, but the paper positions it as the number that hides the problem — governance can succeed at every individual decision while failing as a system, and the batching evidence shows risk being manufactured by the process's own friction. Option B moralises what the paper analyses; note the diagnostic sophistication worth stealing — when teams route around governance, the paper reads the routing as data about the governance, which is exactly the posture your change management skill's "actively improving and optimising" requires. Option D overshoots into a claim the paper's own proposal refutes: differentiated governance is the compatibility mechanism. Main-point questions at this level test whether you can hold a document's full argumentative shape — including what it argues against — and that is also the skill of writing board papers whose main point cannot be honestly misquoted: the paper's pre-emption of the success-rate misreading is the model. Papers that anticipate their misreadings survive their board meetings.

**Question 12 (challenging) — True/False/Cannot say with layered scope**

*Passage:* "Under the revised framework, all High-risk changes to Gold-tier services require a completed service continuity impact statement before CAB submission. Since the framework's introduction in April, every High-risk change submitted to the CAB has included the statement. Two High-risk changes to Gold-tier services were implemented in May through the emergency route."

Statement: "Since April, every implemented High-risk change to a Gold-tier service has had a completed service continuity impact statement."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Map the coverage of each sentence against the statement's claim. The rule attaches the statement requirement to CAB submission of High-risk Gold-tier changes. The compliance report covers changes "submitted to the CAB" — every one included the statement. But the third sentence introduces two High-risk Gold-tier changes implemented through the emergency route, and the emergency route, on this passage's evidence, may not involve CAB submission at all (the passage does not describe its requirements). Did those two changes have continuity impact statements? The rule as quoted binds submission to the CAB; the report as quoted covers CAB submissions; the two emergency changes fall — on the passage's information — outside both sentences' coverage. The statement claims universal coverage of implemented changes; the passage supports it only for the submitted ones and is silent on the emergency pair. Neither supported nor contradicted: Cannot say. The construction is worth naming because it is the most important verbal pattern at governance level: a rule scoped to a route, a compliance measure scoped to the same route, and a second route through which the same class of change travels unmeasured. Real assurance gaps live in exactly this shape — "100% compliance" statistics that are true of the monitored path while the unmonitored path carries the risk. As the owner of both routes, the question this passage should trigger in you operationally is the one the test rewards you for noticing logically: what does the emergency route require, and who checks? A chair who reads compliance reports with route-scope in mind audits the gap before the auditor does.

### Preparation tips

- **Track attribution as you read.** Mark (mentally or literally) whether each claim belongs to the passage's author, a review's findings, or a quoted individual's view. Most hard True/False/Cannot-say items at this level turn on who said it, not what was said.
- **Read exceptions as part of their sentence.** General rule plus tail exception is the standard structure of governance text. Practise restating such rules from both directions until the full rule is what you remember.
- **Check compound conditions completely.** Quoracy, authorisation, and compliance requirements typically have a numeric condition and a qualitative one. Statements satisfying only the memorable half are the test's favourite trap and governance's favourite dispute.
- **Hold scope constant.** Sample versus population, submitted versus implemented, monitored route versus all routes, past finding versus present claim. Before answering, ask: does the statement's scope match the passage's?
- **Interrogate recommendation bridges.** When a text moves from evidence to a specific remedy, locate the unstated step. It is usually a quantity, mechanism, or causal claim the evidence never established.
- **Practise on your own governance corpus.** Your change policy, recent audit findings, and incident reviews are ideal material — and reading them with test-grade literalness routinely surfaces real ambiguities worth fixing in the text you own.
- **Write your practice answers' justifications.** For each True/False/Cannot-say, note the exact words that decide it. If you cannot point to the words, your answer is a guess wearing confidence.

### Common pitfalls to avoid

- **Importing operational knowledge.** You know how CABs, emergency routes, and audits actually work; the passage may not say. Answer the text, not your experience — the test is measuring exactly that separation.
- **Laundering views into findings.** "The incident manager believes" is not "the review found". The conflation fails test questions and, worse, misdirects real remediation.
- **Treating the measured proxy as the rule.** "Reviewed at a subsequent CAB" versus "reviewed at the next CAB": compliance language often quietly loosens the requirement it reports against. Measure with the rule's own words.
- **Reading modality loosely.** Must, should, may, and conditional musts distribute obligation deliberately. Both misreadings — hardening shoulds and softening musts — misstate authority, in tests and in post-incident arguments.
- **Accepting universal claims from route-scoped evidence.** "Every submitted change complied" cannot support "every implemented change complied" while a second route exists. Hunt the unmonitored path.
- **Answering the passage you expected.** Familiar formats (incident review, audit finding, board paper) invite skimming into assumption. The test places its discriminating details precisely where fluent readers stop reading.
- **Losing the argument's shape in its details.** For main-point questions, ask what the author wants the reader to conclude and do — including what the text explicitly argues against. The striking statistic is rarely the point; sometimes it is the decoy.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks you to identify the most effective response — or sometimes the least effective, or a rating or ranking of all the options. It contains no calculations and no passages; it measures professional judgement: how you weigh service risk against delivery pressure, when you hold a decision and when you escalate or delegate it, how you handle seniority, conflict, error, and your own accountability, and how you develop the people and processes around you.

The typical format is an online assessment of 20 to 40 minutes with 10 to 20 scenarios, usually untimed or generously timed. Options are engineered: alongside the strongest response you will typically find a near-miss that skips one essential element, an avoidance option dressed as diplomacy, and an overreaction dressed as decisiveness. Scoring is keyed by experienced practitioners and calibrated to level — which, at yours, means something specific: the scored behaviours include exercising authority you genuinely hold (not deferring decisions that are yours), owning issues until resolved or properly handed over, protecting governance under pressure from above as well as below, and improving systems rather than just resolving instances. The lone-hero answer still scores poorly, but so now does the over-escalation answer: your role is the escalation point, and sending upward what you exist to decide reads as abdication.

Why do employers assess situational judgement for this role with particular care? Because your failure modes are behavioural, not technical. A change and release manager who folds under a director's deadline pressure, or who applies process rigidly until delivery teams route around it, or who chairs a CAB where only the loudest voices shape risk decisions, or who quietly reallocates blame after a failure — each defect can coexist with excellent technical knowledge, and each corrodes exactly what the role exists to protect: the organisation's ability to change safely and quickly at once. The scenarios below rehearse these pressure points deliberately. They are drawn from the recognisable life of the role: the pre-CAB corridor conversation, the 2am back-out call, the report your own manager wants softened, the team that has discovered the emergency route is easier than planning.

Approach the practice honestly — answer as you believe you would act, then test yourself against the reasoning. Situational judgement improves through exactly this loop: rehearsal, comparison, reflection. Every scenario here is one you may genuinely meet; meeting it first on paper, with time to think and a worked rationale to argue with, is the cheapest preparation you will ever get.

### How this assessment maps to your role

The judgement dimensions map directly to the named skills in your capability framework:

- **Decision ownership under pressure** maps to your role as decision-maker for all technical changes and escalation point, and to your **Ownership and topic** skill: owning an issue until it is resolved, mitigated, or properly transferred — including when the pressure to shortcut comes from above.
- **Risk-proportionate governance behaviour** maps to your **Change management** skill: implementing processes is the floor; the scored behaviour is running them so that rigour lands where risk lives, and improving them when teams' workarounds reveal friction.
- **Incident and problem judgement** maps to your **Incident management** and **Problem management** skills: diagnosing and prioritising under uncertainty, consulting specialists effectively, choosing resolutions, and converting recurring patterns into preventative measures rather than recurring heroics.
- **Developing people and teams** maps to your **Community collaboration** skill: adapting feedback so it is effective and lasting, identifying problems in team dynamics and rectifying them, and using mechanisms like Agile health checks to surface what teams will not volunteer.
- **Chairing and inclusion** maps to the same skill applied to the board you lead: a CAB's risk judgement is only as good as the range of voices that actually shape it, and the chair owns that range.
- **Serving users through governance** maps to your **User focus** and **Service focus** skills: remembering that behind every deferral, freeze exception, and window negotiation are users whose services the process exists to protect — and building frameworks coherent enough that protection and delivery stop being rivals.

### Practice questions

**Question 1 (easy) — The corridor authorisation**

An hour before the CAB, a programme director intercepts you: "The migration change on today's agenda — I need it approved. The programme board meets tomorrow and I want to report it green. The impact assessment's a bit thin, I know, but my team knows this system inside out. Can we just call it approved and tidy the paperwork after?" The change is High-risk and the impact assessment omits the downstream effects on two dependent services. What is the most effective response?

- A) Agree — the director carries the delivery accountability, and their team's expertise is genuine.
- B) Explain that High-risk changes are authorised by the CAB and this one will be, today, on its merits — the thin assessment is the obstacle, so offer the fastest legitimate route: their team supplies the missing dependency analysis before the meeting, or the Board conditions approval on it being completed before implementation.
- C) Refuse to discuss changes outside the CAB and end the conversation.
- D) Take the change off today's agenda to avoid the pressure influencing the Board.

**Correct answer: B**

**Explanation:** Locate the actual conflict before choosing a posture: the director does not need a corridor approval — they need a green status by tomorrow, and a legitimate path to it may well exist. Option B holds the constitutional line without theatre (High-risk authorisation belongs to the Board; a chair cannot "call it approved", and saying so plainly is not confrontation, it is orientation) and then does the chair's real work: converting pressure into process. The missing dependency analysis might be producible in an hour by a team that "knows the system inside out"; alternatively, conditional approval — a standard governance instrument — lets the Board authorise with the gap explicitly fenced. Either route gives the director something true to report tomorrow. Option A dissolves the CAB's purpose at the first application of seniority, and "tidy the paperwork after" converts a governance record into a fiction — note that accountability does not transfer the way the director implies: an unassessed dependency failure will land on the services and their users, and on the authorisation record with your name on it. Option C wins the exchange and loses the relationship — refusing to even hear a stakeholder teaches senior people that the change process is a wall, and walls get routed around at exactly your level of visibility. Option D punishes the change for its sponsor's behaviour, delaying delivery to protect a Board that does not need protecting — chairs manage pressure; they do not flee it. The scored pattern: name the boundary once, then spend your energy on the legitimate fastest path.

**Question 2 (easy) — The disengaged Board member**

The service operations representative on your CAB — whose presence is required for quoracy — has for a month joined late, kept their camera off, visibly multitasked, and voted with the majority on every item without comment. Operations context has been missing from several risk discussions as a result. What is the most effective response?

- A) Speak with them privately: share what you have observed, ask what is competing for their time, and make the case for what the Board loses without operations' voice — exploring fixes, whether that is agenda timing, sharper operations-relevant papers, or a properly briefed alternate.
- B) Raise their disengagement at the next CAB so the whole Board can address it.
- C) Ask their line manager to nominate someone more committed.
- D) Accept it — quoracy is technically satisfied, and their vote is recorded.

**Correct answer: A**

**Explanation:** Diagnose before escalating: month-long disengagement from a previously functioning member usually has a cause — workload collision, meetings that waste their time, papers written for developers rather than operators, or a belief that the Board ignores operations anyway. Option A goes to the source privately, leads with observation rather than accusation, and treats the disengagement as a solvable design problem, which it often is: if every operations-relevant item sits at the meeting's end, or the papers bury operational impact on page nine, the fix is yours to make. The conversation also carries the necessary steel — the Board needs the voice, not just the vote — while offering face-saving routes (including a briefed alternate, which honours the role while acknowledging the person's constraints). Option B converts a private performance issue into public shaming; whatever it wins in acknowledgement it loses in the member's future candour, and boards remember how their chair treats members. Option C escalates over the person's head before speaking to the person — the conversation their manager will rightly ask whether you had. Option D is the trap the scenario is built on: quoracy is the constitutional minimum, not the purpose; a required representative voting silently with the majority satisfies the letter of governance while deleting its substance — operations context is precisely the risk information High-risk decisions need, and its absence "from several risk discussions" is already a cost, not a future one. Chairs own the difference between a quorate meeting and a functioning one. Your community collaboration skill names this directly: identify problems in team dynamics and rectify them — the CAB is one of your teams.

**Question 3 (easy) — The sanitised failure review**

A change failed last week, causing a two-hour outage. Reading the delivery team's post-implementation review before it reaches the CAB, you notice it attributes the failure entirely to "an unforeseeable infrastructure fault" — but the incident timeline you own shows the team received a failing pre-deployment health check and proceeded anyway. What is the most effective response?

- A) Accept the review — the team is otherwise strong, and one generous review preserves the relationship for future candour.
- B) Annotate the review with the health-check evidence yourself and circulate the corrected version to the CAB.
- C) Go back to the team's lead with the timeline evidence, ask them to reconcile the review with it, and be clear the review that reaches the Board must account for the health-check decision — while signalling that the Board's interest is the decision process, not punishment.
- D) Present both versions to the CAB and let the Board decide which to believe.

**Correct answer: C**

**Explanation:** Two duties collide here — record integrity and team relationships — and option C is the move that serves both, in the right order. The review cannot stand: a governance record attributing a failure to bad luck when evidence shows a risk signal was overridden will corrupt every downstream use of it — the failure statistics, the lessons register, the Board's calibration of this team's future submissions. But the correction should come from the team, prompted by evidence, not imposed by the chair: going back to the lead gives them the chance to fix their own record (there may also be context you lack — perhaps the health check was a known false positive, which changes the story again and is itself worth documenting), and the explicit framing — the Board wants the decision process examined, not people punished — is what makes honesty affordable. This matters beyond the instance: teams write sanitised reviews when they believe accurate ones are career events; every interaction that proves otherwise is an investment in the next review's candour. Option A inverts that logic — accepting a fiction to preserve "future candour" purchases the opposite, teaching the team that reviews are negotiable and their chair is manageable. Option B gets the facts right and the ownership wrong: a review corrected over its authors' heads arrives at the Board with the team blindsided and adversarial, and you may have annotated in a context gap. Option D outsources to the Board a reconciliation that is precisely the chair's preparatory job — boards adjudicate risk, not competing narratives their chair could have resolved with one conversation. Sequence is the skill: evidence to the team first, corrected record to the Board second, and the escalation path remains available if the team refuses — which is a different, rarer scenario.

**Question 4 (moderate) — The emergency route regulars**

Your monthly data shows one delivery team now raises 60% of its changes through the emergency route, against an organisational average of 5%. Sampling their recent emergency changes, you find most cite deadlines rather than incidents or urgent risk: the route is being used to skip the forward schedule. The team's head is influential and their programme is genuinely under delivery pressure. What is the most effective response?

- A) Reject their next several emergency changes to send a clear signal.
- B) Tighten the emergency criteria and require your personal pre-approval for all emergency changes organisation-wide.
- C) Take the data to the team's head as a shared problem: show the pattern, distinguish genuine emergencies from deadline pressure, understand why the normal route is failing them — then fix both sides, agreeing what qualifies as an emergency while addressing whatever lead-time or scheduling friction is driving the workaround.
- D) Report the team's non-compliance to the service management board with a recommendation for formal censure.

**Correct answer: C**

**Explanation:** Read the 60% as information before treating it as violation: a twelvefold deviation from the organisational average is rarely pure delinquency — it is usually a genuine delivery constraint colliding with a process that is not serving it, and the emergency route relieving the pressure the normal route should have absorbed. Option C investigates and fixes both sides, which is the only durable resolution: the conversation opens with data (unarguable, unaccusatory), separates the legitimate emergencies from the deadline-driven ones, and asks the question a process owner should always ask of a workaround — what is the normal route costing this team that the emergency route saves? If authorisation lead time genuinely cannot fit their delivery cadence, the fix may be scheduling adjustments, standard-change templates for their recurring changes, or submission planning support; in exchange, the emergency criteria get re-agreed and enforced with the head's buy-in, which is what makes enforcement stick. Option A punishes changes rather than behaviour — rejecting a genuine emergency to make a point would put services at risk for pedagogy, and the team's head would be right to escalate it. Option B is the classic over-correction: it taxes every compliant team organisation-wide to discipline one team, inserts you as a bottleneck into the very route designed for speed, and still does not address why the workaround exists. Option D reaches for formal machinery before the direct conversation — with an influential head, arriving with data and a partnership frame will usually get you an ally; arriving via a censure recommendation guarantees an adversary, and the board will ask whether you spoke to them first. The deep pattern, which your change management skill's "actively improving and optimising" encodes: workarounds are user research about your process. Teams tell you where governance fails them by where they route around it; the managers who listen to that signal end up with processes teams defend rather than dodge.

**Question 5 (moderate) — Two service owners, one window**

The payments service owner and the case management service owner both require the final release window before the financial year end — payments for a regulatory compliance change with a fixed statutory date, case management for a performance improvement their users have been promised, backed by a director. Both have escalated to you, separately, each insisting their release cannot move. The window genuinely cannot hold both. What is the most effective response?

- A) Award the window to payments — regulatory deadlines outrank performance improvements — and inform case management of the decision.
- B) Convene both owners, make the decision criteria explicit (statutory obligation versus deferrable benefit, and the cost of each delay), test whether the constraint itself can move — an additional window, a smaller case management release, an earlier partial deployment — and if not, decide for payments transparently, with case management's release protected in the first available window and the rationale recorded.
- C) Escalate the conflict to the two owners' common director for a decision.
- D) Give the window to whichever release was scheduled first, as a neutral rule.

**Correct answer: B**

**Explanation:** The substantive ranking is not the test — options A and B agree that a statutory date beats a promised improvement, and any defensible framework says so. The test is decision craft: how the ranking is reached and delivered determines whether the loser accepts it, and whether the next conflict arrives as a negotiation or an ambush. Option B does four things option A skips. It decides in the open, with both parties hearing the same criteria — which converts the outcome from "the chair favoured payments" into "the framework favoured the statutory date", a distinction that preserves your neutrality for every future conflict. It attacks the constraint before accepting the trade-off: coordinators who ask "must this be either/or?" find, some meaningful fraction of the time, that an extra window, a split release, or a descoped deployment dissolves the conflict entirely — and even when the answer is no, case management has watched you try. It prices the loss and schedules the remedy: "first available window, recorded rationale" turns a defeat into a deferral with a date, which is what the owner must now carry to their director — and a written rationale is precisely what they need for that conversation. And it keeps the decision where it belongs: coordinating releases and their interdependencies is your role's explicit duty; option C exports a decision you are equipped and mandated to make, teaching both owners that escalating past you works — the escalation point escalating is an abdication with a long tail. Option D is neutrality as abdication: "first come, first served" is indifferent to consequence, and a scheduling accident is not a reason a statutory obligation should wait. Note finally what B protects that no other option even considers: the users behind both releases — the framework decides, but the craft ensures both services' users get their outcome at the least total cost. That is service focus exercised through a calendar.

**Question 6 (moderate) — Your delegate's error**

You have delegated Medium-risk authorisations to a capable senior analyst while you cover a vacancy. Reviewing the week's decisions, you find they authorised a change that policy required them to refer upward: it touched a financial-code service, which caps delegated authority at Low risk. The change was implemented — successfully — three days ago. The analyst clearly did not notice the financial-code flag. What is the most effective response?

- A) Since the change succeeded, note it privately and sharpen the delegation letter for the future.
- B) Withdraw the delegation — the analyst has shown they cannot be trusted with it yet.
- C) Record the authorisation breach honestly, walk through it with the analyst as a learning review — establishing why the flag was missed — and fix the system gap that let one person's oversight become an implemented change, such as an automatic financial-code check in the tooling; retain the delegation with the added safeguard, and report the exception through your own line transparently.
- D) Have the analyst self-report to the audit team to underline the seriousness.

**Correct answer: C**

**Explanation:** Separate the three questions the scenario braids together: what happened (a genuine authorisation breach — success is irrelevant to that classification, and option A's "no harm, no record" quietly teaches your governance that outcomes launder process), who failed (partly the analyst, who missed a flag; but interrogate the miss — was the flag prominent in the tooling, or buried in a service attribute three clicks deep? A capable person missing a control usually indicts the control's design as much as the person), and what prevents recurrence (this is where option C earns its keep: an automatic check that blocks or routes financial-code changes converts a human vigilance requirement into a system property, which is the only fix that scales past this analyst to every future delegate). C also handles the two relationships correctly. With the analyst: a learning review of a self-evident miss, conducted without humiliation, is how capable people convert errors into reliability — and retaining the delegation with a safeguard added tells them the error was survivable and the trust is real, which is what makes your future delegations mean something. With your own line: the exception report is non-negotiable, because the delegation was yours, the accountability for its exercise remains yours, and a breach your manager learns about from an auditor rather than from you converts a process exception into a trust incident. Option B punishes one miss with the maximum sanction, losing the capacity the delegation existed to provide and teaching everyone watching that working under delegation is career-hazardous. Option D performs seriousness instead of achieving it — self-reporting to audit is theatre that outsources to a third party the honest recording and system fix that are yours to do. The delegation lesson worth engraving: you can delegate authority, never accountability — and the practical meaning of that phrase is exactly C's shape: honest record, developmental correction, systemic fix, upward transparency.

**Question 7 (moderate) — The 02:40 back-out call**

You are woken at 02:40. A release to the document service completed at 01:30; since 02:15, intermittent errors have affected roughly 15% of transactions. The incident manager wants your decision: back out now, or hold. The back-out is tested but takes ninety minutes, meaning it must start by 05:30 to finish before the 07:00 business day. The on-call engineer suspects a cache warming issue that would resolve itself by roughly 04:00 but cannot yet prove it. The service is Silver-tier; the morning brings its daily peak. What is the most effective response?

- A) Order the back-out immediately — with users affected, reversal is always the safe default.
- B) Hold until the engineer is certain of the diagnosis, whenever that is.
- C) Set a decision gate: hold while the engineer works to confirm the cache hypothesis, define what evidence would confirm or kill it, and pre-agree that if errors persist or worsen by a set time — comfortably before the 05:30 back-out deadline, say 04:15 — the back-out proceeds without further debate; brief the incident manager on the gate and stay engaged until resolution or handover.
- D) Delegate the decision to the on-call engineer, who has the most technical context.

**Correct answer: C**

**Explanation:** The scenario hands you a decision under genuine uncertainty with an expiring option, and the scored skill is recognising that you do not have to choose between deciding now and deciding well — you can decide the decision rule now. Work the timeline: back-out must start by 05:30; the hypothesis predicts self-resolution by 04:00; therefore a gate at ~04:15 buys the hypothesis its full window while preserving a 75-minute margin on the reversal option. If the engineer is right, you avoid a ninety-minute back-out (itself a change, with its own failure modes) and the morning peak meets a healthy service; if wrong, the back-out completes before business hours with room to spare. Option C also does the quieter things senior incident judgement requires: it defines evidence in advance (what would confirm or kill the hypothesis), which prevents 04:15 becoming a fresh debate conducted by exhausted people; it keeps the incident manager commanding the incident while you own the change decision — the correct division of an incident's labour; and it holds your engagement until resolution or explicit handover, which is your ownership skill's literal wording. Option A buys certainty it does not need to afford yet — with 15% intermittent errors on a Silver service at 02:40, three hours from peak, the option value of forty minutes of diagnosis is high and its cost is low; "always reverse" is a slogan, not a judgement. Option B is the mirror error: "until certain, whenever that is" surrenders the timeline to the diagnosis, and certainty arriving at 05:45 is certainty arrived too late — uncertainty does not suspend deadlines. Option D confuses input with ownership: the engineer's technical context is essential and their hypothesis is driving your gate, but the back-out decision weighs business exposure, peak timing, and reversal risk across concerns no on-call engineer holds — and 02:40 delegation of an expiring decision reads, correctly, as the escalation point declining to be one. Decisions for all technical changes is your role's sentence; at 02:40 it has no asterisk.

**Question 8 (moderate) — The resisted improvement**

You are introducing a requirement that production deployments run through the automated pipeline, replacing manual deployment for the services that still use it. The longest-tenured engineering team resists: their lead argues their manual process "has not caused an incident in four years", the pipeline does not yet handle two of their edge cases, and the requirement reads as distrust of the team most experienced in the estate. Adoption elsewhere is going well. What is the most effective response?

- A) Grant the team a permanent exemption in recognition of their record.
- B) Enforce the deadline uniformly — exceptions unravel standards, and their objections are ultimately about status.
- C) Engage the substance and the sentiment separately: commission the two edge cases into the pipeline's backlog with the team's own engineers involved in specifying them, agree a dated transition tied to those fixes landing, and reframe the requirement's rationale — the pipeline is about institutional resilience (auditability, repeatability, and safety that survives any individual's absence), not about this team's competence.
- D) Ask the service management board to impose the requirement so the resistance attaches to the mandate rather than to you.

**Correct answer: C**

**Explanation:** Take the objections apart, because they are of different kinds and deserve different answers — that decomposition is the whole skill. The edge cases are a substantive, checkable claim: if the pipeline genuinely cannot handle their deployments, the requirement as applied to them is currently an instruction to break production, and enforcing it (option B) would either force non-compliance or cause the incident the pipeline exists to prevent. C's move — their engineers specify the fixes, the transition dates to the fixes landing — converts opponents into contributors and makes the deadline something the team helped construct, which is where durable adoption comes from. The four-year record is real but answers the wrong question: manual deployment's risk is not only incident frequency but institutional fragility — undocumented steps, key-person dependency, unauditability — and naming that honestly ("this would be required even if your record were perfect, because of what it makes survivable") is what detaches the requirement from the insult reading. Which leaves the sentiment, and it matters: your community collaboration skill's "adapt feedback to ensure it's effective and lasting" applies to process feedback too — a change experienced as distrust will be complied with minimally and gamed quietly; the reframe, delivered credibly, is not soft-soap but the difference between adoption and compliance theatre. Option A trades the standard away entirely: a permanent exemption for the most senior team announces that seniority buys out of governance, and every other team notices the price. Option B wins the mandate and loses the estate's most experienced engineers — and is factually reckless about the edge cases. Option D borrows authority you already hold and spends the board's; resistance does not attach to mandates, it attaches to whoever the team must actually deal with — still you — minus the respect the direct engagement would have earned. Improvement work at your level is mostly this: separating the objection that improves your rollout from the emotion that resists it, and answering both.

**Question 9 (challenging) — The failure you authorised**

Three weeks ago you personally authorised a Medium-risk change under your delegated authority, judging its assessment adequate. The change contained a defect that yesterday caused the department's most visible outage of the year. Preparing the post-incident review for the service management board, you can see the assessment you approved missed a dependency that a more searching review might have caught — though the assessment met the documented standard at the time. A colleague advises: "Present it as the delivery team's assessment failure — technically true, and no one will read it differently." What is the most effective response?

- A) Follow the advice — the assessment was the team's product, and the documented standard was met; your authorisation was procedurally sound.
- B) Present the full chain including your own authorisation judgement: the assessment met the documented standard, the standard itself does not require the dependency analysis that would have caught this, your approval applied the standard as written — and therefore the remedial action is strengthening the standard (and its authorisation checklist), which you propose, with dates.
- C) Present the team's assessment failure but privately acknowledge your role to your own manager.
- D) Preface the review with a personal apology and offer to return your delegated authority pending the board's confidence.

**Correct answer: B**

**Explanation:** The colleague's advice contains its own refutation: "technically true, and no one will read it differently" is a precise description of a misleading account — one whose literal components are defensible and whose received meaning is false. Option B declines it not merely on ethics but on analysis, and the analysis is the senior skill here. Walk the causal chain as B presents it: the team produced an assessment meeting the documented standard; the standard does not mandate the dependency analysis that would have caught the defect; the authoriser applied the standard as written. Read honestly, that chain locates the systemic failure in the standard — which is both the truthful account and the only account that generates the right fix. The blame-shifted version (options A and C) does not just wrong the team; it misdirects the remedy — a board told "the team's assessment failed" will prescribe assessment training for a team that followed the rules, and the standard's gap survives to cause the next outage. That is the deepest reason honest reviews outperform protective ones: reviews are steering inputs, and a steered-by-fiction process fails again. B's inclusion of your own judgement in the chain, without theatrical self-flagellation, is calibrated accountability — "my approval applied the standard as written" is a fact the board needs, stated by the person who owns it, arriving with the fix attached and dated. Option C is the quiet version of A: the board — the body actually steering the process — still receives the misdirecting account; a private aside to your manager launders your conscience, not the record. Option D overcorrects into a different error: surrendering delegated authority over a defect the standard invited converts systemic learning into personal drama, invites the board to treat a process gap as a competence question, and — notice — still fails to propose the standard's fix, which is the review's actual job. The mature position, worth carrying beyond any test: when the process you own fails, the account you give is itself an exercise of the role — accurate about the chain, explicit about your link in it, and pointed at the fix. Boards trust managers whose failure accounts read like engineering; they replace managers whose accounts read like advocacy.

**Question 10 (challenging) — The Board that agrees too quickly**

Reflecting on six months of CAB minutes, you notice a pattern: decisions are unanimous almost without exception, discussion averages under three minutes per item, dissent — when it occurs at all — comes from the same two senior members, and the three junior members (including the security representative, the only woman on the Board) have not initiated a challenge in the entire period. Outcomes have been acceptable, but two recent near-misses involved risks that a security or operations challenge should plausibly have caught. What is the most effective response?

- A) Leave it alone — outcomes are acceptable, unanimity is efficient, and manufactured dissent wastes senior time.
- B) Redesign how the Board reaches decisions so that challenge is structural rather than temperamental: for High-risk items, ask named perspectives (security, operations) for their view before opening general discussion and before any senior member speaks; introduce a rotating "risk challenge" role charged with arguing the case against; and speak privately with the quieter members about what would make challenge feel safe and expected — while examining your own chairing for signals that dissent is unwelcome.
- C) Tell the Board plainly that unanimity has become a problem and you expect more disagreement.
- D) Replace one of the junior members with someone more assertive.

**Correct answer: B**

**Explanation:** The scenario describes a board whose social dynamics have quietly disabled its function — risk scrutiny — while its metrics stay green, and the near-misses are the early invoice. Diagnose the mechanism before choosing the fix: three-minute unanimity with dissent monopolised by two senior voices is not evidence that everyone agrees; it is evidence that the discussion order and status gradient decide items before junior perspectives enter — once two seniors have spoken for approval, a junior security representative challenging costs social capital she has watched no one else spend. That diagnosis is why options C and D fail even though they "act": C demands a behaviour while leaving intact the structure that punishes it — exhortation against a gradient loses to the gradient, and the meeting after the speech will be unanimous again; D personalises a systemic problem, and note whom it selects for replacement — a junior woman is deemed insufficiently assertive by a process that never gave her a safe opening; the next appointee inherits the same silencing structure. Option B changes the structure itself, and each element targets the mechanism: speaking order inversion (named perspectives before seniors, before general discussion) removes the pre-decision that juniors currently arrive into — the security view is heard while the item is still open; the rotating challenge role makes dissent a duty rather than a personality trait, decoupling disagreement from social risk entirely; and the private conversations — including the honest audit of your own chairing — address the accumulated learning that silence was the safe strategy at this board. Option A, finally, is the trap the whole scenario is built around: "outcomes are acceptable" is survivorship phrased as assurance — the near-misses are the outcomes-in-waiting, and a board that agrees in three minutes is not efficient; it is decorative. The chairing truth underneath, which your community collaboration skill states almost verbatim (identify problems in the team dynamic and rectify them; help stimulate the right responses): a board's inclusiveness is not a courtesy extended to its quiet members — it is the mechanism by which the organisation's risk information actually reaches its risk decisions. Chairs own that mechanism. Unanimity should have to be earned by the item, not manufactured by the room.

**Question 11 (challenging) — The report your manager wants softened**

Your quarterly change performance report to the service management board is drafted. It shows the emergency change ratio doubling, driven largely by a programme sponsored by your own head of operations — your line manager. Reviewing your draft, she says: "Soften the emergency change section. The programme's under enough scrutiny, the board will overreact, and frankly it reflects on both of us. Fold the numbers into the general statistics this quarter — they'll come down next quarter anyway." What is the most effective response?

- A) Comply — she is accountable for the report's context, she may be right about the board overreacting, and the numbers are predicted to recover.
- B) Decline to obscure the data, but engage her real concerns: keep the emergency trend visible and accurately attributed, and offer to strengthen the surrounding context — the programme's delivery pressures, the remediation already agreed, the expected trajectory — so the board reads an honest picture with its explanation attached rather than a bare alarming number; if she still directs the change, state your position clearly and record it.
- C) Submit the softened report but send the board secretary the full figures informally.
- D) Refuse outright and escalate her request to the board chair as attempted interference.

**Correct answer: B**

**Explanation:** Hold onto both truths the scenario contains: the instruction is improper — a governance report exists to inform the board, and folding a doubling trend into general statistics is concealment by aggregation, requested by a person with an interest in the concealment — and the concerns behind it are partly legitimate: boards do overreact to bare numbers, the programme's pressure is real, and context genuinely is missing from a naked ratio. Option B is the only response that treats the impropriety and the legitimacy separately, which is the senior skill. Its first move is the unmovable one: the data stays visible and attributed — your reporting duty runs to the board, and a report shaped to protect its subjects is not a report but a press release. Its second move is where the craft lives: everything she legitimately wants — the board understanding the pressure, the remediation, the trajectory — can be achieved honestly, through context added rather than data removed, and offering to write that context converts you from obstacle into ally on the part of her concern that deserves an ally. The closing clause matters most: if she nonetheless directs the change, a clear stated position and a record — a file note, a repeated objection in writing — is the professional mechanism that distinguishes "I was overruled" from "I participated". Option A is capture with a rationalisation attached: "she may be right about overreaction" hands the decision about what the board can be trusted to know to the person the data embarrasses; and note the tell in "it reflects on both of us" — the invitation is to make her problem yours, priced in your integrity. Option C is the worst of every world: your signed report misleads while an unsigned back-channel contradicts it — the informal route destroys the report's integrity and your deniability simultaneously, and when it surfaces (informal routes surface), both versions and their author are discredited. Option D turns a recoverable conversation into an accusation while skipping B's entire repertoire: she has asked, not yet directed; the request may not survive your reasoned refusal plus a better offer; and escalation remains available at the point of actual direction — deployed then, it is a duty rather than a first resort deployed now, it reads as a manager who cannot navigate their own line. The general form is worth keeping: when pressured to obscure, offer to contextualise. It is the honest version of what the pressurer usually wants, it frequently satisfies them, and when it does not, their refusal of an honest alternative tells you — and later, if needed, others — exactly what was being asked for.

**Question 12 (challenging) — The dependency you cannot command**

Your flagship release in six weeks depends on an API change owned by another department's platform team — outside your organisation's change process entirely, with their own governance and their own priorities. Their team lead has now told your delivery team, informally, that the API change "will probably slip a month" because of their internal pressures. Your release will otherwise be complete, tested, and heavily committed: a minister-announced service improvement depends on it. You have no authority over the platform team. What is the most effective response?

- A) Continue as planned — their lead said "probably", their slippage is their accountability, and your own governance is in order.
- B) Escalate immediately to director level to have pressure applied to the platform team's priorities.
- C) Work the problem at every available level: contact the platform team's lead and their change management counterpart directly to convert "probably slip" into a firm, dated position and to understand their constraint; explore technical decoupling with both delivery teams (interim endpoint, feature-flagged partial release, mock-backed launch of independent components); replan your release's critical path around the honest date; and give your programme sponsors an early, accurate risk position with the options priced — reserving director-level escalation for when facts, not rumours, justify it.
- D) Instruct your delivery team to build against the API's published specification and hold the platform team to it via a formal inter-departmental commitment.

**Correct answer: C**

**Explanation:** The scenario strips away positional authority to expose what coordination actually runs on: information quality, relationships, technical options, and honest stakeholder management. Option C works all four, in the right order. First, the information: "will probably slip a month", delivered informally to your delivery team, is a rumour of a risk — the single highest-value action available is converting it into a fact with a date and a reason, and the route is direct professional contact with the owning team and their governance counterpart (your peer, whom you should know: your community collaboration skill's "actively networking with others" is not a pleasantry — this scenario is what the network is for). Their constraint matters too: understanding why they are slipping tells you whether the date is recoverable, negotiable, or fixed — and teams under internal pressure respond very differently to a peer asking "what would it take, and what can we absorb?" than to pressure from above. Second, the technical degrees of freedom: dependency risk is rarely binary, and the decoupling menu — interim endpoints, feature flags, launching the independent components on schedule with the API-dependent slice following — frequently converts "the release slips a month" into "one feature follows in a month", a materially different ministerial conversation. Third, the honest replan and early sponsor briefing with options priced: your sponsors' worst outcome is not the slip — it is discovering the slip late, and the manager who brings the risk early with three costed responses is doing the coordinating-interdependencies duty at its most valuable. Option A is governance-as-alibi: "their slippage is their accountability" will be true and irrelevant when the minister's announcement fails — accountability for the dependency's owner does not discharge ownership of the outcome, and your ownership skill's wording (own it until mitigated, resolved, or properly handed over) does not recognise "someone else's fault" as a handover. Option B spends the escalation card on a rumour: directors moving on "their lead informally said probably" generates inter-departmental friction, hardens the platform team against you, and — if the informal signal proves wrong — costs credibility you will need for real escalations; escalation is C's reserve move, made potent precisely by the facts C gathers first. Option D is coordination by litigation: building against a specification the owning team is telling you will slip, then brandishing a commitment document, wins arguments and loses releases — the API will still not exist on the day, however firmly you were entitled to it. The senior truth underneath: past a certain level, most of what you must deliver depends on people you cannot instruct. The managers who thrive there are the ones for whom authority was always the backup plan.

### Preparation tips

- **Answer at your level's altitude.** Before choosing, ask: what does the decision-maker for all technical changes, the escalation point, the chair do here? Options that defer your own authority upward, or reach past a conversation to a mandate, are usually mis-calibrated for the role.
- **Separate the substance from the sentiment.** The hardest scenarios braid a checkable claim with an emotional charge (resistance, pressure, embarrassment). The strong answers engage both, on their own terms — fix the edge cases and reframe the distrust; keep the data and add the context.
- **Look for the option that fixes the system.** At manager level, resolving the instance is table stakes; the scored differentiator is usually the element that prevents recurrence — the tooling check, the speaking-order redesign, the strengthened standard.
- **Convert pressure into process.** When someone pushes for an outcome, find the fastest legitimate route to what they actually need. "No" and "yes" are both usually weaker than "here is how".
- **Time-box uncertainty with decision gates.** Where a scenario offers an expiring option and an unproven hypothesis, the strong answer typically defines evidence, sets a gate before the deadline, and pre-agrees the default. Practise spotting that shape.
- **Rehearse the integrity positions before you need them.** Decline-but-contextualise, state-and-record, evidence-then-escalate: knowing your moves for improper requests in advance is what makes them deliverable calmly at the moment of pressure — in assessments and in careers.
- **Debrief your real weeks.** After each significant judgement call, name the four options you had and rank them honestly. Six months of that habit is worth more than any question bank — and it is exactly the reflective practice Agile health checks institutionalise for teams.

### Common pitfalls to avoid

- **Deferring decisions that are yours.** Escalating a release conflict you are mandated to resolve, delegating a 02:40 back-out call, exporting resistance to a board — at this level, over-escalation scores as poorly as lone heroics.
- **Letting outcomes launder process.** The successful unauthorised change, the lucky skipped verification, the acceptable-outcomes board that agrees in three minutes: judging acts by their results this quarter is how the next quarter's incident is purchased.
- **Enforcing without investigating.** Workaround patterns, emergency-route abuse, and resistance to improvements are data about your process before they are violations of it. The strong answers read the signal, then re-agree the rule.
- **Protecting people from information.** Softened reports, sanitised reviews, blame routed to the technically-true target: every version of managing what decision-makers know corrupts the steering the organisation runs on — and implicates the manager who shaped it.
- **Performing accountability instead of exercising it.** Dramatic authority-surrenders, third-party self-reports, and public apologies frequently substitute theatre for the honest record and the dated systemic fix, which are what accountability actually consists of.
- **Treating structure as personality.** Silent board members, disengaged representatives, and unassertive juniors are usually products of speaking orders, status gradients, and meeting design — chair-owned variables. Fix the structure before judging the person.
- **Mistaking the mandate for the relationship.** Authority wins the meeting; networks, honest data, and priced options deliver the release. The scenarios where you command nothing are the truest test of the role — prepare for them most.

## Conclusion

You have reached the end of a demanding piece of work — four full assessment disciplines, nearly fifty scenarios, each one grounded in the real materials and pressures of change and release management. Completing it is itself evidence of the professional seriousness these assessments try to measure.

Consider what you have practised. In the cognitive section, you applied risk classification rules without deference to plausibility, traced dependency chains to their forced conclusions, found the same-CI collision buried in a clean-looking schedule, diagnosed a certificate failure from its internal-versus-external signature, and read the footnote that changed a go-live decision. In the numeric section, you converted availability nines into their real minutes, kept percentage points and percent honestly apart, computed the fifteen-incident perfect streak an SLA recovery actually requires, and priced a process improvement into the payback argument that gets it funded. In the verbal section, you held policy text to its exact scope and modality, tracked findings apart from quoted opinions, measured compliance with the rule's own words rather than the audit's looser proxy, and spotted the unmonitored route beneath a perfect compliance statistic. And in the situational judgement section, you rehearsed the pressure points that define the role: the corridor authorisation declined and redirected, the 02:40 decision gate, the failure account that steered the fix to the standard rather than the scapegoat, the report kept honest and made contextual, and the dependency delivered through influence where authority ran out.

The thread running through all four sections is worth naming, because it is the role itself: your value is the discipline you bring to the space between evidence and action. Change governance done well is not caution, and not speed — it is the consistent practice of knowing exactly what the data, the policy, the assessment, and the incident timeline do and do not establish, and acting proportionately on precisely that. Every technique in this guide — base-checking, scope-holding, mechanism-tracing, gate-setting, contextualising instead of concealing — is that one discipline wearing different clothes.

If you carry three habits forward, let them be these. First, interrogate the number and the sentence before you use them: the base, the scope, the attribution, the footnote — at your level, most avoidable errors are inherited from unexamined inputs. Second, treat workarounds, resistance, and silence as information about the systems you own: the teams routing around your process and the board members not speaking at your CAB are telling you where your next improvement lives. Third, keep the record honest especially when it is expensive: the sanitised review, the softened report, and the technically-true account are each available every quarter, and declining them — with context and a fix attached — is what compounds into the kind of trust that makes a change manager's authority real.

Practise steadily rather than heroically, return to the sections that stretched you, and take the assessment as you take a release into production: prepared, unhurried, and with your judgement already rehearsed. The organisation's ability to change safely and quickly at the same time is not an abstraction — it is the accumulated effect of decisions like the ones you have been practising here, made well, repeatedly, by someone who takes them seriously. You clearly do. Good luck.
