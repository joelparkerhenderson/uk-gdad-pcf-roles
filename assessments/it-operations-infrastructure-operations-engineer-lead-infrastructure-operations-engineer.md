# Lead Infrastructure Operations Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a lead infrastructure operations engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, pursuing a promotion or a move, benchmarking your own capability, or calibrating what you expect of the engineers whose development you manage, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. At lead level, that means something quite specific. The assessments described here are job-specific: they draw on the artefacts you genuinely handle — team workload and performance data, supplier service reports and contract schedules, release and test plans, architectural options papers, high-impact change requests, budgets and capability plans — and the judgements you genuinely make: balancing service obligations against team sustainability, holding suppliers to contractual and regulatory requirements, deciding which changes proceed and which wait, and building the capability that lets your team deliver services as required.

Why do these assessments matter for your role in particular? Because leadership in operations is a reasoning discipline as much as a people discipline. You manage the operational support of IT solutions and services — which means reading service data accurately and acting on what it actually says. You manage the workload, performance and development of a team of IT operations specialists — which means allocating finite capacity against competing demands, spotting the trends in team data that precede burnout or backlog, and making development decisions that compound over years. You manage third-party provision of IT operations services — which means precise reading of contracts, service credits, and supplier reports, and the numeracy to challenge a supplier's own figures. You manage the provision of expertise to programmes and projects, and the development of architectural solutions across the service life cycle — which means evaluating options papers, test plans, and impact assessments with the rigour of someone whose sign-off carries weight. Cognitive, numeric, verbal, and situational assessments map directly onto those demands.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters at your level, a mapping of the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. Attempt every question honestly, committing to an answer before reading the explanation. Treat the explanations as technique made explicit — at lead level, the margin lies in disciplined method and in judgement under ambiguity, and the walkthroughs surface both. Read with two hats: as a candidate sharpening your own performance, and as a leader who develops others — much of this material converts directly into coaching conversations, team exercises, and the standards you set for escalations, reports, and assessments that cross your desk. Finally, revisit the material after a few weeks; judgement, like any capability, consolidates through spaced practice.

The questions progress from easy through moderate to hard within each section, and the hard questions are genuinely hard — as they should be, because your role is where the difficult calls land. Take your time, work honestly, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using practical scenarios rather than abstract puzzles. For a lead infrastructure operations engineer, the scenarios centre on the reasoning of operational leadership: reading patterns in team and service data, tracing the consequences of high-impact changes through technical and organisational dependencies, spotting the inconsistency in a supplier report or a release plan, and sequencing competing work under interacting constraints of capacity, risk, and obligation.

The typical format is an online, timed test lasting 15 to 30 minutes, with 20 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group; adaptive difficulty is common, and employers typically see accuracy and speed separately. Ungraded practice questions usually precede the scored test.

At lead level, cognitive assessment measures something your role exercises constantly but rarely names: the ability to reason correctly about systems you no longer touch directly. Your engineers run the tools; you run the picture. That means your raw material is largely second-hand — dashboards, reports, escalation summaries, supplier figures — and your value lies in reading it critically: noticing the trend beneath the noise, the claim that does not follow from its evidence, the dependency nobody mapped, the queue that is quietly becoming a crisis. Leading the investigation and resolution of incidents means directing reasoning as much as performing it: knowing which questions cut fastest, which evidence discriminates between hypotheses, and when a confident narrative is outrunning its facts. Being proactive in searching for potential problems — your ownership skill's explicit demand — is pattern recognition pointed at the future. A well-designed cognitive assessment reproduces all of this in miniature, and practising it sharpens exactly the critical reading that operational leadership consists of.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Problem management** skill (initiating and monitoring actions to investigate patterns and trends) and to your **Ownership and topic** duty to be proactive in searching for potential problems — reading team, service, and supplier data for the signal that precedes the incident.
- **Logical deduction** maps to your **Incident management** skill of leading investigation and resolution — directing hypothesis-driven diagnosis — and to your **Change management** skill of managing high impact, complex change requests, where consequences must be reasoned out before they occur.
- **Error checking** maps to your **Asset and configuration management** skill (secure configuration, accurate information), your **Technical specialism** duty to set standards for definition, security and integrity of objects and ensure conformity, and your **Testing** skill of providing authoritative advice on test planning — authority rests on catching what others miss.
- **Prioritisation** maps to your duty to manage the workload, performance and development of a team — allocating scarce specialist capacity — and to your **Availability and capacity management** responsibility for keeping service components against business needs and KPIs.
- **Applied problem solving** maps to your duty to manage the development of architectural solutions for IT operations throughout the service life cycle, your **Service focus** skill of establishing coherent frameworks that work, and your **Coding and scripting** capability to interact with, read and write code when the situation demands direct verification.

### Practice questions

**Question 1 (easy) — Pattern recognition in team workload data**

Your team's weekly ticket closure and intake figures over six weeks:

| Week | Intake | Closures |
|---|---|---|
| 1 | 110 | 112 |
| 2 | 115 | 114 |
| 3 | 118 | 113 |
| 4 | 124 | 110 |
| 5 | 129 | 106 |
| 6 | 133 | 101 |

What pattern most warrants your attention as team lead?

- A) Closures are stable, so the team is performing consistently.
- B) Intake is rising while closures are falling — the gap is widening each week, so backlog is accelerating and the team's capacity is diverging from demand.
- C) Week 1 shows closures exceeding intake, which suggests over-capacity.
- D) The figures are within normal variation and need no action.

**Correct answer: B**

**Explanation:** Compute the weekly balance (closures minus intake): +2, −1, −5, −14, −23, −32. The gap is not just negative — it is widening at an increasing rate, which means backlog is compounding: roughly 73 tickets of net backlog have accumulated over five weeks, most of it recent. Option A misreads falling closures (112 → 101) as stability; option C over-interprets a single balanced week; option D ignores a second-difference trend that will not self-correct. The leadership content is in what the pattern implies: falling closures against rising intake suggests either demand change (something upstream is generating tickets — a problem investigation candidate), capacity change (absence, attrition, a hidden workload like a project drawing your engineers), or both. The lead's move is to decompose the trend before reacting to it — more overtime against a demand-driven surge fixes nothing. Managing team workload starts with reading workload data the way you would read a capacity graph: trends and second differences, not snapshots.

**Question 2 (easy) — Deduction from a release policy**

Your release policy states: "A release containing database schema changes must be deployed with a tested rollback script, and must not share a release window with any other schema-changing release." Release R1 contains schema changes and is scheduled for Saturday's window. Release R2 is scheduled for the same window. Which conclusion must be true?

- A) R2 does not contain schema changes, or the policy is being breached.
- B) R2 does not contain schema changes.
- C) R2 has a tested rollback script.
- D) The Saturday window must be cancelled.

**Correct answer: A**

**Explanation:** The policy forbids two schema-changing releases sharing a window. R1 changes schemas and occupies Saturday. If R2 also changes schemas, the policy is breached; if it does not, the schedule is compliant. The facts given do not say which — so B asserts more than is known, C attaches R1's rollback obligation to R2 without knowing R2's content, and D invents a remedy no rule requires. Only the disjunction in A must be true. This is the reasoning shape of release governance: ensuring that release policies, procedures and processes are applied — your change management skill — is largely the discipline of converting policy plus partial facts into exactly the right question ("does R2 touch schemas?") rather than a premature conclusion. Leads who deduce precisely ask fewer, sharper questions — and their release reviews are faster and safer for it.

**Question 3 (easy) — Error checking a supplier service report**

Your storage supplier's monthly report states: "Availability: 99.92% (21 minutes downtime). Incidents: 2 (both Severity B). All contractual targets met. Note: the 14th's four-hour degradation of the replication service is excluded from availability figures as it affected a secondary function." Your contract defines availability across all contracted services, including replication, with no exclusion clause for secondary functions. What is the report's key defect?

- A) The downtime arithmetic: 99.92% of a month is not 21 minutes.
- B) The supplier has unilaterally excluded a four-hour degradation from availability, but the contract contains no such exclusion — so the availability figure and possibly the "targets met" claim do not follow from the contract's own definition.
- C) Two incidents in a month is above acceptable norms.
- D) Severity B is the wrong classification for a degradation.

**Correct answer: B**

**Explanation:** Check the claims against their governing document. The report's headline figures depend on an exclusion ("secondary function") that the contract — the only document that defines availability for contractual purposes — does not contain. Including four hours (240 minutes) of degradation would move measured downtime from 21 minutes toward 261, pulling availability below 99.4% and likely breaching the target the report claims is met. Option A is the decoy: 0.08% of a 30-day month (43,200 minutes) is about 34.6 minutes, so 21 minutes is arithmetically consistent with a slightly better figure — approximately 99.95% — a minor rounding-style discrepancy worth a query, but not the structural defect. Options C and D substitute your judgement for contractual terms without basis. Managing third-party provision — your role's explicit duty — turns on exactly this reading: suppliers report their own performance, definitional drift flatters the numbers, and the lead who reconciles reports against contract definitions is the control. The follow-up is procedural, not personal: query the exclusion in writing, request restated figures, and check whether service credits are triggered.

**Question 4 (easy) — Prioritising your own attention**

It is Monday 09:00. Four items compete for your attention as lead:

1. A P1 is running: payroll interface down, your most experienced engineer leading it competently; last update 15 minutes ago, next expected in 15.
2. Your director's office asks for a briefing note on Friday's supplier outage by 12:00 — you have the facts.
3. A junior engineer is scheduled for their fortnightly development one-to-one at 09:30.
4. The change board meets at 10:30 and two of your team's high-impact change requests need your final review before submission.

What is the most defensible allocation of your next 90 minutes?

