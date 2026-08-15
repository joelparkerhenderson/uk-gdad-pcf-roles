# Lead End User Computing Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a lead end user computing engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills and professional judgement that predict success in a role. For a lead end user computing engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the materials you genuinely handle — vendor contracts and supplier performance data, high-impact change requests, release policies, test plans spanning functional and non-functional specifications, procedures and standards you draft and enforce, and the reports through which you represent end user computing to the wider organisation — and the decisions you genuinely make, such as holding suppliers to account, leading the investigation of the incidents that matter most, setting standards for the security and integrity of the estate, and working with technical architecture to judge feasibility.

Why do these assessments matter at your level in particular? Your role summary is explicit: you hold expert technical understanding and accountability for vendor and supplier management, and you work across IT operations and other functions to understand productivity, development and feasibility at the levels below you. That is a role defined by judgement exercised across boundaries — technical, commercial and organisational. The thinking skills underneath it are testable: recognising patterns in supplier and estate data that others miss; reasoning rigorously about high-impact changes where a wrong assessment cascades; checking documents — contracts, test plans, release notes, procedures — whose errors become everyone's errors; prioritising where your accountability, not just your time, is the scarce resource; interpreting data sets for stakeholders who will act on your reading; and making judgement calls where users, engineers, suppliers and architecture pull in different directions. Being proactive in searching for potential problems — your ownership skill's own phrase — is very nearly a definition of the assessed skill set.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of its dimensions to the named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The four sections cover:

1. A **cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation and applied problem solving, using vendor data, change and release artefacts, standards and test plans.
2. A **numeric reasoning assessment** — percentages, rates, weighted figures, trends, forecasts and cost analysis, built on supplier SLAs, estate data, test metrics and budgets.
3. A **verbal reasoning assessment** — precise comprehension of contracts, policies, vendor advisories, architecture papers and stakeholder correspondence, with true/false/cannot-say discipline.
4. A **situational judgement assessment** — realistic dilemmas about supplier accountability, high-impact change, standards enforcement, leading investigations, mentoring, and championing users.

To get the most from this guide: work one section at a time; commit to an answer before reading each explanation; and treat every explanation as a mini-lesson even when you answered correctly. At your level there is a further use — these worked walkthroughs are the reasoning you increasingly teach: to senior engineers learning escalation judgement, to teams learning test planning, and to stakeholders learning what good evidence looks like. Consider each one a rehearsal.

You are accountable for outcomes across an estate. Let's sharpen the thinking that accountability runs on.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical scenarios rather than abstract puzzles. At lead level, the materials are the artefacts of accountability: supplier performance summaries, high-impact change requests, release policy checks, test plans, security standards, and the cross-functional evidence through which you judge feasibility and productivity.

The typical format is an online, timed test lasting 15 to 30 minutes, with 15 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group; platforms often adapt difficulty as you perform well and report speed and accuracy separately. Short ungraded practice questions usually precede the real test.

For a lead engineer, cognitive assessment is particularly relevant because your professional value is structured thinking applied where errors are most expensive. Leading the investigation and resolution of incidents means reasoning about causes when the estate's most complex faults have defeated the first two attempts. Managing high-impact, complex change requests means tracing consequences through dependencies others have not mapped. Ensuring release policies are applied, and setting standards for the definition, security and integrity of objects, means detecting the deviation before it becomes the incident. Vendor and supplier management means reading performance data the supplier has presented in its own best light. And being proactive in searching for potential problems — the distinctive obligation of your ownership skill — is pattern recognition pointed at the future rather than the past. A well-designed cognitive test samples all of this in miniature.

### How this assessment maps to your role

- **Pattern recognition** maps to your **Problem management** and **Ownership** skills: initiating investigations of patterns and trends, and proactively searching for potential problems, both begin with seeing structure in noisy estate and supplier data — the drift that precedes the failure.
- **Logical deduction** maps to your **Change management** skill: managing high-impact, complex change requests means reasoning from proposed alterations through dependency chains to consequences, and ensuring release policies, procedures and processes are applied means applying rule systems exactly.
- **Error checking** maps to your **Technical specialism** skill: drafting and maintaining procedures and documentation, and setting standards for the definition, security and integrity of objects while ensuring conformity, is professional-grade inconsistency detection — in documents you wrote and documents suppliers send you.
- **Prioritisation** maps to your **Ownership** and **Service focus** skills: taking accountability for issues and achieving excellent user outcomes across groups of services requires ranking by impact across a whole estate, not a single queue.
- **Applied problem solving** maps to your **Incident management** skill (lead the investigation and resolution of incidents) and your **Testing** skill (manage the planning of system and acceptance tests across functional and non-functional specifications): both decompose complex, contested situations into checkable parts.

### Practice questions

**Question 1 (easy) — Pattern in supplier performance data**

Your hardware repair supplier reports monthly turnaround times (days) for the last eight months: 4.1, 4.0, 4.2, 4.1, 4.6, 5.1, 5.7, 6.2. The contract target is 5.0 days, and the supplier notes "only three months have exceeded target." What is the most important pattern?

- A) Five of eight months met target, so performance is broadly acceptable.
- B) A steady upward drift began around month 5 and has continued for four consecutive months — the trajectory, not the current breach count, is the story, and it projects further deterioration if unaddressed.
- C) Month 8 is an outlier that should be excluded.
- D) The average of 4.75 days is under target, so no action is needed.

**Correct answer: B**

**Explanation:** Characterise the shape before judging the level. Months 1–4 hold a stable band (4.0–4.2); from month 5 the series climbs monotonically — 4.6, 5.1, 5.7, 6.2 — four consecutive rises with a growing increment. That is drift, not noise, and drift has a cause: capacity loss, a subcontractor change, a parts shortage. The supplier's framing ("only three months exceeded") and option D's average are both level-statements that a trend erodes monthly — the average is under target only because the good early months still dominate it. Option C mislabels the latest point of a smooth climb as an outlier; outliers depart from a pattern, and 6.2 is the pattern. The vendor-management consequence: raising this at review as "three breaches" invites a promise about next month; raising it as "four months of monotonic drift — what changed in month 5?" demands a causal account, which is the conversation that actually fixes turnaround. Your accountability for supplier management is, in large part, refusing level-framings of trend-problems.

**Question 2 (easy) — Deduction through a release policy**

Your release policy states: (i) production releases require a completed acceptance test report; (ii) releases touching security components additionally require sign-off from the security architect; (iii) emergency security patches may release with sign-off alone, with the acceptance report completed retrospectively within five working days; (iv) a release using rule (iii) may not itself be followed by another rule-(iii) release for the same component until its retrospective report is filed. A team released an emergency security patch for the VPN client on Monday under rule (iii). On Thursday (report not yet filed), a new critical VPN client vulnerability is announced. What does the policy permit?

- A) Another rule-(iii) emergency release immediately — critical vulnerabilities always qualify.
- B) A rule-(iii) release only after Monday's retrospective report is filed — which the team can expedite today, then release under (iii); alternatively a full rule-(i)+(ii) release at any time.
- C) No release of any kind until five working days elapse.
- D) A normal release without the acceptance test report, since one is already pending.

**Correct answer: B**

**Explanation:** Rule (iv) is the gate: Monday's release used rule (iii), its report is unfiled, so the emergency route is closed for the VPN client — option A fails on exactly the clause written to prevent serial untested patching. But closed is not locked: the team controls the key, because filing Monday's retrospective report (which was due within five days anyway) re-opens rule (iii); and the ordinary route — completed acceptance report plus security sign-off — was never closed. Option B captures both lawful paths, and the practical reading matters: the fastest compliant response to Thursday's vulnerability is probably "finish Monday's report today, then emergency-release," which is also exactly the behaviour rule (iv) was designed to incentivise. Option C invents a waiting period the policy nowhere imposes; option D bootstraps a pending obligation into a waiver. Ensuring release policies are applied — your change management skill — means reading them as systems of incentives, not just constraints: here the policy converts urgency into a reason to complete the safety work, and the lead engineer who sees that turns a compliance problem into a two-hour task list.

**Question 3 (easy) — Error checking a standards conformity report**

Your encryption standard requires: all laptops encrypted with algorithm X; all USB-exception devices encrypted with algorithm X and logged in the exceptions register; servers out of scope. A conformity report states: "Estate scan: 1,180 of 1,200 laptops confirmed algorithm X. 15 laptops running legacy algorithm Y. 5 laptops returned no scan result. 3 USB-exception devices found, all algorithm X, 2 present in the exceptions register. Conclusion: 98.3% conformity; standard effectively met."

Which finding most undermines the report's conclusion?

- A) The 15 algorithm-Y laptops — legacy encryption is the largest count.
- B) The report treats "no scan result" and an unregistered exception device as if they were near-conformity, but 5 unscanned laptops are unknown-state (not conforming), and 1 USB device operating outside the register is a control failure regardless of its encryption — the conclusion's framing, not just its arithmetic, is wrong.
- C) The 98.3% figure is miscalculated and should be 98.4%.
- D) Servers were not scanned.

**Correct answer: B**

**Explanation:** The report's numbers are roughly honest; its epistemology is not. Three distinct states are being blended: non-conforming (15 laptops on algorithm Y — a remediation queue), unknown (5 laptops with no result — which a conformity conclusion must treat as not-known-to-conform, since "we couldn't see it" is precisely where breaches hide), and control-broken (1 exception device encrypted correctly but absent from the register — the register is the control; a device outside it is invisible to future audits even though today's spot-check happened to find it healthy). "Standard effectively met" launders all three into a single reassuring percentage. Option A ranks by count, but the 15 known-bad laptops are the best-understood item on the list — identified, bounded, fixable. Option C is decimal-point pedantry. Option D cites an explicit out-of-scope. Setting standards and ensuring conformity to them — your technical specialism verbatim — depends on exactly this discrimination: a conformity report's job is to separate conforming, non-conforming, unknown and uncontrolled, and any report that sums them into one number has already failed, whatever the number says.

