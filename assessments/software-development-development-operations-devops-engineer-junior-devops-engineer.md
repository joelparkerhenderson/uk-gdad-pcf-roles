# Junior DevOps Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a junior DevOps engineer in the UK Government Digital and Data profession. You might be preparing for an assessment as part of a development review, getting ready to apply for your next role, or simply wanting to understand how these tests connect to the work you do. Whatever your reason, this document will help you practise with confidence.

Let's start with the basics: a psychometric assessment is a structured, standardised set of exercises that measures the thinking skills and workplace behaviours that predict success in a role. That may sound daunting, but there is good news. Well-designed assessments contain no trick questions, and every skill they measure can be strengthened with practice. Better still, the assessments in this guide are job-specific: they are built from the materials you genuinely work with — scripts and pipeline configurations, monitoring dashboards, service tickets, maintenance procedures, user stories, and code review comments — and from the decisions you genuinely face while learning on the job, building software components, and working under supervision.

Why do these assessments matter for a junior DevOps engineer in particular? Your role sits at a busy crossroads. You design, code, test, correct, and document simple programs and scripts under the direction of others. You help fix service faults following agreed procedures and carry out maintenance tasks on service support infrastructure. You assist, as part of a team, in the design of components of larger systems, and you are learning how systems integrate and why interfaces between them are challenging. Every one of those duties leans on the four abilities this guide covers: cognitive ability (spotting patterns and errors, reasoning through rules), numeric reasoning (percentages, rates, and reading monitoring data), verbal reasoning (understanding procedures, standards, and user stories precisely), and situational judgement (choosing wisely when work gets messy or pressured).

The document is organised into four main assessment sections, each following the same pattern. First comes an overview of what the assessment measures and the typical test format, so nothing on the day surprises you. Next, a mapping section connects the assessment directly to the named skills in your role summary — from programming and build to systems integration and user focus — so you can see this is practice for your real job, not abstract puzzling. Then come the practice questions, starting easy and building to hard, each with a full worked explanation that walks through the reasoning or arithmetic step by step. Finally, each section closes with preparation tips and common pitfalls.

Here is how to get the most from the guide. Work through one section at a time; there is no prize for finishing quickly. Attempt each question honestly, and write your answer down before reading the explanation — the moment of commitment is where learning happens. Treat every explanation as a mini-lesson, even when you answered correctly, because the technique it describes will transfer to other questions and to your daily work. When arithmetic is involved, follow it with pen and paper. And be reassured: at junior level, assessments measure carefulness, clear thinking, and potential — not encyclopaedic knowledge. Nobody expects you to know everything; they expect you to reason well with what is in front of you, which is a skill you exercise every working day.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the mental processes your role actually uses, presented through practical workplace scenarios rather than abstract puzzles. Instead of shape sequences with no context, you will reason about the everyday materials of a junior DevOps engineer's week: script configurations, pipeline stage rules, log extracts, branching conventions, maintenance procedures, and interface specifications.

The typical format is an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your responses are compared against a norm group of people at a similar career stage, so you are measured fairly against other early-career engineers, not against seasoned specialists. Many platforms adapt difficulty as you go — if the questions feel like they are getting harder, that usually means you are doing well. Employers typically receive a balance of speed and accuracy rather than a single number, so a careful, methodical approach scores well. Almost every test offers ungraded warm-up questions first, so you can settle into the interface without pressure.

For a junior DevOps engineer, cognitive assessment is particularly relevant because your core daily activities are structured thinking in miniature. When you code and test a simple script under direction, you hold a specification in mind and check your work against it. When you help fix a fault following an agreed procedure, you trace conditions and branches precisely. When you assist with the design of a component in a larger system, you reason about how rules and dependencies interact. A good cognitive test simulates exactly these demands, which means practising for it genuinely sharpens your work, not just your test score.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to **Programming and build (software engineering)** and **Service support**: designing, coding, and correcting simple scripts means recognising the recurring shapes of healthy code, consistent naming, and normal log output — and noticing quickly when something deviates.
- **Logical deduction** maps to **Systems integration** and **Availability and capacity management**: explaining the process and principles of integrating systems requires reasoning about dependencies — if service A needs interface B, and B is not deployed, what follows? — and availability processes are built from precisely such conditional rules.
- **Error checking** maps to **Modern development standards** and **Programming and build**: applying development standards under guidance means comparing artefacts — a script against its specification, a configuration against the team convention — and spotting mismatches before they reach the shared pipeline.
- **Prioritisation** maps to **Service support** and working under supervision: helping fix faults following agreed procedures, while also carrying out maintenance tasks, means constantly sequencing work sensibly and knowing which deadline genuinely binds.
- **Applied problem solving** maps to **Systems design** and **Prototyping**: assisting in the design of components, and knowing when a quick prototype will answer a question faster than a debate, both depend on reasoning about cause and effect in the development process.

### Practice questions

**Question 1 (easy) — Pattern recognition in branch names**

Your team's convention for git branch names is `<type>/<ticket-number>-<short-description>`, where type is one of `feature`, `bugfix`, or `chore` — for example `bugfix/DEV-214-fix-timeout`. You are reviewing the branch list before a tidy-up:

1. `feature/DEV-301-add-retry-logic`
2. `bugfix/DEV-305-null-check`
3. `DEV-310-update-readme/chore`
4. `chore/DEV-312-bump-dependencies`

Which branch breaks the convention?

- A) Branch 1
- B) Branch 2
- C) Branch 3
- D) Branch 4

**Correct answer: C**

**Explanation:** Check each branch against the pattern piece by piece: type first, then a slash, then ticket number, hyphen, description. Branches 1, 2 and 4 all follow it. Branch 3 reverses the structure — the ticket and description come first and the type `chore` is at the end. The reliable method is component-by-component comparison rather than an overall glance, because reversed or shuffled elements can look superficially plausible. Naming conventions matter in real life for the same reason they appear in tests: automation often keys off them — a pipeline might run different checks for `bugfix/` branches than for `chore/` branches — so a malformed name can silently get the wrong treatment. Spotting convention breaks quickly is part of applying modern development standards under guidance.

**Question 2 (easy) — Logical deduction from deployment rules**

Your team's rules say: (i) every change must pass the automated test suite before it can be merged; (ii) every merged change is automatically deployed to the test environment; (iii) only changes that have been in the test environment for at least one day may be promoted to staging. A colleague tells you their change was merged this morning. Which statement must be true?

- A) The change has passed the automated test suite.
- B) The change is already in staging.
- C) The change will be promoted to staging tomorrow.
- D) The change has been reviewed by a senior engineer.

**Correct answer: A**

**Explanation:** Work backwards from what you are told: the change was merged. Rule (i) says passing the test suite is a requirement for merging, so a merged change must have passed — statement A is guaranteed. Statement B cannot be true yet: rule (iii) requires at least a day in test, and the change was merged only this morning. Statement C confuses "may be promoted" with "will be promoted" — eligibility is not a schedule; nobody has said anyone will promote it. Statement D introduces a review requirement that appears nowhere in the given rules, however sensible it sounds. The discipline being tested is deducing only what the rules guarantee, which is the same discipline you use when reasoning about your team's real pipeline: knowing what a green tick actually proves, and what it does not, keeps your debugging assumptions honest.

**Question 3 (easy) — Error checking a script against its specification**

You have been asked to write a small script to the following specification: "Read the list of servers from `servers.txt`. For each server, check disk usage. If usage is 90% or above, write the server name to `alerts.txt`. Print a summary count at the end." Your first draft does the following: reads `servers.txt`; checks disk usage for each server; writes the server name to `alerts.txt` if usage is above 90%; prints a summary count. What is the discrepancy?

- A) The script reads the wrong file.
- B) The script treats exactly 90% differently from the specification.
- C) The script fails to print a summary.
- D) There is no discrepancy.

**Correct answer: B**

**Explanation:** Compare each behaviour with the specification clause by clause. Reading `servers.txt`: matches. Checking each server: matches. The alert condition is where they diverge: the specification says "90% or above" (which includes exactly 90%), but the draft alerts only when usage is "above 90%" (which excludes exactly 90%). A server sitting at precisely 90% would be missed. The summary count: matches. Boundary conditions — "above", "at least", "or above", "more than" — are the single most common source of small script bugs, and test questions probe them because real specifications hinge on them. When you design, code, test, and correct simple programs under direction, building the habit of checking boundaries explicitly (what happens at exactly the threshold?) will save you and your reviewers many round trips.

**Question 4 (easy) — Sequencing a maintenance procedure**

A maintenance task on the log-collection infrastructure has these steps with dependencies: Step W (notify the team) must happen before anything else; Step X (stop the collector service) must happen before Step Y (rotate the log archive); Step Z (restart the collector and confirm logs are flowing) must be last. Which order satisfies all the constraints?

- A) W, Y, X, Z
- B) X, W, Y, Z
- C) W, X, Y, Z
- D) W, X, Z, Y

**Correct answer: C**

**Explanation:** Apply the constraints one at a time and eliminate. W must be first: that eliminates option B (which starts with X). X must precede Y: that eliminates option A (Y before X). Z must be last: that eliminates option D (Y after Z). Only option C survives: notify, stop, rotate, restart-and-confirm. Elimination against explicit constraints is faster and more reliable than trying to imagine the whole procedure at once. This mirrors your real duty of carrying out maintenance tasks on service support infrastructure: maintenance runbooks are dependency chains, and understanding *why* the order matters — you cannot safely rotate an archive a running service is still writing to, and you always confirm recovery at the end — turns rote step-following into genuine operational understanding.

**Question 5 (moderate) — Pattern recognition in error logs**

You are investigating a fault. The application log shows these entries over ten minutes: 09:00 OK, 09:01 OK, 09:02 TIMEOUT, 09:03 OK, 09:04 OK, 09:05 TIMEOUT, 09:06 OK, 09:07 OK, 09:08 TIMEOUT, 09:09 OK. A colleague asks what you notice. Which observation is most accurate and useful?

- A) Timeouts are random noise and can be ignored.
- B) Timeouts occur every third minute — a regular cycle that suggests a periodic cause, such as a scheduled job competing for resources.
- C) The service is down.
- D) Timeouts are increasing in frequency.

**Correct answer: B**

**Explanation:** Lay the entries out and look for structure: TIMEOUT appears at 09:02, 09:05, and 09:08 — exactly every three minutes, with normal operation in between. That regularity is the finding. Option A dismisses a clear pattern; option C overstates it (seven of ten checks are OK — the service is degraded periodically, not down); option D is contradicted by the even spacing. The useful part of option B is the inference: strictly periodic failures usually have periodic causes — a cron job, a polling process, a batch flush — which immediately narrows the investigation. This is the shape of good fault-finding under agreed procedures: describe the pattern precisely first ("every three minutes"), then let the pattern suggest where to look. Vague reports ("it times out sometimes") send investigations in circles; precise ones shorten them.