- A) Take over the P1 personally — nothing else matters during a P1.
- B) Confirm the P1 lead has what they need and hold the update cadence; write the director's note; review the change requests before 10:30; move the one-to-one to later today with an apology and a firm new time.
- C) Hold the one-to-one as scheduled — development commitments must never move — then do the note and reviews afterwards.
- D) Delegate the director's note to the engineer leading the P1, freeing you for the reviews and the one-to-one.

**Correct answer: B**

**Explanation:** The P1 tests a lead's discipline in the opposite direction from instinct: a competent engineer is leading it well on a healthy update cadence, so the leadership action is support and monitoring, not seizure — taking over (option A) undermines the engineer, signals distrust, and leaves the lead-level obligations (governance, upward communication) undone. Option B sequences the genuinely time-bound items: the director's note (hard 12:00 deadline, and upward communication during service issues is lead work), the change reviews (hard 10:30 gate, and unreviewed high-impact changes either miss the board or enter it unexamined — both bad), and the P1 cadence (a monitoring commitment throughout). The one-to-one moves — with an apology and a firm rebooking, which is the difference between deferring development and deprioritising it; a same-day reschedule honours the commitment while acknowledging that two hard deadlines and a P1 outrank a movable meeting. Option C treats the development commitment as immovable in a way that costs two hard deadlines; option D loads administrative work onto the person running a P1 — the one team member whose attention you should be protecting. Lead-level prioritisation questions test exactly this: distinguishing what only you can do (governance, upward comms, reviews carrying your authority) from what your team is already doing well.

**Question 5 (moderate) — Deduction through an architectural dependency**

An options paper proposes consolidating three services' file storage onto a single new platform. Facts: (i) Service A requires data residency in UK data centres; (ii) Service B's contract with its business owner guarantees restoration of any file within 4 hours; (iii) Service C generates 80% of total I/O load; (iv) the proposed platform is UK-hosted, restores at a fixed rate that would take up to 9 hours for Service B's largest data set, and is sized for the combined average load with 20% headroom. Which service's requirement is the paper's design demonstrably failing to meet?

- A) Service A — residency.
- B) Service B — the 4-hour restoration guarantee cannot be met at the platform's restore rate for its largest data set.
- C) Service C — load.
- D) None — the design meets all stated requirements.

**Correct answer: B**

**Explanation:** Test each requirement against the design facts. Service A: requires UK residency; platform is UK-hosted — met. Service C: the platform is sized for combined average load with 20% headroom — whether that is enough for peaks is a fair question to raise, but the stated facts do not demonstrate failure. Service B: the contract guarantees any file restored within 4 hours; the platform's own restore rate implies up to 9 hours for B's largest data set — a stated fact that directly contradicts a stated guarantee. Option B is demonstrable from the paper's own numbers; everything else is at worst unproven. This is the lead's architectural review discipline: requirements are met by mechanisms, not by intentions, and the reviewer's job is to find the requirement whose mechanism the design does not contain. Note also the reviewer's precision in separating "demonstrably fails" (B) from "warrants a question" (C's peak behaviour, and the missing definition of "largest data set's" growth) — managing the development of architectural solutions means holding both categories, clearly labelled, in the same review.

**Question 6 (moderate) — Pattern recognition across incident and change data**

Preparing a quarterly review, you cross-tabulate your team's 40 major incidents against the preceding 72 hours:

- 24 incidents followed a change implemented by the team (the team implements ~30 changes/week).
- 10 followed a supplier-implemented change (suppliers implement ~5 changes/week).
- 6 followed no recorded change.

A colleague concludes: "Our own changes cause most major incidents — team change quality is the priority problem." What is the sounder reading?

- A) The colleague is right: 24 of 40 incidents followed team changes.
- B) Normalise by change volume: team changes preceded 24 incidents across ~360 changes in the quarter (~6.7%), supplier changes preceded 10 across ~60 (~16.7%) — a supplier change is roughly 2.5 times more likely to precede a major incident, so supplier change quality is the larger per-change risk, though team changes' volume still makes them the larger absolute contributor.
- C) The 6 no-change incidents are the real story.
- D) Post-change incidents cannot be attributed, so the data says nothing.

**Correct answer: B**

**Explanation:** The colleague's reading is a base-rate error: team changes dominate the incident count because they dominate the change count. Normalising gives the per-change risk — step by step: team ≈ 30 × 12 = 360 changes, 24 ÷ 360 = 6.7%; supplier ≈ 5 × 12 = 60 changes, 10 ÷ 60 = 16.7%; ratio ≈ 2.5×. Option B holds both truths at once, which is the lead-level move: per-change risk points the improvement effort at supplier change practice (pre-change review, joint testing, tighter method statements — squarely your third-party management duty), while absolute counts mean team change quality still matters for total incident load. Option A acts on the raw count and would direct the whole improvement budget at the smaller per-change risk. Option C elevates a minority segment without argument (though 6 unexplained incidents deserve their own look — possibly unrecorded changes, itself a finding). Option D retreats from usable evidence; "followed within 72 hours" is imperfect attribution but far from nothing, and quarterly reviews act on exactly this grade of evidence. Being proactive in searching for potential problems means doing this arithmetic before the narrative hardens.

**Question 7 (moderate) — Error checking a test plan you must sign**

You are reviewing the acceptance test plan for a new backup platform before sign-off. The requirement set includes: full restore of the largest production data set within 8 hours; verified integrity of restored data; restore capability at the secondary site if the primary site is lost. The plan's test cases: (1) full restore of the largest production data set at the primary site, timed against the 8-hour target; (2) checksum verification of the restored data set against source; (3) documentation review of the secondary site's configuration to confirm it matches primary. Which requirement lacks a genuine test?

- A) The 8-hour restore — a single timed run is not statistically valid.
- B) Integrity — checksums are insufficient.
- C) Secondary-site restore — a documentation review confirms configuration on paper, but no test case actually performs a restore at the secondary site, so the capability that matters when the primary is lost is never exercised.
- D) None — all three requirements are covered.

**Correct answer: C**

**Explanation:** Map requirements to test cases and grade the evidence each case produces. Requirement one: case 1 exercises the actual restore under the actual time target — direct evidence. Requirement two: case 2 verifies integrity mechanically against source — direct evidence (option B's complaint is a preference, not a gap; checksum comparison is a standard integrity mechanism). Requirement three: case 3 reads about the secondary site rather than testing it — configuration parity on paper does not demonstrate restore capability, because site-loss restores fail for reasons documentation reviews cannot see: network paths, credential scope, bandwidth to the secondary, media accessibility, the hundred details that only an executed restore exercises. The requirement that exists for the worst day is the one the plan verifies most weakly — a pattern so common it deserves a name in your review checklist: the disaster-path test is always the expensive, disruptive one, and always the one quietly downgraded to a paperwork check. Providing authoritative advice and guidance on test planning — your testing skill — means catching exactly this substitution of documentation for demonstration before your signature makes it acceptable. Option A raises a fair statistical point but one timed run against target is at least real evidence; the review's job is to find the requirement with none.

**Question 8 (moderate) — Reading code as a lead**

A junior engineer asks you to sanity-check their cleanup script before it runs against the production file store tonight. The core logic reads:

```
for dir in $(ls /data/archive/); do
  age=$(get_age_days "/data/archive/$dir")
  if [ "$age" -gt 90 ]; then
    rm -rf "/data/archive/$dir"
  fi
done
echo "Cleanup complete"
```

The intent: delete archive directories older than 90 days. Which observation is the most important one to raise?

- A) The script echoes completion without logging which directories it deleted — no audit trail.
- B) The script has no dry-run mode, no logging of deletions, and destructive `rm -rf` runs on the first execution against production with no record of what it removed; it should first run in a list-only mode, log every candidate with its age, and only delete after the list is verified — and the deletion pass should itself log each removal.
- C) Using `ls` in a loop is unfashionable; `find` would be more idiomatic.
- D) The completion message should include a timestamp.

**Correct answer: B**

**Explanation:** All four observations have some merit; the question — like a real review — asks which matters most. Option B names the operational risk category: an irreversible bulk-delete, first executed against production, with no verification pass and no record. The professional pattern for destructive automation is invariant: list first, verify the list, then act, logging every action — so that a wrong `get_age_days` result, an unexpected mount point under /data/archive, or a directory name with a space (a real hazard with the `ls` loop) surfaces as a wrong line in a log instead of lost data. Option A is a true subset of B; option C gestures at the word-splitting hazard but frames it as style — the idiom matters here because it can cause wrong deletions, which B's verification pass would catch; option D is trivia. Two lead-level skills are being exercised at once: interacting with and reading code — your coding and scripting skill, which at your level is mostly critical reading of exactly this kind — and mentoring, because the feedback that changes the junior's career is the category ("destructive operations earn a dry-run and an audit trail, always") rather than the instance. Sign-offs that miss this pattern are how "cleanup complete" becomes an incident title.

**Question 9 (moderate) — Prioritisation of engineering investment**

Your team can staff one significant improvement next quarter. Four candidates, with your own estimates:

1. Automate the certificate renewal process: prevents the class of outage that caused two P1s last year; ~3 weeks' effort.
2. Migrate monitoring to the new corporate platform: mandated within 18 months; ~10 weeks' effort; no service risk from waiting two quarters.
3. Refresh the team's runbook library: improves mean time to resolve across many incident types; ~6 weeks' effort; benefits diffuse but broad.
4. Build a real-time dashboard for the director: requested last week; ~4 weeks' effort; the underlying data is already available weekly.

Which allocation is most defensible?

- A) Item 4 — director requests carry implicit priority.
- B) Item 2 — mandates always come first.
- C) Item 1 — highest risk-reduction per week of effort, addressing a proven P1-generating failure class, with capacity left over toward item 3.
- D) Item 3 — broad benefits beat narrow ones.

**Correct answer: C**

