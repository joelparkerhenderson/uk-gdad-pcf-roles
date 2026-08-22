# Associate Infrastructure Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as an associate infrastructure engineer working within the UK Government Digital and Data profession. You are at the start of an exciting career: you work in an established team, you support experienced infrastructure engineers in their daily work, and you learn under their direction. This document will help you practise the kinds of psychometric assessments you may meet during your career — and, just as importantly, it will help you build confidence in the thinking skills that your role depends on every day.

First, let's be clear about what psychometric assessments are. They are structured, standardised exercises that measure the mental abilities and behavioural tendencies that predict success in a job. That might sound intimidating, but there is nothing mysterious about them. They are simply a fair, consistent way of asking: can this person spot a pattern, follow a logical rule, work with numbers, read carefully, and choose a sensible course of action at work? The good news is that every one of those abilities improves with practice — and this guide gives you lots of practice, using scenarios drawn directly from your own role.

Why do these assessments matter for you in particular? As an associate infrastructure engineer, you support the infrastructure services that underpin everything your department does — the servers, storage, networks, cloud services, and software packages that internal users and members of the public rely on. Even as a trainee, your daily work involves spotting things that look wrong, following runbooks and checklists accurately, reading tickets and instructions carefully, and knowing when to pass a problem on to your team. Those are exactly the abilities that cognitive, numerical, verbal, and situational judgement assessments measure. Practising them will make you better at the assessments and better at the job.

This document is organised into four main assessment sections. Each one follows the same friendly pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment to the specific skills in your role's capability framework, a set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The questions start easy and get gradually harder, so you can build up steadily.

Here is how to get the most from this guide. First, read each "About this assessment" section so you know what to expect — surprises cause nerves, and knowledge removes them. Second, try each practice question honestly: write down your answer before you read the explanation. Third, treat every explanation as a mini-lesson. Even when you get a question right, the walkthrough will show you a reliable technique you can reuse. Fourth, do not rush. You are learning, and learning takes repetition. If a question stumps you, that is not a failure — it is a signpost showing you exactly where a little more practice will help.

One last thing before you begin: be kind to yourself. Nobody expects an associate to know everything. Your role level is about learning, supporting, and asking good questions, and this guide is written with that in mind. The scenarios describe supervised, day-to-day tasks — checking a server list, reading a ticket, following an escalation process — because that is your real world right now. Take your time, enjoy the practice, and notice how much you improve between the first question and the last. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of asking you to rotate shapes or complete number sequences with no context, it presents you with the everyday materials of your job — server naming conventions, patching schedules, monitoring alerts, ticket queues, and simple system diagrams — and asks you to reason quickly and accurately about them.

The typical format is an online, timed test lasting 15 to 30 minutes, with somewhere between 15 and 30 questions. The questions cover pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared against a norm group of people at a similar career stage, so you are not being measured against engineers with twenty years of experience. Many modern platforms adapt the difficulty of questions based on your previous answers, which means a test that feels hard is often a test you are doing well on. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working carefully matters just as much as working quickly. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without any pressure.

Why do employers use this kind of assessment for associate infrastructure engineers? Because at your level, raw experience is limited by definition — you are a trainee — so employers look for the underlying thinking abilities that predict how quickly and safely you will learn. Infrastructure work is detail-critical: a single wrong character in a hostname, a missed step in a checklist, or a misread alert can affect a live service that the public depends on. Cognitive assessments are a fair way to check that you can hold details in mind, follow rules exactly, and notice when something does not fit the pattern. These are learnable skills, and this section will help you sharpen them.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **IT infrastructure** skill: supporting computer, storage, networking, physical infrastructure, software, COTS packages, and open source solutions means working with structured information every day — naming conventions, IP address ranges, version numbers, and configuration lists. Spotting the entry that breaks the pattern is a core support skill.
- **Logical deduction** maps to your **Systems integration** skill: explaining the process and principles of integrating systems requires you to follow if-then reasoning — if system A sends data to system B, and B is down, what follows? It also maps to **Information security**, because security controls are rules, and applying rules correctly is deduction.
- **Error checking** maps to your **Troubleshooting and problem resolution** skill: demonstrating basic troubleshooting capability starts with noticing what is wrong — a mismatched configuration, an alert that contradicts a dashboard, a checklist step that was skipped.
- **Prioritisation** maps to your **Ownership and topic** skill: showing an awareness of problem resolution processes and knowing when to pass problems on to your team means judging what needs attention first and what can wait.
- **Applied problem solving** maps to your **Problem management** skill: investigating problems in systems, processes, and services — and understanding whether a problem is strategic, tactical, or operational — is structured problem solving in action, and to your **Systems design** skill, because assisting a team with the design of components means reasoning about how parts fit together.

### Practice questions

**Question 1 (easy) — Pattern recognition in server names**

Your team names servers using this convention: two letters for the site (LN for London, MC for Manchester), then three letters for the function (WEB, APP, DBS), then a two-digit number. For example, LNWEB01 is the first web server in London. While checking a server list, you see these entries:

1. LNWEB01
2. MCAPP03
3. LNDBS12
4. WEBLN02
5. MCWEB07

Which entry breaks the naming convention?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: C**

**Explanation:** Work through the rule one part at a time: site code first, then function, then number. Entry 1 is LN + WEB + 01 — correct. Entry 2 is MC + APP + 03 — correct. Entry 3 is LN + DBS + 12 — correct. Entry 4 begins with WEB, which is a function code, not a site code: the parts are in the wrong order, so it breaks the convention. Entry 5 is MC + WEB + 07 — correct. In real support work, naming conventions matter because scripts, monitoring tools, and colleagues all rely on them; a wrongly named server can be missed by backups or patching. The reliable technique is to check each entry against the rule piece by piece rather than trusting your first glance.

**Question 2 (easy) — Logical deduction about a patching rule**

Your team's rule says: "Every Windows server must be patched during the monthly maintenance window, unless it is tagged 'exempt' by the security team." A colleague tells you: "Server MCAPP03 is a Windows server and it was not patched during this month's window." Which one of the following must be true?

- A) The team forgot to patch MCAPP03.
- B) MCAPP03 is tagged 'exempt' by the security team.
- C) Either MCAPP03 is tagged 'exempt', or the rule was broken.
- D) MCAPP03 is not really a Windows server.

**Correct answer: C**

**Explanation:** The rule has exactly one permitted exception: an 'exempt' tag. From the facts given, you cannot tell whether that exception applies. So option A is only a possibility, not a certainty — perhaps the server is exempt. Option B is also only a possibility — perhaps the team really did forget. Option D contradicts the facts you were given. The only statement that must be true in every case is option C: either the exception applies, or the rule was broken. This careful habit — concluding only what the information guarantees — is exactly what you need when you investigate problems as part of **Problem management**: check the exemption list before assuming a mistake, and check the facts before blaming anyone.

**Question 3 (easy) — Error checking a checklist**

You are following a runbook to restart a service. The runbook says: Step 1: notify the service desk. Step 2: check no batch jobs are running. Step 3: stop the service. Step 4: wait two minutes. Step 5: start the service. Step 6: confirm the service responds. Step 7: notify the service desk that work is complete. Your colleague's notes from last night read: "Notified service desk, checked batch jobs, stopped service, started service, confirmed responding, notified completion." Which step appears to have been skipped?

- A) Step 2
- B) Step 4
- C) Step 6
- D) Step 7

**Correct answer: B**

**Explanation:** Match the notes against the runbook step by step. Notified service desk = Step 1. Checked batch jobs = Step 2. Stopped service = Step 3. Started service = Step 5. Confirmed responding = Step 6. Notified completion = Step 7. The two-minute wait (Step 4) is missing from the notes. Waiting steps are the easiest to skip because they produce no visible output, yet they often exist for good technical reasons — for example, letting connections close cleanly. As an associate, comparing what was done against what should have been done is one of your most valuable contributions: fresh eyes catch skipped steps. The technique is simple and reliable: tick off each recorded action against the list, and whatever has no tick is your answer.

**Question 4 (easy) — Prioritising two tickets**

You are monitoring the team's ticket queue under supervision. Two new tickets arrive at the same time. Ticket 1: "Printer on floor 3 is showing a low toner warning." Ticket 2: "Staff in the contact centre report they cannot log in to the case system — citizens are waiting on calls." Your supervisor is at lunch. What is the most sensible first action?

- A) Deal with the toner warning first because it arrived at the top of the queue.
- B) Flag the contact centre ticket to the team straight away, because it is stopping a live service to the public.
- C) Wait until your supervisor returns before doing anything.
- D) Close the toner ticket because toner warnings are not real incidents.

**Correct answer: B**

**Explanation:** Prioritisation means comparing impact and urgency, not queue position. Ticket 2 describes many users unable to work and citizens directly affected — high impact and high urgency. Ticket 1 is a warning, not a failure: the printer still works, so it is low impact and low urgency. Option A confuses arrival order with importance. Option C delays a serious issue unnecessarily — your role summary says you should show awareness of problem resolution processes and pass problems on to your team, which is exactly what option B does: you are not expected to fix the login system yourself, but you are expected to raise it promptly. Option D is wrong because the toner ticket is valid work; it just comes later. Notice that the best answer is not "fix it yourself" — at your level, fast, accurate escalation is the professional response.

**Question 5 (moderate) — Pattern recognition in IP addresses**

Your site uses the address range 10.20.0.0/16, and the team convention is: the third number identifies the floor (1 to 4), and the fourth number identifies the device, where numbers 1–99 are workstations and 100–199 are printers. You are checking four devices recorded in the asset register:

1. 10.20.2.45 — workstation, floor 2
2. 10.20.4.120 — printer, floor 4
3. 10.20.3.150 — workstation, floor 3
4. 10.20.1.7 — workstation, floor 1

Which record is inconsistent with the convention?

- A) Record 1
- B) Record 2
- C) Record 3
- D) Record 4

**Correct answer: C**

**Explanation:** Check each record against both parts of the rule. Record 1: third number 2 matches floor 2; fourth number 45 is in the workstation range 1–99, and the record says workstation — consistent. Record 2: floor 4 matches; 120 is in the printer range 100–199, and the record says printer — consistent. Record 3: floor 3 matches; but 150 is in the printer range 100–199, and the record says workstation — inconsistent. Record 4: floor 1 matches; 7 is in the workstation range — consistent. In real infrastructure support, an inaccurate asset register causes wasted visits and failed changes, so this kind of cross-check genuinely matters. The technique: when a record has two properties to verify (floor and device type), check both — many people stop after the first one matches.

