# IT Service Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an IT service analyst working within the UK Government Digital and Data profession. You might be preparing for an internal assessment, applying for a new post, or simply curious about how psychometric tests connect to the work you do every day on the service desk. Whatever brought you here, this document will help you practise, build confidence, and feel ready.

First, a friendly reassurance: psychometric assessments are not designed to catch you out. They are structured, standardised exercises that measure the thinking skills and workplace judgement that predict success in a role. For an IT service analyst, that means the tests are about things you already do. Every day you diagnose problems, read incident tickets carefully, check details against an asset register, work out whether a service level agreement (SLA) is being met, and decide when to resolve something yourself and when to escalate it to a resolver group. The assessments in this guide use exactly those kinds of situations, so practising them is really practising your job.

The guide covers four types of assessment, and each one links to a real part of your role:

- A **cognitive assessment** looks at how you spot patterns, follow rules, check for errors, and prioritise — the same skills you use when you triage a queue of tickets or perform root cause analysis.
- A **numeric reasoning assessment** looks at how you work with numbers — percentages, averages, and simple rates — the same skills you use when you read SLA reports or count ticket volumes.
- A **verbal reasoning assessment** looks at how carefully you read — the same skill you use when you follow a knowledge base article, read a policy extract, or write a clear ticket update.
- A **situational judgement assessment** looks at how you choose to act in everyday workplace situations — the same judgement you use when a user is upset, a ticket is about to breach its SLA, or a colleague needs help.

Each of the four sections follows the same pattern. First, "About this assessment" explains what the test measures and what the format usually looks like, so there are no surprises. Then "How this assessment maps to your role" connects the test directly to the named skills in your role summary, such as **IT service reporting** and **Ownership and topic**. After that come practice questions, arranged from easy to hard, each with a full worked explanation. Finally, you get preparation tips and a list of common pitfalls to avoid.

Here is how to get the most from this guide. Take one section at a time — there is no need to do it all in one sitting. Try each practice question honestly and write down your answer before you read the explanation. Read every explanation, even for questions you got right, because the walkthroughs teach technique, not just answers. And be kind to yourself: nobody gets every question right, and every mistake you make in practice is one you are less likely to make on the real test.

You already use these skills every day. This guide simply helps you show them at your best. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the thinking skills your role actually uses, through practical scenarios rather than abstract puzzles. Instead of asking you to rotate shapes, it presents the materials of your working day — incident tickets, asset records, checklists, escalation rules, and knowledge base entries — and asks you to reason about them quickly and accurately.

The typical format is an online, timed test lasting 15 to 30 minutes, with somewhere between 15 and 30 questions. The questions cover pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared against a norm group of people at a similar level. Many modern platforms are adaptive, which means the questions get slightly harder when you answer correctly and slightly easier when you do not — so do not panic if the test feels like it is getting tougher; that usually means you are doing well. Employers often see a breakdown of your speed and your accuracy, not just one score, so working carefully matters as much as working quickly. You will normally be offered a few ungraded practice questions before the real test starts, so you can get used to the screen layout without any pressure.

Why do employers use this kind of test for IT service analysts? Because frontline support is, at its heart, structured thinking under time pressure. When a user reports that "the system is broken", you have to gather clues, spot the pattern, rule things out one by one, and either resolve the issue or route it to the right resolver group — all while the SLA clock is ticking. A cognitive assessment is a miniature version of exactly that. It checks that you can hold a few facts in mind, apply a rule correctly, notice when a detail does not fit, and decide what matters most right now. These are learnable skills, and the practice questions below will help you sharpen them.

One more reassurance before you start: at the analyst level, assessments are calibrated for the analyst level. You are not being compared with senior managers. You are being asked to show the careful, methodical thinking that makes a good frontline analyst — the thinking you use every shift.

### How this assessment maps to your role

Each dimension of the cognitive assessment maps to a named skill in your role summary:

- **Pattern recognition** maps to your **problem solving** duties and your **Business analysis (IT operations)** skill. Diagnosing complex problem situations means noticing patterns: five tickets in an hour all mentioning the same application, or printer faults that only happen on one floor. Spotting the pattern early turns five separate incidents into one underlying problem.
- **Logical deduction** maps to your duty to **diagnose, evaluate and resolve complex problem situations or, when appropriate, escalate or route them to IT resolver groups**. Escalation rules are if-then rules. Applying them correctly — and only deducing what the facts actually support — is logical deduction in action.
- **Error checking** maps to your **Asset and configuration management** skill: you track, log and correct information to protect assets and components. A single wrong serial number or mismatched user record can undermine an entire asset register, so careful checking is central to your role.
- **Prioritisation** maps to your duty to respond to and resolve service desk incident tickets **according to a service level agreement (SLA)**, and to your **Ownership and topic** skill: owning an issue until it is resolved or handed to a new owner means constantly judging what needs your attention first.
- **Applied problem solving** maps to your **root cause analysis** duty and your work to **develop checklists for typical problems** and **recommend procedures and controls for problem prevention**. Root cause analysis is problem solving with discipline: separating symptoms from causes and testing each possibility in turn.
- Working through questions quickly but accurately also reflects your **Service focus** skill — showing awareness of different products and services means knowing which clues belong to which service.

### Practice questions

**Question 1 (easy) — Pattern recognition in a ticket queue**

You are watching the incoming ticket queue on Monday morning. The last six tickets read:

1. "Cannot log in to HR portal — password not accepted"
2. "Printer on floor 2 showing paper jam"
3. "HR portal rejects my password"
4. "HR portal login fails with error 401"
5. "Request: new starter needs a laptop"
6. "HR portal — locked out after password change"

What is the most likely pattern in this queue?

- A) A hardware fault is affecting floor 2
- B) Several tickets point to a possible shared issue with HR portal authentication
- C) The new starter's laptop is causing login failures
- D) There is no pattern; all six tickets are unrelated

**Correct answer: B**

**Explanation:** Four of the six tickets (1, 3, 4 and 6) mention the HR portal and a login or password failure. That is a cluster: several users, one service, one type of symptom, in a short time window. The most likely explanation is a shared issue — perhaps an authentication service problem — rather than four coincidences. Ticket 2 is a routine printer fault and ticket 5 is a service request, not an incident, so neither belongs to the cluster. Option A over-weights a single ticket, and option C invents a connection the facts do not support. Spotting clusters like this is exactly how a frontline analyst turns repeated incidents into a single problem record, which is the first step of root cause analysis and can save the resolver groups hours of duplicated effort.

**Question 2 (easy) — Logical deduction from an escalation rule**

Your service desk procedure says: "If an incident affects more than ten users, it must be escalated to the major incident manager immediately." A colleague tells you: "I have an incident affecting exactly ten users." Based only on the rule and this fact, which statement must be true?

- A) The incident must be escalated to the major incident manager
- B) The incident must not be escalated under any circumstances
- C) The rule does not require this incident to be escalated
- D) The incident affects the HR portal

**Correct answer: C**

**Explanation:** Read the rule carefully: it applies when an incident affects *more than* ten users. Ten users is not more than ten, so the rule does not require escalation. That is all you can deduce. Option A misreads "more than ten" as "ten or more" — a small wording difference with a big consequence. Option B goes too far the other way: the rule not *requiring* escalation is not the same as *forbidding* it; your judgement or another procedure might still support escalating. Option D introduces information that appears nowhere in the question. Assessments reward exactly this discipline: conclude only what the given words guarantee. On the service desk, the same discipline stops you escalating too early or too late, and helps you explain your decision by pointing at the exact wording of the procedure.

**Question 3 (easy) — Error checking an asset record**

You are logging a laptop into the asset register. Your service desk standard says every asset record must contain: asset tag (format GOV-nnnnn, five digits), owner's staff ID (format two letters then four digits), and location code (three letters). A colleague has drafted this record for you to check:

- Asset tag: GOV-04213
- Staff ID: JT29A4
- Location: LDN

Which field is wrong?

- A) Asset tag
- B) Staff ID
- C) Location
- D) None; the record is correct

**Correct answer: B**

**Explanation:** Check each field against its rule, one at a time. The asset tag GOV-04213 matches "GOV-" plus five digits — correct. The location LDN is three letters — correct. The staff ID must be two letters then four digits, such as JT2904; but JT29A4 has a letter in the middle of the digits, so it breaks the format. Working methodically field by field is the key technique: it stops your eye skimming past a small error because the record "looks about right". This mirrors your **Asset and configuration management** skill directly — you track, log and correct information to protect assets, and one badly formatted staff ID can mean a laptop that cannot be traced to its owner when a security team needs to find it fast.

**Question 4 (easy) — Prioritising two tickets**

It is 14:00. You have two open tickets:

- Ticket A: a director cannot change her email signature. Priority 4 (low). SLA resolution target: 3 working days. Logged this morning.
- Ticket B: a caseworker cannot access the benefits processing system and has citizens waiting. Priority 2 (high). SLA resolution target: 4 hours. Logged at 11:30.

Which ticket should you work on first, and why?

- A) Ticket A, because directors are senior and should never wait
- B) Ticket B, because it has higher priority and its SLA target is closer to breaching
- C) Ticket A, because it was logged first
- D) Ticket B, but only after you finish Ticket A, to keep the queue tidy

**Correct answer: B**

**Explanation:** Priority on a service desk is set by impact and urgency, not by the seniority of the person who logged the ticket. Ticket B stops a caseworker serving citizens — real business impact — and its 4-hour SLA target, started at 11:30, means it is due by 15:30. It is both higher priority and closer to breach. Ticket A is a minor inconvenience with three days of headroom. Option A confuses seniority with priority: a good analyst treats the director politely but works the queue by agreed priority. Option C uses arrival order, which ignores impact entirely. Option D delays the urgent work for no benefit. Working the queue by priority and SLA clock is the everyday meaning of resolving tickets "in a timely manner according to a service level agreement", straight from your role description.

**Question 5 (moderate) — Deduction during troubleshooting**

