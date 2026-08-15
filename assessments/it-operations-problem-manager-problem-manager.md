# Problem Manager - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a problem manager working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise deliberately, reflect honestly, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a problem manager, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — incident feeds from the service desk and monitoring, problem records and known error databases, root cause analyses, trend reports, change impact assessments, runbooks, and the recommendations you put in front of service owners — and the kinds of decisions you genuinely make, such as which recurring fault to investigate next, whether an analysis has truly reached root cause, how to coordinate a team of specialists across organisational boundaries, and how to make prevention stick in organisations that naturally prioritise the urgent over the important.

Why do these assessments matter for your role in particular? Your professional purpose is to resolve and control the root causes of incidents and prevent their recurrence — to pick up feeds from numerous sources and put in place continual improvements that stop regular service outages happening again. That purpose is cognitively demanding: root cause analysis is disciplined reasoning about evidence, and a plausible-but-wrong cause is your occupational hazard. It is numerically demanding: trends, recurrence rates, cost-of-fault arithmetic and KPI data are the currency in which problems are prioritised and fixes are justified. It is verbally demanding: you read specialists' reports and suppliers' bulletins precisely, and you write findings that must survive scrutiny in reviews. And it is judgement-demanding above all: coordinating investigations you do not personally perform, working closely with major incident managers whose urgency competes with your thoroughness, and telling organisations uncomfortable truths about why their incidents keep recurring — these are behavioural skills, and situational judgement tests measure exactly them.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment's dimensions to the specific skills in the problem manager capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format. Second, attempt the practice questions honestly — commit to an answer before reading the explanation. Third, treat every explanation as a mini-lesson: even when you answer correctly, the reasoning walkthrough will deepen your technique, exactly as a good root cause review deepens a team's diagnostic craft. Finally, use the preparation tips for self-reflection: they connect assessment performance back to your professional development as the person your organisation trusts to make incidents stop coming back.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. For a problem manager, it presents the everyday materials of your discipline — incident feeds, trend data, causal chains, known error records, change histories, and dependency information — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group; many platforms adapt difficulty to your performance, and employers typically receive accuracy and speed profiles rather than a single figure. Short unscored practice items usually precede the real test.

For your role, cognitive assessment is peculiarly on-the-nose, because problem management *is* applied cognition. Root cause analysis is logical deduction with evidence discipline: distinguishing correlation from cause, a contributing factor from a root cause, and a cause you can fix from a cause you can only name. Trend work is pattern recognition with statistical honesty: seeing the signal that three teams' separate tickets conceal, without hallucinating patterns in noise. Prioritising a problem backlog is structured judgement about impact, frequency, cost and risk. And coordinating an investigation is problem decomposition: choosing the next question whose answer most reduces uncertainty. A well-designed cognitive test rehearses each of these in miniature — which is why practising it genuinely sharpens the day job.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Pattern recognition** maps to **Problem management**: ensuring the right actions are taken to investigate, resolve and *anticipate* problems begins with recognising recurring structure in incident feeds — the five tickets that are one problem, the monthly rhythm nobody else sees.
- **Logical deduction** maps to **Problem management** and **Incident management**: root cause analysis that minimises the adverse impact of incidents means reasoning validly from symptoms, timelines and test results to causes — and refusing conclusions the evidence does not force.
- **Error checking** maps to **Asset and configuration management** and **Change management**: tracking, logging and correcting information, and analysing and assessing the impact of change, both require spotting the record or assessment that contradicts the rest.
- **Prioritisation** maps to **Ownership and initiative** and **Availability and capacity management**: taking accountability, being proactive in searching for potential problems, and managing components against KPIs all demand ranking a problem backlog by evidence rather than by noise.
- **Applied problem solving** maps to **Problem management** and **Service focus**: coordinating the team to investigate problems, implement solutions and take preventive measures — while seeing the bigger picture across groups of services — is structured problem solving as a management discipline.

### Practice questions

**Question 1 (easy) — Pattern recognition across incident feeds**

Your morning review of feeds shows these overnight and early-morning items:

1. Service desk: "Case system slow" — 08:05, Team North
2. Monitoring: database platform CPU at 95% — 08:00-08:20
3. Service desk: "Cannot log in to HR portal" — 08:10, one user
4. Service desk: "Case searches timing out" — 08:12, Team South
5. Monitoring: nightly batch overran, finished 08:15 (normally 06:30)

Which grouping best identifies a single candidate problem?

- A) Items 1, 3 and 4 — all are service desk tickets
- B) Items 1, 2, 4 and 5 — case-system slowness coinciding with database CPU saturation and an overrunning batch that was still executing during working hours
- C) Items 2 and 3 — both involve infrastructure
- D) Items 3 and 5 — both are about timing

**Correct answer: B**

**Explanation:** Group by causal plausibility, not by superficial category. Items 1 and 4 are the same symptom (case-system slowness) from different teams within minutes. Item 2 shows the shared database platform saturated across exactly that window. Item 5 supplies a candidate mechanism: a batch that normally finishes at 06:30 was still hammering the platform at 08:15 — during the login peak. Together they sketch a coherent story: overrunning batch → platform saturation → user-visible slowness. Item 3 is a single-user login issue on a different service with no connecting evidence. Option A groups by source (all service desk), C by vague category — both are the classification errors that keep real patterns invisible when feeds are reviewed carelessly. The problem-manager habit: your feeds are different *vantage points* on the same estate; the patterns live in their combination, which is precisely why your role picks up feeds from numerous sources.

**Question 2 (easy) — Root cause versus contributing factor**

An outage review establishes: the service failed when disk space ran out; disk space ran out because a log-cleaning job had been silently failing for weeks; the job failed because its service account password expired; monitoring did not alert on the failing job because job-failure alerts were never configured. Which statement best characterises "the service account password expired"?

- A) It is the root cause — the deepest fact in the chain.
- B) It is one cause in a chain, but the absence of job-failure alerting is a distinct, independent deficiency: fixing the password alone leaves the organisation blind to the next silent job failure, so both must be addressed.
- C) It is irrelevant — the root cause is the disk filling up.
- D) It is a user error and out of scope for problem management.

**Correct answer: B**

**Explanation:** Trace the structure. The causal chain runs: expired password → failed cleaning job → disk full → outage. The password expiry is the deepest link *in that chain* — but notice the fourth finding sits outside the chain: alerting that would have caught the failing job (whatever its cause) was never configured. That is a separate systemic weakness, and it is the more valuable finding, because password expiries, and a dozen other faults, will happen again — the question is whether they get to run silently for weeks. Fix both: a password process (rotation, service account monitoring) and job-failure alerting. A stops one link short of the full picture; C confuses the proximate cause with the root; D miscategorises a process gap as blame. Root cause analysis at your level routinely produces this two-track output: the specific cause of *this* outage, and the detection gap that let it grow — and assessments reward candidates who can hold both.

**Question 3 (easy) — Error checking a problem record**

You are quality-checking problem records before a review. One record reads:

| Field | Entry |
|---|---|
| Problem | Recurring email delivery delays |
| Linked incidents | 14 |
| First occurrence | 3 May |
| Root cause | Confirmed: mail queue misconfiguration |
| Status | Root cause under investigation |
| Workaround | Manual queue flush, documented |

Which inconsistency most needs correcting?

- A) 14 linked incidents is too many for one record.
- B) The root cause field says "Confirmed" while the status says "under investigation" — the record contradicts itself about the most decision-relevant fact.
- C) The first occurrence date is too long ago.
- D) A workaround should not be documented before root cause is confirmed.

**Correct answer: B**

**Explanation:** Scan for internal contradiction. The root cause field asserts confirmation; the status field says investigation continues. Both cannot be true, and the difference matters operationally: a confirmed root cause unlocks fix planning and changes what the service desk tells users, while an open investigation means resources are still allocated to diagnosis. Whichever field is stale, every consumer of this record — your analysts, the change team, the service owner — currently gets a coin-flip answer to "do we know why?". A, C and D assert rules that do not exist: heavily recurring problems legitimately link many incidents, long-running problems are common, and workarounds are routinely documented before causes are confirmed (that is what workarounds are for). Record hygiene is your **Asset and configuration management** discipline applied to your own artefacts — and reviewers who find one self-contradicting record start doubting the rest, which taxes everything you present afterwards.

**Question 4 (moderate) — Prioritising the problem backlog**

Four problems compete for your two available analysts this fortnight:

1. P-101: causes ~20 incidents/month, each 30 minutes' impact for one user; workaround exists; steady for a year.
2. P-102: caused 3 incidents in the last 6 weeks — but each was a full outage of a statutory reporting service, and frequency appears to be rising (0 in the previous quarter).
3. P-103: one incident ever, three months ago, no recurrence, cause unknown.
4. P-104: causes ~8 incidents/month on a retiring service; decommissioning completes in 6 weeks.

Which two problems should get the analysts?

- A) P-101 and P-104 — the highest incident counts
- B) P-102 and P-101 — the emerging high-severity problem and the largest steady drain
- C) P-102 and P-103 — the severe one and the mysterious one
- D) P-103 and P-104 — clear the small ones first

**Correct answer: B**

**Explanation:** Prioritise on impact × frequency × trajectory, adjusted for future relevance. P-102 leads on two dimensions: severity (full outages of a statutory service) and trajectory (0 → 3 in consecutive quarters — an emerging problem, and anticipating problems is written into your skill definition; investigating while frequency is still low is exactly when investigation is cheapest). P-101 is the classic steady drain: 20 incidents/month × 30 minutes = 10 user-hours monthly, modest per event but perpetual — worth an analyst now, because "stable and workarounded" faults are precisely the ones that otherwise run for years. P-104's arithmetic is decisive the other way: any fix lands roughly when the service retires, so the six weeks of incidents cost less than the investigation — monitor, apply workarounds, let decommissioning be the fix. P-103 is a single unrepeated event with no pattern to analyse; park it with a reopen trigger (recurrence) rather than spend a fortnight on one cold data point. A chases raw counts; C over-weights mystery — intellectual interest is not impact; D confuses "small" with "quick wins". The scored logic: severity-weighted trajectory first, steady cost second, doomed and dormant last.

**Question 5 (moderate) — Deduction from a timeline with a confounder**

Incidents on a service spiked in the week beginning 6 October. Two things happened around then: a new application version deployed on 3 October, and the annual benefit-application deadline fell on 10 October, historically doubling user traffic that week. Which investigation step most efficiently separates the two candidate causes?

- A) Roll back the application version and see whether the spike ends.
- B) Compare this year's deadline week against previous years' deadline weeks (same traffic surge, old version): if previous deadline weeks showed no comparable spike, the new version becomes the prime suspect; if they showed similar spikes, traffic load explains it.
- C) Wait until the week after the deadline — if incidents fall, traffic was the cause.
- D) Survey users about which version they prefer.

**Correct answer: B**

**Explanation:** The confounder is that both candidate causes changed together this week — but history provides a natural control group. Previous deadline weeks had the traffic surge *without* the new version, so their incident rates isolate the traffic effect cleanly: spikes then too → traffic-driven, and the fix conversation is capacity; no spikes then → the new version fails to cope where the old one did (either a defect, or a capacity regression — the follow-up test distinguishes). B extracts this answer from data you already hold, at zero operational risk. A is a live intervention with real rollback risk, and it is confounded in the same direction: if incidents fall after both the rollback *and* the passing deadline, you have learned nothing — which is also exactly C's flaw: post-deadline quiet is predicted by *both* hypotheses, so waiting discriminates nothing while users absorb a week of incidents. D measures preference, not causation. The transferable technique — find the historical comparison that varies one factor at a time — is the observational workhorse of root cause analysis, and test items reward reaching for it before reaching for interventions.

**Question 6 (moderate) — Error checking a change impact assessment**

Ahead of the change advisory board, you review an impact assessment for a database index change intended to fix problem P-230 (slow searches). It states: (i) "Affects the case management service only"; (ii) "The reporting warehouse reads the same tables nightly"; (iii) "Index rebuild runs 01:00-03:00, during which searches degrade"; (iv) "No interaction with the nightly warehouse extract, which runs 01:30-04:00". Which pair of statements needs challenging?

