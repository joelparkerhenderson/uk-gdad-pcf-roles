# Infrastructure Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as an infrastructure engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For an infrastructure engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — build sheets, configuration files, monitoring dashboards, physical and logical designs, test scripts, capacity reports, and change records — and the kinds of decisions you genuinely make: building and configuring infrastructure solutions according to departmental policy, owning an issue until it is resolved or properly handed over, translating logical designs into physical designs, working with third parties who provide infrastructure services, and troubleshooting problems across different technology capabilities.

Why do these assessments matter for your role in particular? At your level you have moved beyond supervised support into genuine independent delivery. You build, configure, administer, and support solutions and services — networking and physical infrastructure, COTS software, open source packages, virtual and cloud computing — and other people rely on your work being right. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting the configuration that breaks the pattern, calculating whether a storage volume will survive until the next procurement, extracting precise obligations from a supplier contract clause, and choosing the most professional course of action when a change goes wrong at the worst possible moment.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it for this role, a mapping of the assessment dimensions to the specific named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The questions progress from easy through moderate to hard, and every scenario is drawn from realistic infrastructure engineering work in a UK government context.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format before you meet it for real. Second, attempt the practice questions honestly — commit to an answer before reading the explanation. Third, treat every explanation as a mini-lesson: even when you answer correctly, the worked reasoning will sharpen your technique, and each explanation ties the technique back to a specific part of your job. Fourth, use the preparation tips and pitfalls sections for self-reflection: they connect assessment performance to your professional development as an engineer who delivers services that internal users and the public depend on.

Assessments reward calm, methodical thinking — which is also what good infrastructure engineering rewards. The habits you practise here are the habits that make changes succeed, incidents shorter, and documentation trustworthy. Take your time, work through each section honestly, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of shape sequences and letter grids, it presents you with the everyday materials of your job — configuration files, firewall rule sets, DNS records, patching schedules, dependency maps, and design documents — and asks you to reason quickly and accurately about them.

The typical format is an online, timed test lasting 15 to 30 minutes, with 20 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group of professionals at a similar level, and modern platforms often adapt question difficulty to your performance — so a test that feels increasingly hard is usually a test you are doing well on. Employers typically receive a breakdown of speed versus accuracy rather than a single score, which means disciplined, careful work is rewarded alongside pace. Short ungraded practice questions are normally offered before the timed section starts.

For an infrastructure engineer, cognitive assessment is particularly relevant because your core professional value is precise, structured thinking applied to systems. A firewall rule set is a logic problem. A configuration drift report is an error-checking exercise. An incident with three plausible causes is a deduction problem with real stakes. When you translate a logical design into a physical design, you are performing exactly the kind of systematic mapping these tests measure — and when you troubleshoot across compute, storage, and networking, you are running hypothesis-driven elimination under time pressure. Employers use these assessments because they predict how reliably an engineer will do all of that on an ordinary Tuesday, with a change window closing and a service owner waiting.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **IT infrastructure** skill: building, configuring, administering, and supporting solutions means working daily with structured artefacts — naming conventions, address schemes, rule sets, version matrices — where the anomaly that breaks the pattern is the defect you are paid to find.
- **Logical deduction** maps to your **Systems design** skill: translating logical designs into physical designs and producing detailed designs requires valid step-by-step reasoning — if the design requires resilience across two sites, what physically follows? It also maps to **Information security**, because security controls are conditional rules that must be applied exactly.
- **Error checking** maps to your **Systems design** duty to effectively document all work using required standards, and to your **Testing** skill: correctly executing test scripts means noticing every mismatch between expected and actual results.
- **Prioritisation** maps to your **Ownership and topic** skill — owning an issue until a new owner is found or the problem is mitigated or resolved forces constant judgements about what to do first — and to your duty to ensure services are delivered and used as required.
- **Applied problem solving** maps to your **Troubleshooting and problem resolution** skill (troubleshooting and identifying problems across different technology capabilities) and your **Problem management** skill (investigating problems in systems, processes, and services, and understanding whether a problem is strategic, tactical, or operational).
- **Working with structured tools** maps to your **Coding and scripting** skill: describing the scripting tools currently in use presumes you can follow the logic a script encodes — loops, conditions, and order of operations are pure applied deduction.

### Practice questions

**Question 1 (easy) — Pattern recognition in a configuration standard**

Your team's standard for virtual machine names is: environment code (P for production, T for test), two-letter service code, role code (WEB, APP, DB), and a two-digit sequence number — for example, PHRWEB01 is production HR web server 1. A build sheet lists:

1. PHRWEB01
2. THRAPP02
3. PFIDB01
4. PFIWEB1
5. TFIAPP03

Which entry breaks the standard?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: C**

**Explanation:** Decompose each name against the four-part rule. Entry 1: P + HR + WEB + 01 — valid. Entry 2: T + HR + APP + 02 — valid. Entry 3: P + FI + DB + 01 — valid. Entry 4: P + FI + WEB + 1 — the sequence number has one digit, not two; the standard requires "01". Entry 5: T + FI + APP + 03 — valid. A single missing zero looks trivial, but automation does not forgive it: scripts that select servers by pattern, monitoring rules, and backup selections all key on exact formats, so PFIWEB1 could silently fall outside every automated process that expects PFIWEB01. The technique — parse each candidate into its component fields and validate each field — is the same discipline you apply when reviewing build sheets before provisioning, and it is faster and more reliable than reading names whole.

**Question 2 (easy) — Logical deduction from a firewall policy**

Departmental policy states: "Inbound connections from the internet are permitted only to servers in the DMZ network. Servers in the internal network may receive connections only from the DMZ or from other internal servers." A colleague proposes a design in which an internet-facing monitoring service connects directly to a database server in the internal network. Which one of the following must be true?

- A) The proposal complies with policy because monitoring traffic is read-only.
- B) The proposal does not comply with policy as stated.
- C) The proposal complies if the database server has a strong password.
- D) The policy does not cover monitoring services.

**Correct answer: B**

**Explanation:** Apply the rules literally. The database server is in the internal network. Policy permits internal servers to receive connections only from the DMZ or other internal servers. An internet-facing service connecting "directly" is neither, so the connection is not permitted: the proposal breaches policy as stated — option B. Option A invents an exemption for read-only traffic that the policy does not contain; the rules constrain sources of connections, not their purpose. Option C confuses authentication strength with network policy — a strong password does not relocate the traffic source. Option D is wishful: the policy covers "inbound connections" generically, which includes monitoring. The compliant design would place a relay or collector in the DMZ. This is precisely how you exercise your **Information security** skill in design reviews: test the proposal against the control's exact wording, and if the words forbid it, the fix is to change the design, not to reinterpret the control.

**Question 3 (easy) — Error checking expected versus actual test results**

You are executing a test script for a new file service. The script's expected results and your recorded actuals are:

| Step | Expected | Actual |
|---|---|---|
| 1. Map drive | Drive maps as S: | Drive maps as S: |
| 2. Create file | File created, owner = tester | File created, owner = tester |
| 3. Set read-only permission | Other users can open but not edit | Other users cannot open |
| 4. Delete file | File moves to recycle store | File moves to recycle store |

Which step should be recorded as failed?

- A) Step 1
- B) Step 2
- C) Step 3
- D) Step 4

**Correct answer: C**

**Explanation:** Compare each expected/actual pair exactly. Steps 1, 2, and 4 match word for word. Step 3 does not: the expectation is "open but not edit" (read access preserved, write access removed), while the actual is "cannot open" (all access removed). The permission applied is more restrictive than designed — and "more secure than intended" is still a defect, because users who legitimately need to read the files cannot. This is the core discipline of your **Testing** skill: a test passes only when the actual result matches the expected result, not when the result seems broadly acceptable. Recording step 3 as failed, with the exact observed behaviour, gives whoever fixes it the information they need. The habit of reading both columns completely — rather than pattern-matching on the first few words — is what separates trustworthy test records from optimistic ones.

**Question 4 (easy) — Prioritising a morning workload**

You arrive to find four items: (1) an alert that a production web server's certificate expires in 48 hours; (2) a request from a project manager for a test server build, needed next week; (3) a monitoring warning that a development server's disk is 85% full; (4) an incident ticket — a shared printer used by one team is offline. Which item should you address first?

- A) Item 2, because project work drives delivery dates
- B) Item 1, because an expired certificate will cause a production outage with a known deadline
- C) Item 3, because disk alerts always precede failures
- D) Item 4, because incidents always outrank other work

**Correct answer: B**

**Explanation:** Weigh impact against urgency. Item 1 combines high impact (a production service will fail or show security warnings to every user when the certificate expires) with a hard, known deadline (48 hours, and renewal plus deployment takes time) — it is both important and urgent. Item 4 is an incident, but its impact is one team's printing — worth handling soon, not first; option D's "incidents always outrank" is a rule of thumb, not a law, and priority frameworks rank a pending production outage above a minor live one. Item 3 is a development system at 85% — worth a scheduled clean-up, low urgency. Item 2 has a week of runway. The professional pattern, central to your **Ownership and topic** skill, is to rank by impact-weighted urgency and then communicate: a quick note to the printer team and the project manager stating when you will get to their items turns your prioritisation into managed expectations rather than silence.

**Question 5 (moderate) — Pattern recognition in a DNS record review**

Your standard says every production application server must have: an A record (name to address), a PTR record (address to name), and a monitoring entry. You review four servers:

| Server | A record | PTR record | Monitoring |
|---|---|---|---|
| PFIAPP01 | 10.30.1.11 | 10.30.1.11 → PFIAPP01 | Yes |
| PFIAPP02 | 10.30.1.12 | 10.30.1.12 → PFIAPP02 | Yes |
| PFIAPP03 | 10.30.1.13 | 10.30.1.31 → PFIAPP03 | Yes |
| PFIAPP04 | 10.30.1.14 | 10.30.1.14 → PFIAPP04 | No |

How many servers have at least one defect against the standard?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: C**

**Explanation:** Check each server against all three requirements. PFIAPP01: A record, matching PTR, monitored — clean. PFIAPP02: clean. PFIAPP03: the A record points to 10.30.1.13, but the PTR record is registered against 10.30.1.31 — the digits are transposed, so forward and reverse resolution disagree: one defect. PFIAPP04: records match, but monitoring is "No": one defect. Two servers are defective — option C. The transposition in PFIAPP03 is the kind of error that hides in plain sight because 13 and 31 contain the same digits; mismatched reverse DNS then causes subtle failures in services that verify hostnames. The missing monitoring on PFIAPP04 is the more dangerous gap: an unmonitored production server fails silently. Reviewing a matrix row by row, requirement by requirement — rather than scanning for anything that "looks odd" — is exactly how you administer infrastructure reliably as part of your **IT infrastructure** skill.

**Question 6 (moderate) — Deduction through a script's logic**

A housekeeping script your team uses runs nightly with this logic: "For each log file in the target folder: if the file is older than 30 days AND larger than 100 MB, compress it. If the file is older than 90 days, delete it (whether or not compressed)." Tonight the folder contains: File W — 95 days old, 50 MB; File X — 40 days old, 200 MB; File Y — 20 days old, 500 MB; File Z — 95 days old, 2 GB. What happens to each file?

- A) W deleted; X compressed; Y untouched; Z deleted
- B) W untouched; X compressed; Y compressed; Z compressed
- C) W deleted; X compressed; Y compressed; Z deleted
- D) W compressed; X compressed; Y untouched; Z deleted

**Correct answer: A**