A user reports they cannot open a shared network folder. You establish these facts: (i) the user can open other network folders; (ii) a colleague sitting next to them, on the same network, can open the folder; (iii) the user could open the folder yesterday; (iv) the user's account was moved to a new security group last night as part of a planned change. What is the most likely cause to investigate first?

- A) The network cable at the user's desk is faulty
- B) The folder has been deleted from the server
- C) The user's permissions changed when their account moved security groups
- D) The whole network is down

**Correct answer: C**

**Explanation:** Use each fact to rule things out. Fact (i) — other folders open fine — rules out a general connection problem at the desk, so A is unlikely, and D is ruled out by both (i) and (ii). Fact (ii) — a colleague can open the folder — proves the folder still exists, ruling out B. Fact (iii) tells you something changed since yesterday, and fact (iv) hands you a known change that fits perfectly: security group membership controls folder permissions. The strongest hypothesis is the one consistent with all the evidence, and C is the only option that explains every fact. This is textbook root cause thinking: "what changed?" is one of the most powerful diagnostic questions an analyst can ask, and checking recent changes before deep technical digging often resolves incidents in minutes.

**Question 6 (moderate) — Pattern recognition across a week**

You are reviewing last week's incident log for the print service as part of developing a problem-prevention checklist. Incidents occurred at these times: Monday 09:05, Tuesday 09:12, Wednesday 09:03, Thursday 09:08, Friday 09:10. Each incident cleared by itself after about 20 minutes. Which line of investigation does the pattern most strongly suggest?

- A) Random hardware failures with no common cause
- B) Something scheduled or load-related that happens shortly after 09:00 each weekday
- C) A single user misusing the printer
- D) A fault that only occurs on Mondays

**Correct answer: B**

**Explanation:** Lay the data points side by side: five incidents, five weekdays, all within a nine-minute window just after 09:00, all self-clearing after roughly the same duration. Random failures (option A) would scatter across the day; a Monday-only fault (option D) contradicts four of the five data points; a single user (option C) is possible but explains neither the precise timing nor the daily regularity as well as B does. The tight time pattern points to something systematic: perhaps a scheduled job, a backup finishing late, or the morning login surge overloading the print server. As an analyst who develops checklists for typical problems and recommends procedures and controls for problem prevention, recognising time-based patterns is one of your most useful tools — it converts "the printer is flaky" into a specific, testable hypothesis you can pass to the resolver group.

**Question 7 (moderate) — Error checking a knowledge base article**

You are reviewing a draft knowledge base article before it is published. The article says:

"To reset a locked account: (1) Verify the caller's identity using two approved checks. (2) Open the admin console and select Unlock. (3) Ask the caller to confirm they can log in. (4) If the caller fails identity verification, complete the unlock and then report the call to security."

Which step contains a serious error?

- A) Step 1
- B) Step 2
- C) Step 3
- D) Step 4

**Correct answer: D**

**Explanation:** Steps 1 to 3 form a sensible flow: verify, unlock, confirm. Step 4 is dangerous: it says that when a caller *fails* identity verification, you should complete the unlock anyway and merely report it afterwards. That defeats the entire purpose of verification — if the caller might not be who they claim to be, unlocking the account could hand it to an attacker. The correct procedure would be to refuse the unlock, keep the account secured, and report the attempt. Reading each step and asking "what would actually happen if I followed this exactly?" is the error-checking technique assessments look for. It also reflects your real responsibilities: analysts follow and improve documented procedures, and a flawed knowledge article gets repeated by every analyst who trusts it, so catching the error before publication protects the whole desk.

**Question 8 (moderate) — Prioritisation with four competing demands**

It is 09:15. Four things need your attention:

1. A Priority 2 ticket you own, due to breach its SLA at 10:00, waiting on one final check you can do in 10 minutes.
2. A walk-up user who says their mouse is "acting strangely" but they can still work.
3. A voicemail from a resolver group asking you to confirm details on a ticket you escalated yesterday; they cannot progress it until you reply.
4. Your team leader has asked everyone to complete a mandatory security e-learning module "by the end of the week".

Which order is most defensible?

- A) 1, 3, 2, 4
- B) 2, 1, 3, 4
- C) 4, 1, 3, 2
- D) 3, 2, 4, 1

**Correct answer: A**

**Explanation:** Item 1 is urgent (45 minutes to SLA breach), high impact, and quick to finish — clearing it first prevents a breach on a ticket you own. Item 3 comes next: another team is blocked waiting on you, and your **Ownership and topic** skill means an escalated ticket is still your issue until the new owner can genuinely progress it; a quick reply unblocks them. Item 2 is a minor issue where the user can still work — deal with it politely once the urgent items are clear. Item 4 has a Friday deadline and no urgency today. Option B lets an SLA breach happen while you look at a working mouse; option C puts routine training ahead of everything; option D leaves your own near-breach ticket until last. The pattern to learn: sequence by urgency and impact together, and remember that unblocking other people multiplies your usefulness.

**Question 9 (moderate) — Applied problem solving with a checklist**

You are building a first-line checklist for "user cannot connect to Wi-Fi" incidents. You want the checklist to rule out the most common, quickest-to-test causes first. Which ordering best follows that principle?

- A) Check building network outage dashboard → check airplane mode / Wi-Fi toggle on device → forget and rejoin the network → escalate to network team
- B) Escalate to network team → check airplane mode → check outage dashboard → forget and rejoin
- C) Forget and rejoin the network → escalate to network team → check airplane mode → check outage dashboard
- D) Check airplane mode → forget and rejoin → check outage dashboard → escalate to network team

**Correct answer: A**

**Explanation:** A good diagnostic checklist tests broad, fast, high-probability causes before narrow or slow ones — and escalates only when first-line steps are exhausted. Checking the outage dashboard takes seconds and instantly tells you whether this is one user or a building-wide event; if there is an outage, every later step is wasted effort, so it earns first place. The device-level toggle check is the next fastest and catches a very common cause. Forget-and-rejoin takes a little longer and changes device state, so it comes after the quick checks. Escalation is correctly last in every good ordering — options B and C escalate before doing the basics, which wastes resolver group time and delays the user. Option D is close but skips the seconds-long dashboard check until third, risking three wasted steps during a known outage. This "cheap and likely first" principle is the heart of your duty to develop checklists for typical problems.

**Question 10 (hard) — Deduction with multiple rules**

Your desk's routing rules say: (i) hardware faults go to the Desktop team; (ii) access requests go to the Identity team; (iii) any ticket mentioning suspected phishing goes to Security, and this rule overrides all others; (iv) if a ticket fits none of these, it stays with the service desk. A ticket reads: "My new keyboard arrived but I also got an email asking me to 'verify my payroll login' via a link — it looks suspicious. Also, please can I get access to the finance shared drive?" Where should the ticket go first?

- A) Desktop team, because a keyboard is hardware
- B) Identity team, because there is an access request
- C) Security, because suspected phishing overrides all other routing
- D) It stays with the service desk, because it fits several categories at once

**Correct answer: C**

**Explanation:** The ticket touches three rules: a hardware mention (keyboard), an access request (finance drive), and suspected phishing (the "verify your payroll login" email). Rule (iii) states explicitly that phishing routing *overrides all others*, so Security must see the ticket first — a phishing email is time-critical because other staff may have received the same message. Options A and B each apply a valid rule but ignore the stated override; option D invents a rule that does not exist. In practice, you would route to Security first and also make sure the access request and keyboard note are logged separately so they are not lost — good analysts split multi-part tickets. The assessment skill here is handling several rules at once and respecting explicit precedence; the workplace skill is exactly the same, because routing errors on security issues are among the most costly a frontline analyst can make.

**Question 11 (hard) — Root cause analysis from an incident timeline**

You are doing root cause analysis on Friday's outage of the appointment booking service. The timeline: 08:00 nightly maintenance completes normally; 08:30 a configuration change is applied to the booking server; 08:45 monitoring shows response times rising; 09:10 users begin reporting timeouts; 09:30 the change is rolled back; 09:40 response times return to normal. Which conclusion does the timeline best support?

- A) The nightly maintenance caused the outage
- B) User reports caused the slow response times
- C) The 08:30 configuration change is the most likely cause, supported by symptoms starting after it and stopping after rollback
- D) The cause cannot be narrowed down at all from this timeline

**Correct answer: C**

**Explanation:** Root cause analysis leans on two questions: what changed before the symptoms started, and what made the symptoms stop? Maintenance finished at 08:00 with the service normal for 30 minutes afterwards, which weakens option A. The configuration change at 08:30 is followed within 15 minutes by rising response times — and, crucially, rolling back that change at 09:30 is followed within 10 minutes by recovery. Symptoms starting after a change *and* stopping after its reversal is strong evidence, far stronger than either clue alone. Option B reverses cause and effect: users reported the slowness because it existed. Option D is too pessimistic — the evidence does narrow things down, even if a formal review would still confirm the mechanism. Note the careful wording of C: "most likely cause". Good analysts hold conclusions with appropriate confidence, which is exactly what your **root cause analysis** duty and your **Business analysis (IT operations)** skill — investigating problems in existing processes — require.

**Question 12 (hard) — Problem prevention reasoning**

Over three months, your desk logged 90 incidents of "user locked out after password expiry". Investigation shows: passwords expire every 90 days; the expiry warning email is sent only once, 14 days before expiry; and 80% of locked-out users say they never saw the warning. You are asked to recommend one control for problem prevention. Which recommendation attacks the root cause most directly?

- A) Add more analysts to the desk on Mondays to handle lockout calls faster
- B) Improve the warning process — for example, repeated reminders through a channel users actually see, closer to the expiry date
- C) Tell users to write their passwords down so they do not forget them
- D) Increase the SLA time allowed for lockout tickets so they breach less often

**Correct answer: B**

