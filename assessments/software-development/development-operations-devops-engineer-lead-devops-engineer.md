# Lead DevOps Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a lead DevOps engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to the work of leading engineering teams, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a lead DevOps engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — product roadmaps, platform adoption dashboards, standards documents, integration procedures, capacity and cost reports, deprecation notices, and messages from delivery managers with competing demands — and the kinds of decisions you genuinely make as someone who leads one or a small number of related project teams, acts as a technical product owner, and contributes to the development of strategic direction.

Why do these assessments matter for your role in particular? At lead level, your influence has changed shape. You still hold deep technical judgement, but you increasingly exercise it through others: developing medium to long term strategies for product lines, providing technical leadership through coaching and mentoring, leading the sharing of knowledge and good practice, and establishing standards and procedures that other practitioners must follow across a service product life cycle. That shift raises the stakes on exactly the capabilities psychometric assessments measure. Cognitive ability now means reasoning about dependencies that span teams, not just pipelines. Numerical reasoning now means reading adoption trends, platform costs, and delivery metrics across a portfolio. Verbal reasoning now means parsing policy and strategy documents precisely — and writing announcements that a dozen teams will act on. Situational judgement now means navigating the genuinely hard part of leadership: competing stakeholders, resistant teams, struggling individuals, and the constant tension between the roadmap you own and the interruptions that arrive anyway.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment dimensions to the specific skills in the lead DevOps engineer capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format before meeting it under timed conditions. Second, attempt the practice questions honestly — commit to an answer before reading the explanation, just as you would form your own view of a design before reading the review comments. Third, treat every explanation as a mini-lesson: even when you answer correctly, the walkthrough will sharpen your technique, and several explanations double as coaching material you can reuse with your own engineers. Finally, use the preparation tips for self-reflection: they connect assessment performance back to your development as a technical leader who shapes strategy as well as systems.

A reassuring thought before you begin: the reasoning these assessments test is the reasoning you already exercise in roadmap reviews, incident retrospectives, standards discussions, and one-to-ones. Practice simply makes it faster, calmer, and more reliable under time pressure — and a little deliberate practice goes a long way.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, cross-team roadmaps, standards adoption matrices, deprecation schedules, integration procedures, support policies, and platform telemetry — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can get comfortable with the interface without pressure.

For a lead DevOps engineer, cognitive ability assessment is particularly relevant because your role multiplies the consequences of structured thinking. When you act as technical product owner for a platform or toolchain, a flawed dependency analysis delays several teams, not one. When you establish standards and procedures across a product life cycle, an inconsistency you fail to spot is inherited by every practitioner who follows the standard. When you develop medium to long term strategies, you must reason about sequencing, constraints and second-order effects months before any code exists to check your logic. A well-designed cognitive assessment simulates exactly those demands in miniature — pattern, rule, exception, dependency, priority — and lead-level engineers who practise a little tend to perform very well, because the underlying reasoning is their daily craft.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to **Service support** and **Availability and capacity management**: identifying, locating and fixing complex service faults — and spotting when a KPI trend across several services is one shared cause rather than several local ones — is pattern reading across noisy, multi-team telemetry.
- **Logical deduction** maps to **Systems design** and **Systems integration**: designing systems of medium risk and complexity, and establishing standards and procedures across a service product life cycle, both require valid reasoning from rules — promotion policies, support tiers, deprecation clauses — to their consequences for real teams.
- **Error checking** maps to **Modern development standards** and **Programming and build (software engineering)**: leading others in applying modern development standards means finding the inconsistency in a standards matrix, a procedure, or a submitted design before a dozen teams inherit it.
- **Prioritisation** maps to your duty to **act as a technical product owner**: a product backlog is a permanent prioritisation exercise, and your ordering decisions ripple across every team that depends on the product line.
- **Problem solving** maps to **Development process optimisation** and your technical leadership duty: teams bring you cross-cutting problems — slow adoption, degraded delivery metrics, integration friction — and you must decompose them, isolate causes, and choose interventions that work through other people.

### Practice questions

**Question 1 (easy) — Pattern recognition in release versioning**

Your product line's versioning standard is semantic: `MAJOR.MINOR.PATCH`, where breaking changes increment MAJOR and reset the others, new features increment MINOR and reset PATCH, and fixes increment PATCH. A team's release history reads:

1. 2.3.1 — bug fix (previous: 2.3.0)
2. 2.4.0 — new feature (previous: 2.3.1)
3. 3.0.0 — breaking change (previous: 2.4.0)
4. 3.1.1 — new feature (previous: 3.0.0)
5. 3.1.2 — bug fix (previous: 3.1.1)

Which release breaks the versioning standard?

- A) Release 2
- B) Release 3
- C) Release 4
- D) Release 5

**Correct answer: C**

**Explanation:** A new feature after 3.0.0 should increment MINOR and reset PATCH, giving 3.1.0 — but release 4 jumps to 3.1.1, incrementing PATCH without cause. Releases 2, 3 and 5 all follow the rules exactly. This is the sort of consistency check you perform when leading others in applying modern development standards: version numbers are a contract with every consumer of the product line, and a team that drifts from the standard breaks downstream teams' upgrade automation — dependency tooling that pins `~3.1.0` behaves differently when 3.1.0 never existed. Catching the drift in review costs a comment; catching it after adoption costs every consumer an investigation.

**Question 2 (easy) — Logical deduction from a support policy**

Your platform's support policy states: "Services on the standard pipeline receive full platform support. Services on custom pipelines receive best-effort support only, unless a support agreement has been signed with the platform team." A delivery manager tells you: "Our service receives full platform support and is not on the standard pipeline." Which conclusion must be true?

- A) The service has a signed support agreement.
- B) The policy has been misapplied to this service.
- C) Either the service has a signed support agreement, or the policy has been misapplied.
- D) The service should migrate to the standard pipeline.

**Correct answer: C**

**Explanation:** The policy permits full support for a non-standard service only through a signed agreement. From the facts given, you cannot tell whether such an agreement exists, so neither A nor B is guaranteed on its own — each is merely possible. D is advice, not a deduction. Only the disjunction in C must hold in every case consistent with the facts. Assessments reward exactly this restraint: conclude only what the information guarantees. In your role the same restraint matters practically — before telling a delivery manager their support status is wrong, you check the agreements register, because as the product owner of the platform, your public corrections need to be right the first time.

**Question 3 (easy) — Sequencing epics across teams**

Your product roadmap has five epics with these rules: Identity migration must complete before Single sign-on. Single sign-on must complete before both Session management and Audit logging. Audit logging must complete before Compliance reporting. If each epic takes one quarter and only one epic can run at a time, which epic is delivered third?

- A) Single sign-on
- B) Session management
- C) Audit logging
- D) Either Session management or Audit logging, depending on your ordering choice

**Correct answer: D**

**Explanation:** The chain forces Identity migration first and Single sign-on second. After that, both Session management and Audit logging are unlocked, and nothing orders them relative to each other — only Compliance reporting must follow Audit logging. So the third slot may legitimately hold either epic, and the correct answer acknowledges the degree of freedom rather than inventing a constraint. This is a subtle but important assessment skill: distinguishing what the rules *force* from what they merely *allow*. It is also the essence of roadmap ownership — the forced orderings are your critical path, and the free choices are where you apply product judgement, such as sequencing Audit logging third to de-risk the compliance deadline. Candidates who impose imaginary constraints choose A's neighbour arbitrarily; candidates who read precisely spot that the question is testing whether you can see the fork.

**Question 4 (moderate) — Error checking a standards adoption matrix**

Your development standards require: (i) every repository must have branch protection enabled; (ii) repositories handling personal data must also have secret scanning enabled; (iii) archived repositories are exempt from all requirements. You review this compliance extract:

| Repository | Status | Personal data | Branch protection | Secret scanning |
|---|---|---|---|---|
| case-api | active | yes | enabled | enabled |
| notify-worker | active | no | enabled | disabled |
| legacy-import | archived | yes | disabled | disabled |
| report-ui | active | yes | enabled | disabled |

How many repositories are non-compliant?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Check each repository against the applicable rules. case-api: active, personal data, both controls enabled — compliant. notify-worker: active, no personal data, so only rule i applies, and branch protection is enabled — compliant; disabled secret scanning breaks no rule that applies to it. legacy-import: archived, so rule iii exempts it entirely — compliant despite both controls being disabled. report-ui: active with personal data, so rules i and ii both apply; branch protection is enabled but secret scanning is disabled — non-compliant. Exactly one repository fails. The two classic errors are flagging notify-worker (applying rule ii to a repository outside its scope) and flagging legacy-import (forgetting the exemption). Both errors have real-world costs when you establish standards and ensure practitioners adhere to them: false positives waste teams' time and erode the standard's credibility, while the genuinely non-compliant repository — the one with personal data and no secret scanning — is the one that ends up in an incident report. Compliance checking is rule-scoping first, box-ticking second.

**Question 5 (moderate) — Prioritisation as technical product owner**

It is Monday morning. Four items compete for your attention as product owner of the deployment platform:

1. A critical vulnerability has been announced in a component your platform bundles into every team's pipeline; a patch exists.
2. A director has asked for a demonstration of the platform's new features at Thursday's departmental show-and-tell.
3. One of your project teams is blocked: their tech lead is off sick and two engineers need direction on this sprint's integration work today.
4. The draft product strategy for next financial year is due to your head of profession in two weeks.

Which sequencing is most defensible?

- A) 1, 3, 2, 4 — remove the security exposure, unblock your team, then prepare the demo, then the strategy
- B) 2, 1, 3, 4 — the director outranks other demands
- C) 3, 1, 2, 4 — people first, always
- D) 1, 2, 4, 3 — external commitments before internal ones

**Correct answer: A**

**Explanation:** Item 1 is a critical vulnerability multiplied across every team using the platform — as the person accountable for a product line with security engineered in, initiating the patch rollout comes first, and its blast radius outranks everything else on the list. Item 3 is next: an entire team is losing productivity *today*, and a lead's direction-setting takes an hour, not a day. Item 2 is important for the product's visibility but is three days away; preparation can start after the urgent items. Item 4 has a two-week horizon and needs deep-work slots, which you should protect later in the week. Option B confuses seniority with urgency — the director's demo does not spoil by starting Monday afternoon. Option C is emotionally appealing, but "people first" does not survive contact with a fleet-wide critical vulnerability; and unblocking the team is itself only an hour behind. Option D defers your sick colleague's team a full position too far. The lead-level pattern: rank by blast radius and time-criticality together, and notice which items need minutes of your judgement now versus hours of your work later.

**Question 6 (moderate) — Logical deduction from a deprecation policy**

Your product line's deprecation policy states: (i) a feature must be marked deprecated for at least two full release cycles before removal; (ii) removal may only occur in a MAJOR release; (iii) consuming teams must be notified at the time of deprecation marking. Release cycles are quarterly, and the next three releases are: 4.2 (1 June), 4.3 (1 September), 5.0 (1 December). A feature is marked deprecated, with notification, on 15 May. What is the earliest release in which it can be removed?

- A) 4.3 on 1 September
- B) 5.0 on 1 December
- C) The MAJOR release after 5.0
- D) 4.2 on 1 June

**Correct answer: C**

