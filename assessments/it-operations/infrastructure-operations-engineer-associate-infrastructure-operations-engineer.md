# Associate Infrastructure Operations Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an associate infrastructure operations engineer working within the UK Government Digital and Data profession. You are at the start of an exciting career. As a trainee, you work in an established team, and you support infrastructure operations engineers in their daily work, under their direction. That means you are learning every day — and this guide is here to help you learn in one more useful way: by practising psychometric assessments.

First, let's take the mystery out of the words. A psychometric assessment is simply a structured set of questions that measures how you think and how you approach work situations. Employers use them because they are fair: everyone gets the same style of questions, and the scoring is the same for everyone. You may meet them when you apply for your next role, when your team runs a development exercise, or when you want to check your own progress. They are not designed to catch you out. They are designed to show what you can do.

The assessments in this guide are job-specific. That means the questions are not abstract puzzles about shapes or riddles. Instead, they use the real materials of your working day: monitoring dashboards, incident tickets, checklists, handover notes, alert emails, and simple reports about the infrastructure that keeps government services running. If you have ever logged an incident, checked a server's status, followed a checklist under the guidance of a more experienced engineer, or passed a tricky problem to your team, you already have the raw experience these assessments measure.

This document is organised into four main assessment sections:

1. A workplace job-specific cognitive assessment, which measures how you spot patterns, check for errors, reason logically, and decide what to do first.
2. A workplace job-specific numeric reasoning assessment, which measures how you work with the numbers you meet at work — ticket counts, percentages, uptime figures, and simple tables.
3. A workplace job-specific verbal reasoning assessment, which measures how carefully you read and understand written material such as procedures, emails, and policy extracts.
4. A workplace job-specific situational judgement assessment, which measures how you choose to act in realistic workplace situations, such as an alert going off while your supervisor is away.

Each section follows the same friendly pattern. First, an overview explains what the assessment measures and why it matters for your role. Next, a mapping shows how the assessment connects to the specific skills in your role: incident management, ownership, problem management, and user focus. Then comes the heart of each section: a full set of practice questions, starting easy and getting gradually harder, each with the correct answer and a step-by-step explanation. Finally, you get preparation tips and a list of common pitfalls to avoid.

Here is how to get the most from this guide. Take it slowly — there is no timer here. Try each question honestly and write down your answer before you read the explanation. Read every explanation, even when you get the question right, because the explanations teach technique, not just answers. And be kind to yourself: as a trainee, you are not expected to know everything. Every question you practise makes the real thing feel more familiar and less stressful.

Ready? Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the thinking skills your role uses every day, using workplace scenarios instead of abstract puzzles. For you, that means questions built around monitoring screens, incident tickets, checklists, server naming patterns, and the simple but important decisions a trainee makes: what to log, what to check, who to tell, and what to do first.

The typical format is an online, timed test lasting around 15 to 30 minutes, with somewhere between 15 and 30 questions. The questions usually cover pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Many modern platforms are adaptive, which means the questions get slightly harder when you answer correctly and slightly easier when you do not — so do not panic if the questions feel like they are getting tougher; that can be a good sign! Scoring is objective: your answers are compared with those of many other people, and employers often see a balance of speed and accuracy rather than a single number. Before the real test begins, you will normally be offered a few ungraded practice questions so you can get used to the screen layout without any pressure.

Why do employers use this kind of assessment for infrastructure operations roles? Because the job depends on careful, structured thinking. Production services — the systems that citizens and colleagues rely on — send out streams of information: alerts, logs, dashboards, and tickets. Someone in your role needs to notice when something breaks a pattern, follow a process step by step without skipping anything, spot the one wrong entry in a list, and know when a situation needs to be passed to a more experienced engineer. A cognitive assessment simulates exactly those demands in miniature. Practising it will also genuinely help you at work, because the habits it rewards — read carefully, check before you act, reason from the facts you have — are the same habits that make a great operations engineer.

One more reassurance before you begin: at your level, nobody expects deep technical knowledge in these tests. The questions give you all the information you need. Your job is simply to read carefully and think clearly.

### How this assessment maps to your role

The assessment dimensions connect directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Incident management** skill. When you identify and register incidents, gathering the required information and allocating it to the appropriate channel, you are recognising patterns: which alerts belong together, which ticket looks like the one from last week, and which category an incident fits.
- **Logical deduction** maps to your **Problem management** skill. When you investigate problems in systems, processes and services — and think about whether a problem is strategic, tactical or operational — you reason step by step from evidence to a sensible conclusion.
- **Error checking** maps to both **Incident management** and **Problem management**. Gathering the required information for an incident means noticing when a detail is missing or wrong. Contributing to the implementation of remedies and preventative measures means checking that a fix has actually been applied correctly.
- **Prioritisation** maps to your **Ownership and topic** skill. As a trainee, you show an awareness of problem resolution processes and you pass problems on to your team. Knowing what to escalate first, and what can wait, is prioritisation in action.
- **Applied problem solving** maps to your **User focus** skill. Showing an awareness of user experience analysis, and understanding the purpose of user stories and the focus on user needs, means always asking the practical question: what does this issue mean for the people using the service?

### Practice questions

**Question 1 (easy) — Pattern recognition in server names**

Your team names its servers using this pattern: a three-letter service code, a hyphen, the environment (PRD for production or TST for test), a hyphen, and a two-digit number. For example: WEB-PRD-01. During a morning check, you see this list on the monitoring dashboard:

1. WEB-PRD-01
2. WEB-PRD-02
3. WEB-TST-01
4. WEBPRD-03
5. APP-TST-02

Which entry breaks the naming pattern?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: C**

**Explanation:** Check each entry against the rule: three letters, hyphen, environment code, hyphen, two digits. Entries 1, 2, 3 and 5 all follow it exactly. Entry 4, "WEBPRD-03", is missing the first hyphen between the service code and the environment. This matters at work because monitoring tools and scripts often rely on exact naming: a server with a broken name may be missed by automated checks. Spotting small format errors like this is part of gathering accurate information when you register incidents — a skill you use every day, and one this assessment measures directly.

**Question 2 (easy) — Following a checklist in order**

Your daily morning checklist says: (1) log in to the monitoring dashboard; (2) check overnight alerts; (3) record any new alerts in the ticket system; (4) tell your supervising engineer about any alert marked "critical". This morning there are two new alerts: one marked "warning" and one marked "critical". You have logged in and looked at the alerts. According to the checklist, what should you do next?

- A) Tell your supervising engineer about the critical alert straight away, then record both alerts.
- B) Record both alerts in the ticket system, then tell your supervising engineer about the critical alert.
- C) Record only the critical alert, then tell your supervising engineer.
- D) Wait for your supervising engineer to arrive and ask what to do.

**Correct answer: B**

**Explanation:** The checklist gives the steps in a fixed order: step 3 (record any new alerts — that means both of them) comes before step 4 (tell your supervisor about critical alerts). Option B follows the checklist exactly. Option A swaps the order, and option C skips recording the warning alert, which breaks the instruction to record "any new alerts". Option D delays action that the checklist clearly tells you to take. In real life there are moments when common sense says act faster — and the situational judgement section explores those — but a cognitive test question like this one is testing whether you can follow written process precisely. As a trainee working under direction, performing routine tasks according to process is exactly what your team relies on you for.

**Question 3 (easy) — Spotting the odd one out in alerts**

Four alerts arrive within ten minutes:

1. "Disk space at 91% on WEB-PRD-01"
2. "Disk space at 93% on WEB-PRD-02"
3. "Disk space at 95% on WEB-PRD-03"
4. "Password expiry reminder for account svc-backup"

A senior engineer asks you which alerts look like they might be related to one another. What is the best answer?

- A) All four alerts are related.
- B) Alerts 1, 2 and 3 look related; alert 4 is different.
- C) Alerts 3 and 4 look related; alerts 1 and 2 are different.
- D) None of the alerts are related.

**Correct answer: B**

**Explanation:** Alerts 1, 2 and 3 share a clear pattern: the same type of problem (disk space filling up), on three servers with the same naming stem (WEB-PRD), at similar levels (91-95%), at almost the same time. That pattern suggests a common cause — perhaps a log file growing on all three web servers. Alert 4 is a routine account notice with no connection to disk space. Grouping related alerts is a core part of identifying and registering incidents and allocating them to the appropriate channel: three related disk alerts might become one incident ticket rather than three, which helps the engineer who investigates. Noticing what belongs together — and what does not — is pattern recognition doing real work.

**Question 4 (easy) — Simple deduction from a rule**

Your team's rule says: "If a server alert is marked critical, it must be escalated to the on-call engineer within 15 minutes." You know that an alert on APP-PRD-02 was escalated to the on-call engineer. Which one of the following conclusions must be true?

- A) The alert on APP-PRD-02 was marked critical.
- B) The alert on APP-PRD-02 was escalated within 15 minutes.
- C) The rule was followed correctly.
- D) None of the above must be true.

**Correct answer: D**

**Explanation:** This question rewards careful logic. The rule says critical alerts must be escalated — but it does not say only critical alerts get escalated. An engineer might escalate a warning alert too, just to be safe. So option A is not guaranteed. We also are not told when the escalation happened, so option B is not guaranteed either. And because we cannot confirm A or B, we cannot confirm C. The safe conclusion is D. The lesson: deduce only what the given facts guarantee, and do not add assumptions. This careful habit matters when you contribute to problem investigations — writing "the alert was escalated" in a ticket is a fact; writing "the alert was critical" when you have not checked would be a guess dressed up as a fact.

**Question 5 (moderate) — Error checking a ticket record**

You are asked to check a new incident ticket before it is passed to the second-line team. Your team's standard says every incident ticket must include: the affected server name, the time the alert was received, the alert severity, and the name of the person who logged it. The ticket reads:

"Incident 4821. Alert received 09:42. Severity: warning. Logged by: A. Begum. Description: repeated login failures reported by service desk."

What is wrong with this ticket?

- A) The severity is missing.
- B) The affected server name is missing.
- C) The time is in the wrong format.
- D) Nothing is wrong; the ticket is complete.

**Correct answer: B**