**Question 4 (moderate) — Prioritising accountability, not tasks**

Monday, 09:00. Four matters compete for your personal attention this week:

1. The quarterly supplier review with your hardware vendor is Thursday; their performance data arrived Friday and nobody has analysed it yet.
2. A high-impact change request — migrating 2,000 users' profiles to new storage — awaits your impact assessment, with the change board meeting Wednesday.
3. A senior engineer has fully diagnosed a recurring estate-wide fault and drafted an escalation to the software vendor; they ask you to review and send it under your name.
4. Your service desk manager asks you to personally lead the investigation of a P2 affecting one directorate's printers, "because the seniors are busy."

What is the strongest disposition of the four?

- A) Do all four yourself in deadline order: 2, 1, 3, 4.
- B) Own 1 and 2 personally (supplier accountability and high-impact change assessment are yours and hard-deadlined); review and strengthen 3 quickly — it is nearly done and sending it under your name is right; push back on 4: a P2 printer fault is squarely within a senior engineer's remit, so re-prioritise the seniors' queue rather than absorbing their work.
- C) Delegate 1 and 2 to seniors to develop them; personally take 4 to stay hands-on; send 3 unread since the engineer is capable.
- D) Do 2 and 4 this week; postpone the supplier review and let the engineer send 3 themselves.

**Correct answer: B**

**Explanation:** Lead-level prioritisation allocates accountability, not just hours. Items 1 and 2 are irreducibly yours: vendor management is your named accountability, and Thursday's review is only as good as the analysis behind it — a review walked into unprepared is a review the supplier controls; the high-impact change assessment is exactly what "manage high impact, complex change requests" means, and Wednesday is fixed. Item 3 is leadership at its cheapest and best: the engineer has done the work; your review adds authority and a teaching moment, and your name adds weight with the vendor — fifteen minutes, high leverage (sending unread, option C, spends your authority without your judgement — signing what you have not checked is how names lose their value). Item 4 is the trap: "the seniors are busy" is a prioritisation problem inside the seniors' queue, and absorbing it converts you into surge capacity while your unique work — items 1 and 2 — degrades; the lead response is to help re-rank the seniors' work, not to do it. Option A treats all four as your tasks; option D sacrifices the supplier review, the single item where unpreparedness compounds across a whole contract quarter. The pattern: protect the work only you can do, multiply the work others have nearly done, and route the rest back to where it belongs.

**Question 5 (moderate) — Deduction about a high-impact change's dependencies**

The profile-migration change (2,000 users) has these facts: (i) migration runs at 250 profiles per night, weeknights only; (ii) the old storage's support contract expires in 15 working days; (iii) profiles containing legacy-format archives (estimated 20%, exact list unknown) fail migration unless pre-converted; (iv) pre-conversion is done by a script processing 100 profiles per day, runnable in parallel with migrations; (v) failed migrations must be retried after conversion, consuming a night's slot capacity. What is the critical vulnerability in the schedule?

- A) Migration capacity: 2,000 ÷ 250 = 8 nights, comfortably within 15 days.
- B) The unknown identity of the ~400 legacy-format profiles: if conversion (4 days for 400) is not sequenced ahead of the affected profiles' migration slots, failures consume retry capacity and the schedule slips against a hard contract expiry — so the first action is identifying the legacy profiles, not starting the migration.
- C) The script's 100-per-day rate is too slow and must be improved before anything starts.
- D) The contract expiry should be extended as a precaution.

**Correct answer: B**

**Explanation:** Run the arithmetic to find where the risk concentrates. Raw migration: 8 weeknights for 2,000 — inside 15 working days with a buffer (option A is true and incomplete). Conversion: 400 profiles at 100/day = 4 days, parallel — also fits. The vulnerability is informational, not capacity: nobody knows which 400 profiles need conversion, so an unsequenced migration hits unconverted profiles, burns slots on failures, and pays again on retries — and every wasted night erodes a buffer bounded by a contract expiry you do not control. Option B's operational conclusion follows: the critical path's first task is the cheap one — enumerate legacy-format profiles (a scan), then order the migration queue so converted profiles migrate first while conversion runs ahead of the remainder. Option C fixes a rate that already fits; option D reaches for a commercial remedy (with cost and negotiation lead-time) before exhausting the engineering one. The lead-level habit this trains: in complex changes, the schedule-killer is usually the unknown that determines sequencing, not the capacity that determines duration — impact assessment means finding the fact whose absence makes every other number soft.

**Question 6 (moderate) — Error checking a supplier's test summary**

Your MDM vendor submits acceptance evidence for a platform upgrade: "Functional: 312 of 320 test cases passed (97.5%). The 8 failures are cosmetic UI issues, fix scheduled next quarter. Non-functional: enrolment load test passed at 500 concurrent enrolments (contracted volume). Performance test of policy-push completed on the vendor reference environment. Security: penetration test passed with no critical findings; two medium findings mitigated. Recommendation: proceed to production."

As the manager of acceptance test planning, which gap most needs challenge before you accept?

- A) The 8 cosmetic failures should be fixed before acceptance.
- B) The policy-push performance test ran on the vendor's reference environment, not on (or modelled on) your estate — reference environments are tuned and unrepresentative, so the one non-functional result most sensitive to environment is currently evidence about the vendor's lab, not your service; require the test re-run or validated against your environment profile.
- C) Two medium security findings are unacceptable; demand zero findings.
- D) 97.5% is below the 100% a production system requires.

**Correct answer: B**

**Explanation:** Audit each evidence line for what it actually demonstrates. Functional 97.5% with characterised, scheduled cosmetic failures is acceptable evidence — option A and option D apply a perfection standard acceptance testing has never used; the question is whether failures are understood and tolerable, and "cosmetic, fix scheduled" answers it (verify the characterisation by sampling the 8, but that is diligence, not blockage). "Passed with no critical findings; mediums mitigated" is likewise normal security evidence — option C's zero-findings demand would reject every real system. The load test names its condition (500 concurrent, contracted volume) — checkable. The soft spot is the sentence that names no result at all: the policy-push test "completed" (not "passed", worth noticing) on the vendor reference environment — and environment-sensitivity is precisely what non-functional testing exists to expose: your estate's network topology, device mix and directory load are what a tuned lab lacks. Accepting it would let the least transferable result stand as proof for production. Managing the planning of system and acceptance tests, co-ordinating functional and non-functional specifications — your testing skill verbatim — is largely this: for each claim, ask "what environment, what condition, what verdict?", and challenge the line where the answer goes vague. Vendors put their weakest evidence in their smoothest sentence.

**Question 7 (moderate) — Pattern across incident, change and release data**

Reviewing three months of estate data, you notice: P1/P2 incident counts are flat; but incidents tagged "regression after release" have risen from 2 to 5 to 9 per month; over the same months, releases went from 6 to 9 to 14, of which "expedited" releases (reduced pre-release testing under an approved fast-track) went from 1 to 3 to 8. Normal-track releases (5, 6, 6) are roughly constant. What is the most defensible reading?

- A) More releases naturally mean more regressions; the growth is proportionate and benign.
- B) Regressions are growing faster than releases overall, and the growth aligns with the expedited track specifically (1→3→8) while normal-track volume is flat — the fast-track's reduced testing is the prime suspect, warranting a per-track regression breakdown and a review of what the fast-track skips.
- C) The teams releasing software have become careless and need retraining.
- D) Releases should be frozen until regressions return to baseline.

**Correct answer: B**

**Explanation:** Test proportionality before accepting it. Releases roughly doubled (6→14); regressions more than quadrupled (2→9) — option A's "proportionate" fails its own arithmetic. Now decompose the release growth: normal-track is flat (5, 6, 6), so essentially all growth is expedited (1→3→8) — and the regression curve's shape tracks the expedited curve, not the total. The inference is a hypothesis with a mechanism: expedited releases skip testing, skipped testing ships regressions — but option B claims it at the right strength ("prime suspect") and names the discriminating next step: tag regressions by originating track; if expedited releases carry a several-fold higher regression rate, the fast-track's scope needs tightening — perhaps it is being used for changes it was never designed for. Option C leaps to a people-explanation when the process data points at a process change. Option D burns the estate's release capacity to treat a symptom whose cause one query would isolate. This is the lead synthesis your role summary implies — release policy ownership, problem trends and reporting joined into one investigation — and the recurring method: when an aggregate accelerates, decompose it along the dimension that changed.

**Question 8 (moderate) — Feasibility judgement with architecture**

Technical architecture proposes replacing your estate's remote-support tooling with a platform-native alternative, citing licence savings of £60,000 per year. Your assessment finds: the native tool covers 90% of current use cases; the missing 10% is unattended access to kiosk devices in public-facing sites — used by your team roughly 40 times per month, with the nearest engineer typically 90 minutes from each site; the native roadmap lists unattended access "under consideration." Which response best serves the decision?

- A) Support the proposal — 90% coverage and £60,000 savings clearly outweigh a 10% gap.
- B) Oppose the proposal — any capability regression is unacceptable.
- C) Quantify the gap before the decision: 40 monthly kiosk interventions × ~3 hours engineer travel-and-fix ≈ 120 engineer-hours per month (~£3,000–4,000/month at loaded cost, plus kiosk downtime in public-facing sites), which materially offsets the £60,000 annual saving; present both numbers, plus options — retain a minimal licence subset for kiosk coverage, or gate migration on the roadmap item maturing — and let the decision be made on the full comparison.
- D) Escalate the disagreement to the service desk manager to adjudicate.

