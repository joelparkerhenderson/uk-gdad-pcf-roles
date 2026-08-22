# Change and Release Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a change and release analyst working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for your next post, checking your own progress, or simply curious about how psychometric assessments connect to your day-to-day work, this document will help you practise, build confidence, and feel ready.

First, a reassuring word. Psychometric assessments can sound intimidating, but they are really just structured, standardised exercises that measure the thinking skills and workplace judgement that predict success in a role. Nobody expects you to be perfect, and nobody passes every question. What matters is steady, careful practice — and that is exactly what this guide gives you. Everything here has been designed around your actual role, at your actual level. You will not find abstract brain-teasers about coloured shapes or trains leaving stations. Instead, you will work with the materials you genuinely handle: change requests, release schedules, deployment checklists, configuration records, incident logs, and messages from DevOps colleagues and service designers.

Why do these assessments matter for your role in particular? As a change and release analyst, you plan and roll out software, and you design and carry out the procedures for distributing and installing changes to systems and services. You analyse what happened after each release and set the plan for upcoming changes. That work rewards four capabilities that assessments measure directly: cognitive ability (spotting a broken step in a deployment procedure before it causes an incident), numerical reasoning (working out a release success rate or reading a table of change volumes), verbal reasoning (understanding exactly what a change policy does and does not say), and situational judgement (choosing the right action when a release goes wrong at 4:55pm on a Friday). Practising these skills does not just prepare you for a test — it makes you better at the job itself.

This document is organised into four main assessment sections, one for each assessment type. Each section follows the same friendly pattern: an overview of what the assessment measures and how it is usually run, a mapping of the assessment to the specific skills in your role, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The questions start easy and get gradually harder, so you can warm up before you stretch.

Here is how to get the most from the guide. First, read each "About this assessment" section so the format holds no surprises. Second, attempt each practice question honestly — write your answer down before you peek at the explanation. Third, treat every explanation as a mini-lesson: even when you answer correctly, the walkthrough will sharpen your technique and show you how the skill appears in your real work. Fourth, do not rush. Little and often beats one long cramming session, and the confidence you build by practising calmly will serve you far better on the day than memorised tricks.

One more thing before you begin: be kind to yourself. You are early in your journey in change and release management, and that is exactly where you are supposed to be. Every question you get wrong in practice is one you will get right when it counts. Take a breath, find a quiet spot, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of asking you to rotate shapes in your head, it presents the everyday materials of your job — change requests, release calendars, deployment runbooks, configuration management database (CMDB) records, and post-release reports — and asks you to reason quickly and accurately about them.

The typical format is an online, timed test lasting 15 to 30 minutes, with somewhere between 15 and 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared against a norm group of people at a similar level, so you are never being measured against senior managers with twenty years of experience. Many modern platforms are adaptive, which means the questions get slightly harder when you answer correctly and slightly easier when you do not — so if the test feels like it is stretching you, that is a sign you are doing well, not badly. Employers usually receive a breakdown of accuracy and speed rather than a single pass-or-fail mark. You will almost always be offered a few ungraded practice questions before the real test starts, so you can get comfortable with the screen layout without any pressure.

Why do employers use cognitive assessments for a change and release analyst? Because your role is, at its heart, about careful structured thinking under time pressure. When you plan a software rollout, you hold several moving parts in mind at once: which environments the release passes through, which changes depend on which others, which release window is available, and what the back-out plan is if something fails. When you carry out post-release analysis, you look for patterns in what went well and what did not. When you check a change request, you spot missing or contradictory information before it reaches the change advisory board. A well-designed cognitive assessment simulates exactly those demands in miniature — which is why practising for it genuinely improves your daily work.

One reassurance about timing: these tests are designed so that most people do not finish every question. Working steadily and accurately is almost always a better strategy than racing. Accuracy first, speed second — the speed comes naturally with practice.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Asset and configuration management** skill: maintaining secure configuration and accurate information means noticing when a CMDB record does not follow the naming convention, when the same server appears twice under different labels, or when a cluster of failed deployments shares a common feature. It also supports your post-release analysis duty — patterns in release outcomes tell you what to change in the next plan.
- **Logical deduction** maps to your **Change management** skill: analysing and assessing the impact of change requires you to reason from rules — change freeze policies, approval requirements, dependency statements — to their necessary consequences. If the policy says X and the facts say Y, what must follow?
- **Error checking** maps to both **Asset and configuration management** (verifying the location and state of IT assets) and **Change management** (documenting change requests): a single wrong field in a change record or a step out of order in an installation procedure can cause a failed release, so your eye for small inconsistencies is one of your most valuable professional assets.
- **Prioritisation** maps to your **Incident management** skill (identifying and registering incidents and allocating them to the appropriate channel) and to your **Ownership and topic** skill (knowing when to handle something yourself and when to pass a problem to your team): every working day asks you to decide what to do first.
- **Applied problem solving** maps to your **Problem management** skill: investigating problems in systems, processes and services — and understanding whether a problem is strategic, tactical or operational — means decomposing a messy situation into causes and contributing to remedies and preventative measures. It also draws on your duty to liaise with DevOps and service designers, because solving release problems is nearly always a team activity.

### Practice questions

**Question 1 (easy) — Pattern recognition in release version numbers**

Your team names releases using the pattern "service name, hyphen, major version, dot, minor version, dot, patch number" — for example, "caseportal-2.4.1". While preparing next month's release calendar, you see these five entries:

1. caseportal-2.5.0
2. paygateway-1.12.3
3. docstore-3.0.1
4. notifyhub-4.2
5. caseportal-2.5.1

Which entry breaks the naming pattern?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: C**

**Explanation:** The pattern requires three numbers separated by dots: major, minor, and patch. Entry 4, "notifyhub-4.2", has only two numbers — the patch number is missing. Entry 2 might look odd because "12" is a two-digit minor version, but nothing in the rule limits how large each number can be, so it is fine. Entries 1, 3 and 5 all follow the rule exactly. This is precisely the kind of consistency check you perform when you maintain accurate configuration information: naming conventions look like small details, but a release calendar with inconsistent version labels causes real confusion when someone has to work out which patch is actually deployed in production. In the test, read the rule carefully first, then check each option against it one at a time — do not rely on what "looks" wrong.

**Question 2 (easy) — Logical deduction from a change freeze rule**

Your organisation's change policy states: "During the December change freeze, no changes may be deployed to production unless the change is classed as an emergency change and has been approved by the change and release manager." It is 12 December, inside the freeze. A colleague tells you: "The fix for the payments service was deployed to production this morning." Which one of the following conclusions must be true?

- A) The fix was an emergency change approved by the change and release manager.
- B) The deployment breached the change policy.
- C) Either the fix was an approved emergency change, or the deployment breached the policy.
- D) The payments service had a major incident this morning.

**Correct answer: C**

**Explanation:** The policy is a rule with exactly one permitted exception. From the facts given, you know a production deployment happened during the freeze — but you do not know whether it qualified for the exception. So option A is possible but not guaranteed, and option B is possible but not guaranteed. Option D invents information that appears nowhere in the question: emergency changes are often linked to incidents, but the question never says so here. The only statement that must be true in every situation consistent with the facts is option C: one of the two possibilities holds. Assessments reward this discipline of deducing only what the information guarantees — and so does your job. Before flagging a colleague's deployment as a breach, you would check the emergency change records first. That habit protects both your accuracy and your working relationships.

**Question 3 (easy) — Error checking a deployment checklist**

Your standard installation procedure for a service update lists these steps in order: (1) confirm the change is approved; (2) take a backup of the current version; (3) deploy the new version to the staging environment; (4) run the smoke tests in staging; (5) deploy to production; (6) run the smoke tests in production; (7) update the CMDB with the new version number. A new team member has written up the procedure for a different service as: confirm approval, deploy to staging, take a backup, run staging smoke tests, deploy to production, run production smoke tests, update the CMDB. What is wrong with the new write-up?

- A) The backup step is missing entirely.
- B) The backup happens after deployment to staging instead of before it.
- C) The CMDB update should happen before production deployment.
- D) Nothing is wrong; the order is acceptable.

**Correct answer: B**

**Explanation:** Compare the two sequences step by step. The standard procedure takes the backup as step 2, before anything is deployed anywhere. The new write-up moves the backup to after the staging deployment. The backup is present (so A is wrong), and the CMDB is correctly updated last, after production reflects reality (so C is wrong — a CMDB updated before deployment would briefly record a version that is not actually live, which is exactly the kind of inaccuracy your role exists to prevent). The order matters because the backup exists to support a back-out: you want a clean copy of the known-good state before the change process begins. In staging the risk is small, but procedures exist so that the safe order becomes a habit that carries into production. Methodical step-by-step comparison — old list against new list, one line at a time — is the reliable technique here, and it is the same technique you use when you verify the state of IT assets against their records.

**Question 4 (moderate) — Prioritisation on a busy morning**

It is 9:15 on Tuesday morning. Four items are waiting for you:

1. A user has emailed you directly reporting that the document upload feature has stopped working since last night's release. No incident ticket exists yet.
2. Your post-release analysis report for last night's release is due to your manager by the end of the day.
3. A change request you documented is on the agenda for the change advisory board at 2pm, and the change and release manager has asked you to add the missing back-out plan before the meeting.
4. The CMDB record for a decommissioned test server still shows it as live; you noticed this yesterday.

Which sequencing is most defensible?

- A) 1, 3, 2, 4 — register the incident, then complete the CAB paperwork, then the report, then the CMDB fix
- B) 2, 1, 3, 4 — the report has today's deadline, so do it first
- C) 3, 1, 2, 4 — the CAB meeting is the most senior audience, so prepare for it first
- D) 4, 1, 3, 2 — CMDB accuracy is the foundation of everything, so fix it first

**Correct answer: A**

**Explanation:** Work through impact and urgency together. Item 1 is a live service problem affecting users right now, possibly caused by the very release you are analysing — and no incident ticket exists, so nothing will happen until someone registers it. Your incident management skill says exactly what to do: identify and register the incident, gather the required information, and allocate it to the appropriate channel. That takes minutes and unblocks the whole resolution process, so it comes first. Item 3 has a hard deadline at 2pm and blocks a governance decision, so it comes next. Item 2 is due by end of day — important, and conveniently the incident you just registered may become a key finding in it — but it can follow the 2pm deadline. Item 4 matters for data accuracy but a decommissioned test server marked as live is low risk and can wait until today's deadlines are met. Option B confuses "due today" with "most urgent this minute"; option C prioritises by seniority of audience rather than by impact; option D treats an important background task as an emergency. Notice the pattern: quick actions that unblock other people (registering the incident) often deserve first place even when bigger tasks loom.

**Question 5 (moderate) — Logical deduction about release scheduling**

Your release calendar has these rules: (i) releases to the payments service may only happen in the Tuesday or Thursday evening windows; (ii) a release cannot be deployed until its change request has been approved at the weekly change advisory board, which meets on Wednesday afternoons; (iii) after approval, the DevOps team needs one full working day to prepare the deployment pipeline. A change request for the payments service is submitted on Monday and is expected to be approved at the next board. What is the earliest window in which the release can be deployed?

- A) Tuesday evening the same week
- B) Thursday evening the same week
- C) Tuesday evening the following week
- D) Thursday evening the following week

**Correct answer: B**