**Explanation:** Separate the symptom (lockout calls) from the cause chain: expiry is routine, but the *warning is not reaching users* — 80% never saw the single email sent 14 days out. Option B attacks that link directly: more reminders, better timing, and a channel users notice would prevent lockouts before they happen. Option A treats the symptom — it handles calls faster but generates just as many. Option D is worse: it changes the measurement, not the reality, so users wait just as long while the numbers look better. Option C creates a security risk to solve a convenience problem, which no assessment or security team will ever reward. This is the essence of your duty to **recommend procedures and controls for problem prevention**: a good control removes future incidents rather than absorbing them, and the evidence (the 80% figure) tells you exactly which link in the chain is broken.

### Preparation tips

- **Practise with your own materials.** Spend ten minutes with a recent ticket queue, an asset register extract, or a knowledge base article and quiz yourself: what pattern do I see? Which record has an error? What would I do first? Your daily work is free practice material.
- **Read the question twice before answering.** Many cognitive questions turn on one word — "more than ten" versus "ten or more". Slow down on the wording; it takes two seconds and prevents the most common mistakes.
- **Rule things out.** When you are unsure, eliminate the options that contradict the given facts. Even removing one wrong option improves your odds, and often only one option survives.
- **Practise being timed.** Set a gentle timer — say 90 seconds a question — so the ticking clock feels familiar rather than frightening on the day.
- **Do the untimed practice questions the platform offers.** They exist so the interface holds no surprises. Use them to learn the buttons, not to judge yourself.
- **Sleep and setup matter.** Take the test rested, on a reliable connection, in a quiet spot, with notepaper if allowed. Frontline analysts know that environment affects performance — apply that knowledge to yourself.

### Common pitfalls to avoid

- **Assuming instead of deducing.** Adding facts the question never gave you — "the director probably matters more" — is the number one error. Work only from what is written.
- **Misreading thresholds and negatives.** "More than", "at least", "unless", "except" — these small words carry the logic. Underline them mentally.
- **Letting seniority override priority.** In prioritisation questions (and real queues), impact and urgency set the order, not job titles.
- **Escalating too early in problem-solving questions.** Options that skip the basic checks and jump straight to a resolver group are almost always wrong — just as they are on a real desk.
- **Rushing the easy questions.** Early questions are where careless errors cost most, because they are the marks everyone else gets. Bank them calmly.
- **Freezing when questions get harder.** On adaptive tests, harder questions mean you are doing well. Keep your method: read, extract facts, apply rules, eliminate, answer.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how confidently and accurately you work with the kinds of numbers your role genuinely handles. For an IT service analyst, that means ticket volumes, SLA percentages, resolution times, first-time fix rates, asset counts, and simple trends over weeks and months. You will not need advanced mathematics: the building blocks are percentages, averages, ratios, rates, and reading tables and simple charts. What the test really measures is whether you can pick the right numbers out of a table, do the right calculation with them, and sanity-check the result — all under gentle time pressure.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions. Each question usually shows a small table or chart plus a short scenario, then asks a multiple-choice question. Calculators are normally allowed (check your invitation email), and rough paper is your friend. Like the cognitive test, scoring compares you to a norm group, and some platforms adapt the difficulty as you go. Accuracy and speed are both recorded, so a steady, methodical pace beats a rushed one.

Why do employers test numeric reasoning for this role? Because numbers run through everything a service desk does. Your role summary says you resolve incident tickets "in a timely manner according to a service level agreement" — an SLA is a number with a promise attached. Your **IT service reporting** skill asks you to produce reports, interpret a data set, and communicate it to others. When a team leader asks "are we meeting the 95% target this week?", or a stakeholder asks "why did average resolution time go up?", the analyst who can read the data confidently gives better answers, spots problems earlier, and earns trust. Practising numeric reasoning is practising those conversations.

A reassurance before you begin: the arithmetic in these tests is deliberately simple. The challenge is care, not cleverness — reading the right row, using the right base for a percentage, and not being rushed into a slip. Every worked explanation below shows the arithmetic step by step, so you can follow the whole method and reuse it.

### How this assessment maps to your role

- **Reading tables and charts** maps directly to your **IT service reporting** skill: you produce relevant reports in an appropriate format and agreed timeframe, and you interpret a data set and communicate it to others. Most service desk reporting lives in tables — tickets by priority, breaches by week, volumes by category.
- **Percentages** map to SLA performance, the core measure of your day: percentage of tickets resolved within target, first-time fix percentage, percentage change in volumes. Your duty to work to an SLA makes percentage fluency essential.
- **Averages and rates** map to your **root cause analysis** duty and your **Business analysis (IT operations)** skill: investigating problems in existing processes often starts with "the average handle time rose" or "we get 12 lockouts a day" — and knowing what those figures do and do not prove.
- **Ratios and proportions** map to your **Asset and configuration management** skill: stock levels, spares per site, and assets per user are all ratios, and keeping them accurate protects components and budgets.
- **Trend reading** maps to your **User focus** skill — using quantitative data about users to turn user focus into outcomes — and to your **Strategic thinking** skill, because communicating how activities meet goals usually means showing a number moving in the right direction.
- **Communicating numbers clearly** maps to your **Stakeholder relationship management (IT operations)** skill: using evidence to explain decisions made is only possible when you have read the evidence correctly.

### Practice questions

**Question 1 (easy) — Percentage of tickets resolved within SLA**

Last week your desk closed 200 incident tickets. Of these, 178 were resolved within their SLA target. What percentage of tickets met the SLA?

- A) 82%
- B) 85%
- C) 89%
- D) 91%

**Correct answer: C**

**Explanation:** Percentage met = (tickets within SLA ÷ total tickets) × 100. Step 1: 178 ÷ 200 = 0.89. Step 2: 0.89 × 100 = 89%. A quick sanity check: 90% of 200 would be 180, and 178 is just below that, so "just under 90%" confirms 89%. This is the single most common calculation in service desk reporting — if your desk's target is 95%, you can immediately say the week fell 6 percentage points short, which is the kind of clear, evidence-based statement your **IT service reporting** skill calls for.

**Question 2 (easy) — Average tickets per day**

You logged the following numbers of tickets over five days: Monday 46, Tuesday 38, Wednesday 41, Thursday 35, Friday 50. What was the average (mean) number of tickets per day?

- A) 40
- B) 42
- C) 44
- D) 46

**Correct answer: B**

**Explanation:** Step 1: add the daily totals: 46 + 38 = 84; 84 + 41 = 125; 125 + 35 = 160; 160 + 50 = 210. Step 2: divide by the number of days: 210 ÷ 5 = 42. Sanity check: the values range from 35 to 50, and 42 sits comfortably inside that range — an average outside the range of the data always means a slip. Daily averages like this feed staffing conversations ("we take about 42 tickets a day, so each of six analysts handles about seven") and give you a baseline, so that a sudden 70-ticket day stands out as a possible incident cluster worth investigating.

**Question 3 (easy) — Reading a simple table**

The table shows open tickets by priority at 09:00 today.

| Priority | Open tickets | SLA target |
|---|---|---|
| P1 (critical) | 1 | 2 hours |
| P2 (high) | 6 | 4 hours |
| P3 (medium) | 28 | 2 days |
| P4 (low) | 45 | 5 days |

What fraction of all open tickets are Priority 3?

- A) 28/80
- B) 28/74
- C) 35/80
- D) 28/45

**Correct answer: A**

**Explanation:** Step 1: find the total of open tickets: 1 + 6 + 28 + 45 = 80. Step 2: the P3 count is 28, so the fraction is 28/80 (which simplifies to 7/20, or 35%). Option B forgets to include the P2 tickets in the total (1 + 28 + 45 = 74); option D compares P3 to P4 rather than to the whole; option C muddles the numerator. The technique to remember: a fraction or percentage always needs the right *base* — "out of what?" — and in queue reporting the base is usually the whole queue. Getting the base right is the difference between a report a stakeholder can trust and one that quietly misleads.

**Question 4 (easy) — Percentage change in ticket volume**

In June your desk received 1,200 tickets. In July it received 1,380. By what percentage did ticket volume increase from June to July?

- A) 12%
- B) 15%
- C) 18%
- D) 20%

**Correct answer: B**

**Explanation:** Percentage change = (difference ÷ original) × 100. Step 1: difference = 1,380 − 1,200 = 180. Step 2: divide by the *original* (June) figure: 180 ÷ 1,200 = 0.15. Step 3: 0.15 × 100 = 15%. The classic error is dividing by the new figure: 180 ÷ 1,380 ≈ 13%, which is why reading "from June to July" matters — the starting month is the base. A 15% monthly rise is exactly the kind of movement your reports should flag with a suggested cause to investigate (a new system rollout? seasonal leave patterns? a recurring fault?), turning a number into a useful conversation with stakeholders.

**Question 5 (moderate) — First-time fix rate comparison**

The desk's first-time fix (FTF) figures for two months:

| Month | Tickets closed | Fixed at first contact |
|---|---|---|
| September | 950 | 646 |
| October | 1,100 | 726 |

Which statement is correct?

- A) FTF rate improved from September to October
- B) FTF rate fell from 68% to 66%
- C) FTF rate stayed exactly the same
- D) FTF rate fell from 72% to 68%

**Correct answer: B**

**Explanation:** Work out each month's rate. September: 646 ÷ 950 = 0.68, so 68%. (Check: 68% of 950 = 0.68 × 950 = 646 ✓.) October: 726 ÷ 1,100 = 0.66, so 66%. (Check: 0.66 × 1,100 = 726 ✓.) The rate fell by two percentage points even though the *number* of first-time fixes rose from 646 to 726. That is the trap: option A is tempting because more tickets were fixed first time, but the desk also closed more tickets overall, and a rate compares like with like. This distinction — counts versus rates — comes up constantly in service reporting, and being able to explain it simply ("we fixed more, but we also received more") is a mark of an analyst who can interpret a data set and communicate it to others.

**Question 6 (moderate) — SLA breach deadline arithmetic**

A Priority 2 ticket has a 4-working-hour resolution target. Working hours are 08:00 to 16:00. The ticket was logged at 14:30 on Tuesday. By what time must it be resolved to meet the SLA?