**Correct answer: C**

**Explanation:** The proposal prices one side of the ledger. Option C prices the other: the "10% of use cases" resolves to 40 monthly incidents that each convert a remote fix into a 90-minute-each-way site visit — roughly 120 engineer-hours monthly, £36,000–48,000 annually at loaded cost, before counting the harder-to-price item, public-facing kiosks standing dark for half a day. Suddenly the £60,000 saving is a £12,000–24,000 saving with a service regression attached, and the genuinely good options appear: a retained minimal licence pool for the kiosk use case (capturing most savings and all capability), or sequencing the migration behind the vendor's roadmap. That is what working with technical architecture "to understand lower level productivity, development and feasibility" — your role summary's phrase — actually means: architecture sees the platform; you see the 40 monthly events the platform summary compresses into "10%". Option A accepts percentage-framing of an operational cost; use-case percentages weight all cases equally, and your kiosk cases are the expensive ones. Option B is capability conservatism with no numbers — the posture that gets operations excluded from design decisions. Option D escalates a disagreement you have not yet turned into evidence; adjudication without quantification just picks a loser. The lead pattern: translate coverage gaps into hours, pounds and user outcomes — then the right decision usually makes itself.

**Question 9 (challenging) — Leading an investigation that crosses three parties**

A directorate reports that managed laptops intermittently freeze for 30–60 seconds. Your seniors have established: freezes correlate with security-agent scan windows (vendor A's product); vendor A blames "known conflicts" with the disk-encryption driver (vendor B), citing a generic advisory; vendor B states their driver is certified for this laptop model and blames the security agent's I/O load; your own telemetry shows freezes only on the 40% of the estate with the older SSD variant, and only when scan and encryption-key-rotation windows overlap. Neither vendor has seen your telemetry. What is the strongest next move?

- A) Accept vendor A's advisory and disable scanning on affected machines pending their fix.
- B) Convene a three-way technical session where you table the telemetry as the controlling evidence — the SSD-variant restriction and the window-overlap condition discriminate between both vendors' blame theories — and propose a joint reproduction on the older-SSD configuration with both vendors' engineers observing; meanwhile mitigate by de-conflicting the two scheduled windows on affected machines, a change within your own control.
- C) Escalate both vendors' blame-shifting to commercial contacts and let contract managers resolve it.
- D) Replace the older SSDs across 40% of the estate, since the fault follows that variant.

**Correct answer: B**

**Explanation:** You hold the evidence neither vendor has: telemetry showing the fault requires three coincident factors — older SSD, scan window, key-rotation overlap. That triple condition explains everything the blame theories cannot: why vendor B's certification is honest (the driver is fine except under overlapped load on slower storage), why vendor A's generic advisory is unfalsifiable hand-waving, and why the fault is intermittent (windows only sometimes overlap). Option B uses the evidence as leverage in the right order: a joint reproduction on the discriminating configuration converts finger-pointing into a shared observable — vendors stop blaming when both watch the same failure — while the immediate mitigation (de-conflicting the schedules) sits entirely within your own control and likely stops most user pain today without waiting for either vendor. That mitigation choice is itself diagnostic: if de-overlapping eliminates freezes, the interaction hypothesis is confirmed. Option A disables a security control estate-wide on the strength of the vaguer vendor's theory — trading a freeze for an exposure. Option C converts a solvable technical question into a commercial dispute; contracts allocate blame, they do not find root causes, and you would arrive at that table without the joint reproduction that proves your case anyway. Option D spends hardware budget on a correlation before testing the cheap interaction fix. Leading the investigation and resolution of incidents — your incident management skill verbatim — means recognising when you are the only party with the whole picture, and designing the demonstration that makes everyone else see it.

**Question 10 (challenging) — Proactive problem search in quiet data**

All headline metrics are green: SLAs met, incident counts stable, user satisfaction steady. Practising your ownership skill's mandate to search proactively for potential problems, you dig deeper and find four sub-surface signals. Which most warrants preventative investigation?

1. Average laptop age has risen from 2.1 to 3.4 years as replacement purchasing slowed; battery-related tickets are up 15% from a low base.
2. One of three service-desk shifts now resolves 30% fewer tickets per engineer than the others, having lost two experienced staff.
3. The estate's device-encryption compliance holds at 99.1%, but the 0.9% non-compliant population has been the same 30 devices for four months, all in one remote site.
4. Software licence utilisation for a niche engineering application has fallen from 80% to 45% of purchased seats.

- A) Signal 1 — ageing hardware affects the most users.
- B) Signal 2 — team productivity is the lead's core concern.
- C) Signal 3 — a static, geographically-concentrated non-compliant population means the compliance process has a systematic blind spot: whatever excludes that site from remediation (connectivity, local practice, an unmanaged network segment) is a standing security exposure that green headline percentages will conceal indefinitely.
- D) Signal 4 — wasted licence spend is a recoverable cost.

**Correct answer: C**

**Explanation:** All four deserve a place on a risk register; the question is which one preventative investigation must reach first, and the discriminator is self-correction: will the normal machinery surface and fix this, or will it persist invisibly? Signal 1 is visible drift with a visible symptom — the ticket trend itself will force the replacement conversation, and the fix (a purchasing case) is standard. Signal 2 has a known cause (two leavers), a natural owner (the shift's manager), and standard remedies. Signal 4 is money, bounded and recoverable at next renewal. Signal 3 is different in kind: the same 30 devices, one site, four months means remediation is systematically failing there while the headline sits at 99.1% — and a static unencrypted population at a remote site is exactly the shape of the breach post-mortems describe. Worse, the metric's greenness is the camouflage: 99.1% reads as success, so no routine process will ever ask why the residue never shrinks. Persistence plus concentration plus invisibility-to-metrics is the signature of a process hole, and process holes compound. This is your ownership skill's proactive search operating as designed — and the general lesson for both assessments and estates: in green dashboards, investigate the residuals that never change, because static remainders are where systematic failures hide from averages.

**Question 11 (challenging) — Standards, evidence and an exception request**

You own the standard requiring all admin access to estate management tools via named individual accounts with multi-factor authentication; shared accounts are prohibited. A field-services team requests a standing exception: "site engineers share workstations in depots with no mobile signal for MFA, and per-engineer login adds 10 minutes per depot visit; we need one shared depot account." Their productivity data is real. What is the strongest response?

- A) Refuse: the standard exists for security and admits no exceptions.
- B) Grant the exception: documented productivity costs justify it, and field conditions are genuinely different.
- C) Treat the request as a requirements signal, not a compliance question: the legitimate need is fast, authenticated access under poor connectivity — solvable within the standard's intent via hardware tokens or offline authenticators (MFA without mobile signal) and fast user-switching profiles; pilot that at two depots against the 10-minute baseline, and only if intent-preserving options demonstrably fail consider a tightly-scoped, logged, expiring exception — never an unlogged shared account.
- D) Grant a temporary shared account while a working group studies the problem.

**Correct answer: C**

**Explanation:** A standards owner has three tools — refuse, except, redesign — and the scenario is built so the third wins. The request conflates its need (fast authenticated access without mobile signal) with its proposed solution (a shared account), and the two are separable: hardware tokens and offline authenticator apps deliver MFA with no signal; fast user-switching attacks the 10-minute cost directly. A pilot against the measured baseline converts the argument into evidence. Option A defends the standard's letter while ignoring a real operational cost — and standards enforced without engagement teach teams to stop requesting and start quietly working around, which is how shared credentials appear anyway, unlogged. Option B solves productivity by dissolving accountability: a shared admin account makes every depot action anonymous — the exact property the standard exists to prevent, and the property incident investigation will one day need. Option D is option B with a calendar attached; "temporary" shared credentials outlive their working groups with great reliability. Note the ordering inside option C: intent-preserving redesign first, and only after demonstrated failure a scoped, logged, expiring exception — exceptions as pressure-release valves are legitimate; exceptions as the path of least resistance are erosion. Setting standards for security and integrity and ensuring conformity — your technical specialism — is at its best exactly here: holding the intent fixed while negotiating the implementation, so the standard earns conformity instead of merely demanding it.

### Preparation tips

- **Practise on supplier and estate data you own.** Take a quarter of vendor performance figures or release/incident data and interrogate the shapes: drifts, static residuals, decompositions along whatever changed. The assessment's patterns are your Tuesday afternoon, formalised.
- **Read rule systems for incentives, not just constraints.** Release policies, standards and contracts encode intended behaviour. For each rule, ask what it makes cheap and what it makes expensive — questions about them nearly always turn on the clause that changes the incentive.
- **Audit evidence line by line for what it demonstrates.** For every claim in a test summary or conformity report: what environment, what condition, what verdict? The vague line is the question's answer more often than the failing line.
- **Quantify before you adjudicate.** Feasibility and priority questions reward the option that converts percentages into hours, pounds and user outcomes. Practise the translation until it is reflex — "10% of use cases" should trigger "which ones, how often, costing what?"
- **Protect your unique work in prioritisation items.** The strong answer keeps accountability where only you can hold it (vendors, high-impact assessments), multiplies nearly-finished work with a light touch, and routes absorbed work back. Options where the lead does everything — or signs anything unread — are traps.
- **Time-box hard questions.** Ninety seconds of structured effort, best answer, flag, move on. Estate-level judgement and assessment scoring both reward calibrated throughput.

### Common pitfalls to avoid

