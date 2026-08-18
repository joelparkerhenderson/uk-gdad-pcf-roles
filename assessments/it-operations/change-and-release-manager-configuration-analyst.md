# Configuration Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a configuration analyst working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for your next post, measuring your own progress, or simply curious about how psychometric assessments relate to the work you do, this document will help you practise steadily and build real confidence.

Let's start with reassurance. Psychometric assessments can sound daunting, but they are simply structured, standardised exercises that measure the thinking skills and workplace judgement known to predict success in a role. Nobody gets every question right, and you are never compared against people far senior to you — your results are read against others at a similar level. Better still, everything in this guide is job-specific. You will not wrestle with abstract shape puzzles. Instead you will work with the materials you genuinely handle: configuration management database (CMDB) records, asset registers, discovery scan reports, change control procedures, audit findings, and requests from engineers and your change and release manager.

Why do these assessments matter for your role in particular? As a configuration analyst, you provide administrative support to the change and release manager, you help maintain the integrity of the CMDB, and you independently solve smaller problems. That is detail work with real consequences: an accurate CMDB is what lets incident responders find the right server at 2am, lets change assessors see what a change will really touch, and lets your organisation know what it owns, where it is, and what state it is in. The four assessment types in this guide measure exactly the capabilities that work depends on: cognitive ability (spotting the one record that contradicts the others), numerical reasoning (turning an audit sample into an accuracy percentage), verbal reasoning (reading a data standard or a disposal procedure precisely), and situational judgement (deciding what to do when someone asks you to "just tweak a record" without a change reference).

This document is organised into four main assessment sections, one per assessment type. Each follows the same friendly pattern: an overview of what the assessment measures and how it usually runs, a mapping of the assessment to the specific skills named in your role, a substantial set of practice questions with fully worked explanations, practical preparation tips, and common pitfalls to avoid. Questions start easy and build gradually, so you can warm up before you stretch.

Here is how to get the most from the guide. First, read each "About this assessment" section so the format holds no surprises on the day. Second, attempt every practice question honestly — commit to an answer before reading the explanation. Third, treat each explanation as a mini-lesson: even when you answered correctly, the walkthrough will deepen your technique and show you how the same skill appears in your daily work. Fourth, go at a sustainable pace. Short, regular practice sessions beat one long cram, and calm familiarity is what actually improves scores.

One final thought before you begin: the care and precision that drew you to configuration work are exactly the qualities these assessments reward. You already practise them every time you verify an asset or correct a record. This guide simply helps you show those qualities under test conditions. Find a quiet spot, take a breath, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the mental processes your role actually demands, using practical workplace scenarios rather than abstract puzzles. For you, that means questions built from CMDB records, asset registers, naming conventions, dependency maps, discovery scans, and the procedures that govern how records may be created, changed, and retired.

The typical format is an online, timed test of 15 to 30 minutes with 15 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, against a norm group at your level. Many platforms are adaptive: questions get slightly harder as you answer well, so a test that feels stretching is usually a test going well. Employers typically see accuracy and speed separately, and almost every platform offers ungraded warm-up questions first — always take them; they settle the nerves for free.

Why do employers use cognitive assessments for a configuration analyst? Because your professional value is exactness at scale. A CMDB holds thousands of records, and its usefulness depends on consistency you can only maintain by noticing small things: a naming convention broken in one entry, a status field that contradicts a relationship, a server that appears in the register but not in the scan. You also reason with structure — if the payroll application depends on a database which depends on a server, then a change to that server touches payroll, whether or not anyone says so out loud. And because you independently solve smaller problems, you regularly decompose a puzzle — a sync job that keeps failing, a count that will not reconcile — into causes you can check one by one. A good cognitive assessment is a miniature of precisely this work, which is why practising for it genuinely makes you better at the job.

A reassurance about timing: these tests are designed so most people do not finish. Steady accuracy beats hurried coverage nearly every time. Work carefully, keep moving, and let the speed come with practice.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Asset and configuration management** skill: maintaining secure configuration and accurate information means recognising conventions — naming patterns, status lifecycles, record structures — and instantly noticing the entry that breaks them. It is also how duplicates and ghost records get caught.
- **Logical deduction** maps to your **Change management** skill: applying change control procedures under supervision means reasoning from rules to consequences — if the procedure requires a change reference for every edit, and this edit has none, what follows? It also underpins dependency reasoning across the CMDB's relationship data.
- **Error checking** maps to your core duty of helping to maintain the integrity of the CMDB, and to **Asset and configuration management** (verifying the location and state of IT assets): reconciling records against scans, licences against installations, and registers against reality is the beating heart of your role.
- **Prioritisation** maps to your **Incident management** skill (identifying and registering incidents and allocating them to the appropriate channel) and your **Ownership and topic** skill (knowing which problems to handle and which to pass to your team): support roles live or die by choosing the right next task.
- **Applied problem solving** maps to your **Problem management** skill and to your role's distinctive phrase "independently solving smaller problems": investigating why a record, a job, or a count is wrong — and understanding whether the problem is operational, tactical, or strategic — is structured detective work, and the assessment rehearses it in miniature.

### Practice questions

**Question 1 (easy) — Pattern recognition in configuration item names**

Your CMDB naming standard for server configuration items is: three-letter site code, hyphen, three-letter platform code, hyphen, three-digit number — for example, "LDS-WIN-014" for a Windows server in Leeds. While tidying the register you see these entries:

1. LDS-WIN-015
2. MAN-LNX-002
3. LDS-WIN-16
4. NCL-LNX-101
5. MAN-WIN-033

Which entry breaks the naming standard?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: B**

**Explanation:** Check each entry against the three parts of the rule: three-letter site code, three-letter platform code, three-digit number. Entries 1, 2, 4 and 5 all fit. Entry 3, "LDS-WIN-16", has only a two-digit number — it should read "LDS-WIN-016". The missing leading zero looks trivial, but in a real CMDB it matters: sorted lists misorder, automated matching against other systems fails, and someone may later create "LDS-WIN-016" as a duplicate of the same machine. Consistency checking of exactly this kind is your bread and butter as the person maintaining accurate configuration information. In the test, restate the rule in your own words first, then check each option mechanically against it — do not just scan for what "looks odd", because well-formed oddities (like the three-digit "101" in entry 4) are placed there to distract you.

**Question 2 (easy) — Logical deduction from an access rule**

Your CMDB procedure states: "Records may only be edited by staff who have completed the data standards training, and every edit must reference an approved change or an approved data correction request." You see in the audit log that a colleague, Priya, edited a server record yesterday, and the edit references an approved data correction request. Which one of the following conclusions must be true?

- A) Priya has completed the data standards training.
- B) Priya's edit complied with the procedure in full — if she has completed the data standards training.
- C) The edit was authorised by the change and release manager personally.
- D) Priya is a configuration analyst.

**Correct answer: B**

**Explanation:** The procedure imposes two conditions: trained editor, and a valid reference. The audit log confirms the second condition (an approved data correction request) but tells you nothing about the first. So option A is not guaranteed — the log shows the edit happened, not that it was permitted; untrained staff editing records is precisely the kind of breach audits look for. Option B is the careful conclusion: the edit satisfied the reference requirement, so full compliance now turns only on the training condition, which is exactly what B says. Option C invents an authoriser the procedure never mentions — data correction requests are approved, but not necessarily by the manager personally. Option D guesses at Priya's job from no evidence. The discipline here — conclude only what the evidence guarantees, and name the condition still unverified — is exactly how you should read audit logs at work: one confirmed condition is not the same as compliance.

**Question 3 (easy) — Error checking within a single record**

You are reviewing a CMDB record before an audit:

- Name: LDS-WIN-021
- Status: Decommissioned
- Decommission date: 12 March
- Location: Leeds data centre, rack B4
- Relationships: "hosts — Payroll application (Live)"
- Last verified: 3 January

What is the most significant inconsistency in this record?

- A) The last verified date is before the decommission date.
- B) A decommissioned server is still recorded as hosting a live application.
- C) The location field should be blank for a decommissioned server.
- D) The name does not match the naming standard.

**Correct answer: B**

**Explanation:** Read the fields as claims about the world and ask whether they can all be true together. A server decommissioned on 12 March cannot currently be hosting a live payroll application — one of those statements is wrong, and the contradiction is dangerous in both directions: either payroll is really running on a machine everyone believes is switched off, or the relationship is stale and an incident responder chasing a payroll fault will waste time on a dead server. Option A is not an inconsistency at all — verification naturally happened before decommissioning; the date being months old is a mild staleness note, nothing more. Option C is wrong because decommissioned assets still have locations until physically disposed of — knowing where retired kit sits is part of verifying the location and state of IT assets. Option D is false: the name fits the standard from Question 1. The skill being tested — and the skill your audits depend on — is cross-field consistency checking: not "is each field plausible alone?" but "can these fields all be true of the same asset at the same time?"

**Question 4 (moderate) — Prioritisation on a busy morning**

It is 9:00 on Thursday morning. Four items are waiting for you:

1. Your change and release manager has asked for the configuration records for tomorrow's change advisory board papers by midday.
2. An engineer has emailed: their team cannot find the record for a network switch they need to modify tonight under an approved change, and they think the record may be missing.
3. The weekly discovery scan report arrived overnight showing 30 new unreconciled discrepancies — the routine review you normally do on Thursdays.
4. A colleague mentions in passing that the printers on floor 2 are offline; no ticket exists.

Which sequencing is most defensible?

- A) 1, 2, 4, 3
- B) 4, 2, 1, 3
- C) 2, 4, 1, 3
- D) 3, 1, 2, 4

**Correct answer: C**

**Correct sequencing explained.**

**Explanation:** Weigh urgency and impact together, and notice which items are quick. Item 2 blocks an approved change happening tonight — if the switch's record is genuinely missing, the change assessment is working blind, and finding or creating the record takes investigation time you cannot leave until afternoon. It is both urgent and squarely your CMDB-integrity duty, so it leads. Item 4 takes two minutes: you identify and register the incident and allocate it to the appropriate channel — printers offline affects users right now, but your part is routing, not repair, so do that small unblocking action next. Item 1 has a hard midday deadline and supports your manager's governance duties — start it with the morning still ahead. Item 3 is genuinely important but routine and unscheduled beyond "Thursday"; it absorbs whatever time remains. Option A delays the tonight-blocking record hunt behind a midday task; option B puts a two-minute routing job ahead of a time-critical investigation, which is defensible only if you notice it is two minutes — but it then also defers the investigation behind nothing else, so C still dominates; option D puts routine reconciliation first purely because it arrived first. The pattern to remember: quick actions that unblock others slot in early, hard deadlines get protected, and routine work flexes around both.

**Question 5 (moderate) — Deduction across dependency relationships**

The CMDB records these relationships: the HR portal depends on the identity service and on database DB-HR. Database DB-HR runs on server LDS-LNX-007. The identity service runs on servers LDS-LNX-001 and LDS-LNX-002, and stays available as long as at least one of its two servers is running. Tonight's approved change will take LDS-LNX-007 and LDS-LNX-002 offline simultaneously for patching. Assuming the records are accurate, what is the impact on the HR portal during the patching window?

- A) No impact — the identity service stays available on LDS-LNX-001.
- B) The HR portal will be unavailable, because DB-HR will be offline.
- C) The HR portal will be unavailable, because the identity service will be offline.
- D) Cannot be determined from the records.

**Correct answer: B**

**Explanation:** Trace each dependency separately. Identity service: it needs at least one of LDS-LNX-001 and LDS-LNX-002; the change takes only LDS-LNX-002 offline, so the identity service survives on LDS-LNX-001 — which rules out C. Database DB-HR: it runs on LDS-LNX-007, which the change takes offline, so DB-HR goes down with it. The HR portal depends on both the identity service and DB-HR; losing either breaks it. So the portal is unavailable during the window, and the cause is the database — answer B. Option A checks only the redundant dependency and forgets the single-point one; that is the classic error in impact assessment, because redundancy in one branch feels like safety everywhere. Option D underrates the records: the question says they are accurate, and they contain everything needed. This is exactly why your CMDB relationship data matters — the change was approved for two servers, but its real impact statement should have said "HR portal outage". When you keep relationships current, you are the person who makes that impact visible before the change advisory board, rather than after the service desk phones start ringing.

**Question 6 (moderate) — Error checking licences against installations**

