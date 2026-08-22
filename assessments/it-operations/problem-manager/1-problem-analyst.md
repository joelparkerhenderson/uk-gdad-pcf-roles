# Problem Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a problem analyst working within the UK Government Digital and Data profession. Perhaps you are preparing for an internal assessment, applying for a new post, or simply curious about how psychometric tests connect to your day-to-day work. Whatever brought you here, this document will help you practise, build confidence, and feel ready.

First, a reassurance: psychometric assessments are not about catching you out, and they are not IQ tests full of strange puzzles. They are structured exercises that measure the everyday thinking skills your job already uses. As a problem analyst, you maintain software systems once they are up and running, and you support your problem manager in coordinating the resolution of problems. That work is full of exactly the skills these tests measure: spotting patterns in incident records, checking data carefully, reading procedures accurately, working out percentages and trends, and choosing sensible actions when the day gets busy.

The assessments in this guide are job-specific. That means every practice question uses material you genuinely handle: incident logs, known error records, configuration data, trend spreadsheets, service reports, knowledge articles, and emails from colleagues and specialists. You will not meet abstract shapes or trick riddles. You will meet a recurring printer fault, a spreadsheet of weekly incident counts, a change procedure with rules to apply, and a busy Tuesday where three things need doing at once. If you can handle those in real life — and you can — you can learn to handle them in a test.

This document is organised into four main assessment sections:

- a **cognitive assessment**, about pattern spotting, logical thinking, error checking, and prioritising
- a **numeric reasoning assessment**, about percentages, averages, and reading tables and trends
- a **verbal reasoning assessment**, about reading procedures and reports accurately
- a **situational judgement assessment**, about choosing effective actions in realistic work situations

Each section follows the same friendly pattern: what the assessment is, how it maps to the named skills in your role, ten to twelve practice questions that start easy and get gradually harder, full worked explanations for every answer, preparation tips, and common pitfalls to avoid.

Here is how to get the most from this guide. Work through it at your own pace — there is no timer here. Try each question honestly and write down your answer before reading the explanation. Then read the explanation even if you were right, because each one is a small lesson in technique. If a question feels hard, that is normal and useful: the explanation will walk you through it step by step, and the same idea will feel easier next time. Nobody starts fast; speed comes from practice.

One more encouragement before you begin. The skills in this guide are learnable. Analysts improve at these tests the same way they improve at root cause analysis: by doing a little, regularly, and paying attention to the feedback. Every question you practise here makes both your test performance and your daily work a little stronger.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the thinking skills your role uses every day, through practical scenarios rather than abstract puzzles. For a problem analyst, that means questions built from incident records, error patterns, configuration data, simple procedures, and the kind of detective work you do when the same fault keeps coming back.

The typical format is an online, timed test lasting 15 to 30 minutes. Questions cover pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Each question is multiple choice, and scoring is objective — your answers are compared against a norm group of people at a similar level. Many tests adapt as you go, giving you slightly harder questions when you answer correctly. Do not let that worry you: it simply means the test is finding your level, and everyone gets questions that stretch them. You will usually be offered a few unscored practice questions first, so you can get used to the screen and buttons without any pressure.

Why does this assessment matter for your role? Because problem analysis is structured thinking. When you support your problem manager, you look through incident records for patterns and trends. When you maintain systems, you check data carefully and notice when something does not match. When several tasks compete for your time, you decide what matters most. A cognitive test simply presents small, tidy versions of those same challenges. Practising them will genuinely sharpen your daily work — pattern spotting in a test and pattern spotting in an incident log are the same mental muscle.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your capability framework:

- **Pattern recognition** maps to your **Problem management** skill: initiating and monitoring actions to investigate patterns and trends is the heart of your role — noticing that five incidents are really one recurring problem.
- **Logical deduction** maps to **Incident management** and **Problem management**: diagnosing incidents, investigating their causes, and finding resolutions all mean reasoning carefully from evidence to conclusions — and knowing when the evidence is not enough.
- **Error checking** maps to **Asset and configuration management**: tracking, logging and correcting information to protect assets means spotting the record that does not match reality.
- **Prioritisation** maps to **Incident management** and **Ownership and initiative**: diagnosing and prioritising incidents, and owning an issue until it has a new owner or is resolved, both depend on ranking work sensibly.
- **Applied problem solving** maps to **Problem management** and **Service focus**: consulting specialists effectively, determining resolutions and preventative measures, and taking inputs to establish coherent frameworks that work.

### Practice questions

**Question 1 (easy) — Spotting a pattern in incident records**

You are reviewing this week's incidents for the case management application:

1. Monday 09:05 — "Application slow to load" — Team A
2. Monday 09:10 — "Case screen takes ages to open" — Team B
3. Tuesday 14:30 — "Forgotten password" — Team A
4. Wednesday 09:08 — "System very slow this morning" — Team C
5. Friday 09:12 — "Application crawling again" — Team B

Which incidents most likely belong to one recurring problem?

- A) 1, 2 and 3
- B) 1, 2, 4 and 5
- C) 3 and 4
- D) All five

**Correct answer: B**

**Explanation:** Look for what the incidents share. Incidents 1, 2, 4 and 5 all describe the same symptom (slowness) on the same application, and — the key detail — all occur within a few minutes of 09:00 on their day. That timing pattern suggests one recurring cause, perhaps something that runs each morning or the daily login peak. Incident 3 is different in every way: a password issue, mid-afternoon, unrelated symptom. Grouping related incidents is the first step of problem analysis: it turns four separate reports into one problem record worth investigating. In the test, count the shared features — symptom, system, timing — and group by those, not by team name or by how the user worded it.

**Question 2 (easy) — Simple deduction from a rule**

Your team's procedure says: "A problem record must be raised whenever the same fault causes three or more incidents in one month." The print service failed twice this month. A colleague says: "The procedure means we must not raise a problem record for it." Is your colleague right?

- A) Yes — the procedure forbids raising a record below three incidents.
- B) No — the procedure requires a record at three or more, but it does not forbid raising one earlier if it seems useful.
- C) Yes — problem records are only for major incidents.
- D) No — the procedure requires a record after every incident.

**Correct answer: B**

**Explanation:** Read the rule carefully. It says a record *must* be raised at three or more incidents. That sets a floor — a point where a record becomes compulsory. It says nothing about what you may do below that point, so raising a record after two worrying failures is still allowed; it just is not required. Your colleague has turned "must at three" into "must not below three", which the words do not say. A and C add rules that are not there; D ignores the threshold completely. This careful reading habit matters daily: procedures tell you what is required, what is forbidden, and — importantly — what is left to your judgement. Noticing that third category is a skill tests reward and teams value.

**Question 3 (easy) — Error checking a configuration record**

You are tidying configuration records after a software upgrade. The records show:

| Server | Application version | Last patched | Status |
|---|---|---|---|
| SRV-01 | v4.2 | 2 June | Live |
| SRV-02 | v4.2 | 2 June | Live |
| SRV-03 | v3.9 | 2 June | Live |
| SRV-04 | v4.2 | 2 June | Retired |

The upgrade notes say all live servers were upgraded to v4.2 on 2 June, and retired servers were left alone. Which record needs investigating?

- A) SRV-01
- B) SRV-02
- C) SRV-03
- D) SRV-04

**Correct answer: C**

**Explanation:** Check each row against the notes. SRV-01 and SRV-02 are live and on v4.2 — matches. SRV-04 is retired and was left on… wait, it shows v4.2. Check again: the notes say retired servers were left alone, so SRV-04 showing v4.2 could be odd — unless it was already on v4.2 before retirement, which is possible, so it is not clearly wrong. SRV-03 is clearly wrong: it is live, the notes say all live servers were upgraded, yet it still shows v3.9 — either the upgrade missed it (a real risk to fix) or the record is out of date (a data error to correct). Either way it needs investigating, and that is your **Asset and configuration management** skill in action: track, log and correct. In tests, pick the row that directly contradicts the stated facts, not the row that is merely slightly curious.

**Question 4 (moderate) — Prioritising your morning**

You arrive at 09:00 to find four tasks:

1. The problem manager has asked for your incident trend data by 11:00 for a meeting with the service owner.
2. A specialist has emailed answering your question about last week's database problem — no deadline.
3. The weekly configuration data check is due by the end of the day; it takes about an hour.
4. A colleague asks if you can help them understand a knowledge article "sometime today".

What is the most sensible order?

- A) 2, 4, 3, 1
- B) 1, 3, 2, 4
- C) 4, 3, 2, 1
- D) 3, 1, 4, 2

**Correct answer: B**

**Explanation:** Start with deadlines and importance together. Task 1 has the earliest hard deadline (11:00) and feeds a meeting where your problem manager depends on you — first. Task 3 has a same-day deadline and a known one-hour duration, so schedule it next to be safe. Tasks 2 and 4 have no deadlines: reading the specialist's answer (2) moves a real problem investigation forward, so it comes before the friendly but flexible help request (4) — though both fit in the afternoon. Option A puts no-deadline work ahead of an 11:00 commitment. Option C starts with the most flexible task. Option D does the hour-long check first and risks squeezing the 11:00 data. The pattern to remember: hard deadlines first (earliest first), then important-but-flexible work, and keep promises to people who are waiting on you — that is **Ownership and initiative** in daily form.

**Question 5 (moderate) — What changed before the fault?**

A reporting system worked fine until Thursday. Facts: (i) on Wednesday evening, a scheduled change updated the reporting system's database driver; (ii) on Thursday 08:00, users began getting "connection failed" errors; (iii) the database itself passes its health checks; (iv) a second system using the same database, but an older driver, works fine. What is the most reasonable first suspect?

- A) The database is down.
- B) The new database driver installed on Wednesday evening.
- C) Users are entering the wrong passwords.
- D) The network cable to the reporting server is unplugged.

**Correct answer: B**

**Explanation:** Line up the timing and the evidence. The fault appeared the morning after the driver change — timing that makes the change a strong suspect. The database passes health checks and serves the other system fine, which argues against A. Password errors (C) would not usually say "connection failed", and an unplugged cable (D) is pure guesswork with no supporting evidence — and the fact that the change touched exactly the failing component makes B far more likely. Notice the careful wording: the driver is the most reasonable *first suspect*, not the proven cause. You would test it — perhaps roll it back in a controlled way — before concluding. "What changed just before the fault?" is the single most useful first question in problem analysis, and test questions reward you for asking it while staying honest that a suspect is not yet a culprit.

**Question 6 (moderate) — Reading a pattern across the week**

The service desk sends you daily incident counts for the self-service portal over two weeks:

Week 1: Mon 8, Tue 7, Wed 8, Thu 7, Fri 8
Week 2: Mon 8, Tue 7, Wed 21, Thu 8, Fri 7

What does this pattern most suggest?

- A) The portal is steadily getting worse.
- B) Something unusual happened on Wednesday of Week 2, and it is worth finding out what.
- C) The Week 2 Wednesday number must be a typing mistake.
- D) Wednesdays are always the worst day for the portal.

**Correct answer: B**

**Explanation:** Read the shape of the numbers. Both weeks sit steadily at 7-8 incidents a day, except one day: Week 2 Wednesday spikes to 21 — nearly three times normal — then returns to normal on Thursday. That is a spike, not a trend, so A is wrong (nothing is steadily worsening). D is wrong because Week 1's Wednesday was a normal 8. C jumps to a conclusion: a typo is possible, and checking the raw records is a sensible first step, but you cannot *know* it is a mistake without looking. B is the honest reading: one day stands out clearly, and your job is to investigate — was there a failed change that morning, a spike in one error type, or indeed a data entry error? This is exactly your **Problem management** skill: spot the pattern, then investigate before concluding.

**Question 7 (moderate) — Choosing the most informative check**

Users in one office report that the HR system logs them out every few minutes. You want to know whether the fault is in the HR system itself or in that office's network. Which single check tells you the most?

- A) Ask the affected users to restart their computers.
- B) Find out whether users in other offices are also being logged out.
- C) Read the HR system's user guide.
- D) Wait a day to see if it stops.

**Correct answer: B**

**Explanation:** Think about what each result would tell you. If other offices have the same problem, the fault is probably in the HR system centrally; if only this office suffers, the fault is probably local — that office's network or setup. One question, and either answer cuts your search area in half. That is what makes it the most informative check. A might help one user temporarily but tells you nothing about the cause. C is background reading, not evidence. D loses a day and, worse, if the fault stops by itself you have learned nothing and it will likely return — problems that vanish untreated usually come back. Analysts call this kind of thinking "isolating the fault": design each check so that both possible results teach you something. It is a habit worth practising, and tests reward it directly.

**Question 8 (moderate) — Known error or new problem?**

A user reports that document uploads fail with error code E-417. You search the known error database and find a record: "E-417: upload fails when the file name contains special characters. Workaround: rename the file using letters and numbers only. Permanent fix scheduled in next quarter's release." The user's file is called "Report_Final(v2)!.docx". What should you do first?

- A) Raise a brand-new problem record for E-417.
- B) Apply the known workaround: ask the user to rename the file, confirm it works, and link the incident to the existing known error record.
- C) Tell the user the fix is coming next quarter and close the incident.
- D) Escalate to a specialist immediately.

**Correct answer: B**

**Explanation:** This is the known error process working exactly as designed. The error code matches, and the file name contains special characters — brackets and an exclamation mark — so the known cause fits. The right first move is the documented workaround: rename, confirm the upload now works, and link the incident to the known error record so the count of affected users stays accurate (that count is the evidence your problem manager uses to argue the permanent fix should stay scheduled — or be brought forward). A duplicates a record that already exists, which muddies the data. C leaves the user stuck for months when a one-minute workaround exists — the opposite of **User focus**. D spends a specialist's time on a solved question, which is not consulting specialists effectively. Remember the pattern: match, apply the workaround, link the record. It keeps users working and keeps the evidence clean.

**Question 9 (challenging) — Five whys, one wrong turn**

After a service outage, your team runs a "five whys" analysis: (1) Why did the service stop? The application server ran out of disk space. (2) Why? Log files filled the disk. (3) Why? Log files were never being deleted. (4) Why? The clean-up job that deletes old logs stopped running three months ago. (5) Why? …The team writes as its final answer: "Because the disk was too small," and recommends buying a bigger disk. What is the flaw in this conclusion?

- A) There is no flaw — a bigger disk would stop the outage happening.
- B) The final answer abandons the chain: the fourth answer points at the stopped clean-up job, so the fifth why should ask why that job stopped; a bigger disk only delays the same failure while the real cause remains.
- C) The analysis should have had six whys, not five.
- D) The first why is wrong because services stop for many reasons.

**Correct answer: B**

**Explanation:** Follow the chain. Each answer should explain the one before it. Answers 1 to 4 link cleanly: no space ← logs filled it ← never deleted ← clean-up job stopped. The fifth answer should therefore explain *why the clean-up job stopped* — perhaps a failed update, an expired account, or nobody monitoring it. Instead the team jumped sideways to "the disk was too small", which does not explain answer 4 at all. And the recommendation shows why this matters: with a bigger disk and a still-broken clean-up job, the logs simply take longer to fill the space — the outage is postponed, not prevented. Determining preventative measures — part of your **Problem management** skill — depends on following the chain to a cause you can actually fix. C misses the point (the count of whys is a guide, not a rule), and D rejects a verified fact. In tests and in real reviews, check that each "because" genuinely explains the step before it.

**Question 10 (challenging) — Two changes, one fault**

On Friday night, two changes ran: Change X updated the email service, and Change Y updated the shared login service that many systems use, including email. On Monday, users report two things: email attachments fail to open, and the HR system — untouched by either change on its own software — rejects some logins. Which explanation fits all the evidence best?

- A) Change X caused both issues.
- B) Change Y caused both issues.
- C) Change X likely caused the attachment fault, and Change Y likely caused the login fault — two changes, two separate issues.
- D) Neither change is connected to the faults.

**Correct answer: C**

**Explanation:** Test each option against both symptoms. Could Change X (email only) cause the HR login failures? No — X touched nothing the HR system uses. So A fails. Could Change Y (shared login) cause attachments to fail to open inside email? That is a stretch — login problems stop you getting in; they do not usually break attachment handling once you are in. So B fits one symptom well and one badly. C fits both cleanly: X (email update) explains the email attachment fault; Y (shared login update) explains login trouble on a system that uses that shared service. D ignores the timing of two faults appearing right after two related changes. The lesson: resist the urge to find one cause for everything. Sometimes there really are two problems, and forcing them into one explanation sends the investigation down the wrong path. Match each symptom to the change that touched what the symptom involves.

**Question 11 (challenging) — When the workaround hides the evidence**

A recurring fault crashes a case management service roughly once a week. The quick fix each time is to restart the service, which takes five minutes and clears the fault — but restarting also wipes the diagnostic logs that might show the cause. The specialist investigating the problem has asked for those logs. The service has just crashed again, users are waiting, and your standard instruction is to restart immediately. What is the best action?

- A) Restart immediately, as always — users come first, and the logs are lost every time anyway.
- B) Leave the service down until the specialist can come and inspect it, however long that takes.
- C) Take two minutes to copy the diagnostic logs somewhere safe, then restart the service and send the logs to the specialist.
- D) Restart immediately, but write down from memory what you think the logs would have shown.

**Correct answer: C**

**Explanation:** This is a classic problem-analysis dilemma: restoring service versus preserving evidence. The best answers usually do both, and here the numbers make it easy — two minutes of log copying against a weekly crash that will otherwise keep recurring forever because its evidence is destroyed every time. C restores service almost as fast as A while finally giving the specialist what the investigation needs; that is consulting specialists effectively, which is a named part of your **Problem management** skill. A repeats the loop that has already failed for weeks: quick fix, lost evidence, next crash. B swings too far the other way — leaving users without service for hours is a real harm when a two-minute compromise exists. D is well-meant but memory is not evidence; the specialist needs the actual logs. If you face this at work, it is also worth suggesting the team update the standard instruction: "copy logs, then restart" — a small process improvement that is precisely the preventative thinking your role exists to provide.

**Question 12 (challenging) — Building the coherent picture**

Your problem manager asks you to summarise everything known about a recurring network fault before a specialist meeting. You have: 14 linked incidents over 8 weeks; a note that 11 of the 14 occurred on Mondays; monitoring graphs showing bandwidth spikes each Monday 08:30-09:30; and an email from a specialist saying a Monday-morning data sync was doubled in size 9 weeks ago. Which summary best prepares the meeting?

- A) "We have 14 incidents and some graphs. The network team should look into it."
- B) "A recurring network fault (14 incidents, 8 weeks) occurs mainly on Monday mornings (11 of 14). Monitoring shows bandwidth spikes Mondays 08:30-09:30. A Monday data sync was doubled in size 9 weeks ago — just before the incidents began. Working theory: the enlarged sync saturates the network; proposed next step: test by rescheduling or throttling the sync."
- C) "The Monday data sync is definitely the cause and must be cancelled permanently."
- D) "Incidents happen at various times and no clear pattern has emerged yet."

**Correct answer: B**

**Explanation:** A good problem summary does three things: states the evidence, connects it into a working theory, and proposes a testable next step — while staying honest about what is theory and what is fact. B does all three: the incident count and timing pattern, the matching bandwidth spikes, the sync change that landed just before the incidents began, a clearly labelled "working theory", and a safe test (reschedule or throttle, not cancel). A wastes the analysis you have already done — handing specialists raw material they must re-assemble. C overshoots: the evidence is strong but circumstantial, and "definitely" plus "cancel permanently" turns a theory into a verdict and a business process into a casualty. D is simply false to the data — 11 of 14 on Mondays is a clear pattern. This is your **Service focus** skill — taking inputs and establishing coherent frameworks that work — and it is also how an analyst earns trust: arrive with the story assembled, the theory labelled as a theory, and a sensible test ready to propose.

### Preparation tips

- **Practise little and often.** Ten minutes a day for two weeks beats a two-hour session the night before. Regular short practice builds speed gently and keeps it.
- **Use your real work as free practice.** When incident records arrive, spend two minutes grouping them by shared features before doing anything else. When you check configuration data, predict what should be there before you look. Your job is a cognitive test with better scenery.
- **Learn the question rhythms.** Pattern questions want shared features; deduction questions want only what the evidence guarantees; error-check questions want the row that contradicts the facts; priority questions want deadlines and importance weighed together. Naming the type helps you choose the right method quickly.
- **Do timed practice near the end.** Start untimed while you learn the methods, then add a timer for your last few sessions so the real test's pace feels familiar rather than alarming.
- **Read the question before the data.** Knowing what you are looking for makes tables and lists much faster to scan.
- **Look after yourself on the day.** Sleep, water, a quiet room, and a stable internet connection genuinely help. Arrive at the test the way you would want to arrive at an important investigation: calm and prepared.

### Common pitfalls to avoid

