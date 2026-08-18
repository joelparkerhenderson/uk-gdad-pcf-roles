# Lead DevOps Engineer (Management) - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a lead DevOps engineer on the management track within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a promotion or a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your work leading teams, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a lead DevOps engineer with management responsibilities, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — product line roadmaps, toolchain strategies, team capacity plans, policy and standards proposals, incident trend reports, and budget lines for platform services — and the kinds of decisions you genuinely make, such as acting as technical product owner for a platform product line, developing medium to long term strategies, leading one or several related project teams, and leading the sharing of knowledge and good practice across them.

Why do these assessments matter for your role in particular? At lead level you have crossed a threshold: your primary output is no longer the work you do with your own hands but the direction, standards and capability of the teams you lead. You contribute to the strategic direction of your organisation's engineering, you set policy and standards for how change is implemented, and you develop the experts who deliver service improvements. Assessments of cognitive ability, numerical reasoning, verbal reasoning, and situational judgement map directly onto those demands. Practising them sharpens exactly the skills your role depends on: spotting the logical flaw in a multi-team migration plan before you commit three teams to it, interpreting a quarter's delivery and cost data before a portfolio review, extracting precise meaning from a policy consultation or a supplier contract summary, and choosing the most effective course of action when strategy, team wellbeing and a live service pull in different directions.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters for your role, a mapping of the assessment dimensions to the specific skills in the lead DevOps engineer capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format and timing you are likely to face. Second, attempt the practice questions honestly — commit to an answer before reading the explanation, and note how long each takes you. Third, treat every explanation as a mini-lesson: even where you answer correctly, the reasoning walkthrough will deepen your technique, and many explanations show how the same thinking pattern appears in your real work on strategy, standards and teams. Finally, use the preparation tips and pitfalls for self-reflection: they connect assessment performance back to your development as a leader who is still, at heart, an engineer.

Take your time, be kind to yourself, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic intelligence test, it presents you with the everyday materials of your job — in your case, product line roadmaps, multi-team dependency maps, standards documents, platform service catalogues, incident trend summaries, and migration plans — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group, and modern platforms often adapt question difficulty based on your previous answers: answer correctly and the questions get harder, so rising difficulty is usually a sign you are doing well. Employers usually receive a breakdown of speed versus accuracy rather than a single score, so working both quickly and carefully matters. You will normally be offered short, ungraded practice questions before the real test begins, so you can settle into the interface without pressure.

For a lead DevOps engineer, cognitive assessment is particularly relevant because your decisions now bind multiple teams at once. When you act as technical product owner for a product line, an error in your reasoning does not cost one engineer an afternoon — it can commit several teams to a flawed migration sequence, an inconsistent standard, or a roadmap whose dependencies cannot be satisfied. You must hold in mind how project teams' plans interlock, where a policy you set will collide with a team's local reality, and what follows logically when one product line's strategy changes. On the management track you also reason constantly about people: capacity, capability, succession, and where knowledge is dangerously concentrated. A well-designed cognitive assessment simulates precisely those demands in miniature.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Pattern recognition** maps to **Development process optimisation**: analysing current processes across several teams and identifying opportunities to optimise them means recognising recurring structures — the same bottleneck appearing in three pipelines, the same failure signature across product lines, the same workaround reinvented by every team — in large, messy operational data.
- **Logical deduction** maps to **Systems design**, **Systems integration** and your product ownership duty: reasoning validly from standards, dependency rules and strategic constraints to their consequences is how you plan integration builds across systems and how you test whether a medium to long term strategy is internally coherent.
- **Error checking** maps to **Modern development standards**: identifying and applying standards to support complex projects and programmes — and leading others in applying them — requires you to spot inconsistencies between artefacts quickly: a roadmap that contradicts a policy you set, a design that breaches a standard, a service catalogue entry that cannot be true.
- **Prioritisation** maps to **Availability and capacity management** and to leading a team of experts: identifying capacity issues, initiating remedial action, and deciding where your teams' scarce expert time goes all depend on ranking impact and urgency together across a wider portfolio than a single service.
- **Problem solving** maps to **Information security** and **Service support**: when your teams escalate the problems they cannot solve, you are the person who must decompose them, weigh hypotheses against evidence, and choose the intervention that fixes the cause — often across team boundaries where no one else has the full picture.

### Practice questions

**Question 1 (easy) — Pattern recognition in a service catalogue**

Your platform service catalogue requires each entry to follow the pattern `<product-line>/<service>/<tier>`, where tier is one of `critical`, `standard`, or `dev`. Reviewing entries submitted by your teams, you see:

1. `payments/gateway/critical`
2. `payments/ledger/standard`
3. `identity/critical/verify`
4. `identity/tokens/dev`
5. `notify/email/standard`

Which entry breaks the pattern?

- A) Entry 2
- B) Entry 3
- C) Entry 4
- D) Entry 5

**Correct answer: B**

**Explanation:** The pattern fixes the order: product line, then service, then tier. Entry 3 places the tier word `critical` in the service position and a service-like word `verify` in the tier position. All other entries conform. Catalogue conventions are the kind of standard you now own rather than merely follow: automation that routes alerts by tier, reports that aggregate by product line, and funding models that charge by service all depend on every entry parsing correctly. When you lead others in applying standards, the review comment that matters is not just "entry 3 is wrong" but "here is what silently breaks downstream when it is wrong" — that is what makes a standard stick across teams you do not sit with daily.

**Question 2 (easy) — Logical deduction from a policy you set**

You have set this policy for your product lines: "Every service must publish health metrics to the central monitoring platform, unless the service is scheduled for decommissioning within six months and an exception has been recorded in the risk log." A team reports: "Our reporting service does not publish health metrics to the central platform." Which one of the following conclusions must be true?

- A) The reporting service is scheduled for decommissioning within six months.
- B) The team has breached the policy.
- C) Either the service has a recorded decommissioning exception, or the policy has been breached.
- D) The central monitoring platform does not support the reporting service's technology.

**Correct answer: C**

**Explanation:** The policy is a conditional with a two-part exception (decommissioning within six months AND a recorded exception). From the facts given, you cannot tell whether the exception applies, so neither A nor B must be true individually — each is merely possible. D invents information. Only the disjunction in C is guaranteed. The discipline — deduce only what the information given guarantees — matters doubly when you wrote the policy yourself: policy owners are the people most tempted to assume breach, because they remember the rule more vividly than the exceptions they granted. Checking the risk log before challenging the team is both correct logic and correct leadership.

**Question 3 (easy) — Error checking a roadmap against strategy**

Your product line strategy states: (i) the legacy build system will be retired by end of Q4; (ii) no new services may adopt the legacy build system from Q1 onwards; (iii) all migration work is to be scheduled by the platform team, not by service teams individually. A draft roadmap from one of your teams shows: a new service adopting the legacy build system in Q2; migration of two existing services scheduled by the platform team in Q3; retirement of the legacy build system in Q4. How many strategy points does the draft roadmap breach?

- A) 0
- B) 1
- C) 2
- D) 3

**Correct answer: B**

**Explanation:** Check each point. Point (i): retirement is shown in Q4 — compliant. Point (ii): a new service adopts the legacy system in Q2, which is after Q1 — breach. Point (iii): the migrations shown are scheduled by the platform team — compliant. Exactly one breach. The trap is double-counting: the Q2 adoption feels like it should also threaten the Q4 retirement (a service adopted in Q2 must be migrated within months), and in real life you would raise that as a consequence — but the question asks how many stated points are breached, and only one is. Separating "what breaches the rules" from "what is unwise but compliant" is a distinction you use constantly when reviewing team plans: the first list is non-negotiable, the second is a conversation.

**Question 4 (moderate) — Prioritisation across a portfolio**

It is Monday morning. Four items compete for your attention:

1. One of your teams' citizen-facing services is degrading intermittently; the team is investigating but has asked you to join because the fault seems to involve a platform component your other team owns.
2. Your product line strategy paper is due to the architecture review board on Wednesday; it still needs the cost section written.
3. A line report has asked for an urgent conversation — they hinted in this morning's stand-up that they have received an outside job offer.
4. The quarterly knowledge-sharing session you host for all your teams is scheduled for tomorrow and has no agenda yet.

Which sequencing is most defensible?

- A) 1, 3, 2, 4 — live cross-team fault first, then the retention conversation, then the strategy paper, then the session agenda
- B) 2, 1, 3, 4 — the board deadline outranks everything
- C) 3, 1, 2, 4 — people always come first
- D) 1, 2, 4, 3 — delivery items first, people items later

**Correct answer: A**

**Explanation:** Item 1 is urgent and specifically needs you: a live degradation whose diagnosis spans two of your teams is exactly the cross-boundary problem a lead exists to unblock — no one else holds both halves of the picture. Item 3 comes next: a possible resignation is time-sensitive (offers expire), high impact (losing an expert affects your capability plan for quarters), and the request signals trust that a delay would spend. Item 2 has a real deadline but Wednesday allows Tuesday work; item 4 is tomorrow but is a bounded, delegable task — an ideal opportunity to ask one of your senior engineers to shape the agenda, which develops them and frees you. Option B privileges a document over a live service and a person in motion. Option C's rule fails because the fault is harming users now while the conversation can wait an hour. Option D defers a retention risk behind an agenda-writing task, mispricing both. Lead-level prioritisation weighs user harm, people risk and deadlines together — and looks for the item that can be delegated rather than sequenced.

**Question 5 (moderate) — Pattern recognition in cross-team incident data**

Reviewing the quarter's incident summaries across your four teams, you note the count of incidents whose root cause was classified "configuration error": Team A 2, Team B 3, Team C 11, Team D 2. The teams run services of similar complexity and change volume, but you recall that Team C is the only team whose configuration changes are not yet validated by the automated policy checks you introduced elsewhere. What is the most reasonable interpretation?

- A) Team C's engineers are less careful and need performance management.
- B) The data is consistent with the missing automated validation being a factor — worth verifying by checking whether Team C's incidents would have been caught by the checks, then prioritising the rollout.
- C) The classification is wrong; eleven configuration errors is implausible.
- D) Nothing can be concluded because teams classify root causes differently.

**Correct answer: B**

**Explanation:** The outlier is real — 11 against a cluster of 2-3 — and you hold a plausible explanatory variable: Team C uniquely lacks the automated validation. But "consistent with" is not "proven": option B's strength is that it pairs the hypothesis with a concrete verification (would the checks have caught these specific incidents?) before committing rollout effort. Option A leaps from an outlier to a people judgement while ignoring the known systemic difference — a leadership error as much as a logical one, since blaming people for system gaps corrodes trust and hides the fix. Option C rejects data for being inconvenient. Option D raises a fair caveat (classification consistency is worth checking) but uses it to abandon analysis rather than refine it. The lead-level habit: when you spot an outlier, ask "what do I know that differs about this case?" — and then test it, because the answer justifies investment in your process optimisation programme.

**Question 6 (moderate) — Deduction about multi-team migration sequencing**

