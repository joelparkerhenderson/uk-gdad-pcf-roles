# End User Computing Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as an end user computing engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills and workplace judgement that predict success in a role. For an end user computing engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the materials you genuinely handle — incident tickets, asset registers, change requests, test scripts, KPI reports, and knowledge articles — and the decisions you genuinely make, such as diagnosing a fault at a user's desk, deciding whether to resolve or escalate, applying change control procedures, and keeping customers informed while you work.

Why do these assessments matter for your role in particular? You work on-site, maintaining hardware and fixing technical problems as quickly as possible. Your value lies in first-time resolution: troubleshooting and diagnosing faults, or escalating them cleanly to service desk managers, incident managers and problem managers when investigation needs to go deeper. That work rests on a compact set of mental skills: recognising patterns across incidents, reasoning logically through symptoms and causes, checking records and configurations for errors, prioritising a busy queue, working accurately with service data such as SLA percentages and ticket volumes, reading procedures and messages precisely, and making sound judgement calls about users, colleagues, and process. You also coach associates and share knowledge with team colleagues, which adds another layer: explaining your reasoning clearly enough that someone else can follow it. Psychometric assessments sample exactly these skills, which is why practising them strengthens both your test performance and your daily craft.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The four sections cover:

1. A **cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving, all using the artefacts of desk-side support.
2. A **numeric reasoning assessment** — percentages, averages, rates, and reading tables and charts, built on ticket volumes, SLA figures, asset counts, and KPI data.
3. A **verbal reasoning assessment** — precise comprehension of knowledge articles, change procedures, policy extracts, and user messages, including true/false/cannot-say discipline.
4. A **situational judgement assessment** — realistic dilemmas about escalation, ownership, coaching, change control, and user care, with most-effective and least-effective response formats.

Here is how to get the most from this guide. Work through one section at a time. For each practice question, commit to an answer before reading the explanation — honest attempts teach far more than skimming. Treat every explanation as a mini-lesson: even when you answer correctly, the walkthrough will sharpen your technique or connect it back to a skill in your framework. Use the preparation tips for self-reflection, and notice how often good assessment technique is simply good engineering practice — checking sources, testing assumptions, communicating clearly.

You solve problems for a living. This guide simply helps you show that ability in a structured setting. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Instead of shape sequences and number grids, it presents the everyday materials of desk-side support — ticket queues, asset registers, configuration records, escalation rules, diagnostic evidence — and asks you to reason about them quickly and accurately.

The typical format is an online, timed test lasting 15 to 30 minutes, with 15 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty to your performance — questions getting harder usually means you are doing well. Employers typically receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. Most platforms offer short, ungraded practice questions before the real test begins.

For an end user computing engineer, cognitive assessment is particularly relevant because diagnosis is structured thinking under time pressure. First-time resolution — the heart of your role — depends on generating hypotheses from symptoms, testing them in a sensible order, and knowing when the evidence says "escalate." The same applies off the tools: maintaining secure configuration and accurate asset information means spotting inconsistencies in records; applying change control procedures means following conditional rules exactly; coaching associates means being able to articulate why a diagnostic step comes next. A well-designed cognitive assessment simulates these demands in miniature, which is why it predicts success in support engineering so well.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Problem management** skill: investigating problems in systems, processes and services begins with noticing that separate incidents share a signature — same building, same model, same update — and understanding whether the problem is operational, tactical or strategic in scale.
- **Logical deduction** maps to your **Incident management** and **Technical specialism** skills: troubleshooting and diagnosing faults is applied logic — if the fault follows the user between machines, the machine is not the cause — and routine maintenance depends on applying documented rules correctly.
- **Error checking** maps to your **Asset and configuration management** skill: maintaining secure configuration and accurate information, and verifying the location and state of IT assets, is a continuous exercise in spotting records that contradict reality or each other.
- **Prioritisation** maps to your **Ownership and topic** skill: owning an issue until a new owner has been found or the problem has been resolved forces constant judgement about what to do first, what to escalate, and what can safely wait.
- **Applied problem solving** maps to your **Change management** and **Testing** skills: implementing change requests and correctly executing test scripts under supervision both require working through multi-step procedures while noticing when reality diverges from the plan.
- **Structured thinking** overall maps to your **Service management framework knowledge**: a Level 3 service management qualification gives you the vocabulary — incident, problem, change, known error — and the assessment tests whether you can apply those distinctions at speed.

### Practice questions

**Question 1 (easy) — Pattern recognition across incident tickets**

Monday's queue contains these tickets:

1. 08:55 — Building C, floor 1: "Desktop shows no network connection."
2. 09:10 — Building C, floor 1: "Cannot reach shared drive."
3. 09:14 — Building A, floor 3: "Mouse not working."
4. 09:22 — Building C, floor 1: "Email stuck in outbox."
5. 09:40 — Building C, floor 2: "Printer offline."

Which grouping most deserves investigation as a single underlying issue?

- A) Tickets 1, 2 and 4 — same location, all symptoms consistent with loss of network connectivity
- B) Tickets 3 and 5 — both involve hardware peripherals
- C) Tickets 1, 2, 4 and 5 — all in Building C
- D) All five tickets — they arrived within an hour

**Correct answer: A**

**Explanation:** Strong pattern recognition combines location and symptom coherence. Tickets 1, 2 and 4 come from the same floor of the same building within half an hour, and all three symptoms — no network, unreachable shared drive, email stuck in outbox — are downstream effects of one plausible cause: a network failure on that floor, perhaps a switch fault. Ticket 5 is in Building C but a different floor, and "printer offline" has many causes; it is worth a glance but does not belong in the core cluster without more evidence. Option B groups by superficial category (peripherals) with no shared cause. Option C over-groups by building alone, and option D over-groups by time alone — both would dilute an investigation with noise. The professional discipline: group incidents by plausible common cause, not by superficial resemblance. This is exactly how repeat issues get identified for escalation to problem managers.

**Question 2 (easy) — Logical deduction from a diagnostic test**

A user's laptop cannot connect to Wi-Fi at their desk. You have the user sign in on a colleague's laptop at the same desk: it connects perfectly. You then take the user's laptop to another floor: it still cannot connect. Which conclusion is best supported?

- A) The desk's Wi-Fi coverage is faulty.
- B) The user's account is misconfigured.
- C) The fault most likely lies with the user's laptop itself.
- D) The building's wireless network is failing.

**Correct answer: C**

**Explanation:** This is isolation testing — the everyday logic of desk-side diagnosis. Test 1: a different laptop, same desk, same user account, connects fine. That clears the desk location (ruling out A) and largely clears the account (weakening B, since the user signed in successfully elsewhere). Test 2: the user's laptop fails on another floor too. That clears the original location again and shows the fault travels with the device. The one element present in every failure and absent from every success is the user's laptop — so C is the supported conclusion. Option D is contradicted by the colleague's successful connection. In an assessment, as at the desk, ask of each hypothesis: is it present in all failures and absent in all successes? This habit is the engine of first-time resolution, and it is precisely the reasoning you will one day narrate aloud when coaching an associate through their first diagnosis.

**Question 3 (easy) — Error checking an asset register**

Policy: every laptop record must show status ("In use", "In store", or "Retired"), a location, and — only when status is "In use" — an assigned user. An extract reads:

| Asset | Status | Location | Assigned user |
|---|---|---|---|
| LT-2201 | In use | Building A | R. Singh |
| LT-2202 | In store | IT store | T. Nowak |
| LT-2203 | Retired | Disposal store | — |
| LT-2204 | In use | Building B | — |

Which rows breach the policy?

- A) Rows 2 and 3
- B) Rows 2 and 4
- C) Rows 3 and 4
- D) Row 4 only

**Correct answer: B**

**Explanation:** Test each row against the rules: status present, location present, and a user assigned when — and only when — status is "In use." Row 1: in use, located, user assigned — compliant. Row 2: in store, but a user (T. Nowak) is assigned — breach, because only in-use devices carry users; a stored laptop with a lingering assignment is exactly how devices go missing on paper, since the register claims someone holds it while the shelf claims otherwise. Row 3: retired, located in the disposal store, no user — compliant; retired devices correctly carry no assignment. Row 4: "In use" with no assigned user — breach of the conditional rule in the opposite direction; a live device nobody officially holds cannot be audited, recalled, or patched reliably. So the breaches are rows 2 and 4, answer B. Notice the symmetry worth remembering: the two register errors that matter most operationally are the phantom assignment (user where none should be) and the orphaned device (no user where one must be) — both break your ability to verify the location and state of IT assets, which is why this check is worth running whenever you touch the register.

**Question 4 (moderate) — Prioritisation of a mixed queue**

At 09:30 you hold four items:

1. A P2 incident: a shared printer used by a 40-person casework team is down; their statutory output is due today.
2. A P3 incident you diagnosed yesterday: one user's laptop needs a part; the loan laptop you issued is working well.
3. A scheduled change: install approved software on six machines, change window closes at 17:00.
4. A message from an associate: "Stuck on a ticket — can you look when free? User is waiting at my desk."

What is the most defensible order of attention?

- A) 1, 4, 3, 2 — restore the team-wide service, unblock the associate and their waiting user, complete the change in window, then progress the parts order
- B) 2, 1, 3, 4 — finish what you started yesterday first
- C) 1, 3, 4, 2 — incidents, then changes, then coaching
- D) 4, 1, 3, 2 — colleagues always come before tickets

**Correct answer: A**

**Explanation:** Rank by impact-weighted urgency. Item 1 is a service-affecting incident touching 40 users with a statutory deadline today — clearly first. Item 4 comes next for a compound reason: an associate is blocked and a user is physically waiting at their desk; a few minutes of your attention unblocks two people, and coaching associates is a named duty at your level, not an optional extra. Item 3 has a hard window closing at 17:00 but seven hours remain — schedule it, do not panic about it. Item 2 is stable: the user is working on a loan device, so the parts-dependent repair is genuinely the least urgent. Option B confuses personal completion with priority — "finish what I started" is a preference, not a triage rule. Option C applies category ordering (incidents before changes before people) rather than judging the actual situations; the waiting user behind item 4 outranks a change with hours of slack. Option D inverts the same error. Notice the deeper pattern: the strong answer treats the associate's request as an operational item with real users behind it, which is exactly how a coaching engineer should see it.

**Question 5 (moderate) — Deduction from change control rules**

Your change procedure states: (i) standard changes (pre-approved, documented, low risk) may be implemented by any engineer; (ii) normal changes require approval at the weekly change board before implementation; (iii) emergency changes may be implemented immediately but must be retrospectively reviewed at the next board; (iv) any change touching the identity system is never a standard change. You are asked today (Tuesday; the board meets Thursday) to make a documented, low-risk configuration update to the identity system to fix a fault currently locking out a 60-person team. What does the procedure require?

- A) Implement it now as a standard change — it is documented and low risk.
- B) Wait for Thursday's board, then implement it as a normal change.
- C) Implement it now as an emergency change and take it to Thursday's board for retrospective review.
- D) The procedure does not permit this change at all.

**Correct answer: C**