**Explanation:** Work through the standard like a checklist and tick off each required item: time received — present (09:42); severity — present (warning); logged by — present (A. Begum); affected server name — not present anywhere in the ticket. The description mentions login failures but never says which server or system is affected. Option B is correct. This is exactly the kind of quality check that makes you valuable when you identify and register incidents: a ticket without the affected server name forces the next engineer to waste time asking questions before they can even start. In an assessment, the technique is to compare the record against the required list item by item, rather than reading the ticket and judging whether it "feels" complete.

**Question 6 (moderate) — Deduction about a sequence of events**

A senior engineer shows you three facts from last night's logs: (i) the backup job on FIL-PRD-01 always runs after the antivirus scan finishes; (ii) the antivirus scan finished at 02:30; (iii) the backup job failed. A teammate says: "So the backup job failed some time after 02:30." Is your teammate's conclusion sound?

- A) Yes — the backup runs after the scan, the scan finished at 02:30, so the failure happened after 02:30.
- B) No — the backup job might have failed before 02:30.
- C) No — the antivirus scan might have caused the failure.
- D) Yes — because backup jobs always run in the early morning.

**Correct answer: A**

**Explanation:** Put the facts in order. The backup job always runs after the antivirus scan finishes (fact i). The scan finished at 02:30 (fact ii). So the backup job cannot have started, let alone failed, before 02:30. The failure (fact iii) must therefore have happened after 02:30. Option A states exactly this chain. Option B contradicts fact (i). Option C might be an interesting theory about the cause, but the question asks only whether the timing conclusion is sound — and adding a cause is going beyond the facts. Option D reaches the right answer for a wrong, made-up reason. Reasoning about the order of events is a daily part of investigating problems in systems: logs tell a story, and your job is to read that story in the right sequence.

**Question 7 (moderate) — Prioritising alerts as a trainee**

You are alone at your desk for twenty minutes while your supervising engineer is in a meeting (reachable by message for emergencies). Four things happen at once:

1. A critical alert: the production payments service is not responding.
2. A warning alert: disk space at 82% on a test server.
3. A colleague asks you to help move a monitor to another desk.
4. A routine reminder: your weekly timesheet is due by the end of the day.

What should you do first?

- A) Help your colleague — it only takes a minute.
- B) Message your supervising engineer about the critical payments alert, following the escalation process.
- C) Investigate and fix the payments service yourself to save time.
- D) Clear the disk space warning on the test server first because it is the easiest.

**Correct answer: B**

**Explanation:** Rank the items by impact and urgency. A production payments service not responding affects real users right now — it is both urgent and high impact, so it comes first. As an associate, the right action is not to attempt a solo fix on a critical production service (option C); it is to follow the escalation process and alert your supervising engineer immediately, which is exactly why they are reachable for emergencies. This reflects your Ownership and topic skill at your level: show awareness of the resolution process and pass problems to your team promptly. The test server warning (option D) is low impact and can wait; the monitor and the timesheet are routine. Notice the pattern for prioritisation questions: production before test, users before convenience, escalation before heroics.

**Question 8 (moderate) — Pattern recognition across time**

You keep a simple tally of one recurring alert. Over the past five Mondays, the alert "memory usage high on APP-PRD-01" fired at these times: 09:05, 09:02, 09:08, 09:04, and 09:06. Today is Monday and the alert fires at 09:05. A colleague suggests possible next steps. Which suggestion makes the best use of the pattern you have spotted?

- A) Ignore the alert — it happens every Monday, so it must be normal.
- B) Record the pattern in the problem ticket: the alert fires every Monday just after 09:00, which suggests a scheduled weekly task may be the cause, and pass this to your team.
- C) Restart APP-PRD-01 every Monday at 08:55 to prevent the alert.
- D) Delete the alert rule so it stops firing.

**Correct answer: B**

**Explanation:** The times cluster tightly: every Monday, within a few minutes of 09:00. That regularity is a strong clue that something scheduled — a weekly report, a batch job, a sync task — drives the memory spike. The best trainee action is option B: record the evidence clearly and pass it to your team, which matches your Problem management skill (investigate problems and contribute to remedies) and your Ownership skill (pass problems on to your team). Option A confuses "recurring" with "harmless" — recurring problems deserve investigation precisely because they keep coming back. Options C and D treat the symptom or hide it: restarting a production server weekly without diagnosis could cause outages, and deleting the alert removes your early warning without fixing anything. In assessments and at work alike, a spotted pattern is evidence to report, not a licence to improvise.

**Question 9 (moderate) — Error checking against two sources**

Your team's asset list says the server BCK-PRD-01 is located in Rack 4 and runs "Backup Agent version 7.2". During a supervised check of Rack 4, you find BCK-PRD-01 present, but its screen shows "Backup Agent version 7.1". Your supervising engineer asks you to summarise what you found. Which summary is accurate?

- A) "Everything matches the asset list."
- B) "The server is missing from Rack 4."
- C) "The server's location matches the asset list, but the software version does not: the list says 7.2 and the server shows 7.1."
- D) "The asset list is wrong and needs to be corrected to say 7.1."

**Correct answer: C**

**Explanation:** Compare the two sources field by field. Location: list says Rack 4; you found it in Rack 4 — match. Version: list says 7.2; server shows 7.1 — mismatch. Option C reports both findings precisely, which is what an accurate summary looks like. Option A ignores the mismatch and option B is simply false. Option D is tempting but goes one step too far: you have found a discrepancy, but you do not yet know which source is wrong. Perhaps the list is out of date — or perhaps the server missed an upgrade it should have received, which would be the more worrying possibility. The right move is to report the discrepancy and let the team decide. Careful, neutral reporting of differences between records and reality is the foundation of good configuration information, and assessments reward answers that state exactly what was observed, no more and no less.

**Question 10 (hard) — Multi-step deduction about a failed change**

Last night, three changes were made to the web platform, one after another: Change 1 updated the firewall rules at 22:00; Change 2 patched the web servers at 23:00; Change 3 updated the load balancer at 23:45. This morning, users report they cannot reach the website. You learn three facts: (i) a test at 23:30 confirmed the website was working normally; (ii) no other changes happened after 23:45; (iii) the website was first reported broken at 00:10. Which change is the most likely cause of the outage?

- A) Change 1, the firewall update, because firewalls block traffic.
- B) Change 2, the web server patch, because patches often cause problems.
- C) Change 3, the load balancer update, because the site worked at 23:30 and only changed after 23:45.
- D) It is impossible to say anything useful from these facts.

**Correct answer: C**

**Explanation:** Build a timeline and place each fact on it. Changes 1 and 2 were both complete before the 23:30 test, and the test showed the site working normally — so whatever those changes did, the site survived them. Between 23:30 and 00:10, exactly one thing changed: the load balancer update at 23:45 (fact ii rules out anything else). The site was then found broken at 00:10. The most likely cause is therefore Change 3. Options A and B rely on general prejudice ("firewalls block traffic", "patches cause problems") instead of the actual timeline — a classic trap. Option D is too pessimistic: the facts do support a useful, testable conclusion, even though a careful engineer would still verify it rather than treat it as proven. This is timeline reasoning, the single most useful deduction technique in incident investigation: establish the last known good time, list what changed after it, and suspect those changes first.

**Question 11 (hard) — Prioritisation with dependencies**

Your supervising engineer gives you four tasks for the afternoon and one constraint. Tasks: (1) update the asset list with three new laptops, which takes 30 minutes; (2) run the monthly test-restore of a backup, which takes 60 minutes and must be started before 15:00 because the backup system locks at 16:00; (3) write up this morning's incident notes while your memory is fresh, 30 minutes; (4) collect a delivery of cables from the post room, which closes at 17:00, 15 minutes. It is now 14:00 and you finish at 17:00. The constraint: the test-restore, once started, must not be interrupted. What is the best order?

- A) 1, 2, 3, 4
- B) 2, 3, 1, 4
- C) 3, 2, 1, 4
- D) 4, 1, 3, 2

**Correct answer: B**

**Explanation:** Start with the hardest deadline: the test-restore must start before 15:00 and runs uninterrupted for 60 minutes. Starting it at 14:00 (option B) satisfies the deadline with the largest safety margin — if anything goes wrong, you still have until 15:00 to restart it. It finishes at 15:00, leaving two hours for the three short tasks (30 + 30 + 15 = 75 minutes), all of which comfortably fit before their deadlines. Within those, doing the incident notes next respects the "while your memory is fresh" advice, then the asset list, then the post room before 17:00. Option C also technically works, but it starts the critical task at 14:30, halving your safety margin for no benefit. Option D is worst: starting the restore at 15:15 breaks the "start before 15:00" rule outright. Option A delays the deadline task behind a task with no deadline pressure. The technique: identify the task with the tightest, least movable constraint, schedule it first with maximum margin, then fit flexible tasks around it.

**Question 12 (hard) — Applied problem solving with user focus**

The service desk reports that some users of an internal HR application see a "page not found" error. You gather these facts under your engineer's direction: (i) users on the Leeds office network all see the error; (ii) users on the Manchester office network can all use the application normally; (iii) the application runs on a single server, which the monitoring dashboard shows as healthy; (iv) no changes were made to the application this week. Which is the most reasonable working theory to suggest to your team?

- A) The application server is down.
- B) Something on the network path between the Leeds office and the application is the likely cause, because the problem affects one location while the server itself looks healthy.
- C) The users in Leeds are making mistakes typing the address.
- D) The application code has a bug affecting all users.

**Correct answer: B**

**Explanation:** Use elimination, fact by fact. Fact (iii) says the server is healthy, and fact (ii) proves it: Manchester users reach it normally — so option A falls, and so does option D, because a code bug would not choose victims by office. Option C is implausible at scale: one user mistyping is believable, but every Leeds user mistyping at once is not, and it would be a poor, user-blaming theory to offer. That leaves the one factor that separates the affected from the unaffected users: their location, and therefore their network path. Option B names it, with the reasoning attached. Notice how this connects to your User focus skill: the investigation started from user reports, and the theory is built by asking which users are affected and what they share. Describing an issue in terms of who is affected and how — rather than jumping to a component — is both good assessment technique and good operations practice.

### Preparation tips