The software register says your organisation holds 80 licences for a diagram tool. The quarterly installation scan reports the tool installed on 84 machines. Before flagging a licence shortfall, you check the details and find: 3 of the 84 machines are marked "rebuilt — awaiting software removal verification", and 2 of the 84 are in the training suite, where the supplier's contract allows unlicensed classroom use. Based on this, what is the most accurate current position?

- A) A shortfall of 4 licences — 84 installations against 80 licences.
- B) No shortfall — the exceptions cover the gap.
- C) A possible shortfall of up to 2 licences: 79 countable installations are confirmed against 80 licences, but the 3 unverified rebuilds could raise the count to 82.
- D) A shortfall of 2 licences.

**Correct answer: C**

**Explanation:** Work the numbers with their statuses, not just their totals. Start at 84 detected installations. The 2 training-suite machines are contractually exempt, so they never count: 84 − 2 = 82 potentially countable. The 3 rebuilt machines are awaiting verification that the software was removed — they might each still have it (count) or not (do not count), so the countable figure sits between 79 (if all three are clean) and 82 (if none are). Against 80 licences, that range means anything from 1 licence spare to 2 short. Option C states exactly this: confirmed position 79 against 80, with an unverified band that could produce a shortfall of up to 2. Option A ignores both exception categories; option B asserts safety the unverified machines cannot yet guarantee; option D asserts a definite shortfall that is equally unproven. The professional lesson mirrors the arithmetic: your next action is not a compliance alarm or a shrug — it is to verify the state of those 3 assets, which is your named skill, and which collapses the uncertainty to a single true number. Precise error checking often ends not in an answer but in exactly the right question.

**Question 7 (moderate) — Pattern recognition in duplicate records**

Reviewing possible duplicate laptop records, you find four suspect pairs. For each pair, the two records show:

- Pair 1: same serial number, same user, names "LT-4471" and "LT-4471a"
- Pair 2: same serial number, different users, one marked "In use", one marked "In store"
- Pair 3: different serial numbers, same user, same model
- Pair 4: same serial number, same name, identical in every field

Which pair is most likely NOT a duplicate — that is, most likely to represent two genuinely different assets?

- A) Pair 1
- B) Pair 2
- C) Pair 3
- D) Pair 4

**Correct answer: C**

**Explanation:** The strongest identity evidence for hardware is the serial number, because manufacturers assign it uniquely to a physical machine. Pairs 1, 2 and 4 all share a serial number, so each pair almost certainly describes one physical laptop recorded twice: pair 4 is a pure duplicate (identical fields), pair 1 is a duplicate with a name-mangling history ("a" suffixes usually betray a failed merge or re-import), and pair 2 is a duplicate where the two records have drifted apart — the most dangerous kind, because each looks internally plausible and they disagree about who has the machine and where it is. Pair 3, by contrast, has different serial numbers: one person holding two laptops of the same model is entirely ordinary (a replacement not yet returned, a loaner, a specialist build). So pair 3 is most likely two real assets — answer C. The transferable technique: when hunting duplicates, anchor on the field with the strongest claim to uniqueness, and treat matching weak fields (user, model, name) as suggestive only. And note the follow-up your role would demand: pair 2's drift means physically verifying that laptop's location and holder before merging the records — merge first, verify second is how CMDBs quietly enshrine a guess.

**Question 8 (moderate) — Independently solving a smaller problem**

Every night, an automated job syncs new records from the procurement system into the CMDB. The job has failed with a "row rejected" error on three of the last five nights. Checking the logs, you find each failure rejected exactly one row, and each rejected row was a purchase from the same new supplier, whose product descriptions include an unusual special character. Rows from all other suppliers load cleanly, including on the nights the job "failed". As the person who noticed, what is the best characterisation and next step?

- A) A random intermittent fault — re-run the failed rows and monitor.
- B) A systematic data-format problem with one supplier's descriptions — reproduce it with one rejected row, then raise a specific fix (handle or cleanse the character), noting that other suppliers are unaffected.
- C) A major CMDB integrity failure — escalate to the change and release manager as urgent before doing anything.
- D) A procurement-system fault — pass the whole issue to the procurement team.

**Correct answer: B**

**Explanation:** Test each characterisation against the evidence. Random? No — the failures correlate perfectly with one supplier and one data feature (the special character), and everything else loads even on failure nights. That correlation is the signature of a systematic, narrow cause, which is also why C over-reads it: the blast radius is one row per night from one supplier, contained and understood — worth recording and mentioning, not an urgent escalation. D gives the problem away prematurely: the rows may be perfectly valid data that your sync job handles badly, in which case the fix belongs on your side; you cannot know until you reproduce it. Option B is the shape of independent problem solving your role names: form a hypothesis from the pattern, confirm it cheaply (one row, one test), then raise a precise, evidenced fix — and its size fits your remit, "independently solving smaller problems", exactly. Notice also the problem-management framing from your skills list: this is an operational-level problem with a clear preventative measure (handle the character once, and every future supplier with quirky descriptions loads cleanly). Small, well-evidenced fixes like this are how a configuration analyst quietly makes the whole data pipeline sturdier.

**Question 9 (challenging) — Multi-constraint scheduling of verification visits**

You must physically verify assets at four sites — Leeds (L), Manchester (M), Newcastle (N), and Sheffield (S) — one site per day, Monday to Thursday. Constraints: (i) the Newcastle server room is only accessible on Tuesday and Wednesday; (ii) the same security escort accompanies you at Leeds and Sheffield, must complete the Leeds visit first, and needs at least one clear day between the two visits to process the Leeds access paperwork that Sheffield's site requires; (iii) Manchester must be visited before Sheffield, because Sheffield's check needs a barcode scanner that is currently in Manchester and travels back with you; (iv) Monday cannot be Leeds, because Leeds access passes are only issued from Monday afternoon. On which day must you visit Sheffield?

- A) Monday
- B) Tuesday
- C) Wednesday
- D) Thursday

**Correct answer: D**

**Explanation:** Eliminate day by day, starting with Monday. Monday cannot be Leeds (iv), cannot be Newcastle (i), and cannot be Sheffield — Sheffield needs both Manchester (iii) and Leeds (ii) completed before it, which is impossible on the first day. So Monday must be Manchester. That leaves Tuesday, Wednesday and Thursday for Leeds, Newcastle and Sheffield. Now apply constraint (ii): Leeds comes before Sheffield with at least one clear day between them. Among the three remaining days, the only pair with a whole clear day between them is Tuesday and Thursday — Tuesday and Wednesday are adjacent, and so are Wednesday and Thursday. Therefore Leeds is Tuesday and Sheffield is Thursday, leaving Newcastle on Wednesday, comfortably inside its Tuesday-or-Wednesday access window. Check the finished schedule against every rule: Manchester Monday (before Sheffield — iii satisfied, with the barcode scanner travelling back with you Monday evening, available well before Thursday); Leeds Tuesday (passes were issued Monday afternoon — iv satisfied); Newcastle Wednesday (i satisfied); Sheffield Thursday, with Wednesday clear between the escort's two visits (ii satisfied). No other arrangement survives the elimination, so Sheffield must be Thursday. The technique to carry away: fix the most constrained slot first — Monday, where three of the four sites were impossible — and then let each placement shrink the remaining choices until only one arrangement is left. Real verification tours produce exactly these puzzles, with escort bookings, access windows, and shared equipment as the constraints, and solving them on paper before you travel is considerably cheaper than discovering a conflict in a car park in Sheffield with the scanner eighty miles away.

**Question 10 (challenging) — Deduction: which record must be wrong?**

Three sources describe the same four servers. The CMDB says: A is Live, B is Live, C is Decommissioned, D is Live. The monitoring system, which can only see powered-on servers, currently reports data from A, C, and D. The data centre's physical log, updated this morning and considered reliable, records that exactly three of the four servers are powered on and racked, and that B was physically removed last week. Assuming the physical log is correct and monitoring is working normally, which CMDB record must be wrong?

- A) Only B's record
- B) Only C's record
- C) Both B's and C's records
- D) The records are consistent with the evidence.

**Correct answer: C**

**Explanation:** Use the reliable source as the anchor. The physical log says B was removed last week — so the CMDB's "B is Live" must be wrong: a removed server is not live. That alone eliminates options B and D. Now check C: the CMDB says C is Decommissioned, but monitoring — which can only see powered-on servers — is currently receiving data from C. A decommissioned server should not be powered on and reporting; since monitoring is working normally, C is running, so "Decommissioned" must also be wrong (or at the very least, the status does not reflect the machine's actual state, which is precisely what a status field exists to do). The physical log corroborates: exactly three servers are powered on, and monitoring sees A, C, D — a consistent trio that includes C. So both B's and C's records are wrong: answer C. Records for A and D agree with all the evidence. The method — anchor on the most reliable source, then test each record against every independent signal — is exactly how you reconcile the CMDB against discovery scans and physical audits in real life. And the two failure directions here are worth naming: B is a ghost record (the CMDB believes in a server the world no longer has), while C is the reverse (the world has a running server the CMDB has written off). The second kind is usually more dangerous: unmanaged running kit receives no patches, no monitoring attention by policy, and no change control.

**Question 11 (challenging) — Following a branching retirement procedure**

Your asset retirement procedure states: "On receiving an approved retirement request: set the asset's status to 'Pending disposal'. If the asset stores data, it must be securely wiped and a wipe certificate attached to the record before collection may be booked. If the asset is leased, notify the leasing coordinator, who arranges return instead of disposal collection. Only when either a disposal collection is completed or a lease return is confirmed may the status be set to 'Retired', and the record must retain its history rather than being deleted." You receive an approved retirement request for a leased laptop with a hard drive. The drive has been securely wiped and the certificate is attached. What is the correct next step?

- A) Book a disposal collection, then set the status to Retired when collection completes.
- B) Notify the leasing coordinator and await confirmed lease return before setting the status to Retired.
- C) Set the status to Retired now — the wipe certificate is attached, which was the blocking condition.
- D) Delete the record once the wipe certificate is attached, since the asset is leaving the organisation.

**Correct answer: B**

**Explanation:** Walk the branches with this asset's attributes: it stores data (hard drive) and it is leased. The data branch required a secure wipe and certificate before collection could be booked — done. But the lease branch redirects the exit route entirely: leased assets go back to the lessor via the leasing coordinator, and the procedure's closing condition says Retired status requires either a completed disposal collection or a confirmed lease return. For a leased asset, only the second route applies. So the next step is notifying the leasing coordinator, and Retired waits for the confirmed return — option B. Option A books the wrong exit route: disposing of a leased laptop your organisation does not own would create a contractual mess the lease branch exists to prevent. Option C mistakes a completed precondition for a completed process — the wipe unblocked the journey; it did not finish it, and marking Retired now would make the CMDB claim an ending that has not happened. Option D violates the explicit instruction to retain history, and deleting records is the cardinal sin of configuration management: the audit trail is the point. Reading procedures attribute-by-attribute — which branches does this asset trigger, and what does each require — is precisely the skill of applying change control procedures under supervision, and it is what keeps the CMDB truthful at the untidy edges of an asset's life.

**Question 12 (challenging) — Reconciling three sources under a deadline**

An external audit starts Monday. On Friday afternoon you reconcile the count of live Windows servers across three sources: the CMDB says 120, the discovery scan says 116, and the licensing report generated from the CMDB last month says 124. You have two hours. Investigating the CMDB-versus-scan gap of 4, you quickly confirm: 2 servers were decommissioned this week but their CMDB status was not yet updated, and 2 sit on an isolated network segment the scanner cannot reach. What is the strongest position to take into Monday's audit?

- A) Report 116 as the true figure, since the scan measures reality directly.
- B) Report that the sources conflict and the count is unknowable before Monday.
- C) Correct the 2 stale CMDB records to give a reconciled current figure of 118 — the scan's 116 plus the 2 verified unscannable servers — and explain the licensing report's 124 as last month's snapshot, which predates this week's decommissions and reflects the register as it stood.
- D) Adjust the CMDB to 116 to match the scan exactly, so all current sources agree before the auditors arrive.

**Correct answer: C**