**Explanation:** Apply the rules in sequence. Rule (iv) removes the standard-change route: however documented and low-risk, an identity-system change can never be standard — so A fails. That leaves normal or emergency. A 60-person team locked out is a live, service-affecting fault; waiting two days for a board (option B) contradicts the purpose of the emergency route, which exists precisely for urgent fixes that cannot wait for approval. Rule (iii) fits exactly: implement immediately, then present for retrospective review Thursday — option C. Option D invents a prohibition; the procedure offers a lawful route. The reading discipline here matters in real change work: exclusion rules like (iv) override qualifying descriptions like "documented and low risk," and the emergency route is not a loophole but a defined path with its own obligation (the retrospective review) that you must actually honour. Applying change control procedures under supervision means knowing which lane a change belongs in — and why.

**Question 6 (moderate) — Error checking a test script execution**

You are executing a post-build test script for new laptops, under supervision. The script says: Step 3: "Confirm disk encryption status shows 'Active'. Record the status shown. If not Active, stop and report — do not proceed to step 4." Your checklist for three laptops reads:

- Laptop 1: step 3 recorded "Active"; steps 4–7 completed.
- Laptop 2: step 3 recorded "Pending activation"; steps 4–7 completed.
- Laptop 3: step 3 left blank; steps 4–7 completed.

Which laptops were tested in breach of the script?

- A) Laptop 2 only
- B) Laptops 2 and 3
- C) Laptop 3 only
- D) None — all laptops completed every step

**Correct answer: B**

**Explanation:** The script imposes two duties at step 3: record the status, and stop if it is not "Active." Laptop 1 satisfies both. Laptop 2 recorded the status honestly — but "Pending activation" is not "Active," so proceeding to steps 4–7 breached the stop condition. Laptop 3's step 3 is blank: the recording duty was not met, and with no recorded status there is no evidence the gate was checked at all — proceeding was therefore also a breach. So B is correct. Option D reflects a dangerous mindset: "completed every step" is not the goal of a test script; respecting its gates is. This is what correctly executing test scripts under supervision genuinely means — the stop conditions exist because an unencrypted laptop reaching a user is a security incident, not a paperwork slip. In assessments and in the build room alike, read gates as hard rules: record, check, and stop means stop.

**Question 7 (moderate) — Pattern recognition in performance data**

You maintain the team's weekly count of "laptop will not boot" incidents: week 1: 3; week 2: 4; week 3: 3; week 4: 4; week 5: 11; week 6: 12. A colleague says the jump is random variation. What is the most reasonable position?

- A) Agree — small numbers always bounce around.
- B) The counts roughly tripled and stayed high for two consecutive weeks — that is a step change, not a bounce, and it warrants investigating what changed around week 5.
- C) Conclude that laptops are wearing out and order replacements.
- D) Wait ten more weeks to be statistically certain.

**Correct answer: B**

**Explanation:** Distinguish noise from signal by shape. Weeks 1–4 oscillate between 3 and 4 — that is the noise band. Weeks 5 and 6 sit at 11 and 12: roughly three times the established band, and sustained for two weeks rather than spiking once. A single odd week could be chance; a sustained shift suggests a cause — commonly a change: an operating system update, a new build image, a batch of devices from one supplier. The productive next question is "what changed in or just before week 5?" — which is exactly how your problem management skill turns incident data into an investigation, and the kind of repeat-issue evidence worth escalating to the problem manager. Option A ignores the shape of the data. Option C leaps to an expensive remedy with no causal evidence. Option D confuses operational judgement with statistical ceremony — two more weeks of a genuine fault harms real users while you wait for certainty you do not need. Pattern first, hypothesis second, evidence third.

**Question 8 (moderate) — Applied problem solving at the desk**

A user reports their docking station "stopped working — no monitors, no keyboard." You observe: laptop battery charging when docked; both external monitors dead; USB keyboard dead; the same dock powers a colleague's laptop with full function. What is the most efficient next diagnostic step?

- A) Replace the docking station.
- B) Reinstall the laptop's operating system.
- C) Check and update the dock-related drivers and settings on the user's laptop, since power passes through the dock but data functions fail only for this laptop.
- D) Test each monitor on a different machine individually.

**Correct answer: C**

**Explanation:** Read what the evidence has already established. The dock delivers power to the user's laptop (charging works) and delivers everything to the colleague's laptop — so the dock itself, its power supply, and its downstream peripherals are very likely sound. The failure pattern is specific: data functions (video, USB) fail only in the pairing of this laptop with this dock. That points at the laptop's side of the data connection — typically drivers, dock firmware negotiation, or port settings — making C the efficient next step. Option A replaces hardware the evidence just exonerated. Option D tests peripherals that worked moments ago for the colleague — redundant given that observation. Option B is the sledgehammer: an OS reinstall might eventually fix a driver fault, but at hours of cost when a targeted driver update takes minutes, and first-time resolution favours the smallest sufficient intervention. The transferable habit: before choosing a next step, list what your observations have already ruled out — most wasted diagnostic time is spent re-testing the exonerated.

**Question 9 (challenging) — Multi-constraint scheduling**

You must complete four tasks today: (i) a 2-hour laptop build that must finish before the courier collection at 15:00; (ii) a 1-hour change implementation whose approved window is 12:00–14:00 only; (iii) a 30-minute desk-side fix for a director, who is only available 09:00–10:00; (iv) a 1-hour stint covering the walk-up desk, which must happen sometime today but can be moved. You start at 09:00 and finish at 17:00; tasks cannot overlap. Which plan works?

- A) 09:00 director fix; 09:30 build; 11:30 desk cover; 12:30 change; finished by 13:30.
- B) 09:00 build; 11:00 director fix; 12:00 change; 13:00 desk cover.
- C) 09:00 desk cover; 10:00 director fix; 10:30 build; 12:30 change.
- D) 09:00 director fix; 09:30 change; 10:30 build; 12:30 desk cover.

**Correct answer: A**

**Explanation:** Check each plan against the constraints. Plan A: director fix 09:00–09:30 (inside 09:00–10:00 ✓); build 09:30–11:30 (finishes well before 15:00 ✓); desk cover 11:30–12:30 (any time ✓); change 12:30–13:30 (inside 12:00–14:00 ✓). All constraints satisfied. Plan B: the director fix at 11:00 falls outside the director's 09:00–10:00 availability — fails. Plan C: desk cover 09:00–10:00 pushes the director fix to 10:00–10:30, but the director leaves at 10:00 — fails. Plan D: the change at 09:30 is outside its approved 12:00–14:00 window — a change control breach, not merely a scheduling slip — fails. The method: anchor the tasks with the narrowest windows first (the director's hour, the change window), then flow the flexible tasks around them. This is the same reasoning you use daily to sequence site visits, change windows, and courier deadlines — and the same reasoning change procedures encode: windows are constraints, not suggestions.

**Question 10 (challenging) — Deduction with a misleading correlation**

After a printer driver update is deployed on Monday, "cannot print" tickets triple on Tuesday. A manager concludes: "The update broke printing — roll it back." You check the evidence: the update went only to Building A, but Tuesday's tickets come almost equally from Buildings A, B and C; also, the print server had an outage Tuesday morning affecting all buildings. What does the evidence best support?

- A) The manager is right — the timing proves the update caused the tickets.
- B) The building distribution undermines the update hypothesis: an update deployed only to Building A cannot explain tickets in B and C, while the all-building print server outage fits the pattern; the outage is the stronger explanation.
- C) Both the update and the outage caused equal numbers of tickets.
- D) The tickets are unrelated to either event.

**Correct answer: B**

**Explanation:** Timing alone makes the update a suspect; distribution is the test. If the update were the cause, its effects should concentrate where it was deployed — Building A — yet tickets arrive almost equally from three buildings, two of which never received the update. The print server outage, by contrast, affects all buildings and matches the distribution cleanly. So B: the evidence favours the outage. This does not acquit the update absolutely — a careful engineer might still compare Building A's ticket rate with B's and C's for any excess — but rolling back a deployment on timing alone (option A) is the classic post hoc error, and rollbacks carry their own risk and cost. Option C invents a fifty-fifty split no data supports; option D ignores an obvious cause staring at you. The disciplined habit: when two events precede a symptom, ask which one's footprint matches the symptom's footprint. That question — where did it happen, not just when — is often the fastest route to root cause and the difference between evidence-led escalation and noisy guessing.

**Question 11 (challenging) — Prioritising evidence for an escalation**

You are escalating a recurring fault to the problem manager: over three weeks, 14 users have reported intermittent audio failures in video calls, all on the same laptop model, mostly after resume from sleep, and a vendor forum thread describes an identical fault fixed by a firmware update. You may include only four items in the escalation summary. Which set serves the investigation best?

- A) The 14 ticket references; the affected model; the "after resume from sleep" trigger pattern; the vendor firmware lead.
- B) Your personal theory; the angriest user's complaint verbatim; the model; a request for urgent action.
- C) The 14 ticket references; the dates of each ticket; the names of each user; the buildings involved.
- D) The model; the vendor firmware lead; a note that users are frustrated; your availability for a call.

**Correct answer: A**

**Explanation:** An escalation summary exists to let the receiving owner reproduce your reasoning and act. Option A carries the four load-bearing elements: the evidence base (ticket references — verifiable, countable), the scope boundary (one model — instantly narrows the search), the trigger condition (resume from sleep — reproducible, diagnostic gold), and a candidate remedy (the vendor firmware lead — a tested next step). A problem manager receiving this can validate, reproduce, and plan a fix within the hour. Option B leads with opinion and emotion; theories belong after evidence, and urgency claims persuade less than 14 ticket references do. Option C is evidence-rich but insight-poor — dates, names and buildings without the model and trigger bury the signal in administrative detail. Option D includes the frustration note and your diary, neither of which advances diagnosis, while omitting the trigger pattern entirely. The craft being tested — and the craft your role's escalation duty demands — is curation: pass upward the smallest set of facts from which the whole picture can be rebuilt.

**Question 12 (challenging) — Coaching an associate's reasoning**

An associate shows you their diagnosis: "User's laptop is slow. I checked and the disk is 95% full, so that's the cause. I'll delete temporary files and close the ticket." You know disk pressure can cause slowness, but you also notice the ticket says the slowness began "suddenly, yesterday, especially in video calls." What is the best coaching response?

- A) Approve the plan — the associate found a genuine issue and needs the confidence.
- B) Take over the ticket and diagnose it properly yourself while the associate watches.
- C) Ask the associate two questions — "does a 95% disk fit a sudden onset?" and "what else changed yesterday, and why would video calls be worst?" — then let them revise their own diagnosis with your support.
- D) Tell the associate the diagnosis is wrong and to go and find the real cause.

**Correct answer: C**

**Explanation:** The associate has made the commonest diagnostic error: first plausible finding, case closed. A nearly full disk is real but fits poorly with the evidence — disks fill gradually while this slowness began suddenly, and disk pressure does not single out video calls, which point instead toward something network-, driver- or update-related from yesterday. Option C corrects the diagnosis and builds the diagnostician: the two questions hand the associate the exact tests their reasoning skipped — does the cause fit the timeline, and does it fit the symptom pattern — so the revised diagnosis is theirs, which is how coaching creates capability rather than dependence. Option A trades the user's outcome for the associate's comfort; kind in the moment, costly to both later, and likely to bounce the ticket back tomorrow. Option B fixes today's ticket and teaches only spectating. Option D provides the verdict without the method — demoralising and uninstructive at once. This is your role summary made concrete: coach associates and share knowledge means transferring the reasoning, not just the answer. Note the general habit worth teaching: a diagnosis must explain the onset, the pattern, and the timing — not merely coexist with the symptom.

### Preparation tips