- A) (i) and (ii) — a service that reads the same tables is plausibly affected
- B) (ii) and (iii) — both mention timing
- C) (iii) and (iv) — the windows overlap, yet (iv) claims no interaction; and taken with (ii), statement (i)'s "only" is doubtful too
- D) Nothing needs challenging — the assessment is internally consistent

**Correct answer: C**

**Explanation:** Two challenges hide in these four sentences, and C names the sharper one plus its knock-on. First: the rebuild window (01:00-03:00) and the warehouse extract (01:30-04:00) overlap by ninety minutes, yet (iv) flatly asserts no interaction — an index rebuild on tables a heavy extract is simultaneously reading is a textbook contention scenario, so (iv) needs evidence, not assertion. Second, following the thread: if the warehouse reads the same tables (ii), then (i)'s "case management only" is also suspect. A catches that second issue but misses the direct timing contradiction, which is the assessment's most checkable — and most confidently wrong — claim. The reviewing habit this trains is your **Change management** skill at its most valuable: read impact assessments as claims to be cross-examined against each other, especially absolute words ("only", "no interaction") sitting next to facts that undermine them. A fix for one problem that births another is problem management's own recurring nightmare; the cross-examination is how you prevent it.

**Question 7 (moderate) — The trend that is not there**

A service owner shows you this and asks you to open a problem investigation: monthly incident counts for their service over six months: 22, 19, 24, 20, 25, 23. "The last month jumped from 25 to… wait — look, three of the last four months are above 21. It's trending up." What is the statistically honest reading?

- A) The service owner is right: three high months of four is a trend.
- B) The counts oscillate between 19 and 25 with no sustained direction — the "trend" is normal month-to-month variation, and an investigation should wait for a genuine signal, though you can agree a threshold with the owner that would trigger one.
- C) The counts are trending down, since the final value (23) is below the peak (25).
- D) Six months of data can never support any conclusion.

**Correct answer: B**

**Explanation:** Look at the sequence's shape: 22, 19, 24, 20, 25, 23 — it alternates up and down around a level of roughly 22, ending within one incident of where it started. Every value sits inside a narrow band (19-25); there is no run of consecutive increases, and the "three of four above 21" observation is selection — with a midpoint around 22, half the months will sit above 21 in any period. A genuine emerging trend looks like Question 4's P-102: consecutive movements in one direction, or a step to a new sustained level. C commits the mirrored error (two cherry-picked points). D is over-scepticism — six months is plenty to characterise variation; it simply characterises *stability* here. The professional finish is B's second clause: rather than a bare "no", agree a trigger with the owner ("two consecutive months above 27, or any month above 30, and we open it") — which respects their concern, defines the signal in advance, and protects your analysts from investigating noise. Guarding the boundary between signal and noise is a core problem-manager duty: every noise investigation you accept is a real problem's analyst-fortnight spent on nothing.

**Question 8 (moderate) — Choosing the next diagnostic action**

A recurring fault (intermittent transaction failures, ~2% of transactions, no obvious pattern) has an investigation stalled between three hypotheses: (H1) a race condition under concurrent load; (H2) a malformed-data issue from one upstream source; (H3) intermittent network drops to the payment gateway. The failed transactions are logged with full context. Which single analysis most efficiently discriminates between the hypotheses?

- A) Add more logging and wait a month for new data.
- B) Profile the existing failed transactions against each hypothesis's signature: correlation with concurrency levels (H1), concentration by upstream source (H2), and clustering with gateway timeout errors (H3) — each signature implicates one hypothesis and exonerates others.
- C) Fix all three possible causes simultaneously to be safe.
- D) Reproduce the fault in a test environment by trial and error.

**Correct answer: B**

**Explanation:** The stem's key sentence is "logged with full context" — the discriminating evidence already exists, and each hypothesis makes a different testable prediction about it. If failures spike when concurrency is high, H1 gains; if 80% of failures trace to one upstream source, H2 gains; if failures co-occur with gateway timeouts, H3 gains. One afternoon of profiling can settle what a month of new logging (A — which ignores the data in hand) or an open-ended reproduction hunt (D — expensive for intermittent faults, and unnecessary when production evidence is rich) would settle slowly. C is the tempting managerial shortcut with three hidden costs: triple engineering spend, no learning (when failures stop you cannot say which fix worked, so the next similar fault restarts from zero), and tripled change risk on a live service. The technique — derive each hypothesis's observable signature, then test all signatures against existing evidence — is the single highest-leverage move in root cause analysis, and it is precisely how you coordinate a stalled team back into motion: give each specialist a signature to check.

**Question 9 (challenging) — The fix that worked for the wrong reason**

Problem P-310 (weekly report generation failures) was closed after a fix: the report service was moved to a larger server, and failures stopped. Two months later, failures resume — same symptoms. Reviewing the original analysis, an analyst notes: the failures had stopped in the week *before* the server move, immediately after a separate team quietly halved the report's input data volume during an unrelated clean-up; volumes have since regrown past their old level. What does this history most strongly suggest?

- A) The larger server fixed the problem, and an even larger server is now needed.
- B) The original "fix" was likely coincidental: the failures track input data volume, not server capacity — the true mechanism is probably volume-sensitive (a timeout, a memory ceiling in the report code), and the reopened investigation should test against volume directly.
- C) The other team's clean-up caused the current failures.
- D) The problem is unfixable and should be converted to a permanent workaround.

**Correct answer: B**

**Explanation:** Reconstruct the timeline honestly: failures stopped *before* the intervention that got the credit — which breaks the causal story the closure relied on — and the event that does align with the recovery (volume halving) also aligns, in reverse, with the recurrence (volume regrowth past the old level). Cessation and resumption both tracking volume is a strong signature: the mechanism is probably something that degrades with input size and cliff-edges at a threshold — and the larger server may even have raised that threshold slightly, muddying the picture further. A doubles down on the discredited story and starts an expensive hardware ratchet: each upgrade buys quiet until volumes grow again — cost without cure. C inverts the logic: the clean-up *relieved* the symptom; regrowth is normal operations re-approaching an unaddressed limit. D gives up on a problem that has just become more tractable, not less — a volume-correlated failure is eminently testable (vary input size, find the cliff, read the failing component's behaviour at it). Two professional lessons: verify fixes against the *mechanism*, not just the symptom's silence — "failures stopped after our change" must survive the question "did they stop *because* of it?" — and treat recurrence after closure not as failure but as new, unusually informative evidence. This is what "perform root cause analysis" means when done to completion.

**Question 10 (challenging) — Coordinating under a dependency clash**

The permanent fix for P-278 requires three sequential pieces of work: the supplier patches their module (3 weeks from order), then your applications team integrates and tests (2 weeks, cannot start before the patch arrives), then deployment in a monthly release window (releases go live on the first Monday of each month; integration must be *complete* before a release's code-freeze, which falls one week before go-live). It is Monday 1 September, a go-live day. If you order the supplier patch today, what is the earliest release that can carry the fix?

- A) The 6 October release
- B) The 3 November release
- C) The 1 December release
- D) It cannot be scheduled without more information

**Correct answer: B**

**Explanation:** Walk the chain forward. Patch ordered Monday 1 September, arriving 3 weeks later: Monday 22 September. Integration and test, 2 weeks from arrival: complete Monday 6 October. Now map to release gates: the October release goes live Monday 6 October with code-freeze one week earlier (29 September) — integration finishes a week too late, so October is missed. The November release (first Monday: 3 November) freezes on 27 October; integration completing 6 October comfortably precedes that freeze. Earliest carrying release: 3 November — option B. The trap answer A comes from comparing integration completion (6 October) with the go-live date (6 October) and forgetting the freeze sits a week earlier: fixes must beat the *freeze*, not the launch. This is the coordination arithmetic your skill definition means by "co-ordinate the team to investigate problems, implement solutions and take preventive measures" — three parties' timelines composed against a governance calendar — and the practical corollary is worth absorbing: a one-day delay in ordering that patch would not have mattered here, but had integration slipped even two days past a freeze, the fix would wait another month. Order long-lead items immediately; know your freeze dates cold.

**Question 11 (challenging) — Anticipating a problem before it exists**

Reviewing capacity and incident data across services (your role's bigger-picture view), you notice: (i) the document store's storage utilisation grows 5 percentage points monthly and stands at 70%; (ii) a policy change in eight weeks will require caseworkers to attach roughly double the documents per case; (iii) the store's incident history shows that a similar service began throwing intermittent write failures at about 92% utilisation before anyone predicted trouble. No incidents have occurred yet. What is the strongest action?

- A) Nothing yet — problem management responds to incidents, and there are none.
- B) Raise a proactive problem record now: on current growth the store reaches ~90% in four months, but the policy change in two months will steepen the curve sharply; propose capacity expansion (or archival) scheduled to complete before the policy lands, citing the comparator service's failure threshold as evidence.
- C) Wait until utilisation reaches 92%, then declare an incident and act with proper urgency.
- D) Email the storage team a general warning to "keep an eye on the document store".

**Correct answer: B**

**Explanation:** Assemble the three facts into a projection: baseline growth alone reaches ~90% around month four; but the policy change at month two roughly doubles the growth driver, so the danger zone arrives much sooner — plausibly around month three, with the comparator service's history (write failures near 92%) supplying an evidence-based failure threshold rather than a guess. That is a *predictable* problem with a *deadline*, and B converts it into the artefact your organisation can act on: a proactive problem record with a projection, a threshold, a proposed measure, and a completion date pinned to the policy change — prevention with a business case. A misstates your own discipline: your skill definition says *anticipate* problems, and your role definition says be proactive in searching for potential problems; reactive-only problem management is half the job. C is A with a countdown attached — deliberately scheduling the crisis. D discharges the worry without transferring the analysis: "keep an eye on it" carries none of the projection, threshold or deadline that make action fundable and schedulable; warnings without artefacts evaporate. The examiner's pattern: proactive-problem items reward the option that produces a *formal, evidenced, deadline-bearing record* — the same standard as reactive work, applied before the first incident instead of after the fortieth.

**Question 12 (challenging) — Reading a multi-cause incident honestly**

A serious outage occurred when three things aligned: a fault in a load balancer (dormant for months), a configuration error made during Tuesday's routine change (which activated the fault), and an on-call engineer's misdiagnosis that extended the outage by two hours (the runbook's decision tree did not cover the observed symptom combination). The service owner asks: "So what was THE root cause?" Which answer best serves the organisation?

- A) "The configuration error — the person who made it triggered everything."
- B) "The load balancer fault — it was there first."
- C) "The outage had no single root cause: a latent fault, an activating change error, and a runbook gap that turned a misdiagnosis into two extra hours all contributed — and each yields a distinct preventive action: fix the fault, strengthen pre-change validation for that configuration class, and extend the runbook's decision tree. Treating any one as 'THE cause' leaves the other two armed."
- D) "The engineer's misdiagnosis — the outage would have been short without it."

**Correct answer: C**