**Explanation:** Work forwards through the rules. The request is submitted Monday; the board meets Wednesday afternoon, so approval arrives Wednesday. Rule (iii) then requires one full working day of pipeline preparation — that day is Thursday. Can the release go out Thursday evening? Yes: Thursday is a permitted window for payments (rule i), and by Thursday evening the full working day of preparation (Thursday's working day) is complete. Tuesday evening the same week fails because it is before approval. The following week's windows are permissible but not the earliest. A common error is to add the preparation day and conclude Friday is the earliest ready date, pushing the release to the next Tuesday — but "one full working day after Wednesday afternoon approval" is satisfied by close of Thursday, and the evening window sits after the working day ends. In the test, draw a quick timeline on your scratch paper; in your real job, this is exactly the reasoning you use when you set the plan for upcoming changes and coordinate with DevOps colleagues on pipeline readiness.

**Question 6 (moderate) — Error checking CMDB records against a scan**

An automated discovery scan reports four servers in the web tier: WEB01 (running operating system version 8), WEB02 (version 8), WEB03 (version 9), WEB04 (version 8). The CMDB records for the web tier read:

| CMDB record | Recorded OS version | Recorded status |
|---|---|---|
| WEB01 | 8 | Live |
| WEB02 | 7 | Live |
| WEB03 | 9 | Live |
| WEB05 | 8 | Live |

Assuming the scan is accurate, how many separate discrepancies are there between the scan and the CMDB?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: C**

**Explanation:** Compare systematically, item by item. WEB01: scan says version 8, CMDB says 8 — match, no discrepancy. WEB02: scan says version 8, CMDB says 7 — discrepancy one (a wrong attribute value). WEB03: scan says 9, CMDB says 9 — match. WEB04: present in the scan but has no CMDB record at all — discrepancy two (a missing record). WEB05: present in the CMDB as live but absent from the scan — discrepancy three (a record for something that does not appear to exist, sometimes called a ghost record). Total: three. The tempting mistake is to treat WEB04 and WEB05 as a single "mismatch" — perhaps someone mistyped the name — and answer B. That may well turn out to be the root cause, but the question asks how many discrepancies exist between the two sources as they stand, and there are three: one wrong value, one missing record, one unverified record. This mirrors your real duty to verify the location and state of IT assets: first record every discrepancy accurately, then investigate causes. Merging discrepancies too early can hide a real problem — WEB04 and WEB05 might genuinely be two different machines.

**Question 7 (moderate) — Pattern recognition in release outcomes**

Reviewing six months of post-release analysis, you tabulate the outcomes of 24 releases. The 6 failed releases were: release 3 (Friday, payments service), release 7 (Friday, document service), release 11 (Tuesday, payments service), release 15 (Friday, notifications service), release 19 (Friday, payments service), release 22 (Friday, case service). The 18 successful releases were spread across Tuesdays, Wednesdays and Thursdays, with two successes on Fridays. Which pattern is best supported by this data?

- A) The payments service causes most release failures.
- B) Friday releases fail disproportionately often.
- C) Releases fail more often as the year goes on.
- D) Tuesday is the safest release day.

**Correct answer: B**

**Explanation:** Test each candidate pattern against the data. Failures by day: five of the six failures happened on a Friday, and only two Friday releases succeeded — so five of seven Friday releases failed (about 71%), against one failure in seventeen non-Friday releases (about 6%). That is a strong, consistent pattern. Failures by service: payments appears in three of six failures, but payments also failed on a Tuesday and other services failed too, so the service pattern is weaker and mixed. Option C: the failure numbers (3, 7, 11, 15, 19, 22) are spread fairly evenly across the sequence, showing no worsening trend. Option D: Tuesday had a failure (release 11), so it cannot be called safe on this evidence, and the data does not compare Tuesday against Wednesday and Thursday in any detail. The strongest supported statement is B. This is post-release analysis exactly as your role describes it: finding the signal (a risky release day, perhaps because fewer support staff are available before the weekend) that should change your plan for upcoming changes — for example, proposing that releases move away from Fridays.

**Question 8 (moderate) — Applied problem solving during a rollout**

You are rolling out a software update to 200 branch office machines in batches of 50 per evening. After batch one, 46 machines updated successfully and 4 failed with the same error code. Your procedure says a batch failure rate above 5% requires you to pause the rollout and investigate. What should you do next?

- A) Continue with batch two — 4 failures out of 200 machines is only 2%.
- B) Pause the rollout — 4 failures out of 50 machines is 8%, which is above the 5% threshold, and investigate the common error code.
- C) Retry the 4 failed machines immediately and continue if at least 2 succeed.
- D) Abandon the rollout and revert the 46 successful machines.

**Correct answer: B**

**Explanation:** The threshold in the procedure applies to the batch: 4 failures out of the 50 machines attempted is 4 ÷ 50 = 8%, which exceeds 5%. Option A makes a subtle but important error — it divides by the total planned population (200) rather than the machines actually attempted (50). Only 50 machines have been through the process, so only 50 can tell you anything about the failure rate. Option C invents a rule that appears nowhere in the procedure, and retrying without investigating wastes the most valuable clue you have: all four failures share the same error code, which strongly suggests a single common cause that batch two would likely hit as well. Option D is disproportionate — 46 machines updated successfully, and nothing suggests the update itself is harmful. The disciplined response is to follow the documented procedure (pause), then apply your problem management skill: investigate the shared error code, understand whether the problem is operational (say, four machines with full disks) or something broader, contribute a remedy, and only then resume. Procedures like the 5% rule exist precisely so that the pause decision is made calmly by rule, not anxiously by gut feel, at 9pm.

**Question 9 (challenging) — Multi-constraint release scheduling**

You must schedule three releases — Alpha (A), Bravo (B), and Charlie (C) — across five weekday evenings, Monday to Friday, at most one release per evening. Constraints: (i) B depends on a configuration change delivered by A, and needs at least one clear evening between A and B for verification (so if A is Monday, B is Wednesday at the earliest); (ii) C must not be on the evening immediately after any other release, because the support team needs a quiet evening after each release before starting another with reduced cover — but C may share no such restriction looking forwards; (iii) the DevOps engineer needed for A is only available Monday and Tuesday; (iv) Friday is reserved for emergency changes only. On which evening must B take place?

- A) Tuesday
- B) Wednesday
- C) Thursday
- D) It cannot be scheduled within the constraints.

**Correct answer: C**

**Explanation:** Work through the constraints one at a time. Rule (iv) removes Friday for all three releases, leaving Monday to Thursday. Rule (iii) puts A on Monday or Tuesday. Try A on Monday: rule (i) requires a clear evening between A and B, so B is Wednesday or Thursday. C must fit on a remaining evening such that it is not immediately after another release (rule ii). If B is Wednesday, the remaining evenings for C are Tuesday and Thursday: Tuesday is immediately after Monday's A — not allowed; Thursday is immediately after Wednesday's B — not allowed. So B on Wednesday fails. If B is Thursday, C can take Wednesday only if Wednesday is not immediately after a release — Tuesday would need to be empty, and it is, since A is Monday and B is Thursday. Wednesday immediately follows Tuesday (empty), so C on Wednesday is allowed... but check again: is Wednesday immediately after Monday? No — "immediately after" means the next evening, and the evening after Monday is Tuesday. So A Monday, C Wednesday, B Thursday satisfies everything? Check rule (i): A Monday, B Thursday — Tuesday and Wednesday lie between, at least one clear evening — satisfied. Check rule (ii) for C: Wednesday's predecessor Tuesday has no release — satisfied. Valid. Now try A on Tuesday: B needs a clear evening, so B is Thursday at the earliest (Wednesday would be immediately after... no — rule (i) needs one clear evening between, so A Tuesday means B Thursday). C must then fit on Monday or Wednesday: Wednesday is immediately after Tuesday's A — not allowed; Monday precedes everything and follows nothing — allowed. So A Tuesday, C Monday, B Thursday is also valid. In every valid arrangement, B lands on Thursday. The answer is C) Thursday. The technique — enumerate the options systematically, eliminate what breaks a rule, and see what survives in all cases — is exactly how you build a real release calendar around dependency rules, staff availability, and protected windows.

**Question 10 (challenging) — Deduction from post-release evidence**

The morning after a release that changed three components — the web front end, the search index, and the payment connector — users report that searching works but every payment attempt fails. Overnight monitoring shows: the web front end served all pages normally; the search index rebuilt successfully at 2am; the payment connector logged "certificate not found" errors starting at 1:30am, which is when the release deployed it. The payment provider confirms their systems were healthy all night. Which conclusion is best supported?

- A) The release's payment connector change is the most likely cause, and the certificate error is the lead to investigate.
- B) The payment provider caused the failure and is concealing it.
- C) The search index rebuild interfered with payments.
- D) The web front end is the most likely cause because users see the failure there.

**Correct answer: A**

**Explanation:** Reason by elimination and by timing. The failure began at 1:30am, exactly when the payment connector was deployed, and the connector is logging a specific, plausible error — a missing certificate, which commonly happens when a deployment package omits a credential file or points at the wrong certificate store. The provider reports healthy systems and you have no evidence against that, so B asserts far more than the facts support. The search rebuild finished successfully and search works, and no evidence links the index to payments, so C is speculation. D confuses where users see a failure with where the failure originates — the front end is faithfully displaying an error that arises deeper in the chain, and its own logs are clean. Option A follows the evidence: correlation in time with the deployment, plus a specific error message, makes the connector the strongest lead — while the word "most likely" keeps appropriate humility, because investigation could still surprise you. This is your problem management skill in action: understanding the level of the problem (operational, in this case), following evidence rather than blame, and knowing that "the component we changed, logging errors since the moment we changed it" is where a sensible investigation starts.

**Question 11 (challenging) — Procedure logic with branching conditions**

Your back-out procedure states: "If production smoke tests fail after deployment, first retry the smoke tests once. If they fail again, check whether any users have submitted data through the new version. If no user data has been submitted, restore the backup taken before deployment. If user data has been submitted, do not restore the backup; instead escalate to the change and release manager and keep the new version running." Last night's deployment finished at 11pm. Smoke tests failed at 11:10pm and again on retry at 11:20pm. The logs show one user submitted a form through the new version at 11:15pm. According to the procedure, what should the on-call analyst have done?

- A) Restored the backup, because the smoke tests failed twice.
- B) Retried the smoke tests a third time before deciding.
- C) Escalated to the change and release manager and kept the new version running.
- D) Restored the backup but exported the user's form first.

**Correct answer: C**

**Explanation:** Follow the branches exactly as written. Smoke tests failed at 11:10pm — the procedure says retry once. The retry at 11:20pm also failed — the procedure now says check for user data submitted through the new version. The logs show a submission at 11:15pm, which is after deployment and through the new version, so user data exists. The procedure's instruction for that branch is explicit: do not restore the backup; escalate and keep the new version running. Option A applies the "restore" branch while ignoring the user-data condition that switches the branch — restoring the pre-deployment backup would silently destroy the user's 11:15pm submission, which is exactly the harm the condition exists to prevent. Option B invents a third retry the procedure does not contain. Option D sounds pragmatic, and something like it may well be what the change and release manager decides — but the procedure deliberately reserves that judgement for the escalation point rather than the on-call analyst, because handling user data during an incident carries risks (completeness, integrity, data protection) that deserve a senior decision. Reading conditional procedures precisely — which branch applies, given these facts — is a core analyst skill, both in tests and at 11:20pm in real life. When you write procedures yourself, this question also shows why clear branch conditions matter: the person following them may be tired, stressed, and alone.

**Question 12 (challenging) — Integrated reasoning across artefacts**

You are preparing the plan for next month's changes. Three sources are in front of you. The release calendar shows the finance service has a protected freeze for the first week of the month (year-end processing). An email from a service designer says user research found that the new accessibility fix for the finance service "should reach users as early as possible in the month". A change request from DevOps proposes deploying the accessibility fix together with a database upgrade in a single combined release "to save a release window", and notes the database upgrade needs two evenings of preparation that can only start after year-end processing completes. What is the strongest recommendation for your plan?

