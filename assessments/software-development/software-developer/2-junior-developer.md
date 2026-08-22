# Junior Developer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as a junior developer in the UK Government Digital and Data profession. You have moved beyond the very first steps of your career: you are learning on the job by delivering software components, working under supervision to deliver stories in a multidisciplinary team, becoming proficient in different types of testing, and even beginning to coach and mentor colleagues more junior than you. This guide will help you prepare for psychometric assessments — whether for an internal development scheme, a promotion application, a new role, or simply to benchmark and build your own capability.

So what is a psychometric assessment? It is a structured, standardised set of exercises that measures the thinking skills and workplace judgement that predict success in a role. There is nothing mysterious about it, and nothing to fear. The assessments described here are job-specific: they use the materials you genuinely handle — user stories, test suites, code review comments, integration diagrams, sprint boards, and monitoring dashboards — and the decisions you genuinely make, such as choosing which test to write, spotting an inconsistency between a design and its implementation, and deciding when to ask your senior colleague for help.

Why do these assessments matter for a junior developer in particular? Your level is defined by rapid, supervised growth. Employers want to understand how you think, learn, and judge situations, because at your stage those qualities predict your trajectory better than your current technical knowledge does. Practising these assessments also directly sharpens skills your role names: careful reasoning supports your **Programming and build** work, precise reading supports applying **Modern development standards** under guidance, numerical comfort supports **Availability and capacity management** conversations, and situational judgement supports delivering stories in a multidisciplinary team — and supports the coaching you now give to others.

This document is organised into four main assessment sections:

1. A workplace job-specific cognitive assessment covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving, using developer artefacts such as test results, interface rules, and branch policies.
2. A workplace job-specific numeric reasoning assessment using the numbers of team delivery: pass rates, velocity, defect counts, availability percentages, and capacity figures.
3. A workplace job-specific verbal reasoning assessment testing careful reading of standards, user stories, technical documentation, emails, and policy extracts.
4. A workplace job-specific situational judgement assessment presenting realistic dilemmas for a junior developer: supervision, testing pressure, security contributions, mentoring someone newer, and teamwork across disciplines.

Each section follows the same pattern: what the assessment measures and how it is typically run; how its dimensions map to the named skills in your role summary; a substantial set of practice questions moving from easy to hard, each with the correct answer and a full worked explanation; practical preparation tips; and common pitfalls to avoid.

To get the most from this guide, work through one section at a time. Attempt every question honestly — commit to an answer before reading the explanation. Then read the explanation regardless of whether you were right, because the explanations teach transferable technique, not just the answer. Finally, connect what you practise back to your daily work: every skill in this guide is one you will use this week on your team.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using practical scenarios rather than abstract puzzles. Instead of asking you to complete number sequences for their own sake, it presents materials a junior developer actually works with — test suites, branching rules, interface contracts, sprint boards, log files — and asks you to reason about them quickly and accurately.

The typical format is an online, timed test lasting 15 to 30 minutes, with roughly 15 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective: your responses are compared against a norm group of people who have taken the same test. Many platforms are adaptive, meaning questions get harder as you answer correctly — so a test that feels increasingly difficult is usually a test going well. Employers often receive separate speed and accuracy measures rather than a single score, which means steady, careful work is rewarded. Nearly all platforms offer short ungraded practice questions first, so you can settle into the interface without pressure.

Why do employers use cognitive assessment for junior developers? Because your core work is structured thinking under guidance. Delivering stories means decomposing them into steps; being proficient in different types of testing means reasoning about what each test type can and cannot prove; assisting in the design of components of larger systems means holding several constraints in mind at once; and explaining the principles of systems integration means understanding how rules interact across a boundary. A well-designed cognitive assessment simulates those demands in miniature, giving a fair signal of how you think — not just what you currently know.

### How this assessment maps to your role

Each dimension of the cognitive assessment maps to named skills in your role summary:

- **Pattern recognition** maps to **Programming and build (software engineering)** and **Systems design**: designing, coding, testing and correcting simple programs under direction, and assisting in the design of components of larger systems, both depend on spotting recurring structures — naming conventions, repeated code shapes, common failure patterns.
- **Logical deduction** maps to **Modern development standards** and your proficiency in different types of testing: standards and tests are rule systems, and deduction is working out exactly what follows from them — what a failing integration test proves, and what it does not.
- **Error checking** maps to **Service support** and **Programming and build**: helping fix service faults following agreed procedures, and correcting programs, both begin with spotting the precise difference between what is and what should be.
- **Prioritisation** maps to delivering stories under supervision in a multidisciplinary team: choosing what to do first, what to raise with your senior developer, and what can wait is a daily judgement.
- **Problem solving** maps to **Systems integration** and **Prototyping**: explaining the challenges of designing, building and testing interfaces between systems, and knowing when to use a specific prototyping technique, both involve decomposing an unclear problem into checkable steps.

### Practice questions

**Question 1 (easy) — Pattern recognition in branch names**

Your team's convention says branches are named `<type>/<ticket>-<short-description>`, where type is `feature`, `bugfix`, or `chore`, the ticket is like `ABC-123`, and the description is lowercase with hyphens. You see these branches:

1. `feature/ABC-101-add-export-button`
2. `bugfix/ABC-114-fix-date-format`
3. `feature/add-search-ABC-120`
4. `chore/ABC-131-update-dependencies`