- **Practise on your own queue.** Ten minutes with yesterday's tickets is free training: which incidents cluster? What would you check first and why? What did the resolution notes miss? Real artefacts build the exact instincts these assessments measure.
- **Narrate your diagnostic logic.** Whether coaching an associate or working alone, say the reasoning out loud: "power works, data fails, so the fault is on the data path." Articulated logic is faster to check, easier to test, and precisely what deduction questions reward.
- **Anchor on constraints first.** In scheduling and rule questions, find the narrowest windows and the hardest rules (change windows, stop conditions, exclusions) and build outward. Flexible items flow around fixed ones, never the reverse.
- **List what the evidence has excluded.** Before every "next step" decision, note what your observations have already ruled out. It stops you re-testing the exonerated — the biggest time sink in both assessments and real diagnosis.
- **Refresh your framework vocabulary.** Skim your service management framework notes on incidents, problems, changes and known errors. Cognitive questions about routing and process lean on exactly the distinctions your Level 3 qualification taught.
- **Time-box hard questions.** Give any single question ninety seconds of honest effort, choose your best answer, flag it, and move on. Accuracy across the whole test beats perfection on one item.

### Common pitfalls to avoid

- **Grouping by resemblance instead of cause.** "All printer tickets" is a category; "all tickets explainable by one failed switch" is a pattern. Assessments — and problem managers — reward the second.
- **Trusting timing over distribution.** "It broke after the update" is a hypothesis, not a verdict. Check whether the footprint of the symptom matches the footprint of the suspected cause before concluding.
- **Treating gates as paperwork.** Stop conditions in test scripts and exclusions in change procedures are hard rules. Options that "complete all the steps" while sailing through a failed gate are traps.
- **Choosing the biggest intervention.** Reinstall, replace, roll back — sledgehammer options feel decisive and cost hours. The strong answer is usually the smallest step that discriminates between remaining hypotheses.
- **Sequencing by preference.** "Finish what I started," "people before tickets," "incidents before changes" — rigid orderings feel principled and ignore actual impact and urgency. Triage every queue on its facts.
- **Losing marks on easy questions.** Early items are gentle by design; careless reading there costs more than hard items ever will. Bank the easy marks with full attention.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your role genuinely produces: ticket volumes, SLA percentages, resolution times, asset counts, stock levels, and KPI trends. It is not an abstract mathematics exam. Each question presents a small table, chart, or described dataset and asks you to calculate or interpret something a working engineer would actually need to know.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions. A calculator and rough paper are normally allowed; the test measures whether you select the right numbers, choose the right operation, and sense-check the result — not mental arithmetic for its own sake. Scoring is objective against a norm group, often reporting speed and accuracy separately, and some platforms adapt difficulty as you go.

For an end user computing engineer, numeric fluency runs through the whole role. Your IT service reporting skill asks you to collate data from repositories, provide basic reporting, and explain what a KPI is and why it matters — which means calculating closure rates, understanding percentage change, and knowing when an average misleads. Incident work involves SLA clocks that pause and resume. Asset and configuration management involves counts, reconciliations, and stock that must not run dry. Even your user focus skill has a numeric edge: using quantitative data about users to turn user focus into outcomes means reading numbers about waiting times and affected populations and drawing fair conclusions. An engineer who owns the numbers can challenge a misleading report, size a problem honestly for escalation, and explain performance to users and managers without hand-waving.

The arithmetic itself stays deliberately practical — percentages, ratios, averages, rates, and simple forecasting. The tested skill is care and method under time pressure.

### How this assessment maps to your role

- **Percentages and rates** map to your **IT service reporting** skill: closure rates, SLA attainment, and first-time-fix percentages are the KPIs you collate and must be able to compute, verify, and explain.
- **Reading tables and charts** maps to **IT service reporting** and **Problem management** together: trend tables are where repeat issues first become visible, and misreading a row or column produces confidently wrong conclusions.
- **Counts and reconciliation** map to your **Asset and configuration management** skill: verifying the location and state of IT assets is arithmetic — what entered, what left, what remains, and whether the register agrees with the shelf.
- **Time and rate calculations** map to your **Incident management** skill and SLA duties: response and resolution targets are clock arithmetic, including pauses outside working hours.
- **Averages and distributions** map to your **User focus** skill: quantitative user data — waiting times, affected numbers — only turns into good outcomes when you understand what a mean does and does not tell you.
- **Simple forecasting** maps to your **Technical specialism** duties: routine maintenance and administration include consumables and stock, where run-out dates and reorder points are small but consequential calculations.

### Practice questions

**Question 1 (easy) — SLA attainment percentage**

This week your team closed 240 incidents, of which 204 were closed within the SLA target. What percentage of closed incidents met the target?

- A) 80%
- B) 82%
- C) 85%
- D) 88%

**Correct answer: C**

**Explanation:** Percentage = part ÷ whole × 100. Step 1: identify the part (within target = 204) and the whole (closed = 240). Step 2: divide — 204 ÷ 240 = 0.85. Step 3: multiply by 100 — 85%. Answer C. Sense-check: 10% of 240 is 24, so 85% is 240 − 36 = 204 — consistent. This is the single most common calculation in service reporting, and being able to reproduce it from raw figures means you can verify a report rather than merely repeat it — the difference between collating data and understanding it.

**Question 2 (easy) — Reading a category table**

Tickets closed last week by category:

| Category | Closed | Reopened |
|---|---|---|
| Hardware | 62 | 4 |
| Software | 85 | 10 |
| Access | 48 | 1 |
| Network | 25 | 3 |

Which category has the highest reopen rate (reopened as a share of closed)?

- A) Hardware
- B) Software
- C) Access
- D) Network

**Correct answer: D**

**Explanation:** The question asks for a rate, so divide each category's reopened count by its closed count. Hardware: 4 ÷ 62 ≈ 6.5%. Software: 10 ÷ 85 ≈ 11.8%. Access: 1 ÷ 48 ≈ 2.1%. Network: 3 ÷ 25 = 12.0%. The highest rate is Network at 12%, answer D. The trap is answering Software because it has the largest raw count of reopens (10) — but 10 out of 85 is a slightly smaller proportion than 3 out of 25. Reopen rates matter operationally: a high rate suggests fixes that do not stick, which is exactly the kind of quality signal you would investigate under problem management or raise when discussing reporting with stakeholders. Rule: when a question says "rate" or "share," a division is mandatory before any comparison.

**Question 3 (easy) — Average resolution time**

Five hardware incidents this week took 30, 45, 60, 45, and 70 minutes to resolve. What was the mean resolution time?

- A) 45 minutes
- B) 50 minutes
- C) 52 minutes
- D) 55 minutes

**Correct answer: B**

**Explanation:** Mean = total ÷ count. Step 1: total — 30 + 45 = 75; 75 + 60 = 135; 135 + 45 = 180; 180 + 70 = 250 minutes. Step 2: divide by 5 — 250 ÷ 5 = 50 minutes. Answer B. Sense-check: the values run from 30 to 70, and 50 sits centrally, which is what a mean of a fairly balanced set should do. Worth noticing: the median here (sort: 30, 45, 45, 60, 70) is 45 minutes — close to the mean because there is no extreme outlier. When mean and median diverge sharply, one long incident is usually distorting the mean; when they agree, the average is a fair summary. That quick comparison is a professional habit worth keeping for your reporting work.

**Question 4 (moderate) — Percentage change in demand**

Incident volume rose from 320 in March to 400 in April, then fell to 360 in May. What were the month-on-month percentage changes?

- A) +25% then −10%
- B) +20% then −10%
- C) +25% then −11.1%
- D) +80% then −40%

**Correct answer: A**

**Explanation:** Each change divides by its own starting month. March to April: difference = 400 − 320 = 80; 80 ÷ 320 = 0.25 = +25%. April to May: difference = 360 − 400 = −40; −40 ÷ 400 = −0.10 = −10%. Answer A. Option C's −11.1% comes from dividing 40 by 360 — the wrong base; percentage change always uses the original (earlier) value. Option B miscomputes the first change with 400 as the base. Note the asymmetry lesson hiding here: a +25% rise followed by a −10% fall does not return you to the start (320 → 400 → 360), because the percentages act on different bases. When you interpret a data set and communicate it to others — or simply report monthly volumes — stating the base month explicitly prevents the most common misreading in trend discussions.

**Question 5 (moderate) — SLA clock with working hours**

Your resolution SLA for P3 incidents is 8 working hours; working hours are 09:00–17:00, Monday to Friday. A P3 incident is logged at 14:00 on Friday. By when must it be resolved?

- A) 22:00 Friday
- B) 12:00 Monday
- C) 14:00 Monday
- D) 17:00 Monday

**Correct answer: C**

**Explanation:** Count only working time. Friday from 14:00 to 17:00 contributes 3 hours, leaving 8 − 3 = 5 hours. The clock stops over the weekend and restarts Monday 09:00. Five hours from 09:00 is 14:00 Monday — answer C. Option A ignores the end of the working day; option B adds only 3 hours on Monday (a subtraction slip); option D assumes the whole SLA restarts Monday. Method worth keeping: track "hours consumed" and "hours remaining" as two explicit numbers rather than juggling clock times in your head — it makes pauses, weekends, and part-days mechanical instead of error-prone. Accurate SLA arithmetic is not bureaucratic fuss: it determines what you can honestly promise a user, and informing customers on progress with true deadlines is a named part of your role.

**Question 6 (moderate) — Stock reconciliation**

The asset register showed 45 loan laptops at the start of the month. During the month: 12 were issued to users, 7 were returned, 3 new laptops were added to stock, and 2 were retired from stock as beyond repair. A physical count at month end finds 39 laptops in the store. What does the register predict, and what is the discrepancy?

- A) Register predicts 41; discrepancy of 2
- B) Register predicts 40; discrepancy of 1
- C) Register predicts 39; no discrepancy
- D) Register predicts 43; discrepancy of 4

**Correct answer: A**

**Explanation:** Work the movements from the opening balance: 45 − 12 (issued out) = 33; 33 + 7 (returned) = 40; 40 + 3 (new stock) = 43; 43 − 2 (retired) = 41. The register therefore predicts 41 laptops in the store; the physical count found 39, a discrepancy of 2 — answer A. The arithmetic is simple; the discipline is signs: issues and retirements subtract, returns and additions add. Operationally, a discrepancy of 2 is not a rounding matter — it is two devices whose location and state cannot be verified, which your asset and configuration management skill exists to prevent. The correct next step in practice is investigation (recent unrecorded issues? devices at repair?) and correction of the register, not quiet adjustment of the number to match the shelf.

**Question 7 (moderate) — First-time fix rate with exclusions**

Your first-time fix (FTF) definition: incidents resolved by the first engineer without reassignment, as a percentage of all incidents closed; incidents reopened within 5 working days are excluded from the numerator but stay in the denominator. Last month: 180 incidents closed; 126 resolved by the first engineer without reassignment; of those 126, 9 were reopened within 5 working days. What is the FTF rate?

- A) 70%
- B) 65%
- C) 75%
- D) 61%

**Correct answer: B**

**Explanation:** Build the fraction from the definition. Denominator: all incidents closed = 180. Numerator: first-engineer resolutions (126) minus the quick reopens excluded by the rule (9) = 117. Rate: 117 ÷ 180 = 0.65 = 65% — answer B. Option A (126 ÷ 180 = 70%) forgets the exclusion; option D subtracts 9 from both top and bottom (117 ÷ 171 ≈ 68.4%, which is not even offered accurately — a sign that method was wrong); option C is a plausible-looking distractor with no valid derivation. The professional point: KPI definitions with inclusion and exclusion rules must be computed exactly as written, because a two-line definition can move a headline figure by five points. When you produce or check reports, sketch the fraction first — what exactly goes on top, what exactly goes underneath — before touching the calculator.