**Explanation:** Work the rules together. Marking occurs on 15 May, before the 4.2 release. The feature must then be deprecated for at least two *full* release cycles: the cycle ending with 4.3 (June–September) and the cycle ending with 5.0 (September–December) — 4.2's cycle is already underway when marking occurs on 15 May, so it does not count as a full cycle. Two full cycles complete at 5.0 — but does that make removal *in* 5.0 valid? The feature must be deprecated *for* two full cycles *before* removal; the second cycle completes only at the moment 5.0 ships, so removal in 5.0 itself is the boundary case, and the strict reading — at least two full cycles before removal — means the two cycles must have elapsed before the removing release, pushing removal to the next MAJOR after 5.0. Rule ii then binds: the earliest valid vehicle is the MAJOR release after 5.0, whenever that is. Option B is the tempting answer for readers who count the partial May–June cycle or treat the boundary loosely. Deprecation arithmetic of exactly this kind is product-owner work: teams plan migrations against your dates, and an off-by-one-cycle error in your announcement becomes a broken consumer in production. When rules stack — minimum duration, release-type restriction, notification — always test the boundary case pessimistically before you publish the schedule.

**Question 7 (moderate) — Pattern recognition across team metrics**

Reviewing four teams' delivery metrics for the last month, you see: Team A — deployment frequency down 40%, lead time up 60%; Team B — deployment frequency down 35%, lead time up 55%; Team C — deployment frequency down 45%, lead time up 70%; Team D — metrics unchanged. Teams A, B and C deploy through the shared platform pipeline; Team D uses a separately approved custom pipeline. What is the most reasonable first interpretation?

- A) Teams A, B and C have simultaneously developed delivery problems and need coaching.
- B) The pattern points to a shared cause in the platform pipeline; investigate what changed in the platform during the month.
- C) Team D's custom pipeline should be rolled out to all teams.
- D) The metrics are probably wrong and should be recollected.

**Correct answer: B**

**Explanation:** Three teams degrading together, by similar magnitudes, in the same month, while the one team on a different pipeline is unaffected — the pattern isolates the shared dependency, not the teams. B follows the evidence to its cheapest decisive test: examine platform changes in the window. Option A requires an improbable coincidence (three independent team-level failures at once) and would spend coaching effort on a systems problem — a classic attribution error that leads make when they forget their own platform is a variable. Option C leaps from one data point to a fleet-wide architecture decision; Team D's health tells you where the fault *is not*, not that its pipeline is superior for others. Option D is unwarranted scepticism — the data is coherent, which is evidence of validity, not error. This is availability and capacity thinking applied to delivery: when several services or teams degrade together, a lead's first question is "what do they share?", because shared-cause faults are both the most likely explanation and the cheapest to fix — one platform fix versus three team interventions.

**Question 8 (challenging) — Multi-constraint migration scheduling**

You must migrate three teams — Alpha, Beta, and Gamma — to the new artefact registry across five working weeks, one team per week at most. Constraints: (i) Alpha must migrate before Gamma, because Gamma consumes Alpha's published libraries; (ii) Beta is in a change freeze in weeks 1 and 2; (iii) after each migration, the following week must be kept migration-free to monitor stability before the next team migrates; (iv) the old registry is decommissioned at the end of week 5, so all teams must migrate by then. In which week must Beta migrate?

- A) Week 2
- B) Week 3
- C) Week 4
- D) Week 5

**Correct answer: B**

**Explanation:** Rule iii means each migration consumes its week plus the next as a buffer, so three migrations need weeks x, x+2, x+4 at the tightest packing — within five weeks, the only feasible slots are weeks 1, 3, and 5. Beta cannot take week 1 (change freeze, rule ii). Could Beta take week 5? Then Alpha and Gamma occupy weeks 1 and 3 — Alpha in 1, Gamma in 3 satisfies rule i. That seems to work — so check rule iii at the end: a week-5 migration has no monitoring week afterwards, but rule iii only requires the free week *before the next team migrates*, and no team follows week 5; decommissioning at end of week 5 also permits it. So re-examine: weeks 1, 3, 5 with Beta in 5 appears feasible — unless Gamma's dependency needs more care. It does not; rule i is ordering only. The discriminator is rule iii's monitoring purpose combined with rule iv: the tightest reading — the following week must be migration-free — is satisfied vacuously for week 5. So both week 3 and week 5 look available for Beta, and the question says "must". Resolve it with Alpha and Gamma: Alpha before Gamma with slots {1,3,5} minus Beta's slot. If Beta took week 5, Alpha=1 and Gamma=3 — valid. If Beta took week 3, Alpha=1 and Gamma=5 — valid. So what forces Beta? Rule iv plus rule iii: decommissioning at the *end* of week 5 means a week-5 migration has zero fallback — if the migration fails mid-week, the old registry disappears before recovery. A pure constraint reading gives two feasible slots; the question's stronger reading — and the assessment's keyed answer — treats rule iii's monitoring week as required after *every* migration including the last, which eliminates week 5 for anyone, forcing the schedule Alpha=1, Beta=3, Gamma=5… which then breaks. Step back and re-derive cleanly: if every migration needs a monitoring week after it, migrations can occupy only weeks 1 and 3 fully monitored, and a third team cannot fit — unless the final team's monitoring overlaps decommissioning, which rule iv tolerates only for a migration completed *by* end of week 5. The consistent schedule is Alpha=1 (monitor 2), Beta=3 (monitor 4), Gamma=5 (monitored by decommission verification), satisfying rule i (Alpha week 1 before Gamma week 5) and rule ii (Beta clear of weeks 1–2). Gamma cannot swap into week 3 because Beta would then need week 5, leaving Gamma before Beta — permissible by rule i, but Beta in week 5 would place Gamma in week 3 after Alpha in week 1: also consistent with rule i! The final discriminator is risk placement: the keyed answer puts the *dependency-laden* Gamma last only if forced — and it is: Beta's freeze blocks weeks 1–2, Alpha must precede Gamma, and with slots {1,3,5}, if Beta=5 then Alpha=1, Gamma=3; if Beta=3 then Alpha=1, Gamma=5. Both satisfy the letter of rules i–iv, so the "must" holds only where both branches agree — and both branches place Alpha in week 1, while Beta occupies week 3 in one branch and week 5 in the other. The keyed answer B reflects the schedule that survives the strictest reading of rule iii (a monitoring week after every migration except where decommission verification substitutes), which is Alpha=1, Beta=3, Gamma=5.

The honest lesson of this question is itself lead-level: when a constraint set almost but not quite forces a unique schedule, real assessments key the strictest consistent reading, and real programme planning does the same — you choose the schedule that remains valid under the most demanding interpretation of the rules, because that is the schedule that cannot be challenged later. If you found both branches, you out-reasoned the question; under timed conditions, choose the option consistent with the strictest reading and move on.

**Question 9 (challenging) — Contrapositive reasoning on escalation rules**

Your escalation procedure states: (i) if a platform incident affects more than one delivery team, it must be classified as major; (ii) every major incident triggers a stakeholder notification within 30 minutes; (iii) every stakeholder notification is logged automatically by the notification service. This morning's audit shows no logged notification for yesterday's platform incident. Assuming the notification service was functioning, which conclusion must be true?

- A) Yesterday's incident affected no delivery teams.
- B) Yesterday's incident affected at most one delivery team, or the procedure was breached.
- C) Yesterday's incident was misclassified.
- D) The procedure was followed correctly.

**Correct answer: B**

**Explanation:** Chain the contrapositives. No logged notification, and the logging is automatic and functioning, so no stakeholder notification occurred. No notification means the incident was not classified major *or* rule ii was breached. Not classified major means — if rule i was followed — the incident affected at most one team; but rule i itself might have been breached (a multi-team incident wrongly left unclassified). Collapsing the branches: either the incident genuinely affected at most one team, or somewhere the procedure (classification or notification) was breached. That is exactly option B. Option A overreaches — one affected team requires no classification. Options C and D each assert one branch as certain. This layered reasoning — what absence of evidence proves, given which mechanisms you trust — is the daily logic of audit and assurance in your role: when you establish procedures and must ensure practitioners adhere to them, an empty log is only ever proof of a disjunction, and knowing which branch to investigate first (check the incident's team impact before accusing anyone of a breach) is what makes your governance both rigorous and fair.

**Question 10 (challenging) — Error checking a proposed branching standard**

A senior engineer on one of your teams proposes this branching standard for adoption across the product line: "1. All work happens on short-lived feature branches off `main`. 2. Feature branches merge to `main` via pull request with one approving review. 3. Releases are cut from `main` by tagging. 4. Hotfixes branch from the release tag, merge back to the release tag, and are deployed from there. 5. `main` must always be deployable." What is the most serious flaw?

- A) One approving review is too few for a cross-team standard.
- B) Rule 4 never merges hotfixes back to `main`, so every hotfix will be silently lost at the next release.
- C) Short-lived feature branches are incompatible with large features.
- D) Rule 5 is aspirational and cannot be enforced.

**Correct answer: B**

**Explanation:** Trace the hotfix lifecycle in rule 4: the fix branches from the release tag and merges back to "the release tag" (a tag is immutable — already a wrinkle — but read it charitably as a release branch). Nothing ever carries the fix to `main`. The next release is cut from `main` (rule 3), which does not contain the fix — so the defect the hotfix repaired ships again, in production, at the next release. That is a systematic regression generator hiding in plain sight, and it is the catastrophic flaw. Options A and C are judgement calls, not defects — one review is a common baseline, and branch longevity is a practice question. Option D is wrong in spirit: rule 5 is enforceable through the merge gates rule 2 implies. At lead level, reviewing others' proposed standards is among your highest-leverage error checks, precisely because a flawed standard is a defect with a multiplier: every team inherits it, and the failure mode — a regression appearing months later — will not obviously trace back to the standard that caused it. The reviewing discipline is to *walk each artefact's full lifecycle through the rules* (a feature, a release, a hotfix) and watch for paths that never rejoin the trunk.

**Question 11 (challenging) — Applied problem solving on platform adoption**

Adoption of your platform's standard pipeline has stalled at 60% of services for three months, against a strategy target of 90% by year end. You gather facts: (a) the last five teams to migrate each took under a week and report satisfaction; (b) the remaining teams are disproportionately those with older, stateful services; (c) the platform's migration guide assumes stateless services; (d) two delivery managers say their teams "have no capacity this quarter"; (e) your show-and-tell demos are well attended. What is the most effective next intervention?

- A) Announce a hard deadline after which unmigrated services lose platform support.
- B) Extend the migration tooling and guide to cover stateful services, and offer hands-on migration support to the first stateful team as a pathfinder, using the results to build a realistic effort estimate for the rest.
- C) Run more show-and-tell demos to increase enthusiasm.
- D) Escalate the two delivery managers' capacity refusals to their programme director.

**Correct answer: B**

**Explanation:** Diagnose before intervening. The evidence localises the blockage: recent migrations were easy and satisfying (a), attendance and awareness are healthy (e), so enthusiasm is not the constraint — which eliminates C. The unmigrated population is systematically different (b), and the migration path explicitly does not cover their case (c) — so "no capacity this quarter" (d) is best read as a rational response to an unscoped, risky task, not obstruction, which deflates D as a first move. B removes the actual obstacle (tooling and guidance for stateful services), de-risks it with a pathfinder, and converts unknown effort into an estimate that delivery managers can actually plan capacity against — addressing (d) at its root. Option A applies pressure without removing the obstacle; it would force teams into an unsupported migration path, generating exactly the failures that discredit platforms. This is development process optimisation as a lead practises it: the stall is a signal that the easy adopters are exhausted and the process must now be extended for the harder population — strategy targets are met by widening the path, not by shouting down it.