- **Judging levels when the story is trend.** "Average under target" and "only three breaches" are level-framings that monotonic drift makes obsolete monthly. Characterise shape first.
- **Blending unknown into conforming.** Unscanned devices, unlogged exceptions, "completed" tests without verdicts — treating absence of evidence as weak conformity is how green reports precede incidents.
- **Accepting the vendor's environment as yours.** Reference-lab results transfer only where environment doesn't matter — and non-functional results are defined by environment. Ask where every number was measured.
- **People-explanations for process-shaped data.** When regressions track the expedited-release curve, "teams got careless" is a reach past the obvious. Decompose along what changed before blaming who didn't.
- **Absorbing what should be routed.** Personally taking the P2 because "seniors are busy" feels responsive and starves the work only you can do. Re-rank their queue; keep your accountabilities.
- **Enforcing standards without engaging needs.** Flat refusals drive workarounds underground; easy exceptions dissolve the control. The scored answer redesigns within intent — and makes exceptions scoped, logged and expiring when granted at all.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your role genuinely runs on: supplier SLA and credit calculations, estate-wide compliance and refresh figures, release and test metrics, capacity forecasts, and the cost comparisons behind vendor and feasibility decisions.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions, each built around a table, chart or described dataset. A calculator and rough paper are normally allowed; the tested skill is selecting the right figures, choosing the right method, and sense-checking results — under time pressure and, at your level, under someone else's framing, because many of the numbers you receive arrive pre-packaged by parties with positions: vendors presenting their own performance, teams presenting their own test results, proposals presenting their own savings.

For a lead engineer, numeric fluency is a form of accountability. Vendor and supplier management is conducted through numbers — turnaround times, availability percentages, service credits, penalty thresholds — and the party that computes more carefully controls the review. Managing high-impact changes means schedule, capacity and risk arithmetic where errors cascade across thousands of users. Your reporting skill requires interpreting data sets for stakeholders who will act on your interpretation, and your testing skill requires reading pass rates and performance results as evidence rather than reassurance. Meanwhile your service focus — getting the best from groups of underlying services — often reduces to cost-per-outcome comparisons across options nobody else has priced fairly.

The mathematics stays practical: percentages, rates, weighted figures, trends, forecasting and cost modelling. The questions lean hard on interpretation — the wrong denominator, the flattering average, the unpriced side of the ledger — because at lead level, arithmetic is rarely the hard part; noticing whose arithmetic you are trusting is.

### How this assessment maps to your role

- **SLA and service-credit calculations** map to your **vendor and supplier management** accountability: contract percentages, measurement windows and credit formulas are where supplier performance becomes money, and misreading them cedes the review.
- **Estate-scale rates and compliance figures** map to your **Asset and configuration management** skill (manage service compliance via accurate information) and your **Technical specialism** (standards conformity): percentages of large populations, and the residuals inside them, are your daily material.
- **Trend analysis and decomposition** map to your **Problem management** and **Ownership** skills: investigating patterns and proactively searching for potential problems means distinguishing drift from noise and decomposing aggregates along whatever changed.
- **Schedule and capacity arithmetic** maps to your **Change management** skill: high-impact change assessment is critical-path calculation with hard external deadlines.
- **Test metrics** map to your **Testing** skill: managing acceptance test planning means reading pass rates, load results and defect data with the denominators exposed.
- **Cost modelling** maps to your **Service focus** and feasibility work with **technical architecture**: total-cost comparisons, savings claims and licence utilisation are decided by whoever prices both sides of the ledger.

### Practice questions

**Question 1 (easy) — Supplier availability against contract**

Your device-management platform's contract guarantees 99.5% monthly availability during core hours (07:00–19:00, 22 working days this month — 264 core hours). The platform was down for 100 minutes during core hours this month. Did the supplier meet the SLA?

- A) Yes — availability was about 99.4%, within rounding of target.
- B) No — availability was about 99.37%, below the 99.5% floor, which permits at most about 79 minutes of core-hours downtime.
- C) Yes — 100 minutes is negligible over a month.
- D) Cannot tell without knowing the annual figure.

**Correct answer: B**

**Explanation:** Convert the guarantee into minutes — the form in which it can be checked. Core hours: 264 × 60 = 15,840 minutes. Permitted downtime: 0.5% of 15,840 = 79.2 minutes. Actual: 100 minutes — over the allowance. Availability achieved: (15,840 − 100) ÷ 15,840 = 15,740 ÷ 15,840 ≈ 0.99369 = 99.37%, below 99.5% — the SLA is breached, answer B. Option A's "within rounding" gives away exactly what the contract's decimal exists to hold: at these availability levels, the action all happens in fractions of a percent, and 99.37 versus 99.5 is a 26% overshoot of the downtime budget (100 v 79 minutes). The lead habit: pre-compute each contract percentage into its minutes-per-month allowance once, and every incident thereafter can be scored against the budget in real time — walking into a supplier review already knowing "you used 127% of the downtime allowance" is a different conversation from asking whether 99.4-ish is close enough.

**Question 2 (easy) — Service credit calculation**

The same contract's credit clause: "For each 0.1 percentage point (or part thereof) below 99.5% monthly availability, a service credit of 2% of the monthly charge applies, capped at 10%." The monthly charge is £18,000 and availability was 99.37%. What credit is due?

- A) £360
- B) £720
- C) £540
- D) £1,800

**Correct answer: B**

**Explanation:** Work the clause mechanically. Shortfall: 99.5 − 99.37 = 0.13 percentage points. Credit bands of 0.1 "or part thereof": 0.13 spans one full band (0.1) plus a part-band (0.03) — the "or part thereof" wording rounds the part up, giving 2 bands. Credit: 2 bands × 2% = 4% of £18,000 = £720 — answer B. Option A pays one band, misreading "or part thereof"; option D applies the 10% cap without cause. The two-word phrase is the whole question: "part thereof" is a rounding-up instruction written into the contract, and suppliers' own credit calculations have been known to round in the other direction. At your accountability level, checking a credit calculation against the clause's exact banding language — before countersigning the supplier's figure — is five minutes that repays itself monthly; and noticing which way every rounding clause in a contract points is due diligence performed once per contract, dividend paid forever.

**Question 3 (easy) — Estate refresh arithmetic**

The laptop estate is 2,400 devices. Refresh policy targets replacement at 4 years. Purchases over the last four years were: year 1: 700; year 2: 450; year 3: 350; year 4: 500 — the remaining 400 devices are older than four years. If next year's budget covers 550 replacements, prioritised oldest-first, how many over-policy devices will remain at year end (ignoring failures), counting the year-1 cohort as passing the 4-year mark during next year?

- A) 0
- B) 400
- C) 550
- D) 250

**Correct answer: C**

**Explanation:** Count the over-policy population at next year's end before applying the budget. Already over 4 years now: 400. During next year, the year-1 cohort (700 devices) passes the 4-year mark, joining them: 400 + 700 = 1,100 over-policy devices by year end. Budget replaces 550, oldest first: 1,100 − 550 = 550 remain over policy — answer C. Option B forgets the cohort crossing the threshold during the year — the standard error in refresh arithmetic, which always understates the backlog because populations age while budgets are spent. The planning insight the calculation surfaces: the year-2 purchasing dip (450) and the year-1 spike (700) mean the backlog is about to lurch, and a flat 550-per-year budget against a 600-average annual requirement (2,400 ÷ 4) never catches up — the case for smoothing purchase volumes, or for a one-off catch-up bid, is sitting inside this arithmetic, and the lead who runs it owns the budget conversation rather than inheriting its consequences.

**Question 4 (moderate) — Weighted supplier comparison**

Two repair suppliers quote for your next contract. Supplier X: £45 per repair, historical first-time-fix 92%, failed first fixes redone free but adding 5 days' user downtime each. Supplier Y: £38 per repair, first-time-fix 80%, same free-redo terms and 5-day redo delay. You expect 1,200 repairs per year, and you cost user downtime at £30 per day. Which supplier is cheaper on the full comparison, and by roughly how much per year?

- A) Y, by about £8,400 — the £7 unit saving times 1,200
- B) X, by about £13,200 — Y's extra redo downtime outweighs its unit saving
- C) They are equal within £1,000
- D) X, by about £4,800

**Correct answer: B**

**Explanation:** Price both columns of both ledgers. Repair charges: X = 1,200 × £45 = £54,000; Y = 1,200 × £38 = £45,600 — Y saves £8,400 on unit price (option A stops here). Redo downtime: X fails first-time on 8% of 1,200 = 96 repairs, costing 96 × 5 days × £30 = £14,400; Y fails on 20% of 1,200 = 240 repairs, costing 240 × 5 × £30 = £36,000. Full annual cost: X = £54,000 + £14,400 = £68,400; Y = £45,600 + £36,000 = £81,600. X is cheaper by £13,200 — answer B. The structure to internalise: the quality gap (12 percentage points of first-time-fix) applies to the whole volume and multiplies by the downtime cost, while the price gap is just £7 × volume — quality differences compound through consequences, price differences do not. This is vendor selection arithmetic your accountability turns on, and the £30/day downtime figure deserves its own scrutiny in real life — for public-facing caseworkers it is likely an underestimate, which would widen X's advantage further. Cheapest-per-unit is a procurement instinct; cheapest-per-outcome is a service one.

**Question 5 (moderate) — Compliance percentage under scrutiny**

A monthly report states: "Patch compliance improved from 94.0% to 96.0% of in-scope devices." You check the detail: last month 2,256 of 2,400 devices were compliant; this month 2,208 of 2,300 — the scope shrank because 100 "long-offline" devices were reclassified out of scope. How much of the reported improvement is real?