- A) 18:30 Tuesday
- B) 09:30 Wednesday
- C) 10:30 Wednesday
- D) 12:30 Wednesday

**Correct answer: C**

**Explanation:** The clock only runs during working hours. Step 1: from 14:30 to 16:00 on Tuesday is 1.5 working hours, leaving 4 − 1.5 = 2.5 hours on the clock. Step 2: the clock restarts at 08:00 Wednesday. Step 3: 08:00 + 2.5 hours = 10:30 Wednesday. Option A wrongly runs the clock past the end of the working day; option B only adds 1.5 hours on Wednesday; option D adds the full 4 hours from 08:30. SLA clock arithmetic is bread and butter for an analyst working "in a timely manner according to a service level agreement" — knowing the real deadline tells you whether to keep working a ticket now or whether it can safely wait until morning, and prevents both needless panic and accidental breaches.

**Question 7 (moderate) — Asset stock ratio**

Your site standard says you must hold spare laptops in the ratio of 1 spare for every 25 staff. Your site has 450 staff and currently holds 14 spare laptops. Which statement is correct?

- A) The site meets the standard exactly
- B) The site is 4 spares short of the standard
- C) The site holds 4 more spares than the standard requires
- D) The site is 11 spares short of the standard

**Correct answer: B**

**Explanation:** Step 1: required spares = staff ÷ 25 = 450 ÷ 25 = 18. Step 2: compare with the actual holding: 18 required − 14 held = 4 short. So option B is correct. Option D likely comes from 25 − 14 = 11, a calculation that mixes up the ratio with a count. A quick estimation check: 450 ÷ 25 is the same as 45 ÷ 2.5 = 18 ✓. Ratio checks like this sit inside your **Asset and configuration management** skill — verifying stock against a standard, spotting the shortfall, and logging a replenishment request before the shortage bites during a busy week is exactly the "track, log and correct information" behaviour your role calls for.

**Question 8 (moderate) — Weighted workload across categories**

Yesterday you closed 20 tickets: 12 password resets averaging 6 minutes each, 5 software installs averaging 18 minutes each, and 3 hardware faults averaging 30 minutes each. What was the average time per ticket across all 20 tickets?

- A) 12.6 minutes
- B) 14.4 minutes
- C) 18.0 minutes
- D) 10.8 minutes

**Correct answer: A**

**Explanation:** You cannot just average 6, 18 and 30 (that gives 18, option C) because the categories have different volumes — you must weight by ticket count. Step 1: total time = (12 × 6) + (5 × 18) + (3 × 30) = 72 + 90 + 90 = 252 minutes. Step 2: divide by total tickets: 252 ÷ 20 = 12.6 minutes. Sanity check: most tickets were quick 6-minute resets, so the overall average should sit much closer to 6 than to 30 — 12.6 fits, 18 does not. Weighted averages matter whenever you summarise mixed work, and mis-averaging is one of the commonest reporting errors on any desk; being the analyst who gets it right protects the accuracy of the reports your stakeholders rely on.

**Question 9 (moderate) — Reading a trend for a report**

Monthly SLA achievement for the desk: March 96%, April 95%, May 93%, June 92%, July 90%. The target is 95%. Which sentence is the most accurate summary for your monthly report?

- A) "Performance is stable and consistently above target."
- B) "Performance has declined for four consecutive months and has been below the 95% target since May."
- C) "Performance collapsed in July after a strong June."
- D) "Performance varies randomly with no clear direction."

**Correct answer: B**

**Explanation:** Test each sentence against the data. The series falls every month — 96, 95, 93, 92, 90 — so "stable" (A) and "random" (D) are both wrong. Option C invents a story: June (92%) was already below target and the July fall of 2 points matches the general slide, so "collapsed after a strong June" misdescribes the shape. Option B states both facts that matter: a steady four-month decline, and below-target status starting in May (93% < 95%). Writing sentences that say exactly what the data shows — no more, no less — is the reporting half of your **IT service reporting** skill, and a steady decline is precisely the pattern that should trigger investigative work under your **Business analysis (IT operations)** skill, because gradual erosion usually has a systemic cause rather than a one-off explanation.

**Question 10 (hard) — Percentage of a percentage**

Last month the desk received 1,500 tickets. 40% of them related to the case management system. Of those case management tickets, 15% were escalated to the applications resolver group. How many case management tickets were escalated?

- A) 60
- B) 90
- C) 225
- D) 600

**Correct answer: B**

**Explanation:** Take it in two steps, keeping track of the base each time. Step 1: case management tickets = 40% of 1,500 = 0.40 × 1,500 = 600. Step 2: escalated = 15% of *those 600* = 0.15 × 600 = 90. Option D stops after step 1; option C wrongly takes 15% of 1,500; option A takes 10% of 600. The lesson is the same as in Question 3 but chained: every percentage needs its own base, and in multi-step questions the base changes as you go. In real reporting this pattern appears whenever you drill down — "of our incidents, how many were system X, and of those, how many breached?" — and getting the chain right is what makes a drill-down trustworthy.

**Question 11 (hard) — Estimating the impact of a prevention control**

Your desk receives 90 password-expiry lockout tickets per quarter, each taking an average of 10 minutes of analyst time. A proposed reminder improvement is expected to prevent 70% of these tickets. Roughly how much analyst time per quarter would the improvement save?

- A) About 6.3 hours
- B) About 10.5 hours
- C) About 9 hours
- D) About 15 hours

**Correct answer: B**

**Explanation:** Step 1: tickets prevented = 70% of 90 = 0.70 × 90 = 63 tickets. Step 2: time saved = 63 × 10 minutes = 630 minutes. Step 3: convert to hours: 630 ÷ 60 = 10.5 hours per quarter. Option C is the *remaining* tickets' time (27 × 10 = 270 minutes = 4.5 hours) miscounted, option D is the time for all 90 tickets, and option A halves the correct figure. This is the arithmetic behind your duty to **recommend procedures and controls for problem prevention**: a recommendation lands far better when it carries a quantified benefit ("this would free roughly ten and a half analyst-hours a quarter") because stakeholders can weigh it against the cost of making the change — evidence-based persuasion, exactly as your **Stakeholder relationship management (IT operations)** skill describes.

**Question 12 (hard) — Combining two tables**

Two extracts from this week's reporting:

Table 1 — tickets received by channel:

| Channel | Tickets |
|---|---|
| Phone | 240 |
| Email | 160 |
| Self-service portal | 100 |

Table 2 — percentage of each channel's tickets resolved within SLA:

| Channel | Within SLA |
|---|---|
| Phone | 95% |
| Email | 85% |
| Self-service portal | 92% |

How many tickets in total were resolved within SLA this week?

- A) 456
- B) 464
- C) 453
- D) 500

**Correct answer: A**

**Explanation:** Work channel by channel, then add. Step 1: phone = 95% of 240 = 0.95 × 240 = 228. Step 2: email = 85% of 160 = 0.85 × 160 = 136. Step 3: portal = 92% of 100 = 0.92 × 100 = 92. Step 4: total = 228 + 136 + 92 = 456. A common shortcut error is averaging the three percentages — (95 + 85 + 92) ÷ 3 ≈ 90.7% — and applying it to 500 tickets, giving about 453 (option C). That is wrong because the channels have different volumes: the busy phone channel deserves more weight than the smaller portal. Combining tables correctly, respecting volumes, is exactly what you do when you assemble a weekly report from several sources — and the overall figure you would report is 456 ÷ 500 = 91.2% within SLA, a number you can now defend line by line if a stakeholder asks how it was calculated.

### Preparation tips

- **Rebuild the basics until they are automatic.** Percentages, averages, and percentage change cover most questions. Practise each until you can do them without hesitating: (part ÷ whole) × 100; total ÷ count; (difference ÷ original) × 100.
- **Always ask "out of what?"** Before any percentage, name the base out loud in your head. Most numeric errors are base errors, not arithmetic errors.
- **Use real desk reports to practise.** Take last week's SLA report and recompute one or two figures yourself. If your numbers match the report, you have practised; if they do not, you have learned something either way.
- **Write down intermediate steps.** Even with a calculator, jotting "600 → 15% → 90" keeps the chain visible and catches slips instantly.
- **Estimate first, calculate second.** A rough answer ("just under 90%") tells you which precise answers are even plausible, and rescues you when a finger slips on the calculator.
- **Check the units.** Minutes versus hours, working hours versus clock hours, counts versus rates — half the hard questions turn on units, and so do half of real SLA disputes.
- **Keep a steady pace.** A minute of care per question beats thirty seconds of speed plus a wrong answer. Accuracy is scored; panic is not.

### Common pitfalls to avoid

- **Dividing by the wrong base.** Percentage change uses the *original* figure; a share of the queue uses the *whole* queue. Name the base every time.
- **Averaging percentages across different-sized groups.** As Question 12 showed, unweighted averages of rates mislead. Always go back to the counts.
- **Confusing counts with rates.** "More first-time fixes" and "a better first-time fix rate" can move in opposite directions. Say which one you mean.
- **Running SLA clocks through non-working hours.** Deadline arithmetic must respect the working day, exactly as your ticket tool does.
- **Stopping one step early.** Multi-step questions (percentage of a percentage) often offer the intermediate value as a wrong option. Re-read the question to confirm what is actually being asked.
- **Ignoring the sanity check.** An average outside the data's range, or a percentage over 100 where it should not be, is a flashing warning light. Two seconds of checking saves the mark.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and draw conclusions from written material — using the kinds of documents your role actually involves. For an IT service analyst, that means SLA definitions, service desk procedures, knowledge base articles, policy extracts, emails from users and stakeholders, and incident reports. The classic format shows you a short passage and then asks whether statements that follow are **True** (the passage supports them), **False** (the passage contradicts them), or **Cannot say** (the passage gives you too little information to decide either way). Other question styles include picking the best summary of a passage, identifying what can properly be inferred, and judging which version of a sentence communicates most clearly.