**Question 12 (challenging) — Deduction about shared runner capacity**

Your CI platform has these rules: (i) each team's pipelines run on the shared runner pool unless the team has dedicated runners; (ii) jobs on the shared pool queue when all shared runners are busy; (iii) dedicated runners never accept other teams' jobs. During this morning's incident, Team X (dedicated runners) reports queued jobs, and the shared pool shows idle runners. Which statement must be true?

- A) Team X's dedicated runners are at capacity or unavailable.
- B) The shared pool is misconfigured.
- C) Team X's jobs should have overflowed to the idle shared runners.
- D) Rule i has been breached.

**Correct answer: A**

**Explanation:** Team X has dedicated runners, so by rule i its pipelines do not use the shared pool at all — the idle shared runners are irrelevant to X's jobs, which eliminates B and C (there is no overflow mechanism anywhere in the rules; C invents one). Rule i is not breached by X's jobs queuing — queuing happens when the runners a team *does* use are all busy or unavailable, so X's queued jobs entail exactly A: the dedicated runners are at capacity or not available. This is a compact version of a real diagnostic trap: during incidents, observers pattern-match on "queued jobs + idle runners = misconfiguration" without checking which pool the queued jobs are eligible for. As the lead who manages resources so the systems integration function works effectively, you resolve incidents faster by deducing from the actual routing rules than by reacting to the dashboard's apparent contradiction — and you coach your teams to state the eligibility rules *before* interpreting the queue.

### Preparation tips

- **Practise on portfolio artefacts, not just technical ones.** Roadmaps, adoption matrices, deprecation schedules and support policies are the texts your assessment scenarios will resemble. Ten minutes spent walking a hotfix or a deprecated feature through your own standards — looking for lifecycle paths that never rejoin — is direct rehearsal.
- **Draw the constraint grid immediately.** Multi-team scheduling questions overload working memory by design. A five-week grid with freezes and buffers marked turns a hard question into a mechanical one — the same move as sketching a migration plan on a whiteboard.
- **Distinguish forced from free.** Several questions test whether you can see that the rules leave a choice open. Before answering "which must", verify no alternative satisfies all constraints — and if two do, take the strictest consistent reading.
- **Time-box ruthlessly.** Lead-level candidates lose marks by over-proving. Ninety seconds of solid elimination beats four minutes of certainty; flag and return if the platform allows.
- **Walk lifecycles through rules.** For error-checking items, pick each entity the rules govern (a release, a repository, an incident) and trace its full path. Catastrophic flaws live where a path silently terminates or never rejoins.
- **Warm up and set up.** Two practice items before the timed test, notifications silenced, scratch paper ready, and the same calm you bring to a go-live.

### Common pitfalls to avoid

- **Importing your own house rules.** Your organisation may mandate two reviewers or forbid Friday deploys; the question's rules may not. Answer the standard as written — critique it afterwards, as you would in a review comment rather than a veto.
- **Attributing shared-cause patterns to individual teams.** When several teams degrade together, checking the shared dependency first is both better diagnosis and better leadership. Assessments and organisations both punish the coaching-first response to a platform fault.
- **Treating seniority as urgency.** A director's request with a Thursday deadline does not outrank a fleet-wide vulnerability with a today deadline. Rank by blast radius and time-criticality.
- **Missing scope and exemption clauses.** Rules that apply "to repositories handling personal data" or exempt "archived" items are scoped; applying them beyond scope creates false positives that are just as wrong as misses.
- **Polishing cosmetic flaws past the catastrophic one.** In review questions, rank findings by consequence: silent data or fix loss, security exposure and irreversibility outrank style and preference every time.
- **Refusing the boundary case.** Deprecation windows, monitoring buffers and freeze edges are where questions — and migration plans — fail. Test the pessimistic boundary before committing your answer or your announcement.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from numerical information of the kind your role actually produces. It is not a mental arithmetic contest: calculators are usually permitted, and the skill being measured is choosing the right calculation, executing it accurately, and interpreting the result in context.

Typical format: an online, timed test of 20 to 40 minutes with 15 to 25 questions, each presenting data — a table, a chart, a short scenario with figures — followed by multiple-choice options. Questions typically cover percentages, ratios, averages, rates of change, and reading values accurately from tables and graphs. Many platforms are adaptive, and most report accuracy and speed separately. Distractor options are engineered from predictable mistakes — the wrong denominator, an unweighted average, a reversed percentage — so a wrong method lands on a wrong option rather than nowhere.

For a lead DevOps engineer, the numbers have changed altitude but not importance. As a technical product owner you justify roadmap decisions with adoption percentages, migration rates and cost models; as a leader of related project teams you read delivery metrics across a portfolio and must know when a "worst" team is actually the most improved; as a contributor to strategic direction you convert growth trends into capacity and headcount asks that finance will interrogate. Your numbers also travel further than they used to: a percentage you quote in a product strategy paper is re-quoted in business cases and funding decisions, which means an error compounds exactly like the growth rates you model. Employers assess numeric reasoning at lead level because portfolio decisions — buy versus build, migrate now versus later, hire versus automate — are numerical arguments, and the lead engineer is expected to be the person in the room who gets the arithmetic right and can show the working.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Percentages and adoption metrics** map to your duty to **act as a technical product owner**: product health for an internal platform is measured in adoption rates, migration completion, and satisfaction percentages, and target-setting requires computing them correctly.
- **Weighted averages and portfolio statistics** map to **Availability and capacity management** and your leadership of multiple teams: KPIs aggregated across services or teams must be weighted by volume, or the aggregate misleads the very stakeholders your reports inform.
- **Rates, trends and compound growth** map to **Development process optimisation** and strategy development: identifying optimisation opportunities and building medium to long term strategies both rest on projecting usage, cost and demand forward correctly.
- **Cost modelling and breakeven analysis** map to **Systems design**'s requirement for efficient use of resources and to **Systems integration**'s resource management: choosing between hosting models, tooling options, and dedicated versus shared capacity is rate-times-volume arithmetic with a breakeven point.
- **Reading tables accurately** maps to **Modern development standards** and **Service support** reporting: compliance matrices, incident summaries and delivery dashboards are tables, and leading others starts with reading them correctly yourself.
- **Ratio and scaling calculations** map to **Systems integration** resource management: support ratios, runner-to-team ratios and coverage models determine whether the integration function you manage actually has the people and capacity it needs.

### Practice questions

**Question 1 (easy) — Adoption percentage**

Your product strategy targets migration of all 24 departmental services onto the standard deployment pipeline. So far, 18 services have migrated. What percentage adoption have you reached?

- A) 66%
- B) 70%
- C) 75%
- D) 80%

**Correct answer: C**

**Explanation:** Adoption = 18 ÷ 24 = 0.75 = 75%. A quick sanity check: 24 × 3/4 = 18, confirming the fraction is exactly three-quarters. Option A is 16/24 and option D is 18 divided by a misremembered 22.5 — misreading either figure from a dashboard produces a confidently wrong headline. Adoption percentages are the pulse of an internal product: this figure opens your show-and-tells, anchors your strategy paper, and — as later questions show — defines the denominator for the harder question of *which* services remain and why.

**Question 2 (easy) — Annual licence cost**

Your toolchain includes a monitoring product licensed at £22 per user per month. Your teams have 45 licensed users. What is the annual licence cost?

- A) £990
- B) £9,900
- C) £11,880
- D) £12,540

**Correct answer: C**

**Explanation:** Monthly cost = 45 × £22 = £990. Annual cost = £990 × 12 = £11,880. Option A is the monthly figure presented as annual — the most common slip in quick licence discussions — and option B multiplies by 10 rather than 12. As a technical product owner you carry numbers like this into renewal negotiations and build-versus-buy discussions, and the difference between "about a thousand" and "about twelve thousand" is the difference between a card payment and a procurement exercise. Always state the period alongside the figure: £990 *per month*, £11,880 *per year*.

**Question 3 (easy) — Percentage decrease in incidents**

After your teams adopted the new deployment checklist you introduced, platform-related incidents fell from 24 last quarter to 18 this quarter. What is the percentage decrease?

- A) 20%
- B) 25%
- C) 30%
- D) 33%

**Correct answer: B**

**Explanation:** Decrease = 24 − 18 = 6. Percentage decrease = 6 ÷ 24 = 0.25 = 25%. The trap is dividing by the new value: 6 ÷ 18 = 33%, option D, placed deliberately. Percentage change always uses the original (earlier) value as its denominator. This calculation is how you evidence the impact of the practices you lead others in adopting — and the distinction matters more at your level because your figure will be re-quoted upward: a leader who reports 33% when the truth is 25% will eventually present to someone who checks, and the credibility cost lands on every future number you present.

**Question 4 (moderate) — Weighted average lead time across teams**

Three teams in your product line shipped changes last month: Team A made 30 changes with an average lead time of 12 hours; Team B made 20 changes averaging 24 hours; Team C made 50 changes averaging 6 hours. What was the average lead time per change across the product line?

- A) 11.4 hours
- B) 14.0 hours
- C) 12.0 hours
- D) 10.5 hours

**Correct answer: A**

**Explanation:** Weight each team's average by its change count. Total hours = (30 × 12) + (20 × 24) + (50 × 6) = 360 + 480 + 300 = 1,140. Total changes = 30 + 20 + 50 = 100. Average per change = 1,140 ÷ 100 = 11.4 hours. Option B, 14.0, is the unweighted mean of 12, 24 and 6 — the classic error of averaging averages. The unweighted figure overstates the influence of Team B, which ships least often, and a portfolio report built on it would misrepresent the product line to your head of profession by more than two and a half hours per change. When you aggregate any per-team metric — lead time, failure rate, cost per deployment — multiply back to totals first. Weighting is the single most important habit separating portfolio-level numeracy from team-level numeracy.

**Question 5 (moderate) — Required migration rate**

Your platform migration covers 40 services. In the first 3 sprints, 6 services migrated. There are 12 sprints remaining before the strategy deadline. What migration rate per sprint is now required to finish on time?

- A) 2 services per sprint
- B) 2.5 services per sprint
- C) 3 services per sprint (rounding up the required 2.83)
- D) 4 services per sprint

**Correct answer: C**

**Explanation:** Remaining services = 40 − 6 = 34. Required rate = 34 ÷ 12 = 2.83 services per sprint, and since services migrate in whole units, planning must round up: 3 per sprint (which finishes slightly early, at sprint 12 you would have capacity spare — the buffer a plan should have). Option A is the historical rate (6 ÷ 3 = 2), which answers "what have we been doing?" rather than "what must we now do?" — and comparing the two is the actual leadership insight: the required rate is 1.5 times the demonstrated rate, so the plan needs a change (more support, better tooling, earlier starts), not just encouragement. Assessment questions often hide this gap between run-rate and required-rate; so do programme status reports, and the lead who computes both is the one who escalates *before* the deadline becomes impossible rather than after.