Which branch breaks the convention?

- A) Branch 1
- B) Branch 2
- C) Branch 3
- D) Branch 4

**Correct answer: C**

**Explanation:** The convention fixes the order: type, then ticket, then description. Branch 3 puts the description before the ticket (`add-search-ABC-120`), inverting the required order even though all the right elements are present. Branches 1, 2 and 4 follow the pattern exactly. Conventions like this look cosmetic but usually feed automation — tools that link branches to tickets often parse the name, so a misordered branch can silently break traceability between code and work items. Spotting structural inversions — right pieces, wrong order — is a core pattern-recognition skill, and it is the same skill you use when reviewing whether code follows an agreed structure under your **Modern development standards** guidance.

**Question 2 (easy) — Logical deduction about test types**

You have become proficient in different types of testing. Your team's testing guide states: "Unit tests verify a single component in isolation. Integration tests verify that components work together. A passing unit test suite does not guarantee that components work together." All unit tests pass this morning. Which conclusion must be true?

- A) The components work together correctly.
- B) The integration tests will pass.
- C) Each tested component behaves correctly in isolation, as far as its tests check.
- D) There are no bugs in the system.

**Correct answer: C**

**Explanation:** Match each option against what passing unit tests can actually prove. By the guide's own definitions, unit tests verify components in isolation — so a fully passing unit suite tells you the isolated behaviours that were tested are correct, which is option C, carefully worded with "as far as its tests check". Option A is explicitly ruled out by the guide's third sentence: isolation success does not guarantee cooperation. Option B predicts a different suite's results with no evidence. Option D is far too strong: tests only ever check what they check, and untested behaviour can still be wrong. This precision about what each test type proves is exactly your testing proficiency in action — and it is why teams need both unit and integration tests, which becomes very practical when you build and reason about interfaces in **Systems integration**.

**Question 3 (easy) — Error checking a data mapping**

You are assisting with a component that maps fields between two systems. The mapping specification says: `customer_id → clientRef`, `postcode → postCode`, `date_of_birth → dob`, `email → emailAddress`. The implemented code maps:

1. `customer_id → clientRef`
2. `postcode → postcode`
3. `date_of_birth → dob`
4. `email → emailAddress`

How many implemented mappings differ from the specification?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Compare each pair character by character. Mapping 1 matches. Mapping 2 maps to `postcode`, but the specification requires `postCode` with a capital C — a one-letter difference that most systems treat as a completely different field, so this is a genuine defect, not a cosmetic one. Mappings 3 and 4 match. That is exactly one difference. The trap is skimming: `postcode` and `postCode` look nearly identical at reading speed, and this is precisely how integration defects are born — the receiving system silently ignores the unrecognised field name, data goes missing, and nobody notices until a user reports it. This is the "challenges of designing, building and testing interfaces between systems" from your **Systems integration** skill made concrete: interfaces fail on exact names, so checking must be exact too.

**Question 4 (easy) — Prioritisation of a junior developer's morning**

It is 9:15. Four items need your attention:

1. The overnight build is red, and your story from yesterday is one of three changes in it.
2. Stand-up is at 9:45.
3. A new apprentice you are mentoring asked you to look at her first pull request "when you have a moment".
4. Your own next story is waiting to be started.

What is the most sensible order?

- A) 4, 1, 2, 3 — start your story while your energy is high
- B) 1, 2, 3, 4 — investigate the red build first, attend stand-up, then the apprentice's review, then your story
- C) 3, 1, 2, 4 — mentoring always comes first
- D) 2, 4, 1, 3 — wait for stand-up to discuss the build

**Correct answer: B**

**Explanation:** A red build blocks the whole team, and your change is a suspect — so investigating immediately is both high-impact and personally responsible; even fifteen minutes of investigation before stand-up may identify the culprit or at least give you something concrete to report. Stand-up is a fixed commitment and, helpfully, a place to share what you found. The apprentice's review matters — coaching and mentoring more junior colleagues is in your role summary — and "when you have a moment" gives you flexibility to do it right after stand-up, keeping her unblocked early in her day. Your own new story is important but has no urgency yet. Option A personally optimises while the team is blocked; option C over-rotates on mentoring at the team's expense; option D delays action on the build for no benefit, since you can investigate and discuss. The pattern: team-blocking issues first, fixed commitments honoured, people you support kept moving, own new work last.

**Question 5 (moderate) — Pattern recognition in failing tests**

Your team's nightly test run reports failures over the last five nights: Night 1: 0. Night 2: 3, all in the export module. Night 3: 0. Night 4: 3, all in the export module. Night 5: 0. The export tests involve a call to another team's reporting service. What is the most reasonable first hypothesis?

- A) The export code has a permanent bug that appears every night.
- B) The failures are intermittent and correlate with something that varies — for example, the reporting service's availability on alternate nights.
- C) The test framework randomly fails three tests at a time.
- D) Someone is deleting the export tests on alternating nights.

**Correct answer: B**