- A) Schedule the combined release in week one — accessibility needs outweigh the freeze.
- B) Schedule the combined release in week three, after the freeze and the two evenings of preparation.
- C) Split the releases: deploy the accessibility fix alone in week two, and the database upgrade later once its preparation is complete.
- D) Delay both changes to the following month to avoid all risk.

**Correct answer: C**

**Explanation:** Lay out what each source demands. The freeze rules out week one entirely — option A breaches a protected window for the sake of speed, which is precisely what freezes exist to prevent. The user need pulls the accessibility fix as early as possible. The database upgrade cannot even begin preparation until after week one, needs two evenings, and only then can be scheduled — realistically week two at the earliest, more comfortably week three. The combined release forces the accessibility fix to wait for the slowest component: that is the hidden cost of "saving a release window". Splitting the release lets the accessibility fix go out in week two — the earliest week the freeze allows — while the database upgrade proceeds on its own timeline without pressure. Option B is orderly but makes users wait an extra week for an accessibility improvement for no user benefit, only for release-administration convenience. Option D avoids nothing except delivering value. Option C best reconciles all three sources, and it reflects two things your role summary asks of you: liaising with DevOps and service designers (you would explain the reasoning to both, and check DevOps are content to run two windows), and showing user focus — understanding that behind the change request is a user need, and the plan should serve the need, not just the calendar.

### Preparation tips

- **Practise with your own artefacts.** Spend ten minutes with a recent change request, release calendar, or CMDB extract and quiz yourself: what rule does this follow? What would break it? Which two records contradict each other? Real materials train the same muscles the test measures.
- **Draw timelines for scheduling questions.** Dependency and calendar questions become far easier when you sketch the days across a scrap of paper and place events on it. Do not try to hold five constraints in your head — externalise them.
- **Check options against the rule, not against your instinct.** For pattern and error-checking questions, restate the rule in your own words first, then test each option against it mechanically. Instinct tells you something looks odd; the rule tells you whether it is wrong.
- **Deduce only what must be true.** For logic questions, the correct answer is often the cautious one — "either A or B" rather than "definitely A". If an option adds information the question never gave you, it is almost certainly wrong.
- **Do the untimed practice first, then add the clock.** Build accuracy before speed. When you do practise against time, note which question types slow you down and give those extra untimed practice.
- **Rest and set-up matter.** Take the real test somewhere quiet, on a reliable connection, with scrap paper ready and notifications silenced. A calm start is worth several marks.
- **Use the pre-test practice questions.** Nearly every platform offers ungraded warm-up questions. Always take them — they cost nothing and settle your nerves.

### Common pitfalls to avoid

- **Racing the clock.** Most candidates lose more marks to careless speed than to slowness. If the test is adaptive, harder questions mean you are doing well — do not panic and speed up.
- **Answering from job experience instead of the question.** Sometimes the scenario simplifies reality. Answer from the rules and facts given in the question, even if your organisation does things differently.
- **Dividing by the wrong base.** As in the rollout question above, rates and percentages must use the population actually involved, not the total planned population. Ask yourself: "out of what?"
- **Merging separate discrepancies.** When error-checking, count each inconsistency on its own first; theorise about shared causes second. Jumping to "it's probably one typo" hides real findings.
- **Choosing the dramatic option.** In problem-solving questions, wholesale rollbacks and abandonments are rarely the best answer when a targeted pause-and-investigate is available. The same is true at work.
- **Ignoring stated thresholds and branches.** If the question gives you a procedure with conditions, follow the conditions exactly. The test is checking whether you read carefully, not whether you can improvise well.
- **Letting one hard question shake you.** Mark your best guess, move on, and reset. One question rarely decides an outcome; a rattled ten minutes can.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how confidently and accurately you work with the numbers your role genuinely produces: change volumes, release success rates, incident counts, availability percentages, capacity figures, and the tables and simple charts they appear in. It is not a mathematics exam. You will not need algebra beyond simple rearrangement, and you will never need anything more advanced than percentages, ratios, averages, rates, and reading data tables carefully. What the test rewards is care: choosing the right numbers, doing the right operation, and sense-checking the result.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions. Each question usually presents a small table, chart, or short scenario with figures, followed by four or five answer options. An on-screen calculator is usually allowed — and you should use it, because the test measures reasoning, not mental arithmetic. As with cognitive tests, many platforms adapt difficulty to your performance, and employers typically see accuracy and speed separately. Most people do not finish every question, and that is normal.

Why do employers use numeric reasoning tests for a change and release analyst? Because your role runs on operational numbers. When you undertake analysis after a release, you are computing success rates and comparing them to previous releases. When you set the plan for upcoming changes, you are counting change requests, estimating durations, and checking they fit the available windows. When you explain availability and capacity management processes, you are talking about percentages of uptime and headroom before a threshold. When you help maintain the CMDB, audits of its accuracy come back to you as sample percentages. An analyst who misreads a table or divides by the wrong number can pause a healthy rollout — or worse, fail to pause an unhealthy one. The good news: every one of these techniques is learnable, and the worked examples below show each calculation step by step.

A quiet word of reassurance: many capable people feel anxious about numeric tests, often because of memories of school mathematics. Workplace numeric reasoning is different — it is closer to careful reading than to algebra. If you can find the right two numbers in a table and know whether to divide, multiply, or subtract, you can do well. Practice removes most of the anxiety, because familiarity is what turns "a maths test" into "the same calculations I do at work anyway".

### How this assessment maps to your role

The numeric skills tested map directly to the named skills in your role summary:

- **Percentages and rates** map to your **Change management** and post-release analysis duties: release success rates, failure rates against thresholds, and month-on-month changes in change request volumes are all percentage work. They also underpin **Availability and capacity management**, where you explain availability figures such as 99.5% and what they mean in real minutes of downtime.
- **Averages and weighted averages** map to your **Incident management** skill: average incidents per day, average resolution effort, and correctly combining figures from teams of different sizes are everyday operational analysis.
- **Ratios and proportions** map to your **Asset and configuration management** skill: sampling CMDB records for an accuracy audit and scaling the result to the whole database is proportional reasoning, as is splitting change volumes across categories.
- **Reading tables and identifying trends** maps to your duty to undertake analysis after release and set the plan for upcoming changes: quarterly change volume tables, growth trends in requests, and capacity projections all require you to extract the right figures and project them sensibly forwards. Your **Continuity management** and **Availability and capacity management** knowledge both rest on being able to read this kind of data correctly.
- **Time and duration arithmetic** maps to your core duty of planning and rolling out software: fitting deployments, smoke tests, and back-out plans inside release windows is addition and subtraction with consequences.

### Practice questions

**Question 1 (easy) — Release success rate**

Last month your team implemented 40 changes. 34 were successful and 6 failed or were backed out. What was the change success rate?

- A) 80%
- B) 85%
- C) 88%
- D) 90%

**Correct answer: B**

**Explanation:** Success rate = successful changes ÷ total changes × 100. Step 1: 34 ÷ 40 = 0.85. Step 2: 0.85 × 100 = 85%. A quick sense-check: 6 failures out of 40 is 6 ÷ 40 = 15%, and 100% − 15% = 85%, which confirms the answer two ways. This is the single most common figure in post-release analysis, and it is worth being able to produce it almost automatically. Notice the base is 40 — all changes attempted — not some larger number of changes planned or requested. Choosing the right base is the heart of percentage work.

**Question 2 (easy) — Average incidents per day**

In the five working days after a major release, the service desk registered the following numbers of release-related incidents: Monday 12, Tuesday 8, Wednesday 15, Thursday 9, Friday 6. What was the average (mean) number of release-related incidents per day?

- A) 9
- B) 10
- C) 11
- D) 12

**Correct answer: B**

**Explanation:** Mean = total ÷ number of days. Step 1: add the daily counts: 12 + 8 = 20; 20 + 15 = 35; 35 + 9 = 44; 44 + 6 = 50. Step 2: divide by the number of days: 50 ÷ 5 = 10. Sense-check: the values range from 6 to 15, and 10 sits comfortably inside that range — an average outside the range of the data always means an arithmetic slip. In your post-release report, you might use this average as a baseline: if the previous release averaged 6 incidents per day, this release generated markedly more, which is a finding worth investigating. Adding in stages, as shown, reduces slips under time pressure.

**Question 3 (easy) — Ratio of change categories**

Your organisation's changes last quarter split into standard, normal, and emergency categories in the ratio 7 : 4 : 1. There were 120 changes in total. How many were emergency changes?

- A) 8
- B) 10
- C) 12
- D) 17

**Correct answer: B**

**Explanation:** Step 1: add the ratio parts: 7 + 4 + 1 = 12 parts. Step 2: find the size of one part: 120 ÷ 12 = 10 changes per part. Step 3: emergency changes are 1 part: 1 × 10 = 10. Sense-check the whole split: standard = 7 × 10 = 70, normal = 4 × 10 = 40, emergency = 10, and 70 + 40 + 10 = 120, which matches the total. Ratios like this appear whenever you summarise the change mix for the change advisory board. The emergency share matters operationally: a rising proportion of emergency changes often signals that planning is being bypassed, which is exactly the kind of pattern your analysis should surface.

**Question 4 (moderate) — Percentage change in failures**

In April, 15 changes failed. In May, 12 changes failed. By what percentage did the number of failed changes decrease from April to May?

- A) 3%
- B) 12.5%
- C) 20%
- D) 25%

**Correct answer: C**

**Explanation:** Percentage change = (difference ÷ original value) × 100, and the original value is always the earlier figure. Step 1: difference = 15 − 12 = 3. Step 2: divide by April's figure: 3 ÷ 15 = 0.2. Step 3: 0.2 × 100 = 20%. The trap in option D comes from dividing by the later figure: 3 ÷ 12 = 25% — a very common error. Option A mistakes the absolute difference (3 changes) for a percentage. When you report improvement in a post-release or monthly summary, the direction of comparison matters: "failures fell 20% from April" uses April as the base. If someone later says "so a 20% rise would take us back to 15", gently check their arithmetic — 20% up from 12 is 14.4, not 15, because the base has changed. Being precise about bases makes your analysis trustworthy.

**Question 5 (moderate) — Availability percentage**

The document service is expected to be available 24 hours a day. In a 30-day month it suffered two outages: one of 90 minutes and one of 126 minutes. What was the service's availability for the month?

- A) 99.0%
- B) 99.3%
- C) 99.5%
- D) 99.8%

**Correct answer: C**

**Explanation:** Step 1: total minutes in the month = 30 days × 24 hours × 60 minutes = 43,200 minutes. Step 2: total downtime = 90 + 126 = 216 minutes. Step 3: downtime as a fraction = 216 ÷ 43,200 = 0.005, which is 0.5%. Step 4: availability = 100% − 0.5% = 99.5%. This calculation sits at the centre of your ability to explain availability and capacity management processes. It is also worth internalising the reverse direction: a target like "99.5% availability" sounds close to perfect, but it permits 216 minutes — over three and a half hours — of downtime a month. When you schedule releases, the downtime a deployment causes counts against figures like this, which is one reason release windows sit in quiet hours.

**Question 6 (moderate) — Reading a change volume table**

The quarterly change report shows:

| Category | Q1 changes | Q2 changes |
|---|---|---|
| Standard | 240 | 264 |
| Normal | 80 | 96 |
| Emergency | 20 | 27 |

Which category grew by the largest percentage from Q1 to Q2?

- A) Standard
- B) Normal
- C) Emergency
- D) They all grew by the same percentage