**Explanation:** Evaluate on risk-reduction and value per unit of scarce capacity. Item 1 removes a demonstrated P1 generator (two last year) for three weeks' work — the highest return per week, and prevention of a known failure class is the purest expression of proactive problem management. Item 2 is mandatory but not yet urgent: an 18-month deadline with no waiting risk makes next quarter's start a scheduling decision, not a priority one — "mandated" (option B) answers whether, not when. Item 3 is genuinely valuable and, at six weeks, could partially follow item 1 in the same quarter — which option C explicitly banks. Item 4 fails the value test: the data exists weekly, the request is a week old, and four weeks of specialist capacity for presentational immediacy is poor conversion — the lead's answer to the director is a respectful alternative (weekly data now, dashboard scoped into the migration work), not silent compliance (option A) or flat refusal. Option D's principle ("broad beats narrow") ignores magnitude: item 1's narrow benefit is two P1s a year. Managing team workload at lead level is portfolio management: per-week returns, sequencing, and the political skill of declining gracefully — and assessments reward the option that shows all three.

**Question 10 (hard) — Leading a diagnosis you are not performing**

A major incident is 40 minutes in: the document platform is failing intermittently for all users. Two of your engineers hold competing hypotheses. Engineer A: "It's the new load balancer firmware from Tuesday — the failure pattern matches connection resets; I want to roll it back now." Engineer B: "Resets started before Tuesday at low volume — I think it's the storage array's controller, and rollback will waste forty minutes and prove nothing." Both are credible. Rollback takes 40 minutes and is low-risk; a controller failover test takes 10 minutes and is low-risk; the two actions are independent. As incident lead, what is the strongest direction?

- A) Order the rollback — Engineer A is more senior, and firmware is the more common culprit.
- B) Run the 10-minute controller failover test first: it is quick, low-risk, and discriminating — if failures stop, B is confirmed; if they continue, A's rollback proceeds with B's hypothesis largely eliminated — and have Engineer B pull the pre-Tuesday reset data meanwhile, since that fact, if verified, materially weakens the firmware theory.
- C) Run both actions simultaneously to save time.
- D) Pause all action until the pre-Tuesday reset claim is fully verified.

**Correct answer: B**

**Explanation:** Leading the investigation and resolution of incidents — your incident management skill at lead level — is choosing the sequence of actions that buys the most diagnostic information per minute of user impact. Option B applies test-ordering logic: the failover test is 4× faster than the rollback, equally low-risk, and cleanly discriminating; running it first costs at most 10 minutes against the rollback path and may save 40. Ordering by cost-to-inform, not by seniority (option A's tiebreaker, which also ignores B's disconfirming evidence — the pre-Tuesday resets — that a lead should weight heavily precisely because it is inconvenient to the leading theory). Option C destroys the experiment: with both actions in flight, recovery confirms neither hypothesis, so the next similar incident starts from the same ignorance — simultaneous action is the right call only when impact severity outweighs diagnostic value, which a 10-minute sequencing delta does not. Option D inverts the balance: verification of history is Engineer B's parallel task, not a reason to hold all action during a live all-user failure. The deeper leadership content: your direction visibly rewards evidence over rank — the team that watches the lead order the discriminating test first, and assign the disconfirming-data check to its own proposer, learns how diagnosis is actually done.

**Question 11 (hard) — Multi-constraint planning of a migration programme**

You must sequence four migration waves (W1–W4) over four months (Jan–Apr), one wave per month. Constraints: (i) W3 contains the finance systems and must not run in Jan or Apr (year-end freeze months); (ii) W2 must precede W4, because W4 reuses W2's network configuration; (iii) the supplier's specialist team, required for W1, is only available in Feb and Mar; (iv) W3 must immediately follow W2, in the next calendar month, because W3 validates W2's shared storage layer while the supplier warranty window is open. Which sequence satisfies all constraints?

- A) W2 Jan, W3 Feb, W1 Mar, W4 Apr
- B) W1 Feb, W2 Jan, W3 Mar, W4 Apr
- C) W2 Jan, W1 Feb, W3 Mar, W4 Apr
- D) W1 Jan, W2 Feb, W3 Mar, W4 Apr

**Correct answer: A**

**Explanation:** Check each option mechanically. Option D: W1 in Jan violates constraint (iii) — the supplier team is only available Feb/Mar. Option B: W3 in Mar must immediately follow W2 — but W2 is in Jan, with W1's Feb between them, violating (iv). Option C: same failure — W2 Jan, W3 Mar, not consecutive. Option A: W2 Jan, W3 Feb — consecutive, satisfying (iv); W3 in Feb avoids Jan and Apr, satisfying (i); W1 in Mar sits inside the supplier window, satisfying (iii); W2 (Jan) precedes W4 (Apr), satisfying (ii). All four constraints hold — option A is the unique solution. The efficient route in constraint problems is to start from the tightest coupling: constraint (iv) welds W2→W3 into a consecutive pair, and constraint (i) then forces that pair into Jan–Feb or Feb–Mar; testing those two placements against (iii)'s supplier window resolves the puzzle in seconds. The same discipline governs real migration planning — find the hardest coupling, place it first, and fit the flexible work around it — and it is why programme schedules built person-by-month before constraints are mapped end up rebuilt in month two. Managing the development of architectural solutions across the life cycle includes exactly this sequencing rigour.

**Question 12 (hard) — The anomaly in the quiet data**

Reviewing monthly dashboards, everything is green: incidents down 12%, changes succeeding at 97%, availability targets met. One quiet series catches your eye: out-of-hours administrative logins to the payment platform's management interface have risen from a baseline of 2–3 per month to 19 this month. No incidents, no changes, and no on-call activity map to them. Your on-call engineers say "probably the new supplier engineers doing maintenance". The supplier's maintenance schedule shows no out-of-hours work this month. What is the strongest response?

- A) Accept the on-call explanation — supplier engineers frequently work odd hours, and everything is green.
- B) Treat the anomaly as a potential security incident: an unexplained 6–8× rise in privileged out-of-hours access to a payment platform, explicitly contradicted by the supplier's own schedule, warrants immediate engagement of your security team, preservation of the access logs, verification of the accounts involved — and no tipping-off via broad announcements until the accesses are explained.
- C) Email the supplier asking them to remind their engineers to log maintenance work properly.
- D) Add the metric to next quarter's review agenda for trend confirmation.

**Correct answer: B**

**Explanation:** Grade the anomaly by what it touches and what explains it. What it touches: privileged access, out of hours, on a payment platform — the highest-value target class in your estate. What explains it: nothing — no incidents, no changes, no on-call work, and the convenient hypothesis ("supplier maintenance") is affirmatively contradicted by the supplier's own schedule. An unexplained privileged-access pattern on a payment system is a potential compromise until explained, and option B responds at that grade: security team engaged now, evidence preserved (access logs age out; preservation is time-critical), accounts verified, and — the detail that separates practised responses — no broad announcements that would tip off an intruder using valid credentials. Option A demonstrates the failure mode green dashboards induce: service metrics measure service, not security, and "everything is green" describes exactly what a credentialed intruder looks like. Option C acts on the explanation the evidence just eliminated, and does so in writing to the party whose credentials may be compromised. Option D files a potential live compromise under quarterly trend analysis. This question is your ownership skill's proactive clause at full stretch — searching for potential problems means reading the quiet series, and having the escalation grammar ready when one speaks. Note also the standing lesson for your dashboard design: the only reason you caught this is that someone put privileged-access counts on a page a human reads. Keep them there.

### Preparation tips

- **Practise on your own management data.** Team workload trends, supplier reports, change-versus-incident tabulations — every artefact crossing your desk is a practice question with real stakes. Read for second differences, base rates, and definitional drift as a habit, and the test versions will feel familiar.
- **Normalise before you narrate.** Whenever counts differ, ask "per what?" before concluding. Per change, per user, per week of effort — most leadership-level data errors are missing denominators, and most test distractors are un-normalised readings.
- **Review by mapping claims to mechanisms.** For options papers, test plans, and supplier reports: list each requirement or claim, then find the mechanism or evidence that delivers it. The defect is the claim with no mechanism — and it is usually the disaster-path one.
- **Sequence constraints from the tightest coupling.** In scheduling questions, weld the hardest-coupled items first and place them; the flexible work fits around. Verify every option against every constraint — two violations often hide behind the first.
- **Rehearse test-ordering logic.** For diagnosis questions: rank candidate actions by information gained per minute and per unit of risk. The quick, discriminating, low-risk test goes first, and disconfirming evidence gets weight precisely because it is inconvenient.
- **Grade anomalies by asset value and explanation quality.** A small anomaly on a high-value asset with no surviving explanation outranks a large anomaly with a good one. Practise saying which grade you are assigning and why.

### Common pitfalls to avoid

- **Reading counts without base rates.** "Most incidents follow our changes" — because most changes are yours. Normalise first; the un-normalised conclusion misdirects entire improvement budgets.
- **Seizing work your team is doing well.** In prioritisation scenarios, taking over a competently led incident is the flattering wrong answer. Lead-level marks go to doing what only the lead can do.
- **Accepting definitional drift in others' figures.** Supplier availability, project "pass rates", team "closure rates" — check what the number's own governing document says it should measure. The drift is always flattering.
- **Letting documentation substitute for demonstration.** Configuration reviews are not restore tests; matching versions are not working failovers. Sign-offs that accept paper evidence for disaster-path requirements fail on the day the requirement exists for.
- **Deference as a tiebreaker.** Seniority, directors' requests, and confident narratives all recruit your agreement. The scored answer follows discriminating evidence and value-per-effort, and so should the real one.
- **Explaining away the quiet anomaly.** "Probably maintenance" is how compromises and slow failures survive review. An anomaly is resolved by evidence, not by the first convenient story — especially when the story's own source contradicts it.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with quantitative material: percentages, ratios, weighted averages, rates, projections, and data in tables and charts. At lead level the material shifts decisively toward management data — team capacity and utilisation, supplier service credits and penalty clauses, budgets and cost comparisons, KPI consolidations, and the quantitative content of business cases and options papers.