- **Jumping from suspect to culprit.** "It broke after the change" makes the change your first suspect, not your proven cause. Choose answers that test the suspicion, and be wary of options containing "definitely" or "must be".
- **Adding rules a procedure does not contain.** "Must at three" does not mean "must not at two". Answer from what the text says, not what feels stricter.
- **Forcing one cause onto every symptom.** Sometimes two faults happen at once. Check each symptom against each candidate cause separately.
- **Treating a spike as a trend.** One bad Wednesday is not a worsening service. Look at the shape of the numbers before choosing words like "increasing" or "getting worse".
- **Rushing table checks.** Error-checking questions are lost to skimming, not to difficulty. Check each row against the stated facts, one at a time.
- **Freezing on hard questions.** Adaptive tests are supposed to stretch you. If a question feels too hard, give your best reasoned answer and move on — one question rarely decides your result, but a lost five minutes can.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how confidently you work with the kinds of numbers your role genuinely handles: incident counts, percentages, averages, availability figures, simple trends, and tables of service data. It is not a maths exam. Calculators are almost always allowed, and the arithmetic itself stays simple — percentages, division, subtraction. What the test really measures is whether you pick the right calculation, read tables accurately, and draw honest conclusions from data.

The typical format is an online, timed test of 20 to 35 minutes with 15 to 25 questions. Each question shows a small table, chart or short description of some data, then asks a multiple-choice question about it. Many tests adapt to your level as you go. Employers see your accuracy and speed, and they understand that both improve with familiarity — which is exactly what this section gives you.

Why does numeric reasoning matter for a problem analyst? Because numbers are your evidence. When you investigate patterns and trends, the pattern usually lives in counts: how many incidents, how often, on which days, rising or falling. When you help your problem manager make the case for a permanent fix, the case is numerical: this fault costs so many incidents a month and so many lost hours. When you manage service components against key performance indicators (KPIs), you compare actual figures with targets. An analyst who reads data accurately gets listened to; an analyst who mixes up a percentage can send a whole investigation down the wrong path. The good news: the handful of techniques below covers nearly everything, and each one is practised step by step.

### How this assessment maps to your role

- **Percentages and targets** map to **Availability and capacity management**: managing service components to meet business needs and KPIs means comparing actual availability and performance figures against targets, and converting between percentages and real hours.
- **Counts, rates and trends** map to **Problem management**: initiating and monitoring the investigation of patterns and trends is mostly done with incident counts over time — and knowing whether a number is genuinely rising or just wobbling.
- **Averages** map to **Incident management**: understanding typical resolution times, and noticing when one extreme value distorts the average.
- **Careful table reading** maps to **Asset and configuration management**: tracking and correcting information depends on reading the right row and column every time, whether it is asset counts or licence totals.
- **Data about users** maps to **User focus**: using quantitative data about users to turn user focus into outcomes — for example, working out which team or site is suffering most incidents per person.
- **Simple cost reasoning** maps to **Problem management** and **Change management**: determining preventative measures often means showing, with simple multiplication, that a fix costs less than the fault.

### Practice questions

**Question 1 (easy) — Percentage of incidents from one cause**

Last month there were 120 incidents on the services you support. Your analysis shows 30 of them were caused by the same recurring printer fault. What percentage of incidents came from that fault?

- A) 20%
- B) 25%
- C) 30%
- D) 33%

**Correct answer: B**

**Explanation:** Percentage = (part ÷ whole) × 100. Step 1: 30 ÷ 120 = 0.25. Step 2: 0.25 × 100 = 25%. A quick check without a calculator: 30 out of 120 is the same as 1 out of 4 (divide both by 30), and one quarter is 25%. Option C is the trap of repeating the raw number (30) as a percentage — always do the division. This little calculation is one you will use constantly: "one fault causes a quarter of all our incidents" is exactly the sentence that persuades people a permanent fix is worth the effort.

**Question 2 (easy) — Comparing before and after**

A permanent fix for a recurring fault went in at the end of June. Monthly incident counts for that fault: May 40, June 36, July 9. Roughly what percentage drop is July compared with June?

- A) 25%
- B) 50%
- C) 75%
- D) 90%

**Correct answer: C**

**Explanation:** Step 1: the fall = 36 − 9 = 27 incidents. Step 2: divide by the starting month (June): 27 ÷ 36 = 0.75. Step 3: × 100 = 75% drop. The important habit: percentage change always divides by the *starting* value, not the new one. A common error divides 27 by 9 or compares with May instead of June — read which months the question names. And notice what the number means for your work: a 75% drop right after the fix is strong evidence the fix worked, and the remaining 9 incidents are worth a look — same fault lingering somewhere, or something different that was being lumped in with it? Numbers like this are how you check whether preventative measures actually prevented.

**Question 3 (easy) — Reading a table accurately**

The weekly report shows open problem records by service:

| Service | Open problems | Of which: awaiting specialist | Of which: fix scheduled |
|---|---|---|---|
| Email | 6 | 2 | 3 |
| Case management | 9 | 5 | 1 |
| Portal | 4 | 1 | 2 |
| Printing | 7 | 3 | 4 |

Which service has the most problems awaiting a specialist?

- A) Email
- B) Case management
- C) Portal
- D) Printing

**Correct answer: B**

**Explanation:** The question asks about one specific column: "awaiting specialist". Read down that column only: Email 2, Case management 5, Portal 1, Printing 3. The largest is Case management with 5. The trap in table questions is answering from the wrong column — Printing has the second-most *total* open problems (7) and the most *fixes scheduled* (4), so if you skim you can easily pick D. Put your finger or cursor on the exact column the question names before comparing. Careful column-reading sounds trivial, but it is the same care that keeps your configuration records and problem data trustworthy — and it is the most common place easy marks are lost.

**Question 4 (moderate) — Average resolution time**

Five problems were closed this quarter. Their times from being raised to being resolved were: 5 days, 8 days, 6 days, 41 days, and 10 days. What is the average (mean) time, and what should you notice about it?

- A) 14 days; nothing unusual.
- B) 14 days; one very long problem (41 days) has pulled the average well above the typical case.
- C) 10 days; the average equals the middle value.
- D) 7 days; ignore the 41 because it is clearly wrong.

**Correct answer: B**

**Explanation:** Step 1: add the values: 5 + 8 + 6 + 41 + 10 = 70. Step 2: divide by how many there are: 70 ÷ 5 = 14 days. So the mean is 14 — but look at the data: four of the five problems took 10 days or less. The single 41-day problem has dragged the average up to a figure that describes none of the actual cases. That is what B says, and it is the honest reading. D invents a reason to delete real data — the 41-day case is not "wrong"; it is probably the most interesting problem in the list (why did it take six weeks — waiting on a supplier? lost ownership?). When you report averages to your problem manager, mention the outlier: "typically under 10 days, one exception at 41" tells the true story that "average 14" hides.

**Question 5 (moderate) — Availability target in hours**

A service must be available 99% of the time, measured over a 30-day month. There are 720 hours in that month. The service was down for a total of 9 hours. Did it meet the target?

- A) Yes — 9 hours is a small amount of downtime.
- B) Yes — the allowance is 10 hours and 9 is within it.
- C) No — the allowance is 7.2 hours and 9 exceeds it.
- D) No — any downtime at all breaches a 99% target.

**Correct answer: C**

**Explanation:** Work out the allowance first. A 99% availability target allows 1% downtime. Step 1: 1% of 720 hours = 0.01 × 720 = 7.2 hours. Step 2: compare: actual downtime 9 hours is more than the 7.2-hour allowance, so the target was missed. To confirm with the other direction: availability achieved = (720 − 9) ÷ 720 = 711 ÷ 720 = 0.9875 = 98.75%, which is below 99%. A relies on gut feel instead of arithmetic — "small" is not a calculation. B guesses a round number. D misunderstands how availability targets work: 99% deliberately allows some downtime. Converting percentages into real hours is a small skill that makes your KPI reports precise — and makes conversations about **Availability and capacity management** concrete: "we have 7.2 hours of allowance and we have used 9" is a sentence everyone understands.

**Question 6 (moderate) — Incidents per user: which site suffers most?**

Two sites use the same case system. Site A: 300 users, 45 incidents last month. Site B: 120 users, 30 incidents last month. A colleague says: "Site A has the bigger problem — 45 incidents versus 30." What do the rates say?

- A) The colleague is right: Site A has more incidents, so it has the bigger problem.
- B) Site A: 0.15 incidents per user; Site B: 0.25 incidents per user — Site B's users are actually suffering more, per person.
- C) The sites are equal.
- D) Rates cannot be worked out from these numbers.

**Correct answer: B**

**Explanation:** Raw counts mislead when the groups are different sizes, so divide by users. Step 1: Site A rate = 45 ÷ 300 = 0.15 incidents per user. Step 2: Site B rate = 30 ÷ 120 = 0.25 incidents per user. Step 3: compare: 0.25 is higher than 0.15, so the *typical user* at Site B experiences more incidents, even though Site A generates more tickets in total. Both facts are useful: total volume (Site A) tells you where the workload lands; the per-user rate (Site B) tells you where users are having the worse experience — and where an investigation might help most people fastest. This is **User focus** with numbers: quantitative data about users, turned into a decision about where to look. In tests, whenever two groups have different sizes, expect the question to hinge on rates, not totals.

**Question 7 (moderate) — Is the trend real?**

Weekly incident counts for a document service over eight weeks: 12, 14, 11, 13, 12, 15, 18, 21. Which statement best describes the data?

- A) The counts are steady with no change.
- B) The counts were steady around 11-15 for six weeks, then rose in the last two weeks (18, 21) — a possible emerging trend worth investigating now.
- C) The counts have been rising steadily all eight weeks.
- D) The last two weeks are certainly random variation and can be ignored.

**Correct answer: B**

**Explanation:** Look at the shape. Weeks 1-6 wobble between 11 and 15 — normal variation around a steady level. Weeks 7-8 step up to 18 and then 21 — two consecutive values above anything in the previous six weeks, and moving in the same direction. That is the classic early signature of an emerging trend. C overstates it (the first six weeks were flat, not rising); A ignores the last fortnight; D dismisses exactly the signal your role exists to catch — two rising weeks are not proof, but they are precisely when investigating is cheapest, before the trend becomes an outage. B says what the data says, no more, no less: steady, then rising, worth investigating. Catching this shape early — and saying it carefully — is the day-to-day craft of **Problem management** trend work.

**Question 8 (moderate) — Percentage of a percentage**

Of last month's 200 incidents, 40% related to the login service. Of those login incidents, 25% were caused by expired passwords. How many incidents were caused by expired passwords?

- A) 20
- B) 50
- C) 80
- D) 130

**Correct answer: A**

