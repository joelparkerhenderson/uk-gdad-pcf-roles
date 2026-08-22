# Apprentice DevOps Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an apprentice DevOps engineer in the UK Government Digital and Data profession. You might be preparing for an assessment as part of your apprenticeship, getting ready to apply for a junior post, or simply curious about how these tests work. Whatever brought you here, this document will help you practise, build confidence, and feel ready.

First, let's answer the obvious question: what is a psychometric assessment? It is a structured, standardised set of exercises that measures the thinking skills and workplace behaviours that predict success in a job. That might sound intimidating, but it really is not. There are no trick questions in a well-designed assessment, and there is nothing you cannot prepare for. The tests in this guide are job-specific, which means they use the kinds of things you genuinely see every day: build pipeline outputs, monitoring dashboards, service tickets, runbooks, security guidance, and messages from your team. If you have spent time shadowing your colleagues, watching deployments, and helping to investigate service faults under direction, you have already been building exactly the skills these assessments measure.

Why do these assessments matter for your role in particular? As an apprentice DevOps engineer, you spend a significant proportion of your time shadowing others, you are involved in implementation but not planning, and you are steadily building your knowledge. Employers want to know that you can spot when something looks wrong in a pipeline log, follow a runbook step by step without skipping anything, read an email from a senior engineer and take away the right instruction, and make sensible choices when something unexpected happens — like noticing a password pasted into a team chat. Those are precisely the four areas this guide covers: cognitive ability, numerical reasoning, verbal reasoning, and situational judgement.

The document is organised into four main assessment sections, and each one follows the same friendly pattern. First there is an overview of what the assessment measures and what the test format usually looks like, so nothing surprises you on the day. Then there is a mapping section that connects the assessment to the actual skills in your role description — such as service support, information security, and modern development standards — so you can see that this is not abstract puzzle-solving but practice for your real job. After that come practice questions, starting easy and getting gradually harder, each with a full worked explanation. Finally there are preparation tips and a list of common pitfalls to avoid.

Here is how to get the most from this guide. Take it one section at a time — there is no need to do everything in one sitting. Try each practice question honestly and write down your answer before you read the explanation. Do not worry at all if you get some wrong; the explanations are mini-lessons, and getting a question wrong then understanding why is one of the best ways to learn. When a worked explanation shows arithmetic, follow it with a pen and paper so the method sticks. And remember: at apprentice level, nobody expects you to know everything. Assessments for your level are about potential, carefulness, and willingness to learn — qualities you are already showing by working through this guide.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the thinking processes your role actually uses, wrapped in practical workplace scenarios rather than abstract puzzles. Instead of asking you to rotate shapes or complete number sequences with no context, it shows you the everyday materials of a DevOps apprenticeship — pipeline stage outputs, version numbers, monitoring alerts, checklists, and runbook steps — and asks you to reason quickly and accurately about them.

The typical format is an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your answers are compared against a norm group of people at a similar level, so you are being measured fairly against other apprentices and early-career engineers, not against principal engineers. Many modern platforms adapt the difficulty as you go, which means that if the questions seem to get harder, that is usually a sign you are doing well, not badly. Employers usually see a balance of speed and accuracy rather than a single score, so working carefully matters just as much as working quickly. You will almost always be offered a few ungraded practice questions before the real test starts, so you can get comfortable with the screens and buttons without any pressure.

For an apprentice DevOps engineer, cognitive assessment is especially relevant because so much of your learning happens through observation and careful checking. When you shadow a senior engineer during a deployment, you are watching for patterns: which steps always happen in which order, what a healthy log looks like, what a failing one looks like. When you help with the investigation of a service fault, completing defined activities under direction, you are doing structured error checking. A well-designed cognitive test simulates those demands in miniature — and practising them here will genuinely help you at work, not just in the test.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Programming and build (software engineering)** skill: having a basic knowledge of how services are built means learning to recognise the recurring shapes of healthy builds — the usual order of pipeline stages, consistent version numbering, and log lines that follow a standard format.
- **Logical deduction** maps to **Availability and capacity management** and **Information security**: when you explain availability processes or security controls, you are reasoning from rules to consequences — if the rule says every service must have an alert configured, and this service has no alert, something follows logically from that.
- **Error checking** maps to **Service support**: helping with the investigation and fixing of service faults, completing defined activities under direction, is fundamentally about comparing what you see against what should be there and spotting the difference.
- **Prioritisation** maps to your day-to-day reality of shadowing and supervised work: even at apprentice level you must decide sensible ordering — which task to do first when your mentor has given you more than one, and when to pause and ask.
- **Applied problem solving** maps to **Modern development standards** and **Prototyping**: understanding why standards matter, and why teams prototype and pair, requires you to think through cause and effect in the development process.

### Practice questions

**Question 1 (easy) — Pattern recognition in a pipeline**

You are shadowing a senior engineer, watching the team's build pipeline. Every successful run follows the same stage order: Checkout, Build, Unit tests, Package, Deploy to test. This morning you watch four runs and note the stage orders shown below. Which run does not follow the standard pattern?

- A) Run 1: Checkout, Build, Unit tests, Package, Deploy to test
- B) Run 2: Checkout, Build, Unit tests, Package, Deploy to test
- C) Run 3: Checkout, Unit tests, Build, Package, Deploy to test
- D) Run 4: Checkout, Build, Unit tests, Package, Deploy to test

**Correct answer: C**

**Explanation:** Compare each run against the standard order, stage by stage. Runs 1, 2 and 4 match exactly. Run 3 swaps the second and third stages: it tries to run unit tests before the build. Working through a comparison methodically — first stage, second stage, third stage — is much more reliable than glancing at the whole list and hoping the odd one jumps out. This is exactly the observational skill you build while shadowing: once you know what "normal" looks like for your team's pipeline, anything unusual becomes visible. In real life, a reordered pipeline usually means someone has changed the configuration, and noticing it early is genuinely valuable — even an apprentice pointing out "that run looked different" can save the team time.

**Question 2 (easy) — Spotting the odd one out in version numbers**

Your team names its releases using the pattern `service-name-v<major>.<minor>.<patch>`, for example `queue-worker-v2.4.1`. You are asked to check a list of release tags for anything that breaks the pattern:

1. `queue-worker-v2.4.1`
2. `queue-worker-v2.4.2`
3. `queue-worker-2.5.0`
4. `queue-worker-v2.5.1`

Which tag breaks the naming pattern?

- A) Tag 1
- B) Tag 2
- C) Tag 3
- D) Tag 4

**Correct answer: C**

**Explanation:** The pattern requires the letter `v` before the version numbers. Tag 3 reads `queue-worker-2.5.0` — the `v` is missing. Tags 1, 2 and 4 all follow the rule. The reliable technique is to check each tag against each part of the pattern in turn: service name, hyphen, `v`, then three numbers separated by dots. Small naming inconsistencies like this matter more than they might seem: automated tools often select releases by matching the pattern, so a tag without the `v` might be silently ignored by a deployment script. Careful checking of small details is one of the first ways an apprentice adds real value to a DevOps team, and it is a core part of understanding how services are built and released.

**Question 3 (easy) — Following a runbook rule**

A runbook you are following under direction says: "If the disk usage alert is above 80%, run the cleanup script. If the cleanup script does not bring usage below 80%, escalate to the on-call engineer." You run the cleanup script because the alert showed 85%. Afterwards, usage shows 82%. What should you do next, according to the runbook?

- A) Run the cleanup script again
- B) Escalate to the on-call engineer
- C) Wait an hour and check again
- D) Close the alert, because usage went down

**Correct answer: B**

**Explanation:** Read the rule as a chain of conditions. Usage was above 80%, so you correctly ran the cleanup script. The next rule says: if the script does not bring usage below 80%, escalate. Usage is now 82%, which is still above 80%, so the condition for escalating is met. The runbook does not say "run the script again" or "wait and see" — options A and C add steps that are not there, and option D ignores the threshold entirely: usage fell, but not far enough. In service support at your level, completing defined activities under direction means doing exactly what the agreed procedure says, and escalating when the procedure says to. Escalation is not failure — it is the runbook working as designed, and it is precisely what your seniors want you to do.

**Question 4 (easy) — Logical deduction about security controls**

Your organisation's security guidance states: "Every laptop used for development must have full-disk encryption enabled unless a written exception has been approved by the security team." A colleague mentions that their development laptop does not have full-disk encryption. Which one of the following must be true?

- A) Your colleague has broken the security rules.
- B) Your colleague has a written exception from the security team.
- C) Either your colleague has a written exception, or the rules have been broken.
- D) Your colleague's laptop cannot be used for development work.

**Correct answer: C**

**Explanation:** The rule is conditional with one permitted exception. From what you know, you cannot tell whether an exception exists — so you cannot conclude A (a breach) or B (an exception) on its own; each is only possible. Option D goes beyond anything the rule says. The only statement guaranteed to be true is C: one of the two situations must hold. This kind of careful deduction matters when you are learning to explain information security and the security controls that protect services: jumping to "you've broken the rules!" before checking the facts damages trust, while ignoring the situation entirely would be a miss. The right instinct — in the test and at work — is to recognise exactly what the information guarantees, and then, at work, to ask a friendly question or mention it to your mentor.

**Question 5 (moderate) — Error checking a deployment checklist**

Before each deployment to the test environment, your team completes a checklist: (1) all unit tests passing, (2) code reviewed by at least one other person, (3) change recorded in the change log, (4) test environment health check green. You are asked to check the evidence for today's deployment: the pipeline shows tests passing; the pull request shows two approvals; the change log's latest entry is dated last week and describes a different change; the health check dashboard is green. How many checklist items are satisfied?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: C**

**Explanation:** Check each item against its evidence, one at a time. Item 1: tests passing — satisfied. Item 2: at least one review — two approvals, satisfied. Item 3: change recorded in the change log — the latest entry is last week's and describes a different change, so today's change has not been recorded — not satisfied. Item 4: health check green — satisfied. Three items are satisfied. The trap in questions like this is to skim: the change log has an entry, and a hurried reader counts that as a tick without checking the date and description. Matching evidence to requirements precisely is the heart of error checking, and it mirrors real service support work: an out-of-date change log makes fault investigation much harder later, because the record no longer tells you what actually changed and when.