Your migration plan has these rules: (i) Team A's services must migrate before Team B's, because B consumes A's APIs through the new gateway; (ii) Team A cannot start until the platform team delivers the landing zone, which will be ready at the start of month 2; (iii) Team A's migration takes one full month; (iv) Team B's migration must complete within one month of Team A completing, or B's temporary dual-running costs double. Team B's migration takes one month. What is the latest month in which Team B can start without doubling dual-running costs?

- A) Month 2
- B) Month 3
- C) Month 4
- D) Month 5

**Correct answer: B**

**Explanation:** Work through the chain. The landing zone is ready at the start of month 2, so Team A migrates during month 2 (one full month) and completes at the end of month 2. Rule (iv) attaches to completions: Team B must complete within one month of A completing, so by the end of month 3. B's migration takes one month, so completing by end of month 3 requires starting at the start of month 3 — starting in month 4 would complete at the end of month 4, one month late, doubling the dual-running costs. The latest compliant start is therefore month 3. The tempting error, option C, comes from attaching the "within one month" clause to B's start rather than B's completion — reading it as "B must start within a month of A finishing". Deadline clauses in migration plans and contracts bind to completions unless they say otherwise, and misreading them at your level turns into a real budget variance across teams. Before answering any sequencing question — or signing off any migration plan — identify which event each deadline clause actually binds to.

**Question 7 (moderate) — Error checking a standards matrix**

You maintain a compliance matrix for your product lines. Your standards say: (i) every `critical`-tier service must have a tested disaster recovery plan; (ii) every service, regardless of tier, must have a named service owner; (iii) `dev`-tier services must not hold production data. An extract reads:

| Service | Tier | DR plan tested | Named owner | Holds production data |
|---|---|---|---|---|
| Gateway | critical | Yes | Yes | Yes |
| Ledger | standard | No | Yes | Yes |
| Sandbox | dev | No | No | No |
| Tokens | critical | No | Yes | Yes |

How many services are non-compliant with the standards?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** Apply each rule only where it binds. Gateway: critical with a tested DR plan, named owner, and production data is unrestricted at critical tier — compliant. Ledger: standard tier, so rule (i) does not apply; it has an owner; production data is unrestricted at standard tier — compliant (its untested DR plan may be unwise, but no standard requires it). Sandbox: dev tier holding no production data satisfies rule (iii), but rule (ii) applies to every service and Sandbox has no named owner — non-compliant. Tokens: critical with an untested DR plan breaches rule (i) — non-compliant. Two services are non-compliant. The traps are over-flagging Ledger (importing a "DR plans are good practice" instinct into a compliance count) and under-flagging Sandbox (assuming dev-tier services escape universal rules). As the standards owner, precision in both directions is what keeps your compliance reporting credible to the teams measured by it.

**Question 8 (moderate) — Applied problem solving on a cross-team failure**

Two of your teams independently report that overnight batch deployments failed last night. You gather: both teams' pipelines failed at the artefact-download step; a third team's overnight deployment, which uses a regional mirror of the artefact repository, succeeded; the artefact repository's maintenance calendar shows a storage migration scheduled last night; daytime deployments today are succeeding. Which hypothesis best fits all the evidence?

- A) Both teams introduced coincidental pipeline bugs on the same evening.
- B) The artefact repository was unavailable overnight during its storage migration, affecting consumers of the primary repository but not of the mirror.
- C) The network between the teams' runners and all repositories failed overnight.
- D) The third team's pipeline is more robustly written.

**Correct answer: B**

**Explanation:** Test each hypothesis against every fact. Coincidental bugs (A) would not both localise at the artefact-download step, and would still fail today. A general network failure (C) should have affected the mirror-using team too. Pipeline robustness (D) does not explain why the failing step was artefact download in both cases, nor the timing correlation with the scheduled migration, nor today's recovery. B explains everything: the primary repository was down for migration overnight, its consumers failed at exactly the download step, the mirror's consumer was insulated, and service resumed by morning. Note what the diagnosis buys you beyond the fix: an action for your process optimisation backlog (should all teams use the mirror? should maintenance windows gate overnight deployments?) and a communication action (why did two teams not know about the maintenance window?). Lead-level diagnosis ends with system changes, not just explanations.

**Question 9 (challenging) — Multi-constraint scheduling of a strategy rollout**

You must schedule three events for your new toolchain strategy — the strategy briefing for all teams (B), the pilot team's cutover (C), and the lessons-learned review (R) — across five working days, Monday to Friday, at most one event per day. Constraints: (i) B must come before C, because the pilot team's context depends on the briefing; (ii) the head of engineering must attend B and is available only Tuesday and Friday; (iii) after C, at least one full working day of live running is needed before R can usefully review it; (iv) R must happen this week, because next week the pilot team is away. On which day must C take place?

- A) Tuesday
- B) Wednesday
- C) Thursday
- D) Friday

**Correct answer: B**

**Explanation:** Anchor the most constrained element first. B needs the head of engineering, so B is Tuesday or Friday; if B were Friday, C and R could not follow within the week, so B must be Tuesday. C must follow B, so C is Wednesday at the earliest. Now test the later options for C. If C were Thursday, the one full day of live running would be Friday, pushing R into next week — forbidden by constraint (iv). If C were Friday, both the live-running day and R would fall outside the week. So C on Wednesday is the only placement that works: Thursday provides the full day of live running, and R lands on Friday, satisfying every constraint. The method — place the least-free element, propagate consequences forwards, then eliminate the remaining options by testing them against the tightest deadline — is exactly how you pressure-test a rollout plan before committing teams to it. Notice also what the exercise reveals: the schedule that satisfies all constraints has zero slack, and a lead who sees that on Monday builds a fallback (a remote review next week, agreed in advance) rather than gambling the week on nothing slipping.

**Question 10 (challenging) — Deduction across knowledge concentration**

Your skills matrix shows: only engineers P and Q can operate the certificate infrastructure; only Q and R can operate the secrets platform; only P can administer the artefact repository. Q has resigned, leaving at the end of the month; R is on extended leave for the next two months; P is present. For the two months after Q leaves, which capabilities have no available operator apart from a single person, and which have none at all?

- A) Certificates: single person (P); secrets: none available; artefact repository: single person (P)
- B) Certificates: none available; secrets: single person (R); artefact repository: single person (P)
- C) Certificates: single person (P); secrets: single person (R); artefact repository: none available
- D) All three capabilities have no available operator

**Correct answer: A**

**Explanation:** Work through membership and availability. Certificates: operators are P and Q; Q has left, so only P — a single point of failure, but available. Secrets: operators are Q and R; Q has left and R is on leave for the window in question, so no available operator at all. Artefact repository: P alone, present — a single point of failure by design. So: certificates single-person, secrets none, artefact repository single-person — option A. The reasoning is simple set intersection with a time window, but the leadership content is why it appears here: this is the arithmetic behind succession planning and knowledge-sharing, and it is exactly what your duty to lead the sharing of knowledge and good practice exists to prevent. The correct real-world sequel: before Q's last day, prioritise secrets-platform handover — the capability that goes to zero — over the capabilities that merely thin to one, and put recurring cross-training on the calendar so the matrix never again depends on one resignation and one period of leave.

**Question 11 (challenging) — Prioritising remedial actions across product lines**

A portfolio review surfaces four issues: (1) a critical-tier service's failover has never been tested and its next scheduled test is in five months; (2) two teams are queueing an average of 90 minutes daily for shared build agents; (3) a supplier's managed database service, used by one product line, has announced end-of-support in ten months; (4) your incident data shows the same manual deployment step caused three minor incidents this quarter across different teams. You can commission substantial work on exactly one issue this quarter. Which is the strongest choice, and why?

- A) Issue 1 — an untested failover on a critical service is an unquantified availability risk that could realise at any time
- B) Issue 2 — it wastes the most engineer-hours per week
- C) Issue 3 — end-of-support is the hardest deadline
- D) Issue 4 — repeated incidents show active harm

**Correct answer: A**

**Explanation:** Compare the risks' shapes, not just their sizes. Issue 1 is the only one whose worst case is severe, immediate and unbounded: a critical-tier service whose failover has never been tested may not fail over at all, and the trigger (an infrastructure failure) can arrive any day — the five-month test date is a fact about the calendar, not about the risk. Issue 2 is a steady, quantifiable drain (roughly 7-8 engineer-hours daily) — significant, but bounded and tolerable for another quarter, and partially self-mitigating through scheduling behaviour. Issue 3 has the longest runway: ten months against a migration you control the timing of; it needs a plan this quarter, not the work. Issue 4 causes real but minor harm with a known cheap fix (automate the step) that may not need "substantial" commissioning at all — delegate it as routine improvement. The discriminating question for A versus D is severity times uncertainty: three minor incidents are a known small cost; an untested failover is an unknown, possibly total one, on your most important tier. Availability and capacity leadership means spending your scarce quarter where the tail risk lives.

**Question 12 (challenging) — Decomposing a strategic complaint**

The head of delivery tells you: "Your platform is slowing every team down." Before responding you gather data: average pipeline duration is 22 minutes (down from 30 last quarter); teams' median wait for a new environment is 9 days; the platform team's request queue has 40 open tickets, of which 28 are environment requests; deployment failure rates are stable at 4%. Which response addresses the evidence most directly?

- A) Dispute the claim — pipeline durations improved 27% this quarter.
- B) Accept the complaint applies to pipelines and commission further pipeline optimisation.
- C) Identify environment provisioning as the dominant bottleneck the complaint most plausibly refers to, and propose a self-service provisioning capability plus an interim triage of the 28 queued requests.
- D) Ask the head of delivery to tell every team to raise fewer tickets.

**Correct answer: C**

**Explanation:** Decompose the complaint against the data. Pipelines are improving and take minutes; environment provisioning takes days and dominates the request queue (28 of 40 tickets). A team's experienced "slowness" is governed by its worst wait, not its average one — nine days for an environment dwarfs any pipeline gain. Option A wins the argument and loses the customer: it answers a different metric from the one causing the pain. Option B optimises the part that is already improving. Option D punishes the demand signal instead of serving it. Option C names the dominant term, proposes the strategic fix (self-service, which removes the queue rather than working it faster) and an interim one (triage the backlog) — the paired horizon thinking your medium to long term strategy duty requires. The assessment habit: when a stakeholder's complaint arrives vague, locate the specific process whose numbers could generate that experience before accepting or disputing anything. It usually is one specific process.

### Preparation tips