**Explanation:** Take it in two steps. Step 1: login incidents = 40% of 200 = 0.40 × 200 = 80. Step 2: expired-password incidents = 25% of those 80 = 0.25 × 80 = 20. So 20 incidents. The trap answers are the intermediate values: 80 is the login total (option C), and 50 is what you get by wrongly adding the percentages or taking 25% of 200. Percentages "of a percentage" always chain by multiplying step by step — never add them, and always apply the second percentage to the smaller group, not the original total. This pattern appears constantly in analysis work: "40% of incidents are service X, and a quarter of those are cause Y" is exactly how you narrow a big pile of tickets down to one fixable cause.

**Question 9 (challenging) — Combining unequal months fairly**

The recurring database fault caused these incident counts: April 10 incidents in 1,000 total incidents; May 30 in 2,000 total. A colleague calculates: "April 1%, May 1.5%, so on average the fault causes 1.25% of incidents." What is the true combined percentage across the two months?

- A) 1.25% — the colleague is right.
- B) 1.33% — combine the raw numbers: 40 fault incidents out of 3,000 total.
- C) 2.5% — add the two percentages.
- D) 1.5% — use the bigger month only.

**Correct answer: B**

**Explanation:** To combine two periods, go back to the raw numbers. Step 1: total fault incidents = 10 + 30 = 40. Step 2: total incidents = 1,000 + 2,000 = 3,000. Step 3: combined percentage = 40 ÷ 3,000 = 0.0133 = 1.33%. The colleague averaged the two percentages (1% and 1.5% → 1.25%), which silently treats both months as the same size — but May had twice the incidents, so its 1.5% deserves twice the weight. Averaging percentages from different-sized groups is one of the most common data mistakes in workplaces, and one of the most common traps in numeric tests. The safe rule is short: *percentages combine through their raw numbers, not through each other.* When your monthly figures feed a quarterly report, this one habit keeps the quarterly number honest.

**Question 10 (challenging) — Does the fix pay for itself?**

A recurring fault causes 6 incidents per month. Each incident takes a technician about 2 hours to resolve, and on average 15 users each lose 1 hour of work. Staff time is costed at £30 per hour for everyone involved. A permanent fix would take a specialist 3 full days (24 hours) at £60 per hour. Roughly how many months of avoided incidents pay for the fix?

- A) About half a month
- B) About 1 month
- C) About 3 months
- D) About 6 months

**Correct answer: A**

**Explanation:** Work out both sides. Cost of one incident: technician 2 hours × £30 = £60; users 15 × 1 hour × £30 = £450; total = £510 per incident. Monthly cost: 6 × £510 = £3,060. Cost of the fix: 24 hours × £60 = £1,440. Payback: £1,440 ÷ £3,060 ≈ 0.47 of a month — about half a month, or roughly two weeks of avoided incidents. So the fix pays for itself almost immediately, and every month afterwards saves about £3,000. Two habits to notice: include *everyone's* lost time, not just the technician's (the users' £450 dwarfs the £60 of fixing), and compare like with like (monthly cost versus one-off cost). This is the arithmetic behind determining preventative measures — your **Problem management** skill — and it is how an analyst turns "this fault is annoying" into "this fault costs £3,000 a month and the fix costs £1,440", which is a sentence that gets fixes approved.

**Question 11 (challenging) — Reading two measures together**

The monthly report for four services shows incident counts and average resolution times:

| Service | Incidents | Average resolution time |
|---|---|---|
| Email | 60 | 2 hours |
| Case management | 25 | 8 hours |
| Portal | 40 | 3 hours |
| Printing | 75 | 1 hour |

Which service consumed the most total resolution effort (incidents × average time)?

- A) Email
- B) Case management
- C) Portal
- D) Printing

**Correct answer: B**

**Explanation:** Multiply each pair. Email: 60 × 2 = 120 hours. Case management: 25 × 8 = 200 hours. Portal: 40 × 3 = 120 hours. Printing: 75 × 1 = 75 hours. The most total effort went into Case management — 200 hours — even though it had the *fewest* incidents. Neither column alone tells you this: Printing tops the incident count but each one is quick; Case management's incidents are few but long. Total effort = frequency × duration is one of the most useful single calculations in problem analysis, because it shows where the organisation's time is actually going — and therefore which problem, if permanently fixed, would give the most time back. A fault that is "rare but slow" can quietly cost more than the noisy frequent one everyone complains about. Tests love this question shape; so do good problem managers.

**Question 12 (challenging) — Honest conclusions from a small table**

An analysis of 80 incidents on the portal shows how they were resolved:

| Resolution route | Count | Average time to resolve |
|---|---|---|
| Known error workaround applied | 32 | 30 minutes |
| Restart by service desk | 28 | 45 minutes |
| Escalated to specialist | 20 | 6 hours |

A colleague drafts this conclusion: "75% of portal incidents are resolved quickly without specialists, so the portal has no serious underlying problems." Which assessment of the draft is fairest?

- A) Fully correct — the numbers prove the portal is healthy.
- B) The 75% figure is right (60 of 80 resolved without escalation), but the conclusion overreaches: 32 incidents needed a known error workaround and 28 needed restarts — quick fixes repeated 60 times suggest underlying problems that are being patched, not absent.
- C) The figure is wrong — only half were resolved without specialists.
- D) Nothing can be concluded from only 80 incidents.

**Correct answer: B**

**Explanation:** Check the arithmetic first: resolved without specialists = 32 + 28 = 60; 60 ÷ 80 = 0.75 = 75%. The figure is correct, so C is out. But now read what the routes *mean*. A "known error workaround" applied 32 times means a known fault is still occurring 32 times a month — the workaround is quick, but the fault is real and recurring. Similarly, 28 restarts suggest something repeatedly needs restarting. Fast resolution is good news for incident management; it is not evidence of problem-free services — if anything, the table is a to-do list for problem management: the known error and the restart-prone component are both candidates for permanent fixes. That is the distinction at the heart of your role: incidents ask "how fast did we recover?", problems ask "why did it keep happening?". D is too defeatist — 80 incidents with clear route patterns is plenty to reason from, carefully. The fairest reading is B: right number, wrong conclusion. Being able to say exactly that — politely, with the arithmetic to back it — is one of the most valuable things a problem analyst brings to a meeting.

### Preparation tips

- **Master the big five.** Part-of-whole percentages, percentage change, averages, rates per user or per day, and frequency × duration cover nearly every question you will meet. Practise each until the method is automatic.
- **Write the sum before reaching for the calculator.** Jot "27 ÷ 36" or "40 ÷ 3,000" first. Choosing the right division is the skill; the calculator only does the digits.
- **Recompute one real report each week.** Take your team's weekly figures and redo the percentages yourself. It is realistic practice, and you will occasionally catch a genuine error — which is your job anyway.
- **Sanity-check every answer.** A drop from 36 to 9 should feel like "most of it gone" — if your calculator says 25%, something is off. Rough expectations catch typing slips.
- **Slow down on tables.** Find the exact row and column the question names before comparing anything. Ten careful seconds beat a fast wrong answer.
- **Practise explaining a number out loud.** "One fault causes a quarter of our incidents" — turning calculations into plain sentences is both a test skill (the right answer usually matches the honest sentence) and the analyst's real craft.

### Common pitfalls to avoid

- **Dividing by the wrong number.** Percentage change divides by the starting value; per-user rates divide by the number of users; combined percentages divide total part by total whole. Most wrong options are right arithmetic on the wrong base.
- **Averaging percentages from different-sized groups.** April's 1% and May's 1.5% do not average to 1.25% when May is twice the size. Combine raw numbers, then take the percentage.
- **Judging by totals when sizes differ.** More incidents does not mean worse service if one site is three times bigger. Compare rates.
- **Letting one outlier speak for the data.** One 41-day problem makes the average 14 days even when typical is under 10. Report both the average and the exception.
- **Adding chained percentages.** 40% of incidents, then 25% of those, means multiply (0.40 × 0.25 = 10% of the total) — never add.
- **Confusing fast recovery with good health.** Quick workarounds sixty times a month is a problem wearing a friendly face. In test questions and real reports, check what the resolution routes actually imply.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand written material of the kind your role uses every day: procedures, knowledge articles, known error records, emails from specialists and suppliers, and extracts from service reports. The most common question type gives you a short passage and then statements to judge as **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage does not give enough information either way). Other questions ask you to draw a sensible inference, find the main point, or pick the clearest piece of writing.

The typical format is an online, timed test of 15 to 25 minutes with 20 to 30 statements spread across several passages. The golden rule — and it takes practice — is to answer *only from the passage*, even when you know the topic well. If the passage says something different from how your department works, the passage wins for the purposes of the test.

Why does this matter for a problem analyst? Because your work runs on accurate reading. You follow procedures where one word — "must", "may", "unless" — changes what is required. You read known error records and apply workarounds exactly as written. You read specialists' emails and pass their findings on without distorting them. And you write updates that colleagues and your problem manager rely on. Misreading is not a small slip in this role: a workaround applied to the wrong conditions, or a specialist's "possible cause" reported as "the cause", can send an investigation the wrong way for weeks. The reading discipline this test measures — exact, calm, and honest about what the text does and does not say — is the same discipline that makes your analysis trustworthy.

### How this assessment maps to your role

- **Reading procedures precisely** maps to **Change management** and **Incident management**: implementing change requests and applying change control procedures under supervision means doing exactly what the procedure says — no more, no less.
- **True/False/Cannot say discipline** maps to **Problem management** and **Asset and configuration management**: recording what an investigation has established — and only that — keeps problem records and configuration data honest.
- **Understanding technical explanations** maps to **Problem management**: consulting specialists effectively includes reading their answers accurately, including the difference between "confirmed", "likely" and "possible".
- **Reading continuity and process documents** maps to **Continuity management**: explaining the basic principles of continuity processes starts with reading those processes correctly.
- **Clear-writing judgement** maps to **User focus** and **Community collaboration**: engaging users and contributing to the work of others depends on writing that busy readers understand first time.

### Practice questions

**Passage 1 (for Questions 1-4):**

"When a known error record exists for a fault, service desk staff must apply the documented workaround before considering escalation. If the workaround fails, the incident must be escalated to the problem analyst, who will verify whether the failure indicates a new problem or a change in the existing one. Known error records may be updated only by the problem management team. Workarounds must be reviewed every three months to confirm they remain effective. A known error record may be closed only when the permanent fix has been deployed and verified."

**Question 1 (easy) — True, False, or Cannot say**