- **Practise with your real work.** The best preparation for a job-specific cognitive test is the job itself. When you check a dashboard, name the pattern you see. When you log a ticket, check it against the required fields like a mini error-checking question. These small habits are free practice.
- **Read the question twice before answering.** Many wrong answers come from misreading, not from weak thinking. In the practice questions above, notice how often one word — "any", "only", "after", "must" — decides the answer.
- **Learn the timeline technique.** For any question about events, sketch the order things happened: last known good, what changed, when the problem appeared. It turns confusing stories into simple pictures.
- **Answer from the facts given, not from memories of similar situations.** Assessments deliberately include tempting options based on general assumptions ("patches cause problems"). Discipline yourself to use only what the question states.
- **Time yourself gently.** Once you feel comfortable, redo a few questions with a clock running — around 60 to 90 seconds each is typical. Speed comes from familiarity, so build familiarity first and speed second.
- **Look after the basics.** Sleep well before a real assessment, set up a quiet space, check your internet connection, and use the ungraded practice questions the platform offers. Calm conditions are worth several extra marks.

### Common pitfalls to avoid

- **Jumping to the technical answer.** Trainees sometimes pick the option that sounds most technical, assuming it must be right. Assessments reward reasoning, not jargon. The correct option is the one the facts support.
- **Skipping steps in ordered processes.** When a question describes a checklist or procedure, the order is usually the point. Do not reorder steps because a different order "feels faster".
- **Confusing "possible" with "must be true".** In deduction questions, an option can be perfectly plausible and still wrong, because the facts do not guarantee it. Ask: could there be a situation where the facts hold but this option is false? If yes, it is not a "must".
- **Fixing instead of reporting.** Several questions — and much of your real job at this level — turn on knowing when to escalate. Options where a trainee quietly fixes a production issue alone are almost always traps.
- **Rushing the easy questions.** Early questions are where careless errors happen, because they look simple. Bank those marks by reading just as carefully at the start as at the end.
- **Letting one hard question shake you.** If a question stumps you, choose your best answer, let it go, and reset for the next one. Assessments measure your overall performance, not any single question.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how confidently and accurately you work with the numbers that appear in your job. This is not a maths exam full of algebra. It is about everyday workplace arithmetic: percentages, averages, simple ratios, rates, and reading small tables and charts — the kind of numbers that fill monitoring dashboards, ticket reports, and capacity summaries.

The typical format is an online, timed test of about 20 to 30 minutes, with 15 to 25 questions. Each question presents some data — a table of ticket counts, a disk usage figure, an uptime percentage — and asks you to calculate or interpret something from it. A basic on-screen calculator is usually allowed, and rough paper is your friend. As with the cognitive test, scoring compares your accuracy and speed against other people, and some platforms adapt the difficulty as you go. You will normally get a couple of unscored practice questions first to settle your nerves.

Why does this matter for an associate infrastructure operations engineer? Because infrastructure runs on numbers. Disk space is a percentage. Uptime is a percentage. Ticket queues are counts and averages. Backup windows are durations. When your supervising engineer says "that disk will be full in about a week", they got there by simple arithmetic on a growth rate — and one day soon, you will do the same. Even at trainee level, you will read dashboards where the difference between 89% and 98% disk usage is the difference between "note it" and "escalate it now". Employers test numeric reasoning because they need people who can look at a number, understand what it means for the service, and not be fooled by a misleading average or a percentage taken out of context.

Here is the encouraging part: the maths itself is genuinely simple — adding, subtracting, multiplying, dividing, and percentages. Every question in this section shows its arithmetic step by step in the explanation, so even if numbers are not your favourite thing, you can follow each one and build confidence. Work through them slowly the first time. Accuracy first, speed later.

### How this assessment maps to your role

- **Percentages and thresholds** map to your **Incident management** skill. Alerts fire at percentage thresholds — disk at 90%, memory at 85%. Registering an incident correctly means understanding what those figures mean and how close to the limit a system really is.
- **Counts, averages and rates** map to your **Problem management** skill. Investigating problems means noticing that a certain error happens, say, 12 times a day on average, or that a queue is growing at 20 tickets an hour — patterns and trends are numbers over time.
- **Reading tables and simple charts** maps to your **Ownership and topic** skill. When you pass a problem to your team, you often pass a small table of evidence with it. Reading such tables accurately — and summarising them honestly — makes your handovers trustworthy.
- **Practical estimation** maps to your **User focus** skill. Numbers become meaningful when you translate them into user impact: "the service was down for 30 minutes during lunch, when usage peaks" says far more about user needs than the raw duration alone.

### Practice questions

**Question 1 (easy) — Disk space percentage**

A server has a 500 GB disk. The monitoring dashboard shows that 350 GB is used. What percentage of the disk is used?

- A) 60%
- B) 65%
- C) 70%
- D) 75%

**Correct answer: C**

**Explanation:** Percentage used = (used ÷ total) × 100. Step 1: 350 ÷ 500 = 0.7. Step 2: 0.7 × 100 = 70%. So the disk is 70% used. A quick sense-check: half of 500 is 250, so 350 must be more than 50%; and 75% of 500 would be 375, so 350 must be a little less than 75%. The answer 70% fits neatly between those two anchors. Sense-checking against easy landmarks (50%, 75%) is a habit worth building — it catches calculator slips in seconds, and it is exactly how experienced engineers glance at a dashboard and know instantly whether a number looks right.

**Question 2 (easy) — Counting tickets across a week**

Your team logged the following numbers of incident tickets: Monday 14, Tuesday 9, Wednesday 11, Thursday 16, Friday 10. How many tickets were logged in total that week?

- A) 58
- B) 60
- C) 62
- D) 64

**Correct answer: B**

**Explanation:** Add the daily counts step by step: 14 + 9 = 23. Then 23 + 11 = 34. Then 34 + 16 = 50. Then 50 + 10 = 60. The total is 60 tickets. In a timed test, add in a fixed order and keep a running total on paper rather than trying to hold it all in your head — transcription slips are the most common cause of wrong answers on simple addition. Totals like this appear constantly in operations reporting, and they feed the averages and trends you will meet in the harder questions below.

**Question 3 (easy) — Average tickets per day**

Using the same week of data (Monday 14, Tuesday 9, Wednesday 11, Thursday 16, Friday 10 — a total of 60), what was the average (mean) number of tickets per day?

- A) 10
- B) 11
- C) 12
- D) 13

**Correct answer: C**

**Explanation:** Mean = total ÷ number of days. Step 1: the total is 60 (from Question 2). Step 2: there are 5 working days. Step 3: 60 ÷ 5 = 12. The average is 12 tickets per day. Notice something useful about averages: no single day actually had 12 tickets — the mean is a summary, not a description of any one day. Thursday (16) was well above average and Tuesday (9) well below. When your team says "we get about 12 tickets a day", that is what they mean: a level around which real days vary. Understanding this stops you panicking on a 16-ticket day and stops you relaxing too much on a 9-ticket day.

**Question 4 (easy) — Percentage of alerts that were critical**

Last month your team received 240 alerts. Of these, 36 were marked critical. What percentage of alerts were critical?

- A) 12%
- B) 15%
- C) 18%
- D) 20%

**Correct answer: B**

**Explanation:** Percentage = (part ÷ whole) × 100. Step 1: 36 ÷ 240 = 0.15. Step 2: 0.15 × 100 = 15%. So 15% of alerts were critical. If you prefer to avoid the division, simplify the fraction first: 36/240 divides top and bottom by 12 to give 3/20, and 3/20 as a percentage is 15% (because 1/20 = 5%). Fluency with a few friendly fractions — 1/4 = 25%, 1/5 = 20%, 1/20 = 5% — lets you answer questions like this in seconds and saves your time for the harder ones later in a real test.

**Question 5 (moderate) — Uptime percentage and downtime minutes**

A production service has an availability target of 99.5% for a 30-day month. A 30-day month contains 43,200 minutes. What is the maximum downtime, in minutes, the service can have while still meeting the target?

- A) 43.2 minutes
- B) 216 minutes
- C) 432 minutes
- D) 2,160 minutes

**Correct answer: B**

**Explanation:** If the service must be up 99.5% of the time, it may be down at most 100% − 99.5% = 0.5% of the time. Step 1: convert 0.5% to a decimal: 0.5 ÷ 100 = 0.005. Step 2: multiply by the total minutes: 43,200 × 0.005 = 216. So the service can be down for at most 216 minutes — about 3.6 hours — in the month. Option A is the trap for misplacing the decimal (0.1% instead of 0.5% would give 43.2), and option C comes from using 1% instead of 0.5%. Uptime targets, often called SLAs, are everyday language in operations teams; being able to translate "99.5%" into "about three and a half hours a month" turns an abstract target into something you can genuinely picture.

**Question 6 (moderate) — Reading a table of disk usage**

The morning report shows disk usage on four production servers:

| Server | Disk size | Used | Alert threshold |
|---|---|---|---|
| WEB-PRD-01 | 200 GB | 150 GB | 90% |
| WEB-PRD-02 | 200 GB | 184 GB | 90% |
| APP-PRD-01 | 400 GB | 350 GB | 90% |
| FIL-PRD-01 | 1,000 GB | 870 GB | 90% |

Which server has crossed its alert threshold?

- A) WEB-PRD-01
- B) WEB-PRD-02
- C) APP-PRD-01
- D) FIL-PRD-01

**Correct answer: B**

**Explanation:** Work out each server's usage percentage, then compare with 90%. WEB-PRD-01: 150 ÷ 200 = 0.75 = 75%. WEB-PRD-02: 184 ÷ 200 = 0.92 = 92%. APP-PRD-01: 350 ÷ 400 = 0.875 = 87.5%. FIL-PRD-01: 870 ÷ 1,000 = 0.87 = 87%. Only WEB-PRD-02, at 92%, has crossed the 90% threshold. The trap in this question is judging by raw gigabytes: FIL-PRD-01 has by far the most data used (870 GB), but it also has the biggest disk, so its percentage is fine. Thresholds are set as percentages precisely so that servers of different sizes can be compared fairly — always convert to the same units (here, percent) before comparing.

**Question 7 (moderate) — Growth rate and time to full**

A log folder on a server currently holds 60 GB, on a disk partition of 100 GB used only for logs. The folder grows by about 5 GB per week and nothing is deleted. At this rate, in how many weeks will the partition be full?

