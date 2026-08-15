# Lead Infrastructure Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a lead infrastructure engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your leadership work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a lead infrastructure engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — programme plans, supplier contracts and performance data, security-engineered designs, lifecycle standards, test strategies, team workloads, and code and scripts under review — and the kinds of decisions you genuinely make: managing third-party provision of infrastructure services, overseeing programmes and projects, designing solutions with security controls engineered in, establishing standards and procedures across the service product life cycle, leading teams in design and support, and leading others in applying modern development standards.

Why do these assessments matter for your role in particular? At lead level, your primary instruments are no longer your own hands but your judgement, your standards, and your people. You take accountability for issues that occur and proactively search for potential problems. You manage the planning of system and acceptance tests. You provide expertise that turns architectural intent into operational reality across whole programmes. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands: dissecting a supplier's root-cause report for the flaw it is engineered to hide, quantifying whether a programme's resource plan survives contact with its schedule, reading a contract clause the way a dispute would read it, and choosing well when accountability, delivery, and people pull in different directions.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it for this role, a mapping of the assessment dimensions to the specific named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. Questions progress from easy through moderate to hard, and the harder items are deliberately lead-shaped: programme-level trade-offs, supplier management, standards governance, mentoring judgement, and accountability under ambiguity.

Here is how to get the most from it. First, read each "About this assessment" section so the formats hold no surprises. Second, attempt every question honestly — commit before reading the explanation. Third, treat the explanations as the real content: each demonstrates a transferable technique and ties it to a specific lead responsibility, and several are worth discussing with the engineers you mentor. Fourth, use the preparation tips and pitfalls for self-reflection — at your level, most of them are as much about how you lead as how you test.

The habits that score well here — evidence before conclusion, quantification before argument, proportionate escalation, standards applied consistently — are the habits your teams learn by watching you. Practising them is leading by example in miniature. Take your time, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. For a lead infrastructure engineer, the materials are those that cross a leader's desk: programme dependency maps, supplier root-cause analyses, security architecture proposals, lifecycle standards awaiting ratification, test strategies, scripts submitted for review, and the competing claims of teams, suppliers, and programmes about the same set of facts.

The typical format is an online, timed test lasting 15 to 30 minutes, with 20 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group at a comparable level; adaptive difficulty is common, and results usually separate speed from accuracy.

At lead level, the cognitive demand has a distinctive shape: you reason at one remove. The evidence reaching you has been filtered — by dashboards, by suppliers with commercial interests, by engineers reporting upward, by programmes defending schedules — and your value lies in reconstructing the underlying reality from partial, interested accounts. You audit reasoning as much as you produce it: a supplier's incident narrative, a team's capacity claim, a test strategy's coverage argument. And your decisions cascade: an error in a standard you ratify replicates across every project that follows it; a flaw you miss in a security design ships in every deployment. Employers assess cognition at this level because leads are the last technical filter before problems become programmes' problems — and because the role's characteristic failure, plausible reasoning accepted unexamined, is exactly what these tests are built to catch.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Ownership and topic** skill — being proactive in searching for potential problems means detecting the weak signals (recurring near-misses, drifting metrics, converging risks) before they become incidents — and to your **Problem management** duty to initiate and monitor investigations into patterns and trends.
- **Logical deduction** maps to your **Information security** skill: designing solutions with security controls specifically engineered to mitigate threats is threat-to-control reasoning — what attack paths exist, what does each control block, what remains. It also maps to your **Systems integration** duty to establish standards and procedures across the life cycle, since standards are general rules whose consequences you must foresee.
- **Error checking** maps to your **Coding and scripting** skill (interacting with, reading, and writing code, and baseline repair means finding the defect in the diff) and to your **Testing** skill of providing authoritative advice on test planning — auditing coverage claims against reality.
- **Prioritisation** maps to your role-level duty to oversee programmes and projects and your **Systems integration** duty to manage resources so the integration function works effectively: allocation under scarcity is the daily arithmetic of leadership.
- **Applied problem solving** maps to your **Troubleshooting and problem resolution** skill: using lateral thinking to break problems into component parts and diagnose root causes across computing, storage, networking, physical infrastructure, software, COTS, and open source.
- **Auditing others' reasoning** maps to your duty to manage third-party provision: supplier reports, vendor roadmaps, and contractor assurances are arguments to be dissected, not facts to be filed.

### Practice questions

**Question 1 (easy) — Pattern in programme risk data**

You oversee four infrastructure projects. Their monthly risk reports show open high-severity risks: Project A: 4, 4, 3, 3. Project B: 2, 2, 2, 2. Project C: 1, 2, 4, 7. Project D: 6, 5, 3, 2. Which project most needs your intervention?

- A) Project A — consistently elevated
- B) Project B — risks are not reducing
- C) Project C — risk count is accelerating upward
- D) Project D — highest total across the period

**Correct answer: C**

**Explanation:** Read trajectories, not snapshots. Project C's sequence 1, 2, 4, 7 shows increments of +1, +2, +3 — acceleration, the signature of a project losing control of its risk environment: each month generates more new high-severity risks than it retires. Project D, despite the highest historical numbers, shows the healthiest dynamic: 6, 5, 3, 2 is a project working risks down. Project A drifts gently downward; Project B is static at a low level — worth a question about whether those two risks are being actively managed, but not an intervention. Option D's "highest total" reasoning is the classic dashboard error: cumulative history is not current condition. Your role-level duty to oversee programmes and projects depends on exactly this discrimination, because leads have attention for one deep intervention at a time and the derivative — the direction and rate of change — is what tells you where it belongs. In review meetings, always ask for the series, never just the number.

**Question 2 (easy) — Deduction from a security control design**

Your design principle states: "Every administrative pathway to production systems must pass through the privileged access gateway, which enforces multi-factor authentication and session recording. No direct administrative protocol access from user networks is permitted." A review of firewall rules finds a rule permitting SSH from the engineering team's user subnet directly to a production database server, added eight months ago with the comment "temporary - migration support". Which conclusion must be true?

- A) The rule was authorised as an exception at the time.
- B) The rule violates the stated principle as it stands today.
- C) Engineers have been using the rule to bypass the gateway.
- D) The migration is still in progress.

**Correct answer: B**

**Explanation:** Test the rule against the principle's two clauses: administrative pathways must pass through the gateway, and no direct administrative protocol access from user networks. SSH is an administrative protocol; the rule permits it from a user subnet directly to production, bypassing the gateway. Whatever its history, the rule as it stands contradicts the principle: option B, and it is the only conclusion the facts compel. Option A is possible but unestablished — "temporary" comments are not exception records. Option C confuses the existence of a pathway with evidence of its use; the logs would tell you, the rule alone does not. Option D is contradicted by nothing but supported by nothing — eight-month-old "temporary" rules more often outlive their migrations than track them. The lead-level point: your **Information security** skill of engineering controls against threats includes auditing whether the engineered state still holds, and the discipline of concluding exactly what the evidence supports — a violation exists — while listing what needs establishing (authorisation, usage, ongoing need) is what makes your escalation credible rather than alarmist.

**Question 3 (easy) — Error checking a script under review**

An engineer submits this decommissioning script logic for your review: "Step 1: read the list of servers marked 'decommission' in the CMDB. Step 2: for each server in the list, disable monitoring. Step 3: for each server in the list, remove from backup schedules. Step 4: for each server in the list, power off. Step 5: after 30 days, for each server powered off in step 4, delete the virtual machine." The team's decommissioning standard requires that services are confirmed migrated before any destructive action, and that backups are retained for 90 days after power-off. Which two defects should your review flag?

- A) Steps 2 and 3 are in the wrong order; step 5 should wait 60 days.
- B) No step confirms migration before power-off, and step 3 removes backup coverage at the start rather than retaining backups for 90 days after power-off.
- C) Step 1 should not trust the CMDB; step 4 should reboot rather than power off.
- D) The script needs error handling; otherwise it is compliant.

**Correct answer: B**

**Explanation:** Audit the script against each clause of the standard. Clause 1: "services confirmed migrated before any destructive action" — the script moves from list-reading to disabling monitoring to power-off with no confirmation step anywhere; power-off is destructive to service availability, so the gate is missing. Clause 2: "backups retained for 90 days after power-off" — step 3 removes servers from backup schedules before power-off, so the final backups age and expire on the normal retention cycle, and nothing guarantees 90 days of post-power-off retention; the deletion at 30 days (step 5) compounds the exposure by destroying the recovery source well inside the retention window. Option B names both. Option A invents an ordering problem (monitoring before backup removal is harmless) and the wrong number. Option C raises speculative concerns the standard does not state. Option D's error handling is a fair review comment but not a compliance defect — and "otherwise compliant" is false. This is your **Coding and scripting** skill deployed as leadership: reading code against the governing standard, clause by clause, is how automation inherits your standards rather than your team's assumptions — and scripted mistakes replicate at scripted speed.

**Question 4 (easy) — Prioritising as a lead**

Four items compete for your afternoon: (1) a supplier's major incident report for last week's network outage has arrived, and your assessment is due to the service owner in three days; (2) an engineer you mentor asks for an hour to talk through a design they must present tomorrow; (3) a programme board meets in two hours and its paper misstates your team's position on a migration dependency — the error favours an unrealistic schedule; (4) your monthly team workload report is due at the end of the week. Which sequence is most defensible?

- A) 1, 3, 2, 4 — the incident report is the most substantive work
- B) 3, 2, 1, 4 — correct the board paper before the meeting, then the time-boxed mentoring, then the report work
- C) 2, 3, 1, 4 — people always come first
- D) 3, 1, 2, 4 — board first, then the report; mentoring can wait until tomorrow

**Correct answer: B**