Statement: "Service desk staff may update a known error record if they discover the workaround no longer works."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says known error records "may be updated only by the problem management team". The word "only" excludes everyone else, including service desk staff — whatever they discover. What the service desk should do in that situation is also in the passage: a failed workaround means escalation to the problem analyst. So the statement contradicts the text: False. Watch for "only" in every passage you read — it is a small word that draws a hard boundary, in tests and in real procedures alike.

**Question 2 (easy) — True, False, or Cannot say**

Statement: "A known error record can stay open even after the permanent fix has been deployed."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage says a record may be closed "only when the permanent fix has been deployed *and verified*". Deployment alone is not enough — verification must also happen. So between deployment and verification, the record is still open, which means it can indeed stay open after deployment: True. If that felt like a trick, re-read the rule: two conditions joined by "and" must *both* be met. This mirrors good practice you will recognise: a fix is not finished when it is installed; it is finished when someone has confirmed it works. The test simply checks that you notice the two-part condition in the words.

**Question 3 (moderate) — True, False, or Cannot say**

Statement: "Workaround reviews happen every three months because workarounds often stop working."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage confirms the first half — workarounds must be reviewed every three months — but the statement also claims a *reason*: "because workarounds often stop working". The passage gives no reason at all. The review rule might exist because workarounds often fail, or as routine good practice, or for audit reasons; the text simply does not say. When a statement adds a motive or explanation the passage never gives, the answer is Cannot say, even if the added reason sounds perfectly sensible. This is one of the most common traps in the format: half-true statements. Check every part of the statement against the text — one unsupported part makes the whole statement unverifiable.

**Question 4 (moderate) — Inference**

Which of the following is the best inference from Passage 1 as a whole?

- A) The process is designed so that quick relief (workarounds) and permanent cure (fixes) are both managed, with clear ownership at each step.
- B) The service desk is not trusted by the problem management team.
- C) Most known errors never receive a permanent fix.
- D) Workarounds are more important than permanent fixes.

**Correct answer: A**

**Explanation:** Step back and ask what the rules collectively achieve: users get fast relief (workaround first), failures of that relief reach an analyst who checks whether the problem has changed, record quality is protected (one team updates), workarounds stay effective (quarterly review), and records only close when the cure is proven. That is a system balancing speed with thoroughness, each step owned — which is option A. B turns a data-quality rule into a motive about trust that the passage never expresses. C and D make claims about frequency and importance the text nowhere supports. Good inference questions reward the option that summarises what the text *does*, without inventing feelings, frequencies or rankings. It is the same skill as writing an honest summary of a procedure for a colleague.

**Passage 2 (for Questions 5-7):**

"Specialist email, Tuesday: 'I have examined the logs you preserved from Monday's crash. The memory usage climbs steadily from 06:00 until the crash at around 11:30, which is consistent with a memory leak in the reporting module. I cannot yet confirm this is the cause — two other explanations remain possible, and I have requested the supplier's diagnostic tool to narrow it down. In the meantime, restarting the service each morning before 08:00 should prevent crashes, as memory will not reach critical levels within a working day. Please log each restart and note the memory reading at restart time; those readings will tell us more.'"

**Question 5 (easy) — True, False, or Cannot say**

Statement: "The specialist has confirmed that a memory leak in the reporting module caused Monday's crash."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The specialist says the pattern is "consistent with" a memory leak, and then states directly: "I cannot yet confirm this is the cause — two other explanations remain possible." The statement claims confirmation; the passage explicitly denies it. That contradiction makes the answer False — not Cannot say, because the text does not merely stay silent; it actively says the opposite. This distinction — *consistent with* versus *confirmed* — is one you will meet constantly in specialist emails. Passing it on accurately ("the leading theory is a memory leak, not yet confirmed") is exactly what consulting specialists effectively means: their carefulness deserves to survive your summary.

**Question 6 (moderate) — True, False, or Cannot say**

Statement: "If the service is restarted at 07:30 each morning, memory will not reach critical levels before the end of the working day."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The specialist writes that "restarting the service each morning before 08:00 should prevent crashes, as memory will not reach critical levels within a working day". A restart at 07:30 is before 08:00, so the passage's claim applies to it directly: True. Note two honest wrinkles. First, the specialist says "should", so the passage presents this as their stated expectation — and the statement matches that expectation as given; the test asks whether the passage supports the statement, and it does. Second, the reading-and-logging request is separate: whether or not you log, the memory claim stands as written. If you hesitated between True and Cannot say, re-read the sentence: the passage commits to "memory will not reach critical levels within a working day" as the stated reason. Statements that restate the passage's own claims, applied to a case the passage covers (07:30 is before 08:00), are True.

**Question 7 (moderate) — What is being asked of you?**

According to the passage, what exactly should you do each day, and why?

- A) Restart the service before 08:00, log each restart, and record the memory reading at restart time — the readings will give the specialist more evidence.
- B) Restart the service whenever memory looks high, and email the specialist each time.
- C) Run the supplier's diagnostic tool each morning.
- D) Restart the service before 08:00; nothing else is needed.

**Correct answer: A**

**Explanation:** Gather the instructions from the text. There are three: restart each morning before 08:00; log each restart; note the memory reading at restart time. The purpose is also stated: "those readings will tell us more" — the routine is not just prevention, it is evidence-gathering for the open investigation. B invents a trigger ("whenever memory looks high") the specialist did not give — the instruction is time-based, not judgement-based. C confuses who does what: the *specialist* has requested the supplier's tool; nothing asks you to run it. D drops the logging, which discards exactly the data the specialist needs — prevention without evidence, which would leave the problem unconfirmed for another month. Instruction-reading questions reward completeness: find *every* imperative in the passage, and keep the stated purpose attached, because the purpose often tells you which details matter.

**Passage 3 (for Questions 8-9):**

"Change freeze notice: A change freeze will apply from 17:00 on Friday 20 March until 08:00 on Monday 30 March, covering all services in the casework group. During the freeze, standard and normal changes must not be scheduled or actioned. Emergency changes remain permitted, subject to the usual emergency approval process. Changes to services outside the casework group are unaffected by this freeze but remain subject to standard change control. The freeze supports the year-end processing period, during which system stability takes priority over all non-essential work."

**Question 8 (easy) — True, False, or Cannot say**

Statement: "During the freeze, an emergency change to a casework service can still go ahead if it passes the emergency approval process."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The notice says it plainly: "Emergency changes remain permitted, subject to the usual emergency approval process." The statement matches, including the condition (approval). True. The reading habit to note: freeze notices, like most rules, come with exceptions, and the exceptions are as much a part of the rule as the ban. A reader who remembers only "no changes during the freeze" will wrongly block a legitimate emergency fix; a reader who remembers only "emergencies allowed" will forget the approval condition. Accurate reading holds both — the rule *and* its exception *and* the exception's condition.

**Question 9 (challenging) — True, False, or Cannot say**

Statement: "A normal change to a payroll service — which is not in the casework group — scheduled for 25 March, is not permitted."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Trace the scope carefully. The freeze covers "all services in the casework group". The payroll service is stated to be outside that group, and the notice says such services are "unaffected by this freeze but remain subject to standard change control". So the freeze does not forbid this change; it merely leaves it under normal rules — which the statement's flat "not permitted" contradicts. The answer is False. If you hesitated toward Cannot say, notice why B is right: the passage does speak about out-of-scope services, and what it says ("unaffected") directly contradicts "not permitted". Cannot say is for silence; this passage is not silent. Scope questions — what a rule covers and what it leaves alone — are a favourite in tests because they matter so much in practice: applying a freeze too widely blocks legitimate work just as surely as applying it too narrowly causes year-end outages.

**Question 10 (moderate) — Clear-writing judgement**

You need to update the service desk about a recurring fault. Which version is clearest and most useful?

- A) "Further to ongoing investigative activities concerning the intermittent degradation phenomenon, stakeholders should note that remediation timescales remain to be confirmed."
- B) "The document upload fault is still under investigation. Until it is fixed: if a user reports error E-417, ask them to rename the file using only letters and numbers, then retry. This works in almost all cases. Log each occurrence against problem record PR-2041. Next update: Friday."
- C) "The upload thing is being looked at. Do the usual workaround."
- D) "Please be advised that the problem management function is cognisant of the upload issue and is progressing it through the appropriate process channels."

**Correct answer: B**

**Explanation:** Test each version against what a busy service desk reader needs: what fault, what to do, how well it works, where to log it, when they will hear more. B answers all five in plain words — the error code, the exact workaround steps, a realistic reliability note ("almost all cases"), the problem record for logging (which keeps the incident-linking evidence flowing to problem management), and a committed update day. A and D are fog: long words, no instructions — the reader finishes them knowing nothing they can do. C is at least brief, but "the usual workaround" assumes knowledge the reader may not have and gives no logging instruction, so the evidence trail dies. Clear writing is not casual writing and not formal writing; it is *complete and plain*: every needed fact, no unneeded word. That standard — shared by GOV.UK's plain-language guidance — is also the standard the test's clear-writing questions score against.

**Question 11 (moderate) — Reading a supplier bulletin accurately**

A supplier bulletin reads: "Version 5.2 resolves the intermittent session-timeout defect for customers using single sign-on. Customers not using single sign-on are unaffected by the defect and do not require this update. Version 5.2 requires a database schema update, which is irreversible once applied. We recommend applying 5.2 in a test environment first." Your department uses single sign-on. Which summary for your problem manager is most accurate?

- A) "Version 5.2 fixes our session-timeout problem. Because it includes an irreversible schema change, the supplier recommends testing first — so we should plan a test-environment installation before any production date."
- B) "Version 5.2 is optional for us since some customers do not need it."
- C) "Version 5.2 fixes the timeout problem and can be rolled back if it causes trouble."
- D) "We are unaffected by the defect."

**Correct answer: A**

**Explanation:** Apply the bulletin's conditions to your situation. You use single sign-on, so: the defect affects you (D is wrong — that sentence applies only to non-SSO customers, and B borrows their situation too); the fix is relevant; the schema change is *irreversible*, which C directly contradicts with "can be rolled back"; and the supplier recommends testing first. A carries all four facts across accurately and turns them into a sensible next step (test first, then plan production) — which is exactly what a problem manager needs from your summary: the facts that drive decisions, with nothing lost and nothing added. Bulletin questions reward conditional reading: work out which sentences apply to *your* case before summarising, and treat words like "irreversible" as load-bearing — they change how cautiously the whole plan must proceed.

**Question 12 (challenging) — Spotting the unsupported conclusion**