- A) 5 weeks
- B) 8 weeks
- C) 12 weeks
- D) 20 weeks

**Correct answer: B**

**Explanation:** Step 1: work out the remaining space: 100 − 60 = 40 GB free. Step 2: divide the free space by the growth per week: 40 ÷ 5 = 8. At the current rate the partition will be full in 8 weeks. Option C (12) is the trap for dividing the used space (60) by the rate instead of the free space, and option D (20) comes from dividing the whole disk (100) by the rate. The formula to remember is: time to full = remaining space ÷ growth rate. This simple projection is one of the most genuinely useful calculations in operations — it turns "the disk is filling up" into "we have about eight weeks to act", which is exactly the kind of evidence your team wants in a problem ticket.

**Question 8 (moderate) — Percentage change in incident volume**

In March your team logged 80 incidents. In April it logged 100 incidents. What was the percentage increase from March to April?

- A) 20%
- B) 25%
- C) 30%
- D) 80%

**Correct answer: B**

**Explanation:** Percentage change = (change ÷ original) × 100. Step 1: the change is 100 − 80 = 20 incidents. Step 2: divide by the original (March) figure: 20 ÷ 80 = 0.25. Step 3: 0.25 × 100 = 25%. The increase is 25%. The classic trap is option A: dividing the change by the new figure (20 ÷ 100 = 20%) instead of the original. Always divide by the starting value — "increase from March" means March is the baseline. One extra insight worth carrying to work: if incidents later fell from 100 back to 80, that would be a 20% decrease (20 ÷ 100), not 25% — percentage changes are not symmetrical, which surprises many people and occasionally causes arguments over dashboards.

**Question 9 (moderate) — Backup success rate**

Over 30 nights, the backup job succeeded 27 times and failed 3 times. Your team's standard requires a success rate of at least 95%. Did the backup meet the standard, and what was its success rate?

- A) Yes — the success rate was 97%.
- B) Yes — the success rate was 95%.
- C) No — the success rate was 90%.
- D) No — the success rate was 93%.

**Correct answer: C**

**Explanation:** Success rate = (successes ÷ attempts) × 100. Step 1: 27 ÷ 30 = 0.9. Step 2: 0.9 × 100 = 90%. The standard requires at least 95%, and 90% is below it, so the backup did not meet the standard. A quick alternative route: 3 failures out of 30 is 3/30 = 1/10 = 10% failure, so success = 100% − 10% = 90%. Sometimes calculating the small side (failures) and subtracting from 100% is faster and less error-prone than calculating the large side. Three failed backups in a month is also a pattern worth flagging in its own right — numbers like these are exactly what "investigating patterns and trends" looks like in practice, and reporting them accurately is a contribution a trainee can make from day one.

**Question 10 (hard) — Ratios of ticket allocation**

Your service desk allocates infrastructure tickets to three queues — Network, Servers, and Storage — in the ratio 2 : 3 : 1. Last week 120 infrastructure tickets arrived in total. How many went to the Servers queue?

- A) 20
- B) 40
- C) 60
- D) 72

**Correct answer: C**

**Explanation:** A ratio of 2 : 3 : 1 means the tickets are split into 2 + 3 + 1 = 6 equal parts. Step 1: find the size of one part: 120 ÷ 6 = 20 tickets per part. Step 2: the Servers queue gets 3 parts: 3 × 20 = 60 tickets. As a check, the other queues get Network 2 × 20 = 40 and Storage 1 × 20 = 20, and 60 + 40 + 20 = 120, which matches the total — always verify a ratio answer by adding the shares back together. Option B is the Network queue's share, a trap for picking the wrong ratio position. Ratio splits appear in real operations work whenever workload, cost, or capacity is shared across teams or systems, and the "total the parts, size one part, multiply" method works every time.

**Question 11 (hard) — Combining averages with a target**

The service desk answers calls with a target average answer time of 60 seconds or less each day. So far today, 40 calls have been answered with an average answer time of 66 seconds. There are expected to be 20 more calls today. What average answer time do those 20 calls need, so that the whole day's average meets the 60-second target exactly?

- A) 42 seconds
- B) 48 seconds
- C) 54 seconds
- D) 57 seconds

**Correct answer: B**

**Explanation:** Work in total seconds, because averages combine through totals. Step 1: the day's target total for 60 calls at an average of 60 seconds is 60 × 60 = 3,600 seconds. Step 2: the first 40 calls have already used 40 × 66 = 2,640 seconds. Step 3: the remaining 20 calls may use at most 3,600 − 2,640 = 960 seconds. Step 4: 960 ÷ 20 = 48 seconds average. So the remaining calls need to average 48 seconds. The insight: because the morning ran 6 seconds over target across 40 calls (a debt of 40 × 6 = 240 seconds), the afternoon's 20 calls must each run 240 ÷ 20 = 12 seconds under target — 60 − 12 = 48, the same answer by a quicker route. Averages cannot be "averaged" directly (66 and 54 do not simply balance); converting to totals is the reliable method, in tests and in real service reporting alike.

**Question 12 (hard) — Interpreting a trend table with care**

A monthly report shows the number of failed login incidents and the total number of logins for an internal service:

| Month | Failed login incidents | Total logins |
|---|---|---|
| May | 30 | 10,000 |
| June | 45 | 18,000 |
| July | 60 | 30,000 |

A colleague says: "Failed login incidents have doubled from May to July — the service is getting worse." Based on the failure rate per login, what is the fairer conclusion?

- A) The colleague is right: the service is getting worse.
- B) The failure rate has actually fallen from 0.3% in May to 0.2% in July, so relative to usage the service is getting better, even though raw incident numbers rose.
- C) The failure rate is unchanged across the three months.
- D) The table cannot tell us anything about failure rates.

**Correct answer: B**

**Explanation:** Calculate the rate for each month: rate = incidents ÷ total logins × 100. May: 30 ÷ 10,000 = 0.003 = 0.3%. June: 45 ÷ 18,000 = 0.0025 = 0.25%. July: 60 ÷ 30,000 = 0.002 = 0.2%. The raw count did double (30 to 60), but total logins tripled (10,000 to 30,000), so the failure rate per login fell steadily from 0.3% to 0.2%. Option B captures this. The lesson is one of the most important in all numeric reasoning: raw counts mislead when the underlying volume changes. A growing service will naturally produce more incidents even as it becomes more reliable per use. When you contribute evidence to a problem investigation, quoting the rate alongside the count keeps the picture honest — and in a test, whenever a question gives you both a count and a volume, the examiner almost always wants you to compute the rate.

### Preparation tips

- **Refresh the four core tools.** Nearly every question uses one of: percentage = part ÷ whole × 100; percentage change = change ÷ original × 100; mean = total ÷ count; and ratio shares = total ÷ sum of parts. Write these on a card and practise until they feel automatic.
- **Always write down the steps.** Even with a calculator, jot each intermediate number. Most errors are lost digits and skipped steps, not wrong methods.
- **Sense-check against landmarks.** Before accepting an answer, compare it with an easy nearby value: is it more or less than half? More or less than 10%? A two-second check catches most slips.
- **Use your own dashboards as practice.** Next time you see a disk usage figure or a ticket count at work, quietly compute something from it — the percentage free, the weekly average, the time to full. Real data makes the methods stick.
- **Practise reading tables before calculating.** Half the challenge is picking the right numbers out of the table. Underline exactly which row and column the question asks about before touching the calculator.
- **Keep calm about the calculator.** Learn the on-screen calculator during the unscored practice questions. If it feels awkward, rough paper plus simple mental steps is often faster for the easy questions.

### Common pitfalls to avoid

- **Dividing by the wrong baseline.** Percentage change questions almost always tempt you with the answer you get from dividing by the new value instead of the original. "Increase from X" means X is the denominator.
- **Comparing raw numbers when sizes differ.** A big disk with lots of data used may be healthier than a small disk with less. Convert to percentages or rates before comparing anything of different sizes.
- **Averaging averages.** You cannot combine two averages by averaging them unless the groups are the same size. Convert to totals, combine, then divide.
- **Misreading the units.** Minutes versus hours, GB versus TB, per day versus per week. Circle the units in the question and make sure your answer uses the ones asked for.
- **Forgetting what the number is for.** In role-specific tests, the final step is often interpretive: does 92% cross a 90% threshold? Does 90% meet a 95% standard? Do the arithmetic, then answer the actual question asked.
- **Spending too long on one calculation.** If a question is consuming minutes, make your best estimate, select it, and move on. Ten answered questions beat three perfect ones.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and draw conclusions from written material — using the kinds of documents your role actually produces and consumes. For you, that means procedure documents, incident notifications, policy extracts, emails from the service desk, handover notes, and short reports.

The typical format is an online, timed test lasting 15 to 25 minutes. You are shown a short passage and then asked questions about it. The most common question type is "true / false / cannot say": you decide whether a statement is definitely true based on the passage, definitely false based on the passage, or whether the passage simply does not give enough information to decide. Other questions ask you to pick the best summary of a passage, identify what a word or instruction means in context, or choose the clearest way to phrase a message. Scoring rewards accuracy under time pressure, and — importantly — it rewards answering from the passage alone, not from your own background knowledge.

Why does verbal reasoning matter for an associate infrastructure operations engineer? Because your work runs on precise reading. A patching procedure that says "restart the service after the update" is different from one that says "restart the server after the update" — one word changes the action completely. Incident tickets, change notices, and security bulletins are written documents, and misreading them causes real outages. Equally, your own writing matters: when you register an incident or hand over a problem to your team, the next person acts on what you wrote. Employers test verbal reasoning because they need people who read instructions faithfully, who notice the difference between what a document says and what they assume it means, and who can pass on information without distorting it.

The golden rule for this whole section — worth learning before you attempt a single question — is this: answer only from the passage. In real life, you bring experience to everything you read. In a verbal reasoning test, the passage is the entire universe. If the passage does not say it, and it does not follow necessarily from what the passage says, then the answer is "cannot say" — even if you happen to know it is true in the real world.

### How this assessment maps to your role