**Question 6 (moderate) — Deduction about system dependencies**

You are told: (i) the payroll application depends on the database server; (ii) the database server depends on the storage array; (iii) the intranet does not use the database server or the storage array. This morning the storage array went offline for ten minutes. Which of the following must have been affected during those ten minutes?

- A) The intranet only
- B) The database server and the payroll application
- C) The payroll application only
- D) Nothing, because ten minutes is too short to matter

**Correct answer: B**

**Explanation:** Follow the dependency chain step by step. The storage array went offline. The database server depends on the storage array, so the database server was affected. The payroll application depends on the database server, so the payroll application was affected too. The intranet uses neither, so it carried on unaffected — eliminating options A. Option C forgets the middle link: if the payroll application was affected through the database, then the database itself was certainly affected. Option D is wishful thinking — duration changes how serious an outage is, not whether dependent systems were affected. Dependency chains like this are the foundation of **Systems integration** understanding: knowing what connects to what tells you who to warn, what to check, and where a fault will show up next. When you draw or read a dependency diagram, always trace the full chain, not just the first hop.

**Question 7 (moderate) — Error checking a change request**

A colleague drafts a change request and asks you to give it a quick read before submission. It says: "Change: apply firmware update to switch LNSW02. Date: Saturday 14 June. Window: 02:00–04:00. Impact: brief network interruption on floor 2. Rollback: reapply the new firmware. Approver: network team lead." What is the clearest error in this change request?

- A) The window is at the weekend, which is not allowed.
- B) The rollback plan reapplies the new firmware instead of restoring the old firmware.
- C) The impact statement mentions floor 2.
- D) The approver should be the service desk.

**Correct answer: B**

**Explanation:** Read each field and ask "does this make sense for its purpose?" A rollback plan exists so you can return to the previous known-good state if the change fails. Reapplying the new firmware would repeat the failed change, not undo it — the plan should say "restore the previous firmware version". Option A is wrong because weekend windows are common precisely to reduce impact on users; nothing in the scenario forbids them. Option C is not an error — stating which users are affected is good practice. Option D invents a rule: approvers vary by organisation, and a network team lead is a plausible approver for a switch change. Spotting a rollback plan that cannot actually roll back is exactly the "basic troubleshooting capability" and error-checking your **Troubleshooting and problem resolution** skill describes: think about what each safeguard is for, then test whether it would really work.

**Question 8 (moderate) — Prioritisation with an escalation process**

Your team's escalation process says: Priority 1 (P1) incidents affect a whole service and must be escalated to the on-call engineer immediately; Priority 2 (P2) incidents affect several users and must be escalated within one hour; Priority 3 (P3) incidents affect one user and are handled in normal queue order. At 09:00 you see three unassigned tickets: Ticket X (logged 08:55): one user's monitor is flickering. Ticket Y (logged 08:20): the department's file-sharing service is down for everyone. Ticket Z (logged 08:45): six users in finance cannot print. In what order should the tickets be actioned according to the process?

- A) X, Y, Z — oldest personal issue first
- B) Y, Z, X — P1 immediately, then P2 within the hour, then P3
- C) Z, Y, X — most users first regardless of service impact
- D) Y, X, Z — P1 first, then the oldest remaining ticket

**Correct answer: B**

**Explanation:** Classify each ticket first, then apply the process. Ticket Y affects a whole service for everyone: P1, escalate immediately. Ticket Z affects several users: P2, escalate within one hour — and note it was logged at 08:45, so the one-hour clock is already running. Ticket X affects one user: P3, normal queue order. So the order is Y, then Z, then X — option B. Option C looks tempting because Z names six users while Y just says "everyone", but a whole-service outage outranks a several-user fault in any standard model. Option D wrongly promotes the P3 above the P2 based on age; the process says priority classes come first, and age orders tickets within a class. This is your **Ownership and topic** skill in action: you do not need to fix any of these yourself — you need to route each one correctly and promptly.

**Question 9 (moderate) — Applied problem solving with monitoring alerts**

At 10:15 the monitoring system shows: web server LNWEB01 — CPU at 98% for 20 minutes; web server LNWEB02 — CPU at 30%; both servers sit behind a load balancer that should share traffic equally between them. Users report the website is slow. Which is the most reasonable first hypothesis to investigate?

- A) Both servers are underpowered and need to be replaced.
- B) The load balancer is not distributing traffic evenly, so LNWEB01 is doing nearly all the work.
- C) Users are imagining the slowness because LNWEB02 is fine.
- D) The monitoring system is broken and both figures are wrong.

**Correct answer: B**

**Explanation:** Good troubleshooting starts by asking "what single explanation fits all the evidence?" The evidence: one server overloaded, its twin nearly idle, and a device in between whose whole job is to share traffic equally. If the load balancer were working, both servers would show similar load. The pattern — one hot, one cold — points at uneven distribution, so option B fits everything. Option A does not fit: if both servers were underpowered, both would be busy. Option C dismisses user reports that are consistent with the data from LNWEB01. Option D assumes two independent readings are both wrong with no supporting evidence — always prefer the explanation that requires the fewest extra assumptions. As an associate, you would report this hypothesis to your team rather than reconfigure the load balancer yourself, which is exactly the right behaviour: investigate, form a hypothesis, and pass the problem on with useful evidence attached.

**Question 10 (hard) — Deduction with multiple conditions**

Your team's backup rules state: (i) every production server is backed up nightly; (ii) every server that holds citizen data is encrypted; (iii) test servers are never backed up nightly. You learn that server LNAPP09 is backed up nightly and is not encrypted. Which one of the following must be true?

- A) LNAPP09 is a production server that holds citizen data.
- B) LNAPP09 is not a test server, and it does not hold citizen data.
- C) LNAPP09 is a test server.
- D) LNAPP09 holds citizen data.

**Correct answer: B**

**Explanation:** Take the facts one at a time. LNAPP09 is backed up nightly. Rule (iii) says test servers are never backed up nightly, so LNAPP09 cannot be a test server — that eliminates option C. LNAPP09 is not encrypted. Rule (ii) says every server holding citizen data is encrypted; since LNAPP09 is not encrypted, it cannot hold citizen data — that eliminates options A and D. Both remaining conclusions — not a test server, and no citizen data — are guaranteed, so option B must be true. Notice one subtle point: you cannot conclude that LNAPP09 is a production server. Rule (i) says production servers are backed up nightly, but it does not say only production servers are — there might be other categories. This "the rule points one way, not both ways" trap appears constantly in assessments and in real security and backup policies, which is why reading **Information security** controls precisely is a named skill at your level.

**Question 11 (hard) — Problem solving across a sequence of events**

A service failed at 03:00 on Tuesday. You gather these facts: (i) a patch was applied to the server at 22:00 on Monday; (ii) the same patch was applied to an identical server at another site at 22:00 on Monday, and that server is fine; (iii) a scheduled disk clean-up job runs on the failed server at 02:45 every night; (iv) the clean-up job does not run on the other site's server; (v) the failed service came back by itself at 03:20 without anyone doing anything. Which line of investigation does the evidence best support?

- A) The patch alone caused the failure.
- B) The clean-up job, or the clean-up job interacting with the newly patched system, caused a temporary failure.
- C) The other site's server will fail within 24 hours.
- D) The failure was caused by a hardware fault.

**Correct answer: B**

**Explanation:** Use comparison and timing — two of the most powerful troubleshooting tools. If the patch alone were the cause, the identical patched server at the other site should also have failed; it did not, which weakens option A. What differs between the two servers? The 02:45 clean-up job runs only on the failed server, and the failure began at 03:00, shortly after the job started — timing and difference both point at the job, possibly interacting with the fresh patch, which is option B. Option C is a prediction the evidence does not support: the other server has no clean-up job, so the suspected trigger is absent there. Option D fits poorly because hardware faults rarely resolve themselves neatly at 03:20 with no intervention, whereas a job that finishes and releases resources would. This is your **Problem management** skill in miniature: investigate by comparing what is the same, what is different, and what happened when — then contribute your findings so the team can implement a remedy, such as re-timing the job or testing the interaction.

**Question 12 (hard) — Integration reasoning under constraints**

Your team must connect a new HR system to three existing systems: the identity service, the payroll system, and the reporting warehouse. The constraints are: (i) the identity connection must be built and tested before any other connection, because the other systems trust identity for login; (ii) the payroll connection can only be tested in the last week of the month, when the payroll test environment is refreshed; (iii) the reporting connection needs two weeks of build work and can start any time after identity is done; (iv) it is now the first week of the month, and the identity connection needs one week to build and test. What is the earliest the payroll connection can be tested, and what should the team work on while waiting?

- A) Test payroll in week 2; build reporting afterwards.
- B) Test payroll in the last week of the month; build the reporting connection during weeks 2 and 3 while waiting.
- C) Test payroll in the last week of the month; do nothing until then because identity must finish first.
- D) Test payroll immediately, because it is the most important system.

**Correct answer: B**

**Explanation:** Lay out the timeline. Week 1: build and test identity (constraint i and iv). Payroll can only be tested in the last week of the month (constraint ii), so week 2 is impossible — eliminating options A and D, which both ignore a hard constraint. That leaves the question of what to do in weeks 2 and 3. Constraint (iii) says reporting needs two weeks and can start any time after identity — so weeks 2 and 3 are exactly enough. Option C wastes two weeks: identity blocks the start of other connections, but once it is finished in week 1, nothing blocks reporting. Option B respects every constraint and uses the waiting time productively. This mirrors the challenges your role summary describes in **Systems integration** — designing, building, and testing interfaces between systems is mostly about sequencing work around dependencies and environment availability. The exam technique: convert wordy constraints into a simple week-by-week grid, then read the answer off the grid.

### Preparation tips

- **Practise with your real materials.** Look at your team's naming conventions, runbooks, and escalation matrix. Ask yourself: what is the rule here, and what would break it? Ten minutes a day of this builds exactly the muscles the assessment tests.
- **Slow down on rules with exceptions.** Phrases like "unless", "except", and "only" carry most of the meaning in policy-style questions. Underline them (mentally or on paper) before answering.
- **Check every option before answering.** At your level the wrong options are often "almost right". Eliminate confidently wrong answers first, then compare what remains.
- **Use the untimed practice questions platforms offer.** They exist so the interface never surprises you. Do them all, even if they feel easy.
- **Simulate light time pressure.** Once you are comfortable, give yourself about 60–90 seconds per question. Accuracy first, speed second — speed comes naturally with familiarity.
- **Sleep and setup matter.** Take the real test rested, on a reliable connection, with paper and a pen for working. Small practical preparations noticeably improve scores.
- **Ask your team.** Experienced engineers on your team have done these assessments before. Asking how they approach them is exactly the kind of learning-under-direction your role is designed around.