**Explanation:** Two items have hard near-term deadlines; sequence within them by decay rate. Item 3 expires in two hours: once the board endorses a schedule built on a misstated dependency, unwinding it costs a governance cycle and your team inherits an impossible commitment — a short, precise correction to the paper's owner (or at the meeting) is high leverage available only now. Item 2 expires tomorrow morning: the engineer's presentation is fixed, so the mentoring hour is valuable only today — and developing people through their real deliverables is core lead work, not an interruption to it. Item 1 has three days and deserves the deep reading a supplier incident report requires (see this section's later questions); starting it today is good, doing it first is not. Item 4 has the week. Option B sequences by expiry and leverage. Option A treats substance as urgency. Option C applies a slogan where a calendar would do — people do come first, which is why the engineer gets today's protected hour rather than a squeezed slot after the board. Option D quietly drops the mentoring, which is how leads teach their teams that development commitments are the flexible ones. Overseeing programmes and managing resources is mostly this: ordering by when value evaporates.

**Question 5 (moderate) — Auditing a supplier's root-cause narrative**

A supplier's incident report concludes: "Root cause: an unprecedented traffic surge overwhelmed the firewall cluster. The surge exceeded design parameters, and no reasonable capacity planning could have anticipated it. Recommendation: the customer should fund a capacity upgrade." Your own monitoring shows: traffic at the incident peak was 40% above normal but 10% below the level handled without issue during last year's peak season; the firewall cluster was running a firmware version two releases behind the supplier's own currency standard; and one of the cluster's two nodes had been out of service for maintenance, halving capacity, under the supplier's control. Which assessment is soundest?

- A) Accept the report — the supplier is the expert on its own equipment.
- B) The narrative fails against your evidence: the "surge" was within historically handled levels; the halved capacity (supplier-controlled maintenance) and outdated firmware are omitted contributing causes under the supplier's responsibility; the report shifts remediation cost toward the customer. Challenge it with the evidence and require a revised analysis.
- C) Reject the report and terminate the supplier relationship.
- D) Accept the recommendation but fund the upgrade jointly.

**Correct answer: B**

**Explanation:** Test the narrative's load-bearing claims against independent evidence. "Unprecedented surge": your data shows the peak was below last year's handled levels — the adjective collapses, and with it "no reasonable planning could have anticipated". What the report omits is more instructive: a cluster at half capacity due to supplier-scheduled maintenance handles any surge with half its designed headroom, and outdated firmware is a currency failure against the supplier's own standard. The report's structure — external inexplicable cause, customer-funded remedy — is the standard shape of cost-shifting root-cause analysis, and detecting it is precisely why your role-level duty to manage third-party provision requires independent monitoring: without your own data, option A is all you can do. Option B responds proportionately: evidence-based challenge and a required revision, which preserves the relationship while refusing the narrative — most suppliers produce honest second drafts when the first is shown to be checkable. Option C escalates a correctable report into a procurement crisis. Option D splits a cost the evidence assigns: joint funding may end the negotiation, but conceding it before the corrected analysis surrenders the facts that determine fair shares. Lead-level pattern: never assess a supplier report without laying your own telemetry beside it.

**Question 6 (moderate) — Deduction through standards interaction**

You are ratifying two standards. Standard A (yours, draft): "All infrastructure automation code must pass peer review and automated testing in the pipeline before deployment to production." Standard B (existing, security team): "Emergency security patches must be deployed within 24 hours of release for critical vulnerabilities." An engineer objects: "During an emergency patch, there may be no time for peer review — the standards conflict." Which resolution is most sound?

- A) The standards do not interact; dismiss the objection.
- B) Standard B overrides Standard A in emergencies; note nothing.
- C) The objection identifies a genuine interaction: add an emergency pathway to Standard A — expedited review by any available senior engineer, or post-deployment review within a defined period when none is available — so both standards can be satisfied, and the exception is designed rather than improvised.
- D) Withdraw Standard A — it cannot handle emergencies.

**Correct answer: C**

**Explanation:** Model the interacting case concretely: a critical patch released at 02:00 requires automation changes deployed within 24 hours; if no reviewer is available inside that window, an engineer must choose which standard to breach — a real conflict, so option A fails on the facts. Option B resolves it by silent precedence: workable tonight, corrosive over time, because unwritten override rules are applied inconsistently, invoked opportunistically ("it was sort of an emergency"), and invisible to audit. Option D abandons the general good for the exceptional case. Option C is how mature standards are engineered — your **Systems integration** duty to establish standards and procedures across the life cycle, and ensure practitioners adhere to them, depends on standards that survive their edge cases: a designed emergency pathway (expedited review, or time-bound retrospective review) keeps the control's intent intact under pressure and makes compliance possible, which is the precondition of enforcement. The deeper lead lesson is in the sequence: the objection was a gift — practitioners stress-testing a draft find the cases the author's desk cannot — and the response that incorporates the objection, credits it, and strengthens the standard also teaches the team that raising problems with your documents is welcome. Standards ratified over objections get complied with resentfully and abandoned quietly.

**Question 7 (moderate) — Error checking a test strategy's coverage claim**

A programme's test strategy, submitted for your authoritative review, claims: "Full non-functional coverage is achieved: performance testing will run at 120% of forecast peak load; failover testing will exercise the loss of each component individually; backup restoration will be tested monthly." The system it covers is a two-site design where the stated recovery requirement is continuity through the loss of an entire site, and forecast load grows 40% within the strategy's two-year lifetime. Which gap is most significant?

- A) Performance testing should run at 150% of peak, not 120%.
- B) Component-level failover testing does not exercise whole-site loss — the stated recovery requirement is never tested — and 120% of today's peak is below year-two forecast load.
- C) Monthly backup restoration testing is too frequent.
- D) The strategy fails to name the testing tools.

**Correct answer: B**

**Explanation:** Audit the coverage claim against the stated requirements, not against generic good practice. The recovery requirement is site-loss continuity; the strategy tests component-loss failover — a materially weaker condition, since site loss removes many components simultaneously plus their shared dependencies (power, network egress, the failover coordination itself), and systems that survive every individual component failure routinely fail whole-site tests. The headline requirement is simply never exercised: that is the principal gap. Secondarily, arithmetic: 120% of today's peak is overtaken by forecast growth of 40% within the strategy's own lifetime — by year two, "120%" tests below expected peak (1.2 < 1.4), so the margin is an illusion with a sell-by date. Option B captures both. Option A proposes a bigger number without the requirement-anchored reasoning — 150% is as arbitrary as 120%; the right target derives from forecast load plus margin. Option C objects to prudence. Option D is administrative. This is your **Testing** skill at its lead altitude — providing authoritative advice and guidance on test planning means testing the claim "full coverage" against the requirements the way an incident eventually would, and "the strategy never tests the thing the design promises" is the finding that justifies the word authoritative.

**Question 8 (moderate) — Lateral decomposition of a cross-capability problem**

Users report that large file transfers to a partner organisation fail at almost exactly 10 minutes, regardless of file size or time of day. Small files always succeed. Your teams have checked their own components in isolation: the network team reports the link healthy, the server team reports the transfer service healthy, the security team reports the proxy healthy. The failures continue. As lead, which investigative direction is most promising?

- A) Recheck each component more thoroughly, one team at a time.
- B) The consistent 10-minute cutoff regardless of size or load suggests a timeout somewhere in the end-to-end path — likely a session or idle timeout in a mid-path device (firewall, proxy, load balancer) or at the partner's side; investigate the path as a whole, correlating timestamps, and test with a transfer engineered to exceed 10 minutes at low bandwidth.
- C) Blame the partner organisation's infrastructure, since your components are all healthy.
- D) Advise users to split large files into chunks that transfer in under 10 minutes.

**Correct answer: B**

**Explanation:** The signature is the clue: failures locked to elapsed time, invariant to size, load, and time of day, are the fingerprint of a configured timeout, not of capacity, congestion, or intermittent faults — which is why each component, examined in isolation for health, reports healthy: a timeout is healthy behaviour, configured somewhere, interacting with long-lived sessions. Option B reasons laterally — your **Troubleshooting and problem resolution** skill's exact phrasing — from the pattern to the mechanism class, then designs the discriminating test: a deliberately slow transfer exceeding 10 minutes distinguishes elapsed-time cutoffs from data-volume effects cleanly. The structural insight for leads: option A repeats the method that has already failed three times — component-isolation checking cannot find an interaction property, however thoroughly each team rechecks; when every part is healthy and the whole still fails, the fault lives in the composition, and only someone with cross-team authority can direct a whole-path investigation. That someone is you. Option C exports the hypothesis space's remainder to the party you cannot inspect — possibly right, but asserted without evidence and guaranteed to start the partner conversation badly; the path correlation in B produces the evidence either way. Option D institutionalises the fault as user procedure — a workaround masquerading as a resolution, taxing every future transfer with the problem you were asked to remove.

**Question 9 (moderate) — Resource allocation across the integration function**

Your integration function has 5 engineers and three concurrent demands: Programme X needs 3 engineers for 4 weeks (hard regulatory deadline in 5 weeks); Programme Y needs 2 engineers for 6 weeks (deadline in 8 weeks); business-as-usual (BAU) integration support needs 1 engineer continuously, and historically generates an unplanned surge roughly one week in four requiring a second engineer. Which allocation plan is most robust?

- A) X: 3, Y: 2, BAU: 0 — programmes first; BAU can wait five weeks.
- B) X: 3, BAU: 1, Y: 1 — staff the regulatory deadline and BAU fully now; Y starts with 1 engineer and receives 2 more when X completes in week 4, still finishing within its week-8 deadline; BAU surges draw temporarily from Y's single engineer, with the deficit recovered after X releases staff.
- C) X: 2, Y: 2, BAU: 1 — spread evenly and hope X's deadline flexes.
- D) X: 3, Y: 2, BAU: 1 — commit 6 engineers and recruit a contractor immediately to cover the sixth seat.

**Correct answer: B**

**Explanation:** Check each plan against the constraints and the surge reality. Total capacity is 5; demands sum to 6 at peak, so something must be sequenced — option D resolves the arithmetic with an instant contractor, but procurement, clearance, and onboarding make "immediately" fictional inside a 4-week window, and the plan carries no fallback while the fiction resolves. Option A zeroes BAU: integration support demand does not pause because it is unstaffed — it becomes incidents, escalations, and interruptions that will raid X's staffing anyway, unplanned. Option C understaffs the one immovable deadline on a hope. Option B does the sequencing arithmetic: X fully staffed completes in week 4, inside the week-5 regulatory line with a week's margin; Y runs weeks 1–4 at reduced pace on 1 engineer, then takes 3 from week 5 — its remaining work compresses into weeks 5–8, meeting the week-8 deadline; BAU keeps its continuous engineer, and the one-week-in-four surge borrows from Y, whose early-phase pace is the plan's designed flex. This is your **Systems integration** duty — managing resources so the function works effectively — in its real form: not dividing headcount, but sequencing commitments so every hard constraint is met, the flexible commitment absorbs the variance, and the plan states where its slack lives. Present allocation plans with exactly that structure and programmes stop negotiating against arithmetic.