- **Reading comprehension of procedures** maps to your **Incident management** skill. Identifying and registering incidents means following written processes exactly: gathering the required information listed in the procedure and allocating the incident to the channel the procedure names.
- **True/false/cannot-say discipline** maps to your **Problem management** skill. Investigating problems requires separating what the evidence states from what you are tempted to assume — the same discipline the test rewards. Writing "the server restarted at 03:00" only when a log actually says so is problem management in miniature.
- **Inference from written reports** maps to your **Ownership and topic** skill. When you pass a problem to your team, you must first understand the written material well enough to summarise it honestly, without adding or losing meaning.
- **Clear-writing judgement** maps to your **User focus** skill. Understanding user stories — short written statements of what a user needs and why — depends on reading them carefully, and communicating with users or the service desk depends on writing plainly, without jargon that hides the message.

### Practice questions

**Question 1 (easy) — Understanding a procedure step**

Read this extract from your team's patching procedure:

"All test servers must be patched on the first Tuesday of each month. Production servers must be patched no earlier than seven days after the test servers, and only if no problems have been reported on the test servers during those seven days."

Statement: "Production servers are patched exactly seven days after test servers."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Read the wording precisely. The procedure says production servers are patched "no earlier than seven days after" the test servers. That sets a minimum wait of seven days — it does not fix the gap at exactly seven days. Production patching could happen after eight days, ten days, or later, and would still follow the procedure. The statement claims the gap is "exactly seven days", which contradicts what the passage allows, so the statement is false. Words like "no earlier than", "at least", "up to", and "within" carry precise meanings in procedures, and one of the most valuable habits this test builds is treating those small phrases as the load-bearing parts of a sentence — because in operational documents, they are.

**Question 2 (easy) — What the passage does not say**

Read this notification email:

"Planned maintenance: the file storage service will be unavailable on Saturday from 08:00 to 12:00 while the storage team replaces a network switch. Users should save their work before Friday evening. Email and calendar services are not affected."

Statement: "The maintenance is taking place because the network switch is faulty."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The email says the switch is being replaced, but it never gives the reason. Perhaps the switch is faulty — that is one plausible reason — but switches are also replaced as routine upgrades, for capacity, or because support contracts expire. The passage neither confirms nor denies a fault, so the correct answer is "cannot say". This is the single most important verbal reasoning skill: resisting a plausible assumption. Notice that the statement is not false — the passage does not contradict it — it is simply unsupported. At work, the same discipline keeps your incident notes trustworthy: "switch replaced" is what you know; "switch was faulty" is a guess unless someone tells you so.

**Question 3 (easy) — Identifying the required action**

Read this extract from the incident logging guide:

"When the service desk transfers a call about a possible infrastructure fault, first record the caller's name, team, and contact number. Next, record which service is affected and what the caller was doing when the problem occurred. Do not attempt to diagnose the fault during the call. Finally, tell the caller their incident reference number before ending the call."

According to the passage, which of the following should you do during the call?

- A) Diagnose the fault while the caller waits.
- B) Record the caller's details and what they were doing, and give them the incident reference number.
- C) Transfer the caller back to the service desk.
- D) Ask the caller to email the details instead.

**Correct answer: B**

**Explanation:** Match each option against the passage. The passage instructs you to record the caller's name, team and contact number, record the affected service and the caller's activity, and give the incident reference before ending the call — all captured by option B. Option A is explicitly forbidden ("Do not attempt to diagnose the fault during the call"). Options C and D describe actions the passage never mentions. This question type — "what does the procedure actually tell you to do?" — rewards systematic matching rather than memory: run your eye down the passage and tick each part of the answer option against a sentence in the text. It is the same care you use when gathering the required information to register a real incident.

**Question 4 (easy) — Meaning in context**

Read this line from a handover note:

"APP-PRD-02 was rebooted at 14:30; the memory alert has cleared, but keep an eye on it — if it recurs, raise a problem ticket rather than another incident."

In this note, "if it recurs" means:

- A) If the server is rebooted again.
- B) If the memory alert happens again.
- C) If the handover note is updated.
- D) If a problem ticket already exists.

**Correct answer: B**

**Explanation:** "Recur" means to happen again, and the "it" points back to the most recent relevant subject — the memory alert, which has cleared but is being watched. So "if it recurs" means "if the memory alert happens again". Reading pronouns carefully ("it", "this", "they") is a small skill with big consequences in operational writing, where a wrongly resolved "it" can send someone to reboot the wrong thing. The note also carries a genuinely useful operational idea: a fault that keeps returning stops being a series of separate incidents and becomes a problem to investigate — which is exactly the distinction your Problem management skill describes, and why the note says to raise a problem ticket for a repeat.

**Question 5 (moderate) — True/false/cannot-say on a policy extract**

Read this extract from a security policy:

"Administrator passwords must be changed every 90 days. Service accounts are exempt from scheduled password changes, but their passwords must be changed immediately if a team member with knowledge of them leaves the organisation. All password changes must be recorded in the credential management system."

Statement: "If a team member who knows a service account password leaves, that password must be changed and the change must be recorded."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Combine two sentences from the passage. First: service account passwords "must be changed immediately if a team member with knowledge of them leaves the organisation" — that covers the change. Second: "All password changes must be recorded in the credential management system" — "all" includes this change, so the recording is covered too. Both parts of the statement follow necessarily from the passage, so it is true. This question shows that "true" does not always mean "stated in a single sentence": sometimes you must connect two stated rules. That is still safe deduction, because each link is explicit in the text. Contrast this with assuming an unstated reason (as in Question 2) — connecting stated rules is allowed; importing outside facts is not.

**Question 6 (moderate) — Choosing the accurate summary**

Read this short report:

"During Tuesday's incident, the monitoring system generated the first alert at 10:04. The on-call engineer acknowledged it at 10:06 and restored the service at 10:41. The root cause has not yet been confirmed, although early evidence points to a failed disk in the storage array. A full review is scheduled for Friday."

Which is the most accurate one-line summary for a handover?

- A) "Tuesday's incident was caused by a failed disk and resolved in 37 minutes."
- B) "Tuesday's incident was resolved in 37 minutes; root cause unconfirmed but a failed disk is suspected; review on Friday."
- C) "Tuesday's incident is still ongoing and under review."
- D) "The monitoring system failed on Tuesday and a review is scheduled."

**Correct answer: B**

**Explanation:** Check each summary against the passage. The service went down and was restored 10:04 to 10:41 — 37 minutes, so "resolved in 37 minutes" is fair. The root cause "has not yet been confirmed", so option A overstates the disk theory as fact — a subtle but serious distortion. Option C is false: the incident was resolved, only the review remains. Option D blames the monitoring system, which the passage never does — the monitoring system worked, generating the alert. Option B preserves every claim at its correct strength: resolved (fact), disk suspected (hypothesis), review scheduled (fact). Summarising without upgrading suspicions into facts is precisely the skill you use when you pass a problem to your team; the difference between "is" and "points to" is the difference between an honest handover and a misleading one.

**Question 7 (moderate) — Inference from an email**

Read this email from the service desk manager:

"Since Monday's change to the login system, we have received 43 calls about slow logins, compared with a typical 5 per week. We have not received calls about failed logins. Could your team investigate whether the change is related? Until then, we are advising callers that the issue is known and under investigation."

Which conclusion is best supported by the email?

- A) Monday's change definitely caused the slow logins.
- B) Call volumes about slow logins are far above their usual level, and the timing coincides with the change, which justifies an investigation.
- C) The login system is failing for most users.
- D) The service desk has stopped taking calls about logins.

**Correct answer: B**

**Explanation:** The email establishes two facts: an unusual volume (43 calls versus a typical 5) and a timing coincidence (since Monday's change). It explicitly asks whether the change "is related" — that is, the connection is a question, not a conclusion. Option A converts the coincidence into proven cause, which the email does not support; even the writer avoids that claim. Option C exaggerates: slow logins for some callers is not failure for most users, and the email says there were no failed-login calls at all. Option D misreads the final sentence — the desk is still taking calls and giving holding advice. Option B matches the email's actual strength: elevated volume plus timing equals grounds to investigate. Learning to hold a conclusion at exactly the strength the evidence supports — "coincides with" rather than "caused by" — is central to problem investigation, and verbal tests probe it constantly.

**Question 8 (moderate) — Following conditional instructions**

Read this extract from the out-of-hours instructions:

"If a critical alert fires between 18:00 and 08:00, phone the on-call engineer. If the on-call engineer does not answer within 10 minutes, phone the duty manager. For warning alerts during these hours, log a ticket for the day team; do not phone anyone unless the same warning fires three or more times within one hour."

At 22:15 the same warning alert fires for the third time since 21:30. According to the instructions, what should you do?

- A) Log a ticket for the day team and take no further action.
- B) Phone the duty manager immediately.
- C) Phone the on-call engineer, because the warning has fired three times within one hour.
- D) Wait until 08:00 and tell the day team in person.

**Correct answer: C**

**Explanation:** Trace the conditions. The alert is a warning, in the 18:00–08:00 window, so the default is: log a ticket, phone nobody. But there is an exception: "unless the same warning fires three or more times within one hour". Three firings between 21:30 and 22:15 is three or more within one hour (21:30 to 22:15 is 45 minutes), so the exception applies and phoning is now permitted — and the phoning route given in the instructions starts with the on-call engineer; the duty manager is only for when the on-call engineer does not answer within 10 minutes. So option C is correct: option A ignores the triggered exception, option B skips a step in the phoning chain, and option D ignores the instructions altogether. Conditional instructions — if X, do Y, unless Z — are everywhere in operations documents, and the technique is always the same: establish which conditions are met before choosing the action.

**Question 9 (moderate) — Clear-writing judgement**

You need to tell a non-technical user that their reported issue is fixed. Which message is best?

- A) "The incident has been remediated via a config rollback on the affected node; closing the ticket."
- B) "Your issue with saving documents is now fixed. Please try again and let us know if you have any further problems. We are closing this ticket, but you can reopen it by replying."
- C) "Fixed."
- D) "Following triage and RCA, we executed a rollback per the CAB-approved change; service restored to BAU."

**Correct answer: B**