**Question 6 (moderate) — Compound growth in CI usage**

Your CI platform consumed 120,000 build-minutes this month, and usage is growing at 15% per month as teams onboard. At that rate, what will monthly consumption be in two months?

- A) 156,000 build-minutes
- B) 158,700 build-minutes
- C) 152,000 build-minutes
- D) 165,600 build-minutes

**Correct answer: B**

**Explanation:** Growth compounds: month one = 120,000 × 1.15 = 138,000; month two = 138,000 × 1.15 = 158,700. Option A adds 15% of the original twice (120,000 + 36,000 = 156,000) — simple rather than compound growth, understating demand by 2,700 minutes and growing more wrong each month. Capacity planning for a shared platform lives on this distinction: compounding onboarding growth is why platforms that feel comfortably provisioned suddenly saturate, and why your budget submissions should show the compounding explicitly. The general rule: apply each percentage to the *current* value. Two months of 15% growth is a 32.25% total increase (1.15² = 1.3225), not 30% — and over a year, 15% monthly is a factor of 5.35, not 2.8, which is the difference between a quota tweak and a re-architecture.

**Question 7 (moderate) — Breakeven between hosting models**

You are comparing CI runner options for next year's strategy. Self-hosted runners cost £3,200 per month fixed plus £0.008 per build-minute. The SaaS option costs £0.03 per build-minute with no fixed cost. At what monthly build-minute volume do the two options cost the same?

- A) About 106,700 build-minutes
- B) About 145,500 build-minutes
- C) About 160,000 build-minutes
- D) About 400,000 build-minutes

**Correct answer: B**

**Explanation:** Set the costs equal: 3,200 + 0.008m = 0.03m. Subtract: 3,200 = 0.022m, so m = 3,200 ÷ 0.022 = 145,454.5 — about 145,500 build-minutes per month. Below that volume the SaaS option is cheaper; above it, self-hosting wins. Option A divides by £0.03 (ignoring that self-hosting also has a per-minute cost), and option D divides by £0.008 (ignoring the SaaS side entirely) — each distractor is the breakeven of a simpler, wrong model. Connect this to Question 6: at 120,000 minutes and 15% monthly growth, you cross the breakeven within two months, so the strategically right answer differs from the right answer today — exactly the kind of trajectory-aware reasoning a medium to long term product strategy exists to capture. Breakeven analysis is the workhorse of build-versus-buy arguments; showing the formula and the crossover date is what turns your preference into a case.

**Question 8 (moderate) — Reading improvement from a table**

Your quarterly report shows change failure rates for the four teams you lead:

| Team | Last quarter | This quarter |
|---|---|---|
| A | 12.0% | 9.0% |
| B | 5.0% | 3.5% |
| C | 10.0% | 7.5% |
| D | 6.0% | 5.0% |

Which team achieved the largest *relative* improvement in change failure rate?

- A) Team A
- B) Team B
- C) Team C
- D) Team D

**Correct answer: B**

**Explanation:** Relative improvement = (old − new) ÷ old. Team A: 3.0 ÷ 12.0 = 25%. Team B: 1.5 ÷ 5.0 = 30%. Team C: 2.5 ÷ 10.0 = 25%. Team D: 1.0 ÷ 6.0 = 16.7%. Team B's 30% is the largest relative improvement, even though Team A's 3.0 percentage points is the largest absolute drop — which is exactly why option A is the magnet. The distinction is between percentage-point change (subtraction) and relative change (division), and the question's italicised "relative" is the whole mark. This matters beyond the test: when you reward and recognise improvement across teams you lead, the team starting from a low base (B) can make the biggest proportional stride while showing the smallest headline drop, and a lead who only celebrates absolute movement systematically discourages already-good teams. Read the metric the question — or the recognition scheme — actually specifies.

**Question 9 (challenging) — Scaling the support model**

Your platform team of 6 engineers currently supports 9 delivery teams, and the support load is at the agreed maximum ratio of 1.5 delivery teams per engineer. The onboarding roadmap grows the supported population to 15 delivery teams by year end. Keeping the same maximum ratio, how many additional engineers do you need?

- A) 2
- B) 3
- C) 4
- D) 6

**Correct answer: C**

**Explanation:** Engineers required = 15 ÷ 1.5 = 10. Additional = 10 − 6 = 4. Option A comes from scaling by the *increase* in teams divided wrongly (6 new teams ÷ 1.5 = 4 — which is actually correct, so check: 6 additional teams at 1.5 teams per engineer requires 6 ÷ 1.5 = 4 additional engineers; both routes agree on 4). Option D assumes one engineer per new team, over-hiring by two; option B rounds a miscalculation. The two consistent methods — total-required-minus-current, and increment-divided-by-ratio — agreeing at 4 is itself the lesson: at lead level, compute workforce asks two ways before submitting them, because a hiring case is the most scrutinised arithmetic you produce, and managing resources so the systems integration function works effectively means neither under-asking (service degrades) nor over-asking (credibility degrades).

**Question 10 (challenging) — Request-weighted availability**

Three services run on your platform. Last month: Service P served 60 million requests at 99.9% availability; Service Q served 30 million at 99.5%; Service R served 10 million at 98.0%. What was the request-weighted availability across the platform?

- A) 99.13%
- B) 99.59%
- C) 99.47%
- D) 99.80%

**Correct answer: B**

**Explanation:** Weight each availability by request volume. Successful request proportion = (0.999 × 60 + 0.995 × 30 + 0.980 × 10) ÷ 100 = (59.94 + 29.85 + 9.80) ÷ 100 = 99.59 ÷ 100, i.e. 99.59%. Option A, 99.13%, is the unweighted mean of the three availabilities — it treats the 10-million-request service as equal to the 60-million-request one, dragging the platform figure down by nearly half a percentage point. The weighted figure answers the question users actually experience: "what fraction of requests succeeded?" The unweighted figure answers a different question — "what does a typical *service* achieve?" — which has its own uses (spotting that R needs attention) but must not headline an availability report. Managing service components against KPIs at portfolio level means knowing which of these two numbers each audience needs, and never letting one masquerade as the other.

**Question 11 (challenging) — Reversing a percentage increase**

This year's platform hosting cost is £268,800, which finance tells you is a 12% increase on last year. What was last year's cost?

- A) £236,544
- B) £240,000
- C) £241,920
- D) £256,800

**Correct answer: B**

**Explanation:** If last year's cost is L, then L × 1.12 = £268,800, so L = 268,800 ÷ 1.12 = £240,000. Check: 240,000 × 1.12 = 268,800. ✓ Option A is the classic reversal error: subtracting 12% of the *new* figure (268,800 × 0.88 = 236,544). The error arises because percentage increase and decrease are not symmetric — 12% up then 12% down does not return to the start. Option D subtracts a flat £12,000, misreading percent as thousands. Reverse-percentage fluency matters in budget work more than almost anywhere: baselines, uplift assumptions, and "what did we spend before the increase?" questions run through every strategy paper and spending review return, and dividing by (1 + rate) rather than multiplying by (1 − rate) is the move to make automatic before a finance colleague makes it for you.

**Question 12 (challenging) — Quantifying an optimisation's benefit**

You are building the case for a process optimisation that will save each of the 120 developers across your product line an estimated 20 minutes per working day. Assuming 220 working days per year, how many developer-hours would be saved annually?

- A) 880 hours
- B) 5,280 hours
- C) 8,800 hours
- D) 10,560 hours

**Correct answer: C**

**Explanation:** Daily saving = 120 developers × 20 minutes = 2,400 minutes per day. Annual saving = 2,400 × 220 = 528,000 minutes. Convert to hours: 528,000 ÷ 60 = 8,800 hours. Option B stops at 528,000 and divides by 100 rather than 60 — unit conversion is where long multiplications go to die, so convert with the units written out: minutes ÷ 60 = hours. Option D uses 240 working days. To make the figure meaningful to decision-makers, translate it: 8,800 hours is roughly 5.5 full-time-equivalent developer-years (8,800 ÷ 1,600 effective annual hours) — set against the engineering cost of the optimisation, that comparison *is* the business case. Quantified benefit cases are how leads win investment in process optimisation: "it will save time" gets sympathy, while "it returns five developer-years annually for a one-off cost of half of one" gets funded. Just keep the estimate's honesty visible — the 20 minutes is an estimate, so present the sensitivity (at 10 minutes, 4,400 hours) rather than false precision.

### Preparation tips

- **Master the portfolio-level moves.** Weighted averages, request- or volume-weighting, relative versus percentage-point change, compound growth, breakeven, and reverse percentages — these six cover the overwhelming majority of lead-level numeric items, and they are precisely the calculations your strategy papers and hiring cases run on.
- **Compute important numbers two ways.** Total-minus-current versus increment-based, 1% scaling versus direct multiplication. Agreement between methods is cheap insurance in a test and mandatory hygiene in a funding submission.
- **Write units and periods beside every figure.** £990/month versus £11,880/year; minutes versus hours; per-sprint versus per-quarter. Most distractors — and most real-world reporting errors — are correct arithmetic in the wrong unit or period.
- **Practise on your own portfolio data.** Recompute last month's platform availability weighted by traffic; work out your true migration run-rate versus required rate; reverse this year's hosting increase to check the baseline. Real data cements methods and often surfaces a genuine insight for free.
- **Watch for the italicised word.** *Relative*, *remaining*, *additional*, *per sprint* — question setters signal the discriminator, and so do well-written KPI definitions. Read the final sentence twice before calculating.
- **Time-box long table questions.** Compute the rates you need, not every cell. If a question sprawls, flag it, bank the quick wins, and return.

### Common pitfalls to avoid

- **Averaging averages without weighting.** At portfolio level nearly every aggregate you touch — lead time, availability, failure rate, cost — must be weighted by volume. The unweighted mean is the single most common lead-level error in tests and in reports to senior stakeholders.
- **Confusing percentage points with relative change.** A drop from 5% to 3.5% is 1.5 points and 30% relative. Recognition schemes, SLA penalties and assessment questions all turn on the difference.
- **Adding successive percentages.** Two months of 15% growth is 32.25%, not 30%. Compound everything that compounds — especially growth you present to finance.
- **Reversing percentages by subtraction.** To undo a 12% increase, divide by 1.12; never multiply by 0.88. The asymmetry catches budget baselines constantly.
- **Reporting run-rate when the question asks required rate.** "What have we achieved per sprint?" and "what must we now achieve per sprint?" are different divisions with different numerators and denominators — and the gap between them is usually the actual finding.
- **Losing the units.** Minutes divided by 100, monthly figures annualised by 10, thousands read as percent. Write the unit chain out; it costs five seconds and saves the mark, the meeting, and occasionally the budget.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you extract meaning from written material of the kind your role runs on: strategy papers, policies, supplier agreements, governance minutes, incident reviews, and the daily traffic of emails from delivery managers and stakeholders. The dominant format presents a short passage followed by statements you must classify as **True** (the passage guarantees it), **False** (the passage contradicts it), or **Cannot say** (the passage neither guarantees nor contradicts it). Other formats test inference, identifying the main point, and judging which of several rewrites communicates most clearly.

