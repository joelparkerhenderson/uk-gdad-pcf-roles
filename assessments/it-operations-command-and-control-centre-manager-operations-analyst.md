# Operations Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an operations analyst working in a command and control centre within the UK Government Digital and Data profession. You might be preparing for an internal assessment. You might be applying for a promotion. Or you might simply want to understand your own strengths better. Whatever brought you here, this document will help you practise, build confidence, and feel ready.

First, let's answer the obvious question: what is a psychometric assessment? It is a structured, standardised exercise that measures the thinking skills and workplace judgement that predict success in a role. That may sound intimidating, but please don't worry. The assessments in this guide are not abstract puzzles designed to catch you out. They are job-specific. They use the kinds of materials you genuinely handle every day: monitoring dashboards, incident tickets, alert queues, asset registers, change request forms, and shift handover notes. They ask the kinds of questions you genuinely answer every day: which alert matters most right now, which channel should this incident go to, does this record match reality, and what should I do next?

Why do these assessments matter for your role in particular? As an operations analyst, you are often the first pair of eyes on a live service. You watch performance trends, you spot things that look unusual, you register incidents with the right information, and you alert support staff when something needs attention. You also provide administrative support to your manager, which means accuracy, tidiness, and reliability really count. The four assessment types in this guide map directly onto those demands. Cognitive questions sharpen your pattern spotting and error checking. Numeric questions build your confidence with the percentages, counts, and averages that fill your dashboards. Verbal questions strengthen your reading of procedures, emails, and handover notes. Situational judgement questions help you rehearse the everyday decisions of the job, such as when to escalate and when to keep watching.

This document is organised into four main assessment sections. Each one follows the same friendly pattern: an overview of what the assessment measures and how it usually works, a mapping of the assessment to the specific skills in your role, a set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from this guide. First, read each "About this assessment" section so the format holds no surprises. Second, try each practice question honestly. Write down your answer before you read the explanation. No one is watching, so be truthful with yourself. Third, treat every explanation as a mini lesson. Even when you get a question right, the walkthrough will show you a reliable technique you can reuse. Fourth, go at your own pace. This is practice, not a test. You can take breaks, come back tomorrow, and repeat questions as often as you like.

One last thing before you begin. Early-career assessments are designed for people at your level. Nobody expects you to reason like a service owner or a head of operations. They expect care, attention, honesty, and steady thinking, and those are all things you can practise. Take your time, be kind to yourself, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract shapes and symbols. Instead of asking you to rotate a triangle in your head, it shows you the everyday materials of your job: an alert queue, an asset register extract, a shift rota, a set of incident tickets, or a monitoring dashboard. It then asks you to reason quickly and accurately about them.

The typical format is an online, timed test lasting 15 to 30 minutes. You can usually expect between 15 and 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared against a norm group of people at a similar level. Many modern platforms are adaptive, which means the questions get slightly harder when you answer correctly and slightly easier when you don't. That is normal, so don't panic if the test suddenly feels harder — it may mean you are doing well. Employers usually see a breakdown of your speed and your accuracy, so working carefully matters just as much as working quickly. Most platforms offer a few ungraded practice questions before the real test starts, so you can get used to the screens without any pressure.

Why do employers use this assessment for an operations analyst? Because your core value to the command and control centre is attentive, accurate thinking. You proactively monitor live services and performance trends to identify potential problems. You track, log, and correct information to protect assets and components. You identify and register incidents, gathering the required information and allocating each one to the appropriate channel. Every one of those duties is, at heart, a cognitive task: noticing what has changed, checking what doesn't match, deciding what matters most, and reasoning carefully from the rules you have been given. A well-designed cognitive assessment simulates those demands in miniature, which is why practising it genuinely helps you do the job better too.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your core duty of proactive monitoring and to **Availability and capacity management**: spotting a trend in a dashboard — a slowly climbing response time, a repeating overnight alert — is pattern recognition applied to service components and their key performance indicators (KPIs).
- **Error checking** maps to **Asset and configuration management**: you track, log and correct information to protect assets and components, which means comparing records against reality and catching the entry that doesn't fit.
- **Logical deduction** maps to **Change management** and **Continuity management**: applying change control procedures under supervision, and explaining the basic principles of continuity processes, both require you to follow written rules exactly and work out what they mean in a specific case.
- **Prioritisation** maps to **Incident management** and **Ownership and initiative**: when several alerts arrive together, you must decide which to register and escalate first, and you own an issue until a new owner is found or the problem is resolved.
- **Applied problem solving** maps to **Problem management** and **Service focus**: you investigate problems in systems, processes and services, understanding whether a problem is strategic, tactical or operational, and you take inputs and establish coherent frameworks that work.

### Practice questions

**Question 1 (easy) — Pattern recognition in an alert queue**

Your monitoring tool labels alerts with a severity code and a source system, in the fixed format "SEV<number>-<SYSTEM>", for example "SEV2-PAYMENTS". This morning's queue shows:

1. SEV1-CASEWORK
2. SEV3-PAYMENTS
3. PAYMENTS-SEV2
4. SEV2-IDENTITY

Which entry breaks the labelling pattern?

- A) Entry 1
- B) Entry 2
- C) Entry 3
- D) Entry 4

**Correct answer: C**

**Explanation:** The pattern puts the severity code first, then a hyphen, then the source system. Entries 1, 2 and 4 all follow it. Entry 3 reverses the order, putting the system name before the severity. This looks like a small thing, but it matters in real monitoring work: tools often sort, filter and route alerts based on the label format, so a reversed label can slip past a filter and be missed. When you track and log information as part of asset and configuration management, checking that entries follow the agreed format is one of the simplest and most valuable habits you can build. In the assessment, scan each option against the stated rule one at a time rather than trusting your first glance — the eye loves to "auto-correct" reversed text.

**Question 2 (easy) — Logical deduction from a procedure**

Your incident procedure states: "If an alert affects a citizen-facing service, register an incident immediately. If an alert affects only an internal test system, log it in the daily notes instead." An alert arrives for the system "Benefits Portal", which your service catalogue lists as citizen-facing. What should happen, according to the procedure?

- A) Log the alert in the daily notes.
- B) Register an incident immediately.
- C) Wait to see whether a second alert arrives.
- D) Ask the test team whether the portal is in a test window.

**Correct answer: B**

**Explanation:** The procedure gives two clear rules, and the facts tell you which one applies. The Benefits Portal is citizen-facing, so the first rule fires: register an incident immediately. Options C and D add extra steps the procedure does not ask for, and option A applies the wrong rule. This discipline — do exactly what the written rule says for the case in front of you — is the heart of applying change control procedures under supervision and registering incidents correctly. In assessments, be careful not to import outside knowledge or invent caveats; answer from the rules and facts you are given. In real life you can and should ask questions, but the question tests whether you can read a rule and apply it faithfully.

**Question 3 (easy) — Error checking an asset register**

You are checking a printout of the asset register against the four monitors physically present in the control room. The register lists:

| Asset tag | Item | Location |
|---|---|---|
| MON-101 | 27-inch monitor | Control room desk 1 |
| MON-102 | 27-inch monitor | Control room desk 2 |
| MON-103 | 27-inch monitor | Storage cupboard B |
| MON-104 | 27-inch monitor | Control room desk 4 |

In the room you find monitors tagged MON-101, MON-102, MON-103 and MON-104, one on each desk. How many register rows need correcting?

- A) 0
- B) 1
- C) 2
- D) 4

**Correct answer: B**

**Explanation:** Compare each row with reality. MON-101, MON-102 and MON-104 are recorded in the control room and are in the control room, so those rows are fine. MON-103 is recorded in "Storage cupboard B" but is actually on a desk in the control room, so that one row needs its location corrected. The answer is 1. Notice the method: go row by row and compare a single fact at a time, rather than trying to hold the whole table in your head. Tracking, logging and correcting information to protect assets is exactly this kind of careful, one-item-at-a-time verification. A wrong location in a register seems harmless until someone needs that asset urgently during an incident and looks in the wrong place.

**Question 4 (easy) — Prioritisation of incoming alerts**

Three items arrive within the same minute. Your team's rule is: severity first, then citizen impact, then age. Which do you deal with first?

1. A SEV3 alert on an internal reporting tool, arrived 10 minutes ago.
2. A SEV1 alert on the citizen-facing appointments service, arrived just now.
3. A SEV2 alert on an internal staff directory, arrived 5 minutes ago.

- A) Item 1, because it has waited longest
- B) Item 2, because it has the highest severity
- C) Item 3, because it is mid-severity and mid-age
- D) Whichever is quickest to close

**Correct answer: B**

**Explanation:** The rule tells you the order to compare things in: severity first. Item 2 is SEV1, the highest severity in the list, so it comes first, and you don't even need the tie-breakers. It also happens to affect a citizen-facing service, which would win the second comparison anyway. Option A confuses "oldest" with "most important" — age only matters when severity and impact are equal. Option D is tempting in a busy shift but ignores the rule entirely; closing easy items first can leave a serious incident unattended. This mirrors your incident management duty to allocate each incident to the appropriate channel promptly: the queue order should follow impact, not convenience.

**Question 5 (moderate) — Pattern recognition in a performance trend**

The average response time of a service, measured at the same hour each day, has been: Monday 210 ms, Tuesday 215 ms, Wednesday 224 ms, Thursday 238 ms, Friday 257 ms. The alert threshold is 300 ms. As the analyst monitoring this trend, what is the most accurate description of what you are seeing?

- A) The service is fine because it has never breached the threshold.
- B) Response time is rising, and the daily increase is itself getting bigger, so it is worth flagging before the threshold is breached.
- C) Response time is rising at a steady rate of 5 ms per day.
- D) The figures are random noise and no action is needed.

**Correct answer: B**

**Explanation:** Look at the day-to-day increases: +5, +9, +14, +19. The service is not just getting slower; it is getting slower faster. That accelerating pattern suggests something is building up — perhaps a memory leak or a growing queue — and if the pattern continues, the next increases might be around +24 and +29, taking the service past 300 ms early the following week. Option A is technically true today but misses the whole point of proactive monitoring: your role exists to identify potential problems before they become incidents. Option C describes a steady rise, which the numbers contradict. This is exactly the "performance trends" part of your role description, and it links to availability and capacity management: managing service components so they keep meeting their KPIs means acting on the trend, not just the current value.