**Explanation:** Serious failures in complex systems are characteristically conjunctions: a latent condition, a trigger, and a degraded response, each necessary and none sufficient. Options A, B and D each perform the same operation — collapsing the conjunction onto one factor — and each collapse does organisational damage: A and D pin systemic weaknesses on individuals (the config error was survivable-by-design if validation catches it; the misdiagnosis was the *runbook's* gap given an uncovered symptom set — blaming the people ensures the next person inherits the same traps, plus a culture that hides errors from your investigations); B stops at the oldest fact, as if latency conferred primacy. C does what mature root cause analysis does: names all three contributing causes, attaches a specific preventive action to each, and — the managerially crucial move — explains *why* the single-cause framing is itself a risk. Your role definition's phrase "deal with problems and root cause analysis" means being the person in the room who can decline the seductive question "what was THE cause?" without declining accountability: three causes, three fixes, all tracked. When a stakeholder wants one sentence, give them C's first clause — "several things had to align, and we are fixing each of them" — which is both true and more reassuring than any scapegoat.

### Preparation tips

- **Practise on your own feeds.** Each morning for a week, spend five minutes grouping the previous day's incidents and monitoring events by candidate common cause before reading anyone else's triage. This is direct rehearsal of the test's pattern items using live data.
- **Rehearse the signature technique.** For any open problem, write down what evidence each live hypothesis *predicts* you should find, then check. The discipline of "derive the signature, then look" is the highest-value habit in both the test and the job.
- **Drill timeline arithmetic.** Sequencing questions (patches, freezes, release windows) reward methodical forward-walking. Practise on your real change calendar: pick a hypothetical fix and compute its earliest release, including the freeze.
- **Interrogate closed problems.** Revisit two or three of your team's closed records and ask: did we verify the mechanism, or just observe silence? Question 9's pattern — the coincidental fix — hides in most backlogs, and finding one is better training than any practice set.
- **Time-box easy items.** Managers lose test marks by over-verifying questions they solved in ten seconds. Practise trusting your first careful pass on easy items and banking the time for the multi-step ones.
- **Review errors by mechanism.** After practice sessions, label each miss: anchored, cherry-picked, missed a freeze date, collapsed a conjunction. You would demand mechanism-level findings from a post-incident review; give yourself the same quality of feedback.

### Common pitfalls to avoid

- **Declaring root cause at the first plausible link.** "Password expired" feels like an answer; the alerting gap behind it is the finding that prevents the next five silent failures. Follow chains to the systemic level, and check for causes *outside* the chain.
- **Trusting a fix because symptoms stopped.** Verify mechanism, not silence — especially when something else changed around the same time. The coincidental fix is problem management's most expensive illusion.
- **Seeing trends in oscillation.** Cherry-picked endpoints and "three of the last four" observations manufacture trends from noise. Look for consecutive movement or sustained level shifts before committing analysts.
- **Prioritising by raw incident count.** Severity, trajectory and future relevance can all outrank volume — a retiring service's noisy problem may deserve nothing, while a statutory service's three outages deserve everything.
- **Fixing all hypotheses at once.** Shotgun remediation triples cost and risk and teaches you nothing — when the symptoms stop, you cannot say why, so the learning that prevents the next fault never happens.
- **Comparing against go-live instead of code-freeze.** In any scheduling item (and any real release), the gate that matters is the earliest one. Walk every dependency to the *first* deadline it must beat.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from numerical information of the kind your role genuinely produces: incident and recurrence counts, trend series, availability and KPI figures, cost-of-fault and cost-of-fix arithmetic, and the tables that populate problem reviews and service reports. Calculators are usually permitted — the test measures whether you choose the right calculation and read data accurately, not mental agility for its own sake.

Typical format: an online, timed test of 20 to 35 minutes with 15 to 25 questions, each presenting a table, chart or short data description followed by multiple-choice options. Questions typically require percentages, ratios, weighted averages, rates, and simple projections; the harder items chain two or three steps or embed an interpretation trap — the right arithmetic on the wrong base, the average that conceals the tail, the trend read from cherry-picked points.

For a problem manager, numbers are not decoration; they are the argument. Which problem gets investigated first is a numerical case: frequency × impact × trajectory. Whether a fix is worth its cost is a numerical case: recurring cost against one-off investment. Whether a fix *worked* is a numerical case: recurrence rates before and after, honestly baselined. Your continual improvement remit lives or dies on measurement — "regular service outages stopped recurring" is a claim about counts — and your credibility with service owners, change boards and finance colleagues depends on arithmetic that survives checking. Employers test numeric reasoning for this role because a problem manager whose percentages wobble loses the authority to redirect other teams' effort, which is most of what the role does.

### How this assessment maps to your role

- **Trend and recurrence arithmetic** maps to **Problem management**: investigating patterns and trends, and demonstrating that preventive measures worked, are exercises in rates, baselines and before/after comparison.
- **Impact and cost quantification** maps to **Problem management** and **Ownership and initiative**: the case for each fix — and your accountability for recommending it — rests on cost-of-fault versus cost-of-fix arithmetic done honestly.
- **KPI and availability figures** maps to **Availability and capacity management**: managing service components against business needs and KPIs requires fluent conversion between percentages, hours and thresholds.
- **Weighted combination across services** maps to **Service focus**: the bigger-picture view across groups of services demands combining unequal figures correctly — weighted, never naively averaged.
- **Change and schedule arithmetic** maps to **Change management**: assessing the impact of change includes computing windows, durations and clashes.
- **User-impact data** maps to **User focus**: quantitative data about users — who is affected, how often, how badly — is how user focus becomes prioritisation rather than sentiment.

### Practice questions

**Question 1 (easy) — Share of incidents from known problems**

Last month the service desk logged 480 incidents. Of these, 168 were linked to existing problem records. What percentage of incidents came from known problems?

- A) 30%
- B) 35%
- C) 40%
- D) 45%

**Correct answer: B**

**Explanation:** Share = part ÷ whole × 100. Step 1: 168 ÷ 480 = 0.35. Step 2: × 100 = 35%. Quick check: 10% of 480 is 48, so 35% is 3.5 × 48 = 168 — confirmed. This single figure is one of your discipline's headline metrics: it says a third of the desk's workload is *predictable* — incidents your open problems are already forecasting. Tracked over time, it tells a story either way: rising means known problems are not getting fixed; falling means fixes are landing or new unknowns are arriving. Either way, you want the number exact before you build the story.

**Question 2 (easy) — Did the fix reduce recurrence?**

A permanent fix for a recurring login fault deployed at the end of March. Monthly incident counts for that fault: January 44, February 40, March 42, April 6, May 4. What was the percentage reduction comparing the March count with the May count?

- A) 80%
- B) 85%
- C) 90%
- D) 95%

**Correct answer: C**

**Explanation:** Step 1: reduction = 42 − 4 = 38. Step 2: divide by the pre-fix baseline (March): 38 ÷ 42 = 0.904…. Step 3: × 100 ≈ 90%. The question names its comparison months — March and May — so resist averaging or picking other months; in tests, compute exactly what is asked. Professionally, note the residual: 4-6 incidents a month persist post-fix. Before celebrating, you would check whether those are the same fault lingering in an unfixed pathway, or different faults previously miscategorised under the same banner — a 90% reduction is a success; the last 10% is either a follow-up task or a categorisation lesson. Fix verification is a before/after rate comparison plus an honest look at the remainder.

**Question 3 (easy) — Reading a problem review table**

The quarterly review table shows:

| Problem | Linked incidents this quarter | Change vs last quarter | Fix status |
|---|---|---|---|
| P-201 | 36 | +12 | Fix scheduled |
| P-214 | 28 | −20 | Fix deployed |
| P-222 | 31 | +2 | Under investigation |
| P-230 | 15 | +9 | Under investigation |

Which problem shows the fastest *proportional* growth in linked incidents?

- A) P-201
- B) P-214
- C) P-222
- D) P-230

**Correct answer: D**

**Explanation:** Proportional growth compares the change against the previous quarter's level, which you reconstruct from the two given columns. P-201: previous = 36 − 12 = 24; growth = 12 ÷ 24 = 50%. P-222: previous = 29; growth = 2 ÷ 29 ≈ 7%. P-230: previous = 15 − 9 = 6; growth = 9 ÷ 6 = 150%. (P-214 fell.) The fastest proportional growth is P-230 — from 6 to 15, one and a half times its former size — even though P-201 added the same-or-more in absolute terms from a bigger base. Both views matter: absolute growth (P-201) shows where workload is piling up; proportional growth (P-230) is the early-warning signature of an emerging problem still small enough to fix cheaply. The table-reading discipline — derive the missing baseline before judging — is exactly the care that keeps quarterly reviews honest.

**Question 4 (moderate) — Cost of a recurring problem**

A recurring fault causes 14 incidents per month. On average, each incident consumes 1.5 hours of a technician's time (£35/hour) and interrupts 20 users for 30 minutes each (average £28/hour). What is the approximate monthly cost of the fault?

- A) £735
- B) £3,920
- C) £4,655
- D) £6,240

**Correct answer: C**

**Explanation:** Cost one incident first. Technician: 1.5 × £35 = £52.50. Users: 20 users × 0.5 hours × £28 = £280. Per incident: £52.50 + £280 = £332.50. Monthly: 14 × £332.50 = £4,655. The distractors are diagnostic: £735 is technician time only (14 × £52.50) — the error of costing the fixers and forgetting the interrupted; £3,920 is user time only; £6,240 miscomputes the user interruption at a full hour. The structural lesson is that user impact dominates: £280 of the £332.50 per incident is users, not IT — which is usually the case, and which is why cost-of-fault arithmetic that includes users' time makes fixes look as valuable as they truly are. This number is the first half of every business case you will write; the second half is Question 5.

**Question 5 (moderate) — Payback period for the fix**

The fault in Question 4 costs £4,655 per month. The permanent fix requires 5 days of a developer (8 hours/day at £55/hour) plus a £2,500 supplier fee. How long until the fix pays for itself?

- A) About 2 weeks
- B) About 1 month
- C) About 2 months
- D) About 4 months

**Correct answer: B**

**Explanation:** Cost the fix: developer = 5 × 8 × £55 = £2,200; plus supplier £2,500; total £4,700. Payback = £4,700 ÷ £4,655 per month ≈ 1.01 months — about one month. After that, the fix returns roughly £4,655 every month indefinitely (about £56,000 a year). Present it that way: "pays for itself in a month, then saves £4.7k monthly" is the sentence that turns a maintenance request into an obvious decision. Note the honest-arithmetic habits: include *all* fix costs (the supplier fee more than matches the developer time), and use the full fault cost from Question 4 — a payback computed against technician-time-only (£735/month) would show 6.4 months and might sink a fix that actually repays in one. Prevention cases die from underestimated fault costs far more often than from overestimated fix costs.

**Question 6 (moderate) — Weighted recurrence across services**

You report a combined "repeat incident rate" (incidents linked to known problems) across three services: Service A — 400 incidents, 30% repeats; Service B — 100 incidents, 60% repeats; Service C — 500 incidents, 20% repeats. What is the overall repeat rate?

- A) 36.7% — the average of the three rates
- B) 28% — total repeats (280) divided by total incidents (1,000)
- C) 30% — the middle value
- D) 20% — the largest service dominates

**Correct answer: B**

**Explanation:** Combine through raw numbers. Repeats: A = 0.30 × 400 = 120; B = 0.60 × 100 = 60; C = 0.20 × 500 = 100. Total repeats = 280; total incidents = 400 + 100 + 500 = 1,000. Overall rate = 280 ÷ 1,000 = 28%. The trap answer A averages the percentages ((30 + 60 + 20) ÷ 3 = 36.7%), silently treating a 100-incident service as equal to a 500-incident one — overweighting Service B's admittedly alarming 60% by a factor of five. That 60% is still your most interesting *finding* (B's users suffer repeat incidents at triple C's rate — worth its own investigation), but it must not distort the *combined* figure a service owner will quote. The rule to keep: rates combine through their numerators and denominators, never through each other — and the exceptions you notice on the way are findings, not weighting errors.

**Question 7 (moderate) — Availability arithmetic for a KPI conversation**

A service has a 99.7% availability KPI, measured monthly over its 600 service hours. Recurring problem P-244 caused three outages this month totalling 2.4 hours; other causes added 0.4 hours of downtime. Did the service meet its KPI, and how much of the breach (if any) is attributable to P-244?

- A) Met the KPI — total downtime 2.8 hours is small.
- B) Missed the KPI: the allowance is 1.8 hours, total downtime was 2.8 hours, and P-244 alone (2.4 hours) exceeded the entire allowance — the KPI would have been met without it.
- C) Missed the KPI, but no single cause is responsible.
- D) Met the KPI because 99.7% of 600 hours allows 18 hours of downtime.

**Correct answer: B**

**Explanation:** Step 1: allowance = (100% − 99.7%) × 600 = 0.003 × 600 = 1.8 hours. Step 2: actual downtime = 2.4 + 0.4 = 2.8 hours — exceeds 1.8, so the KPI was missed (achieved availability: 597.2 ÷ 600 = 99.53%). Step 3: attribution — P-244's 2.4 hours alone exceeds the whole 1.8-hour allowance; without P-244, downtime would have been 0.4 hours, comfortably within allowance. So the breach is attributable to P-244 in the strong sense: no P-244, no breach. D slips a decimal (0.3% of 600 is 1.8, not 18); A substitutes feel for arithmetic; C is refuted by the attribution step. This calculation pattern — allowance, actual, attribution — is precisely how you connect a problem record to a KPI breach, which is often the argument that gets a fix prioritised: "this single problem consumed 133% of the month's entire downtime budget" is **Availability and capacity management** speaking in a dialect service owners act on.

**Question 8 (moderate) — Projecting a backlog honestly**