**Question 8 (moderate) — Interpreting a utilisation chart**

A described bar chart shows walk-up desk visitors by hour: 09:00: 14; 10:00: 9; 11:00: 7; 12:00: 12; 13:00: 15; 14:00: 8; 15:00: 6; 16:00: 5. The desk can serve roughly 10 visitors per hour with one engineer. Which staffing conclusion does the data best support?

- A) Two engineers all day, to be safe.
- B) One engineer all day — the daily average of 9.5 visitors per hour is below capacity.
- C) One engineer for most of the day, with a second engineer covering the 09:00 opening and the 12:00–14:00 lunchtime peak.
- D) Close the desk from 15:00 — demand is too low to justify it.

**Correct answer: C**

**Explanation:** First find the shape, then the numbers. Demand exceeds the 10-per-hour capacity in three hours: 09:00 (14), 12:00 (12), and 13:00 (15); it is comfortably below capacity from 14:00 onward. Option C matches staffing to that shape. Option B illustrates a classic averaging error: the mean (14+9+7+12+15+8+6+5 = 76; 76 ÷ 8 = 9.5) is below 10, but averages smooth away exactly the peaks where queues form — users at 13:00 experience the 15-visitor hour, not the 9.5 average. Option A over-staffs five quiet hours to solve three busy ones. Option D leaps from "quieter" to "close" — 5 or 6 visitors an hour is reduced demand, not zero demand, and abandoning them fails the service. This is what turning quantitative data about users into outcomes looks like in miniature: read the distribution, not just the average, and match resource to when users actually arrive.

**Question 9 (challenging) — Comparing performance fairly across engineers**

A manager drafts a league table: Engineer A closed 60 tickets with an average resolution of 40 minutes; Engineer B closed 45 tickets averaging 65 minutes. The manager concludes B is underperforming. You check the mix: A's tickets were 80% password resets (target 15 minutes); B's were 70% hardware faults (target 90 minutes). What is the fairest reading?

- A) The manager is right — B is slower and closed fewer tickets.
- B) The raw comparison is invalid: the engineers handled different work mixes, and against category targets B's 65-minute average on mostly 90-minute-target work may actually be strong, while A's figures reflect a queue of quick tasks.
- C) A is underperforming, not B.
- D) Both engineers are performing identically.

**Correct answer: B**

**Explanation:** Averages are only comparable when the underlying work is comparable. Engineer A's queue was dominated by password resets with a 15-minute target — a mix that mechanically produces low averages and high counts. Engineer B's queue was dominated by hardware faults with a 90-minute target: an average of 65 minutes on that mix sits well inside target, which suggests efficient work on harder tickets. So the league table's raw comparison is invalid — answer B. Note what B does not claim: it does not conclude A is bad (option C invents a symmetrical error) — A may be performing perfectly well on the work assigned; the point is that the comparison, not either engineer, is broken. The fair method is to compare each engineer's times against the targets for their own ticket mix. This matters directly to your reporting skill — interpret a data set and communicate this to others — and to team health: unfair league tables corrode morale and teach engineers to cherry-pick easy tickets, which is a worse outcome than the one the table tried to measure.

**Question 10 (challenging) — Consumables run-out and reorder timing**

Your team replaces laptop batteries at a steady rate of 6 per week. Stock today: 27 batteries. Supplier lead time: 4 weeks from order to delivery. Orders can only be placed on Mondays (today is Monday, and you can order today). To avoid ever running out, what is the latest Monday you can place the order, and how many batteries remain when the delivery arrives if you order then?

- A) Order today; 3 remain at delivery
- B) Order next Monday (week 2); 0 remain — delivery arrives exactly at run-out
- C) Order today; 27 remain at delivery
- D) Order in week 3; 3 remain at delivery

**Correct answer: A**

**Explanation:** First find run-out: 27 ÷ 6 = 4.5 weeks — stock runs out midway through week 5. A delivery ordered on the Monday of week W arrives at the start of week W + 4. Ordering today (week 1) delivers at the start of week 5: consumption by then is 4 weeks × 6 = 24, leaving 27 − 24 = 3 batteries — the delivery lands just before the mid-week-5 run-out, with 3 in hand. Answer A. Test the alternative: ordering in week 2 delivers at the start of week 6, but stock hits zero mid-week 5 — half a week of outage, so option B's arithmetic actually describes a failure, not a safe order. Options C and D contain arithmetic errors (C forgets consumption during the lead time entirely). The transferable method: run-out date first, then step back by the lead time, then respect the ordering calendar — three constraints, applied in order. Routine maintenance and administration lives on small calculations like this; the engineer who does them keeps users working while the one who "had plenty last time they looked" does not.

**Question 11 (challenging) — Weighted average across sites**

You support two sites. Site 1 closed 150 incidents with 90% inside SLA; Site 2 closed 50 incidents with 70% inside SLA. A colleague averages the percentages: "(90 + 70) ÷ 2 = 80% overall." What is the true combined SLA figure?

- A) 80%
- B) 82%
- C) 85%
- D) 87.5%

**Correct answer: C**

**Explanation:** Percentages from different-sized groups cannot be averaged directly; convert to counts first. Site 1: 90% of 150 = 135 inside SLA. Site 2: 70% of 50 = 35 inside SLA. Combined: (135 + 35) ÷ (150 + 50) = 170 ÷ 200 = 0.85 = 85% — answer C. The colleague's simple average of 80% treats the sites as equal, but Site 1 closed three times as many incidents, so its 90% deserves three times the weight — and indeed 85% sits three-quarters of the way from 70% toward 90%. This error — averaging averages — is one of the commonest in service reporting, and it always biases toward the smaller group. Catching it is exactly what your reporting skill means by interpreting a data set correctly, and gently correcting it ("let's weight by volume") is the kind of contribution that builds a team's trust in its own numbers.

**Question 12 (challenging) — Trend and projection with a caveat**

Reopened-incident counts over four months: May 8, June 12, July 18, August 27. A manager asks: "If this continues, what should we expect in September, and how much confidence should we place in that number?" Which answer is best?

- A) About 40 — each month has been roughly 1.5 times the previous month, and 27 × 1.5 ≈ 40; but a four-point trend is thin evidence, so treat it as a planning estimate and investigate the cause of the growth rather than just forecasting it.
- B) Exactly 41 — the pattern adds 4, then 6, then 9, so next it adds 14.
- C) About 33 — add the average monthly increase of 6.3 to August's 27.
- D) It cannot be estimated.

**Correct answer: A**

**Explanation:** First characterise the growth. Differences: +4, +6, +9 — the increases themselves grow, so the trend is not linear, and option C's straight-line method (mean increase (8→27 over three steps) ≈ 6.3; 27 + 6.3 ≈ 33) will undershoot a compounding pattern. Check ratios instead: 12 ÷ 8 = 1.5; 18 ÷ 12 = 1.5; 27 ÷ 18 = 1.5 — consistent multiplicative growth of 50% per month, projecting 27 × 1.5 = 40.5 ≈ 40 for September. Option A pairs the right arithmetic with the right humility: four data points support a working estimate, not a certainty, and — the professionally decisive part — a metric compounding at 50% monthly is a problem to investigate, not merely a number to forecast. Reopens growing like this usually signal fixes that do not hold, a knowledge gap, or a new fault class: precisely the pattern-and-trend investigation your problem management skill calls for. Option B forces an over-precise pattern the differences do not quite support; option D gives up on data that plainly supports an estimate. Report the number, flag the uncertainty, chase the cause.

### Preparation tips

- **Master the four core moves.** Percentage (part ÷ whole), percentage change (difference ÷ original), weighted combination (convert to counts, then divide), and mean versus median. Nearly every service-data question is one of these wearing work clothes.
- **Sketch the fraction before calculating.** For any rate or KPI question, write down exactly what belongs in the numerator and denominator — including exclusions — before touching the calculator. Most KPI errors are fraction-construction errors, not arithmetic ones.
- **Convert percentages to counts when combining.** Whenever two groups of different sizes appear, averaging their percentages is almost certainly the trap. Counts first, division last.
- **Track SLA clocks as consumed and remaining.** Two running numbers make pauses, weekends and part-days mechanical. Practise with your own team's SLA definitions until the method is automatic.
- **Sense-check every answer against the data's shape.** Is the result inside the plausible range? Does it sit nearer the bigger group? Would a user recognise it as describing their experience? Ten seconds of sense-checking catches most slips.
- **Rebuild one real report by hand.** Take last month's team report and reproduce two of its figures from raw data. Whatever friction you hit — definitions, exclusions, mismatched totals — is exactly what assessments test, and finding it improves your actual reporting.

### Common pitfalls to avoid

- **Comparing counts when the question asks for rates.** The biggest raw number is rarely the answer to a "highest rate" question. Divide first.
- **Using the wrong base in change questions.** Percentage change divides by the starting value — always. Watch for options built on the ending value; they are planted deliberately.
- **Averaging averages.** Combining 90% and 70% into 80% ignores group sizes and is nearly always wrong. This single pitfall probably appears in more service-reporting questions than any other.
- **Letting the mean speak for the peaks.** Capacity and staffing questions turn on distribution — when demand arrives — not on daily averages that smooth queues out of existence.
- **Forgetting definitional exclusions.** If a KPI definition removes reopened incidents from the numerator, the calculation must too. Read definitions as algorithms, not descriptions.
- **Projecting without characterising.** Before extending a trend, check whether growth is additive or multiplicative — differences versus ratios. The wrong model produces a confident, wrong forecast; and any forecast from a handful of points deserves a stated caveat.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret, and draw conclusions from written material — using the documents an end user computing engineer genuinely works with: knowledge articles, change procedures, security policies, handover notes, service announcements, and user emails.

The typical format is an online, timed test of 15 to 25 minutes. You are shown a short passage and asked structured questions about it. The dominant style is **true / false / cannot say**: decide whether a statement is definitely supported by the passage, definitely contradicted, or simply not addressed. Other styles include choosing the best summary, identifying what a message is actually requesting, and judging which of several drafts communicates most clearly. The governing rule never changes: answer from the passage alone. Your technical knowledge — however sound — must not be imported into the text.

Why does this matter for your role? Because in desk-side support, reading is a safety-critical activity. A knowledge article's stop condition, a change procedure's exclusion clause, a security policy's "must" versus "should" — these carry operational force, and misreading them creates incidents rather than resolving them. Handover notes carry the state of live investigations; misreading one means repeating ruled-out steps or, worse, undoing a colleague's progress. User messages carry needs wrapped in mislabelled symptoms; extracting the real report is the first act of every accurate diagnosis. And your own writing matters just as much: informing customers on progress, advising on workarounds, and documenting resolutions for the knowledge base all depend on producing text that others can trust. Since you also coach associates, you are increasingly the person who explains what a procedure actually says — which requires reading it better than anyone.

The assessment does not reward vocabulary or speed-reading tricks. It rewards disciplined extraction: what does this text state, what does it rule out, and what does it leave open?

### How this assessment maps to your role