- **Practise on portfolio-shaped artefacts.** Take a real multi-team plan, standards matrix or incident summary and hunt deliberately for rule breaches, infeasible dependencies and knowledge single-points. Lead-level questions are portfolio questions; train on portfolio material.
- **Anchor the most constrained element first.** In every scheduling or sequencing item, find the constraint with the least freedom (a person's availability, a fixed delivery date) and place it before reasoning about anything else.
- **Separate "breach" from "unwise".** Compliance counts want breaches of the stated rules only. Keep a mental second list for things that are compliant but concerning — in real reviews you raise both, but you never confuse them.
- **Check which event a deadline binds to.** "Within one month of completing", "before starting", "after delivery" — misattaching a clause to the wrong endpoint is the commonest sequencing error, in tests and in migration plans.
- **Time-box to 60-90 seconds per question in practice**, and learn your personal signal for "I am now guessing" — at that point, mark, move on, and return.
- **Name the technique as you use it.** Set intersection, transitive dependency, dominant-term analysis, conditional-with-exception: labelling the tool makes it retrievable under pressure, exactly as it does when you teach it.

### Common pitfalls to avoid

- **Assuming breach because you wrote the rule.** Policy owners over-detect violations. The exception you granted in March exists whether or not you remember it; deduce only what the stem guarantees.
- **Blaming people for system gaps.** When an outlier team lacks a control the others have, the missing control is the lead hypothesis — not the team's diligence. Tests and leadership both penalise the leap to blame.
- **Double-counting consequences as breaches.** A single non-compliant item often has several bad implications; count the breaches the question asks about, not the worries it inspires.
- **Measuring risk by its calendar date.** A test scheduled in five months does not make the underlying risk five months away. Distinguish when a risk could realise from when you plan to look at it.
- **Optimising the improving metric.** When a complaint arrives, the metric you have already improved is the one you will want to talk about and the one least likely to be the cause. Follow the worst wait, not the best trend.
- **Losing accuracy chasing the clock.** Adaptive difficulty rising means you are scoring. Keep the pace you calibrated in practice and never abandon method on the hard items — they are worth the most.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from numerical information of the kind your role genuinely produces. Rather than abstract arithmetic drills, it presents tables, charts and short data narratives — in your case, portfolio delivery metrics, availability and capacity figures across product lines, platform cost breakdowns, team utilisation and recruitment numbers, migration budgets, and supplier pricing comparisons — and asks questions requiring calculation, comparison and inference.

Typical format: an online, timed test lasting 20 to 35 minutes, usually 15 to 20 questions, each based on a data table or chart. A basic on-screen calculator is normally permitted, and every question is answerable from the data given — no outside knowledge of "real" figures is wanted. Scoring compares accuracy and speed against a norm group, and several questions may share one dataset, so time invested understanding a table pays back across questions.

For a lead DevOps engineer on the management track, numeric fluency is the difference between owning your product line's story and having it told to you. You act as technical product owner, which means the roadmap you defend at portfolio reviews rests on cost, capacity and delivery numbers; you set policy and standards, which means you must quantify their effect to justify them; you lead teams of experts, which means pay, recruitment, utilisation and on-call load arithmetic shapes your people decisions; and you contribute to strategic direction, which means projecting trends over quarters and years, not sprints. Employers assess numeric reasoning at this level because a lead who misreads a cost table commissions the wrong platform investment, and a lead who cannot challenge a supplier's percentage claims negotiates badly on the department's behalf.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Percentages and rates** map to **Availability and capacity management**: availability achieved against target, capacity utilisation, growth rates and error budgets across several product lines are the numbers on which you initiate remedial action — or decline to.
- **Ratios and proportions** map to **Development process optimisation** and team leadership: engineer-to-service ratios, on-call load per person, build capacity per team — leading a team of experts to deliver improvements starts with knowing whether the ratios are sustainable.
- **Averages and distributions** map to your product ownership duty: lead times, deployment frequencies and failure rates summarise a product line's health, and knowing when a mean misleads (and a percentile tells the truth) keeps your reporting honest.
- **Trend reading and projection** map to your **medium to long term strategy** duty: multi-quarter cost curves, compounding growth and capacity runway calculations convert strategy from aspiration into dated commitments.
- **Table and chart comprehension** map to **Systems design** review and **Information security** oversight: supplier proposals, risk registers and vulnerability summaries arrive as tables, and reviewing others' work for efficient use of resources is largely the discipline of reading their numbers more carefully than they did.

### Practice questions

**Question 1 (easy) — Availability across a product line**

One of your services has a 99.95% availability target over a 30-day month. To the nearest minute, how much downtime can it incur while still meeting the target?

- A) 4 minutes
- B) 22 minutes
- C) 43 minutes
- D) 66 minutes

**Correct answer: B**

**Explanation:** Total minutes in a 30-day month: 30 × 24 × 60 = 43,200. Permitted downtime: 100% − 99.95% = 0.05%, and 43,200 × 0.0005 = 21.6 minutes — 22 to the nearest minute. Option C is the allowance for 99.9% (43.2 minutes); option A approximates 99.99% (4.3 minutes); option D matches roughly 99.85%. As the owner of availability policy for your product lines, having the standard tiers memorised — 99.9% ≈ 43 minutes, 99.95% ≈ 22 minutes, 99.99% ≈ 4 minutes monthly — lets you challenge a proposed target in the meeting where it is proposed, rather than a week later in writing.

**Question 2 (easy) — Portfolio change failure rate**

Last quarter your three teams deployed 120, 200 and 80 times, with change failure rates of 5%, 4% and 10% respectively. How many failed changes occurred across the portfolio?

- A) 19
- B) 22
- C) 25
- D) 76

**Correct answer: B**

**Explanation:** Compute each team's failures, then sum. Team 1: 5% of 120 = 6. Team 2: 4% of 200 = 8. Team 3: 10% of 80 = 8. Total: 6 + 8 + 8 = 22. Option A likely comes from averaging the rates (6.33%) and applying it to 300 deployments — but the teams' volumes differ, and the portfolio total must be built from the parts. Note also the portfolio rate: 22 ÷ 400 = 5.5%, which is not the simple average of 5, 4 and 10 — a weighted-versus-unweighted distinction that will recur whenever you aggregate team metrics upwards. Reporting a portfolio number you built incorrectly is worse than reporting none, because it fails precisely when someone checks.

**Question 3 (easy) — Team capacity arithmetic**

Your team of 8 engineers each has 6 productive hours per working day. Next sprint (10 working days), two engineers will be on leave for the whole sprint and the team will spend a total of 40 hours on interviews and knowledge-sharing sessions. How many productive engineering hours remain for sprint work?

- A) 320 hours
- B) 360 hours
- C) 400 hours
- D) 440 hours

**Correct answer: A**

**Explanation:** Available engineers: 8 − 2 = 6. Base capacity: 6 engineers × 6 hours × 10 days = 360 hours. Subtract the committed overhead: 360 − 40 = 320 hours. Option B forgets the overhead; option C forgets the leave but not the overhead (8 × 6 × 10 = 480, minus 40 = 440 — that is option D, forgetting the leave). Capacity arithmetic looks trivial, yet overcommitted sprints are usually born exactly here: a plan built on nominal headcount rather than available hours. As the lead who signs the team up to portfolio commitments, this subtraction — done before the promise, not after the miss — is a core act of care for your teams.

**Question 4 (moderate) — Platform cost per deployment trend**

Your platform's monthly run cost and deployment volumes were: Q1 average £30,000 per month with 300 deployments per month; Q4 average £36,000 per month with 500 deployments per month. What happened to the cost per deployment from Q1 to Q4?

- A) It rose from £100 to £120
- B) It fell from £100 to £72
- C) It fell from £120 to £100
- D) It rose because total cost rose 20%

**Correct answer: B**

**Explanation:** Cost per deployment: Q1: £30,000 ÷ 300 = £100. Q4: £36,000 ÷ 500 = £72. Unit cost fell 28% even as total cost rose 20%, because volume rose 67%. Option D confuses total cost with unit cost — the exact confusion a finance reviewer will probe when your platform's budget line grows. The strategic story the numbers tell is the one you should be telling: the platform is scaling efficiently, absorbing two-thirds more delivery for one-fifth more cost. A lead who can only report "costs went up" invites cuts; a lead who reports unit economics defends the investment. Always compute the per-unit figure before a budget conversation, whichever direction it argues.

**Question 5 (moderate) — Weighted average lead time**

Across your product line last month: Team A completed 30 changes with a mean lead time of 2 days; Team B completed 10 changes with a mean lead time of 8 days. What was the mean lead time across all 40 changes?

- A) 5 days
- B) 3.5 days
- C) 4 days
- D) 2.75 days

**Correct answer: B**

**Explanation:** Weight by volume. Total lead-time-days: (30 × 2) + (10 × 8) = 60 + 80 = 140. Mean: 140 ÷ 40 = 3.5 days. Option A is the unweighted average of 2 and 8 — the classic error when aggregating team metrics. Sanity check: three-quarters of the changes came from the 2-day team, so the portfolio mean must sit much nearer 2 than 8, and 3.5 does. There is also a management insight hiding in the spread: the portfolio mean conceals that Team B's changes take four times as long — worth investigating (harder domain? heavier process? fewer people?) before the portfolio number is quoted anywhere, because the first question a good reviewer asks about an average is what it is hiding.

**Question 6 (moderate) — Comparing supplier pricing models**

A supplier offers two pricing models for a managed build service your teams would share. Model X: £4,000 per month flat, including 10,000 build minutes, then £0.30 per additional minute. Model Y: £0.55 per build minute with no flat fee. Your teams currently use 14,000 build minutes per month. Which model is cheaper at current usage, and by how much per month?

- A) Model X, by £1,500
- B) Model Y, by £1,500
- C) Model X, by £2,500
- D) They cost the same

**Correct answer: C**

**Explanation:** Compute both totals fully before comparing. Model X: £4,000 flat + (14,000 − 10,000) × £0.30 = £4,000 + £1,200 = £5,200. Model Y: 14,000 × £0.55 = £7,700. Model X is cheaper, by £7,700 − £5,200 = £2,500 per month. Option A pairs the right model with the wrong difference — the £1,500 figure comes from forgetting the 4,000-minute overage charge and comparing £4,000 against a mangled Y total; option B inverts the winner. Identifying the cheaper model is only half the mark: procurement comparisons reward computing both totals in full before subtracting, because a right conclusion with a wrong magnitude still misstates the business case you are signing. In real supplier negotiations, also compute the crossover point — X and Y break even near 9,500 minutes, so if your usage were falling rather than stable, the recommendation could flip within the contract term. Leads earn their seat in commercial conversations by bringing exactly that second-order arithmetic.

**Question 7 (moderate) — On-call load fairness**

Your on-call rota covers 42 weeks of the coming year with 6 engineers. Two engineers have agreed adjustments limiting them to 4 weeks each. If the remaining weeks are shared equally among the other 4 engineers, how many weeks does each of them carry, and what percentage more is that than the all-equal share of 7 weeks?

- A) 8.5 weeks each — about 21% more
- B) 8 weeks each — about 14% more
- C) 9 weeks each — about 29% more
- D) 8.5 weeks each — about 14% more

**Correct answer: A**