Your problem backlog: 24 open records. Each month, on average, 6 new problems are opened and 4 are closed. If nothing changes, how many will be open in 6 months, and what closure rate would hold the backlog flat?

- A) 36 open; closures would need to rise to 6/month
- B) 30 open; closures would need to rise to 5/month
- C) 36 open; closures are fine as they are
- D) 24 open; the backlog is already flat

**Correct answer: A**

**Explanation:** Step 1: net monthly change = 6 opened − 4 closed = +2. Step 2: over 6 months: +12, so 24 + 12 = 36 open. Step 3: flat backlog requires closures = arrivals = 6/month. That is option A. The management insight sits behind the arithmetic: a backlog growing by 2 per month is not "roughly stable", it is 50% bigger in half a year — and problem backlogs age badly, because old unfixed problems keep generating incidents (their cost compounds even while the record count merely creeps). The follow-up questions the projection should trigger are your real work: can closure capacity rise (more analyst time, simpler fixes first)? Should arrival quality tighten (are all 6 monthly openings genuine problems, or is noise getting recorded — Question 7 of the cognitive section)? Small steady net rates are how queues quietly become crises; computing them is how you catch it six months early.

**Question 9 (challenging) — Before/after with a changing denominator**

A fix for a printing problem deployed in June. Printing incidents: May 60, July 45. But the organisation also shrank: May had 4,000 active users, July 3,000 (an office closed). A colleague says: "Incidents fell 25% — decent, but the fix underperformed expectations." What do the per-user rates show?

- A) The colleague is right: a 25% fall is the true effect.
- B) Per-user rates are identical: 0.015 in both months, so the fix achieved nothing at all.
- C) May: 60 ÷ 4,000 = 0.015 incidents/user; July: 45 ÷ 3,000 = 0.015 incidents/user — per user, nothing changed: the entire 25% fall is explained by having fewer users, and the evidence suggests the fix had no measurable effect.
- D) Rates cannot be compared across months with different user counts.

**Correct answer: C**

**Explanation:** Compute the rates. May: 60 ÷ 4,000 = 0.015 incidents per user. July: 45 ÷ 3,000 = 0.015 incidents per user. Identical. The 25% fall in raw counts (60 → 45) exactly matches the 25% fall in users (4,000 → 3,000) — the "improvement" is the denominator shrinking, not the fault retreating. So the honest reading is C: the fix shows no measurable per-user effect, and the investigation should reopen (wrong root cause? fix not reaching the failing pathway?). Note the difference between C and B: the *rates* are the same claim, but B's "achieved nothing at all" overreaches slightly — C's "no measurable effect, evidence suggests" is the calibrated version, and calibration matters when you are about to tell a team their fix did not work. D gives up exactly where normalisation succeeds — differing denominators are *why* you compute rates, not a reason you cannot. This trap — verifying fixes against raw counts while the population shifts — catches real problem managers every year; office closures, seasonal staff, and service migrations all move denominators. Normalise before you celebrate.

**Question 10 (challenging) — Which problem drains most user time?**

Four recurring problems, one analyst slot. The data:

| Problem | Incidents/month | Avg users affected per incident | Avg disruption per user (minutes) |
|---|---|---|---|
| P-301 | 40 | 1 | 60 |
| P-302 | 6 | 150 | 15 |
| P-303 | 12 | 25 | 20 |
| P-304 | 2 | 400 | 10 |

Ranked by total user-hours lost per month, which problem should the analyst take first?

- A) P-301 — most incidents
- B) P-302 — big user numbers and moderate frequency
- C) P-303 — the balanced middle case
- D) P-304 — the biggest single events

**Correct answer: B**

**Explanation:** Compute total user-minutes for each: P-301: 40 × 1 × 60 = 2,400 (40 hours). P-302: 6 × 150 × 15 = 13,500 (225 hours). P-303: 12 × 25 × 20 = 6,000 (100 hours). P-304: 2 × 400 × 10 = 8,000 (about 133 hours). Ranking: P-302 (225h) > P-304 (133h) > P-303 (100h) > P-301 (40h). The analyst goes to P-302 — which tops neither the incident count (P-301 does), nor users-per-event (P-304), nor per-user disruption (P-301): it wins on the *product*, which no single column reveals. That is the point: prioritising by any one column picks a different — wrong — problem, and each distractor is exactly one column's champion. Frequency × breadth × depth is the impact arithmetic your prioritisation should run by default, and it is **User focus** made quantitative: the question "who is losing the most time?" has a computable answer, and the loudest problem (P-301, forty tickets a month) is here the *smallest* drain. In real work you would layer severity nuances on top (P-304's mass events may carry reputational weight), but the user-hours baseline comes first.

**Question 11 (challenging) — Trend with seasonality: is the fix working?**

A fix for a case-system problem deployed at the end of September. Monthly linked incidents: July 30, August 32, September 34, October 28, November 26. A stakeholder says: "Only a 24% drop from September — disappointing." However, your records show last year's counts (no fix, same system): July 28, August 30, September 33, October 40, November 44 — the autumn caseload surge historically *increases* incidents by around 30% into November. What is the fairest assessment of the fix?

- A) The stakeholder is right — a 24% drop is modest.
- B) Against the seasonal counterfactual the fix looks strong: last year incidents *rose* ~33% from September to November (33 → 44); this year they *fell* 24% (34 → 26) despite the same surge — comparing November actual (26) with a seasonal expectation of ~44, the fix is suppressing roughly 40% of expected incidents.
- C) The fix made things worse in September.
- D) Two months of data can support no conclusion.

**Correct answer: B**

**Explanation:** The naive before/after (34 → 26, a 24% drop) understates the effect because the season was pushing the other way. Build the counterfactual from last year: September → November rose from 33 to 44, a ~33% seasonal climb. Apply that to this year's September (34): expected November ≈ 34 × 1.33 ≈ 45 without a fix. Actual November: 26. The fix is plausibly preventing around 19 of 45 expected incidents — roughly 40% suppression — while simultaneously *reversing* the seasonal direction (fell while it always rises). That is B. A reads the raw delta without the seasonal baseline — the same class of error as Question 9, but with time instead of population as the shifting denominator. C misreads September (pre-fix; the fix landed at month-end). D is too defeatist: two months against a well-documented seasonal pattern is real evidence — you would keep monitoring, but the direction reversal is exactly what effectiveness looks like. The transferable method: verify fixes against *what would have happened*, not just what came before — and when you present it, show the stakeholder both numbers, because "24% down in the rising season, 40% against expectation" is a stronger and more honest sentence than either figure alone.

**Question 12 (challenging) — The improvement target arithmetic**

Your continual improvement objective: reduce repeat incidents (incidents linked to known problems) by 40% within two quarters. Baseline quarter: 900 repeat incidents. Your three planned fixes address problems currently generating 320, 180, and 120 repeat incidents per quarter respectively, with expected effectiveness of 90%, 75%, and 50%. If all land on schedule and nothing else changes, do you hit the target?

- A) Yes — comfortably, with about 483 incidents prevented (54%)
- B) Yes — just: 288 + 135 + 60 = 483 prevented, which is 53.7% against a 40% target of 360
- C) No — only 483 of the 620 addressed incidents are prevented, and 620 was the relevant base
- D) No — effectiveness percentages cannot be combined this way

**Correct answer: B**

**Explanation:** Work each fix: 320 × 0.90 = 288 prevented; 180 × 0.75 = 135; 120 × 0.50 = 60. Total prevented = 288 + 135 + 60 = 483 per quarter. Target: 40% of the 900 baseline = 360. Since 483 > 360, the target is met — projected repeat incidents fall to 900 − 483 = 417, a 53.7% reduction. So B (and A's numbers agree; the difference is the word "comfortably" versus "just" — 483 against 360 is a 34% margin, so "comfortably" is defensible, but B is the answer because its arithmetic is *shown* and its comparison explicit; in a test, prefer the option whose stated reasoning is complete and correct). C misapplies the base: the target was defined against total repeats (900), not against the subset addressed. D is false — expected preventions do sum when the problems are independent, which linked-incident counts to distinct problems are. Two professional footnotes worth carrying into real plans: the margin (483 vs 360) is your insurance against a fix slipping a month or underperforming its effectiveness estimate — plan for margin deliberately; and "nothing else changes" is the assumption doing the heaviest lifting — new problems will arrive during those two quarters, so track the *rate*, not just the plan. This is the arithmetic of continual improvement, which is your role's defining phrase.

### Preparation tips

- **Master the six moves.** Part-of-whole percentages, percentage change against the right baseline, weighted combination through raw numbers, per-unit rates (user, month, opportunity), frequency × breadth × depth impact products, and cost/payback arithmetic. They cover almost every question — and almost every business case you will ever write.
- **Always name your denominator.** Before dividing, say what the base is: baseline month, total incidents, user population, addressed subset. Most traps in the test — and most disputes in reviews — are denominator disputes.
- **Build counterfactuals on real data.** Practise Question 11's method on your own estate: take a deployed fix, find the seasonal or population baseline, and compute effect-against-expectation. It is the strongest fix-verification technique available and superb test preparation.
- **Recompute one report monthly.** Take a service report you receive and rebuild its headline figures from raw columns. Realistic practice, and an audit of numbers you were about to trust.
- **Sanity-check magnitudes.** 0.3% of 600 hours is 1.8, not 18; a fall from 42 to 4 is ~90%, not ~40%. A two-second plausibility pass catches the decimal slips that timed conditions invite.
- **Practise presenting both numbers.** Raw change and normalised change; absolute growth and proportional growth; share of majors and per-opportunity rate. The habit of holding both views is what the hardest questions — and the sharpest stakeholders — test.

### Common pitfalls to avoid

- **Right arithmetic, wrong base.** Percentage change uses the pre-period; targets use their defined baseline; rates use the population. Check the base before the calculator.
- **Averaging rates across unequal groups.** Percentages combine through raw numerators and denominators. If the group sizes differ and you averaged the rates, you are wrong by construction.
- **Verifying fixes on raw counts.** Populations shrink, seasons turn, services migrate. Normalise per user and per season before declaring a fix effective — or ineffective.
- **Prioritising by a single column.** Incident count, users-per-event and minutes-per-user each crown a different problem; only their product finds the real drain.
- **Forgetting users in cost arithmetic.** Technician time is usually the small half. Cost the interrupted, not just the fixers, or every prevention case you write will be undersold.
- **Treating projections as stable facts.** "+2 per month" compounds; "nothing else changes" never holds. State assumptions, plan margins, and track rates after the plan launches.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you extract meaning from the written material your role runs on: problem management procedures, root cause analysis reports, supplier bulletins, runbook extracts, post-incident reviews, and the emails in which specialists hedge, assert and qualify their findings. The dominant format presents a passage followed by statements to classify as **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage gives insufficient information). Additional items test inference, main-point identification, argument evaluation, and judgement about clear writing.

Typical format: an online, timed test of 15 to 25 minutes with 20 to 30 statements across several passages, often adaptive. The governing rule is strict: answer only from the passage, suspending your own operational knowledge even where the passage differs from your department's practice.

For a problem manager, verbal precision is a load-bearing professional skill in both directions. Reading: root cause analysis consumes text — specialists' reports whose "consistent with" must not become "confirmed" in your retelling, supplier bulletins whose scoping clauses determine who is affected, procedures whose "must/may/only" allocate authority. A problem manager who reads loosely contaminates the record at its source. Writing and judging writing: your findings travel — into reviews, change boards, service owner briefings — and they must state exactly what the evidence supports, at the right level of certainty, in language each audience can act on. Employers test verbal reasoning for this role because the entire problem management value chain — evidence, analysis, finding, recommendation — is transmitted in prose, and every imprecision compounds downstream.

### How this assessment maps to your role

- **Precise reading of procedures and criteria** maps to **Change management** and **Incident management**: analysing change impact and leading investigation within defined processes requires exact parsing of what documents mandate, permit and forbid.
- **True/False/Cannot say discipline** maps to **Problem management** and **Asset and configuration management**: recording what an investigation has established — and only that — is the textual form of evidence discipline; problem records must not claim more than their sources.
- **Certainty-level tracking** maps to **Problem management**: root cause analysis lives on the gradient between "possible", "likely" and "confirmed"; preserving each claim's position on that gradient is the core of honest analysis.
- **Argument evaluation** maps to **Community collaboration** and **Ownership and initiative**: reviews and retrospectives (including Agile health checks) require separating valid grievances from invalid conclusions, and giving feedback that is effective and lasting.
- **Runbook and continuity text comprehension** maps to **Continuity management**: managing and testing runbooks starts with reading their conditions, branches and preconditions exactly.
- **Audience-fit writing judgement** maps to **User focus** and **Service focus**: findings and recommendations must land with users, service owners and boards — each needing different altitude, none needing distortion.