**Question 6 (moderate) — Logical deduction about change windows**

Your change control procedure, which you apply under supervision, says: (i) standard changes may be implemented on any weekday outside business hours; (ii) business hours are 08:00 to 18:00; (iii) any change to the payments system, of any type, additionally requires written approval from the payments service manager before implementation. You have a standard change request for the payments system, and it is currently 19:30 on a Tuesday. Which statement must be true?

- A) You may implement the change now.
- B) You may implement the change now only if the payments service manager's written approval has been given.
- C) You must wait until the weekend.
- D) The change is forbidden because payments changes cannot be standard changes.

**Correct answer: B**

**Explanation:** Work through the rules one at a time. Rule (i) with rule (ii): it is a weekday and 19:30 is outside 08:00–18:00, so the timing condition is satisfied. Rule (iii): because this change touches the payments system, it also needs the service manager's written approval. So the change may go ahead now if and only if that approval exists — which is exactly option B. Option A ignores rule (iii). Option C invents a weekend requirement that appears nowhere. Option D invents a prohibition the rules don't contain. Assessments often hide the answer in the word "additionally": one rule being satisfied does not switch the others off. The same reading habit protects you at work when you implement change requests: check every applicable condition, not just the first one you find.

**Question 7 (moderate) — Error checking a shift handover note**

A handover note from the night shift reads: "Three incidents open at handover: INC-4411 (network, SEV2, opened 02:10), INC-4412 (email, SEV3, opened 03:40), INC-4413 (portal, SEV2, opened 05:55). Total open incidents: 3. Oldest open incident: INC-4412." Which single statement in the note is wrong?

- A) The total count of open incidents
- B) The identity of the oldest open incident
- C) The severity of INC-4411
- D) Nothing is wrong

**Correct answer: B**

**Explanation:** Check each claim against the listed facts. Three incidents are listed and the note says the total is 3, so the count is right. The severities are simply restated, so there is nothing to contradict them. The "oldest" claim is checkable: INC-4411 opened at 02:10, which is earlier than INC-4412's 03:40, so the oldest open incident is INC-4411, not INC-4412. The note's final claim is wrong. This is a classic internal-consistency check: you don't need any outside knowledge, just a careful comparison of the note against itself. In your role, correct record keeping during handover is vital — the day shift will chase the "oldest" incident first, and a wrong claim sends effort to the wrong place. When you own an issue until a new owner is found, accurate handover is how that ownership passes safely.

**Question 8 (moderate) — Applied problem solving with a runbook**

A morning check shows the report-generation service failed overnight. The continuity runbook gives this recovery order: (1) confirm the database service is running; (2) restart the report service; (3) re-run the failed report job; (4) confirm output appears in the shared folder. You confirm the database is running and restart the report service, and it starts cleanly. You re-run the failed job, but no output appears in the shared folder. What is the most sensible next step?

- A) Restart the database, because it must be the real cause.
- B) Mark the check complete, because three of the four steps worked.
- C) Check whether the job actually ran successfully and whether the shared folder path is correct, then escalate with what you find.
- D) Delete the failed job and wait for tomorrow's scheduled run.

**Correct answer: C**

**Explanation:** The runbook got you through steps 1 to 3, and the failure is now at step 4: output is missing. The disciplined move is to gather information at the point of failure before escalating — did the job report success? Is the folder path right? Has permission changed? That gives support staff something concrete to work with, which is exactly your duty to gather required information and allocate the issue to the appropriate channel. Option A jumps to a cause the evidence doesn't support: the database was confirmed running. Option B is the most dangerous answer — a check is complete when the outcome is achieved, not when most steps ran. Option D hides the problem for a day. This question also touches continuity management basics: runbooks tell you what to do, but when a runbook step fails, your job is to capture the facts and pass the issue to someone who can fix it, while keeping ownership until they do.

**Question 9 (moderate) — Prioritisation with a manager's request**

At 09:00 your manager asks you to prepare the weekly performance summary for a 14:00 meeting; it usually takes you about an hour. At 09:05 a SEV2 alert appears on the citizen-facing licensing service. At 09:06 a colleague asks you to help find a missing keyboard listed in the asset register. What order should you handle these in?

- A) Summary, alert, keyboard — your manager asked first.
- B) Alert first (register and escalate it), then the summary, then the keyboard.
- C) Keyboard first because it is quickest, then the alert, then the summary.
- D) Summary and keyboard first, leaving the alert for the afternoon.

**Correct answer: B**

**Explanation:** A SEV2 alert on a citizen-facing service is a live-service issue, and identifying and registering incidents promptly is the most time-critical duty you hold. Registering and escalating it may only take minutes, after which support staff take over the technical work while you retain a watching brief. The summary has a real deadline, 14:00, but there is ample time after the alert is handled. The keyboard matters for asset accuracy, but nothing about it is urgent. Option A confuses "asked first" with "most important". Option C falls for the quick-win trap. Option D fails the basic test of your role: live services come first. Notice that the best answer is not "do everything for the alert yourself" — it is to do your part (register, gather information, escalate) quickly and correctly, which is precisely what an operations analyst at your level is asked to do.

**Question 10 (hard) — Deduction across two records**

The change log says: "Change CH-208 (update firewall rule) was implemented Tuesday at 21:00." The incident log says: "INC-4460 opened Wednesday 08:15: staff in Office A cannot reach the case system. Resolved Wednesday 10:05 after the Tuesday firewall change was rolled back." Your manager asks: "Does this prove the firewall change caused the incident?" Which is the most accurate answer?

- A) Yes — the rollback fixed it, so the change was definitely the cause.
- B) No — the timing is a coincidence and the change should be re-applied at once.
- C) The evidence strongly suggests the change was involved, but it is not absolute proof; the investigation should confirm the mechanism before final conclusions.
- D) It is impossible to say anything at all from these records.

**Correct answer: C**

**Explanation:** Weigh the evidence carefully. The change preceded the incident, and the incident was resolved when the change was rolled back. That is strong circumstantial evidence — in problem management terms, the change is the leading hypothesis. But "resolved after rollback" is not quite the same as "resolved because of rollback": something else could have changed at the same time, or the rollback could have restarted a component that was failing for another reason. The mature answer keeps the strong hypothesis and asks the investigation to confirm the mechanism (for example, did the new rule actually block Office A's traffic?). Option A overstates the certainty; option B ignores the evidence; option D understates it. This is the level of thinking your problem management skill asks for: investigate problems with an understanding of the level and cause, and contribute to remedies without leaping past the evidence. Cautious, evidence-ranked reasoning also reads well to assessors.

**Question 11 (hard) — Multi-condition scheduling**

You must complete three routine tasks today: a configuration audit (takes 2 hours, must finish before the 15:00 change freeze), the daily monitoring check (takes 30 minutes, must be done between 09:00 and 10:00), and a records tidy-up (takes 1 hour, can be done any time). You start at 09:00 and take lunch 12:30–13:00. Assuming tasks cannot overlap, which schedule works?

- A) 09:00 check; 09:30 audit until 11:30; 11:30 tidy-up until 12:30; lunch; free afternoon.
- B) 09:00 audit until 11:00; 11:00 check; 11:30 tidy-up until 12:30; lunch.
- C) 09:00 tidy-up until 10:00; 10:00 check; 10:30 audit until 12:30; lunch.
- D) 09:00 check; 09:30 tidy-up until 10:30; 10:30 audit until 12:30, finishing after the freeze.

**Correct answer: A**

**Explanation:** Test each option against the three constraints: check within 09:00–10:00, audit finished by 15:00, no overlaps with lunch. Option A: check 09:00–09:30 (inside the window), audit 09:30–11:30 (finishes well before 15:00), tidy-up 11:30–12:30, lunch 12:30. Everything fits. Option B does the check at 11:00, outside the 09:00–10:00 window. Option C starts the check at 10:00, but the window closes at 10:00, so a 10:00–10:30 check misses it. Option D is a trick: the audit runs 10:30–12:30, which actually finishes before the freeze, but the option's own description says it finishes after the freeze — read every word, because assessments sometimes test whether you verify claims rather than accept them; the safest choice is the one whose stated schedule you have confirmed works, which is A. Methodically eliminating options against constraints is the same skill as scheduling your work around change freezes and monitoring windows in the control centre.

**Question 12 (hard) — Identifying the level of a problem**

Over the last month you have noticed: (a) the same disk-space alert fires on the reporting server every Friday evening; (b) each time, the on-call engineer clears temporary files and the alert stops; (c) no one has investigated why the files build up. Your problem management skill asks you to understand whether a problem is strategic, tactical or operational. How would you best describe the situation and the right contribution at your level?

- A) Operational only — the weekly fix works, so nothing more is needed.
- B) A recurring operational symptom pointing to an unaddressed underlying problem; register it as a problem record and contribute the pattern evidence you have gathered.
- C) Strategic — it requires a change to the organisation's five-year IT strategy.
- D) Tactical — you should personally redesign the reporting server's storage.

**Correct answer: B**

**Explanation:** Sort the layers. The Friday alert and the file clearance are operational events — they keep the service running today. But the same symptom recurring weekly, with a workaround and no root-cause investigation, is the textbook trigger for problem management: something underlying (perhaps a job that never cleans up after itself) keeps generating the symptom. It is not strategic — it doesn't touch organisational direction — and personally redesigning the server is beyond an analyst's remit and skips the investigation step. The right contribution at your level is exactly what option B says: register the problem, attach the evidence of the pattern you spotted (dates, alert details, what the workaround was), and let the investigation proceed with your data. This is "investigate problems... and contribute to the implementation of remedies and preventative measures" in action, and it shows the proactive monitoring mindset your role centres on: workarounds hide problems; patterns reveal them.

### Preparation tips