The typical format is an online, timed test of 20 to 35 minutes with 15 to 25 questions; an on-screen calculator is normally available. Scoring compares accuracy and speed against a norm group, and lead-level variants weight interpretation and challenge — "is this stated conclusion sound?" — as heavily as computation.

Why does numeracy matter distinctively at your level? Because you are the numerical control point between your team and everyone your team answers to. Supplier reports arrive with the supplier's arithmetic; your review is where flattering baselines and convenient exclusions get caught, and service-credit money is recovered or lost on your reading of a percentage. Business cases and options papers arrive with cost comparisons whose assumptions determine their conclusions; your sign-off is where those assumptions meet someone who checks them. Team plans rest on capacity arithmetic — utilisation, absence, on-call loading — and the difference between a sustainable rota and a burnout engine is a calculation someone must do honestly. KPI packs consolidate across services and months, and every consolidation is an opportunity for the weighted-average error to mislead a director. Your role summary says you ensure the service and the contractual and regulatory requirements of the organisation are met — and contracts, budgets, and KPIs are all, finally, numbers.

The mathematics never exceeds confident arithmetic: the four operations, percentages, and averages. The difficulty — and the professional value — lies entirely in setup, baselines, and interpretation. Every explanation below shows its arithmetic step by step, so you can audit method as well as answers.

### How this assessment maps to your role

- **Contractual and service-credit arithmetic** maps to your duty to **manage third party provision of IT operations services**: availability definitions, credit thresholds, and penalty calculations are percentage arithmetic with money attached.
- **Capacity and utilisation arithmetic** maps to your duty to **manage workload, performance and development of a team**: sustainable allocation, on-call loading, and absence planning are ratio and rate problems about people.
- **Cost and options comparison** maps to your duty to **manage the development of architectural solutions**: options papers turn on total-cost comparisons whose baselines and time horizons must be checked, not believed.
- **KPI consolidation and trend reading** map to your **Availability and capacity management** skill and your duty to manage operational support against KPIs: weighted averages, rates versus counts, and honest period-on-period comparisons.
- **Risk and impact quantification** maps to your **Change management** skill (managing high impact, complex change requests means quantifying the impact) and your **Testing** skill of managing test planning, where coverage and result statistics inform acceptance decisions.

### Practice questions

**Question 1 (easy) — Team utilisation percentage**

Your team of 8 engineers each has 37 working hours per week. This week, 74 hours went to incident response across the team. What percentage of total team hours went to incident response?

- A) 20%
- B) 25%
- C) 29%
- D) 33%

**Correct answer: B**

**Explanation:** Total team hours = 8 × 37 = 296. Percentage = 74 ÷ 296 = 0.25 = 25%. Sense-check: 74 is a quarter of 296 (since 74 × 4 = 296) — exact. A quarter of capacity on unplanned incident work is a number worth tracking as a trend: if it climbs while project commitments stay constant, the excess comes out of development time, documentation, and eventually people. Utilisation figures are the raw material of workload management — and the first discipline is computing them against true capacity (all hours) rather than nominal capacity (hours left after meetings), stating which one you used.

**Question 2 (easy) — Service credit calculation**

Your supplier contract specifies: availability below 99.5% in a month triggers a service credit of 10% of the monthly charge; below 99.0% triggers 20%. The monthly charge is £42,000. The supplier reports 99.2% availability. What credit is due?

- A) £0
- B) £4,200
- C) £8,400
- D) £12,600

**Correct answer: B**

**Explanation:** Locate 99.2% in the threshold structure: it is below 99.5% (triggering the 10% tier) but not below 99.0% (so the 20% tier does not apply). Credit = 10% × £42,000 = £4,200. Option C applies the 20% tier a band too early; option A misses the trigger entirely. Tiered thresholds reward exact boundary reading — "below 99.0%" means strictly below, so a hypothetical 99.0% exactly would still sit in the 10% tier. Managing third-party provision includes invoicing these credits: a lead who cannot compute them from the contract leaves money — and more importantly, performance pressure — on the table.

**Question 3 (easy) — Weighted mean resolution time across two sub-teams**

Your infrastructure sub-team resolved 90 incidents at a mean of 3.0 hours; your platform sub-team resolved 30 incidents at a mean of 7.0 hours. What is the team-wide mean resolution time?

- A) 4.0 hours
- B) 4.5 hours
- C) 5.0 hours
- D) 5.5 hours

**Correct answer: A**

**Explanation:** Combine via totals. Infrastructure: 90 × 3.0 = 270 hours. Platform: 30 × 7.0 = 210 hours. Combined: 480 hours across 120 incidents. Mean = 480 ÷ 120 = 4.0 hours. The unweighted trap, (3.0 + 7.0) ÷ 2 = 5.0 (option C), overweights the smaller sub-team threefold. Note the management reading too: the platform sub-team's 7.0-hour mean on a third of the volume might reflect harder incidents, thinner staffing, or weaker runbooks — the consolidated 4.0 answers the director's question, and the 3.0/7.0 split answers yours. Report both: consolidations inform upward, decompositions inform action.

**Question 4 (easy) — Percentage change in a budget line**

Your team's software tooling budget was £64,000 last year and is £56,000 this year. What is the percentage reduction?

- A) 8.0%
- B) 12.5%
- C) 14.3%
- D) 16.0%

**Correct answer: B**

**Explanation:** Reduction = (64,000 − 56,000) ÷ 64,000 = 8,000 ÷ 64,000 = 0.125 = 12.5%. Option C is the wrong-baseline trap (8,000 ÷ 56,000 = 14.3% — the increase needed to get back, not the cut suffered). Budget conversations are precisely where baseline discipline pays: "a 12.5% cut" and "we need a 14.3% uplift to restore" are both true, describe the same £8,000, and land differently in a finance meeting — the lead who understands both framings chooses deliberately which to use, and catches others' choices.

**Question 5 (moderate) — On-call loading fairness**

Your on-call rota covers 52 weeks with 6 engineers. Two engineers have negotiated exemptions from overnight duty for six months each (26 weeks of the year each), during which the remaining engineers cover their share. If overnight cover is one engineer per week, how many overnight weeks per year does each non-exempt engineer carry during the exemption periods, assuming the two exemptions run concurrently and load is shared equally among the four available engineers in that period?

- A) 6.5 weeks
- B) 8.7 weeks
- C) 10.4 weeks
- D) 13.0 weeks

**Correct answer: A**

**Explanation:** During the 26 concurrent exemption weeks, 4 engineers share 26 overnight weeks: 26 ÷ 4 = 6.5 weeks each in that period. (For the full-year picture: the other 26 weeks are shared six ways at 26 ÷ 6 ≈ 4.3, giving non-exempt engineers ≈ 10.8 overnight weeks annually versus 4.3 for exempt colleagues — a 2.5× disparity.) The question's arithmetic is one division; the management content is what the numbers expose: equal-share-among-available produces materially unequal annual loads, which is exactly the kind of quiet unfairness that corrodes rotas. Sustainable accommodation designs compensate elsewhere — daytime duties, weekend weighting, rota credits — and the design conversation starts from computed loads, not impressions. Managing team workload means doing this arithmetic before someone else does it resentfully.

**Question 6 (moderate) — Options paper cost comparison with unequal horizons**

An options paper compares storage solutions: Option X costs £120,000 up front plus £15,000 per year; Option Y costs £30,000 up front plus £45,000 per year. The paper states: "Over three years, Y (£165,000) is cheaper than X (£165,000 — equal), and Y avoids capital outlay; we recommend Y." The platforms' expected service life is six years. What does the six-year comparison show?

- A) Equal costs — the three-year comparison holds at any horizon.
- B) X totals £210,000 and Y totals £300,000 over six years — X is £90,000 cheaper across the actual service life, and the paper's three-year horizon, stopping exactly at the crossover point, conceals this.
- C) Y remains cheaper because avoided capital outlay compounds.
- D) The comparison cannot be made without discount rates.

**Correct answer: B**

**Explanation:** Compute both at the service-life horizon. X: £120,000 + 6 × £15,000 = £120,000 + £90,000 = £210,000. Y: £30,000 + 6 × £45,000 = £30,000 + £270,000 = £300,000. X is £90,000 cheaper over the life the organisation will actually run the platform. The structure to recognise: high-capital/low-running versus low-capital/high-running options always cross over, and the chosen comparison horizon decides the winner — here the paper's three-year window ends precisely at the crossover (both £165,000), the most flattering possible framing for Y. Option D gestures at discounting, which is legitimate refinement (public-sector business cases do discount future costs — a Green Book discipline) but does not rescue a horizon set at half the service life; at any plausible discount rate, £90,000 of undiscounted difference does not vanish. Option C is rhetoric without arithmetic. Reviewing architectural options papers — your role's duty — means always asking: whose horizon is this, and what happens at the asset's actual life? Horizon-picking is the most common honest-looking distortion in cost cases.

**Question 7 (moderate) — Supplier report: rate versus target with exclusions**

Your supplier's contract requires 95% of Priority 2 incidents resolved within 8 business hours. Their quarterly report: "P2 performance: 96.2% (101 of 105 within target). Excludes 12 incidents pending customer information, per clause 14.2." You check clause 14.2: it permits excluding time spent awaiting customer response from the resolution clock — not excluding the incidents entirely. If the 12 excluded incidents are included, and 5 of them met the 8-hour target once waiting time is properly deducted, what is the true performance figure?

- A) 96.2% — the report is right.
- B) 90.6% — (101 + 5) of (105 + 12) = 106 of 117.
- C) 86.3% — 101 of 117.
- D) 92.4% — the average of the two candidate figures.

**Correct answer: B**