The typical format is an online, timed test lasting 15 to 25 minutes, with 20 to 30 statements spread across several passages. The golden rule is that you answer *only from the passage*, not from your own experience. This feels strange at first — you know a lot about IT services, and sometimes the passage will say less than you know, or even differ from how your desk does things. Set your knowledge aside and treat the passage as the whole world for the duration of the question.

Why do employers test verbal reasoning for this role? Because frontline support runs on precise reading and clear writing. Your role summary asks you to respond to and document incident tickets — documentation others will rely on. Your **Stakeholder relationship management (IT operations)** skill asks you to communicate clearly and regularly and to tailor communication to stakeholders' needs. Every shift, you read procedures and follow them exactly, read user emails and extract what actually happened, and write updates that a colleague — or the user — must understand first time. Misreading one clause of an SLA, or one step of a security procedure, has real consequences. The verbal test is a safe rehearsal of that daily precision.

A reassurance: this test does not measure vocabulary breadth or literary flair. It measures careful, honest reading — a skill you exercise constantly and can sharpen quickly with practice.

### How this assessment maps to your role

- **Comprehension of procedures and policies** maps to your duty to resolve tickets **according to a service level agreement** and to your **Service management framework knowledge** skill: a Level 3 service management qualification is largely about understanding defined processes precisely, and the test's passages mirror the process documents you follow.
- **True/False/Cannot say discipline** maps to your **root cause analysis** duty and your **Business analysis (IT operations)** skill: investigation means separating what the evidence establishes from what it merely suggests. "Cannot say" is the verbal test's version of "we need more data before we conclude".
- **Inference** maps to your work with users under your **User focus** skill: users rarely describe faults in technical terms, so you constantly infer the real issue from imperfect descriptions — while staying alert to the difference between a safe inference and a guess.
- **Clear-writing judgement** maps to your ticket documentation duty and your **IT service reporting** skill: producing reports in an appropriate format, and communicating an interpreted data set to others, both depend on choosing plain, unambiguous wording.
- **Reading stakeholder emails accurately** maps to your **Stakeholder relationship management (IT operations)** skill: identifying what a stakeholder actually asked for — rather than what you expected them to ask for — is the first step of tailoring communication to their needs.
- **Understanding strategic context in documents** maps to your **Strategic thinking** skill: working within a strategic context starts with reading strategy and policy extracts correctly, so you can explain how your daily activities support the wider goals.

### Practice questions

For Questions 1 to 5, read this passage, then answer each question using only the passage.

> **Extract from the Service Desk Operations Manual**
> All Priority 1 incidents must be escalated to the duty incident manager within 15 minutes of being logged. Priority 2 incidents must be escalated within one hour if no resolver group has accepted the ticket. Analysts may reclassify a ticket's priority only with the agreement of their team leader, except where the standard priority matrix clearly indicates a different priority, in which case the analyst may reclassify and must record the reason. The service desk operates from 08:00 to 18:00 on working days. Outside these hours, Priority 1 incidents are handled by the on-call team; all other tickets are queued for the next working day.

**Question 1 (easy) — True, False, or Cannot say**

Statement: "A Priority 1 incident logged at 10:00 on a working day must be escalated to the duty incident manager by 10:15."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage states that all Priority 1 incidents must be escalated to the duty incident manager within 15 minutes of being logged. A ticket logged at 10:00 on a working day (within desk hours) therefore has an escalation deadline of 10:15. The statement restates the rule with specific times, and the arithmetic (10:00 + 15 minutes = 10:15) is exact. This is a "True" because the passage directly supports every part of the statement — the right response when the text and the statement match cleanly. In your job, this is the same skill as reading an SLA clause and correctly stating the deadline it creates for a specific ticket.

**Question 2 (easy) — True, False, or Cannot say**

Statement: "Priority 2 incidents must always be escalated within one hour."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Check the exact wording of the passage: Priority 2 incidents must be escalated within one hour *if no resolver group has accepted the ticket*. The rule is conditional. The statement drops the condition and adds "always", turning a conditional rule into an absolute one — and the passage contradicts that absolute version, because a P2 ticket accepted by a resolver group within the hour needs no escalation. Words like "always", "never", "all" and "only" are signal flags in verbal tests: they often convert a true conditional into a false absolute. The same alertness protects you at work, where the difference between "escalate P2s after an hour" and "escalate unaccepted P2s after an hour" changes what you actually do at 60 minutes.

**Question 3 (moderate) — True, False, or Cannot say**

Statement: "Analysts are never permitted to change a ticket's priority on their own."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage gives a general rule (reclassification needs team leader agreement) *and an exception*: where the standard priority matrix clearly indicates a different priority, the analyst may reclassify alone, recording the reason. The statement says "never permitted... on their own", which the exception directly contradicts, so the answer is False. The trap is to stop reading at the general rule and mark True. Exceptions are where procedures earn their keep — and where misreading causes real incidents to be wrongly prioritised. Whenever a passage contains "except", "unless" or "other than", expect at least one statement testing whether you noticed.

**Question 4 (moderate) — True, False, or Cannot say**

Statement: "A Priority 3 ticket logged at 19:30 will be resolved on the next working day."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage says that outside desk hours, tickets other than Priority 1 are *queued* for the next working day. Queued is not resolved. The ticket will certainly wait until the next working day before anyone works on it, but whether it will actually be *resolved* that day depends on facts the passage does not give — its complexity, the queue length, its SLA target. The passage neither confirms nor contradicts the statement, so the honest answer is "Cannot say". This is the most important habit the verbal test teaches: noticing when a statement goes one step beyond the text. On the desk, the same habit stops you promising a user "it will be fixed tomorrow" when all you truly know is "it will be looked at tomorrow" — a distinction that protects trust.

**Question 5 (moderate) — Inference from the passage**

Which of the following can properly be inferred from the passage?

- A) The on-call team resolves Priority 1 incidents faster than the day service desk
- B) The organisation treats Priority 1 incidents as needing urgent human attention at any hour
- C) Team leaders dislike analysts reclassifying tickets
- D) The service desk is closed at weekends

**Correct answer: B**

**Explanation:** Test each option against the text. Option A compares speeds — the passage says nothing about resolution speed. Option C attributes feelings to team leaders — nothing in the text supports it. Option D is tempting: the desk operates "on working days", and weekends are usually not working days, but the passage never actually says weekends are excluded (some desks class Saturday as a working day), so D stretches beyond the text. Option B is a safe inference: P1s get a 15-minute escalation clock in hours and a dedicated on-call team out of hours — the only category handled by humans around the clock — which together show the organisation treats P1s as urgent at any hour. A proper inference is a conclusion the passage makes unavoidable, not merely plausible. That is the standard you should hold your own incident write-ups to as well.

For Questions 6 to 8, read this passage.

> **Email from the Facilities Programme Office**
> Subject: Desk moves — Building C, weeks 12 and 13
> The programme will relocate 120 staff from Building C to Building A in weeks 12 and 13. IT support requirements: each relocated member of staff will need their desktop equipment reconnected and tested at the new desk within one working day of their move. The programme office will supply the move schedule one week in advance. Please note that 30 of the staff use specialist accessibility equipment, which must be reconnected by a trained analyst. Network points in Building A have been tested, but floor 3 has six points still awaiting repair; staff allocated to those desks will need temporary Wi-Fi access until repairs are complete.

**Question 6 (easy) — Detail retrieval**

How many of the relocating staff use specialist accessibility equipment?

- A) 6
- B) 30
- C) 120
- D) The email does not say

**Correct answer: B**

**Explanation:** The email states directly: "30 of the staff use specialist accessibility equipment". Option A (6) is the number of faulty network points on floor 3 — a different fact from a nearby sentence, which is exactly how detail questions try to catch a skimming reader. Option C is the total number of relocating staff. The technique: when a question asks for a number, go back to the passage and put your finger on the exact sentence rather than trusting memory, because emails often contain several numbers close together. On the desk, the same habit — re-checking the source rather than recalling it — prevents mis-logged asset counts and wrong user details, which your **Asset and configuration management** skill exists to protect.

**Question 7 (moderate) — True, False, or Cannot say**

Statement: "All network points in Building A are working."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The email says network points in Building A "have been tested, but floor 3 has six points still awaiting repair". Six points awaiting repair are, by clear implication of the sentence, not currently working — that is why staff at those desks need temporary Wi-Fi. The statement claims *all* points are working, which the passage contradicts, so the answer is False. Notice the structure of the sentence: a reassuring first half ("have been tested") followed by a "but" that carries the important operational fact. In workplace emails, the qualification after "but" or "however" is often the part that creates work for you — train your eye to slow down there, because that is where this email tells you that six desks need a Wi-Fi workaround on day one.

**Question 8 (hard) — Best summary for action**

Your team leader asks you to summarise the email's IT actions in one sentence for the team huddle. Which is best?

- A) "Facilities are moving some people and we should keep an eye on it."
- B) "120 staff move from Building C to A over weeks 12–13; we reconnect and test each desk within one working day of each move, trained analysts must handle 30 accessibility setups, and six floor-3 desks need temporary Wi-Fi until their points are repaired."
- C) "There are network problems in Building A so the move will probably be delayed."
- D) "We need to reconnect 120 desks in week 12."

**Correct answer: B**

**Explanation:** A good operational summary preserves every fact a team must act on, and nothing else. Option B keeps all five action-bearing facts: the volume (120), the window (weeks 12–13), the SLA (one working day per desk), the constraint (30 accessibility setups need trained analysts), and the workaround (temporary Wi-Fi for six floor-3 desks). Option A is too vague to plan from. Option C invents a delay the email never mentions — summaries must not add conclusions. Option D drops the second week, the accessibility requirement and the Wi-Fi workaround, and compresses the timeline wrongly. Summarising is a core analyst skill: your ticket notes and handovers are summaries, and the test of a good one is that a colleague could act on it without reading the original. That is clear communication exactly as your **Stakeholder relationship management (IT operations)** skill describes it.