**Explanation:** Apply each condition exactly. File W: 95 days old — the delete rule (older than 90 days) applies regardless of size, so W is deleted; note the compression rule's size condition (50 MB < 100 MB) is irrelevant because deletion does not depend on it. File X: 40 days old and 200 MB — older than 30 AND larger than 100 MB, so compressed; not older than 90, so kept. File Y: 20 days old — fails the age condition of the compression rule despite its 500 MB size (AND requires both), and is nowhere near deletion: untouched. File Z: 95 days — deleted. That is option A. The common errors: treating AND as OR (which would compress Y — option B), and assuming small old files escape deletion (option D keeps W). Reading compound conditions precisely is the essence of your **Coding and scripting** skill — scripts do exactly what their conditions say, never what the author hoped — and tracing logic on paper before running it is how engineers avoid deleting the wrong files at 2 a.m.

**Question 7 (moderate) — Error checking a physical design against a logical design**

A logical design states: "The application tier comprises two servers in an active-active pair, each in a different data hall, each connected to both network switches, with shared storage accessible from both halls." The draft physical design allocates: Server 1 — Hall A, connected to Switch 1 and Switch 2; Server 2 — Hall A, connected to Switch 1 and Switch 2; storage array — Hall B, accessible from both halls. Which single change makes the physical design match the logical design?

- A) Connect each server to only one switch
- B) Move Server 2 to Hall B
- C) Move the storage array to Hall A
- D) Add a third server in Hall B

**Correct answer: B**

**Explanation:** Map each logical requirement to the physical allocation. Two servers, active-active: present. Each connected to both switches: satisfied. Shared storage accessible from both halls: satisfied. "Each in a different data hall": violated — both servers sit in Hall A, so a single hall failure takes down the entire application tier, defeating the resilience the logical design intends. Moving Server 2 to Hall B (option B) restores the separation with one change. Option A would break a satisfied requirement. Option C merely relocates storage without separating the servers. Option D adds cost the design does not call for — three servers is a different design, not a corrected one. This translation check — walking requirement by requirement from logical to physical — is literally your **Systems design** skill: "translate logical designs into physical designs" means preserving every property the logical design encodes, and resilience properties are the easiest to lose because the design still works on a sunny day.

**Question 8 (moderate) — Prioritisation during an incident with a change pending**

At 14:00 you are mid-way through a scheduled, approved change: migrating file shares to a new server, currently at the step where both old and new servers are live and data is synchronising. At 14:10 the service desk reports a P2 incident: the email gateway is rejecting some external mail, affecting several teams, and you are the only engineer available with gateway knowledge. Your change window closes at 17:00, and rolling back or pausing the migration at this step is safe and documented. What is the most defensible course of action?

- A) Finish the migration first — approved changes take precedence over incidents.
- B) Pause the migration at the documented safe point, address the P2 incident, and resume or reschedule the migration depending on time remaining.
- C) Attempt to do both simultaneously, switching between tasks every few minutes.
- D) Ignore the incident — the service desk should find someone else.

**Correct answer: B**

**Explanation:** The scenario deliberately provides the fact that makes the decision safe: the migration has a documented safe pause point. A P2 incident affecting several teams' external mail has live business impact now; the migration's value is realised whenever it completes, and its window can be renegotiated. Pausing at a safe point, fixing the live impact, then making a clear-headed resume-or-reschedule decision (option B) protects users first and the change second — and both decisions remain controlled and documented. Option A inverts service priorities: changes exist to improve services, not to outrank their availability. Option C is the seductive wrong answer: context-switching between a live migration and a live incident invites errors in both — half-attention on a data synchronisation step is how migrations corrupt data. Option D abandons your **Ownership and topic** duty — you are the available engineer with the knowledge; ownership means taking the issue until a proper handover exists, not hoping one appears. Note also the communication step implied: telling the change approver about the pause keeps the change record honest.

**Question 9 (moderate) — Deduction from monitoring evidence**

Users on floor 3 report intermittent disconnections from all networked services. Users on other floors are unaffected. Your evidence: (i) floor 3 connects through switch SW3, which uplinks to the core switch; (ii) the core switch reports no errors on any port except the SW3 uplink port, which shows intermittent errors; (iii) SW3's own logs show no errors on any user-facing port; (iv) servers and services show no faults. What is the most probable location of the fault?

- A) The core switch's software
- B) The uplink link between SW3 and the core switch (cable, transceivers, or ports)
- C) Floor 3 users' devices
- D) The servers hosting the affected services

**Correct answer: B**

**Explanation:** Localise by intersecting the evidence. All floor-3 services are affected, but only floor 3 — so the fault sits on the path unique to floor 3, which is SW3 and its uplink. SW3's user-facing ports are clean (iii), which argues against many independent device problems (option C — also implausible because every user would need a simultaneous fault). Services are healthy for other floors (iv), eliminating option D. The core switch reports errors on exactly one port — the SW3 uplink (ii) — which points not at core switch software (option A would affect other ports or floors) but at that specific link: cable, transceivers, or the ports at either end. Option B names the segment where every symptom intersects. This is the elimination method at the heart of your **Troubleshooting and problem resolution** skill: draw the path, mark what is proven healthy, and the fault lives in what remains. Intermittent link errors also suggest the practical next step — check transceiver seating and cable integrity before replacing hardware.

**Question 10 (hard) — Multi-constraint scheduling of a build**

You must complete five build tasks for a new service: (1) rack and cable the hardware — 1 day; (2) install and configure the operating system — 1 day, requires task 1 complete; (3) configure storage — 1 day, requires task 2; (4) install the application — 1 day, requires task 3; (5) security scan — 1 day, requires task 4, and scans are only run by the security team on Tuesdays and Thursdays. Work starts Monday morning, one task per day, no weekend working. What is the earliest day the security scan can run?

- A) Friday of week 1
- B) Tuesday of week 2
- C) Thursday of week 1
- D) Monday of week 2

**Correct answer: B**

**Explanation:** Build the timeline. Monday: task 1. Tuesday: task 2. Wednesday: task 3. Thursday: task 4 — complete by Thursday evening. Task 5 requires task 4 complete, so the scan cannot run before Friday of week 1 — but scans run only on Tuesdays and Thursdays, and Friday is neither. Thursday of week 1 is impossible because task 4 finishes that same day (option C double-books the day). The next scan day after Thursday of week 1 is Tuesday of week 2 — option B. Options A and D ignore the security team's schedule constraint. The instructive point: the critical path is not simply the sum of task durations — it is durations plus resource availability windows, and the three-day wait (Friday to Tuesday) is pure calendar loss caused by missing a window by one day. In real planning, spotting this in advance lets you compress earlier tasks or negotiate the scan slot — exactly the coordination your role level's duty to ensure services are delivered as required implies.

**Question 11 (hard) — Root-cause deduction with a red herring**

A web application became slow at 09:00 and recovered at 11:30 without intervention. Facts: (i) a backup job on the application's database server ran from 02:00 to 03:15 — normal duration; (ii) the application's request volume this morning was typical; (iii) at 08:55 an operating system update began downloading, throttled to finish by 11:30, on the same virtual host that runs the application's database server; (iv) network monitoring shows the virtual host's storage traffic saturated from about 09:00 to 11:30; (v) a similar slowdown occurred last month on the same date. What is the most probable cause?

- A) The 02:00 backup job left the database in a degraded state.
- B) The OS update download saturated the virtual host's storage or network path, starving the database server from 09:00 to 11:30.
- C) Unusually high user demand overloaded the application.
- D) The application has a memory leak that clears itself every month.

**Correct answer: B**

**Explanation:** Align the timelines. The slowdown ran 09:00–11:30. The backup (option A) ended at 03:15 with normal duration — nearly six hours before onset, and nothing links its end state to a 09:00 start. Request volume was typical (ii), eliminating option C. The update download began at 08:55 and was throttled to finish at 11:30 — matching both onset and recovery almost exactly — and the saturation evidence (iv) covers the same window on the same virtual host that carries the database. Cause, mechanism, and timing all align: option B. Option D is built on fact (v), the deliberate red herring — a monthly recurrence pattern is consistent with a monthly scheduled update, which supports B rather than an unevidenced memory leak; leaks also degrade gradually, not with sharp start and end times. The technique from your **Problem management** skill: plot every event on one timeline, demand that a candidate cause explain both the start and the end of the symptom, and treat recurrence patterns as pointers to schedules. The preventative measure follows directly — re-time or rate-limit updates on hosts sharing storage with production databases.

**Question 12 (hard) — Integration interface reasoning**

You are building an interface that transfers staff records nightly from the HR system to the access-control system. The specification says: (i) the HR system exports at 01:00; the export takes up to 45 minutes; (ii) the access-control system imports whatever file is present at 02:00 exactly, and an import of a partial file corrupts its database; (iii) the network file copy between systems takes up to 20 minutes; (iv) your transfer job can be scheduled at any time and must never deliver a partial file. Which design is safest?

- A) Schedule the copy at 01:30, so the file arrives before 02:00.
- B) Schedule the copy at 01:50, leaving just enough time before the import.
- C) Have the HR export write to a temporary name, rename it to the final name only on completion; your job copies at 01:46 or later only if the final-name file exists, copying first to a temporary name at the destination and renaming on completion before 02:00.
- D) Copy the file continuously every five minutes so the latest version is always present.

**Correct answer: C**

**Explanation:** The hazard is partial files at either end. At 01:30 (option A) the export may still be running — up to 01:45 — so you could copy a half-written file. Option B starts after the latest export finish (01:45), but the copy itself takes up to 20 minutes, potentially still writing at 02:10 when the import already ran at 02:00 against a partial destination file. Option D makes the hazard continuous: some five-minute copy will inevitably catch the export mid-write. Option C engineers the hazard away with the write-then-rename pattern: a file only ever appears under its final name when complete, at both source and destination, so the 02:00 import can only ever see a whole file or no file — and "no file" is recoverable while corruption is not. The timing (01:46 earliest start + 20 minutes worst-case copy = 02:06) still risks missing the 02:00 import in the worst case, which option C's design converts from a corruption into a skipped night — the safest available failure mode, and a finding you would raise against the specification. This is your **Systems integration** skill in earnest: building and testing simple interfaces between systems is mostly about designing for the failure cases, and atomic rename is one of the most useful patterns in the trade.

### Preparation tips

- **Practise decomposition on real artefacts.** Take a build sheet, a firewall rule set, or a script from your own environment and check it field by field against its standard. This is the exact skill the test measures, using materials you already have.
- **Trace logic on paper.** For any conditional rule — script logic, policy clauses, backup schedules — write the conditions as a table and walk each case through. AND/OR confusion causes more errors than any other single factor.
- **Draw the path when troubleshooting questions appear.** A ten-second sketch of the components and connections makes elimination reasoning almost mechanical.
- **Time yourself progressively.** Start untimed for accuracy, then apply roughly 60–90 seconds per question. Infrastructure engineers usually have the accuracy; practice buys the pace.
- **Demand that causes explain the whole symptom.** In deduction questions, the right answer accounts for onset, recovery, and scope. Options explaining only part of the picture are distractors.
- **Rehearse with your monitoring data.** Yesterday's dashboards are free practice: pick an anomaly and reason to its most probable cause using only recorded evidence.
- **Use the platform's practice questions.** Interface familiarity removes a whole category of avoidable stress. Never skip the warm-up items.

### Common pitfalls to avoid