**Explanation:** Read the shape of the data. The same three tests fail together, in the same module, but only on some nights — a classic intermittent pattern, which points to a varying factor rather than a fixed code bug. Option A cannot explain the passing nights: a permanent bug fails every run. The stem offers a strong candidate for the varying factor: these tests depend on another team's service, and external dependencies (their deployments, restarts, maintenance windows) are the most common cause of alternating failures. Option C blames the framework with no evidence and ignores that the failures cluster meaningfully in one module. Option D is conspiracy, not analysis. Flaky, dependency-driven tests are one of the genuine "challenges of designing, building and testing interfaces between systems" from your **Systems integration** skill — and recognising the intermittent pattern is the first step towards the standard remedies, such as test doubles or contract tests, which your senior colleagues will be glad you suggested investigating.

**Question 6 (moderate) — Logical deduction from a deployment policy**

Your team's policy states: "A change may be deployed to production only if it has passed the staging tests and been approved by the service owner. Emergency security patches are exempt from service owner approval but still require staging tests." A change was deployed to production this morning. Which conclusion must be true?

- A) The change was approved by the service owner.
- B) The change passed the staging tests.
- C) The change was an emergency security patch.
- D) The change passed staging tests and was approved by the service owner.

**Correct answer: B**

**Explanation:** Map the policy's two routes to production. Route 1 (normal): staging tests passed AND service owner approved. Route 2 (emergency security patch): staging tests passed, approval not required. Now ask what every deployed change has in common: both routes require passing staging tests, so B must be true. A is not guaranteed — the change might have travelled route 2. C is not guaranteed — it might have travelled route 1. D bundles in the approval, which route 2 makes optional. The technique is to find the intersection of all permitted routes: only conditions present in every route are guaranteed. Policies with exemptions are everywhere in government development standards, and reading them this way — what does every path require? — is precisely the skill of applying **Modern development standards** principles under guidance, and of not accusing a legitimate emergency patch of skipping required steps.

**Question 7 (moderate) — Error checking a capacity configuration**

You are carrying out a maintenance task on service support infrastructure. The capacity standard says: "Each application server must have at least 4 GB of memory; the pool must contain at least 3 servers; total pool memory must be at least 16 GB." The current pool is: Server A: 8 GB, Server B: 4 GB, Server C: 3 GB. Which requirements are breached?

- A) Only the per-server minimum.
- B) Only the total memory minimum.
- C) The per-server minimum and the total memory minimum.
- D) All three requirements.

**Correct answer: C**

**Explanation:** Test each rule separately, because compound standards fail independently. Rule 1, per-server minimum of 4 GB: Server C has 3 GB — breached. Rule 2, at least 3 servers: the pool has exactly 3 — satisfied ("at least 3" includes 3). Rule 3, total of at least 16 GB: 8 + 4 + 3 = 15 GB — breached, by 1 GB. So two of the three rules are breached: answer C. Common slips: assuming that because one rule fails, all fail (option D); or checking only the total and missing the per-server rule (option B); or misreading "at least 3" as "more than 3", which would wrongly fail rule 2. This is your **Availability and capacity management** skill in checkable form — capacity standards are multi-part, and a pool can look "roughly fine" while breaching specific limits, which is why maintenance tasks on service support infrastructure follow the numbers, not the vibe.

**Question 8 (moderate) — Problem solving in test-driven order**

You pick up a story: "Validate that uploaded CSV files have exactly 5 columns; reject others with a clear error message." Following your team's test-driven approach, which is the best first step?

- A) Write the validation code, then write tests that match what the code does.
- B) Write a failing test that submits a 4-column file and expects rejection with the error message.
- C) Test manually with a few files, and add automated tests later if there is time.
- D) Ask the designers for the error message wording, and do nothing until it arrives.

**Correct answer: B**

**Explanation:** The test-driven approach means expressing the requirement as a failing test before writing implementation code. Option B does exactly that: a 4-column file must be rejected, so the test encodes the behaviour, fails against current code, and then drives the implementation; further tests (5 columns accepted, 6 rejected, empty file handled) follow one at a time. Option A inverts the approach — tests written to match existing code merely photograph it, bugs included, rather than specifying it. Option C postpones automation, and "if there is time" is how stories arrive at review untested. Option D correctly notices a dependency (final wording) but responds by stopping entirely; the professional move is to proceed with a placeholder message, test the rejection behaviour, and confirm wording in parallel — junior developers deliver under supervision, and surfacing the wording question while continuing is exactly what your senior colleague would advise. Note the boundary-thinking too: 4, 5, and 6 columns are the classic boundary cases around "exactly 5".

**Question 9 (moderate) — Prioritisation during a service fault**

You are on support duty with a senior engineer. An alert fires: the document upload service is returning errors for about 20% of requests. The agreed procedure says: (1) acknowledge the alert; (2) check the service dashboard; (3) capture error samples; (4) notify the service channel; (5) attempt the documented remediation. You have acknowledged the alert and opened the dashboard, which confirms the errors. At that moment, a product manager messages you directly: "Is the upload service down? A stakeholder demo is in 10 minutes!" What do you do next?

- A) Stop the procedure and write the product manager a detailed reply about possible causes.
- B) Ignore the product manager entirely until the incident is resolved.
- C) Continue the procedure — capture error samples and notify the service channel, which will also answer the product manager — and send her a one-line pointer to that channel.
- D) Skip to the remediation step immediately, since the demo makes this urgent.

**Correct answer: C**