- **Practise with your own dashboards.** Ten minutes a day reading your real monitoring screens with a question in mind — "what changed since yesterday?" — is superb pattern-recognition training, and it makes assessment scenarios feel familiar.
- **Read rules like a checklist.** When a question quotes a procedure, number its conditions in your head and tick each one off against the scenario. Words like "additionally", "unless" and "only" carry most of the meaning.
- **Answer from the page, not from memory.** Use only the facts in the question. Your real-world knowledge is valuable at work, but in a test it can lead you to "correct" the question instead of answering it.
- **Do the untimed practice first, then add the clock.** Accuracy first, speed second. Once your method is reliable, timing yourself builds pace without panic.
- **Check the easy things every time.** Counts, dates, and labels are where questions hide their errors — just as registers and handover notes hide theirs.
- **Sleep and settle.** Cognitive tests reward a calm, rested brain. Prepare your test space, close distractions, and treat the first two questions as your warm-up.

### Common pitfalls to avoid

- **Rushing the reading.** Most wrong answers at this level come from misreading, not from inability. Slow down on the question stem; speed up on the arithmetic of elimination.
- **Choosing the "hero" answer.** Options that have you fixing everything yourself often overreach your role. At analyst level, the strong answer usually involves gathering information, registering the issue, and escalating well.
- **Treating the first plausible option as correct.** Read all four options. Assessments deliberately place a "nearly right" option before the best one.
- **Ignoring stated rules in favour of common sense.** If the procedure in the question says escalate, escalate — even if you'd personally have a quicker fix.
- **Letting one hard question shake you.** Adaptive tests are supposed to find your limit. Flag it mentally, give your best answer, and reset for the next question.
- **Confusing "oldest" with "most important".** Priority rules in questions (and in your queue) usually rank severity and impact above waiting time.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how well you work with numbers in the situations your job actually presents. It is not a maths exam. You will not need algebra, trigonometry, or anything you haven't used since school beyond the basics. What you will need is confidence with percentages, averages, ratios, rates, and simple trends — and the ability to read a table or chart carefully and pull out the right figure.

The typical format is an online, timed test lasting 20 to 30 minutes, with roughly 15 to 20 questions. Each question usually shows you a small data set — a table of ticket volumes, a chart of uptime percentages, a shift rota with headcounts — and asks a focused question about it. Calculators are normally allowed, and on-screen calculators are often provided; the test measures your reasoning and care, not your mental arithmetic. Scoring compares your accuracy and speed against a norm group at your level. As with the cognitive test, many platforms adapt difficulty as you go.

Why does this matter for an operations analyst? Because the command and control centre runs on numbers. Availability is a percentage. Capacity is a ratio of used to total. Incident workload is a count with a trend. KPIs — the key performance indicators your availability and capacity management skill asks you to help services meet — are all numeric. When you prepare an administrative summary for your manager, you are often summarising exactly these figures, and a small numeric slip can send a wrong signal up the chain. Practising this assessment builds the checking habits that make your summaries trustworthy, and it makes dashboards feel like plain language rather than a wall of digits.

One reassurance before you start: every question below shows its arithmetic step by step in the explanation. If you get one wrong, follow the working line by line and find the exact step where your path differed. That is the fastest way to improve.

### How this assessment maps to your role

- **Percentages and uptime** map to **Availability and capacity management**: managing service components to meet business needs and KPIs means reading and calculating availability percentages, breach rates, and headroom.
- **Counts, averages and trends** map to your core duty of **proactive monitoring of live services and performance trends**: a trend is just a sequence of numbers, and spotting whether it is rising, falling, or accelerating is numeric reasoning.
- **Table reading and cross-checking** map to **Asset and configuration management**: registers are tables, and correcting information means finding the row whose numbers don't add up.
- **Rates and workload figures** map to **Incident management** and **Problem management**: incidents per day, time to resolve, and recurrence counts are the evidence base you gather and contribute to investigations.
- **Simple resource arithmetic** maps to your **administrative support** duties and **Service focus**: rotas, meeting summaries, and weekly reports all involve totals, averages, and percentages presented clearly and correctly.

### Practice questions

**Question 1 (easy) — Reading a ticket volume table**

The incident counts for last week were:

| Day | Incidents |
|---|---|
| Monday | 12 |
| Tuesday | 9 |
| Wednesday | 15 |
| Thursday | 10 |
| Friday | 14 |

How many incidents were registered in total last week?

- A) 58
- B) 60
- C) 62
- D) 55

**Correct answer: B**

**Explanation:** Add the daily counts one step at a time: 12 + 9 = 21. Then 21 + 15 = 36. Then 36 + 10 = 46. Then 46 + 14 = 60. The total is 60. A tidy habit for table sums is to add in order and jot the running total, because jumping around the table invites double-counting or missing a row. Totalling ticket volumes is bread-and-butter work when you prepare the weekly summary for your manager, and getting the baseline total right matters because every percentage you calculate afterwards depends on it.

**Question 2 (easy) — A simple average**

Using the same table (12, 9, 15, 10, 14), what was the average (mean) number of incidents per day?

- A) 11
- B) 12
- C) 13
- D) 15

**Correct answer: B**

**Explanation:** The mean is the total divided by the number of days. From Question 1 the total is 60. There are 5 days. 60 ÷ 5 = 12. So the average is 12 incidents per day. Notice that the average is a summary, not a fact about any single day — no day actually had exactly 12 until you look, and Monday happens to match by coincidence. When you report "we averaged 12 incidents a day", you are turning five numbers into one, which is helpful for busy readers but always worth pairing with the highest day (Wednesday's 15) so the summary doesn't hide the peak. That habit of pairing the average with the extreme is exactly what makes a monitoring summary useful for spotting capacity pressure.

**Question 3 (easy) — Percentage of alerts escalated**

Yesterday the control centre received 40 alerts. You registered 8 of them as incidents and escalated those to support staff. What percentage of alerts were escalated?

- A) 8%
- B) 15%
- C) 20%
- D) 25%

**Correct answer: C**

**Explanation:** Percentage = (part ÷ whole) × 100. The part is 8 escalated alerts; the whole is 40 alerts. 8 ÷ 40 = 0.2. Then 0.2 × 100 = 20%. So 20% of alerts became incidents. A quick sense-check: 10% of 40 would be 4, so 8 must be 20% — doubling a known easy percentage is a fast way to verify your answer. Escalation rate is a figure managers genuinely watch, because a rising rate can mean services are getting less stable, while a falling rate can mean thresholds are set too loosely. Being able to produce this number quickly and correctly is part of the administrative support your role provides.

**Question 4 (easy) — Uptime percentage**

A service was unavailable for a total of 90 minutes during a 30-day month. Taking the month as 30 × 24 = 720 hours, which is 43,200 minutes, what was the service's availability percentage, to two decimal places?

- A) 99.79%
- B) 99.90%
- C) 98.75%
- D) 99.98%

**Correct answer: A**

**Explanation:** Work step by step. Total minutes in the month: 30 days × 24 hours × 60 minutes = 43,200 minutes. Available minutes: 43,200 − 90 = 43,110. Availability = 43,110 ÷ 43,200 = 0.997916..., and × 100 gives 99.7916...%, which rounds to 99.79%. A common slip is dividing the downtime instead: 90 ÷ 43,200 = 0.00208, i.e. about 0.21% downtime — subtract that from 100% and you get the same 99.79%, so both routes agree, which is a nice built-in check. Availability percentages like this are the KPIs at the centre of your availability and capacity management skill, and knowing that "99.79%" hides 90 real minutes of user impact helps you talk about the number meaningfully, not just report it.

**Question 5 (moderate) — Comparing against an SLA target**

Your service level agreement (SLA) requires 99.5% availability per month. In a 30-day month (43,200 minutes), what is the maximum downtime, in minutes, that still meets the SLA?

- A) 43.2 minutes
- B) 216 minutes
- C) 100 minutes
- D) 129.6 minutes

**Correct answer: B**

**Explanation:** If availability must be at least 99.5%, then downtime may be at most 100% − 99.5% = 0.5% of the month. Calculate 0.5% of 43,200: first 1% of 43,200 = 432, then half of that is 216. So the service can be down for up to 216 minutes (3 hours 36 minutes) and still meet the SLA. Option A is 0.1% (a much stricter target), and option D is 0.3%. This "downtime budget" way of thinking is genuinely how control centres track SLA risk mid-month: if 150 of the 216 minutes are already spent by day 10, the service is in danger, and that is exactly the kind of early warning your proactive monitoring is meant to raise before the KPI is breached.

**Question 6 (moderate) — Percentage change in incident volume**

The control centre registered 250 incidents in June and 290 incidents in July. What was the percentage increase from June to July, to the nearest whole percent?

- A) 14%
- B) 16%
- C) 40%
- D) 86%

**Correct answer: B**

**Explanation:** Percentage change = (change ÷ original) × 100. The change is 290 − 250 = 40 incidents. The original (the earlier month) is 250. 40 ÷ 250 = 0.16, and × 100 gives 16%. The classic error is dividing by the new value: 40 ÷ 290 = 13.8% ≈ 14%, which is option A — always divide by the starting figure. Another error is reporting the raw change (40) as if it were a percentage, which is option C. Month-on-month incident growth is a trend your manager will want explained, so pairing the number with a possible cause ("July included the licensing service go-live") turns a statistic into useful monitoring insight.

**Question 7 (moderate) — Ratio of alerts to incidents**

Over a week, the monitoring system produced 360 alerts, of which 45 were registered as incidents. What is the ratio of alerts to incidents, in simplest form?

- A) 9:1
- B) 8:1
- C) 45:360
- D) 7:1

**Correct answer: B**

**Explanation:** The ratio is 360:45. Simplify by dividing both sides by their highest common factor. Both divide by 45: 360 ÷ 45 = 8 and 45 ÷ 45 = 1. So the ratio is 8:1 — eight alerts for every incident. Option C is the ratio written backwards and unsimplified, and option A comes from the tempting but wrong division 360 ÷ 40. An 8:1 alert-to-incident ratio tells a story about signal and noise: if the ratio grows to 20:1, the monitoring thresholds may be too sensitive and real incidents could drown in noise; if it falls to 2:1, thresholds may be too loose and problems may be surfacing late. Reading that story in the numbers is proactive monitoring at its best.

**Question 8 (moderate) — Average resolution time with a twist**

Four incidents were resolved today with resolution times of 30 minutes, 45 minutes, 25 minutes, and 4 hours. What was the mean resolution time?