**Explanation:** Weeks covered by the two adjusted engineers: 2 × 4 = 8. Remaining: 42 − 8 = 34 weeks across 4 engineers = 8.5 weeks each. Compare with the all-equal share: 42 ÷ 6 = 7 weeks. Excess: 8.5 − 7 = 1.5 weeks; 1.5 ÷ 7 = 0.214, about 21% more. Option D pairs the right weeks with the wrong percentage; B and C miscompute the division. The management content matters as much as the arithmetic: reasonable adjustments are right to grant, and their load lands somewhere — quantifying it is how you keep the rest of the rota consensual (people accept "8.5 weeks, and here is why, reviewed quarterly" far better than an unexplained drift), and how you know when the answer must instead be "we need a seventh person on the rota". Fairness you have not computed is fairness you are guessing at.

**Question 8 (moderate) — Error budget across a quarter**

A critical service has a 99.9% availability objective measured over each 30-day month, giving a monthly error budget of 43.2 minutes. In the first month of the quarter it consumed 12 minutes; in the second, 58 minutes. The team asks to "borrow" the third month's budget to keep releasing at full speed. As the product owner, what does the data support?

- A) The quarter's total budget is 129.6 minutes and only 70 are used, so full-speed releasing is fine.
- B) The objective is monthly: month two breached it (58 > 43.2), the breach cannot be offset by other months, and month three should run with heightened caution and a review of what caused month two's consumption.
- C) Month two's overrun means all releases must stop for a quarter.
- D) The error budget concept no longer applies once breached.

**Correct answer: B**

**Explanation:** First the arithmetic: 58 minutes against a 43.2-minute monthly budget is a breach of the month-two objective, regardless of month one's healthy 12 minutes, because the objective is defined per month — budgets measured monthly do not pool across the quarter unless the objective says so. Option A silently redefines the measurement window to rescue the conclusion, which is exactly the manoeuvre a lead must catch when a team (or a supplier) reports against a target: changing the window changes the promise. But option C overcorrects — error budget practice modulates release risk, it does not impose punitive freezes that teach teams to hate the mechanism. B pairs the correct reading with the proportionate response: caution, plus a causal review, because 58 minutes in one month after 12 in the previous is a signal worth understanding, not just recording. Numeric questions at lead level often hinge on the definition of the measurement window; read it before computing anything.

**Question 9 (challenging) — Capacity runway with changing growth**

A shared database cluster is at 3.0 TB of its 5.0 TB capacity. Growth has been 0.25 TB per month, but a new service joining next month is expected to add a further 0.15 TB per month from its first month. Your policy requires expansion work to begin when utilisation reaches 80%. Expansion takes two months to complete. In which month from now must the expansion work begin to finish before the threshold is crossed — and is that feasible?

- A) Work must begin in month 2; feasible with a month to spare
- B) Work must begin by month 0 (now); only just feasible
- C) Work must begin in month 1; exactly feasible
- D) The threshold will not be crossed for six months, so month 4 is fine

**Correct answer: C**

**Explanation:** Threshold: 80% of 5.0 TB = 4.0 TB. Headroom: 4.0 − 3.0 = 1.0 TB. Growth: the new service joins next month and adds from its first month, so every month from month 1 onwards adds 0.25 + 0.15 = 0.40 TB. Cumulative: end of month 1: 3.40 TB; end of month 2: 3.80 TB; during month 3 the total passes 4.0 TB. Expansion takes two months, so the latest safe start is the start of month 1: it completes at the end of month 2, just before the crossing — exactly feasible, with no slack month. Starting in month 2 would complete at the end of month 3, after the threshold has been crossed. Option D is the pre-acceleration runway (1.0 ÷ 0.25 = 4 months), the trap for anyone who misses the new joiner in the stem. Option B is what a prudent lead would actually do — begin now and bank the slack — but the question asks for the latest month that still meets the policy, and reading precisely what is asked is part of the test. The strategic habit underneath: every time demand changes shape, recompute the runway. The old forecast dies the day the new service signs up, and initiating remedial action against a dead forecast is how thresholds get crossed in production.

**Question 10 (challenging) — Reading a portfolio metrics table**

The quarterly portfolio review table shows:

| Team | Deploys | Change failure rate | Mean restore time (min) | Availability target | Achieved |
|---|---|---|---|---|---|
| Alpha | 180 | 5% | 30 | 99.9% | 99.92% |
| Beta | 60 | 5% | 120 | 99.9% | 99.88% |
| Gamma | 240 | 2.5% | 45 | 99.5% | 99.7% |

Which team caused the most failed changes, and which team's profile best explains a missed availability target?

- A) Gamma caused most failures; Beta's long restore time explains its miss
- B) Alpha caused most failures; Beta's failure rate explains its miss
- C) Alpha and Beta tie on failures; Gamma missed its target
- D) Alpha caused most failures; Beta's long restore time explains its miss

**Correct answer: D**

**Explanation:** Failed changes: Alpha 5% × 180 = 9; Beta 5% × 60 = 3; Gamma 2.5% × 240 = 6. Alpha caused the most failures — same rate as Beta, three times the volume; Gamma's bigger volume is offset by half the rate. For the availability miss: only Beta achieved below target (99.88 < 99.9). Why Beta and not Alpha, with identical failure rates? Restore time: Beta takes 120 minutes to restore against Alpha's 30 — fewer failures, but each one bleeds four times longer, and availability is failure count times duration. Option A misidentifies the failure leader; B blames Beta's rate, which equals Alpha's and so explains nothing on its own. The portfolio lesson is one of the most useful in DevOps metrics: teams miss availability targets through slow recovery at least as often as through frequent failure, so the remedial investment for Beta is restore capability (runbooks, rollback automation, alerting) rather than release gating. Reading a table means finding the column that discriminates, not the column that alarms.

**Question 11 (challenging) — Compound growth in platform costs**

A platform cost line is £20,000 per month today and growing at 8% per quarter, compounding. The head of finance asks for its projected monthly cost in one year (four quarters). What do you report, to the nearest £500?

- A) £26,400
- B) £27,000
- C) £27,200
- D) £25,600

**Correct answer: B**

**Explanation:** Compound four quarters: 1.08⁴. Step by step: 1.08² = 1.1664; 1.1664² ≈ 1.3605. Projection: £20,000 × 1.3605 ≈ £27,210. Now apply the rounding instruction: to the nearest £500, the candidates are £27,000 and £27,500, and £27,210 is nearer £27,000 — so you report £27,000. Option A (£26,400) is the linear trap: treating four quarters of 8% as 32% simple growth (£20,000 × 1.32). Option C is what you get by rounding £27,210 upwards out of habit rather than to the nearest step. Option D applies partial compounding and slips. Two professional habits are being tested at once: compound rates multiply (1.08⁴ ≈ 1.360, not 1.32 — a difference that grows every further quarter), and rounding instructions are part of the question, applied once at the end. A projection delivered at the wrong precision invites either false confidence or needless alarm in a finance conversation, and a lead's cost forecasts get quoted upwards verbatim — so the precision you hand over is the precision the portfolio board will believe.

**Question 12 (challenging) — Business case for a process investment**

You propose investing 120 engineer-days building self-service environment provisioning. Current state: teams raise 25 environment requests per month, each consuming 1.5 days of platform-engineer effort and imposing an average 6 working days of waiting on the requesting team. Future state: 90% of requests self-served instantly at negligible marginal effort; the remaining 10% still need 1.5 days each. Measured in platform-engineer effort alone, how many months does the investment take to pay back?

- A) About 2.5 months
- B) About 3.6 months
- C) About 4.8 months
- D) About 8 months

**Correct answer: B**

**Explanation:** Current platform effort: 25 × 1.5 = 37.5 engineer-days per month. Future: 10% of 25 = 2.5 requests × 1.5 = 3.75 days per month. Monthly saving: 37.5 − 3.75 = 33.75 engineer-days. Payback: 120 ÷ 33.75 = 3.56 — about 3.6 months. Option A likely divides by the gross current effort (120 ÷ 37.5 = 3.2, then misrounds); option D halves the saving. Note what the calculation deliberately excludes: the 6 waiting days per request imposed on requesting teams — roughly 150 team-days of waiting per month — vanishes for 90% of requests, which is the larger benefit and the one your strategy paper should lead with, clearly labelled as waiting time rather than effort. A lead's business case earns trust by keeping the categories clean: effort savings pay back the build; waiting-time savings transform the delivery experience; conflating them invites a finance reviewer to disbelieve both.

### Preparation tips

- **Keep your standard conversions warm.** Minutes per 30-day month (43,200), downtime allowances at each availability tier, and the fact that compound rates multiply. You use these in real meetings; the test just removes the meeting.
- **Build portfolio numbers from parts.** Whenever teams differ in volume, compute each team's contribution before aggregating. Averaging rates across unequal teams is the most common lead-level error, in tests and in portfolio reviews alike.
- **Read the measurement window before calculating.** Monthly objectives, quarterly budgets, per-sprint capacity: the window is part of the definition, and distractors are built by quietly changing it.
- **Compute both sides of every comparison.** For supplier models, before/after states and payback cases, resist concluding from one total; the magnitude of the difference is usually where the marks (and the negotiations) are.
- **Practise unit-cost thinking.** Take any rising cost in your own reporting and compute the per-deployment or per-request figure. Total cost tells you what you spend; unit cost tells you whether you are scaling well.
- **Check rounding instructions last.** After the arithmetic, re-read what precision the question wants — nearest minute, nearest £500 — and round once, at the end.

### Common pitfalls to avoid

- **Averaging team averages.** Unequal volumes demand weighting. If the sanity check ("must sit nearer the bigger group") fails, redo it.
- **Linearising compound growth.** Four quarters at 8% is 36%, not 32%. The linear answer is always among the distractors because it is always the tempting shortcut.
- **Confusing total with unit cost.** A budget line can rise while unit economics improve. Compute both before the conversation, whichever one you expect to defend.
- **Pooling budgets across windows.** A monthly objective breached in month two is breached, whatever the quarter's total says. Redefining windows to rescue a conclusion is the error — catching others doing it is the skill.
- **Forgetting demand changes.** Capacity runway computed on last quarter's growth rate dies the day a new consumer joins. Recompute on every change of shape.
- **Right winner, wrong margin.** In comparisons, a correct conclusion with an incorrect magnitude still fails — in tests by the mark, in procurement by the million.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you read, interpret and evaluate written material of the kind your role deals with daily. Rather than literary passages, it presents workplace texts — in your case, extracts from technology strategies, spend approval guidance, supplier contract summaries, audit findings, policy consultations, and correspondence from senior stakeholders — and asks you to determine what the text does and does not establish.

Typical format: an online, timed test lasting 15 to 25 minutes. The commonest style presents a short passage followed by statements to classify as True (the passage supports it), False (the passage contradicts it), or Cannot Say (insufficient information either way). Other styles test inference, identifying the main point, and judging which formulation of a message is clearest. The critical rule: answer only from the passage, not from your professional knowledge. A statement can be true in the real world and still be Cannot Say on the test.