- A) All of it — 96.0% is genuinely higher than 94.0%.
- B) None of it is demonstrated by these figures: compliant devices actually fell (2,256 → 2,208); on last month's constant scope, this month is at best 2,208 + (up to 100 unknown-state devices) of 2,400 — between 92.0% and 96.2% — so the "improvement" rests entirely on removing 100 unknown-state devices from the denominator.
- C) Half of it.
- D) The comparison is impossible in principle.

**Correct answer: B**

**Explanation:** Recompute on a constant basis before crediting any trend. Raw compliant counts fell by 48 (2,256 → 2,208). Held at last month's 2,400 scope, this month's rate is 2,208 ÷ 2,400 = 92.0% if the 100 reclassified devices are non-compliant, up to (2,208 + 100) ÷ 2,400 = 96.2% if they are all somehow compliant — but "long-offline" devices cannot demonstrate compliance, so the honest constant-scope figure trends toward 92%, a two-point decline dressed as a two-point improvement by a denominator change. Option B also names the deeper problem: reclassifying unknown-state devices out of scope is the same epistemic laundering as the conformity report in the cognitive section — offline is where non-compliance lives. Option D overcorrects: the comparison is perfectly possible once the scope is held constant; that is the fix, not the impossibility. The reporting standard this enforces — yours to set, per your reporting and standards skills: any metric whose scope changed reports both the new figure and the constant-scope figure, with the reclassification stated. Denominators are policy decisions wearing arithmetic's clothes; a lead engineer audits them as such.

**Question 6 (moderate) — Release risk arithmetic**

Your release data over a year: normal-track releases: 70, of which 6 caused regression incidents; expedited releases: 30, of which 9 caused regression incidents. A team argues expedited releases are fine because "most regressions (6 is close to 9) come from the normal track anyway... actually more come from expedited, but the tracks are similar in scale." Compute and compare the regression rates, and the expedited track's risk multiple.

- A) Rates: normal ≈ 8.6%, expedited 30% — expedited releases are roughly 3.5 times as likely to cause a regression.
- B) Rates: normal 6%, expedited 9% — expedited is 1.5 times riskier.
- C) The counts (6 v 9) are close enough that the tracks carry similar risk.
- D) Rates cannot be compared across tracks with different volumes.

**Correct answer: A**

**Explanation:** Rate = incidents ÷ releases, per track. Normal: 6 ÷ 70 ≈ 0.086 = 8.6%. Expedited: 9 ÷ 30 = 0.30 = 30%. Risk multiple: 30 ÷ 8.6 ≈ 3.5 — an expedited release is about three and a half times as likely to ship a regression, answer A. Option B divides both counts by the total 100 releases — a mixed denominator that answers no question anyone asked. Option C compares raw counts across unequal volumes, the error the fictional team is half-making; 9 from 30 versus 6 from 70 are not "similar in scale" in any decision-relevant sense. The decision arithmetic this enables: if next year's 30 expedited releases were subjected to normal-track testing, expected regressions fall from 9 to about 30 × 8.6% ≈ 2.6 — roughly six avoided regression incidents, which you can now price against the testing time the fast-track saves. That conversion — from rates, to risk multiple, to avoided incidents, to a priced trade-off — is how release-policy decisions should reach a change board, and producing it is precisely your combination of release-policy ownership and reporting skill.

**Question 7 (moderate) — Acceptance load-test interpretation**

The contracted enrolment volume for your MDM platform is 500 concurrent enrolments. The vendor's load test report shows: at 250 concurrent: mean response 1.1s, 99th percentile 2.0s; at 500: mean 1.9s, 99th percentile 8.5s; at 600: mean 4.2s, 99th percentile 31s, error rate 2%. The contract requires 99th percentile ≤ 5s at contracted volume. What do the figures show?

- A) Pass — the mean at 500 (1.9s) is well under 5s.
- B) Fail at contracted volume — the requirement binds the 99th percentile, which is 8.5s at 500 concurrent; the degradation curve (2.0 → 8.5 → 31s) also shows the system entering non-linear collapse just beyond contracted volume, leaving no headroom.
- C) Pass with caution — only the 600-concurrent figures breach, and 600 exceeds the contract.
- D) The test is invalid because error rates only appear at 600.

**Correct answer: B**

**Explanation:** Bind the requirement to its own metric: 99th percentile ≤ 5s at 500 concurrent; measured, 8.5s — fail, at exactly the contracted condition. Option A substitutes the mean, and the substitution is not innocent: the gap between mean (1.9s) and tail (8.5s) at 500 is the signature of a system beginning to queue — most requests fine, the unlucky tail waiting long — and tails are what percentile requirements exist to police because the 99th percentile is a real user every hundred enrolments. Option C misreads which row breaches: 500 is the contracted volume and it fails on the percentile. The shape adds the strategic finding: tail latency quadrupling from 250→500 (2.0→8.5s) then nearly quadrupling again with 20% more load (31s, plus errors) is a knee in the curve at almost exactly contracted volume — meaning even a "fixed" 4.9s pass at 500 would leave zero growth headroom, worth writing into the acceptance response. Providing authoritative advice on test planning — your testing skill's phrase — sounds exactly like this: the requirement fails on its own terms, and the degradation shape tells you the fix must move the knee, not shave the number.

**Question 8 (moderate) — Budget allocation across preventative options**

You have £40,000 of year-end preventative budget and four costed options: (1) £15,000 — battery replacements for 300 oldest laptops, preventing an estimated 90 failure incidents next year; (2) £25,000 — UPS units for 5 site comms rooms, preventing an estimated 10 outage incidents each affecting ~60 users for ~2 hours; (3) £40,000 — automated test environment for release testing, estimated to prevent 6 regression incidents each affecting ~200 users for ~1 hour; (4) £12,000 — spare-pool expansion cutting repair-loan waits from 3 days to 1 for ~200 users' repairs a year. Using user-hours of disruption avoided per pound as the yardstick, which single option or affordable combination scores highest? (Assume a battery failure costs its user ~4 hours; a repair-loan wait day costs ~2 hours.)

- A) Option 3 alone — it targets the highest-profile incidents.
- B) Options 1 + 2 (£40,000): ≈ 360 + 1,200 = 1,560 user-hours per £40,000 ≈ 0.039 user-hours per pound.
- C) Options 1 + 4 (£27,000): ≈ 360 + 800 = 1,160 user-hours for £27,000 ≈ 0.043 per pound, leaving £13,000 unspent or reallocated.
- D) Options 2 + 4 (£37,000): 1,200 + 800 = 2,000 user-hours ≈ 0.054 per pound.

**Correct answer: D**

**Explanation:** Compute each option's user-hours avoided. Option 1: 90 incidents × 4 hours = 360. Option 2: 10 outages × 60 users × 2 hours = 1,200. Option 3: 6 × 200 × 1 = 1,200 user-hours — for the entire £40,000 alone (0.030/£). Option 4: 200 repairs × 2 days saved × 2 hours/day = 800. Now combine within budget: B (1+2) = 1,560 for £40,000 → 0.039/£. C (1+4) = 1,160 for £27,000 → 0.043/£. D (2+4) = 2,000 for £37,000 → 0.054/£ — the highest yield, and it also leaves £3,000 unspent; answer D. Option A picks by profile, not arithmetic — regression incidents are visible to management, but option 3 is the worst pound-for-pound of the four (though it may still merit next year's core budget on strategic grounds the yardstick ignores: it compounds annually and improves release confidence — a caveat worth one sentence in your recommendation). The method is the message: a common yardstick (user-hours per pound), every option priced in it, combinations checked against the constraint — determine preventative measures, as your problem management skill puts it, done with a spreadsheet instead of an instinct.

**Question 9 (challenging) — Trend decomposition in user satisfaction**

Estate-wide user satisfaction with IT support: Q1 78%, Q2 77%, Q3 76%, Q4 71%. Digging in, you find satisfaction by channel: walk-up desks: steady 85% all year; remote support: steady 74% all year; and the channel mix shifted — walk-up handled 40% of contacts in Q1–Q3 but 15% in Q4 after two desk closures. Which reading is correct?

- A) Support quality deteriorated in Q4 across the service.
- B) Within-channel satisfaction never moved; the Q4 fall is a mix effect — closing desks pushed contacts from the 85%-satisfaction channel to the 74% one. Check: Q4 predicted = 0.15 × 85 + 0.85 × 74 ≈ 75.7%... which overshoots the actual 71%, so the mix shift explains most but not all of the fall — roughly 3 points of the 5-point drop, leaving ~2 points of genuine Q4 decline (or a remote channel strained by its new volume) to investigate.
- C) The mix effect explains the entire fall; no further investigation needed.
- D) Satisfaction data is too subjective to decompose.

**Correct answer: B**

**Explanation:** Run the counterfactual, then respect its residue. Q1–Q3 blended: 0.40 × 85 + 0.60 × 74 = 34 + 44.4 = 78.4% — matching the observed 78–76 band. Q4 with the new mix but unchanged channel quality: 0.15 × 85 + 0.85 × 74 = 12.75 + 62.9 = 75.65% — so the mix shift alone predicts a fall to about 75.7%, explaining roughly 3 points of the observed 5-point drop to 71%. The remaining ~2 points must come from within-channel change the annual "steady" figures may be too coarse to show — most plausibly the remote channel degrading under a doubled load (its 85% of Q4 contacts versus 60% before), which per-month Q4 channel data would confirm. Option C is the sophisticated trap: having found the elegant mechanism, declaring victory before checking whether it covers the magnitude — decomposition is only complete when predicted matches observed. Option A misattributes a mostly-structural effect to quality. The two lead-level lessons: channel-mix arithmetic should be run before any closure decision, not after its satisfaction dip arrives (the 3-point cost was predictable); and every explanation owes you a magnitude check — mechanisms that explain the direction but not the size are partial answers, and the residual is where your next investigation lives.