For Questions 9 to 11, read this passage.

> **Extract from the departmental IT policy**
> Users must not install unapproved software on departmental devices. Requests for new software must be submitted through the service catalogue and are assessed for security, licensing and cost. The assessment normally takes up to ten working days. Where software is needed urgently to meet a legal deadline, a director may sponsor an expedited assessment, which takes up to three working days. Approved software is added to the catalogue so that future requests can be fulfilled without a new assessment.

**Question 9 (moderate) — True, False, or Cannot say**

Statement: "A user who needs new software urgently for a legal deadline can always have it installed within three working days."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Trace what the policy actually promises. An expedited assessment (a) requires a director's sponsorship — not every urgent user will have that — and (b) takes up to three working days for the *assessment*, which may still end in rejection on security, licensing or cost grounds, and says nothing about installation time after approval. The statement's "always... installed within three working days" is contradicted twice: the route is conditional on sponsorship, and an assessment is not an installation, let alone a guaranteed approval. So the answer is False. This question rewards reading a process for what each stage actually delivers — precisely the skill you use when you set user expectations about a catalogue request, so you promise the process, not the outcome.

**Question 10 (moderate) — Purpose of a provision**

According to the passage, why is approved software added to the catalogue?

- A) So that future requests can be fulfilled without a new assessment
- B) To increase the department's software budget
- C) To make sure directors approve every installation
- D) The passage does not say

**Correct answer: A**

**Explanation:** The final sentence states the purpose explicitly: "Approved software is added to the catalogue so that future requests can be fulfilled without a new assessment." Option A restates it almost word for word. Options B and C are not in the passage at all — and C actually reverses the policy's logic, since the catalogue route exists so most requests need no senior involvement. When a question asks "why", look for purpose connectives in the text: "so that", "in order to", "because". Understanding *why* a process step exists, not just what it is, also makes you better at your job: an analyst who knows the catalogue's purpose can explain to an impatient user that requesting listed software is the fast path, turning a policy conversation into a helpful one — user focus in action.

**Question 11 (hard) — Clear-writing judgement**

You must update a user whose software request was rejected on licensing grounds. Which message is the clearest and most appropriate?

- A) "Per policy, your request has been declined pursuant to licensing assessment outcomes. Refer to the catalogue documentation."
- B) "Your software request was not approved. The licensing review found the product's licence doesn't permit use on departmental devices. You can ask us to look for an approved alternative in the catalogue — reply to this ticket and I'll help."
- C) "Request rejected."
- D) "Unfortunately the powers that be have said no to your software, sorry! Nothing I can do."

**Correct answer: B**

**Explanation:** Judge each message against three tests: is it accurate, is it plain, and does it help the user take a next step? Option B passes all three: it states the outcome, gives the specific reason in plain words, and offers a constructive route forward with a named action. Option A is accurate but wrapped in officialese ("pursuant to", "refer to the documentation") that pushes work onto the user. Option C is accurate but so bare it will generate a follow-up call — brevity is not clarity if it leaves obvious questions unanswered. Option D is friendly but unprofessional, vague about the reason, and wrongly closes the door ("nothing I can do") when an alternative route exists. Clear-writing questions reward the answer that serves the reader, which is exactly what "tailor communication to stakeholders' needs" means in your skill set.

**Question 12 (hard) — Combining two short texts**

Text 1, from the SLA: "Priority 3 incidents will be resolved within two working days."
Text 2, from a team briefing: "From Monday, all incidents affecting the payments team are to be logged as Priority 2 while the year-end payment run is in progress."

A payments team user reports a broken monitor on Tuesday, during the payment run. Based only on the two texts, which statement is true?

- A) The incident should be logged as Priority 3 because a monitor is minor
- B) The incident should be logged as Priority 2, so the two-working-day P3 target does not apply to it
- C) The incident cannot be logged until the payment run finishes
- D) The two texts contradict each other, so neither applies

**Correct answer: B**

**Explanation:** Combine the texts carefully. Text 2 creates a temporary rule: during the payment run, *all* incidents affecting the payments team are logged as Priority 2 — no exception for seemingly minor items, because the briefing's purpose is to protect a critical business period. So the monitor incident is P2, and the P3 target in Text 1 simply is not the applicable clause. Option A applies your general instinct instead of the stated rule — remember, answer from the texts. Option C invents a restriction neither text contains. Option D miscalls a contradiction: the texts operate at different levels (a standing SLA and a temporary override) and fit together without conflict. Reading multiple documents and working out which rule governs the case in front of you is daily life on a service desk, especially around freezes, major incidents and special business periods.

### Preparation tips

- **Practise the three-way discipline.** For a week, when you read a claim in an email or article, ask: does the source *support* it, *contradict* it, or *not say*? "Cannot say" is the option untrained readers use least and skilled readers use most.
- **Answer from the passage, not from your desk.** Your real-world knowledge is an asset at work and a hazard in the test. If the passage differs from how your organisation does things, the passage wins.
- **Slow down at signal words.** "Unless", "except", "only", "all", "normally", "but" — circle them mentally. Most wrong answers are born at these words.
- **Point at the sentence.** For detail questions, physically locate the supporting sentence before answering. Memory blurs numbers and conditions that sit close together.
- **Practise summarising.** After reading any procedure or email, try to restate its action points in one sentence. Compare against the original: did you keep every fact someone would need to act?
- **Read your own ticket notes critically.** Yesterday's notes are today's practice passage. Would a colleague reading them know exactly what happened and what is left to do?

### Common pitfalls to avoid

- **Marking "True" for things that are merely plausible.** Plausible is not supported. If you find yourself reasoning "well, usually...", the answer is probably "Cannot say".
- **Missing exceptions and conditions.** A rule with an "except" clause is two rules. Statements are frequently built to test the clause you skimmed.
- **Treating "queued" as "resolved", "assessed" as "approved".** Passages choose their verbs precisely; so should you. Substituting a stronger verb than the text used is a classic error — in tests and in promises to users.
- **Letting absolutes slip past.** "Always" and "never" convert conditional truths into false claims. Check every absolute against the text's qualifiers.
- **Adding your own conclusion to a summary.** A summary reports; it does not predict, judge, or explain beyond the source.
- **Rushing long passages.** Spending 40 seconds reading properly, then answering four statements quickly and correctly, beats skimming in 15 seconds and wobbling on all four.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (often called an SJT) presents realistic workplace scenarios and asks you to judge possible responses. Unlike the other three assessments, there is no arithmetic and no passage analysis: the question is always some version of "in this situation, what would be the most effective thing to do?" Common formats include choosing the most effective response, choosing the least effective response, ranking all the responses from best to worst, or rating each response on a scale from "counterproductive" to "highly effective". The scenarios in a job-specific SJT for your role are drawn straight from service desk life: an upset user, a ticket about to breach, a security worry, a colleague who needs help, a mistake you have made, a procedure that does not quite fit the situation.

The typical format is an online test of 15 to 30 scenarios, often untimed or generously timed, because it measures judgement rather than speed. There is usually no single "trick" answer: several responses may be reasonable, and scoring reflects how closely your judgements match those of experienced practitioners and the organisation's professional behaviours — things like user focus, ownership, collaboration, honesty when things go wrong, appropriate escalation, and inclusion.

Why do employers use SJTs for IT service analysts? Because the technical half of your job can be trained, but the judgement half — how you treat users, when you escalate, how you behave under pressure, whether you own a problem to the end — is what actually determines the user's experience of the service desk. Your role summary is full of judgement words: work independently, share information, assist others, own an issue until it is resolved or has a new owner, escalate "when appropriate". An SJT measures exactly those judgements in advance.

Two honest tips about how to approach SJTs. First, answer as your best professional self — the analyst you are on a good day, following your organisation's values — rather than trying to guess exotic "right answers". Second, notice that the worst options usually share features: they ignore the user, hide a problem, dodge ownership, break a security rule, or embarrass a colleague. Steering away from those features gets you most of the way to a strong score.

### How this assessment maps to your role

- **User-focused choices** map to your **User focus** skill — engaging with users, understanding their needs, and turning that focus into outcomes — and to your desk's core purpose of frontline support. Many scenarios test whether you keep the user informed and treated with respect while you fix the technology.
- **Ownership choices** map to your **Ownership and topic** skill: owning an issue until a new owner has been found or the problem has been mitigated or resolved. SJT scenarios love the moment when a ticket could quietly slip between teams — and reward the analyst who keeps hold of it.
- **Escalation choices** map to your duty to resolve problems "or, when appropriate, escalate or route them to IT resolver groups". Both extremes score badly: heroically struggling alone past the point of sense, and bouncing everything upward without doing the basics.
- **Collaboration choices** map to your duty to **work independently, share information and assist others with requests for service**, and to your **Stakeholder relationship management (IT operations)** skill: building consensus, communicating clearly and regularly, and improving relationships using evidence.
- **Process and improvement choices** map to your **Business analysis (IT operations)** skill and your duties to develop checklists and recommend prevention controls: scenarios where something keeps going wrong test whether you fix the instance *and* raise the pattern.
- **Integrity and security choices** map to your **Asset and configuration management** skill (protecting assets and information) and to the professional honesty every civil service role expects — especially scenarios about mistakes, shortcuts, and pressure to bend rules.

### Practice questions

**Question 1 (easy) — The frustrated user**

A user calls the desk. Their laptop crashed and they lost an hour's work on a report due this afternoon. They are audibly upset and say, "Your systems are useless." What is the most effective first response?

- A) Explain that crashes are usually caused by users running too many applications
- B) Acknowledge their frustration, reassure them you will help now, and start diagnosing while confirming the report deadline so you understand the urgency
- C) Tell them to log a ticket through the portal so it can be prioritised properly
- D) Apologise repeatedly for several minutes before beginning any technical questions

**Correct answer: B**