Your team's draft monthly report contains this paragraph: "Incidents linked to the finance system fell from 60 in January to 45 in February. This 25% fall shows that the memory patch applied in late January has resolved the underlying problem. Problem record PR-1980 can therefore be closed." Which critique of the paragraph is most accurate?

- A) The arithmetic is wrong: 60 to 45 is not a 25% fall.
- B) The arithmetic is right, but the conclusions overreach: a one-month fall after the patch is encouraging evidence, not proof of resolution — February may differ from January for other reasons — and the closure rule for problem records (fix deployed *and verified*) needs more than one suggestive month.
- C) The paragraph is fine as written.
- D) The paragraph is wrong because incident counts can never tell us anything about problems.

**Correct answer: B**

**Explanation:** Check the number first: fall = 60 − 45 = 15; 15 ÷ 60 = 0.25 = 25%. The arithmetic is correct, so A fails. Now weigh the words resting on it. "Shows that the patch has resolved the underlying problem" — one month's improvement after a patch is *consistent with* resolution (like the specialist's phrasing in Passage 2), but a single month can also reflect ordinary variation, February's shorter length, quieter workloads, or another change entirely. And "can therefore be closed" leaps further still: closing a problem record needs verification that the fix worked — a second month of data, or targeted checks that the patched fault specifically has stopped, would be reasonable verification; one suggestive number is not. D throws away evidence entirely, which is as unbalanced as the draft's overclaim. B holds the honest middle: right arithmetic, encouraging signal, conclusions too strong. Spotting exactly where a well-written paragraph steps beyond its evidence — and saying so constructively — is among the most valuable reading skills a problem analyst can bring to a team, and it is precisely what the hardest verbal questions measure.

### Preparation tips

- **Learn the three verdicts by heart.** True = the passage supports it. False = the passage contradicts it. Cannot say = the passage is silent or gives too little. Say them to yourself before each practice session until they are automatic.
- **Underline the small heavy words.** "Only", "must", "may", "unless", "and", "before", "irreversible" — circle them as you read. Most questions turn on one of them.
- **Check every part of a statement.** Half-true statements are the format's favourite trap: the review happens quarterly (true) *because workarounds fail* (not stated) — one unsupported clause changes the verdict.
- **Practise with your own documents.** Take a real procedure or supplier bulletin, write three statements about it (one true, one false, one cannot-say), and test a colleague — then swap. Ten minutes, genuinely effective, and your team's documents get a quiet quality check too.
- **Notice certainty words in real emails.** For a week, spot "confirmed", "likely", "possible", "should" in the messages you read, and keep the same word when you pass the information on. This is both test training and professional craft.
- **Pace yourself gently.** Around 30 to 45 seconds per statement is typical. If one statement ties you in knots, choose your best answer, flag it, and come back — momentum protects more marks than perfectionism.

### Common pitfalls to avoid

- **Answering from your own knowledge.** You know how known error records work in your department; the passage may differ. For the test, the passage is the only truth. This is the single most common cause of lost marks for experienced staff.
- **Confusing False with Cannot say.** False needs a contradiction in the text. If the passage simply never mentions it, the answer is Cannot say — however unlikely the statement sounds.
- **Missing scope boundaries.** Who and what does the rule cover? Freezes cover named groups; commitments cover named customers. Applying a rule outside its stated scope — or missing that the passage *does* address the case — flips your answer.
- **Upgrading uncertainty.** "Consistent with a memory leak" is not "caused by a memory leak". Keep the author's level of certainty; do not promote theories to facts, in tests or in your summaries.
- **Dropping conditions from instructions.** "Restart before 08:00 *and log the readings*", "deployed *and verified*", "permitted *subject to approval*" — conditions joined by "and" all count. Answers that keep only the memorable half are wrong.
- **Picking the most formal-sounding writing as "clearest".** Formality is not clarity. The clearest option is the one a busy reader can act on first time: concrete steps, plain words, complete facts.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace situations and asks you to judge how effective different responses would be. Unlike the other assessments, there is often no single provably right answer — instead, your choices are compared with the judgement of experienced practitioners and with the professional behaviours your organisation values. Question formats include picking the most effective response, picking the most *and* least effective, ranking all the options, or rating each option separately.

The typical format is 12 to 25 scenarios in 25 to 40 minutes. For a problem analyst, the scenarios live where your real dilemmas live: a fix that is tempting to apply without approval, a workaround that keeps hiding the evidence, a busy day where a promise to your problem manager competes with a colleague's urgent request, a specialist whose answer you do not fully understand, or a mistake — yours or someone else's — that would be easier not to mention. Employers use SJTs because these moments, far more than technical puzzles, predict who will be trusted with problems: the role runs on care, honesty and follow-through.

A reassurance before you start: SJTs are not personality tests, and they are not trying to trap you. The scoring consistently rewards a small set of professional behaviours you already know: keep the user's outcome in view, work openly with colleagues and specialists, own what you pick up until it truly has a new home, escalate honestly and at the right time, and treat everyone — including apprentices and quieter colleagues — in a way that helps them contribute. When you are unsure, a simple test works remarkably well: which option would you be comfortable explaining tomorrow to your manager, the affected user, and your own conscience? That option is usually the scored answer.

### How this assessment maps to your role

- **Ownership dilemmas** map to **Ownership and initiative**: own an issue until a new owner has been found or the problem has been mitigated or resolved — scenarios test whether you hold on, hand over properly, or quietly drop things.
- **Evidence and honesty dilemmas** map to **Problem management** and **Asset and configuration management**: root cause analysis is only as good as its records; scenarios test whether you protect evidence and report findings straight, even when it is awkward.
- **Working-with-others dilemmas** map to **Community collaboration**: contributing to the work of others, motivating and empowering colleagues, creating the right environment, and recognising and dealing with issues in the team.
- **Escalation and consultation dilemmas** map to **Problem management** and **Incident management**: consulting specialists effectively and escalating at the right moment — neither too early with nothing prepared, nor too late with users suffering.
- **Process-under-pressure dilemmas** map to **Change management**: implementing change requests and applying change control procedures under supervision, especially when a shortcut looks harmless.
- **User-outcome dilemmas** map to **User focus**: remembering that behind every incident count is a person trying to get their work done.

### Practice questions

**Question 1 (easy) — The tempting unapproved fix**

While investigating a recurring fault, you find a configuration setting you are confident is the cause. Changing it takes thirty seconds. Your team's procedure requires configuration changes to go through a change request, which for this type is usually approved within a day. The fault is annoying but has a working workaround. What is the most effective response?

- A) Make the change now — it is tiny, you are confident, and the paperwork can follow.
- B) Raise the change request today, noting the evidence that points to this setting, and apply the change once it is approved.
- C) Leave it — the workaround works, so nothing more is needed.
- D) Ask a colleague to make the change instead, since you found it.

**Correct answer: B**

**Explanation:** Check what is actually at stake. The fault is managed (a workaround exists), and approval takes about a day — so the cost of following the procedure is small, and the benefit is real: the change is reviewed, recorded, and visible to whoever investigates anything unusual afterwards. That record-keeping is not bureaucracy; unrecorded changes are one of the most common causes of mystery faults that problem teams later spend weeks untangling. B also does your analyst's job properly by attaching the evidence to the request. A breaks **Change management** — apply change control procedures under supervision — for a saving of one day on a mitigated fault. C stops at the workaround and abandons the permanent fix, leaving the underlying problem alive forever; workarounds are bridges, not destinations. D just moves the rule-breaking to someone else. The scored behaviours here: ownership of the real fix, through the proper route, with the evidence attached.

**Question 2 (easy) — You do not understand the specialist's answer**

You asked a database specialist about a recurring fault. Their emailed reply is full of terms you do not understand, and you cannot tell whether they are saying the fault is fixed or needs more work. Your problem manager expects your summary tomorrow. What is the most effective response?

- A) Copy the specialist's paragraphs into your summary unchanged — that way nothing gets distorted.
- B) Reply to the specialist: thank them, say you want to represent them accurately, and ask them to confirm in plain terms whether the fault is resolved or what remains to be done. Then summarise.
- C) Guess the most likely meaning from context and write your summary from that.
- D) Leave the specialist's email out of the summary to avoid getting it wrong.

**Correct answer: B**

**Explanation:** The honest position is: you have the information but not yet the understanding — and your job is to carry *meaning* to your problem manager, not just text. B fixes that directly, and notice how it does it: asking a specialist to clarify is not admitting weakness; it is **Problem management** as your framework defines it — consulting specialists *effectively* — and framing the request as "I want to represent you accurately" makes almost any specialist glad to help. A passes the confusion downstream: your problem manager now faces the same jargon with less context than you have. C risks building tomorrow's decisions on a guess — and a summary that says "resolved" when the specialist meant "needs more work" can close an investigation that should stay open. D deletes evidence from the record because it was inconvenient to read, which is the opposite of honest analysis. A useful lifelong habit sits inside this answer: never pass on information you could not explain in your own words; get it explained first.

**Question 3 (easy) — The colleague's repeated question**

A newer colleague asks you — for the third time this month — how to link incidents to a problem record. You showed them twice already. You are busy, and the explanation takes about ten minutes. What is the most effective response?

- A) Tell them, kindly, that you have already shown them twice and they should have noted it down.
- B) Do it for them each time they ask — it is quicker than teaching.
- C) Walk them through it once more, but this time have them do the steps while you watch, and afterwards point them to (or quickly write) a short crib sheet they can follow alone next time.
- D) Suggest they ask someone else this time so the load is shared.

**Correct answer: C**

**Explanation:** Ask why the two previous explanations did not stick — most likely because the colleague watched instead of doing. C changes the method, not just the repetition: people learn procedures by performing them (which is why the walkthrough has *them* at the keyboard), and the crib sheet turns the third explanation into the last one anyone needs to give — including for the next new starter. That is **Community collaboration** in its fullest sense: contributing to the work of others and creating the right environment, where asking is safe and learning materials exist. A makes the colleague feel foolish for asking, which teaches people to stop asking — and colleagues who stop asking start guessing, which is how records get mislinked. B keeps the colleague dependent forever and quietly grows your own workload. D passes the cost sideways without fixing the cause. Ten minutes invested this way repays itself within the month — SJTs reward the option that solves this instance *and* prevents the next.

**Question 4 (moderate) — Restore fast or preserve the evidence?**

The finance reporting service has crashed — the same crash the problem team has been chasing for a month. Users are waiting. You know from the investigation notes that the diagnostic state is lost at restart, and the specialist has never yet had a capture from a live failure. Copying the diagnostics takes about three minutes; then a restart takes five. Your service desk colleague is already reaching for the restart. What is the most effective response?