**Explanation:** Apply the clause as written: waiting time is deducted from each incident's clock, but the incidents remain in the population. Corrected numerator: 101 + 5 = 106 (the 5 excluded incidents that, with waiting time properly deducted, met the 8-hour target). Corrected denominator: 105 + 12 = 117. Performance: 106 ÷ 117 = 0.906 = 90.6% — below the 95% contractual target, not above it. The supplier's method (dropping inconvenient incidents from the population wholesale) converted a target breach into a headline pass. Option C forgets that 5 of the excluded incidents legitimately count as successes; option D averages two numbers, one of which is simply wrong. The professional sequence this rehearses is the heart of supplier management: read the clause, recompute per the clause, compare against target, then raise the discrepancy formally — with your arithmetic shown, because the conversation that follows is contractual. Exclusion-handling is where supplier percentages most often drift; the lead who recomputes is the reason the drift stops.

**Question 8 (moderate) — Change risk quantification**

A high-impact change will interrupt an internal service used by 1,200 staff for 45 minutes. The service saves each user an average of 12 minutes per hour of use versus the manual fallback, and on average 30% of staff use it in any given 45-minute window. The business asks for the productivity cost of the interruption in staff-hours. What is the best estimate?

- A) 900 staff-hours
- B) 270 staff-hours
- C) 54 staff-hours
- D) 4.5 staff-hours

**Correct answer: C**

**Explanation:** Build the estimate factor by factor. Affected users in the window: 1,200 × 30% = 360 staff. Each affected user loses not the whole 45 minutes but the service's productivity increment: 12 minutes per hour = 12/60 = 20% of their time; over 45 minutes, 45 × 0.20 = 9 minutes each. Total: 360 × 9 = 3,240 staff-minutes = 3,240 ÷ 60 = 54 staff-hours. Option A (900) charges all 1,200 staff for the full 45 minutes — the "everything stops" overestimate; option B (270) charges the 360 users the full window, forgetting the fallback exists. The modelling discipline matters in both directions: overstated impact numbers get changes needlessly refused (or leads' figures discounted in future), understated ones get real disruption waved through. Managing high-impact, complex change requests — your named skill — includes producing impact estimates whose factors (population, exposure, increment) are each visible and challengeable. Present the chain, not just the 54.

**Question 9 (moderate) — Trend versus target in a KPI pack**

Your quarterly KPI pack shows first-time fix rate for the service desk's infrastructure tickets: Q1 78%, Q2 74%, Q3 71%, Q4 69%, against a target of 70%. The pack's commentary reads: "Target met in three of four quarters; performance broadly on track." What is the accurate reading?

- A) The commentary is fair — 3 of 4 quarters met target.
- B) The rate has declined steadily (78 → 69, a 9-point fall) and has now crossed below target; "3 of 4 met" is technically true but the trend means Q1's healthy margin has eroded to a breach, and without intervention Q1 next year will breach further.
- C) The decline is seasonal and will self-correct.
- D) A 9-point fall on 78 is only an 11.5% relative decline — immaterial.

**Correct answer: B**

**Explanation:** Both facts are true: three quarters at or above 70, and a monotonic decline of about 3 points per quarter now sitting below target. The commentary reports the first and buries the second — but the second is the decision-relevant one, because trend extrapolation (69 − 3 = 66 next quarter, absent intervention) says the breach deepens. Option B reads level and trend together, which is the KPI discipline: a metric above target and falling is a different management object from one below target and rising, though snapshot reporting renders them identically. Option C asserts seasonality no data supports (four points, one direction, no prior-year comparison offered). Option D's relative-decline arithmetic is correct (9 ÷ 78 = 11.5%) and its conclusion does not follow — materiality is set by the target's proximity, and the metric has crossed it. Managing operational support against KPIs means writing (and challenging) commentary that reports the trend that hurts, not the framing that flatters — packs that soothe in Q4 produce crises in Q2.

**Question 10 (hard) — Compound demand against stepped capacity**

A platform your team runs handles 400,000 transactions per month, growing 6% per month compound as services onboard. Its current capacity ceiling is 600,000 transactions per month. An upgrade doubling capacity to 1,200,000 requires 4 months from approval to live. Approximately how many months from now does demand hit the current ceiling, and what is the latest approval month to avoid breaching it?

- A) Ceiling hit around month 7; approval needed by about month 3.
- B) Ceiling hit around month 9; approval needed by about month 5.
- C) Ceiling hit around month 12; approval needed by about month 8.
- D) Ceiling hit around month 5; approval is already too late.

**Correct answer: A**

**Explanation:** Find n where 400,000 × 1.06ⁿ ≥ 600,000, i.e. 1.06ⁿ ≥ 1.5. Compound stepwise: 1.06² = 1.124; 1.06⁴ = 1.124² = 1.262; 1.06⁶ = 1.262 × 1.124 = 1.419; 1.06⁷ = 1.419 × 1.06 = 1.504 — crosses 1.5 at month 7. (Rule-of-72 sanity check: doubling at 6% takes ≈ 12 months, and 1.5× is materially sooner than doubling — month 7 fits; option C confuses the 1.5× point with the doubling point.) Latest approval: 7 − 4 = month 3. Option B misplaces the crossover; option D invents an emergency. The two-step structure — compound the demand curve, then subtract the response lead time — is the core arithmetic of capacity leadership: identifying capacity issues and implementing required changes on time is your availability and capacity duty, and the figure that belongs in your report is the decision deadline (month 3), not the event date (month 7). Present both, with the arithmetic, and the approval conversation starts from your numbers.

**Question 11 (hard) — Test coverage statistics in an acceptance decision**

A supplier reports acceptance testing of a system your team will operate: "412 of 420 test cases passed (98.1%). The 8 failures are all in the disaster recovery suite, which contains 10 cases. We recommend acceptance with DR fixes scheduled post-go-live." As the lead whose team inherits operations, what is the sharpest numerical reading?

- A) 98.1% overall pass is comfortably acceptable; proceed.
- B) The aggregate conceals the structure: the DR suite failed 8 of its 10 cases (an 80% failure rate in exactly the capability that cannot be tested in production and exists for the worst day), while the rest of the system passed 410 of 410; acceptance should treat "system functionality" and "disaster recovery" as separate acceptance decisions — the first is clean, the second has failed outright and "fix post-go-live" means operating without proven DR for an undefined period.
- C) 8 failures out of 420 is within any reasonable tolerance; the suite they cluster in is immaterial.
- D) The pass rate should be recomputed excluding the DR suite, giving 100%, which supports acceptance.

**Correct answer: B**

**Explanation:** Decompose the aggregate. All 8 failures sit in the 10-case DR suite, so the DR suite passed only 2 of 10 — a 20% pass rate, 80% failure. The non-DR remainder passed 410 of 410 — a perfect 100% (420 − 10 = 410 cases, 412 − 2 = 410 passes). The 98.1% headline is a weighted average of a perfect suite and a failed one, with the failed suite's tiny size (10 of 420 cases) hiding its total collapse. Option B reads the structure and draws the operational consequence: failure clustering is diagnostic — these are not random defects but a capability that does not work; DR is precisely the capability whose absence is invisible in normal operation and catastrophic when invoked; and "post-go-live fixes" to DR mean the exposure window is open exactly when go-live instability makes invocation most likely. Options A and C accept the aggregate at face value — the error the report's framing invites; option D is the supplier's framing taken to its cynical conclusion (excluding the failures produces 100% by construction). Managing test planning and acceptance — your testing skill — means insisting that pass rates be reported per capability, and that acceptance decisions attach to capabilities, not to averages. The one-line version for your board paper: "Functionally complete; disaster recovery failed 8 of 10 cases and is not accepted."

**Question 12 (hard) — Reconciling utilisation, absence, and commitment arithmetic**

You are asked to commit 2.0 full-time-equivalents (FTE) of your 8-engineer team to a 6-month programme. Current team load: incident and request work consumes 45% of capacity on average; changes and maintenance 25%; the remainder covers development, documentation, and cover. Planned absence (leave and training) averages 12% of gross capacity, and the 45%/25% figures are measured against capacity net of absence. What percentage of net capacity would remain for development, documentation, and cover if the 2.0 FTE commitment proceeds — assuming incident, request, change, and maintenance workloads are fixed in absolute terms?

- A) 30%
- B) About 6.7%
- C) About 17%
- D) About 21%

**Correct answer: B**

**Explanation:** Work in net-capacity units. Current net capacity: 8 FTE × 88% = 7.04 FTE-equivalents (absence takes 12% of gross). Current absolute loads: incidents/requests 45% × 7.04 = 3.168; changes/maintenance 25% × 7.04 = 1.76; remainder 30% × 7.04 = 2.112. The programme takes 2.0 FTE of engineers — but those engineers also carry absence, so the team's net capacity falls by 2.0 × 0.88 = 1.76, to 7.04 − 1.76 = 5.28. Fixed workloads still consume 3.168 + 1.76 = 4.928. Remaining for development, documentation, and cover: 5.28 − 4.928 = 0.352 FTE-equivalents, which is 0.352 ÷ 5.28 = 6.7% of the reduced net capacity. Option A is the before picture; options C and D come from skipping the absence adjustment on one side or the other. The management translation: the commitment is arithmetically possible and operationally hollow — 0.35 FTE across 6 engineers is no meaningful development time, no documentation, and no slack for a single bad incident week, meaning the commitment is really funded by stopping improvement work and burning contingency. The lead's answer to the programme is not "no" but the arithmetic itself: "2.0 FTE costs us all development and resilience margin; here are the options — 1.5 FTE, backfill, or explicit acceptance that improvement stops." Workload commitments made without this calculation are how teams hollow out; building capability to deliver services as required — your role's phrase — depends on someone doing it before saying yes.

### Preparation tips