- A) 60 minutes
- B) 85 minutes
- C) 100 minutes
- D) 76 minutes

**Correct answer: B**

**Explanation:** First convert everything to the same unit — this is where most mistakes happen. 4 hours = 240 minutes. Now add: 30 + 45 = 75; 75 + 25 = 100; 100 + 240 = 340 minutes total. Divide by the 4 incidents: 340 ÷ 4 = 85 minutes. Option C is the trap for stopping the addition before the converted value, and option A is what you get by averaging only the three short times. Notice how one long incident drags the mean far above the typical case: three of the four incidents were resolved in under 46 minutes, yet the "average" is 85. When you report resolution times, it is often worth mentioning both the mean and the outlier ("one long-running network incident skewed the average"), because that is the honest picture your record keeping should give.

**Question 9 (moderate) — Reading a two-way table**

This table shows incidents by service and severity for last month:

| Service | SEV1 | SEV2 | SEV3 | Total |
|---|---|---|---|---|
| Portal | 2 | 8 | 30 | 40 |
| Payments | 1 | 6 | 13 | 20 |
| Reporting | 0 | 4 | 36 | 40 |
| Total | 3 | 18 | 79 | 100 |

What percentage of the Payments service's incidents were SEV2?

- A) 6%
- B) 20%
- C) 30%
- D) 33%

**Correct answer: C**

**Explanation:** The question asks about SEV2 incidents *as a share of Payments incidents*, so both numbers come from the Payments row: 6 SEV2 incidents out of 20 Payments incidents. 6 ÷ 20 = 0.3, × 100 = 30%. Option A mistakes the raw count for a percentage. Option D (6 ÷ 18) wrongly uses the SEV2 column total as the whole — that would answer a different question ("what share of all SEV2 incidents were Payments?"). Two-way tables are everywhere in service reporting, and the whole skill is choosing the correct denominator: read the question twice and ask "percentage *of what*?". This care with denominators is exactly what keeps the statistics in your weekly summaries accurate and defensible.

**Question 10 (hard) — Capacity headroom projection**

A file store currently holds 720 GB of data on a 1,000 GB volume. Usage has grown by 20 GB in each of the last four weeks. The team's rule is to raise a capacity warning when usage is projected to exceed 90% within four weeks. Should you raise the warning, and why?

- A) No — usage is only 72% now, well below 90%.
- B) Yes — in four weeks usage is projected at 800 GB, which is 80%, and that breaches the rule.
- C) Yes — in four weeks usage is projected at 800 GB, which is 80%; but 90% of 1,000 GB is 900 GB, so no breach is projected and no warning is needed. Wait — this option contradicts itself.
- D) No — projected usage in four weeks is 720 + (4 × 20) = 800 GB, which is 80% of the volume, below the 90% trigger, so the rule does not require a warning yet.

**Correct answer: D**

**Explanation:** Step through it. Growth rate: 20 GB per week. Projection over four weeks: 4 × 20 = 80 GB. Projected usage: 720 + 80 = 800 GB. The trigger level: 90% of 1,000 GB = 900 GB. Compare: 800 GB is below 900 GB, so the projection does not breach the rule, and the warning is not yet required. Option A reaches the right action for the wrong reason — the rule is about the *projection*, not today's figure, so "72% now" alone doesn't answer it. Option B does the projection correctly but then misreads 80% as breaching a 90% trigger. Option C is deliberately self-contradictory, and spotting that is part of careful reading. The professional follow-up, worth noting even though the rule doesn't demand action, is that at 20 GB/week the store hits 900 GB in (900 − 720) ÷ 20 = 9 weeks — a fact worth a line in your monitoring notes, because proactive monitoring means knowing when the warning *will* come due, not just whether it is due today.

**Question 11 (hard) — Weighted availability across services**

Your manager asks for the overall availability across two services, weighted by usage. Service A had 99.0% availability and handled 3 million requests. Service B had 99.8% availability and handled 1 million requests. What is the usage-weighted average availability?

- A) 99.40%
- B) 99.20%
- C) 99.60%
- D) 99.80%

**Correct answer: B**

**Explanation:** A weighted average multiplies each value by its weight, sums the results, and divides by the total weight. Weights: 3 million and 1 million, total 4 million. Step 1: 99.0 × 3 = 297.0. Step 2: 99.8 × 1 = 99.8. Step 3: sum = 297.0 + 99.8 = 396.8. Step 4: divide by 4: 396.8 ÷ 4 = 99.2. So the weighted availability is 99.20%. The unweighted average, (99.0 + 99.8) ÷ 2 = 99.4%, is option A — the classic trap. The weighted figure is lower because the less reliable service carries three times the traffic, so users experienced more of its failures. This is a genuinely important idea for availability reporting: an unweighted average can flatter the picture, and the KPI that matters to users is the one weighted by how much they actually use each service.

**Question 12 (hard) — Trend, rate, and a deadline**

At 09:00 a message queue contains 6,000 items. Messages are arriving at 900 per hour and being processed at 600 per hour. The queue's alert threshold is 9,000 items, and the daily change freeze starts at 17:00, after which no fix can be applied until tomorrow. Will the queue breach the threshold before the freeze, and roughly when?

- A) No — the queue is shrinking because processing is continuous.
- B) Yes — the queue grows by 300 items per hour and reaches 9,000 at 19:00, which is after the freeze, so a fix must be arranged before 17:00 anyway.
- C) Yes — the queue reaches 9,000 at 14:00, well before the freeze.
- D) No — the queue reaches only 8,400 by 17:00 and the threshold is never relevant.

**Correct answer: B**

**Explanation:** Find the net rate first: arrivals 900/hour minus processing 600/hour = net growth of 300 items per hour. The gap to the threshold: 9,000 − 6,000 = 3,000 items. Time to breach: 3,000 ÷ 300 = 10 hours after 09:00, which is 19:00. So the breach itself lands *after* the 17:00 freeze — but that is exactly why the situation is urgent: if nothing is fixed before 17:00, the breach at 19:00 becomes unavoidable until the next day. Check option D's arithmetic: by 17:00 (8 hours), the queue is 6,000 + 8 × 300 = 8,400 — the number is right, but the conclusion ("never relevant") ignores what happens at 19:00. Option C miscalculates the breach time. The lesson is one every control centre learns: combine the trend (net rate), the threshold, and the operational calendar (the freeze) before deciding whether "later today" means "someone else's problem" or "escalate now". Here, escalating well before 17:00 is the numerate, proactive answer.

### Preparation tips

- **Refresh the big four.** Percentages, averages, ratios, and rates cover almost every question. Ten minutes a day converting between them (0.5% of 43,200; 8:1 as a fraction; per-hour to per-day) rebuilds fluency fast.
- **Always name your denominator.** Before dividing, say to yourself "percentage of *what*?" Most table errors are denominator errors.
- **Convert units first.** Mixed minutes and hours (or GB and TB) cause more wrong answers than hard arithmetic does. Convert everything to one unit before you calculate.
- **Use the calculator, but estimate first.** A rough estimate ("about 20%") catches typos ("2.04%") instantly.
- **Practise on your own reports.** Take last week's real dashboard and recalculate one figure yourself — availability, escalation rate, average resolution time. Real data is the best practice data.
- **Show working on scrap paper even in a test.** Writing the steps (total, then divide) keeps you honest under time pressure and makes it easy to re-check a doubtful answer.

### Common pitfalls to avoid

- **Dividing by the new value in percentage change.** Change is always measured against the *original* figure. June to July means divide by June.
- **Averaging percentages without weights.** When services differ in size or traffic, the plain average of their percentages can mislead — check whether the question implies weighting.
- **Reading the wrong row or column.** Two-way tables punish haste. Put your finger (or cursor) on the row you need and keep it there.
- **Forgetting to convert time units.** "4 hours" hiding among minutes is a deliberate trap; it will appear again and again.
- **Stopping at the calculation and skipping the comparison.** Many questions end "does this breach the threshold?" — the arithmetic is only half the answer; the comparison is the other half.
- **Panic-guessing when numbers look big.** 43,200 minutes is just 30 × 24 × 60. Big numbers usually come from simple multiplications, and they divide just as easily.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and reason from written material — using the kinds of documents your job really involves. For an operations analyst in a command and control centre, that means procedure extracts, incident notifications, handover notes, service bulletins, emails from support teams, and short policy passages about things like change control and continuity.

The typical format is an online, timed test of 15 to 25 minutes. You are shown a short passage and asked questions about it. The most common question style is "True / False / Cannot say": a statement is presented, and you must decide whether the passage makes it definitely true, definitely false, or whether the passage simply doesn't give enough information to decide. Other question styles include choosing the best summary of a passage, identifying what a passage implies (rather than states), and judging which of several sentences communicates a point most clearly. Scoring is objective and usually norm-referenced, and — as with the other assessments — accuracy and speed are both recorded.

Why do employers use verbal reasoning for this role? Because so much of your work arrives as text and leaves as text. You read procedures and must apply them exactly. You read alerts and notifications and must extract the facts that matter. You write incident records, and the required information you gather must be captured precisely so the appropriate channel can act on it. You produce administrative summaries for your manager where one loose sentence can create a wrong impression. Misreading a single word — "may" instead of "must", "all" instead of "some" — can turn a correct action into a wrong one. Verbal reasoning practice trains the exact, careful reading that safe operations depend on.

A key rule to absorb before the practice questions: answer only from the passage. In "Cannot say" questions especially, the test is whether you can resist filling gaps with your own knowledge. If the passage doesn't say it and doesn't logically guarantee it, the answer is "Cannot say" — even when you happen to know it's true in real life.

### How this assessment maps to your role

- **Comprehension of procedures** maps to **Change management** and **Continuity management**: applying change control procedures under supervision, and explaining the basic principles of continuity processes, both start with reading procedural text exactly as written.
- **Extracting facts from notifications** maps to **Incident management**: identifying and registering incidents means pulling the required information — what, where, when, who is affected — out of alert text and user reports without adding or losing anything.
- **True/false/cannot-say discipline** maps to **Asset and configuration management** and record keeping: correcting information requires knowing the difference between what a record states, what it implies, and what it simply doesn't cover.
- **Inference and tone** map to **Community collaboration** and **User focus**: contributing to the work of others, and engaging with users or stakeholders to collate user needs evidence, both depend on reading messages accurately — including what a frustrated user's email is really telling you.
- **Clear-writing judgement** maps to your **administrative support** duties and **Service focus**: your summaries and updates must take inputs and turn them into coherent, readable records that work for the next reader.