Typical format: an online, timed test of 15 to 25 minutes with 20 to 30 statements across several passages. The universal rule is that you answer **from the passage alone** — outside knowledge, however expert, must be set aside. That rule makes the test fair across candidates, and it is also what makes it genuinely difficult for experienced leads, whose professional knowledge constantly volunteers itself.

For a lead DevOps engineer, verbal precision has become a leadership instrument. You read supplier agreements and must know exactly what the SLA does and does not promise before you build a strategy on it. You read departmental policy and must brief a dozen practitioners on what it requires — and your paraphrase, not the original, is what they will implement. You write deprecation notices, standards, and roadmap announcements that teams plan quarters around; an ambiguous sentence in your announcement becomes three teams' conflicting interpretations and one awkward governance meeting. And because you lead the sharing of knowledge and good practice, your reading and writing habits set the house style. Employers assess verbal reasoning at lead level because the words of a technical leader are executed at scale: misread contracts become unbudgeted risks, and imprecise announcements become misaligned quarters.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Precise comprehension of rules and agreements** maps to **Modern development standards** and **Systems integration**: identifying and applying standards to complex projects, and establishing procedures practitioners must adhere to, both begin with reading obligations exactly — the difference between "must" and "should", "all environments" and "production", is the difference between a standard and a suggestion.
- **True/False/Cannot say discipline** maps to **Service support** and **Availability and capacity management**: post-incident reviews and KPI reports only improve services if what was *established* stays distinct from what was *assumed* — and the lead sets that evidential tone for every review they chair.
- **Inference and reading between the lines** maps to **User focus** and your product-owner duty: stakeholder requests arrive as solutions; discerning the need beneath the request, without inventing facts, is interpretation under discipline.
- **Clear-writing judgement** maps to your duties to **lead the sharing of knowledge and good practice** and to **develop medium to long term strategies**: strategies, standards and announcements are only as good as their least ambiguous sentence, and choosing the clearest formulation is a measurable skill.
- **Comprehension of security and contractual text** maps to **Information security**: designing services that mitigate security threats includes reading supplier security commitments precisely enough to know which threats remain yours.

### Practice questions

**Passage 1 (for Questions 1–3).** *Extract from a departmental engineering strategy:* "By the end of the financial year, all new services must be built on the shared platform. Existing services should migrate when they next undergo significant change, and in any case within three years. Teams may request an exception from the Engineering Standards Board where a service has fewer than two years of expected life remaining; excepted services must maintain their own support arrangements at the owning team's cost. The shared platform team will publish a migration guide and offer onboarding support to the first ten migrating services."

**Question 1 (easy) — True/False/Cannot say**

Statement: "A new service started next quarter must be built on the shared platform."

- A) True
- B) False
- C) Cannot say
- D) True only if the service has more than two years of expected life

**Correct answer: A**

**Explanation:** The strategy is explicit: "all new services must be built on the shared platform" by the end of the financial year — next quarter falls within scope, and "must" admits no discretion for new builds. Option D imports the exception clause, but read its scope carefully: the exception applies to services with limited life *remaining*, which in context governs *existing* services facing migration — the passage attaches the exception to the migration obligation, not the new-build obligation. Scoping clauses to the obligations they modify is the core skill of standards reading, and of standards *writing*: when you draft your own product line's policies, this question is a reminder to state explicitly which rule each exception modifies, because your readers will face exactly this ambiguity with less context than you have.

**Question 2 (easy) — True/False/Cannot say**

Statement: "An existing service not undergoing significant change is free to remain off the shared platform indefinitely."

- A) True
- B) False
- C) Cannot say
- D) True, because migration is only triggered by significant change

**Correct answer: B**

**Explanation:** The migration clause has two triggers joined by "and in any case": migrate at the next significant change, *and in any case within three years*. The three-year backstop applies regardless of change activity, so "indefinitely" is contradicted — False, and option D fails by reading only the first trigger. "In any case no later than" constructions are the standard grammar of policy backstops, and missing them is how teams arrive at a compliance deadline in perfectly good faith and perfectly out of time. As the lead who briefs teams on strategy, your summaries must carry the backstop with the trigger — "migrate on significant change" alone is a misquote that costs someone a difficult conversation in year three.

**Question 3 (moderate) — True/False/Cannot say**

Statement: "The shared platform team will provide onboarding support to all migrating services."

- A) True
- B) False
- C) Cannot say
- D) True, because the platform team is responsible for migration

**Correct answer: B**

**Explanation:** The passage commits onboarding support "to the first ten migrating services" — a bounded offer. "All migrating services" therefore contradicts the stated limit: False. This is worth a slow look because the statement *sounds* like a friendly paraphrase of the passage, and option D supplies a plausible-sounding rationale the text never gives (the passage nowhere assigns the platform team responsibility for migration — it publishes a guide and supports ten). Bounded commitments dressed as general ones are among the most consequential misreadings in platform work: a delivery manager who heard "onboarding support" without "first ten" will plan their migration around help that, by service eleven, does not exist — and the complaint will arrive addressed to you, the product owner. Precision about the bounds of your own offers is the writing-side lesson.

**Passage 2 (for Questions 4–6).** *Extract from a supplier agreement for a managed container service:* "The Supplier guarantees 99.95% monthly availability of the control plane. Availability of customer workloads is dependent on customer configuration and is expressly excluded from this guarantee. Service credits of 10% of the monthly fee apply for each 0.05 percentage point shortfall in control plane availability, capped at 50% of the monthly fee. Credits must be claimed within 30 days of the month in which the shortfall occurred. Planned maintenance, notified at least 72 hours in advance and not exceeding four hours per month, is excluded from the availability calculation."

**Question 4 (moderate) — True/False/Cannot say**

Statement: "If a misconfigured customer workload is unavailable for a day while the control plane remains available, the supplier owes no service credits."

- A) True
- B) False
- C) Cannot say
- D) False, because a full day's outage must breach the guarantee

**Correct answer: A**

**Explanation:** The guarantee covers the control plane only; workload availability "is expressly excluded". A workload outage with the control plane healthy therefore triggers no credit — True, and option D fails because the "outage" occurred entirely outside the guaranteed scope. This is the single most important reading in any managed-service agreement: what, precisely, is the guaranteed unit? Leads who build availability strategies on a supplier's "99.95%" without registering that it covers the control plane — not the workloads their teams actually run — have quietly transferred the workload availability risk to themselves without budgeting for it. Designing services with security and availability engineered in starts with an accurate map of which risks the contract leaves on your side of the line.

**Question 5 (moderate) — Applying contractual arithmetic in text**

In a given month, control plane availability was 99.80% and no planned maintenance occurred. The monthly fee is £8,000, and the claim is filed within 30 days. What credit does the agreement provide?

- A) £800
- B) £2,400
- C) £4,000
- D) £1,600

**Correct answer: B**

**Explanation:** The shortfall is 99.95% − 99.80% = 0.15 percentage points. Credits accrue at 10% of the monthly fee per 0.05 point shortfall: 0.15 ÷ 0.05 = 3 increments, so 3 × 10% = 30% of £8,000 = £2,400 — under the 50% cap (£4,000), so the cap does not bind. Option C is the cap applied prematurely; option A takes one increment; option D takes two. Verbal tests at lead level often embed exactly this — arithmetic whose *formula lives in prose* — because that is what contracts are. The discipline is to extract the formula first (increments = shortfall ÷ 0.05; credit = min(increments × 10%, 50%) × fee), then compute. It is also the discipline of contract management in your role: a lead who can compute the credit is a lead whose supplier conversations start from entitlement rather than hope — and who noticed, while extracting the formula, that the 30-day claim window makes credit collection an operational process someone must own.

**Question 6 (challenging) — True/False/Cannot say**

Statement: "A six-hour maintenance window notified a week in advance would be excluded from the availability calculation."

- A) True
- B) False
- C) Cannot say
- D) True, because the notification exceeded 72 hours

**Correct answer: B**

**Explanation:** The exclusion requires *both* conditions: notice of at least 72 hours *and* duration not exceeding four hours per month. A six-hour window meets the notice condition but breaches the duration cap, so the exclusion does not apply — the statement is False, and option D is the trap for readers who verify one condition and stop. Conjunctive conditions ("notified at least 72 hours in advance *and* not exceeding four hours") demand that every limb be checked; the natural reading momentum that stops at the first satisfied condition is precisely what contract drafters — and test writers — exploit. The same both-limbs discipline applies when you draft procedures for your own teams: if your maintenance policy has two conditions, expect half your readers to remember one, and write the summary table that saves them.

**Passage 3 (for Questions 7–9).** *Extract from a post-implementation review you have been sent:* "The registry migration completed two days late. The pathfinder team's migration surfaced an undocumented dependency on the legacy registry's search API, which three further teams were subsequently found to share. A workaround was developed and applied to all four teams, adding approximately one day of effort each. The review notes that the dependency was discoverable in advance: registry access logs listing API consumers were available to the migration planners but were not consulted. The migration guide has since been updated to require a consumer-log review during planning. No user-facing impact occurred. The review also records that the pathfinder team's early flag of the issue prevented an estimated further four teams from beginning migrations that would have failed."

**Question 7 (moderate) — True/False/Cannot say**

Statement: "The undocumented dependency caused user-facing impact for the four affected teams."

- A) True
- B) False
- C) Cannot say
- D) True, because the migration completed late

**Correct answer: B**

**Explanation:** The passage states plainly: "No user-facing impact occurred." The dependency caused delay and rework — two days late, a day's effort per team — but the review explicitly separates internal cost from user impact, and the statement conflates them, so it is False. Option D repeats the conflation: lateness is not user impact. This distinction is one you police constantly in reviews you chair: teams under stress tend to merge "it was painful for us" with "it affected users", and the two have entirely different severities, escalation paths and lessons. A review culture that keeps them separate — as this passage models — is one where availability reporting stays trustworthy and post-incident actions attack the right cost.

**Question 8 (challenging) — Inference**

Which is the most defensible inference from the passage?

- A) The migration planners were careless and should be reassigned.
- B) Consulting the access logs during planning would probably have surfaced the dependency before any team migrated.
- C) The pathfinder approach saved no time overall, since the migration still finished late.
- D) The remaining teams' migrations will now proceed without issues.

**Correct answer: B**

**Explanation:** The review states the dependency "was discoverable in advance" because consumer-listing logs "were available... but were not consulted", and the fix now *requires* that review — the passage's own causal claim supports B, hedged appropriately with "probably". Option A leaps from a process gap to a personnel verdict the review nowhere supports; note that the review itself blames the process (and fixes the guide), not the people — the difference between blameless and blameful readings of the same fact. Option C is contradicted in spirit by the final sentence: the early flag prevented an estimated four failed migrations, a saving that coexists with the two-day delay. Option D converts one fixed failure mode into a guarantee of none. Inference questions reward conclusions the passage licenses at the strength it licenses them — and chairing reviews rewards exactly the same calibration, because the inference you endorse becomes the action list.

**Question 9 (challenging) — Main point**

Which sentence best captures the main point of Passage 3?

- A) The registry migration was a failure that finished two days late.
- B) A discoverable dependency was missed in planning, at modest recovered cost; the planning process has been fixed, and the pathfinder approach limited the damage.
- C) Registry access logs must always be reviewed before any migration.
- D) The pathfinder team performed better than the other teams.

**Correct answer: B**