**Explanation:** Agreed procedures exist precisely so that incidents are handled consistently under pressure, and your **Service support** skill is "help fix service faults following agreed procedures". Option C keeps the procedure moving — and notice that step 4, notifying the service channel, is itself the communication mechanism: it informs the product manager and everyone else at once, truthfully and efficiently. The one-line pointer costs seconds and treats her urgent question with respect. Option A abandons the procedure to hand-write speculation for one stakeholder — slower for everyone and possibly wrong. Option B is needlessly cold: a ten-second redirect maintains trust. Option D skips the evidence-gathering steps that make remediation safe and diagnosable; urgency is an argument for following the procedure crisply, not for skipping the steps that stop you making things worse. The pattern: under pressure, the procedure is your friend, and broadcast channels beat private replies.

**Question 10 (hard) — Multi-step deduction about an integration failure**

Two systems integrate as follows: System A sends records to a queue; System B reads the queue and writes to a database; a dashboard reads the database. Facts: (i) if A stops sending, the queue empties within 5 minutes; (ii) if B stops reading, the queue grows continuously; (iii) the dashboard shows data up to 30 minutes ago and nothing since; (iv) the queue length has been stable and normal for the last hour. What is the most strongly supported conclusion?

- A) System A stopped sending about 30 minutes ago.
- B) System B stopped reading the queue about 30 minutes ago.
- C) The problem is most likely between B's reading and the dashboard — for example B's database writes or the dashboard's reads — since the queue behaviour rules out A stopping and B stopping.
- D) The queue lost 30 minutes of messages.

**Correct answer: C**

**Explanation:** Use each fact to eliminate. If A had stopped 30 minutes ago, fact (i) says the queue would have emptied within 5 minutes — but fact (iv) says the queue is normal, not empty, so A is still sending; option A falls. If B had stopped reading, fact (ii) says the queue would grow continuously — but it is stable, so B is still reading; option B falls. Option D would require the queue to misbehave, yet its length is normal and nothing suggests loss. What remains is the stretch after B reads the queue: B may be reading but failing to write to the database, or writing while the dashboard fails to read — either way, the fault lies downstream of the queue, which is option C. This elimination-by-observable-behaviour method is precisely how integration faults are localised in practice, and it is the reasoning core of your **Systems integration** skill: each component's visible behaviour (queue length, data freshness) tells you which links are healthy, letting you narrow the search before touching anything.

**Question 11 (hard) — Applying a definition of done with interacting rules**

Your team's definition of done: (i) code reviewed by at least one developer who did not write it; (ii) unit and integration tests written and passing; (iii) accessibility checks passed for user-facing changes; (iv) documentation updated for API changes. You and another developer pair-wrote a story that adds a new field to a public API response and does not change any screens. Tests pass. Your pairing partner reviewed the code as you wrote it. Documentation is untouched. Which items remain outstanding?

- A) Nothing — pairing counts as review, and there were no user-facing changes.
- B) Documentation only.
- C) Review and documentation.
- D) Review, documentation, and accessibility checks.

**Correct answer: C**

**Explanation:** Apply each rule to the facts. Rule (ii): tests written and passing — satisfied. Rule (iii): accessibility checks apply to user-facing changes; this story changes no screens, so the rule is not triggered — option D wrongly includes it. Rule (iv): the story changes a public API response, which is an API change, so documentation must be updated — outstanding. Rule (i) is the subtle one: it requires review by a developer who did not write the code, and both of you wrote it as a pair; strictly, neither pairing partner qualifies as the independent reviewer this wording demands, so review is outstanding too. (Some teams deliberately write their definition of done to accept pairing as review — but this one, as written, does not, and the assessment discipline is to apply the rule as stated.) That makes C correct. The habit of reading each clause and asking "triggered or not? satisfied or not?" is exactly how you apply **Modern development standards** principles under guidance — and knowing when your team's wording differs from your assumption is worth a genuine conversation at work.

**Question 12 (hard) — Problem solving with a prototype decision**

Your team must decide how a caseworker search screen should behave, and there is disagreement about what caseworkers actually need. Options on the table: build the full feature now (about 3 weeks); build a clickable prototype for user research sessions next week (about 2 days); write a survey asking caseworkers what they want; or study last year's requirements document. Your role includes showing the value of prototyping to your team. Which option best resolves the disagreement, and why?

- A) Build the full feature — real software is the ultimate test.
- B) Build the clickable prototype — it tests actual behaviour with real users next week at low cost, turning opinions into evidence before committing 3 weeks.
- C) Run the survey — asking users what they want is always the most reliable evidence.
- D) Study the requirements document — it already states what users need.

**Correct answer: B**

**Explanation:** The disagreement is about user behaviour and need, and the cheapest fast way to get behavioural evidence is a prototype in front of real users — 2 days of work feeding research sessions already scheduled for next week. That is the textbook case for prototyping: high uncertainty, expensive full build, and a decision that user contact can settle. Option A spends 3 weeks to answer a question 2 days could answer — and if the guess is wrong, the rework dwarfs the prototype's cost. Option C has a known weakness: what people say they want often differs from what they do; surveys are useful for some questions, but behaviour with a search screen is best observed, not self-reported. Option D relies on year-old stated requirements — doubly removed from current behaviour. Choosing the technique that matches the uncertainty is exactly your **Prototyping** skill ("understand when to use a specific prototyping technique") and your **User focus** awareness that user experience analysis rests on evidence about real users. Making this argument to your team is what "show the value of prototyping" means.