**Explanation:** Judge each message from the user's point of view. Options A and D are written in operations jargon — "config rollback", "node", "RCA", "CAB", "BAU" — which tells a non-technical user almost nothing and may feel dismissive. Option C is plain but so brief that it fails the user: fixed what? Should they do anything? Can they come back? Option B does everything a closure message should: it names the issue in the user's terms ("saving documents"), states the outcome, tells them what to do next ("try again"), and leaves the door open ("reopen it by replying"). This is your User focus skill in written form — user stories and user needs teach that communication succeeds when it works for the reader, not when it showcases the writer's vocabulary. Assessments include clear-writing questions because how you write to users is part of how the service serves them.

**Question 10 (hard) — True/false/cannot-say with a subtle scope**

Read this extract from a service standard:

"All production servers must send their logs to the central logging platform. Test servers may send logs to the central platform where capacity allows. Logs held on the central platform are retained for 12 months and are accessible to the operations and security teams."

Statement: "Logs from test servers are retained for 12 months."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** This needs two careful steps. First, do test server logs reach the central platform at all? The passage says they "may" be sent "where capacity allows" — so some test logs may be on the platform and some may not; sending is optional and conditional. Second, the 12-month retention applies to "logs held on the central platform". So a test server's logs are retained 12 months if they are on the platform — but the statement is a general claim about "logs from test servers", and for any test server not sending logs to the platform, the passage says nothing about retention at all. Because the statement's truth depends on facts the passage leaves open, the answer is "cannot say". The skill here is scope-tracking: noticing exactly which group each rule covers. "All production servers" is a universal rule; "may … where capacity allows" is permission, not obligation. Misreading scope is one of the commonest causes of compliance mistakes in real operational documents, which is why tests probe it hard.

**Question 11 (hard) — Reconciling two documents**

Read these two extracts.

Extract 1, from the change schedule: "Change CH-2210: apply security patch to all web servers, Thursday 20:00–22:00. Approved."

Extract 2, from an email sent Wednesday by the change manager: "Please note CH-2210 has been rescheduled to Saturday 06:00–08:00 at the request of the web team, to avoid clashing with Thursday's product launch. The change schedule will be updated tomorrow."

On Thursday morning, a colleague checks only the change schedule and prepares to patch at 20:00. Based on both extracts, which statement is most accurate?

- A) The colleague is right to prepare for Thursday, because the schedule says Thursday and the schedule is the official record.
- B) The patch has been cancelled.
- C) The most current information says the change now happens Saturday 06:00–08:00; the schedule the colleague read had not yet been updated.
- D) The two documents contradict each other, so no one can know when the change will happen.

**Correct answer: C**

**Explanation:** Order the information in time. The schedule shows the original plan (Thursday). The Wednesday email is later information: the change is rescheduled to Saturday, and — crucially — the email explains why the schedule still shows Thursday ("the change schedule will be updated tomorrow"). So the documents do not truly conflict; one is simply newer than the other, and the newer one accounts for the older one's content. Option C captures this. Option A mistakes the official record for the current truth even when the record is known to lag. Option B invents a cancellation — rescheduled is not cancelled. Option D gives up too early: apparent contradictions often dissolve when you sequence the documents by date. This is a highly realistic scenario — out-of-date schedules cause real mis-timed changes — and the reading skill it tests, reconciling sources by recency and explanation, is one you will use whenever documentation and email disagree.

**Question 12 (hard) — Inference about user needs from a user story**

Read this user story and its acceptance note, written by a service owner:

"As a caseworker, I need the case system to stay available during the lunch period, so that I can complete urgent child-protection referrals without delay. Note: caseworker usage peaks between 12:00 and 14:00, unlike most internal systems, which peak mid-morning. Any maintenance window for the case system must avoid the lunch period."

Which of the following best explains why the standard mid-day maintenance slot used for other internal systems would be wrong for this system?

- A) Because maintenance is never allowed on internal systems.
- B) Because this system's users, unusually, need it most at exactly the time other systems are quietest — and the work they do then is urgent and high-stakes.
- C) Because caseworkers do not take lunch breaks.
- D) Because the system is too old to be maintained safely.

**Correct answer: B**

**Explanation:** The user story states the need (availability during lunch), the reason (urgent child-protection referrals), and the evidence (usage peaks 12:00–14:00, unlike other systems). A mid-day maintenance slot works for most systems precisely because mid-day is quiet for them — but for this system, mid-day is the peak, and the work done at the peak is urgent and serious. Option B assembles exactly this reasoning from the passage. Option A is a universal rule the passage never states; option C over-reads (the passage says usage peaks at lunchtime, not that nobody takes a break); option D invents a fact. This question shows why your role summary includes understanding the purpose of user stories: they exist to stop teams applying a standard technical decision — like a default maintenance window — to users whose needs do not fit the standard pattern. Reading a user story well is reading for the "so that" clause: the need behind the request.

### Preparation tips

- **Learn the three verdicts cold.** True means the passage guarantees it. False means the passage contradicts it. Cannot say means the passage neither guarantees nor contradicts it. Before every answer, ask which of those three actually applies.
- **Treat qualifier words as the main event.** "All", "some", "may", "must", "no earlier than", "unless", "where capacity allows" — circle them as you read. In both tests and procedures, these small words decide everything.
- **Answer from the passage, not from experience.** Your real-world knowledge of servers and patching is an asset at work but a liability in this test if it leaks into answers. If the passage does not say it, you do not know it.
- **Practise on real documents.** Take a team procedure or a GOV.UK service standard page, read a paragraph, and write two statements about it: one that is definitely true and one that is "cannot say". This trains the exact discipline the test measures.
- **For summary questions, check claim strength.** A good summary keeps facts as facts and suspicions as suspicions. Eliminate options that upgrade "suspected" to "confirmed" or downgrade "must" to "should".
- **Sequence documents by date.** When a question gives two sources, note which is newer and whether the newer one explains the older one. Recency plus explanation usually resolves the apparent conflict.

### Common pitfalls to avoid

- **Choosing "true" for plausible statements.** Plausible is not proven. The test deliberately writes statements that sound right but are unsupported — that is what "cannot say" exists for.
- **Choosing "cannot say" out of general caution.** The opposite error also costs marks. If the passage genuinely guarantees a statement — even by combining two sentences — the answer is "true", not "cannot say".
- **Missing the scope of a rule.** A rule about "production servers" says nothing about test servers. A rule about "logs on the platform" says nothing about logs elsewhere. Match the statement's subject to the rule's subject exactly.
- **Losing track of pronouns.** When a note says "restart it" or "if it recurs", pin down what "it" is before acting or answering. Ambiguous pronouns are a common trap in tests and a common cause of real mistakes.
- **Rushing long passages.** Skimming feels efficient but forces re-reading when the questions probe details. One careful read with qualifiers circled is faster overall than two hasty reads.
- **Writing (or choosing) jargon for the wrong audience.** In clear-writing questions, the best option is the one the intended reader would understand and act on — not the most technically complete one.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks you to judge how effective different responses would be. Unlike the other three assessments, there is no arithmetic and no passage to parse — the material is human: a colleague under pressure, an alert at an awkward moment, a mistake you have just noticed, a user who is frustrated. You are typically asked either to pick the most effective response, to pick the most and least effective from a set, or to rate each response on a scale.

The typical format is an online test of 25 to 40 minutes with 12 to 20 scenarios. It is usually untimed or generously timed, because it measures judgement rather than speed. There are no trick questions, but there are carefully written wrong answers: responses that sound decisive but skip escalation, or sound humble but dodge responsibility. Scoring compares your choices against the judgement of experienced professionals and against the behaviours the organisation values — things like user focus, collaboration, taking ownership, escalating appropriately, and treating people with respect.

Why does this assessment matter for an associate infrastructure operations engineer? Because at your level, judgement is mostly about knowing the edges of your role — and that is a genuine skill, not a limitation. You work under the direction of experienced engineers. The most valuable trainee is not the one who tries to solve everything alone, nor the one who asks before every keystroke, but the one who reliably knows which situations to handle, which to check, and which to escalate immediately. Employers assess this because getting it wrong in production environments has real consequences: a well-meaning solo fix can take down a service that citizens depend on, and an unreported mistake can turn a small problem into a large one.

A reassuring note about how to approach these questions: answer as your best professional self, not as you fear you might act on a bad day. The scenarios are designed so that the effective responses reflect honesty, promptness, user focus, and appropriate escalation. If you keep those values in view, your instincts will usually be right.

### How this assessment maps to your role

- **Escalation judgement** maps to your **Ownership and topic** skill: showing awareness of problem resolution processes and passing problems on to your team. Many scenarios test exactly when to handle, when to check, and when to escalate.
- **Honesty and accuracy under pressure** map to your **Incident management** skill: gathering the required information means reporting what actually happened — including your own mistakes — promptly and factually.
- **Curiosity with discipline** maps to your **Problem management** skill: contributing to investigations and remedies without exceeding your authority or guessing beyond the evidence.
- **Care for the people affected** maps to your **User focus** skill: showing awareness of user experience and user needs means remembering, in every scenario, that behind each ticket is a person trying to get something done.

### Practice questions

**Question 1 (easy) — An alert while your supervisor is away**

You are monitoring the dashboard while your supervising engineer is at lunch. A critical alert fires: a production database server has stopped responding. Your team's process says critical production alerts must be escalated immediately. What is the most effective response?

- A) Wait until your supervisor returns from lunch so you do not disturb them.
- B) Follow the escalation process immediately: contact the on-call engineer, log the incident, and let your supervisor know.
- C) Restart the database server yourself to save time.
- D) Watch the alert for 30 minutes to see whether it clears on its own.

**Correct answer: B**

**Explanation:** The process exists for exactly this moment, and it does not pause for lunch breaks. Option B follows it: escalate immediately, record the incident, and keep your supervisor informed — prompt, honest, and within your role. Option A confuses politeness with effectiveness; a critical production fault outranks an undisturbed lunch, and experienced engineers expect to be interrupted for this. Option C exceeds a trainee's remit on a critical production system — a restart at the wrong moment can corrupt data or destroy the evidence needed to diagnose the fault. Option D substitutes hope for action while users are affected. The professional behaviours at work here are ownership (you act rather than freeze) and escalation (you act through the right channel). At your level, escalating fast is not passing the buck — it is the job done well.