**Question 10 (hard) — Deduction across a threat model**

You are reviewing the security engineering of a design that exposes an API to partner organisations. Controls in the design: (i) mutual TLS authenticates partner systems; (ii) an API gateway enforces per-partner rate limits; (iii) all requests are logged with partner identity; (iv) payloads are validated against a strict schema. The threat register lists four threats: (T1) an unauthorised third party calling the API; (T2) a compromised partner system flooding the API; (T3) a compromised partner system submitting malformed payloads to exploit the parser; (T4) a compromised partner system exfiltrating another partner's data through the API. Which threat is not addressed by the stated controls?

- A) T1
- B) T2
- C) T3
- D) T4

**Correct answer: D**

**Explanation:** Map each threat to the control engineered against it. T1 (unauthorised caller): mutual TLS blocks unauthenticated systems — addressed by (i). T2 (flooding from a compromised partner): per-partner rate limits cap the damage — addressed by (ii), with (iii) supporting detection. T3 (malformed payloads): strict schema validation rejects them before the parser's vulnerable depths — addressed by (iv). T4 (cross-partner data access): authentication proves who is calling, rate limiting bounds how often, logging records that it happened, and schema validation checks the request's shape — but nothing in the stated controls checks whether an authenticated partner is authorised to access the specific data requested. Authentication without per-partner authorisation on data access leaves T4 open: a compromised Partner A system, validly authenticated, well-formed, and under its rate limit, requests Partner B's records — and every stated control waves it through, while the logs politely record the exfiltration. The missing control is tenant-scoped authorisation (and ideally data partitioning) at the resource level. This is the systematic method your **Information security** skill names — controls "specifically engineered to mitigate security threats" implies a threat-by-threat audit, and the review question is never "are there controls?" but "which threat does each control kill, and which threat does no control touch?" The authenticated-but-unauthorised gap is among the most common in real partner API designs, precisely because four strong controls make the design feel finished.

**Question 11 (hard) — Reconciling contradictory accounts**

A programme escalates: "The infrastructure team's environment delays have cost us three sprints." Your team's account: "The programme changed its environment requirements four times; each rebuild was delivered within our five-day standard." You pull the records: the programme submitted requirement changes on four dates; your team delivered each rebuild in 4–5 working days; but the records also show the first requirements document sat in your team's intake queue for nine days before work began, and two of the programme's four changes were corrections of misunderstandings from a kickoff meeting your team's representative missed. Which conclusion do the records best support?

- A) The programme's account is correct and your team's is wrong.
- B) Your team's account is correct and the programme's is wrong.
- C) Both accounts are selectively true: your team met its per-rebuild standard but contributed the nine-day intake delay and, by missing kickoff, contributed to two avoidable requirement changes; the programme drove four changes but two trace partly to your side. The delay is co-produced; fix intake latency, kickoff attendance, and requirements confirmation jointly.
- D) The records are inconclusive; commission an independent review.

**Correct answer: C**

**Explanation:** Audit each account against the record. Your team's claim — every rebuild within five days — is true and incomplete: it measures from work-start, silently excluding the nine days of intake queue, which the programme experienced as delay identically to slow delivery. The programme's claim — four requirement changes caused the rebuilds — is true and incomplete: two of the four changes corrected misunderstandings that a kickoff attendee from your team would likely have caught at source. Each account is accurate within its chosen frame and misleading in total — the standard structure of escalated disputes, because each side compiles its evidence from the subset it controls. Option C is what the merged record supports, and note its practical geometry: the remedies (intake latency target, mandatory kickoff coverage, requirements confirmation step) are process fixes, not blame allocations, which is what lets both sides adopt them. Options A and B each accept one frame whole — and a lead who reflexively backs their own team's framing (option B's real temptation) teaches the team that internal accounts need not survive external audit. Option D outsources a reconciliation the records have already performed; independent review is for evidence you cannot obtain, not conclusions you would rather not draw. Taking accountability for issues that occur — your **Ownership and topic** skill — begins with owning your side's contribution before negotiating anyone else's, which is also, not coincidentally, the move that makes the joint fix negotiable.

**Question 12 (hard) — Baseline repair decision under uncertainty**

An overnight automated deployment has left a configuration baseline in a mixed state: 60 of 200 servers received a new configuration version, 140 did not, and the deployment tool's state database was corrupted mid-run — so its records of which 60 are unreliable. The new configuration is functionally compatible with the old (services run correctly on both), but the mixed estate breaks compliance reporting and the next deployment cannot run until the baseline is coherent. You can: query every server directly for its actual version (a script your team can write in about 2 hours, then an hour to run); restore the state database from its pre-run backup (10 minutes, but it will claim all 200 are on the old version — wrong for the 60); or re-push the new configuration to all 200 servers (4 hours, makes reality uniform, but re-applies configuration to 140 servers outside any approved change window). Which recovery is soundest?

- A) Restore the state database from backup — fastest, and the tool will self-correct over time.
- B) Re-push to all 200 immediately — uniform reality is worth the unapproved deployment.
- C) Query the estate for ground truth first (≈3 hours), rebuild the state database from actual server responses, then schedule the completion push for the remaining 140 through the normal change process — services are running correctly meanwhile, so the urgency is coherence, not availability.
- D) Do nothing until the vendor of the deployment tool investigates the corruption.

**Correct answer: C**

**Explanation:** Establish what is actually at stake: services run correctly on both versions, so there is no availability emergency — the damage is epistemic (you no longer know the estate's state) and procedural (compliance reporting and future deployments are blocked). That diagnosis orders the options. Option C rebuilds knowledge from ground truth — the servers themselves are the authoritative record of what they run, and three hours of scripted query converts unreliable tool-state into verified fact; the state database is then rebuilt from reality rather than from a backup's convenient fiction, and the completing push for the 140 goes through the change process it belongs in, because nothing burning justifies bypassing it. This is **Coding and scripting** as your role defines it — baseline repair activities — done in the correct epistemic order: observe, then record, then act. Option A repairs the database by installing a known falsehood: the tool now confidently misreports 60 servers, and "self-correct over time" means future deployments computing diffs from wrong premises — automation acting on false state is how mixed estates become broken ones. Option B fixes reality by unauthorised mass change: it trades a compliance-reporting gap for an actual compliance breach on 140 servers, plus four hours of deployment risk, to save scheduling a change. Option D abandons a recoverable estate to a vendor timeline; the corruption's cause deserves that investigation in parallel, not as a precondition. The lead pattern: when state and reality diverge, reality is the baseline — repair your records from it, never it from your records.

### Preparation tips

- **Practise auditing filtered accounts.** Take a real supplier report or programme escalation and test each load-bearing claim against your own telemetry and records. The gap between narrative and evidence is where lead-level cognitive questions live.
- **Read code against standards, not just for correctness.** Review your team's next automation submission clause-by-clause against the governing standard. Script defects that violate standards are the test's favourite error-checking material.
- **Trend everything.** Convert any static number you meet this week — risks, incidents, utilisation — into its series and its derivative. Trajectory questions reward the habit instantly.
- **Map threats to controls explicitly.** For any design you review, build the two-column table: each threat, the control that kills it. The empty cell is both the exam answer and the real finding.
- **Sequence, don't split, in allocation problems.** Check hard deadlines first, place the immovable demands, and let the flexible commitment absorb variance — then verify the arithmetic of every phase.
- **When components pass and systems fail, investigate composition.** Timeouts, interactions, and shared dependencies live between the boxes on the diagram. Practise naming the mechanism class from the failure signature.
- **Time-box at 60–90 seconds per question.** Lead candidates over-deliberate. Practise committing on sufficient evidence — the same calibration your real decisions need.

### Common pitfalls to avoid

- **Accepting narratives because they are expert.** Suppliers, programmes, and your own team all present selectively. Check load-bearing claims against independent evidence before adopting any account.
- **Reading snapshots instead of trajectories.** Highest current number is not greatest need. The derivative directs intervention.
- **Concluding beyond the record.** A violating rule proves violation — not usage, intent, or authorisation history. Match your conclusion's strength to the evidence's.
- **Reviewing against good practice instead of stated requirements.** The significant gap is the requirement never tested, the threat never controlled — findable only by auditing claims against the specific stated obligations.
- **Resolving standard conflicts by silent precedence.** Designed exception pathways survive audit and pressure; unwritten overrides survive neither.
- **Repairing records instead of knowledge.** When tool-state and reality diverge, query reality. Restoring a plausible fiction is faster and strictly worse.
- **Backing your team's frame reflexively.** In contradictory accounts, audit your own side's contribution first. The reconciliation that admits it is the one that gets adopted.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the quantities your role genuinely handles — and at lead level, most of those quantities carry money, people, or contractual force. Alongside the engineering staples (capacity, availability, throughput), your numbers now include supplier service credits and performance penalties, programme resource plans, cost models across options and years, test coverage and defect statistics at programme scale, and the workload arithmetic of the teams you lead. The underlying mathematics remains accessible — percentages, ratios, weighted averages, rates, compound growth, and reading tables and charts — but the questions demand interpretation, multi-step assembly, and the judgement to notice when a correct number supports an incorrect conclusion.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions, each presenting realistic data — a supplier performance table, a cost comparison, a programme burn-down, a capacity model — followed by a multiple-choice question. Calculators are usually permitted; rough paper is essential; scoring is norm-referenced and often adaptive.

Why do employers assess numeric reasoning for lead infrastructure engineers? Because at this level, your arithmetic is contractual and budgetary. When you manage third-party provision, service credit calculations and performance measurements are the enforcement mechanism of the contract — and suppliers employ people who compute them carefully in the other direction. When you oversee programmes, resource and schedule arithmetic determines whether commitments made in your name are physically possible. When you input to budgets, your cost models compete with others' for finite public money, and the model that survives scrutiny wins. A lead who cannot rapidly verify a weighted figure, a pro-rated credit, or a compound growth projection is negotiating unarmed. The assessment rehearses, in miniature, the daily numeracy of accountable technical leadership.

### How this assessment maps to your role

- **Contractual and performance arithmetic** maps to your role-level duty to manage third-party provision of infrastructure services: measuring supplier performance against contracted definitions, verifying service credits, and challenging computed claims are core enforcement numeracy.
- **Programme and resource arithmetic** maps to your duty to oversee programmes and projects and your **Systems integration** duty to manage resources so the function works effectively: schedules, allocations, and burn rates are rate-and-ratio problems with deadlines attached.
- **Cost and investment comparison** maps to your management-path duty to lead teams in the design and implementation of solutions: option papers, total-cost models, and consolidation cases are decided on arithmetic you must be able to build and audit.
- **Test and quality metrics at scale** map to your **Testing** skill: managing the planning of system and acceptance tests and identifying process improvements requires fluency with pass rates, defect discovery curves, and coverage figures — including their bases.
- **Risk and reliability quantification** maps to your **Information security** and **Ownership and topic** skills: proactive problem-searching is largely trend arithmetic, and security investment cases are probability-times-impact estimates presented honestly.
- **Team workload figures** map to your duty to lead and direct infrastructure specialist teams: sustainable rotas, utilisation, and capacity claims are the numbers behind your people decisions.

### Practice questions

**Question 1 (easy) — Service credit calculation**

A supplier contract specifies: availability below 99.5% in a month earns a service credit of 5% of the monthly charge; below 99.0%, the credit is 10%. The monthly charge is £48,000. The supplier delivered 99.2% availability this month. What credit is due?

- A) £4,800
- B) £2,400
- C) £0
- D) £7,200