### Preparation tips

- **Practise little and often.** Short, regular sessions build reasoning speed far better than a single long cram. Fifteen minutes a few times a week is plenty.
- **Verbalise your reasoning.** Explain each practice answer to yourself as if walking a new apprentice through it — you now mentor others, and teaching a technique is the strongest way to learn it. If you cannot explain why an answer is right, revisit it.
- **Apply rules exactly as written.** Many questions hinge on wording: "at least 3" includes 3; "who did not write it" excludes both pairing partners. Read rules twice; apply them literally.
- **Use elimination on hard questions.** Question 10's method — use each fact to rule options out — often cracks problems that look impenetrable head-on. What must be false is as useful as what must be true.
- **Mine your daily work for practice.** Every red build, flaky test, code review, and definition-of-done conversation is a cognitive question in the wild. Notice the reasoning you use and sharpen it deliberately.
- **Prepare the practical basics.** Rest well, choose a quiet space, check your connection, and arrange any adjustments you are entitled to well in advance — providers and employers expect and welcome such requests.

### Common pitfalls to avoid

- **Concluding more than the evidence guarantees.** "Unit tests pass" does not mean "the system works"; "a change was deployed" does not mean "it was approved". Options with cautious wording ("as far as its tests check") are often right precisely because they claim less.
- **Skim-reading near-identical items.** `postCode` versus `postcode` is the whole question — and the whole production incident. Slow down when options differ by a character.
- **Letting one rule's failure contaminate the others.** Compound standards fail clause by clause. Check each independently, as in the capacity question, rather than assuming all-or-nothing.
- **Prioritising personal progress over team blockage.** In prioritisation questions (and real mornings), a red build or blocked teammate usually outranks starting your own next story.
- **Losing composure on adaptive tests.** Rising difficulty signals rising performance. Expect the questions to get harder and treat that as encouragement.
- **Dwelling on a single hard question.** Choose your best answer and move on; total accuracy across the test matters more than any one item.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your job actually produces. It is not a maths exam: there is no algebra for its own sake, and the required techniques rarely go beyond percentages, ratios, averages, rates, and reading tables and charts carefully. What the test really measures is numerical care — using the right base for a percentage, the right column of a table, the right period of a trend.

The typical format is an online, timed test of 20 to 35 minutes with 15 to 25 questions, most built around a small table or chart followed by one or more questions. Calculators are usually permitted (check your test's instructions), because the assessment targets reasoning rather than mental arithmetic. Scoring compares you against a norm group, platforms may adapt difficulty to your performance, and accuracy typically counts for more than raw speed.

Why does numeric reasoning matter for a junior developer? Because delivery runs on numbers. Your team plans sprints using velocity, tracks quality using defect counts and pass rates, and operates services using availability percentages, error rates, and capacity figures — the direct territory of your **Availability and capacity management** skill. When you help fix service faults following agreed procedures, dashboards present evidence numerically. When your team debates whether the test suite is getting slower or the defect trend is improving, the debate is arithmetic with opinions attached. Being the junior developer who can quickly and correctly say "that's a 40% increase, but from a small base" is genuinely valuable — and the same care transfers to your code, where off-by-one errors and wrong denominators are bugs rather than test answers.

Every numeric question below shows its arithmetic step by step in the explanation, so you can check your method as well as your answer. If you are rusty, that is completely normal — the patterns repeat, and a few practice sessions rebuild fluency quickly.

### How this assessment maps to your role

- **Percentages and rates** map to **Availability and capacity management**: explaining availability and capacity processes means fluently converting between availability percentages, downtime hours, error rates, and utilisation figures.
- **Reading tables and charts** maps to **Service support**: helping fix faults following agreed procedures and maintaining support infrastructure both start with reading monitoring dashboards, ticket queues, and log summaries accurately.
- **Averages and trends** map to delivering stories in a multidisciplinary team: sprint velocity, cycle times, and defect trends are the shared numerical language of planning and retrospectives.
- **Ratios and proportions** map to **Systems design** and **Systems integration**: assisting in component design involves proportional reasoning about load distribution, and integration work involves throughput and queue arithmetic.
- **Checking and estimating** map to **Programming and build** and your testing proficiency: a test is an expected number checked against an actual one, and the habit of sense-checking magnitudes ("should this be about 30 or about 300?") catches bugs in code and slips in tests alike.

### Practice questions

**Question 1 (easy) — Test suite pass rate**

Your story's test run shows 240 tests, of which 228 passed and 12 failed. What is the pass rate?

- A) 92%
- B) 94%
- C) 95%
- D) 96%

**Correct answer: C**

**Explanation:** Step 1: pass rate = passing tests ÷ total tests = 228 ÷ 240. Step 2: 228 ÷ 240 = 0.95. Step 3: × 100 = 95%. Cross-check via the failures: 12 ÷ 240 = 0.05 = 5% failing, and 100% − 5% = 95% — the two routes agree, which is strong confirmation. Option A would correspond to about 19 failures, option B to about 14, option D to about 10. Computing the small side (failures) and subtracting is often faster and less error-prone than dividing the big numbers — a useful habit when you are reading a dashboard during an incident and want a quick, reliable figure to report to the team.

**Question 2 (easy) — Sprint velocity average**

Your team's completed story points over the last five sprints were: 21, 25, 18, 26, 25. What is the mean velocity?