### Common pitfalls to avoid

- **Trusting the first glance.** Pattern questions are designed so the broken entry looks normal at speed. Check each part of each entry against the rule.
- **Concluding more than the facts allow.** "Must be true" means true in every possible case, not "probably true". If you can imagine a situation where the facts hold but the conclusion fails, it is not the answer.
- **Reading rules backwards.** "All production servers are backed up" does not mean "everything backed up is a production server". Watch for this reversal — it is the most common logic trap.
- **Prioritising by queue order or loudness.** Impact and urgency decide priority. An old low-impact ticket does not outrank a new whole-service outage.
- **Trying to fix instead of route.** Some situational-flavoured cognitive questions reward escalation, not heroics. At associate level, "flag it promptly with good evidence" is usually the strongest action.
- **Panicking when questions get harder.** Adaptive tests raise difficulty when you are doing well. Feeling stretched is a sign of success, not failure.
- **Leaving answers blank.** Unless the instructions say wrong answers are penalised, an educated elimination-based guess is always better than a blank.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your role genuinely produces: disk space figures, ticket counts, uptime percentages, patching completion rates, bandwidth readings, and simple cost tables. It is not a maths exam. There is no algebra, no trigonometry, and nothing you did not meet at school — the mathematics is percentages, ratios, averages, rates, and reading tables and charts. What the assessment really measures is whether you can extract the right numbers from realistic workplace data and do simple calculations with them carefully, sometimes under mild time pressure.

The typical format is an online, timed test lasting 20 to 30 minutes with 15 to 20 questions. Each question presents a small data set — a table of ticket volumes, a chart of server capacity, a summary of an invoice — followed by a multiple-choice question. Calculators are usually allowed (check the instructions each time), and rough paper is strongly recommended. Scores compare your accuracy and speed against a norm group at a similar level. As with cognitive tests, many platforms adapt difficulty as you go.

Why do employers use numeric assessments for associate infrastructure engineers? Because infrastructure runs on numbers. When you support storage, you read capacity figures. When you help with monitoring, you read utilisation percentages. When your team reports to management, someone counts tickets, measures uptime, and tracks patching progress. Even as a trainee working under direction, you will be asked to gather figures, sanity-check them, and notice when a number looks wrong — a disk filling faster than expected, an uptime figure that does not match the outage you remember. Employers want to know that numbers are a tool you can handle, not a source of anxiety. The friendly truth is that everything in this section is learnable with practice, and every question below shows its arithmetic step by step so you can borrow the method.

### How this assessment maps to your role

- **Percentages and capacity calculations** map to your **IT infrastructure** skill: supporting storage, computing, and networking means constantly reading "used versus total" figures — disk usage, memory usage, licence counts — and converting between absolute numbers and percentages.
- **Rates and trends** map to your **Problem management** skill: investigating problems often means asking "how fast is this growing?" — a disk filling at 2 GB a day, a ticket type rising week on week — and contributing to preventative measures before the trend becomes an incident.
- **Averages and comparisons** map to your **Troubleshooting and problem resolution** skill: a server whose response time is far above the average of its identical twins is a clue, and recognising it requires comfortable, accurate averaging.
- **Reading tables and charts** maps to your **Ownership and topic** skill and your awareness of problem resolution processes: ticket queues, SLA reports, and monitoring dashboards are all tables and charts, and routing problems correctly depends on reading them correctly.
- **Simple proportional reasoning** maps to your **Systems design** and **Systems integration** skills: assisting with component design and understanding interfaces involves sizing questions — if one server handles 200 users, how many servers do 900 users need? — that are ratio problems in work clothes.

### Practice questions

**Question 1 (easy) — Disk space percentage**

A file server has a 500 GB disk. The monitoring dashboard shows 350 GB used. What percentage of the disk is used?

- A) 60%
- B) 65%
- C) 70%
- D) 75%

**Correct answer: C**

**Explanation:** Percentage used = used ÷ total × 100. Step 1: 350 ÷ 500 = 0.7. Step 2: 0.7 × 100 = 70%. So the disk is 70% used. A quick sanity check: half of 500 is 250, so 350 is clearly more than half (50%) but less than four-fifths (400 GB would be 80%), and 70% sits comfortably in that range. Sanity-checking against easy landmarks like 50% and 80% catches most slips. You will read "used versus total" figures like this daily when supporting storage as part of your **IT infrastructure** work, and many teams have alert thresholds at 70%, 80%, and 90% — so translating between gigabytes and percentages is genuinely everyday work, not exam artifice.

**Question 2 (easy) — Counting tickets**

Last week your team closed the following numbers of tickets: Monday 12, Tuesday 15, Wednesday 9, Thursday 14, Friday 10. What was the average (mean) number of tickets closed per day?

- A) 11
- B) 12
- C) 13
- D) 14

**Correct answer: B**

**Explanation:** The mean = total ÷ number of days. Step 1: add the daily figures: 12 + 15 = 27; 27 + 9 = 36; 36 + 14 = 50; 50 + 10 = 60. Step 2: divide by the 5 days: 60 ÷ 5 = 12. The average is 12 tickets per day. Tip: when adding a short list, add in pairs that make round numbers where you can (12 + 9 = 21, 15 + 14 = 29 is less round — so just add steadily and write down the running total). Averages like this appear in every weekly team report, and knowing the average matters because it gives you a baseline: a day with 25 closures or 3 closures then stands out as worth a question — which is the beginning of the pattern-and-trend thinking your **Problem management** skill describes.

**Question 3 (easy) — Uptime percentage**

A service is expected to be available 24 hours a day. Yesterday it was down for 36 minutes. Roughly what was its availability percentage for the day? (There are 1,440 minutes in a day.)

- A) 92.5%
- B) 95.0%
- C) 97.5%
- D) 99.5%

**Correct answer: C**

**Explanation:** Step 1: minutes up = 1,440 − 36 = 1,404. Step 2: availability = 1,404 ÷ 1,440 × 100. Step 3: 1,404 ÷ 1,440 = 0.975. Step 4: 0.975 × 100 = 97.5%. A faster route: work out the downtime percentage first — 36 ÷ 1,440 = 0.025 = 2.5% — then subtract from 100% to get 97.5%. The subtraction route is usually quicker and less error-prone, and it is how availability is calculated in real service reports. Availability percentages are the common currency of infrastructure services — you will see targets like 99.5% or 99.9% in service level agreements — so being able to convert between "minutes down" and "percentage available" helps you understand what your team is being measured against.

**Question 4 (easy) — Reading a simple table**

The patching report for your four servers reads:

| Server | Patches required | Patches applied |
|---|---|---|
| LNWEB01 | 20 | 20 |
| LNWEB02 | 20 | 15 |
| LNAPP01 | 30 | 24 |
| LNDBS01 | 10 | 10 |

Which server has the lowest percentage of required patches applied?

- A) LNWEB01
- B) LNWEB02
- C) LNAPP01
- D) LNDBS01

**Correct answer: B**

**Explanation:** Calculate each percentage. LNWEB01: 20 ÷ 20 = 100%. LNWEB02: 15 ÷ 20 = 0.75 = 75%. LNAPP01: 24 ÷ 30 = 0.8 = 80%. LNDBS01: 10 ÷ 10 = 100%. The lowest is LNWEB02 at 75%. Note the trap: LNAPP01 has the most missing patches in absolute terms (6 missing versus LNWEB02's 5), but the question asks about percentage, and 5 missing out of 20 (25% missing) is proportionally worse than 6 missing out of 30 (20% missing). Assessments — and real patching reports — frequently mix absolute counts and percentages, so always re-read the question to check which one is being asked for. Patch compliance percentages are a standard security measure, connecting directly to your **Information security** awareness of the controls that protect services.

**Question 5 (moderate) — Disk growth rate**

A log disk currently holds 240 GB of data on a 400 GB volume. The data is growing steadily at 8 GB per week. In how many weeks will the disk reach its 90% alert threshold?

- A) 10 weeks
- B) 15 weeks
- C) 20 weeks
- D) 25 weeks

**Correct answer: B**

**Explanation:** Step 1: find the 90% threshold in gigabytes: 90% of 400 = 0.9 × 400 = 360 GB. Step 2: find the remaining headroom: 360 − 240 = 120 GB. Step 3: divide headroom by the weekly growth rate: 120 ÷ 8 = 15 weeks. So the alert will trigger in 15 weeks. Common errors: using the full 400 GB instead of the 360 GB threshold (giving 160 ÷ 8 = 20 weeks, option C), or forgetting to subtract the current usage. This "when will we hit the threshold?" calculation is one of the most genuinely useful pieces of arithmetic in infrastructure support: it turns a monitoring number into a forecast, which lets your team plan a fix calmly instead of reacting to an alert at 2 a.m. — exactly the preventative thinking your **Problem management** skill asks you to contribute to.

**Question 6 (moderate) — Ratio for sizing**

Guidance says one application server comfortably supports 150 concurrent users. A new internal service is expected to have 620 concurrent users at peak. Following the guidance, how many application servers are needed at minimum?

- A) 3
- B) 4
- C) 5
- D) 6

**Correct answer: C**

**Explanation:** Step 1: divide users by capacity per server: 620 ÷ 150 = 4.13 (to two decimal places). Step 2: because you cannot deploy a fraction of a server, and 4 servers would only support 4 × 150 = 600 users — leaving 20 users unsupported at peak — you must round up to 5 servers. Rounding up in capacity questions is the rule: rounding 4.13 down to 4 (option B) is the classic error, and in real life it produces a service that falls over at peak. Check: 5 × 150 = 750 ≥ 620, so 5 works. This is proportional reasoning applied to sizing, the same arithmetic you will meet when assisting with component design as part of your **Systems design** skill — designs are full of "how many do we need?" questions, and the answer is always "divide, then round up".

**Question 7 (moderate) — Percentage change in incidents**

In March your team logged 160 incidents. In April the team logged 184 incidents. What was the percentage increase from March to April?

- A) 12%
- B) 15%
- C) 18%
- D) 24%

**Correct answer: B**