### Practice questions

**Passage 1 (for Questions 1-4):**

"A problem record must be raised when trend analysis identifies three or more incidents with a suspected common cause, or when a major incident review recommends one. Problem records may also be raised proactively where analysis indicates a significant risk of future incidents. Each problem record must have a named owner within the problem management team. Root cause must be recorded as 'confirmed' only where testing has demonstrated the causal mechanism; otherwise it must be recorded as 'suspected'. A known error record must be created once a root cause is confirmed and a workaround is documented. Problem records may be closed only when the permanent fix is deployed and post-deployment monitoring has shown no recurrence for one full reporting period."

**Question 1 (easy) — True, False, or Cannot say**

Statement: "A problem record may be raised even when no incident has yet occurred."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage's third sentence states it directly: records "may also be raised proactively where analysis indicates a significant risk of future incidents" — risk of *future* incidents, meaning none need have occurred. True. The design principle is worth noticing even though the test only wants the verdict: the procedure encodes both halves of your discipline — reactive (three incidents, or a major review) and proactive (significant risk) — matching your skill definition's word "anticipate". Candidates who skim only the first sentence's "three or more incidents" answer False; the test rewards reading *all* the triggering clauses before judging, exactly as the job does.

**Question 2 (easy) — True, False, or Cannot say**

Statement: "A known error record requires both a confirmed root cause and a documented workaround."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage: "A known error record must be created once a root cause is confirmed and a workaround is documented." The conjunction "and" makes both conditions necessary before the creation duty triggers, which is what the statement claims: True. Parse the structure — two conditions, jointly sufficient to *require* creation. Note what the sentence does not say: it does not forbid documenting workarounds earlier, nor address records for unconfirmed causes; it defines when creation becomes mandatory. Statements that correctly restate a rule's actual conditions are True; the adjacent trap statements (about what happens *before* both conditions hold) would be Cannot say. Reading conjunctions at full weight is the same skill that stops a known error database filling with half-verified entries.

**Question 3 (moderate) — True, False, or Cannot say**

Statement: "A problem record whose fix has been deployed, with no recurrence for two weeks, may be closed."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Closure requires deployment plus "no recurrence for one full reporting period". The statement offers two weeks of quiet — but the passage never defines the reporting period's length. If the period is weekly or fortnightly, closure is permitted; if monthly or quarterly, it is not. The decisive fact — the period's length — is absent, so the honest verdict is Cannot say. The tempting error is importing your own department's convention (monthly, probably) and answering False; but the passage, not your practice, governs. This is the format's most instructive trap for experienced practitioners: the more automatic your operational assumptions, the more deliberately you must check whether the text actually states them. The same discipline protects real records: "no recurrence since deployment" means nothing until the observation window is stated.

**Question 4 (moderate) — Inference**

Which is the best inference about this procedure's design?

- A) It is designed to make problem records easy to open and hard to close — pulling risks into management early, and preventing premature declarations of victory.
- B) It assumes most root causes will never be confirmed.
- C) It exists primarily to generate known error records for the service desk.
- D) It shows that proactive problems matter more than reactive ones.

**Correct answer: A**

**Explanation:** Read the asymmetry the rules build. Opening has three routes (trend threshold, major review recommendation, proactive risk) — many doors in. Closing has one narrow gate: deployed fix *plus* a clean monitoring period — and the confirmed/suspected distinction plus mandatory ownership keep records honest and owned in between. That architecture embodies a bias: better to manage a risk that fades than to close a problem that recurs — which is A. B mistakes a careful evidence standard for pessimism about meeting it. C inverts priorities: known error records serve the process; they are not its purpose. D reads the "may also" proactive clause as a ranking, which the text nowhere makes. Procedure-inference items reward identifying what failure mode each rule prevents — premature closure being the failure this procedure most visibly armours against, for good reason: a problem closed and reopened has usually cost more than one never closed.

**Passage 2 (for Questions 5-7):**

"RCA report extract, P-2214 (intermittent payment submission failures): Analysis of 41 failed submissions shows 39 occurred while the fraud-screening module's response time exceeded 8 seconds. Load testing reproduced the failure pattern: submissions time out when screening exceeds the payment service's 8-second wait limit. We therefore assess the causal mechanism as confirmed for the 39 correlated failures. The remaining 2 failures show no screening delay and remain unexplained; they may share a cause or be unrelated. Screening delays themselves correlate with the module's nightly model refresh overrunning into business hours, but this upstream link is not yet tested. Recommended: raise the wait limit to 15 seconds as an interim mitigation; investigate the model refresh overrun as a suspected upstream cause."

**Question 5 (easy) — True, False, or Cannot say**

Statement: "The report confirms that the nightly model refresh causes the payment submission failures."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The report is explicit about its two levels of certainty: the screening-delay → timeout mechanism is "confirmed" (correlated in 39 of 41 cases *and* reproduced under load testing); the refresh → screening-delay link "is not yet tested" and is recommended for investigation as a "suspected upstream cause". The statement claims confirmation of the upstream link, which the passage directly denies — False, not Cannot say, because the text speaks to exactly this point and says the opposite. This two-tier structure — confirmed mechanism, suspected upstream cause — is textbook RCA writing, and preserving the tiers when you brief others is the verbal discipline your role most depends on: flatten "suspected" into "confirmed" and your organisation may fix the refresh, skip the wait-limit mitigation, and keep failing.

**Question 6 (moderate) — True, False, or Cannot say**

Statement: "If the wait limit is raised to 15 seconds, the 39 correlated failures would not have occurred."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Tempting to answer True — the confirmed mechanism is "screening exceeds 8 seconds → timeout", so a 15-second limit would prevent timeouts for screenings between 8 and 15 seconds. But check what the passage actually establishes: it says the 39 failures occurred while screening "exceeded 8 seconds", without stating *how far* it exceeded — if some screenings ran 20 or 30 seconds, those submissions would time out even at a 15-second limit. The passage calls the raise an "interim mitigation", not a complete prevention, which is consistent with this gap. Since the counterfactual claim depends on the distribution of screening delays — a fact the passage does not give — the verdict is Cannot say. This is a high-value distinction in your daily reading: a mechanism can be confirmed while the *coverage* of a mitigation remains unquantified, and mitigations sized against unquantified distributions are exactly where interim fixes underdeliver. The strongest candidates — and problem managers — notice when a plausible arithmetic inference quietly requires data the text never supplied.

**Question 7 (moderate) — Main point**

Which sentence best captures the report's overall position?

- A) The payment service is poorly built and should be replaced.
- B) A confirmed timeout mechanism explains almost all the failures; an untested upstream cause and two unexplained failures remain open; mitigate now, investigate next.
- C) The fraud-screening module should be removed from the payment path.
- D) All 41 failures have been fully explained.

**Correct answer: B**

**Explanation:** B reproduces the report's actual architecture: what is known (confirmed mechanism, 39/41), what is not (untested refresh link, 2 unexplained failures), and what to do (interim mitigation plus further investigation). D overstates — the report itself reserves 2 failures as unexplained and flags them honestly as "may share a cause or be unrelated". A and C recommend actions the report never proposes; C in particular converts a diagnostic finding (screening delays cause timeouts) into an architectural amputation the evidence does not support — the report's own recommendation is far more conservative. Main-point items reward the option that matches the passage's *shape* — findings, open questions, recommendations, each at the stated certainty level — rather than the option with the boldest conclusion. Summarising RCA reports at exactly their own strength, no more and no less, is what you do every time you brief a service owner; this question is that skill in miniature.

**Passage 3 (for Questions 8-9):**

"Supplier bulletin SB-77: A defect in versions 12.0 to 12.3 of the integration gateway can cause message duplication when automatic failover occurs between gateway nodes. Customers running a single-node configuration are not exposed. Version 12.4 resolves the defect. Customers unable to upgrade immediately can prevent duplication by disabling automatic failover, at the cost of manual intervention being required if a node fails. The defect does not cause message loss; duplicated messages carry identical transaction identifiers, allowing downstream deduplication where supported."

**Question 8 (easy) — True, False, or Cannot say**

Statement: "A customer running version 12.2 in a two-node configuration with automatic failover enabled is exposed to the defect."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Apply each scoping condition. Version 12.2 falls inside the affected range (12.0 to 12.3). Two nodes means not single-node, so the exemption does not apply. Automatic failover enabled means the triggering condition (duplication "when automatic failover occurs") is live. Every condition for exposure is met: True. Bulletin questions are scope-tracing exercises — version range, configuration exemptions, triggering conditions — and the professional stakes of tracing them correctly are immediate: your estate's exposure assessment, which drives whether you raise a proactive problem record and what interim measure you choose, is precisely this reading applied to your configuration data. One misread clause and you either panic a safe estate or leave an exposed one unprotected.

**Question 9 (challenging) — True, False, or Cannot say**

Statement: "For an exposed customer who cannot upgrade, disabling automatic failover eliminates the duplication risk without introducing any new operational risk."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Split the compound statement. First half: disabling automatic failover prevents duplication — supported ("can prevent duplication by disabling automatic failover"). Second half: "without introducing any new operational risk" — directly contradicted: the bulletin states the cost, "manual intervention being required if a node fails", which is a new operational risk (a node failure now needs a human, extending recovery). One half true, one half contradicted: the compound statement as a whole is False. The reading lesson: compound claims fail on their weakest clause, and "without any" is an absolute quantifier that a single stated cost defeats. The professional lesson is the same shape: every mitigation trades one risk for another, and your **Change management** assessment of the workaround must record the traded-in risk (manual failover) as explicitly as the retired one (duplication) — bulletins usually state the trade honestly, and summaries that drop the cost clause are how organisations get surprised by their own workarounds.

**Question 10 (moderate) — Clear-writing judgement for a service owner briefing**

You must brief a non-technical service owner on P-2214 (the payment RCA from Passage 2). Which opening paragraph is best?

- A) "Analysis of 41 failure events indicates an 8-second synchronous wait-limit breach correlating at 95% with fraud-screening latency excursions, with an untested upstream hypothesis concerning ML model refresh scheduling."
- B) "We now know why almost all the payment failures happen: when the fraud check runs slowly, payments give up waiting and fail. We have confirmed this by testing. We recommend an immediate change that will prevent most failures while we investigate why the fraud check slows down — we suspect an overnight process overrunning, but that is not yet confirmed. Two of the 41 failures had a different, still-unknown cause; we are keeping those open."
- C) "The payment problem is basically solved and the fix is coming."
- D) "There are several complicated interacting factors and the situation is evolving; a fuller technical picture will follow in due course."

**Correct answer: B**

**Explanation:** Grade each against what a service owner needs: what is known, how certain, what happens next, what remains open. B delivers all four in plain language *while preserving every certainty level* from the report — "confirmed by testing", "suspect… not yet confirmed", "still-unknown, keeping open". That combination is the craft: translation without distortion. A is accurate but untranslated — jargon density ("latency excursions", "synchronous wait-limit breach") forces the reader to either guess or disengage, and a briefing the audience cannot parse is not communication. C is translated but distorted: "basically solved" flattens the open upstream question and the two orphan failures — precisely the overclaim that returns as "you told us it was fixed". D says nothing with an apologetic tone — the fog option. Note that plain language did not cost precision anywhere in B; it never has to. Writing findings so each audience can act on them, at unaltered certainty, is **User focus** applied to your own prose and the standard GOV.UK plain-language guidance encodes.

**Question 11 (moderate) — Evaluating an argument in a review**

At a service review, an operations lead argues: "Problem management keeps recommending fixes that need change windows, and change windows keep getting used for feature releases instead. So problem management should get its own dedicated monthly change window, guaranteed, ahead of features." Which is the strongest evaluation?