**Question 6 (moderate) — Deduction about interface compatibility**

You are assisting with a simple integration. Service P sends dates as `DD-MM-YYYY`. Service Q, which consumes P's messages, expects dates as `YYYY-MM-DD`. A transformation component T sits between them and converts P's format into Q's. The team plans to upgrade P so it sends `YYYY-MM-DD` directly. If P is upgraded but T is left unchanged and still applies its conversion, what is the most likely result?

- A) Everything works, because P now sends the format Q expects.
- B) T will mangle the already-correct dates — for example reading the year field as a day — so Q receives wrong or invalid dates.
- C) Q will reject the messages because P changed.
- D) T will automatically detect the new format and pass it through.

**Correct answer: B**

**Explanation:** Trace the data through each component. After the upgrade, P emits `YYYY-MM-DD`. T, unchanged, still assumes its input is `DD-MM-YYYY` and applies its rearrangement — so it will treat the first field (the year) as a day and reshuffle correct dates into nonsense, or fail outright when "2025" is not a valid day. Q then receives garbage. Option A forgets T exists; option D credits T with intelligence it was never given — simple transformations do what they are coded to do, nothing more; option C is vague and misplaces the failure point. This is a classic illustration of why "designing, building and testing interfaces between systems" is challenging, exactly as your systems integration skill describes: every component encodes assumptions about its neighbours, and changing one end of a chain without checking the middle breaks integrations in quiet, confusing ways. The test-taking technique — follow the data step by step through each stage — is also the debugging technique.

**Question 7 (moderate) — Prioritisation under supervision**

It is 9:30am. Your supervisor is out until 1pm but reachable for emergencies. On your plate: (1) a fault ticket assigned to you yesterday, with an agreed procedure to follow, promised to the affected team "by end of day"; (2) your coding task for the sprint, due at Thursday's review — it is Tuesday; (3) a calendar reminder that the weekly cleanup job on the support infrastructure must be started before 10am, taking five minutes to kick off; (4) a chat message from a developer asking you to review a pull request "when you get a chance". What do you do first?

- A) Start the fault ticket — it has today's deadline.
- B) Kick off the cleanup job now, then work the fault ticket, fit the pull request review into a natural break, and continue the sprint task after that.
- C) Reply to the pull request first — a colleague is waiting on you.
- D) Message your supervisor to ask what to do first.

**Correct answer: B**

**Explanation:** Sequence by deadline hardness and cost. The cleanup job has the nearest hard deadline (before 10am), takes five minutes, and missing it costs a whole week — do it immediately. The fault ticket has a same-day commitment to another team and an agreed procedure to follow: it becomes your main work next. The pull request has no stated urgency ("when you get a chance") and fits a natural break mid-morning — leaving a colleague blocked all day would be unhelpful, but it need not jump the queue. The sprint task has two days of slack. Option A skips a five-minute task whose window closes in half an hour; option C puts the softest request first; option D outsources a decision you have enough information to make — supervisors want juniors to sequence routine work themselves and ask about genuine uncertainties, not calendars. The pattern: short, hard-deadlined tasks first, then committed work, with courtesy tasks slotted into gaps.

**Question 8 (moderate) — Error checking a pipeline configuration**

The team convention for the pipeline configuration is: every service must define the stages `build`, `test`, and `deploy`, in that order; the `deploy` stage must name a target environment; and notification on failure must go to the team channel `#platform-alerts`. You review this configuration summary for a new service: stages defined: `build`, `test`, `deploy` (in that order); deploy target: (blank); failure notifications: `#platform-alerts`. How many convention requirements are violated?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Audit each requirement independently. Requirement 1: the three stages exist in the right order — satisfied. Requirement 2: the deploy stage must name a target environment — the target is blank, so this is violated. Requirement 3: failure notifications to `#platform-alerts` — satisfied. Exactly one violation. The method is a compliance checklist: enumerate the rules, check each against the evidence, count. Rushing produces two classic errors: missing the blank field because the stage itself exists (the stage being present is not the same as the stage being complete), or double-counting one defect under two rules. In real work, a blank deploy target is exactly the kind of quiet misconfiguration that passes casual review and then fails — or worse, deploys somewhere unintended — at the worst moment. Careful configuration review is applying modern development standards in its most practical form.

**Question 9 (moderate) — Applied problem solving: what changed?**

A script you wrote runs nightly and has worked for three weeks. Last night it failed with "permission denied" when writing its output file. You have changed nothing in the script. Three events happened yesterday: (1) the infrastructure team applied security hardening to the server, tightening directory permissions; (2) you renamed a variable inside a *different* script; (3) the nightly backup ran an hour later than usual. What should you investigate first?

- A) The variable rename in the other script
- B) The security hardening and the permissions on the output directory
- C) The backup timing
- D) Rewrite the script from scratch

**Correct answer: B**

**Explanation:** Match the symptom to the candidate causes. The error is "permission denied" on a write — a permissions symptom. Event (1) is a permissions change on that server: a direct mechanism. Event (2) happened in a different script and cannot affect this one's permissions. Event (3) could in principle cause contention, but it does not produce "permission denied", and the timing correlation is weaker than a same-day permissions change with a matching symptom. Option D abandons diagnosis entirely — rewriting without understanding the cause usually reproduces the failure. The technique — "what does the error message say, and which recent change has a mechanism that produces exactly that?" — is the everyday core of helping fix service faults. It also illustrates a humbling operational truth worth internalising early: "I changed nothing" never means "nothing changed". Environments change around your code constantly, which is why teams track infrastructure changes as carefully as code changes.

**Question 10 (hard) — Multi-constraint scheduling**

You must complete four tasks today: D (documentation update, 1 hour, must be done before the 4pm team demo); M (maintenance window task, exactly 12:00–13:00, fixed); F (fault fix following the agreed procedure, 2 hours, must be finished before the maintenance task because the maintenance reboots the server you need); and R (code review for a colleague, 30 minutes, any time). You start at 9:00 and take lunch 13:00–13:30. Which schedule works?

- A) F 9:00–11:00, R 11:00–11:30, M 12:00–13:00, D 13:30–14:30
- B) D 9:00–10:00, F 10:00–12:00, M 12:00–13:00, R 13:30–14:00
- C) R 9:00–9:30, D 9:30–10:30, M 12:00–13:00, F 13:30–15:30
- D) F 9:00–11:00, M 11:00–12:00, D 12:00–13:00, R 14:00–14:30

**Correct answer: A**

**Explanation:** Test each option against every constraint. Option A: F occupies 9:00–11:00, finishing before M — satisfied; M sits exactly at 12:00–13:00 — satisfied; D at 13:30–14:30 finishes well before the 4pm demo — satisfied; R fits at 11:00–11:30 — satisfied. All constraints hold. Option B looks plausible, but check F: 10:00–12:00 means F finishes exactly as M begins — "finished before the maintenance task" is satisfied only if 12:00 counts as before; more decisively, D is done 9:00–10:00, which is fine, and R at 13:30–14:00 is fine — the flaw is that F ending at precisely 12:00 leaves zero margin, and strict reading of "before" makes it borderline; option A is unambiguously valid. Option C puts F *after* M — but M reboots the server F needs, and the constraint says F must finish first: violated. Option D schedules M at 11:00–12:00, but the window is fixed at 12:00–13:00: violated. When two options both seem workable, prefer the one that satisfies every constraint cleanly rather than at the boundary — in scheduling questions and in real maintenance planning, zero-margin plans fail the moment anything runs five minutes long.

**Question 11 (hard) — Deduction from monitoring rules**

Your team's alerting rules state: (i) if CPU usage exceeds 80% for 10 consecutive minutes, a warning alert fires; (ii) if memory usage exceeds 90% at any point, a critical alert fires immediately; (iii) a critical alert always pages the on-call engineer; (iv) warning alerts page the on-call engineer only outside working hours (working hours are 9:00–17:00). At 14:20, CPU has been at 85% since 14:05, and memory peaked at 92% at 14:12. Which pages has the on-call engineer received?

- A) None — it is working hours.
- B) One page, from the critical memory alert at 14:12.
- C) Two pages — one for CPU, one for memory.
- D) One page, from the CPU warning alert at 14:15.

**Correct answer: B**

**Explanation:** Evaluate each rule against the timeline. Memory: exceeded 90% at 14:12, so a critical alert fired immediately (rule ii), and criticals always page (rule iii) — one page at 14:12. CPU: above 80% since 14:05; ten consecutive minutes completes at 14:15, so a warning alert fired then (rule i). But rule (iv) says warnings page only outside working hours, and 14:15 is inside 9:00–17:00 — so the warning fired but did not page. Total pages: exactly one, from the memory critical. Option C misses the working-hours condition; option D misses that criticals always page; option A misses that the working-hours restriction applies only to warnings. Layered conditional rules like these are precisely how real alerting policies work, and being able to trace them accurately is core availability and capacity management: when you can explain *why* the on-call phone did or did not ring, you understand the alerting design rather than merely living with it.

**Question 12 (hard) — Evaluating a process change with evidence**

Your team's pipeline runs the full test suite (25 minutes) on every commit. A senior engineer proposes splitting it: a fast subset (5 minutes) on every commit, with the full suite running before merge and nightly. A fellow junior objects: "That means some bugs will be caught later than they are now." Evaluate the objection.

- A) The objection is wrong: the fast subset will catch every bug the full suite catches.
- B) The objection is technically true but incomplete: bugs caught only by the full suite surface at merge time or overnight rather than per-commit, yet developers get feedback on most changes 20 minutes sooner, which speeds up the whole loop — the trade-off can still be strongly favourable.
- C) The objection is decisive: any delay in catching any bug makes the proposal unacceptable.
- D) The objection is irrelevant because test timing does not affect development speed.

**Correct answer: B**

**Explanation:** Good evaluation separates what is true in an objection from what follows from it. It is true that a bug detectable only by the full suite now surfaces at merge or overnight instead of on the triggering commit — the objection identifies a real cost. But it is incomplete: it ignores the benefit side (every commit gets feedback in 5 minutes instead of 25, so developers iterate faster and integrate more often) and the mitigation already in the proposal (the full suite still runs before anything merges, so the protection at the merge boundary is unchanged). Option A overclaims — a subset by definition may miss things; option C treats any cost as a veto, which is not how engineering trade-offs work; option D denies an obvious link. The reasoning pattern — name the cost, name the benefit, check the mitigations, then judge the balance — is how development process improvements are actually argued, and practising it prepares you for the day you propose one yourself.

### Preparation tips