**Explanation:** Percentage change = (new − old) ÷ old × 100. Step 1: find the change: 184 − 160 = 24. Step 2: divide by the original (March) figure: 24 ÷ 160 = 0.15. Step 3: multiply by 100: 15%. The most common error is dividing by the new figure (24 ÷ 184 ≈ 13%) — remember, percentage change is always measured against the starting value. Another trap is option D, which is just the raw difference (24) dressed as a percentage. A 15% month-on-month rise in incidents is the kind of trend your team would investigate: is it a one-off (a big outage generating many tickets) or a pattern (a failing component generating steady noise)? Spotting and quantifying the trend is the first contribution you can make to that investigation.

**Question 8 (moderate) — Bandwidth and transfer time**

You need to copy a 90 GB backup file to another site over a link that sustains 60 MB per second. Roughly how long will the transfer take? (Use 1 GB = 1,000 MB.)

- A) 15 minutes
- B) 25 minutes
- C) 40 minutes
- D) 90 minutes

**Correct answer: B**

**Explanation:** Step 1: convert the file size to megabytes: 90 GB × 1,000 = 90,000 MB. Step 2: divide by the transfer rate: 90,000 ÷ 60 = 1,500 seconds. Step 3: convert to minutes: 1,500 ÷ 60 = 25 minutes. So the transfer takes about 25 minutes. The unit conversions are where errors creep in: keep writing the units next to your numbers (MB, MB/s, seconds, minutes) and check they cancel sensibly. In real work you would also allow a margin because links rarely sustain their headline rate perfectly — but the assessment wants the clean calculation. Time-to-transfer arithmetic matters whenever your team moves backups, restores data during an incident, or plans a migration window: "how long will this take?" is often the first question a supervisor asks, and being able to answer it from rate and size is a quiet superpower for an associate.

**Question 9 (moderate) — Reading a chart of CPU usage**

A bar chart shows average CPU usage for server LNAPP01 across five days: Monday 40%, Tuesday 45%, Wednesday 85%, Thursday 44%, Friday 41%. The team considers anything above 80% "high". Which statement best describes the week?

- A) CPU usage was high all week.
- B) CPU usage was normal all week.
- C) CPU usage was normal except for a spike on Wednesday, which deserves investigation.
- D) CPU usage rose steadily through the week.

**Correct answer: C**

**Explanation:** Compare each day against the 80% threshold: Monday 40 (normal), Tuesday 45 (normal), Wednesday 85 (high), Thursday 44 (normal), Friday 41 (normal). Four days cluster in the low 40s and one day spikes above the threshold — that is a single outlier, not a steady rise (eliminating D) and not a uniformly high or normal week (eliminating A and B). The professional habit is in the second half of option C: an outlier "deserves investigation", not instant alarm — perhaps a batch job ran, perhaps a backup overlapped with a busy period, perhaps something genuinely misbehaved. Reading charts against thresholds and spotting outliers is precisely how monitoring dashboards are used in your **Troubleshooting and problem resolution** work: the chart tells you where to look, and the investigation tells you what it means.

**Question 10 (hard) — Combining percentages across servers**

Your team manages 60 Windows servers and 40 Linux servers. This month, 90% of the Windows servers and 75% of the Linux servers were fully patched. How many servers in total were fully patched, and what percentage of the whole estate is that?

- A) 84 servers; 84%
- B) 82 servers; 82%
- C) 84 servers; 82.5%
- D) 80 servers; 80%

**Correct answer: A**

**Explanation:** Work each group separately, then combine. Step 1: Windows: 90% of 60 = 0.9 × 60 = 54 servers. Step 2: Linux: 75% of 40 = 0.75 × 40 = 30 servers. Step 3: total patched = 54 + 30 = 84 servers. Step 4: total estate = 60 + 40 = 100 servers, so the overall percentage = 84 ÷ 100 = 84%. Because the estate happens to total 100, the count and the percentage match. Note the tempting error in option C: averaging the two percentages (90% and 75%) gives 82.5%, but a simple average is wrong when the groups are different sizes — the Windows group is bigger, so it pulls the overall figure up. This "weighted versus simple average" distinction is one of the most common traps in workplace numeric tests and in real compliance reporting alike: always go back to the underlying counts.

**Question 11 (hard) — SLA arithmetic across a month**

A service has a 99.5% monthly availability target. In a 30-day month, how many minutes of downtime can the service have while still meeting the target, and did it meet the target if it actually had 3 hours 20 minutes of downtime? (30 days = 43,200 minutes.)

- A) Allowance 216 minutes; actual 200 minutes; target met
- B) Allowance 216 minutes; actual 220 minutes; target missed
- C) Allowance 432 minutes; actual 200 minutes; target met
- D) Allowance 216 minutes; actual 200 minutes; target missed

**Correct answer: A**

**Explanation:** Step 1: the allowed downtime is 100% − 99.5% = 0.5% of the month. Step 2: 0.5% of 43,200 minutes = 0.005 × 43,200 = 216 minutes. Step 3: convert the actual downtime: 3 hours 20 minutes = (3 × 60) + 20 = 180 + 20 = 200 minutes. Step 4: compare: 200 ≤ 216, so the target was met — option A. Option B miscalculates the actual downtime (3 hours 40 minutes would be 220). Option C doubles the allowance by using 1% instead of 0.5%. Option D does the arithmetic correctly but draws the wrong conclusion — a reminder to finish the question, not just the calculation. SLA arithmetic like this is the backbone of service reporting: your team lives against availability targets, and understanding how minutes convert into percentages helps you see why a 20-minute outage at month-end can cause so much concern when the allowance is nearly spent.

**Question 12 (hard) — Cost comparison table**

Your team is choosing between two support options for a software package used on 25 servers. Option 1: £40 per server per month. Option 2: a flat £700 per month for up to 20 servers, plus £25 per month for each server above 20. Over a full year, how much cheaper is the better option?

- A) £1,500 cheaper
- B) £2,100 cheaper
- C) £1,800 cheaper
- D) The options cost the same

**Correct answer: B**

**Explanation:** Cost each option per month, then per year. Step 1 — Option 1: 25 servers × £40 = £1,000 per month. Step 2 — Option 2: the flat £700 covers the first 20 servers; the extra 5 servers cost 5 × £25 = £125; total = £700 + £125 = £825 per month. Step 3 — monthly saving with the cheaper option (Option 2): £1,000 − £825 = £175. Step 4 — yearly saving: £175 × 12 = £175 × 10 + £175 × 2 = £1,750 + £350 = £2,100. So the better option is £2,100 cheaper over a year — option B. Option C (£1,800) comes from the common slip of costing the extra servers at £40 instead of £25 (£850 per month gives £150 × 12 = £1,800); option A comes from forgetting the extra-server charge entirely. Finish with a verification pass: recompute the key steps a different way (here, confirm 25 × 40 and 700 + 125 separately) before committing. Cost comparisons like this are real associate-level work — teams regularly check invoices and licence tiers against actual server counts, and a careful pair of eyes on the arithmetic saves genuine money.

### Preparation tips

- **Refresh the core four:** percentages, averages, ratios, and rates cover almost every question. Ten minutes a day with everyday examples (discounts, journey times, sharing a bill) rebuilds fluency quickly.
- **Always write the calculation down.** Even with a calculator, jotting "350 ÷ 500 × 100" before typing prevents the most common slip: dividing the wrong way round.
- **Learn the threshold shortcuts.** 10% is "shift the decimal", 5% is half of that, 1% is shift twice. Most workplace percentages can be built from these blocks in your head.
- **Practise reading tables before calculating.** Half the errors in numeric tests are extraction errors — right maths, wrong row. Point at the row and column (physically, if allowed) before you compute.
- **Check which figure the question wants.** Absolute number or percentage? Increase or final value? Per month or per year? Circle the units in the question.
- **Use your own dashboards.** Your monitoring tools and ticket reports are free practice material. Recreate the calculations in this section using this week's real numbers.
- **Round for sanity, calculate for accuracy.** Estimate a ballpark answer first (620 users ÷ 150 per server ≈ "a bit more than 4"), then calculate exactly. If the two disagree, investigate before answering.

### Common pitfalls to avoid

- **Dividing by the wrong base.** Percentage change uses the original value; patch compliance uses the required count; availability uses total minutes. Ask "out of what?" every time.
- **Rounding down when capacity says round up.** 4.13 servers means 5 servers. Fractions of a server, engineer, or licence do not exist.
- **Averaging percentages from different-sized groups.** Combine the underlying counts, then convert to a percentage at the end.
- **Unit slips.** GB versus MB, hours versus minutes, per-month versus per-year. Write units beside every number and make them cancel.
- **Answering the calculation instead of the question.** You may compute 216 minutes correctly and still pick the wrong option if you forget to make the final comparison.
- **Losing time on one hard question.** Every question is usually worth the same. If a question is consuming minutes, make your best elimination-based choice, flag it if the platform allows, and move on.
- **Skipping the sanity check.** A two-second "is this plausible?" glance — an availability of 97.5%, a transfer of 25 minutes — catches order-of-magnitude errors that pure calculation confidence misses.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand and evaluate written information of the kind your role really uses: security policy extracts, change procedures, supplier emails, incident reports, and knowledge-base articles. The classic format presents a short passage followed by statements you must judge as **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage gives you neither enough support nor a contradiction). Other question types ask you to pick the best summary of a passage, identify what can properly be inferred, or choose the clearest rewrite of a clumsy sentence.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions. The golden rule throughout is: judge every statement using only the passage in front of you, not your background knowledge. This feels strange for technical people, because you know things about servers and networks that a passage might not mention — but the test is measuring careful reading, not technical knowledge, so what you know must sit quietly while what the passage says does the talking.

Why do employers use verbal reasoning tests for associate infrastructure engineers? Because your working day is full of text that must be understood exactly. A runbook step misread is a service broken. A security policy skimmed is a control missed. An email from a supplier half-understood becomes a wrong configuration on a live system. At your level you are often the person turning written instructions into careful actions under direction, so precise reading is arguably the most job-relevant skill an assessment can measure. And there is a second reason: government work runs on clear writing — tickets you update, handover notes you leave, and questions you ask in writing all need to be understandable. Verbal assessments check both directions: reading accurately and recognising clear writing when you see it.

### How this assessment maps to your role