**Question 10 (challenging) — Licence true-up exposure**

Your desktop-management suite is licensed for 2,200 devices at £48 per device per year. The vendor's annual true-up audits actual deployment; devices over the licensed count are charged retrospectively at 130% of list for the months deployed, then added to the licence base. Inventory shows deployment grew from 2,150 to 2,420 devices linearly over the 12 months just ending. Estimate the true-up charge, and the better strategy for next year.

- A) About £8,000; keep the same licence count since the average deployment (2,285) roughly matches.
- B) About £6,900: deployment crossed 2,200 around month 2–3, averaging ~110 devices over licence for ~10 months; 110 × £48 × 1.3 × (10/12) ≈ £5,700–£6,900 depending on crossing point — and next year's base should be set at the projected year-end count (~2,690 if growth continues), or growth capped, because true-up at 130% makes under-licensing systematically more expensive than honest forecasting.
- C) About £13,700 — all 220 excess devices at full-year premium rate.
- D) Nothing — the vendor must prove deployment monthly.

**Correct answer: B**

**Explanation:** Model the excess as the area between the deployment line and the licence line. Growth: 2,150 → 2,420 is +270 over 12 months (≈ 22.5/month), crossing the 2,200 licence line at about month 2.2. Excess thereafter grows linearly from 0 to 220 over ~9.8 months, averaging ≈ 110 devices. Charge: 110 devices × £48 × 1.30 × (9.8/12) ≈ £5,600–6,900 (sensitivity to the exact crossing month; option B correctly quotes a range with its driver). Option C charges all 220 for a full year — ignoring that the excess ramped from zero; option A's average-of-endpoints (2,285) misprices both the excess and the exposure. The strategic half matters more than the arithmetic: the 130% multiplier is the contract telling you that under-forecasting is the expensive habit — at 30% premium, licensing to your honest year-end projection beats true-up whenever growth is even roughly foreseeable, and your inventory data (accurate information, per your asset and configuration skill) is exactly what makes it foreseeable. A lead who brings the deployment curve to the renewal conversation prices the licence; one who doesn't gets priced by the audit.

**Question 11 (challenging) — Presenting uncertainty honestly**

Your Windows upgrade programme must complete by a support-expiry date 40 weeks out. Progress: 4 weeks in, 360 of 3,600 devices upgraded — but week-by-week: 60, 80, 100, 120. The programme manager asks for a completion forecast for the board: "one number, please." What is the most professionally honest response?

- A) "Week 40 exactly — 3,600 ÷ 90 average per week = 40 weeks."
- B) "Week 36" — extrapolating the +20/week acceleration: cumulative upgrades reach 3,600 around week 22 if acceleration continues, so quote week 22 with confidence.
- C) Give the range with its logic and a recommendation: "At the current 120/week steady rate, remaining 3,240 devices take 27 more weeks — completion week 31. If early acceleration continues to a plateau of ~150/week, week 26–27. If the tail behaves like every estate tail — the last 10% (offline, exotic, refusing devices) moving at half rate — add 3–4 weeks: realistic band week 30–35 against a week-40 deadline; adequate buffer, but the tail-device identification should start now. If the board needs one number: week 33, with the band stated in the notes."
- D) "It cannot be forecast this early."

**Correct answer: C**

**Explanation:** Audit each forecast's model. Option A divides by the 4-week average (90/week) — but the series 60, 80, 100, 120 is not a flat 90; averaging a ramp misprices the current run-rate (already 120) and coincidentally lands on the deadline, a comfort answer with two errors cancelling. Option B extrapolates the +20/week acceleration indefinitely — early-programme acceleration is ramp-up (scheduling, comms, engineer familiarity) and plateaus; compounding it to week 22 is fantasy planning. Option C builds the forecast from mechanisms: current rate as the base case (3,240 ÷ 120 = 27 weeks → week 31), a plateau scenario, and — the professionally distinctive element — the estate-tail correction, because the last devices are always the slowest and every experienced lead knows it; then it answers the actual question ("one number: week 33") without hiding the band, and converts the forecast into action: start tail identification now, while the buffer exists. Option D refuses a forecast the data adequately supports. This is interpreting a data set and communicating it to others at board altitude: models named, band stated, single number supplied on request with its caveat attached — and the forecast used to change the plan, not just predict it.

### Preparation tips

- **Convert every contract percentage into its unit allowance.** 99.5% availability is 79 minutes a month; a 0.1-point credit band is a rounding rule. Numbers you have pre-converted are numbers you control in reviews — practise on your own contracts.
- **Hold denominators constant before crediting trends.** Scope changes, reclassifications and "in-scope device" redefinitions manufacture improvements. Recompute on last period's basis first, every time.
- **Price both sides of every ledger.** Unit savings versus quality-consequence costs; licence savings versus site-visit hours; testing time versus avoided regressions. The offered comparison is usually half a comparison — completing it is the lead's contribution.
- **Check explanations for magnitude, not just mechanism.** A mix effect that explains 3 points of a 5-point fall leaves 2 points unexplained. Predicted-versus-observed is the completeness test; residuals are assignments.
- **Forecast from mechanisms, not curve-fits.** Run-rates, plateaus and estate tails are real; indefinite acceleration is not. Quote bands with drivers, and give the single number with its band attached when asked.
- **Interrogate the metric's percentile.** Means reassure; tails bind. Whenever a requirement or SLA names a percentile, check that the evidence reports that percentile — substitution is the commonest flattering error in vendor test data.

### Common pitfalls to avoid

- **Accepting the presenter's denominator.** Vendors, teams and proposals all choose the division that flatters. Ask what was excluded from the bottom of every fraction — offline devices, blocked tests, reclassified scope.
- **Comparing counts across unequal volumes.** Six regressions from seventy releases versus nine from thirty is a 3.5× rate difference wearing a "similar counts" disguise. Divide first.
- **Means where tails bind.** A 1.9s mean at a 5s 99th-percentile requirement showing 8.5s is a fail — and the mean-tail gap is itself diagnostic of queueing collapse. Read the metric the requirement names.
- **Forgetting populations age during the plan.** Refresh backlogs, licence counts and compliance scopes all move while budgets execute. Count the cohort that crosses the threshold mid-year.
- **Extrapolating ramps.** Early acceleration plateaus; estate tails drag. The two corrections pull opposite ways — apply both before quoting completion dates.
- **Stopping at the elegant explanation.** The mix effect, the supplier's excuse, the first mechanism that fits the direction — check it covers the size. Explanations that pass the magnitude test are findings; the rest are hypotheses.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret and draw conclusions from written material — using the documents a lead end user computing engineer genuinely works with: supplier contracts and advisories, release and security policies, architecture papers, audit findings, procedures you draft and others follow, and the correspondence through which vendors, teams and stakeholders position themselves.

The typical format is an online, timed test of 15 to 25 minutes: a passage, then structured questions — predominantly **true / false / cannot say** (is the statement guaranteed, contradicted, or unaddressed by the passage?), plus best-summary, best-draft and two-document reconciliation items. The governing rule is constant: answer from the text alone, however experienced your instincts.

At lead level, reading is a commercial and governance skill as much as a technical one. Contracts mean exactly what their clauses say, and the difference between "reasonable endeavours" and "shall" is the difference between a request and an obligation. Vendor advisories are drafted by people managing liability as well as informing customers — their hedges are load-bearing. Audit findings, policies and standards operate on precise definitions where a misread scope clause becomes an estate-wide exposure. And the documents you produce — procedures, standards, escalations, reports — are read by engineers, suppliers and boards who will act on precisely what you wrote rather than what you meant: your technical specialism's mandate to draft and maintain procedures and documentation makes you an author whose readers include auditors. The assessment rewards disciplined extraction, sensitivity to hedged and obligated language, and the ability to reconcile documents that disagree.

### How this assessment maps to your role

- **Contract and obligation reading** maps to your **vendor and supplier management** accountability: distinguishing "shall" from "should" from "reasonable endeavours", and tracking definitions, exclusions and remedy clauses, is the reading half of holding suppliers to account.
- **Policy and standards precision** maps to your **Change management** skill (ensure that release policies, procedures and processes are applied) and your **Technical specialism** (set standards and ensure conformity): enforcement begins with exact comprehension — including of documents you wrote months ago.
- **True/false/cannot-say discipline** maps to your **Problem management** and **Incident management** skills: leading investigations fairly means holding the line between what evidence states, what parties claim, and what remains open — especially when vendors' statements are engineered to blur it.
- **Reconciling conflicting documents** maps to your **Service focus** and framework knowledge: groups of services generate overlapping policies, advisories and contracts; precedence, dates and scope decide, and your **ITIL life-cycle knowledge** supplies the vocabulary.
- **Summary and drafting judgement** maps to your **IT service reporting** skill and your **User focus**: representing users internally and reporting to stakeholders both mean compressing without distorting — and recognising drafts that spin, bury or blame.

### Practice questions

**Question 1 (easy) — Obligation language in a contract**

A support contract states: "The Supplier shall resolve Priority 1 incidents within 4 hours. The Supplier shall use reasonable endeavours to resolve Priority 2 incidents within 8 hours. Where on-site attendance is required, the Customer shall provide site access within 1 hour of request; resolution clocks are suspended until access is provided."