**Question 6 (moderate) — Pattern recognition in log timestamps**

You are watching a service's log with a senior engineer. A background job writes a "heartbeat" line every 5 minutes. You see heartbeats at 09:00, 09:05, 09:10, 09:20, 09:25. The senior engineer asks: "Anything odd?" What is the most accurate observation?

- A) Nothing is odd; heartbeats appear regularly.
- B) The expected 09:15 heartbeat is missing, suggesting the job paused or failed once.
- C) The job is running twice as fast as it should.
- D) The heartbeats stopped after 09:10.

**Correct answer: B**

**Explanation:** Lay out the expected pattern: every 5 minutes from 09:00 gives 09:00, 09:05, 09:10, 09:15, 09:20, 09:25. Comparing expected against actual, one entry is missing: 09:15. Option A misses the gap; option C would require heartbeats more often than every 5 minutes, which is not what the log shows; option D is contradicted by the entries at 09:20 and 09:25 — the job recovered. The precise observation is that a single expected event is missing. This "expected versus actual" habit is one of the most useful techniques in operations work: write down what should be there, then compare. A single missed heartbeat may be harmless, but noticing it — and saying so — is exactly the kind of contribution that shows you are building on your knowledge while shadowing.

**Question 7 (moderate) — Prioritisation under direction**

Your mentor is in a meeting for the next hour. Before leaving, they gave you three tasks: (1) finish writing up your notes from yesterday's shadowing session, needed for your apprenticeship portfolio review next week; (2) run the daily backup verification check, which the runbook says must be completed before midday — it is now 11:20 and the check takes about 15 minutes; (3) read the new coding standards document before Friday. While your mentor is away, a developer drops by and asks if you can "quickly look at" a failing test on their machine. What is the most sensible order for your next hour?

- A) Help the developer first, then the backup check, then notes, then reading
- B) Run the backup verification check first, then let the developer know your mentor will be back within the hour, then continue with notes or reading
- C) Finish your portfolio notes first because your review is important
- D) Read the standards document first because standards underpin everything

**Correct answer: B**

**Explanation:** Reason about deadlines and your level. The backup verification check has a hard deadline (before midday), is due in 40 minutes, and takes 15 — it must come first. The developer's request is not one of your defined activities, and at apprentice level you are involved in implementation under direction, not ad-hoc troubleshooting on your own; the courteous and correct move is to explain that your mentor is back soon, rather than attempting something outside your assigned work. Your notes (next week) and the reading (Friday) both have distant deadlines and can follow. Option A puts an unassigned, undirected task ahead of a same-day runbook deadline; options C and D ignore the midday deadline altogether. The pattern to remember: hard, near deadlines on assigned work come first; be helpful about everything else without abandoning your defined tasks.

**Question 8 (moderate) — Deduction from environment rules**

Your team has three environments: development, test, and live. The rules are: (i) every change must be deployed to test before live; (ii) only changes that have passed review may be deployed to test; (iii) apprentices may deploy to development at any time, but may deploy to test only when paired with a senior engineer. You have written a small script change that has not yet been reviewed. Which of the following are you allowed to do right now?

- A) Deploy it to test, as long as you pair with a senior engineer
- B) Deploy it to live, because it is only a small change
- C) Deploy it to development
- D) Nothing — you cannot deploy it anywhere until it is reviewed

**Correct answer: C**

**Explanation:** Test each option against the rules. A fails because rule (ii) blocks unreviewed changes from test — pairing solves the "apprentice" condition in rule (iii), but not the review condition. B fails twice over: rule (i) requires test before live, and the change is unreviewed. D is too strong: the rules restrict test and live, but rule (iii) explicitly allows apprentices to deploy to development at any time, and no rule requires review before development. So C is correct. Notice the technique: check every rule against every option, because an option can pass one rule and fail another. This mirrors how environment permissions genuinely work in government digital teams, and understanding why the gates exist — protecting test and live from unreviewed changes — is part of explaining the importance of modern development standards.

**Question 9 (moderate) — Applied problem solving: why did the build break?**

A build worked at 10:00. At 10:30 it failed with the error "package not found". Between 10:00 and 10:30, three things happened: (1) a colleague merged a change that added a new package to the project's dependency list; (2) the office wifi dropped for two minutes at 10:10; (3) you renamed your local copy of the project folder. The build runs on a shared build server, not on your laptop. What is the most likely cause to investigate first?

- A) The colleague's merged change adding the new package
- B) The wifi drop at 10:10
- C) Your renamed local folder
- D) The build server needs restarting

**Correct answer: A**

**Explanation:** Use two filters: what could cause this error, and what could affect this system. The error is "package not found", which points directly at dependencies — and the one dependency-related event is the colleague's change adding a new package (perhaps the package name is misspelt, or the package repository does not have it). The wifi drop affected the office, not necessarily the build server, and it ended long before 10:30. Your local folder rename cannot affect a shared build server at all. Option D is a guess with no supporting evidence — restarting things at random is not investigation. Working from the error message towards the most plausible recent change is the basic method of fault investigation, and it is exactly what "helping with the investigation and fixing of service faults" looks like in practice: gather what changed, match it against the symptom, and check the most likely cause first.

**Question 10 (hard) — Multi-step deduction about a monitoring rota**

Your team checks three dashboards every morning: Availability, Capacity, and Security. Each dashboard is checked by exactly one person per day. The rules are: (i) nobody may check the same dashboard two days in a row; (ii) yesterday, Amal checked Availability, Bea checked Capacity, and Chris checked Security. Today, Bea is on leave, so the three dashboards must be covered by Amal, Chris, and you. Amal has already picked up Capacity. Which dashboard must you check today?

- A) Availability
- B) Capacity
- C) Security
- D) Any of the three — the rules allow more than one arrangement

**Correct answer: C**

**Explanation:** Work through the constraints step by step. Amal takes Capacity — allowed under rule (i), because Amal had Availability yesterday, not Capacity. That leaves Availability and Security to be shared between Chris and you. Now apply rule (i) to Chris: Chris checked Security yesterday, so Chris cannot check Security today. Chris must therefore take Availability (allowed — Chris did not have it yesterday), which leaves exactly one dashboard for you: Security. You have no yesterday assignment to conflict with, so the arrangement is valid, and it is the only valid one — which also rules out option D. The technique to remember is patient elimination: fix the assignments you are told, apply each rule to narrow the remaining choices, and see what is forced. Rota and cover puzzles like this genuinely occur in availability and capacity management, where handovers and leave cover must respect several constraints at once, and being able to reason "Chris can't repeat Security, so I must be on Security" is exactly the kind of clear thinking that makes a shadowing apprentice a trusted pair of hands.

**Question 11 (hard) — Error checking across two artefacts**

The team wiki says: "The nightly batch job runs at 02:00 and takes about 45 minutes. If it is still running at 03:30, raise an incident." You are shown a monitoring extract for last night: job started 02:00; job still running at 03:10; job finished 03:25. A colleague says: "The wiki says we should have raised an incident." Is the colleague right?

- A) Yes — the job overran its usual 45 minutes, so an incident was needed.
- B) No — the incident rule triggers only if the job is still running at 03:30, and it finished at 03:25.
- C) Yes — any job running past 03:00 needs an incident.
- D) Cannot say — the wiki does not define "running".

**Correct answer: B**

**Explanation:** Separate the two statements in the wiki. "Takes about 45 minutes" is a description of normal behaviour, not a rule. The rule is precise: raise an incident if the job is still running at 03:30. Last night the job finished at 03:25 — five minutes before the trigger time — so the rule was never triggered, even though the job ran well over its usual 45 minutes. Option A confuses the description with the rule; option C invents a threshold that appears nowhere; option D manufactures ambiguity where the rule is clear enough. That said, in real life the best response would be B plus a friendly observation: "No incident needed, but it ran slow — worth mentioning at stand-up." Distinguishing descriptions from rules is a subtle but essential reading skill for service support, where runbooks mix background information with precise triggers, and acting on the wrong sentence causes either false alarms or missed escalations.

**Question 12 (hard) — Applied problem solving with a process change**

Your team currently deploys to the test environment once a week, on Thursdays. Deployments frequently fail because many changes are bundled together, and finding which change caused a failure takes hours. A senior engineer proposes deploying every day instead, with fewer changes per deployment. An apprentice colleague objects: "More deployments means more failures — we'd be failing every day instead of once a week!" Which statement best evaluates the objection?

- A) The objection is correct: more deployments always mean more total failures.
- B) The objection misses the point: smaller deployments make each failure easier to diagnose and fix, and fewer bundled changes make each deployment less likely to fail in the first place.
- C) The objection is correct because daily deployments leave no time for testing.
- D) Both approaches are identical in risk, so the change is pointless.

**Correct answer: B**

**Explanation:** Think about cause and effect. Failures in the current process are driven largely by bundling: many unrelated changes interact, and when something breaks, the search space is huge. Deploying daily shrinks each batch, which does two things: it reduces the chance that any single deployment fails (fewer interacting changes), and when one does fail, the cause is almost certainly in that day's small batch — so diagnosis takes minutes, not hours. The objection counts deployment events while ignoring failure probability per deployment and time-to-fix, which are what actually matter. Option C assumes testing is skipped, but the proposal changes frequency, not the pipeline's test stages. Option D ignores the reasoning entirely. This is the core logic behind modern development standards such as continuous integration and frequent small releases — and being able to explain *why* the standard helps, not just *that* it exists, is exactly the "explain the importance of modern development standards" skill at your level.

### Preparation tips