- A) Fully sound: the premise is true, so the remedy follows.
- B) The grievance is legitimate and worth solving — fixes losing window slots to features is a real prioritisation failure with real recurrence costs — but the specific remedy needs scrutiny rather than automatic adoption: a guaranteed window that sits empty some months wastes scarce release capacity, and "always ahead of features" is as crude a rule as "always behind"; the underlying need is a prioritisation mechanism that weighs a fix's recurrence cost against a feature's value case by case, which might be a reserved-capacity rule, a priority scoring gate, or indeed sometimes a dedicated window.
- C) Invalid: operations leads have no standing to propose change policy.
- D) Invalid: fixes never deserve priority over features, because features deliver new value.

**Correct answer: B**

**Explanation:** Separate the argument's layers, as review-quality evaluation must. The factual premise (fixes displaced by features) is granted — and it matters, because every displaced fix converts directly into another month of the incidents you have already costed. The leap is from "the current allocation fails" to one specific rigid remedy: a guaranteed monthly window is a blunt instrument that can waste capacity in quiet months and still lose the *big* contests (a genuinely urgent feature versus a genuinely expensive fault needs weighing, not a standing rule either way). B does what strong evaluation does: validates the grievance, names the remedy's specific failure modes, and redirects to the underlying need with several candidate mechanisms — including conceding the proposed one might sometimes be right. A skips the scrutiny; C attacks standing rather than substance (the move most corrosive to collaborative reviews); D is the mirror-image dogma of the original proposal. In your chair at that review, this is **Community collaboration** — adapting feedback so it is effective and lasting — fused with your prioritisation arithmetic: the winning contribution extracts the true premise, prices it, and builds the mechanism, rather than accepting or rejecting the slogan.

**Question 12 (challenging) — Precision when closing the loop**

You are drafting the closure summary for P-2214, three months on. The facts: wait limit raised to 15 seconds in week 1; correlated failures fell from ~13/month to 1/month; the model refresh overrun was subsequently confirmed by testing as the upstream cause and fixed in week 6; failures have been zero for the last full reporting period; the original 2 unexplained failures never recurred and remain unexplained. Which closure sentence is most accurate?

- A) "All causes were confirmed and fixed, and all failures have been eliminated."
- B) "Root cause (screening delays caused by model refresh overrun) confirmed and permanently fixed; interim mitigation (raised wait limit) remains in place; zero recurrence for one full reporting period, meeting closure criteria. Two early failures from the original 41 were never explained and never recurred; they are noted in the record should the pattern reappear."
- C) "The problem appears resolved, though uncertainty remains and further monitoring is advised indefinitely."
- D) "Closed: fix deployed."

**Correct answer: B**

**Explanation:** A closure summary is the record's final testimony, and B is the only option that testifies exactly. It states the confirmed causal chain (now including the upstream link, which graduated from "suspected" to "confirmed by testing" in week 6 — note how the certainty language has legitimately *changed* since Passage 2, because new testing happened; tracking that evolution is precisely the skill), the status of the mitigation (still in place — a fact future readers need, since the raised limit is now part of the service's configuration), the closure evidence (zero for a full reporting period — matching Passage 1's criterion), and the honest residue: two failures never explained, never recurred, *flagged for pattern-matching* rather than either buried or left as vague doubt. A claims "all causes confirmed" — false for the two orphans — and is exactly the overclaim that makes a record worthless when a similar failure appears next year and the searcher trusts the word "all". C converts a bounded, well-evidenced closure into open-ended hedging, which both understates the achievement and dodges the closure criteria the procedure defines. D is administratively complete and evidentially empty — the anti-record. The craft on display is your discipline's textual signature: every claim at its earned certainty, every loose end named, every future reader served. Records written this way are why organisations trust problem management; this question is that trust, reduced to one sentence choice.

### Preparation tips

- **Drill the three verdicts with compound statements.** True = supported; False = contradicted; Cannot say = silent or insufficient — and a compound statement is False if *any* clause is contradicted, Cannot say if a needed fact is missing. Most hard items are compounds; practise splitting them.
- **Track certainty words like a ledger.** "Confirmed", "suspected", "consistent with", "not yet tested", "may" — when practising, underline them, and check that your answer (or your summary) keeps each claim at its stated level. This is simultaneously test technique and the core hygiene of RCA reading.
- **Trace scope before judging bulletins.** Version ranges, configuration exemptions, triggering conditions: list them, then test the statement's case against each. One pass, in order, beats three anxious re-reads.
- **Practise on your own records.** Take a real RCA report or closure summary and write five statements about it — two true, two false, one undecidable. Marking a colleague's attempt (and having them mark yours) audits both your reading and the document's clarity.
- **Rewrite one briefing weekly.** Take something technical you sent and rewrite it for a non-technical reader, preserving every certainty level. The B-option in Question 10 is a learnable style; a few weeks of practice makes it your default.
- **Keep pace with flags.** Thirty to forty-five seconds per statement; flag the tangled ones and return. Verbal sections reward steady throughput — and the flagged item often looks simple on second approach.

### Common pitfalls to avoid

- **Answering from operational habit.** Your department's reporting period, closure rules or severity tiers are not the passage's. The text governs, even when it differs from good practice — especially then, because that is where the test looks for imported assumptions.
- **Flattening certainty gradients.** "Suspected" reported as "confirmed" — or "confirmed" hedged back into "appears" — both misrepresent the source. Preserve the author's exact strength, in test answers and briefings alike.
- **Missing the weak clause in compound claims.** "Prevents duplication without any new risk" fails on its second half. Read every clause; absolutes ("all", "any", "only") are where compounds break.
- **Inferring quantities the text never gave.** A confirmed mechanism does not quantify a mitigation's coverage; "exceeded 8 seconds" does not say by how much. When your inference needs a distribution, a duration or a definition the passage omits, the answer is Cannot say.
- **Judging arguments by their premises alone.** A true grievance does not validate its proposed remedy. Evaluate premise, leap and remedy separately — the strongest option usually honours the premise while rebuilding the remedy.
- **Preferring polish to fitness in writing items.** The best communication option is the one its named audience can act on with certainty levels intact — not the most technical, the most confident, or the most elegantly vague.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of possible responses. There is usually no provably correct answer; options are scored against the pooled judgement of experienced practitioners and the organisation's professional behaviours. Formats include most-effective, most-and-least-effective, full ranking, and independent rating of each option.

Typical format: 12 to 25 scenarios in 25 to 40 minutes. For a problem manager, scenarios cluster around the role's true difficulty — which is rarely technical. You coordinate investigations performed by teams you do not manage, in organisations that reward firefighting over prevention. You work closely with major incident managers whose clock runs in minutes while yours runs in weeks. You publish findings that implicate decisions, processes and sometimes named teams. You must keep evidence honest under pressure to soften it, keep investigations moving without authority to compel, and keep prevention funded against the permanent competition of the new and urgent. Employers use SJTs for this role because these tensions — thoroughness versus speed, honesty versus comfort, influence without authority — are where problem managers succeed or fail.

The behaviours being assessed align with the values of the Government Digital and Data profession: user focus (preventing harm to the people using services, not just closing records), collaboration (specialists, service desk, major incident managers, suppliers — coordinated, credited, and challenged when needed), ownership (accountability for outcomes you influence but do not control), sound escalation (with evidence, at the right time, to the right level), and inclusion (investigations and reviews where every contributor — junior analyst to veteran engineer — can surface what they know). As you judge each option, ask: what does this do to the users, the evidence, the relationships, and the recurrence rate?

### How this assessment maps to your role

- **Coordination dilemmas** map to **Problem management** and **Community collaboration**: co-ordinating the team to investigate problems, implement solutions and take preventive measures — across boundaries, without line authority, keeping specialists engaged and credited.
- **Evidence integrity dilemmas** map to **Problem management** and **Ownership and initiative**: root cause analysis is only as good as its honesty; scenarios test whether findings survive pressure, and whether your own errors are owned as readily as others'.
- **Interface-with-incident dilemmas** map to **Incident management** and your defined duty to work closely with major incident managers: scenarios test the live handoffs — evidence preservation during restoration, problem input during majors, honest division of the aftermath.
- **Prevention advocacy dilemmas** map to **Problem management**, **Change management** and **Availability and capacity management**: making preventive measures happen in change queues and budget rounds that favour features.
- **Blame and culture dilemmas** map to **Community collaboration** and **User focus**: reviews that fix systems rather than scapegoat people, and team dynamics (including Agile health checks) that keep information flowing to your investigations.
- **Runbook and continuity dilemmas** map to **Continuity management**: managing and testing runbooks, and acting when testing reveals uncomfortable gaps.

### Practice questions

**Question 1 (easy) — The service desk's shortcut**

You discover that service desk staff, under pressure to hit handling-time targets, have started closing repeat incidents without linking them to their problem records — the linking screen "takes too long". Incident-to-problem linkage is the evidence base for your trend analysis and fix justifications. What is the most effective response?

- A) Email the service desk manager citing the linking procedure and requesting compliance.
- B) Talk to the desk team and their manager: explain specifically what the links buy (fix prioritisation for the very faults flooding their queues), acknowledge the time cost, and jointly pursue both compliance and a fix for the real blocker — a faster linking workflow, perhaps a one-click "link to known problem" option.
- C) Have your own analysts re-link incidents retrospectively each week, leaving the desk out of it.
- D) Report the non-compliance to service management leadership so targets are adjusted.

**Correct answer: B**

**Explanation:** Diagnose the non-compliance the way you would diagnose any recurring fault: the desk is not malicious — it is responding rationally to a target (handling time) that punishes a step whose benefits are invisible to them. B treats the root cause, on both sides: the motivational gap (they have never seen what linking buys — so show them: the links are what get their most annoying repeat faults *fixed*) and the mechanical gap (a slow workflow is a legitimate defect in your process; champion the one-click fix). A restates the rule to people who already know it — rules lose to targets unless the friction or the incentive changes. C silently absorbs the cost forever and lets the data decay on every week your analysts fall behind; it also teaches the desk that linking is someone else's job. D escalates before engaging — sometimes eventually necessary, but as a first move it converts potential collaborators into defendants. The scored pattern: fix the system that produces the behaviour, with the people in it — **Community collaboration** doing the work that policy citation cannot.

**Question 2 (easy) — Evidence versus restoration, live**

A recurring fault has just recurred — and this time you are on the bridge as the incident manager prepares to restart the failing service, which will destroy the in-memory state your investigation has waited weeks to capture. Restoration is genuinely urgent: a citizen-facing service is degraded. Capturing state takes an estimated ten minutes. What is the most effective response?

- A) Insist the restart wait for a full diagnostic capture, however long it takes — the investigation matters more than ten minutes of degradation.
- B) Say nothing — restoration always outranks investigation, and it is the incident manager's call.
- C) Tell the incident manager what a ten-minute capture would buy (likely root cause identification, ending these recurrences), ask for the ten minutes, and accept their call if the answer is no — then pursue alternative evidence (logs, monitoring) and agree a pre-authorised capture plan for the next recurrence.
- D) Begin the capture yourself without raising it, since it only takes ten minutes.

**Correct answer: C**

**Explanation:** The scenario tests the incident-problem interface at its live friction point, and C gets every element of the protocol right. The incident manager commands the incident — restoration authority is theirs, and your role definition says work *closely with* major incident managers, not around them. But commanding well requires knowing the price of each option, and only you know what the capture is worth; so your duty is to put the trade on the table fast — cost (ten minutes), benefit (probably ending the recurrences that keep creating these bridges) — and then respect the call. The follow-up clauses are what make C the top answer rather than merely correct: alternative evidence keeps the investigation alive if the answer is no, and the *pre-authorised capture plan* converts today's friction into next time's procedure — turning an ad-hoc loss into a permanent fix for the evidence problem itself. A inverts authority and understates a citizen-facing degradation. B abandons weeks of investigation without even stating the price of the restart — silent deference is not collaboration. D is the worst: an unannounced action on a degraded production service during a live incident, discovered later, would damage exactly the trust the interface runs on. Speak, price it, defer, and systematise.

**Question 3 (easy) — The analyst's premature certainty**

Your problem analyst — capable, keen, and presenting to stakeholders tomorrow — shows you their RCA conclusion: "Root cause confirmed: the memory leak in the session module." You probe: the evidence is a strong correlation (crashes align with memory growth) plus one specialist's agreement, but no test has demonstrated the mechanism, and an alternative explanation (a connection-pool exhaustion with similar symptoms) has not been ruled out. What is the most effective response?