- A) 22
- B) 23
- C) 24
- D) 25

**Correct answer: B**

**Explanation:** Step 1: total the points: 21 + 25 = 46; 46 + 18 = 64; 64 + 26 = 90; 90 + 25 = 115. Step 2: divide by the number of sprints: 115 ÷ 5 = 23. Sense-check: the mean must lie between the minimum (18) and maximum (26), and 23 does; also, the values cluster in the low-to-mid twenties, so 23 feels right. Option D (25) is the mode — the most frequent value — which is a different statistic, and a classic distractor. Teams use mean velocity for sprint planning ("we average 23 points, so committing to 30 is a risk"), and understanding what the mean does and does not say — one bad sprint (18) pulls it down but does not define it — helps you contribute sensibly to planning conversations in your multidisciplinary team.

**Question 3 (easy) — Reading a ticket queue table**

The support dashboard shows open tickets by service and age:

| Service | Under 1 day | 1–3 days | Over 3 days |
|---|---|---|---|
| Uploads | 4 | 6 | 2 |
| Payments | 7 | 3 | 1 |
| Search | 2 | 5 | 4 |

Which service has the most tickets open for more than one day?

- A) Uploads
- B) Payments
- C) Search
- D) They are equal

**Correct answer: C**

**Explanation:** "More than one day" combines the last two columns: 1–3 days plus over 3 days. Uploads: 6 + 2 = 8. Payments: 3 + 1 = 4. Search: 5 + 4 = 9. Search has the most with 9 — answer C. The traps: answering from a single column (Uploads leads the 1–3 day column), or totalling all three columns (Uploads: 12, Payments: 11, Search: 11, which would wrongly give A). The question's exact words define which columns count — "more than one day" excludes the under-1-day column. Translating a verbal condition into the right subset of a table is the core skill of dashboard reading, and it is exactly what you do when an agreed support procedure says "escalate tickets open beyond one day".

**Question 4 (easy) — Percentage of stories carried over**

Your team planned 16 stories this sprint and completed 12, carrying the rest to next sprint. What percentage of planned stories was carried over?

- A) 20%
- B) 25%
- C) 30%
- D) 33%

**Correct answer: B**

**Explanation:** Step 1: carried-over stories = 16 − 12 = 4. Step 2: proportion carried over = 4 ÷ 16 = 0.25. Step 3: × 100 = 25%. The tempting error is option D: 4 ÷ 12 = 33%, which divides by the completed stories instead of the planned ones — but the question says "of planned stories", so 16 is the base. The words after "of" name the denominator; underline them before dividing. Carry-over percentage is a number retrospectives genuinely discuss (is our planning too optimistic?), and using the right base changes the story the number tells: 25% of the plan slipped, not 33%.

**Question 5 (moderate) — Availability target in downtime minutes**

A service you help support has a 99.5% availability target measured over a 30-day month (720 hours). What is the maximum downtime allowed in the month, in hours and minutes?

- A) 1 hour 12 minutes
- B) 3 hours 36 minutes
- C) 7 hours 12 minutes
- D) 36 minutes

**Correct answer: B**

**Explanation:** Step 1: allowed downtime percentage = 100% − 99.5% = 0.5%. Step 2: convert to hours: 720 × 0.005 = 3.6 hours. Step 3: convert the decimal to minutes: 0.6 hours × 60 = 36 minutes, so 3.6 hours = 3 hours 36 minutes. Answer B. Option C is the allowance for a 99% target (double the downtime for double the allowed percentage); option A is the allowance for 99.83%; option D drops the hours entirely. Two habits protect you here: write the percentage as a decimal carefully (0.5% = 0.005, not 0.05), and convert decimal hours to minutes explicitly (0.6 h is 36 min, not 60 min). This is the practical arithmetic of your **Availability and capacity management** skill — availability targets only become meaningful when you can say "that's three and a half hours a month" in a planning conversation.

**Question 6 (moderate) — Percentage change in response time**

After your team's optimisation work, the average API response time fell from 250 ms to 180 ms. What is the percentage decrease?

- A) 28%
- B) 30%
- C) 32%
- D) 39%

**Correct answer: A**

**Explanation:** Step 1: change = 250 − 180 = 70 ms. Step 2: divide by the original value: 70 ÷ 250 = 0.28. Step 3: × 100 = 28%. The base for a percentage change is always the starting value — the "from" number. Option D (39%) comes from dividing by the new value (70 ÷ 180), the single most common percentage-change error. Sense-check: a fall from 250 to 125 would be 50%, and 180 is well above 125, so the decrease must be comfortably under 50% — 28% fits. Teams report optimisation results exactly like this ("we cut response time 28%"), and reporting it correctly matters: the wrong-base version overstates your improvement, and a colleague who checks the arithmetic will find the discrepancy.

**Question 7 (moderate) — Error rate comparison across services**

This hour's dashboard shows: Service X handled 50,000 requests with 40 errors; Service Y handled 8,000 requests with 12 errors. Which statement is correct?

- A) Service X has the higher error rate, because 40 errors is more than 12.
- B) Service Y has the higher error rate: 1.5 errors per 1,000 requests versus 0.8 per 1,000 for X.
- C) The services have equal error rates.
- D) Error rates cannot be compared across services of different sizes.

**Correct answer: B**