**Correct answer: B**

**Explanation:** Locate 99.2% in the credit bands: it is below 99.5% (triggering the 5% band) but not below 99.0% (so the 10% band does not apply). Credit = 5% of £48,000 = 0.05 × 48,000 = £2,400 — option B. Option A applies the 10% band; option D applies 15% (adding the bands — credits in tiered structures replace, not stack, unless the contract says otherwise, and this one does not). The mechanical part is easy; the lead-level habit is band-edge care: contracts written "below 99.5%" exclude exactly 99.5%, and suppliers report to the decimal that matters — a reported "99.5%" deserves a look at the underlying minutes, because 43,178 up-minutes out of 43,200 is 99.949%, but 43,155 is 99.896%, and rounding conventions decide real money. When you manage third-party provision, always recompute credits from raw downtime minutes and the contract's own rounding rules, not from the supplier's pre-banded summary.

**Question 2 (easy) — Programme resource burn**

A 12-week infrastructure project was planned at 3 engineers full-time throughout (36 engineer-weeks total). At the end of week 8, the project has consumed 30 engineer-weeks and completed 60% of its planned work. If the remaining work is completed at the same productivity rate the project has achieved so far, how many more engineer-weeks are needed?

- A) 6
- B) 12
- C) 20
- D) 18

**Correct answer: C**

**Explanation:** Compute achieved productivity first: 60% of the work consumed 30 engineer-weeks, so each 1% of work costs 30 ÷ 60 = 0.5 engineer-weeks. Remaining work is 40%, so at the same rate: 40 × 0.5 = 20 engineer-weeks — option C. Option A is the planned remainder (36 − 30), which assumes the plan's productivity despite eight weeks of evidence against it; option B assumes the remaining 40% costs what a plan-rate 40% would (0.4 × 36 = 14.4, near neither — while 12 comes from 40% × 30 engineer-weeks, a base error). The comparison that matters for your oversight duty: the plan allowed 36 engineer-weeks total; the evidence-based forecast is 30 + 20 = 50 — a 39% overrun, and with 4 calendar weeks left, 20 engineer-weeks needs 5 engineers, not 3. This is earned-value reasoning in its simplest clothes, and its lead-level moral: after real evidence exists, forecasts extrapolate achieved rates, not planned ones — and the moment the forecast diverges from the plan is the moment to surface it, not the moment the plan runs out.

**Question 3 (easy) — Weighted supplier scorecard**

Your supplier scorecard weights: availability 50%, incident response 30%, project delivery 20%. This quarter's scores (out of 100): availability 92, incident response 70, project delivery 85. The contract requires a weighted score of at least 82 to avoid a performance review meeting. What is the weighted score, and is a review triggered?

- A) 82.3 — no review
- B) 84.0 — no review
- C) 79.5 — review triggered
- D) 82.0 — no review (exactly at threshold)

**Correct answer: B**

**Explanation:** Multiply each score by its weight and sum. Availability: 92 × 0.50 = 46.0. Incident response: 70 × 0.30 = 21.0. Project delivery: 85 × 0.20 = 17.0. Weighted score: 46.0 + 21.0 + 17.0 = 84.0 ≥ 82 — no review, option B. Option A (82.3) is the unweighted mean, (92 + 70 + 85) ÷ 3 — close enough to the threshold to feel plausible; option C (79.5) comes from misassigning the weights (50% on incident response); and the clustering of the options around the 82 threshold is deliberate: weighted-average questions in contractual contexts are engineered so the weighting decision changes the outcome, exactly as real scorecards are. Two lead habits follow. First, verify the weights sum to 1.0 before computing — misprinted scorecards exist. Second, notice what the weighting conceals: a 70 in incident response is a poor quarter's performance sheltering under strong availability; the contract may not trigger a review, but your supplier management conversation should — scorecards are floors for contractual consequence, not ceilings for management attention.

**Question 4 (easy) — Capacity of a consolidation target**

You are consolidating three legacy clusters onto one platform. Their current peak utilisations are: Cluster A, 240 vCPU; Cluster B, 310 vCPU; Cluster C, 180 vCPU. Historical data shows their peaks never coincide: the highest combined simultaneous peak observed is 640 vCPU. Policy requires 25% headroom above observed peak. What minimum vCPU capacity must the target platform provide?

- A) 730
- B) 800
- C) 912
- D) 640

**Correct answer: B**

**Explanation:** Use the combined simultaneous peak, not the sum of individual peaks. The individual peaks total 240 + 310 + 180 = 730, but they never coincide; the observed simultaneous peak is 640. Apply the policy headroom: 640 × 1.25 = 800 vCPU — option B. Option A is the non-coincident sum (730) with no headroom — double-counting peaks that never overlap while omitting the required margin; option C applies headroom to that inflated sum (730 × 1.25 = 912.5), compounding the error into a 14% over-purchase; option D forgets the headroom entirely. The statistical point is the one that saves real money in consolidation cases: aggregate demand is not the sum of individual maxima unless the maxima coincide, and measuring observed simultaneous peak is precisely why consolidation pays. The lead-level caveat to carry into the business case: "never coincided historically" is evidence, not law — workload growth or rescheduled batch jobs can synchronise peaks, so the 25% policy headroom is doing real work, and the case should say what monitoring will watch for peak convergence.

**Question 5 (moderate) — Compound growth against a fixed budget**

Your storage costs are £200,000 this year and growing at 15% per year compound. The budget line is fixed at £260,000 per year for the next three years. In which year does cost first exceed budget, and by roughly how much? (Year 1 is next year.)

- A) Year 2, by about £4,500
- B) Year 3, by about £44,000
- C) Year 2, by about £14,500
- D) Year 3, by about £30,000

**Correct answer: A**

**Explanation:** Compound forward year by year. Year 1: 200,000 × 1.15 = £230,000 — under the £260,000 budget. Year 2: 230,000 × 1.15 = £264,500 — over budget by £4,500. The first breach is therefore Year 2, by about £4,500 — option A. (Year 3 continues to £304,175, an excess of about £44,000 — option B's figure, correct arithmetic attached to the wrong question: the item asks for the first breach.) Options C and D come from simple, non-compound growth: a flat £30,000 per year gives Year 2 = £260,000 (exactly at budget, no breach) and Year 3 = £290,000 (£30,000 over) — and that comparison is the lesson. The compounding difference in Year 2 — £264,500 versus £260,000 — is precisely what decides which side of the budget line you land on: at growth rates and horizons typical of infrastructure costs, simple-growth shortcuts land on the wrong side of thresholds. Model compound growth as compound, answer exactly the question asked (first breach, not largest), and when your roadmap input says "the line breaks in Year 2", include the year-by-year table so the budget holder can verify the arithmetic in ten seconds.

**Question 6 (moderate) — Defect discovery and release readiness**

Your programme's system testing has run for 6 weeks. New defects found per week: 28, 24, 19, 13, 8, 5. Critical-severity defects among them per week: 4, 3, 2, 1, 0, 0. Exit criteria for release: weekly new-defect discovery below 10, no new critical defects for 2 consecutive weeks, and all previously found critical defects fixed and retested (2 remain open). Which statement is correct?

- A) All exit criteria are met — release can proceed.
- B) The discovery trend (below 10 for two weeks) and critical-discovery criteria (none for two weeks) are met, but 2 open critical defects block release until fixed and retested.
- C) No exit criteria are met — testing must restart.
- D) The trend criteria fail because week 4 found 13 defects.

**Correct answer: B**

**Explanation:** Test each criterion against the data. Criterion 1 — weekly discovery below 10: weeks 5 and 6 found 8 and 5; the criterion as stated ("weekly new-defect discovery below 10") is currently satisfied, and if read as requiring sustained achievement, two consecutive compliant weeks exist. Week 4's 13 (option D) is history, not current state — exit criteria describe the present condition of the trend. Criterion 2 — no new criticals for 2 consecutive weeks: weeks 5 and 6 found 0 and 0 ✔. Criterion 3 — all found criticals fixed and retested: 2 remain open ✗. Two of three criteria pass; the third blocks: option B. The shape of the numbers is worth reading as a lead — a falling discovery curve (28→5) with criticals extinguished first is the classic signature of a product converging to releasable, which is why the open pair is a completion matter, not a stability concern; your **Testing** skill's release advice should say exactly that: "the trend supports release; the two open criticals are the entire critical path — fix, retest, ship." Option A waves through open critical defects; option C discards five weeks of convergence evidence. Exit criteria exist to be checked one by one; the discipline of reporting which passed, which failed, and what that means for the decision is what "authoritative advice on test planning" sounds like in numbers.

**Question 7 (moderate) — Pro-rated credit with an exclusion clause**