- **Scanning instead of parsing.** Anomalies like transposed digits and single missing characters are invisible to a skim. Parse structured data into fields and check each field.
- **Reading rules the way you wish they worked.** Policies and scripts mean exactly what they say. "Older than 30 days AND larger than 100 MB" spares a 500 MB file that is 20 days old, whether or not that seems sensible.
- **Letting one matching detail sell you an answer.** A distractor typically matches the scenario on one fact and fails on another. Verify every clause of the option you choose.
- **Prioritising by category labels.** "It's an incident" or "it's an approved change" are starting points, not verdicts — impact and urgency decide, and safe pause points change the calculus.
- **Anchoring on the first plausible cause.** The backup job that ran last night is the classic red herring. Check the timeline alignment before accepting any cause.
- **Ignoring resource windows in scheduling problems.** Task durations alone rarely give the answer; availability constraints (scan days, change windows, freeze periods) usually add the decisive delay.
- **Rushing the final options.** Under time pressure, candidates stop reading at the first acceptable answer. In hard questions the best answer is often option C or D, deliberately placed after a plausible-but-flawed earlier option.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your role genuinely produces: capacity figures, utilisation percentages, availability statistics, backup durations, licence counts, bandwidth calculations, and cost tables. The mathematics itself is deliberately modest — percentages, ratios, averages, rates, and reading tables and charts — because the test is not measuring mathematical education. It is measuring whether you can extract the right figures from realistic operational data, perform accurate calculations under mild time pressure, and interpret the result sensibly.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions, each presenting a small data set — a capacity table, an availability report, a supplier quote — followed by a multiple-choice question. Calculators are usually permitted (always check), rough paper is essential, and scoring compares accuracy and speed against a norm group. Adaptive difficulty is common.

For an infrastructure engineer, numeric fluency is not an adjacent skill — it is load-bearing. Capacity planning is division and rate-of-growth arithmetic. Availability reporting is percentage conversion. RAID and backup sizing are ratio problems. Bandwidth and transfer-window questions decide whether your migration plan is feasible before you ever touch a server. When you provide input on whether a service meets its targets, or sanity-check a supplier's invoice against the servers actually under support, arithmetic is the tool that turns opinion into evidence. Employers test numeric reasoning at this level because engineers who calculate confidently plan changes that fit their windows, size systems that survive their growth, and catch billing and capacity errors that others miss.

### How this assessment maps to your role

- **Percentages and capacity arithmetic** map to your **IT infrastructure** skill: building, configuring, and administering compute, storage, and networking means constant used-versus-total, headroom, and threshold calculations.
- **Rates, trends, and forecasting** map to your **Problem management** skill: investigating problems and contributing to preventative measures often begins with quantifying a trend — growth per week, errors per thousand requests — and projecting when it becomes an incident.
- **Averages and comparative statistics** map to your **Troubleshooting and problem resolution** skill: identifying the server whose metrics deviate from its peers requires accurate baselines and comparisons.
- **Reading tables and charts** maps to your duty to ensure services are delivered and used as required, and to your **Service focus** skill: establishing coherent frameworks from inputs starts with reading operational reports correctly.
- **Cost and licensing arithmetic** maps to your duty to work with and support third parties: supplier quotes, support tiers, and licence models are proportional-reasoning problems, and checking them protects public money.
- **Sizing and conversion calculations** map to your **Systems design** skill: producing detailed designs means committing to numbers — node counts, volume sizes, bandwidth requirements — that must be derived, not guessed.

### Practice questions

**Question 1 (easy) — Storage utilisation percentage**

A storage volume has a capacity of 2,000 GB and currently holds 1,440 GB. What is the utilisation percentage?

- A) 68%
- B) 70%
- C) 72%
- D) 76%

**Correct answer: C**

**Explanation:** Utilisation = used ÷ capacity × 100. Step 1: 1,440 ÷ 2,000 = 0.72. Step 2: 0.72 × 100 = 72%. Sanity check with landmarks: 70% of 2,000 is 1,400, and 1,440 is slightly above that, so the answer must sit just above 70% — confirming 72% and instantly eliminating 68%. Building the habit of bracketing an answer with easy reference points (halves, tenths) catches keying errors on the calculator. Utilisation figures drive real decisions in your **IT infrastructure** work — alert thresholds, expansion requests, and rebalancing between volumes — so moving fluently between gigabytes and percentages is daily currency.

**Question 2 (easy) — Average change duration**

Your last five file-server changes took 45, 60, 35, 70, and 50 minutes. You are asked for the average duration to help plan future change windows. What is it?

- A) 48 minutes
- B) 50 minutes
- C) 52 minutes
- D) 55 minutes

**Correct answer: C**

**Explanation:** Mean = total ÷ count. Step 1: sum the durations: 45 + 60 = 105; 105 + 35 = 140; 140 + 70 = 210; 210 + 50 = 260. Step 2: divide by 5: 260 ÷ 5 = 52 minutes. When planning windows, note that the average alone is not the whole story: the worst case here was 70 minutes, so a 52-minute window would have failed one change in five. A sensible window uses the average for scheduling density and the maximum (plus rollback time) for the window itself. Assessments usually ask for the plain mean, but the professional interpretation — mean for typical, maximum for safety — is worth carrying into your change planning, where an overrun against a closed window becomes an unauthorised change.

**Question 3 (easy) — Availability from downtime**

A service ran for a 30-day month (43,200 minutes) with two outages: one of 90 minutes and one of 40 minutes. What was its availability for the month, to one decimal place?

- A) 99.7%
- B) 99.5%
- C) 99.3%
- D) 98.7%

**Correct answer: A**

**Explanation:** Step 1: total downtime = 90 + 40 = 130 minutes. Step 2: downtime fraction = 130 ÷ 43,200 = 0.003009. Step 3: downtime percentage ≈ 0.3%. Step 4: availability = 100% − 0.3% = 99.7%. The subtract-from-100 route is faster and safer than computing uptime minutes (43,070 ÷ 43,200) directly, though both give the same answer. Common slips: using only one outage, or dividing by minutes in a week rather than the month. Availability arithmetic underpins the service reporting your role feeds into — and knowing that 130 minutes in a month is 0.3% helps you translate between the engineer's view ("two outages, one bad") and the service report's view ("99.7%"), which is exactly the bridging your role level performs between operations and management.

**Question 4 (easy) — Reading a patching compliance table**

The monthly security report shows:

| Estate | Servers | Fully patched |
|---|---|---|
| Production Windows | 80 | 72 |
| Production Linux | 50 | 46 |
| Test (all) | 70 | 49 |

Which estate has the highest patching compliance percentage?

- A) Production Windows
- B) Production Linux
- C) Test
- D) They are all equal

**Correct answer: B**

**Explanation:** Compute each percentage. Production Windows: 72 ÷ 80 = 0.90 = 90%. Production Linux: 46 ÷ 50 = 0.92 = 92%. Test: 49 ÷ 70 = 0.70 = 70%. Highest is Production Linux at 92% — option B. The trap is anchoring on absolute numbers: Windows has the most patched servers (72), but the question asks for the compliance rate. Note also what the comparison reveals operationally: test at 70% is the outlier worth investigating — test estates commonly lag because nobody owns their patching, yet unpatched test servers on the same network are still attack surface, which your **Information security** skill would flag. In reports, always establish whether a figure is a count or a rate before comparing rows; mixing the two is the most common misreading in operational meetings.

**Question 5 (moderate) — Forecasting disk exhaustion**

A database volume of 1,200 GB currently holds 840 GB. Analysis of the last eight weeks shows steady growth of 30 GB per week. The procurement process for additional storage takes six weeks from request to installation. If growth continues, how many weeks until the volume is 100% full, and is there enough time to procure more storage before then if you request it today?

- A) 12 weeks until full; procurement fits comfortably
- B) 10 weeks until full; procurement fits with 4 weeks to spare
- C) 12 weeks until full; procurement does not fit
- D) 8 weeks until full; procurement fits exactly

**Correct answer: A**

**Explanation:** Step 1: remaining capacity = 1,200 − 840 = 360 GB. Step 2: weeks to full = 360 ÷ 30 = 12 weeks. Step 3: compare with procurement: 6 weeks needed, 12 available — it fits with 6 weeks of margin, so option A. Option B miscalculates the headroom (it uses 300 GB). In practice you would not aim at 100% — databases misbehave well before a volume is literally full — so the working engineer's version targets, say, 90% (1,080 GB): (1,080 − 840) ÷ 30 = 8 weeks, which still accommodates six-week procurement but with only two weeks of margin, transforming "comfortable" into "request it today". This layered calculation — time to hard limit, time to safe limit, lead time — is capacity planning in its entirety, and it is how your **Problem management** skill converts a trend into a preventative measure instead of a 3 a.m. incident.

**Question 6 (moderate) — Backup window arithmetic**

A nightly backup must copy 4.5 TB of data, and the backup window is six hours. What minimum sustained throughput is required, in MB per second? (Use 1 TB = 1,000 GB and 1 GB = 1,000 MB.)

- A) About 125 MB/s
- B) About 208 MB/s
- C) About 750 MB/s
- D) About 21 MB/s

**Correct answer: B**

**Explanation:** Step 1: convert the data volume: 4.5 TB = 4,500 GB = 4,500,000 MB. Step 2: convert the window: 6 hours = 6 × 3,600 = 21,600 seconds. Step 3: required throughput = 4,500,000 ÷ 21,600 = 208.3 MB/s. So roughly 208 MB/s sustained — option B. Option A results from using 4 hours' worth of seconds incorrectly or mis-keying; option C from using minutes instead of hours somewhere; option D from a factor-of-ten slip. The defence against all of these is writing units at every step and cancelling them explicitly: MB ÷ seconds must give MB/s. Operationally, this number then drives design questions — can the storage read, the network carry, and the backup target write at 208 MB/s simultaneously? The lowest of those three is your real ceiling. Backup-window arithmetic is one of the most frequently needed calculations in your **IT infrastructure** work, because data grows and windows do not.

**Question 7 (moderate) — Percentage change in incident volume**

After you rebuilt a problematic print server, weekly printing incidents fell from 35 to 21. What was the percentage reduction?

- A) 14%
- B) 33%
- C) 40%
- D) 67%

**Correct answer: C**

**Explanation:** Percentage change = (old − new) ÷ old × 100. Step 1: reduction = 35 − 21 = 14 incidents. Step 2: divide by the original figure: 14 ÷ 35 = 0.4. Step 3: × 100 = 40%. Option A is the raw difference masquerading as a percentage. Option B comes from dividing by the new figure (14 ÷ 21 ≈ 67% — which is option D's error inverted; 21 ÷ 35 = 60%, and 100 − 60 = 40 confirms the answer by another route). Percentage-change questions hinge entirely on the base: reductions are measured against the starting value. Being able to state "the rebuild cut printing incidents by 40%" — accurately — is also how you evidence the value of your own work: your role's duty to ensure services are delivered as required is demonstrated with exactly this kind of before-and-after figure in service reviews.

**Question 8 (moderate) — Licence and cost check**

A supplier invoices your team £13,800 for annual monitoring-tool licences, stating "60 licences at £230 each". Your asset register shows 52 servers using the tool. Check the invoice arithmetic and the licence count. Which statement is correct?

- A) The arithmetic is right and the count matches the register.
- B) The arithmetic is right, but you are being billed for 8 more licences than the register supports; the difference is £1,840.
- C) The arithmetic is wrong: 60 × £230 is £12,800.
- D) The arithmetic is wrong and the count is wrong.

**Correct answer: B**

**Explanation:** Step 1: verify the multiplication: 60 × £230 = £13,800 — the arithmetic is correct, eliminating options C and D. Step 2: compare counts: invoiced 60 versus registered 52 — a difference of 8 licences. Step 3: value the difference: 8 × £230 = £1,840. So option B. The professional follow-up matters as much as the arithmetic: a count mismatch is a query, not an accusation — perhaps licences cover test servers not in your register, or perhaps the supplier's count is stale from before decommissioning. Your role's duty to work with and support third parties includes exactly this: reconciling supplier figures against your own records, raising discrepancies factually, and either correcting the bill or correcting the register. Either outcome improves accuracy, and £1,840 of public money justifies the ten minutes of checking.