- **Practise on your team's real artefacts.** Ten minutes a day reading pipeline configurations, branch lists, alerting rules, and log extracts builds the pattern library that cognitive questions draw on. Familiarity with "normal" is what makes "abnormal" jump out.
- **Check boundaries deliberately.** For any rule or specification, ask what happens at exactly the threshold — at precisely 90%, at exactly 12:00. Boundary conditions decide more test questions (and cause more script bugs) than any other single feature.
- **Use elimination on constraint questions.** For scheduling and rule puzzles, testing each option against each constraint and crossing off failures is faster and more reliable than constructing the answer from scratch.
- **Trace data through systems step by step.** For integration questions, follow one message through every component, asking what each one assumes and does. This is also, not coincidentally, how you will debug real interfaces.
- **Narrate your reasoning when pairing.** When you work under supervision, say your logic out loud — "the error is X, so I'll check Y first". Your supervisor's corrections will tune exactly the deduction habits these tests measure.
- **Do timed practice last.** Accuracy first, speed second. Once your method is reliable, practise at roughly 90 seconds per question so the real test's tempo feels routine.

### Common pitfalls to avoid

- **Answering the expected question rather than the asked one.** Read the final sentence of the stem twice — "must be true", "most likely", and "how many violations" each demand different reasoning.
- **Importing your own team's conventions.** Test scenarios are self-contained. Answer from the rules given, even when your team does it differently.
- **Confusing eligibility with certainty.** "May be promoted tomorrow" does not mean "will be promoted tomorrow". Deduction questions punish upgrading possibilities into facts.
- **Glossing over quantifier and boundary words.** "Every", "only", "at least", "or above", "consecutive" — these small words carry the logic. Most wrong answers trace back to one skimmed word.
- **Sticking with a stuck approach.** If a hard question is going nowhere after two minutes, eliminate what you can, choose your best remaining option, and move on. One question is never worth three questions' time.
- **Panicking when difficulty rises.** Adaptive tests get harder as you succeed. A brutal question late in the test is usually evidence you are doing well — treat each question as a fresh start.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how confidently and accurately you handle the numbers your role genuinely produces. It is not a maths exam — no algebra, no geometry, nothing you have not met before. You will read small tables and charts and answer questions using percentages, ratios, averages, rates, and trend-spotting, all set in DevOps contexts: request error rates, build durations, disk growth, test coverage, ticket queues, and environment costs.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions. Each question presents a compact data set — a monitoring table, a chart of weekly deployments — and asks one specific thing about it. A basic on-screen calculator is usually provided and rough paper is almost always allowed; check your test's instructions. Scoring is objective and normed against people at a similar career stage, and platforms report accuracy alongside speed, so careful methodical work is rewarded.

Employers use numeric reasoning tests for DevOps roles because operations runs on numbers. Availability is a percentage; capacity is usage against a threshold; pipeline health is pass rates and durations; support work is queue lengths and response times. At junior level you are not expected to build capacity plans, but you are expected to read a dashboard correctly, compute a rate without help, notice when a metric is drifting, and sanity-check figures before repeating them — for example when helping fix a fault where "how often?" and "since when?" are the first questions. You also carry out maintenance on service support infrastructure, where windows, durations, and data volumes are all arithmetic. Every explanation in this section shows its working step by step so you can absorb the method, not just the answer, and reuse it at your desk.

### How this assessment maps to your role

The numeric skills in the test map directly to the named skills in your role summary:

- **Percentages and thresholds** map to **Availability and capacity management**: explaining availability and capacity processes means being fluent in uptime percentages, usage thresholds, and headroom calculations.
- **Averages and rates** map to **Programming and build (software engineering)** and **Service support**: build durations, script run times, fault arrival rates, and time-to-fix figures are the numbers you meet while coding under direction and helping fix faults by agreed procedures.
- **Ratios and proportions** map to **Modern development standards** and **Systems design**: test coverage proportions, the split of unit versus integration tests, and resource allocations across components are all ratio reasoning.
- **Reading tables and charts** maps to **Systems integration** and **Service support**: interface error tables and monitoring graphs are often the first evidence in an integration fault, and extracting the right number from the right cell is step one.
- **Trend interpretation** maps to **User focus**: quantitative data about users — traffic patterns, error rates experienced by real people — is one of the evidence types your user focus skill asks you to be aware of, and reading it correctly keeps the team honest about what users actually experience.

### Practice questions

**Question 1 (easy) — Reading a deployment table**

The team's deployment log shows deployments to the test environment: Monday 4, Tuesday 6, Wednesday 3, Thursday 7, Friday 5. What was the total number of deployments that week?

- A) 23
- B) 24
- C) 25
- D) 26

**Correct answer: C**

**Explanation:** Add step by step: 4 + 6 = 10; 10 + 3 = 13; 13 + 7 = 20; 20 + 5 = 25. Total: 25 deployments. A quicker regrouping: pair numbers into tens where possible — 4 + 6 = 10 and 3 + 7 = 10, leaving 5, giving 10 + 10 + 5 = 25 — and the regrouped route doubles as a check on the first. Totalling a simple table accurately is the foundation for every weekly report and stand-up statistic; answer questions like this quickly and correctly to bank time for the multi-step ones later. In real life, deployment counts feed conversations about batch size and release rhythm, so being the person whose numbers add up is a quiet credibility builder.

**Question 2 (easy) — Error rate as a percentage**

This morning a service handled 2,000 requests, of which 30 returned errors. What is the error rate as a percentage?

- A) 0.15%
- B) 1.5%
- C) 3%
- D) 15%

**Correct answer: B**

**Explanation:** Error rate = errors ÷ total × 100. Step 1: 30 ÷ 2,000 = 0.015. Step 2: 0.015 × 100 = 1.5%. A mental shortcut: 1% of 2,000 is 20, so 30 errors is one-and-a-half lots of 1%, which is 1.5%. The wrong options are all decimal-place slips of the same calculation — which is exactly how such errors happen at work, too. When a number will be repeated in a ticket or at stand-up ("error rate this morning was one and a half per cent"), a ten-second recheck of the decimal point is always worth it: 15% would be an emergency, 1.5% a concern, 0.15% barely a blip, and the difference between those three stories is just the placement of a dot.

**Question 3 (easy) — Average script runtime**

You have been testing a script you wrote and recorded five runs: 12 seconds, 15 seconds, 11 seconds, 18 seconds, 14 seconds. What is the mean runtime?

- A) 13 seconds
- B) 14 seconds
- C) 15 seconds
- D) 16 seconds

**Correct answer: B**

**Explanation:** Mean = total ÷ count. Step 1: total = 12 + 15 + 11 + 18 + 14. Add in stages: 12 + 15 = 27; 27 + 11 = 38; 38 + 18 = 56; 56 + 14 = 70 seconds. Step 2: 70 ÷ 5 = 14 seconds. Sense-check: the mean must lie between the minimum (11) and maximum (18), and 14 does. Documenting a typical runtime is part of documenting simple programs properly — a future teammate scheduling your script needs to know it takes "about 14 seconds", and if one day it takes 90, the recorded baseline is what makes the anomaly visible. Note also the spread: runs range from 11 to 18 seconds, so quoting "14 seconds, varying between roughly 11 and 18" is more honest than the bare average.

**Question 4 (easy) — Proportion of test types**

Your component's automated test suite contains 150 tests: 90 unit tests, 45 integration tests, and 15 end-to-end tests. What fraction of the suite is integration tests?

- A) 1/5
- B) 1/4
- C) 3/10
- D) 1/3

**Correct answer: C**

**Explanation:** Fraction = part ÷ whole = 45 ÷ 150. Simplify step by step: divide top and bottom by 5 to get 9/30, then by 3 to get 3/10. Check as a decimal: 45 ÷ 150 = 0.3, and 3/10 = 0.3 ✓. (Check the whole, too: 90 + 45 + 15 = 150 ✓.) The layered shape of this suite — many fast unit tests, fewer integration tests, a handful of end-to-end tests — is the classic "test pyramid" that modern development standards recommend, so this little fraction actually describes something real about healthy engineering. When a question offers close options like 1/4 (0.25) and 3/10 (0.3), convert to decimals and match precisely rather than judging by eye.

**Question 5 (moderate) — Availability from downtime**

A service you help support is expected to run 24 hours a day. Over a 28-day reporting period it had two outages: one of 3 hours and one of 45 minutes. What was its availability percentage, to one decimal place?

- A) 99.1%
- B) 99.4%
- C) 99.6%
- D) 99.8%

**Correct answer: B**

**Explanation:** Step 1: total period = 28 × 24 = 672 hours. Step 2: total downtime = 3 hours + 45 minutes = 3.75 hours. Step 3: uptime = 672 − 3.75 = 668.25 hours. Step 4: availability = 668.25 ÷ 672 × 100. Compute the downtime share instead for ease: 3.75 ÷ 672 = 0.005580..., which is 0.558%; availability = 100 − 0.558 = 99.442%, rounding to 99.4%. Two habits matter here: convert minutes to decimal hours before mixing units (45 minutes = 0.75 hours — a very common slip is typing 45 into an hours calculation), and round only at the end. Availability arithmetic like this is the literal content of the availability management processes you are learning to explain, and knowing that roughly 0.5% of a four-week month is about three and a half hours gives you an instant feel for what any availability figure really means.

**Question 6 (moderate) — Ratio of environment resources**

A component you are helping design will run across the test and staging environments with instances allocated in the ratio 3:2 (test:staging). The team has agreed to run 20 instances in total. How many instances run in staging?

- A) 6
- B) 8
- C) 10
- D) 12

**Correct answer: B**

**Explanation:** A ratio of 3:2 divides the total into 3 + 2 = 5 equal parts. Step 1: one part = 20 ÷ 5 = 4 instances. Step 2: staging = 2 parts = 2 × 4 = 8 instances. Check: test = 3 × 4 = 12, and 12 + 8 = 20 ✓. The universal ratio method — total the parts, size one part, multiply — works for every ratio question, and the add-back check catches slips in seconds. Watch the direction trap: option D (12) is the *test* figure, and ratio questions love to ask for the second-named quantity while your eye computes the first-named one. Reread which side of the ratio was asked for before answering — in tests, and equally in real capacity discussions where "3:2" gets quoted across a noisy stand-up.

**Question 7 (moderate) — Percentage change in queue length**

The support ticket backlog was 64 tickets at the start of the month and 48 tickets at the end. By what percentage did the backlog fall?

- A) 16%
- B) 20%
- C) 25%
- D) 33%

**Correct answer: C**

**Explanation:** Percentage change = (change ÷ original) × 100. Step 1: change = 64 − 48 = 16 tickets. Step 2: divide by the *original* value: 16 ÷ 64 = 0.25. Step 3: 0.25 × 100 = 25%. The classic error is dividing by the final value: 16 ÷ 48 = 33% (option D, sitting there waiting). Remember: percentage change is always measured from where you started. Option A repeats the raw change (16) dressed as a percentage — another standard trap. A useful cross-check: a 25% fall from 64 means losing a quarter of 64, which is 16, landing on 48 ✓. Backlog trends like this appear in every service support review, and quoting the change correctly ("down a quarter this month") is the kind of small numeracy that makes your updates trusted.