- **Recompute everything that arrives computed.** Supplier percentages, options-paper totals, KPI commentary, test pass rates — at lead level, the test (and the job) is rarely "calculate" and usually "verify". Practise the reflex of rebuilding the headline number from its raw parts.
- **State your baseline, horizon, and denominator aloud.** Percentage change against which year? Costs over which lifespan? Rate per what population? Most planted distortions — and most real-world ones — live in exactly these three choices.
- **Decompose aggregates before accepting them.** Weighted averages hide failed subsets (DR suites, degraded sub-teams, one bad service). Ask what populations were combined and whether any subset tells a different story from the whole.
- **Convert event dates to decision deadlines.** Capacity ceilings, contract renewals, compliance dates: subtract lead times and present the latest-decision date. That single habit turns forecasts into governance.
- **Do people-arithmetic with absence and increments.** FTE commitments, rota loads, and utilisation all mislead unless absence rates and productivity increments are carried through. The plausible wrong options are always the ones that skip a factor.
- **Practise on this quarter's real pack.** Take your live KPI pack or a recent supplier report and find one baseline choice, one aggregation, and one horizon to challenge. If you find none, look again — then use the exercise with your team.

### Common pitfalls to avoid

- **Accepting flattering exclusions.** Excluded incidents, excluded degradations, excluded test suites. Check the governing document's actual exclusion rule and recompute with the population restored.
- **Horizon-picking in cost comparisons.** Any comparison ending at or before the crossover point of two cost structures is chosen, not neutral. Recompute at the asset's actual service life.
- **The unweighted consolidation.** Averaging sub-team means, service availabilities, or quarterly rates without volume weights misstates the estate — usually in whichever direction the author preferred.
- **Level without trend, or trend without level.** "Met target three of four quarters" and "declining three points a quarter" are both true; decisions need both. Commentary offering only one is framing, not reporting.
- **Charging interruptions at gross rather than incremental cost.** Impact estimates that bill every user for every minute overstate; estimates that forget the affected population understate. Build factor chains and show them.
- **Committing capacity without carrying absence.** FTE promises made on gross capacity are broken on day one. Net everything — absence, on-call, fixed workloads — before agreeing numbers that bind your team.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret, and draw conclusions from written material. At lead level the material is the documentation of operational governance: contracts and their schedules, regulatory and policy extracts, release and change policies, supplier correspondence, audit findings, business cases, and the reports — upward, outward, and formal — that your role signs or challenges.

The typical format is an online, timed test of 15 to 25 minutes: passages followed by questions, with true/false/cannot-say as the dominant type, supported by which-rule-governs questions, best-summary questions, inference-strength questions, and clear-writing judgements. Scoring rewards accuracy under time pressure and strict fidelity to the passage over background knowledge.

Why is verbal precision a leadership skill in your role? Your summary answers directly: you ensure the service and the contractual and regulatory requirements of the organisation are met. Contractual and regulatory requirements exist only as text, and they are met or breached according to what the text actually says — not what anyone remembers it saying. You manage third-party provision, which means supplier obligations, exclusions, and remedies live in clauses you must read the way suppliers' commercial teams read them. You ensure release policies, procedures and processes are applied — an enforcement duty that starts with knowing precisely what they require. You draft and maintain procedures and documentation, and set standards for definition and conformity — your technical specialism — so your own writing becomes the text others must read precisely. And everything your team escalates to you, and everything you send upward, is a written claim whose strength you must grade before acting on it or forwarding it: the lead is the point where "the supplier says it's fine" either gets checked against what the supplier actually wrote, or doesn't.

The golden rule is unchanged from every level: answer from the passage alone. At lead level, add its governance corollary: in real disputes, the document defeats the recollection — so the habit of returning to the text, practised here under time pressure, is the habit that wins supplier negotiations, survives audits, and keeps your assurances accurate.

### How this assessment maps to your role

- **Contract and clause comprehension** maps to your duty to **manage third party provision**: obligations, exclusions, notice periods, and remedies are all creatures of exact wording, and your reading is the organisation's control.
- **Policy and regulation application** maps to your duty to meet **contractual and regulatory requirements** and to your **Change management** skill of ensuring release policies and processes are applied — enforcement begins with precise comprehension.
- **Inference-strength discipline** maps to your **Incident management** skill of leading investigations (grading evidence in reports before acting on it) and your **Problem management** skill (conclusions sized to their evidence).
- **Summary and reporting judgement** maps to your upward and outward reporting duties: board papers, supplier letters, and incident summaries succeed when every claim carries its correct strength.
- **Clear-writing and standards judgement** maps to your **Technical specialism** duty to draft and maintain procedures and set standards, and to your **User focus** skill of championing user research and representing users — writing judged by what its reader can correctly do with it.

### Practice questions

**Question 1 (easy) — Reading a contractual notice clause**

Read this extract from your supplier contract:

"Either party may terminate this agreement for convenience by giving not less than 90 days' written notice, such notice to expire no earlier than the end of the Initial Term. The Initial Term is 24 months from the Commencement Date. Termination for material breach may be effected at any time by written notice, subject to a 30-day remediation period following notification of the breach."

The Commencement Date was 20 months ago. Statement: "The organisation could serve notice of termination for convenience today, taking effect in 90 days."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Two conditions govern convenience termination: at least 90 days' notice, and expiry no earlier than the end of the Initial Term (24 months from commencement). Today is month 20; notice served today plus 90 days expires around month 23 — before the Initial Term ends at month 24. The second condition fails, so notice "taking effect in 90 days" is not available: false. You could serve notice today expiring at month 24 (that is, about 120 days' notice) — but that is not what the statement says. The two-condition structure is the point: contractual rights routinely carry paired constraints (duration and earliest-effect), and reading only the famous one (90 days) is how organisations mistime exits. Managing supplier relationships includes keeping a calendar of these windows — and reading them from the clause, not from the summary someone once wrote.

**Question 2 (easy) — Regulatory scope**

Read this extract from a (fictional) regulatory notice:

"From 1 January, public bodies operating systems that process payment card data must ensure such systems are assessed annually against the applicable industry standard by an approved assessor. Systems that store, process, or transmit card data are in scope. Systems that merely link to third-party payment pages, without card data touching the body's infrastructure, are out of scope."

Your estate: System P processes card payments directly; System Q redirects users to a third-party payment provider, with no card data touching your infrastructure; System R stores tokenised references to cards but, per its design documents, no card data. Statement: "Systems P and Q require annual assessment under the notice."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Apply the scope test per system. P processes card data — in scope, assessment required. Q matches the out-of-scope description exactly: it links to a third-party payment page and no card data touches your infrastructure — out of scope. The statement bundles P (correct) with Q (incorrect), and a conjunction with one false conjunct is false. R — deliberately unasked — is the interesting case for your real work: tokenised references may or may not constitute card data under the industry standard's definitions, and the notice as quoted does not resolve it; the professional move is a definitional check, not an assumption either way. Regulatory reading at lead level is population sorting: each system enters exactly the obligations its facts trigger, and compliance costs money while non-compliance costs more — so the sorting is worth doing against the text, system by system.

**Question 3 (easy) — What the audit finding actually says**

Read this extract from an internal audit report:

"Finding 4 (Medium): Of 25 sampled emergency changes, 6 lacked evidence of retrospective review at the following CAB, contrary to the change policy. We note management's assertion that reviews occurred but were not minuted. Recommendation: implement a tracking mechanism ensuring retrospective reviews are performed and evidenced. Management response: accepted; to be implemented within 90 days."

Statement: "The audit found that 6 emergency changes were not retrospectively reviewed."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Correct answer explanation follows.**

**Explanation:** Read the finding's precise object: 6 changes "lacked evidence of retrospective review" — an evidential absence, not an established non-occurrence, and the report itself preserves the distinction by noting management's assertion that reviews happened but went unminuted. Whether the 6 reviews occurred is exactly what the evidence cannot determine: cannot say. The distinction is not pedantry — it is the entire grammar of audit: findings attach to evidence, and "not evidenced" is a real deficiency (unevidenced controls fail audits and, worse, cannot be relied on) without being the same claim as "not performed". Leads live on both sides of this line: when your team is audited, conflating the two overstates the failure; when you review your own controls, treating "probably happened" as adequate understates it. The recommendation's wording — "performed and evidenced" — shows the auditor holding both requirements deliberately.

**Question 4 (easy) — Meaning in context in supplier correspondence**

Read this line from a supplier's email about a fault your team escalated:

"Our engineering team has identified a probable cause and is developing a remediation, which we expect to include in the next scheduled maintenance release, subject to successful regression testing."

Which reading of the supplier's commitment is accurate?

- A) The fault's cause is confirmed and the fix will arrive in the next maintenance release.
- B) The supplier has committed to nothing firm: the cause is "probable" not confirmed, the remediation is in development not complete, inclusion in the next release is an expectation not a promise, and even that is conditional on regression testing.
- C) The supplier has refused to fix the fault.
- D) The fix will arrive only if your organisation performs regression testing.

**Correct answer: B**

**Explanation:** Inventory the hedges: "probable cause" (diagnosis unconfirmed), "developing" (incomplete), "expect to include" (intention, not commitment), "subject to successful regression testing" (a condition owned by the supplier — option D misassigns it to you). Every load-bearing element is qualified, so the email promises precisely nothing enforceable — which is not the same as bad faith (option C overreads): it is a normal engineering status honestly hedged. The lead's task is to know the difference between status and commitment, and to convert one into the other where the service needs it: a reply asking for a committed release identifier and date, or invoking the contractual fault-resolution clause if one exists. Suppliers' commercial teams draft with these hedges deliberately; reading them as commitments — then reporting "fix due next release" upward as fact — is how leads inherit other people's ambiguity as their own broken promise.

**Question 5 (moderate) — Which policy provision governs**

Read this extract from your organisation's release policy:

"Standard releases follow the monthly release calendar. Expedited releases may be approved by the service's lead engineer where a fault materially degrades service, and must be notified to the CAB retrospectively. Security releases addressing vulnerabilities rated High or Critical must be deployed within 14 days of patch availability, notwithstanding the release calendar. Where a security release also contains functional changes, the functional changes require standard or expedited approval in their own right."

A vendor patch rated High was released 10 days ago. Bundled in the same vendor package is a new reporting feature your service owner wants. Which statement correctly applies the policy?

- A) The whole package must be deployed within 14 days under the security provision.
- B) The security content must be deployed within 4 days to meet the 14-day rule, but the bundled functional change requires its own standard or expedited approval — so deploy the security fix within the deadline, and route the reporting feature through its own approval (or deploy the package with the feature approved expedited, if the lead engineer's criteria are genuinely met).
- C) The 14-day rule is suspended because the package contains functional changes.
- D) The reporting feature can ride along under the security deadline, since separating them is inconvenient.

**Correct answer: B**

**Explanation:** The policy anticipates the bundling problem explicitly: security content carries the 14-day obligation "notwithstanding the release calendar", while bundled functional changes "require standard or expedited approval in their own right". Option B applies both provisions to their own objects and does the deadline arithmetic (14 − 10 = 4 days remaining). Option A stretches the security deadline into an approval bypass for the feature — the exact move the final sentence exists to block. Option C inverts the "notwithstanding": the security obligation overrides calendars; nothing suspends it. Option D is option A with its motive showing. Note what the correct answer preserves: the expedited route remains legitimately available for the feature if its criteria are met — the policy constrains the path, not necessarily the outcome. Ensuring release policies are applied — your change management skill — is precisely this: obligations tracked to their objects, deadlines computed, and convenient bundlings unbundled before they set precedents. The 4-day residue is also a lead-level planning fact: whoever separates the package needs to start today.

**Question 6 (moderate) — The board summary that must be accurate**

Read this extract from your team's draft major incident report:

"The outage lasted 3 hours 40 minutes and prevented approximately 4,000 staff from accessing case files. Recovery was delayed roughly 90 minutes because the failover runbook referenced a decommissioned server; the on-call engineer improvised a correct alternative. The root cause was a storage firmware defect; the supplier has issued a fixed version, now deployed. The runbook error had been reported by a team member five weeks earlier but the correction was not prioritised."

Which one-paragraph summary is most appropriate for the board?

- A) "A storage firmware defect caused a 3h40m outage affecting ~4,000 staff. The supplier's fixed firmware is deployed. Recovery was extended by ~90 minutes because our failover runbook was out of date — an error reported internally five weeks earlier but not actioned. We are fixing the runbook process, including how reported errors are prioritised."
- B) "A supplier firmware defect caused an outage; the supplier has provided a fix. Recovery took slightly longer than planned due to a documentation issue, now resolved."
- C) "An outage occurred due to a combination of supplier and process factors. All issues are resolved and lessons have been learned."
- D) "A storage firmware defect caused the outage. Recovery was delayed by a runbook error. The engineer responsible for the outdated runbook has been identified."

**Correct answer: A**

**Explanation:** Grade each summary against the draft's facts and against what boards need: impact, cause, status, and the uncomfortable finding with its remedy. Option A carries all of it — duration, population, root cause, fix status, the 90-minute runbook delay, and the five-week-old unactioned report, which is the governance finding: the organisation had the information to prevent the delay and lacked the process to act on it. It also commits to the systemic remedy (prioritisation of reported errors), not just the instance. Option B launders: "slightly longer than planned" for 90 minutes of a 220-minute outage (41% of it), and the five-week miss vanishes. Option C is content-free reassurance — "lessons have been learned" without naming any is the phrase boards should, and increasingly do, distrust. Option D converts a process failure into a person failure: the report's facts say the error was reported and not prioritised — a prioritisation-process defect — and "the engineer responsible has been identified" aims accountability at the wrong layer while teaching your team that reporting errors creates suspects. The lead's summary discipline: the version that goes up must contain the fact you would least like it to contain, stated plainly, with its remedy — because boards discover omissions eventually, and the discovering is what destroys credibility.

**Question 7 (moderate) — Inference strength in an escalated claim**

Your service desk manager escalates: "Users are saying the new VPN client is causing laptop crashes. Twelve crash reports this week from VPN users, versus two or three in a normal week. The desktop team says nothing else changed this week. I think we should pull the client." Which assessment of the evidence is soundest?

- A) The evidence proves the VPN client causes crashes; pull it today.
- B) The evidence is a strong signal worth acting on — a 4–6× crash-rate rise coinciding with the rollout, with no other known change — but it is correlational: the sound next steps are to check crash diagnostics for VPN-client involvement, compare crash rates between updated and not-yet-updated laptops (the rollout's natural control group), and prepare rollback criteria — with immediate rollback justified if the diagnostic check or the comparison confirms, or if crash severity escalates meanwhile.
- C) The evidence is anecdotal; take no action until users file formal tickets.
- D) The desktop team's claim that nothing else changed should be accepted as establishing the VPN client as the only possible cause.

**Correct answer: B**

**Explanation:** Grade the claim: a coincident 4–6× rise with no known alternative change is genuinely strong — far above anecdote (option C's dismissal fails users and the twelve reports are tickets in substance) — but short of proof: "nothing else changed" means nothing else known changed (option D converts an absence of knowledge into an exhaustive fact), and crash attribution needs diagnostics, not chronology alone. Option B holds the correct strength and — the lead-level content — designs the discrimination: the phased rollout provides a natural experiment (updated versus not-yet-updated crash rates), diagnostics provide mechanism, and pre-agreed rollback criteria convert "should we pull it?" from a repeated argument into a threshold check. Option A acts on proof it does not have — and if the true cause is elsewhere (a concurrent silent update, a hardware batch), pulling the client both disrupts users and delays the real finding. Leading investigation and resolution — your incident management skill — is mostly this: acting proportionately on strong-but-unproven signals while spending the smallest possible time converting them to proof. Note the escalation itself was good: the manager brought data, a comparison baseline, and a recommendation — the format your escalation standards should require.

**Question 8 (moderate) — Procedure drafting judgement**

You are setting the standard for your team's runbooks. Which opening instruction best exemplifies the standard you should require?

- A) "In the event of replication failure, appropriate remedial action should be taken by the responsible engineer in a timely manner, having regard to prevailing service conditions."
- B) "If replication lag exceeds 15 minutes (alert REPL-04): (1) check replication service status on DB-PRD-01 per §2; (2) if the service is stopped, restart it and confirm lag falls below 5 minutes within 10 minutes; (3) if the service is running or lag does not fall, do NOT restart the database — escalate to the DBA on-call (rota page) quoting this runbook section and current lag. Restarting the database during active replication recovery can cause data divergence."
- C) "Replication issues: see the DBA team's documentation."
- D) "Fix replication per standard practice. Escalate if unsure."

**Correct answer: B**

**Explanation:** Judge each against what a runbook is for: enabling a competent engineer who is not the author to act correctly under stress. Option B has every load-bearing element: a quantified trigger tied to a named alert; numbered steps with verification criteria (lag below 5 within 10 — success is measurable); a prohibition with its reason (the "why" converts a rule into understanding, so the engineer facing a variant situation reasons correctly); and an escalation path with the exact information to quote. Option A is governance prose — "appropriate", "timely", "having regard to" — which delegates every real decision to the reader while appearing to guide them; it is unfalsifiable and therefore unexecutable. Option C outsources to another team's documents, which may assume that team's context and access. Option D's "standard practice" names a thing that exists only in the heads of people who no longer need runbooks. The standards question inside the writing question: your technical specialism duty — draft and maintain procedures, set standards and ensure conformity — means the assessment is not "can you write option B?" but "do you require option B, spot options A, C and D in review, and coach their authors?" A lead's documentation standard is enforced in review comments, and this is what the review comment protects.

**Question 9 (moderate) — User research in an operational decision**

Read this extract from a user researcher's findings, shared with your team:

"Research with 22 caseworkers across three sites on the file service migration: 18 rely on the 'recent files' feature to resume interrupted work — interruptions average 6 per day in frontline roles. The target platform's equivalent feature retains 10 items against the current 50; several participants routinely navigate to files 20–30 items back after multi-day absences. Participants were enthusiastic about the new platform's search speed. Caveat: all three sites were high-volume processing centres; the long-tail usage of specialist teams (est. 15% of users) was not sampled."

Your migration plan currently treats the recent-files difference as cosmetic. What does the research support?

- A) Proceeding unchanged — 22 users is too small a sample to matter.
- B) Treating the recent-files reduction as a workflow risk for frontline caseworkers — the evidence shows heavy, structural reliance (interruption-driven, 6/day, reaching 20–30 items back) that a 10-item list breaks — while noting the search-speed positive, and commissioning the unsampled specialist-team research before finalising; the plan should seek a configuration change, a workaround, or explicit service-owner acceptance of the degradation.
- C) Halting the migration — the platform has failed user research.
- D) Proceeding, since participants were enthusiastic about search speed.

**Correct answer: B**

**Explanation:** Read the findings at their actual strength and structure. The reliance evidence is strong for the sampled population: 18 of 22, a mechanism (interruption-driven work resumption), a frequency (6/day), and a specific breaking point (items 20–30 versus a 10-item retention) — that is not preference data; it is workflow-structure data, and "cosmetic" is untenable against it. The enthusiasm about search is real and belongs in the picture (option D cherry-picks it; option C ignores it and overreads the negative — one degraded feature with possible mitigations is not a failed platform). The caveat does lead-level work: the researcher has flagged a sampling boundary, and option B's response — commission the missing sample rather than either generalising past it or discarding the study (option A's sample-size dismissal misunderstands qualitative workflow research, where 18 of 22 showing the same structural dependence is a strong signal) — is what "champion user research" and "collaborate with user researchers, represent users internally" mean operationally: your user focus skill, exercised at the point where migration plans get corrected. The output shape matters too: risk named, mitigation options framed, decision routed to the accountable owner with honest evidence.