**Question 9 (moderate) — Reading a utilisation trend chart**

A chart shows month-end memory utilisation for a virtualisation host over six months: March 58%, April 61%, May 65%, June 68%, July 72%, August 75%. The host must stay below 85% to guarantee failover capacity. If the trend continues at the same average monthly rate, in which month will the host first breach 85%?

- A) October
- B) November
- C) December
- D) January

**Correct answer: B**

**Explanation:** Step 1: find the average monthly growth: total rise = 75 − 58 = 17 percentage points over 5 intervals; 17 ÷ 5 = 3.4 points per month. Step 2: project forward from August's 75%: September ≈ 78.4%, October ≈ 81.8%, November ≈ 85.2%. Step 3: the first month at or above 85% is November — option B. October (option A) reaches only 81.8%, so it is the common off-by-one answer for anyone projecting from the wrong starting month or using 4 intervals. Two disciplines matter here: divide the total change by the number of intervals (5 gaps between 6 data points, not 6), and project from the last actual figure. Operationally, the answer buys you a planning horizon: roughly two months to migrate guests, add memory, or rebalance the cluster — a **Service focus** framework of "measure, project, act before the threshold" that turns monitoring history into scheduled work rather than emergencies.

**Question 10 (hard) — Weighted availability across services**

Your team reports availability for three services: Service A (email relay) 99.8%, Service B (file service) 99.2%, Service C (print service) 98.5%. The services handle 60%, 30%, and 10% of user activity respectively. What is the activity-weighted average availability across the three services?

- A) 99.17%
- B) 99.49%
- C) 99.62%
- D) 99.50%

**Correct answer: B**

**Explanation:** Weight each availability by its activity share and sum the products. Step 1: Service A: 99.8 × 0.60 = 59.88. Step 2: Service B: 99.2 × 0.30 = 29.76. Step 3: Service C: 98.5 × 0.10 = 9.85. Step 4: sum: 59.88 + 29.76 = 89.64; 89.64 + 9.85 = 99.49. The activity-weighted average availability is 99.49% — option B. Option A (99.17%) is the simple unweighted mean of the three figures, (99.8 + 99.2 + 98.5) ÷ 3, which is the classic error: it treats the little-used print service as equal in importance to the heavily used email relay, dragging the figure down unfairly. Options C and D are near-miss distractors designed to punish rounding guesses. Two lessons: first, each weight multiplies its own service's figure and the products then sum — check that the weights themselves total 100% before you start; second, re-verify the final addition by regrouping (59.88 + 9.85 = 69.73; 69.73 + 29.76 = 99.49) because transpositions in the last step are the most common calculation error. Weighted averages appear whenever services differ in size; reporting the unweighted mean misstates the experience your users actually had.

**Question 11 (hard) — RAID and usable capacity**

You are designing storage for a new file service. You have 12 disks of 4 TB each. Option 1: RAID 10 (mirrored pairs striped together) gives usable capacity of half the raw total. Option 2: RAID 6 gives usable capacity of the raw total minus two disks' worth. The service needs 30 TB usable. Which statement is correct?

- A) Only RAID 10 meets the requirement.
- B) Only RAID 6 meets the requirement.
- C) Both meet the requirement.
- D) Neither meets the requirement.

**Correct answer: B**

**Explanation:** Step 1: raw capacity = 12 × 4 TB = 48 TB. Step 2: RAID 10 usable = 48 ÷ 2 = 24 TB — below the 30 TB requirement, so RAID 10 fails. Step 3: RAID 6 usable = 48 − (2 × 4) = 48 − 8 = 40 TB — meets the requirement with 10 TB of headroom. Therefore only RAID 6 qualifies — option B. The arithmetic is simple; the design judgement it feeds is the point: RAID 10 buys performance and fast rebuilds at a 50% capacity cost, while RAID 6 buys capacity and double-disk failure tolerance at a write-performance cost. If the requirement had been 20 TB, both would pass and the decision would move to performance and rebuild-time criteria — showing how a capacity calculation is usually the first filter in a **Systems design** decision, not the whole decision. In detailed designs, always show this arithmetic explicitly: reviewers can then check the reasoning, which is what "effectively document all work using required standards" looks like in practice.

**Question 12 (hard) — Change window feasibility with combined tasks**

A migration change requires, in sequence: pre-checks (25 minutes), data copy of 300 GB over a link sustaining 100 MB/s, verification (35 minutes), and cutover (20 minutes). The agreed window is 03:00 to 06:00. Rollback, if needed, takes 30 minutes and must be complete by 06:00. By what time must you make the go/no-go rollback decision, and how much contingency does the plan have before that decision point? (Use 1 GB = 1,000 MB.)

- A) Decision by 06:00; contingency 50 minutes.
- B) Decision by 05:30; the plan finishes exactly at the decision point with no contingency.
- C) Decision by 05:00; contingency 10 minutes.
- D) Decision by 05:30; contingency 20 minutes.

**Correct answer: D**

**Explanation:** Work out the two halves separately: the decision deadline, then the plan duration. Step 1 — decision deadline: rollback takes 30 minutes and must be complete by 06:00, so the last safe moment to decide "roll back" is 06:00 − 30 minutes = 05:30. This is the binding constraint, not the raw window end — option A misses it entirely. Step 2 — copy time: 300 GB = 300,000 MB; 300,000 ÷ 100 MB/s = 3,000 seconds = 50 minutes. Step 3 — total planned duration: 25 + 50 + 35 + 20 = 130 minutes. Step 4 — finish time: 03:00 + 130 minutes = 05:10. Step 5 — contingency: the work should be verifiably complete by 05:10, and the rollback decision can be deferred until 05:30, so the plan can absorb 20 minutes of overrun before the decision point — option D. Option B assumes a 150-minute plan (a common slip: misreading the copy as 70 minutes); option C invents a 05:00 deadline by subtracting a full hour. The deeper lesson: window feasibility is task arithmetic plus the rollback deadline, and the rollback deadline almost always binds first. Showing exactly this calculation in your change record — durations, decision point, contingency — is what makes approvers trust your changes, and it is the numeric backbone of your duty to ensure services are delivered as required.

### Preparation tips

- **Drill the core four with operational examples.** Percentages, ratios, rates, and averages cover nearly every question. Practise on your own capacity reports and availability figures — familiarity with the context halves the reading time.
- **Write units at every step.** MB versus GB, minutes versus seconds, per-week versus per-month cause more wrong answers than the arithmetic itself. Make units cancel visibly on paper.
- **Count intervals, not data points.** Trend questions divide total change by the number of gaps between readings. Six months of readings contain five intervals.
- **Identify the base before dividing.** Percentage change uses the original value; compliance uses the required total; weighted averages use activity shares. Ask "out of what?" aloud if necessary.
- **Estimate first, calculate second.** A ballpark ("720 GB at 100 MB/s is about two hours") catches order-of-magnitude errors before they become confident wrong answers.
- **Rehearse backwards planning.** Change-window questions are solved from the deadline backwards — rollback deadline first, then each preceding task. Practise on your own recent changes.
- **Verify the final addition.** The last step of a multi-part calculation is where transpositions live. Re-add the final sum by a different grouping before answering.

### Common pitfalls to avoid

- **Comparing counts with rates.** Seventy-two patched servers is not better than 92% compliance. Establish what each figure is before ranking rows.
- **Unweighted averages over unequal groups.** When services or estates differ in size, weight by size or return to raw counts. The simple mean of percentages is almost always wrong.
- **Base-value errors in percentage change.** Reductions and increases are measured against the starting figure, never the ending one.
- **Rounding down capacity requirements.** Servers, licences, and disks come in whole units; requirements round up. 4.13 of anything means 5.
- **Forgetting the safety margin is part of the question.** Time-to-full at 100% is arithmetic; time-to-act uses the alert threshold and the procurement lead time. Read which one the question wants.
- **Losing the rollback deadline.** In any window calculation, the binding constraint is usually "rollback must complete by close", not the window's raw length.
- **Presenting unchecked figures.** In the test and in service reviews alike, one transposed digit undermines the whole analysis. Budget ten seconds per question for verification — it is the highest-value time you will spend.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand, evaluate, and act on written information of the kind your role genuinely handles: departmental policies, change and incident procedures, supplier contract clauses, vendor advisories, technical documentation, and operational emails. The dominant format presents a short passage followed by statements to judge as **True** (supported by the passage), **False** (contradicted by the passage), or **Cannot say** (neither supported nor contradicted). Supporting formats include best-summary questions, inference questions, and clear-writing judgements where you select the most effective rewrite of a poorly drafted communication.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions. The governing rule throughout: judge every statement strictly against the passage, not against your technical knowledge or experience. This is the hardest discipline for experienced engineers, precisely because you know so much that the passage does not say — and the test deliberately probes whether you can keep that knowledge from contaminating your reading.

Why do employers use verbal reasoning tests for infrastructure engineers? Because at your level, misread text becomes misconfigured systems. Departmental policy defines what you may build and how; supplier advisories define what must be patched and by when; handover notes and change records are how your work becomes safely operable by others. Your role summary is explicit that you support and maintain solutions "as directed and according to departmental policy" — and following policy precisely presumes reading it precisely. There is also the outbound direction: you produce documentation, and your role requires you to "effectively document all work using required standards". Engineers who write clearly reduce incidents, shorten handovers, and make their own work auditable. Verbal assessments sample both abilities — precise comprehension and sound judgement about clarity — in a standardised, job-relevant way.

### How this assessment maps to your role

- **Reading policy and control language precisely** maps to your **Information security** skill: explaining security controls, and building according to departmental policy, depends on parsing the exact force of "must", "may", "should", and their conditions.
- **Following and evaluating procedures** maps to your **IT infrastructure** skill and your duty to support services as directed: runbooks, vendor documentation, and change procedures reward literal, complete reading — and punish the confident skim.
- **Distinguishing statement from inference** maps to your **Problem management** and **Troubleshooting and problem resolution** skills: incident records state observations; causes are established by investigation, not by reading between lines — the exact discipline "Cannot say" trains.
- **Comprehending supplier communications** maps to your duty to work with and support third parties: contract clauses, support notices, and end-of-life advisories create obligations and deadlines your team must extract accurately.
- **Judging clear writing** maps to your **Systems design** documentation duty: producing detailed designs and documenting all work to required standards means recognising — and writing — prose that a colleague can act on without ambiguity.
- **Understanding standards texts** maps to your **Modern development standards** skill: explaining the most important principles and applying them under guidance starts with digesting the written standards accurately.

### Practice questions

**Question 1 (easy) — True/False/Cannot say on a change policy**

Passage: "All changes to production infrastructure require an approved change record before implementation. Standard changes — pre-approved, low-risk, repeatable changes — are recorded but do not require individual approval. Emergency changes may be implemented before a record is raised, provided a record is completed within 24 hours of implementation."

Statement: "A standard change may be implemented without any record being created."

- A) True
- B) False
- C) Cannot say
- D) True, provided the change is low risk

**Correct answer: B**