**Question 8 (moderate) — Reading a two-way integration table**

A weekly report shows message failures at two interfaces, by cause:

| Interface | Format errors | Timeout errors |
|---|---|---|
| Payments → Ledger | 12 | 28 |
| Booking → Notifications | 18 | 22 |

What percentage of all recorded failures were format errors?

- A) 30%
- B) 35%
- C) 37.5%
- D) 40%

**Correct answer: C**

**Explanation:** Step 1: total format errors = 12 + 18 = 30. Step 2: total timeout errors = 28 + 22 = 50. Step 3: grand total = 30 + 50 = 80 failures. Step 4: format share = 30 ÷ 80 × 100. Compute: 30 ÷ 80 = 0.375, so 37.5%. Always ask "out of what?" before dividing — the question asks about *all* failures across *both* interfaces, so the base is 80, not one row's total (12 ÷ 40 = 30% and 18 ÷ 40 = 45% are the per-interface figures a hurried reader computes instead). Two-way tables reward one disciplined habit: total the rows and columns first, then answer from the totals the question actually needs. As a bonus, notice what the numbers say about the systems: both interfaces fail more by timeout than by format, which would sensibly steer the team's next investigation — reading a table well and drawing the operational hint from it is exactly the skill your systems integration duties are building.

**Question 9 (moderate) — Backup window and data growth**

A nightly maintenance job backs up a data store at a steady 6 GB per minute, inside a fixed 60-minute window. The store currently holds 288 GB and grows by 12 GB per week. In how many weeks will the backup no longer fit inside the window?

- A) 4 weeks
- B) 6 weeks
- C) 8 weeks
- D) 12 weeks

**Correct answer: B**

**Explanation:** Step 1: the window's capacity = 6 GB/min × 60 min = 360 GB — the largest store the job can back up in time. Step 2: headroom = 360 − 288 = 72 GB. Step 3: weeks until the headroom is consumed = 72 ÷ 12 = 6 weeks. So from week 7 the backup overruns its window. The three-step pattern — convert the constraint into the same units as the data (a 60-minute window *is* 360 GB at this rate), find the gap, divide by the growth rate — solves every "when will it stop fitting?" question, and such questions are the arithmetic heart of capacity management. In practice you would report this as: "backups fit for about six more weeks at current growth; we should act before then" — a forecast plus a recommendation, which is precisely how juniors turn arithmetic into useful contributions during maintenance planning.

**Question 10 (hard) — Comparing failure rates fairly**

Two interfaces ran last month. Interface X processed 12,000 messages and had 180 failures. Interface Y processed 4,000 messages and had 100 failures. A teammate says: "X is the problem interface — it had nearly twice the failures." Which statement is accurate?

- A) The teammate is right: 180 failures is worse than 100.
- B) X's failure rate is 1.5% and Y's is 2.5%, so Y fails proportionally more often, despite fewer total failures.
- C) Both interfaces have the same failure rate.
- D) The rates cannot be compared because the interfaces carry different message types.

**Correct answer: B**

**Explanation:** Different volumes make raw counts misleading, so convert to rates. Interface X: 180 ÷ 12,000 = 0.015 = 1.5%. (Check: 1% of 12,000 is 120, so 180 is 1.5 lots of 1% ✓.) Interface Y: 100 ÷ 4,000 = 0.025 = 2.5%. (Check: 1% of 4,000 is 40, and 100 = 2.5 × 40 ✓.) Y fails one message in forty; X one in about 67. The teammate compared totals, not rates — the most common analytical slip in operational discussions. Option D manufactures an excuse for not comparing: message-type differences might explain *why* rates differ, but they do not prevent computing them. The transferable rule: whenever two things differ in volume — interfaces, environments, weeks — divide before comparing. Offering, kindly, "shall we check the rates?" is a high-value junior contribution to any dashboard conversation, and it is exactly the quantitative habit your user focus skill asks for when judging what users actually experience.

**Question 11 (hard) — Weighted average response time**

A service's response times were measured across three periods yesterday: morning (200 requests, average 120 ms), afternoon (600 requests, average 180 ms), and evening (200 requests, average 150 ms). What was the overall average response time across the whole day?

- A) 150 ms
- B) 156 ms
- C) 160 ms
- D) 162 ms

**Correct answer: D**

**Explanation:** You cannot simply average the three averages (120 + 180 + 150) ÷ 3 = 150 ms — option A, the trap — because the periods carry different numbers of requests. Weight each average by its request count. Step 1: total time = (200 × 120) + (600 × 180) + (200 × 150) = 24,000 + 108,000 + 30,000 = 162,000 ms. Step 2: total requests = 200 + 600 + 200 = 1,000. Step 3: overall average = 162,000 ÷ 1,000 = 162 ms. The busy afternoon, with three times the traffic, pulls the true average up towards its 180 ms. Sense-check: the answer must sit between the extremes (120 and 180) and closer to the heavily weighted one ✓. Unweighted averages of averages quietly misreport performance dashboards everywhere; knowing when weighting matters — whenever group sizes differ — is one of the most practically valuable numeric skills a junior engineer can bring to monitoring discussions.

**Question 12 (hard) — Multi-step environment cost comparison**

Your team is choosing between two configurations for a new test environment over a 30-day month. Configuration P: 8 virtual machines at £0.40 per hour each, running 24 hours a day. Configuration Q: 12 virtual machines at £0.40 per hour each, running only 10 hours per day on the 22 working days of the month. How much cheaper is the cheaper configuration for the month?

- A) £1,190.40
- B) £1,248.00
- C) £1,305.60
- D) £1,382.40

**Correct answer: B**

**Explanation:** Cost each configuration fully, then subtract. Configuration P: hours per machine = 30 × 24 = 720; machine-hours = 720 × 8 = 5,760; cost = 5,760 × £0.40 = £2,304. Configuration Q: hours per machine = 22 × 10 = 220; machine-hours = 220 × 12 = 2,640; cost = 2,640 × £0.40 = £1,056. Q is cheaper; the difference = £2,304 − £1,056 = £1,248, matching option B exactly. Verify by a second route: the machine-hour gap is 5,760 − 2,640 = 3,120, and 3,120 × £0.40 = £1,248 ✓. Two independent routes agreeing is the gold standard for multi-step money arithmetic. One final habit completes the job: after a long calculation, slow down for five seconds and match your figure to the options character by character — the neighbouring options (£1,190.40, £1,305.60) exist precisely to catch a hasty final click after perfect arithmetic. Cost comparisons of exactly this shape underpin real environment decisions, where "more machines, fewer hours" frequently beats "always on", and a junior who can lay out the machine-hours clearly gives the team a solid basis for the choice.

### Preparation tips

- **Drill the core four methods.** Percentage = part ÷ whole × 100; percentage change = change ÷ original × 100; mean = total ÷ count (weighted by group size when groups differ); ratio = total the parts, size one part, multiply. These four cover nearly every question.
- **Say "out of what?" before every division.** Choosing the right base — the grand total, the original value, the correct row — decides more marks than the arithmetic itself.
- **Keep units consistent.** Convert minutes to decimal hours, GB to the same unit throughout, before calculating. Unit mix-ups are the top cause of confidently wrong answers.
- **Verify by a second route when steps stack up.** For multi-step questions, a different path to the same figure (as in the cost questions above) is the strongest check available under time pressure.
- **Practise on your team's real dashboards.** Compute this week's error rate, the month's availability, the backlog change. It doubles as genuine service support skill-building, and real data has the awkward numbers tests imitate.
- **Learn your calculator before the day.** If the test provides an on-screen calculator, spend your warm-up moments locating the buttons; fumbling costs more time than any single calculation.

### Common pitfalls to avoid

- **Averaging averages without weighting.** When group sizes differ, the unweighted average of averages is simply wrong. Multiply out totals first.
- **Dividing by the new value in change questions.** Percentage change is measured from the original. This single trap appears in almost every numeric test.
- **Comparing counts across different volumes.** Convert to rates first — 100 failures from 4,000 is worse than 180 from 12,000.
- **Unit slips.** 45 minutes is 0.75 hours, not 0.45; a 60-minute window at 6 GB/min is 360 GB. Write units next to numbers as you work.
- **Rounding mid-calculation.** Carry full precision to the final step, then round to the asked-for precision. Early rounding shifts answers just enough to hit the wrong option.
- **Losing the last-step match.** After computing correctly, match your figure to the options carefully — neighbouring options exist precisely to catch the hasty final click.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, interpret, and draw conclusions from written material of the kind your role actually produces: runbooks and agreed procedures, coding standards, user stories, incident reports, interface documentation, security guidance, and emails between teams.

The most common question style presents a short passage followed by statements, and for each statement you answer **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage does not give enough information either way). Other styles include choosing the best summary, identifying what an instruction requires in a specific case, and judging which sentence communicates most clearly. Tests usually run 15 to 25 minutes with 20 to 30 questions, scored objectively against a norm group at your level.

The golden rule throughout is: **answer only from the passage.** You may be confident that something is true at your workplace, but if the text does not say it, the answer is "cannot say". This discipline feels unnatural at first and becomes automatic with a little practice.

Employers test verbal reasoning for DevOps roles because the job arrives largely as text, and misreading text has operational consequences. At junior level you code from written specifications, fix faults by following agreed procedures whose branch-words ("if", "otherwise", "unless") must be traced exactly, apply standards documents that distinguish "must" from "should" deliberately, and read user stories whose acceptance criteria are the difference between done and not done. You also *write* text others depend on — commit messages, handover notes, script documentation — so the clear-writing judgement questions are as job-relevant as the comprehension ones. Precision in reading and writing is a safety skill in operational work, and this section strengthens both directions.

### How this assessment maps to your role

The verbal skills in the test map directly to the named skills in your role summary:

- **Comprehension of procedures** maps to **Service support**: helping fix service faults "following agreed procedures" is only as good as your reading of those procedures — the conditions, the order, and the escape hatches.
- **True/false/cannot-say discipline** maps to **Information security**: using information security practices means representing guidance exactly — neither inflating a recommendation into a ban nor softening a requirement into a suggestion.
- **Inference** maps to **Systems integration** and **Systems design**: interface documentation and design notes rarely spell out every consequence; connecting stated facts into their guaranteed implications ("if the component needs the new library, the build image must include it") is daily work.
- **Understanding user stories** maps to **User focus**: your role summary explicitly asks you to explain the purpose of user stories and the focus on user needs — and the reading skill behind that is extracting who, what, and why from a story and its acceptance criteria.
- **Clear-writing judgement** maps to **Programming and build (software engineering)** and **Prototyping**: documenting simple programs properly, and showing the value of prototypes to your team, both depend on writing that a busy reader understands first time.