**Explanation:** A reconciliation is finished when every difference is explained, not when the numbers are forced to match. Work the arithmetic: the scan sees 116; it cannot see the isolated segment, whose 2 servers you have verified exist and are live, so reality is 116 + 2 = 118. The CMDB's 120 exceeds that by exactly the 2 servers decommissioned this week whose statuses lag — correct those records (squarely your job, with the decommissions as the authorising events) and the CMDB reads 118 too. The licensing report's 124 needs explaining, not fixing: it is a snapshot from last month, when more servers were live; a dated snapshot disagreeing with today is a timeline, not a contradiction — though the 124 versus 120 gap also tells you roughly 4 servers were retired between the snapshot and this week, which you can evidence from decommission records if asked. Option A worships the scanner and would understate the estate by the 2 unscannable servers — exactly the sort of gap auditors probe. Option B surrenders with the answer two corrections away. Option D is the worst: editing the CMDB to match a source you know is blind makes the sources agree by making one of them wrong — cosmetic consistency over truth, and a breach of the integrity you exist to maintain. The audit-ready position is C's shape: one reconciled figure, every source's deviation explained, and the corrections made through proper process. Auditors are rarely troubled by differences; they are troubled by unexplained differences.

### Preparation tips

- **Practise on your own CMDB.** Ten minutes with a filtered record list — hunting broken conventions, contradictory fields, or stale statuses — is ideal training, and it improves the database while it improves you.
- **Restate the rule before checking options.** For pattern and procedure questions, put the rule in your own words first, then test each option against it mechanically. Rules beat instincts.
- **Anchor on the strongest evidence.** In reconciliation questions, decide which source is most reliable (a physical log, a serial number) and test everything else against it, rather than averaging your way to confusion.
- **Check fields against each other, not just alone.** Cross-field contradictions — decommissioned yet hosting, removed yet live — are the heart of integrity checking. Ask: can all these claims be true of one asset at once?
- **Draw the dependencies.** For impact and scheduling questions, sketch the servers, services, and days on scrap paper. Externalising the structure frees your head for the reasoning.
- **Time-box hard questions.** If a multi-constraint puzzle resists you after ninety seconds, mark your best answer and move on. Steady accuracy across the whole test beats heroics on one question.
- **Warm up first.** Always use the platform's ungraded practice questions, and try a few questions from this guide on the same day as the real test to get your eye in.

### Common pitfalls to avoid

- **Trusting the tidy-looking record.** Well-formatted records can still contradict reality. The test — and the audit — rewards checking substance, not neatness.
- **Stopping at the first fault found.** A record or dataset can hold several independent problems (a ghost record and an unrecorded live server). Count each one before theorising about causes.
- **Forcing sources to agree.** Editing data to make numbers match is not reconciliation. Every difference needs an explanation; only genuine errors get corrected.
- **Forgetting the invisible.** Scanners miss isolated segments; monitoring misses powered-off machines. Ask what each source cannot see before treating its number as the truth.
- **Following the wrong procedure branch.** List the asset's attributes first (leased? stores data?), then walk only the branches those attributes trigger. Skipped branches are how leased laptops end up in skips.
- **Confusing a completed step with a completed process.** One satisfied precondition does not finish the workflow. Check the procedure's closing condition before setting a final status.
- **Racing the clock.** Most marks are lost to hurry, not slowness. If the test adapts and gets harder, that is success — settle in and keep your method.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how confidently and accurately you work with the numbers your role genuinely produces: record counts, accuracy percentages, audit samples, licence positions, discrepancy trends, and the small tables and reports they live in. It is not a mathematics exam. Nothing here goes beyond percentages, ratios, averages, rates, and careful table reading. What the test rewards is exactly what your role rewards: picking the right numbers, applying the right operation, and sense-checking the result before you rely on it.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions. Each question presents a short scenario, table, or chart with figures, followed by four or five options. An on-screen calculator is usually permitted — use it freely, because the test measures reasoning, not mental arithmetic. Scoring compares you with a norm group at your level, adaptive difficulty is common, and it is entirely normal not to finish every question. Accuracy carries more weight than raw speed on nearly every platform.

Why do employers use numeric reasoning tests for a configuration analyst? Because your role turns numbers into trust. When your change and release manager reports CMDB accuracy to senior stakeholders, the percentage comes from an audit you helped run. When a licence review asks whether the organisation is compliant, the answer is a comparison of counts you maintain. When the discrepancy backlog grows or shrinks, someone needs to say by how much, and whether the trend is improving. A configuration analyst who can compute a sample-based estimate correctly, or spot that two figures use different bases, protects the organisation from confidently wrong conclusions — which are far more dangerous than honestly uncertain ones.

If numbers have never felt like your strong suit, take heart: workplace numeric reasoning is closer to careful reading than to school algebra. Every technique you need is demonstrated step by step in the worked answers below, and each one is a calculation your job genuinely uses. Practise them a few times and they stop being test skills and become work skills — which is the whole idea.

### How this assessment maps to your role

The numeric skills tested map directly to the named skills in your role summary:

- **Percentages and proportions** map to your **Asset and configuration management** skill: record accuracy rates, verification coverage, and licence utilisation are all percentage work, and audit sampling — checking a subset and scaling up — is proportional reasoning applied to maintaining accurate information.
- **Averages and rates** map to your day-to-day administrative support duties: records processed per day, average time to clear a discrepancy, and how long a verification exercise will take at a given rate are the calculations that make your workload plannable — and make your promises to the change and release manager reliable.
- **Comparing counts across sources** maps to your core duty of maintaining CMDB integrity: reconciling register counts, scan counts, and report snapshots is arithmetic with statuses attached, and the test's table questions rehearse exactly that discipline.
- **Trends and projections** map to your **Availability and capacity management** knowledge: explaining capacity processes means understanding headroom, growth rates, and time-to-threshold — simple divisions with important consequences.
- **Reading data tables carefully** maps to your **Incident management** and **Problem management** skills: incident counts by category, discrepancy trends across audits, and pattern-hunting in problem data all start with extracting the right figures from a table before drawing any conclusion.

### Practice questions

**Question 1 (easy) — Record accuracy percentage**

You check 60 CMDB records against physical assets during a spot check. 51 records are fully accurate and 9 contain at least one error. What is the accuracy rate of the checked records?

- A) 80%
- B) 85%
- C) 88%
- D) 91%

**Correct answer: B**

**Explanation:** Accuracy rate = accurate records ÷ records checked × 100. Step 1: 51 ÷ 60 = 0.85. Step 2: 0.85 × 100 = 85%. Sense-check via the error side: 9 ÷ 60 = 0.15 = 15%, and 100% − 15% = 85% — the two routes agree, which is the quickest self-check available. Note the base: records checked (60), not the whole CMDB. A spot check tells you about the records you inspected; whether you may generalise further depends on how the sample was chosen, which is a later question in this set. Accuracy percentages are the headline number of configuration work — this calculation should become as automatic as logging in.

**Question 2 (easy) — Average records processed per day**

Over five working days you processed the following numbers of record updates: 34, 28, 41, 30, 37. What was your average (mean) number of updates per day?

- A) 32
- B) 33
- C) 34
- D) 36

**Correct answer: C**

**Explanation:** Mean = total ÷ number of days. Step 1: add in stages: 34 + 28 = 62; 62 + 41 = 103; 103 + 30 = 133; 133 + 37 = 170. Step 2: divide: 170 ÷ 5 = 34. Sense-check: the daily values run from 28 to 41, and 34 sits comfortably inside that range — a mean outside the range always signals an arithmetic slip. Averages like this are how you plan realistically: if a data-cleansing task involves about 500 updates and you average 34 a day alongside your other work, you can tell your change and release manager it needs roughly three working weeks, not "a few days". Grounded estimates are a quiet professional superpower, and they start with this humble calculation.

**Question 3 (easy) — Ratio of configuration item types**

The CMDB contains hardware, software, and network configuration items in the ratio 5 : 3 : 2. There are 4,000 configuration items in total. How many are network items?

- A) 400
- B) 800
- C) 1,200
- D) 2,000

**Correct answer: B**

**Explanation:** Step 1: total ratio parts = 5 + 3 + 2 = 10. Step 2: one part = 4,000 ÷ 10 = 400 items. Step 3: network items = 2 parts = 2 × 400 = 800. Full sense-check: hardware = 5 × 400 = 2,000; software = 3 × 400 = 1,200; and 2,000 + 1,200 + 800 = 4,000 — the split reproduces the total exactly. Option A is the one-part value (an easy slip), and option D is the hardware count. Ratios appear whenever you summarise the shape of the estate — for audit scoping ("network items are a fifth of the database"), for dividing verification work fairly across the team, or for judging whether a category's growth is changing the balance of what you manage.

**Question 4 (moderate) — Percentage change in discrepancies**

The monthly reconciliation between the CMDB and the discovery scan found 64 discrepancies in June and 48 in July. By what percentage did discrepancies fall from June to July?

- A) 16%
- B) 20%
- C) 25%
- D) 33%

**Correct answer: C**

**Explanation:** Percentage change = (difference ÷ original) × 100, and the original is the earlier month. Step 1: difference = 64 − 48 = 16. Step 2: divide by June's figure: 16 ÷ 64 = 0.25. Step 3: 0.25 × 100 = 25%. Option D is the classic wrong turn — dividing by the later figure (16 ÷ 48 = 33%) — and option A mistakes the raw difference for a percentage. Direction matters when you report this: "discrepancies fell 25% from June" uses June as the base, but if someone asks what rise would return July's 48 to June's 64, the answer is 33%, because the base has switched to 48. Being precise about bases is what makes your data-quality reporting to the change and release manager dependable, and month-on-month discrepancy trends are among the most watched numbers in configuration management: they are the pulse of CMDB health.

**Question 5 (moderate) — Licence utilisation and headroom**

Your organisation holds 150 licences for a project management tool. The CMDB shows the software installed and in use on 129 machines. The procurement pipeline shows 12 new starters next month who will each need the tool. Will the current licences cover next month's need, and what will utilisation be if all 12 are installed?

- A) Yes — utilisation will be 94%
- B) Yes — utilisation will be 86%
- C) No — there will be a shortfall of 9 licences
- D) Yes — utilisation will be 96%

**Correct answer: A**

**Explanation:** Step 1: projected installations = 129 + 12 = 141. Step 2: compare with licences held: 141 ≤ 150, so yes, the licences cover the need, with 150 − 141 = 9 spare — note how option C tries to recycle that same 9 as a shortfall, hoping you subtract in the wrong direction. Step 3: utilisation = 141 ÷ 150 = 0.94 = 94%. Option B is current utilisation (129 ÷ 150 = 86%) — true today, but not what was asked. This two-part shape — a yes/no comparison, then a percentage — is very common in tests and in real licence reviews. The professional layer on top: 94% utilisation means 9 licences of headroom, and if hiring continues at anything like 12 a month, next month's review will need a purchase recommendation. Spotting that a healthy number is about to stop being healthy is exactly the forward glance your capacity management knowledge describes.

**Question 6 (moderate) — Reading an audit results table**

Two successive audits categorised CMDB record errors as follows:

| Error category | Spring audit | Autumn audit |
|---|---|---|
| Wrong location | 40 | 30 |
| Wrong owner | 25 | 15 |
| Wrong status | 20 | 18 |
| Missing relationship | 15 | 12 |

Which error category improved by the largest percentage between audits?

- A) Wrong location
- B) Wrong owner
- C) Wrong status
- D) Missing relationship

**Correct answer: B**

**Explanation:** Compute each category's percentage fall, using the spring figure as the base. Wrong location: (40 − 30) ÷ 40 = 10 ÷ 40 = 25%. Wrong owner: (25 − 15) ÷ 25 = 10 ÷ 25 = 40%. Wrong status: (20 − 18) ÷ 20 = 2 ÷ 20 = 10%. Missing relationship: (15 − 12) ÷ 15 = 3 ÷ 15 = 20%. The largest percentage improvement is wrong owner at 40%. The trap is option A: wrong location fell by the joint-largest absolute amount (10 errors), but from a much bigger base, so its percentage improvement is smaller. Absolute change and percentage change answer different questions — "where did we remove the most errors?" versus "which problem are we beating fastest?" — and a good audit summary reports both. There is also a story in the laggard: wrong status improved only 10%, which might suggest the process fix that helped owners and locations has not touched status updates — precisely the kind of pattern your problem management skill should flag for investigation.

**Question 7 (moderate) — Time to complete a verification exercise**

Before the annual audit you must physically verify 320 assets. You can verify assets at a rate of 8 per hour, and you can spend 2 hours per day on verification alongside your other duties. There are 22 working days before the audit. Will you finish in time, and with how many days to spare (if any)?