Statement: "If the supplier misses an 8-hour Priority 2 resolution despite genuine effort, the supplier has breached the contract."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The P2 obligation is "reasonable endeavours to resolve... within 8 hours" — an effort standard, not an outcome guarantee. A miss despite genuine effort is compatible with full compliance; contrast the P1 clause's bare "shall resolve within 4 hours", which is an outcome obligation where a miss is a breach regardless of effort. The statement asserts breach from a P2 miss with genuine effort — the clause's own structure contradicts it: false. Note also the third sentence's trap for your own side: the access obligation runs against the Customer, and clock suspension means a slow site-access process converts supplier misses into your misses. Reading contracts as a lead means mapping which party each "shall" binds and which obligations are outcome versus effort — the two-minute exercise that determines what a supplier review can actually demand, and what the supplier will point at when you demand it.

**Question 2 (easy) — A vendor advisory's hedges**

An advisory reads: "We have identified a potential issue affecting a limited number of devices running firmware 3.1 in conjunction with certain third-party encryption products. Customers may experience unexpected shutdowns. We recommend affected customers consider upgrading to firmware 3.2. Firmware 3.2 has completed internal validation; broad field data is not yet available."

Statement: "The vendor states that firmware 3.2 resolves the shutdown issue."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Search the passage for a resolution claim — there is none. The vendor "recommends" that affected customers "consider" upgrading (a hedged suggestion, two modals deep), and says 3.2 "has completed internal validation" with "broad field data not yet available" — a testing status, not a fix claim. Nowhere does the text state 3.2 resolves, addresses or fixes the shutdowns; equally, nothing denies it. Cannot say. The advisory is a masterclass in liability-managed drafting — "potential issue", "limited number", "certain third-party products", "may experience" — every noun hedged, and the recommendation carefully stopping short of a promise. The operational consequence of reading it correctly: before rolling 3.2 across your estate you would demand the missing sentence from the vendor ("does 3.2 remediate the shutdown mechanism — yes or no?") or pilot for the specific symptom, because your rollout justification currently rests on a fix claim the vendor conspicuously declined to make. Vendors' omissions are as informative as their statements; a lead reads both.

**Question 3 (easy) — Scope of an audit finding**

An audit report states: "Finding 3 (Medium): Local administrator passwords on sampled devices in Buildings A and B (n=40) had not been rotated within the 90-day policy period; 12 of 40 sampled devices were non-compliant. The audit did not test devices in Buildings C–F. Management response due within 30 days."

Statement: "The audit found that 30% of the estate's devices have non-compliant local administrator passwords."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The finding establishes 12 of 40 = 30% non-compliance within a sample drawn from two buildings, and explicitly excludes Buildings C–F from testing. The statement generalises the sample rate to "the estate's devices" and attributes that generalisation to the audit — but the audit made no estate-wide claim; it carefully bounded its own scope. The statement therefore misdescribes what the audit found: false. (A statement that "30% of estate devices are non-compliant" without the "audit found" wrapper would be cannot-say — possibly true, but not established; the attribution to the audit is what makes this one false.) The management-response discipline follows the same logic in reverse: your response should address the sampled buildings' remediation and the unsampled buildings' verification — because the honest reading of a bounded finding is "30% where we looked, unknown where we didn't", and treating unsampled as unaffected is exactly the error your conformity-report question punished. Audit literacy — scope, sample, population — is contract literacy's sibling, and both are lead-level reading.

**Question 4 (moderate) — Precedence between policy and contract**

Document 1 (your organisation's security policy, updated last month): "Remote access software on managed devices must be configured to require multi-factor authentication. No exceptions."
Document 2 (supplier contract, signed two years ago): "The Supplier's remote diagnostic tool will be deployed on managed devices per Appendix D. The Customer shall not modify the tool's authentication configuration, which is centrally managed by the Supplier. The Supplier's tool currently authenticates via certificate-based single factor."

Statement: "The two documents place the organisation under conflicting obligations regarding the supplier's tool."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Extract each obligation. The policy: all remote access software on managed devices must require MFA, no exceptions — which includes the supplier's tool on those devices. The contract: the Customer shall not modify the tool's authentication configuration, which is single-factor. The organisation is simultaneously obliged to ensure MFA (policy) and forbidden from imposing it (contract): a genuine conflict — true. Neither document resolves it: the policy's "no exceptions" forecloses the easy out, and the contract's modification bar sits with the supplier. What the conflict generates is lead-level work: the resolution routes are commercial (negotiate the supplier's roadmap to MFA — likely a contract variation), procedural (a formally-governed policy exception with compensating controls, if your governance allows what the policy says it doesn't), or architectural (network-level controls wrapping the tool). Spotting that a conflict exists — rather than assuming one document silently wins — is the tested skill: policies do not override contracts by being newer, and contracts do not override policies by being signed; conflicts are surfaced, escalated and resolved explicitly. In your role the reflex should be to find these at policy-update time, not at audit time.

**Question 5 (moderate) — What a supplier's RCA actually concedes**

A supplier's root-cause analysis reads: "The service interruption of 14 May resulted from an unanticipated interaction between a scheduled maintenance script and a database index rebuild. Our monitoring detected elevated error rates within 4 minutes. Contributing factors included an atypical data volume in the Customer's tenant. Process improvements have been identified, including enhanced pre-maintenance checks. We consider this a one-time event."

Statement: "The supplier accepts that its own maintenance process caused the interruption."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Strip the drafting to its assertions. The interruption "resulted from an unanticipated interaction between a scheduled maintenance script and a database index rebuild" — both components are the supplier's own operations; the sentence attributes causation to them, however passively voiced. The "contributing factor" (your tenant's "atypical data volume") is positioned to share blame but is explicitly subordinate — a condition, not the stated cause. And "process improvements have been identified, including enhanced pre-maintenance checks" concedes the process was improvable — you do not enhance checks for processes that worked. So the passage does accept, in engineered language, that the supplier's maintenance caused the event: true. The lead skill is reading past voice and framing to the admission structure: passive constructions ("resulted from", "have been identified") and blame-sharing garnish are how RCAs concede liability without conceding it loudly. The follow-through at the service review: accept the RCA's causal admission on the record, test the "one-time event" claim against the improvement list (four improvements for a one-time event is a tension worth naming), and convert "identified" improvements into dated, verifiable commitments — because "identified" is not "implemented", and that gap is where repeat incidents live.

**Question 6 (moderate) — Best summary for a governance board**

You must summarise this situation for a governance board: your estate's remote-support licence renewal is 10 weeks out; architecture proposes migrating to a platform-native tool saving £60,000/year; your analysis shows the native tool lacks unattended kiosk access, costing an estimated £36,000–48,000/year in engineer travel plus public kiosk downtime; the vendor's roadmap lists the gap "under consideration"; a hybrid (minimal licence retention for kiosks) captures most savings. Which summary is best?

- A) "Architecture and IT operations disagree on the remote-support migration; the board is asked to adjudicate between the two positions."
- B) "Migrating fully to the native tool saves £60,000/year but removes unattended kiosk support, whose loss we cost at £36,000–48,000/year plus public-facing downtime — a marginal-to-negative net. A hybrid retaining ~40 kiosk licences captures an estimated £45,000 of the saving with no capability loss. Recommendation: approve the hybrid now; revisit full migration if the vendor's roadmap delivers unattended access. Decision needed within 6 weeks for renewal lead-time."
- C) "The native tool is inadequate for operational needs and the migration should be rejected until the vendor's product matures."
- D) "Both options have merits and risks which the attached 14-page analysis details for the board's consideration."

**Correct answer: B**

**Explanation:** A governance summary is judged by whether the board can decide correctly from it alone. Option B carries the five load-bearing elements: both sides of the ledger quantified (the £60,000 and its £36,000–48,000 offset — the honest net), the hybrid option with its arithmetic, a recommendation (boards act on recommendations, not menus), the condition under which the decision should be revisited (roadmap delivery — keeping the door open architecture wants open), and the deadline with its driver (renewal lead-time). Option A presents the disagreement instead of the analysis — asking the board to adjudicate positions rather than evidence, which wastes governance on work you should have finished. Option C is your conclusion without your ledger, and its framing ("inadequate", "rejected") burns the architecture relationship a hybrid preserves. Option D delegates reading to the board — attachment-shaped abdication. The drafting principle, which is your reporting skill at governance altitude: quantified net, recommended action, revisit condition, deadline — four sentences that let a board be as smart as your analysis. And note B's diplomatic structure: it adopts architecture's goal (savings) and shows the route that survives operational arithmetic — summaries that let both proposers win the right way get implemented.

**Question 7 (moderate) — A procedure's failure mode**

You are reviewing a draft procedure written by one of your senior engineers: "Decommissioning a laptop: 1. Confirm the user has migrated their data. 2. Remove the device from management systems. 3. Initiate certified data wipe. 4. Record the wipe certificate ID in the asset register. 5. Update the asset status to 'Disposed' and arrange collection. Note: for devices that fail to boot, steps 1 and 3 may be skipped; physical destruction via the disposal vendor applies instead."

Statement: "Under this procedure as drafted, a non-booting laptop's disposal is recorded with a wipe certificate ID."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Trace the non-booting path: steps 1 and 3 are skipped; physical destruction applies. Step 4 records "the wipe certificate ID" — but no wipe occurred, so there is no wipe certificate; and the note, having redirected to physical destruction, is silent about what step 4 becomes on that path. As drafted, the non-booting laptop cannot be recorded with a wipe certificate ID — the statement is contradicted by the procedure's own structure: false. And that contradiction is the draft's defect, which your review should catch: the destruction path generates a different evidence artefact (a destruction certificate from the disposal vendor) that the procedure never tells anyone to obtain or record — so non-booting devices, the ones whose data was never wiped, are precisely the ones that exit the estate with no recorded evidence of data destruction. This question is your documentation duty exercised as reading: drafting and maintaining procedures means walking every branch to its record-keeping end, because branches that skip steps also skip the steps' evidence unless the author says otherwise. Procedures fail at their exceptions; audits look there first, and so should your review.