For a lead DevOps engineer on the management track, verbal precision has become a leadership instrument. You read governance documents and must know exactly what they permit before you commit teams to a course. You read audit findings and must separate what was evidenced from what was inferred before you accept actions on your teams' behalf. You write strategy papers whose every qualifier will be quoted back to you, and you review the papers your senior engineers write, teaching them the same precision. When you lead the sharing of knowledge and good practice, the documents you circulate become the profession's reference material — and an imprecise sentence at your level propagates across every team that trusts you. Assessors weight verbal reasoning heavily in selection for lead posts because the cost of misreading scales with the number of people who act on your reading.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Literal comprehension** maps to **Modern development standards** and **Information security**: identifying and applying standards to complex programmes begins with reading mandates, scopes and exemptions precisely — and leading others in applying them means being the person who resolves interpretive disputes correctly.
- **True/False/Cannot Say discipline** maps to your product ownership and **Service support** duties: incident reports, supplier claims and delivery updates each mix evidence with assertion, and acting on assertion as if it were evidence is how product owners commit teams to the wrong bets.
- **Inference** maps to **Systems design** and **Systems integration**: contract summaries and interface documents rarely state everything; sound inference — and recognising the exact point where inference must give way to a clarifying question — keeps multi-team integration commitments honest.
- **Clear-writing judgement** maps to your duty to provide **technical leadership through coaching and mentoring**: you review and improve the runbooks, proposals and strategies your teams write, and the standard you enforce becomes their standard.
- **Identifying the main point** maps to your **strategic direction** contribution: consultations, ministerial priorities and architecture papers are only actionable once their central claim is extracted from the surrounding qualification — and misidentifying it wastes your organisation's response.

### Practice questions

**Passage 1 (for Questions 1–3)**

"Departmental spend approval is required for any new technology commitment exceeding £100,000 over the contract lifetime. Renewals of existing commitments are exempt from approval provided the renewal value does not exceed the previous contract value by more than 10%. Cloud consumption commitments are treated as new commitments at each renewal, regardless of value. Where approval is required, teams must allow a minimum of 15 working days for the approval process."

**Question 1 (easy) — True/False/Cannot Say**

Statement: "A renewal of a £200,000 software licence at £215,000 is exempt from spend approval."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Apply the renewal exemption's condition: the renewal may exceed the previous value by at most 10%. Ten per cent of £200,000 is £20,000, so the ceiling is £220,000. At £215,000, the increase is £15,000 — within the allowance — so the exemption applies and the statement is True. (One check: is this a cloud consumption commitment? The stem says "software licence", so the cloud carve-out does not bite.) The technique is to convert the percentage condition into an absolute figure before judging, exactly as you would when a team asks whether their renewal needs to go through approval — a question you, as the lead who owns the relationship with governance, will be asked often and must answer correctly, because a wrong "no" surfaces as an audit finding months later.

**Question 2 (easy) — True/False/Cannot Say**

Statement: "A cloud consumption commitment renewing at 5% above its previous value is exempt from spend approval, provided it is under £100,000."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Trace carefully. Cloud consumption commitments are "treated as new commitments at each renewal, regardless of value" — so the renewal exemption cannot rescue it, and the 5% increase is irrelevant. As a new commitment, it requires approval if it exceeds £100,000 over the contract lifetime. The statement stipulates it is under £100,000 — in which case the general rule does not require approval, making the statement look True. But note what the passage does not say: it defines when approval is required; it does not state that commitments under £100,000 are exempt from all approval routes — other rules could exist outside this extract. The disciplined classification is Cannot Say: the passage supports "this rule does not require approval" but not the broader "is exempt from spend approval". This is a fine distinction, and deliberately so: at lead level, the difference between "this policy doesn't require it" and "nothing requires it" is exactly the gap in which non-compliance lives, and the safe professional answer to a team is "this policy doesn't bite — let me confirm nothing else does".

**Question 3 (moderate) — True/False/Cannot Say**

Statement: "A team that needs approval for a new £150,000 commitment and wants to sign within 10 working days will be unable to sign on time through the standard process."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The commitment is new and exceeds £100,000, so approval is required. The passage sets a minimum of 15 working days for the approval process. A minimum of 15 exceeds the desired 10, so through the standard process described, signature within 10 working days is not achievable — True. The word doing the work is "minimum": it guarantees the process cannot be assumed shorter, which is what makes the statement provable rather than merely likely. Notice also the phrase "through the standard process" in the statement — it matches the passage's scope, so no speculation about expedited routes is needed. Reading durations, minimums and scope qualifiers this precisely is how you plan team commitments around governance instead of discovering governance inside your critical path — a planning failure that, at your level, delays several teams at once.

**Passage 2 (for Questions 4–6)**

"Internal audit reviewed the department's deployment controls across five services. In three services, production changes were consistently traceable to approved tickets. In one service, 12 of 250 sampled changes could not be matched to an approved ticket; the service team states that these were emergency fixes, but the emergency process log records only 5 emergency changes in the period. In the remaining service, sampling was not possible because deployment logs are retained for only 30 days. The audit rates the department's overall deployment control environment as 'requires improvement' and recommends extending log retention to 12 months across all services."

**Question 4 (moderate) — True/False/Cannot Say**

Statement: "In the service with unmatched changes, at least 7 changes were neither matched to an approved ticket nor recorded in the emergency process log."

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Twelve sampled changes lacked approved tickets. The team's explanation — emergency fixes — could legitimately cover changes recorded in the emergency log, which shows only 5 emergency changes in the period. Even if every one of those 5 logged emergencies were among the 12 unmatched changes (the most generous possible assumption), at least 12 − 5 = 7 changes remain with neither an approved ticket nor an emergency record. The statement is True, and the audit's arithmetic is the interesting kind: it doesn't accuse anyone of lying; it simply shows the explanation cannot cover the facts by at least 7 changes. This is a reading-and-reasoning pattern leads need constantly: when an account is offered for a discrepancy, check whether the account has the capacity to explain the whole discrepancy before accepting it — and do it with the generous assumption, so your conclusion survives challenge.

**Question 5 (moderate) — True/False/Cannot Say**

Statement: "The department's deployment controls failed in two of the five services reviewed."

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** One service clearly shows control weaknesses (unmatched changes exceeding the emergency log's capacity to explain). But the fifth service's position is different: sampling "was not possible" because logs are retained for only 30 days. Absence of evidence that controls worked is not evidence that they failed — the audit could not test them. Whether that service's controls failed is unknown from the passage, so "failed in two" is neither supported nor contradicted: Cannot Say. Note that short log retention is itself a control deficiency in the auditors' eyes (hence the recommendation), but a retention weakness is not the same claim as "deployment controls failed". Keeping "we found a failure", "we couldn't test", and "the testing infrastructure is deficient" as three separate categories is precisely the precision you need when you respond to audit findings on your teams' behalf — conceding the right category, and only the right category, is what a well-drafted management response does.

**Question 6 (moderate) — Inference**

Which conclusion is best supported by Passage 2?

- A) The service team with unmatched changes fabricated its emergency-fix explanation.
- B) The department cannot currently demonstrate full deployment control traceability, and its ability to evidence controls is limited in at least one service by log retention.
- C) Extending log retention to 12 months will fix the control weaknesses.
- D) The three fully traceable services have the best engineering teams.

**Correct answer: B**

**Explanation:** B states only what the passage establishes: traceability could not be fully demonstrated (12 unmatched changes in one service; another untestable), and retention limits evidencing in at least one service. Option A overreaches — the arithmetic shows the explanation is insufficient, not that it was dishonest; some of the 12 may genuinely have been emergencies that went unlogged, which is a process failure rather than a fabrication. Option C converts a recommendation into a predicted outcome: longer retention improves auditability, but the unmatched-changes weakness is an approval-discipline problem retention does not touch. Option D invents a causal league table. The pattern for audit-adjacent reading: the supported conclusion is usually about what can and cannot be demonstrated, not about motives or guaranteed fixes. When you brief your head of profession on findings like these, B's phrasing — capability-focused, evidence-bounded — is both the correct answer and the correct sentence to say.

**Passage 3 (for Questions 7–9)**

"The proposed engineering strategy commits the department to consolidating onto a single deployment platform within two years. The paper argues this will reduce duplicated tooling effort, currently estimated at 20% of platform engineering time, and improve security posture through consistent controls. Funding covers migration of the eight services on supported legacy platforms. Three further services run on platforms that are already out of support; their migration is described as 'urgent but unfunded, subject to the next spending review'. The paper notes that consolidation increases concentration risk: an outage of the single platform would affect all services simultaneously. It proposes mitigating this through multi-region deployment and a tested platform recovery capability, and states that the residual risk 'is judged acceptable by the design authority, subject to annual review'."

**Question 7 (moderate) — True/False/Cannot Say**

Statement: "The strategy paper claims consolidation will reduce duplicated tooling effort by 20%."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Read the figure's role precisely: 20% is the current estimated size of duplicated tooling effort ("currently estimated at 20% of platform engineering time"), not the size of the promised reduction. The paper claims consolidation will reduce that duplicated effort — by how much, it does not say. The statement misattaches the number to the reduction, contradicting the passage's actual claim structure: False. This "quantity transplant" — a true number attached to the wrong noun — is among the most common distortions when strategy papers get summarised upwards, and one of the most consequential: "saves 20% of platform engineering time" would be a far stronger claim than the paper makes, and a lead who lets that misquote circulate will be held to it at benefits review. When you quote a number, quote its noun with it.

**Question 8 (challenging) — True/False/Cannot Say**

Statement: "All eleven services requiring migration have funded migration paths."

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Count the populations the passage defines: eight services on supported legacy platforms — funded; three services on out-of-support platforms — "urgent but unfunded, subject to the next spending review". Eight funded plus three unfunded means not all eleven are funded: the statement is contradicted — False. The dangerous detail is that the three unfunded services are the most at-risk (already out of support), a prioritisation inversion the passage presents without comment: the money follows the easier population while the urgent one waits for a spending review. Spotting what a paper juxtaposes but does not remark upon is a senior reading skill — the passage never says "our funding is misaligned with risk", but a lead reviewing this strategy should say it, and propose either reprofiling funds or an explicit interim risk treatment for the three exposed services. Verbal tests check you can extract the fact pattern; your role requires you to also notice what the fact pattern means.

**Question 9 (challenging) — Evaluating a risk statement**

Based only on Passage 3, which reading of the concentration-risk position is most accurate?

- A) The concentration risk has been eliminated by multi-region deployment.
- B) The risk is acknowledged, mitigations are proposed, and a named authority has accepted the residual risk with a review cycle — but the passage does not state that the mitigations are yet in place or tested.
- C) The design authority has rejected the strategy because of concentration risk.
- D) The concentration risk makes consolidation inadvisable.

**Correct answer: B**