### Practice questions

**Question 1 (easy) — True/false/cannot say from a procedure**

Passage: "The database maintenance procedure runs on the first Sunday of each month. During maintenance, the reporting service is unavailable, but the booking service continues to operate normally. Users of the reporting service are notified by email three days in advance."

Statement: "The booking service is unavailable during database maintenance."

- A) True
- B) False
- C) Cannot say
- D) True on Sundays only

**Correct answer: B**

**Explanation:** The passage states directly that "the booking service continues to operate normally" during maintenance. The statement claims the opposite, so the passage contradicts it: False. This is the cleanest kind of verbal question — the deciding sentence is right there — and the skill is simply locating it and matching carefully, noticing that the passage names two services and assigns them opposite fates. Option D invents a refinement the passage does not make. Speed matters on easy questions: find the sentence, confirm the contradiction, answer, and bank the time. The workplace parallel is exact: when someone asks "will bookings be affected by the maintenance?", the trustworthy answer comes from the sentence in the procedure, not from a general impression that maintenance affects everything.

**Question 2 (easy) — What does the standard require here?**

Passage (from the team's coding standards): "All scripts must log their start time, end time, and outcome. Scripts that modify data must additionally log the number of records affected. Read-only scripts are encouraged, but not required, to log the number of records read."

You have written a script that only reads records and produces a summary. According to the standards, which logging is required?

- A) Start time, end time, outcome, and records read
- B) Start time, end time, and outcome only
- C) Records read only
- D) No logging, because the script is read-only

**Correct answer: B**

**Explanation:** Sort the requirements by which scripts they bind. The first sentence binds *all* scripts: start time, end time, outcome — your script included. The second binds only scripts that *modify* data — yours does not, so "records affected" does not apply. The third addresses read-only scripts like yours, but with "encouraged, but not required" — an explicit non-requirement. So the required set is exactly the universal trio: option B. Option A upgrades encouragement into obligation, the mirror-image error to option D, which treats "read-only" as an exemption from everything. Standards documents are tiered like this on purpose, and applying the right tier to the right case is precisely what "apply modern development standards principles under guidance" means — including being able to tell a reviewer *why* your read-only script logs three things and not four.

**Question 3 (easy) — Reading a user story**

Passage (a user story from your team's backlog): "As a caseworker, I need the search results to show each applicant's reference number, so that I can quote it when phoning the applicant. Acceptance criteria: reference numbers appear on every result row; reference numbers can be copied to the clipboard; search speed is not made noticeably slower."

Which of the following best describes the *user need* this story serves?

- A) Caseworkers need faster search.
- B) Caseworkers need to quote reference numbers when phoning applicants.
- C) Applicants need to know their reference numbers.
- D) The team needs the clipboard feature to work.

**Correct answer: B**

**Explanation:** A user story has a standard anatomy: *who* (as a caseworker), *what* (search results showing reference numbers), and *why* (so that I can quote it when phoning the applicant). The user need is the *why* — option B. Option A picks up the speed criterion, but that is a constraint protecting existing behaviour, not the need driving the story. Option C names the wrong "who": the user in this story is the caseworker, not the applicant. Option D mistakes an acceptance criterion (a way of verifying the what) for the need itself. Being able to point at the need inside a story is exactly your user focus skill — "explain the purpose of user stories and the focus on user needs" — and it has practical bite: when implementation gets hard, the team trades away nice-to-haves, and knowing which part is the *need* tells you what must survive.

**Question 4 (easy) — Cannot-say discipline**

Passage: "The new deployment tool supports automatic rollback: if the health check fails within five minutes of a deployment, the previous version is restored without manual intervention. The feature is enabled by default in the test environment."

Statement: "The automatic rollback feature is enabled in the staging environment."

- A) True
- B) False
- C) Cannot say
- D) True, because rollback is enabled by default

**Correct answer: C**

**Explanation:** The passage tells you the feature exists, how it behaves, and that it is enabled by default *in the test environment*. About staging it says nothing at all. The statement about staging is therefore neither supported nor contradicted: cannot say. Option D shows the exact trap the question is built for — stretching "enabled by default in test" into a general claim about everywhere; the sentence's scope is explicitly limited, and defaults can differ per environment. Note the difference from Question 1: there, a sentence contradicted the statement (False); here, no sentence addresses it (Cannot say). Keeping that boundary sharp is the core skill. At work, the parallel is answering "is rollback on in staging?" with "the doc only says test — let me check staging's configuration" rather than a confident guess: the habit that prevents a whole family of deployment surprises.

**Question 5 (moderate) — Tracing branches in an agreed procedure**

Passage (fault-fixing procedure): "When the queue depth alert fires, first check the consumer service status. If the consumer is stopped, restart it and monitor for ten minutes; if the queue then drains, close the alert. If the consumer is running, or if the queue does not drain after restart, escalate to the platform team with the queue depth graph attached. Do not purge the queue unless the platform team instructs it."

The alert has fired. You checked the consumer: it was stopped. You restarted it and monitored for ten minutes; the queue has not drained. What does the procedure require next?

- A) Purge the queue to clear the backlog.
- B) Restart the consumer again and monitor for another ten minutes.
- C) Escalate to the platform team, attaching the queue depth graph.
- D) Close the alert, since the consumer is now running.

**Correct answer: C**

**Explanation:** Walk the branches with your actual facts. Consumer stopped → restart and monitor: done. Queue drains → close: *not* your case — the queue did not drain. The procedure's next clause covers you exactly: "if the queue does not drain after restart, escalate to the platform team with the queue depth graph attached". So option C, including the attachment — procedures that specify what to attach do so because the receiving team needs it. Option A violates an explicit prohibition ("do not purge... unless the platform team instructs it"). Option B invents a retry loop the procedure never offers. Option D closes on the wrong condition — the close trigger is the queue draining, not the consumer running. This is "helping fix service faults following agreed procedures" in its purest form: your judgement is exercised *inside* the procedure's branches, and the escalation clause is as binding as any other step.

**Question 6 (moderate) — Inference from interface documentation**

Passage: "The notifications API accepts requests only over the department's private network. Callers must present a valid service token, issued by the platform team, which expires after 90 days. Requests without a valid token receive a 401 response. The booking service calls the notifications API and last renewed its token in early January."

It is now mid-April of the same year. Which conclusion is best supported?

- A) The booking service's requests are currently receiving 401 responses.
- B) The booking service's token has expired or is about to expire, so if it has not been renewed since January, calls will start failing with 401 responses.
- C) The notifications API is unavailable.
- D) The platform team has failed to issue tokens on time.

**Correct answer: B**

**Explanation:** Chain the facts carefully. Tokens expire after 90 days; the last stated renewal was early January; early January plus 90 days lands in early April — before "mid-April" now. So *if no renewal has happened since*, the token has expired and, per the passage, requests receive 401s. But the passage only tells you the *last renewal the passage knows of*; a more recent renewal is possible. That is why B, with its conditional phrasing, is better supported than A, which asserts current failures as fact. C and D have no support at all — nothing suggests the API is down or the platform team at fault. This calibrated inference — computing the implication while flagging the assumption — is exactly the reasoning you need when describing challenges of interfaces between systems: expiring credentials are a classic integration failure mode, and the engineer who says "our token window closed last week unless someone renewed — let's check" finds the fault hours before the one who waits for certainty.

**Question 7 (moderate) — True/false/cannot say on security guidance**

Passage (from security guidance): "Secrets such as passwords, API keys, and tokens must never be committed to source code repositories. Teams must use the approved secrets management service. Where a secret is accidentally committed, it must be treated as compromised: rotate it immediately and notify the security team. Removing the secret from the repository history is required but is not sufficient on its own."

Statement: "If an accidentally committed secret is removed from the repository history quickly enough, rotation is unnecessary."

- A) True
- B) False
- C) Cannot say
- D) True, if the repository is private

**Correct answer: B**

**Explanation:** The passage anticipates precisely this hope and closes it: an accidentally committed secret "must be treated as compromised: rotate it immediately", and removal from history "is required but is not sufficient on its own". No speed qualifier is offered — the obligation to rotate applies regardless of how quickly the removal happens. The statement therefore contradicts the passage: False. Option D adds a private-repository exception that appears nowhere in the text (and the passage's logic — treat as compromised — admits no such carve-out). Notice the reading skill: the passage builds a rule *and* pre-refutes a tempting shortcut, and the question tests whether you caught the refutation. This mirrors real security practice, where "it was only there for a minute" is a well-known trap; using information security practices to protect solutions and services means knowing that rotation plus notification is the non-negotiable response.

**Question 8 (moderate) — Clear-writing judgement in a commit message**

Your team's standards ask for commit messages that let a reader understand a change without opening the diff. Which message best meets that bar for a small fix you made?

- A) "Fixed stuff."
- B) "Fix timeout in report script: increase API call timeout from 5s to 30s because the monthly export exceeds 5s on large datasets."
- C) "Various improvements and enhancements were implemented to address the previously observed issues."
- D) "Changed line 47."

**Correct answer: B**

**Explanation:** Judge each message by what a future reader — possibly you, six months on, mid-incident — can do with it. A says nothing. C uses many words to say nothing, its passive constructions ("were implemented") concealing every specific. D gives a location without a reason or an effect — the diff already shows line 47 changed; the message's job is the *why*. B delivers the full anatomy of a good message: what changed (timeout 5s → 30s), where (report script's API call), and crucially why (monthly export exceeds 5s on large datasets) — enough to understand the change, evaluate it, and revisit it if the timeout needs tuning again. The pattern — specific what, specific where, honest why — is the same one that makes script documentation and handover notes useful, and writing to it is part of documenting simple programs properly under your programming and build skill.

**Question 9 (moderate) — Scope and applicability of a policy**

Passage (from an environments policy): "This policy applies to all shared environments: test, staging, and live. Individual developer sandboxes are excluded. In shared environments, configuration changes must be made through the pipeline, not manually. Manual changes are permitted in sandboxes. During a declared major incident, the incident lead may authorise manual changes in any environment; such changes must be recorded and reconciled through the pipeline within 48 hours."

Statement: "A manual configuration change in staging is never permitted."

- A) True
- B) False
- C) Cannot say
- D) True, except in sandboxes

**Correct answer: B**

**Explanation:** Staging is a shared environment, so the default rule bans manual changes there — which makes the statement *look* true. But keep reading: during a declared major incident, the incident lead may authorise manual changes "in any environment", which includes staging. So there is a defined circumstance in which a manual staging change is permitted, and a statement containing "never" is contradicted by a single legitimate exception: False. Option D confuses the geography — sandboxes are outside the policy entirely, not an exception within staging. The reading lesson is about absolute words: "never", "always", "all" make statements fragile, and checking a "never" means hunting specifically for exception clauses before answering. The operational lesson is just as real: knowing the emergency route exists — authorised, recorded, reconciled within 48 hours — is part of understanding how disciplined teams bend without breaking during incidents.