- **Practise with real artefacts.** Spend ten minutes a day reading your team's pipeline output, monitoring dashboards, and runbooks — even ones for services you do not work on. The more familiar "normal" looks, the faster you spot "abnormal", which is exactly what cognitive tests measure.
- **Use the expected-versus-actual habit.** For any checking question, write down (or clearly picture) what *should* be there before you look at what *is* there. Comparing two explicit lists is far more reliable than scanning and hoping.
- **Read rules like a computer would.** Runbook and policy questions hinge on exact conditions: "above 80%" is not the same as "80% or above", and "still running at 03:30" is not the same as "ran longer than usual". Slow down on the condition words.
- **Do a little, often.** Three short practice sessions a week beat one long cram. Timed practice matters too: once you are comfortable with the question styles, set a timer for around 90 seconds per question so the pace of a real test feels familiar.
- **Ask your mentor to think aloud.** When you shadow a fault investigation, ask your senior colleague to narrate their reasoning. Hearing "the error says X, so I'll check Y first" trains exactly the deduction pattern these tests reward — and it is a completely natural apprenticeship question to ask.
- **Look after the basics.** Sleep well the night before, set up a quiet space, close chat notifications, and use the ungraded practice questions at the start of the real test to settle your nerves.

### Common pitfalls to avoid

- **Rushing the reading.** The most common error at every level is answering the question you expected rather than the question asked. Read the scenario once for the story, then again for the exact rule or number that matters.
- **Adding knowledge the question did not give you.** If a scenario describes a fictional team's rules, answer from those rules — not from how your own team happens to do it. Test questions are self-contained.
- **Jumping to conclusions.** As Question 4 showed, "must be true" is a high bar. If the information allows two possibilities, an answer that names only one of them is wrong, however plausible it feels.
- **Treating "escalate" or "ask" as weak answers.** At apprentice level, options that involve following the procedure, pausing, or asking for direction are often the *strongest* answers, because they reflect how your role is actually meant to work.
- **Panicking after a hard question.** Adaptive tests get harder when you do well. One baffling question does not mean you are failing — answer your best, let it go, and give the next question a fresh start.
- **Leaving questions blank.** Unless the instructions say wrong answers are penalised, an educated guess after eliminating one or two options is always better than no answer.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how confidently and accurately you work with the numbers that appear in your job. It is not a maths exam: you will not need algebra, geometry, or anything you have not met since school. Instead, you will read small tables and charts and answer questions using percentages, averages, ratios, rates, and simple trend-spotting — all wrapped in DevOps scenarios such as disk usage, build times, uptime figures, and ticket counts.

The typical format is an online, timed test lasting 20 to 30 minutes with somewhere between 15 and 25 questions. Each question usually shows a small data set — a table of ticket volumes, a chart of build durations — and asks one specific thing about it. A basic on-screen calculator is often provided, and rough paper is almost always allowed; check the instructions for your specific test. As with the cognitive assessment, scoring is objective and compared against a norm group at your level, and speed and accuracy are balanced, so a careful, methodical approach scores well.

Employers use numeric reasoning tests for DevOps roles because operations work is full of numbers that matter. Availability is expressed as a percentage; capacity is judged by usage against thresholds; build health is tracked by pass rates and durations; service support is managed through ticket counts and response times. At apprentice level, nobody expects you to design capacity plans — but you are expected to read a dashboard and understand what the numbers say, notice when a figure is drifting in the wrong direction, and explain availability and capacity management processes in plain terms. Practising the arithmetic here builds exactly that comfort. Every explanation below shows the working step by step, so even if numbers make you nervous, you can follow the method and reuse it.

### How this assessment maps to your role

The numeric skills in the test map directly to the named skills in your role summary:

- **Percentages** map to **Availability and capacity management**: explaining these processes means understanding uptime percentages ("the service was available 99.5% of the time") and usage thresholds ("the disk alert fires at 80%").
- **Averages and rates** map to **Programming and build (software engineering)**: build durations, test pass rates, and deployment frequency are the everyday numbers of understanding how services are built and shipped.
- **Reading tables and charts** maps to **Service support**: helping to investigate service faults often starts with a monitoring graph or a ticket report, and the first skill is simply extracting the right number from the right row.
- **Ratios and proportions** map to **Information security** and **Modern development standards**: security reports talk about proportions of patched machines; standards discussions talk about the share of code covered by tests.
- **Trend spotting** maps to your role-level duty to **build on your knowledge**: noticing that a number is creeping up week after week — and saying so — is one of the simplest, most valuable habits an apprentice can develop.

### Practice questions

**Question 1 (easy) — Reading a ticket table**

Your team's service desk report shows tickets received this week: Monday 12, Tuesday 9, Wednesday 15, Thursday 11, Friday 8. How many tickets were received in total this week?

- A) 50
- B) 55
- C) 57
- D) 60

**Correct answer: B**

**Explanation:** Add the daily figures one step at a time: 12 + 9 = 21. Then 21 + 15 = 36. Then 36 + 11 = 47. Then 47 + 8 = 55. The total is 55 tickets. A tip for addition under time pressure: add in pairs that make round numbers where you can (12 + 8 = 20, 9 + 11 = 20, then 20 + 20 + 15 = 55) — regrouping like this is faster and easier to check. Reading a table accurately and totalling it is the foundation of every service support report you will meet, and getting the easy questions right quickly banks time for the harder ones later in the test.

**Question 2 (easy) — Disk usage percentage**

A test server has a 500 GB disk. The monitoring dashboard shows 350 GB used. What percentage of the disk is used?

- A) 60%
- B) 65%
- C) 70%
- D) 75%

**Correct answer: C**

**Explanation:** Percentage used = used ÷ total × 100. Step 1: 350 ÷ 500 = 0.7. Step 2: 0.7 × 100 = 70%. A quicker mental route: 10% of 500 GB is 50 GB, and 350 ÷ 50 = 7, so 350 GB is 7 lots of 10%, which is 70%. This is exactly the calculation behind capacity alerts: if your team's alert threshold is 80%, you can now say the server is 10 percentage points below the alert level, which on a 500 GB disk is 50 GB of headroom. Being able to translate between gigabytes and percentages in both directions is a small skill that makes capacity conversations much easier to follow when you are shadowing.

**Question 3 (easy) — Average build time**

You are asked to note down how long the last five builds took: 6 minutes, 8 minutes, 5 minutes, 9 minutes, 7 minutes. What is the average (mean) build time?

- A) 6 minutes
- B) 6.5 minutes
- C) 7 minutes
- D) 7.5 minutes

**Correct answer: C**

**Explanation:** The mean is the total divided by the count. Step 1: total = 6 + 8 + 5 + 9 + 7. Add in order: 6 + 8 = 14; 14 + 5 = 19; 19 + 9 = 28; 28 + 7 = 35 minutes. Step 2: divide by the number of builds: 35 ÷ 5 = 7 minutes. A sense-check habit worth building: the mean must sit between the smallest value (5) and the largest (9), so answers like 4 or 10 could be rejected instantly. Build-time averages matter in real life because a rising average is often the first sign that a pipeline needs attention — and "the average build has gone from 7 to 11 minutes this month" is a genuinely useful observation an apprentice can bring to stand-up.

**Question 4 (easy) — Percentage of tests passing**

A test run executes 200 automated tests, and 8 of them fail. What percentage of the tests passed?

- A) 92%
- B) 94%
- C) 96%
- D) 98%

**Correct answer: C**

**Explanation:** First find how many passed: 200 − 8 = 192. Then calculate the pass rate: 192 ÷ 200 × 100. Step by step: 192 ÷ 200 = 0.96, and 0.96 × 100 = 96%. An alternative route is to work out the failure rate first: 8 ÷ 200 = 0.04 = 4%, so the pass rate is 100% − 4% = 96%. The failure-rate route is often quicker when the failing number is small. Watch for the classic trap: option A (92%) is what you get if you subtract 8 from 100 directly — mixing up a count of 8 tests with 8 per cent. Keeping counts and percentages clearly separate in your head is a small discipline that prevents many real-world misreadings of test dashboards.

**Question 5 (moderate) — Uptime percentage**

A service is expected to be available 24 hours a day. Last month (30 days), it was unavailable for a total of 6 hours. What was its availability percentage for the month, to one decimal place?

- A) 99.2%
- B) 99.4%
- C) 99.6%
- D) 99.8%

**Correct answer: A**

**Explanation:** Step 1: total hours in the month = 30 × 24 = 720 hours. Step 2: available hours = 720 − 6 = 714. Step 3: availability = 714 ÷ 720 × 100. Compute 714 ÷ 720 = 0.99166..., and multiplying by 100 gives 99.166...%, which rounds to 99.2%. A neat alternative: unavailability = 6 ÷ 720 = 0.008333 = 0.83%, and 100% − 0.83% = 99.17% ≈ 99.2%. Availability percentages like "99.2%" are the everyday language of availability management, and it is genuinely useful to know how they are produced: when you can explain that each 0.1% of a 30-day month is about 43 minutes, phrases like "three nines" stop being jargon and start being quantities you can picture.

**Question 6 (moderate) — Ratio of environments**

Your team runs 24 virtual machines in total, split between the test environment and the development environment in the ratio 5:3 (test:development). How many virtual machines are in the test environment?

- A) 9
- B) 12
- C) 15
- D) 18

**Correct answer: C**

**Explanation:** A ratio of 5:3 means the machines are divided into 5 + 3 = 8 equal parts. Step 1: size of one part = 24 ÷ 8 = 3 machines. Step 2: test environment = 5 parts = 5 × 3 = 15 machines. (Check: development = 3 × 3 = 9, and 15 + 9 = 24 ✓.) The reliable method for any ratio question is always the same: add the ratio numbers to find the total parts, divide the real total by that to find one part, then multiply. Ratios appear throughout infrastructure work — machines per environment, capacity split between services, licence allocations — and the check step (do the pieces add back to the total?) is a habit that catches slips before anyone else sees them.

**Question 7 (moderate) — Change in ticket volume**

The number of service faults reported each week has changed over four weeks: Week 1: 40, Week 2: 44, Week 3: 50, Week 4: 60. By what percentage did weekly faults increase from Week 1 to Week 4?

- A) 20%
- B) 33%
- C) 50%
- D) 60%

**Correct answer: C**