**Explanation:** Track the verbs' tense and force. The paper "proposes mitigating" — proposal, not implementation; the recovery capability is described as "tested" within the proposal's design, not as tested-and-operational today. The residual risk "is judged acceptable... subject to annual review" — an acceptance with conditions, by a named authority. B captures all of this without adding or subtracting. A converts mitigation into elimination (mitigations reduce risk; "eliminated" is never supported, and multi-region deployment cannot remove all common-mode failures — a platform-wide software defect deploys to every region). C contradicts the recorded acceptance. D substitutes your own risk appetite for the evidence. The professional application is direct: when your teams inherit obligations from strategy papers, the difference between "mitigations proposed" and "mitigations in place" defines your delivery backlog — leads who read B's distinction accurately know what work they have just been signed up for; leads who read A's version discover it during an incident.

**Question 10 (moderate) — Clear-writing judgement**

You are reviewing a senior engineer's draft announcement of a new standard to all teams. Which version is most effective?

- A) "Following extensive stakeholder consultation and in alignment with our strategic direction of travel, it has been determined that containerisation approaches should, where practicable, be harmonised going forward."
- B) "From 1 October, all new services must use the approved container base images (list linked below). Existing services must migrate by 31 March. Exemptions: apply via the design authority. Questions: #platform-standards channel."
- C) "We are excited to announce a transformative change to our container journey!"
- D) "Teams should probably start thinking about using the standard base images at some point soon, unless it doesn't suit their service."

**Correct answer: B**

**Explanation:** A standards announcement succeeds when every team can answer four questions from it: what exactly is required, from when, what happens to existing work, and what to do if it does not fit. B answers all four with dates, scope ("all new services"), a migration deadline, an exemption route and a support channel. A is process-proud and content-free: "should, where practicable, be harmonised" mandates nothing and will be read five different ways by five teams — the opposite of leading others in applying standards. C is tone without substance. D converts a standard into a suggestion and embeds its own escape clause, guaranteeing patchy adoption and an unfair playing field between compliant and non-compliant teams. Note that B's virtue is not brevity for its own sake but decidability: every sentence lets a reader make a decision. When you coach senior engineers on communication — part of your technical leadership duty — "could a team lead act on each sentence without asking you anything?" is the review question that improves drafts fastest.

**Question 11 (challenging) — Comprehension of contractual language**

A supplier contract summary reads: "The provider guarantees 99.9% monthly availability of the build service, measured at the provider's service boundary. Service credits of 10% of the monthly fee apply for each 0.1 percentage point below the guarantee, capped at 50% of the monthly fee. Credits are the sole remedy for availability failures. Scheduled maintenance, notified 5 working days in advance and not exceeding 4 hours per month, is excluded from the availability calculation."

Which statement is correct?

- A) If availability falls to 99.5% in a month, the department receives a 40% service credit and may also claim consequential losses.
- B) A 6-hour maintenance window notified 10 working days in advance is fully excluded from the availability calculation.
- C) If availability measured at the department's network edge falls below 99.9% but the provider's boundary measurement shows 99.95%, no credit is due under this clause.
- D) Credits are capped at 40% of the monthly fee.

**Correct answer: C**

**Explanation:** Work through each option against the text. A: 99.5% is 0.4 points below 99.9%, giving 4 × 10% = 40% credit — but "credits are the sole remedy" excludes consequential losses, so A's second half fails. B: the exclusion covers maintenance "not exceeding 4 hours per month"; a 6-hour window exceeds it, so it is not fully excluded regardless of generous notice. D: the cap is stated as 50%, not 40%. C is correct and is the option testing the clause's sharpest tooth: availability is "measured at the provider's service boundary", so degradation between that boundary and your teams — network paths, integrations — is invisible to the guarantee, and the provider's 99.95% measurement controls. This measurement-point clause is precisely what a lead must catch before signing, because your teams experience availability at their edge, not the provider's; the mitigation is contractual (negotiate the measurement point) or architectural (monitor and manage the intervening path yourself). Contract questions reward reading each qualifying phrase as a live constraint, because each one was drafted by someone whose job was to limit the promise.

**Question 12 (challenging) — Main point of a strategic consultation**

"This consultation seeks views on the proposed Engineering Excellence Framework. The framework would not mandate specific tools. Instead, departments would self-assess annually against outcome-based criteria — deployment safety, recovery capability, supply chain assurance — with results shared across government to identify where support is most needed. Self-assessments would not be used for departmental league tables or funding decisions in the first two years, while the criteria are calibrated. Views are particularly sought on whether the criteria adequately reflect the differing scales of departments' engineering functions."

Which statement best captures the main point?

- A) The framework mandates standard tools across government engineering functions.
- B) The framework proposes annual outcome-based self-assessment with cross-government sharing to target support, explicitly not linked to league tables or funding for two years, and the consultation especially wants views on whether the criteria suit different scales of engineering function.
- C) The framework will rank departments to determine funding.
- D) The consultation has concluded that current engineering practice is inadequate.

**Correct answer: B**

**Explanation:** B preserves each load-bearing element: the mechanism (annual self-assessment against outcomes), the purpose (sharing to target support), the explicit temporal safeguard (no league tables or funding linkage for two years — note "in the first two years" implies the position may change after calibration, which B's phrasing correctly carries), and the specific question asked of respondents. A contradicts "would not mandate specific tools". C inverts the safeguard, and D invents a conclusion the consultation never states. The scale question matters for you particularly: as a lead contributing to strategic direction, your response to exactly this kind of consultation is how your teams' context — their size, their legacy load — gets reflected in the frameworks that will later measure them. Answering the consultation's actual question, rather than the question a skimmed reading suggests, is how a profession's voice gets heard; and inside your own department, circulating B's summary rather than A's or C's misreading is the difference between calm engagement and needless alarm.

### Preparation tips

- **Quote numbers with their nouns.** The commonest distortion at lead level is a true figure attached to the wrong quantity. When practising, restate each number's noun phrase aloud before classifying any statement about it.
- **Track verb force and tense.** "Proposes", "guarantees", "is judged", "would not" — the modality of each verb defines what is claimed. Mitigations proposed are not mitigations in place; exclusions conditional are not exclusions absolute.
- **Convert percentage conditions to absolutes.** Renewal ceilings, credit calculations, threshold clauses: do the arithmetic before judging the statement, and the classification usually falls out.
- **Practise the generous-assumption check.** When a passage offers an explanation for a discrepancy, test whether the explanation could cover the facts even in the best case. If it cannot, that shortfall is provable — and provable beats plausible.
- **Read one governance document per week adversarially.** Take a contract summary, audit finding or policy extract from your real work and write down: what is claimed, what is measured, where, by whom, and what is explicitly not promised. This is direct rehearsal for both the test and your job.
- **For clear-writing items, apply the decidability test.** The best option is the one from which every affected reader could make their decision without asking a follow-up question.

### Common pitfalls to avoid

- **Importing professional knowledge.** You know how spend controls, audits and SLAs usually work; the passage defines how these ones work. Answer from the text alone.
- **Confusing "this rule doesn't require it" with "nothing requires it".** Passages define their own scope; statements that generalise beyond it are usually Cannot Say, and the same gap in real life is where compliance failures hide.
- **Treating absence of evidence as failure.** "Could not be tested" is a different finding from "failed". Auditors know the difference; so must your reading and your management responses.
- **Upgrading mitigation to elimination.** Risk language is graded deliberately. The dramatic reading is nearly always the wrong one.
- **Missing the measurement point.** Where a figure is measured — provider boundary, network edge, monthly window — is part of its meaning. A clause read without its measurement point has not been read.
- **Summarising by vibe.** Main-point questions punish summaries that drop qualifiers ("in the first two years", "where approval is required"). So do the stakeholders who receive your summaries.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of possible responses. Unlike cognitive or numeric tests, there is rarely a provably correct answer; instead, responses are scored against the judgement of experienced practitioners and the behaviours your organisation values — in the UK Government Digital and Data context, behaviours such as user focus, collaboration, taking ownership, appropriate escalation, developing others, and inclusion.

Typical format: an online test of 10 to 20 scenarios, often untimed or generously timed. Question styles include picking the most effective response, picking the most and least effective from four options, ranking all options, or rating each option independently. Read the instructions carefully: "most effective" asks what works best, not what you would instinctively do, and rating formats allow several options to score well.

For a lead DevOps engineer on the management track, the SJT examines the judgement calls that now define your job. Your scenarios involve line management: a struggling senior engineer, an underperformer others are compensating for, a conflict between two of your teams. They involve product ownership: a stakeholder demanding a commitment your capacity cannot honour, a strategic bet that your pilot data undermines. They involve organisational citizenship: a peer's team heading into a known trap, a governance decision you disagree with, credit and blame flowing to the wrong places. In each case the scored answer balances delivery, honesty, the development of people, and the health of the wider organisation — because at lead level, the way you handle one scenario becomes the story your teams tell about what is acceptable. The SJT is, in effect, a rehearsal of your culture-setting.

### How this assessment maps to your role

The assessment dimensions map directly to the skills in your capability framework:

- **Ownership and escalation judgement** maps to **Availability and capacity management** and **Service support**: initiating remedial action at portfolio scale means knowing which problems you resolve on your own authority, which you escalate, and how to keep accountability clear across teams while faults are found and fixed.
- **Developing others** maps to your duty to provide **technical leadership and guidance through coaching and mentoring**: scenarios probe whether you grow senior engineers into leaders, address underperformance honestly and kindly, and delegate real authority rather than tasks.
- **Collaboration and influence** map to **Development process optimisation** and your duty to **lead the sharing of knowledge and good practice**: improving processes across teams you do not control, and spreading practice without mandating everything, are influence problems before they are technical ones.
- **Integrity under pressure** maps to **Information security** and **Modern development standards**: when commercial, political or schedule pressure meets a control or a standard, the lead's visible behaviour becomes the de facto policy for every watching team.
- **User focus** maps to your **User focus** skill: as technical product owner you are the guardian of user needs against the gravitational pull of internal convenience, stakeholder desires and sunk costs — several scenarios test whether that guardianship survives pressure.

### Practice questions

**Question 1 (easy) — A senior engineer struggling with a new leadership role**

Three months ago you promoted a strong engineer into a senior role leading a workstream. Their technical output remains excellent, but two engineers have mentioned that workstream meetings are disorganised and decisions keep reopening. The senior engineer has not raised any concerns with you. What is the most effective response?

- A) Wait — they are technically excellent, and leadership skills come with time.
- B) Raise it in their next one-to-one: share the specific observations, ask for their view of how the workstream is going, and agree a development plan — for example facilitation coaching, pairing them with an experienced chair, and a follow-up review.
- C) Quietly attend their meetings and take over facilitation when discussions drift.
- D) Move the meeting-chairing duties to another engineer so they can focus on technical work.

**Correct answer: B**

**Explanation:** You promoted this person, so their success in the new role is squarely your development responsibility. Option B does the fundamentals: it surfaces specific, behavioural observations (not vague "people are unhappy"), invites their self-assessment first — they may know exactly what is wrong and be too proud or too new to ask for help — and treats the gap as a skills gap with a plan, not a character verdict. That is what technical leadership through coaching means in practice. Option A mistakes hope for development; unstructured meetings are a learnable failure, and three months of reopened decisions is already taxing the team. Option C rescues the meeting but humiliates the leader — being visibly overridden by your boss in your own meeting teaches the team to route around you. Option D solves this quarter by quietly demoting them without the honesty of saying so, and forecloses the growth you promoted them for. The scored behaviour: address performance early, specifically, and developmentally — the kindest feedback is the feedback that arrives while the problem is still small.