**Explanation:** The passage distinguishes two obligations: approval and recording. Standard changes escape individual approval, but the text says they "are recorded" — recording still applies. The statement claims no record is needed, which the passage contradicts: False. Option D fails for the same reason — low risk removes the approval step, not the record. This approval/record distinction is not exam pedantry: in real change management, the record is what makes an unattended 2 a.m. configuration difference explicable three weeks later, and auditors treat unrecorded changes as unauthorised regardless of their risk level. Train yourself to track each obligation in a policy separately; sentences frequently relax one requirement while silently retaining another, and the wrong answers in verbal tests are built from exactly that conflation.

**Question 2 (easy) — Comprehension of a vendor advisory**

Passage (vendor advisory): "A vulnerability in the management interface of AppGate 400-series devices allows unauthenticated remote code execution. Devices running firmware 7.2 or later are not affected. For affected devices, apply hotfix HF-2214 immediately. As an interim mitigation only, restricting management-interface access to the administrative VLAN prevents exploitation from other networks; this does not remove the vulnerability."

Statement: "Restricting management access to the administrative VLAN removes the vulnerability from affected devices."

- A) True
- B) False
- C) Cannot say
- D) True, if the restriction is applied immediately

**Correct answer: B**

**Explanation:** The advisory could not be plainer: the VLAN restriction "does not remove the vulnerability" — it only "prevents exploitation from other networks" as an "interim mitigation only". The statement claims removal, which the passage explicitly contradicts: False, and option D's timing condition changes nothing. The mitigation/remediation distinction is one of the most operationally important reading points in your **Information security** work: a mitigation reduces exposure while the weakness remains; remediation (here, hotfix HF-2214, or firmware 7.2+) removes the weakness. Teams that read mitigations as fixes leave vulnerabilities in place indefinitely — a pattern that features in real-world breach reports with depressing regularity. When you triage advisories, extract three things exactly: the affected condition (firmware below 7.2), the remediation, and any interim mitigations, and never let the third substitute for the second.

**Question 3 (easy) — Cannot say discipline on a service report**

Passage: "In quarter two, the storage service achieved 99.9% availability, exceeding its 99.5% target. Two incidents occurred, both resolved within their target resolution times. Capacity utilisation ended the quarter at 71%."

Statement: "The storage service will meet its availability target in quarter three."

- A) True
- B) False
- C) Cannot say
- D) True, because the service exceeded its target in quarter two

**Correct answer: C**

**Explanation:** The passage reports quarter two only. A statement about quarter three is a prediction, and past performance — however encouraging — neither guarantees nor precludes future performance; the passage makes no claim about the future at all. Not supported, not contradicted: Cannot say. Option D names the exact cognitive slip being tested: converting evidence of past performance into certainty about the future. Engineers fall into this trap in real reporting, too — "the service has always met its target" quietly becomes "the service will meet its target" in a planning meeting, and risk decisions get made on the strength of a tense change. The professional discipline mirrors the test discipline: keep observed history and forward projection explicitly separate, and label projections as projections with their assumptions stated.

**Question 4 (easy) — Choosing the clearest handover note**

You must leave a handover note about an unresolved issue. Which version is most effective?

- A) "There were some problems with the backup thing earlier, might be worth keeping an eye on it."
- B) "Backup job BK-114 (finance file server, PFIFS01) failed at 01:20 with 'destination unreachable'. I verified the network path at 08:30 — now clear — and re-ran the job at 08:45; it is in progress, about 40% complete. If it fails again, the runbook is KB-0231; escalate to the storage team via the on-call rota."
- C) "BK-114 failed. Re-run in progress. See KB-0231."
- D) "The backup infrastructure experienced an anomalous failure event which has been subjected to remedial re-execution and is currently pending completion assessment."

**Correct answer: B**

**Explanation:** A handover note succeeds when the reader can act without finding you. Option B delivers every element of actionability: what failed (job, server, service), when and how (time, error message), what has been done (verification, re-run, current progress), and what to do next (runbook reference, escalation route). Option A is vague on every axis — "the backup thing" and "keep an eye on it" transfer anxiety, not information. Option C is accurate but incomplete: it omits the error, the verification already done, and the escalation route, forcing the reader to rediscover your morning's work. Option D is the pompous passive at its worst — many words, no facts a responder can use. Your role's documentation duty — "effectively document all work using required standards" — is tested every time you write one of these; the four-part pattern (what, when, done, next) is worth making a reflex, because incidents change shifts and your note is the only memory that survives the handover.

**Question 5 (moderate) — Inference across a support contract clause**

Passage (contract extract): "The supplier will respond to Priority 1 incidents within 30 minutes and restore service within 4 hours, measured from the customer's logging of the incident in the supplier's portal. Incidents reported by telephone are logged by the supplier on the customer's behalf within 15 minutes of the call. Failure to meet restoration targets in two consecutive months triggers service credits under Schedule 4."

Statement: "A Priority 1 incident reported by telephone at 10:00 must be restored by 14:15 at the latest for the supplier to meet its target."

- A) True
- B) False
- C) Cannot say
- D) True, but only if service credits have been triggered

**Correct answer: A**

**Explanation:** Chain the clauses. Telephone reports are logged by the supplier "within 15 minutes of the call" — so a 10:00 call is logged by 10:15 at the latest. The 4-hour restoration clock runs "from the customer's logging of the incident in the supplier's portal" — here, the logging done on the customer's behalf, so the clock starts no later than 10:15, making the latest compliant restoration 14:15. Every link is in the passage; joining them is supported inference, so True. Option D confuses the remedy mechanism (credits after two consecutive failing months) with the target itself. This is exactly how you must read supplier agreements in your duty to work with and support third parties: obligations are usually assembled from two or three separated clauses — a target, a measurement definition, and a start-the-clock rule — and the measurement definition is where suppliers and customers most often discover they disagree. Extract it first.

**Question 6 (moderate) — Reading a security standard's conditions**

Passage: "Administrative access to servers must use individual named accounts. Shared administrative accounts are permitted only where a system cannot technically support individual accounts; in such cases, the shared credential must be stored in the approved password vault, checked out per use, and rotated after each checkout. Storing credentials in documents, scripts, or configuration files is prohibited in all circumstances."

Statement: "A team may use a shared administrative account for a legacy system that cannot support individual accounts, keeping its password in an encrypted spreadsheet that only administrators can open."

- A) True
- B) False
- C) Cannot say
- D) True, because the spreadsheet is encrypted and access-controlled

**Correct answer: B**

**Explanation:** Two rules apply, and both must be satisfied. The shared account itself is permitted — the legacy system meets the "cannot technically support individual accounts" condition. But the storage requirement is specific: the approved password vault, with per-use checkout and rotation. An encrypted spreadsheet is a "document", and the final sentence prohibits credential storage in documents "in all circumstances" — an absolute clause that admits no exception for encryption or access control. One requirement satisfied plus one violated equals non-compliance: False. Option D is the realistic rationalisation — "it's encrypted, so surely it's fine" — that the absolute wording exists to defeat. Notice the reading technique: when a passage grants a conditional permission and then imposes mandatory conditions on its exercise, verify each condition independently, and give phrases like "in all circumstances" and "regardless of" their full blocking force. That is precisely how your **Information security** skill operates when colleagues propose almost-compliant arrangements.

**Question 7 (moderate) — Main point of a standards passage**

Passage: "Infrastructure as code brings the disciplines of software development to infrastructure operations. When server configurations are defined in version-controlled files rather than applied by hand, every change has an author, a timestamp, and a reviewable difference. Environments can be rebuilt identically on demand, which turns disaster recovery from a bespoke crisis into a routine deployment. Hand-built servers, by contrast, accumulate undocumented changes until no one can say with confidence how they work. The barrier to adoption is rarely tooling, which is mature, but habit: teams must stop making direct changes, even small ones, and that discipline is harder than any technology."

What is the main point of the passage?

- A) Infrastructure-as-code tooling is not yet mature enough for production use.
- B) Infrastructure as code delivers traceability and reproducibility, and the main obstacle to adoption is behavioural discipline rather than technology.
- C) Disaster recovery is impossible without infrastructure as code.
- D) Small direct changes to servers are acceptable if documented.

**Correct answer: B**

**Explanation:** The passage advances two connected claims: the benefits (authored, reviewable changes; identical rebuilds; disaster recovery as routine) and the obstacle (habit, not tooling — "that discipline is harder than any technology"). Option B captures both. Option A contradicts the passage, which calls tooling "mature". Option C overstates: the passage says infrastructure as code makes disaster recovery routine, not that recovery is otherwise impossible — watch for answer options that convert a comparative advantage into an absolute necessity. Option D contradicts the passage's insistence that teams stop direct changes "even small ones". Identifying a two-part main point matters because summaries that capture only the benefits half would misrepresent the author's emphasis. This connects to your **Modern development standards** skill — explaining the most important principles and applying them under guidance — and the passage's content is worth absorbing as well as parsing: version-controlled configuration is the direction of travel for exactly your role.

**Question 8 (moderate) — True/False/Cannot say on an incident report**

Passage (incident report): "At 11:42 the load balancer marked both application servers as unhealthy and stopped routing traffic, causing a complete service outage. Investigation found that a certificate on the health-check endpoint had expired at 11:40. The certificate had been excluded from the automated renewal system when the endpoint was rebuilt in March. Service was restored at 12:15 by temporarily disabling certificate validation on the health check, and a correctly issued certificate was deployed at 14:30."

Statement: "The engineer who rebuilt the endpoint in March failed to follow the rebuild procedure."

- A) True
- B) False
- C) Cannot say
- D) True, because the certificate was excluded from renewal

**Correct answer: C**

**Explanation:** The report establishes a factual chain: expiry at 11:40, health checks failing at 11:42, exclusion from automated renewal dating from the March rebuild. What it does not establish is why the exclusion happened — the rebuild procedure may not have covered renewal enrolment at all (a procedure gap), the enrolment may have failed silently (a tooling fault), or an engineer may indeed have missed a step. The statement asserts one specific explanation among several the passage leaves open: Cannot say. Option D repeats the fact of exclusion as if it identified a culprit — facts about the system are not findings about a person. This distinction carries directly into your **Problem management** practice: good problem records separate observed facts from attributed causes, and blameless investigation stays possible only while that separation holds. In the test, any statement naming fault, intention, or motive deserves special suspicion — passages rarely support them.

**Question 9 (moderate) — Evaluating an argument about third-party support**

Passage (email from a colleague): "We should bring storage support in-house when the supplier contract ends. The supplier took six hours to resolve last month's array fault, and we pay them £85,000 a year. Our own team knows the environment better than any supplier ever will, so we'd get faster fixes for free."

Which is the strongest criticism of the argument?

- A) Suppliers should never be criticised in writing.
- B) The argument generalises from a single incident, and "for free" ignores the real costs of in-house support — training, tooling, spare parts, and out-of-hours cover — as well as losing the supplier's specialist escalation routes.
- C) £85,000 a year is objectively cheap for storage support.
- D) The team does not know the environment better than the supplier.

**Correct answer: B**

**Explanation:** Test the argument's evidence and its accounting. Evidence: one six-hour resolution is a sample of one — it may be typical or exceptional, and the contract's target for that incident class is unstated. Accounting: "for free" is the fatal flaw — in-house support costs staff time, training and certification, diagnostic tooling, spares holding, and (for a service underpinning others) an out-of-hours rota; it also forfeits the supplier's access to manufacturer engineering escalation for complex faults. Option B captures both failures. Options C and D are counter-assertions, not criticisms of the reasoning — they could each be true or false without repairing the argument's logic. Option A is irrelevant. Weighing arguments like this is a live part of your duty to work with and support third parties: contract renewal decisions deserve total-cost comparison and representative performance data, and the engineer who asks "what does the full year's incident data show, and what would in-house actually cost?" converts an opinion clash into an evidence question.