**Question 8 (moderate) — Representing users against a desire**

A directorate head writes: "My caseworkers want the new lightweight laptops — the current ones are heavy and everyone's asking when they'll get the thin ones the executive team has. Please prioritise our directorate for the next refresh." Your user research data on that directorate shows: top pain points are 40-second login times (raised by 71% of surveyed caseworkers), document-system crashes (58%), and — seventh on the list — device weight (18%). The lightweight model has a smaller battery and weaker performance against the login and crash issues.

Statement: "The directorate head's request, if fulfilled, would address the directorate's main evidenced user needs."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Set the request against the evidence. The evidenced needs rank login delay (71%) and application crashes (58%) far above weight (18%, seventh); the requested lightweight model does not address the top two and — with weaker performance — plausibly worsens them. Fulfilling the request therefore would not address the main evidenced needs: false, on the data given. This is the user-needs-versus-desires distinction your user focus skill names explicitly — the desire (thin laptops like the executives') is real and reported honestly by the directorate head; the needs (fast login, stable documents) are what the research evidences; and the two point at different purchases. The lead move this sets up: respond to the directorate head with the research — "your caseworkers' top issues are login and crashes; the thin model would not help those and may worsen them; here is what we propose for each, and where weight genuinely binds (frequent travellers), a targeted lightweight allocation" — which represents users internally better than either compliance or refusal. Champion the research, translate desire into the need beneath it (status? portability for a mobile subset?), and spend the refresh where the 71% lives.

**Question 9 (challenging) — Reconciling three documents in an incident**

Document 1 (release policy): "Rollbacks of security patches require security-team approval, obtainable via the emergency channel at any hour."
Document 2 (last night's release record): "Patch KB-4471 deployed estate-wide 22:00. Post-deployment checks green 23:30."
Document 3 (this morning's incident channel, service desk manager, 08:40): "Widespread reports: shared-drive access failing since ~08:15. Timing points at last night's patch. Per my authority as incident lead, roll back KB-4471 now — we'll square paperwork later."

Statement: "Following the service desk manager's instruction as given would breach the release policy."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The policy conditions security-patch rollbacks on security-team approval — with an emergency channel expressly provided for speed at any hour. The instruction orders rollback "now", explicitly deferring authorisation ("square paperwork later"), and incident-lead authority is not security-team approval — nothing in the three documents grants the service desk manager that power. Executing the instruction as given would therefore breach the policy: true. Note what makes the reasoning fair rather than obstructive: the emergency channel means compliance costs minutes, not hours — the policy anticipated exactly this morning, so "policy or speed" is a false choice; the lead response is to trigger the emergency approval immediately (and in parallel sanity-check the causal claim: green checks at 23:30 versus failures from 08:15 leaves nine quiet hours — a gap worth one diagnostic question, since rollbacks of security patches carry their own risk and the timing correlation is looser than the channel message assumes). The tested skill is triple: extracting the approval condition, refusing to let asserted authority substitute for documented authority, and noticing that well-designed policies usually contain their own fast path — which is also a standard you apply when you draft them.

**Question 10 (challenging) — An architecture paper's load-bearing assumption**

An architecture options paper argues: "Option B (thin-client estate) reduces endpoint incidents by an estimated 60%, based on Reference Organisation R's results. R's deployment covered call-centre staff with fixed desks, standardised applications and constant connectivity. Our estate serves 40% mobile and field workers, 200+ line-of-business applications, and sites with intermittent connectivity. We therefore recommend Option B for the full estate, projecting a 60% incident reduction."

Statement: "The paper's own description of the two estates undermines applying R's 60% figure to the full estate."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The 60% transfers only if the estates are relevantly similar — and the paper itself lists the dissimilarities that matter most for thin clients: R was fixed-desk, standardised, always-connected; yours is 40% mobile/field, 200-application, intermittently connected. Thin clients' benefits depend on connectivity and standardisation — precisely the properties your estate lacks in the segments described — so the paper documents the defeater of its own projection while making it: true. (Compare the field-tool proposal pattern from mid-level materials: pilots generalise along their mechanisms, and mechanisms are environment-bound.) The lead-level response the reading sets up is constructive scoping, not rejection: R's conditions do hold for your fixed-desk 60% — a segmented Option B (thin client where its mechanism exists; managed laptops for mobile/field) could honestly claim a large share of the benefit, with the projection re-based on the covered segment only. This is feasibility work with architecture as your role defines it: your contribution is knowing which estate realities break which architectural assumptions, stated as segmentation arithmetic rather than resistance — the difference between operations as veto and operations as design input.

**Question 11 (challenging) — Drafting the message after a supplier failure**

Your repair supplier missed contracted turnaround on 40% of last month's repairs, including several for assistive-technology users left without adapted equipment. The supplier's account manager, with whom relations are otherwise productive, has emailed: "A rough month — new depot bedding in. Trust we can handle this pragmatically rather than formally." You must reply, copying your service desk manager. Which draft is best?

- A) "Thanks for the context — these things happen. Let's keep an eye on it and hope the depot settles."
- B) "This is a formal notification of material SLA breach. All contractual remedies are reserved. Our commercial team will be in touch regarding termination provisions."
- C) "Last month's 40% turnaround failure is a material breach, and its user impact was severe — including assistive-technology users left without adapted equipment, which we treat with particular seriousness. We're applying the contractual service credits for the month; that is the formal position and it stands. In parallel: we value the relationship and accept depots bed in — so let's meet this week with your depot recovery plan, weekly turnaround data until performance re-stabilises, and expedited handling as standard for assistive-technology repairs. Handled that way, this stays a recovered blip rather than a pattern."
- D) "We are disappointed by last month's performance and expect improvement going forward."

**Correct answer: C**

**Explanation:** The account manager's email is a bid to convert a contractual breach into a relationship favour — "pragmatically rather than formally" means "without credits or record" — and each weak option mishandles the bid differently. Option A grants it: remedies waived, no recovery mechanism, and a precedent that breaches cost apologies; it also silently accepts the harm to assistive-technology users, which your user focus cannot let pass as rounding error. Option B swings to maximal formality — reserving termination language over one bad month torches a productive relationship and, tellingly, requests no recovery plan: it punishes without fixing. Option D is disappointment-shaped nothing: no remedy, no plan, no data, no date. Option C separates the layers professionals keep separate: the formal layer (breach named, credits applied — not negotiable, and applying them this month is what keeps "part thereof" clauses respected next month), the impact layer (assistive-technology users named specifically, with an expedite as the structural fix), and the relationship layer (bedding-in acknowledged, recovery plan and weekly data as the pragmatism actually worth offering). The closing line gives the account manager the story to sell internally — recovered blip versus pattern — which is influence, not concession. Vendor management in writing is exactly this register: warm, specific, and never at the expense of the remedy the contract exists to provide.

### Preparation tips

- **Build an obligation-language glossary.** "Shall" (outcome duty), "reasonable endeavours" (effort duty), "may" (discretion), "part thereof" (rounding direction), "recommend considering" (no promise), "identified" (not implemented). Read one real contract schedule against it — the assessment's contract questions are drawn from exactly these distinctions.
- **Read scope and sample clauses first.** Audits, advisories and test reports bound their own claims — "sampled devices", "Buildings A and B", "internal validation". The generalisation the question offers usually exceeds the bound the passage set.
- **Trace every procedural branch to its evidence.** For each exception path in a procedure ("if the device fails to boot..."), ask what record it produces. Branches that skip steps skip records — in draft reviews and in test questions alike.
- **Extract admissions from engineered prose.** Practise rewriting one vendor RCA or advisory into plain assertions: who caused what, what is promised, what is merely "identified". The passive voice dissolves under the exercise, and so do the questions built on it.
- **Reconcile document pairs deliberately.** Take a policy and a contract that touch the same system and hunt the conflict. Finding "the two documents disagree" is a legitimate — and frequently correct — reading; practise recognising when neither text wins.
- **Draft, then audit for layers.** In your next difficult message, check the formal position, the impact statement, and the relationship move are each present and separate. The best-draft questions score exactly that separation.

### Common pitfalls to avoid

- **Upgrading hedges into promises.** "Recommend considering an upgrade" plus "internal validation complete" is not "this fixes it". Vendors omit the fix claim deliberately; readers who supply it fail the question and, later, the rollout.
- **Letting samples speak for populations.** 30% of forty devices in two buildings is not 30% of the estate — and attributing the generalisation to the auditor is false, not cannot-say. Track who claims what, at what scope.
- **Assuming the newer or louder document wins.** Policies and contracts conflict without resolving; asserted authority is not documented authority. The correct reading is often "these obligations collide" — say so.
- **Reading past the evidence gap.** "Approval obtainable via the emergency channel" means the speed-versus-policy dilemma is false; "square paperwork later" means the instruction breaches anyway. Both halves matter.
- **Choosing drafts that pick one layer.** Pure formality burns relationships; pure warmth waives remedies; pure disappointment does nothing. Scored drafts hold remedy, impact and relationship simultaneously.
- **Forgetting your own authorship.** Procedures, standards and reports you wrote are read as exactly as contracts you sign. The evidence-less branch and the scope-less claim are as likely to be yours as the supplier's — audit your documents the way these questions audit others'.

<!-- APPEND -->