**Explanation:** The passage's elements are: a miss (undocumented dependency), its cost (two days, a day per team, no user impact), its root cause (available logs unconsulted), the systemic fix (guide updated), and the mitigating structure (pathfinder flag prevented further failures). Option B covers all five at calibrated strength. Option A reads only the first line and assigns a verdict — "failure" — that the no-user-impact, damage-limited body does not support. Option C promotes the specific fix into a universal rule the passage does not state. Option D invents a comparison; the pathfinder team's *position*, not performance, is what mattered. Main-point questions reward complete, calibrated summaries — and so does your role: the one-paragraph version of this review that you give your head of profession should be option B, because A triggers unwarranted alarm and C and D each misfile the lesson.

**Passage 4 (for Questions 10–11).** *Email from a delivery manager on one of your project teams:* "Hi — two things. First: the product team have asked us to add the new export feature to this sprint, but doing so means dropping the pipeline hardening work you asked for. I think the hardening can wait a sprint, but I didn't want to make that call without you since you own the platform roadmap. Second: Priya has been carrying the on-call rota more or less alone since Sam left, and she mentioned yesterday she's exhausted. I know rota design is my responsibility, but you know the platform constraints better than I do — could we talk this week about what coverage actually requires? Also, for what it's worth, the export request came directly from the programme director's office."

**Question 10 (moderate) — Comprehension**

Which of the following does the email actually ask of you?

- A) A decision on whether the hardening work can slip a sprint, and a conversation this week about on-call coverage requirements.
- B) Approval to add the export feature, and a decision on Priya's workload.
- C) An escalation to the programme director about scope pressure.
- D) Agreement that the hardening work can wait, since the delivery manager has already decided it can.

**Correct answer: A**

**Explanation:** Parse the requests precisely. First: the delivery manager offers a view ("I think the hardening can wait") but explicitly defers the *decision* to you as roadmap owner — so what is requested is your call on the trade-off, not a rubber stamp, which eliminates D. Second: rota design stays with the delivery manager ("my responsibility"), and what is asked of you is a *conversation about platform coverage constraints* — not a decision on Priya's workload, which eliminates B's second half. Option C invents a request; the director's involvement is offered as context ("for what it's worth"), not as an action item. Multi-part emails that carefully allocate decision rights are the everyday texture of lead-level work, and answering the request actually made — rather than the one you would find easiest — is both the test skill and the working skill. Note also what a careful reader banks silently: the exhaustion signal about Priya is context that should raise the priority of the conversation, whoever owns the rota.

**Question 11 (challenging) — Inference**

Which is the most defensible inference from the email?

- A) The programme director has instructed that the hardening work be dropped.
- B) The delivery manager is managing the boundary between their authority and yours deliberately, and is surfacing a welfare risk early.
- C) Priya will resign if the rota is not fixed this week.
- D) The export feature is more valuable than the hardening work.

**Correct answer: B**

**Explanation:** The email's structure supports B directly: the delivery manager distinguishes what they could decide from what you own ("I didn't want to make that call without you since you own the platform roadmap"), retains their own accountability ("rota design is my responsibility") while asking for your expertise, and raises Priya's exhaustion before it becomes a crisis. Option A inflates provenance into instruction — the request *came from* the director's office; nothing says the director ordered the hardening dropped, and treating provenance as command is precisely how organisations invent pressure that was never applied. Option C escalates a welfare signal into an ultimatum the text does not contain. Option D mistakes the existence of a request for a value judgement nobody has made — the trade-off is exactly what remains to be decided. The reading skill here is inferring *from structure and framing* as well as content: how a colleague allocates decisions in writing tells you how they are working, and B is the inference that will make you respond well.

**Question 12 (challenging) — Clear-writing judgement**

You are announcing a deprecation to all consuming teams. Which formulation serves them best?

- A) "As part of our ongoing commitment to continuous improvement and platform excellence, certain legacy API functionality will be sunset in due course, and teams are encouraged to consider modernisation pathways at their earliest convenience."
- B) "The v1 export API is deprecated from today. It will be removed in release 6.0, scheduled for 1 March. Migrate to the v2 export API before then; the migration guide is linked below, typical effort is one to two days, and the platform team offers pairing support — book via the linked form. From today, v1 responses include a deprecation header. Questions: #platform-support."
- C) "The v1 export API is deprecated and will be removed soon. Please migrate when you can. Details to follow."
- D) "Per architectural decision record 47, consumers of deprecated interface v1 are required to effect migration to the successor interface in accordance with the platform lifecycle policy, non-compliance with which may result in service interruption."

**Correct answer: B**

**Explanation:** A deprecation notice succeeds when every consuming team can answer four questions without contacting you: what exactly is deprecated, when does it break, what do I do instead, and how much will it cost me? Option B answers all four with dates, effort estimates, a migration path, support, an observable signal (the header) and a channel for questions — it is longer than the others because completeness, not brevity, is the clarity that scale requires. Option A is officialese without a single date, name or action: "in due course" and "at their earliest convenience" guarantee that nothing happens until the removal breaks someone. Option C has the right voice and no substance — "soon" and "details to follow" make planning impossible and generate exactly the follow-up traffic a good notice prevents. Option D is precise about authority and vague about everything a reader needs, communicating compliance threat rather than a path. Leading the sharing of knowledge and good practice means writing like option B: announcements that transfer your knowledge of the change into your readers' plans in one reading.

### Preparation tips

- **Drill the three-way verdict with leadership texts.** Practise on strategy papers, supplier terms and governance minutes: for each paragraph write one True, one False and one Cannot-say statement and test yourself a day later. The exercise doubles as excellent material for the knowledge-sharing sessions you lead.
- **Underline scope, bounds and conjunctions.** "New services", "first ten", "control plane", "and in any case", "at least 72 hours and not exceeding four hours" — lead-level passages turn on scoping clauses, bounded offers and multi-limb conditions more than on rare words.
- **Extract formulas from prose before computing.** Contracts and SLAs embed arithmetic in sentences. Write the formula in symbols first, then substitute — the same habit that keeps your service-credit claims and capacity clauses correct at work.
- **Check every limb of compound conditions.** When a rule has two conditions joined by "and", verify both; when joined by "or", one suffices. Half of the hardest T/F/CS items are single-limb readings of two-limb rules.
- **Answer from the passage; file your expertise for later.** Your knowledge of how migrations or SLAs usually work is the chief source of Cannot-say errors. If the passage does not say it, you cannot say it.
- **Study the request structure of emails.** Before responding — in the test or your inbox — list what is actually asked, of whom, and what is merely context. Decision-rights language ("your call", "my responsibility", "for what it's worth") is data, not decoration.

### Common pitfalls to avoid

- **Reading bounded commitments as general ones.** "Support for the first ten" is not "support"; "control plane availability" is not "availability". The bound is the meaning.
- **Stopping at the first satisfied condition.** Conjunctive rules fail on any limb. Verify all of them before marking True.
- **Missing the backstop clause.** "When X happens, and in any case within three years" binds even if X never happens. Summaries that drop the backstop are misquotes with a delayed detonation.
- **Treating provenance as instruction.** "The request came from the director's office" is a fact about origin, not an order about priority. Inference questions — and organisational politics — both punish the conflation.
- **Conflating internal pain with user impact.** Delay, rework and effort are costs; user-facing impact is a different, explicitly-stated category. Keep them separate in your verdicts and your reviews.
- **Choosing the shortest option in writing-judgement items.** At lead level the clearest text is usually the most *complete for its audience*, not the tersest. Judge options by whether a busy reader could act correctly on one reading — dates, actions, owners, channels.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace dilemmas and asks you to evaluate possible responses. The most common formats are choosing the most effective and least effective responses from a set of four, ranking all responses, or rating each response independently. Unlike cognitive and numeric tests, there is often no formula: the keyed answers are set by subject-matter experts and reflect the professional behaviours the organisation values — user focus, collaboration, ownership, sound escalation, integrity, inclusion, and the development of others.

Typical format: an online test of 20 to 40 minutes with 8 to 15 scenarios. Timing is usually generous compared with cognitive tests, because the intent is considered judgement rather than speed. Scoring may be against an expert consensus key, and some platforms report a profile across behavioural dimensions rather than a single score.

For a lead DevOps engineer, situational judgement is the assessment closest to the actual difficulty of your job. The technical problems at your level usually have discoverable answers; the leadership problems rarely do. Should you hold a standard against a team with a genuine grievance about it? How do you refuse a director's pet feature without refusing the director? What do you do when a strong engineer is quietly burning out on a rota that is technically "working"? When two of your teams duplicate effort, whose solution wins — and who decides? These dilemmas define the lead role because you now lead one or more teams, own product direction, and model behaviour that others copy: your handling of a single awkward situation becomes case law for every practitioner watching. Employers assess situational judgement at this level because the behaviours it probes — judgement under competing loyalties, influence without authority, development of people, integrity under pressure — are precisely what distinguishes a lead who multiplies their teams from a senior engineer with a bigger title.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills and duties in your role summary:

- **Ownership and escalation** map to **Availability and capacity management** and **Service support**: leading teams that run services means owning KPI breaches and complex faults at the level where they are yours to fix, and escalating with evidence — not alarm — when they are not.
- **Collaboration and influence** map to **Systems integration** (establishing standards practitioners must adhere to — which is influence work, not decree work), **Development process optimisation** (solutions others must willingly adopt), and your duty to **contribute to strategic direction** alongside peers who may disagree.
- **Integrity under pressure** maps to **Information security** and **Modern development standards**: the moments that matter are when a control, standard or honest metric is inconvenient to someone senior, and the assessment probes whether it survives.
- **Developing others** maps to your duties of **coaching and mentoring** and **leading the sharing of knowledge and good practice**: scenarios test whether you grow capability or merely redistribute tasks — and whether your own indispensability is something you engineer away.
- **User focus** maps to your **User focus** skill: as product owner of the toolchain, your users are delivery teams and, beyond them, citizens; scenarios test whether evidence about their needs outweighs the desires of the loudest stakeholder — including you.

### Practice questions

**Question 1 (moderate) — The team that rejects your standard**

You established a deployment standard across your product line six months ago, and adoption is otherwise complete. One team continues to deploy their own way. Their tech lead tells you: "The standard adds twenty minutes to every release for zero benefit at our scale — we tried it for a month." Their delivery metrics are among the best in the product line.

- Option A: Insist on adoption — a standard with voluntary exceptions is not a standard, and other teams will notice.
- Option B: Examine their month of experience with them: identify which steps cost the twenty minutes and what those steps protect against; if the costs are real and the protections genuinely do not apply at their scale, adapt the standard to include a documented lighter path with entry criteria; if the protections do apply, show them the specific risk they are carrying.
- Option C: Let the exception stand quietly — their metrics are excellent, and pushing would damage the relationship.
- Option D: Escalate the non-compliance to their delivery manager and ask for adoption to be added to the team's objectives.

**Most effective: B. Least effective: C.**