### Practice questions

**Question 1 (easy) — Basic comprehension of a bulletin**

Passage: "The service desk will move to the new ticketing system on Monday 3 June. From that date, all new incidents must be registered in the new system. Incidents already open in the old system will continue to be worked there until they are closed. The old system becomes read-only on 1 July."

Statement: "After 3 June, a brand-new incident may be registered in the old system."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says that from 3 June "all new incidents must be registered in the new system." The word "all" leaves no exceptions, so registering a new incident in the old system after that date would contradict the passage. The statement is therefore false. Notice the difference between new and existing incidents: existing ones stay in the old system until closed, and that is what makes the wrong answer tempting if you skim. In your job, transition notices like this one arrive regularly, and acting on a skim-read ("the old system is still open, so I'll log it there") creates exactly the kind of record-keeping mess your asset and configuration discipline exists to prevent. Read for the categories the passage sets up — new versus existing — and apply the right rule to the right category.

**Question 2 (easy) — True/false/cannot say on a status update**

Passage: "At 10:20 the payments service began returning errors for approximately 15% of transactions. The support team identified a failed component at 10:45 and restarted it. Error rates returned to normal levels by 11:05. The root cause is under investigation."

Statement: "The failed component caused the transaction errors."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Read carefully what the passage commits to. A component failed, it was restarted, and errors then stopped — but the passage explicitly says "the root cause is under investigation." The sequence strongly *suggests* the component caused the errors, and in real life it would be a good hypothesis, but suggestion is not statement. The passage does not say the component caused the errors, and it flags that the cause is not yet established. So the correct answer is "Cannot say." This mirrors the disciplined language you should use in incident records: "errors ceased after the restart" is a fact; "the component caused the errors" is a conclusion that belongs to the investigation. Assessors reward — and good control centres depend on — writers who keep facts and conclusions clearly separated.

**Question 3 (easy) — Extracting required information**

Passage (email from a user): "Hi team — since about half past nine this morning, nobody in our Leeds office has been able to open the case tracking system. We just get a spinning wheel. The Manchester office says theirs is fine. We have a tribunal deadline today so this is quite urgent. Thanks, Priya."

Which set of facts should go into the incident record?

- A) System affected: case tracking. Impact: all users nationally. Start: 09:30 approx. Urgency: high.
- B) System affected: case tracking. Impact: Leeds office users; Manchester unaffected. Start: 09:30 approx. Urgency: high (tribunal deadline today).
- C) System affected: email. Impact: Leeds office. Start: this morning. Urgency: normal.
- D) System affected: case tracking. Impact: Leeds office. Start: 09:30 approx. Urgency: low, since Manchester is working.

**Correct answer: B**

**Explanation:** Go through the email fact by fact. The system is case tracking (not email — the message merely arrived by email). The impact is the Leeds office, and the detail that Manchester is fine is valuable diagnostic information worth recording, because it suggests a local or network issue rather than a full outage. The start time is "about half past nine", best recorded as approximately 09:30. The urgency is high because of a same-day tribunal deadline — a concrete business impact. Option A wrongly inflates the impact to national; option D wrongly deflates the urgency because one office works. Gathering the required information and allocating the incident to the appropriate channel is your core incident management duty, and this is what it looks like in practice: capture what the user said, preserve the diagnostic clues, and record the business reason for urgency in plain terms.

**Question 4 (easy) — Following written instructions exactly**

Passage (from the monitoring procedure): "Perform the morning checks between 08:30 and 09:30. Record each check result as PASS or FAIL in the checks log. If any check FAILS, register an incident and note the incident number next to the FAIL entry. Do not mark the morning checks complete until every line has either a PASS or a FAIL with an incident number."

You have completed nine checks: eight PASS, one FAIL. You registered incident INC-5120 for the failure. What remains before you may mark the checks complete?

- A) Nothing — all checks have results and the incident exists.
- B) Confirm the incident number INC-5120 is written next to the FAIL entry in the log.
- C) Re-run the failed check until it passes.
- D) Wait until 09:30, since checks cannot be completed early.

**Correct answer: B**

**Explanation:** The procedure sets a precise completion condition: every line must show either PASS, or FAIL *with an incident number noted next to it*. You have registered the incident, but the passage's condition is about what is written in the log — so the remaining step is confirming the incident number appears beside the FAIL entry. Option A skips that final recording step, which is exactly the sort of small documentation gap that procedures are written to prevent. Option C invents a requirement (the procedure never says a FAIL must be turned into a PASS), and option D misreads the time window: 08:30–09:30 is when checks must be *performed*, not a bar on finishing early. Precision like this is the whole game in procedural reading: completion conditions, time windows, and recording requirements each mean exactly what they say.

**Question 5 (moderate) — Inference from a continuity policy extract**

Passage: "Each critical service must have a documented continuity procedure. Continuity procedures must be reviewed at least annually. The case tracking system's continuity procedure was last reviewed fourteen months ago. The case tracking system is classified as a critical service."

Statement: "The case tracking system's continuity procedure is currently out of compliance with the review requirement."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Chain the passage's statements together. Critical services need continuity procedures reviewed at least annually — that is, within the last twelve months. Case tracking is critical, so the requirement applies to it. Its procedure was last reviewed fourteen months ago, which is more than twelve. Therefore the review requirement is currently not met, and the statement is true. This is a valid deduction, not an assumption: every link comes from the passage. Contrast this with Question 2, where the conclusion needed information the passage withheld. Learning to feel that difference — "the passage guarantees this" versus "the passage merely hints at this" — is the central verbal reasoning skill, and it matches the continuity management basics in your role: knowing what the policy actually requires is the first step in explaining continuity principles to anyone else.

**Question 6 (moderate) — Identifying the main point**

Passage: "Monitoring thresholds exist to draw attention to abnormal conditions. If thresholds are set too tightly, analysts receive frequent alerts for conditions that resolve themselves, and genuine problems risk being lost in the noise. If thresholds are set too loosely, genuine problems may not generate alerts until users are already affected. Threshold reviews should therefore use recent operational data to balance sensitivity against noise."

Which option best states the main point?

- A) Monitoring thresholds should be as sensitive as possible so nothing is missed.
- B) Analysts receive too many alerts.
- C) Threshold settings involve a trade-off, and reviews should use real data to balance it.
- D) Users are usually affected before alerts fire.

**Correct answer: C**

**Explanation:** The passage has a classic shape: a purpose, two opposite failure modes (too tight, too loose), and a recommendation that follows from them. The main point is the trade-off plus the recommendation — option C. Option A contradicts the passage, which explicitly warns against over-tight thresholds. Options B and D each take one half of one failure mode and present it as the whole message; they are details, not the point. Summarising accurately matters in your role because your manager often reads only your summary line: if you compress a balanced bulletin into a one-sided warning, the decision made on your summary may be wrong. When you take inputs and establish coherent frameworks — your service focus skill — the coherence starts with representing the source material faithfully.

**Question 7 (moderate) — True/false/cannot say with tempting outside knowledge**

Passage: "The department's change calendar shows a firewall update scheduled for Thursday evening. The change record states that no user-facing services will be affected. The control centre has been asked to monitor the appointments service closely on Thursday evening as a precaution."

Statement: "The firewall update will affect the appointments service."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** This one pulls in two directions. The change record *states* no user-facing services will be affected — but a record's claim is a prediction, and the passage does not confirm the outcome. Meanwhile, the request for close monitoring "as a precaution" might make you suspect trouble — but a precaution is not a prediction of failure either. The passage neither guarantees the statement true nor guarantees it false: it reports one claim (no impact expected) and one prudent action (monitor anyway). So the answer is "Cannot say." If you answered B, you treated the change record's claim as settled fact; if you answered A, you treated the precaution as evidence of expected impact. Both moves add certainty the text doesn't contain. This exact tension — records say one thing, precautions hint at another — is everyday life in a control centre, and the analysts who thrive are the ones who keep claims, hints and facts in separate mental boxes.

**Question 8 (moderate) — Choosing the clearest rewrite**

Your draft handover line reads: "The thing with the reports that was happening before is still sort of going on, though it's better than it was, but keep an eye on it."

Which rewrite is clearest and most useful for the next shift?

- A) "Reports issue ongoing. Monitor."
- B) "INC-5133 (report generation delays) remains open. Delays have reduced from 40 minutes to 10 minutes since 14:00. Continue monitoring; escalate to the data team if delays exceed 20 minutes."
- C) "The report generation situation has substantially ameliorated relative to its antecedent state, notwithstanding residual latency."
- D) "Reports were broken earlier. Someone should probably check them at some point."

**Correct answer: B**

**Explanation:** Good operational writing answers three questions for the next reader: what exactly is the situation, what has changed, and what should I do? Option B does all three, with an incident reference, concrete numbers, a timestamp, and a clear action with a trigger condition. Option A is admirably short but strips out the reference, the trend, and the escalation trigger — the next shift can't tell whether "monitor" means "all calm" or "on a knife-edge." Option C uses long words to say almost nothing, and option D is vague about both state and action. Notice that clarity is not the same as brevity: the clearest option here is the second-longest because the content earns its space. Handover notes, incident updates, and the records you keep are read by people under pressure; writing like option B is one of the most valuable habits an operations analyst can build, and clear-writing questions in assessments reward exactly this judgement.

**Question 9 (moderate) — Inference about process, not content**

Passage: "All change requests must be submitted using form CR-1. Requests submitted by email will be returned to the sender with a link to the form. On Tuesday, Sam emailed a change request to the change team."

Statement: "Sam's request will be processed after the change team transfers it into form CR-1."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage states the process for emailed requests: they are "returned to the sender with a link to the form." That is what happens — the sender must resubmit properly; nothing in the passage says the change team transfers requests into the form themselves. The statement describes a different process from the one the passage defines, so it is false, not merely unsupported. The distinction between "false" and "cannot say" trips many candidates: choose "false" when the passage actively contradicts the statement (as here — the stated procedure is return-to-sender, which excludes team-side transfer for emailed requests), and "cannot say" when the passage is simply silent. Reading procedures at this level of precision is the foundation of applying change control correctly under supervision: knowing not just what must happen, but who the procedure says must do it.