A supplier's monthly charge is £60,000. The contract: unavailability earns a credit of 2% of monthly charge per full hour of downtime, capped at 20% of the monthly charge; downtime during customer-requested emergency changes is excluded from the calculation. This month's downtime: one 6.5-hour outage (supplier fault) and one 3-hour outage during an emergency change your department requested. What credit is due?

- A) £12,000
- B) £7,200
- C) £11,400
- D) £10,800

**Correct answer: B**

**Explanation:** Apply the exclusion first: the 3-hour emergency-change outage is excluded, leaving the 6.5-hour supplier-fault outage. Apply the "per full hour" definition: 6.5 hours contains 6 full hours (contracts saying "per full hour" count completed hours unless stated otherwise). Credit: 6 × 2% = 12% of £60,000 = 0.12 × 60,000 = £7,200 — option B. Check the cap: 20% of 60,000 = £12,000; £7,200 is under it, so the cap does not bind. Option A charges all 9.5 hours (ignoring the exclusion, rounding up: 9.5 → 10 hours × 2% = 20%, hitting the cap at £12,000). Option C counts 9.5 as 9.5 hours (19% = £11,400), ignoring both the exclusion and the full-hour rule. Option D rounds 6.5 up to 7 hours... wait — 7 × 2% = 14% = £8,400, while £10,800 is 18% (9 full hours of 9.5 — exclusion ignored, full-hour rule applied). Every wrong option is a defensible-looking misreading of one clause: this is exactly how supplier credit disputes arise, and why the lead managing third-party provision computes the credit from the contract's exact words — exclusion, then full-hour counting, then cap — and shows the sequence, so the number arrives with its reasoning attached and the negotiation is about facts rather than arithmetic.

**Question 8 (moderate) — Team utilisation and the cost of interruptions**

Your 6-engineer team logs its time for a month (each engineer: 160 hours, 960 team hours total): project work 480 hours; BAU operations 240 hours; unplanned interruptions (incident pulls, ad-hoc requests) 144 hours; improvement work 48 hours; training 48 hours. A programme asks you to commit "half your team" (480 hours/month) to a new project while "keeping everything else running". What does the arithmetic show?

- A) The commitment fits — 480 hours of project work is already happening, so the new project simply replaces it.
- B) The commitment fits if training is cancelled.
- C) The commitment cannot fit alongside existing obligations: non-project demands (240 + 144 + 48 + 48 = 480 hours) already consume half the team's hours, and the existing 480 project hours presumably serve current commitments — so the new project requires either dropping existing project work, reducing BAU/interruption load, or additional people; present these options with the data.
- D) The commitment fits because interruptions can be eliminated by refusing ad-hoc requests.

**Correct answer: C**

**Explanation:** Sum the non-project demand: BAU 240 + interruptions 144 + improvement 48 + training 48 = 480 hours — exactly half the team's 960. The other 480 is current project work, which serves existing commitments that do not vanish because a new programme asks. So "half your team for the new project, keeping everything else running" requires 480 (new) + 480 (existing projects) + 480 (everything else) = 1,440 hours from a 960-hour team: arithmetically impossible without change — option C, whose second half is the lead skill: the answer to the programme is not "no" but the options table — displace which existing project, fund which additional capacity, or reduce which standing demand — with the time data attached. Option A assumes existing project commitments are free to cancel — sometimes true, never assumable. Option B recovers 48 hours against a 480-hour gap while spending the team's development — the classic false economy that leads are specifically positioned to refuse. Option D prices interruptions at zero: the 144 hours are incidents and genuine operational needs; refusal converts them into outages and escalations, not into capacity. Managing resources so the function works effectively — your **Systems integration** duty — begins with a truthful hours ledger, and this month's real logged data is the most persuasive document in any resourcing negotiation.

**Question 9 (moderate) — Reading a trend with seasonality**

Monthly incident counts for the service you oversee, over 12 months (January to December): 82, 78, 80, 76, 74, 71, 69, 72, 88, 92, 95, 90. A stakeholder says: "Incidents rose 10% over the year (82 → 90), and the autumn numbers show the service deteriorating rapidly." Last year showed the same autumn shape (September–December well above summer). What is the soundest reading?

- A) The stakeholder is right: the autumn rise shows accelerating deterioration.
- B) The year shows a gentle underlying improvement (January's 82 to August's 72, a downward drift) overlaid with a recurring autumn seasonal peak also present last year; compare autumn to last autumn, not to summer, before concluding deterioration.
- C) The data shows no pattern at all.
- D) Incidents fell 12% (82 → 72), so the service improved and autumn can be ignored.

**Correct answer: B**

**Explanation:** Decompose trend from seasonality. January through August drifts downward — 82 to 72, roughly −1.4/month — a genuine underlying improvement. September–December (88, 92, 95, 90) jumps well above the drift line, but the passage states last year showed the same autumn shape: a recurring seasonal pattern (in government services, often driven by annual cycles — year-end processing, seasonal demand, onboarding surges). The valid deterioration test is year-on-year like-for-like: this autumn's 88–95 against last autumn's figures — data the stakeholder's summer-versus-autumn comparison ignores. Option B states both components and names the correct comparison. Option A reads seasonality as trend — the most common error in operational reporting, and one that misdirects real money toward fixing a phenomenon that recurs on schedule regardless. Option D makes the opposite error, cherry-picking the drift's endpoints and dismissing autumn — the seasonal load is real and must be planned for, even though it is not deterioration. Option C gives up on visibly structured data. Your proactive problem-searching duty (**Ownership and topic**) runs on exactly this decomposition: the underlying drift tells you whether prevention is working; the seasonal component tells you when to pre-position capacity; and confusing them wastes both budgets.

**Question 10 (hard) — Cost model with utilisation-dependent pricing**

You are evaluating two support models for a 400-server estate. Model 1: fixed £180,000/year covering unlimited incidents. Model 2: £96,000/year base plus £150 per incident. Historical incident volume is 40 incidents per month, but a reliability programme completing this year is forecast (with reasonable confidence) to reduce volume by 30% from month 1 of the contract. The contract runs 24 months. Which model is cheaper over the contract, and what does the decision most depend on?

- A) Model 1, by £4,800 — and the decision is insensitive to incident volume.
- B) Model 2, by about £67,000 if the 30% reduction materialises; but if volume stays at 40/month, Model 2 saves only about £24,000 — Model 2 is cheaper either way, though the margin varies substantially with the forecast.
- C) Model 2, by about £24,000 regardless of the reduction.
- D) Model 1, because unlimited cover always beats per-incident pricing at this scale.

**Correct answer: B**

**Explanation:** Cost both models at both volumes over 24 months. Model 1: £180,000 × 2 = £360,000 regardless of volume. Model 2 at reduced volume (40 × 0.7 = 28 incidents/month): incidents = 28 × 24 = 672; cost = (£96,000 × 2) + (672 × £150) = £192,000 + £100,800 = £292,800; saving versus Model 1 = £360,000 − £292,800 = £67,200. Model 2 at unreduced volume (40/month): incidents = 40 × 24 = 960; cost = £192,000 + (960 × £150) = £192,000 + £144,000 = £336,000; saving = £24,000. In both scenarios Model 2 is cheaper — the decision is robust to whether the reliability programme delivers — but the margin ranges from about £24,000 to about £67,000: option B. The break-even volume makes the robustness precise: Model 2 costs more than Model 1 when 192,000 + 150 × N > 360,000, i.e. N > 1,120 incidents over 24 months ≈ 46.7/month — 17% above even the historical volume. Option A and D assert Model 1 without arithmetic; option C fixes the margin at its worst case. The lead-level method on display: cost options under both the forecast and its failure, find the break-even, and report the decision's sensitivity — "cheaper either way; margin depends on the reliability programme" is a recommendation a budget holder can sign, and sensitivity analysis is what separates a cost model from a hope.

**Question 11 (hard) — Availability of serial and parallel compositions**

A service chain has three stages: a load-balanced web tier (two independent nodes, each 99.0% available — the tier works if either node works), a single application server (99.5% available), and a database cluster (99.9% available). Stages are in series: the service works only if all three stages work. Assuming independence, what is the approximate end-to-end availability?

- A) 99.90%
- B) 99.39%
- C) 98.41%
- D) 99.99%

**Correct answer: B**

**Explanation:** Compute the parallel tier first, then multiply the series. Web tier: each node fails 1% of the time; both fail simultaneously (independent) with probability 0.01 × 0.01 = 0.0001, so tier availability = 1 − 0.0001 = 99.99%. Series composition: 0.9999 × 0.995 × 0.999. Step by step: 0.9999 × 0.995 = 0.99490; 0.99490 × 0.999 = 0.99391 ≈ 99.39% — option B. Option A quotes the best component; option D quotes the redundant tier alone; option C (98.41%) is what you get by multiplying all four raw component figures including both web nodes in series (0.99 × 0.99 × 0.995 × 0.999) — the error of treating redundant components as serial dependencies. Two design lessons your reviews should carry: redundancy multiplies failure probabilities (making the redundant tier nearly perfect), while series chains multiply availabilities (making the whole worse than its weakest link — here the single 99.5% application server dominates the loss). The immediate engineering conclusion from the arithmetic: the next pound of resilience investment belongs at the application server, not the already-redundant web tier — and a lead who can produce that conclusion, with the calculation, in a design review is doing security-and-resilience engineering by numbers rather than by instinct. The independence assumption deserves its caveat in real designs: shared power, network, or platform makes "independent" optimistic, which is why measured availability runs below composed arithmetic.

**Question 12 (hard) — Reconciling a programme's schedule claim**

A programme reports: "Environment builds are 75% complete (18 of 24 environments delivered), consistent with the 75% elapsed schedule (week 9 of 12), so delivery is on track." Your team's records show the 18 delivered environments were the simple ones (average build effort 2 engineer-days each); the remaining 6 are the complex integration environments (average 8 engineer-days each). Your build team has 4 engineers, each contributing 4 build-days per week (the rest goes to support). Is the programme on track, and what is the soundest correction to its arithmetic?