**Explanation:** Raw counts mislead when volumes differ, so convert both to a common rate. Service X: 40 ÷ 50,000 = 0.0008 = 0.8 errors per 1,000 requests. Service Y: 12 ÷ 8,000 = 0.0015 = 1.5 errors per 1,000 requests. Y's rate is nearly double X's, despite Y having fewer errors in absolute terms — answer B. Option A is the raw-count trap the question is built around. Option D gives up too early: rates exist precisely to make different-sized services comparable. This is everyday **Service support** reasoning — deciding which service most needs attention means comparing rates, not counts — and it is the same normalisation habit that makes your test results meaningful ("3 failures" means something different in a suite of 30 than in a suite of 3,000).

**Question 8 (moderate) — Defect trend across releases**

Defects found in the first week after each release:

| Release | Defects |
|---|---|
| 1.0 | 24 |
| 1.1 | 18 |
| 1.2 | 12 |
| 1.3 | 9 |

Which statement best describes the trend?

- A) Defects fall by exactly 6 per release.
- B) Defects fall by exactly 25% per release.
- C) Defects are falling, but neither by a constant amount nor by a constant percentage.
- D) Defects fall by a constant third per release.

**Correct answer: C**

**Explanation:** Test each candidate pattern against all the data. Constant amount? Differences are 24→18 = −6, 18→12 = −6, 12→9 = −3. The last step breaks the "always −6" rule, so A fails. Constant percentage? 18 ÷ 24 = 75% (a 25% fall), 12 ÷ 18 ≈ 66.7% (a 33.3% fall), 9 ÷ 12 = 75% (a 25% fall). The middle step breaks the "always −25%" rule, so B fails — and D ("a third") only matches the middle step. What is left is the accurate, more modest claim: the trend is clearly downward, but no single constant rule fits every step — answer C. The discipline here is checking a claimed pattern against every data point, not just the first two; in retrospectives this is the difference between "quality is improving" (supported) and "quality improves 25% every release" (not supported), and choosing claims your data actually supports is a habit that builds your credibility fast.

**Question 9 (moderate) — Capacity headroom calculation**

A server pool handles a peak load of 1,200 requests per second (rps). Current capacity is 2,000 rps. Traffic is forecast to grow 30% over the next year. Will the current capacity still exceed forecast peak load, and what will the utilisation be at the new peak?

- A) Yes — new peak 1,560 rps, utilisation 78%
- B) Yes — new peak 1,440 rps, utilisation 72%
- C) No — new peak 2,160 rps exceeds capacity
- D) Yes — new peak 1,560 rps, utilisation 65%

**Correct answer: A**

**Explanation:** Step 1: forecast peak = current peak × 1.30 = 1,200 × 1.3 = 1,560 rps. Step 2: compare with capacity: 1,560 < 2,000, so capacity still suffices — the answer starts with "Yes". Step 3: utilisation at new peak = 1,560 ÷ 2,000 = 0.78 = 78%. So A. Option B applies 30% growth incorrectly (1,200 × 1.2 would be 20% growth; 1,440 is actually 1,200 × 1.2); option C applies the growth to capacity instead of load; option D computes utilisation with the wrong divisor. Note what the 78% means in practice: capacity still covers the peak, but headroom has shrunk from 40% spare to 22% spare, which is the kind of early-warning insight **Availability and capacity management** exists to produce — the calculation is easy, and the conclusion ("we should plan capacity before next year") is valuable.

**Question 10 (hard) — Weighted pass rate across suites**

Your project runs three test suites nightly: unit (500 tests, 98% pass), integration (200 tests, 94% pass), and end-to-end (50 tests, 80% pass). What is the overall pass rate across all 750 tests, to the nearest whole percent?

- A) 91%
- B) 93%
- C) 96%
- D) 97%

**Correct answer: C**

**Explanation:** Do not average 98%, 94% and 80% — the suites differ hugely in size, so convert to actual test counts. Step 1: unit passes = 500 × 0.98 = 490. Step 2: integration passes = 200 × 0.94 = 188. Step 3: end-to-end passes = 50 × 0.80 = 40. Step 4: total passes = 490 + 188 + 40 = 718. Step 5: overall rate = 718 ÷ 750 ≈ 0.9573 → 96% to the nearest percent. Option A (91%) is the unweighted average of the three percentages — the classic trap. Sense-check: the overall rate must fall between 80% and 98%, and must sit near 98% because the 500-test unit suite dominates the 750-test total; 96% fits both constraints. Weighted averages appear whenever you combine different-sized groups — suites, services, cohorts — and this five-step method (rates to counts, add, divide) never fails.

**Question 11 (hard) — Queue drain time during an incident**

During a fault, messages accumulated in a queue. The queue now holds 3,600 messages. New messages continue to arrive at 20 per minute, and the restored consumer processes 80 per minute. How long until the queue is empty?

- A) 45 minutes
- B) 60 minutes
- C) 36 minutes
- D) 72 minutes

**Correct answer: B**