- A) Let the presentation proceed — the analyst is probably right, and confidence builds credibility with stakeholders.
- B) Take over the analysis yourself and present it in their place.
- C) Coach through questions: what would distinguish the leak from pool exhaustion? What test would demonstrate the mechanism? Then have them present tomorrow with the honest status — "leading suspected cause, confirmation test planned" — which is a strong finding in itself.
- D) Cancel the presentation until root cause is properly confirmed.

**Correct answer: C**

**Explanation:** Two things need protecting and both survive in C: the record's integrity and the analyst's growth. The evidential standard here is the one your discipline (and Passage-1-style procedures everywhere) encodes — "confirmed" means demonstrated mechanism, and correlation-plus-agreement is "suspected", however probable. But the correction's *form* matters as much as its content: coaching through questions ("what would distinguish...?") teaches the distinction permanently and hands the analyst the better analysis as their own work, where simply overruling would teach compliance and taking over (B) would teach nothing while spending your time and their confidence. A lets a certainty error reach stakeholders under your quality assurance — and when the alternative explanation surfaces later, both the analyst's and your function's credibility pay. D overcorrects: "suspected cause identified, confirmation test planned" is a perfectly presentable — indeed reassuring — status; cancelling teaches that honesty about uncertainty is shameful, the exact opposite of the culture your evidence depends on. The scored behaviours: **Community collaboration** (feedback that is effective and lasting), evidence discipline, and the developmental patience that turns analysts into your successors.

**Question 4 (moderate) — The fix that keeps slipping**

The permanent fix for P-330 — your costliest recurring problem, ~£8,000/month in user impact — has now been bumped from three consecutive release windows by feature work, each time by a reasonable-sounding individual decision. The next window is in three weeks. What is the most effective response?

- A) Accept the pattern — releases are the delivery teams' domain, and the workaround is holding.
- B) Escalate to the service owner with the accumulated arithmetic: three slips × £8,000/month of ongoing impact, the recurrence risk profile, and a request that the fix be committed to the next window — and propose that fix-versus-feature displacement decisions henceforth weigh the recurring cost explicitly.
- C) Demand the release calendar be changed to always prioritise fixes over features.
- D) Ask your analysts to quietly bundle the fix into an unrelated approved change to bypass the queue.

**Correct answer: B**

**Explanation:** Name the real problem: not any single slip — each was locally reasonable — but a *decision pattern* whose cumulative cost (£24,000 and counting) no one has been shown, because each decision saw only its own month. That is a systemic finding, and B handles it exactly as your discipline handles systemic findings: assemble the evidence (the arithmetic is your business case — this is where the numeric section's payback calculations earn their keep), take it to the accountable owner, and propose the *process* fix (displacement decisions that price recurring cost) so the pattern, not just this instance, ends. The second half matters: without it you will be back in this scenario for P-331. A mistakes a holding workaround for an acceptable end-state — £8,000/month is not "holding", it is bleeding on schedule. C is the crude rule Question 11 of the verbal section dismantled: "always fixes first" is as blind as "always features first", and demanding it spends your credibility on a slogan. D is the integrity failure: smuggling changes past governance corrupts change control (your own **Change management** skill), creates an undocumented delta in the release, and — when discovered — costs problem management its reputation for playing straight, which is the asset every future escalation depends on. Influence without authority runs on evidence and process design; B is both.

**Question 5 (moderate) — The review that wants a name**

At a post-incident review you are chairing, a director interrupts your systemic findings: "This is the third database outage this year. Someone is responsible. Who?" The truthful answer is distributed: one engineer made a defensible configuration choice under ambiguous documentation, a monitoring gap hid the consequence for weeks, and the team's capacity plan was cut two quarters ago. What is the most effective response?

- A) Name the engineer — their change was the proximate trigger, and the director deserves a direct answer.
- B) Say responsibility cannot be assigned and move the agenda on.
- C) Answer the underlying question directly: "Accountability sits with the system we run, and I can show you exactly where it failed" — then walk through the three findings, each with its owner and fix date, and offer the director the tracking role: these three actions, reviewed at this table, are what prevents outage number four.
- D) Privately give the director the engineer's name after the review to keep the meeting constructive.

**Correct answer: C**

**Explanation:** Decode the director's question before answering it: "who is responsible?" is usually "will someone make sure this stops?" — a demand for accountability, which C satisfies *better* than a name would. It reframes without dodging: three concrete failures, three named owners of fixes, three dates, and — the deft move — the director enlisted as the accountability mechanism they were demanding exists. That converts the review's most dangerous moment into its most productive one. A buys the room's comfort with the engineer's reputation and the organisation's future: a defensible choice under ambiguous documentation is a *documentation finding*, and naming its maker teaches every engineer present to hide choices from reviews — starving your future investigations of exactly the honesty they run on. B refuses the question's legitimate core and looks evasive doing it; directors who feel stonewalled repeat the question with more force in worse venues. D is A with a delay and a cover-up: the engineer is condemned without hearing, in a channel with no record — the least accountable form of "accountability" available. The chair's craft being scored: absorb the pressure, translate the demand, and hand back something stronger than what was asked for — **Ownership and initiative** exercised on behalf of the whole system, including its people.

**Question 6 (moderate) — The runbook test that failed quietly**

You run problem management and also own runbook testing for your services. This quarter's continuity test of the case-management failover runbook technically "passed" — the service failed over — but only because the engineer running the test spotted and manually corrected an outdated step mid-execution (a server name from two migrations ago). The test report currently reads "Pass". The service owner reads these reports. What is the most effective action?

- A) Leave "Pass" — the failover worked, which is what the test verifies.
- B) Record the result honestly as "Pass with critical finding": the runbook as written would have failed without expert improvisation; fix the outdated step now, check the rest of the runbook (and sibling runbooks) for the same class of staleness, and raise the systemic question — why did two migrations not trigger runbook updates?
- C) Record "Fail" and schedule a full retest before any further reporting.
- D) Quietly fix the outdated step and leave the report as "Pass", since the defect is now gone.

**Correct answer: B**

**Explanation:** Define what the test actually measures: not "did the service fail over with our best engineer improvising", but "does the *runbook* work" — because runbooks exist for the 03:00 when the expert is on leave and someone else is reading step by step. As written, the runbook would have failed; that is a critical finding wearing a "Pass" costume, and B strips the costume while keeping the truth's both halves (the failover *did* succeed; the artefact is defective). Then B does what your **Problem management** instincts should do to your own **Continuity management** domain: treat the stale step as one incident of a *problem* — two migrations updated servers without updating runbooks, so every sibling runbook is suspect, and the missing update-trigger in the migration process is the root cause. A and D both certify a document that fails without improvisation — D is worse, adding a silent fix that hides even the trace; the service owner's confidence in their continuity posture becomes fiction either way, discovered only during a real disaster. C is honest but disproportionate: the finding is precise (one known-stale step, now identified), so "fail everything, retest from scratch" spends engineering time to re-learn what the test already taught. The scored pattern: report what the evidence means, not what the box allows — and turn your own domain's defect into a systemic investigation as readily as anyone else's.

**Question 7 (moderate) — The specialist team that stopped replying**

The network team owns the key action on P-315 (recurring branch-office connectivity drops, 30 incidents/month). After an enthusiastic start, they have gone quiet: three chasers over five weeks, no substantive reply. You learn informally that their lead was redeployed to a datacentre migration and the team is underwater. What is the most effective response?

- A) Keep chasing weekly and log the non-response in the problem record until they re-engage.
- B) Escalate to the network team's head with the five-week silence documented, requesting intervention.
- C) Talk to the network team's management with the situation reframed: acknowledge the migration pressure, quantify what P-315 costs per month it waits, and negotiate options — a smaller scoped action, a named deputy, your analyst seconded to do the legwork under their guidance, or an agreed restart date after the migration — then record whatever is agreed with a review date.
- D) Reassign the investigation to your own analysts, who can learn networking as they go.

**Correct answer: C**

**Explanation:** The informal intelligence changes the problem: this is not neglect to be escalated but a genuine capacity collision to be *managed* — and coordinating investigations through other teams' realities is your defining skill. C brings everything your role can uniquely bring: the cost-of-delay arithmetic (30 incidents/month priced — evidence that lets network management weigh P-315 against the migration honestly, which raw chasers never let them do), flexibility on *how* (scoped-down action, deputy, seconded legwork under their expertise — that option is often the unlock, since guidance costs a team far less than execution), and formality on *what* (an agreed, recorded, dated commitment replacing an open-ended silence). A is process theatre: documenting non-response weekly builds a grievance file, not a fix, while users absorb thirty incidents a month. B skips the conversation and leads with the charge sheet — escalation is the legitimate *next* step if C's negotiation fails, and it will go better with C's arithmetic in hand and the collaborative attempt on record. D pretends expertise is fungible: analysts learning networking mid-investigation produce slow, low-confidence findings on a live problem — consulting specialists exists precisely because it is cheaper than becoming one. The scored behaviours: networked collaboration, evidence-based negotiation, and ownership that adapts its route without releasing the outcome.

**Question 8 (challenging) — Most and least effective: the pattern across silos**

Your cross-service trend review surfaces something unclaimed: authentication-related incidents are rising slowly across *four* services owned by four different teams — each team's share is small enough that none has flagged it, but the combined curve is unmistakable, and all four services depend on the same identity platform, whose team insists their metrics are green. Consider four actions:

1. Open a problem record for the combined pattern, present the cross-service data to the identity platform team as a question ("what could produce this pattern while your metrics stay green?"), and convene the four service teams to pool their incident details.
2. Send each of the four teams their own slice of the data and let each decide independently whether to investigate.
3. Escalate immediately to leadership that the identity platform is failing and its team is in denial.
4. Add the combined curve to your monthly report and wait a quarter for a stronger signal before acting.

Which pairing is correct?

- A) Most effective: 1; least effective: 4
- B) Most effective: 1; least effective: 3
- C) Most effective: 2; least effective: 3
- D) Most effective: 3; least effective: 2

**Correct answer: B**

**Explanation:** Action 1 is the role performed whole: the pattern only exists in the combined view that only you hold (**Service focus** — the bigger picture across groups of services), so you formalise it (problem record — institutional memory, an owner, a trajectory), take it to the accountable team as an *evidence-bearing question* rather than an accusation ("green metrics plus rising incidents" is genuinely interesting — their dashboards may measure availability while the failures are latency or token-expiry shaped, and framing it as a puzzle recruits their expertise instead of their defences), and convene the silos whose pooled details will make the pattern diagnosable. Ranking the least effective discriminates the card: Action 4 is passive but preserves the option — the curve is at least on record, and a slow rise might justify a quarter's patience if nothing else were possible (much else is). Action 2 dissolves the finding: each team receives a slice too small to act on — *which is the exact mechanism that kept the pattern invisible* — so the action reproduces the problem it should solve, yet it is merely useless, not destructive. Action 3 is destructive: it converts unexplained correlation into an accusation of failure-plus-denial, launched over the platform team's heads before they have even seen the data. It poisons the relationship your investigation needs most, stakes your credibility on a cause you have not established (the platform is the leading hypothesis, not a finding — four services' shared dependency makes it *plausible*; nothing yet makes it *true*), and teaches every team that your trend reviews arrive as indictments. So: most 1, least 3 — option B. The senior pattern: cross-silo signals are found by synthesis, formalised as problems, and investigated as questions — never launched as verdicts.

**Question 9 (challenging) — Your own finding was wrong**

Six weeks ago you presented P-290's root cause to the service owner as confirmed — a supplier defect, backed by the supplier's own acknowledgement — and the supplier's patch was deployed at some expense. The incidents continued, and your analyst has now traced the true cause: a configuration value your own team recommended two years ago, correct then, wrong since a subsequent capacity upgrade. The supplier defect was real but dormant — not the operative cause. What is the most effective response?

- A) Present the configuration fix as "phase two" of the resolution, leaving the original finding undisturbed — the patch had value anyway.
- B) Tell the service owner directly: the confirmed-cause finding was wrong, here is what the evidence actually showed and how we misread it (the supplier's acknowledgement anchored us), here is the true cause — including that it originated in our own historical recommendation — the corrected fix, and the change to our confirmation standard (mechanism demonstration, not supplier say-so) that prevents this class of error.
- C) Fix the configuration quietly; if the incidents stop, the record can be tidied later.
- D) Ask the analyst to double- and triple-check before anything is said, and keep checking until certainty is absolute.