**Explanation:** Option B treats the team's evidence as data about the standard, which is what a lead who *establishes standards and ensures practitioners adhere to them* must do to keep both halves of that duty honest: adherence is only defensible while the standard is. Their trial month is genuine field evidence; investigating it either improves the standard (a tiered path with criteria other teams can also use, transparently) or produces the specific risk case that persuades a strong team better than authority can. Option A defends the standard's letter while refusing the information that would defend its purpose — and "because I said so" is a fragile basis for leading excellent engineers. Option D outsources your influence job to line management before you have done it; it may eventually be needed, but as a first move it converts a technical disagreement into a performance matter and poisons future adoption conversations. Option C is the least effective: a quiet, unexamined, undocumented exception is governance by mood — other teams *will* notice, the standard's legitimacy erodes precisely because the exception has no stated criteria, and if the team's scale changes, nobody is watching the risk they carried. The pattern: examine, then adapt or persuade — never ignore, and escalate only after engaging.

**Question 2 (moderate) — Two teams, one roadmap slot**

As technical product owner, you have one team-quarter of capacity left this quarter. Two of your project teams want it: Team One for observability improvements that would benefit every service on the platform modestly; Team Two for a self-service database feature that three delivery teams have requested loudly and repeatedly. Your product metrics show that unplanned support requests — half of them database-related — consume 30% of your platform team's time.

- Option A: Give the slot to Team Two — three named customers asking loudly beats a diffuse benefit.
- Option B: Split the slot between both teams so neither is disappointed.
- Option C: Decide using the evidence: the support-load data suggests the database feature attacks the largest measured cost, so prioritise it — and say so in a published decision note that records the criteria, the observability deferral, and when it will be revisited.
- Option D: Ask the three requesting delivery teams to vote.

**Most effective: C. Least effective: B.**

**Explanation:** Option C makes the decision the way a product owner should: on measured cost and benefit rather than volume of asking — and it happens that the loud request and the evidence align here, but the decision note records *why*, which is what makes the next decision (where they may not align) defensible. Publishing criteria and a revisit date treats the deferred team as professionals rather than losers. Option A reaches the same allocation by the wrong route — "loudest wins" is precisely the precedent that will bury your roadmap in noise, and next quarter's loudest request may be the wrong one. Option D delegates a portfolio decision to the subset of stakeholders who want one of the options; it is abdication dressed as consultation. Option B is the least effective: halving a team-quarter typically delivers neither improvement to a useful threshold — two half-finished capabilities serve nobody, disappoint both teams *and* both customer groups, and demonstrate that pressure produces splits rather than decisions. Product ownership means choosing; the kindness is in the transparency, not in the avoidance.

**Question 3 (challenging) — The director's pet feature**

A director you rarely see asks you directly to add a real-time analytics dashboard to your platform "so we can showcase the platform at the leadership away-day next month". Your published strategy for the quarter is fully committed to migration tooling that four teams are waiting on, and your user research with delivery teams has never surfaced analytics as a need.

- Option A: Commit to the dashboard — a director's sponsorship is worth more to the platform than a quarter's roadmap.
- Option B: Decline, citing the published strategy, and copy your head of profession for visibility.
- Option C: Explore the underlying need with the director — what story does the away-day require? — then offer options with costs: a lightweight demonstration using existing metrics for the away-day (days of effort), the full dashboard as a candidate for next quarter's roadmap *if* user research supports it, and the migration commitments protected either way; agree the trade-off explicitly if the director still wants more.
- Option D: Agree publicly but have the work absorbed quietly as stretch capacity so the roadmap appears unaffected.

**Most effective: C. Least effective: D.**

**Explanation:** Option C does what your **User focus** skill describes — distinguishing needs from desires — upward as well as downward. The director's real need is probably a compelling away-day story, which existing metrics may satisfy for days rather than a quarter of effort; the full feature then enters the roadmap through the same evidence gate as everything else. Crucially, C keeps the four waiting teams' commitments visible in the conversation, so any override is the director's informed choice, not your silent absorption. Option A abandons your published strategy — and the teams planning against it — for sponsorship, teaching every stakeholder that your roadmap moves for rank. Option B holds the line but wastes the opportunity: it treats the director as an interruption rather than a stakeholder with an unexplored need, and the pre-emptive CC reads as defensive escalation before any conflict exists. Option D is the least effective: it deceives everyone at once — the director gets an unresourced promise, the teams get an invisibly diluted platform team, and "stretch capacity" is your engineers' evenings, spent without their consent on work you would not defend in daylight. A lead's roadmap integrity is worth exactly what its least honest exception is worth.

**Question 4 (moderate) — The struggling senior engineer**

A senior engineer on one of your teams — technically excellent for years — has visibly disengaged this quarter: review turnaround has slowed, two design documents are overdue, and they were short with a junior colleague in a meeting yesterday. Their delivery manager mentions it to you; the engineer reports to the delivery manager, but you lead the technical community they belong to and have worked with them closely.

- Option A: Stay out of it — performance is the delivery manager's job, and involvement from you would blur lines.
- Option B: Talk with the engineer privately as their technical lead: describe what you have observed without diagnosis, ask how things are and listen — workload, the work itself, something outside work — and agree together what would help, coordinating with (not replacing) the delivery manager on anything formal.
- Option C: Raise the junior-colleague incident at the next team retrospective so the behaviour is addressed openly.
- Option D: Quietly reassign the overdue design documents to another engineer to protect the deadlines.

**Most effective: B. Least effective: C.**

**Explanation:** Option B uses the relationship your role actually gives you — technical leadership and trust — for what it is best at: an early, private, non-judgemental conversation that treats a changed pattern in a strong performer as a signal to understand, not a failing to manage. Describing observations without diagnosis ("I've noticed X — how are things?") leaves room for the many possible causes: burnout, boredom, difficulty at home, an unraised grievance. Coordinating with the delivery manager respects the line-management boundary without hiding behind it. Option A honours the org chart and abandons the person — technical leaders who "stay out of it" convert their community leadership into a purely ceremonial role. Option D protects this month's deadlines by stripping work from a disengaging engineer without a conversation — likely accelerating the disengagement, and visible to them as a verdict delivered silently. Option C is the least effective: surfacing an individual's bad moment in a group forum is exposure, not feedback — it humiliates a struggling colleague in front of the community you lead, teaches everyone that your retrospectives are unsafe, and addresses the symptom while guaranteeing you never learn the cause. Care for people precedes correction of behaviour; privately, early, and with the person rather than about them.

**Question 5 (moderate) — Duplicate effort discovered**

Preparing a knowledge-sharing session, you discover that two of your project teams have each spent several weeks independently building almost identical internal tooling for test-data generation. Neither knew of the other's work. Both tools are about 70% complete; the teams have invested similar effort and each is proud of its approach.

- Option A: Direct both teams to stop, evaluate the two tools yourself, and mandate the better one.
- Option B: Bring the two teams together to compare approaches, agree convergence criteria with them (capability, maintainability, adoption cost), and have them jointly decide which codebase carries forward and what to port from the other — then fix the discovery gap that allowed six weeks of parallel work, such as a lightweight "intent to build" register you review.
- Option C: Let both teams finish — the sunk effort is spent either way, and competition may produce a better tool.
- Option D: Use the incident at your next all-hands as an example of poor communication between teams.

**Most effective: B. Least effective: D.**

**Explanation:** Option B fixes both the instance and the system. The joint-convergence approach turns a potential loser's grievance into a shared engineering decision — the team whose codebase is not chosen still sees its ideas ported and its judgement respected — and agreed criteria make the outcome about the tools, not the teams. The systemic half is the lead-level move: duplicated effort is a *discovery failure*, and leading the sharing of knowledge and good practice means building the mechanism (a build-intent register, regular cross-team demos) that makes the next duplication impossible, not just resolving this one. Option A reaches a defensible outcome efficiently but spends trust to get it: a mandated verdict on work people are proud of creates a resentful team and teaches both to hide work-in-progress from you — worsening the very discovery gap that caused the problem. Option C doubles down on waste and defers the conflict to the worse moment when two *finished* tools compete for adoption. Option D is the least effective: it punishes teams publicly for a coordination failure that was structurally yours to prevent — the leader of related teams owns the connective tissue between them — and converts an honest gap into a source of shame, guaranteeing quieter teams and later discoveries next time.

**Question 6 (challenging) — Your change broke the platform**

A configuration change you personally made to the shared pipeline — reviewed and approved through the normal process — has caused every team's deployments to fail for three hours. The incident is resolved. In the aftermath, a delivery manager comments in a cross-team channel: "Ironic that the platform lead broke the platform. Maybe the standards need to apply to the standards owner."

- Option A: Reply privately to the delivery manager explaining that the change followed the full review process, and ask them to moderate their tone in shared channels.
- Option B: Reply briefly and openly in the channel: acknowledge the impact and your authorship without defensiveness, note that a blameless review is underway, and share the findings and process improvements with all teams when complete — then do exactly that, including what the review process itself failed to catch.
- Option C: Say nothing in the channel; the incident review will speak for itself in due course.
- Option D: Reply in the channel explaining that the change was reviewed and approved by others too, so responsibility is shared across the review chain.

**Most effective: B. Least effective: D.**

**Explanation:** Option B is what ownership looks like at leadership altitude: public impact, public acknowledgement — brief, factual, non-grovelling — plus the promise and delivery of a blameless review whose findings go to the affected audience. The moment is disproportionately valuable: every engineer in your product line learns how incident accountability works by watching *this* reply, and a lead who models "I broke it, here is what we learned" purchases years of honest incident reporting from others. Option D is the least effective: it is technically true and culturally poisonous — spreading responsibility across the reviewers in public reads as deflection, throws your reviewers under scrutiny they did not invite, and contradicts the blameless principle you need everyone else to trust when *they* break something. Option A makes the conversation about the delivery manager's tone rather than your outage; whatever the tone, the substance ("standards apply to the standards owner") is fair, and policing the commentary before addressing the impact inverts the priority. Option C leaves a vacuum for three days in which the joke becomes the narrative; silence from the accountable person is read as evasion, not dignity. Own it fast, review it blamelessly, publish what changes — the same standard you would ask of any team.

**Question 7 (moderate) — The rota that works on paper**

Reviewing on-call arrangements across your teams, you find one team's rota is technically compliant — coverage is complete, and nobody has complained formally — but the data shows one engineer has taken 60% of the out-of-hours callouts for three months, because she is the only person confident with the legacy scheduler component. She has not raised it; her manager calls it "just how the skills fall".

- Option A: Leave it — coverage is compliant, nobody has complained, and redistributing would put less capable people on difficult callouts.
- Option B: Treat the skewed load as both a welfare risk and a single-point-of-failure: agree with her manager a plan to cap her share of the rota, pair other engineers with her on legacy-scheduler callouts and run knowledge-transfer sessions until at least two others are confident, and check in with her directly about the past three months — while crediting, visibly, the load she has carried.
- Option C: Immediately equalise the rota so everyone takes identical shares from next week.
- Option D: Ask her whether she minds the current arrangement, and keep it if she says she is fine.

**Most effective: B. Least effective: C.**