- **Comprehension of procedures** maps to your **Change management** and **Testing** skills: implementing change requests and executing test scripts under supervision demand exact reading of ordered steps, gates, and conditions — "do not proceed" clauses have no tolerance for paraphrase.
- **True/false/cannot-say discipline** maps to your **Problem management** skill: fair investigation separates what the evidence states from what you suspect; the same discipline separates "the passage says" from "I happen to know."
- **Extracting the real request** maps to your **User focus** and **Incident management** skills: identifying and engaging with users to collate needs evidence starts with reading their words accurately — the stated symptom, the recent change, the deadline, and the need beneath the request.
- **Reading definitions precisely** maps to your **IT service reporting** and **Service management framework knowledge** skills: KPI definitions and framework terms (incident versus problem versus known error) are exact vocabularies where near-synonyms change meanings.
- **Clear-writing judgement** maps to your duty of **informing customers on progress and advising on workarounds**, and to **coaching associates**: your updates, handovers and knowledge articles become other people's source texts, so writing clearly is reading's twin skill.

### Practice questions

**Question 1 (easy) — Comprehension of a knowledge article**

A knowledge article states: "Before replacing a suspected faulty docking station, test the user's laptop with a known-good dock. Replace the dock only if the known-good dock works normally with the user's laptop. If the known-good dock also fails, escalate to the hardware team — do not replace either device."

Statement: "If the user's laptop fails with the known-good dock, you should replace the user's dock."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The article defines two branches. Branch 1: known-good dock works with the laptop → replace the original dock. Branch 2: known-good dock also fails → escalate, and explicitly do not replace either device. The statement describes branch 2 (the laptop fails with the known-good dock) but attaches branch 1's action (replace the dock) — the passage directly contradicts it, so the answer is false, not "cannot say." The underlying logic is worth internalising: if the laptop fails with a good dock, the evidence points at the laptop, and replacing the dock would treat an exonerated component. Notice how the article encodes correct diagnostic reasoning as a procedure — reading it precisely and understanding why it says what it says are the same skill viewed from two angles, which is exactly what you will explain when an associate asks why they cannot just swap the dock.

**Question 2 (easy) — What is the user actually reporting?**

A user emails: "Subject: URGENT laptop replacement needed. Hi — I'm sure my laptop is dying and needs replacing. It's got really slow over the past month, the fan is loud all the time, and yesterday a message popped up about my disk being almost full. I've got performance reviews to write this week and can't afford downtime. Please just swap it for a new one."

Which reading best captures the situation?

- A) The user needs an urgent replacement laptop this week.
- B) The user reports gradual slowness, constant fan noise, and a disk-nearly-full warning, and has requested a replacement; the symptoms suggest the request and the need may differ, and the real constraint is avoiding downtime during review-writing week.
- C) The laptop has a hardware fault and must be replaced.
- D) The user's real problem is the performance reviews.

**Correct answer: B**

**Explanation:** Separate the report (symptoms), the request (a swap), and the need (no downtime this week). The symptoms — gradual slowdown, loud fan, disk nearly full — are classic signs of a resource-constrained machine and may well be resolvable in place, which matters because the user's own priority, avoiding downtime, is arguably better served by a quick fix than by the migration a replacement involves. Option B captures all three layers without prejudging the diagnosis. Option A adopts the user's proposed solution as the requirement. Option C converts suspicion into a hardware verdict the text cannot support. Option D is flippant. This is your user focus skill in written form: users state solutions; engineers read for needs. And the distinction is precisely what you would flag when coaching an associate through triaging this ticket — respond to the need beneath the request, while taking the request seriously as evidence of how the user feels.

**Question 3 (easy) — True/false/cannot say on a service notice**

A notice reads: "The VPN service will be upgraded on Wednesday between 19:00 and 22:00. Users connected during this window will be disconnected and unable to reconnect until the upgrade completes. Office-based network access is unaffected."

Statement: "The upgrade will finish by 22:00 on Wednesday."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The notice states when the upgrade will occur — "between 19:00 and 22:00" — which is a planned window, not a guarantee of completion. Windows overrun; the text neither promises completion by 22:00 nor denies it. So the passage does not determine the statement: cannot say. The tempting error is "true," reading the window's end as a commitment — but a careful engineer knows, and the text confirms only, that the work is scheduled within the window. This distinction has real communication consequences: told a user "you'll definitely be reconnected by 22:00," you have made a promise the notice never made, and overruns then land on your credibility. The accurate version — "the planned window ends at 22:00" — is one word longer and infinitely more honest. Precision in reading enables precision in promising.

**Question 4 (moderate) — Following a procedure with stacked conditions**

A security procedure states: "(1) All laptops must be encrypted before issue. (2) Laptops for staff handling protectively marked material must additionally have the enhanced security build. (3) Loan laptops are exempt from the enhanced build requirement, except loans to staff handling protectively marked material, which must have the enhanced build regardless of loan status. (4) No exemptions to rule 1 exist."

A caseworker who handles protectively marked material needs a loan laptop urgently. What does the procedure require?

- A) Encryption only — loan laptops are exempt from the enhanced build.
- B) Both encryption and the enhanced security build.
- C) The enhanced build only — encryption can follow later given the urgency.
- D) The procedure does not cover loans to such staff.

**Correct answer: B**

**Explanation:** Trace each rule. Rule 1: encryption — universal, and rule 4 slams the door on any exemption, urgent or not, so option C fails immediately. Rule 3 is the subtle one: it grants loan laptops an exemption from the enhanced build, then withdraws that exemption for exactly this case — loans to staff handling protectively marked material "must have the enhanced build regardless of loan status." So both requirements apply: encryption (rules 1 and 4) and the enhanced build (rule 3's exception to the exemption) — answer B. Option A reads rule 3's first clause and stops before its "except"; option D pretends the clause that decides the case does not exist. Exception-within-exemption structures are common in security policy, and the reading method is mechanical: for each rule, ask "does this apply to my case?" and read to the end of the sentence before answering. Half-read rules are how urgent loans go out insecure — and why change and security procedures reward engineers who read like auditors.

**Question 5 (moderate) — Inference from a handover note**

A handover note reads: "INC-41022 — intermittent black screens on user's laptop during video calls. Ruled out: cable (replaced, no change), monitor (fault follows laptop to other monitors), recent OS update (rolled back, no change). Graphics driver update applied 16:40 — too late to test with a real call. User warned it may recur; asked to report either way tomorrow. If it recurs, next step is hardware diagnostics on the graphics chip."

Statement: "The engineer has identified the graphics driver as the cause of the fault."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The note shows the engineer treating the driver as the current hypothesis — an update was applied, and a hardware fallback is queued "if it recurs." But has the note stated the driver is the cause? No: the fix is untested ("too late to test"), the user was explicitly warned it may recur, and a next step exists precisely because the diagnosis is unconfirmed. Equally, nothing contradicts the driver hypothesis — no recurrence has been observed since the update. The passage therefore neither establishes nor refutes the statement: cannot say. Choosing "true" mistakes a hypothesis under test for a conclusion; choosing "false" mistakes absence of confirmation for refutation. This is the epistemic state most live investigations occupy, and the note models excellent practice: what is ruled out, what is applied, what is untested, what happens next. When you write handovers — and when you teach associates to — this is the standard: a reader should be able to tell your conclusions from your hypotheses at a glance.

**Question 6 (moderate) — Choosing the clearest user update**

A user's incident (intermittent laptop crashes) is with the hardware team awaiting a part; expected fix Thursday. The user is anxious and has chased twice. Which update is best?

- A) "Your incident remains open with our hardware resolver group pending component availability. SLA obligations continue to be monitored."
- B) "Hi — an update on your laptop crashes: the cause is a faulty memory module, and the replacement part is due Wednesday. We expect your repair to be finished by Thursday. I know you've chased twice and I'm sorry for the wait — I'll update you Wednesday when the part arrives, even if there's no other news. Meanwhile the loan laptop is yours as long as you need it."
- C) "Hi — this is now with the hardware team, so it's out of my hands. They'll be in touch."
- D) "Hi — good news, this will all be sorted very soon! Nothing to worry about at all."

**Correct answer: B**

**Explanation:** Judge each draft against what a good update must do: state cause and status, give a dated expectation, acknowledge the user's experience, commit to the next contact, and confirm the workaround. Option B does all five — and its most trust-building sentence is the promised Wednesday update "even if there's no other news," which is what actually stops a user chasing: not resolution, but reliable contact. Option A is process-speak — accurate, cold, and unreadable to a non-technical user; "SLA obligations continue to be monitored" comforts nobody. Option C commits the ownership sin — "out of my hands" — which your role summary explicitly forbids: you own an issue until a new owner has been found, and even after handover, the user should feel continuity, not abandonment. Option D is warmth without content and makes an implicit promise ("very soon") that Thursday may break. The pattern is worth writing on a sticky note: cause, date, empathy, next contact, workaround. Five sentences, every time.

**Question 7 (moderate) — Precise reading of a policy definition**

A policy defines: "A Major Incident is an incident causing, or likely to cause, service unavailability to fifty or more users, or any service unavailability affecting a service on the critical services register, regardless of user count. Major Incidents must be declared to the incident manager within fifteen minutes of identification."

Statement: "An incident making a critical-register service unavailable to twelve users must be declared to the incident manager within fifteen minutes."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Parse the definition's two routes to Major Incident status. Route one: fifty or more users affected. Route two: any unavailability of a critical-register service, "regardless of user count." The scenario — a critical-register service unavailable to twelve users — fails route one but exactly satisfies route two; the phrase "regardless of user count" exists precisely to make twelve (or two) sufficient. Once classified Major, the declaration duty follows: fifteen minutes from identification. So the statement is true. The error to avoid is anchoring on the memorable number: fifty sticks in the mind, and candidates (and, in real service desks, engineers at 2 a.m.) wrongly treat it as the sole gate. Definitions with "or" create independent doors; walking through either one triggers everything downstream. Your service management framework knowledge is largely a vocabulary of such definitions — incident, problem, known error, Major Incident — and this question shows why the framework insists on them: at the moment of declaration, precision of reading becomes speed of response.

**Question 8 (moderate) — Best summary of a change notice**

A notice reads: "From 1 June, the standard laptop build will move to version 12. New issues from that date will carry v12. Existing laptops will be upgraded in a phased programme over twelve weeks, scheduled by directorate; users will receive fourteen days' notice and can rebook once within their directorate's window. Devices not upgraded by the end of their window will lose access to the corporate network until upgraded. Known incompatibility: the legacy case-recording application does not run on v12; affected teams will receive the replacement application before their upgrade window opens."

Which summary is best?

- A) All laptops will be upgraded to v12 on 1 June, and the legacy case-recording application will stop working.
- B) From 1 June new laptops get v12; existing ones upgrade in phased, directorate-scheduled windows over twelve weeks with notice and one rebooking; missing your window costs network access until upgrade; teams using the incompatible legacy case-recording application get its replacement before their window.
- C) Users can postpone the v12 upgrade indefinitely, though they may lose network access.
- D) The upgrade mainly affects the case-recording application, which is being replaced from 1 June.

**Correct answer: B**

**Explanation:** A faithful summary keeps every operationally decisive element and adds nothing. Option B preserves all six: the start date's real meaning (new issues only), the phased twelve-week programme, the notice-and-one-rebooking allowance, the consequence of missing a window (network access lost until upgraded), the named incompatibility, and the mitigation's sequencing ("before their window" — the detail that stops teams losing their casework tool). Option A compresses the phased programme into a single-day event and inflates the incompatibility into a bare loss, dropping the replacement entirely — two distortions in one sentence. Option C converts "rebook once" into "postpone indefinitely," exactly inverting the notice's constraint. Option D mistakes a subordinate detail for the main event. Summarising notices like this is a daily reality of your role: you are often the person a user asks, "so what does this actually mean for me?" — and the six elements B preserves are precisely the six a user needs. In the assessment, check each candidate summary for the three classic distortions: compression of timelines, dropped qualifiers, and promoted side-issues.