- A) Yes, with 2 days to spare
- B) Yes, with 4 days to spare
- C) No, you will be 2 days short
- D) Yes, with exactly no days to spare

**Correct answer: A**

**Explanation:** Step 1: daily verification capacity = 8 per hour × 2 hours = 16 assets per day. Step 2: days needed = 320 ÷ 16 = 20 days. Step 3: compare with the 22 available days: 22 − 20 = 2 days to spare. So yes, with 2 days' margin — option A. The professional reading of that margin matters as much as the arithmetic: 2 days out of 22 is thin protection against sick days, urgent interruptions, or assets that turn out to be harder to locate than planned (and some always do). A careful analyst would tell the change and release manager "on track, but with little slack — flag early if anything erodes the two hours a day". Rate × time calculations like this one are how you turn a mountain of records into a plan, and how you make commitments you can actually keep — which, over time, is what a reputation for reliability is made of.

**Question 8 (moderate) — Weighted average accuracy across domains**

An audit checks two domains of the CMDB. In the server domain, 200 records are checked with 90% found accurate. In the laptop domain, 300 records are checked with 80% found accurate. What is the overall accuracy across all checked records?

- A) 84%
- B) 85%
- C) 86%
- D) 88%

**Correct answer: A**

**Explanation:** You cannot average 90% and 80% to get 85%, because the domains contributed different numbers of records. Step 1: accurate server records = 90% of 200 = 0.9 × 200 = 180. Step 2: accurate laptop records = 80% of 300 = 0.8 × 300 = 240. Step 3: total accurate = 180 + 240 = 420. Step 4: total checked = 200 + 300 = 500. Step 5: overall accuracy = 420 ÷ 500 = 0.84 = 84%. The overall figure sits closer to the laptop domain's 80% because laptops contributed more records — that is what "weighted" means. The unweighted 85% (option B) is the classic error, and here it flatters the database by a full percentage point. When your work feeds a report your manager signs, that difference is not cosmetic: overstating CMDB accuracy to a governance board, even innocently, spends credibility the team will want back later. Always return to raw counts before combining percentages.

**Question 9 (challenging) — Scaling a sample estimate**

The CMDB holds 12,000 records. For the quarterly quality check, you audit a random sample of 400 records and find 22 with at least one error. Based on the sample, approximately how many records in the whole CMDB would you expect to contain at least one error?

- A) 220
- B) 550
- C) 660
- D) 880

**Correct answer: C**

**Explanation:** Step 1: sample error rate = 22 ÷ 400 = 0.055 = 5.5%. Step 2: apply the rate to the full database: 5.5% of 12,000 = 0.055 × 12,000 = 660. The scaling route agrees: the database is 12,000 ÷ 400 = 30 times the sample, and 22 × 30 = 660. Option A forgets to scale at all; option B halves the multiplier somewhere; option D would follow from misreading the error count. Two professional footnotes: first, this works because the sample was random — if you had sampled only server records, or only records touched recently, the 5.5% could not be projected onto the whole database, so how a sample is drawn matters as much as the arithmetic. Second, report the projection with honest softness: "around 660 records, based on a 400-record sample" — a different sample would give a slightly different figure. Sampling is how real CMDB audits work, because hand-checking 12,000 records is nobody's quarter well spent; the analyst who can run and explain the projection is contributing directly to maintaining accurate information at scale.

**Question 10 (challenging) — Backlog clearance with ongoing arrivals**

The discrepancy backlog currently holds 180 items. Each week, the reconciliation process adds an average of 20 new discrepancies, and you and a colleague together clear an average of 35. At these rates, in how many weeks will the backlog be fully cleared?

- A) 5 weeks (rounding to the nearest week)
- B) 9 weeks
- C) 12 weeks
- D) The backlog will never clear at these rates

**Correct answer: C**

**Explanation:** The backlog changes each week by arrivals minus clearances: 20 − 35 = −15, a net reduction of 15 items per week. Time to clear = current backlog ÷ net weekly reduction = 180 ÷ 15 = 12 weeks. Option A comes from dividing 180 by the clearance rate alone (180 ÷ 35 ≈ 5), which quietly pretends no new discrepancies will arrive — the single most common error in backlog arithmetic, and one that produces promises you cannot keep. Option D would only be right if arrivals matched or exceeded clearances. The net-rate idea is the heart of every queue you will ever manage: backlogs fall only as fast as the gap between out and in. It also points at the two levers: clearing faster, or arriving slower — and the second lever is often cheaper. If a chunk of those 20 weekly arrivals trace to one systematic cause (say, a sync job mangling one field), fixing that cause — your problem management skill's "preventative measures" — might cut arrivals to 10 and nearly double the net rate. The best backlog work often happens at the inlet, not the outlet.

**Question 11 (challenging) — The cost of ghost records**

An audit identifies that 45 of the estate's recorded servers are "ghosts" — decommissioned machines never removed from support contracts. Each ghost server costs £30 per month in support fees. The one-off administrative cost of properly verifying and removing all 45 from the contracts is £8,100. After how many months of savings does the removal exercise pay for itself?

- A) 4 months
- B) 6 months
- C) 8 months
- D) 12 months

**Correct answer: B**

**Explanation:** Step 1: monthly saving once removed = 45 × £30 = £1,350. Step 2: payback time = one-off cost ÷ monthly saving = £8,100 ÷ £1,350 = 6 months. So after 6 months the exercise has paid for itself, and every month thereafter saves a clean £1,350 — £16,200 a year. This is the calculation that turns data hygiene into a business case. Ghost records are usually discussed as a tidiness problem, but they are also a money problem: the organisation pays real support fees for machines that no longer exist, and your verification work — confirming the location and state of IT assets — is what finds and stops the leak. When you can attach a payback period to a cleanup proposal, "we should tidy the CMDB" becomes "this pays for itself by spring and saves £16,200 a year", which is a sentence budget-holders act on. Payback arithmetic is simple; the habit of doing it is what gets data-quality work funded.

**Question 12 (challenging) — Verification coverage target with mixed progress**

Your team's target is to physically verify 90% of the estate's 2,400 assets by year end. So far, 1,824 assets have been verified. Of the remaining unverified assets, 96 are known to be in a locked storage facility that will not be accessible until January. Can the 90% target still be met this year, and what is the minimum number of additional assets you must verify to meet it?

- A) No — the locked assets make the target impossible.
- B) Yes — verify at least 336 more assets.
- C) Yes — verify at least 240 more assets.
- D) Yes — verify at least 216 more assets.

**Correct answer: B**

**Explanation:** Step 1: the target in assets = 90% of 2,400 = 0.9 × 2,400 = 2,160. Step 2: additional verifications needed = 2,160 − 1,824 = 336. Step 3: check feasibility against the constraint: unverified assets = 2,400 − 1,824 = 576; of these, 96 are inaccessible, leaving 576 − 96 = 480 assets that can still be verified this year. Since 480 ≥ 336, the target remains achievable — answer B. Option A gives up without doing step 3: the locked facility removes 96 candidates, but the target only needs 336 of the accessible 480. Option C misreads the target as 90% of the unverified remainder, and option D subtracts the locked assets from the requirement, as if inaccessibility reduced the target itself — it does not; it only shrinks the pool you can draw from. The three-step shape — convert the percentage target to a count, find the gap, then check the gap fits within what is actually reachable — is exactly how you should answer "can we still hit it?" questions for your manager: with a number, a yes-or-no, and the constraint named. And the margin (480 available versus 336 needed) is itself useful planning information: you can afford 144 of the accessible assets to prove hard to find before the target is at risk.

### Preparation tips

- **Master the five core moves.** Percentage of a total, percentage change, weighted average, rate × time, and net rate (in minus out). Nearly every question above is one of these — recognise which, and the hard part is done.
- **Name the base before dividing.** Out of records checked? Out of the earlier month? Out of assets still accessible? Saying the base aloud prevents the most common error in the whole test.
- **Go back to raw counts before combining.** Whenever two percentages meet — two domains, two months, two sources — convert to counts, combine, then re-percentage. Never average percentages directly.
- **Write intermediate results down.** One-part values, totals, differences: jot each on scrap paper. Re-keying a half-remembered subtotal into the calculator is where careless marks go to die.
- **Sense-check with the answer's meaning.** An accuracy rate near the error counts you saw, an average inside the data's range, a payback period that feels commercially plausible — a five-second reality check catches most slips.
- **Practise on your own reports.** Recompute last quarter's accuracy figure, the discrepancy trend, or the licence position by hand. Real data is the best rehearsal, and you might even catch something.
- **Keep units and timeframes consistent.** Per hour versus per day, monthly costs versus one-off costs, spring audit versus autumn audit. Convert early, label clearly.

### Common pitfalls to avoid

- **Dividing by the wrong base.** The later month instead of the earlier, the whole estate instead of the sample, the remainder instead of the total. Base errors produce confident nonsense.
- **Averaging percentages from unequal groups.** 90% and 80% only average to 85% when the groups match in size. Weighted thinking is not optional.
- **Ignoring the inflow.** Backlog and clearance questions punish anyone who divides by the clearance rate alone. Always compute the net rate first.
- **Confusing absolute with percentage change.** The biggest raw improvement and the fastest proportional improvement are routinely different rows. Read which the question wants.
- **Projecting from a biased sample.** Scaling up is only valid for random or representative samples. If a question mentions how the sample was chosen, that detail is probably the point.
- **Answering the question you expected.** Current utilisation versus projected utilisation, spare licences versus shortfall — near-miss options are built from correct arithmetic aimed at the wrong target. Re-read the final sentence of the question before choosing.
- **Rounding too early.** Carry full precision through the steps and round only at the end; small early roundings compound into wrong options that feel close enough to be tempting.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and reason about written material of the kind your role handles daily: data standards, asset disposal procedures, audit findings, change control policies, status definitions, and emails from engineers and your change and release manager. The most common question style presents a short passage and a statement, then asks whether the statement is **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage does not give enough information to decide). Other styles ask for the main point of a passage, a safe inference, an unstated assumption, or a judgement about which version of a piece of writing communicates most clearly.

The typical format is an online, timed test of 15 to 25 minutes with 15 to 30 questions. The golden rule: answer only from the passage in front of you. You may know from your own workplace that a statement is true — but if this passage does not support it, the answer is "Cannot say". The test deliberately measures your ability to separate what a text states from what you assume, remember, or expect. Scoring is against a norm group at your level, adaptive difficulty is common, and unfinished questions are normal.

Why do employers use verbal reasoning tests for a configuration analyst? Because your role is built on precise reading. A CMDB is only as good as the definitions behind it: what "Live" means, when "Retired" may be set, which edits need which approvals. Those definitions live in written standards, and applying them correctly — especially under supervision, where you follow documented procedures rather than personal judgement — depends on reading them exactly. The same goes for audit findings you act on, disposal procedures you execute, and requests you receive: an engineer's email saying "can you update the record for the old server" contains at least three ambiguities, and noticing them before editing is what protects the data. Verbal reasoning tests compress this daily discipline into short, sharp exercises.

If reading tests make you nervous, here is the reframe that helps most people: this is not English literature. There are no hidden meanings and no style points. It is literal, careful, evidence-based reading — much closer to checking a record against a standard than to interpreting a poem — and it is a skill that visibly improves within a week or two of practice.

### How this assessment maps to your role

The verbal skills tested map directly to the named skills in your role summary:

- **Precise comprehension of definitions and conditions** maps to your **Asset and configuration management** skill: maintaining secure configuration and accurate information means applying written definitions — statuses, naming rules, mandatory fields — exactly as the standard states them, not approximately as habit remembers them.
- **True/False/Cannot-say discipline** maps to your core duty of maintaining CMDB integrity: a record's claim is verified, contradicted, or unverified — precisely the three verdicts the test trains. Verifying the location and state of IT assets is Cannot-say discipline applied to the physical world.
- **Reading procedures branch by branch** maps to your **Change management** skill: applying change control procedures under supervision means following the written branch that matches the case in front of you, and recognising when a case matches no branch — which is the moment to ask, not improvise.
- **Inference and assumption-spotting** maps to your **Problem management** skill: reading audit findings and incident notes, drawing only the conclusions the evidence supports, and noticing what a report assumes but never establishes.
- **Clear-writing judgement** maps to your **Community collaboration** and **User focus** skills: writing data correction requests, audit notes, and emails that busy colleagues can act on first time — plain, specific, and organised for the reader — is how a support role multiplies its value.

### Practice questions