**Question 2 (easy) — You make a mistake**

While updating the asset register under direction, you accidentally delete a row containing a server's details. You are fairly sure you can retype it from memory. What is the most effective response?

- A) Retype the row from memory and say nothing — no harm done.
- B) Tell your supervising engineer what happened straight away, and ask whether the record can be restored from a backup or a previous version rather than from your memory.
- C) Leave the register as it is and hope nobody notices.
- D) Blame the register software for being confusing.

**Correct answer: B**

**Explanation:** Two values decide this scenario: honesty and accuracy. Option B is honest (you report the mistake promptly) and accurate (restoring from a backup or version history recovers the true data, whereas your memory might silently introduce errors — a wrong serial number in an asset register can mislead people for years). Option A might reconstruct the row correctly, but it conceals the incident and gambles on memory; if your recollection is wrong, you have converted a visible mistake into an invisible one, which is far worse. Option C abandons ownership entirely, and option D deflects blame instead of solving the problem. Everyone makes mistakes, especially while learning — organisations know this, and what they assess is what you do next. The trainee who reports errors immediately becomes trusted with more; the one who hides them becomes trusted with less.

**Question 3 (easy) — A frustrated user on the phone**

The service desk transfers a call to you. The caller is audibly frustrated: their team's shared drive has been slow all morning and they have a deadline. Your job is to log the incident; you do not know the cause. What is the most effective response?

- A) Say "that's not my area" and transfer them back to the service desk.
- B) Tell them the drive seems fine from where you are sitting, so it is probably their laptop.
- C) Listen, acknowledge the frustration, gather the details the incident process requires, give them their reference number, and explain what happens next.
- D) Promise the drive will be fixed within the hour so the caller feels better.

**Correct answer: C**

**Explanation:** Option C does everything within your role and does it with care: it treats the caller with respect, captures accurate information (your Incident management skill), and sets honest expectations by explaining the next step. Option A bounces a frustrated user between teams — the opposite of user focus. Option B dismisses their experience with a guess; "works for me" is neither diagnosis nor empathy, and blaming the user's equipment without evidence damages trust. Option D is kindness in the moment but dishonesty in effect: you cannot promise a fix time when you do not know the cause, and a broken promise will make the user angrier than the original fault did. Notice the shape of the best answer: acknowledge the person, do your part precisely, and be truthful about what you do not know. That combination — empathy plus accuracy — is what user focus looks like from the operations side of a phone call.

**Question 4 (moderate) — Asked to skip a step**

A busy engineer from another team asks you to apply a small configuration change to a test server for them, saying: "No need to raise a change record, it's only test — just do it now, I'll owe you one." Your team's process says all configuration changes, including on test servers, need a change record. What is the most effective response?

- A) Apply the change without a record — it is only a test server, and helping colleagues matters.
- B) Refuse rudely and report the engineer to their manager.
- C) Explain that your team's process requires a change record even for test servers, offer to help them raise one quickly, and check with your supervising engineer if the colleague pushes back.
- D) Apply the change secretly but write it down in your personal notebook in case anyone asks.

**Correct answer: C**

**Explanation:** The pressure in this scenario is social — a friendly colleague, a small favour, a plausible-sounding shortcut. Option C holds the process line while staying collaborative: you explain the rule, you actively help the colleague meet it (which usually takes minutes), and you escalate to your supervisor if disagreement continues — the right move for a trainee facing pressure from someone more senior. Option A breaks a process you were trusted to follow; test-server changes need records precisely because "only test" systems feed into patching schedules, capacity plans, and the next production release. Option B protects the process but wrecks the relationship; effectiveness includes how you treat people. Option D is the most corrosive: it knows the change should be recorded (hence the notebook) yet hides it from the systems that exist to hold that record. The behaviours being assessed are integrity under social pressure and constructive collaboration — saying "yes, via the right route" rather than plain "no".

**Question 5 (moderate) — Conflicting instructions**

Your supervising engineer asked you this morning to spend the day checking and updating the asset register. Mid-morning, a different senior engineer from your team asks you to drop that and help them cable a new rack for the rest of the day. Both cannot be done. What is the most effective response?

- A) Quietly stay on the asset register work, since it was assigned first, and hope the senior engineer forgets.
- B) Switch to the cabling work, since the request came from someone senior.
- C) Explain to the senior engineer that your supervising engineer assigned you the register work, and ask the two of them (or message your supervisor) to agree your priority before you switch.
- D) Try to do both by alternating every half hour.

**Correct answer: C**

**Explanation:** The trap is choosing based on who asked most recently or most senior. As a trainee, your task priorities are set through your supervising engineer, and the effective response makes the conflict visible to the people who can resolve it — quickly and without drama. Option C does that: it is transparent (both engineers know the situation), respectful (no one is refused outright), and correct (the decision is made at the right level, not by you guessing). Option A avoids the conversation and leaves the senior engineer expecting help that never comes. Option B silently abandons work your supervisor assigned, and they may be relying on it. Option D sounds diplomatic but serves both tasks badly — cabling half-done and a register half-checked. The professional behaviours here are communication and appropriate escalation: when two legitimate instructions collide, surfacing the conflict is not weakness, it is exactly what keeps small coordination problems from becoming missed commitments.

**Question 6 (moderate) — You spot something odd that nobody mentioned**

While doing a routine morning check, you notice that a production server's backup job has shown "completed with warnings" for the past four nights. No alert has fired, nobody has mentioned it, and your checklist only says to confirm the job ran. What is the most effective response?

- A) Do nothing — the checklist only requires confirming the job ran, and it ran.
- B) Mention it to your supervising engineer, show them the four nights of warnings, and ask whether it should be logged as a problem for investigation.
- C) Delete the warning messages so the report looks clean.
- D) Rerun the backup job yourself to see if the warnings disappear.

**Correct answer: B**

**Explanation:** This scenario tests the difference between doing the checklist and doing the job. The checklist is a minimum, not a ceiling: it says confirm the job ran, but four consecutive nights of warnings is a pattern — and patterns are the raw material of problem management. Option B shows exactly the proactive awareness your role asks of you: you noticed, you gathered the evidence (four nights, not one), and you passed it to your team through the right person, framing it as a question rather than a diagnosis. Option A is technically compliant and professionally hollow — the assessment behind the assessment is whether you care about the service or only the tick-box. Option C is falsification, full stop. Option D acts on a production backup system beyond your remit, and rerunning the job might mask the warnings without fixing whatever causes them — destroying the evidence an investigation would need. Curiosity plus escalation is the trainee's superpower: you are often the person who looks at routine outputs most regularly, which means you are often the first person able to spot a slow-burning problem.

**Question 7 (moderate) — Learning versus delivery pressure**

Your supervising engineer is walking you through diagnosing a network fault — a genuine learning opportunity. Halfway through, the service desk calls you: a user needs their incident reference number from this morning, which only you logged. Your engineer says "we're at the interesting bit". What is the most effective response?

- A) Ignore the service desk call; learning comes first.
- B) Abandon the diagnosis session entirely and spend the rest of the hour with the service desk.
- C) Ask your engineer for two minutes, quickly look up and pass on the reference number, then rejoin the diagnosis session.
- D) Tell the service desk to find the number themselves.

**Correct answer: C**

**Explanation:** Weigh the two demands honestly. The user's need is small but real and time-bound: they are waiting on the phone for a reference number that only you can provide, because you logged the incident. The learning session is valuable but can pause for two minutes without harm. Option C serves both: a brief, bounded interruption, then back to learning. Option A leaves a user stuck to protect your own development — inverting user focus. Option B overcorrects: the interruption needed two minutes, not an hour. Option D pushes work onto colleagues who cannot do it (the detail is with you) and fails the user. The judgement being assessed is proportionality: interruptions should cost what they need to cost and no more. There is also an ownership lesson tucked inside: because you logged the incident, you own the follow-through — "I logged it this morning" comes with "I can be asked about it this afternoon".

**Question 8 (moderate) — A colleague's risky shortcut**

You notice a fellow trainee logging into a shared administrator account using a password taped to the desk, rather than their own account, "because it's faster". You know your team's security guidance says administrative access must use individual accounts and passwords must never be written down. What is the most effective response?

- A) Say nothing — you are both trainees, and it is not your place.
- B) Speak to your colleague directly and kindly: point out the guidance, suggest they remove the taped password and use their own account, and if the practice continues, raise it with your supervising engineer.
- C) Immediately report them to the security team without speaking to them.
- D) Start using the taped password yourself, since it is clearly team custom.

**Correct answer: B**

**Explanation:** Security scenarios test whether you act at all, and then whether you act proportionately. Option B does both: a direct, friendly conversation gives your colleague the chance to fix an honest mistake (many shortcuts are habits nobody has challenged, not deliberate wrongdoing), while the follow-up condition — escalate if it continues — makes sure the risk does not simply persist because the conversation was comfortable. Option A treats speaking up as above your grade; it is not. Security is explicitly everyone's responsibility, including trainees, and a taped admin password is a genuine risk to production systems. Option C jumps to the most severe response first, skipping the collegial step that would usually resolve it — proportionality matters, though note that in cases of deliberate or serious wrongdoing, direct escalation would be right. Option D spreads the bad practice. The behaviours assessed: courage to raise concerns, respect for colleagues, and commitment to doing things properly even when shortcuts beckon.

**Question 9 (hard) — Pressure to close tickets**

It is the last day of the month, and your team's ticket-closure statistics are being reported tomorrow. An engineer says to you, half-joking: "Close out those five old incidents you logged — just mark them resolved, nobody checks. It makes our numbers look better." You know at least two of the five issues have not actually been confirmed as fixed with the users who reported them. What is the most effective response?

- A) Close all five — the engineer knows the team's ways better than you do.
- B) Close the three that seem genuinely done, and quietly leave the other two open; say nothing about the request.
- C) Explain that you are not comfortable marking unconfirmed incidents as resolved, offer to contact the two users today to check whether their issues are actually fixed, and mention the conversation to your supervising engineer if you are pressured further.
- D) Refuse and immediately email the whole team about the engineer's unethical behaviour.

**Correct answer: C**