**Explanation:** Percentage change = (new − old) ÷ old × 100. Step 1: the increase = 60 − 40 = 20 faults. Step 2: divide by the *original* value: 20 ÷ 40 = 0.5. Step 3: 0.5 × 100 = 50%. The most common error is dividing by the new value (20 ÷ 60 = 33%, option B) — remember that percentage change is always measured against where you started. It is also worth noticing the trend shape: the weekly increases are 4, 6, and 10 — the rises themselves are growing, which suggests something is getting steadily worse rather than a one-off blip. Spotting and clearly stating that kind of trend ("faults are up 50% in a month, and accelerating") is precisely how monitoring data turns into a useful early warning.

**Question 8 (moderate) — Reading a two-way table**

A monthly report shows fault tickets by service and by priority:

| Service | High priority | Low priority |
|---|---|---|
| Payments API | 6 | 18 |
| Booking site | 4 | 12 |
| Reporting tool | 2 | 8 |

What fraction of all tickets were high priority?

- A) 1/5
- B) 6/25
- C) 1/4
- D) 3/10

**Correct answer: B**

**Explanation:** Step 1: total high-priority tickets = 6 + 4 + 2 = 12. Step 2: total low-priority tickets = 18 + 12 + 8 = 38 (add in stages: 18 + 12 = 30, then 30 + 8 = 38). Step 3: total tickets = 12 + 38 = 50. Step 4: fraction high priority = 12/50. Simplify by dividing top and bottom by 2: 12/50 = 6/25. Now compare with the options carefully, because two of them are deliberately close: 6/25 = 0.24, while 1/4 = 0.25. The exact answer is 6/25 — option B. When options sit this close together, do not round or eyeball; convert each candidate to a decimal and match it against your calculation. Also note the base you divided by: the question asked for high-priority tickets out of *all* tickets (50), not out of low-priority tickets or out of one service's tickets. Asking yourself "out of what?" before dividing is the single best habit for two-way tables — the same tables you will meet in real monthly service reports.

**Question 9 (moderate) — Time and rates for a backup job**

A backup job copies data at a steady 4 GB per minute. Tonight it must back up 288 GB. The backup window closes 90 minutes after the job starts. Will the job finish inside the window, and with how much time to spare (or over)?

- A) Yes, with 18 minutes to spare
- B) Yes, with 12 minutes to spare
- C) No, it will overrun by 6 minutes
- D) No, it will overrun by 18 minutes

**Correct answer: A**

**Explanation:** Time = amount ÷ rate. Step 1: 288 ÷ 4 = 72 minutes to complete the backup. Step 2: compare with the window: 90 − 72 = 18 minutes to spare, so the job fits comfortably. To do 288 ÷ 4 quickly, halve twice: 288 ÷ 2 = 144, and 144 ÷ 2 = 72. Rate calculations like this sit underneath many operational questions — how long a data migration will take, whether a job fits its overnight window, when a disk will fill at the current growth rate. Notice too the value of stating the answer with its margin ("finishes with 18 minutes spare") rather than a bare yes: margins tell your team how much risk is left if the job runs a little slow, which is the beginning of real capacity thinking.

**Question 10 (hard) — Percentage threshold and headroom**

A database server has 640 GB of storage, currently 60% full. Data grows by 16 GB per week. The capacity alert fires when usage reaches 85%. Assuming steady growth, in how many weeks will the alert fire?

- A) 8 weeks
- B) 10 weeks
- C) 12 weeks
- D) 16 weeks

**Correct answer: B**

**Explanation:** Work in gigabytes throughout. Step 1: current usage = 60% of 640 = 0.6 × 640 = 384 GB. Step 2: alert level = 85% of 640 = 0.85 × 640 = 544 GB. (To compute 0.85 × 640: 0.8 × 640 = 512, and 0.05 × 640 = 32, so 512 + 32 = 544.) Step 3: headroom before the alert = 544 − 384 = 160 GB. Step 4: weeks until alert = 160 ÷ 16 = 10 weeks. The multi-step structure — convert percentages to real amounts, find the gap, divide by the rate — is the standard pattern for "when will we run out?" questions, and it is genuine availability and capacity management in miniature. In real life you would add one more thought: 10 weeks is the forecast *if growth stays steady*, so the number should prompt a plan, not complacency.

**Question 11 (hard) — Comparing failure rates fairly**

Two pipelines ran last month. Pipeline A ran 250 times and failed 20 times. Pipeline B ran 80 times and failed 10 times. A colleague says: "Pipeline A is worse — it failed twice as often." Which statement is accurate?

- A) The colleague is right: 20 failures is worse than 10.
- B) Pipeline A's failure rate is 8%, Pipeline B's is 12.5%, so Pipeline B fails proportionally more often.
- C) Both pipelines have the same failure rate.
- D) The failure rates cannot be compared without knowing the build durations.

**Correct answer: B**

**Explanation:** Raw counts mislead when the totals differ, so convert both to rates. Pipeline A: 20 ÷ 250 = 0.08 = 8%. (Check: 10% of 250 is 25, so 20 failures must be a little under 10% ✓.) Pipeline B: 10 ÷ 80 = 0.125 = 12.5%. (Check: 10% of 80 is 8, so 10 failures is above 10% ✓.) Pipeline B fails on one run in eight; Pipeline A on one in twelve and a half. The colleague compared counts, not rates — the most common statistical slip in operational conversations. Option D is a distraction: durations affect how *painful* failures are, not how *frequent* they are. Whenever you compare two services, teams, or time periods with different volumes, divide before you compare. Saying, kindly, "shall we check the rates?" is an excellent apprentice contribution to any dashboard discussion.

**Question 12 (hard) — Multi-step cost and capacity question**

Your team's cloud test environment costs £0.50 per hour per virtual machine. The environment runs 10 machines, 24 hours a day. A senior engineer proposes shutting the environment down outside working hours, running it only 12 hours a day on weekdays (5 days a week) and not at all at weekends. Over a 4-week period (28 days), how much money would the proposal save?

- A) £1,680
- B) £2,160
- C) £2,760
- D) £3,360

**Correct answer: B**

**Explanation:** Calculate each scenario's cost over 28 days, then subtract. Current: hours = 28 days × 24 = 672 hours per machine; cost = 672 hours × 10 machines × £0.50 = £3,360 (672 × 10 = 6,720 machine-hours; halve it for the 50p rate: £3,360). Proposed: running days = 5 weekdays × 4 weeks = 20 days; hours = 20 × 12 = 240 hours per machine; cost = 240 × 10 × £0.50 = £1,200 (2,400 machine-hours, halved = £1,200). Saving = £3,360 − £1,200 = £2,160. Verify by a second, independent route: hours saved per machine = 672 − 240 = 432; saving = 432 × 10 × £0.50 = £2,160 ✓. Two different routes agreeing is the gold standard of verification for multi-step arithmetic, and it is worth the extra thirty seconds on any question involving money. Cost-per-hour arithmetic exactly like this underpins real cloud capacity decisions, and even as an apprentice you may well be asked to gather the numbers behind a proposal like this one — being able to lay out the working clearly is as valuable as getting the total right.

### Preparation tips

- **Rebuild comfort with the core four.** Percentages, averages, ratios, and rates cover almost every question. Practise each until the *method* is automatic: percentage = part ÷ whole × 100; mean = total ÷ count; ratio = find one part first; rate questions = amount ÷ rate = time.
- **Always divide by the original for percentage change.** Say it to yourself before every change question. It is the single most-tested trap.
- **Use the answer options.** Before calculating, glance at the spread of options. If they are far apart, estimation may be enough; if two are close together (like 6/25 and 1/4), you know precision is required.
- **Sense-check every answer.** The mean sits between the smallest and largest value; a percentage of a quantity is smaller than the quantity; parts must add back to the whole. Ten seconds of checking catches most slips.
- **Practise with your team's real dashboards.** Ask your mentor to show you the availability and capacity graphs, and try computing the numbers yourself: what is this month's uptime percentage? How full will that disk be in six weeks? This doubles as excellent apprenticeship evidence.
- **Get comfortable with the on-screen calculator** before the day, if one is provided — knowing where the buttons are is worth a question or two of time.

### Common pitfalls to avoid

- **Confusing counts with percentages.** "8 tests failed" and "8% of tests failed" are different claims. Label your numbers as you work.
- **Comparing raw counts across different totals.** As Question 11 showed, always convert to rates before saying one thing fails "more often" than another.
- **Dividing by the wrong base.** Percentage change uses the original value; proportions use the overall total, not a subtotal. Ask "out of what?" every time.
- **Rounding too early.** Keep full precision until the final step, then round. Rounding midway is how 99.17% quietly becomes 99.0% and the wrong option gets picked.
- **Misreading tables.** Check row and column headers twice — the most common table error is reading the right number from the wrong row.
- **Spending too long on one hard question.** Every question is usually worth the same. If a multi-step calculation is going nowhere after two minutes, make your best elimination-based guess, flag it if the platform allows, and move on.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, understand, and draw conclusions from written material — the kind you genuinely meet in a DevOps apprenticeship. Rather than literary passages, you will read short extracts from runbooks, security guidance, team emails, incident reports, standards documents, and service descriptions, and then answer questions about what the text actually says.

The most common format presents a passage followed by statements, and for each statement you choose **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage gives too little information either way). Other question styles include picking the best summary of a passage, identifying what a word or instruction refers to, and judging which sentence communicates most clearly. Tests typically run 15 to 25 minutes with 20 to 30 short questions, and — like the other assessments — are scored objectively against a norm group at your level.

The golden rule of verbal reasoning is: **answer only from the passage.** You may know from work that a statement is probably true in real life, but if the passage does not say it, the answer is "cannot say". This feels strange at first and becomes natural with practice.

Employers use verbal reasoning tests for DevOps roles because so much of the job arrives as text. At apprentice level you follow written runbooks step by step, read security guidance you are expected to explain back, receive instructions by email and chat, and write up notes that others rely on. Misreading a single sentence — doing step 4 before step 3, or treating "should" as "must" — can cause real problems in a live-adjacent environment. Careful reading is a safety skill in this profession, and this section will strengthen yours.

### How this assessment maps to your role

The verbal skills in the test map directly to the named skills in your role summary:

- **Comprehension of instructions** maps to **Service support**: completing defined activities under direction depends entirely on reading procedures precisely — the order of steps, the conditions attached to them, and who must be told what.
- **True/false/cannot-say discipline** maps to **Information security**: explaining security controls accurately means saying exactly what the guidance says, neither more nor less; over-claiming ("the policy bans all USB drives") is as wrong as under-claiming.
- **Inference** maps to **Programming and build (software engineering)** and **Availability and capacity management**: understanding how services are built and run often means connecting statements — if the release notes say a service now depends on a new component, you can infer that component must be deployed first.
- **Clear-writing judgement** maps to **Prototyping** and working in an open, collaborative environment: pair working and open teams run on clear messages; recognising which sentence a reader will understand fastest is a skill you will use in every note and handover you write.
- **Reading for tone and audience** maps to your day-to-day duty to **build on your knowledge** while shadowing: much of what you learn arrives as written guidance, and getting the right meaning first time accelerates everything else.

### Practice questions

**Question 1 (easy) — True/false/cannot say from a runbook extract**

Passage: "The nightly report job runs at 01:00 every day, including weekends. If the job fails, it retries automatically once after 15 minutes. If the retry also fails, the on-call engineer receives an alert. The job's output file is stored for 90 days."

Statement: "The nightly report job runs on Saturdays."

- A) True
- B) False
- C) Cannot say
- D) True only in summer

**Correct answer: A**

**Explanation:** The passage says the job runs "every day, including weekends". Saturday is part of the weekend, so the statement is directly supported: True. Notice how the answer comes from matching the statement against the exact words of the passage — "including weekends" was written precisely to remove doubt. Option D invents a condition that appears nowhere. Easy questions like this are the ones to answer quickly and confidently, banking time for harder ones. The workplace habit being trained is looking for the sentence that settles the question rather than relying on general impressions — the same habit that stops you assuming a job "probably doesn't run at weekends" when the runbook says otherwise.

**Question 2 (easy) — What does the instruction require?**

Passage (from a security notice): "All staff must complete the annual security awareness training by 31 March. Staff who joined after 1 January should complete the training within eight weeks of their start date instead. Line managers must confirm completion for their team members."

You joined the organisation on 10 February this year. According to the notice, what applies to you?

- A) You must complete the training by 31 March.
- B) You should complete the training within eight weeks of 10 February.
- C) You are exempt from the training this year.
- D) Your line manager completes the training on your behalf.

**Correct answer: B**

**Explanation:** The notice sets a general rule (by 31 March) and then an exception for staff who joined after 1 January — and 10 February is after 1 January, so the exception applies to you: eight weeks from your start date. Option A applies the general rule while ignoring the exception that displaces it. Option C invents an exemption the text never gives. Option D misreads the manager's duty — they *confirm* completion, they do not complete the training for you. Reading rules with exceptions is a core skill for explaining security controls: the overall pattern is "general rule, exception, who checks", and identifying which clause applies to which person is exactly what you will do when colleagues ask you what the guidance means.

**Question 3 (easy) — Best summary of an email**

Email from a senior engineer: "Hi — quick heads-up. We're freezing changes to the test environment from Thursday 5pm until Monday 9am because the performance testing team needs a stable environment over the weekend. Anything already deployed can stay. If something urgent comes up, talk to me before touching anything. Thanks!"

Which is the best one-sentence summary?

- A) The test environment is being switched off over the weekend.
- B) No new changes to the test environment between Thursday 5pm and Monday 9am, except urgent ones agreed with the sender first.
- C) All deployments must be removed from the test environment by Thursday.
- D) The performance testing team is taking ownership of the test environment permanently.

**Correct answer: B**

**Explanation:** Check each candidate against the email. A is wrong: the environment stays running (the testers need it stable, not off). C is wrong: "anything already deployed can stay" says the opposite. D is wrong: the arrangement is for one weekend, not permanent. B captures all three key elements — the freeze window, its scope (new changes), and the exception route (talk to the sender first). A good summary keeps every load-bearing fact and drops only decoration. Summarising accurately matters more than it sounds: apprentices often relay messages between people and write up notes, and a summary that turns "freeze with exceptions" into "environment off" would send colleagues down entirely wrong paths.

**Question 4 (easy) — Cannot-say discipline**

Passage: "Version 2.9 of the deployment tool introduces role-based access control. Administrators can now restrict who may deploy to each environment. The release notes recommend enabling this feature for all production environments."

Statement: "Version 2.9 is the most widely used version of the deployment tool."

- A) True
- B) False
- C) Cannot say
- D) True, because new versions are always adopted quickly

**Correct answer: C**

**Explanation:** The passage describes what version 2.9 *introduces* and what the release notes *recommend*. It says nothing about how many people use any version. The statement might be true in the real world or it might not — but the passage gives no evidence either way, so the disciplined answer is "cannot say". Option D shows exactly the reasoning the test is designed to catch: importing a plausible-sounding general belief ("new versions are adopted quickly") that the text never states. Holding the line on "cannot say" is the single most important verbal reasoning skill, and it has a direct workplace parallel: when someone asks you what the security guidance says, the trustworthy answer distinguishes crisply between what the document states and what you are guessing.

**Question 5 (moderate) — Following referents in a procedure**

Passage (from a maintenance procedure): "First, stop the message consumer service. Next, clear the queue using the purge script. The script writes a log to the shared drive; check it for errors before proceeding. If it contains errors, restart the consumer and raise a ticket. Otherwise, apply the configuration update and restart the consumer."

You have run the purge script and its log shows no errors. According to the procedure, what do you do next?

- A) Raise a ticket
- B) Restart the consumer immediately
- C) Apply the configuration update, then restart the consumer
- D) Stop the message consumer service

**Correct answer: C**

**Explanation:** Track the branch. The procedure splits after the log check: errors → restart consumer and raise a ticket; no errors ("otherwise") → apply the configuration update and restart the consumer. Your log shows no errors, so you take the "otherwise" branch: update first, then restart. Option B is the subtle trap — restarting is part of both branches, but in your branch it comes *after* the update; restarting immediately would apply the old configuration and defeat the whole procedure. Option D repeats a step already done, and A belongs to the other branch. Procedures are full of branch words — "if", "otherwise", "unless" — and words like "it" whose meaning you must track ("it" = the log). Reading them as precisely as a computer would is exactly what "helping fix service faults, completing defined activities under direction" requires.

**Question 6 (moderate) — Inference from release notes**

Passage: "From release 4.2, the booking service requires the new authentication component. Environments that have not installed the authentication component must remain on release 4.1. Release 4.1 will stop receiving security fixes at the end of December."

Which conclusion follows from the passage?

- A) Every environment must install the authentication component before the end of December.
- B) An environment still without the authentication component in January will be running a release that no longer receives security fixes.
- C) Release 4.2 contains no security fixes.
- D) The authentication component is difficult to install.

**Correct answer: B**

**Explanation:** Chain the statements. No authentication component → stuck on 4.1 (sentence two). After December, 4.1 gets no security fixes (sentence three). Therefore an environment without the component in January is on a release without security fixes — exactly option B. Option A goes further than the text: the passage describes consequences, not an obligation ("must install by December" is never stated — an organisation could, unwisely, accept the risk). Option C confuses "4.1 stops receiving fixes" with a claim about 4.2. Option D has no support at all. This is inference done properly: connecting stated facts into their guaranteed consequence, without upgrading consequences into commands. Exactly this reading skill lets you explain to a teammate *why* the team is prioritising the component install — a small but real contribution to information security.

**Question 7 (moderate) — True/false/cannot say on a standards extract**

Passage (from a coding standards document): "All scripts committed to the shared repository must include a header comment stating the script's purpose and owner. Scripts without a header will be rejected by the automated check. Personal experiments kept in your own workspace are out of scope for this standard."

Statement: "A script in your own workspace without a header comment breaches the standard."

- A) True
- B) False
- C) Cannot say
- D) True, but only for long scripts

**Correct answer: B**

**Explanation:** The final sentence explicitly places personal workspace experiments *out of scope*: the standard does not apply to them. A statement claiming such a script "breaches the standard" is therefore contradicted by the passage — the answer is False, not "cannot say". This question tests the difference between the three verdicts: "cannot say" is for missing information, while False is for statements the passage actively rules out — and here the passage does rule it out by defining its own scope. Scope sentences ("this applies to X; Y is out of scope") are everywhere in standards and security documents, and applying a rule outside its stated scope is as much a misreading as ignoring the rule. Knowing where a standard stops is part of explaining modern development standards accurately.

**Question 8 (moderate) — Clear-writing judgement**

You are writing a handover note about a task you finished. Which sentence communicates most clearly to the next person?

- A) "The thing from before was sorted out after the usual problems, so it should probably be fine now."
- B) "Utilisation of the remediation script effectuated resolution of the aforementioned anomaly."
- C) "I fixed the failed backup on server TST-04 by re-running the backup script at 14:30; it completed successfully and I checked the log."
- D) "Backup issues were experienced but actions were taken and outcomes were achieved."

**Correct answer: C**

**Explanation:** Judge each sentence by what a reader could *do* with it. A is vague on every axis — which thing, which problems, how confident? B dresses a simple event in inflated vocabulary that slows every reader down. D uses the passive voice to remove all specifics: which issues, which actions, which outcomes? C names the problem (failed backup), the location (TST-04), the action (re-ran the script), the time (14:30), the result (completed), and the verification (checked the log) — everything the next person needs, in plain words. The pattern for good operational writing is: specific noun, specific action, specific result, evidence. This matters daily in an open, collaborative team: your notes are how your pair, your mentor, and the next shift know what actually happened.

**Question 9 (moderate) — Understanding a policy's conditions**

Passage (from an access policy): "Access to the live environment is granted only to named engineers who have completed the operations induction. Apprentices may view live dashboards but may not hold live access credentials. Access reviews take place quarterly, and unused accounts are disabled after 60 days of inactivity."

Statement: "An apprentice who completes the operations induction may hold live access credentials."

- A) True
- B) False
- C) Cannot say
- D) True after the next quarterly review

**Correct answer: B**