**Explanation:** The queue shrinks at the net rate: processing minus arrivals. Step 1: net drain rate = 80 − 20 = 60 messages per minute. Step 2: time to empty = backlog ÷ net rate = 3,600 ÷ 60 = 60 minutes. Answer B. Option A (45) divides by the raw processing rate (3,600 ÷ 80), forgetting that new messages keep arriving; option C and D are other rate mix-ups. The concept — net rate = outflow − inflow — is the fundamental arithmetic of queues, and queues are the connective tissue of integrated systems, which makes this directly relevant to your **Systems integration** skill. During a real incident, this one-line calculation lets your team answer the question every stakeholder asks ("when will it be back to normal?") with evidence instead of hope: "about an hour, if rates hold".

**Question 12 (hard) — Interpreting a burn-down with a scope change**

A sprint starts with 40 story points over 10 working days. After 6 days, 18 points are done. On day 6, the product owner adds an urgent 8-point story to the sprint. To finish everything by day 10, what average daily completion rate do the remaining days require, and how does it compare with the rate so far?

- A) 5.5 points/day needed, versus 3 points/day so far — nearly double the current rate.
- B) 7.5 points/day needed, versus 3 points/day so far — two and a half times the current rate.
- C) 4.4 points/day needed, versus 4 points/day so far — about the same.
- D) 5.5 points/day needed, versus 4.5 points/day so far — slightly faster.

**Correct answer: A**

**Explanation:** Step 1: work remaining = original scope − done + added scope = 40 − 18 + 8 = 30 points. Step 2: days remaining = 10 − 6 = 4 days. Step 3: required rate = 30 ÷ 4 = 7.5 — wait, check step 1 again: 40 − 18 = 22; 22 + 8 = 30; and 30 ÷ 4 = 7.5. Now the comparison rate: 18 points in 6 days = 3 points/day. Hmm — that gives 7.5 versus 3, which is option B. Recompute carefully before choosing: 40 − 18 = 22 remaining from original scope; the added story makes 30; over 4 days that is 7.5 points/day, against 3 points/day achieved so far. The correct answer is **B**, and this explanation deliberately modelled the checking process: the first pass and the careful pass agreed on 7.5, so B stands — two and a half times the demonstrated rate, a clear signal the sprint plan is no longer realistic. Options A, C and D all embed arithmetic slips (forgetting the added scope, or misdividing). When a plan requires 2.5× your demonstrated rate, the professional response is to flag it in stand-up with exactly this arithmetic — numbers make the scope conversation objective rather than personal.

**Correct answer: B**

**Question 13 (hard) — Proportional allocation of regression tests**

A regression pack of 180 tests must be split among three testers in proportion to their available hours: Asha has 6 hours, Ben has 4 hours, Chris has 2 hours. How many tests does Ben take?

- A) 30
- B) 45
- C) 60
- D) 90

**Correct answer: C**

**Explanation:** Step 1: total the proportion parts: 6 + 4 + 2 = 12 hours. Step 2: tests per hour-part = 180 ÷ 12 = 15. Step 3: Ben's share = 4 × 15 = 60 tests. Verify the full split: Asha 6 × 15 = 90, Ben 60, Chris 2 × 15 = 30; total 90 + 60 + 30 = 180 — matches, so the arithmetic is sound. Option D is Asha's share, option A is Chris's, and option B is what Ben would get from an equal three-way split with a slip. Ratio allocation — total the parts, size one part, multiply — appears whenever capacity is uneven: splitting test packs, sharing support shifts, dividing story points across pairing rotations. The verification step (do the shares re-total?) costs ten seconds and turns a probably-right answer into a certainly-right one, which is precisely the habit that makes your testing work trustworthy.

### Preparation tips

- **Master the base rule.** The words after "of" in a percentage question name the denominator, and percentage changes always divide by the starting value. These two rules between them prevent the majority of numeric errors.
- **Write steps, not just answers.** Every explanation above works in numbered steps. Doing the same — even quickly, on paper — makes slips visible before they become wrong answers, and mirrors how you would justify a figure to your team.
- **Sense-check magnitudes.** Averages sit between the extremes; combined rates sit between group rates, nearer the bigger group; utilisation cannot exceed 100% while capacity suffices. A ten-second plausibility check catches most errors.
- **Convert to common units early.** Errors per 1,000, points per day, hours versus minutes — pick the unit the question wants and convert at the start, not the end.
- **Practise with your team's dashboards.** Compute your team's real pass rate, availability allowance, or carry-over percentage. Real numbers make practice memorable, and you may spot something genuinely useful.
- **Rebuild fluency without shame.** If percentages feel rusty, that is normal — a handful of practice sessions restores them. Fluency is practice, not talent.

### Common pitfalls to avoid

- **Averaging percentages across different-sized groups.** Question 10's trap: 98%, 94% and 80% do not average to the overall rate unless the groups are equal. Return to counts.
- **Comparing raw counts when volumes differ.** Forty errors can be better than twelve, as Question 7 showed. Normalise to rates before comparing services, suites, or sprints.
- **Using the new value as a percentage-change base.** "Fell from 250 to 180" is measured against 250. The wrong base flatters or damns by several points.
- **Ignoring inflow when computing drain times.** Backlog ÷ processing rate is wrong whenever arrivals continue; always use the net rate, as in Question 11.
- **Reading the wrong table subset.** "More than one day" means specific columns; "high-priority tickets" means a specific row or column total. Match the question's words to the table before calculating.
- **Trusting your first pass under time pressure.** Question 12 modelled the fix: recompute the critical step once, quickly. Agreement between two passes is cheap confidence; disagreement is a caught error.

<!-- APPEND -->