- A) On track — 75% complete at 75% elapsed is the definition of on schedule.
- B) Not on track: measured by effort, the programme is 36 of 84 engineer-days from completion (43% of effort remains); the remaining 48 engineer-days at 16 build-days/week needs 3 weeks exactly — schedule-feasible only if nothing slips, with zero contingency; measured properly, the programme is at high risk, not "on track".
- C) Not on track: the remaining work needs 6 weeks, so the programme will finish 3 weeks late.
- D) On track, because the complex environments can be descoped.

**Correct answer: B**

**Explanation:** Recompute progress in effort, the unit that predicts time. Total effort: (18 × 2) + (6 × 8) = 36 + 48 = 84 engineer-days. Completed: 36 of 84 = 42.9% — not 75%; the count-based figure flatters because the easy units were (rationally) built first, a bias so common it has a name in delivery circles: the "watermelon" report — green outside, red inside. Remaining: 48 engineer-days. Capacity: 4 engineers × 4 build-days = 16 engineer-days/week. Time required: 48 ÷ 16 = 3 weeks — exactly the 3 weeks remaining (weeks 10–12). So the arithmetic says feasible with zero slack: any illness, environment defect, or integration surprise (and complex integration environments are where surprises live) lands directly on the deadline. Option B's verdict — schedule-feasible, zero contingency, high risk, and the unit-of-measure correction — is the full truthful picture. Option A accepts the flattering unit. Option C overshoots: 6 weeks would need the remaining work to be 96 engineer-days or capacity halved; the records support neither. Option D resolves the schedule by discarding scope nobody has agreed to discard — descoping is a board decision to propose, not an assumption to book. The lead pattern, central to overseeing programmes: progress percentages are only as honest as their units; recompute in effort, state the contingency explicitly (here: none), and escalate risk while the mitigation options — early support-load relief, a fifth builder, sequenced acceptance — are still cheap.

### Preparation tips

- **Recompute supplier figures from raw data and contract words.** Take a real invoice or credit calculation and rebuild it: exclusions first, then counting rules, then caps. The sequence is where disputes and test marks both live.
- **Practise both-scenario costing.** For any option comparison, cost the forecast and its failure, and find the break-even. Sensitivity is the difference between a model and a guess.
- **Convert progress claims into effort units.** Any percentage you meet this week — complete, compliant, utilised — ask: what is the unit, and does it predict what we care about? Recompute one real "on track" claim in engineer-days.
- **Drill compound growth against thresholds.** Year-by-year tables, not exponent shortcuts. The interesting answers are which side of a line you land on, and simple-growth approximations land wrong.
- **Master the two composition rules.** Parallel: multiply failure probabilities. Series: multiply availabilities. Then identify the weakest serial link — that is where the design conversation goes.
- **Keep an honest hours ledger for your team.** One month of real logged time is the most powerful artefact in resourcing negotiations and the direct analogue of the utilisation questions.
- **Decompose trend from seasonality before concluding.** Fit the drift on like-for-like periods; compare seasons to the same season last cycle. Practise on your own incident data.

### Common pitfalls to avoid

- **Stacking tiered credits or ignoring exclusions.** Contract bands replace each other; exclusions apply before counting; caps apply last. Order of operations is contractual, not stylistic.
- **Forecasting from plan rates after evidence exists.** Eight weeks of achieved productivity outranks the plan's assumption. Extrapolate reality.
- **Summing non-coincident peaks.** Consolidation capacity derives from observed simultaneous demand plus policy headroom — not the sum of individual maxima.
- **Simple growth where compounding decides.** Near thresholds and over multi-year horizons, the compounding term is the answer.
- **Counting units when effort predicts.** 75% of environments is not 75% of work when the hard ones remain. Recompute in the unit that maps to time.
- **Treating redundant components as serial (or vice versa).** Draw the reliability diagram before multiplying anything.
- **Reporting single numbers without sensitivity or contingency.** "Cheaper by £X if Y holds; by £Z if not" and "feasible with zero slack" are the honest forms. Both the test's hard questions and your board papers reward them.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand, evaluate, and act on written information of the kind a lead infrastructure engineer handles: supplier contracts and their schedules, programme governance papers, security architecture documents, lifecycle standards you author and ratify, escalations written to persuade, and the technical writing of the engineers you lead. The dominant formats are True/False/Cannot say judgements against a passage, supported-inference questions, best-summary items, argument evaluation, and clear-writing judgements — with the passages at your level longer, more interested, and more consequential than earlier in your career.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions. The governing rule remains: judge strictly from the passage, not from expertise or expectation — and at lead level a second discipline joins it: detect what a passage is doing as well as what it says, because much of what you read is written to persuade you of something its author needs.

Why do employers use verbal reasoning tests at this level? Because your role runs on high-stakes text in both directions. Inbound: contracts whose clauses you enforce against suppliers, programme papers whose claims you endorse or challenge at boards, incident narratives engineered to relocate cost, and standards whose interactions you must foresee before ratifying. A misread clause becomes an unenforced obligation; an unchallenged claim becomes your accountability. Outbound: you establish standards and procedures that practitioners across the life cycle must follow — text that fails only when someone follows it exactly and reaches the wrong place — and you lead others in applying modern development standards, which is largely the work of explaining written rules accurately and persuasively. At lead level, careful reading is due diligence, and clear writing is governance.

### How this assessment maps to your role

- **Contract-grade comprehension** maps to your role-level duty to manage third-party provision of infrastructure services: obligations, exclusions, measurement definitions, and remedy clauses assemble across separated text, and enforcement depends on assembling them correctly.
- **Auditing persuasive claims** maps to your duty to oversee programmes and projects and your **Ownership and topic** accountability: board papers, supplier narratives, and escalations arrive framed; your reading must separate what is established from what is asserted.
- **Standards drafting and interaction analysis** maps to your **Systems integration** duty to establish standards and procedures across the service product life cycle and ensure practitioners adhere to them — text you ratify becomes behaviour, including its ambiguities.
- **Security document precision** maps to your **Information security** skill: threat models, control descriptions, and advisory language carry exact scopes and conditions that your designs must honour.
- **Reviewing and developing others' writing** maps to your duty to lead teams and to lead others in applying **Modern development standards**: your review comments and worked examples are how the team's documentation standard is actually set.
- **Test documentation judgement** maps to your **Testing** skill: authoritative advice on test planning includes reading strategies, exit criteria, and results reports for what they claim versus what they demonstrate.

### Practice questions

**Question 1 (easy) — True/False/Cannot say on a contract schedule**

Passage (contract schedule): "The supplier shall provide 24/7 monitoring of the managed infrastructure. Alerts classified as critical shall be actioned within 15 minutes at all times. Alerts classified as major shall be actioned within 1 hour during core hours (07:00–19:00, Monday to Friday) and within 4 hours outside core hours. Classification of alerts is performed by the supplier's monitoring platform according to Annex F."

Statement: "A major alert raised at 21:00 on a Wednesday must be actioned by 22:00."

- A) True
- B) False
- C) Cannot say
- D) True, because monitoring is 24/7

**Correct answer: B**

**Explanation:** Classify the case, then apply its rule. The alert is major, raised at 21:00 Wednesday — outside core hours (which end at 19:00). The applicable obligation is the outside-core-hours term: actioned within 4 hours, so by 01:00 Thursday. The statement claims a 1-hour obligation (by 22:00), importing the core-hours term into a non-core case: contradicted, so False. Option D confuses monitoring coverage (24/7 watching) with response obligation (time-banded actioning) — a distinction suppliers rely on and customers routinely miss. The lead-level habit this rehearses: contracts define obligations as a matrix (severity × time window × sometimes site or service tier), and enforcement means locating the exact cell before citing a breach. Escalating a "missed" 1-hour response that the contract prices at 4 hours spends your credibility precisely where you need it most — and the final sentence's quiet delegation (the supplier's platform classifies the alerts, per Annex F) is the clause an experienced reader flags for later: whoever controls classification controls which obligations apply.

**Question 2 (easy) — What a standards clause actually requires**

Passage (from a standard you are asked to ratify): "All infrastructure changes should be tested in a representative environment before production deployment. Where no representative environment exists, teams must document the gap and the compensating verification performed. Teams must review their environments' representativeness annually."

Statement: "The standard makes pre-production testing in a representative environment mandatory for all infrastructure changes."

- A) True
- B) False
- C) Cannot say
- D) True, because the annual review enforces it

**Correct answer: B**

**Explanation:** Read the modal verbs with drafting-grade precision. The first sentence says "should" — in standards drafting, a recommendation, not an obligation; the mandatory terms ("must") attach only to documenting the gap and compensating verification when no representative environment exists, and to the annual review. So the standard does not mandate representative-environment testing; it recommends it and mandates the fallback discipline: the statement is False. Option D confuses reviewing representativeness with requiring testing. This should/must discipline is not pedantry at your level — it is exactly what you police when you establish standards and ensure practitioners adhere to them: a "should" cannot be enforced as a "must" (practitioners will justly object), and a "must" drafted as "should" is a control you believe exists but does not. When ratifying, read every requirement asking "what exactly is mandatory, on whom, triggered by what?" — and if the intent was mandatory testing, the finding is a drafting defect to fix before ratification, not after the first dispute.

**Question 3 (easy) — Cannot say on a programme board paper**

Passage (board paper): "The migration programme completed Tranche 1 on schedule. Stakeholder feedback has been positive. The programme team has identified efficiencies that will be applied to Tranche 2. The infrastructure workstream reports no open risks."

Statement: "Tranche 2 will complete on schedule."

- A) True
- B) False
- C) Cannot say
- D) True, because Tranche 1 did and efficiencies have been identified

**Correct answer: C**

**Explanation:** The paper reports Tranche 1's history, unquantified sentiment, an intention about efficiencies, and a risk-register snapshot. None of these is a claim about Tranche 2's completion, and no schedule forecast for Tranche 2 appears at all: the statement is neither supported nor contradicted — Cannot say. Option D performs the inference the paper is composed to invite — past success plus positive-sounding intentions read as future assurance — which is exactly how optimistic board papers work on hurried readers: nothing false is stated; the favourable conclusion is assembled in the reader's mind from adjacent true sentences. The lead-level reading skill is noticing what a paper does not say: no Tranche 2 baseline, no dependency status, no quantified efficiency, and "no open risks" from one workstream (which may mean none exist, or none are being recorded — itself a question worth asking). Your duty to oversee programmes means reading board papers the way this question requires: crediting exactly what is established, and turning the gaps into the meeting's questions.