**Explanation:** Two rules interact here. The first sentence sets a necessary condition for live access (named engineer + induction). The second sentence adds a specific prohibition: apprentices "may not hold live access credentials" — with no exception mentioned for those who complete the induction. A specific prohibition is not cancelled by meeting a general condition, so the statement contradicts the policy: False. Option D invents a mechanism (the quarterly review as a promotion route) that the passage never describes — reviews check existing access, nothing more. When two clauses could seem to conflict, the precise reading asks: does the general rule contain an exception for this group, or does the specific rule stand? Here the specific rule stands. Reading access policies this carefully is foundational information security practice — and it also tells you, usefully, exactly what your own permissions should and should not be.

**Question 10 (hard) — Inference across an incident report**

Passage (from an incident report): "At 10:14 the booking service began returning errors. The on-call engineer identified that the database server's disk had filled. Log files, which are normally rotated nightly, had not been rotated for six days because the rotation job's schedule was accidentally disabled during last week's server migration. Space was freed at 10:52 and the service recovered by 10:58. The rotation job has been re-enabled, and a disk-usage alert has been added."

Which statement is best supported by the report?

- A) The server migration caused the disk to fill immediately.
- B) If the rotation job had been running normally, the disk would probably not have filled.
- C) The on-call engineer disabled the rotation job.
- D) The booking service was unavailable for six days.

**Correct answer: B**

**Explanation:** Trace the causal chain the report describes: migration → rotation job accidentally disabled → six days of unrotated logs → disk full → errors. The report presents the missing rotation as the reason the disk filled, so it supports the counterfactual in B — with rotation running, the accumulation that filled the disk would probably not have happened ("probably" is appropriately careful). A distorts the timeline: the migration set the cause in motion, but the disk filled six days later, not immediately. C misattributes the mistake — the schedule was disabled "during the migration", and the report never says by whom; blaming the on-call engineer is unsupported. D confuses the six days of missed rotation with the outage, which lasted 44 minutes (10:14 to 10:58). Incident reports reward exactly this careful reading of cause, agent, and timeline — and as an apprentice you will read many of them, because they are among the best learning documents operations teams produce.

**Question 11 (hard) — Weighing "should" against "must"**

Passage (from deployment guidance): "Deployments to the test environment must be recorded in the change log. Deployments should take place before 4pm so that any problems can be resolved within working hours. Deployments after 4pm require the agreement of the duty engineer. All deployment records must include the version number and the name of the person deploying."

Which statement accurately reflects the guidance?

- A) Deploying to test at 5pm is forbidden.
- B) Deploying to test at 5pm is permitted with the duty engineer's agreement, and must still be recorded with version number and deployer's name.
- C) Deployments before 4pm do not need to be recorded.
- D) The duty engineer must approve all deployments.

**Correct answer: B**

**Explanation:** Distinguish the modal verbs. "Must be recorded" is an absolute requirement applying to all deployments. "Should take place before 4pm" is a strong recommendation, not a ban — and the next sentence confirms late deployments are possible via a defined route: duty engineer agreement. So a 5pm deployment is permitted with agreement (not forbidden — A wrong), the recording requirement still applies (C wrong, since "must be recorded" has no time exception), and the duty engineer's approval is needed only after 4pm, not always (D wrong). B combines all three readings correctly. The should/must distinction is one of the most practically important reading skills in government digital work — standards documents use these words deliberately, and treating a "should" as a "must" (or the reverse) leads either to needless blockers or to genuine breaches.

**Question 12 (hard) — Evaluating an argument in a team discussion**

Passage (from a team wiki discussion): "We should adopt pair working for all changes to deployment scripts. Last quarter, the three incidents caused by scripting errors all involved scripts written by one person working alone. Pairing catches mistakes as they are made, and it spreads knowledge so we are less dependent on any single engineer. It will feel slower at first, but the time saved on incident response should more than repay it."

Which of the following, if true, would most weaken the argument?

- A) Some engineers enjoy pair working more than others.
- B) The three scripting incidents last quarter were all caused by a fault in the script-testing tool that has since been fixed, not by mistakes a pair would have caught.
- C) Pair working is also used by other government departments.
- D) Deployment scripts are stored in the shared repository.

**Correct answer: B**

**Explanation:** First identify the argument's structure: the key evidence is that all three incidents involved solo-written scripts, and the conclusion is that pairing would prevent such incidents. To weaken an argument, attack the link between evidence and conclusion. Option B does precisely that: if the incidents were caused by a tooling fault — now fixed — that pairing would not have caught, the incidents no longer support the case for pairing at all. Option A is about preference, not effectiveness; C mildly *supports* the argument; D is irrelevant. Note that B does not prove pairing is worthless — knowledge-sharing benefits still stand — it only weakens the incident-based case. Evaluating arguments this way connects directly to your prototyping skill's collaborative theme: teams that pair and work openly still need members who can tell the difference between evidence that genuinely supports a practice and evidence that merely sits near it.

### Preparation tips

- **Read the passage twice: once for the story, once for the details.** The first pass gives you the shape; the second, focused on the statement you are judging, gives you the exact words that decide the answer.
- **Underline (mentally or on paper) the condition words.** "Must", "should", "may", "unless", "only", "including", "out of scope" — these small words carry most of the meaning in workplace documents, and most wrong answers come from gliding over them.
- **Practise "cannot say" until it feels natural.** Take any work document and write three statements about it: one it supports, one it contradicts, one it simply does not address. Doing this a few times rewires the instinct to fill gaps with assumptions.
- **Answer from the passage, never from your workplace.** Test scenarios are self-contained; your team's real conventions are irrelevant, however sensible they are.
- **Read your team's real documents actively.** Runbooks, incident reports, and security notices are perfect practice material — and asking your mentor "does this 'should' mean we can skip it?" is a genuinely good apprentice question that doubles as test preparation.
- **Build a little speed last.** Accuracy first; once you are reliably correct, practise with a timer at roughly 45–60 seconds per statement so the real test's pace feels familiar.

### Common pitfalls to avoid

- **Importing outside knowledge.** The most common verbal reasoning error at every level. If the passage does not say it, you do not know it — even if you are sure it is true at work.
- **Confusing "False" with "Cannot say".** False means the passage *contradicts* the statement; cannot say means the passage is *silent*. Before answering False, find the sentence that rules the statement out.
- **Treating recommendations as rules.** "Should" invites, "must" requires. Mixing them up flips the meaning of guidance documents.
- **Losing track of branches and referents.** In procedures, "otherwise" and "it" decide what happens next. Trace which branch you are on and what each pronoun points to before answering.
- **Answering from the question's tone.** A statement that sounds sensible and professional can still be unsupported; a blunt-sounding statement can be exactly what the passage says. Judge support, not style.
- **Over-reading a summary question.** The best summary is the one that keeps every decision-relevant fact — not the longest option, and not the most dramatic one.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (often shortened to SJT) presents realistic workplace dilemmas and asks you to judge how effective different responses would be. There are no calculations and no passages to parse — instead, each question describes a situation you could genuinely meet as an apprentice DevOps engineer and offers four possible actions. You might be asked to pick the **most effective** response, the **least effective** response, or occasionally to rank all four.

Typical format: 15 to 25 scenarios, usually untimed or generously timed (30 to 45 minutes), delivered online. Scoring compares your judgements against those of experienced professionals and against the behaviours the organisation values — in UK government digital teams, these include user focus, collaboration, taking ownership, knowing when to escalate, honesty when things go wrong, and inclusion. Importantly, SJTs are not personality tests and there is no trick: they measure whether you recognise what good professional behaviour looks like in context.

For an apprentice, the "right" behaviours have a particular shape, and it is worth naming it before you start. At your level, strong answers usually involve: following agreed procedures; being honest immediately when you make a mistake or do not understand; asking for direction rather than guessing on anything that could affect shared environments; contributing observations even though you are junior; and treating security concerns as everyone's business. Weak answers usually involve: staying silent to avoid looking inexperienced; improvising beyond your defined activities; ignoring procedures to be helpful quickly; or passing responsibility for your own learning to others. Notice that "escalate" and "ask first" are often the *strongest* options for you — the opposite of what a senior engineer's SJT might reward. Employers use SJTs precisely because this judgement — knowing what your role requires *at your level* — predicts success better than technical knowledge alone.

### How this assessment maps to your role

The behaviours the SJT measures map directly to your role summary:

- **Following procedures and working under direction** maps to **Service support**: your role is to help with fault investigation "completing defined activities under direction" — so scenarios test whether you stay within agreed procedures and check before deviating.
- **Speaking up and honesty** maps to **Information security** and to shadowing: you are learning to explain security controls, and scenarios test whether you raise concerns (a shared password, an odd email) promptly, even when it feels awkward.
- **Collaboration and openness** maps to **Prototyping**: your skill description explicitly includes working "in an open and collaborative environment (by pair working, for example)" — scenarios test how you behave in pairs, how you receive feedback, and how you include others.
- **Knowing your limits and escalating well** maps to being **involved in implementation but not planning**: scenarios test whether you recognise decisions that belong to others and route them there quickly rather than deciding alone.
- **Curiosity and building knowledge** maps to your duty to **build on your knowledge**: scenarios reward asking good questions, writing up what you learn, and turning mistakes into learning rather than hiding them.

### Practice questions

**Question 1 (easy) — You broke something in the test environment**

While practising a deployment in the test environment, exactly as your mentor showed you, you run a command with a typo and the test service stops responding. Your mentor is at lunch. Nobody has noticed yet. What is the most effective response?

- A) Try a series of commands you found online to fix it before anyone notices.
- B) Say nothing — it is only the test environment, and someone will restart it eventually.
- C) Tell the team straight away what you ran and what happened, via the team channel, and ask what you should do.
- D) Wait until your mentor is back from lunch, then mention it privately.

**Correct answer: C**

**Explanation:** The strongest behaviours here are honesty, speed, and staying within your competence. Option C shows all three: the team learns immediately that the environment is down and why, which saves colleagues from wasting time investigating a mystery, and you ask for direction rather than experimenting. Option A compounds the problem — running unfamiliar commands from the internet on a shared environment is exactly how a small incident becomes a big one. Option B is dishonest by omission and disrespects colleagues who rely on the test environment. Option D is honest but slow: an hour of teammates hitting a broken environment is a real cost, and "privately" suggests managing appearances rather than the problem. Mistakes are expected at apprentice level; what is being assessed is your response to them. Teams consistently say the same thing: an apprentice who says "I broke it, here's what I did" earns trust faster than one who never appears to make mistakes.