**Question 10 (hard) — Inference across an incident report**

Passage (from an incident report): "At 15:40 the booking confirmation emails stopped sending. The notifications service was healthy, but its message queue showed messages arriving and failing repeatedly. Investigation found that the 14:55 booking service release had changed the date format in messages from `YYYY-MM-DD` to `DD/MM/YYYY`, which the notifications service could not parse. The release had passed all of the booking service's own tests. The fix was deployed at 17:10 and queued messages were reprocessed successfully. Action: add contract tests covering the message format between the two services."

Which statement is best supported by the report?

- A) The booking service's test suite was failing at release time.
- B) The booking service's tests did not check the message format contract with the notifications service, which is why the breaking change reached production.
- C) The notifications service caused the incident.
- D) Emails sent between 15:40 and 17:10 were permanently lost.

**Correct answer: B**

**Explanation:** Assemble the evidence: the release changed the message format; it "passed all of the booking service's own tests"; and the action item adds "contract tests covering the message format between the two services". A change that passed all tests yet broke the integration means the tests did not cover the thing that broke — exactly what the action item confirms by adding that coverage. Option A directly contradicts "passed all... tests". Option C blames the component that behaved consistently — the notifications service could not parse what it was never designed to parse; the change originated in the booking service. Option D is contradicted by "queued messages were reprocessed successfully": the emails were delayed, not lost — the queue did its job. This report is a compact lesson in your systems integration skill: interfaces fail at the *boundary*, each side's own tests can be green while the contract between them silently breaks, and contract tests exist precisely to catch that. Reading incident reports this closely is one of the fastest ways a junior learns how systems really behave.

**Question 11 (hard) — Should versus must in a standards extract**

Passage (from deployment standards): "Deployments to staging must be performed through the pipeline. Deployments should be scheduled outside the 11:00–14:00 peak testing window. A deployment during the peak window requires the testing coordinator's agreement. All deployments must be announced in the platform channel beforehand, whatever the time."

Which statement accurately reflects the standards?

- A) Deploying to staging at 12:00 is forbidden.
- B) Deploying to staging at 12:00 is permitted with the testing coordinator's agreement, and it must still go through the pipeline and be announced beforehand.
- C) Deployments outside the peak window need no announcement.
- D) The testing coordinator must agree to every staging deployment.

**Correct answer: B**

**Explanation:** Separate the modal verbs and their scopes. "Must be performed through the pipeline" — absolute, all staging deployments. "Should be scheduled outside 11:00–14:00" — a recommendation, not a ban, and the next sentence supplies the sanctioned route for exceptions: coordinator agreement. "Must be announced... whatever the time" — absolute, explicitly time-independent. So a 12:00 deployment is permitted with agreement (A wrong), the announcement requirement has no time exception (C wrong — "whatever the time" was written to kill exactly that reading), and the coordinator's agreement attaches only to peak-window deployments (D wrong). B assembles all three readings correctly. Standards documents choose "must" and "should" deliberately — the distinction runs through government service standards and RFC-style specifications alike — and reading them precisely is what lets you apply modern development standards under guidance without either inventing blockers or committing breaches.

**Question 12 (hard) — Evaluating an argument about prototyping**

Passage (from a team discussion): "We should prototype the new dashboard layout before building it properly. Last quarter we built the alerts page straight to production standard, and users found the layout confusing; reworking it cost three sprints. A rough prototype shown to five caseworkers would have surfaced the confusion in days. Prototyping the dashboard will likewise save us rework."

Which of the following, if true, would most weaken the argument?

- A) Prototyping tools have improved this year.
- B) The dashboard's layout is tightly constrained by an accessibility-approved departmental template, so its layout decisions — unlike the alerts page's free-form design — are already fixed and user-validated.
- C) Some caseworkers enjoyed giving feedback on the alerts page rework.
- D) The alerts page rework took three sprints rather than two.

**Correct answer: B**

**Explanation:** First expose the argument's skeleton: evidence — building the alerts page without prototyping led to costly layout rework; bridge — the dashboard is a similar case; conclusion — prototype the dashboard. The strongest attack undermines the bridge, and option B does exactly that: if the dashboard's layout is fixed by a template already validated with users, then the specific risk prototyping would mitigate — unvalidated layout choices — barely exists for this project, so the alerts-page lesson does not transfer. Option A mildly *supports* prototyping; C is irrelevant to effectiveness; D adjusts a detail of the evidence without touching the inference. Note what B does not do: it does not claim prototyping is generally useless — it breaks the analogy for this case only, which is how strong counterarguments usually work. This evaluation skill connects directly to your prototyping skill — understanding *when* to use a specific prototyping technique means being able to argue when it earns its cost and when it does not — and to showing the value of prototyping to your team with reasoning rather than ritual.

### Preparation tips

- **Read the passage twice: shape first, then detail.** The first pass gives you the structure; the second pass, driven by the statement you are judging, finds the deciding sentence. Most questions are decided by one sentence — your job is to locate it.
- **Circle the modal and absolute words.** "Must", "should", "may", "never", "all", "unless", "not sufficient on its own" — these carry the logic of workplace documents, and nearly every wrong answer glosses over one of them.
- **Practise the three-verdict discipline.** For any work document, write one statement it supports, one it contradicts, and one it does not address. A week of this makes True/False/Cannot-say instinctive.
- **Trace procedures with your finger.** For branch-heavy passages, follow the exact path your facts take through the if/otherwise structure before looking at the options. The options are written to reward exact tracing and punish gist.
- **Study your team's real documents as test material.** Agreed procedures, standards, user stories, and incident reports are precisely the genres tests imitate — and active reading of them is simultaneously genuine professional development for your service support and integration skills.
- **Add timing pressure only at the end.** Accuracy first; once reliable, practise at 45–60 seconds per statement so the real pace feels familiar rather than frantic.

### Common pitfalls to avoid

- **Importing workplace knowledge into the passage.** The scenario's world is complete as written. If the passage does not say staging has rollback enabled, you do not know it — however your real environments are configured.
- **Confusing False with Cannot say.** False requires a contradicting sentence; Cannot say means silence. Before answering False, point at the sentence that does the contradicting.
- **Missing the exception clause.** Statements with "never" or "always" are usually decided by an exception buried later in the passage. Hunt for it before agreeing with an absolute.
- **Upgrading recommendations into requirements.** "Should" and "encouraged" do not bind; "must" does. Standards questions turn on this line, and so does correctly applying real standards.
- **Answering the story instead of the statement.** After absorbing a vivid incident report, it is easy to judge statements against your mental movie rather than the text. Re-anchor on the exact words before each verdict.
- **Choosing the most professional-sounding option.** Wrong answers are often dressed in confident, polished language. Support in the passage — not tone — is the only criterion.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace dilemmas and asks you to judge the effectiveness of different responses. There are no calculations and no passages to dissect — each question describes a situation a junior DevOps engineer could genuinely meet and offers four possible actions. You may be asked to pick the **most effective** response, the **least effective** response, or occasionally to rank all four.

Typical format: 15 to 25 scenarios, usually untimed or generously timed (30 to 45 minutes), taken online. Your judgements are scored against those of experienced professionals and against the behaviours the organisation values — in UK government digital teams these include user focus, collaboration, honesty and ownership, sensible escalation, and inclusion. SJTs are not personality tests, and there is no trick: they measure whether you recognise what good professional behaviour looks like in context, at your level.

That last phrase matters, so let's make the junior-level shape explicit before you start. Strong junior responses usually involve: following agreed procedures and standards, even under friendly pressure; being honest immediately about mistakes, uncertainty, and slipping timescales; timeboxing struggle — trying properly yourself, then asking a well-formed question rather than sinking silently; raising risks and observations even though others are senior; and protecting shared environments by defaulting to the cautious option when an action is irreversible. Weak responses usually involve: improvising beyond your supervision on shared systems; staying quiet to avoid looking inexperienced; bypassing procedures to be quick or agreeable; and escalating either everything (avoiding ownership) or nothing (avoiding visibility). Notice that asking for help *after a genuine attempt* is a strength at your level, not a weakness — the skill being tested is judging when and how. Employers use SJTs precisely because this calibration — knowing what your role owes the team at your level — predicts success better than technical knowledge alone.

### How this assessment maps to your role

The behaviours the SJT measures map directly to your role summary:

- **Following agreed procedures under pressure** maps to **Service support**: helping fix faults "following agreed procedures" is tested by scenarios where speed, seniority, or friendliness tempt you to skip steps.
- **Working well under supervision** maps to your role level — you "work under supervision" and "assist in the building of a complex story" — so scenarios probe when to persist alone, when to ask, and how to ask well.
- **Security vigilance** maps to **Information security**: using security practices to contribute to protecting services means scenarios about credentials in the wrong place, suspicious requests, and accidental exposure.
- **Collaboration and code review behaviour** maps to **Programming and build (software engineering)** and **Prototyping**: coding under the direction of others means receiving feedback constructively, giving observations respectfully, and showing the value of quick experiments to the team.
- **User focus in everyday choices** maps to **User focus**: scenarios reward remembering that behind tickets and stories are real users of public services, and that their needs — not team convenience — are the point.
- **Speaking up about design and integration risks** maps to **Systems design** and **Systems integration**: assisting in team design work means voicing what you notice, even when you are the least experienced person in the room.

### Practice questions

**Question 1 (easy) — Your merged change broke the test environment**

Yesterday you merged a small script change; it passed the pipeline. This morning you notice the test environment's data load job failing, and the log points clearly at your change — an edge case you had not considered. Nobody has said anything yet, and the team is busy preparing a demo. What is the most effective response?

- A) Quietly revert your change and say nothing, since the revert fixes it.
- B) Post in the team channel: your change broke the data load, you are reverting it now, and you will bring a fixed version back through review — flagging it before the demo in case anyone was relying on fresh data.
- C) Wait to see whether anyone else notices; the demo might not need the data load anyway.
- D) Start fixing the edge case immediately and merge the fix as fast as possible to cover the gap.

**Correct answer: B**

**Explanation:** Option B combines the three behaviours teams value most after a mistake: prompt honesty (the team hears it from you, before the demo, not from a failing job mid-demo), immediate mitigation (revert first — restore the shared environment, then fix at leisure), and process respect (the fix returns through review, because speed does not suspend standards). Option A does the right technical action while hiding the information others need — teammates may burn time investigating stale data, and quiet reverts erode the trust that makes supervision light-touch. Option C gambles the team's demo on hope. Option D inverts the correct order — while you perfect the fix, the environment stays broken — and "merge as fast as possible" is how one bug becomes two. The general pattern: restore first, disclose immediately, fix through the normal route. Mistakes are expected at junior level; the response is what is assessed.