**Question 10 (hard) — Interacting conditions in an operational policy**

Passage: "Servers may be added to the production network only after: completion of a security build review; enrolment in monitoring; and enrolment in the backup service, except where the server is explicitly classified as stateless, in which case backup enrolment is not required. A server's stateless classification must be recorded in the configuration management database (CMDB) and approved by the service owner. Unapproved classifications are treated as if the server were stateful."

Statement: "A server whose stateless classification is recorded in the CMDB but not yet approved by the service owner may be added to the production network without backup enrolment, provided the build review and monitoring enrolment are complete."

- A) True
- B) False
- C) Cannot say
- D) True, because the classification is recorded in the CMDB

**Correct answer: B**

**Explanation:** Follow the classification rules to their conclusion. The backup exemption applies only to servers "explicitly classified as stateless", and classification requires two elements: CMDB record AND service-owner approval. This server has the record but not the approval — and the final sentence resolves exactly this case: "unapproved classifications are treated as if the server were stateful." A stateful server requires backup enrolment before joining production. The statement claims the exemption applies: False. Option D stops at the first condition and ignores the second — the standard trap in two-condition rules. Notice the drafting pattern, common in real infrastructure policy: a general rule, an exception, conditions on the exception, and a default for incomplete cases. The default clause ("treated as if...") is the most powerful sentence in the passage because it closes the gap that ambiguity would otherwise open — and spotting such clauses quickly is a hallmark of engineers who build "according to departmental policy" rather than according to a half-remembered version of it.

**Question 11 (hard) — Inference from a migration plan**

Passage: "The virtualisation platform migration will move 240 guest servers from the legacy cluster to the new cluster over twelve weekends, in batches of 20. Each batch is selected two weeks in advance and its service owners notified. A batch may be deferred at the service owner's request no later than five working days before its scheduled weekend; deferred servers join the final batch. The final batch weekend has capacity for 40 servers. If deferrals would take the final batch above 40, the migration schedule will be extended."

Statement: "If 25 servers are deferred during the migration, the schedule will be extended."

- A) True
- B) False
- C) Cannot say
- D) True, because 25 exceeds the batch size of 20

**Correct answer: A**

**Explanation:** Work the arithmetic the passage implies. Twelve batches of 20 equals 240 servers, so the final batch already contains 20 scheduled servers. Deferred servers "join the final batch", so 25 deferrals would make the final batch 20 + 25 = 45 servers. The final weekend's capacity is 40, and the passage states that if deferrals take the final batch above 40, the schedule "will be extended". Since 45 exceeds 40, extension follows necessarily: True. Note why option D, though reaching the same verdict, reasons wrongly: the batch size of 20 is not the constraint — the final batch's special capacity of 40 is, and 21 deferrals (making 41) would already trigger extension while 20 would not. Verbal tests at this level increasingly embed light arithmetic inside prose, mirroring real planning documents where the numbers live in sentences rather than tables. Extract the quantities, compute, then return to the conditional language to see what the result triggers — the same skill you use when reading a migration plan your team must actually deliver.

**Question 12 (hard) — Judging a complete communication**

Passage (draft email to service owners, written by a teammate for your review): "Subject: Server patching. We will be patching servers this month as usual. Some downtime may occur on some systems at some point during the maintenance windows. If you experience issues afterwards, contact the service desk. No action is required."

The email will go to owners of services whose servers will be rebooted between 22:00 and 02:00 on specific dates listed in the change schedule. Which criticism of the draft is most important?

- A) The subject line should be more exciting to encourage opens.
- B) The email omits the specific dates, times, and affected systems, so "some downtime on some systems at some point" leaves owners unable to warn their users or plan around the reboots — and "no action is required" is arguably wrong, since owners should check their service afterwards.
- C) The email is too short; professional emails should be at least three paragraphs.
- D) The email should not mention downtime, to avoid alarming service owners.

**Correct answer: B**

**Explanation:** Judge the draft against its purpose: enabling service owners to protect their users through a known, scheduled disruption. The information that achieves this exists — specific dates, the 22:00–02:00 window, and the affected systems are all in the change schedule — and the draft withholds all of it behind three "some"s. An owner reading it cannot tell whether their service is affected, when, or for how long; and "no action is required" discourages the one genuinely useful action, a post-patching service check. Option B identifies both failures. Options A and C confuse style metrics with effectiveness; option D proposes concealment, which trades short-term calm for justified anger at unannounced downtime — the opposite of the user focus your profession expects. The reviewing skill here is part of your documentation duty: before approving any operational communication, ask "what decision or action should the reader be able to take, and does the text contain everything that requires?" Vagueness in maintenance notices converts planned work into perceived incidents — a wholly avoidable reputational cost.

### Preparation tips

- **Practise the three-way judgement on work documents.** Your change policy, security standards, and supplier contracts are ideal material: write statements about them and classify each as True, False, or Cannot say strictly from the text.
- **Extract obligations into checklists.** When reading any policy passage, list each "must/may/prohibited" separately with its conditions. Most wrong answers merge two obligations the passage keeps distinct.
- **Give absolute phrases full force.** "In all circumstances", "regardless of", "only where" — these decide hard questions. Slow down and apply them literally.
- **Separate facts from attributions.** In incident-report passages, statements about people's failures or intentions are almost always Cannot say. Practise spotting the difference between "the certificate was excluded" and "the engineer failed".
- **Do the embedded arithmetic.** Modern verbal tests hide small calculations in prose. When quantities appear, extract and compute before judging the statement.
- **Review your own recent writing.** Take a handover note or change record you wrote and test it against the what/when/done/next standard. Improving your writing sharpens your eye for the clear-writing questions — and vice versa.
- **Read the statement first, then hunt.** Knowing what you must verify turns your second read of the passage into a targeted search rather than a re-read.

### Common pitfalls to avoid

- **Answering from expertise instead of the passage.** You know how certificates, backups, and RAID behave; the passage may say less, or differently. Only the passage counts.
- **Treating "not mentioned" as "false".** Absence of support means Cannot say; False requires contradiction. This single distinction decides more marks than any other.
- **Under-reading default clauses.** Sentences like "unapproved classifications are treated as stateful" resolve the ambiguous cases the question will target. Find them before answering.
- **Accepting the right verdict for the wrong reason.** Options that reach a correct-sounding conclusion through faulty reasoning are still wrong when the question asks which statement is supported or which criticism is strongest. Check the reasoning, not just the destination.
- **Confusing mitigation with remediation.** In advisory passages, interim measures do not remove vulnerabilities, and options claiming they do are contradicted, not supported.
- **Judging writing by length or formality.** The clearest option is the one that enables the reader to act. Short can be incomplete; long can be empty; formal can be useless.
- **Lingering on one passage.** Two careful reads should settle most statements. If not, make your best elimination-based judgement and move on — the test rewards overall accuracy, not perfection on a single item.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to evaluate possible responses — choosing the most effective, identifying the most and least effective, ranking all options, or rating each independently. Unlike the other assessment types, SJTs are scored against the consensus of experienced professionals and the organisation's valued behaviours rather than against a single provable answer. The typical format is an online test of 15 to 25 minutes with 10 to 20 scenarios, often untimed or generously timed, because it measures judgement rather than speed.

The scenarios at your level are not about whether you can perform the technical work — that is assumed. They probe the judgement wrapped around the work: what you do when a change misbehaves mid-window, how you handle a third party who cuts corners, when you escalate versus persevere, how you balance a project deadline against an operational risk, and how honestly you communicate when the news is bad. The options are engineered so that several look reasonable; the difference lies in corners cut — an unlogged workaround, a silent assumption, a user impact accepted without communication — or in over-reactions that create new problems while solving old ones.

Why do employers use SJTs for infrastructure engineers? Because at this level your decisions touch live services directly and often alone. You support and maintain solutions "as directed and according to departmental policy", you own issues "until a new owner has been found or the problem has been mitigated or resolved", and you work daily with third parties whose actions you do not control but whose outcomes you answer for. The behaviours that score well are stable and learnable: protect users first, follow the process and improve it when it fails, communicate early and honestly — especially bad news — escalate at the right moment with the right information, and treat colleagues and suppliers with professional respect. This section lets you rehearse those behaviours against scenarios drawn from the genuine texture of infrastructure operations.

### How this assessment maps to your role

- **Issue ownership under pressure** maps directly to your **Ownership and topic** skill: owning an issue until it is resolved, mitigated, or properly handed over is the behavioural spine of most scenarios — the test probes whether you hold ownership without hoarding it.
- **Change and incident discipline** maps to your **IT infrastructure** duty to support and maintain services according to departmental policy: scenarios about mid-change failures, workarounds, and unauthorised shortcuts test whether policy holds when it is inconvenient.
- **Working with third parties** maps to your role-level duty to work with and support third parties providing infrastructure services: scenarios test constructive challenge, verification, and escalation with suppliers.
- **Honest investigation and prevention** maps to your **Problem management** skill: contributing to remedies and preventative measures requires accurate accounts of what happened, including your own part in it.
- **Security behaviour under social pressure** maps to your **Information security** skill: access requests, credential handling, and policy exceptions test whether you apply controls when a person — sometimes a senior person — pushes back.
- **Team collaboration and quality** maps to your **Systems design**, **Testing**, and **Service focus** skills: scenarios about reviewing others' work, reporting inconvenient test results, and establishing workable frameworks test whether you raise quality without raising conflict.

### Practice questions

**Question 1 (easy) — A change starts going wrong mid-window**

You are implementing an approved change to a storage array at 23:30, inside a window that closes at 02:00. Halfway through, an unexpected warning appears that the documentation does not mention. The remaining steps might work anyway; the rollback procedure is tested and takes 40 minutes. What is the most effective response?

- A) Continue with the remaining steps — the warning is probably cosmetic.
- B) Pause; spend a bounded amount of time investigating the warning against vendor documentation and, if you cannot positively establish it is safe to proceed with time for rollback in hand, roll back and reschedule.
- C) Roll back immediately without investigating.
- D) Stop work, leave the array in its current state, and email the team to look at it in the morning.

**Correct answer: B**

**Explanation:** Option B is the disciplined middle path: a time-boxed investigation respects the possibility that the warning is benign, while the rollback deadline (02:00 minus 40 minutes means a decision by 01:20) keeps the safe exit open. The decisive principle is "proceed only on positive knowledge, not on hope" — the burden of proof sits on continuing, not on stopping. Option A gambles a storage array on "probably", and unexplained warnings during storage changes are precisely how data loss happens. Option C is safe but wasteful as a first move: rolling back at the first anomaly, with hours of window remaining and investigation unattempted, throws away the change unnecessarily — although it would become correct once the decision deadline nears. Option D is the genuinely dangerous answer: a half-applied change is an undefined state, and abandoning it converts a controlled situation into tomorrow's incident. Note the follow-through the strong answer implies: whatever you decide, the change record gains the warning, your investigation, and the outcome — that record is how the next engineer avoids your surprise.

**Question 2 (easy) — You discover your own earlier mistake**

While reviewing firewall rules for an unrelated task, you notice a rule you added three weeks ago is broader than the change record specified — it permits a whole subnet where it should permit one server. Nothing bad appears to have happened. What is the most effective response?

- A) Quietly correct the rule to match the change record and move on.
- B) Correct the rule promptly through an appropriate change process, tell your team lead what you found, and check logs for any use of the unintended access during the three weeks.
- C) Leave it — the broader rule is working and changing it might break something.
- D) Correct the rule and update the old change record to match what you originally implemented, so the records are consistent.

**Correct answer: B**