**Question 2 (easy) — A password pasted in the team chat**

A developer in your team pastes a database password into the open team chat channel so a colleague can "grab it quickly". You are the only other person who seems to have noticed. What is the most effective response?

- A) Ignore it — you are the most junior person, and it is not your place to comment.
- B) Quietly message the developer to flag it, so they can remove it and rotate the password, and mention it to your mentor so the right process is followed.
- C) Post "You shouldn't share passwords in chat!" in the channel so everyone learns from it.
- D) Copy the password into your own notes in case you need it later.

**Correct answer: B**

**Explanation:** Security is everyone's business, including apprentices — your role explicitly includes learning to explain security controls, and this is one working in front of you. Option B raises the issue promptly, routes it kindly (a private nudge preserves the developer's dignity and gets fast action), and ensures proper follow-through (rotation, and your mentor's awareness) because a pasted password stays in chat history even after deletion. Option A treats seniority as a reason to ignore a live risk — the behaviour SJTs most want to rule out. Option C addresses the issue but chooses public embarrassment over effectiveness; shaming colleagues makes people hide problems next time. Option D is itself a security breach: storing credentials you have no need for violates the least-privilege principle. The pattern to remember: raise security concerns quickly, kindly, and through the right channel — and never widen the exposure.

**Question 3 (easy) — You do not understand the task you were given**

Your mentor asks you to "check the overnight jobs and flag anything unusual", then joins a meeting. You realise you are not sure which jobs count as "the overnight jobs" or what "unusual" means here. What is the most effective response?

- A) Wait for the meeting to end — an hour or so — and ask then, doing nothing in the meantime.
- B) Check whatever jobs you can find and flag anything that looks odd to you, guessing at what was meant.
- C) Look for a runbook or wiki page about overnight job checks; if you find one, follow it and note your assumptions; if not, send your mentor a short message asking which jobs are meant, and start with what you can confirm.
- D) Ask another team entirely, so you do not bother your mentor.

**Correct answer: C**

**Explanation:** This scenario tests resourcefulness balanced with honesty about uncertainty. Option C shows the ideal apprentice pattern: first try to resolve the ambiguity yourself using team documentation (building your knowledge), make your assumptions visible, and ask a precise, non-urgent question that your mentor can answer in ten seconds between meetings. Option A wastes an hour when a message would do — passivity is a weak behaviour even at apprentice level. Option B guesses on a monitoring task, which risks both false alarms and missed problems, and hides the uncertainty that your mentor needs to know about to teach you. Option D routes a question about *your team's* jobs to people without the context, spending others' time to avoid a trivial interruption. The general rule: try the documentation, state your assumptions, ask early and precisely. Nobody expects an apprentice to know — they expect an apprentice to find out visibly.

**Question 4 (easy) — Pairing is not working for you**

You are pair working with a developer on a small script — a core part of how your team works. The developer types fast, rarely explains, and you have understood little for the past hour. They seem happy and have not noticed. What is the most effective response?

- A) Keep nodding — interrupting would slow them down, and you can try to figure it out later.
- B) Say, at a natural pause: "Could we slow down a little? I'd learn a lot more if I could drive for a bit while you guide me."
- C) Stop pairing with this developer and ask your mentor to always pair you with someone else.
- D) Secretly record the session so you can review it later.

**Correct answer: B**

**Explanation:** Pair working exists precisely so knowledge transfers — your role summary names working openly and collaboratively, "by pair working, for example", as part of your prototyping skill. Option B addresses the problem directly, kindly, and constructively: swapping to the driver's seat with the senior navigating is a classic technique that forces the pace down to the learner's speed, and asking for it shows ownership of your own learning. Option A wastes the session and lets a poor pattern continue for future sessions too; silent nodding is the least effective learning behaviour there is. Option C escalates a solvable communication issue into avoidance without ever giving feedback — the developer cannot fix what they have not been told. Option D avoids the real conversation and raises obvious trust and privacy problems. The broader lesson: at apprentice level, politely asking for what you need in order to learn is not an imposition — it is the job.

**Question 5 (moderate) — Asked to skip a step to save time**

You are helping a developer deploy to the test environment, following the team checklist under their direction. The developer says: "Skip the change log entry — it's a tiny change and we're in a hurry. Nobody reads it anyway." What is the most effective response?

- A) Skip it — the developer is senior to you and it is their responsibility.
- B) Refuse loudly and report the developer to their manager immediately.
- C) Say you would rather complete it since it takes only a minute, do it, and if the developer insists on skipping steps, mention the conversation to your mentor afterwards.
- D) Skip it, but secretly write the entry later without telling anyone.

**Correct answer: C**

**Explanation:** This tests whether you hold to agreed procedures under gentle social pressure. Option C does everything well: it keeps the procedure intact with a low-friction, non-confrontational move (the "it only takes a minute" framing lets the developer save face), and it uses your support network appropriately if the pressure continues — your mentor can address a pattern that is not yours to police. Option A treats seniority as overriding an agreed team standard; the change log exists to make fault investigation possible, and "nobody reads it" is exactly wrong — it is read precisely when something breaks. Option B jumps to the most severe escalation for a first, minor lapse, damaging the relationship and skipping every proportionate step. Option D fixes the record but hides a disagreement that the team needs to resolve openly — and doing things "secretly" is almost never a strong SJT behaviour. Remember the shape: comply with standards cheerfully, make compliance easy for others, escalate patterns rather than moments.

**Question 6 (moderate) — You spot something odd while shadowing**

You are shadowing a senior engineer during a live fault investigation — well beyond your level, and you are there to watch and learn. On one screen you notice that the engineer is about to run a cleanup command against what the prompt says is the **live** database, but moments earlier they said they were working on the **test** copy. Everyone is stressed. What is the most effective response?

- A) Say nothing — they are senior, stressed, and you are probably wrong.
- B) Say: "Sorry — quick check: that prompt says live, and I thought we were on the test copy?"
- C) Wait until after the command runs, then ask whether it was the right environment.
- D) Leave the room and report your concern to your mentor.

**Correct answer: B**

**Explanation:** This is the classic "speaking up" scenario, and it appears in SJTs across safety-critical professions for good reason. Option B is a brief, respectful, well-formed challenge: it states the specific observation (the prompt says live), frames it as a check rather than an accusation, and lands *before* the irreversible action. If you are wrong, ten seconds are lost; if you are right, you have prevented a serious incident. Option A weighs your junior status above a possible live-data loss — exactly the deference that incident reviews repeatedly identify as a cause of harm. Option C offers the check only after it can no longer help. Option D routes the concern away from the person who can act on it, at the speed of walking. Note the wider point for your role: teams run shadowing precisely because fresh eyes catch things tired experts miss. A well-phrased "quick check" is among the most valuable contributions an apprentice can make.

**Question 7 (moderate) — Behind on your training log**

Your apprenticeship requires you to keep a training log, reviewed quarterly. You are three weeks behind on entries because project work has been busy and honestly more interesting. Your review is in two weeks. What is the most effective response?

- A) Reconstruct the missing entries in one long evening session the night before the review.
- B) Tell your mentor you are behind, block two or three short slots in your calendar this week to catch up while memories are fresh, and set a recurring weekly slot so it does not happen again.
- C) Ask a fellow apprentice to share their entries so you can adapt them.
- D) Skip the log — the project work itself is surely evidence enough.

**Correct answer: B**

**Explanation:** This scenario tests ownership of your own development, which is the heart of the apprentice role ("build on your knowledge"). Option B has all the strong elements: honesty with your mentor before the review rather than at it; catching up now, while you can still remember what you learned (waiting longer degrades the evidence); and — most importantly — a system change (the recurring slot) so the problem does not recur. Option A produces rushed, thin entries and models exactly the cramming habit that fails in operational work too. Option C crosses an integrity line: a training log is evidence of *your* learning, and adapting someone else's is misrepresentation. Option D unilaterally decides that a programme requirement does not apply to you — a decision that belongs to your apprenticeship provider, not to you. The pattern that generalises: surface the slippage early, recover promptly, and fix the system rather than relying on future willpower.

**Question 8 (moderate) — A teammate is struggling and you could help**

A fellow apprentice on a neighbouring team confides that they are completely lost on a scripting task and are afraid to admit it because "everyone else seems to get it". You remember struggling with, and eventually understanding, the same topic. You also have your own deadline this afternoon. What is the most effective response?

- A) Give them the working script you wrote for the equivalent task so they can submit it.
- B) Tell them everyone struggles and they should just ask their mentor.
- C) Offer a short pairing session — perhaps 30 minutes after your deadline — to talk through the approach, and encourage them to tell their mentor how they are finding it, since mentors want to know.
- D) Tell their mentor yourself, immediately, that the apprentice is struggling and hiding it.

**Correct answer: C**

**Explanation:** This scenario balances collaboration, inclusion, honesty, and managing your own commitments. Option C helps in the way that actually builds capability — talking through the approach rather than handing over an answer — while protecting your own deadline by timeboxing, and it gently pushes the underlying fix: their mentor can only help with what they know about, and normalising "I'm finding this hard" is part of a healthy team culture. Option A feels kind but harms them twice: they learn nothing, and submitting your work as theirs creates an integrity problem for you both. Option B is not wrong, but it is minimal — it dismisses the feeling ("everyone struggles") and passes the whole matter back without offering the concrete help you are well placed to give. Option D breaks a confidence without warning; encouraging them to speak (option C) achieves the same outcome with their agency intact, and escalating over their head is proportionate only if real risk continues. Peer support between apprentices is one of the quiet engines of good teams — offered as teaching, never as substitution.

**Question 9 (moderate) — Ambiguous instruction with a deadline**

Your mentor asked you to "tidy up the old test data on TST-02 today" before leaving for an off-site event; they are reachable but slow to respond. Looking at TST-02, you find two data folders: one clearly labelled `archive-2023` and one labelled `current-cycle` that looks old but is not clearly archived. Deleting the wrong data would disrupt the testing team. It is 3pm. What is the most effective response?