For each True/False/Cannot-say question, judge the statement strictly against the passage.

**Passage 1 (for Questions 1–3)**

*Extract from the CMDB data standard:* "Every configuration item must have exactly one status from the approved list: Ordered, In build, Live, In maintenance, Withdrawn, or Retired. The status Live may only be set once acceptance testing is complete. Retired may only be set by the configuration analyst or the change and release manager, and only after disposal or return has been confirmed. Records for Retired items must be kept for seven years and must not be deleted. Status changes must reference an approved change or an approved data correction request."

**Question 1 (easy) — True/False/Cannot say**

Statement: "A configuration item may hold two statuses at the same time while it moves between states."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The standard's first sentence says every configuration item must have "exactly one status" from the approved list. "Exactly one" rules out two statuses at any time, including during transitions — so the statement contradicts the passage and the answer is False. Notice how much work the word "exactly" does: a standard that said "a status" might arguably tolerate an item briefly holding two, but "exactly one" closes that door. Reading quantity words — exactly, at least, at most, only — with full attention is the core habit of both this test and your data-quality work: those small words are where standards carry their force, and where sloppy reading creates records that pass a casual glance but fail an audit.

**Question 2 (easy) — True/False/Cannot say**

Statement: "Only the change and release manager may set an item's status to Retired."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The passage says Retired "may only be set by the configuration analyst or the change and release manager". The statement drops the configuration analyst — you! — and claims the manager alone holds the permission. That directly contradicts the passage, so the answer is False. This is the classic "narrowed claim" trap: the statement takes a rule about two roles and shrinks it to one, and a fast reader who remembers "only... change and release manager" from the sentence's end will wrongly answer True. Read the whole permission, not the half your eye lands on. The workplace mirror is worth noting too: knowing exactly which permissions your role holds — and which it does not — is what lets you act confidently within them, which is precisely what "applying procedures under supervision" means in practice.

**Question 3 (easy) — True/False/Cannot say**

Statement: "Acceptance testing is carried out by the service desk team."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage mentions acceptance testing once, as a precondition: Live "may only be set once acceptance testing is complete". It says nothing about who performs that testing. Your organisation may well have a testing team, and you may know exactly who they are — but this passage neither confirms nor denies that the service desk does it, so the answer is Cannot say. This is the discipline the whole test rests on: the difference between what the document states and what you know from elsewhere. It has a direct workplace parallel: when a record's field is blank, the truthful position is "unverified", not your best guess — and when a procedure is silent about who does something, the right move is to ask, not to assume. Practise noticing the moment your mind supplies a fact the text never gave you; that noticing is the skill.

**Passage 2 (for Questions 4–5)**

*Extract from the asset disposal procedure:* "Assets awaiting disposal must be stored in the secure holding area. Data-bearing assets must not leave the building until a certified data wipe or physical destruction of the storage media has been completed and certificated. The disposal contractor collects on the last Friday of each month. The configuration analyst updates each asset's record within two working days of collection, attaching the contractor's collection receipt. Where an asset cannot be located at collection time, the analyst must record it as 'Missing — under investigation' and notify the change and release manager the same day."

**Question 4 (moderate) — True/False/Cannot say**

Statement: "A laptop whose drive has not yet been wiped may be moved to the secure holding area inside the building."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Track what the two rules actually restrict. Rule one: assets awaiting disposal must be stored in the secure holding area — that is where an unwiped laptop awaiting disposal belongs. Rule two: data-bearing assets must not leave the building until wiped or destroyed, with certification. Moving a laptop to the holding area inside the building does not involve leaving the building, so rule two is not engaged, and rule one positively requires the move. The statement is supported: True. The trap is a blurred reading that remembers "unwiped assets must not be moved" — but the restriction is on leaving the building, not on movement generally. Procedures are precise about which action they restrict, and so must you be: in real disposal runs, over-reading the rule ("we can't touch it until it's wiped") stalls the process, while under-reading it ("the contractor can take it, the wipe's booked") is a data protection incident. Both errors come from paraphrasing instead of reading.

**Question 5 (moderate) — Inference from the passage**

Based on Passage 2, which of the following is the safest inference?

- A) The procedure anticipates that assets will sometimes be missing at collection time.
- B) The disposal contractor is responsible for wiping data-bearing assets.
- C) Assets are collected weekly.
- D) The secure holding area is outside the main building.

**Correct answer: A**

**Explanation:** The passage dedicates its final sentence to exactly what must happen "where an asset cannot be located at collection time" — a documented branch, with a status value and a same-day notification duty. Procedures do not build branches for situations their authors consider impossible; the existence of the missing-asset path is solid evidence the procedure anticipates it. That is option A, and it is an inference rather than a statement — the passage never says "assets sometimes go missing", but its structure presupposes it. Option B misassigns the wipe: the passage requires wiping before the contractor's collection, and never says who performs it — if anything, the sequencing hints it is done in-house, but "the contractor does it" is contradicted by nothing and supported by nothing, making it a poor inference. Option C contradicts "last Friday of each month". Option D contradicts the logic of Question 4: the holding area must be reachable without leaving the building. Good inference stays one small, well-supported step from the text — and reading procedures for what their structure implies (which failure modes they plan for, which they silently ignore) is a genuinely useful analyst skill when you are asked to improve them.

**Question 6 (moderate) — Must, should, and may in a data standard**

Your data standard states: (i) "Every server record **must** include the physical location field." (ii) "Records **should** include the warranty expiry date where the information is available." (iii) "Analysts **may** add free-text notes to any record." You review a server record that has a location, no warranty date, and no notes. The warranty date is available in the procurement system. Which requirement, if any, does the record breach?

- A) Requirement (i)
- B) Requirement (ii) — although as a "should", it is a compliance gap rather than an absolute breach
- C) Requirement (iii)
- D) The record is fully compliant

**Correct answer: B**

**Explanation:** Apply each word at its defined strength. (i) "Must": the location is present — satisfied. (iii) "May": a permission cannot be breached by not using it; absent notes are fine. (ii) "Should": the standard asks for the warranty date "where the information is available", and the question tells you it is available in the procurement system — so the record falls short of the recommendation. But "should" marks a strong recommendation, not an absolute rule, so the precise verdict is option B's: a compliance gap to be fixed (or justified), not a hard breach like a missing mandatory field. Option D fails because it treats "should" as ignorable — it is not; it is expected-unless-justified. This graded vocabulary (used across government and industry standards, following the RFC 2119 convention) is load-bearing in your work: when you audit records, your findings should distinguish must-breaches (report immediately) from should-gaps (schedule for cleanup), because mixing them makes reports both alarmist and vague. And when you draft standards text yourself one day, you will choose these words deliberately.

**Question 7 (moderate) — Clear-writing judgement**

You need to email an engineer asking them to confirm details so you can correct a record. Which version communicates most clearly?

- A) "Hi — regarding the aforementioned server, there appear to be certain discrepancies in respect of the configuration data held, which it would be appreciated if you could look into at your earliest convenience."
- B) "Hi — quick one: the CMDB thinks LDS-WIN-021 is in rack B4, but Tuesday's scan puts it in rack C1. Can you confirm which rack it's actually in? If you can reply by Thursday I'll correct the record before Friday's audit extract. Thanks!"
- C) "Hi — the CMDB is wrong again. Please fix your server's record."
- D) "Hi — please see the attached spreadsheet of all 340 discrepancies from this week's scan and confirm each row."

**Correct answer: B**

**Explanation:** Judge each version by whether a busy reader can act on it first time. Option B names the asset, states the specific conflict (B4 versus C1, with sources for each claim), asks one answerable question, gives a deadline with its reason, and says what will happen next. The engineer can reply in one line. Option A is fog: "aforementioned server" (which server?), "certain discrepancies" (which?), "earliest convenience" (when?) — polite words arranged to transmit no information. Option C is worse than vague — "wrong again" is an accusation, "your server's record" pushes your job onto the engineer, and no detail is given to act on; emails like this are how support roles lose the goodwill they run on. Option D drowns one urgent question in 340 rows, guaranteeing the Thursday answer arrives in three weeks. The pattern behind B is worth memorising for every correction request you send: specific item, both conflicting claims with sources, one clear question, a dated reason to reply. Clear writing is not decoration in your role — it is how the CMDB actually gets corrected, one well-formed question at a time. That is community collaboration in its most practical form.

**Passage 3 (for Questions 8–9)**

*Extract from an internal audit finding:* "Finding 4: Of 60 sampled laptop records, 12 showed a different assigned user from the person actually holding the device. In 9 of the 12 cases, the device had been legitimately transferred between users, but the transfer form had not been submitted to the configuration team. The remaining 3 cases are unexplained and have been referred for investigation. The audit team notes that the transfer form is a four-page document requiring three signatures, and that several interviewees described it as 'too slow for how teams actually work'. Recommendation: the configuration team should review the transfer process with a view to simplification, and re-audit in six months."

**Question 8 (moderate) — True/False/Cannot say**

Statement: "In most of the mismatched cases, the device had been legitimately transferred but the paperwork had not reached the configuration team."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Check the arithmetic inside the words: 12 records mismatched; in 9 of the 12, the device "had been legitimately transferred between users, but the transfer form had not been submitted". Nine of twelve is three-quarters — comfortably "most" — and the description matches the statement's two parts (legitimate transfer; paperwork not received). So the statement is supported: True. Two details reward attention. First, "most" is a quantity claim, and you verified it numerically rather than by impression — always do that when a statement quantifies. Second, notice what the finding is really saying about your world: the records were wrong not because people were careless with data but because the process was heavier than the behaviour it tried to govern. Users transferred devices in seconds; the form took days. When you read audit findings at work, this pattern — accurate-data-loses-to-inconvenient-process — is one of the most common root causes of CMDB drift, and recognising it in text is the first step to fixing it in fact.

**Question 9 (challenging) — Identifying the unstated assumption**

The audit's recommendation moves from "the transfer form is slow and often skipped" to "simplify the transfer process". Which unstated assumption does the recommendation most depend on?

- A) If the process were simpler, more transfers would be recorded, improving record accuracy.
- B) The three unexplained cases will turn out to be thefts.
- C) Laptops are transferred more often than desktops.
- D) The audit sample of 60 records was too small.

**Correct answer: A**

**Explanation:** An assumption is the unstated bridge an argument must cross. The finding establishes: forms are burdensome, and 9 of 12 mismatches came from unsubmitted forms. The recommendation prescribes: simplify the process. The bridge between them is that the burden causes the non-submission — so reducing the burden will increase submission and, through it, accuracy. That is option A, and if it is false (say, people skip the form because they do not know it exists — a training problem, not a complexity problem), simplification would change little. Option B concerns the 3 referred cases, which the recommendation does not depend on at all. Option C compares device types the passage never mentions. Option D attacks the sample size, which would undermine the finding rather than support the recommendation — the opposite of an assumption it depends on. Assumption-spotting is directly useful in your role: when a proposed process fix reaches you, asking "what is this assuming about why people currently don't comply?" is often the difference between a fix that works and a simpler form that is skipped just as cheerfully. It is also exactly how a six-month re-audit should be read: as the test of assumption A.

**Question 10 (challenging) — Reconciling two documents**

Document 1, the CMDB standard, states: "Records for Retired items must be kept for seven years and must not be deleted." Document 2, a data protection guidance note, states: "Personal data must not be retained longer than necessary for the purpose for which it was collected. Asset records containing the names of assigned users should have user-identifying fields cleared when the record is no longer operationally required." Which statement best describes how the two documents relate?

- A) They contradict each other, and one must be withdrawn.
- B) They are compatible: a Retired record can be kept for seven years with its user-identifying fields cleared once no longer operationally needed.
- C) Document 2 overrides Document 1, so Retired records should be deleted when no longer needed.
- D) Document 1 overrides Document 2, so user names must stay on records for seven years.

**Correct answer: B**

**Explanation:** Look precisely at what each document governs. Document 1 governs the record: keep it seven years, never delete it. Document 2 governs particular data within records: clear user-identifying fields when no longer operationally required. A record can be retained while a field within it is cleared — the two instructions operate on different objects and can both be satisfied at once, which is option B. Options C and D both assume a conflict and then pick a winner, but no conflict exists once the scopes are read carefully; and neither document claims authority over the other. Option A gives up on reading. This question rehearses one of the most valuable skills in any standards-based role: apparent contradictions between documents usually dissolve when you identify exactly what each one applies to — whole record versus field, all assets versus data-bearing assets, retention versus deletion. At work, the practical output of this reading would be a small, precise procedure: on retirement, keep the record, schedule the user-field clearance — satisfying the audit trail and data protection at once. The analyst who reads both documents this carefully is the one who writes that procedure instead of escalating a false conflict.