**Question 9 (challenging) — Inference across two documents**

Document 1 (asset policy): "Devices unaccounted for after two consecutive physical audits must be reported as lost, and their remote-wipe initiated within one working day of the second audit."
Document 2 (audit report, dated today): "LT-3310: not located in March audit. Located June audit in Building D storeroom, unlogged. LT-3320: not located in March audit; not located in June audit. LT-3330: located March; not located June."

Statement: "The policy requires LT-3320's remote-wipe to be initiated within one working day of today's report, but does not require this for LT-3310 or LT-3330."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Apply the policy's trigger — unaccounted for after two consecutive audits — to each device. LT-3320: missed March and June, two consecutive misses; the trigger fires, and the wipe clock (one working day from the second audit, reported today) is running. LT-3310: missed March but was located in June — the June find breaks the consecutive-miss sequence, so no trigger, though its unlogged storeroom presence is a register correction waiting to happen. LT-3330: located in March, missed only June — one miss so far; the trigger requires a second consecutive miss, which only a future audit could supply. So the statement is exactly right: wipe required for LT-3320 alone — true. The reasoning skill here is applying a general rule to a table of cases, one case at a time, resisting two temptations: treating any missing device as wipe-worthy (over-application) and letting LT-3310's messy reappearance blur the analysis (noise). This is precisely how asset compliance works in practice — policies are algorithms, audit reports are their input, and the engineer who executes them accurately is the one whose register can be trusted.

**Question 10 (challenging) — Distinguishing framework terms in context**

A passage from a service report reads: "Fourteen users reported login failures on Tuesday (tickets logged individually). Wednesday's investigation traced all fourteen to a certificate that expired Monday night. A workaround — the web login route — was documented and shared. The certificate renewal is scheduled as a change for Friday's window. The certificate expiry has been recorded with its workaround for future reference."

Statement: "The passage describes fourteen problems, one incident, and one known error."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Map the passage onto framework vocabulary. The fourteen user reports are fourteen incidents — individual instances of service disruption, logged as tickets. The single underlying cause (the expired certificate) is one problem — the root cause behind the incident cluster. Once that cause was diagnosed and documented with its workaround "for future reference," it became a known error. The renewal scheduled for Friday is a change. The statement inverts the first two: it claims fourteen problems and one incident — exactly backwards — so the passage contradicts it: false. This is more than terminology pedantry: the framework's numbers drive real process. Fourteen incidents cluster into one problem record so that investigation happens once, not fourteen times; the known-error record with its workaround lets tomorrow's service desk resolve recurrence in minutes. Your Level 3 service management qualification gives you this vocabulary; verbal reasoning questions test whether you can hold it steady while a passage tries to blur it — and coaching associates tests whether you can explain the difference in one breath: many incidents, one cause, one lesson.

**Question 11 (challenging) — Tone and content in a difficult message**

You must email a team of thirty users whose building's network will be down for four hours tomorrow because an earlier fix by your own team was applied incorrectly and must be redone. Which draft is best?

- A) "Due to unforeseen technical circumstances, network services will be unavailable tomorrow 08:00–12:00. We apologise for any inconvenience."
- B) "Hi all — the network in your building will be down tomorrow 08:00–12:00 while we redo a fix that our team applied incorrectly last week. We're sorry: this second outage is on us. What this means for you: no wired or Wi-Fi access in the building during the window; the ground-floor hub and home working are unaffected, and 4G tethering is available for anyone who needs a connection — reply and we'll set it up today. We'll confirm completion by email before 12:00."
- C) "Hi all — tomorrow's outage (08:00–12:00) is required because of an error in previous engineering work. Questions to the service desk."
- D) "Hi all — unfortunately the network will be down again tomorrow morning. These things unfortunately happen with complex systems and we appreciate your patience as always."

**Correct answer: B**

**Explanation:** The situation demands three difficult things at once: honesty about your team's error, operational clarity, and practical mitigation. Option B delivers all three — it names the cause plainly ("our team applied incorrectly... this second outage is on us"), which reads as accountability rather than weakness; it translates the outage into user consequences (what stops working, what still works); it offers an actionable workaround with a same-day setup route; and it commits to a completion confirmation, closing the loop before users need to chase. Option A hides the cause behind "unforeseen technical circumstances" — a phrase that, for an error your team made, is closer to misdirection than diplomacy, and users who later learn the truth remember the hiding longer than the outage. Option C admits the error in passive officialese ("an error in previous engineering work") while offloading all questions, and offers no workaround. Option D apologises for the world instead of the mistake and mistakes vagueness ("down again tomorrow morning") for gentleness — it does not even give the window precisely. The professional principle, which your ownership skill formalises: when the fault is yours, plain acknowledgement plus concrete mitigation rebuilds trust faster than any wording can protect it.

### Preparation tips

- **Demand a sentence of evidence.** For every true/false/cannot-say answer, point (literally, with a finger or cursor) at the sentence that supports it. No sentence, no verdict — the answer is probably "cannot say."
- **Read rules to the end.** Exceptions, exclusions and "regardless of" clauses live in the second half of sentences. Train yourself never to classify a case until the full rule — including its tail — has been read.
- **Sort statements into three bins deliberately.** "Contradicted by the text" (false), "guaranteed by the text" (true), and "the text is silent" (cannot say). Most errors are boundary errors between false and cannot-say; practising the sort directly is the fastest fix.
- **Practise the framework vocabulary under pressure.** Write one-line definitions of incident, problem, known error, change, and Major Incident from memory, then check them against your framework notes. Passages that blur these terms are a favourite question type for service roles.
- **Audit your own writing weekly.** Take one update or handover you wrote and test it: could a reader distinguish conclusions from hypotheses? Is there a date, a next contact, a workaround? Writing to the standard sharpens your eye for reading to it.
- **Use real documents as gyms.** Security policies, change notices and knowledge articles from your own organisation make ideal practice passages. Write two statements about each — one false, one cannot-say — and notice how the difference feels from the setter's side.

### Common pitfalls to avoid

- **Importing your technical knowledge.** You may know how certificate renewals work; the question only cares what the passage says. Expertise applied to the wrong task is the verbal test's signature trap for experienced engineers.
- **Reading windows as promises.** "Between 19:00 and 22:00" schedules work; it does not guarantee completion. Options converting plans into commitments are planted for the incautious.
- **Stopping at the memorable number.** Definitions often pair a headline threshold with an independent "or" clause. The fifty-user rule you remember is not the only door into Major Incident status.
- **Treating hypotheses as conclusions.** Handover notes describe investigations in flight. "Applied a fix" plus "asked the user to report back" means unconfirmed — and "cannot say" beats both premature verdicts.
- **Choosing summaries that compress or promote.** Wrong summaries collapse phased timelines into single events, drop the qualifier that changes everything, or elevate a side detail into the headline. Check candidates against the original element by element.
- **Writing (and choosing) evasive drafts.** In clear-writing questions, options hiding a team's error behind "unforeseen circumstances" score as badly with assessors as they eventually do with users. Accountability plus mitigation is the pattern the scoring key rewards.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of different responses. The material is human rather than technical: a user under deadline pressure, a change that goes wrong mid-implementation, an associate out of their depth, a conflict between speed and process. For each scenario you typically choose the **most effective** response, the **least effective** response, or rate every option on an effectiveness scale.

The typical format is an online test of 10 to 20 scenarios, untimed or generously timed — the emphasis is judgement, not speed. Responses are scored against the pooled judgement of experienced professionals and the organisation's values. For UK government digital roles, that means professional behaviours: user focus, ownership, collaboration, honesty, appropriate escalation, and inclusion.

Why do employers use SJTs for end user computing engineers? Because at your level, the difficult decisions are rarely purely technical. You work at users' desks, where every fix happens inside a relationship. You own issues until a new owner is found or the problem is resolved — which means constantly judging when to persist, when to escalate to service desk managers, incident managers or problem managers, and how to hand over without dropping the user. You implement changes under control procedures that sometimes collide with urgent requests. And you coach associates, which adds judgement calls about when to step in, when to let someone struggle productively, and how to correct without crushing. An SJT samples exactly these decisions.

A useful orientation: at your level, scoring keys reward engineers who protect the user's outcome, follow the process while making it work harder, escalate with evidence rather than emotion, and treat colleagues — especially juniors — as people to develop rather than route around. Heroics score poorly; so does hiding behind process. The strong answers are active, honest, and proportionate.

### How this assessment maps to your role

- **Escalate or persist** maps to your **Ownership and topic** skill: owning an issue until a new owner has been found or the problem has been mitigated or resolved is a continuous judgement — the assessment tests whether you escalate the right things, at the right moment, with the right evidence, and without abandoning the user mid-handover.
- **Process under pressure** maps to your **Change management** and **Asset and configuration management** skills: implementing change requests and applying change control procedures under supervision, and keeping asset records accurate, are exactly the rules that urgent situations tempt you to bend.
- **Coaching judgement** maps to your role's duty to **coach associates and share knowledge**: scenarios probe whether you develop capability (questions, guided practice) or create dependence (taking over) or risk (rubber-stamping).
- **User care under failure** maps to your **User focus** skill and your duty of **informing customers on progress and advising on workarounds**: the hardest communication happens when things go wrong — SJTs test honesty, empathy, and practical mitigation together.
- **Team collaboration** maps to your **Problem management** and **Service focus** skills: contributing to remedies and preventative measures, and working within coherent frameworks, means raising patterns, supporting colleagues' investigations, and putting the service ahead of personal credit.

### Practice questions

**Question 1 (easy) — Mid-change complication**

You are implementing an approved change: replacing a failing network switch during the 12:00–14:00 window. At 12:40, with the old switch removed, you discover the replacement unit was supplied with the wrong power cable. The correct cable is in the store, 20 minutes away; the window closes at 14:00; the affected floor is without network until you finish.

Which response is most effective?

- A) Improvise with a similar-looking cable from a nearby cupboard to save time.
- B) Send for (or fetch) the correct cable immediately, notify the change coordinator of the complication and revised completion estimate, and update the affected floor's contact with the new expected time.
- C) Abandon the change, reinstall the old failing switch, and rebook the window for next week.
- D) Continue the physical installation and leave the power connection for whoever is on shift after 14:00.

**Correct answer: B**

**Explanation:** Test each option against three duties: the users' outcome, the change process, and honest communication. Option B honours all three — the 20-minute round trip still completes the change comfortably inside the window (13:00–13:20 arrival, well before 14:00), the change coordinator learns of the complication while it is still manageable rather than after it becomes a failure, and the affected users get a revised expectation instead of silence. Option A gambles a switch — and the floor's network — on a cable that merely looks right; improvised power on infrastructure equipment is precisely the kind of shortcut change control exists to prevent. Option C over-corrects: rolling back to a failing switch buys a week of known risk to avoid a 20-minute delay — proportionality matters in both directions. Option D walks away from an incomplete change at a shift boundary, leaving live disruption and an undocumented handover — the opposite of owning an issue until a new owner has been found. The scored pattern: absorb the complication, keep the plan honest, keep everyone informed.