- **Reading policies and controls precisely** maps to your **Information security** skill: explaining information security and the security controls available to protect solutions and services starts with reading control descriptions exactly — what is mandatory, what is recommended, and what is conditional.
- **Following written procedures** maps to your **IT infrastructure** skill: supporting solutions, COTS software, and cloud services is guided by runbooks, vendor documentation, and departmental policy, all of which reward the careful, literal reading these tests measure.
- **Distinguishing fact from assumption** maps to your **Problem management** and **Troubleshooting and problem resolution** skills: an incident report tells you what was observed; a good investigator refuses to "read in" causes the report does not state — which is precisely the discipline behind "Cannot say".
- **Understanding explanations of process** maps to your **Systems integration** and **Modern development standards** skills: explaining the principles of integrating systems and the importance of modern development standards means digesting written explanations and repeating them accurately to others.
- **Knowing when to pass information on** maps to your **Ownership and topic** skill: passing problems to your team effectively depends on reading a ticket well enough to summarise it faithfully.

### Practice questions

**Question 1 (easy) — True/False/Cannot say on a backup policy**

Passage: "All production servers must be backed up every night. Backup copies must be retained for 30 days. Test servers may be backed up at the discretion of the service team, but any backup taken of a test server must also be retained for 30 days."

Statement: "Test servers must be backed up every night."

- A) True
- B) False
- C) Cannot say
- D) True, but only at weekends

**Correct answer: B**

**Explanation:** The passage says test server backups are "at the discretion of the service team" — meaning optional, decided case by case. The statement claims they are compulsory every night, which directly contradicts the discretionary wording, so the answer is False. Notice the structure of the policy: one mandatory rule (production, nightly), one discretionary rule (test, optional), and one condition that applies once a choice is made (30-day retention either way). Assessment writers love placing "must" and "may" close together because skim-readers merge them. In your **Information security** and backup work, the must/may distinction is exactly the difference between a compliance breach and a local choice — so train your eye to slow down on those two little words.

**Question 2 (easy) — Comprehension of a service desk email**

Passage (email from the service desk): "Hi team — we're seeing repeated reports from floor 2 that the wifi drops out around 10:00 each morning. It reconnects by itself after a few minutes. No reports from other floors so far. Could someone take a look when you get a chance? It's annoying rather than urgent, but it's been happening all week."

Which summary best captures the email?

- A) The whole building loses wifi every morning and it is urgent.
- B) Floor 2 has a recurring, self-resolving wifi drop-out around 10:00 each morning; it is low urgency but persistent.
- C) Floor 2's wifi has failed permanently and needs immediate replacement.
- D) The service desk has fixed a wifi problem on floor 2.

**Correct answer: B**

**Explanation:** Test each summary against the email's facts. Option A over-extends "floor 2" to the whole building and contradicts "annoying rather than urgent". Option C contradicts "it reconnects by itself". Option D claims a fix the email never mentions — the desk is asking for help, not reporting a resolution. Option B matches every element: the location (floor 2), the pattern (around 10:00, all week), the behaviour (self-resolving after a few minutes), and the urgency ("annoying rather than urgent, but persistent"). Summarising a ticket faithfully — neither inflating nor shrinking it — is a daily associate task: when you pass a problem to your team, as your **Ownership and topic** skill describes, the team acts on your summary, so its accuracy directly shapes what happens next. The time pattern ("around 10:00 each morning") is also a genuine troubleshooting clue worth preserving.

**Question 3 (easy) — Cannot say discipline**

Passage: "The department's standard build for laptops includes full-disk encryption, automatic screen locking after five minutes, and the approved antivirus package. Laptops that do not meet the standard build must not connect to the departmental network."

Statement: "The department's laptops are more secure than its desktop computers."

- A) True
- B) False
- C) Cannot say
- D) True, because encryption makes laptops secure

**Correct answer: C**

**Explanation:** The passage describes laptop controls only. It says nothing at all about desktop computers — their encryption, locking, antivirus, or anything else. Without any information about desktops, you cannot compare the two, so the answer is Cannot say. This is the discipline the True/False/Cannot say format exists to test: the statement is not contradicted (so not False), but it is not supported either (so not True). Option D shows the classic trap — using your own technical reasoning ("encryption is good, so laptops must be more secure") to fill the gap the passage leaves. Your outside knowledge may even be correct, but the test asks what the passage establishes. The same discipline protects your incident notes at work: record what you observed, and resist recording what you merely assume.

**Question 4 (easy) — Choosing the clearest rewrite**

Your teammate drafts this ticket update: "The issue pertaining to the aforementioned server's non-functionality was in due course subjected to investigation by the undersigned, and remediation was effectuated via a restart." Which rewrite is clearest while keeping the meaning?

- A) "I investigated the server issue and fixed it by restarting the server."
- B) "The server issue, having been investigated, was resolved through the medium of a restart operation."
- C) "Investigation of non-functionality was effectuated; restart remediation followed."
- D) "The server was broken so somebody did something and now it's probably fine."

**Correct answer: A**

**Explanation:** Clear writing says who did what, in plain words, in natural order. Option A does exactly that: I investigated; I restarted; it is fixed — three facts, twelve words. Option B keeps the pompous passive constructions ("through the medium of"). Option C compresses the jargon but keeps it, and loses the actor entirely. Option D is informal to the point of being useless: "somebody did something" and "probably fine" destroy the information a ticket exists to record. Government guidance on writing — which underpins GOV.UK content and good operational records alike — favours short sentences, active voice, and everyday words. Your ticket updates and handover notes are read by colleagues at 3 a.m. during incidents; writing them like option A is a genuine act of teamwork.

**Question 5 (moderate) — Inference from a change procedure**

Passage: "Standard changes are pre-approved, low-risk changes with a documented, repeatable procedure — for example, adding disk space to a virtual server. Normal changes require assessment and approval by the Change Advisory Board (CAB), which meets every Wednesday. Emergency changes may be implemented before approval, but must be reviewed retrospectively by the CAB at its next meeting."

Statement: "A change implemented on Friday to resolve a major outage, without prior approval, must be reviewed by the CAB the following Wednesday."

- A) True
- B) False
- C) Cannot say
- D) True, but only if the change fails

**Correct answer: A**

**Explanation:** Chain the passage's rules together. A change implemented before approval to resolve a major outage fits the emergency change description ("may be implemented before approval"). Emergency changes "must be reviewed retrospectively by the CAB at its next meeting". The CAB "meets every Wednesday". A change made on Friday therefore faces the CAB at the next Wednesday meeting. Every link is stated in the passage; joining them is inference, but supported inference — which makes the statement True rather than Cannot say. Option D adds a condition (only if it fails) that appears nowhere. Distinguishing supported inference (combining things the passage says) from unsupported assumption (adding things it does not) is the heart of moderate-level verbal questions — and of reading real change procedures, where the obligations that bite are often the ones you must assemble from two separate sentences.

**Question 6 (moderate) — Reading a security control description**

Passage: "Multi-factor authentication (MFA) is required for all remote access to departmental systems. On-site access from managed devices connected to the wired network does not require MFA. Access from personal devices is prohibited regardless of location or authentication method."

Statement: "A member of staff working from home on a departmental laptop can access departmental systems if they use MFA."

- A) True
- B) False
- C) Cannot say
- D) False, because home working is prohibited

**Correct answer: A**

**Explanation:** Classify the scenario against each rule. Working from home is remote access, so the MFA requirement applies. The device is a departmental laptop, not a personal device, so the prohibition on personal devices does not apply. The staff member uses MFA, satisfying the requirement. Nothing in the passage blocks the access, and the MFA rule positively provides the route, so the statement is True. Option D invents a prohibition on home working the passage never states — it prohibits personal devices, which is a different thing. This question rehearses a skill at the centre of your **Information security** duties: reading a control and applying it to a concrete case. Real security policies work exactly like this passage — a general rule, an exception, and an absolute prohibition — and support engineers are often the first person a colleague asks "am I allowed to…?" Reading precisely lets you answer correctly or escalate wisely.

**Question 7 (moderate) — Identifying the main point of a standards passage**

Passage: "Modern development standards — such as version control for all configuration, automated testing, and infrastructure as code — are not only for software developers. When infrastructure teams keep server configurations in version control, changes become visible, reversible, and reviewable. When they automate testing of changes, mistakes are caught before they reach live services. Teams that adopt these standards spend less time firefighting and more time improving services."

What is the main point of the passage?

- A) Software developers should learn about infrastructure.
- B) Version control is too complicated for infrastructure teams.
- C) Modern development standards benefit infrastructure teams, not just developers.
- D) Automated testing eliminates all mistakes.

**Correct answer: C**

**Explanation:** The passage's opening sentence announces the thesis — these standards "are not only for software developers" — and every following sentence supports it with infrastructure-specific benefits: visibility and reversibility from version control, early error detection from automated testing, less firefighting overall. Option A reverses the direction of the argument. Option B contradicts the passage's positive tone. Option D overstates: the passage says mistakes are "caught before they reach live services", not eliminated — absolute words like "all" and "eliminates" in an answer option should always send you back to check the passage's actual strength of claim. Recognising main points quickly helps with your **Modern development standards** skill, which asks you to explain the importance of these standards — and explaining well starts with identifying the core message accurately.

**Question 8 (moderate) — True/False/Cannot say on a supplier notice**

Passage (supplier notice): "From 1 September, version 4 of the storage management software will no longer receive security updates. Customers on version 4 are advised to upgrade to version 5 before this date. Version 5 requires a minimum of 16 GB of memory on the management server. Customers with a current support contract can upgrade at no additional licence cost."

Statement: "Customers who stay on version 4 after 1 September will experience a security breach."

- A) True
- B) False
- C) Cannot say
- D) True, because unsupported software is always breached

**Correct answer: C**

**Explanation:** The notice says version 4 will stop receiving security updates — which increases risk — but it makes no claim that a breach will occur. "Will experience a security breach" is a prediction the passage neither supports nor contradicts: staying on version 4 might lead to a breach, or might not. So the answer is Cannot say. Option D's word "always" is doing dishonest work: unsupported software is riskier, not automatically breached, and in any case the passage does not say it. Notice also what the passage does establish, because a follow-up question could test it: the deadline (1 September), the memory prerequisite (16 GB), and the licence cost condition (free only with a current support contract). Reading supplier notices with this precision is real associate work — your team will ask "what exactly does the notice commit us to, and by when?" and the careful reader answers from the text.

**Question 9 (moderate) — Inference from an incident report**