**Correct answer: C**

**Explanation:** Compute each growth rate with the Q1 figure as the base. Standard: increase = 264 − 240 = 24; 24 ÷ 240 = 0.10 = 10%. Normal: increase = 96 − 80 = 16; 16 ÷ 80 = 0.20 = 20%. Emergency: increase = 27 − 20 = 7; 7 ÷ 20 = 0.35 = 35%. Emergency grew fastest in percentage terms, even though its absolute increase (7 changes) is the smallest. This distinction between absolute and percentage growth is one of the most useful habits in operational reporting: standard changes added the most volume (24), but emergency changes growing 35% in a quarter is the finding that should reach the change advisory board, because emergency changes bypass normal planning and carry more risk. A table that only showed absolute increases would bury exactly the signal that matters.

**Question 7 (moderate) — Fitting a deployment into a release window**

Tonight's release window runs from 6:00pm to 10:00pm. The deployment takes 90 minutes, the production smoke tests take 45 minutes, and — if the smoke tests fail — the back-out procedure takes 60 minutes and must be fully complete by the end of the window. What is the latest time the deployment can start?

- A) 6:00pm
- B) 6:25pm
- C) 6:45pm
- D) 7:45pm

**Correct answer: C**

**Explanation:** Plan for the worst case, because the window must contain it. Step 1: worst-case duration = deployment + smoke tests + back-out = 90 + 45 + 60 = 195 minutes. Step 2: convert to hours and minutes: 195 minutes = 3 hours 15 minutes. Step 3: subtract from the window end: 10:00pm − 3 hours 15 minutes = 6:45pm. Starting at 6:45pm means a failed smoke test at 9:00pm still leaves exactly 60 minutes to back out by 10:00pm. Option D uses only the happy path (90 + 45 = 135 minutes), which is the classic planning error: a release plan that only fits if nothing goes wrong is not a plan, it is a hope. When you design distribution and installation procedures, always timetable the back-out — this small calculation is one of the most genuinely protective habits in release work.

**Question 8 (moderate) — Weighted average success rate**

Two teams deployed changes last month. Team A implemented 60 changes with a 90% success rate. Team B implemented 40 changes with an 80% success rate. What was the overall success rate across both teams?

- A) 84%
- B) 85%
- C) 86%
- D) 88%

**Correct answer: C**

**Explanation:** You cannot simply average 90% and 80% to get 85%, because the teams did different amounts of work. Step 1: Team A successes = 90% of 60 = 0.9 × 60 = 54. Step 2: Team B successes = 80% of 40 = 0.8 × 40 = 32. Step 3: total successes = 54 + 32 = 86. Step 4: total changes = 60 + 40 = 100. Step 5: overall rate = 86 ÷ 100 = 86%. The unweighted average (option B) is wrong whenever group sizes differ — here the answer sits closer to Team A's rate because Team A did more of the work. This exact calculation appears when you consolidate figures for a monthly change report, and getting it right protects you from a subtle unfairness too: quoting a simple average would make the overall performance look worse than it was, understating the contribution of the larger, more successful team.

**Question 9 (challenging) — CMDB accuracy audit**

To check CMDB quality, you audit a random sample of 250 records out of the 5,000 in the database. In the sample, 235 records are fully accurate and 15 contain at least one error. Based on this sample, approximately how many records in the whole CMDB would you expect to contain at least one error?

- A) 150
- B) 235
- C) 300
- D) 750

**Correct answer: C**

**Explanation:** Step 1: find the error rate in the sample: 15 ÷ 250 = 0.06, which is 6%. Step 2: apply that rate to the whole database: 6% of 5,000 = 0.06 × 5,000 = 300. An equivalent route uses scaling: the database is 5,000 ÷ 250 = 20 times the sample, and 15 × 20 = 300. Option A halves the true figure (a 3% slip), option B confuses the count of accurate sampled records with an answer, and option D would follow from misreading 15 as 15%. Two professional footnotes worth knowing: first, this is an estimate — a different random sample would give a slightly different figure, so report it as "around 300" rather than exactly 300; second, the accuracy rate here is 94%, and whether that is good news depends on the target your change and release manager has set. Sampling like this is how real CMDB audits work, because checking all 5,000 records by hand is rarely feasible — which makes proportional reasoning a core tool for your asset and configuration management skill.

**Question 10 (challenging) — Forecasting change request volumes**

In January your team received 120 change requests, and the monthly volume has been growing steadily by 15 requests each month (February 135, March 150, and so on). Your team can process at most 200 change requests per month. If the trend continues, in which month will the volume first exceed the team's capacity?

- A) May
- B) June
- C) July
- D) August

**Correct answer: C**

**Explanation:** The volume in a given month = 120 + (15 × number of months after January). Work forward: February = 135, March = 150, April = 165, May = 180, June = 195, July = 210. June's 195 is still within the 200 capacity; July's 210 is the first month above it. Alternatively, solve directly: you need 120 + 15n > 200, so 15n > 80, so n > 5.33; the first whole month is n = 6, which is six months after January — July. Option B is the classic off-by-one error: June reaches 195, close to capacity but not exceeding it. In real planning, of course, you would raise the flag well before July — running at 97.5% of capacity in June leaves no room for an emergency spike — and that is precisely the kind of forward-looking finding your role's planning duty exists to produce. The test rewards the exact arithmetic; the job rewards acting on it early.

**Question 11 (challenging) — Rework as a share of total effort**

Last quarter your team implemented 250 changes. Each change takes 2 hours of implementation effort. 8% of the changes failed, and each failed change required an additional 3 hours of rework on top of its original effort. To one decimal place, what percentage of the team's total change effort was spent on rework?

- A) 8.0%
- B) 10.7%
- C) 12.0%
- D) 24.0%

**Correct answer: B**

**Explanation:** Step 1: count the failed changes: 8% of 250 = 0.08 × 250 = 20 changes. Step 2: rework hours = 20 × 3 = 60 hours. Step 3: original implementation hours = 250 × 2 = 500 hours. Step 4: total effort = 500 + 60 = 560 hours. Step 5: rework share = 60 ÷ 560 = 0.10714… ≈ 10.7%. Option A wrongly assumes the rework share equals the failure rate, but rework hours per failure (3) differ from implementation hours per change (2), so the shares differ too. Option C divides rework by original hours only (60 ÷ 500 = 12%) instead of by the true total. This is a genuinely useful figure in post-release analysis: it converts a failure rate into a cost the whole team feels, and it strengthens the case for preventative measures — if better pre-release checks halved failures, they would recover about 30 hours a quarter. Turning percentages into hours is often what makes your analysis persuasive.

**Question 12 (challenging) — Capacity headroom projection**

A database server has 1,000 GB of storage, of which 600 GB is currently used. Usage is growing by a steady 25 GB per month. Your capacity management process raises an alert when usage reaches 90% of total storage. If the growth continues unchanged, in how many months will the alert threshold be reached?

- A) 10 months
- B) 12 months
- C) 14 months
- D) 16 months

**Correct answer: B**

**Explanation:** Step 1: find the alert threshold in GB: 90% of 1,000 = 900 GB. Step 2: find the headroom between now and the threshold: 900 − 600 = 300 GB. Step 3: divide headroom by the monthly growth: 300 ÷ 25 = 12 months. Option D (16 months) comes from using the full 1,000 GB instead of the 90% threshold — but capacity processes alert early on purpose, because fixing storage takes lead time and systems misbehave long before they are literally full. Option A might come from misreading the used figure. This is the arithmetic behind your availability and capacity management knowledge: capacity work is essentially "headroom ÷ growth rate = time to act", applied to storage, transaction volumes, or licence counts. When you can produce this figure, you can also explain to a service designer or DevOps colleague why a change that doubles data growth needs a capacity conversation before it is scheduled — turning a calculation into exactly the kind of cross-team liaison your role asks of you.

### Preparation tips

- **Rehearse the four core moves.** Nearly every workplace numeric question is one of: percentage of a total, percentage change between two figures, weighted average, or rate × time. Practise each until the method is automatic, and the test becomes recognition rather than invention.
- **Always ask "out of what?"** Before dividing, name the base out loud: out of changes attempted, out of the sample, out of the earlier month. Most numeric errors are right arithmetic on the wrong base.
- **Write the steps down.** Even with an on-screen calculator, jot intermediate results (totals, differences, one-part values) on scrap paper. It prevents re-keying errors and lets you sense-check.
- **Sense-check every answer.** Averages must sit inside the range of the data; availability should be near 100%; a small sample error rate should scale to a modest full-population count. If a result feels absurd, it usually is.
- **Practise reading tables before calculating.** Half the skill is extracting the right two numbers. When you practise, cover the options and ask first: which cells do I actually need?
- **Use your own operational reports.** Take last month's change report or availability figures and recompute the headline numbers yourself. Practising on real data builds both speed and job knowledge at once.
- **Mind units and time periods.** Minutes versus hours, months versus quarters, per-batch versus per-rollout. Convert to one unit early and label it.

### Common pitfalls to avoid

- **Dividing by the wrong base.** The single most common error: using the later month for percentage change, the planned total instead of the attempted total, or original hours instead of total hours. Name the base every time.
- **Averaging percentages from different-sized groups.** 90% and 80% do not average to 85% unless the groups are equal. Always go back to raw counts.
- **Off-by-one errors in projections.** "First month exceeding capacity" is not the month that reaches it. Read comparison words — exceed, reach, at least, more than — with care.
- **Planning only the happy path.** In time questions, include the back-out or contingency duration when the question says it must fit. The same habit protects your real release windows.
- **Confusing absolute and percentage growth.** The biggest raw increase and the fastest percentage growth are often different rows of the table. Check which one the question asks for.
- **Rounding too early.** Keep full precision through intermediate steps and round only the final answer, or small errors compound.
- **Panicking at multi-step questions.** Hard numeric questions are just several easy steps in a row. Write step 1, do it, then look for step 2. You never need the whole path in your head at once.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and reason about written material of the kind your role handles every day: change policy extracts, release procedure documents, emails from DevOps colleagues and service designers, incident notices, service standards, and user stories. The most common question style gives you a short passage and a statement, then asks whether the statement is **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage gives you too little information to decide either way). Other question styles ask you to identify the main point of a passage, draw a safe inference, spot an unstated assumption, or judge which of several rewrites communicates most clearly.

The typical format is an online, timed test lasting 15 to 25 minutes with 15 to 30 questions. The golden rule, which cannot be repeated too often: answer only from the passage. You may know from your own workplace that a statement is true in real life — but if the passage in front of you does not say it, the answer is "Cannot say". The test deliberately measures your ability to separate what a text actually states from what you assume, expect, or remember. As with the other assessments, scoring is against a norm group at your level, adaptive difficulty is common, and unfinished questions are normal.

Why do employers use verbal reasoning tests for a change and release analyst? Because your written accuracy carries operational weight. When you document a change request, the change advisory board decides based on exactly what you wrote — not what you meant. When you read a change freeze policy, the difference between "must" and "should" determines whether a deployment is permitted. When you carry out a procedure at 11pm, you follow the words on the page, so you need the skill of reading conditions precisely — and, when you write procedures for others, of writing them precisely too. And when you liaise with DevOps and service designers, you translate between technical detail and user needs, which demands both careful reading and clear writing. A verbal reasoning test compresses all of that into short, sharp exercises.

If English essays were never your favourite thing at school, take heart: verbal reasoning is not about literary style or vocabulary. It is about disciplined, literal, careful reading — a skill much closer to checking a config file than to writing poetry, and one that improves quickly with practice.

### How this assessment maps to your role

The verbal skills tested map directly to the named skills in your role summary:

- **Precise comprehension of rules and conditions** maps to your **Change management** skill: documenting change requests and actioning changes from change requests depends on reading approval conditions, freeze rules, and procedural branches exactly as written. It also supports your **Continuity management** knowledge, which requires you to explain the basic principles of continuity processes accurately rather than approximately.
- **True/False/Cannot-say discipline** maps to your **Asset and configuration management** skill: verifying the location and state of IT assets is exactly the practice of separating what is confirmed by evidence from what is merely assumed. A record is accurate, inaccurate, or unverified — the same three-way split the test uses.
- **Inference and assumption-spotting** maps to your **Problem management** skill: investigating problems means reading incident notes and reports, drawing conclusions the evidence genuinely supports, and noticing when a report quietly assumes something unproven.
- **Clear-writing judgement** maps to your **User focus** and **Community collaboration** skills: explaining the purpose of user stories, writing release communications that non-technical readers can follow, and contributing to the work of others all require you to recognise — and produce — writing that is plain, unambiguous, and organised for its reader.
- **Reading for the appropriate channel** maps to your **Incident management** and **Ownership and topic** skills: when you identify and register incidents, or pass a problem to your team, you first have to read a message accurately enough to route it correctly.

### Practice questions

For each True/False/Cannot-say question, judge the statement strictly against the passage.

**Passage 1 (for Questions 1–3)**

*Extract from the departmental change policy:* "All normal changes must be submitted to the change advisory board at least five working days before the proposed implementation date. Standard changes are pre-authorised and may be implemented without board review, provided they follow an approved template. Emergency changes may be implemented before board review, but must be reviewed retrospectively at the next board meeting. The board meets weekly. Changes submitted with incomplete back-out plans will be returned to the submitter without review."

**Question 1 (easy) — True/False/Cannot say**

Statement: "Standard changes do not require review by the change advisory board before implementation."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage states directly that standard changes "are pre-authorised and may be implemented without board review, provided they follow an approved template". The statement matches this: no board review is required before implementation. Note the care needed with the proviso — the exemption depends on following an approved template — but the statement as written claims only that standard changes do not require prior board review, which the passage supports. When a statement matches the passage's plain meaning, the answer is True even if the passage adds conditions the statement does not mention, so long as the statement does not contradict those conditions. This mirrors reading policy at work: standard changes are your bread and butter as an analyst, and knowing exactly what is pre-authorised keeps you fast without being careless.

**Question 2 (easy) — True/False/Cannot say**

Statement: "Emergency changes are exempt from review by the change advisory board."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says emergency changes "may be implemented before board review, but must be reviewed retrospectively at the next board meeting". So emergency changes are not exempt from review — the review still happens, just after implementation instead of before. The statement confuses "review happens later" with "no review happens", and the passage directly contradicts it, making the answer False. This is a distinction with real teeth in your job: an emergency change is a deferral of governance, not an escape from it, and part of your documentation duty is making sure the retrospective review actually has the change record it needs. In the test, watch for statements that quietly strengthen a passage's claim — "later" becoming "never", "may" becoming "must" — because strengthened claims are usually False or Cannot say.

**Question 3 (easy) — True/False/Cannot say**

Statement: "The change advisory board meets on Wednesdays."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage says the board "meets weekly" but never says on which day. You may work somewhere the board really does meet on Wednesdays — many do — but the passage neither confirms nor denies the day, so the answer is Cannot say. This is the discipline the whole test rests on: the difference between what a document states and what you happen to know or expect. It matters at work for the same reason. If you tell a DevOps colleague "the board meets Wednesdays" based on habit, and this quarter's schedule moved it, your five-working-day submission calculation could silently slip. Verify from the document; where the document is silent, say so.

**Passage 2 (for Questions 4–5)**

*Extract from the IT continuity procedure:* "In the event of a declared major incident affecting the primary data centre, services will be restored at the secondary site in priority order. Priority 1 services must be restored within four hours of declaration. Priority 2 services must be restored within twenty-four hours. The priority list is reviewed quarterly by service owners. Restoration at the secondary site uses the most recent overnight backup; data entered between the last backup and the incident may be lost. Release activity is suspended during a declared major incident, and any release in progress must be halted and assessed."

**Question 4 (moderate) — True/False/Cannot say**

Statement: "If a major incident is declared while a release is in progress, the release must be halted."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The final sentence states: "any release in progress must be halted and assessed". The statement is a direct match for the first half of that instruction, and adding "and assessed" in the passage does not weaken the statement's claim — the halt is still mandatory. So the answer is True. Notice how the question tests exactly the reading you would need in real time: if you were mid-deployment when a major incident was declared, this sentence is the one that tells you what to do, and "halt" comes before "assess". As the person who designs and carries out release procedures, you would also want your own runbooks to reference this continuity rule, so that the instruction reaches the person at the keyboard — a nice example of how your continuity management knowledge and your release duties connect.

**Question 5 (moderate) — Inference from the passage**

Based on Passage 2, which of the following is the safest inference?

- A) Priority 1 services are more important to the organisation than Priority 2 services.
- B) The secondary site has less capacity than the primary site.
- C) No data is ever lost during failover to the secondary site.
- D) Service owners never change the priority list.

**Correct answer: A**

**Explanation:** Inference questions ask which conclusion the passage best supports without stating it outright. The passage gives Priority 1 services a four-hour restoration target and Priority 2 services twenty-four hours; a restoration ordering by "priority", with much tighter targets for Priority 1, clearly implies those services matter more to the organisation — that is what the priority structure means. Option B may well be true in many real organisations, but nothing in the passage mentions capacity. Option C is contradicted: the passage explicitly warns that data entered since the last backup "may be lost". Option D over-reads the quarterly review the other way — a list that is "reviewed quarterly" could change at any review, and the passage certainly does not say it never changes. The safe inference is the one the text's own structure supports. At work, this is the skill of reading a procedure and correctly grasping its intent, so you can explain continuity principles to others — one of your named skills — without either exaggerating or understating what the procedure promises.

**Question 6 (moderate) — Must, should, and may**

Your release standards document contains these three sentences: (i) "Deployments to production **must** be performed from the approved pipeline." (ii) "Deployment scripts **should** be peer reviewed before first use." (iii) "Analysts **may** schedule standard changes in any approved window." A colleague deployed to production manually last night, using a script that had been peer reviewed, in an approved window. Which requirement, if any, was breached?

- A) Requirement (i) only
- B) Requirement (ii) only
- C) Requirements (i) and (iii)
- D) No requirement was breached

**Correct answer: A**

**Explanation:** In standards language, "must" marks a mandatory requirement, "should" marks a strong recommendation that permits justified exceptions, and "may" marks a permission. Check each: (i) requires production deployments to use the approved pipeline — a manual deployment breaches this mandatory requirement. (ii) recommends peer review before first use — the script was peer reviewed, so no issue, and even had it not been, "should" is not an absolute bar. (iii) grants permission about scheduling — permissions cannot be "breached" by using them, and the window was approved. So exactly one requirement was breached: (i). This vocabulary is load-bearing across government and industry standards (it follows the widely used RFC 2119 convention), and reading it precisely is part of your change management skill: when you document change requests or write procedures, choosing "must" versus "should" tells every future reader what is negotiable. Misreading them in someone else's document is how well-meaning people commit breaches politely.

**Question 7 (moderate) — Clear-writing judgement**

You must send a service notice to non-technical staff about tonight's release. Which version communicates most clearly?

- A) "Pursuant to change CHG-4471, the case management application will undergo scheduled maintenance activities during the designated release window, potentially impacting system availability for end users."
- B) "The case management system will be unavailable tonight between 8pm and 9pm while we install an update. Please save your work and log out before 8pm. It will work normally from 9pm."
- C) "Tonight we are deploying release 3.2.1 to the production environment via the blue-green pipeline, with a rollback checkpoint after smoke testing."
- D) "There may be some disruption to some systems at some point tonight due to essential works."

**Correct answer: B**

**Explanation:** Judge each version against its audience and purpose: non-technical staff need to know what is affected, when, and what to do. Option B gives exactly that, in plain words, with specific times and a clear action ("save your work and log out before 8pm"). Option A is officialese — "pursuant to", "designated release window", "potentially impacting" — that hides the two facts people need and gives no times or actions. Option C is accurate but written for the wrong audience: blue-green pipelines and smoke tests mean nothing to caseworkers and do not tell them what to do. Option D is plain but uselessly vague — "some disruption to some systems at some point" leaves readers unable to plan at all. Clear writing is specific, audience-appropriate, and action-oriented. This is your user focus skill applied to communication: behind every release notice is a user trying to get their work done, and your words are part of the service. It is also worth noticing that B quietly demonstrates good release practice — a defined window and a confident restoration time — which good communication tends to reveal and vague communication tends to hide.

**Passage 3 (for Questions 8–9)**

*User story from the service designer, with a note:* "As a caseworker, I need the document upload page to show a progress bar, so that I know my upload is working and do not refresh the page mid-upload. Note from the service designer: our research sessions showed that when uploads take more than a few seconds, many caseworkers refresh the page, which interrupts the upload and creates duplicate draft records. Support staff then spend time deleting duplicates. We believe a visible progress indicator will reduce refreshing. This change should be released before the winter peak if possible."

**Question 8 (moderate) — True/False/Cannot say**

Statement: "Caseworkers refreshing the page during uploads creates duplicate draft records."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The designer's note states that refreshing "interrupts the upload and creates duplicate draft records" — a direct statement of the causal link, based on their research sessions. The statement mirrors the passage, so it is True. Be careful to distinguish this from the next claim in the note: that a progress indicator "will reduce refreshing" is flagged as a belief ("we believe"), not an established fact. Passages often mix established findings with hopes and hypotheses, and the test — like your job — rewards noticing which is which. Understanding user stories, and the user needs behind them, is one of your named user focus skills: this story tells you not just what to build but why it matters operationally (support staff time spent deleting duplicates), which is exactly the impact information you would carry into a change request.

**Question 9 (challenging) — Identifying the unstated assumption**

The service designer's argument is, in outline: "Caseworkers refresh slow uploads, which creates duplicates; a progress bar will reduce refreshing; therefore the change will reduce duplicate records." Which unstated assumption does this argument most depend on?

- A) Caseworkers refresh pages because they lack feedback that the upload is progressing, rather than for some other reason.
- B) The winter peak will increase upload volumes.
- C) Support staff dislike deleting duplicate records.
- D) The progress bar will be technically easy to implement.

**Correct answer: A**

**Explanation:** An assumption is an unstated claim the argument needs in order to work. The argument moves from "caseworkers refresh" to "a progress bar will reduce refreshing" — that step only holds if the refreshing is caused by uncertainty about whether the upload is working. If caseworkers actually refresh for a different reason (say, the page appears frozen due to a performance bug, or they are trained to refresh by habit), a progress bar might change nothing. Option B is plausible context but the argument about duplicates works regardless of the peak. Option C is likely true but the argument depends on support time being spent, not on anyone's feelings. Option D concerns feasibility, not the logic linking the change to the benefit. Spotting load-bearing assumptions is a quietly powerful analyst skill: in post-release analysis, it is the difference between "we shipped the progress bar" and "we checked whether duplicate records actually fell". If they did not, option A's assumption is the first place to look — and saying so, kindly and factually, is a genuine contribution to the work of others.

**Question 10 (challenging) — Reconciling two documents**

Document 1, the release procedure, states: "The CMDB must be updated within one working day of any production deployment." Document 2, last week's audit report, states: "Of the fifteen production deployments sampled, four had CMDB updates recorded more than one working day after deployment, and one had no CMDB update recorded at all." Which statement is best supported by the two documents together?