**Question 2 (easy) — The VIP queue jump**

You are at a user's desk mid-repair when a director's assistant arrives: "The director's laptop won't start and she has a board meeting in an hour — you need to come now." Your current user's fault is genuine but not urgent: a second monitor issue, with a working laptop.

Which response is most effective, and which is least effective?

- A) Refuse to move until the current job is finished — first come, first served.
- B) Explain the situation honestly to your current user, ensure they can work meanwhile, go to the director's machine, and register both contacts properly so the interrupted job is tracked and returned to.
- C) Drop everything and go immediately, without a word to the user whose desk you are at.
- D) Tell the assistant to log a ticket with the service desk and await triage like everyone else.

**Correct answer: most effective B; least effective C**

**Explanation:** Genuine urgency justifies re-prioritisation: a non-starting laptop an hour before a board meeting is high impact and hard-deadlined, while a monitor fault beside a working laptop can wait. But how you re-prioritise is what the question actually tests. Option B moves fast and leaves no wreckage — the current user hears the reason, keeps working, and keeps a tracked ticket, so the interruption costs them minutes of delay rather than trust; registering the director's contact also keeps the queue honest rather than invisible. Option C reaches the director just as fast but abandons a user mid-repair without explanation — the sort of experience that teaches users the desk only serves the powerful, and it is the least effective option. Option A applies queue fairness as an absolute, ignoring impact and urgency — rules about ordering exist to serve outcomes, not to defeat them. Option D is process-correct and judgement-poor: triage would conclude what you can already see. Note that seniority itself is not the justification — the deadline and the dead laptop are. If the director's fault had been a flickering screensaver, B's structure would apply in reverse.

**Question 3 (easy) — An associate's risky confidence**

You overhear an associate on the phone confidently telling a user to delete a set of files to fix a disk-space problem. From the folder names the associate reads out, you recognise application data whose deletion would break the user's software.

Which response is most effective?

- A) Interrupt immediately but calmly — ask the associate to put the user on hold, explain the risk privately, help them give corrected advice, and afterwards walk through how to verify a folder's purpose before advising deletion.
- B) Wait until the call ends, then explain the error so the associate is not embarrassed mid-call; the user can be called back to undo the advice.
- C) Say nothing — associates learn best from the consequences of their own mistakes.
- D) Take the phone from the associate and finish the call yourself.

**Correct answer: A**

**Explanation:** Weigh the competing goods: the user's system, the associate's development, and the associate's dignity. Option A protects all three in the right order. The interruption must be immediate because harm is in flight — once the user deletes application data, the cost jumps from an awkward pause to a broken system and a recovery job; option B knowingly lets the damage land to spare a moment's discomfort, which inverts the priorities (and the call-back may come too late). The hold-and-private-explanation preserves the associate's standing with the user — correction happens offstage, and the associate delivers the corrected advice themselves, staying the competent voice on the call. The afterwards conversation converts the near-miss into capability: teaching the verification habit ("how do we check what a folder is before advising deletion?") is the coaching duty your role names. Option C mistakes negligence for pedagogy — consequences that fall on users are not learning materials. Option D protects the user but publicly displaces the associate, teaching them only that pressure means being replaced. The pattern: stop live harm now, correct privately, teach the method afterwards.

**Question 4 (moderate) — Evidence versus a manager's instinct**

A service desk manager tells you: "These recurring login failures are obviously the users mistyping passwords — close the cluster as user error." Your investigation of the fourteen tickets shows the failures cluster between 08:50 and 09:10, affect only one building, and include several users whose accounts show no failed-password events in the logs.

Which response is most effective?

- A) Close the tickets as instructed — the manager owns the queue.
- B) Quietly keep investigating after closing the tickets, and reopen them if you find proof.
- C) Share your three findings with the manager — the time clustering, the single building, the absence of failed-password events — and recommend the cluster stay open as a possible problem record, escalating to the problem manager if the disagreement stands.
- D) Email the manager's manager stating that the diagnosis is wrong.

**Correct answer: C**

**Explanation:** The evidence contradicts the instructed diagnosis on three independent axes: mistyping does not synchronise to a twenty-minute window, does not respect building boundaries, and — decisively — cannot occur without failed-password events in the logs. Option C brings exactly this evidence to exactly the right person, in the register that changes minds: findings first, recommendation second, and a legitimate escalation route (the problem manager, whose process this genuinely is) if disagreement persists. That is what your role summary means by identifying repeat issues and escalating them — and it is collaboration, not confrontation, because it lets the manager update on facts rather than defend a position. Option A closes fourteen tickets against the evidence; the failures will recur, now stripped of their pattern history. Option B splits your actions from your records — investigating a "closed" cluster off the books corrupts both the data and the trust the team runs on. Option D leapfrogs the manager without ever showing them the evidence, converting a solvable disagreement into a political incident. The scored behaviours: evidence-led challenge, respect for process roles, escalation as a route rather than a weapon.

**Question 5 (moderate) — The unauthorised-software discovery**

At a user's desk fixing an unrelated fault, you notice unapproved file-sharing software installed — the kind your security policy explicitly prohibits. The user, who has been friendly and is under obvious deadline pressure, says: "Oh, that — everyone in our team uses it to send big files to the printers' contractor. Please don't make it a thing."

Which response is most effective, and which is least effective?

- A) Remove the software immediately without discussion — policy is policy.
- B) Say nothing — you were there for a different fault, and the team clearly depends on it.
- C) Explain why the software is a genuine risk, be honest that you must report it, and pair the report with the constructive half: capture the underlying need (large file transfer to an external contractor) so the security and service teams can provide an approved route — flagging that a whole team uses it, which makes it a systemic need, not one user's misdemeanour.
- D) Tell the user you will overlook it this once if they promise to uninstall it after their deadline.

**Correct answer: most effective C; least effective B**

**Explanation:** Unapproved file-sharing software moving files to external parties is a live data-security exposure — discovery obligates you, and "I was there for something else" does not un-see it, which is why option B, comfortable and friendly, is least effective: it leaves the exposure running, team-wide, indefinitely. But the scenario's second layer is what separates adequate from excellent. The users adopted the tool because a real need — large external transfers — has no approved route they know of. Option C reports the risk and represents the need: that is user focus and service focus operating together, and it converts enforcement into service improvement (the likely outcome: an approved transfer route and a team migrated to it, rather than fourteen quiet reinstalls). Option A removes one installation while leaving the team's habit, the contractor workflow, and eleven other desks untouched — and burns the relationship that surfaced the information. Option D makes you privately complicit and postpones the risk on a promise you cannot verify. The professional pattern for policy-versus-practice collisions: enforce the policy, champion the need, and treat "everyone does it" as scoping information for the fix.

**Question 6 (moderate) — Handover without a receiver**

It is 16:50; your shift ends at 17:00. You are mid-investigation on an incident: a caseworker's laptop loses its network connection every few minutes, and you have narrowed the cause to either the port or the machine's network adapter. The evening-shift engineer has called in sick, and the next cover starts at 08:00 tomorrow. The user is working against a 10:00 deadline tomorrow.

Which response is most effective?

- A) Update the ticket with your findings and go home — the morning shift will pick it up.
- B) Stay as long as it takes tonight to finish the diagnosis, without telling anyone.
- C) Spend ten minutes securing the user's outcome — move the user to a known-good port or spare machine so they can work now and first thing tomorrow — then write a precise handover in the ticket (ruled out, remaining hypotheses, exact next test), flag it to the morning shift's queue with the 10:00 deadline, and alert your team lead to the coverage gap.
- D) Give the user your personal number and tell them to call you tonight if it gets worse.

**Correct answer: C**

**Explanation:** The insight this scenario rewards: with no receiver available until 08:00, ownership transfers to the artefacts you leave behind — the workaround and the written handover become the night shift. Option C secures the user's outcome first (a working connection tonight and tomorrow morning, which converts the 10:00 deadline from a crisis into a background fact), then makes the investigation resumable at full speed: "ruled out X, remaining hypotheses Y and Z, next test is Z-first" lets the morning engineer continue rather than restart. Flagging the deadline routes attention; alerting the team lead surfaces the coverage gap — a service issue bigger than this ticket. Option A hands over the diagnosis but abandons the user: findings without a workaround leave the caseworker facing their deadline on a failing connection. Option B may even finish the diagnosis — at the cost of unrecorded lone working and a precedent that coverage gaps are absorbed silently instead of surfaced; the team lead cannot fix a gap nobody reports. Option D substitutes personal heroics for process: unreachable escalation paths, no record, and a user taught to phone engineers instead of the service. Owning an issue until a new owner is found sometimes means manufacturing the new owner — out of a workaround, a flag, and a paragraph of precise writing.

**Question 7 (moderate) — Credit and the knowledge base**

You spent two evenings cracking an obscure fault — an intermittent audio failure tied to a firmware and power-setting interaction — and wrote it up as a knowledge article. Today, in a team meeting, a colleague presents your diagnosis and workaround to the group, describing it in the first person, as work "I got to the bottom of." Your team lead looks impressed.

Which response is most effective?

- A) Correct the record in the meeting: state clearly that the work and the article are yours.
- B) Say nothing in the meeting, but afterwards stop sharing your write-ups so this cannot happen again.
- C) In the meeting, add to the discussion constructively — extra detail on the diagnosis, the article reference for everyone's use — and afterwards raise the misattribution privately and directly with the colleague; involve the team lead only if it recurs.
- D) Reply-all to the meeting invite afterwards with the article's edit history attached.

**Correct answer: C**

**Explanation:** Two goods are at stake: the team's access to the knowledge (which is why you wrote the article) and honest attribution (which sustains people's willingness to keep writing articles). Option C serves both in the right order. Contributing depth in the meeting keeps the technical discussion useful — and, without staging a confrontation, naturally signals your command of the work; pointing everyone to the article serves the service. The attribution issue is then handled where it can actually be resolved: privately, giving the colleague room to have made an honest slip (people do absorb others' work into "I" after reading it) and a clear path to self-correct — many will amend the record unprompted at the next opportunity. Escalation stays proportionate: a pattern goes to the team lead; a single instance gets a conversation. Option A wins the moment and taxes the room — public attribution disputes make every future meeting warier. Option B punishes the whole team's future users for one colleague's behaviour: withholding knowledge is the one outcome worse than misattributed knowledge, and it directly undermines your named duty to share knowledge with team colleagues. Option D is passive aggression on carbon paper. The scored behaviours: service before ego, directness before escalation, proportionality throughout.

**Question 8 (moderate) — The accessibility deprioritisation**

Your team lead asks you to defer a ticket to next week to make room for a laptop refresh project: the ticket is from a user whose screen-reader stopped working after Tuesday's update, and who has been managing since then by borrowing a colleague's eyes. The refresh has a published deadline; the screen-reader user has not complained about the wait.

Which response is most effective?

- A) Defer the ticket as asked — the user is coping, the refresh has a deadline, and the team lead has decided.
- B) Push back immediately: explain that a broken screen-reader means the user cannot work independently at all — equivalent to a dead laptop, not a degraded one — that "coping by borrowing a colleague" is dependence rather than a workaround, and recommend it be treated as urgent, offering to absorb the refresh slippage elsewhere.
- C) Defer it officially but work on it secretly between refresh tasks.
- D) Advise the user to raise a complaint so the ticket's priority increases.

**Correct answer: B**