**Question 10 (hard) — Reconciling two passages**

Passage 1 (service bulletin, Monday): "Planned maintenance will take the document store offline on Saturday from 06:00 to 12:00. Users should save local copies of any documents they need during this window."

Passage 2 (email, Thursday): "Following stakeholder feedback, the document store maintenance has been shortened. The store will now be offline on Saturday from 06:00 to 09:00 only. All other details in Monday's bulletin still apply."

Statement: "According to the latest information, a user who needs a document at 10:00 on Saturday will need a local copy."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** When two documents conflict, the later one governs — and Passage 2 explicitly updates the window to 06:00–09:00, keeping other details unchanged. At 10:00 on Saturday the store will therefore be back online, so a user at 10:00 does not need a local copy, making the statement false. The reasoning has two steps: recognise that Thursday's email supersedes Monday's bulletin on the one point it changes, and then apply the new window to the 10:00 case. A hasty reader anchors on the first passage's 12:00 end time and answers "true." Handling updates and supersessions is genuine control-centre work: notices are revised, change windows move, and your record keeping must always reflect the latest authoritative version — while noting, for the audit trail, what changed and when. If you found yourself wondering whether maintenance might overrun, notice that this is outside knowledge: the question asks what the latest information says, not what might go wrong on the day.

**Question 11 (hard) — Evaluating an argument's logic**

Passage: "Last month we introduced daily configuration audits. This month, configuration errors found in live services fell by 60%. Therefore the daily audits caused the reduction in errors, and every team should adopt daily audits immediately."

Which is the strongest criticism of this argument?

- A) The percentage is suspicious because 60 is a round number.
- B) The argument moves from a sequence in time to a claim of cause, without ruling out other explanations, and generalises from one team's month to all teams.
- C) Configuration audits are a waste of time.
- D) The argument should have used weekly audits as the comparison.

**Correct answer: B**

**Explanation:** Two logical leaps happen in quick succession. First, "errors fell after we introduced audits" becomes "audits caused the fall" — the classic *after this, therefore because of this* mistake. Other explanations (a quieter change calendar this month, a major fix last month, seasonal workload) haven't been ruled out. Second, one team's single-month experience becomes a recommendation for "every team... immediately" — a generalisation the evidence can't yet carry. Option B names both leaps. Option A attacks the number's roundness, which is irrelevant to the logic; option C rejects the conclusion without engaging the reasoning; option D proposes a different study rather than criticising this one. Why does this matter for you? Because control centres constantly generate before/after stories ("we restarted it and it got better"), and the problem management part of your role — investigating problems and contributing to remedies — depends on treating such stories as hypotheses to test, not conclusions to file. Being able to say, kindly and precisely, "that's a correlation, and here's how we could confirm it" is a professional skill assessors actively look for.

**Question 12 (hard) — Precision with modal language**

Passage (extract from the on-call guidance): "Analysts may be contacted outside working hours only when a SEV1 incident is open. When contacted, an analyst must acknowledge within 30 minutes. An analyst who is unavailable must have arranged cover in advance. Acknowledging an incident does not require the analyst to begin work on it immediately; it confirms the contact was received."

Which statement is consistent with the passage?

- A) An analyst contacted about a SEV2 incident out of hours must acknowledge within 30 minutes.
- B) Acknowledging within 30 minutes commits the analyst to starting work immediately.
- C) An analyst who has arranged cover in advance may be unavailable when contacted.
- D) Analysts must be available at all times without exception.

**Correct answer: C**

**Explanation:** Take the options against the text. Option A fails at the first rule: out-of-hours contact is permitted *only* for SEV1, so the guidance doesn't govern a SEV2 contact — the scenario itself falls outside the rules, and the passage imposes no acknowledgement duty for it. Option B is directly contradicted: the passage says acknowledging "does not require the analyst to begin work on it immediately." Option D is contradicted by the cover arrangement, which exists precisely so an analyst can be unavailable. Option C restates the cover rule correctly: unavailability is permitted when cover was arranged in advance. The skill being tested is modal precision — the difference between *may*, *must*, *only*, and *does not require*. These small words carry the entire meaning of operational policies, and misreading them out of hours, when you are tired and the pressure is real, is how well-meaning analysts break rules they thought they were following. Practising this precision in the calm of an assessment builds the habit for the moments that matter.

### Preparation tips

- **Read the statement twice before judging it.** Most "cannot say" errors come from judging a slightly different statement than the one written.
- **Learn the false/cannot-say boundary.** "False" needs an actual contradiction in the passage; silence means "cannot say." Practise sorting statements into those two bins.
- **Circle the modal words.** May, must, only, all, some, unless, at least — underline them mentally (or literally, on scrap paper). They decide more answers than any other words.
- **Practise on real workplace text.** Take a genuine procedure or bulletin from your intranet, write three statements about it (one true, one false, one unsupported), and check your reasoning. Five minutes of this daily is transformative.
- **Summarise as a habit.** After reading any work email, try stating its main point in one sentence. The "best summary" questions become easy when summarising is routine.
- **Don't bring your job into the test.** Ironically, experienced staff sometimes score lower because they answer from experience rather than the passage. In the test, the passage is the whole world.

### Common pitfalls to avoid

- **Filling gaps with knowledge.** You may know that restarts usually fix that error; if the passage doesn't say so, "cannot say" is still the answer.
- **Anchoring on the first document.** When a later message updates an earlier one, the update wins. Watch for "supersedes", "now", and "still apply."
- **Confusing suggestion with statement.** "Errors stopped after the restart" suggests causation but states only sequence. Keep them separate.
- **Equating brevity with clarity.** The clearest option is the one that answers what/changed/do-next — sometimes that takes a full sentence or three.
- **Missing category words.** "New incidents" versus "existing incidents", "critical services" versus "all services" — passages set up categories, and questions test whether you kept them straight.
- **Rushing the final option.** Verbal questions often place the correct choice last, after three near-misses. Read all the options before committing.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (often called an SJT) presents you with realistic workplace scenarios and asks you to judge how effective different responses would be. Unlike the other three assessments, there is no arithmetic and no passage analysis; instead, the test measures your practical judgement — your instinct for what a professional at your level should do when situations are messy, time is short, and people are involved.

The typical format is an online test of 20 to 40 minutes with 10 to 20 scenarios. Each scenario describes a situation you might face as an operations analyst, followed by three to five possible responses. Question styles vary: you may be asked to pick the *most* effective response, the *least* effective response, to rank all the responses from best to worst, or to rate each response independently on a scale. There is often no time pressure per question, but the overall test is timed. Scoring compares your judgements against those of experienced professionals and subject-matter experts, so the "right" answers reflect how effective behaviour is generally understood in roles like yours — not trick logic.

Why do employers use SJTs for this role? Because an operations analyst's day is full of judgement calls that no procedure fully covers: whether to interrupt a busy engineer, when to escalate versus keep watching, how to tell a manager about a mistake, how to respond to a frustrated user. The role summary is explicit that you provide administrative support, alert support staff when necessary, and own an issue until a new owner has been found — and the word "necessary" is a judgement every single time. SJTs let employers see that judgement safely, before real incidents test it. For you, SJT practice is a chance to rehearse tricky moments in advance, so that when they happen for real, you have already thought them through.

A helpful mindset for SJTs at your level: the most effective responses usually combine honesty, promptness, appropriate escalation, and care for users and colleagues. The least effective responses usually involve hiding problems, exceeding your authority, delaying without reason, or passing blame. When in doubt, ask yourself: "What would the calm, honest, team-minded version of me do?"

### How this assessment maps to your role

- **Escalation judgement** maps to **Incident management** and your duty to alert support staff when necessary: knowing when to escalate, what information to attach, and when watching and waiting is the better call.
- **Ownership behaviours** map to **Ownership and initiative**: owning an issue until a new owner has been found or the problem has been mitigated or resolved — which in scenario terms means not dropping things, not assuming someone else has it, and closing loops.
- **Team scenarios** map to **Community collaboration**: contributing to the work of others, helping create the right environment for the team, and recognising and dealing with issues rather than letting them fester.
- **User scenarios** map to **User focus**: engaging with users to collate needs evidence, and using quantitative and qualitative data about users to turn user focus into outcomes — which begins with taking user reports seriously and treating users with respect.
- **Integrity and accuracy scenarios** map to **Asset and configuration management** and **Change management**: keeping records truthful, correcting errors including your own, and following change control even when a shortcut beckons.

### Practice questions

**Question 1 (easy) — A mistake in your own work**

While preparing the weekly report for your manager, you realise that last week's report — already sent — contained an error you made: it overstated the number of resolved incidents by 15. Nobody has noticed. What is the most effective response?

- A) Say nothing; it is unlikely anyone will check, and this week's report will be correct.
- B) Tell your manager promptly, explain the error and its size, and send a short correction so decisions aren't based on wrong figures.
- C) Quietly adjust this week's figures downward by 15 to make the totals balance out over time.
- D) Wait to see whether anyone queries the figure, and correct it only if asked.

**Correct answer: B**

**Explanation:** Option B is honest, prompt, and practical: it fixes the record, protects any decisions that might rely on the figure, and shows your manager they can trust you to self-correct. Option A gambles your credibility on nobody checking — and reports get compared over time, so discrepancies surface. Option C is the worst of all: it deliberately falsifies a second report to hide the first error, converting an honest mistake into a record-keeping integrity problem. Option D outsources your responsibility to chance. The professional behaviour being assessed is ownership: your role asks you to own issues until they are resolved, and that applies doubly to issues you created. Everyone makes errors in reports; what distinguishes a trusted analyst is the speed and openness of the correction. Managers consistently say the same thing: the mistake costs a moment's awkwardness, but the cover-up costs the relationship.

**Question 2 (easy) — Unsure whether to escalate**

You notice an unusual pattern on the monitoring dashboard: a service's error rate has doubled in the past hour, but it is still below the formal alert threshold. Your manager is in a meeting, and the procedure doesn't cover this exact situation. What is the most effective response?