**Explanation:** Three obligations arise, and option B meets all of them. Fix the exposure — through process, since firewall changes need records even when they are corrections. Be transparent — telling your team lead converts a private error into organisational learning, and protects you far better than concealment if the log check finds something. Verify impact — three weeks of unintended access must be checked, not assumed innocent; "nothing bad appears to have happened" is an observation about tickets, not about traffic. Option A fixes the hole but hides the history and skips the impact check — the log review is arguably the most important step, and it is the one silence forecloses. Option C normalises an unauthorised exposure because remediation is inconvenient. Option D is the worst: falsifying the original record destroys the audit trail's integrity — records document what happened, not what should have happened — and in security contexts that edit can convert an honest mistake into misconduct. SJTs at every level reward the fix-tell-verify pattern; your **Information security** and **Problem management** skills are both, at bottom, built on it.

**Question 3 (easy) — Third-party engineer proposes an undocumented shortcut**

A supplier engineer is on site with you to replace a failed power supply in a production server. Partway through, he suggests also updating the server's firmware "while we're here — it takes ten minutes and saves you a visit", although the change record covers only the power supply. What is the most effective response?

- A) Agree — it is efficient, and he is the manufacturer's engineer.
- B) Decline the firmware update for today, explain that it needs its own assessed and approved change, and offer to raise that change and schedule the work properly.
- C) Agree, but ask him not to mention it to anyone.
- D) Decline and report the engineer to his employer for suggesting it.

**Correct answer: B**

**Explanation:** The suggestion is well-meant and genuinely tempting — which is exactly why it appears in SJTs. But firmware updates carry real risk (they can fail, change behaviour, or require reboots), and the change process exists to assess that risk, schedule user communication, and prepare rollback. "While we're here" work is unassessed, unapproved, and unannounced — the classic unauthorised change, whoever performs it. Option B declines cleanly while honouring the underlying good idea: raising a proper change captures the efficiency without the exposure, and treats the supplier as a partner whose suggestion had merit. Option A lets convenience outrank control; the engineer's expertise addresses how to do the update, not whether tonight is authorised. Option C adds concealment to the breach — the worst pairing available. Option D over-reacts: the suggestion was routine helpfulness in many commercial contexts, and escalating it as misconduct damages a working relationship your role-level duty — working with and supporting third parties — requires you to maintain. Firm on the control, warm to the person, constructive about the path: that triad scores well in tests and works even better in machine rooms.

**Question 4 (easy) — Conflicting demands on your day**

You planned today for a project task: building two servers a delivery team needs by Friday. At 09:30, monitoring shows a production database server's disk filling rapidly — at the current rate it will be full, and the service down, by mid-afternoon. The database team has not noticed. You could work around the disk issue by mid-morning, or ignore it and stay on plan. What is the most effective response?

- A) Stay on the project task — the database team owns that server.
- B) Alert the database team immediately with the evidence and projection; agree who acts; if it falls to you, address the disk risk first and tell the delivery team your build may slip.
- C) Silently fix the disk issue yourself, then resume the project without telling anyone.
- D) Email the database team and continue with the project, assuming they will pick the alert up.

**Correct answer: B**

**Explanation:** A production outage projected for this afternoon outranks a build due Friday — impact and urgency both point the same way. But the scenario's subtlety is ownership: the server belongs to another team, so the first move is a direct, evidenced alert (rate of growth, projected full time), followed by explicit agreement on who acts — which is your **Ownership and topic** skill working properly: own the issue until it has an owner, not necessarily own the fix. Option B also handles the second-order consequence honestly: if the risk falls to you, the delivery team learns about the possible slip now, not on Friday. Option A hides behind organisational boundaries while a preventable outage approaches — "not my server" is never "not my problem" when you hold the information. Option D discharges the duty in form but not substance: an unacknowledged email is not a transfer of ownership, and by mid-afternoon it may be an unread one. Option C fixes the disk but silently changes another team's server (an unauthorised change from their perspective) and leaves the underlying cause uninvestigated — the growth may be a symptom of something the database team urgently needs to know.

**Question 5 (moderate) — Test results block a deadline**

You are executing the test scripts for a new file service that a programme wants live on Monday. On Friday morning, one test fails: permissions on a shared area behave incorrectly in an edge case involving nested groups. The programme manager, under pressure, says: "It's one test out of forty. Mark it as passed with a note, and we'll fix it after go-live." What is the most effective response?

- A) Mark it passed with a note as instructed — the programme manager owns the deadline.
- B) Record the test accurately as failed, explain the actual risk in plain terms, and escalate the go/no-go decision with options — fix now, go live with a documented known issue and mitigation, or delay — to whoever owns the service risk.
- C) Refuse to sign off anything and tell the programme the launch is cancelled.
- D) Mark it failed but say nothing further, leaving the programme to notice.

**Correct answer: B**

**Explanation:** Two things must both survive this scenario: the integrity of the test record and the legitimacy of the decision. A test record that says "passed" when the test failed is a false record — and your **Testing** skill's core discipline is that results are recorded as observed, then decisions are made about them. But accurate recording alone (option D) is passive: dropping a failed result into a report without explanation invites exactly the wrong outcome, a surprise in production. Option B does the full professional job — record accurately, translate the failure into risk language a decision-maker can weigh (who is affected by the nested-group case, how likely, how bad), and route the go/no-go to the risk owner with real options. Note that going live with a documented known issue can be a perfectly good decision — the difference between that and option A is that it is made knowingly by the right person, not embedded in a falsified record by the wrong one. Option C overcorrects: cancelling the launch is not your call either, and "no" without options is as unhelpful as "yes" without truth. Pressure to soften records is common; the engineers trusted with bigger decisions are the ones who kept records straight under it.

**Question 6 (moderate) — A colleague's design has a flaw**

A teammate has produced a physical design for a service and asks you to look it over before submission. You notice both redundant network links from a critical server are routed through the same physical switch — a single point of failure that contradicts the logical design's resilience requirement. Your teammate is defensive about criticism and the design is due tomorrow. What is the most effective response?

- A) Say the design looks fine to avoid conflict — the reviewers will probably catch it.
- B) Raise it directly and specifically with your teammate today — framed against the logical design's requirement rather than as personal criticism — and offer to help rework the affected section before the deadline.
- C) Say nothing to your teammate but email their line manager about the flaw.
- D) Fix the design yourself without telling them.

**Correct answer: B**

**Explanation:** The flaw is objective — the logical design demands resilience the physical design does not deliver — which makes the conversation easier than it feels: option B anchors the feedback in the requirement ("the logical design calls for diverse paths; both links terminate on SW-A") rather than in judgement of the person, which is precisely how defensiveness is defused. Offering rework help converts critic into collaborator and respects the deadline. Option A fails everyone: the teammate submits a flawed design, reviewers may or may not catch it, and if it ships, a single switch failure someday takes down a "resilient" service — you were asked to review, and a review that withholds its only significant finding is worthless. Option C is a trust-destroying escalation of something a peer conversation resolves; going around a colleague to their manager, unasked, converts a technical fix into a political wound. Option D disrespects authorship and forfeits the learning — the teammate would meet the same flaw again in their next design. Reviewing others' work honestly and kindly is how your **Systems design** skill scales beyond your own keyboard, and SJTs consistently reward the direct-specific-supportive pattern.

**Question 7 (moderate) — Supplier misses a deadline that affects your commitment**

A third-party provider was due to deliver configured network equipment to you by today; your team's project plan has you installing it this week, with the service owner expecting completion Friday. The supplier's account manager emails: the delivery will be five working days late, with no explanation. What is the most effective response?

- A) Wait for the equipment and explain the delay to the service owner on Friday when the deadline is missed.
- B) Reply demanding the equipment by tomorrow and threatening contract termination.
- C) Inform the service owner and your team lead today with the revised dates and a re-planned schedule; ask the supplier for the cause of the delay, a firm new date, and any options to mitigate; and record the miss for the supplier's performance review.
- D) Source equivalent equipment from another supplier immediately.

**Correct answer: C**

**Explanation:** The delay is now a fact; the variables you still control are communication, mitigation, and record. Option C works all three: telling the service owner today converts Friday's broken promise into today's managed re-plan (bad news ages terribly — early disclosure preserves trust and lets the owner adjust their own commitments); pressing the supplier for cause, firm date, and options treats them as a partner while testing whether five days is real; and recording the miss feeds the performance management your role-level duty to work with third parties implies — patterns of misses matter at contract review even when a single miss is forgivable. Option A chooses comfortable silence and makes the service owner's Friday worse than it needs to be. Option B is theatre: threats you cannot execute (termination for a first five-day delay is almost never available or wise) spend relationship capital and speed nothing up. Option D exceeds your authority, ignores procurement rules that govern government purchasing, and probably delivers unconfigured equipment later than the delayed configured delivery. The scoring pattern: communicate early, mitigate realistically, escalate proportionately, record factually.

**Question 8 (moderate) — Asked for access outside the process**

A developer you work with regularly and trust messages you: "Deployment's broken and the release is tonight. Can you give my account temporary admin on the app servers? The access request queue is two days deep. I'll only need it for an hour." Granting access without an approved request is against policy, but you technically can do it. What is the most effective response?

- A) Grant it for an hour — you trust them, and the release matters.
- B) Decline to grant unapproved access; instead, offer the legitimate fast paths — run the specific commands for them yourself under your own authorised access, or invoke the emergency access procedure if one exists, or help them get the request expedited.
- C) Decline and end the conversation — their deadline is not your problem.
- D) Grant it, but watch everything they do.

**Correct answer: B**

**Explanation:** The request is sympathetic, time-pressed, and from someone trustworthy — which is exactly the profile of most real access-control failures. The policy exists precisely because individual engineers cannot see what approvers check (conflicting duties, data exposure on those servers, whether "an hour" of admin is proportionate to the need). Option B holds the control while genuinely solving the problem, and the first alternative it offers is usually the right one: you executing specific commands under your own authorised access keeps accountability with an authorised person and gives the developer what they actually need — the deployment fixed, not the privilege itself. Emergency access procedures and expedited approvals are the other legitimate routes; knowing them is part of applying your **Information security** skill in practice rather than in theory. Option A creates unauthorised, unaudited admin access on production — trust does not substitute for authorisation, and "temporary" access has a long history of becoming permanent. Option D adds supervision to a breach without making it authorised. Option C keeps the rule and abandons the colleague — compliance without helpfulness scores poorly too, because user focus and collaboration are being assessed alongside security. Rule held, need met, relationship intact: that is the full mark.

**Question 9 (moderate) — An incident exposes a gap in your documentation**

Overnight, the on-call engineer struggled for two hours with a failed service you built, because the recovery runbook was missing a step you perform from memory — a dependency that must restart in a specific order. The on-call engineer eventually worked it out and mentions it to you, tiredly but without hostility, the next morning. What is the most effective response?

- A) Point out that a competent engineer should have worked it out faster.
- B) Thank them, fix the runbook today with the missing step and the reason for the ordering, ask them to review the fix, and check whether other runbooks you own carry similar from-memory gaps.
- C) Apologise and plan to update the runbook when you next have quiet time.
- D) Suggest that in future they phone you at home rather than rely on runbooks.

**Correct answer: B**