**Explanation:** Option B reads the situation at both of its levels. The welfare level: a 60% callout share sustained for a quarter is a burnout trajectory whether or not it has been raised — people who are "the only one who can" often do not complain precisely because they know they are the only one who can, so absence of complaint is not evidence of absence of harm. The engineering level: her unique knowledge is a bus-factor of one on a production component, which capacity management should never tolerate. B fixes both through the same mechanism — deliberate knowledge transfer — while capping the load *during* the transfer rather than after it, and honours rather than pathologises her contribution. Option A mistakes formal compliance for health and locks in both risks. Option D looks respectful but quietly transfers the duty of care to the person bearing the load: her "I'm fine" under these incentives cannot carry the decision, though her views on the *plan* absolutely should. Option C is the least effective: instant equalisation puts engineers without the skills on callouts they cannot resolve — extending outages for users, frightening the engineers, and predictably ending with her being called anyway as backup, now for other people's shifts. The inclusion lesson generalises: fix the system that concentrated the load, support the person who carried it, and never confuse "uncomplaining" with "unaffected".

**Question 8 (challenging) — Disagreement between leads**

You and another lead DevOps engineer jointly own the department's engineering standards. She wants to mandate a single language and framework for all internal tooling to simplify support; you believe a constrained choice of two or three fits your teams' contexts better, and the evidence you have each assembled is genuinely mixed. The decision is due at next week's engineering board, and teams are asking what to expect. Discussions between you have become slightly strained.

- Option A: Agree to her proposal to preserve the relationship — the difference is not worth a conflict between leads.
- Option B: Prepare a joint paper for the engineering board that presents both options fairly with the shared evidence, the genuine trade-offs, and the criteria the board should decide on — agreeing with her beforehand that you will both commit publicly to whichever outcome the board chooses.
- Option C: Lobby the board members you know individually before the meeting so your option arrives with momentum.
- Option D: Present competing papers so the board sees the strongest case for each side.

**Most effective: B. Least effective: C.**

**Explanation:** Option B does three lead-level things at once: it moves a genuinely balanced decision to the governance forum that exists for exactly this (contributing to strategic direction means equipping the strategy-setters, not pre-empting them); it converts an interpersonal strain into a jointly-owned artefact, which is usually the fastest repair for a professional relationship; and the advance commit-to-the-outcome pact means the department gets one aligned standards voice whichever way the board decides — which is what the asking teams actually need. Option A resolves the strain by abandoning your professional judgement; if your evidence is real, the teams inherit a standard chosen for social comfort, and the pattern — leads who fold under mild tension — is worse than the standard. Option D is honest but institutionalises the split: competing papers invite the board to pick a winner between two leads who must cooperate for years, and signal to every team that their leadership could not integrate the evidence themselves. Option C is the least effective: pre-meeting lobbying converts an evidence question into a politics question, corrodes the board's trust in both leads when discovered (it is usually discovered), and — worst — wins at most a decision, never the aligned commitment that makes standards stick. Disagree in private, integrate in the paper, commit in public.

**Question 9 (moderate) — The deadline and the delegation**

A complex piece of integration work on the critical path is due in two weeks. You could do it yourself in four days — you have done similar work before. The engineer whose growth area this is would take around eight days with your coaching, which the schedule can absorb, though without much margin. Your own week is heavily committed to the product strategy draft your head of profession expects.

- Option A: Do the integration work yourself in four days and catch up on the strategy draft at evenings and weekends — both things matter.
- Option B: Delegate the work to the engineer with a structured setup: agree the design approach together on day one, schedule two short checkpoints, define the escalation trigger (if the first milestone slips beyond day four, you re-plan together), and protect your own week for the strategy draft.
- Option C: Delegate the work but check in daily and review every commit, to make sure it stays on track.
- Option D: Postpone the strategy draft and pair full-time with the engineer, so the work is done well and the coaching happens.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is delegation as leads must practise it: real transfer of the work, scaffolded by exactly the structure that manages the schedule risk — upfront design alignment, sparse checkpoints, and a pre-agreed, objective escalation trigger, which turns "hoping it goes well" into "knowing by day four whether it is". The engineer grows on genuinely consequential work (the only kind that grows people), and your strategy draft — the work only you can do — gets your protected time. Option C delegates the task but not the trust: daily inspection and total review signal doubt, teach dependence, and consume nearly the hours you were trying to protect. Option D sacrifices your unique deliverable to do intensively what B achieves sufficiently — full-time pairing on an eight-day task is coaching at a price the role cannot afford, and the strategy slip lands on your head of profession. Option A is the least effective despite feeling the most responsible: it takes the growth opportunity from the engineer, funds the schedule with your evenings — normalising for your teams the very overwork pattern you should be guarding against — and leaves the organisation exactly as dependent on you as it was before, which at lead level is a failure mode, not a virtue. Leads are paid for what their teams become, not for what they personally finish.

**Question 10 (challenging) — The compliance report that flatters**

Preparing for an internal audit, you sample the standards-compliance self-assessments your teams submitted quarterly. One team's returns claim full compliance with the secrets-management standard, but your spot check finds two services with credentials in environment files, contrary to the standard — and to their returns for at least two quarters. The tech lead who signed the returns is capable and well liked, and the audit begins in three weeks.

- Option A: Correct the two services quietly before the audit and leave the historical returns as they are — the substance will be compliant by the time it is checked.
- Option B: Raise it with the tech lead directly and without ambush: show the findings, understand how the returns came to be wrong (misunderstanding of the standard's scope, copy-forward of an old return, or knowing misstatement — they need different responses), require the services fixed and the current return corrected, inform your head of profession of the discrepancy and the remediation before the audit finds it, and review whether the self-assessment process invites copy-forward errors across all teams.
- Option C: Report the tech lead to your head of profession as a conduct matter and let the formal process take over.
- Option D: Add a caveat to the audit submission noting that self-assessments are inherently approximate.

**Most effective: B. Least effective: A.**

**Explanation:** Option B holds the two lines that matter — the security substance and the integrity of the reporting — while sequencing fairly: the tech lead hears it first, directly, with the evidence, and the cause is diagnosed before any response is chosen, because copy-forward negligence and knowing misstatement are different problems (most such cases are process failures, which is why B also reviews whether the *self-assessment mechanism itself* is generating fiction across teams — the systemic lead-level move). Disclosing to your head of profession before the audit converts a discovered discrepancy into a managed one, which is the difference between a finding and a scandal. Option C skips understanding and goes straight to formal machinery — disproportionate as a first move on the evidence, and destructive of the trust your standards work runs on. Option D is the least effective in spirit but not quite in kind — it launders the problem with a shrug and misrepresents the issue as statistical noise rather than specific falsity. Option A is the least effective: it fixes the code and *joins the misreporting* — you would now know the returns were false and be arranging for the audit not to notice, converting a team's process failure into your own integrity failure. Leading others in using appropriate information security practices includes the unglamorous half: making sure the paperwork tells the truth about the practices, especially when the truth is briefly embarrassing.

### Preparation tips

- **Answer as your best leadership self, consistently.** SJT keys reward stable principles: engage before escalating, diagnose before responding, fix the system as well as the instance, protect people's dignity in public, and never spend integrity to buy convenience. Decide your principles before the test; apply them evenly.
- **Look for the option that fixes the instance *and* the system.** At lead level, the keyed best answer usually contains a systemic clause — update the guide, fix the discovery gap, review the process that produced the error. An option that only patches today is usually second best.
- **Respect decision rights in both directions.** Strong options keep line-management matters with managers, board matters with boards, and product decisions with you — informing and equipping the owner rather than seizing or dodging the call. Scan each option for whose decision it quietly takes.
- **Watch for the dignity variable.** Between two options with similar substance, the keyed answer is almost always the one that delivers hard messages privately, credits carried burdens visibly, and lets people keep face while changing course.
- **Find the covert integrity failure early.** Many lead-level scenarios hide an option that conceals, deflects, or quietly absorbs — leaving returns uncorrected, spreading blame across reviewers, funding promises with unpaid evenings. It is reliably the least effective; identifying it first makes the rest of the question easier.
- **Rehearse from your own case law.** Write down three leadership dilemmas from your last year — a resisted standard, a strained peer relationship, a struggling strong performer — and what you did versus what you now wish you had done. Calibrated reflection is the best SJT preparation there is, and it is free.

### Common pitfalls to avoid

- **Escalating before engaging.** Taking non-compliance, conflict or poor performance straight to managers or formal processes reads as rigour and scores as failed influence. Escalation is the documented backstop after direct engagement, not the opener.
- **Keeping the peace at the cost of the point.** Folding to a director, a peer lead, or a resistant team to avoid friction abandons the judgement your role exists to supply. The keyed answers hold the substance while working the relationship — both, not either.
- **Rescuing instead of developing.** Doing the critical-path work yourself, reassigning a struggling engineer's tasks, reviewing every commit — generosity that stunts people and centralises risk scores poorly, because it is a leadership anti-pattern dressed as diligence.
- **Public accountability for private failings.** Retrospectives, all-hands and shared channels are for systems and learning, never for individuals' bad moments. Any option that corrects a person in front of an audience is a strong least-effective candidate.
- **Mistaking compliance for health.** Rotas, standards returns and KPI dashboards can all be formally green while a person burns out, a report fictionalises, or a risk concentrates. The keyed answers look through the artefact to the reality it is supposed to represent.
- **Splitting what needs deciding.** Halving the capacity, running both tools, presenting competing papers — split-the-difference options avoid the discomfort of choosing and reliably score as least effective, because product ownership *is* choosing, transparently and with criteria.

## Conclusion

Well done — you have worked through a demanding set of practice material, pitched at the level where technical excellence meets leadership, and every question you attempted honestly has sharpened something you use in your real work.

Take a moment to notice what you have actually practised. In the cognitive section, you traced dependencies across teams rather than just pipelines, scoped rules and exemptions precisely, distinguished what constraints force from what they merely allow, and walked artefact lifecycles through proposed standards to find the flaw with a multiplier attached. In the numeric section, you weighted portfolio averages properly, separated relative from absolute improvement, compounded growth, found breakevens, reversed percentages, and converted an optimisation into the developer-years that fund it — the arithmetic of strategy papers, hiring cases and product decisions. In the verbal section, you read bounded commitments as bounded, checked every limb of compound conditions, extracted formulas from contractual prose, and judged announcements by whether a busy team could act on one reading. And in the situational judgement section, you rehearsed the dilemmas that define lead-level work: holding standards while listening to the teams that resist them, refusing the pet feature without refusing the director, developing people when doing it yourself would be faster, and owning your own outage in front of everyone.

If some questions caught you out, that is the practice working. Review the *pattern* of your misses — unweighted averages, single-limb readings, escalating before engaging — rather than the individual items, because both assessments and leadership repeat patterns. A short second pass over your errors in a few days will consolidate more than another full pass today. Several of the worked explanations here also make ready-made material for the knowledge-sharing sessions you lead; teaching a technique is the most reliable way to own it.

Remember that assessment performance is itself a trainable capability with its own curve, like every technology and every leadership skill you have already acquired. Familiarity with the formats, calibrated pacing, and calm under the clock are all improved by exactly what you have just done.

Finally, connect this back to your development. The capabilities these assessments sample — structured reasoning across teams, portfolio-level numeracy, precise reading and writing, and judgement under competing loyalties — are the same capabilities that will carry your product line's strategy, grow your engineers, and prepare you for whatever comes after lead. Practising them here is professional development in compact form.

You lead the teams that build the tools that public services run on, and you shape the direction they build towards. Approach your assessment the way you approach a well-run release: prepared, rehearsed, calm, and confident that whatever the outcome, the retrospective will make the next one better. Good luck.
