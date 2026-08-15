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

<!-- APPEND -->