**Question 10 (hard) — Two clauses in tension**

Read these two extracts from the same supplier contract:

Clause 8.3: "The Supplier shall complete all Priority 1 incident resolutions within 4 hours of notification. Failure in any month to resolve 90% of Priority 1 incidents within this period constitutes a Service Level Failure, entitling the Customer to the remedies in Schedule 5."

Clause 8.7: "Where a Priority 1 incident's resolution requires action by the Customer or a third party outside the Supplier's control, the affected incident shall be excluded from Service Level calculations, provided the Supplier notifies the Customer of the dependency within 1 hour of identifying it."

Last month: 10 P1 incidents; the supplier resolved 8 within 4 hours. Of the 2 late resolutions, one awaited your organisation's network team for 3 hours (the supplier flagged this dependency 40 minutes after identifying it); the other awaited a third-party carrier for 6 hours, which the supplier first mentioned in the monthly report. What does the contract support?

- A) A Service Level Failure occurred: 8 of 10 is 80%, below 90%.
- B) No Service Level Failure: both late incidents are excluded, giving 8 of 8.
- C) The network-team incident is validly excluded (dependency notified within the hour), but the carrier incident is not (no timely notification), so the calculation is 8 of 9 = 88.9% — below 90%, and a Service Level Failure has occurred.
- D) Cannot be determined without Schedule 5.

**Correct answer: C**

**Explanation:** Apply clause 8.7's exclusion test to each late incident separately — the exclusion is conditional, and the condition is notification "within 1 hour of identifying" the dependency. Incident one: dependency on your network team, flagged at 40 minutes — condition met, validly excluded, and note the exclusion removes the incident from the calculation entirely (both numerator and denominator). Incident two: dependency on a carrier, first mentioned in the monthly report — weeks after identification; condition failed, so the incident stays in the calculation as a miss. Result: population 9 (10 − 1 excluded), successes 8, rate 8 ÷ 9 = 88.9% — below the 90% threshold: Service Level Failure, remedies per Schedule 5 available. Option A ignores a valid exclusion; option B grants an invalid one — and the supplier's report will, naturally, be drafted on option B's arithmetic; option D confuses the failure determination (clauses 8.3/8.7, fully quoted) with the remedy quantum (Schedule 5, not needed for the question asked). This is the exact reading discipline your third-party duty requires: exclusions are conditional gifts, their conditions are the customer's protection, and the lead who tracks notification timestamps converts a supplier's 100% into the contract's 88.9%. Procedural note for the real world: the determination letter should cite both clauses, both incidents, and the notification evidence — disputes are won by the party whose paperwork already contains the argument.

**Question 11 (hard) — The business case's quiet assumption**

Read this extract from a business case you are reviewing:

"Migrating the estate's backup service to the proposed cloud platform saves £180,000 annually against current costs. The saving assumes decommissioning the on-premises backup infrastructure at migration completion (month 6), releasing £120,000/year in maintenance, and reducing storage costs by £60,000/year through the platform's deduplication, based on the vendor's benchmark of 4:1 deduplication across mixed estates. Regulatory retention requires 7-year recoverability of financial records. The cloud platform's supported recovery guarantee covers data written to it; recovery of legacy backup sets requires the on-premises infrastructure that created them."

Which is the most significant defect a reviewing lead should raise?

- A) The £120,000 maintenance saving is overstated.
- B) The case simultaneously requires decommissioning the on-premises infrastructure at month 6 (to release the claimed savings) and retaining it (because 7-year regulatory recoverability of legacy backup sets depends on the infrastructure that created them) — the full £180,000 saving and the compliance obligation cannot both hold as drafted; either legacy sets must be migrated/converted (a cost the case omits), or the infrastructure must be retained in some form (reducing the saving), or recoverability is breached.
- C) The 4:1 deduplication benchmark may not be achieved on your estate mix.
- D) Cloud costs may rise after year one.

**Correct answer: B**

**Explanation:** Options A, C and D are all legitimate review questions — C especially, since vendor benchmarks routinely flatter (worth a sensitivity line: at 2:1, the £60,000 halves) — but the question asks for the most significant defect, and option B is structural: the case's two premises contradict each other through a compliance obligation. The savings arithmetic requires the on-premises infrastructure gone at month 6; the regulatory requirement makes legacy backup sets recoverable for 7 years; the passage states legacy recovery requires that same infrastructure. Something must give, and each resolution has a cost the case does not carry: legacy migration/conversion (often substantial), partial retention in a recovery-capable state (eroding the £120,000), or non-compliance (not a cost line anyone may choose). A case whose headline number depends on an impossibility is not optimistic — it is broken, and it is exactly the defect that survives every review that checks arithmetic but not premises, then surfaces in month 7 as an unbudgeted retention requirement. Your review discipline for architectural and business cases: after the numbers, hunt the premise pairs — what must be true simultaneously, and can it be? Regulatory retention is where such contradictions most often hide in operations cases, because the obligation outlives every migration that forgets it.

**Question 12 (hard) — Grading a chain of reported claims**

Your incident manager's weekly summary states:

"The recurring Tuesday slowdowns are resolved. The supplier confirmed their Tuesday maintenance job was the cause, moved it to 03:00, and no slowdown occurred this Tuesday. Separately, the DBA team believes the month-end batch overrun risk is now low, as the query optimisation deployed last week reduced the batch's largest query by 60% in testing; the first month-end run is next Friday. Finally, security confirmed the anomalous logins investigated last month were a misconfigured monitoring probe — closed."

Which grading of the three claims is most accurate?

- A) All three matters are resolved and can be reported upward as closed.
- B) Claim one is well-evidenced but young (cause confirmed by its owner, mechanism removed, one clean Tuesday — report as "resolved, monitoring for two further cycles"); claim two is a forecast resting on a test result, not yet validated in production ("risk reduced, first real validation next Friday"); claim three is closed on the investigating authority's confirmed finding. Only the third is fully closed; the summary's "resolved/low/closed" framing overstates the first two by one grade each.
- C) None can be trusted — all three require independent re-investigation.
- D) Claims one and two are closed; claim three should remain open indefinitely because security matters are never truly closed.

**Correct answer: B**

**Explanation:** Grade each claim by evidence type and maturity. Claim one has the strongest structure — causal confirmation from the component's owner, mechanism removed, and a first confirming observation — but one clean Tuesday after a recurring pattern is a sample of one; the honest grade is "resolved pending confirmation cycles", and the cost of that phrasing is nil while the cost of re-reporting a "resolved" issue that recurs is your summary's credibility. Claim two is categorically different: a 60% test-environment improvement is genuine risk reduction but the claim's object — month-end behaviour under production data volumes — has never been observed; it is a forecast, and forecasts are reported as forecasts with their validation date attached (next Friday), ideally with a contingency noted. Claim three is closed properly: the accountable investigating authority reached a specific, benign finding — option D's "never truly closed" posture confuses vigilance with the inability to close anything, which buries teams in permanent open items. Option A flattens three evidence grades into one word; option C pays re-investigation costs on claims whose owners have done their jobs. The lead-level skill is calibrated onward reporting: each claim forwarded at its own strength, with its next checkpoint — because your summary becomes someone else's certainty, and grade inflation compounds at every level it passes through.

### Preparation tips

- **Read conditions in pairs.** Notice periods with earliest-effect dates, exclusions with notification deadlines, savings with decommissioning premises. Contractual and policy provisions hunt in pairs, and the second condition is where the traps — and the protections — live.
- **Sort populations before applying rules.** Regulatory scope, policy applicability, SLA exclusions: list the items, test each against the definition, and only then apply the obligation. Bundled statements ("P and Q require…") fail on their weakest member.
- **Distinguish evidence-absence from event-absence.** "Not evidenced" is not "not performed"; "no known change" is not "no change". Audit findings, supplier reports, and escalations all trade on this line — hold it.
- **Inventory hedges in commitments.** "Probable", "expect", "subject to" — count the qualifiers before reporting anyone's statement upward as a promise. Convert status to commitment by asking for identifiers and dates, not by optimistic paraphrase.
- **Summarise with the worst fact included.** Draft board summaries by first writing the sentence you would prefer to omit, then building around it. If your summary would survive the full report's later disclosure, it is honest enough to send.
- **Hunt premise contradictions in cases and papers.** After checking the arithmetic, ask what must be simultaneously true — decommissioned and retained, excluded and counted, frozen and deployed — and whether it can be. One structural contradiction outweighs ten quibbles.

### Common pitfalls to avoid

- **Reading the famous condition and skipping its partner.** Ninety days' notice, but expiring no earlier than term-end; excluded, but only if notified within the hour. Partial readings produce confident, wrong conclusions.
- **Accepting the drafter's aggregation.** Suppliers, business cases, and summaries bundle strong claims with weak ones so the strong carry the weak. Unbundle and grade separately — conjunctions fail on one false part.
- **Converting hedged status into firm commitment.** The most expensive misreading in supplier management: "expect to include, subject to testing" reported upward as "fix due next release". Quote hedges; don't launder them.
- **Person-shaped conclusions from process-shaped facts.** When a passage shows a reported error unactioned, the finding is the prioritisation process — not the engineer nearest the error. Summaries that name culprits where facts name processes fail both accuracy and leadership.
- **One clean observation closing a recurring pattern.** A single good Tuesday, one passed test, one quiet month — patterns earn closure through confirmation cycles, and reports should say which cycle they are on.
- **Treating caveats as decoration.** Sampling boundaries, "as drafted", "in testing" — the caveat is usually the researcher's or author's most careful sentence. Build your conclusion inside it, not around it.

<!-- APPEND -->