**Question 2 (easy) — Stuck on a task: when to ask**

You are building your part of a complex story under supervision. You have been stuck on a configuration error for a while: you have re-read the documentation, searched the team wiki, and tried two plausible fixes. It is now nearly two hours, and your next idea would involve changing settings you do not fully understand. Your supervisor is at their desk. What is the most effective response?

- A) Keep going alone — asking now would show you cannot work independently.
- B) Try the settings change; you can always undo it if it goes wrong.
- C) Ask your supervisor now, showing what you tried: the error, the docs you checked, the two fixes attempted and their results, and your untested next idea.
- D) Post the raw error message in the team channel with "anyone seen this?" and wait.

**Correct answer: C**

**Explanation:** This scenario tests the timebox-then-ask pattern that defines effective junior engineers. Option C is the model: you made a genuine, structured attempt (docs, wiki, two hypotheses), you are now at the boundary of your understanding, and your question is well-formed — showing your working lets your supervisor teach in two minutes what trial and error would take hours to find, and demonstrates exactly the independence option A worries about. Option A confuses independence with isolation; two hours is already a generous timebox, and the cost of silence now grows every minute. Option B is the genuinely dangerous one: changing settings you do not understand, reassured by "I can undo it", is how juniors discover that some changes do not undo cleanly — uncertainty plus shared configuration equals ask first. Option D is passive: vague broadcast questions with no context get slow, vague answers. Remember the shape: try properly, then ask promptly, and bring your working with you.

**Question 3 (easy) — A credential in the wrong place**

While reading an old page on the team wiki to help fix a fault, you find a plainly visible database password in the middle of a troubleshooting guide, added two years ago by someone who has since left. You are mid-task and the fault you are fixing is due today. What is the most effective response?

- A) Finish your fault fix first and mention the password at next week's team meeting.
- B) Delete the password from the page yourself and carry on — problem solved.
- C) Report it now to your supervisor or security channel — a quick message with the link — so the password can be rotated and the page cleaned up, then carry on with your fault fix.
- D) Ignore it; a two-year-old password has probably been changed already.

**Correct answer: C**

**Explanation:** Security findings are time-sensitive and belong with people who can act fully. Option C does everything right at the right cost: reporting takes one minute (so your due-today fault fix barely pauses), it reaches people who can do what you cannot — rotate the credential and check whether it was misused — and it treats the find as the team-level issue it is. Option B fixes the visible symptom but not the exposure: the password has been readable for two years and lives on in page history; without rotation, deletion is cosmetic reassurance. Option D gambles on "probably" — long-lived service credentials are notoriously durable, which is precisely why they leak. Option A leaves a live credential exposed for another week for no benefit. The transferable rule from your information security skill: when you find exposed secrets, report fast, let owners rotate, and never assume age equals safety. Contributing to protecting services often looks exactly like this — noticing, and routing promptly.

**Question 4 (easy) — Receiving blunt code review feedback**

A senior engineer has reviewed the script you wrote for the sprint. The feedback is terse: "Wrong approach. Don't parse this manually — use the standard library. Also breaks on empty input. Rework." You feel deflated; you spent two days on it. What is the most effective response?

- A) Rework it as instructed without replying — seniors know best.
- B) Reply thanking them for the catch on empty input, ask which standard library module they would recommend, rework it, and add a test for the empty-input case.
- C) Defend your approach in the review thread — manual parsing gives you more control, and the empty-input case is unlikely.
- D) Ask your supervisor to assign future reviews to a friendlier reviewer.

**Correct answer: B**

**Explanation:** Separate the feedback's content from its tone: the content is a gift — a genuine bug (empty input) and a pointer to a better approach — and option B extracts full value from it: acknowledging the bug, asking a precise follow-up that turns the reviewer into a teacher, and adding a test so the bug stays fixed. That test-adding instinct is what distinguishes "patched it" from "learned from it". Option A complies but wastes the learning: without asking *which* module and *why*, you will make a sibling mistake next sprint. Option C defends two days of sunk cost rather than the codebase — and "unlikely" inputs are what production exists to deliver; coding under the direction of others means engaging with direction, not litigating it. Option D routes around discomfort instead of through it; if tone is a genuine pattern it may merit a separate conversation, but re-assigning reviewers to protect feelings costs you your best learning source. Blunt-but-correct review is a career constant: mine it.

**Question 5 (moderate) — Pressure to skip the agreed procedure**

A fault has taken the reporting service down in the test environment, blocking the testing team. You know the agreed procedure: restart via the pipeline job, which takes 20 minutes and logs everything. A developer standing at your desk says: "Just SSH in and restart the process directly — takes two minutes, I do it all the time." Your supervisor is at lunch. What is the most effective response?

- A) Do the direct restart — the testing team is blocked, and the developer is experienced.
- B) Start the pipeline restart now, tell the developer you would rather stay inside the procedure, and message your supervisor so they know the state of things — mentioning the "I do it all the time" comment only if it comes up again.
- C) Refuse to do anything until your supervisor returns.
- D) Do the direct restart, but write up afterwards exactly what you did.

**Correct answer: B**

**Explanation:** Run the arithmetic the pressure obscures: the procedure costs 18 extra minutes; an unlogged manual restart on shared infrastructure risks hours — untracked state, a masked underlying fault, an environment that no longer matches its configuration record. Option B holds the procedure with a light touch (starting the fix *now*, so the blocked testers are being served), gives the developer a respectful no, and keeps your supervisor informed without escalating a colleague's habits on the first occasion. Option A outsources your judgement to seniority — but the developer holds different responsibilities, and "I do it all the time" is a description of risk-taking, not a procedure. Option D at least preserves honesty, but documentation does not retroactively supply the pipeline's safeguards; it is the better wrong answer. Option C mistakes paralysis for prudence: you have an agreed procedure precisely so you can act without your supervisor. The pattern: act promptly *inside* the procedure, decline deviations kindly, and keep your supervisor in the loop.

**Question 6 (moderate) — You spot a risk in a design discussion**

You are the most junior person in a design session for a component your team is building. The proposed design has the component calling an external API synchronously on every user request. Last month you read that this API's response times spike during monthly reporting periods. Nobody has mentioned it, and the discussion is moving to the next topic. What is the most effective response?

- A) Say nothing — the seniors have presumably considered it, and you might be wrong.
- B) Say briefly: "One thing before we move on — I read that this API slows down badly during monthly reporting. If we call it synchronously on every request, would our users feel those spikes? Should we consider caching or an async pattern?"
- C) Stay quiet in the meeting but raise it privately with your supervisor afterwards.
- D) Interrupt with: "This design won't work — that API is too slow."

**Correct answer: B**

**Explanation:** Your role summary says you assist "as part of a team in the design of components of larger systems" — and this is what that assistance looks like at its best. Option B raises the observation at the moment it can still shape the decision, states its evidence and mechanism (spikes + synchronous calls = users feel them), frames it as a question rather than a verdict, and even offers constructive directions without overreaching. If the seniors have already handled it, you lose thirty seconds and gain the explanation; if not, you have prevented a genuine user-facing problem — that is user focus applied to design. Option A's "presumably considered" is the assumption behind many shipped defects; fresh eyes exist to be used. Option C is better than silence, but the design will have moved on — timing is much of the value. Option D has the right concern and the wrong form: a verdict without evidence, phrased to trigger defence rather than thought. Speak early, speak specifically, speak as a question.

**Question 7 (moderate) — The story is going to be late**

You are building your part of a complex story, due at Thursday's sprint review. On Tuesday afternoon you realise the remaining work is at least two days beyond your estimate — an interface turned out far fiddlier than expected. Your supervisor is optimistic in stand-ups and has not asked for detail. What is the most effective response?

- A) Work late without telling anyone and hope to close the gap by Thursday.
- B) Say nothing until Thursday, then explain the interface complexity at the review.
- C) Tell your supervisor now: what is done, what remains, why the interface cost more than estimated, and your realistic completion date — asking whether to reduce scope, get help, or move the review item.
- D) Quietly cut the fiddly interface handling to hit the date, and raise a follow-up ticket later.

**Correct answer: C**

**Explanation:** Schedule risk is information, and information ages badly. Option C delivers it while it is still actionable: on Tuesday, your supervisor has options — descope, pair you with someone, reorder the sprint review — and your structured account (done, remaining, cause, realistic date) turns a confession into a planning conversation. Crucially, at your level *deciding the response* to the slip is planning work that belongs to your supervisor; *reporting it early and clearly* is precisely your job. Option A bets the sprint on heroics and, win or lose, teaches your estimates to stay silent. Option B ambushes the team when options have run out. Option D is the most subtly harmful: silently descoping means the team believes something works that does not — the "fiddly" interface handling is often exactly the part that matters — and follow-up tickets raised quietly have a way of never surfacing. The professional pattern: surface slips at the first credible signal, with facts and options, and let the planner plan.

**Question 8 (moderate) — A user-focus tension in a small decision**

You are fixing a fault in an error message shown by a citizen-facing form when a document upload fails. The agreed fix is minimal: stop the crash, keep the generic message "An error occurred." While testing, you realise the failure is nearly always caused by files over the size limit, and the message could easily say so — but changing message text is, strictly, beyond your ticket, and content changes are supposed to involve the content designer. What is the most effective response?

- A) Ship the minimal fix and move on — scope is scope.
- B) Change the message yourself to "Your file is too big. Upload a file under 10MB." — it obviously helps users.
- C) Ship the minimal fix now, and flag to your supervisor and the content designer that upload-size failures dominate this error, suggesting a clearer message as a fast follow-up.
- D) Hold the fix back until the message question is resolved, so users get the complete improvement at once.

**Correct answer: C**

**Explanation:** This scenario tests whether user focus survives contact with process — and whether you honour both. Option C does: users get the crash fix immediately; the genuine insight from your testing (size-limit failures dominate) reaches the people who own content decisions; and the improvement travels through the route that exists for good reason — content designers know how to phrase guidance accessibly and consistently (your invented "10MB" might not even be the real limit). Option A follows process but drops the insight on the floor: noticing what users actually struggle with, and passing the evidence on, is exactly the "use data about users to turn user focus into outcomes" behaviour your skill framework describes at higher levels — worth practising now. Option B has the right heart and the wrong method: well-meant freelance content changes on citizen-facing services bypass accessibility and accuracy checks. Option D holds a working fix hostage to a nice-to-have. The pattern: deliver your scope, surface your evidence, respect others' crafts.

**Question 9 (moderate) — Maintenance task meets an obstacle**