**Explanation:** The incident revealed a specific, fixable failure: knowledge you hold that the documentation does not — precisely the gap your **Systems design** documentation duty ("effectively document all work using required standards") exists to close. Option B closes it with every professional refinement: same-day action (runbook gaps are live operational risk — the same failure could recur tonight), the reason for the ordering included (rationale is what lets a stressed engineer adapt when reality deviates from the script), review by the person who found the gap (they know exactly what confused them at 3 a.m.), and the generalisation step — auditing your other runbooks — which converts one incident into systematic prevention, the essence of your **Problem management** skill. Option C concedes the point but leaves the risk open indefinitely; "quiet time" is where documentation goes to die. Option A attacks the person your gap injured — reputationally corrosive and factually backwards. Option D institutionalises the problem: a service recoverable only via one person's phone number is a single point of failure wearing a lanyard, and it fails permanently when you are on leave, asleep, or gone. Documentation debt is invisible until 3 a.m.; the engineers who pay it down promptly are the ones on-call colleagues trust.

**Question 10 (hard) — Workaround becoming permanent**

Six weeks ago, during a major incident, your team applied a temporary workaround: disabling certificate validation between two internal services. The incident record says it would be reverted "within days" once the certificate issue was fixed. You discover today that the certificate was fixed five weeks ago, but the workaround was never reverted — validation is still off, nobody noticed, and reverting requires a change with a small outage. Your team lead is focused on a big migration and unlikely to welcome extra work. What is the most effective response?

- A) Leave it — it has been fine for six weeks, and the migration is the priority.
- B) Revert it yourself immediately without a change record, since it merely restores the intended state.
- C) Raise it today with your team lead as a security exposure with a specific proposal — a small assessed change to re-enable validation — and if it is deprioritised, ensure the risk is explicitly recorded and visible rather than forgotten.
- D) Add a note to the incident record that reversion is pending, and wait for someone to schedule it.

**Correct answer: C**

**Explanation:** Disabled certificate validation means the two services no longer verify each other's identity — a real, ongoing security exposure, invisible precisely because everything "works". Option C does the three things the situation demands. It surfaces the issue today, because silent known exposures are the ones that appear in breach post-mortems. It arrives with a proposal, not just a problem — a small assessed change is easy to say yes to, and easy for a busy lead to slot around a migration. And its final clause handles the realistic outcome that the lead says "not now": an explicitly recorded, visible risk — on the risk log, with an owner and a date — is a decision the organisation has made; a forgotten workaround is a decision nobody made, and the difference matters enormously when things go wrong. Option A accepts indefinite exposure on the evidence that nothing has failed yet — the logic that keeps every unexploded risk in place. Option B has a tempting rationale, but "restores intended state" still needs a change record: it causes an outage, and the record is what tells the next engineer why validation behaviour changed. Option D documents the gap where nobody is looking, which is procedurally tidy abandonment. The behavioural core — proactive ownership of problems nobody assigned you — is your **Ownership and topic** skill at its most valuable: "take accountability... be proactive in searching for potential problems" is the next level's standard, and this is how you grow into it.

**Question 11 (hard) — Balancing honest reporting against team image**

Your team's monthly service report, drafted by a colleague and about to go to the department's service board, states that all backups ran successfully throughout the month. You know that backups for one system failed on four nights mid-month; the failures were fixed and re-runs completed within a day each time, so no recovery point was ultimately missed beyond 24 hours. Your colleague says: "It rounds to fine. The board doesn't need the noise — it makes us look sloppy." The report goes tonight. What is the most effective response?

- A) Let the report go as drafted — the outcome was ultimately fine, and team credibility matters.
- B) Insist the report state the facts accurately but with the context that gives them fair meaning: four backup failures on one system, detected, re-run, and resolved within a day, with root cause and the prevention action taken.
- C) Escalate the inaccuracy directly to the service board chair before the report is sent.
- D) Refuse involvement and let your colleague send whatever they choose.

**Correct answer: B**

**Explanation:** The draft is not a rounding — it is false: "all backups ran successfully" is contradicted by four failures, and boards make risk decisions (about investment, about accepting backup arrangements) on these reports. But the colleague's fear points at something real: bare failure counts without context can mislead in the other direction. Option B threads it precisely — accurate facts plus fair context: failures occurred, detection worked, recovery worked, root cause is known, prevention is in place. That account is actually more creditable than "all fine": it demonstrates a team that detects, recovers, and learns, which is what mature operations look like — and it preserves the report's integrity for the day when something cannot be rounded away. A board that later discovers polished reports stops believing all of them. Option A makes you party to a false record and teaches your team that reports are advertising. Option C skips the cheap fix — the report has not gone yet, and a conversation with the drafter resolves it tonight; leaping to the board chair converts a correctable draft into a colleague's public embarrassment, poisoning exactly the trust that lets teams self-correct. It becomes the right move only if accuracy is refused. Option D is neutrality that isn't: you know the report is false, and silence ships it. Honest reporting with fair context is the **Service focus** behaviour that keeps frameworks coherent — data feeding decisions must be true, or every downstream decision inherits the error.

**Question 12 (hard) — Handover before leave with an unresolved intermittent problem**

You go on two weeks' leave tomorrow evening. For the past week you have been intermittently investigating a problem: roughly twice a day, for a few minutes, authentication slows across several services. You have gathered evidence — times of occurrence, affected services, a suspicion (not yet proven) that it correlates with a directory server's replication schedule — but no root cause. The problem is worsening slowly. No one else has context. Tomorrow is packed with pre-leave tasks. What is the most effective response?

- A) Keep investigating up to the last minute tomorrow — you are closest to it and might crack it.
- B) Park it until you return — it is intermittent and brief, and you will still be closest to it in two weeks.
- C) Today, package the investigation for transfer: write up the evidence, timeline, and hypothesis, brief a named colleague and your team lead in person, agree who owns it in your absence and its priority given the worsening trend, and log it formally as a problem record if not already done.
- D) Email your notes to the whole team tomorrow evening as you leave, so everyone has the information.

**Correct answer: C**

**Explanation:** This is the ownership-transfer scenario in its purest form, and the deadline structure is the test: transfer takes conversation and questions, so it must happen today, not in tomorrow's crush — option C's timing is as important as its content. The package it describes is the professional standard: evidence and timeline (facts the next investigator would otherwise re-gather over days), the hypothesis clearly labelled as unproven (so it guides without anchoring), a named owner (accountability cannot be diffuse), an agreed priority informed by the worsening trend (this is what makes it your team lead's business too), and a formal problem record (so the investigation survives any individual's memory — the exact purpose of your **Problem management** skill's structures). Option A optimises for a heroic ending and, in the likely case that you do not crack it, leaves the worst outcome: no fix and no transfer, with the problem worsening across two unowned weeks. Option B accepts fourteen days of degradation on a worsening fault and gambles that "intermittent and brief" stays that way — trends rarely honour leave plans. Option D transfers information without transferring ownership: an email to everyone is owned by no one, arrives too late for questions, and is the form of handover that feels complete while accomplishing nothing. Own the issue until a new owner has been found — your role summary's exact words — means the handshake, not the send button.

### Preparation tips

- **Internalise the decision hierarchy.** In almost every scenario: user and service safety first, record integrity always, process followed and improved, communication early, escalation proportionate. Options that violate one of these for convenience are the designed distractors.
- **Rehearse bad-news conversations.** The highest-scoring options frequently involve telling someone something unwelcome — a slip, a failure, a flaw — early and factually. Practise the phrasing until it stops feeling dangerous.
- **Know your real procedures.** Emergency access routes, change freeze rules, escalation rotas, problem records: candidates who know the legitimate fast paths recognise the options that use them.
- **Watch for the "quiet fix" trap.** Options where you silently correct, silently continue, or silently absorb are recurring low scorers — the silence is the flaw, not the fix.
- **Time-box, then decide.** Many strong options pair investigation with a deadline ("bounded time, then roll back"). Look for options that keep the safe exit open rather than choosing between recklessness and retreat.
- **Practise the transfer package.** For any issue you currently own, draft the four-part handover: evidence, hypothesis (labelled), owner, priority. Scenario questions about leave, shift ends, and reassignment all reward this structure.
- **Reflect on real dilemmas weekly.** Note one judgement call from your actual week — an escalation, a pushback, a disclosure — and compare your choice against the patterns in this section. SJT skill is transferred habit, not exam technique.

### Common pitfalls to avoid

- **Continuing on hope.** Mid-change anomalies, unexplained warnings, and "probably fine" are the test's favourite bait. The burden of proof always sits on proceeding.
- **Protecting records' appearance over their accuracy.** Any option that softens, rounds, or backdates a record — test results, change records, service reports — is a low scorer regardless of the motive offered.
- **Letting trust substitute for authorisation.** Colleagues you like and suppliers you respect still need approved access and assessed changes. The relationship is preserved by helping through legitimate routes, not by exceptions.
- **Escalating first or never.** Jumping over a peer to their manager, or to a board, when a direct conversation would resolve the issue scores poorly — as does never escalating when the direct route fails. Proportionate sequence is the pattern.
- **Hiding behind ownership boundaries.** "Their server", "their runbook", "their report" do not neutralise information you hold about a live risk. Alert, evidence, and agree ownership explicitly.
- **Confusing information broadcast with ownership transfer.** Emails to everyone, notes in records nobody reads, and last-minute sends are the illusion of handover. A named owner who has accepted, understood, and can ask questions is the reality.
- **Solving the stated problem while creating a governance one.** Unrecorded fixes, undocumented workarounds, and "while we're here" work solve today at tomorrow's expense — the scenarios are engineered to catch exactly this trade.

## Conclusion

Congratulations — you have worked through a complete, role-specific set of practice materials covering the four assessment types an infrastructure engineer is most likely to meet: cognitive ability, numeric reasoning, verbal reasoning, and situational judgement. That is a substantial piece of professional development, and it is worth taking stock of what you have practised.

In the cognitive section, you parsed naming standards field by field, applied firewall policy literally, traced script logic through compound conditions, localised a network fault by elimination, and reasoned through scheduling constraints that mixed task durations with resource windows. In the numeric section, you converted downtime into availability, forecast disk exhaustion against procurement lead times, sized backup throughput from data volumes and windows, weighted averages by usage, and worked a change window backwards from its rollback deadline. In the verbal section, you held the line between mitigation and remediation, separated recorded facts from attributed blame, assembled contractual obligations from scattered clauses, and judged handover notes and maintenance notices against the only standard that matters — whether the reader can act. In the situational judgement section, you rehearsed the behaviours that define a trusted engineer at your level: pausing changes on evidence rather than hope, correcting your own mistakes through process and in the open, holding security controls against sympathetic pressure, transferring ownership properly before leave, and keeping records honest when honesty is inconvenient.

The connecting thread deserves stating plainly: nothing in this guide is separate from your job. The techniques that earn marks — validate every field, identify the base before dividing, give absolute clauses full force, communicate bad news early, keep the safe exit open — are the working habits that make your changes succeed, your incidents short, your documentation trustworthy, and your word reliable. Practising for the assessment and becoming a stronger engineer are the same activity.

As next steps: revisit the questions you found hardest after a week — spaced repetition is what converts technique into instinct. Recreate one numeric question from your own monitoring data and one verbal question from your own change policy; home-ground practice doubles as job mastery. And take one behavioural pattern from the situational judgement section — perhaps the fix-tell-verify response to your own errors, or the four-part handover package — and use it for real this month.

If a live assessment is ahead of you, go in rested and unhurried, remember that adaptive difficulty rising means you are scoring well, estimate before you calculate, and let the passage — not your expertise — answer the verbal questions. Your daily work already exercises every capability these tests measure; the preparation you have just completed simply lets that capability show.

You build and support the infrastructure that public services stand on. Done well, that work is invisible — which makes the discipline behind it matter all the more. Keep practising, keep documenting, keep owning issues until they truly have owners, and keep being the engineer whose judgement colleagues trust at 2 a.m. Good luck — you are well prepared.