**Question 4 (easy) — Judging a standard's worked example**

You are drafting a standard on secrets management and must include a worked example. Which example text best serves practitioners?

- A) "Secrets must be handled appropriately in pipelines, as described conceptually above."
- B) "Example: a deployment pipeline needs a database password. Compliant: the pipeline requests the password at run time from the approved vault using its pipeline identity; the password is never written to logs, code, or variables files. Non-compliant: the password stored in the pipeline's variables file, even marked 'secret' — because it leaves the vault's rotation and audit scope. If the vault is unavailable, the pipeline fails closed and alerts; it does not fall back to cached credentials."
- C) "Example: do not do bad things with passwords, such as putting them where they should not be."
- D) "For examples, consult your team lead."

**Correct answer: B**

**Explanation:** A worked example earns its place by resolving the cases practitioners actually face, and option B does the three jobs examples exist for: a concrete compliant path (run-time retrieval, pipeline identity), a concrete non-compliant path with the reason ("even marked 'secret'" — pre-empting the most common rationalisation, and explaining why: rotation and audit scope), and the edge case with its required behaviour (vault down → fail closed, no cached fallback). That third element is the mark of lead-grade drafting: standards fail at their edges, and the example that answers "but what if the vault is down?" prevents the improvised fallback that becomes an incident. Option A defers to concepts the practitioner has already found insufficient. Option C is exhortation without content. Option D converts a standard into a queue for your attention — and inconsistent oral rulings besides. This is your **Systems integration** standards duty and your **Modern development standards** leadership in one artefact: practitioners adhere to what they can unambiguously follow, and the quality of your examples — not the elegance of your principles — is what determines adherence.

**Question 5 (moderate) — Assembling obligations across contract clauses**

Passage (contract extracts): "Clause 7.2: The supplier shall remedy any security vulnerability classified Critical under Annex D within 5 working days of notification. Clause 7.6: Where remediation requires a change to customer-side configuration, the remediation period is suspended from the date the supplier notifies the customer of the required change until the customer confirms completion. Clause 7.9: Failure to remedy within the applicable period entitles the customer to engage a third party to remediate at the supplier's reasonable cost."

The customer notified a Critical vulnerability on Monday 1st. On Wednesday 3rd, the supplier notified the customer that remediation required a customer-side firewall change; the customer confirmed completion on Tuesday 9th. The supplier completed remediation on Monday 15th. (Assume all weekdays are working days, no holidays.) Did the supplier remedy within the contractual period?

- A) No — 5 working days from Monday 1st expired on Monday 8th, and suspension is irrelevant.
- B) No — the clock ran 2 working days (Tuesday 2nd and Wednesday 3rd), was suspended until the customer's confirmation on Tuesday 9th, then resumed with 3 working days remaining, expiring Friday 12th; completion on Monday 15th missed the deadline by one working day.
- C) Yes — once suspension is applied, the deadline was Monday 15th and the supplier met it exactly.
- D) Cannot be determined without Annex D.

**Correct answer: B**

**Explanation:** Run the clock day by day with the suspension. Using the standard convention that the count starts the working day after notification, days 1 and 2 are Tuesday 2nd and Wednesday 3rd; the supplier's Wednesday notification of the required customer-side change suspends the clock with 3 of 5 working days remaining. Suspension runs until the customer confirms completion on Tuesday 9th. The clock resumes Wednesday 10th: the three remaining working days are Wednesday 10th, Thursday 11th, and Friday 12th — the contractual deadline. The supplier completed on Monday 15th: one working day late, so the answer is that the supplier did not remedy in time — option B. Option A ignores Clause 7.6 entirely and computes a bare Monday 8th deadline, which would wrongly put the supplier three working days late and invite an unwinnable dispute. Option C applies the suspension but then miscounts the resumed period, granting the supplier the extra day it needs. Option D hides behind Annex D, which governs only classification — and the vulnerability is given as Critical. The lead-level takeaway: suspension and pause clauses are where supplier deadlines are won and lost; compute them day by day on paper, because the difference between Friday 12th and Monday 15th is the difference between your contractual remedy rights (Clause 7.9) existing or not — and because a miscomputed accusation costs more credibility than no accusation at all.

**Question 6 (moderate) — Detecting the pivot in a supplier's escalation response**

Passage (supplier letter): "We acknowledge the service issues experienced in recent months and take them seriously. Our engineers have worked tirelessly, often beyond contracted hours, to maintain service. It is worth noting that the customer's environment has grown 30% since the contract was signed, and that several recent incidents originated in components outside our managed scope. We remain committed to service excellence and propose a joint workshop to redefine the service baseline."

Which is the most accurate reading of the letter's substance?

- A) The supplier accepts responsibility and will fix the issues at no change to terms.
- B) The letter concedes nothing specific: it acknowledges "issues" without accepting causation, repositions the cause toward customer growth and out-of-scope components, and its concrete proposal — redefining the baseline — is an opening move toward renegotiating scope or price.
- C) The supplier is declaring the contract void.
- D) The letter is a routine courtesy with no operational significance.

**Correct answer: B**

**Explanation:** Parse what is admitted, what is asserted, and what is proposed. Admitted: "issues experienced" — experience acknowledged, causation not; "worked tirelessly" is effort evidence, which subtly implies the problem exceeds reasonable effort, preparing the reframe. Asserted: 30% growth and out-of-scope origins — both may be true (and deserve verification against your records: growth against the contract's flex provisions, incident origins against your own incident data), but their function in the letter is causal relocation. Proposed: a "joint workshop to redefine the service baseline" — the only concrete action, and redefining a baseline is how scope grows or price rises through a side door. Option B reads all three layers. Option A mistakes tone for content: nothing is accepted, nothing is promised. Option C over-reads considerably. Option D under-reads: a baseline-redefinition proposal is operationally significant and time-sensitive. This is the inbound half of managing third-party provision: supplier correspondence is drafted by people skilled at appearing responsive while repositioning — your reply should accept the workshop, decouple it from any baseline change, and put your incident-origin data on the table first.

**Question 7 (moderate) — Argument evaluation in a governance paper**

Passage (from a paper you must endorse or challenge at a programme board): "We recommend accepting the residual risk of single-site operation for the reporting service. The service is internal-only, and its users have tolerated planned maintenance outages of up to four hours without business impact. Dual-site provision would cost £150,000 per year. No incident has yet caused an unplanned outage exceeding four hours. Therefore the risk is acceptable and the saving should be taken."

Which is the strongest challenge to the argument?

- A) £150,000 is a small amount for a government department, so cost should not be considered.
- B) The argument prices the mitigation but never quantifies the risk: tolerance of planned four-hour outages does not establish tolerance of unplanned multi-day loss — the realistic single-site failure mode (site loss with rebuild-from-backup recovery) — and "no incident yet" is survivorship evidence, not a probability. The comparison the decision needs (likelihood × duration × business cost of site loss versus £150,000/year) is absent.
- C) All services must be dual-site as a matter of principle, regardless of cost.
- D) Internal-only services do not need risk assessment.

**Correct answer: B**

**Explanation:** Audit what the argument compares. It offers: user tolerance of planned, bounded, four-hour outages; an absence of severe incidents to date; and a mitigation cost. The decision requires: the unplanned failure distribution — and single-site's defining exposure is not a four-hour blip but site loss, where recovery is rebuild-from-backup measured in days; the business cost of that duration (month-end reporting deadlines, dependent decisions); and its likelihood. The argument substitutes tolerance of the mild, planned case for tolerance of the severe, unplanned one — a category substitution — and offers "no incident yet" where a rate belongs, which is evidence of the same weight the day before any site loss ever recorded. Option B names both defects and states the missing comparison, which is the constructive form of challenge: it tells the paper's authors exactly what analysis would earn endorsement — risk acceptance may still be the right decision, decided on the actual comparison. Option A dismisses cost, which is always material in public spending. Options C and D replace analysis with absolutes in opposite directions. This is the endorsement duty of overseeing programmes: your name at a board attaches to the argument's quality, not just its conclusion — challenge the reasoning while remaining genuinely open to its repaired conclusion.

**Question 8 (moderate) — Precision in a security architecture document**

Passage: "The platform enforces network segmentation between tenant environments. Traffic between tenants is denied by default. Exceptions require a documented data-sharing agreement between the tenant owners and are implemented as one-directional flows on named ports. Exception flows are reviewed quarterly; flows without a current data-sharing agreement at review are removed. Intra-tenant traffic is not restricted by the platform and is the tenant's responsibility."

Statement: "If Tenant A has a documented data-sharing agreement with Tenant B, the platform permits traffic between them in both directions on the agreed ports."

- A) True
- B) False
- C) Cannot say
- D) True, because the agreement covers both parties

**Correct answer: B**

**Explanation:** The exception mechanism is specified as "one-directional flows on named ports": an agreement enables the creation of directional exceptions, and bidirectional traffic would require two one-directional flows — the passage nowhere says an agreement automatically yields both directions. The statement claims the platform "permits traffic in both directions" on the strength of the agreement alone: contradicted by the one-directional specification, so False. Option D reasons from the agreement's symmetry between parties to the flows' symmetry — a social inference imported into a technical specification, exactly the substitution security reviews exist to catch. Directionality is not pedantry: one-directional flow design is a deliberate control (Tenant A pushing data to B does not entitle B to reach into A), and reading it loosely in a design review would wave through the reverse path an attacker wants. This is your **Information security** skill at documentary grain — controls "specifically engineered to mitigate threats" are specified in exact directional, port-level language, and the review question for every exception is: which direction, which ports, under which agreement, until which review. The quarterly-review-and-removal clause is the passage's second control worth noticing: exceptions decay unless re-justified — a pattern worth copying into your own standards.

**Question 9 (moderate) — Best summary of a lifecycle standards passage**

Passage: "Standards earn adherence through three properties. They must be findable: a standard practitioners cannot locate at the moment of decision does not exist operationally. They must be decidable: a practitioner reading the standard with their actual case in hand must be able to determine what it requires without interpretation escalating to its author. And they must be maintained: a standard contradicted by the current toolchain teaches practitioners that standards in general are optional. Publication ceremonies, mandatory-reading emails, and compliance attestations do not substitute for these properties; they measure exposure to the text, not the text's operational force."