**Explanation:** The scenario tests whether you can see impact that queue metrics hide. A non-functioning screen-reader is total loss of independent working — the user's quiet coping is not evidence of low impact but of a colleague's donated time and the user's practised endurance; disabled users often under-complain precisely because they are used to waiting. Option B corrects the impact assessment respectfully and concretely (the dead-laptop equivalence gives the team lead the right frame in one phrase), and pairs the challenge with a constructive offer on the refresh — challenge plus help is the register that changes decisions. This is championing inclusion as a professional behaviour, and achieving it through the legitimate route: the team lead, better informed, re-decides. Option A executes an instruction whose premise ("coping") you know to be false — deference is not a substitute for surfacing information the decider lacks. Option C fixes one ticket while leaving the team's priority model broken for the next such user, and makes your work-plan dishonest. Option D outsources advocacy to the person the system just failed, asking them to spend energy on process that you could spend in one conversation. The scored behaviours: recognising invisible impact, advocating through the right channel, and never mistaking silence for satisfaction.

**Question 9 (challenging) — Your fix caused the outage**

Monday, you applied what seemed a routine driver update to forty laptops in one directorate. Tuesday morning, eleven of them are blue-screening, the directorate's queue is filling, and a colleague speculates in the team channel that "it looks like yesterday's Windows patch" — which is wrong; the central patch went nowhere near these machines. Only you know the driver update is the common factor.

Which response is most effective, and which is least effective?

- A) Stay quiet and start quietly rolling back the driver on affected machines — the symptom will disappear and the patch theory will die naturally.
- B) Immediately state in the channel that your Monday driver update is the likely cause, share the affected-machine list, propose the rollback plan, alert the incident manager to the scale, and personally front the communication to the directorate.
- C) Let the patch theory stand for now — morale is better served by fixing than blaming — and correct the record in the post-incident review.
- D) Report that the cause is "under investigation" while you verify the driver theory for a day before naming it.

**Correct answer: most effective B; least effective A**

**Explanation:** Speed and honesty compound here — every hour the patch theory survives, colleagues investigate the wrong cause, the fix is delayed for eleven working users, and the eventual correction costs more trust. Option B collapses all of that in one message: naming your own change as the likely cause redirects the whole team's effort to the right target instantly; the machine list scopes the incident; the rollback plan converts confession into remediation; alerting the incident manager honours the process for a multi-user disruption; fronting the directorate communication is ownership where it is least comfortable and most valuable. Teams remember engineers who do this — it is the behaviour that makes blameless culture real. Option A is least effective and worth understanding precisely: the rollback might even work, but it deletes the evidence while colleagues chase a phantom cause, leaves the incident record false, and — if discovered — reads as concealment, converting an honest mistake into a trust breach. Mistakes are recoverable; cover-ups are not. Option C postpones truth to a review that may be weeks away, spending colleague-hours on a known-false theory in the name of morale. Option D hides behind verification: "likely cause, verifying now" is both honest and cautious — a day of silence is neither. The deep pattern: when you are the cause, you hold information the team needs, and withholding it — however gently — is the one genuinely unprofessional option.

**Question 10 (challenging) — Coaching versus the queue**

Your team lead asks you to take over ticket triage permanently because "the associates keep misrouting things and you're faster." You know the associates misroute because nobody has ever taught them the routing rules — and that absorbing triage will cost you two hours daily from incident work you are also measured on.

Which response is most effective?

- A) Accept — the team lead has assessed the options and routing accuracy matters most.
- B) Decline — triage is associate-level work and your incident metrics would suffer.
- C) Propose the developmental alternative: you take triage temporarily while running the associates through the routing rules — paired triage sessions, a one-page routing guide, spot-checks with feedback — with a review in three weeks when the associates take it back, better; explain that permanent absorption fixes today's symptom while guaranteeing the skills gap persists.
- D) Accept the task but delegate it back to the associates informally without telling the team lead.

**Correct answer: C**

**Explanation:** The team lead has proposed a permanent structural fix for what your diagnosis says is a training gap — and the two have very different futures. Permanent absorption (option A) makes routing accurate this week and fragile forever: the skills gap persists, your two daily hours are gone for good, and the team's triage capability now single-points through you — bad for the associates' development, your delivery, and the service's resilience. Option C counters with a plan that fixes the symptom and the cause: accuracy improves immediately (you are doing triage), capability transfers deliberately (paired sessions, a written guide — which is knowledge sharing in its most durable form), and the arrangement has an exit with a date and a success measure. Presenting it as a proposal respects the team lead's authority while giving them a better option than the one they could see — exactly how an engineer influences upward. Option B is a correct diagnosis wrapped in a refusal — it names the problem and helps with none of it. Option D creates a secret gap between the team lead's belief and reality, which is a worse misrouting than any ticket's. The scored pattern, and the coaching instinct your role builds toward: when asked to compensate permanently for a skills gap, offer instead to close it.

**Question 11 (challenging) — The plausible caller**

You take a walk-up call transferred from reception: a confident caller identifies themselves as a named senior manager from another directorate — the name checks out in the directory — working from home before an urgent submission, locked out, and needing a password reset "read out over the phone in the next five minutes." Your identity-verification procedure requires a callback to the registered number or a video check; the caller says their registered phone is the locked laptop's softphone and there's no time for video: "I'll take responsibility — check my name, you can see who I am."

Which response is most effective?

- A) Read out a temporary password after confirming personal details the caller offers — name, job title, and staff number all match the directory.
- B) Refuse verification shortcuts, but actively work the approved routes: attempt the registered callback anyway, offer the video check ("it takes two minutes"), and if both genuinely fail, escalate immediately to your team lead or the security desk for an authorised decision — keeping the caller informed of exactly what you are doing and why.
- C) Tell the caller to email the service desk from their personal email address to prove identity, then reset on receipt.
- D) Reset the password but send it to the manager's registered work email rather than reading it out.

**Correct answer: B**

**Explanation:** The scenario is a textbook social-engineering shape — urgency, authority, a plausible identity, and a tailored reason why each verification step is impossible — and it is equally what a genuinely locked-out manager sounds like. The skill being tested is holding the procedure without abandoning the person, because you cannot tell which case you have, and the procedure exists precisely for that uncertainty. Option B does this exactly: no verification shortcut (directory details prove research, not identity — names, titles and staff numbers are discoverable), but maximum energy inside the approved routes — the callback attempted rather than taken as impossible on the caller's word, the video check offered with its true cost ("two minutes" reframes the refusal as the fast path), and a rapid escalation to someone authorised to make exceptions, which converts "no" into "not me, but here is the person who can decide." A legitimate manager is delayed minutes; an attacker is stopped cold. Option A fails on the fundamental: knowledge of details is not proof of identity. Option C invents an unapproved route — personal email proves less than the phone call did. Option D feels safer but launders the same failure: if the account is already compromised, its mailbox may be too, and the reset was still made without verification. Note the caller's "I'll take responsibility" — authority cannot transfer your security obligations, a pattern this guide's scenarios keep returning because real pressure keeps returning to it. The scored behaviours: procedure under pressure, helpfulness inside the rules, and escalation as service.

### Preparation tips

- **Run every option through three lenses.** The user's outcome, the process's integrity, the relationship's health. Strong answers usually serve all three; the trap options sacrifice one entirely for another.
- **Locate your level.** At engineer level, the scored judgement is deliver and coach: fix what is yours, escalate with evidence what is not, and develop the associates rather than absorbing their work. Options that do the junior's job or the manager's are both mis-calibrated.
- **Watch for the second problem.** The best responses in strong scenarios fix the immediate issue and the system behind it — the unapproved tool and the unmet need, the misrouted tickets and the missing training. Train yourself to ask "what does this incident reveal?"
- **Rehearse honesty under adverse conditions.** The hardest scored behaviour is naming your own error fast. Recall a real mistake and script the two-sentence version: what happened, what you are doing about it. Having the words ready changes what you do under pressure.
- **Treat urgency claims as data to verify.** Deadlines, VIPs, and "no time for process" appear in scenario after scenario. The strong answers verify impact, keep the process, and make it fast — they never trade verification or control for speed on someone's say-so.
- **Debrief scenarios with colleagues.** Talk through "what would you do" cases at the desk — especially with your team's seniors. Their reasoning about edge cases is the norm group you are being scored against.

### Common pitfalls to avoid

- **The heroic absorption.** Staying silently late, taking over triage forever, personally covering every gap — self-sacrifice reads as strength and scores as a systems failure you chose to hide. Surface gaps; do not silently eat them.
- **The comfortable silence.** Not correcting the wrong diagnosis, not reporting the risky tool, not raising the misattribution — inaction is the most commonly chosen weak answer because it feels neutral. It never is; it is a decision to let harm continue.
- **Process as a shield or a casualty.** "Log a ticket like everyone else" and "just this once, skip verification" are the same error in opposite directions. The scoring key rewards process kept and made to work harder — expedited, escalated, energised.
- **Confession postponed.** Correcting the record "later, at the review" spends the team's effort on a falsehood in the meantime. Honesty is time-critical; its value halves every hour it waits.
- **Advocacy outsourced.** Telling the affected user to complain, the associate to figure it out, the manager to notice — routing your professional duty through the person with least power is a signature weak option. Carry it yourself, through the right channel.
- **Winning the moment.** Public corrections, meeting-room showdowns, reply-all evidence dumps — options that feel like justice score as relationship damage. Effectiveness is measured after the meeting ends.

## Conclusion

Well done — you have worked through a substantial set of practice materials covering all four assessment types you are likely to meet as an end user computing engineer: cognitive ability, numeric reasoning, verbal reasoning, and situational judgement.

Along the way, you have practised far more than test technique. You have clustered incidents by plausible cause and isolated faults with discriminating tests, checked asset registers and test-script gates for the breaches that matter, computed SLA clocks, first-time-fix rates, weighted averages and reorder points step by step, read change procedures, policy definitions and handover notes with an auditor's eye, and weighed judgement calls about mid-change complications, VIP interruptions, security pressure, your own mistakes, and the development of the associates who learn from you. Every one of those exercises maps directly to the skills your role names: incident management, problem management, asset and configuration management, change management, IT service reporting, technical specialism, testing, service focus, ownership, user focus, and the service management framework knowledge that ties them together.

A few encouragements as you move forward. First, assessment performance is a skill, and skills respond to practice. If particular question types caught you out, revisit their explanations in a week and attempt similar items again — the recurring methods are deliberately few: isolate the variable, sketch the fraction, read the rule to its end, verify before trusting urgency, escalate with evidence. Second, treat the preparation tips as professional development rather than exam technique. The habits these assessments reward — grouping by cause, checking the base of every percentage, distinguishing hypotheses from conclusions, naming your own errors fast — are exactly the habits that produce first-time resolution and the trust of your users and colleagues. Third, notice how much of this guide doubled as coaching material: every worked explanation is a model for the conversations you have with associates, because articulating why an answer is right is the same skill as teaching it.

Be confident in what you already bring. You diagnose under pressure at real desks, for real users, inside real processes, every working day. These assessments sample — in miniature and under a clock — the thinking you already do at full scale.

If you are preparing for a real assessment, find out the format, timing, and provider in advance, complete any official practice tests offered, and look after the basics: rest, a quiet environment, rough paper, and a steady pace. And whatever the outcome, keep investing in your development — take the trickier tickets, write the knowledge articles, coach generously, and keep turning incidents into lessons.

Good luck — you are better prepared than you were when you started reading. Keep going.