Passage (incident report extract): "At 14:05 users began reporting slow file access. At 14:20 monitoring confirmed high latency on the storage network. At 14:35 engineers identified a failed network card in storage switch B; traffic had automatically failed over to switch A, which was carrying double its usual load. The card was replaced at 16:10 and latency returned to normal by 16:25. No data was lost."

Which statement can properly be inferred from the report?

- A) Switch A cannot handle failover traffic.
- B) The failover mechanism worked, but performance degraded while one switch carried the full load.
- C) Users lost files during the incident.
- D) The network card failed because of poor maintenance.

**Correct answer: B**

**Explanation:** Option B assembles only what the report states: traffic "automatically failed over" (so the mechanism worked — the service stayed up), and switch A carried "double its usual load" while users experienced slowness (so performance degraded under single-switch load). Option A overstates: switch A did handle the traffic — with degraded performance, not failure. Option C is contradicted by "No data was lost". Option D invents a cause: the report says the card failed, not why. This mirrors the reading discipline your **Problem management** skill requires when you investigate problems: the report gives observations and confirmed findings; causes beyond those findings are hypotheses to investigate, not facts to assert. In a real post-incident review, the difference between "the card failed" and "maintenance was poor" is the difference between evidence and accusation.

**Question 10 (hard) — Two conditions interacting in a policy**

Passage: "Administrative access to production servers is granted only to staff who have completed the privileged-access training and hold a current security clearance. Training completions expire after two years. Where clearance is under routine renewal, access may continue provided the renewal application was submitted before the previous clearance expired."

Statement: "A staff member whose training was completed 18 months ago, and whose clearance expired last week without a renewal application being submitted, may retain administrative access."

- A) True
- B) False
- C) Cannot say
- D) True, because the training is still valid

**Correct answer: B**

**Explanation:** The policy requires both conditions: current training and current clearance. Check each. Training: completed 18 months ago, expiry is at two years, so training is still valid. Clearance: expired last week. The continuation provision applies only "provided the renewal application was submitted before the previous clearance expired" — and the statement says no application was submitted. So the clearance condition fails, and the exception cannot rescue it. With one required condition failed, access may not be retained: the statement is False. Option D shows the "one good condition" trap — a conjunction ("and") needs every part true, and a valid training record cannot compensate for lapsed clearance. Access-control policies in government genuinely read like this passage, and applying them correctly is part of explaining security controls under your **Information security** skill. The technique: list each required condition, check each independently, and remember that any single failure fails the whole.

**Question 11 (hard) — Evaluating an argument in an email**

Passage (email from a colleague): "We should stop applying the monthly patches to the print servers. In the last six months, two of our print outages happened within a day of patching. Patching takes the servers down for twenty minutes anyway, so users lose printing either way. Skipping patches would give users a more reliable service."

Which is the strongest criticism of the argument?

- A) It relies on only two incidents and ignores the security risk that patching exists to reduce, so the conclusion does not follow from the evidence.
- B) Print servers never have outages after patching.
- C) Twenty minutes of downtime is too long to be acceptable.
- D) Users do not care about printing reliability.

**Correct answer: A**

**Explanation:** Evaluate what the argument claims versus what its evidence supports. Two outages "within a day of patching" in six months is a small sample, and closeness in time does not prove the patches caused the outages. More importantly, the argument counts only the costs of patching (brief downtime, possible instability) and entirely omits its purpose — closing security vulnerabilities — so "more reliable service" ignores the risk of unpatched servers being compromised, which would cause far worse outages. Option A captures both flaws: weak evidence and a missing consideration. Option B is factually contradicted by the email itself. Options C and D are opinions that neither strengthen nor weaken the logic. Weighing arguments like this matters even at associate level: colleagues will propose shortcuts with persuasive-sounding reasoning, and your **Modern development standards** and **Information security** awareness equips you to ask the quiet, useful question — "what does this control exist to prevent?"

**Question 12 (hard) — Precision across a whole passage**

Passage: "The data centre migration will proceed in three phases. Phase 1 moves development and test systems and is complete. Phase 2, scheduled for October, moves internal business systems; it requires a four-hour outage of each system, agreed with system owners at least two weeks in advance. Phase 3, moving public-facing services, will be scheduled only after a review of Phase 2, and no earlier than January. Any system found to have unsupported operating systems will not be migrated until upgraded."

Which statement is supported by the passage?

- A) Phase 3 will take place in January.
- B) A business system whose owner agreed an outage window one week in advance can be migrated in Phase 2 as planned.
- C) Development systems have already been moved, and a public-facing service running an unsupported operating system will not be migrated before it is upgraded.
- D) The Phase 2 review has already begun.

**Correct answer: C**

**Explanation:** Check each option against the exact wording. Option A converts "no earlier than January" into "in January" — a floor is not a date, so unsupported. Option B fails the stated condition: outages must be agreed "at least two weeks in advance", and one week breaches it. Option D refers to a review that can only happen after Phase 2, which is scheduled for October and not stated as complete — unsupported. Option C joins two things the passage does state: Phase 1 (development and test) "is complete", so development systems have moved; and the final sentence applies to "any system", which includes public-facing services, so an unsupported operating system blocks migration until upgraded. Long passages reward systematic elimination: test each option's every clause, and prefer the option whose every part you can point to in the text. That habit — every claim anchored to a source sentence — is exactly how you should read migration plans and policies in your **IT infrastructure** work.

### Preparation tips

- **Practise the three-way judgement daily.** Take any policy or news paragraph, write three statements about it, and label them True, False, or Cannot say. The "Cannot say" habit is the one that needs most practice.
- **Read the statement before re-reading the passage.** Knowing what you are checking makes your second read targeted and fast.
- **Underline the modal verbs.** Must, may, should, can, will, might — these small words carry the obligations. Most wrong answers turn a "may" into a "must" or vice versa.
- **Park your technical knowledge.** Before answering, ask: "does the passage say this, or do I just know it?" Only the passage counts.
- **Watch for absolute words in options.** "Always", "never", "all", "eliminates" usually overstate a passage's careful claim — check the original strength of wording.
- **Practise with real work documents.** Your department's security policy, change procedure, and supplier notices are ideal material — and reading them closely doubles as job learning.
- **Summarise tickets in one sentence.** After reading any ticket at work, silently compose a one-sentence faithful summary. This trains the same comprehension the test scores.

### Common pitfalls to avoid

- **Using outside knowledge.** The most common error for technical candidates. The passage is the whole world; answer from it alone.
- **Confusing "not supported" with "contradicted".** A statement the passage does not mention is Cannot say, not False. False requires the passage to say the opposite.
- **Skimming policy exceptions.** The "unless", "provided that", and "regardless of" clauses usually decide the answer. Slow down when you meet one.
- **Letting tone sway judgement.** A friendly email can contain an unjustified conclusion; a dry policy can be perfectly logical. Judge content, not style.
- **Over-reading causes into reports.** "The card failed" does not tell you why it failed. Treat unstated causes as unknown.
- **Choosing summaries that add drama.** The best summary neither inflates ("whole building down!") nor deflates ("minor blip") the passage's actual claims.
- **Spending too long on one passage.** If a statement resists judgement after two careful reads, choose your best answer and move on — accuracy across the whole test beats perfection on one item.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of different responses. Unlike cognitive, numeric, and verbal tests, there is often no mathematically provable answer — instead, responses are scored against the judgement of experienced professionals and the behaviours the organisation values. Common formats include: choose the most effective response; choose the most and least effective responses; rank all responses from best to worst; or rate each response independently on an effectiveness scale.

The typical format is an online test of 15 to 25 minutes with 10 to 20 scenarios. It may be untimed or generously timed, because it measures judgement rather than speed. There are no trick questions, but there are carefully written "plausible but flawed" options — responses that feel decisive or helpful but cut a corner that matters, such as skipping an escalation, guessing instead of checking, or protecting your own comfort at a user's expense.

Why do employers use SJTs for associate infrastructure engineers? Because at your level, judgement about how to act matters even more than technical knowledge. You work under direction in an established team, which raises constant small dilemmas: when do I try something myself and when do I ask? What do I do when I spot something wrong that nobody has noticed? How do I respond when I have made a mistake? What comes first when two people want help at once? The safe, professional answers to these questions are what keep live public services stable while you learn. The behaviours that score well are consistent and learnable: focus on users, be honest — especially about mistakes — ask for help early, follow the process, take ownership of handing things over properly, and treat colleagues with respect. This section lets you rehearse those behaviours in scenarios drawn from your real working world.

### How this assessment maps to your role

- **Escalation and passing problems on** maps directly to your **Ownership and topic** skill: showing awareness of problem resolution processes and passing problems to your team is the professional behaviour most SJT scenarios at your level test — not whether you can fix everything, but whether you route things well.
- **Careful, honest handling of incidents** maps to your **Problem management** skill: contributing to the investigation of problems and to remedies and preventative measures requires honesty about what happened, including your own errors.
- **Safe hands with live systems** maps to your **IT infrastructure** and **Information security** skills: scenarios about changes, access requests, and security concerns test whether you respect the controls that protect solutions and services.
- **Learning under direction** maps to your role level itself — a trainee in an established team: scenarios about asking for help, receiving feedback, and admitting the limits of your knowledge test the learning behaviours your level is built around.
- **Team collaboration** maps to your **Systems design** and **Systems integration** skills, which you exercise "as part of a team": scenarios about sharing information, supporting colleagues, and communicating clearly test whether you make the team stronger.

### Practice questions

**Question 1 (easy) — You are unsure about a runbook step**

You are following a runbook to apply a routine update to a server, supervised loosely by a senior engineer who is at her desk nearby. Step 6 says "confirm replication has completed before proceeding", but you are not sure how to check replication status. What is the most effective response?

- A) Skip step 6 — the update has always worked before, so replication is probably fine.
- B) Pause, and ask the senior engineer to show you how to check replication status before you continue.
- C) Stop the whole task and log a ticket asking for the runbook to be rewritten.
- D) Guess which console screen shows replication and proceed if anything looks green.

**Correct answer: B**

**Explanation:** Option B is exactly what "working under direction" is designed for: you pause at the point of uncertainty, you ask a specific question, and you learn the skill for next time — the update proceeds safely and your capability grows. Option A skips a safety check because of past luck; runbook steps exist because someone once learned their importance the hard way. Option D is guessing dressed as checking — "anything looks green" is not a verification. Option C over-reacts: the runbook may be fine and the gap may be in your knowledge, which a two-minute conversation fixes; suggesting a runbook improvement afterwards would be a good extra step, but stopping the task entirely is disproportionate. The professional behaviours here are honesty about what you do not know and asking for help early — both of which score well in SJTs and in real careers.