**Explanation:** The strongest response does two things at once: it treats the person and it starts on the problem. Acknowledging frustration ("I can hear this has come at the worst time — let's get you working again") costs seconds and defuses the emotion; confirming the deadline shows user focus and helps you judge urgency honestly. Option A opens by blaming the user — factually premature and relationally disastrous. Option C hides behind process: redirecting an upset caller to the portal when you could log the ticket yourself puts your convenience above their need. Option D means well but delays help; one sincere acknowledgement beats prolonged apologising. The professional behaviours being scored are user focus and ownership: the user's experience of "the useless system" is now your experience to repair.

**Question 2 (easy) — A ticket you cannot solve**

You have spent 25 minutes on a software fault you have never seen before. Your knowledge base has nothing, and your usual checks have not helped. The ticket's SLA allows four hours and one hour has passed. What is the most effective next step?

- A) Keep trying alone for the rest of the SLA period — asking for help looks weak
- B) Close the ticket and advise the user to restart their machine and log it again if it recurs
- C) Briefly summarise what you have tried, then ask an experienced colleague or route the ticket to the right resolver group with your findings attached
- D) Tell the user it is a known issue with no fix so they stop expecting a resolution

**Correct answer: C**

**Explanation:** Escalation "when appropriate" is a named part of your role, and this is what appropriate looks like: you have done the reasonable first-line checks, documented them, and hit the edge of your knowledge with plenty of SLA time left for the next person to succeed. Attaching your findings is the crucial detail — it saves the resolver group repeating your 25 minutes and shows ownership rather than offloading. Option A confuses persistence with professionalism and risks a breach. Option B is a disguised abandonment: closing an unresolved ticket to tidy the queue betrays the user and corrupts your desk's data. Option D is dishonest — inventing a "known issue" to manage expectations breaks trust permanently when discovered. The scored behaviours are ownership, honesty, and collaborative escalation.

**Question 3 (easy) — The colleague who is drowning**

It is a busy Monday. Your own queue is under control, but you notice a newer colleague has twice as many open tickets as anyone else and looks stressed. What is the most effective action?

- A) Say nothing — their queue is their responsibility, and helping might embarrass them
- B) Offer to take a few of their tickets, and quietly let the team leader know the workload split may need adjusting
- C) Tell the team group chat that your colleague is behind and someone should help
- D) Take over their whole queue so they can watch how you work

**Correct answer: B**

**Explanation:** Your role description says explicitly that you work independently, *share information and assist others*. Option B does both halves well: practical help now (taking a few tickets), plus a discreet flag to the person who can rebalance workload properly — because a lopsided queue on a Monday may be a rota or triage problem, not a personal failing. Option A rationalises inaction and lets users wait longer than they need to. Option C helps, but publicly, in a way that embarrasses the colleague; inclusion means offering support in a way people can accept with dignity. Option D swings too far — taking someone's entire queue undermines their development and your own SLAs. The scored behaviours are collaboration, inclusion, and thinking about the service as a team result rather than a personal scoreboard.

**Question 4 (moderate) — You made a mistake**

While clearing old records in the asset register, you realise you yesterday marked the wrong laptop as "disposed" — the record you deleted belonged to a device still in use by a member of staff. Nobody has noticed. What is the most effective action?

- A) Say nothing; it will probably never matter, and you can quietly fix it if someone asks
- B) Correct the record immediately, tell your team leader what happened, and check whether you made the same slip on any other records from that session
- C) Correct the record quietly and move on — informing anyone would just create fuss
- D) Report that the register "has some errors" without mentioning your involvement

**Correct answer: B**

**Explanation:** Three steps make this the model answer: fix the error, own it openly, and check the blast radius. Your **Asset and configuration management** skill is about tracking, logging and *correcting* information to protect assets — and an inaccurate register has real consequences, from security investigations that cannot find a device to a staff member's laptop being remotely wiped as "disposed". Telling your team leader matters because errors in shared data can propagate (reports, audits, refresh planning), and because a desk where people admit slips quickly is a desk that catches them cheaply. Checking the rest of yesterday's session shows root-cause thinking applied to yourself. Option A gambles the organisation's data integrity on luck; option C fixes the instance but hides the risk pattern; option D is the worst of both — vague enough to be useless, evasive enough to damage trust if traced. The scored behaviours are honesty, ownership, and proactive error checking.

**Question 5 (moderate) — Pressure to skip identity verification**

A caller says they are a senior manager locked out of their account before an important meeting. They are in a hurry, cannot remember the answers to the verification questions, and say, "Just unlock it — you can hear it's me, and I'll take responsibility." What is the most effective response?

- A) Unlock the account — a senior manager has accepted the responsibility
- B) Refuse abruptly and end the call, since the caller failed verification
- C) Politely explain you must verify identity for every account without exception, offer the alternative verification routes your procedure allows, and if none succeed, follow the failed-verification procedure while helping them find another way into their meeting
- D) Unlock the account but email the manager afterwards asking them to confirm it was really them

**Correct answer: C**

**Explanation:** Identity verification exists precisely for this moment: urgency plus seniority plus charm is exactly how social-engineering attacks work, and a genuine senior manager's account is exactly what an attacker most wants. Option C holds the line without hostility: it explains the rule applies to everyone (which genuinely senior people respect), exhausts the legitimate alternatives, and shows user focus by helping with the real underlying need — getting into the meeting, perhaps via a colleague or a temporary arrangement. Option A transfers a risk the caller has no right to accept on the organisation's behalf; "I'll take responsibility" does not survive a compromised account. Option D unlocks first and verifies after, which is verification theatre. Option B follows the rule but fails the person — brusqueness is not security. The scored behaviours are integrity under pressure, protecting assets, and courteous firmness.

**Question 6 (moderate) — The recurring fault**

For the third time this month, you have fixed the same user's application crash with the same workaround from the knowledge base. The workaround takes 20 minutes each time. What is the most effective action after this third fix?

- A) Keep applying the workaround whenever it recurs — it works, and that is what the knowledge base says to do
- B) Tell the user to stop using the application feature that triggers the crash
- C) Log or update a problem record noting the recurrence pattern, attach the three incident references, and suggest the resolver group investigate the root cause; meanwhile keep the workaround available
- D) Attempt to fix the application's code yourself since you know the fault well by now

**Correct answer: C**

**Explanation:** This scenario tests whether you can lift your eyes from incidents to problems. Three identical incidents for one user in a month is a pattern, and patterns are the raw material of your **root cause analysis** duty and your **Business analysis (IT operations)** skill — investigating problems in existing processes and contributing to recommending solutions. Option C does everything right: it creates the record that makes the pattern visible, evidences it with ticket references (so the resolver group starts from data, not anecdote), proposes the next step without overstepping, and keeps the user working meanwhile. Option A treats a chronic problem as an endless series of acute ones — 60 minutes spent this month, forever. Option B makes the user absorb the cost of a fault that is not theirs. Option D exceeds your access, your role, and change control. The scored behaviours are ownership beyond the single ticket, proactive problem prevention, and appropriate routing.

**Question 7 (moderate) — Competing demands at the deadline**

At 15:45 you are working a Priority 2 ticket due to breach at 16:30 — a caseworker's system is down. Your team leader messages: "Can you cover the phones for 30 minutes? Two analysts have gone home sick." Answering phones would mean pausing your P2 work. What is the most effective response?

- A) Silently ignore the message and keep working the P2 until it is resolved
- B) Reply immediately: explain you are on a P2 due to breach at 16:30, and ask whether they want you to hand it over to someone, finish it first, or cover the phones anyway — so the team leader can decide with the full picture
- C) Abandon the P2 and cover the phones — the team leader outranks the SLA
- D) Cover the phones and try to work the P2 between calls without telling anyone about the clash

**Correct answer: B**

**Explanation:** The core skill here is surfacing a conflict rather than resolving it silently and wrongly. Your team leader made a reasonable request without knowing you hold a near-breach P2; option B gives them that fact in one message and offers workable choices, which is exactly what "share information" and clear communication mean under pressure. It also respects the chain of accountability: the team leader is best placed to trade one risk against another once informed. Option A protects your ticket but leaves the phones — and your team leader — in the dark; ignoring a direct request damages trust even when your prioritisation instinct is right. Option C swaps a known, imminent user impact for phone cover without even mentioning the clash. Option D guarantees both tasks are done badly and hides the situation, which is the worst feature an SJT answer can have. Scored behaviours: transparent communication, prioritisation, and constructive escalation of conflicts.

**Question 8 (moderate) — The user who found their own workaround**

A user proudly tells you they solved their file-access problem by using a personal cloud storage account to move departmental documents between computers. The documents include citizens' personal information. What is the most effective response?

- A) Thank them for their initiative and close the ticket, since the problem is solved
- B) Explain calmly that personal cloud storage cannot be used for departmental data — especially citizens' information — help them remove the files from the personal account, restore a proper access route, and report the data-handling incident through the required channel
- C) Report them to their line manager for a security breach without discussing it with them
- D) Advise them to keep using the workaround but delete the files afterwards each time

**Correct answer: B**

**Explanation:** This scenario braids three duties: user focus, data protection, and honest process. The user acted in good faith to stay productive — so the tone is calm and blame-free — but citizens' personal data on a personal cloud account is a reportable data-handling incident in any government organisation, not a matter of discretion. Option B fixes the underlying access problem (removing the *reason* for the workaround), remediates the exposure, and makes the required report so the organisation can assess the risk properly; handled kindly, it also teaches the user why the rule exists. Option A rewards a serious breach because the symptom disappeared. Option C escalates punitively before helping, which teaches users to hide workarounds — the most dangerous culture a desk can create. Option D institutionalises the breach. Scored behaviours: protecting information assets, following mandatory reporting, and maintaining the relationship while correcting the behaviour.

**Question 9 (hard) — Least effective: the major incident rumour**

Multiple tickets are arriving about the case management system running slowly. You overhear that the infrastructure team is already "looking at something". A journalist-facing colleague in the press office calls you directly and asks, "Is the case system down? I need to know what to tell people." Which response is the LEAST effective?