- A) Do nothing until the formal threshold is breached, since the procedure defines that as the trigger.
- B) Register a full SEV1 incident immediately to be safe.
- C) Make a note of the pattern with timestamps, mention it to the relevant support team as a heads-up, and keep watching closely; brief your manager after the meeting.
- D) Restart the affected service yourself before it gets worse.

**Correct answer: C**

**Explanation:** This scenario sits exactly in the space your role was created for: proactive monitoring means noticing potential problems *before* thresholds and procedures force everyone's hand. Option C does everything an analyst at your level should do — record the evidence, alert the people who can act (a proportionate heads-up rather than a formal escalation), continue monitoring, and keep your manager informed. Option A treats the procedure as permission to ignore your own observation; procedures set minimum triggers, not maximum attentiveness. Option B over-escalates: crying SEV1 for a below-threshold trend spends the team's trust and can desensitise everyone to real emergencies. Option D exceeds your authority and bypasses change control — restarting live services is not an analyst's unilateral call, and a restart can destroy diagnostic evidence. The judgement being rewarded is proportionality: act early, act visibly, but act at the right level.

**Question 3 (easy) — A colleague asks you to skip a step**

An engineer you like and respect asks you to log a change as already approved "because the approval will definitely come through this afternoon, and we're in a hurry." What is the most effective response?

- A) Do it — the approval is a formality and the team's speed matters.
- B) Refuse rudely and report the engineer to their manager immediately.
- C) Politely decline to record an approval that hasn't happened, offer to prepare everything else so the change can proceed the moment approval arrives, and flag the time pressure to your manager if the approval is genuinely urgent.
- D) Log it as approved but keep a private note that it wasn't, in case questions come up later.

**Correct answer: C**

**Explanation:** The record must say what is true — that principle is the bedrock of change management and of your asset and configuration duty to keep information accurate. Option C holds the line without damaging the relationship: you decline the false entry, you actively help with everything legitimate (preparing the change so no time is lost), and you use the proper route (your manager) if the approval bottleneck is a real problem. Option A makes you the author of a false record; if the approval doesn't come, or the change goes wrong, the log now misleads everyone investigating. Option D is stranger and worse: an official record you privately know to be false, plus a secret note, is indefensible. Option B gets the refusal right and everything else wrong — escalating a first-time, probably well-intentioned request straight to their manager, with rudeness, damages collaboration your role depends on. Notice the pattern in strong SJT answers: hold the standard, stay kind, offer a legitimate path to the same goal.

**Question 4 (easy) — Handling a frustrated user**

A user phones the control centre, angry: "This is the third time this month the portal has crashed while I was in the middle of an application. You people clearly don't care." What is the most effective response?

- A) Point out that the control centre doesn't build the portal, so it isn't your fault.
- B) Listen, acknowledge the frustration, take full details of all three occurrences, register the incident, and explain what will happen next — then make sure the repeat pattern is flagged, not just today's crash.
- C) Tell them to raise a complaint through the official complaints process and end the call.
- D) Apologise repeatedly but take no details, to keep the call short.

**Correct answer: B**

**Explanation:** Option B treats the caller as a person and the call as data — both matter. Acknowledging frustration costs nothing and de-escalates; taking details of all three occurrences turns an angry call into exactly the qualitative and quantitative user evidence your user focus skill asks you to collate; flagging the *repeat* pattern feeds problem management, because three crashes in a month is a problem signature, not three unrelated incidents. Option A may be technically true and is completely unhelpful — users experience the service, not the org chart, and deflection reads as the very "not caring" they accused you of. Option C abandons a live issue and a user mid-need. Option D is warm but useless: sympathy without a record helps neither the user nor the investigation. The behaviours rewarded here are user focus and ownership: the user's third bad experience becomes your issue until it is properly registered, understood, and moving toward resolution.

**Question 5 (moderate) — Conflicting instructions**

Your manager asked you this morning to spend the day tidying the asset register before Friday's audit. At noon, a senior engineer from the network team tells you to drop that and spend the afternoon helping them test a new dashboard, saying "the audit stuff can wait." What is the most effective response?

- A) Follow the engineer's instruction — they are more senior than you.
- B) Refuse the engineer flatly and continue with the register without telling anyone.
- C) Ignore both tasks and work your normal monitoring queue.
- D) Explain to the engineer that your manager has prioritised the audit preparation, and offer to check with your manager right away whether the priority should change.

**Correct answer: D**

**Explanation:** This is a classic tasking-conflict scenario, and the strong move is almost always the same: be transparent, and route the priority decision to the person who owns your priorities — your manager. Option D does that while treating the engineer respectfully and leaving room for the genuine possibility that the dashboard is more important (you don't actually know; that is exactly why you check). Option A lets seniority override an explicit instruction from your line manager without anyone agreeing to it — if the audit preparation slips and Friday goes badly, "a senior person told me to" will not repair the gap. Option B gets the priority right but the collaboration wrong: silently refusing builds friction, and your manager loses the chance to make an informed call. Option C dodges the conflict entirely. The professional behaviours in play are collaboration and escalation: conflicts between legitimate demands are normal, and resolving them openly through the right person is a skill, not a weakness.

**Question 6 (moderate) — You spot a colleague's error**

Reviewing yesterday's records, you notice a fellow analyst registered an incident against the wrong service — the ticket says "Payments" but the details clearly describe the reporting system. The colleague is on shift with you today. What is the most effective response?

- A) Correct the record silently so no one ever knows.
- B) Mention it to the colleague directly and kindly, so they can correct it and learn from it; if the miscategorisation has already misdirected any work, make sure the affected team is told.
- C) Email the whole team about the importance of accurate categorisation, without naming anyone.
- D) Report the error to your manager before speaking to the colleague.

**Correct answer: B**

**Explanation:** Option B respects both the record and the colleague. Going to them first is collegial and proportionate for an ordinary, non-recurring error; letting them make the correction preserves their ownership and their learning. The check about misdirected work matters operationally: a Payments-tagged ticket may have gone to the Payments queue, and someone may be investigating the wrong system right now. Option A fixes the data but hides the learning — and silently editing colleagues' records, even correctly, erodes the trust a shared record system depends on. Option C is passive-aggressive theatre: everyone wonders who it was, the colleague may not even recognise themselves, and nothing is actually corrected. Option D escalates before the simplest, kindest step has been tried; managers should hear about patterns, not first offences that peer conversation can fix. This maps to your community collaboration skill — recognising and dealing with issues — and to keeping information accurate. Teams where peers can correct each other kindly are teams where records stay clean.

**Question 7 (moderate) — Pressure to close incidents before month end**

It is the last day of the month. A team lead (not your manager) suggests you close five open incidents today "since they're basically done", so the monthly resolution statistics look better. Two of the five are genuinely resolved but awaiting user confirmation; three still have outstanding actions. What is the most effective response?

- A) Close all five — they will probably be fine, and the team's statistics matter for funding.
- B) Close none and say nothing, quietly leaving all five open.
- C) Close only what the process genuinely allows (chase the two user confirmations today so they may close properly), leave the three unfinished incidents open, and be straightforward with the team lead about why.
- D) Close the two awaiting confirmation without chasing the users, and leave the other three open.

**Correct answer: C**

**Explanation:** The heart of this scenario is that statistics exist to describe reality, not to be manufactured. Option C is both honest and genuinely helpful: chasing the two user confirmations is legitimate month-end diligence that may allow two proper closures today, while the three incidents with outstanding actions simply are not resolved, and closing them would falsify the record and risk users being left with broken services and closed tickets. Being straightforward with the team lead — kindly, and with the reason — keeps the relationship workable and gives them the chance to step back from a bad suggestion. Option A prioritises appearances over truth and users; if a "closed" incident re-erupts next week, the record shows the closure was cosmetic. Option D closes tickets whose defining requirement (user confirmation) is unmet — a smaller version of the same falsification. Option B protects the record but ducks the human moment; silence leaves the team lead thinking the suggestion was fine. The behaviours rewarded: integrity in record keeping, user focus (a ticket is for the user, not the statistic), and the confidence to disagree politely with someone senior.

**Question 8 (moderate) — An alert during handover**

You are ten minutes from the end of your shift, mid-handover, when a SEV2 alert fires on the appointments service. Your incoming colleague hasn't finished reading the handover note. What is the most effective response?

- A) Leave on time — the incoming analyst is now responsible for everything that happens on their shift.
- B) Register and triage the alert yourself now, tell the incoming colleague exactly what you've done and what remains, add it to the handover note, and leave once the handover of this incident is genuinely complete.
- C) Handle the entire incident to resolution yourself, however long it takes, without involving the incoming colleague.
- D) Ask the incoming colleague to deal with it alone while you finish writing the handover note about other matters.

**Correct answer: B**

**Explanation:** Ownership does not end at a shift boundary — it ends at a *successful transfer*. Option B embodies that: you take the immediate actions that can't wait (register, triage, escalate if needed), you transfer the incident explicitly with a spoken briefing *and* a written record, and you leave only when the new owner genuinely has it. That is the literal meaning of your ownership skill: own an issue until a new owner has been found. Option A follows the clock rather than the service; an alert that fires into a half-finished handover is precisely when things get dropped. Option C swings too far the other way — staying for hours duplicates effort, exhausts you, and denies your colleague the handover they need to own their own shift; heroics are not the goal. Option D forces a colleague to act without context, which is how triage errors happen. SJT scoring at analyst level consistently rewards the middle path: act on what is urgent, transfer deliberately, and treat the handover note as a live safety document rather than paperwork.

**Question 9 (moderate) — Asked for data you're not sure you should share**

A contractor working with a supplier emails you directly: "Can you send me the full asset register export for the data centre? Need it for our planning work." You have access to the export, but you're not sure whether the contractor is authorised to receive it. What is the most effective response?

- A) Send it — they're working with the department, and being helpful matters.
- B) Ignore the email; if it's important they'll ask someone else.
- C) Refuse and tell them asset data is never shared with anyone.
- D) Reply promptly that you'll check the authorisation first, then confirm with your manager or the information owner whether and how the data may be shared, and follow their steer.