**Question 11 (challenging) — Main point of a passage**

*Extract from a quarterly report:* "This quarter the configuration team processed 2,140 record updates, an 8% increase on last quarter, while the team's error rate on processed updates fell from 2.1% to 1.6%. However, the volume of updates arriving by email rather than through the request portal rose to 40%. Email requests take roughly twice as long to process, because details must be extracted manually and are often incomplete, requiring follow-up. If email volumes continue to rise, the team's throughput gains will be absorbed by rework, and processing times will lengthen despite the team's improved accuracy. We recommend that email requesters be redirected to the portal, and that the portal's request form be reviewed to understand why users avoid it."

Which sentence best expresses the main point of the passage?

- A) The team is performing badly and processing times are already unacceptable.
- B) The team's productivity and accuracy improved, but the growing share of email requests threatens those gains, so request channels need attention.
- C) Users who email requests instead of using the portal should be reported to their managers.
- D) The portal should be decommissioned since 40% of users avoid it.

**Correct answer: B**

**Explanation:** Map the passage's shape: good news (volume up 8%, errors down to 1.6%), a threat (email share risen to 40%, costing double the effort), a projection (gains absorbed if the trend continues), and a two-part recommendation (redirect to the portal, and investigate why the portal is avoided). Option B captures the whole arc — achievement, risk, action. Option A contradicts the reported improvements and asserts a present crisis the passage only forecasts conditionally ("if email volumes continue to rise"). Option C invents an enforcement measure the passage never proposes — and note how the actual recommendation pairs redirection with curiosity about the portal's usability; the passage treats email avoidance as a signal to investigate, not misbehaviour to punish. Option D turns that signal into the opposite conclusion, scrapping the very tool the passage wants improved. Main-point questions reward reading for structure: ask "what does the author want the reader to take away and do?" rather than latching onto the most memorable number. In your role, this is how you should both read and write quarterly reports — and the passage models a habit worth copying: when users route around your process, the mature response is to ask what the process is costing them.

**Question 12 (challenging) — True/False/Cannot say with a subtle scope shift**

*Passage:* "Following the spring audit, all laptop records in the Leeds office were physically verified, and any errors found were corrected at the point of verification. The verification exercise took three weeks. Since it concluded, all new laptop records for Leeds have been created using the barcode scanning process, which eliminates manual transcription of serial numbers."

Statement: "All laptop records in the Leeds office are now free of errors."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Trace what the passage guarantees, and when. The verification corrected the errors it found, at the time it ran — but records can drift after verification (devices move, users change), and the passage covers the weeks since only for newly created records, and even for those, barcode scanning eliminates one error source (serial number transcription), not all errors: a scanned serial can still be attached to the wrong user or location. So "all records are now free of errors" is neither guaranteed by the passage (verification was a snapshot; protection since covers one error type in one subset) nor contradicted by it (nothing says errors have appeared). The answer is Cannot say. This statement is engineered from three quiet inflations: "were corrected then" becomes "are correct now"; "new records use scanning" becomes "all records are protected"; "eliminates transcription errors" becomes "eliminates errors". Each inflation sounds like a paraphrase and each changes the claim. This is the exact skill of your profession: a verified record is accurate as of its verification date, and an honest CMDB carries that humility in its "last verified" field. The analyst who reads — and writes — with tense and scope in sharp focus is the one whose assurances auditors learn to trust.

### Preparation tips

- **Drill True/False/Cannot-say little and often.** Take two sentences from any standard or procedure at work and write one supported statement, one contradicted one, and one the text is silent on. Five minutes a day builds the reflex quickly.
- **Point to the evidence before answering.** Make yourself locate the exact words that support or contradict the statement. If your finger cannot find them, the answer is probably Cannot say.
- **Circle the small words.** Exactly, only, all, most, may, must, should, until, where available — standards carry their meaning in these words, and so do test statements. Read them twice.
- **Watch tense and scope inflations.** "Was corrected" is not "is correct"; "new records" is not "all records"; "one error source" is not "all errors". Hard questions are built from exactly these shifts.
- **Read for what each document governs.** When two texts seem to conflict, identify each one's object — record versus field, building versus room, process versus data — before declaring a contradiction.
- **Practise the clear-writing patterns.** Rewrite one of your own recent emails using the shape from Question 7: specific item, both claims with sources, one question, dated reason. You are preparing for the test and upgrading your daily work simultaneously.
- **Use your role's real documents as practice texts.** Data standards, disposal procedures, and audit reports are ideal — closer to the test than any newspaper, and reading them closely is literally your job.

### Common pitfalls to avoid

- **Importing workplace knowledge.** The most common error: answering True because it is true in your organisation. The test asks only what this passage supports.
- **Under-using Cannot say.** It feels like admitting defeat; it is actually the disciplined verdict for unverified claims — the same verdict an honest audit gives. Expect to choose it often.
- **Paraphrasing instead of reading.** "Must not leave the building" is not "must not be moved"; "may only be set by A or B" is not "may only be set by B". Answer against the words, not your summary of them.
- **Treating "should" as either binding or ignorable.** It is neither: it marks expected-unless-justified. Both over-reading and under-reading it produce wrong answers and bad audits.
- **Declaring contradictions too quickly.** Two documents that seem to clash usually govern different objects or timeframes. Check scopes before choosing "they conflict".
- **Latching onto memorable numbers.** In main-point questions, the striking statistic is rarely the point; the author's intended action usually is. Read the last sentences with care.
- **Rushing long passages.** Skim once for structure, then hunt the sentence each question turns on. Re-reading the whole passage for every statement burns time; never reading it properly burns marks.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment presents realistic workplace scenarios and asks how you would respond. It contains no arithmetic and no comprehension passages — instead it measures professional judgement: how you balance data integrity, process discipline, helpfulness, honesty, and knowing when to act independently versus when to ask. Question formats vary: most commonly you choose the **most effective** response from four options; sometimes you identify the **least effective**, rate each option, or rank all four.

The typical format is an online test of 20 to 40 minutes with 10 to 20 scenarios, usually generously timed, because employers want considered judgement rather than reflexes. There are no trick questions, but options are carefully built: alongside the best response you will typically find one that is nearly right but skips a step, one that avoids the issue, and one that overreacts. Scoring compares your choices against a key set by experienced practitioners and calibrated to your level — which is important reassurance: at configuration analyst level, the strong answer often involves doing the safe immediate thing and then checking with your change and release manager. You are not being scored on making a manager's decisions; you are being scored on excellent analyst judgement.

Why do employers use situational judgement tests for a configuration analyst? Because your role sits where accuracy meets people. Engineers want records changed quickly; auditors want evidence; your manager wants dependable support; and the procedures that protect the CMDB can feel, to busy colleagues, like obstacles. The moments that define your effectiveness are rarely technical: they are the request to "just tweak a record" without a reference, the error you find in a senior person's work, the pressure before an audit to make numbers look tidier than they are, and the judgement call about which problems you solve alone — your role explicitly includes independently solving smaller ones — and which you pass on. These are exactly the behaviours the scenarios below rehearse: user focus, collaboration, ownership, escalation, honesty, and inclusion.

A final reassurance: situational judgement grows through reflection as much as experience. Each scenario here is a safe rehearsal for something you may genuinely face. Thinking it through calmly now — with no stakes and a full explanation afterwards — is precisely how good judgement gets built.

### How this assessment maps to your role

The judgement dimensions map directly to the named skills in your role summary:

- **Integrity under pressure** maps to your core duty of maintaining CMDB integrity and your **Asset and configuration management** skill: the database is only trustworthy if its records reflect reality even when reality is inconvenient — before audits, above all.
- **Process discipline with helpfulness** maps to your **Change management** skill: applying change control procedures under supervision means declining undocumented shortcuts while actively helping requesters use the proper route — firm on the standard, generous with the path.
- **Escalation judgement** maps to your **Ownership and topic** skill: showing awareness of problem resolution processes and passing problems to your team is the defined behaviour at your level. Knowing which problems are yours — "smaller" ones you solve independently — and which to raise is a scored skill, not a confession of limits.
- **Routing and information gathering** maps to your **Incident management** skill: identifying and registering incidents, gathering the required information, and allocating them to the appropriate channel is a daily judgement the scenarios rehearse directly.
- **Working well with others** maps to your **Community collaboration** skill: contributing to others' work, helping create the right environment, and recognising and dealing with issues — including quiet interpersonal ones — are assessed behaviours.
- **Serving the people behind the records** maps to your **User focus** and **Service focus** skills: awareness that every record, request, and process ultimately serves colleagues and citizens keeps your judgements anchored in outcomes rather than paperwork for its own sake.

### Practice questions

**Question 1 (easy) — "Just tweak the record"**

An engineer messages you: "The record for LDS-WIN-021 shows the wrong rack. It's in C1, not B4 — I moved it myself last week. Can you just update it? No time for a data correction request today, I'm mid-migration." Your procedure requires every edit to reference an approved change or data correction request. What is the most effective response?

- A) Update the record — the engineer has first-hand knowledge, and the CMDB should reflect reality as soon as possible.
- B) Refuse and tell them to come back when they have raised the request.
- C) Explain that edits need a reference, offer to raise the data correction request yourself using the details they have just given you, and make the edit as soon as it is approved.
- D) Update the record now and raise the request retrospectively when you have time.

**Correct answer: C**

**Explanation:** Option C keeps both things that matter: the control (every edit traceable to an approved reference) and the outcome (the record corrected quickly, the busy engineer helped rather than bounced). Raising the request yourself is squarely within your administrative support duties, costs a few minutes, and turns a process refusal into a service. Option A abandons the control — and notice that "first-hand knowledge" is exactly what the reference documents; without it, the audit trail shows an edit justified by nothing. It also sets a precedent: this engineer, and everyone they mention it to, now knows edits are available on request. Option B protects the process and fails the person; the migration will finish, the request will be forgotten, and the record will stay wrong — a process victory and a data defeat. Option D inverts the control ("approve then act" becomes "act then perhaps document") and depends on your memory during a busy day. The scored pattern at your level is C's shape: hold the line, carry the load. People stop fighting a process when the person running it makes compliance the easy option.

**Question 2 (easy) — An error in your manager's work**

While preparing records for the change advisory board papers, you notice that a dependency your change and release manager added to the CMDB last week links the payroll application to the wrong database server — you are confident it should be DB-HR, not DB-FIN. The papers go out tomorrow morning. What is the most effective response?

- A) Say nothing — correcting your manager could seem presumptuous, and they probably know something you do not.
- B) Quietly fix the record without mentioning it, so the papers are right and nobody is embarrassed.
- C) Tell your manager today what you found and why you believe it is wrong, so the record and the papers can be corrected before they go out.
- D) Mention it to a colleague and ask them to raise it with the manager.

**Correct answer: C**

**Explanation:** Option C treats the finding exactly as your role should: data integrity is the duty, and the person who can confirm the correction fastest is the person who made the entry. Going today respects tomorrow's deadline; explaining why you believe it is wrong ("the HR portal's dependency map and last month's change record both show DB-HR") makes the conversation evidence-based rather than presumptuous — and leaves room for the possibility option A gestures at, that your manager knows something you do not. If they do, you learn it; if they do not, the papers are corrected. Either outcome is good, which is the signature of a strong response. Option A lets a known-suspect record flow into governance papers — silence out of deference is still silence, and a wrong dependency in CAB papers could misdirect a real impact assessment. Option B is the subtle trap: the record ends up right, but your manager walks into the board unaware their papers changed, the edit lacks the conversation that might have revealed context, and quiet corrections of a supervisor's work — however well-meant — corrode trust in both directions. Option D outsources a conversation you are perfectly entitled to have; it adds a lap and a whisper. Managers worth working for want option C from their analysts, and the ones you will learn most from will thank you for it specifically.

**Question 3 (easy) — A corridor report**

A colleague from the finance team stops you at the kettle: "You're the computer records person, right? My laptop's been crashing all week and I lose my spreadsheets every time. Can you sort it?" No ticket exists. What is the most effective response?