- A) Delete both folders — "tidy up" means tidy up, and the deadline is today.
- B) Delete `archive-2023` now, leave `current-cycle` untouched, and message your mentor: "Cleared archive-2023 on TST-02. Not certain about current-cycle — looks old but isn't marked. Left it alone; happy to clear it tomorrow if you confirm."
- C) Do nothing until your mentor replies, even if that means the task is not done today.
- D) Ask the testing team to make the decision and delete whatever they say.

**Correct answer: B**

**Explanation:** This is a judgement about acting under direction when the direction is incomplete. Option B applies a golden operations principle: do the reversible-in-effect, clearly safe part now, and hold the ambiguous, destructive part until confirmed — deletion is irreversible, so uncertainty defaults to "don't". The message is a model of good communication: what was done, what was not, why, and a proposed next step, letting your mentor resolve it with one word. Option A resolves ambiguity in the riskiest direction to serve a deadline that is almost certainly softer than data loss is costly. Option C is safe but needlessly abandons the half of the task you *can* do confidently — full paralysis is not the goal. Option D consults useful people (a reasonable instinct!) but hands *your* task's decision entirely to another team who may not know your mentor's intent; their input should inform, not replace, your mentor's confirmation. Remember the rule: partial progress on the safe part, plus a crisp question on the risky part, beats both guessing and freezing.

**Question 10 (hard) — Credit for your observation**

Last week, while shadowing, you noticed a recurring warning in a service log and mentioned it to a senior engineer, who investigated and found a genuine problem. At the team meeting, the engineer describes finding the issue without mentioning your observation. Your mentor was not there. What is the most effective response?

- A) Interrupt the meeting to point out that you spotted it first.
- B) Say nothing ever — apprentices should not expect credit.
- C) Afterwards, mention it lightly to the engineer ("glad that warning I spotted turned out to matter!"); if it becomes a pattern, discuss it with your mentor. Record the contribution in your own training log regardless.
- D) Email the whole team correcting the record.

**Correct answer: C**

**Explanation:** This scenario is about proportionality and long-term relationships more than about justice in the moment. Option C fits the scale of the issue: a light, friendly comment gives the engineer the chance to acknowledge you (most will, and many omissions are careless rather than deliberate); the training log ensures your apprenticeship evidence — the thing that formally matters for you — captures the contribution regardless; and the escalation path (mentor, if it becomes a pattern) is reserved for the version of the problem that genuinely warrants it. Option A trades a small grievance for a public confrontation that will define you more than the observation did. Option B swings the other way: your contributions are legitimate evidence of your development, and consistently unacknowledged work is worth addressing — silence forever is self-erasure, not humility. Option D applies maximum force to a first occurrence. The generalisable pattern: address small slights lightly and directly, keep your own record, and escalate patterns, not incidents.

**Question 11 (hard) — Asked to do something beyond your access — by a stranger**

You receive a chat message from someone you do not recognise, whose profile says "Platform Support": "Hi! We're mid-incident and short-handed. Can you run the attached script on the build server? Your mentor said you could help." Your mentor is offline. The request feels urgent and flattering. What is the most effective response?

- A) Run the script — incidents are urgent, and they said your mentor approved it.
- B) Reply that you cannot run scripts on shared servers without direction, and verify the request through a known channel: check with your team lead or the official incident channel before doing anything.
- C) Ignore the message entirely — it is not your problem.
- D) Forward the script to a fellow apprentice who has build server access.

**Correct answer: B**

**Explanation:** This scenario combines social engineering awareness with knowing your limits — both central to your information security skill. The message has classic warning signs: unknown sender, urgency, flattery, an unverifiable authority claim ("your mentor said"), and a request to execute an attachment on shared infrastructure. Option B does the two right things in the right order: declines to act outside direction, and *verifies through an independent, known channel* — never by asking the requester themselves, since a genuine colleague will welcome verification and an attacker cannot survive it. Option A executes an unverified script on a build server on the say-so of a stranger — potentially the single most damaging click available to an apprentice. Option C is safer than A but wrong twice: if the incident is real, the team loses time; if it is an attack, security needs to know it is happening — reporting suspected phishing is part of the control set you are learning to explain. Option D just relocates the risk to a friend. Verify first, act under direction, report the suspicious: that trio serves you at every level of this profession.

**Question 12 (hard) — Least effective: the retrospective after your mistake**

Two weeks ago you accidentally deleted a test dataset; the team lost half a day restoring it. You owned up immediately and the team was supportive. Today's retrospective includes the item "test data loss — how do we prevent recurrence?". You feel embarrassed all over again. Which response would be **least effective**?

- A) Contribute openly: describe what you did, what confused you, and suggest that the deletion script ask for confirmation when pointed at shared datasets.
- B) Stay quiet and hope the item passes quickly; if asked, give brief answers and avoid detail.
- C) Ask the facilitator beforehand whether you can walk the team through the timeline, since you know it best.
- D) Suggest the team also consider whether the dataset should have had a backup, so the fix covers more than your specific slip.

**Correct answer: B**

**Explanation:** Read carefully — this question asks for the *least* effective response, a common SJT format that catches people who stop reading the stem. Option B is the weakest behaviour: retrospectives in digital teams are explicitly blameless and exist to convert incidents into system improvements; withholding the detail only you have (what exactly confused you) starves the team of the very information that prevents recurrence. Every other option strengthens the outcome: A converts embarrassment into a concrete safeguard (confirmation prompts are a classic guard-rail); C shows real ownership by volunteering the clearest account; D broadens a person-shaped fix into a system-shaped one — backups protect against every future cause of deletion, not just yours. Notice the deeper lesson your teams will echo: after a mistake is honestly owned, the follow-through — contributing fully to the fix — is what completes the trust repair. The discomfort is real; the strong move is to bring your knowledge anyway.

### Preparation tips

- **Learn the behaviour patterns, not scripted answers.** Strong apprentice responses almost always combine honesty, promptness, staying within direction, asking precise questions, and fixing systems rather than symptoms. If you can name the behaviours, you can recognise them in any scenario.
- **Read the stem twice — especially for "least effective" questions.** A large share of SJT errors come from answering the opposite question to the one asked.
- **Judge actions, not personalities.** The question is what the *response* achieves, not whether you personally would feel comfortable doing it. Slightly uncomfortable-but-right (a polite challenge, an early admission) usually beats comfortable-but-passive.
- **Anchor on your role level.** Before answering, ask: "What does an apprentice — supervised, learning, not responsible for planning — owe the team here?" Options perfect for a senior engineer (deciding alone, directing others) are often wrong for you, and vice versa.
- **Collect real dilemmas from your workplace.** When you see a colleague handle an awkward situation well — a blameless retro, a graceful challenge, a good escalation — note what made it work. Your team is a living SJT answer key.
- **Do not overthink.** SJTs measure practical judgement, and your first considered reading of a scenario is usually your best. Change an answer only when you have genuinely misread something.

### Common pitfalls to avoid

- **Choosing silence to seem easy-going.** Across scenarios, the most heavily penalised apprentice behaviour is noticing a problem — a security lapse, a wrong environment, your own confusion — and saying nothing.
- **Choosing heroics to seem capable.** The second most penalised behaviour is acting alone beyond your direction: running unknown fixes, deleting ambiguous data, executing strangers' scripts. Your level's strength is asking well, not improvising boldly.
- **Escalating everything, or nothing.** Proportionality is the skill: a quiet word for a first slip, your mentor for patterns and risks, immediate wide alerting for live danger. Options at the wrong intensity for the situation are wrong options.
- **Hiding mistakes or delaying disclosure.** "Tell the team now, plainly" beats every variant of waiting, softening, or managing appearances. SJT scoring reflects what incident reviews show about real teams.
- **Sacrificing procedures to social pressure.** Seniority, hurry, and friendliness are the three pressures scenarios use; agreed standards outrank all three, and there is nearly always a low-friction way to hold the line.
- **Forgetting the person in the problem.** Options that solve the issue while humiliating a colleague (public corrections, instant reports to managers) score below options that solve it while preserving the relationship. Kind and firm beats loud and right.

## Conclusion

Well done for working through this guide — that took real commitment, and commitment to learning is the single most important quality in an apprentice DevOps engineer.

Take a moment to notice what you have practised. In the cognitive section, you compared pipeline runs against expected patterns, followed runbook conditions precisely, reasoned from environment rules, and worked through multi-constraint puzzles step by step. In the numeric section, you calculated disk percentages, uptime figures, build-time averages, fair failure-rate comparisons, and multi-step capacity and cost forecasts — always with the working shown. In the verbal section, you held the line on "cannot say", separated "should" from "must", traced branches through procedures, and judged which sentence a tired colleague at handover would actually understand. And in the situational judgement section, you rehearsed the moments that define early careers: owning a mistake immediately, speaking up before the wrong command runs, holding a procedure under friendly pressure, and spotting a social-engineering attempt dressed up as urgency.

None of that was abstract test technique. Every skill you practised maps straight back to your role: explaining availability and capacity management, understanding how services are built, explaining security controls, working openly in pairs, and helping investigate faults under direction. That means every hour you spent here was professional development twice over — preparation for assessments, and preparation for Tuesday morning at work.

A few parting thoughts. First, keep practising little and often; ten minutes with a real dashboard or a real runbook, asking yourself the kinds of questions this guide asks, will keep the skills sharp. Second, take the behaviour patterns from the situational judgement section into your actual week — ask the precise question, write the specific handover note, raise the quiet security concern — because judgement, like any skill, grows with use. Third, on assessment day itself: sleep, read carefully, sense-check your arithmetic, answer from the passage, and trust the preparation you have done.

Finally, remember what assessments at your level are really measuring: not encyclopaedic knowledge, but carefulness, honesty, clear thinking, and the willingness to learn — qualities you have been demonstrating on every page of this guide. You are at the very beginning of a profession that your organisation and the people who use government services genuinely depend on. Keep shadowing curiously, keep asking good questions, and keep building on your knowledge.

Good luck — you are better prepared than you think.