- A) The release procedure is unrealistic and should be relaxed.
- B) In the sampled deployments, the procedure's CMDB requirement was not met in five cases.
- C) Two-thirds of all production deployments comply with the CMDB requirement.
- D) The team responsible has been careless.

**Correct answer: B**

**Explanation:** Combine the documents carefully. The procedure sets a requirement: update within one working day. The audit found four late updates and one missing update — five sampled deployments that did not meet the requirement (a missing update certainly does not meet a deadline). Option B states exactly that, and no more. Option A leaps from "the requirement was breached" to "the requirement is wrong" — a policy recommendation the documents do not support; breaches might equally indicate a tooling gap or a training need. Option C over-generalises: ten of fifteen sampled deployments complied, but the sample may not represent all deployments, and "two-thirds of all" claims more than the evidence shows — in a verbal test, generalising beyond the sample is a classic trap. Option D assigns blame the documents nowhere support. The disciplined reading is B: state what the evidence establishes, precisely, without extending it. This is also how a good analyst writes: audit findings that stick to what was found are the ones that survive challenge at the change advisory board.

**Question 11 (challenging) — Main point of a passage**

*Extract from a post-implementation review:* "Release 4.1 was deployed successfully within its window, and all smoke tests passed. However, in the following week the service desk logged a 40% increase in calls about the redesigned search screen. Most callers were not reporting faults: the search worked as specified, but users could not find the filter controls, which had moved. Training materials had not been updated to reflect the new layout, because the training team was not informed of the change. We recommend that the release checklist include notifying the training team for any change that alters a user-facing screen."

Which sentence best expresses the main point of the passage?

- A) Release 4.1 failed and should have been backed out.
- B) A technically successful release still caused user disruption because a communication step was missing, and the process should be amended to include it.
- C) Users dislike change and will always call the service desk after a release.
- D) The training team is responsible for the increase in service desk calls.

**Correct answer: B**

**Explanation:** The passage has a shape: technical success ("deployed successfully... smoke tests passed"), followed by an operational problem (call volumes up 40%), a diagnosis (the layout changed but training materials did not, because notification never happened), and a process recommendation (add the notification to the checklist). Option B captures that whole arc. Option A contradicts the passage — the release worked as specified, and nothing suggests a back-out was warranted. Option C turns one incident into a cynical universal law the passage never states. Option D misreads the diagnosis: the training team "was not informed", which locates the gap in the release process, not in the training team's conduct — blaming them inverts the passage's meaning. Finding the main point matters in your role because post-implementation reviews are exactly the documents you write and act on: the whole value of release 4.1's painful week is the checklist improvement at the end, and a reader who takes away A, C, or D would improve nothing. "Deployment success is not the same as release success" is a lesson worth keeping.

**Question 12 (challenging) — True/False/Cannot say with a subtle scope shift**

*Passage:* "Following January's incident, all changes to the payments service now require an additional security review before submission to the change advisory board. The security team aims to complete reviews within three working days. Since the new step was introduced, no payments change has been implemented late."

Statement: "The additional security review has not delayed any change to any service."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Read the scopes carefully. The passage is about the payments service: the new review applies to payments changes, and "no payments change has been implemented late" since it began. The statement claims something broader on one axis and subtly different on another: "any change to any service" extends beyond payments, and "has not delayed" is not the same as "was not implemented late" — a change could be delayed internally (waiting three days for review) yet still land on time against its planned date. Does the passage contradict the statement? No — it says nothing about other services or about internal delays. Does it support the statement? Also no — it only tells us about payments implementation dates. With neither support nor contradiction, the answer is Cannot say. This is the hardest and most valuable habit in verbal reasoning: statements that quietly widen the scope ("any service") or swap a nearby concept ("late" for "delayed") are the ones that catch confident readers. In your work, the same alertness protects your change records — "the release was on time" and "the release was not delayed" can both be true, both be false, or one of each, and precise wording is what keeps your reports honest.

### Preparation tips

- **Drill the True/False/Cannot-say distinction daily.** Take two sentences from any work document and write one statement the text supports, one it contradicts, and one it is silent about. Five minutes a day builds the reflex faster than long sessions.
- **Answer from the passage, never from your workplace.** Before choosing, ask: "where in the text is this supported or contradicted?" If you cannot point to the words, the answer is Cannot say.
- **Watch the strength of claims.** Circle words like all, never, always, only, must, may, some. Statements that strengthen the passage's claim are usually False or Cannot say; statements that soften it are often True.
- **Watch the scope of claims.** Note exactly who and what the passage covers — one service or all services, sampled deployments or all deployments. Scope-widening is the classic hard-question trap.
- **Read the question before re-reading the passage.** Skim the passage once for shape, read the statement, then hunt the relevant sentence. This is faster than memorising the passage.
- **Practise the must/should/may vocabulary.** Government and industry standards rely on it. Rewrite a paragraph of your own procedures using each word deliberately and note how the meaning shifts.
- **Read your own role's documents actively.** Change policies, continuity procedures, and post-implementation reviews are ideal practice texts — and reading them closely makes you better at the actual job while you prepare.

### Common pitfalls to avoid

- **Importing outside knowledge.** The most common error at every level: choosing True because the statement is true in your organisation. The test asks only what this passage supports.
- **Treating Cannot say as a weak answer.** Candidates under-use it, feeling they should "know". Cannot say is frequently the correct, disciplined answer — expect to use it often.
- **Missing negations and reversals.** "Not exempt from review" versus "exempt from review" — a single word flips the answer. Read statements twice, slowly, before deciding.
- **Confusing later with never, and delayed with late.** Near-synonyms are not synonyms. Hard questions turn on exactly these distinctions.
- **Choosing the answer that assigns blame.** In main-point and inference questions, options that blame a team or person usually over-reach the text — and mirror a habit worth avoiding in real post-incident writing too.
- **Over-reading recommendations as facts.** "We believe X will help" is a hypothesis; "X caused Y" is a finding. Keep them separate in tests and in your own reports.
- **Spending too long on one passage.** If a statement resists you after two careful readings, choose your best answer and move on. Verbal tests reward steady discipline across many questions, not perfection on one.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks you to choose how you would respond. Unlike the other assessments in this guide, it has no arithmetic and no passages — instead, it measures your professional judgement: how you balance user needs, process discipline, honesty, teamwork, and knowing when to act yourself versus when to escalate. Question formats vary: the most common ask you to pick the **most effective** response from four options; others ask for the **least effective** response, or ask you to rate each response's effectiveness on a scale, or to rank all four.

The typical format is an online test of 20 to 40 minutes with 10 to 20 scenarios, usually untimed or generously timed, because employers want your considered judgement rather than your reflexes. There are no trick questions, but there are carefully constructed options: alongside the best response you will usually find one that is almost right but skips a step, one that avoids the problem, and one that overreacts. Scoring compares your choices against a key agreed by experienced practitioners and calibrated to the role's level — which matters for you, because at analyst level the "right" answer often involves doing the immediate safe thing and then involving your change and release manager, where at senior levels the right answer might be to decide alone. You are not being tested on whether you can do a manager's job; you are being tested on whether you show good judgement in yours.

Why do employers use situational judgement tests for a change and release analyst? Because your role sits at a busy junction: developers want changes released quickly, users want stability, procedures impose discipline, and unexpected failures demand calm decisions — sometimes late in the evening when you are the only person watching the deployment. Technical skill alone does not predict who handles that junction well. Judgement does: knowing that an unauthorised deployment must be raised even when it is awkward, that a failing rollout is a moment for procedure rather than improvisation, that user impact belongs in every decision, and that asking for help early is a strength. These are exactly the behaviours — user focus, collaboration, ownership, escalation, inclusion — that the scenarios below rehearse.

One reassurance before you start: situational judgement improves with reflection, not just experience. Every scenario here is a safe rehearsal for a situation you may genuinely meet, and thinking it through now — calmly, with no stakes — is precisely how good judgement is built.

### How this assessment maps to your role

The judgement dimensions map directly to the named skills in your role summary:

- **Process discipline under pressure** maps to your **Change management** skill: documenting change requests properly and actioning changes from change requests means holding the line, politely, when someone asks you to shortcut the process — and knowing which shortcuts (emergency change procedures) are legitimate.
- **Escalation judgement** maps to your **Ownership and topic** skill: showing awareness of problem resolution processes and passing problems to your team is not weakness — at your level it is the defined, correct behaviour. The test rewards knowing what is yours to fix and what is yours to raise.
- **Routing and information gathering** maps to your **Incident management** skill: identifying and registering incidents, gathering the required information, and allocating them to the appropriate channel is a judgement call you make daily, and several scenarios rehearse it.
- **Working with others** maps to your **Community collaboration** skill: contributing to the work of others, helping create the right environment for the team, and recognising and dealing with issues — including quiet interpersonal ones like a colleague being talked over — are scored behaviours, not soft extras.
- **User focus** maps to your **User focus** and **Service focus** skills: showing awareness of user experience principles and of the different products and services around you means asking, in every dilemma, "who is affected downstream?" The strongest answer usually serves the user as well as the process.
- **Honesty and learning** maps to your **Problem management** skill: contributing to remedies and preventative measures only works if post-release analysis is honest — including when the analysis points at your own work.

### Practice questions

**Question 1 (easy) — Pressure to skip the process**

A developer you work with often messages you: "Tiny fix for the reporting service, two lines of code, zero risk. Can you just push it out tonight? Raising a change request feels like overkill and the board doesn't meet until Wednesday." What is the most effective response?

- A) Deploy it tonight — maintaining a good relationship with developers matters, and it genuinely is a small change.
- B) Refuse and report the developer to their line manager for attempting to bypass change control.
- C) Explain that all production changes need a change record, help them raise one quickly, and check whether it qualifies as a standard change that would not need to wait for Wednesday's board.
- D) Ignore the message until the developer raises a change request properly.

**Correct answer: C**

**Explanation:** Option C holds the process line while actively helping: it explains the "why", offers practical help with the paperwork, and — importantly — uses real process knowledge to solve the developer's actual problem, because a genuinely small, well-understood, repeatable fix may qualify as a pre-authorised standard change that can go out without board review. That is collaboration and change management working together. Option A trades away change control for likeability; "zero risk" is precisely the claim change assessment exists to test, and unrecorded changes are how CMDBs rot and incident investigations dead-end. Option B treats a common, usually innocent request as misconduct — escalation that damages the relationship without cause. Option D protects the process but abandons the colleague and the underlying need, and silence teaches people to route around you. At analyst level, the scored behaviour is exactly C's shape: firm on the standard, generous with help, fluent in the legitimate fast paths.

**Question 2 (easy) — Your own mistake in the CMDB**

While updating records after last night's release, you realise that a fortnight ago you recorded the wrong server as hosting the notifications service, and the wrong record has been in the CMDB ever since. Nobody has noticed. What is the most effective response?

- A) Correct the record quietly — no harm was done, and mentioning it would only worry people.
- B) Correct the record, then tell your change and release manager what happened and check whether anything relied on the wrong information in the meantime — for example, any incident investigations or planned changes touching that server.
- C) Leave the record as it is — changing it now might cause confusion.
- D) Report the error to your manager and wait for their instruction before touching the record.

**Correct answer: B**