- A) Let the restart go ahead — eight minutes versus five matters to waiting users.
- B) Ask the colleague to hold for three minutes while you capture the diagnostics, then restart — and tell the specialist a capture is finally on its way.
- C) Insist the service stays down until the specialist can log on and inspect it live.
- D) Let the restart happen, then reconstruct what the diagnostics probably contained from the monitoring graphs.

**Correct answer: B**

**Explanation:** Put numbers on the trade-off. The extra delay is three minutes, once. The prize is the first-ever failure capture in a month-long investigation — very possibly the piece that ends the crashes for good. Three minutes against the chance of stopping a recurring outage is one of the best exchanges you will ever be offered, and B claims it while still restoring service within nine minutes. This is the analyst's signature move: serving *both* the incident (restore quickly) and the problem (preserve the evidence), because your role bridges the two. A repeats the pattern that has kept the fault alive for a month — every restart without a capture buys five minutes today and another crash next week. C overcorrects: an open-ended outage while waiting for a specialist harms users out of proportion, when a three-minute capture achieves nearly everything. D is reconstruction, not evidence — graphs show symptoms, not internal state, and the specialist needs the real thing. If your team's standing instruction says "restart immediately", the follow-up move is to propose amending it to "capture, then restart" — a preventative measure of exactly the kind your **Problem management** skill exists to determine.

**Question 5 (moderate) — The promise and the interruption**

You promised your problem manager the monthly trend analysis by 15:00 today; it needs about two more hours, and it is now 12:30. A team leader from another area arrives at your desk, stressed: their printer queue has jammed again and "IT never fixes it properly" — they want you to come and sort it now. The service desk is open and handles printer faults, but the team leader came straight to you because you helped once before. What is the most effective response?

- A) Go and fix the printer — a user in front of you always comes first.
- B) Tell them printers are not your job and turn back to your analysis.
- C) Take two minutes now: log the fault with the service desk yourself while they are with you (or hand it over warmly by phone), note that this is a *recurring* jam worth a problem-record look, and get back to the analysis so the 15:00 promise holds.
- D) Ask them to come back after 15:00.

**Correct answer: C**

**Explanation:** Untangle the three things happening at once: a live fault (belongs with the service desk, whose queue exists exactly for this), a commitment to your problem manager (a hard 15:00 deadline needing the remaining two hours), and — easy to miss — a problem signal: "jammed *again*" and "never fixed *properly*" is a recurring-fault report walking up to an analyst's desk. C handles all three in two minutes: the user leaves with the fault genuinely logged and owned (not deflected — you did the logging, which is what makes this different from B), the recurrence gets flagged toward a permanent look, and your promise survives. A is generous but wrong on the arithmetic: an hour at the printer for a fault the desk can dispatch means breaking a deadline your manager may be relying on in a meeting — and it teaches everyone that queue-jumping to your desk works. B is technically accurate and behaviourally poor: "not my job" sends a frustrated user away angrier and loses the recurrence signal. D just delays B politely. The scored pattern: route the work to the right owner *warmly and personally*, harvest the problem signal, keep your promise — **User focus**, **Ownership and initiative** and **Community collaboration** in one small moment.

**Question 6 (moderate) — Your own mistake in the records**

While preparing trend data for the quarterly review, you realise that a month ago you linked about twenty incidents to the wrong problem record. The error makes problem PR-1990 look much bigger than it really is — and it is one of the problems your manager plans to highlight in the review as needing investment. The review is in three days. Nobody else has noticed. What is the most effective response?

- A) Quietly fix the links and say nothing — the data will be right, and no one needs to know.
- B) Say nothing at all — the exaggerated figure supports a case for investment that is probably justified anyway.
- C) Tell your problem manager today: explain the error, show the corrected figures, and offer to re-run any analysis that used the wrong data before the review.
- D) Mention it casually after the quarterly review, once the moment has passed.

**Correct answer: C**

**Explanation:** Two things need repairing: the data and the decisions resting on it. A repairs only the first — but your manager is about to present conclusions built on the old numbers, so a silent fix leaves them exposed to standing in front of a review with figures that no longer match the records; if anyone checks, the mismatch surfaces at the worst possible moment, without the explanation only you have. C repairs both, three days early, with corrected figures in hand and an offer to re-run the analysis — which is what accountability looks like when it is done well rather than dramatically. B is the most corrosive option on the card: knowingly letting false data argue for a decision, even a "probably right" decision, breaks the one thing a problem analyst cannot work without — trust in their numbers. Decisions built on convenient errors do not stay convenient. D converts an honest mistake into a concealment with a date stamp. Here is the reassuring truth this scenario teaches: managers consistently rate the person who says "I found my own error, here is the correction" as *more* reliable afterwards, not less — self-caught, self-reported errors are how trust is built. Own it early; **Ownership and initiative** includes owning the awkward ones.

**Question 7 (moderate) — The specialist who has gone quiet**

Three weeks ago, a network specialist agreed to investigate the root cause behind a problem record you support. You have heard nothing since. The incidents are still occurring — eight more since then, each resolved with the workaround. Your problem manager has not asked about it yet. What is the most effective response?

- A) Wait until the specialist gets back to you — chasing might seem pushy, and they are surely busy.
- B) Contact the specialist with a friendly, useful nudge: the incident count since they took it on (eight more), an offer of whatever they need (fresh logs, examples), and a question about timescale — and note the contact in the problem record so its status is current.
- C) Escalate immediately to the specialist's manager about the lack of progress.
- D) Report to your problem manager that the investigation has stalled and someone should probably do something.

**Correct answer: B**

**Explanation:** Three weeks of silence with the fault still firing eight times is exactly when an open action needs its owner to act — and the record's owner-in-practice is you, because monitoring initiated actions is a named part of your **Problem management** skill: *initiate and monitor* actions to investigate. B is monitoring done well. Look at its ingredients: the nudge carries new information (eight more incidents — evidence that gently makes the priority case), an offer of help (which turns a chase into collaboration — maybe the silence is because they are stuck waiting for something you can provide), a concrete question (timescale), and a record update so anyone reading the problem sees its true status. A drifts: politeness that lets users absorb eight more incidents a month is not politeness to the users. C escalates before the simple step — a friendly chase — has even been tried; escalation is the right second move if nudges fail, not the first. D hands your own monitoring duty upward in vague form ("someone should"); if you do inform your manager, do it *after* the chase, with facts and a proposed next step. The scored behaviour: hold your threads, chase with evidence and warmth, and keep records truthful.

**Question 8 (challenging) — The pattern nobody asked you to find**

While doing your routine weekly data checks, you notice something odd: over the past six weeks, a small number of incidents across *three different services* all mention slow responses in the last week of the month. It is only eleven incidents in total, each closed individually, spread across teams that never see each other's tickets. You have plenty of assigned work, and no one has asked about this. What is the most effective response?

- A) Ignore it — eleven incidents in six weeks across three services is too small to matter, and it is not your assigned work.
- B) Spend the two or three hours it would take to fully investigate the cause yourself before telling anyone.
- C) Spend twenty minutes assembling what you have — the eleven incidents, the shared end-of-month timing, the three services — and bring it to your problem manager as a possible emerging problem worth a record and a look.
- D) Email the three service teams asking if they have noticed anything, and leave it with them.

**Correct answer: C**

**Explanation:** This scenario is your job description in miniature: patterns and trends do not announce themselves; they surface exactly like this — small, scattered, and visible only to someone who looks across boundaries. The end-of-month timing across three unconnected services hints at a shared cause (month-end processing load is a classic), and the right-sized response is C: organise the evidence briefly, then route it to the person whose role is to decide what problems get investigated — your problem manager, whom you exist to support. That division of labour matters: B inverts it, sinking hours of assigned time into a solo investigation before the problem has even been triaged, prioritised, or recorded — enthusiasm in the wrong order. A dismisses on size alone, but early patterns are *always* small; the ones worth catching are precisely the ones still small enough to fix cheaply, and "not my assigned work" is the boundary-thinking your cross-service vantage point exists to overcome. D scatters the question to teams who each hold only a third of the picture — the pattern only exists in the combined view, which only you currently have. The scored behaviours: proactive noticing, proportionate effort, evidence assembled before escalation, and support flowing to your problem manager in exactly the shape they can act on — **Problem management**, **Service focus** and **Ownership and initiative** working together.

**Question 9 (challenging) — Pressure to soften the findings**

Your analysis for a post-problem review shows clearly that a fault recurred for four months mainly because the fix was deprioritised twice in favour of new feature work. A team leader involved in those decisions catches you before the review and asks you to "soften the timeline section — no need to make it look like anyone sat on it. Just say the fix took time." The data is accurate and you have double-checked it. What is the most effective response?

- A) Soften it as asked — reviews go better when nobody is embarrassed, and the fix is in now anyway.
- B) Keep the timeline factual, and tell the team leader you will present it without blame: the section will state what was deprioritised and when as a process finding — evidence for better prioritisation of fixes — not as criticism of individuals; invite them to add their context about the competing pressures to the review.
- C) Refuse and add more emphasis to the delays so the review cannot miss them.
- D) Remove the timeline section entirely to stay neutral.

**Correct answer: B**

**Explanation:** Separate what the team leader is entitled to from what they are asking for. They are entitled to fair, blame-free framing and the chance to explain context — real pressures did drive those decisions. They are not entitled to a record that hides *why* users lived with a fault for four months, because that "why" is the review's most valuable finding: if fixes lose to feature work by default, that is a process problem which will repeat on the next fault — and preventing recurrence is the entire point of your discipline. B gives each side its due: facts intact, framing systemic ("what does this teach the process"), and the team leader converted from an opponent of the finding into a contributor of context — which is **Community collaboration** applied under pressure, and usually enough to dissolve the objection, since most people can live with true findings that are fairly framed. A trades the organisation's learning for one meeting's comfort; softened reviews produce un-learned lessons, and the same delay pattern next year. C weaponises accurate data — emphasis engineered to embarrass is advocacy, not analysis, and it invites exactly the defensiveness that buries findings. D destroys the finding to avoid the argument, which is A wearing neutral clothing. The analyst's line to hold, gently: *the data stays true; the framing stays kind; the lesson stays in the record.*

**Question 10 (challenging) — Most and least effective: the failing workaround**

The workaround for known error KE-2201 (rename files before upload) has started failing for some users — roughly one attempt in five now fails even after renaming. The permanent fix is scheduled for a release two months away. The service desk is getting frustrated repeat calls. Consider four actions:

1. Gather the evidence of the change — failure examples, rates before and now, anything the failing cases share — and take it to the problem manager: a changed known error may mean the problem itself has changed, and the fix's timing and content may need revisiting.
2. Update the known error record yourself to say "workaround now unreliable", so the desk at least has honest information.
3. Tell the service desk to keep applying the workaround and reassure users that a fix is coming in two months.
4. Ask the desk to log failed-workaround cases distinctly for the next few days while you analyse them.

Which pairing is correct?

- A) Most effective: 1; least effective: 2
- B) Most effective: 4; least effective: 3
- C) Most effective: 1; least effective: 3
- D) Most effective: 2; least effective: 4

**Correct answer: C**

**Explanation:** Rank the actions by what they change. Action 1 is the strongest: a workaround that has *started* failing is a signal the underlying problem may have shifted — new conditions, a partial change somewhere, a second cause joining the first — and that possibility belongs with the problem manager quickly, with evidence, because it can invalidate both the scheduled fix and everything the desk is telling users. (Recall the earlier passage's rule of thumb: a failed workaround goes to the analyst to check whether the problem is new or changed — this is that rule in action.) Action 4 is also genuinely good — structured evidence-gathering, and in real life you would likely do 4 *and* 1 together; but as a single action it delays the escalation a changed problem deserves. Action 2 has the right honesty instinct and the wrong route: known error records are updated only by the problem management team (procedures like Passage 1's exist widely for exactly this reason), so the move is to *get* it updated through the proper owner — which action 1 achieves. Action 3 is the least effective: it doubles down on a degrading workaround, scripts the desk to make promises ("two months") that may no longer hold if the problem has changed, and treats a one-in-five failure rate as nothing — users bounce between failed uploads and reassurance, which is how services lose trust. So: most 1, least 3 — option C. The habit to keep: when a workaround's behaviour changes, treat it as *data about the problem*, not just an inconvenience to manage.

**Question 11 (challenging) — The handover before leave**

You go on leave for two weeks starting tomorrow. You currently hold: (1) an active problem investigation awaiting a supplier response due next week; (2) the weekly data checks only you normally run; (3) a promise to a service desk colleague to review a draft knowledge article "soon" — no date agreed; (4) your monitoring of the KE-2201 situation from the previous question. It is 15:30 on your last day. What is the most effective use of your final ninety minutes?

- A) Work as late as needed tonight to finish everything yourself so nothing needs handing over.
- B) Write one detailed handover email to the whole team covering all four items, send it at 17:00, and go on leave.
- C) Prioritise the time-sensitive items: brief a named colleague (with your manager's agreement) on the supplier response due next week and the KE-2201 watch — live threads that cannot wait two weeks — and show them or write down the weekly checks; then tell the service desk colleague honestly that the article review will happen when you return, offering a date.
- D) Set an out-of-office message directing people to the team inbox, and deal with everything when you return.

**Correct answer: C**

**Explanation:** Sort the four items by what two weeks of silence would do to them. The supplier response (1) is live and due *during* your leave — unowned, it arrives, sits unread, and a month-long investigation loses two more weeks; it needs a named person, briefed, before you go. KE-2201 (4) is an actively changing situation — same verdict. The weekly checks (2) are exactly how patterns like Question 8's get caught; two skipped weeks is a real gap, so they need a temporary runner with instructions — and if your instructions do not exist in writing yet, this is the moment that fact gets fixed. The article review (3) is genuinely deferrable — the effective move is not to rush it tonight but to *re-promise honestly with a date*, which keeps the commitment clean. That is C, and notice its two structural features: handovers go to *named people who accept them* (your framework's ownership rule — an issue is owned until a *new owner has been found*, and a team inbox is not an owner), and your manager is in the loop on the coverage plan. A is the hero trap: investigations awaiting suppliers cannot be "finished tonight" by working late, and exhaustion before leave helps no one. B broadcasts instead of handing over — an email to everyone is owned by no one, and sent at 17:00 it cannot even be questioned. D simply schedules two weeks of dropped threads. The scored behaviour is continuity: live threads get owners, routine duties get runners, deferrable promises get honest new dates — and you get to actually rest, which is also part of sustainable ownership.

**Question 12 (challenging) — When prevention is unpopular**

Root cause analysis of a painful outage found that a data-import job fails whenever a supplier file arrives in a slightly wrong format — and the permanent prevention is a validation step that would reject bad files at the door with a clear error message. The catch: the team that runs imports dislikes the idea ("more steps, more rejections to chase") and points out, accurately, that the outage has happened only twice in a year. Your problem manager asks for your honest recommendation before deciding. What is the most effective recommendation?

- A) Recommend dropping the validation idea — the operating team knows their work best, and twice a year is rare.
- B) Recommend imposing the validation step exactly as designed — root cause analysis has spoken, and teams adjust eventually.
- C) Recommend the prevention, but with the numbers and the team's concern addressed together: quantify the two outages' cost against the validation's ongoing effort, and propose co-designing the details with the import team — for instance, clear rejection messages and a simple resubmission route — so the step prevents outages without becoming the burden they fear; if the numbers do not justify it, say so.
- D) Recommend waiting for a third outage, which would settle the argument.

**Correct answer: C**

**Explanation:** Your problem manager asked for honesty, and honesty here has three parts. First, the arithmetic: two outages a year sounds rare until costed — if each outage stops casework for a day, the comparison against "a validation step's ongoing effort" usually collapses in prevention's favour, and *doing that sum* (as in the numeric section's payback questions) is precisely your contribution; note C's crucial honesty clause — if the numbers genuinely do not justify it, your recommendation says so, because preventative measures must earn their place, not win by default. Second, the objection is *information*: "more rejections to chase" is a real usability flaw in the draft design, and co-designing with the import team — clear messages, easy resubmission — produces a control that works because its daily operators helped shape it. Preventions imposed over the heads of the people who run them get bypassed, quietly, and a bypassed control is worse than none because it is trusted while absent. That is why B fails even when its analysis is right. A defers entirely to convenience, leaving a known root cause armed and waiting. D outsources the decision to the next outage's victims. C is what "determine preventative measures" looks like at full maturity: evidence-costed, honestly bounded, and designed *with* the people who will live with it — **Problem management**, **Community collaboration** and **User focus** arriving at the same answer.

### Preparation tips

- **Anchor on the five behaviours.** User outcome, open collaboration, real ownership, honest and timely escalation, and helping others contribute. Before checking any answer, ask which behaviours each option serves — the scored answer usually serves several at once.
- **Use the "tomorrow morning" test.** Would you be comfortable explaining this choice tomorrow to your manager, the affected user, and a colleague you respect? Options that fail any one of those audiences are rarely the keyed answer.
- **Watch for the two classic traps.** The *heroic solo option* (do it all yourself, skip the process, work late) and the *clean-hands option* (not my job, not my queue, say nothing). Both appear in almost every SJT; both consistently score low. The strong answers route work properly while keeping hold of the outcome.
- **Practise on your real week.** Each day, pick one small dilemma you actually faced and write down the most and least effective responses you can imagine. Five minutes of this builds the judgement muscle the test measures.
- **Read the question stem precisely.** "Most effective *first* action" allows other good actions later — an option is not wrong because it leaves work remaining. "Most and least" questions are really asking you to find the option that helps most and the option that could *harm* most.
- **Stay calm about ambiguity.** Sometimes two options both look reasonable. Pick the one that is more honest, more owned, and kinder to the people involved — and move on. SJTs are scored across many scenarios; no single question decides your result.

### Common pitfalls to avoid

- **Choosing comfort over honesty.** Softening findings, staying quiet about your own error, letting flattering-but-wrong data stand — these options feel kind and score poorly. The kind *and* honest option is almost always available; look for it.
- **Skipping process because the fix is small.** Thirty-second unapproved changes are how mystery faults are born. If the situation is managed and approval is quick, the keyed answer follows the process.
- **Dropping ownership at a boundary.** "It is with the specialist", "the desk handles printers", "I am on leave" — SJTs place dilemmas exactly on these boundaries. The scored answers chase, hand over to named people, or route warmly — they never simply let go.
- **Escalating too early or too late.** Going over someone's head before a friendly chase, or waiting politely while users absorb eight more incidents — both lose marks. The pattern is: try the direct step with evidence first, escalate with evidence second.
- **Treating small signals as beneath attention.** Eleven scattered incidents, a workaround failing one time in five, a colleague going quiet in meetings — SJTs for analyst roles hide the important thing inside the small thing, because that is where real problems start.
- **Forgetting the person inside the ticket.** Options that are procedurally correct but leave a frustrated human standing at your desk unhelped ("not my job") score badly. Warm routing — where you make the connection rather than pointing at a door — costs two minutes and is nearly always part of the keyed answer.

## Conclusion

Well done — you have worked through the whole guide, and that is no small thing. You have met all four assessment types: cognitive questions built from incident patterns and configuration checks, numeric questions built from the percentages and trends that make up your evidence, verbal questions built from the procedures and specialist emails you read every day, and situational judgement questions built from the real dilemmas of an analyst's week. Forty-eight questions, each with a full walkthrough — and every one of them drawn from work you already do.

Here is the most important thing to take away: nothing in this guide asked you to become someone else. The skills that score well in these assessments — grouping incidents by what they share, dividing by the right number, reading "only" and "unless" carefully, preserving evidence before restarting, owning a thread until it truly has a new home — are the same skills that make you good at maintaining systems and supporting your problem manager. Practising for the test and getting better at the job are the same activity. That should take some of the fear out of test day.

Second, remember that these are learnable, practisable skills — not fixed talents. Speed comes from familiarity; accuracy comes from method; judgement comes from reflection. Little and often beats long and rare: ten minutes a day, honest attempts before reading explanations, and a moment after each question to name what the technique was. If some questions in this guide felt hard, that is a good sign — it means they were teaching you something, and the same shape of question will feel familiar next time. Everyone improves with practice; analysts, whose whole craft is learning from recurring patterns, improve faster than most.

Third, let this practice feed your development conversations. Your role sits at a genuinely valuable junction: you see across services, you turn scattered incidents into evidence, and you help turn evidence into fixes that stop things going wrong for good. The habits rehearsed here — careful reading, honest numbers, proportionate escalation, warm collaboration — are exactly the habits that grow analysts into problem managers, should you want that path. Consider sharing what you have practised with your line manager or mentor, and keep building on your Level 3 service management framework knowledge alongside it.

Finally, go gently on yourself. Preparation is not about being perfect; it is about being familiar, rested and calm. You have now seen how these tests think, and you have a set of methods for each type. Trust them, trust your practice, and walk in knowing that the material looks like your day job — because it does. Good luck. You are better prepared than you think.