Which summary best captures the passage?

- A) Standards require better publicity: ceremonies, emails, and attestations drive adherence.
- B) Standards gain operational force from being findable at the point of decision, decidable for real cases without author escalation, and maintained against toolchain reality — properties that exposure mechanisms cannot substitute for.
- C) Standards are generally ignored and the effort of writing them is wasted.
- D) Standards should be short.

**Correct answer: B**

**Explanation:** The passage's architecture: three named properties (findable, decidable, maintained), each with its operational rationale, followed by an explicit anti-claim — exposure mechanisms measure contact with the text, not its force. Option B reproduces all three properties with their point-of-use framing and preserves the anti-claim. Option A asserts what the final sentence denies. Option C converts a theory of adherence into cynicism the passage does not contain. Option D invents a property. Beyond the comprehension marks, the content is a working checklist for your **Systems integration** duty to establish standards and ensure adherence: audit your current standards against the three properties — can an engineer mid-change find the relevant standard in under a minute; does it decide their actual case; does it match the current tooling? — because "ensure that practitioners adhere" is achieved through these properties, not through enforcement theatre. The passage also arms you for a common governance conversation: when compliance attestation rates are offered as evidence of adherence, the distinction between exposure and operational force is the precise objection.

**Question 10 (hard) — Interaction between a policy and a contract**

Passage: "Departmental security policy SP-8: Cryptographic keys protecting departmental data must be generated, stored, and used within hardware security modules (HSMs) under departmental control. Supplier contract clause 14.3: The supplier shall encrypt all customer data at rest using keys managed in the supplier's key management service, which holds a current certification under the applicable international standard. Contract clause 2.1: In the event of conflict between this contract and the customer's published security policies referenced in Schedule 1, the customer's policies prevail. Schedule 1 lists SP-1 through SP-9."

Statement: "For departmental data held by this supplier, encryption keys managed solely in the supplier's key management service satisfy the contractual arrangements as a whole."

- A) True — clause 14.3 expressly provides for it.
- B) False — SP-8 is in Schedule 1's range, so it prevails over clause 14.3 under clause 2.1; keys must be under departmental HSM control, and the supplier's KMS-only arrangement conflicts with the prevailing policy.
- C) Cannot say — the certification status resolves the conflict.
- D) True — certification under the international standard satisfies SP-8's intent.

**Correct answer: B**

**Explanation:** Three texts interact; establish the hierarchy first. Clause 2.1 is a precedence clause: where contract and referenced customer policies conflict, the policies prevail — and Schedule 1 lists SP-1 through SP-9, which includes SP-8. Now test for conflict: SP-8 requires keys generated, stored, and used within HSMs "under departmental control"; clause 14.3 places key management in "the supplier's key management service". Supplier-controlled KMS is not departmental control: the texts conflict, the precedence clause activates, and SP-8 prevails — so the KMS-only arrangement fails the contractual arrangements as a whole: False as stated, option B. Option A reads clause 14.3 in isolation, ignoring the precedence structure — the standard error of reading contracts clause-by-clause rather than as a system. Option D substitutes certification for control: the certification speaks to the KMS's quality, while SP-8's requirement is about who controls the keys — different dimensions, and "satisfies the intent" is exactly the loose reading that precedence clauses exist to shut down. Option C makes certification a resolver the texts nowhere appoint. The lead-level practice this rehearses: when you manage third-party provision, build the document hierarchy before assessing any single clause — precedence provisions, schedules, and referenced policies form the actual rule, and suppliers' delivery teams frequently implement their contract's convenient clause without reading the customer-policy override that defeats it.

**Question 11 (hard) — Evaluating an escalation you must forward**

Passage (escalation from one of your engineers, addressed to a programme director, sent to you for forwarding): "The programme's decision to compress environment testing from three weeks to one is reckless and shows a complete disregard for engineering reality. My team has repeatedly warned about this. When the deployment fails, the record will show whose fault it was. I want this escalation formally noted."

You agree with the underlying technical concern. Which response best fulfils your role?

- A) Forward it unchanged — the concern is valid and the anger is understandable.
- B) Refuse to escalate — the tone makes the concern unraisable.
- C) Rework the escalation with the engineer: keep the substantive claim, replace accusation with evidence (what three weeks of testing covers that one week cannot, with the specific risks left unexamined and their plausible cost), state the requested decision (restore the window, or formally accept the named risks), and send it under joint names — teaching, in the process, why this form is more likely to change the decision.
- D) Send your own soft note asking the programme to "consider testing implications when convenient".

**Correct answer: C**

**Explanation:** Separate the concern (valid, and yours to champion) from the instrument (built to assign blame, not to change a decision). The draft's failure is functional: "reckless", "complete disregard", and "the record will show whose fault" position the programme director as an adversary preparing for an inquiry — the predictable response is defensive entrenchment, and the compression stands. Option C converts the escalation into decision-grade form: the evidence gap (what the lost fortnight of testing would have examined — the specific integration scenarios, failure modes, and data conditions), the consequence estimate, and the decision requested — restore the window or accept the named risks formally, which puts the accountability where the engineer rightly wants it, through governance rather than grievance. Doing the rework with the engineer, not to them, is the leadership half: they learn why evidence-and-decision beats accusation — a lesson that compounds across their career — and joint signature keeps their authorship and courage intact. Option A spends the concern's validity on the draft's tone; forwarding unchanged also implicitly endorses the register as acceptable escalation practice in your team. Option B protects the relationship by silencing the risk — inverting your accountability. Option D raises it in a form engineered to be ignorable: "when convenient" prices the risk at zero. Leading teams includes editing their anger into influence — the concern deserves to win, and form is what determines whether it can.

**Question 12 (hard) — Reading exit criteria the way a dispute would**

Passage (from a programme's test completion report): "System testing is complete. 1,847 of 1,900 planned tests were executed, a 97.2% execution rate. Of executed tests, 96.1% passed. The 53 unexecuted tests relate to the payments reconciliation module, whose test environment was unavailable throughout the test phase; these will be executed in production during the first live reconciliation cycle, under enhanced monitoring. All severity-1 defects are closed. The programme therefore certifies the exit criteria as met: 'execution of the test plan with a pass rate exceeding 95%, and no open severity-1 defects.'"

Which reading should a lead engineer put to the programme?

- A) The certification is sound: 97.2% execution and 96.1% pass both exceed 95%.
- B) The certification does not withstand the criteria's own words: "execution of the test plan" is not satisfied by 97.2% when the entire unexecuted remainder is one module — the plan is unexecuted for payments reconciliation specifically, and "testing in production during the first live cycle" means the module goes live untested; the pass-rate and severity-1 criteria are met, but the certification conceals a concentrated, unmitigated gap behind aggregate percentages.
- C) The certification fails because the pass rate should be measured against planned, not executed, tests.
- D) The certification is sound because enhanced monitoring compensates for the unexecuted tests.

**Correct answer: B**

**Explanation:** Read the criteria as written, then read the aggregates for what they conceal. The criterion says "execution of the test plan" — completion, not a percentage; 97.2% would be a defensible reading if the shortfall were scattered friction, but the passage concentrates all 53 unexecuted tests in one module: payments reconciliation is 0% executed, and the plan for it simply was not run. Aggregation is doing the concealing — 97.2% is true and materially misleading, the exact pattern of the "watermelon" report. The remedy language deserves its own scrutiny: "executed in production during the first live reconciliation cycle" is a euphemism for going live untested on a payments module, with monitoring — which detects failures — offered in the place of testing, which prevents them: option D accepts that substitution; option B names it. Option C invents a measurement basis the criteria do not state (the pass criterion says "pass rate exceeding 95%" and 96.1% of executed meets any reasonable reading). The constructive path option B implies: either the environment gap is closed and the module tested before go-live, or the board formally accepts a quantified, named risk — payments reconciliation live-untested — rather than certifying criteria "met". Your **Testing** skill's authoritative-advice duty is precisely this reading: exit criteria are contracts, aggregates are advocacy, and the lead's question is always where the unexecuted, unpassed, and unexamined are concentrated.

### Preparation tips

- **Read one real contract schedule weekly.** Locate the obligation matrix (severity × window × exclusions) and compute one deadline through any suspension clauses. Contract-grade reading is a trainable speed skill.
- **Parse modal verbs as a drafting audit.** In your own standards, list every "must", "should", and "may" with its subject and trigger. What you find will improve both your test performance and your documents.
- **Practise three-layer reading of interested text.** For any supplier letter or board paper: what is admitted, what is asserted, what is proposed. The substance almost always lives in the proposal.
- **Build document hierarchies before judging clauses.** Precedence provisions, schedules, and referenced policies form the actual rule. Sketch the hierarchy in the margin before answering interaction questions.
- **Hunt concentration behind aggregates.** For any percentage in a report, ask where the remainder is concentrated. Scattered shortfall and concentrated shortfall are different findings wearing the same number.
- **Rework one angry draft into decision form.** Evidence, consequence, requested decision. Doing this exercise on real material trains the judgement the hardest verbal items test.
- **Audit your standards against findable-decidable-maintained.** The exercise improves your estate and fixes the three-property framework in memory for summary questions.

### Common pitfalls to avoid

- **Importing the wrong matrix cell.** Core-hours terms applied to out-of-hours cases, critical timelines applied to major alerts. Locate severity and window before citing any obligation.
- **Reading "should" as "must".** Recommendations cannot be enforced as obligations — in the test or in your governance. The modal verb is the requirement.
- **Accepting invited inferences.** Optimistic papers assemble favourable conclusions from adjacent true sentences. Credit only what is stated; convert the gaps into questions.
- **Mistaking tone for content.** Apologetic supplier letters conceding nothing, angry escalations containing valid risks — judge the substance independently of the register.
- **Reading clauses in isolation.** Precedence provisions and referenced policies routinely defeat the convenient clause. The rule is the system of documents, not any sentence in it.
- **Letting certifications and monitoring substitute for the required thing.** Certification is not control; monitoring is not testing; attestation is not adherence. Match each offered substitute against the actual requirement.
- **Treating aggregate percentages as findings.** The concentrated gap behind a high percentage is the finding. Ask what the denominator hides before endorsing any number.

<!-- APPEND -->