**Explanation:** Two duties operate here: fix the data, and deal honestly with the consequences of it having been wrong. Option B does both, in the right order — the correction is squarely within your role (maintaining accurate configuration information is your named skill), and the disclosure matters because a wrong CMDB record is not harmless while it is wrong: an incident responder might have checked the wrong server, or a change might have been assessed against the wrong dependency. Checking backwards for impact is exactly the "verify the state" habit your role values. Option A fixes the data but hides the exposure window, and quiet corrections corrode the trust a CMDB depends on. Option C is the worst of both. Option D over-escalates a correction you are competent and authorised to make — though note the difference from Question 1's option B: telling your manager is right; being unable to act without instruction is not. Owning mistakes quickly and completely is one of the most reliably scored behaviours in situational judgement tests, because it predicts trustworthiness better than almost anything else.

**Question 3 (easy) — A user reports a problem directly to you**

A caseworker who knows you personally stops you in the corridor: "Since your release last night, the search screen keeps freezing. Can you sort it?" You are on your way to a meeting about next month's release plan. What is the most effective response?

- A) Promise to look at it yourself as soon as your meeting ends.
- B) Explain that faults must go through the service desk and continue to your meeting.
- C) Thank them, gather the key details (what happens, since when, which screen, does it affect colleagues too), register the incident through the proper channel so it is tracked and routed, and let them know the reference so they can follow up.
- D) Tell them it is probably not related to the release, since the smoke tests all passed.

**Correct answer: C**

**Explanation:** This is your incident management skill verbatim: identify and register incidents, gather the required information, and allocate to the appropriate channel. Option C does exactly that, and the small human touches — thanking them, giving them the reference — are user focus in action: the caseworker experiences a service that listened, not a process that deflected. Option A is generous but wrong twice over: an untracked, personally-promised fix bypasses prioritisation (others may be affected more), and if you get pulled elsewhere the report simply evaporates. Option B is procedurally correct and behaviourally poor — sending a user away unheard costs information (you learned it started after your release: that is post-release analysis gold) and goodwill. Option D dismisses evidence because it is inconvenient; smoke tests passing means the tested paths worked, not that nothing broke. Notice the general shape, which recurs throughout situational judgement tests: the best answer routes the issue properly and treats the person well — process and warmth are not competitors.

**Question 4 (moderate) — A rollout starts failing while you are on your own**

At 8:30pm you are running a scheduled deployment. Batch one of the rollout shows a higher failure rate than the procedure's pause threshold, so you pause, as the runbook says. But the runbook's next section assumes the on-call engineer is available, and tonight's on-call engineer is not answering. The release window closes at 10pm. You could probably diagnose the failures yourself with an hour's investigation. What is the most effective response?

- A) Use the hour to investigate yourself — you paused correctly, and fixing it solo would show initiative.
- B) Resume the rollout — the failures were only slightly over the threshold, and the window is closing.
- C) Keep the rollout paused, follow the escalation route to reach the change and release manager (or the documented fallback contact), report the situation factually, and prepare for the likely outcome that the release completes another night with the back-out plan ready if needed.
- D) Back everything out immediately and email a full report for the morning.

**Correct answer: C**

**Explanation:** The pause was right; the question is what comes next when the assumed support is missing. Option C shows the judgement your level is scored on: the system is in a safe, paused state, so the priority is not speed but getting the right decision-maker informed — that is your ownership skill exactly as your role defines it ("pass problems on to your team", with awareness of the resolution process). Escalating past an unresponsive on-call engineer is not telling tales; it is what escalation routes are for. Option A is the tempting one: initiative is a virtue, but a solo, unplanned, late-evening investigation on production, with the window closing and no second pair of eyes, converts a controlled pause into an uncontrolled experiment — and if it goes wrong, no one even knows you are in trouble. Option B overrides a threshold that exists precisely so this decision is not made by a tired person at 8:30pm. Option D is an overreaction: backing out is a real intervention with its own risks, and nothing yet indicates it is needed — the paused state is stable. The mature analyst move is unglamorous and correct: hold safe, escalate, document. Initiative at your level means making the escalation crisp, not making the decision alone.

**Question 5 (moderate) — A senior colleague's incomplete change request**

Reviewing the papers for tomorrow's change advisory board, you notice that a change request submitted by a senior engineer — someone with fifteen years' experience and little patience for paperwork — has no back-out plan, which the policy says means it should be returned without review. The change itself looks important and well designed. What is the most effective response?

- A) Say nothing — the board can spot the gap themselves, and the engineer outranks you.
- B) Contact the engineer today, point out the missing back-out plan, and offer to help them add it in time for tomorrow's board.
- C) Write the back-out plan yourself and attach it to the request without telling the engineer, so the board sees a complete paper.
- D) Flag the request to the board chair as non-compliant and recommend it be returned.

**Correct answer: B**

**Explanation:** Option B fixes the actual problem — an important change at risk of being bounced for an avoidable gap — in the way that best serves everyone: early, direct, and helpful. Seniority is irrelevant to whether a back-out plan is required, but it is very relevant to tone, and B's shape (private, prompt, offering help) is how a junior colleague credibly holds a standard with a senior one. This is your community collaboration skill: contributing to the work of others and recognising and dealing with issues. Option A fails the change, the engineer, and the board — spotting a defect and staying silent because of rank is exactly what assessment scorers mark down, and letting the board discover it wastes a governance slot. Option C is well-meant and wrong: a back-out plan written by someone who does not know the change's internals may be dangerously plausible, and submitting it under the engineer's request without their knowledge muddles accountability — if the change fails at 2am, the person executing your back-out plan believes its author understood the system. Option D reaches for governance before conversation; it is where you end up if the engineer refuses, not where you start. The general rule: escalate defects you cannot resolve, but first try the cheap, human fix — a message today beats a ruling tomorrow.

**Question 6 (moderate) — Caught between DevOps and a service designer**

A DevOps engineer wants next week's release to include a database migration alongside a user-facing fix: "One window, one set of approvals, done." The service designer wants the user-facing fix out as soon as possible and is worried the migration — which needs extra preparation — will delay it: "Users are struggling now." Both have emailed you, separately, asking you to schedule it their way. What is the most effective response?

- A) Schedule it the DevOps engineer's way — they understand the technical risk better than the designer.
- B) Schedule it the service designer's way — user needs always outrank technical convenience.
- C) Get the two of them and yourself into one conversation, lay out the options with their consequences (combined release later, or split releases with the fix sooner), and agree a recommendation to put to the change and release manager.
- D) Schedule both options provisionally and let whoever complains loudest win.

**Correct answer: C**

**Explanation:** Your role summary names this exact situation: a change and release analyst liaises with DevOps and service designers. The failure mode in the scenario is not technical — it is that two colleagues are negotiating through you separately, which guarantees someone feels overruled by a scheduling decision they never got to discuss. Option C fixes the structure: one conversation, options framed with consequences rather than owners ("fix ships week two if split; week three if combined" is discussable in a way "your way versus their way" is not), and a joint recommendation that goes to the decision-maker with everyone's fingerprints on it. That is community collaboration — creating the right environment — plus correct escalation, since the scheduling decision for a contested change belongs with your manager, informed by your groundwork. Options A and B both decide by trusting a category of person rather than examining the case; each also teaches one colleague that emailing you is how decisions get made. B deserves a special note: user focus is a genuine value, and the split-release option that serves users may well win — but it should win in the open conversation, on its merits, not by default. Option D is abdication dressed as flexibility. When a test scenario shows you two reasonable people pulling in different directions, the strongest answer almost always brings them together rather than picking a winner privately.

**Question 7 (moderate) — Asked something you do not know**

In the release planning meeting, the service owner turns to you: "You're across the detail — is the continuity failover tested for the new document service? If the data centre fails mid-release, are we covered?" You are not sure: you know the continuity procedure in general, but you do not know whether this specific service's failover has been tested. Senior people are waiting. What is the most effective response?

- A) Say yes — the continuity team is usually thorough, and you can check afterwards to make sure.
- B) Say you are not certain about this specific service's failover testing, commit to finding out from the continuity team today, and share what you do know: what the standard procedure requires and how the release's back-out plan interacts with it.
- C) Say it is not your area and suggest they invite the continuity team next time.
- D) Give a detailed answer about the continuity procedure in general, without mentioning that you do not know the specific answer.

**Correct answer: B**

**Explanation:** Option B is honest about the boundary of your knowledge, takes ownership of closing the gap with a concrete commitment ("from the continuity team, today"), and still adds value in the moment by contributing what you genuinely do know — which, per your continuity management skill, is the basic principles and how they touch your release. That combination — candour, ownership, useful partial knowledge — is exactly what scorers look for at your level. Option A is the dangerous one: a guessed "yes" about continuity coverage could sit unchallenged in the meeting minutes and become the basis of a risk decision; "check afterwards" does not un-say it, and being caught guessing once costs you the credibility your role runs on. Option D is subtler but similar: fluent generalities delivered in place of the asked-for answer let the room believe the question was answered — an evasion that sounds like expertise. Option C is honest but drops the ball entirely; "not my area" may be true of the testing itself, but chasing the answer for a release you are planning is absolutely your area. "I don't know, I'll find out by X" is one of the most powerful sentences in professional life. Practise saying it without flinching — people trust those who can.

**Question 8 (moderate) — A struggling teammate before a big release**

Two weeks before the biggest release of the year, you notice a fellow analyst is behind on preparing the deployment procedures they own. They seem stressed, have started staying late, and snapped at a colleague in stand-up — very unlike them. Your own preparation is on track. What is the most effective response?

- A) Focus on your own work — commenting on a peer's performance is your manager's job, not yours.
- B) Check in with them privately, ask how they are doing and whether they would like help, and if the release preparation genuinely is at risk, encourage them to raise it with the manager early — offering to share some of the load if you have capacity.
- C) Tell your change and release manager immediately that the release is at risk because of your colleague.
- D) Quietly take over parts of their preparation without discussing it, so the release stays on track and they are spared embarrassment.

**Correct answer: B**

**Explanation:** Option B leads with the person, not the plan — a private, kind check-in first — then deals squarely with the work: if the release preparation is at risk, the manager needs to know early, and the person best placed to raise it well is the colleague themselves, supported rather than reported. Offering specific help, bounded by your real capacity, makes the support concrete. This is your community collaboration skill in its fullest sense: contributing to the work of others, helping create the right environment, and recognising and dealing with issues — including human ones. Option A hides behind hierarchy; noticing a teammate struggling and looking away is precisely the behaviour "create the right environment" exists to rule out, and two weeks before a major release, an unraised risk is everyone's problem. Option C jumps over the colleague to the manager, converting a supportable wobble into a reported failure — it may eventually be necessary, but as a first move it damages trust and skips the cheapest fix. Option D is generous on the surface and corrosive underneath: procedures silently written by someone else are procedures the owner cannot answer for at 9pm on release night, the workload problem stays hidden and recurs, and discovering the quiet takeover is its own embarrassment. Care for the person, honesty about the risk, help with the load: in that order, and in the open.

**Question 9 (challenging) — Discovering an unauthorised change**

Investigating a minor incident, you find the cause: a configuration change made directly on a production server three days ago. There is no change record. The change was made by a well-liked engineer who once helped you out of a difficult spot. When you mention it informally, they say: "It was a tiny tweak to stop the disk filling up — I was going to raise the paperwork, honestly. Can we keep this between us? I'll raise it today." What is the least effective response?

- A) Agree to keep it quiet as long as they raise the change record today as promised.
- B) Tell them you have to record the true cause in the incident investigation, encourage them to raise the retrospective change record right away and to self-report to the change and release manager, and give them the chance to do so before you escalate it yourself.
- C) Record the actual cause accurately in the incident record, including the unauthorised change.
- D) Explain why unrecorded production changes matter — this one caused an incident and cost investigation time precisely because nobody knew about it.

**Correct answer: A**