**Question 2 (easy) — You made a mistake**

While tidying user accounts under instruction, you accidentally disable the account of an active staff member instead of a leaver with a similar name. You realise your mistake ten minutes later. Nobody has noticed yet. What is the most effective response?

- A) Quietly re-enable the account and say nothing — no harm done.
- B) Re-enable the account immediately, then tell your supervisor what happened and how you confused the two names.
- C) Say nothing and hope the user does not report it.
- D) Tell your supervisor that the account system behaved strangely.

**Correct answer: B**

**Explanation:** Option B combines the two things that matter: fix the impact fast (re-enable the account), and be honest about the cause. Telling your supervisor is not self-punishment — it lets the team check for consequences you might not see (did the user lose access to anything mid-task? does the disablement appear in a security log that will confuse someone later?) and it may reveal a process weakness, such as leavers' names not being clearly marked, that the team can fix for everyone. That is your **Problem management** skill in behavioural form: remedies and preventative measures start with accurate information. Option A fixes the symptom but hides the information. Option C leaves a colleague locked out. Option D is actively dishonest and would poison trust if discovered — and in security-relevant systems, false accounts of what happened can cause real investigative harm. In SJTs, honesty after a mistake is one of the most reliably rewarded behaviours; in government IT, it is also the culture that keeps services safe.

**Question 3 (easy) — A user asks you to bypass a rule**

A friendly senior manager from another team stops you in the corridor: "I need admin rights on my laptop for a conference demo tomorrow — the request process takes days. You can just do it quickly, can't you? I'll take responsibility." What is the most effective response?

- A) Grant the rights — a senior manager has accepted responsibility.
- B) Politely explain you cannot grant rights outside the process, and offer to help them raise an expedited request or find who can approve it urgently.
- C) Refuse and walk away without explanation.
- D) Grant the rights but ask them to keep it quiet.

**Correct answer: B**

**Explanation:** Access controls are part of the security controls that protect solutions and services — your **Information security** skill — and they exist independently of seniority or charm. "I'll take responsibility" is not a real control: the manager cannot absorb the consequences of malware installed with admin rights on a departmental device, and you would still have acted outside the process. Option B refuses the bypass while genuinely helping: many departments have urgent-request routes, and pointing the manager to one respects both the rule and their real need — that combination of firmness and helpfulness is what SJTs reward. Option A confuses authority with authorisation. Option C protects the rule but abandons the user; user focus means helping people find the legitimate path, not just saying no. Option D is the worst: a policy breach plus concealment. If you feel pressured after declining, telling your supervisor is a sensible extra step — pressure to bypass controls is itself worth reporting.

**Question 4 (easy) — Two requests at once**

You are alone at the team desk over lunch. A colleague from finance phones: her team's shared drive is inaccessible and month-end processing is due today. At the same moment, an engineer from your team messages asking you to fetch a cable from the store room for a job he is doing this afternoon. What is the most effective response?

- A) Fetch the cable first — your own team comes first.
- B) Take the finance caller's details, raise and prioritise their incident, alert the on-duty engineer to it, and tell your teammate the cable will follow shortly.
- C) Tell the finance caller to ring back when the team is back from lunch.
- D) Try to fix the shared drive yourself immediately without logging anything.

**Correct answer: B**

**Explanation:** Compare impact and urgency: a finance team blocked on month-end processing today is a live business impact with a deadline; a cable for an afternoon job can wait twenty minutes. Option B handles the urgent item properly — logged, prioritised, and escalated to someone who can fix it, which is exactly the "pass problems on to your team" behaviour in your **Ownership and topic** skill — while still committing to the smaller task. Option A prioritises social closeness over business impact. Option C abandons a user with a same-day deadline; "the team is at lunch" is your problem to solve by escalation, not the user's problem to solve by waiting. Option D has generous intent but skips logging (losing the record the team needs) and launches an unsupervised fix on a live service, which at your level risks making things worse. Notice the pattern that runs through associate-level SJTs: the strong answer is rarely "do the fix yourself" and almost always "route it fast, log it properly, keep everyone informed".

**Question 5 (moderate) — You spot something wrong that nobody mentioned**

While checking backup job reports as part of your morning tasks, you notice that backups for one file server have failed silently for the last three nights. The server is not one you look after, and its named administrator is on leave this week. What is the most effective response?

- A) Note it down to mention when the administrator returns from leave next week.
- B) Raise it with your supervisor or the team straight away, with the evidence — the affected server and the three failed dates — so cover can be arranged.
- C) Attempt to fix the backup configuration yourself since the administrator is away.
- D) Assume someone else has already noticed, since the reports are circulated to the whole team.

**Correct answer: B**

**Explanation:** Three nights of failed backups means the server currently has no recent recovery point: if it fails before the backups are fixed, data is lost. That risk grows every day, so option A's one-week delay is genuinely dangerous. Option D is the diffusion-of-responsibility trap — "someone else will have seen it" is precisely how silent failures stay silent; the reports being widely circulated makes it more likely everyone assumes someone else is acting. Option C exceeds your remit on an unfamiliar system: well-meant, but an incorrect backup change could quietly make things worse. Option B is proactive ownership scaled to your level: you noticed, you gathered the specific evidence, and you put it in front of people who can act while the administrator is away. This is the behaviour your **Ownership and topic** and **Problem management** skills describe — awareness of resolution processes, passing problems on effectively — and it is exactly how associates build a reputation as safe, observant engineers.

**Question 6 (moderate) — Receiving critical feedback**

Your supervisor reviews a set of server checks you completed and points out, in front of another team member, that you recorded two checks as "passed" that you did not actually perform, because the console page would not load and you assumed they were fine. He is calm but clearly unimpressed. What is the most effective response?

- A) Explain that the console was broken, so it was not your fault.
- B) Acknowledge the mistake, correct the records now, perform or arrange the missed checks, and agree how to record inaccessible checks in future.
- C) Apologise profusely and offer to redo every check you have ever done.
- D) Say nothing, but privately resolve to argue your case to the team later.

**Correct answer: B**

**Explanation:** The core error was recording as done something that was not done — in infrastructure work, false "passed" records are worse than honest gaps, because the team plans around them. Option B owns that fully: acknowledge, correct the record, close the actual gap (the unperformed checks), and — the mark of a learner — agree the right procedure for next time, which turns the episode into a process improvement. That final step matters: "console would not load" is real information the team needs a convention for, such as recording "unable to verify — console error, escalated". Option A leads with self-defence; the console problem explains the difficulty but not the false record. Option C is disproportionate emotion that transfers the burden of reassurance to your supervisor. Option D converts feedback into grievance. SJTs at trainee level frequently probe how you receive correction, because it predicts how fast you will grow: the winning pattern is acknowledge, repair, prevent — without either defensiveness or collapse.

**Question 7 (moderate) — A colleague is struggling**

A fellow associate joined the team a month after you. You notice he has been stuck for most of the morning on a storage task you learned to do last month, and he looks stressed. He has not asked anyone for help. Your own task list for today is full but not urgent. What is the most effective response?

- A) Leave him to it — struggling alone is how everyone learns.
- B) Quietly offer to pair with him on the task for twenty minutes, showing him what you learned, and suggest he checks the result with a senior engineer afterwards.
- C) Tell your supervisor that he is not coping with the role.
- D) Do the task for him while he watches, so it gets done quickly.

**Correct answer: B**

**Explanation:** Option B helps the person and the work while respecting everyone's role: pairing shares your recent learning (recent learners often teach basics best, because they remember what was confusing), a time-box keeps your own commitments realistic, and routing the result past a senior engineer respects the fact that you are both trainees — your knowledge is a month deep, so verification protects the service. Option A confuses productive struggle with abandonment; an established team is exactly the environment where asking and offering help should be normal, and modelling that norm helps him ask sooner next time. Option C escalates a normal learning moment into a performance concern behind his back — disproportionate and trust-damaging; if a genuine pattern persisted, a supportive word with the supervisor might later be right, but not as the first response. Option D completes the task but not the learning, leaving him equally stuck next time. Collaboration and inclusion — making the team one where it is safe to not know things yet — are behaviours SJTs consistently reward.

**Question 8 (moderate) — Pressure to finish before the window closes**

You are assisting a senior engineer with a maintenance task inside an agreed two-hour change window. With twenty minutes left, the senior engineer is called away to an urgent incident and says, "You've seen me do the remaining steps — finish it off, or roll it back, your call." You have watched the remaining steps but never performed them. What is the most effective response?

- A) Finish the steps from memory — you have seen them done and the window is closing.
- B) Check whether a documented procedure exists for the remaining steps; if you can follow it verifiably within the window, proceed carefully, and if not, perform the practised rollback and report the situation.
- C) Do nothing and let the window expire with the change half-applied.
- D) Phone the senior engineer repeatedly at the incident until he talks you through each step.

**Correct answer: B**

**Explanation:** The decision hinges on verifiability. "I watched someone do it once" is not a safe basis for changing live infrastructure — but a documented procedure you can follow step by step, within time, may be: that is what runbooks are for, and the engineer has explicitly delegated the call. If no such document exists or time is too tight, the rollback — which is a practised, planned path back to a known-good state — is the professionally safe choice, and reporting it promptly lets the team reschedule. That is option B: a genuine decision process, not a reflex. Option A gambles a live service on memory under time pressure — the classic condition for skipped steps. Option C is the worst technical outcome: a half-applied change is an undefined state, less safe than either completing or rolling back. Option D interferes with an urgent incident and outsources your decision instead of making it. Note the deeper lesson for your **IT infrastructure** work: rollback is not failure; it is the system working as designed. SJTs reward candidates who treat "safe retreat plus honest report" as a success.

**Question 9 (moderate) — Third-party engineer on site**

An engineer from a supplier arrives to replace a disk array controller. He is friendly and competent, but you notice he is about to work on the array in rack 7, while the change ticket you were given clearly says rack 9. He says, "The ticket's probably wrong — this is the model I usually work on." What is the most effective response?

- A) Let him proceed — he is the specialist and works on these arrays every week.
- B) Ask him to pause, and verify the correct array with your team before any work starts, explaining that the ticket and his intention disagree.
- C) Insist he works on rack 9 because the ticket says so.
- D) Let him proceed but note your concern in the ticket afterwards.

**Correct answer: B**