**Question 2 (easy) — Stakeholder pressure to commit beyond capacity**

At a programme board, a senior stakeholder asks you to commit your teams to delivering a new integration by the end of next quarter. Your capacity data shows that honouring existing commitments already consumes the quarter, and the integration would need roughly 40% of one team's capacity. The stakeholder is influential and the room is waiting. What is the most effective response?

- A) Commit — you can probably find the capacity somehow, and refusing in public is career-limiting.
- B) Refuse flatly — the data says no.
- C) State clearly that you want to support the outcome, that current commitments consume the capacity, and that you will bring options to the board within a week — for example descoping, trading against an existing commitment, or a later start — so the board can choose with full information.
- D) Commit in the meeting, then quietly deprioritise the least visible existing commitment to make room.

**Correct answer: C**

**Explanation:** This is the product-owner's defining scenario: the answer must protect both the truth of your capacity data and the stakeholder's legitimate outcome. Option C does the essential move — it converts a yes/no ambush into a trade-off decision made by the right forum with real numbers, on a stated timescale that respects the board's need for momentum. Nobody has been refused; nobody has been deceived; the cost of the new work will land on whichever commitment the board consciously chooses, not on whichever team screams last. Option A creates the classic overcommitment spiral: the "found" capacity is your teams' evenings, and the missed deadline arrives with interest next quarter. Option D is worse than A — it makes the trade-off in secret, so the board believes everything is on track while a commitment someone is counting on quietly dies; when discovered, it costs you the credibility that makes every future "it will be done" worth anything. Option B may be factually right but fails the influence test: flat public refusal without options invites the board to overrule you and teaches stakeholders you are an obstacle. Leads are scored on turning pressure into structured choices — that is what "acting as technical product owner" means at a board table.

**Question 3 (moderate) — An underperformer the team is quietly carrying**

A mid-level engineer on one of your teams has been underperforming for months: work is late, reviews find repeated basic errors, and two stronger engineers have been quietly redoing parts of their work "to keep the sprint on track". Their previous lead never raised it formally. The engineer seems unaware there is a problem. What is the most effective response?

- A) Continue as is — the team is compensating successfully and raising it now seems unfair given the previous lead's silence.
- B) Begin a formal performance process immediately with documentation of the past months' failings.
- C) Have an honest, private conversation: describe the gap between expectations and current work with concrete examples, acknowledge that this feedback should have reached them sooner, understand their situation, and agree a clear, supported improvement plan with defined expectations and check-ins — while thanking and relieving the compensating engineers.
- D) Redistribute their responsibilities so their work no longer matters to delivery.

**Correct answer: C**

**Explanation:** Unaddressed underperformance is a triple failure: the engineer is denied the information they need to improve, the compensating engineers pay a hidden tax that will eventually surface as resentment or attrition, and the team learns that standards are theoretical. Option C fixes all three, and the acknowledgement matters: the engineer inherited a feedback vacuum, so fairness requires resetting expectations clearly before judging anyone against them — which is also why B is premature: a formal process built on months of never-communicated concerns is procedurally weak and experienced as an ambush; formal routes remain available if a fair, supported informal stage fails. Option A perpetuates the harm to everyone, including the underperformer, and the "unfairness" argument inverts: what is unfair is letting someone fail unknowingly for more months. Option D is the coward's restructure — it hides the problem inside the org chart, wastes a salary, and broadcasts that difficult conversations get architected around rather than had. The management-track behaviours scored: honesty delivered kindly, protection of the whole team's fairness, and improvement plans that genuinely support rather than merely document.

**Question 4 (moderate) — Conflict between two of your teams**

Two teams you lead disagree sharply about a shared deployment pipeline: Team One wants to add mandatory progressive-rollout stages after a bad incident; Team Two says the added lead time would cripple their fast iteration on a low-risk internal service. The dispute has become personal — each team now describes the other as "reckless" or "bureaucratic" in retrospectives. What is the most effective response?

- A) Decide yourself and mandate one approach — a lead's job is to make the call.
- B) Bring the teams together to separate the real requirements from the positions: agree what risk each service tier genuinely carries, then shape a tiered policy — stronger safeguards for user-facing or high-risk services, a lighter path for low-risk internal ones — and address the interpersonal deterioration directly with both teams.
- C) Let the teams keep separate pipeline configurations and avoid the argument.
- D) Side with Team One — safety concerns always win after an incident.

**Correct answer: B**

**Explanation:** The technical dispute has a technical resolution — risk-tiered deployment policy is standard practice, and each team's position is correct for their context — which is exactly why the situation is really a collaboration failure wearing a technical costume. Option B does three lead-level things: it converts positions ("mandatory stages!" "no stages!") into requirements (what risk does each service carry?), it produces a policy that scales across future services rather than an ad hoc truce, and it treats the name-calling as a first-class problem, because teams that have learned contempt will fight again over the next shared resource. Option A resolves the object dispute but leaves the relationship broken and teaches both teams that influence flows through you rather than through reasoning with each other — a dependency you cannot afford across a growing portfolio. Option C fragments a shared asset to avoid a conversation, buying silence with duplicated maintenance and divergent standards. Option D uses recency as a policy engine; post-incident energy is valuable but unexamined, and blanket rules born of one incident routinely overcorrect. The scored behaviours: resolving conflict by elevating it to shared requirements, building policy rather than verdicts, and refusing to let interpersonal rot become culture.

**Question 5 (moderate) — Your strategy pilot returns bad news**

You championed a strategic migration to a new deployment platform, and secured funding on the strength of your business case. The pilot team's results are now in: migration effort is roughly double your estimate, and two promised platform features are less mature than the vendor claimed. The full rollout across six more services is due to start in three weeks, and the programme board expects your progress report on Friday. What is the most effective response?

- A) Proceed on schedule — pilots always hit teething problems, and pausing would embarrass the programme.
- B) Report the pilot results accurately on Friday with a revised plan: pause the rollout start, re-estimate with real pilot data, press the vendor on the immature features, and present the board with updated options — including the option that the case no longer holds.
- C) Report the pilot as broadly successful and quietly extend the rollout timeline to absorb the overrun.
- D) Cancel the migration — the estimates were wrong, so the strategy is discredited.

**Correct answer: B**

**Explanation:** The pilot did exactly what pilots are for: it bought cheap, early truth. The test is whether you can spend that truth against your own advocacy. Option B treats the business case as a living instrument — re-costed with real data, re-negotiated with the vendor, re-presented with options — and preserves the one asset a technical product owner cannot rebuild quickly: the board's trust that your reports mean what they say. Including "the case no longer holds" among the options is not weakness; it is what makes your recommendation to continue (if you make one) credible. Option A doubles the bet on the discredited estimate and converts a contained pilot overrun into a six-service programme overrun. Option C is the most tempting and the most corrosive: "broadly successful" plus a quiet timeline stretch is a misrepresentation that compounds — every subsequent report must protect the first one. Option D overcorrects from advocate to executioner without analysis; doubled effort may still be worth it against the strategy's benefits, and that is precisely what the re-estimate exists to discover. Scored behaviours: intellectual honesty about your own initiatives, evidence over ego, and keeping decision rights where they belong — with the board, fully informed.

**Question 6 (moderate) — Most and least effective: a peer lead's team heading into a known trap**

A peer lead's team, in a different part of the organisation, is about to adopt a build orchestration approach your teams abandoned last year after painful capacity and reliability problems. You discover this from a design document circulated for general awareness — you were not asked for input. Identify the most effective and least effective responses.

1. Contact the peer lead directly: share your teams' experience, the specific failure modes and the data, and offer a session between your engineers and theirs — while being clear their context may differ and the decision is theirs.
2. Say nothing — their team, their decision, and unsolicited advice between peers is presumptuous.
3. Comment on the circulated document copying both teams' engineers, listing the reasons the approach failed for you.
4. Mention it to your shared head of profession, suggesting they steer the peer's team away from the approach.

- A) Most effective: 1; least effective: 2
- B) Most effective: 1; least effective: 4
- C) Most effective: 3; least effective: 2
- D) Most effective: 1; least effective: 3

**Correct answer: A**

**Explanation:** Option 1 is the model of "leading the sharing of knowledge and good practice": experience offered peer-to-peer, with data, with humility about context, and with decision rights explicitly left where they belong. Choosing the least effective among 2, 3 and 4 is the finer judgement. Option 3 is clumsy — correcting a peer's direction in front of both teams' engineers risks embarrassing them — but it is at least transparent, on-the-record technical input to a document circulated for awareness. Option 4 goes around the peer to their shared boss without ever speaking to them — the move most corrosive to peer trust, and inefficient too, converting a data-sharing conversation into a political one. But option 2 is scored least effective here for a structural reason: it guarantees the organisation pays twice for the same lesson, at the certain cost of a colleague's team's months of pain, to protect a notional etiquette that option 1 demonstrates is easily respected. Knowledge that leads keep siloed out of politeness is a failure of the exact duty your level exists to perform; between a social risk (1), a style error (3), a trust error (4) and a certain organisational loss (2), the certain loss ranks last. If you chose B, note the argument — going over a peer's head is genuinely bad — but silence was the only option with no route to a good outcome at all.

**Question 7 (challenging) — Security disclosure versus product deadline**

A penetration test on one of your product line's services, commissioned ahead of a major public launch in ten days, reports a vulnerability rated high: exploitation is complex but would expose a subset of citizens' personal data. The fix is estimated at seven days' work with three days' retest — putting the launch date at risk. The programme director, under ministerial expectation, asks whether the launch can proceed with the fix following "shortly after". What is the most effective response?

- A) Agree — exploitation is complex, ten days of exposure is a small window, and the ministerial commitment matters.
- B) State that launching with a known high-rated exposure of citizen data is not a risk you can recommend; propose the realistic options — delay by the few days the fix requires, launch with the vulnerable component disabled or degraded if technically separable, or launch to a limited cohort that reduces exposure — and ensure the decision, if made against your recommendation, is taken explicitly at the accountable level with the risk formally recorded.
- C) Refuse to discuss options and escalate directly to the department's security team to block the launch.
- D) Quietly instruct your teams to begin the fix but tell the programme director the launch can proceed, assuming the fix will land in time.

**Correct answer: B**