**Explanation:** Note the reversed question — you are asked for the least effective response, and it is A: agreeing to conceal. Read what A actually trades away. Your incident investigation would have to be silently falsified or left vague, so the organisation loses the true lesson (an ungoverned change caused an outage); the "I'll raise it today" promise has no check on it — and this engineer's relationship to paperwork is, on present evidence, aspirational; and you personally become co-owner of a concealment, purchasable for the price of a past favour. That last point is what the scenario is really testing: whether gratitude and likeability can buy your professional integrity. They cannot be allowed to — an analyst whose records depend on who is asking is not maintaining accurate information at all. The other options are all constructive parts of an effective response, and notice their shared character: none of them is vindictive. B is the strongest single course — honest about what you must do, generous in offering the engineer first move to self-report, which preserves both the truth and, as far as possible, the relationship. C is the non-negotiable core: the record tells the truth. D is the collegial conversation that turns an awkward moment into learning. Real integrity dilemmas rarely require harshness; they require you to be unable to un-know what you know, and to say so kindly.

**Question 10 (challenging) — Your own plan caused the failure**

Post-release analysis of last week's failed release points somewhere uncomfortable: the deployment failed because two changes were scheduled in the same window, and their interaction was never assessed — and you built that schedule. The combined scheduling was your suggestion, made to save a release window. Your manager has asked you to present the analysis at Friday's team review. What is the most effective response?

- A) Present the findings fully, name the scheduling interaction as the cause and your own scheduling decision as part of the chain, and propose a preventative measure — for example, an interaction check whenever changes share a window.
- B) Present the technical interaction as the cause but leave out who scheduled the changes together, since blame is unhelpful and the technical lesson is what matters.
- C) Ask your manager privately to reassign the presentation, since presenting your own mistake is a conflict of interest.
- D) Present the findings but emphasise that the change owners should have flagged the interaction, since they knew their changes best.

**Correct answer: A**

**Explanation:** Option A is post-release analysis done honestly, which is the entire point of your role's analysis duty and the foundation of your problem management skill: contribute to remedies and preventative measures. The preventative measure in A — an interaction check for shared windows — is only findable if the analysis truthfully includes the scheduling decision; sanitise the cause and you sanitise away the fix. Naming your own decision "as part of the chain" is the right register: factual, proportionate, neither self-flagellating nor evasive. Option B smuggles in a half-truth under the respectable banner of blamelessness — but blameless analysis means not punishing honest error, not omitting facts; an analysis that hides the decision behind the failure will produce a remedy that misses it. Option D is worse than omission: it actively redirects responsibility toward colleagues, and doing so while concealing your own part is the behaviour that, once noticed, permanently prices your reports at a discount. Option C misunderstands conflict of interest — you are not judging your own appeal; you are reporting your own findings, and an analyst who presents their own mistake with a straight face and a good fix gains standing, not loses it. Here is the encouraging secret that experienced practitioners know: Friday's presentation, done as option A, is the moment the team learns you can be trusted with anything. Mistakes are tuition; honesty is what makes the fee worth paying.

**Question 11 (challenging) — A colleague being talked over**

In release retrospectives, you have noticed a pattern: a newer analyst on the team — quieter than the others, and the only person on the team from their background — is repeatedly interrupted, and twice their suggestion has been re-stated ten minutes later by someone else and adopted with credit going to the re-stater. They have started saying less each meeting. You are not the meeting chair. What is the most effective response?

- A) Say nothing in the meeting, but tell the newer analyst afterwards that their ideas are good and they should speak up more assertively.
- B) In the moment, redirect credit and attention naturally — "That builds on what Sam suggested earlier; Sam, can you say more?" — and separately mention the pattern to the chair so the meeting itself gets run more inclusively.
- C) Raise it as a formal complaint about the interrupting colleagues.
- D) Start collecting the newer analyst's suggestions yourself before each retrospective and present them on their behalf.

**Correct answer: B**

**Explanation:** Option B acts at both levels the problem lives at. In the moment, the redirect — specific, natural, credit-restoring — costs almost nothing and changes the room immediately: it returns the floor and the authorship to the person who earned them, and it models the behaviour for everyone else. Structurally, the pattern is a meeting-culture problem, and the chair owns the meeting; a quiet word equips them to manage interruptions and draw people in deliberately. This is your community collaboration skill precisely as your framework words it: create the right environment for teams to work in, and recognise and deal with issues. Option A locates the problem in the quiet colleague — "be more assertive" — when the observed fault is in the interrupting; coaching the person being talked over to talk louder treats the symptom, burdens the wrong person, and quietly endorses the room's behaviour. It is also worth noticing what the scenario tells you: the pattern lands on the team's only member from their background, which is exactly how exclusion often operates — not through hostility, but through whose voice gets absorbed and whose gets attributed. Option C reaches for formal machinery before anyone has tried the ordinary human repairs; formality may become right if the pattern persists, but as a first move it escalates conflict rather than culture. Option D makes the newer analyst a ventriloquist's act — protected, dependent, and even less heard in their own voice. Inclusion in practice is mostly made of small moves like B's, made promptly, by peers who noticed.

**Question 12 (challenging) — Pressure to exceed your authority**

Your change and release manager is on leave until Monday, and the deputy is off sick. On Thursday afternoon, a senior programme director arrives at your desk: "The minister's announcement moved to tomorrow morning. I need the content update released tonight. You're the change and release person here — just approve it. I'll take full responsibility." The change is real and matters, but approving changes is beyond your authority, and the emergency change procedure requires an authorised approver. What is the most effective response?

- A) Approve it — a director has explicitly taken responsibility, and blocking a ministerial announcement would be career-limiting.
- B) Refuse and explain that nothing can be released until your manager returns on Monday.
- C) Explain that approval is beyond your authority but that the emergency change procedure exists for exactly this situation, then actively help: locate the authorised approver on the escalation list (or the manager's documented cover arrangement), get the director connected to them fast, and prepare the change record and deployment so no time is lost once approval lands.
- D) Contact your manager on leave and ask them to approve it by phone.

**Correct answer: C**

**Explanation:** Strip away the seniority and the deadline, and the structure is simple: a legitimate urgent need, an authority you do not hold, and a procedure that exists precisely for legitimate urgent needs. Option C honours all three — and notice how much of it is action, not refusal: finding the authorised approver, making the connection, preparing the record and the deployment in parallel so that approval is the only thing anyone waits for. That is what "no, but" looks like when done well, and it is your ownership skill exactly: you own the issue until it reaches the person who can resolve it. Option A fails on a point worth engraving: "I'll take responsibility" is not a transferable instrument — the director cannot take your responsibility for acting outside your authority, and organisations discover this at precisely the worst moments. A verbal assurance at your desk is also not what the procedure means by authorisation; if it were, every determined senior person would be an approver. Option B is the rigid mirror-image failure: it treats process as a wall rather than a route, leaves a genuine need unmet for four days, and misrepresents the situation — the emergency procedure means something can be done tonight. Option D is not absurd — some organisations' escalation lists do reach a manager on leave as a last resort — but as a first move it skips the documented cover arrangements that exist so leave is actually leave. The scored behaviour is C's combination: clear about the boundary, energetic about the path. Under pressure, the best analysts become more procedural and more helpful at the same time — the two are not in tension; they are the job.

### Preparation tips

- **Learn your escalation routes cold.** Half the hardest scenarios dissolve if you know who your fallback contacts, authorised approvers, and cover arrangements are. Look them up this week — it is both test preparation and genuinely useful.
- **Rehearse the pattern "hold safe, then escalate".** At analyst level, the strongest answer to a live problem is very often: put the system in a safe state, then get the right person informed. Practise recognising that shape.
- **Choose answers for the role, not for the hero.** Options that have you solving everything alone, overriding thresholds, or absorbing others' responsibilities usually score poorly at your level. Collaboration and correct escalation are strengths, not cop-outs.
- **Look for the option that fixes the problem and treats people well.** When two options both address the issue, the one that is early, private, and helpful usually beats the one that is late, public, or punitive.
- **Read the question stem twice.** "Most effective" and "least effective" look identical at speed. Underline which one you are being asked for.
- **Reflect on real dilemmas you have seen.** After the next tricky situation at work, ask yourself: what were the four plausible responses, and why did the best one win? This turns everyday work into free test preparation.
- **Be honest in your answers.** Situational judgement tests are calibrated by experienced practitioners; trying to guess a "corporate" answer usually performs worse than answering as the careful, honest analyst you are becoming.

### Common pitfalls to avoid

- **Choosing the lone-hero option.** Investigating solo at 9pm, quietly rewriting a colleague's work, approving beyond your authority — dramatic self-reliance is the most common wrong answer at this level.
- **Choosing the pure-process option.** "Refuse and cite the policy" without helping anyone forward is the second most common wrong answer. The best responses hold the standard and open a path.
- **Escalating as a first move.** Reporting a colleague to a manager or chair before trying a direct, kind conversation usually scores poorly — unless safety, security, or integrity is at stake, in which case escalation rises sharply in value.
- **Trading integrity for relationships.** Any option built on concealment — quiet fixes, omitted causes, secrets kept for likeable colleagues — is almost always the least effective, however small it seems.
- **Confusing kindness with avoidance.** Protecting a struggling colleague by hiding a risk, or sparing someone embarrassment by doing their work secretly, harms them and the team. Kind and honest beat kind and silent.
- **Ignoring the user in the room.** When a scenario mentions users — a caseworker in a corridor, users struggling with a fault — the strong answer acknowledges and serves them, not just the internal process.
- **Answering for a different level.** You are not scored on making a manager's decisions; you are scored on excellent analyst judgement: safe hands, honest records, early escalation, and generous collaboration.

## Conclusion

Well done for working through this guide — that was a substantial piece of professional development, and you should feel genuinely good about completing it.

Take a moment to notice what you have practised. In the cognitive section, you checked release naming conventions, reasoned through change freeze rules, reconciled CMDB records against discovery scans, sequenced releases around dependencies and protected windows, and followed branching back-out procedures precisely — the structured thinking your role uses every day, sharpened under gentle time pressure. In the numeric section, you calculated success rates, availability percentages, weighted averages, audit projections, and capacity headroom, always step by step, always asking "out of what?". In the verbal section, you held the line between what a policy actually says and what you assumed it says, learned to respect the difference between must, should, and may, and judged which release notice a caseworker could actually use. And in the situational judgement section, you rehearsed the moments that define an analyst's reputation: holding a process line while helping a colleague, escalating early and well, owning a mistake in front of the team, and staying both procedural and helpful when a director is standing at your desk.

Here is the encouraging truth that ties it all together: none of this was really test preparation in disguise. Every technique in this guide — base-checking a percentage, reading a conditional procedure branch by branch, registering an incident properly, saying "I don't know, I'll find out by tomorrow" — is the day job of a good change and release analyst. Practising for the assessment and getting better at the role are the same activity. That is exactly what a well-designed job-specific assessment is supposed to achieve, and it means every hour you spent here pays twice.

If you take three habits forward, make them these. First, accuracy before speed: in tests and in releases alike, the careful answer beats the fast one, and speed grows naturally from practice. Second, deduce only what the evidence guarantees: in CMDB records, incident investigations, and verbal reasoning passages, the disciplined reader who can say "cannot say" is the one people learn to trust. Third, escalate early and generously: at your level, knowing what is yours to fix and what is yours to raise — and raising it with the groundwork already done — is not a limitation of the role; it is the craft of it.

Keep practising little and often, revisit the sections that stretched you most, and be patient with yourself: judgement and fluency are built exactly the way you have been building them here, one worked question at a time. You are developing the habits of someone who plans carefully, records honestly, and keeps services safe while change flows through them. That is a professional worth becoming — and you are well on your way. Good luck with your assessment.