- A) Explain that you maintain the configuration database, not laptops, and suggest they contact someone else.
- B) Take the laptop's asset number, promise to look into the crashes yourself, and add it to your list.
- C) Sympathise, capture the key details (asset number, what happens, since when), register the incident through the service desk channel so it reaches the right team with the information attached, and give them the reference number.
- D) Tell them to log a ticket with the service desk when they get a chance.

**Correct answer: C**

**Explanation:** This is your incident management skill verbatim — identify and register incidents, gather the required information, allocate to the appropriate channel — wrapped in ordinary human decency. Option C does the routing and does it warmly: the colleague leaves the kettle with a reference number and the sense that something is now in motion, and the fixing team receives a well-formed ticket with the asset number attached (which, pleasingly, your CMDB knowledge makes better than most people's tickets). Option A is technically accurate about your job description and completely unhelpful about the situation; "not my area" answers a question nobody asked. Option D points at the right channel but leaves the work and the momentum with the person least equipped to know what details matter — most corridor reports handled this way simply evaporate, and this one involves a colleague repeatedly losing work, which deserves better. Option B is kind and doubly wrong: crash diagnosis is not your role (the promise misroutes the problem to someone who cannot fix it), and an untracked personal promise bypasses the prioritisation that might reveal, say, five other finance laptops doing the same thing this week — a pattern only the proper channel can see. The general shape to remember: route properly, capture well, treat the person as a user of a service rather than an interruption to your day.

**Question 4 (moderate) — Unsure mid-task**

Your manager asked you to run a bulk update this afternoon: applying a new location code to 400 records following an office move, using a script the team has used before. Partway through preparing it, you notice the script's filter would also catch 30 records for assets in storage, which the office move should not affect. Your manager is in meetings until 5pm; the update was meant to be done by then. What is the most effective response?

- A) Run the update as instructed — your manager set the task, and 30 records out of 400 is a small proportion.
- B) Exclude the 30 storage records yourself, run the update for the remaining 370, note exactly what you changed and why, and let your manager know — flagging the 30 for their decision.
- C) Pause the whole task until you can speak to your manager at 5pm, missing the deadline.
- D) Run the update on all 400, then correct the 30 storage records afterwards if your manager confirms they were wrong.

**Correct answer: B**

**Explanation:** Test each option against what you actually know. You are confident the 370 genuinely moved — that part of the task is unambiguous, within your competence, and deadline-bound: do it. You suspect the 30 storage records should not change — and your suspicion is well-founded, since assets in storage do not move with an office. Excluding them is the cautious action for the doubtful subset: it leaves those records exactly as they were, which is reversible by definition, while a wrong update is only reversible with more work and a second edit trail. Option B therefore completes the certain work, protects the uncertain records, documents the judgement, and hands the residual decision to the right person — independent problem-solving sized precisely to your level. Option A knowingly writes 30 probable errors into the database to honour the letter of an instruction; "my manager told me to" is a poor caption for avoidable bad data, and managers set filters expecting analysts to notice what filters catch. Option D is option A with an apology scheduled: it prefers editing records twice to pausing once. Option C treats one doubtful subset as if it poisoned the whole task, missing a deadline that 92% of the work never threatened. The transferable principle: when part of a task turns doubtful, separate the certain from the uncertain, act on the certain, hold the uncertain, and communicate. That is what "applying procedures under supervision" looks like when the supervisor is in a meeting.

**Question 5 (moderate) — Tidying the numbers before an audit**

Three days before an external audit, a senior colleague reviewing your reconciliation report says: "These 14 unresolved discrepancies look bad. Most are probably just scan glitches — mark them resolved, and if any turn out to be real we'll fix them after the audit." You have not yet investigated the 14, so you do not know which are glitches. What is the most effective response?

- A) Mark them resolved as suggested — the colleague is senior and is probably right about scan glitches.
- B) Explain that you cannot mark uninvestigated discrepancies as resolved, propose spending the three days investigating as many as possible so the genuine number is as small — and as true — as you can make it, and let your manager know the position.
- C) Mark them resolved but keep a private list so you can investigate later.
- D) Refuse, and tell the auditors on day one that you were asked to falsify the report.

**Correct answer: B**

**Explanation:** Strip the scenario to its core: you are being asked to record as fact ("resolved") something nobody has established, to make a report look better for an audit — that is falsification, however casually proposed and however probable the glitch theory. Option B declines it cleanly and then does the genuinely useful thing: the three days are real time, glitches (if the colleague is right) are quick to confirm and close honestly, and every discrepancy you truly resolve improves the report by the only route that survives an auditor's question "how was this resolved, and when?" Looping in your manager is proportionate: they own the audit position and should not learn of it in the room. Option A trades your professional integrity for deference — and note that "probably right" is doing all the work; auditors sample, and one "resolved" discrepancy that reopens under sampling costs more credibility than fourteen honest open items, because it poisons trust in everything else marked resolved. Option C is quiet complicity with a guilty conscience attached — the report still lies. Option D rockets past every intermediate step: the colleague made a poor suggestion, you declined it, nothing false has been recorded; escalating to external auditors as a first move treats a correctable moment as a scandal and would be a serious misjudgement — though if pressure continued after your refusal, escalating internally through your manager would become exactly right. Remember the audit truth that seasoned practitioners live by: auditors do not expect perfect data; they expect honest data and a team that knows where its problems are. Fourteen open discrepancies with an investigation plan is a good look. It is called integrity.

**Question 6 (moderate) — An access request while your manager is away**

Your change and release manager is on leave today. An engineer you do not know well asks you to grant them edit access to the CMDB "for the afternoon" so they can update records for servers they are rebuilding: "The access request process takes two days, and the records will be wrong all week otherwise. You've got admin rights — it's two clicks." Granting access is technically possible for you but the procedure says access is approved by the change and release manager. What is the most effective response?

- A) Grant the access for the afternoon and remove it before you leave — the records staying accurate is what matters most.
- B) Decline to grant access, but offer to make the record updates yourself today from the engineer's information, and help them submit the access request through the proper route for the future.
- C) Decline and tell them to wait until your manager returns.
- D) Grant the access but email your manager so they know what you did.

**Correct answer: B**

**Explanation:** Separate what the engineer needs (accurate records this week) from what they asked for (your manager's approval authority, exercised by you). Option B serves the need fully while declining the authority: you making the edits keeps every change inside your own accountable, referenced access — the records are right today — and helping with the access request fixes next week too. Nobody waits, nothing is bypassed, and the security model your role's own summary emphasises (the change and release manager owns access to change activities) stays intact. Option A is the tempting one, and its flaw is worth seeing exactly: "two clicks" grants an unknown colleague edit rights that the approval step exists to consider — scope, need, duration, identity — and your removal-before-hometime plan is a memory-dependent control replacing a designed one. Access granted informally also never appears in the access review your auditors will one day run. Option D is option A plus a confession; notification is not authorisation, and it quietly transfers the awkwardness to a manager on leave. Option C protects the boundary and abandons the need — the records stay wrong for a week when you personally could have fixed them within the rules today; that is process used as a shield rather than a tool. The pattern that scores well, here as throughout: refuse the shortcut, absorb the legitimate work it was trying to reach, and route the requester onto the proper path for next time.

**Question 7 (moderate) — A colleague's recurring error**

A newer teammate keeps making the same mistake: when they register incidents, they record the model number in the serial number field. You have now quietly corrected eleven of their tickets over three weeks. They are enthusiastic, hard-working, and clearly have not noticed. What is the most effective response?

- A) Keep correcting the tickets — it takes you seconds, and pointing it out might dent their confidence.
- B) Report the pattern to your manager so it can be addressed through their probation review.
- C) Show them the pattern kindly and directly — ideally with one example ticket — explain why the distinction matters downstream, and mention it could be worth a note in the team's quick-reference guide since the two fields are easily confused.
- D) Post a general reminder in the team channel about using the correct fields, without naming anyone.

**Correct answer: C**

**Explanation:** Eleven corrections over three weeks is no longer an incident; it is a pattern with a simple cause and a kind, five-minute fix. Option C delivers it the way effective teams do: directly to the person (no audience), concretely (one example beats an abstract lecture), with the why attached (a wrong serial number sends an engineer to the wrong physical machine — the downstream harm makes the correction feel like help rather than pedantry), and with a systemic tail: if the fields are easily confused, the confusion is partly the form's fault, and a line in the quick-reference guide fixes it for every future joiner. That last move is your community collaboration skill in miniature — turning one person's stumble into the team's improvement. Option A confuses kindness with silence: it costs you time forever, denies the colleague the feedback they would plainly want ("three weeks and nobody told me?" stings far more than a friendly heads-up), and leaves every uncorrected ticket you miss carrying bad data. Option B escalates a coaching moment into a personnel matter — reaching for the probation review before a first conversation is both disproportionate and unkind, and it would rightly damage the colleague's trust in the team. Option D is the passive-aggressive classic: the one person who needs the message rarely decodes it, while everyone else wonders who it was about. Feedback given early, privately, and generously is one of the highest-value behaviours a team member can practise — and being known as someone who gives it that way is worth more than being known as someone who never mentions problems.

**Question 8 (challenging) — Evidence of an unauthorised change**

Reconciling the CMDB against the discovery scan, you find that a production server's memory was doubled some time in the past month. There is no change record, no data correction request, and the server sits in a cluster your organisation's most experienced infrastructure engineer looks after. Upgrading production hardware without a change record would breach change control. You do not know for certain the engineer did it, or whether an emergency change record exists somewhere you cannot see. What is the most effective response?

- A) Record the discrepancy and mention the missing change reference to your change and release manager, while asking the engineer neutrally whether they know the history — treating it as an unexplained discrepancy to be resolved, not an accusation.
- B) Update the CMDB to show the new memory size, since the scan proves the current reality, and move on.
- C) Email the engineer's line manager stating that an unauthorised change appears to have been made.
- D) Leave the CMDB unchanged until someone explains the discrepancy, so the database does not legitimise an unauthorised change.

**Correct answer: A**

**Explanation:** Hold on to what you actually have: a verified discrepancy (reality changed; no visible authorisation) and two honest unknowns (who, and whether an emergency record exists beyond your view). Option A handles each layer correctly. The discrepancy gets recorded — that is non-negotiable integrity work. The missing reference goes to your manager — change control breaches are precisely the class of problem your ownership skill says to pass upward, and your manager may have visibility you lack (that emergency record, for instance). And the engineer is asked as a source, not confronted as a suspect: "the scan shows this server's memory doubled — do you know the story?" is a question an innocent or authorised person answers easily, and it gathers the fact you are missing. Option B is subtle and corrosive: updating the record to match the scan makes the CMDB accurate about the hardware while erasing the trace of the governance gap — the discrepancy is the evidence, and reconciliation's job is to surface it, not launder it. Option D inverts the same mistake: the CMDB should reflect reality (with the discrepancy flagged and under investigation), because an incident responder tonight needs the true memory size regardless of who authorised it — accuracy and accountability are separate ledgers; keep both. Option C leaps to a conclusion you explicitly do not hold, in writing, to the person's manager, bypassing your own; if the engineer turns out to hold an emergency authorisation, that email cost you a working relationship and your judgement's reputation for nothing. The professional sequence — record faithfully, escalate through your line, inquire without accusing — protects the data, the process, and the people, in that order of certainty.

**Question 9 (challenging) — "Just mark them verified"**

The annual verification deadline is Friday, and 60 assets remain unverified — all in the basement store, all low-value peripherals. A teammate says: "Nobody audits the basement junk. Mark them verified — they were all fine last year, and we'll be down there in a month anyway for the disposal run. Missing the deadline looks worse than a formality." What is the least effective response?

- A) Mark the 60 assets as verified, as suggested.
- B) Tell your manager the honest position: the deadline will be met for all assets except 60 basement peripherals, and propose either a focused push to verify them by Friday or an agreed short extension for that batch.
- C) Spend an hour checking whether the basement batch can realistically be verified before Friday — 60 peripherals in one location may be a few hours' work.
- D) Suggest to the teammate that combining the verification with next month's disposal run be proposed to the manager as a formal re-plan, rather than done silently.

**Correct answer: A**