- A) Tell them what you factually know: multiple slowness reports are logged, investigation is under way, and you will route their query to the incident communications lead for an authoritative statement
- B) Say you are not the right source for external statements and warmly hand them to the incident manager or communications lead
- C) Speculate helpfully: "It looks like the servers are overloaded again, probably the same crash as last month — I'd say it'll be down all afternoon"
- D) Take their contact details, check the incident record for the approved status summary, and call them back within ten minutes with that wording

**Correct answer: C**

**Explanation:** This is a least-effective format — you are hunting the worst option, and it is C. Speculation from a frontline analyst, delivered to someone whose job is to repeat statements externally, can become the department's public position within the hour: "probably the same crash as last month" and "down all afternoon" are guesses dressed as facts, and wrong guesses about government services erode public trust. Options A, B and D are all defensible: each sticks to known facts or routes the query to the accountable communication channel, differing only in style. Notice the SJT lesson: in least-effective questions, eliminate the responses that are honest, bounded, and correctly routed — what remains usually involves speculation, overreach, or secrecy. The workplace behaviours protected here are accurate information sharing, knowing the limits of your role, and supporting — not bypassing — incident communication governance.

**Question 10 (hard) — The accessibility request that is "not standard"**

A new starter with a visual impairment contacts the desk: the screen reader they rely on is not in the software catalogue, and their manager's request was auto-rejected as "non-standard software". They start their casework duties in three days. What is the most effective action?

- A) Explain that only catalogue software can be installed, and suggest they manage without it until the catalogue is updated at the next quarterly review
- B) Treat it as a priority: own the ticket, contact the software assessment team directly to explain the accessibility need and the three-day deadline, invoke your organisation's expedited or workplace-adjustment route if one exists, and keep the user and their manager informed daily
- C) Install the software from the vendor's website yourself, since accessibility is important enough to justify skipping assessment
- D) Advise the user to raise a complaint with HR, since accessibility is not an IT matter

**Correct answer: B**

**Explanation:** Accessibility needs are not "nice to have" requests: a screen reader is the difference between a colleague being able to do their job and not, and UK public sector organisations carry legal duties to make workplace adjustments. Option B shows what strong ownership looks like: you keep the ticket, you take the case *to* the assessment process rather than leaving the user stuck behind an auto-rejection, you use the legitimate fast route (most organisations have one for exactly this), and you communicate proactively so three days of uncertainty do not become three days of silence. Option A treats a process artefact (the quarterly review) as more important than a person's ability to work — the opposite of user focus and inclusion. Option C has the right heart and the wrong method: unassessed software may itself pose security risks, and skipping assessment sets a precedent that undermines the whole control. Option D wrongly bounces an IT-deliverable adjustment out of IT. Scored behaviours: inclusion, ownership, urgency calibrated to human impact, and working through — not around — governance.

**Question 11 (hard) — The tempting SLA shortcut**

It is the last day of the month. Your team leader mentions the desk is at 94.8% SLA achievement against a 95% target, and says, half-joking, "If a couple of those open tickets got closed today, we'd make it." You have two open tickets that are genuinely unresolved: the users are waiting on parts due next week. A colleague suggests closing them now and reopening them as "new" tickets tomorrow. What is the most effective response?

- A) Close and reopen the tickets as suggested — the target will be met and the users are no worse off
- B) Decline, and quietly leave the tickets as they are without comment
- C) Decline the close-and-reopen suggestion, keep the tickets honestly open with a clear "awaiting parts" status, and suggest to your team leader that the report note the two tickets pending parts — so the 94.8% is explained rather than massaged
- D) Ask the users to confirm their issues are "temporarily resolved" so the closures are technically justified

**Correct answer: C**

**Explanation:** This scenario tests integrity in reporting — the foundation of your **IT service reporting** skill, because a report only has value if the data underneath it is honest. Close-and-reopen laundering makes this month look better by making the data false and next month's data worse; once discovered (and patterns like month-end closure spikes are easy to spot), it poisons trust in every number the desk publishes. Option C refuses the fix but does something more useful: it converts the shortfall into information — "94.8%, with two tickets pending parts" is a report a stakeholder can act on, and using evidence to explain outcomes is literally in your **Stakeholder relationship management (IT operations)** skill. Option B protects your own integrity but ducks the conversation, leaving the pressure in place for someone else. Option D manipulates the users into providing cover, which is worse than doing it silently. Option A trades the desk's honesty for 0.2 of a percentage point. Scored behaviours: integrity, transparent reporting, and constructive challenge upward.

**Question 12 (hard) — Ranking responses: the quiet handover risk**

You are going on leave for two weeks from tomorrow evening. You own one complex ticket: an intermittent fault affecting a small team, with a resolver group engaged, a test planned for next week, and a user group anxious for updates. Rank these actions from most to least effective:

1. Write a full handover note in the ticket (history, current hypothesis, next steps, stakeholder expectations) and agree with a named colleague that they will own it, introducing them to the user contact.
2. Set an out-of-office message directing people to the service desk, and leave the ticket in your queue.
3. Mention the ticket verbally to a colleague at the end of your last day and assume they will pick it up.
4. Update the ticket with a note saying you are on leave and the next update will come in two weeks.

- A) 1, 3, 2, 4
- B) 1, 2, 3, 4
- C) 3, 1, 4, 2
- D) 1, 4, 2, 3

**Correct answer: A**

**Explanation:** Your **Ownership and topic** skill defines the standard exactly: own an issue *until a new owner has been found*. Action 1 is the complete version — documented context, a named and willing new owner, and a warm introduction to the stakeholders — so it ranks first in every good ordering. The real discrimination is among the weak options. Action 3 (verbal mention) is flawed but at least attempts a transfer of ownership to a person; things said at 5pm evaporate, but a colleague may follow up. Action 2 transfers nothing to anyone, though the out-of-office at least tells people where to go when they chase, so some safety net exists. Action 4 is worst: it actively tells an anxious user group that a live, intermittent fault will receive no attention for two weeks — freezing the ticket rather than handing it over, and turning your leave into their outage. So the order is 1, 3, 2, 4. The scored behaviours are ownership through transitions, communication that serves the user, and planning ahead — the difference between an analyst who is missed for two weeks and one whose tickets are.

### Preparation tips

- **Re-read your organisation's values and the GDAD behaviours before the test.** SJTs are scored against professional behaviours — user focus, ownership, collaboration, honesty, inclusion. Having the words fresh helps you recognise them inside the options.
- **Answer as your best professional self on a normal day.** Not a fantasy hero, not a rule-quoting robot — the analyst who helps the person, follows the procedure, and tells the truth.
- **Look for the option that does two things.** Strong answers usually pair action with communication: fix and inform, decline and offer an alternative, help now and flag the pattern.
- **In "least effective" questions, hunt for the poison features.** Hiding information, speculating, blaming, breaking security rules, abandoning ownership, embarrassing colleagues. The option with the most poison is your answer.
- **Rehearse with real memories.** Think of three tricky situations from your own desk experience. What did you do? What would the best version of that response have been? That reflection is exactly the muscle the SJT measures.
- **Do not overthink ranking questions.** Fix the best and worst options first; the middle usually orders itself by how much ownership and communication each option preserves.

### Common pitfalls to avoid

- **Choosing the technically fastest option over the humanly right one.** SJTs consistently reward treating the user well even when it costs a few minutes.
- **Escalating everything — or nothing.** Both patterns score poorly. The calibration is: do the reasonable first-line work, document it, then escalate with your findings.
- **Hiding mistakes or bad news.** Any option built on silence, delay, or vagueness about a problem is almost never the credited answer, because trust is the desk's real product.
- **Bending security or data rules for sympathetic reasons.** Urgency, seniority, and kindness are precisely the levers attackers pull. The credited answers hold the rule and help the person another way.
- **Punishing colleagues or users who got something wrong.** Correct the behaviour, protect the relationship, report what must be reported — without public blame.
- **Guessing what "they want to hear".** Second-guessing produces inconsistent answers. A consistent, values-based approach scores better and, more importantly, is who you want to be at work anyway.

## Conclusion

Well done — you have worked through a complete set of psychometric assessment practice materials built specifically for your role as an IT service analyst. That is no small thing, and it is worth pausing to notice what you have actually done.

You have practised cognitive reasoning with the real materials of your job: spotting ticket clusters, applying escalation rules exactly as written, checking asset records field by field, sequencing a busy morning, and reasoning from an incident timeline to a likely root cause. You have practised numeric reasoning with the numbers that run through every desk: SLA percentages, daily averages, first-time fix rates, breach deadlines, stock ratios, and the honest arithmetic behind a prevention recommendation. You have practised verbal reasoning with the documents you handle daily — procedures, policies, and stakeholder emails — and, most importantly, you have practised the discipline of saying "the text supports this", "the text contradicts this", or "the text does not say". And you have practised situational judgement across the moments that define a good analyst: the upset user, the mistake you own up to, the security rule you hold under pressure, the pattern you raise as a problem, and the ticket you hand over properly before your leave.

Notice the thread running through all four sections: careful attention plus honest reasoning plus genuine care for the user. Those are not test tricks. They are the working habits described in your own role summary — problem solving, root cause analysis, ownership, service focus, and clear communication with stakeholders — expressed one question at a time. Every hour you spend practising these assessments is also an hour spent becoming better at the job itself, and every shift on the desk is, in turn, practice for the assessments.

If you have an assessment coming up, a simple plan works best: revisit one section per day in the week beforehand, redo the questions you found hardest, and read the pitfalls lists the evening before. On the day, sleep well, set up a quiet space, use the practice questions the platform offers, and trust your method: read carefully, name the base, rule out the impossible, and choose the answer that helps the user and tells the truth.

And whatever the outcome, remember what these assessments are for: they are a mirror, not a judgement. They show you where your reasoning is already strong and where a little deliberate practice will pay off — knowledge you can fold straight into your development conversations and your growth toward the next level of the profession. You support users for a living; let this guide be something that supported you.

Good luck. You are better prepared than you were when you started — and that preparation shows.