You are performing a routine monthly maintenance task on the log-collection infrastructure, following the runbook: stop the collector, archive old logs, clear the buffer directory, restart. Today, step three fails — the buffer directory contains unfamiliar files with recent timestamps that the runbook does not mention, and the clear command refuses to delete them. The collector is currently stopped. What is the most effective response?

- A) Force-delete the unfamiliar files — the runbook says to clear the directory, and clearing is what you are doing.
- B) Restart the collector (returning the system to a safe, running state), then report the unfamiliar files to your supervisor with names and timestamps, and pause the maintenance until someone confirms what they are.
- C) Leave the collector stopped while you research what the files might be.
- D) Skip step three entirely, restart the collector, and mark the maintenance complete.

**Correct answer: B**

**Explanation:** When a procedure meets conditions it does not describe, the procedure has ended and judgement begins — and junior-level judgement means: make the system safe, then escalate with specifics. Option B does both: restarting the collector ends the outage-in-progress (a stopped collector is quietly losing logs), and the report — names, timestamps, what the runbook expected — gives your supervisor exactly what they need to identify the files, which could be anything from a new component's data to something genuinely wrong. Option A applies force precisely where understanding has run out; "the runbook said clear" does not cover files the runbook's authors never anticipated, and recent timestamps mean something is actively using that directory. Option C leaves the system degraded while you research at junior speed — safety first, curiosity second. Option D restores safety but then falsifies the record: maintenance marked complete-but-not means next month's engineer inherits a mystery plus wrong documentation. Pattern: safe state, honest status, specific escalation.

**Question 10 (hard) — Credit and visibility**

In a design session last month, you suggested caching the external API's responses — the suggestion that shaped the final design. Today, at a show-and-tell with other teams, the senior engineer presenting describes the caching approach without mentioning where it came from. Afterwards, a teammate who was in the original session says to you privately, "That was your idea, you should say something." What is the most effective response?

- A) Say nothing to anyone and let it go entirely; ideas belong to the team.
- B) Mention it lightly to the senior engineer afterwards ("glad the caching idea worked out!"), record the contribution in your own development notes, and raise it with your supervisor only if unacknowledged contributions become a pattern.
- C) Email the show-and-tell attendees clarifying that the caching approach was your suggestion.
- D) Raise it at the next retrospective as a team-culture issue.

**Correct answer: B**

**Explanation:** Calibrate the response to the offence — which may not be an offence at all: presenters compress history, and most omissions are careless, not predatory. Option B fits: the light private comment gives the engineer a natural opening to acknowledge you (most will, and it plants the memory for next time); your development notes preserve the evidence that formally matters for your progression regardless of anyone's memory; and the escalation path is reserved for the pattern, which is the thing actually worth escalating. Option A sounds noble but quietly erases the record your own development reviews depend on — team spirit does not require self-erasure. Option C spends significant social capital correcting a footnote in front of strangers; the correction will be remembered longer than the idea. Option D inflates one ambiguous moment into a culture agenda item, putting the engineer on public trial. The durable pattern: address small slights lightly and directly, keep your own record, escalate patterns rather than incidents — and keep contributing ideas, because a reputation for good suggestions builds faster than any single credit.

**Question 11 (hard) — A suspicious request with a plausible wrapper**

You receive an email, apparently from a project manager in another directorate, asking you to add a new SSH public key ("attached") to the shared build server "for a contractor starting today — the platform team is swamped, and your supervisor said you could help". The email address looks plausible; the tone is friendly and slightly urgent. Your supervisor is in meetings all morning. What is the most effective response?

- A) Add the key — onboarding delays are a bad first impression for a contractor.
- B) Reply asking the sender to confirm they are genuine.
- C) Do not act on the email; verify through independent channels — message your supervisor directly and check with the platform team via their official channel — and report the email as suspicious if either fails to confirm it.
- D) Forward the email to a teammate who has done key additions before and let them decide.

**Correct answer: C**

**Explanation:** Inventory the red flags: an access-granting action (adding an SSH key *is* granting server access), urgency, flattery-adjacent pressure, an unverifiable authority claim ("your supervisor said"), a bypass of the normal owner ("platform team is swamped"), and an attachment you are asked to install. This is the anatomy of social engineering, and option C is the anatomy of the defence: never act on the requesting channel's say-so; verify through channels you already trust (your supervisor directly, the platform team's official route — never a reply, because attackers answer their own emails cheerfully); and report if verification fails, because security teams need to know an attempt is in progress — other juniors may have received the same email. Option A performs a permanent access grant on a shared build system on the strength of one email. Option B asks the possible attacker to vouch for themselves. Option D relocates the decision without adding any verification — your teammate has the same email and less context. Verify independently, act only under confirmed direction, report the suspicious: that trio is your information security skill in executable form.

**Question 12 (hard) — Least effective: the flaky test**

Your team's pipeline has one test that fails intermittently — roughly one run in five — always in the same suite, apparently at random. Reruns usually pass. It has been like this for two weeks, and people have started habitually clicking "re-run" without looking. You have just been bitten by it again on an urgent change. Which response would be **least effective**?

- A) Raise a ticket describing the flakiness with dates, frequency, and links to failing runs, and mention it at stand-up so it gets prioritised.
- B) Ask your supervisor for time to investigate, and try to reproduce the failure locally to narrow the cause.
- C) Add a retry wrapper around the flaky test yourself and merge it quietly, so the pipeline stops bothering people.
- D) Propose at the retrospective that the team adopt a rule: flaky tests are fixed or quarantined within a sprint, because habitual re-running trains everyone to ignore red pipelines.

**Correct answer: C**

**Explanation:** Read the stem carefully — this asks for the *least* effective response, the SJT format that punishes skimming. Option C is the weakest: a quiet retry wrapper does not fix the flakiness, it institutionalises it — the test now "passes" while whatever race condition or environmental fault causes the failures continues undetected, and the masking was merged silently, so the team never even chose the trade-off. Intermittent failures are sometimes real defects showing themselves one run in five; muffling the smoke alarm because it keeps going off is the exact wrong relationship with signals. Every other option strengthens the situation: A converts private irritation into a visible, evidenced, prioritisable problem; B is the correct junior route to actually fixing it — sanctioned time plus systematic reproduction; D addresses the deeper damage (normalised red pipelines corrode the whole team's trust in its safety net) with a durable team rule. Notice the theme, which recurs across DevOps SJTs: responses that *surface and fix* problems outrank responses that *silence* them — especially silently.

### Preparation tips

- **Learn the behaviour patterns, not answers.** Strong junior responses combine: restore safety first, disclose early with specifics, hold procedures kindly under pressure, timebox struggle then ask well, verify before granting or acting, and route insights to their owners. Name the patterns and you will recognise them in any scenario.
- **Read the stem twice — and note "most" versus "least".** A significant share of SJT marks are lost to answering the opposite question.
- **Anchor on your level before judging options.** Ask: "What does an engineer who works under supervision, implements but does not plan, owe the team here?" Options ideal for a senior (deciding alone, directing others, absorbing risk) are often wrong for you — and options ideal for an apprentice (waiting passively for direction) are now too passive.
- **Judge each option by its full consequences.** The tempting wrong answers usually optimise one value (speed, kindness, loyalty, tidiness) at hidden cost to another (safety, honesty, the record). Trace what each option leaves behind a week later.
- **Collect real examples from your team.** When a colleague handles something well — a graceful "no" to a procedure bypass, a crisp early warning about a slipping story — write down what made it work. Your team is a living answer key, and studying it is professional development in itself.
- **Trust your considered first reading.** SJTs measure practical judgement, not puzzle-solving. Change an answer only when you have genuinely misread the situation, not because a second option starts to shimmer.

### Common pitfalls to avoid

- **Silence as a strategy.** The most heavily penalised junior behaviours are variations of saying nothing: hiding a mistake, sitting on a slipping deadline, not raising a spotted risk, ignoring a found credential. Visibility is the junior superpower; SJTs reward it consistently.
- **Heroics as a strategy.** The second most penalised family: acting beyond supervision on shared systems — force-deleting mystery files, freelance SSH restarts, self-approved content changes, quiet retry wrappers. Boldness without understanding is not initiative.
- **Obeying seniority over procedure.** "An experienced person told me to" does not transfer their judgement or their accountability to you. Decline kindly, act inside the procedure, inform your supervisor.
- **Escalating at the wrong intensity.** All-team emails and retrospective tribunals for first offences; total silence for patterns. Match the response to the scale: light and direct first, formal channels for recurrence and risk.
- **Optimising the metric instead of the reality.** Marking incomplete maintenance complete, masking flaky tests, silently descoping — anything that makes the dashboard greener than the truth scores badly, because it is the behaviour that costs teams most.
- **Forgetting the user behind the ticket.** When options differ in how citizens experience the outcome — a clearer error message, a demo built on stale data — the user-facing consequence is part of the judgement, not an afterthought.

## Conclusion

Well done for working all the way through this guide — that persistence is itself one of the qualities that makes a good junior DevOps engineer, and you have just exercised it on several thousand words of deliberate practice.

Look back at what you have covered. In the cognitive section, you checked branch names and pipeline configurations against conventions, traced data through interface transformations, sequenced maintenance steps under dependency constraints, and evaluated a process change by weighing costs against benefits and mitigations. In the numeric section, you computed error rates and availability percentages, sized backup windows against data growth, compared failure rates fairly across different volumes, and learned why averaging averages misleads unless you weight by traffic. In the verbal section, you held the line on "cannot say", found the exception clauses that break "never" statements, traced your exact facts through a fault procedure's branches, and judged commit messages by what a future reader could do with them. And in the situational judgement section, you rehearsed the moments that shape early careers: owning a broken merge before the demo, asking for help with your working shown, declining a procedure bypass kindly, flagging schedule slips while options still exist, and spotting a social-engineering attempt dressed as onboarding urgency.

None of this was generic test technique. Every question was built from the skills in your role summary — programming and build, service support, systems design and integration, information security, modern development standards, prototyping, availability and capacity management, and user focus. That means the hours you spent here count twice: as assessment preparation, and as rehearsal for the decisions and checks of your actual working week.

Keep the momentum gently. Ten minutes with a real dashboard, computing this week's error rate; one agreed procedure read with full branch-tracing attention; one commit message written to the what-where-why standard; one well-formed question asked after a proper attempt — these small repetitions are how the skills in this guide become habits. And carry the situational judgement patterns into real situations, because judgement grows only through use.

On assessment day: sleep properly, read every stem twice, keep units and bases straight, answer from the passage, and remember that at your level the tests measure carefulness, honesty, and clear thinking with what is in front of you — capacities you have been strengthening on every page here.

You are learning a profession that public services genuinely depend on, and you are learning it the right way: on the job, under good supervision, one component at a time. Good luck — you are better prepared than you think.