**Explanation:** This scenario layers social pressure ("half-joking", more experienced colleague) over a data-integrity issue with a user-focus cost: an incident closed without confirmation is a user abandoned — if their issue persists, they must start again from the back of the queue. Option C threads it properly: it declines the improper part clearly but without hostility, it offers a constructive alternative that could legitimately improve the numbers (confirmed fixes closed today are real closures), and it keeps the escalation route ready if pressure continues — the right resort for a trainee, rather than the first move. Option A outsources your integrity to someone else's seniority; assessments consistently score "I was told to" poorly. Option B gets the records half-right but ducks the interpersonal issue, leaving the pressure in place for next month — and for other trainees. Option D takes a legitimate concern and detonates it: public accusation over a first, possibly flippant remark maximises damage and minimises the chance of a good outcome. The assessed behaviours are integrity, user focus, constructive challenge, and proportionate escalation — in that order.

**Question 10 (hard) — The unattended mystery**

You arrive early. Alone in the office, you notice the monitoring dashboard shows a production web server went offline at 06:40 — twenty minutes ago. No alert email was sent (it should have been), the on-call engineer has not been contacted, and nothing is logged. Your team starts arriving in about half an hour. What is the most effective response?

- A) Log the incident now, contact the on-call engineer per the escalation process, and separately note that the alert email failed to send — two issues, both reported.
- B) Wait for the team to arrive; twenty more minutes will not matter.
- C) Restart the web server — early morning is a quiet time, so it is low risk.
- D) Log the incident but do not contact anyone, since the on-call window is nearly over.

**Correct answer: A**

**Explanation:** Untangle the situation: there are two faults here, not one. The visible fault is a production server offline. The quieter, arguably more serious fault is that the alerting system failed — the safety net itself has a hole, which is why nobody knows yet. Option A handles both through the proper channels: escalate the outage immediately (production, users affected, process exists), and report the alerting failure so it gets investigated rather than silently recurring during some future 2 a.m. outage. Option B wastes the exact advantage you have — being the person who noticed — while users may already be affected; "quiet time" is an assumption, not a fact. Option C repeats the trap from earlier questions at a worse moment: a solo production restart with no one else aware, no incident logged, and no diagnosis is how small outages become long ones. Option D follows half the process and abandons the half that gets the service fixed. The deeper behaviour being assessed is proactive ownership: the process tells you what to do with an alert, and you apply it faithfully even when the alert itself failed to arrive. Noticing the failure of the safety net — and saying so — is precisely the kind of contribution that makes trainees indispensable.

**Question 11 (hard) — Most and least effective**

Your team is rolling out a change tonight that will briefly interrupt an internal service. This morning you realise the user-facing notice, which you drafted and your supervisor approved, states the wrong date — it says tomorrow night, not tonight. Users are planning around wrong information. Rank the responses: which is the MOST effective and which is the LEAST effective?

1. Tell your supervising engineer immediately, own the drafting error, and offer to send a corrected notice as soon as they approve it.
2. Send a corrected notice yourself right now without telling anyone, so the error is fixed fastest.
3. Say nothing — the interruption is brief, and most users will not notice.
4. Mention it casually to a teammate at lunch and see what they think you should do.

- A) Most effective: 1; least effective: 3
- B) Most effective: 2; least effective: 4
- C) Most effective: 1; least effective: 2
- D) Most effective: 4; least effective: 3

**Correct answer: A**

**Explanation:** Response 1 is the strongest: it is fast (immediately), honest (owns the error), user-focused (prioritises correcting what users were told), and properly governed (the correction goes out through the same approval that the original had — sensible, since your last unsupervised draft is the one containing the error). Response 3 is the weakest: it knowingly leaves users with false information, gambling that a service interruption they were not warned about will not matter — a direct failure of both honesty and user focus, and the only option that involves deciding to deceive by omission. Response 2 is flawed but not worst: its heart is in the right place (fix it fast) and its speed genuinely serves users, but bypassing your supervisor repeats the conditions that caused the first error and hides the mistake from the person accountable. Response 4 delays action on a time-critical issue, though it at least keeps the issue alive. So the ranking is 1 best, 3 worst — option A. In most-least questions, judge each response against the core behaviours (honesty, user focus, ownership, right channel) and remember that a well-meant wrong action usually ranks above a deliberate silence.

**Question 12 (hard) — Feeling out of your depth**

Three weeks into the role, your supervising engineer asks you to run the Friday morning checks alone for the first time, saying "you're ready". Privately, you are not confident about two of the fifteen steps — you have only watched them done once. It is Thursday afternoon. What is the most effective response?

- A) Say nothing and attempt all fifteen steps on Friday; you can probably work out the two uncertain ones as you go.
- B) Tell your engineer you are not ready and ask them to keep doing the checks for another month.
- C) Tell your engineer you are glad to take it on, name the two steps you are unsure about, and ask to walk through just those two together before Friday — or to have them on call when you reach those steps.
- D) Ask another trainee to do the two difficult steps for you on Friday.

**Correct answer: C**

**Explanation:** This scenario measures self-awareness and honest communication about your own limits — a behaviour that matters enormously in operations, where overconfidence causes outages. Option C is precise honesty: it accepts the development opportunity (you are ready for thirteen of fifteen steps, and your engineer's confidence in you is probably well-founded), and it targets the genuine gap with a specific, low-cost request — a rehearsal of two steps takes minutes on Thursday afternoon. It also gives your engineer accurate information about your capability, which is a gift to their planning, not an admission of failure. Option A gambles with production checks; "work it out as I go" is exactly how uncertain steps become incidents, and the safety cost dwarfs the embarrassment saved. Option B overcorrects: declining the whole task because of two steps stalls your development and mislabels you as less capable than you are. Option D hides the gap from the one person who should know about it, and hands your accountability to someone with no more experience than you. The wider lesson generalises well beyond week three: in this profession, "yes, and here is the specific support I need" is almost always a stronger answer than either silent struggle or blanket refusal.

### Preparation tips

- **Learn your team's escalation routes before any assessment — and before any incident.** Knowing who to contact for what, and how quickly, turns half of these scenarios into questions you have already answered in real life.
- **Use the values as a checklist.** For each option ask: is it honest? Is it prompt? Does it serve the user? Does it use the right channel? Does it treat colleagues with respect? The most effective option usually scores well on all five; the least effective usually fails several.
- **Answer as your best professional self.** Choose what the best version of you would do, and then — the important part — practise being that person at work, so the answer and the habit match.
- **Notice the "quiet fix" trap.** Across many scenarios, one option fixes things silently: no record, no report, no escalation. It almost always scores poorly, because operations runs on shared information. Silence, even competent silence, breaks the team's picture of reality.
- **Talk scenarios through with your supervising engineer.** Real judgement is calibrated socially. Asking "what would you have wanted me to do if…?" over a coffee is both excellent test preparation and excellent apprenticeship.
- **Do not overthink rating scales.** When asked to rate every response, place the clearly good and clearly bad ones first, then position the middling ones relative to those anchors. Your first professional instinct, checked against the values, is usually right.

### Common pitfalls to avoid

- **Choosing the hero option.** Solo fixes on production systems feel decisive and score badly. At your level, fast escalation through the right channel is the decisive act.
- **Choosing pure deference.** "Do whatever the senior person says" fails when the request conflicts with process or integrity. Seniority deserves respect, not blank cheques — the strong options combine respect with honest challenge or escalation.
- **Hiding mistakes.** The scenarios about your own errors have one consistent right shape: report promptly, correct through proper channels, learn. Any option built on concealment — however small the error — is a trap.
- **Confusing kindness with dishonesty.** Promising uncertain fix times, or leaving users with wrong information "to avoid worrying them", fails users. Real kindness is accurate information plus a clear next step.
- **Over-escalating everything.** Escalation is a skill, not a reflex. Options that jump to formal reports, managers, or all-team emails for issues a direct conversation would solve score poorly on collaboration and proportionality.
- **Forgetting the user in the room.** When a scenario includes a waiting, frustrated, or misinformed user, their need is usually the clock the scenario runs on. Options that serve the process but abandon the person rarely score well.

## Conclusion

Well done — you have worked through a full set of psychometric assessment practice materials built specifically for your role as an associate infrastructure operations engineer. That is no small thing, and it is worth pausing to notice what you have actually done.

You have practised cognitive questions using the real materials of your job: server naming patterns, checklists, alert groupings, timelines of changes, and the daily choice of what to do first. You have worked through numeric questions on the numbers that fill your dashboards — disk percentages, ticket averages, uptime targets, growth rates — with every calculation shown step by step. You have sharpened your verbal reasoning on procedures, policies, emails, and user stories, and learned the golden rule of answering from the passage alone. And you have thought your way through situational judgement scenarios about escalation, honesty, mistakes, user care, and the quiet courage of raising concerns — the very judgement calls that define a trusted trainee.

Along the way, you have picked up techniques that transfer directly to your working day: the timeline method for reasoning about incidents, the habit of sense-checking numbers against easy landmarks, the discipline of keeping facts and suspicions at their correct strength, and the checklist of professional values — honest, prompt, user-focused, right channel, respectful — that resolves most workplace dilemmas.

Here is the encouraging truth about assessments at your career stage: they measure skills that grow quickly with practice. Every dashboard you read carefully, every ticket you log completely, every problem you pass to your team with clear evidence, and every question you ask your supervising engineer is building exactly the capabilities these assessments measure. The reverse is also true — the habits these practice questions reward will make you visibly better at your job. That is the point of job-specific assessment: preparation for the test and growth in the role are the same activity.

If you are preparing for a real assessment, come back to this guide more than once. Redo the questions after a few weeks — you will be surprised how much more quickly the techniques come to mind. Time yourself gently on the second pass. Talk through the situational scenarios with your supervising engineer or a mentor; their reactions will calibrate your judgement faster than any written explanation can.

Above all, be encouraged. You are at the beginning of a career in a profession that keeps essential public services running — work that matters to millions of people who will never know your name. The care you bring to reading an alert, checking a number, or escalating a fault is the same care this guide has helped you practise. Keep learning, keep asking good questions, and keep being the person who notices. You are building something valuable: not just a set of test scores, but the professional judgement of a genuinely reliable engineer.

Good luck — and enjoy the journey ahead.