**Explanation:** The question asks for the least effective response, and it is A: recording sixty verifications that never happened. Look past the smallness of the stakes to the structure of the act — "verified" is a factual claim that a person confirmed an asset's existence, location, and state on a date; writing it falsely converts the CMDB's strongest field into decoration, and does so wholesale. The teammate's reasoning deserves dismantling because each plank recurs throughout working life: "nobody audits it" (audits sample precisely to catch what nobody expects to be checked — and basement stores are where ghost assets live); "they were fine last year" (last year's verification is last year's fact; that is the entire point of annual re-verification); "we'll be there next month anyway" (then propose that, openly — which is exactly option D's move). Meanwhile, notice that the effective options form a sequence rather than competitors: C first (an hour of feasibility checking may dissolve the whole dilemma — sixty peripherals in one room is plausibly a single afternoon), then B (the honest position, with two workable proposals, delivered before the deadline rather than after), with D as a legitimate variant of B that turns the teammate's own idea into an honest plan. That is the general lesson: almost every "just fudge it" suggestion contains a reasonable plan trying to get out — the fudge is the silence, not the schedule. Say the true thing to the person who owns the deadline, and the pressure usually resolves into an extension, a push, or a re-plan. Managers forgive missed deadlines flagged early far more readily than met deadlines that turn out to be fiction.

**Question 10 (challenging) — Your independent fix keeps coming back**

Last month you noticed mobile phone records were being created without asset tags, worked out that the onboarding form had a broken field, arranged the fix with the form's owner, and cleaned up the affected records — a tidy piece of independent problem-solving. This week untagged phone records are appearing again: the form's owner rolled back their system to an earlier version, restoring the broken field, and mentions their team does this "most months" during their release cycle. What is the most effective response?

- A) Fix the form again and re-clean the records — your previous solution worked; it just needs re-applying.
- B) Recognise this as a recurring problem with a systemic cause beyond your reach, raise it to your change and release manager with the pattern documented — the fix, the rollback cycle, the recurrence — and suggest what a durable remedy might need, such as the fix being incorporated into the other team's baseline version.
- C) Ask the form's owner to email you before every rollback so you can re-apply the fix each time.
- D) Add a weekly task to your own calendar to check for and clean up untagged phone records.

**Correct answer: B**

**Explanation:** The scenario is a scale test: it hands you a problem that has outgrown the "smaller problems" your role solves independently, and watches whether you notice. Last month's judgement was right — one broken field, one owning team, one fix: analyst-sized. But the recurrence reveals the true shape: the other team's release cycle systematically reverts the fix, which means the durable remedy lives inside their versioning practice — their baseline must carry the correction — and influencing another team's release discipline is a conversation between owners, not something you can arrange from the side. Option B is your problem management skill executed exactly as written for your level: investigate the pattern (done — and your documentation of fix, rollback, recurrence is what makes the escalation land), understand the level of the problem (it has moved from operational to tactical — a process interaction between teams), and contribute to the remedy while passing the problem to where it can actually be killed. Options A, C and D are three costumes on the same mistake — treating a recurring systemic problem as a repeating local one. A signs you up for a monthly ritual of re-fixing; C builds a permanent workaround on the courtesy of a team already too busy to preserve your fix; D institutionalises the symptom into your own workload forever, quietly hiding the problem's cost inside your calendar where no one will ever see it well enough to fix it. Escalating here is not giving up on your fix — it is finishing it. The analyst who can say "I solved this once, it recurred, here is why, and here is where the durable fix lives" is demonstrating more capability than the one still heroically re-cleaning records in month eleven.

**Question 11 (challenging) — The colleague nobody briefs**

Your team of four includes a part-time colleague who works Wednesday to Friday. You have noticed a pattern: decisions and context from Monday and Tuesday — new conventions agreed, priorities shifted, quirks discovered — reach the full-timers by osmosis but often never reach her. Twice this month she has spent her Wednesday morning doing work that Monday's decisions had made unnecessary, and in Thursday's meeting she was corrected for using a naming convention that changed while she was off. She has started apologising for "always being behind". You are not the team lead. What is the most effective response?

- A) Reassure her privately that nobody minds and that being part-time inevitably means missing things.
- B) Start a simple shared decisions log the whole team keeps, tell her about Monday–Tuesday changes yourself in the meantime, and suggest to the team lead that briefing part-time colleagues on what changed be made a standing habit rather than luck.
- C) Suggest she switch to full-time hours if she wants to stay properly informed.
- D) Mention to the team lead that she seems to be struggling to keep up.

**Correct answer: B**

**Explanation:** Diagnose before prescribing: she is not "behind" — the information flow is broken, and it breaks along the line of her working pattern. That framing matters, because three of the four options quietly accept the wrong diagnosis. Option A is warm and defeatist: "inevitably means missing things" tells her to keep absorbing a fixable structural problem as a personal cost — and her apologising for it is precisely the sign it is being personalised. Option C "solves" the exclusion by asking her to stop being part-time — inclusion by assimilation, which is no inclusion at all; working patterns are exactly the kind of difference a well-run team accommodates by design. Option D reports her as the problem ("struggling to keep up") when your own observation shows the team's habits are the problem; that framing could follow her into performance conversations she does not deserve. Option B fixes the mechanism at three levels, none requiring authority you lack: a decisions log helps everyone (full-timers forget Monday's decisions too, and future joiners inherit a history); the interim personal briefing costs you five minutes a week and stops this Wednesday's waste immediately; and the suggestion to the team lead converts a peer's workaround into a team norm — recognising and dealing with issues in the team environment is your community collaboration skill, verbatim. This is what inclusion mostly looks like in practice: not grand gestures, but someone noticing whose chair the information never reaches, and re-plumbing the flow so it does. Teams that fix these small structural leaks keep their part-time colleagues; teams that let people apologise for the rota lose them.

**Question 12 (challenging) — Credit where it is not due**

At the quarterly service review, a senior manager praises the CMDB accuracy improvement — from 84% to 93% — and congratulates the change and release manager, who accepts the praise and moves on. You know the improvement came almost entirely from a data-cleansing method a junior teammate designed and ran over three months; your manager was barely involved and knows it. The junior teammate is not at the meeting. Afterwards, the teammate hears second-hand what happened and tells you, flatly, "That's the last extra effort I put in here." What is the most effective response?

- A) Advise the teammate to let it go — credit drifts upward in every organisation, and complaining changes nothing.
- B) Tell the senior manager directly at the next opportunity that your manager took false credit.
- C) Encourage the teammate to raise it with the change and release manager themselves, and separately mention to your manager — factually, without accusation — that the teammate designed and ran the cleansing work and is feeling unrecognised; managers often correct this readily once aware it landed badly.
- D) Post the true story in the team channel so everyone knows who did the work.

**Correct answer: C**

**Explanation:** Be precise about what happened before choosing a response to it. A manager accepting praise for their team's results is ambiguous — in many organisations, a team's outcome is credited to its head as a matter of course, and no deception was necessarily intended; what is unambiguous is the effect: the person who did the work feels erased, and has told you the consequence in plain words ("the last extra effort"). Option C addresses the effect through the two people who can actually repair it. Encouraging the teammate to speak for themselves respects their ownership of their own work — advocacy that replaces someone's voice, however well-meant, repeats the erasure in a kinder key. Your separate, factual mention to the manager does what a colleague can legitimately do: supply the information ("the cleansing method was Sam's design; I think the review left them feeling invisible") and let the manager choose the repair — a follow-up note to the senior manager, public recognition at the next team meeting — which most managers, faced with the fact, make quickly. Option A is corrosive counsel: it converts one bad afternoon into a settled cynicism, confirms the teammate's decision to stop trying, and abandons a fixable situation — motivation, once taught that effort is invisible, is expensive to win back, and your community collaboration skill names exactly this: recognising and dealing with issues in the team environment. Option B storms the hierarchy with an accusation ("false credit") that outruns your evidence about intent, bypasses your manager's chance to fix it themselves, and turns a repairable oversight into a standoff. Option D performs the correction as a public shaming — the truth, weaponised, at maximum relationship cost. The deep pattern, worth carrying into every credit dispute you will ever witness: fix the recognition, not the scoreboard. The goal is the teammate seen and the work honoured — not the manager convicted.

### Preparation tips

- **Learn where your authority's edges are.** Which edits, approvals, and accesses are yours, and which belong to your change and release manager? Knowing the boundary cold makes half these dilemmas easy — and it is genuinely useful this week, not just on test day.
- **Rehearse "hold the line, carry the load".** The strongest analyst answers pair a firm no to the shortcut with active help toward the proper route. Practise spotting the option with both halves.
- **Separate certain from uncertain.** When a scenario mixes what you know with what you suspect, the best response usually acts on the certain, protects the uncertain, and communicates about both.
- **Watch for the falsification tells.** "Mark it resolved", "mark it verified", "we'll sort it after the audit" — any option that records an unestablished fact is almost always the worst on offer, whatever the stakes' apparent size.
- **Prefer the conversation to the escalation, and the escalation to the silence.** Direct, kind, early conversations solve most things; your manager handles what conversations cannot; silence solves nothing. Options usually sit on exactly this ladder.
- **Read the question stem twice.** "Most effective" and "least effective" are one word apart and score in opposite directions. Underline which you are answering.
- **Debrief real dilemmas.** After each tricky moment at work, privately name the four responses you could have chosen and rank them. A month of this builds sharper judgement than any question bank.

### Common pitfalls to avoid

- **Trading integrity for tidiness.** Clean-looking reports, met deadlines, and matched numbers are worthless when manufactured. The least effective option is nearly always the one that makes data lie, however small.
- **Confusing deference with judgement.** "They're senior, so comply" fails whenever the request is improper. Seniority changes the tone of your response, never its substance.
- **Playing the lone hero.** Granting access informally, re-fixing systemic problems forever, secretly redoing others' work — self-reliance beyond your remit scores poorly because it fails in real life.
- **Using process as a shield.** "Come back with a form" without help is the mirror-image error: technically compliant, practically obstructive. The scored answers keep the control and serve the person.
- **Escalating before conversing.** Going to managers, line managers, or auditors before trying the direct, kind conversation usually ranks low — except where integrity or security is at stake, when prompt escalation through your own line ranks high.
- **Personalising structural problems.** When a scenario shows someone repeatedly disadvantaged — by the rota, the form, the meeting habits — the strong answer fixes the mechanism, not the person.
- **Answering as the manager.** Your scored level is excellent analyst judgement: safe hands, honest records, well-timed escalation, generous collaboration. Options that quietly exercise your manager's authority are traps, not ambition.

## Conclusion

Well done for working through this guide — that was a genuinely substantial piece of professional development, and finishing it is worth pausing to acknowledge.

Look back at what you have practised. In the cognitive section, you caught the broken naming convention, reasoned from access rules to what an audit log does and does not prove, found the record whose fields could not all be true at once, traced dependencies to their real impact, and reconciled three disagreeing sources into one explained figure. In the numeric section, you computed accuracy rates and weighted averages the honest way, scaled a sample to a database, worked a backlog's net rate, and turned ghost records into a payback period a budget-holder would act on. In the verbal section, you held statements strictly to what the standard actually said, learned what "exactly one", "should", and "must not leave the building" each precisely permit, and saw how a well-written correction request gets answered in a day while a vague one waits weeks. And in the situational judgement section, you rehearsed the moments that define a configuration analyst's reputation: declining the undocumented shortcut while carrying the legitimate load, raising the error in a manager's work today rather than never, refusing to mark the unverified as verified, and noticing whose chair the information never reaches.

Here is the encouraging thread that ties it together: none of this was really test preparation in disguise. Base-checking a percentage, verifying before recording, reading a procedure branch by branch, escalating the problem that has outgrown you — these are the daily craft of maintaining a CMDB people can trust. Practising for the assessment and getting better at your job are the same activity, which means every hour you spent here pays twice.

If you carry three habits forward, choose these. First, record only what is established: "verified" means someone verified it, "resolved" means someone resolved it, and the honest "unverified" or "cannot say" is the mark of an analyst whose other entries can be believed. Second, hold the line and carry the load: the process stays intact and the person still gets helped — that combination, more than any technical skill, is what makes colleagues stop routing around the process and start trusting it. Third, size your problems honestly: solve the smaller ones with the independence your role celebrates, and pass the recurring, systemic ones upward with the pattern documented — both halves are skill, and knowing which half you are in is the skill above them.

Keep practising in short, regular sessions, return to whichever section stretched you most, and be patient with yourself: precision and judgement are built exactly the way you have been building them here, one worked question at a time. The care you bring to records that few people see is what keeps services running for the many people who never know your name — and there is real professional pride to be taken in that. Good luck with your assessment: you are better prepared than you think.