**Explanation:** Two authoritative sources disagree: the ticket says rack 9; the specialist says rack 7. Either could be wrong — tickets do contain errors, and specialists do assume. Working on the wrong array could take down a healthy production system, so the only safe move is to stop and verify before anything is touched, which is option B. Option A trusts expertise over verification; expertise is about how to do the work, not necessarily which system needs it. Option C makes the opposite error — enforcing the ticket without checking, when the engineer's doubt is itself evidence worth investigating. Option D is the most insidious: it recognises the risk and documents it while letting the risk happen; a note written after wrong-array work is an autopsy, not a control. This scenario reflects your role level's real duty to work with and support third parties: suppliers are partners, and the site engineer who politely says "let's confirm before we start" is doing exactly the quality-assurance job the department needs. "Pause and verify when sources disagree" is a behaviour worth carrying through your whole career.

**Question 10 (hard) — A security concern involving a senior colleague**

While shadowing a senior engineer, you notice he logs into a shared administrator account using a password kept on a sticky note under the keyboard, and remarks, "Everyone on the team uses this one — it's easier than personal admin accounts." You know from your induction training that shared administrator accounts and written-down passwords are against departmental security policy. What is the most effective response?

- A) Say nothing — he is senior, and this is apparently how the team works.
- B) Report him to the security team immediately without speaking to anyone else.
- C) Ask him about it at a suitable moment — mentioning what your training said — and if the practice continues unaddressed, raise your concern with your supervisor or the security team.
- D) Start using the shared account yourself, since everyone does.

**Correct answer: C**

**Explanation:** This scenario tests whether you can hold onto a security principle under social pressure, and whether you can act on it proportionately. Option C does both: it starts with a direct, respectful conversation — perhaps there is context you lack, perhaps the team has an exemption, or more likely the practice has drifted and your question prompts a fix — and it commits to escalation if the risk remains, because shared credentials on a sticky note defeat accountability (no audit trail shows who acted) and are exactly what your **Information security** skill teaches controls exist to prevent. Option A makes seniority a reason to ignore policy; note that SJT scoring consistently penalises silent acquiescence on security matters. Option D actively joins the breach — the worst answer: "everyone does it" has never made a control unnecessary. Option B is not wrong in principle — security teams do want reports — but as a first move it skips the cheapest, fastest remedy (a conversation) and can damage team trust unnecessarily; it becomes the right move if the conversation fails. Proportionate escalation — person, then supervisor, then security team — is the professional pattern.

**Question 11 (hard) — Balancing learning against delivery**

Your supervisor offers you a choice for the next fortnight: (a) continue doing daily ticket triage, which you now do quickly and confidently, because the team is busy and your speed genuinely helps; or (b) hand triage to another associate and join a project decommissioning old servers, which you have never done and which would stretch you, but where you would initially slow the project down. She says either choice is acceptable and asks what you think. What is the most effective response?

- A) Choose triage — the team is busy and your speed helps most right now.
- B) Choose the project without discussion — your development always comes first.
- C) Discuss it briefly: propose joining the decommissioning project for the learning, while offering to spend a short handover period coaching the other associate on triage so the team keeps its speed.
- D) Ask your supervisor to decide for you, since she knows best.

**Correct answer: C**

**Explanation:** There is no trap here — both (a) and (b) are defensible, which is why the strongest answer is the one that engages with the trade-off rather than picking a side blindly. Option C does three professional things at once: it prioritises development (a trainee who only repeats mastered tasks stops being trained — and the role level exists to grow you into an infrastructure engineer), it mitigates the cost of that choice through a planned handover and coaching, and it treats the supervisor's question as a real invitation to think aloud, which is itself a skill being assessed. Option A is generous but short-sighted: it optimises this fortnight at the expense of your growth and leaves the team with a single point of triage knowledge — the handover in option C actually reduces that risk. Option B grabs the development without acknowledging the team impact. Option D refuses the invitation to exercise judgement; supervisors ask "what do you think?" partly to develop your decision-making, and "you decide" wastes the opportunity. In SJTs and in careers, the pattern scores well: choose growth, and take responsibility for softening its costs.

**Question 12 (hard) — An incident during handover**

It is 17:25; your shift ends at 17:30, and you have a college class tonight. Five minutes ago you noticed intermittent errors in the monitoring console for a database server that supports a public-facing service. You are not certain it is a real problem — it could be monitoring noise — and the evening on-call engineer takes over at 17:30. What is the most effective response?

- A) Leave at 17:30 — the on-call engineer will see the errors on the console if they matter.
- B) Stay as long as it takes to diagnose the errors yourself, missing your class.
- C) Spend the remaining minutes writing a clear handover note — what you saw, when it started, which server and service — and directly brief the on-call engineer before you leave at 17:30.
- D) Silence the alerts so the console is tidy for the evening, and mention the errors tomorrow.

**Correct answer: C**

**Explanation:** The professional core of this scenario is your **Ownership and topic** skill in its purest form: own an issue until it has a new owner. Option C achieves exactly that transfer: the on-call engineer starts the evening knowing what to watch, when it began, and where — the observations only you currently hold — and you leave on time with the issue safely handed over. A direct brief plus a written note is the gold standard, because spoken context and a durable record cover each other's gaps. Option A gambles that the engineer will notice, and discards your most valuable contribution: the time-of-onset context that consoles do not show. Option B is unsustainable heroism: uncertain monitoring errors do not justify missing commitments when a paid, prepared on-call engineer exists precisely for this; chronic overstaying also masks staffing gaps from the team. Option D is the genuinely harmful answer: silencing alerts removes the very signal the on-call engineer would need, converting possible noise into guaranteed blindness. Handover quality is one of the most operationally important behaviours in 24/7 services — practise writing the four-line handover note (what, where, when, what's been done) until it is reflex.

### Preparation tips

- **Learn your escalation routes cold.** Know who your supervisor, on-call engineer, and security contacts are and when to use each. Most associate-level SJT answers involve routing well, and knowing the real routes makes the right option feel obvious.
- **Rehearse the honesty scripts.** Practise saying "I made a mistake — here is what happened" and "I don't know how to do this — can you show me?" out loud. Candidates who are comfortable with these phrases pick the honest options instinctively.
- **Think "users first, process always".** When torn between options, ask: which response best protects the people using the service, through the proper process? That question resolves most dilemmas.
- **Notice the safe-retreat options.** Rollbacks, pauses, and verifications are not weakness — they are frequently the highest-scoring choices. Look for the option that reduces risk while keeping things moving.
- **Read the scenario's constraints carefully.** Details like "your supervisor is nearby", "the administrator is on leave", or "the window closes in twenty minutes" are placed deliberately and usually point at the intended dilemma.
- **Reflect on real moments.** After each working week, note one situation where you chose what to do — an escalation, an admission, an offer of help. Ask a senior colleague how they would have handled it. This converts daily work into SJT preparation.
- **Answer as your best professional self, consistently.** Do not try to guess a "personality the employer wants" — modern SJTs detect inconsistency. The behaviours in this section (honesty, early escalation, user focus, proportionate action) are the genuine standard; practise living them and the test takes care of itself.

### Common pitfalls to avoid

- **Choosing heroics over routing.** "Fix it yourself immediately" options flatter your initiative but usually skip logging, supervision, or expertise. At associate level, fast and accurate escalation is the strong move.
- **Letting seniority override controls.** Managers, specialists, and even your own supervisor do not outrank security policy or change process in these scenarios. Politely holding the line — with help offered — scores best.
- **Concealing or minimising mistakes.** Any option involving silence, cover-up, or a misleading account is a low scorer, however small the error. Fix, then tell, then prevent.
- **Doing nothing because it is not your job.** Silent failures, struggling colleagues, and wrong-rack engineers are everyone's business to raise. "Someone else will notice" is the most common failing answer.
- **Over-escalating as a first move.** Jumping straight to formal reports when a respectful conversation would resolve the issue scores poorly too. Proportionate first steps, with escalation held in reserve, is the pattern.
- **Sacrificing yourself unnecessarily.** Options where you miss commitments, skip breaks, or absorb unreasonable burdens often look virtuous but model unsustainable behaviour. Look for the option that meets the need through proper handover instead.
- **Forgetting the handover.** In any scenario involving shift ends, leave, or absence, the winning option almost always transfers information explicitly — a note, a brief, a logged ticket — rather than assuming the next person will find out.

## Conclusion

Well done — you have worked through a complete set of practice materials covering all four of the assessment types you are most likely to meet as an associate infrastructure engineer: cognitive ability, numeric reasoning, verbal reasoning, and situational judgement. That is a genuine achievement, and it is worth pausing to notice what you have practised along the way.

In the cognitive section, you checked server names against conventions, traced dependency chains, spotted the skipped runbook step, and reasoned carefully about rules with exceptions. In the numeric section, you converted disk usage into percentages, forecast when a growing log volume would hit its threshold, calculated availability against an SLA, and learned to distrust simple averages of different-sized groups. In the verbal section, you held the line on "Cannot say", separated must from may, and read policies, supplier notices, and incident reports with the precision your job demands. In the situational judgement section, you rehearsed the behaviours that make an associate genuinely valuable: escalating early, admitting mistakes quickly, handing over properly, helping colleagues, and holding onto security controls even under friendly pressure.

Here is the encouraging truth that connects all four sections: none of this is separate from your job. Every technique in this guide — check each part against the rule, ask "out of what?", read the modal verbs, route problems fast with good evidence — is a working habit you can use tomorrow morning. Practising for assessments and growing as an engineer are the same activity wearing two different outfits. The associate level exists to turn potential into capability through exactly this kind of deliberate practice, supported by the established team around you.

So what should you do next? Three suggestions. First, revisit the questions you found hardest in a week's time — spaced repetition turns technique into instinct. Second, bring this practice into your real work: recreate a numeric question from this week's monitoring data, or write a one-sentence faithful summary of the next ticket you read. Third, talk to your team. Ask a senior engineer how they prioritise, how they hand over, how they check their arithmetic. Your role level is designed around learning under direction, and every conversation compounds.

If you have a real assessment coming up, go into it rested, prepared, and calm. Remember that adaptive tests get harder when you are doing well, that an educated guess beats a blank, and that accuracy with steady pace beats frantic speed. And remember that the assessment is not a judgement of your worth — it is a snapshot of skills you have now proven you can grow.

You support the infrastructure that public services run on. That matters, and so does the care you are taking to get better at it. Keep practising, keep asking, and keep being the observant, honest, safe pair of hands this guide has been training. Good luck — you are better prepared than you were when you started reading.