**Correct answer: D**

**Correct-answer note and Explanation:** Option D balances helpfulness with protection. The asset register is exactly the kind of information your asset and configuration management skill exists to protect — it describes what the department owns, where it lives, and potentially where its weaknesses are. Sharing it requires knowing the recipient is authorised, and "I wasn't sure, so I checked" is always defensible, while "I wasn't sure, but I sent it" never is. Crucially, D also treats the contractor well: a prompt reply with a clear path ("I'm checking authorisation, will come back to you") is far more professional than silence. Option A confuses friendliness with due care; option B is discourteous and leaves a legitimate need unmet, possibly pushing the contractor to find a less careful source; option C invents a blanket rule that probably isn't true and blocks legitimate work. The behaviours rewarded are protective ownership of information, appropriate escalation of an authorisation question, and courtesy under uncertainty. At analyst level, no one expects you to know every data-sharing rule — they expect you to know when to ask.

**Question 10 (hard) — When your escalation is dismissed**

Yesterday you escalated a concern: a nightly backup job has failed three nights running, and the continuity runbook lists that backup as critical for service recovery. The engineer who received your escalation replied, "Known issue, don't worry about it," but the failures are continuing and nothing in the record shows a fix in progress. What is the most effective response?

- A) Accept the engineer's answer — they know the systems better than you do.
- B) Re-raise the concern with the engineer, referencing the continuity impact and asking what the plan is; if the answer still doesn't address the recovery risk, tell the engineer you'll need to flag it to your manager, and then do so with the evidence.
- C) Go straight to the engineer's head of service and report them for negligence.
- D) Fix the backup job yourself using instructions you found online.

**Correct answer: B**

**Explanation:** This is one of the hardest judgement patterns in operations: persisting with a concern after being told not to worry. The key facts are that the risk is concrete (a critical backup, per the runbook, failing repeatedly) and the reassurance is unevidenced (no fix in progress in the record). Option B persists proportionately: it goes back to the engineer first with a sharper, evidence-based question — "what is the plan, given continuity depends on this?" — which gives them a fair chance to reveal context you lack ("the fix ships tomorrow; here's the change reference"). If the answer still doesn't address the risk, B escalates transparently: telling the engineer you're flagging it isn't a threat, it's honesty, and it keeps the relationship intact. Option A abandons a continuity-critical concern on the strength of "don't worry" — but your role's ownership skill says you own an issue until it is mitigated or resolved, and reassurance without evidence is neither. Option C leaps past every intermediate step to an accusation, poisoning collaboration and possibly embarrassing yourself if there is a plan. Option D is the most dangerous: modifying backup jobs without authority or change control could corrupt the very recovery capability you're trying to protect. The rewarded behaviours: evidence-based persistence, fair warning, clean escalation, and respect for both the risk and the relationship.

**Question 11 (hard) — A quiet team member and a looming deadline**

Your small team is preparing evidence for a service review due in three days. In team discussions, one colleague — newer even than you — clearly has relevant information from their previous rotation, but a louder colleague keeps talking over them, and they have stopped contributing. The team lead hasn't noticed. What is the most effective response?

- A) Stay out of it — team dynamics are the team lead's job, and you're junior.
- B) In the next discussion, deliberately make space — "Before we move on, I'd like to hear Alex's view; they worked on this system last year" — and, if the pattern continues, mention it privately to the team lead as something worth watching.
- C) Publicly tell the louder colleague to stop interrupting people.
- D) Collect the quiet colleague's information privately and present it yourself so the review gets it.

**Correct answer: B**

**Explanation:** Your community collaboration skill explicitly includes helping create the right environment for teams and recognising and dealing with issues — and it doesn't say "only when senior." Option B acts at the lowest effective level: a simple, warm invitation in the moment ("I'd like to hear Alex's view") costs nothing, credits the colleague's expertise, and often fixes the dynamic on its own, because interrupters usually aren't malicious, just unaware. The private word with the team lead — framed as observation, not accusation — covers the case where the pattern persists and genuinely is the lead's to manage. Option A treats a fixable, deadline-relevant problem as someone else's; meanwhile the review loses the exact evidence it needs. Option C might work but risks a public confrontation that embarrasses everyone, including the person you're defending. Option D is the subtle trap: it gets the information into the review but takes the credit and the voice away from your colleague, teaching them that the only way to be heard is through an intermediary. The rewarded behaviours are inclusion, initiative within your level, and choosing the gentlest intervention that actually works. Notice that B also serves the deadline: inclusive teams surface more evidence, faster.

**Question 12 (hard) — Least effective: an ambiguous emergency out of hours**

You are not on call tonight, but at 22:30 you happen to notice — while checking something personal on your phone — a public social media post saying your department's licensing portal appears to be down. You can't verify from home whether it's a real outage. Which response is LEAST effective?

- A) Decide it's not your problem tonight, do nothing, and don't mention it tomorrow.
- B) Send a short message to the on-call analyst or duty channel with a link to the post — "not verified, spotted this, over to you" — and leave it with them.
- C) Do nothing tonight but check the monitoring history and mention the post first thing tomorrow.
- D) Try to log in to the admin console from your personal device to investigate and restart services yourself.

**Correct answer: A** (least effective)

**Explanation:** This question format flips the usual task: you are hunting for the *worst* response, and it helps to rate each option before choosing. Option B is clearly the best: a thirty-second, zero-drama handoff to the person whose job tonight actually is — the essence of "alert support staff if necessary" and of finding the issue a proper owner. Option D is bad — investigating live services from a personal device, outside your on-call duty and probably outside your authority, creates security and change-control risks — but it at least stems from a desire to help, and its dangers make it a strong candidate for "least effective" in some scoring schemes. Option C is imperfect (a real outage would run all night) but defensible: it neither risks anything nor hides anything. Option A, though, combines every failing at once: the service may be down for citizens all night, the on-call analyst never gets a free early warning that would cost you seconds to send, and the silence *the next day* converts an understandable evening judgement into concealment. Zero effort, zero honesty, zero user focus — where option D at least fails while trying to help, option A fails without trying at all. In "least effective" questions, look for the response that abandons both the users and the team while also breaking trust; passivity plus concealment usually beats even reckless helpfulness to the bottom. And note for real life: option B is genuinely all that is asked of you when you're off duty — proportionate, honest, and kind to your own work-life balance too.

### Preparation tips

- **Learn your role's boundaries.** Many SJT questions turn on authority: what an analyst may do alone (register, gather, escalate, monitor) versus what needs supervision or belongs to others (restarts, approvals, unsupervised changes). Re-read your role summary with that lens.
- **Rehearse the honest scripts.** "I made an error in last week's report"; "I can't log that as approved yet, but I can prepare everything else"; "I'm checking authorisation and will come back to you." Having words ready makes the right action easier, in tests and in life.
- **Rate every option before answering.** Especially in most/least questions, judge each response on its own (helps users? honest? right level? closes the loop?) rather than comparing them impressionistically.
- **Look for the response that combines action with communication.** The best options usually *do* something and *tell* someone. Options that only do, or only tell, or neither, rank lower.
- **Reflect on your real weeks.** After a tricky shift, ask: what were my options, and what would I rank them now? Your own history is the richest SJT practice bank there is.
- **Stay in character as your best self.** Answer as the analyst you are on a good day — honest, calm, team-minded — not as a theoretical perfect being or as your most tired Friday self.

### Common pitfalls to avoid

- **Choosing heroics.** Fixing everything yourself is rarely the top answer at analyst level; well-executed escalation and handover usually beat solo rescue.
- **Choosing pure deference.** "They're senior, so I did what they said" fails when it means falsifying records or dropping your manager's priorities without a word.
- **Punishing first offences.** Options that report a colleague before speaking to them typically rank low; proportionate, direct kindness ranks high.
- **Confusing silence with diplomacy.** Not telling the team lead, not correcting the report, not replying to the contractor — silence usually scores as avoidance, not tact.
- **Ignoring the record.** In this role, many scenarios have a record-keeping dimension (logs, registers, handover notes). Responses that leave the record wrong or incomplete lose marks even when the human handling is good.
- **Forgetting the user.** Behind every ticket and statistic is someone trying to apply, book, or renew something. Responses that serve appearances over users are almost never the intended answer.

## Conclusion

Well done for working through this guide. You have covered a lot of ground: what psychometric assessments are and how they work, and four full practice sets — cognitive, numeric, verbal, and situational judgement — built entirely from the real materials and real decisions of your role as an operations analyst in a command and control centre.

Take a moment to notice what you have practised. You have checked asset registers and handover notes for the one entry that doesn't fit. You have read change procedures the way they are meant to be read — condition by condition, with every "additionally" and "only" given its full weight. You have calculated availability percentages, downtime budgets, escalation rates, and weighted averages, and you have seen how a trend plus a threshold plus a calendar becomes an early warning. You have practised the hardest reading skill of all: keeping what a passage states, what it suggests, and what it never says in three separate boxes. And you have rehearsed the judgement calls that define this job — when to escalate, how to correct a mistake, how to hold a standard kindly, and how to hand over an incident so that ownership genuinely transfers.

None of this was abstract. Every question drew on the skills named in your role: incident management, asset and configuration management, change management, availability and capacity management, continuity management, problem management, ownership, service focus, community collaboration, and user focus. That is deliberate. Practising for an assessment and getting better at your actual job are, at this level, the same activity. The habits that raise your test score — careful reading, step-by-step arithmetic, evidence before conclusions, proportionate escalation — are exactly the habits that make a control centre run well.

If an assessment is coming up soon, revisit the preparation tips in each section, get a good night's sleep, and trust your practice. If you found some question types harder than others, that is useful information, not a verdict: return to those sections, redo the questions after a few days, and watch the techniques become automatic. Consider keeping a small learning log — one insight per practice session is plenty — and, if you can, talk through a few scenarios with your manager or a trusted colleague. Their perspective on the situational questions in particular will deepen your own.

Finally, remember why this role matters. Every alert you triage well, every record you keep accurate, every pattern you spot early protects real public services that real people depend on. The care you have shown by practising is the same care the work itself asks for. You are building a strong foundation for a career in IT operations — keep going, keep asking questions, and be proud of the progress you are making. Good luck!