**Correct answer: B**

**Explanation:** Every element of this scenario raises the price of honesty — the finding was *presented as confirmed*, money was spent on it, and the true cause implicates your own team's past advice — which is exactly why the scenario appears in senior SJTs: the keyed answer is the one whose honesty survives maximum pressure. B pays in full and buys everything back: the correction (with the misreading *mechanism* named — anchoring on the supplier's acknowledgement — which converts an embarrassment into a teachable diagnostic error), the uncomfortable provenance of the true cause (disclosed, not excavated later by someone else), the fix, and the process improvement (a stiffened confirmation standard) that transforms the episode from "we were wrong" into "our standard now prevents this". Service owners forgive corrected errors; they do not forgive discovering them independently. A is the seductive option — technically no lie, "phase two" language, the patch retro-justified — but it leaves a false confirmed-cause on the record for future investigators to trust, and its careful wording is designed to prevent the owner understanding what happened: curated truth, functioning as deception. C hopes silence plus success equals absolution; records "tidied later" under pressure of embarrassment are how organisations lose their history. D dresses delay as rigour — the evidence is already sufficient; "absolute certainty" is a standard nothing meets, invoked here to postpone an unpleasant conversation, while the wrong record stands and incidents continue. **Ownership and initiative** — take accountability for issues that occur — is tested most purely on your own issues; the behaviours that score are correction at full speed, disclosure at full depth, and a system improvement that outlives the sting.

**Question 10 (challenging) — The health check that found you**

You run a quarterly health check across the teams feeding problem management. This quarter's anonymous feedback contains a hard theme, from multiple teams: "Problem reviews feel like interrogations — we get grilled on our incidents, then the findings blame our processes. Teams have started sharing less." Your reviews are, in your view, rigorous and non-personal; recurrence rates have improved under them. What is the most effective response?

- A) Note that the feedback conflicts with the results — recurrence is down — and continue with the current review format, which is evidently working.
- B) Soften the reviews: fewer probing questions, findings phrased to avoid mentioning any team's processes.
- C) Treat the feedback as data about a real emerging problem: teams sharing less will starve future investigations regardless of the current format's technical merits. Go to the teams, understand which moments feel like interrogation, and redesign the *experience* without lowering the evidential standard — co-review formats, teams presenting their own timelines, findings framed as system fixes with credit for self-identified issues — then re-measure at the next health check.
- D) Add an anonymous submission route so teams can feed evidence into reviews without attending them.

**Correct answer: C**

**Explanation:** Apply your own discipline to yourself: multiple independent sources reporting the same pattern ("sharing less") is a trend, and the trend threatens the asset your entire function runs on — voluntary information flow. Evidence extracted from defensive teams is late, filtered and incomplete; investigations fed by defensive teams miss the quiet fact that cracks the case (recall the deleted chat message every incident history contains). So the feedback is not a complaint about tone to be weighed against results — it is an early warning about your evidence supply chain, and C investigates it exactly as you would any problem: go to the affected users, locate the mechanism (which moments feel like interrogation?), fix the system (formats where teams narrate their own timelines share the epistemic authority; credit for self-identified issues rewards disclosure — the behaviour you most need), and *re-measure*. The standard stays; the experience changes. A commits the classic delayed-variable error: current recurrence rates reflect past cooperation — the sharing decline poisons *future* investigations, so the metrics contradicting the feedback simply have not caught up with it yet. B protects feelings by dismantling rigour — softened findings produce unfixed systems, and the teams will notice the reviews stopped mattering. D routes around the relationship instead of repairing it, institutionalising the distance the feedback warned about; anonymous evidence also cannot be questioned, which guts its investigative value. The scored insight is the role's most mature: your health checks, reviews and team dynamics are part of the problem management system — **Community collaboration**'s "identify issues through health checks and stimulate the right responses" — and when the system's instrumentation flags *you*, the professional response is the one you would demand of any other team.

**Question 11 (challenging) — The prevention budget showdown**

Annual planning. You have evidence for three preventive investments, but the service owner can fund one this year: (1) £40,000 to fix the estate's top recurring problem — saves a measured £6,000/month (£72,000/year), starting immediately; (2) £25,000 for automated configuration-drift detection — addresses the *class* of cause behind roughly a quarter of last year's problems, savings real but hard to quantify precisely; (3) £60,000 of resilience work on an ageing platform that has not yet failed badly, but whose failure mode, per your analysis, would be a multi-day outage of casework services. The service owner asks for your recommendation and your reasoning. What is the most effective answer?

- A) Recommend option 1 alone — it has the clearest arithmetic, and credibility comes from measurable wins.
- B) Recommend option 3 alone — the catastrophic risk dwarfs the other numbers.
- C) Present all three with their distinct value types — measured return (1), class-level prevention with estimated range (2), tail-risk reduction with impact-scenario costing (3) — recommend option 1 for this year's funding on strength of evidence and immediacy, and propose concrete routes for the other two: option 2 as a candidate for in-year underspend given its smaller ticket, and option 3 costed into next year's planning with a monitoring trigger (defined leading indicators on the ageing platform) that would escalate it immediately if risk signals appear.
- D) Decline to rank them — all three are justified, and choosing is the service owner's job.

**Correct answer: C**

**Explanation:** The question behind the question is whether you can be trusted with investment advice, and C demonstrates the three things that trust requires. First, honest typology: the options are not commensurable on one number — (1) is a measured annuity, (2) is a class-bet with a range, (3) is insurance against a tail — and pretending otherwise (any single-number ranking) would misrepresent at least two of them; showing the owner the *shape* of each value is the analysis they cannot get elsewhere. Second, a real recommendation with reasoning: option 1's evidence is strongest and its payback immediate (£72k/year on £40k — the arithmetic of the numeric section, deployed where it decides real money); recommending it is defensible and decisive, avoiding D's abdication — the owner asked for your recommendation precisely because your evidence discipline is the value you add, and "they are all good" transfers the analysis burden back untouched. Third — the clause that separates C from A — the unfunded options are *routed*, not dropped: option 2 sized for underspend opportunities, option 3 armed with a monitoring trigger so the tail risk gets a tripwire even while unfunded. That trigger matters most of all: B is wrong this year on evidence strength, but B's instinct (catastrophes dwarf annuities) is why option 3 must never silently vanish into "next year" — the leading-indicator trigger is how you hold the tail risk accountable to reality rather than to budget cycles, and it is your **Ownership and initiative** duty ("proactive in searching for potential problems") expressed in planning language. Prevention advocacy that wins year after year looks exactly like C: typed evidence, one clear call, and no risk left unwatched.

**Question 12 (challenging) — Ranking: the morning everything connects**

08:50 Monday. Four items land together: (1) the major incident manager calls — a major is running on the payments service, and she asks whether problem management knows anything relevant: you do — P-341's investigation found the payments database's failover replica has silently stopped syncing, unfixed as of Friday; (2) your analyst's weekend trend alert shows a novel error signature rising fast across two services — small counts, doubling daily for four days; (3) a service owner emails, copying a director, demanding this morning's promised update on P-322 (a chronic, currently quiet problem); (4) the change board convenes at 10:00 and will finalise next month's release content — your two fixes are agenda items 8 and 9, historically the slots that get squeezed out. Rank the order in which you act.

- A) 3, 4, 1, 2 — deadline order as the requests arrived
- B) 1, 2, 4, 3 — the major first (your replica finding may change the incident commander's recovery options right now), the doubling signature next (fast-moving emerging problem — task the analyst immediately), then change-board preparation (a lobbying message to the chair before 10:00 protects both fixes), then the P-322 update (chronic and quiet; a brief honest holding note buys the morning)
- C) 2, 1, 3, 4 — emerging problems are the role's core, then the major, then the human requests
- D) 4, 3, 1, 2 — governance and senior visibility first, operations second

**Correct answer: B**

**Explanation:** Rank by what your action changes and when it must land. Item 1 is decisive and instant: an incident commander is making recovery decisions *now* on a payments major, and your Friday finding — the failover replica is not syncing — could be the difference between a clean recovery and a catastrophe (a failover onto a stale replica during a payments incident is data-loss territory). Sixty seconds on the phone transfers it; nothing else on the list has that urgency-to-effort ratio, and working closely with major incident managers is your role definition executing in real time. Item 2 is the next clock: doubling daily means the signature is eight times Friday's size by Thursday — the emerging-problem window where investigation is cheap is measured in days, so the analyst gets tasked this morning (delegation, not personal deep-dive — you have a morning to run). Item 3 versus item 4 is the instructive pair: the P-322 email has seniority and a copied director; the change board has a 10:00 hard stop and a known failure mode (items 8 and 9 die by squeeze — the Question 4 pattern, catchable *before* the meeting with a two-line case to the chair). The board's deadline is real and its outcome consequential for months; P-322 is explicitly chronic-and-quiet, and a two-sentence honest holding reply ("full update by 14:00 — this morning holds a live major and a fast-moving new signature") serves the service owner *and* models exactly the prioritisation a director should want to see. A and D order by loudness and rank — the perennial trap; C gets items 1 and 2 reversed (the emerging signature has days; the incident commander's decision has minutes) and then lets the board's hard deadline fall behind an email. The scored logic, compressed: minutes-critical knowledge transfer, then days-critical investigation launch, then the hard governance deadline, then the senior communication — each handled at the depth the morning allows, none dropped. That is the role: not doing everything, but making everything happen in the right order — **Problem management**, **Incident management** collaboration, **Change management** advocacy and stakeholder **User focus**, sequenced in one Monday morning.

### Preparation tips

- **Judge options by what they do to information flow.** In almost every problem-management scenario, the best option increases the honesty, speed or completeness of information moving through the organisation — and the worst option (blame, smuggling, softening, silence) restricts it. This single lens resolves a remarkable share of items.
- **Rehearse the correction script.** "The finding was wrong; here is what the evidence showed, how we misread it, the fix, and the standard change." Fluency in that structure — before you need it — is what makes Question 9 behaviour possible under real pressure.
- **Practise pricing delay.** For each of your live problems, know its cost per month of waiting. Scenarios about slipped fixes, quiet specialist teams and budget contests are all won by the person who arrives with that number.
- **Map your escalation ladders.** For each key interface (service desk, specialists, change board, suppliers), know the collaborative step, the evidence-bearing step, and the escalation step — in that order. SJTs consistently reward using them in sequence and penalise skipping to the top.
- **Audit your own reviews for interrogation moments.** Question 10's feedback exists in most organisations, usually unspoken. Asking two teams "what feels worst about our reviews?" is both real improvement and direct SJT preparation.
- **Read stems for the decisive detail.** "Doubling daily", "copied a director", "as of Friday", "items 8 and 9" — problem-manager SJTs hide the ranking key in one quantitative or historical clause. Find it before judging the options.

### Common pitfalls to avoid

- **Escalating before engaging.** Leadership, team heads and directors are the *second* audience; the accountable team, with evidence, is the first. Options that lead with the charge sheet score poorly even when the grievance is real.
- **Protecting findings instead of correcting them.** "Phase two" framings, quiet fixes and tidied records are the discipline's cardinal sins. The keyed answer always surfaces the error, its mechanism, and the standard that prevents recurrence.
- **Accepting the workaround as the end-state.** "It's holding" is how £8,000-a-month problems run for years. Strong options keep the permanent fix moving; weak ones administer the bleeding.
- **Blaming people for system findings.** Defensible choices under bad documentation, targets that punish good practice, runbooks that fail without improvisation — these are process findings. Options that name individuals convert your evidence supply into silence.
- **Doing the specialist's job or the commander's job.** Analysts learning networking mid-case, problem managers capturing state uninvited on live bridges — role-boundary violations read as initiative and score as recklessness. Bring your evidence to the person whose call it is.
- **Letting quiet problems outrank fast ones — or loud ones outrank either.** Chronic-and-stable waits for a holding note; doubling-daily gets an analyst today; minutes-critical knowledge goes by phone now. Rank by trajectory and decision windows, never by who is copied on the email.

<!-- APPEND -->