**Explanation:** Citizen data is the non-negotiable at the centre; everything else is negotiable, and B is the only option that treats both halves properly. It gives an unambiguous professional recommendation — leads are paid for the clarity of "I cannot recommend this", not for softening it — while doing the product-owner work of generating real options that might dissolve the dilemma: component separation and cohort limitation frequently turn "delay or expose" into "launch safely, smaller". And it respects the constitutional reality that risk acceptance at this consequence level belongs to the accountable owner, formally recorded — not because recording protects you, but because forcing the record forces the real decision. Option A quietly normalises "complex exploitation" into "acceptable exposure" — complexity is not a control, and a known vulnerability published into a high-profile launch is a documented breach-in-waiting. Option C abandons influence for procedure: blocking through the security team without exploring options may be where you end up, but starting there converts colleagues into adversaries and forfeits the solutions only your teams can see. Option D is a deception with a countdown timer — if the fix slips a day, you have launched a known-vulnerable service on the strength of your own false assurance. Scored behaviours: user protection as the anchor, option generation as the craft, explicit accountable decision-making as the backstop.

**Question 8 (challenging) — Credit flowing to the wrong place**

At a senior showcase, your head of profession warmly credits you personally for the automated compliance-checking capability that has halved audit preparation time across the department. In fact, the design and the persistent advocacy for it came from one of your senior engineers, who is watching from the audience, and who is currently weighing an external job offer. What is the most effective response?

- A) Accept the praise gracefully — correcting a senior leader publicly is awkward, and you can thank the engineer privately later.
- B) Redirect the credit immediately and specifically: name the engineer as the capability's designer and driving force, describe what they did, and let the room's recognition land where it belongs — following up afterwards to ensure the attribution sticks in any written record.
- C) Say "it was a team effort" and move on.
- D) Interrupt to explain that you personally only did the governance work.

**Correct answer: B**

**Explanation:** Credit is a currency, and at lead level you are largely a distributor of it rather than an earner: your engineers' work becomes visible to the organisation mostly through what you say about it. Option B redirects specifically — naming the person and the contribution, which converts vague warmth into career capital: showcases are where promotion cases and retention counter-offers are quietly born, and this engineer is holding an external offer today. The follow-up on written records matters because attributions in minutes and papers outlive the meeting. Option A banks your engineer's work in your account; the private thank-you afterwards does not compensate, because the engineer watched the public version — and so did everyone else deciding whether working hard on your product line is worth it. Option C is the lazy egalitarianism that feels generous and rewards no one; "team effort" praise is unfalsifiable and unmemorable, and specifically wrong here where the passage tells you one person designed and drove it. Option D turns redirection into self-flagellation, making the moment about you again. The scored behaviours — recognising others, developing careers, and building the culture where good work is visibly safe to invest in — are the retention strategy no counter-offer can match; a lead who reliably redirects credit finds their best people stop reading job boards.

**Question 9 (challenging) — A governance decision against your professional judgement**

The departmental design authority rules that all product lines, including yours, must adopt a centrally chosen observability platform. You argued against it with evidence: the platform lacks two capabilities your teams depend on, and your migration cost estimate is triple the central assumption. The ruling is final. Your teams are angry and one senior engineer proposes "malicious compliance": migrate exactly as instructed and let the failures make the case. What is the most effective response?

- A) Adopt the platform in good faith: plan the migration honestly, engineer the best available mitigations for the capability gaps, register the risks and costs formally so the record is accurate, and revisit the decision through governance if the predicted problems materialise — telling your teams exactly this plan and why.
- B) Endorse the malicious compliance plan — the fastest way to reverse a bad decision is to let it fail visibly.
- C) Delay migration indefinitely through slow-rolled planning while formally appearing to comply.
- D) Tell your teams the decision is wrong but must be followed, and that their frustration is justified.

**Correct answer: A**

**Explanation:** You argued with evidence, through the right forum, and lost: that is governance working, not failing, and what happens next defines your teams' relationship with every future ruling. Option A is full-faith compliance with full-honesty records: mitigations engineered seriously (your duty to your users does not lapse because you disagree with the tooling), risks and true costs registered formally (so the organisation learns from accurate data, and any future revisit stands on records rather than resentment), and — critically — your teams told the whole plan, including the legitimate route by which the decision could change. That last element is what converts angry engineers into professionals watching due process work. Option B weaponises your own services' reliability: "let it fail visibly" means letting citizen-facing observability degrade to score a governance point — a betrayal of user focus dressed as strategy, and one your teams would learn to use on you next. Option C is B with plausible deniability and a longer timeline. Option D validates the feeling and abandons the leadership: agreement-plus-shrug teaches learned helplessness, and quietly licenses the corner-cutting it claims to forbid. The scored behaviours: institutional integrity after losing an argument, honest records over quiet sabotage, and leading teams through disagreement rather than merely sharing it.

**Question 10 (challenging) — Building an inclusive senior pipeline**

You have an open senior engineer position. Your two internal candidates: engineer M, confident and vocal, who has asked for the role repeatedly and matches the "obvious" profile; and engineer J, quieter, from a group under-represented in your senior cohort, whose delivery record is at least as strong but who has not put themselves forward and, when sounded out, said "I'm probably not ready". Your senior cohort currently all share similar backgrounds. What is the most effective response?

- A) Appoint M — they want it, they fit the profile, and J has self-selected out.
- B) Appoint J — the cohort needs diversity and their record justifies it.
- C) Run a fair, structured process against defined role criteria and actively ensure J genuinely competes: tell them directly and specifically why their record makes them a credible candidate, address the "not ready" self-assessment with evidence, and offer the same preparation support to both — then appoint on merit against the criteria.
- D) Delay the decision and hire externally to avoid choosing between them.

**Correct answer: C**

**Explanation:** The scenario hides its trap in "J has self-selected out". Confidence-gated pipelines reproduce themselves: research and workplace experience consistently show that members of under-represented groups are less likely to self-nominate at equal competence, so a process that treats self-promotion as the entry ticket selects for confidence and similarity, not capability — which is precisely how your cohort came to share one background. Option C fixes the process rather than rigging the outcome: structured criteria strip the "obvious profile" advantage that M's resemblance to the existing cohort confers; the direct, evidence-based conversation with J ("here is your delivery record; here is what the role needs; here is why the first maps to the second") addresses miscalibrated self-assessment without lowering any bar; and identical preparation support keeps the competition fair in both directions — M may still win on merit, and if so, deserves to. Option A launders a structural bias through the language of enthusiasm. Option B corrects the demography by abandoning the fairness that makes the correction defensible — an appointment J themselves would carry as an asterisk, and M's allies would too. Option D pays an external premium to avoid a leadership decision and develops nobody. Scored behaviours: inclusion implemented through process design, courageous specific feedback, and merit protected precisely by making the competition genuinely open. This is also succession planning — shaping who becomes senior is the longest-lasting technical decision a lead makes.

**Question 11 (challenging) — Most and least effective: incident accountability across teams**

A serious outage takes down three services for four hours. The immediate cause: a certificate expiry in a shared component owned by your platform team; the renewal automation had been failing silently for weeks, and the alert for it was accidentally disabled during an unrelated cleanup by one of your engineers, who realises this during the incident and is distraught. A programme director emails asking "who is responsible?" Identify the most effective and least effective responses.

1. Reply naming the engineer whose cleanup disabled the alert, since that is factually where the chain began.
2. Reply that responsibility sits with you as the accountable lead; commit to a blameless post-incident review of the systemic failures — silent automation failure, single unmonitored alert, no expiry pre-warning — with actions to follow; separately, support the distraught engineer and make clear their honesty during the incident shortened it.
3. Reply that the outage was a process failure and no individual or team is responsible.
4. Reply accepting accountability, but privately move the engineer off platform work as a precaution.

- A) Most effective: 2; least effective: 1
- B) Most effective: 2; least effective: 4
- C) Most effective: 3; least effective: 1
- D) Most effective: 2; least effective: 3

**Correct answer: A**

**Explanation:** Option 2 is the complete lead-level answer, holding three truths at once: accountability is yours (the component is your team's; accountability at level is not transferable downwards, and saying so plainly is what "who is responsible?" deserves); learning must be systemic (a single disabled alert cannot cause a four-hour, three-service outage unless renewal automation can fail silently, expiry has no pre-warning, and monitoring has no redundancy — the review's real material); and the human being at the sharp end needs protecting, because how you treat the distraught engineer this week determines whether the next near-miss gets reported early or hidden. For least effective, compare 1, 3 and 4. Option 3 is evasive — "no one is responsible" reads as accountability-dodging to a director and wastes the legitimate question — but it at least harms no individual. Option 4 accepts accountability publicly while privately punishing the engineer, quietly teaching the team that honesty costs careers; seriously harmful. But option 1 is the worst: it answers an accountability question by publicly naming the most junior person in the causal chain, which is factually misleading (the chain began years earlier, in unmonitored automation design), managerially cowardly (redirecting a question aimed at you), and culturally catastrophic — it guarantees the next engineer who realises their mistake mid-incident says nothing, lengthening every future outage. Blame flows down only in organisations that have chosen not to learn; a lead's post-incident behaviour is the strongest culture-setting broadcast available.

### Preparation tips

- **Answer as the accountable owner, not the smartest engineer.** Lead-level scoring rewards keeping decision rights with the right forum, accountability with yourself, and credit with your people. If your instinctive answer transfers any of these to the wrong place, look again.
- **Generate the third option.** Most scenarios present a false binary — commit or refuse, launch or block, M or J. The scored answer usually restructures the choice: options papers, tiered policies, structured processes, separable components. Practise asking "what choice architecture dissolves this dilemma?"
- **Protect the reporting channel.** In any scenario touching mistakes, near-misses or bad news, rank the options first by what they teach people about the safety of telling the truth. Culture-of-candour damage outlasts every other cost.
- **Watch for quiet deceptions.** "Quietly deprioritise", "broadly successful", "privately move them" — options containing an unannounced divergence between what stakeholders believe and what is happening are reliably scored worst, even when well-intentioned.
- **Rehearse your organisation's published behaviours** — user focus, honesty, developing others, inclusion — before the test, and for each scenario ask which option a person embodying all four would choose. Ties break on user impact.
- **In most/least formats, rank the harms.** Certain organisational loss, individual scapegoating, and trust-destroying secrecy usually outrank mere clumsiness. Deciding least-effective carefully is where these questions are won.

### Common pitfalls to avoid

- **Making the trade-off in secret.** Overcommitting and silently dropping something is the management-track cardinal sin: it converts a resource problem into an integrity problem.
- **Confusing decisiveness with verdicts.** Imposing your answer on a resolvable conflict scores worse than building the policy that resolves this conflict and the next one.
- **Protecting your initiative instead of the truth.** When your own strategy's pilot returns bad news, advocacy must yield to evidence — visibly.
- **Letting etiquette silo knowledge.** Politeness that lets a peer's team repeat your expensive mistake fails the profession. Share experience humbly, and leave the decision with its owner.
- **Accepting misdirected credit or deflecting deserved accountability.** Both are currency thefts — one steals from your people, the other from your own role. The SJT tests whether you know which direction each should flow.
- **Fixing demography by abandoning process, or protecting process by ignoring demography.** Inclusion scenarios reward redesigning the process so that merit and openness stop being in tension.

<!-- APPEND -->
