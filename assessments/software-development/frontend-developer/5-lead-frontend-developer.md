# Lead Frontend Developer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a lead frontend developer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your capability against the framework, or refreshing the reasoning skills that leadership tends to exercise less visibly than code does, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a lead frontend developer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — cross-team quality dashboards, architecture and standards decisions, accessibility audit programmes, performance budgets spanning multiple services, community talks, governance papers and escalations — and the kinds of judgements you genuinely make, such as setting direction and assuring the quality of development across teams, making and justifying decisions characterised by high levels of risk, impact and complexity, mediating between people and mending relationships, and identifying the appropriate technology and approach from a wide field of options.

Why do these assessments matter at your level in particular? As a lead, you are an expert practitioner whose influence extends well beyond any single codebase. You lead multiple or highly complex services, you provide technical leadership, coaching and mentoring to a community, you speak on behalf of that community to large audiences inside and outside government, and you build consensus between highly independent stakeholders. Every one of those responsibilities rests on the capabilities these assessments measure: reasoning accurately about systems and standards at scale, reading numerical evidence well enough to direct investment across teams, extracting precise meaning from dense documents whose misreading would mislead many people, and exercising judgement in situations where the options are all defensible and the difference between good and best is the whole game.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it at lead level, a mapping of the assessment dimensions to the specific skills in the frontend developer capability framework at lead level, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

Here is how to get the most from it. First, read each "About this assessment" section so you understand the format and pacing. Second, attempt the practice questions honestly — commit to an answer before reading the explanation, and note where your confidence was misplaced in either direction. Third, treat every explanation as a mini-lesson: the walkthroughs are written to expose method, not just answers, and several deliberately model the checking habits that distinguish expert reasoning. Finally, use the preparation tips and pitfalls for reflection — and consider which questions would make good coaching material for the seniors and developers you mentor, because working through a scenario together is one of the best teaching formats there is.

Leadership can quietly erode the sharpness of skills you no longer use daily, and quietly grow ones no test has ever measured for you before. This guide exercises both. Take your time, enjoy the practice, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract shapes and sequences. Unlike a generic intelligence test, it presents you with the everyday materials of your job — standards documents, cross-team dashboards, dependency maps, audit findings, migration plans and governance constraints — and asks you to reason quickly and accurately about them.

Typical format: an online, timed test lasting 15 to 30 minutes, with 15 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group — for lead-level recruitment, often a demanding one — and many platforms adapt difficulty to your performance, so a test that feels like it is fighting back is usually going well. Employers typically receive speed and accuracy profiles rather than a single figure, and you will normally be offered unscored warm-up questions to learn the interface.

For a lead frontend developer, cognitive assessment is relevant in a way that differs subtly from more junior levels. The raw materials are similar — logic, patterns, constraints — but the scale and stakes change what the reasoning is for. You assure quality across teams, which means reasoning about aggregates and exceptions: which of five teams' practices genuinely diverge, which divergence matters, and which apparent anomaly is a measurement artefact. You are proficient in a wide range of technical systems and expected to identify the appropriate technology and approaches, which is multi-criteria decision reasoning under uncertainty. You lead multiple or highly complex services, which means the dependency graphs you reason about span organisations, procurement cycles and other people's roadmaps, not just build steps. And because your conclusions become other teams' direction, an error in your reasoning is multiplied before anyone catches it.

Employers use cognitive assessments at lead level precisely because of that multiplication. They want evidence that the person who will set direction, arbitrate technical disputes and justify high-impact decisions to boards reasons fast, accurately and — most importantly — with the discipline to know what the evidence does and does not establish.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your capability framework at lead level:

- **Pattern recognition** maps to **Modern development standards** — identifying and applying modern development standards to support complex projects and programmes means recognising, across many codebases, which local variations are the same underlying pattern and which are genuine divergence — and to **Prototyping**, where establishing design patterns and iterating them is pattern work by name.
- **Logical deduction** maps to **Systems integration (frontend developer)**: co-ordinating all aspects of integration across services requires valid reasoning from dependency rules, contracts and configuration to their consequences. It also maps to **Strategic thinking**, because leading the design and implementation of strategy means reasoning from principles and policies to what they entail for real teams.
- **Error checking** maps to **Accessibility** and **Programming and build (frontend developer)**: advising on the right way to apply standards and methods to ensure compliance means finding the gap between what teams claim and what artefacts show — audit responses that miss thresholds, support tables that miss requirements, remediations that miss the point.
- **Prioritisation** maps to **Leadership and guidance (frontend developer)**: making and justifying decisions characterised by high levels of risk, impact and complexity, and solving and unblocking issues between teams or departments, depends on rapidly ranking competing demands across a wider field than any one team's backlog.
- **Applied problem solving** maps to **Web performance optimisation** — identifying and resolving performance issues across services, guiding on the best software and methods — and to your duty to identify appropriate technology and approaches, which is structured elimination among options under real constraints.

### Practice questions

**Question 1 (easy) — Pattern recognition across team conventions**

You are reviewing how five teams name their shared frontend packages. The programme convention is: `@dept/<service>-<type>`, where type is one of `components`, `utils` or `styles`. You see:

1. `@dept/benefits-components`
2. `@dept/passports-utils`
3. `@dept/components-licensing`
4. `@dept/pensions-styles`
5. `@dept/grants-utils`

Which package name breaks the convention?

- A) Package 2
- B) Package 3
- C) Package 4
- D) Package 5

**Correct answer: B**

**Explanation:** The convention orders the parts as service first, then type. Package 3 inverts them: `components-licensing` puts the type before the service, so the compliant form is `@dept/licensing-components`. The other four all follow service-then-type with a valid type word. Trivial as it looks, this is the everyday texture of assuring quality across teams: conventions are cheap to follow and expensive to un-break, because tooling, discovery and automation are built against them — a search for all component packages by suffix silently misses package 3 forever. When you lead others in applying standards, the persuasive point is rarely the rule itself but the downstream machinery that depends on it; being able to articulate that machinery is what turns naming pedantry into technical leadership.

**Question 2 (easy) — Deduction from a standards policy**

Programme policy states: "Teams may adopt a new frontend framework only if it is on the approved list, or if they hold a written waiver from the lead frontend developer." You learn: "Team Kestrel has adopted a framework that is not on the approved list." You have issued no waivers this year, but your predecessor may have. Which conclusion must be true?

- A) Team Kestrel has breached the policy.
- B) Team Kestrel holds a waiver issued by your predecessor.
- C) If Team Kestrel holds no written waiver, it has breached the policy.
- D) The approved list is out of date.

**Correct answer: C**

**Explanation:** The policy permits two routes: approved list, or written waiver. The framework is off-list, so compliance now depends entirely on the waiver — about which the facts are genuinely uncertain, since your predecessor may have issued one. A asserts breach without ruling the waiver out; B asserts the waiver without evidence; D changes the subject. C is the conditional that holds in every consistent scenario: no waiver means breach. Notice that C is also the operationally useful conclusion — it tells you exactly what to check before acting. At lead level this discipline has teeth: publicly accusing a team of non-compliance you cannot yet prove damages the trust your cross-team role runs on, while quietly verifying the waiver register costs an email. Valid deduction and good stakeholder management are, here as often, the same behaviour.

**Question 3 (easy) — Error checking a quality dashboard**

Your programme's quality gate requires each service to have: automated accessibility checks passing, at least 80% unit test coverage on frontend code, and a performance budget check in the pipeline. The dashboard shows:

| Service | Accessibility checks | Coverage | Performance budget check |
|---|---|---|---|
| Licensing | Passing | 84% | In pipeline |
| Grants | Passing | 79% | In pipeline |
| Benefits | Passing | 91% | Not configured |
| Passports | Passing | 80% | In pipeline |

How many services currently fail the quality gate?

- A) 1
- B) 2
- C) 3
- D) 0

**Correct answer: B**

**Explanation:** Check each service against all three requirements. Licensing: passing, 84% ≥ 80%, in pipeline — passes. Grants: coverage is 79%, below the 80% threshold — fails. Benefits: performance budget check not configured — fails. Passports: passing, exactly 80%, in pipeline — passes, because "at least 80%" includes 80%. Two services fail. The two traps: reading "at least 80%" as "more than 80%" (which would wrongly fail Passports), and letting Benefits' excellent 91% coverage halo over its missing performance check — gates are conjunctions, and excellence on one criterion buys nothing on another. Assuring the quality of development across teams is substantially this: applying thresholds exactly as written, uniformly, including to teams whose other numbers are impressive, because the moment a gate flexes for a favoured team it stops being a gate.

**Question 4 (moderate) — Deduction through a migration dependency chain**

You are planning a design-system migration across services. Constraints: (i) the shared component library v2 must be published before any service migrates; (ii) the Benefits service cannot migrate until its major service assessment is over, which is at the end of Q2; (iii) Licensing shares a codebase with Grants, so they must migrate in the same quarter; (iv) the library team publishes v2 at the end of Q1; (v) at most two services can be in migration in any one quarter (Licensing and Grants count as two). Passports has no constraints beyond (i) and (v). What is the earliest quarter by which all four services can have migrated?

- A) Q2
- B) Q3
- C) Q4
- D) Q1

**Correct answer: B**

**Explanation:** Work the constraints forwards. v2 lands at end of Q1, so the earliest migration quarter for anyone is Q2. Benefits cannot migrate until after end of Q2, so Benefits' earliest quarter is Q3. In Q2, the capacity of two allows either Licensing+Grants (they must travel together and count as two) or Passports plus nothing else useful. Take Licensing+Grants in Q2 — filling the quarter — then Benefits and Passports together in Q3, which respects the capacity limit and Benefits' assessment constraint. All four are done by end of Q3. Q2 is impossible (Benefits is blocked); Q4 is achievable but not earliest; Q1 precedes the library. The reasoning pattern — find the binding constraint (Benefits' assessment), then pack the remaining capacity around it — is exactly how you sequence change across multiple services: the schedule is set by the least free team, and the lead's job is to make sure nobody else's work waits behind it unnecessarily.

**Question 5 (moderate) — Prioritisation across a portfolio**

Monday morning, four items compete for your attention as lead across several services:

1. A security advisory affecting a JavaScript dependency used by three of your services; exploitability is not yet clear.
2. A request to speak at a cross-government frontend community event in six weeks, requiring a decision this week so the agenda can be published.
3. A team's technical lead has resigned; the team has a design-system migration mid-flight and the delivery manager wants to discuss cover.
4. A pull request of yours on the shared component library has review comments awaiting your response; two teams are waiting on the release.

Which sequencing is most defensible?

- A) 1, 3, 4, 2 — triage the security exposure, stabilise the leaderless team, unblock the waiting teams, then decide the talk
- B) 4, 1, 3, 2 — unblock others first, always
- C) 3, 1, 4, 2 — people problems always precede technical ones
- D) 1, 4, 3, 2 — security, then code, then people, then community

**Correct answer: A**

**Explanation:** Item 1 leads under any defensible weighting: a potentially exploitable dependency across three live public services is the highest-impact unknown on the list, and triage — establishing exploitability and exposure — is quick and shrinks the biggest risk first; note that triage, not necessarily full remediation, is what belongs at the top of Monday. Item 3 is next: a leaderless team mid-migration is a compounding delivery and people risk, and a same-day conversation with the delivery manager starts cover moving. Item 4 unblocks two teams with perhaps an hour's focused work and follows immediately. Item 2 has a real deadline but it is "this week", not today. Option B elevates a code-review courtesy over a portfolio security risk; C hardens a good instinct (people matter) into a rule that ignores magnitudes; D is nearly right but leaves a leaderless team waiting behind a code review, mis-ranking a compounding risk behind a bounded one. Lead-level prioritisation is portfolio triage: impact-weighted urgency, with special weight for risks that grow while you are not looking.

**Question 6 (moderate) — Pattern recognition in cross-team audit findings**

Accessibility audits across four services report their top findings: Licensing — custom select component fails keyboard testing; Grants — modal dialogue traps focus incorrectly; Benefits — autocomplete announces nothing to screen readers; Passports — date picker unusable without a mouse. Standard GOV.UK-style form elements across all four services show near-zero findings. What is the most useful conclusion for you as lead?

- A) The four teams have four unrelated problems requiring four unrelated fixes.
- B) Custom interactive widgets are the systematic weak point; the programme needs shared, accessibility-tested implementations (or design-system alternatives) instead of per-team rebuilds.
- C) The audits are unreliable because they found different things in different services.
- D) Teams should stop using JavaScript for interactive elements.

**Correct answer: B**

**Explanation:** Read across the findings rather than down them: every failing artefact is a custom-built rich widget (select, modal, autocomplete, date picker), and every near-clean area is standard, well-tested componentry. The pattern is not four defects but one capability gap — building accessible custom interactive widgets is genuinely hard, and four teams are each failing at it independently, which is also four times the remediation cost. The lead-level response is structural: provide shared, audited implementations once, or steer teams to existing design-system patterns, converting an ongoing per-team risk into a solved-once problem. Option A is what each team sees from inside; seeing the cross-team pattern is precisely what your position exists for. Option C misreads variety of symptom as inconsistency of method. Option D overcorrects into absurdity — the fix for hard-to-build widgets is to build them once, well, not to abandon interactivity. Identifying and applying standards to support complex programmes starts with spotting exactly this kind of pattern.

**Question 7 (moderate) — Error checking a performance budget exception**

Your programme's performance budget states: no page may ship more than 300 KB of compressed JavaScript; exceptions require a documented trade-off and an agreed remediation date. A team requests an exception: "Our mapping page ships 480 KB because the mapping library is 260 KB. Without the library the page would be 220 KB, which is under budget, so the exception should be automatic. We propose remediation by Q3." What is the flaw in the team's argument?

- A) There is no flaw; the request is sound.
- B) The arithmetic is wrong: 480 − 260 is 220, so the library must be bigger than claimed.
- C) "We would be under budget without the thing that puts us over budget" is true of every over-budget page, so it cannot be grounds for an automatic exception; the request must instead justify why this library's value warrants the cost.
- D) The remediation date is too far away.

**Correct answer: C**

**Explanation:** Check the arithmetic first: 480 − 260 = 220, so the numbers are internally consistent and B is wrong. The flaw is logical, not arithmetic. Every page that exceeds a budget would be under it without its heaviest content — the observation is vacuously true and therefore discriminates nothing; if it justified automatic exceptions, the budget would be a budget for everything except the things that break it. A sound exception request argues the trade-off the policy actually asks for: what user value the 260 KB library delivers, what lighter alternatives were considered and why they fall short, and what the remediation path is. D is a judgement call, not a flaw in the argument as posed — Q3 might be fine. Spotting the vacuous step inside fluent, numerate prose is a core lead skill: much of advising on the right way to apply standards is noticing when a well-written request quietly asks for the standard not to apply.

**Question 8 (moderate) — Deduction about a shared library's blast radius**

Facts: (i) every service in the programme uses the shared component library; (ii) services pin library versions and upgrade on their own schedules; (iii) a bug exists in library versions 4.2 and 4.3, and only those; (iv) the Grants service is unaffected by the bug. Which conclusion must be true?

- A) Grants is not on version 4.2 or 4.3.
- B) Grants is on a version earlier than 4.2.
- C) Most services are unaffected, since Grants is.
- D) Any service on version 4.3 is affected by the bug.

**Correct answer: D**

**Explanation:** Test each option against the facts. A looks tempting, but "unaffected" is not the same as "not running the buggy version": a service could run 4.2 yet be unaffected because it never uses the buggy component — the facts say the bug exists in those versions, not that every user of those versions suffers it. So A can fail in a consistent scenario. B goes further than A and fails the same way. C generalises from one service to most, which nothing supports. D restates fact (iii) correctly at service level: the bug exists in 4.3, so a service on 4.3 is running affected code — it is "affected by the bug" in the sense of carrying it, whether or not the symptom has surfaced yet. This distinction — between carrying a defect and experiencing it — is one you use constantly when co-ordinating integration across services: the blast radius of a library bug is defined by versions shipped, not by symptoms reported, which is why "no one has complained" is never the same as "no one is exposed".

**Question 9 (challenging) — Multi-constraint technology selection**

You must recommend one approach for adding rich data-visualisation to three services. Requirements, in priority order set by the programme: (1) accessible to WCAG 2.2 AA including keyboard and screen reader use; (2) maintainable by the existing frontend community, whose skills are HTML, CSS, JavaScript and the standard framework; (3) total added page weight under 150 KB; (4) delivery within one quarter. The candidates: W — a canvas-based charting library, 90 KB, fast to adopt, but its output is a bitmap requiring a parallel text alternative to be built for every chart; X — an SVG-based library, 120 KB, renders accessible markup with modest configuration, uses the community's existing skills; Y — a vendor's hosted visualisation platform, 30 KB embed, accessible, but charts are configured in the vendor's proprietary tool, not in code; Z — build a bespoke SVG charting layer in-house, fully controllable, estimated at two quarters. Which recommendation best fits the stated priorities?

- A) W
- B) X
- C) Y
- D) Z

**Correct answer: B**

**Explanation:** Apply the priorities in order, eliminating as you go. Requirement 1: W's bitmap output makes accessibility a perpetual parallel-build obligation — achievable but structurally fragile, since every new chart can silently ship without its text alternative; X, Y and Z can all satisfy AA natively. Requirement 2: Y's proprietary configuration tool sits outside the community's skills and outside code review, version control and open working — maintainability by your community is exactly what it lacks; X and Z use the community's SVG/JavaScript skills. Requirement 3: X at 120 KB fits under 150 KB. Requirement 4: Z's two quarters breaches the one-quarter constraint. X alone survives all four filters. The method matters as much as the answer: with priorities stated, selection is sequential elimination, not holistic vibes — and documenting which requirement eliminated each candidate is what makes the recommendation justifiable later, which is the standard your **Leadership and guidance** skill sets: make and justify decisions of high impact. It is also what makes the decision teachable when the next lead asks why the vendor platform lost.

**Question 10 (challenging) — Applied problem solving on a cross-service regression**

After a Tuesday release of the shared component library, dashboards show: Licensing's page-load metrics degraded sharply from Tuesday; Grants' metrics are unchanged; Benefits' metrics degraded, but starting the previous Friday; Passports has not yet taken the new library version and is unchanged. Which hypothesis best fits all the evidence?

- A) The library release degraded performance for every service that took it.
- B) The library release likely degraded Licensing; Benefits' degradation has a different, earlier cause; Grants may not exercise the affected code path.
- C) The library release is innocent, since Grants took it and is unaffected.
- D) Benefits' degradation proves the problem predates the library and therefore Licensing's issue is unrelated to the release.

**Correct answer: B**

**Explanation:** Fit each hypothesis to all four services, not a convenient subset. Licensing: degradation coincides with taking the release — consistent with the library as cause. Benefits: degradation began Friday, four days before the release existed in their build — the release cannot have caused a regression that predates it, so Benefits needs another explanation. Grants: took the release, unaffected — which weakens "the release degrades everyone" but is fully compatible with "the regression lives in a component or code path Grants does not use". Passports: a clean control, untouched and unchanged. Option A is falsified by Grants; C treats one unaffected consumer as exoneration, ignoring path-dependence; D commits the inverse error, letting Benefits' unrelated earlier problem launder the library's very specific Tuesday coincidence at Licensing. B alone respects every timeline. This is the daily epistemology of leading multiple services: shared infrastructure means correlated symptoms, but each service's timeline must be read on its own before you aggregate — and the fastest next step, checking which components Licensing uses that Grants does not, falls straight out of the correct hypothesis.

**Question 11 (challenging) — Prioritising standards effort by leverage**

You have capacity to drive one standards initiative this quarter across your ten teams. Evidence in hand: (a) three teams still lack automated accessibility checks, and manual audits in those teams find roughly four times the defect rate of the other seven; (b) all ten teams format code inconsistently, generating frequent low-heat review comments; (c) two teams use an outdated build tool, adding roughly five minutes to their build times; (d) one team's service has a performance issue on its most-used page, harming users now, which that team can fix with two days of guided pairing. Which allocation of your quarter is most defensible?

- A) Initiative (b) — it touches all ten teams, the widest reach.
- B) Spend two days on (d) immediately, then drive (a) as the quarter's initiative.
- C) Initiative (c) — build speed compounds across every developer's day.
- D) Initiative (a) alone, declining (d) as one team's local problem.

**Correct answer: B**

**Explanation:** Separate the item that is cheap, urgent and user-facing from the items competing for the quarter. (d) harms users today and costs two days of pairing — taking it first is triage, not a quarter's initiative, and declining it (option D) to protect a plan mistakes tidiness for leadership. Among the real initiatives, weigh leverage: (a) targets a four-times defect-rate gap on a user-harming dimension in three identified teams, and automated checks keep paying after you move on — high impact, durable, measurable. (b) touches everyone but the harm is reviewer irritation, and the fix is largely mechanical (adopt a formatter) — worth doing, but it does not need your quarter; it needs a decision and a lunch-and-learn. (c) helps two teams' feedback loops modestly. The leverage ranking is (a), then (c) or (b). Option B sequences the urgent small fix and the high-leverage initiative — which is the general shape of lead-level capacity allocation: protect a triage margin, then spend the strategic capacity where the differential impact is largest, not where the audience is widest. Reach multiplied by depth of harm beats reach alone.

**Question 12 (challenging) — Deduction under governance constraints**

Programme rules: (i) any change to the shared design system requires a published RFC open for comment for at least ten working days; (ii) security fixes are exempt from rule (i) but must be disclosed to all teams within 24 hours of release; (iii) breaking changes additionally require a major version bump and a migration guide at release. On the 3rd, a design-system release shipped that removed a deprecated component (a breaking change) and patched an XSS vulnerability in another component. No RFC was published. A migration guide and major version bump shipped with the release, and all teams were notified on the 4th. Which statement is correct?

- A) The release was fully compliant: the security exemption covers the whole release.
- B) The security patch was compliant, but the component removal breached rule (i): the exemption attaches to the security fix, not to unrelated changes shipped alongside it, though rule (iii) was satisfied.
- C) The release breached rule (ii) because notification arrived a day after release.
- D) The release breached rule (iii) because breaking changes also require an RFC.

**Correct answer: B**

**Explanation:** Parse what each rule attaches to. Rule (ii)'s exemption is for security fixes — the XSS patch qualifies, and notification "on the 4th" for a release "on the 3rd" sits within 24 hours as far as the facts show, so C overreaches (it would need timestamps to establish a breach, and a test rewards you for noticing that). The component removal is not a security fix; bundling it into the same release does not extend the exemption to it — exemptions attach to changes, not to vehicles — so the removal needed the ten-day RFC it never got: rule (i) breached. Rule (iii) asked for a major bump and migration guide, both delivered; D invents an RFC requirement inside rule (iii) that the text does not contain. So B: partially compliant, precisely located. This close-reading of which obligations attach to what is the lead's bread and butter — the same skill that stops a team using an emergency-change route to smuggle ordinary work past governance, a pattern you will meet in real change advisory conversations more than once.

### Preparation tips

- **Practise at portfolio altitude.** Your daily work is full of cross-team tables, dependency plans and exception requests. Once a week, take one and formalise it: what exactly are the constraints, what must be true, what merely might be? That is the test, rehearsed on live material.
- **Rehearse sequential elimination.** For technology and approach decisions, write the criteria in priority order and eliminate candidates one criterion at a time. It is both a test technique and the justification structure boards find most persuasive.
- **Hunt the vacuous step.** In every exception request or proposal you read this month, ask: would this argument work for anything? Arguments that prove too much are the lead-level error-check.
- **Time-box and triage.** At 60 to 90 seconds per question, flag and move on when stuck. Your role is portfolio triage; apply it to the test itself.
- **Verify which facts attach to which entities.** Bugs attach to versions, exemptions to changes, constraints to teams. Misattachment is the engineered error in most hard deduction items.
- **Arrive rested, with paper.** Sketching a dependency chain or a small table beats holding it in your head, and the two minutes of setup pays for itself by question three.

### Common pitfalls to avoid

- **Reasoning from a convenient subset.** Hypotheses must fit all the services, all the rows, all the timelines. The wrong options are usually right about some of the evidence.
- **Letting one clean case exonerate a shared cause.** An unaffected consumer of a shared library weakens a universal claim, not a path-dependent one. Distinguish them explicitly.
- **Treating gates as impressions.** Quality gates are conjunctions applied uniformly. A team's excellence on two criteria never offsets failure on a third, in tests or in programmes.
- **Confusing "carrying a defect" with "experiencing it".** Exposure is defined by what shipped, not by what has been reported. Options that equate silence with safety are traps.
- **Over-weighting reach against depth.** "Touches all ten teams" is seductive; leverage is reach multiplied by harm addressed and durability of the fix. The widest initiative is often the shallowest.
- **Spending three minutes rescuing one question.** Bank the marks you can take; adaptive tests make stubbornness expensive.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace numeric reasoning assessment measures your ability to interpret, manipulate and draw sound conclusions from numerical information of the kind your role actually produces. The mathematics itself stays within percentages, ratios, averages, rates and proportional change; the difficulty is in reading data precisely under time pressure, choosing the correct operation, and declining the plausible wrong answer that the test has thoughtfully provided.

Typical format: an online, timed test of 20 to 30 minutes with 15 to 25 questions, each hung on a short table, chart or data statement. Calculators are usually allowed — the assessment targets reasoning, not arithmetic speed — and adaptive versions adjust difficulty as you answer. Employers receive accuracy and pace profiles benchmarked against a norm group appropriate to the level.

For a lead frontend developer, numbers are the language in which your influence travels. You assure quality across teams through dashboards: coverage percentages, defect rates, Core Web Vitals percentiles, audit finding counts. You direct the evaluation of strategies — your **Strategic thinking** skill — which means judging from measurements whether a strategy is working and where investment should move. You justify decisions characterised by high levels of risk and impact, and at that altitude a decision is justified with quantities: costs compared over sensible time horizons, capacity converted honestly into schedules, benefits expressed in units a programme board recognises. And because teams quote your numbers onwards, an arithmetic slip by a lead does not stay a slip — it becomes three teams' planning assumption.

There is also a subtler reason numeric reasoning matters at your level: aggregated data behaves counterintuitively. Averages across teams of different sizes mislead unless weighted; a metric can improve in every segment while worsening overall; a percentage change on a small base can look more dramatic than a larger absolute change elsewhere. Leads sit exactly where these effects live — at the aggregation layer — and employers test for the numeracy that resists them.

### How this assessment maps to your role

- **Percentages and proportional change** map to **Web performance optimisation** and **Modern development standards**: budgets, regressions, savings and adoption rates across services are all percentage statements, and guiding on the best methods includes getting those statements exactly right.
- **Weighted averages and mix effects** map to your duty to assure quality across teams and to **Strategic thinking**: portfolio-level metrics must be weighted by team size, traffic or output before they mean anything, and directing the evaluation of strategy requires recognising when an aggregate is being moved by mix rather than by performance.
- **Ratios, rates and capacity arithmetic** map to **Leadership and guidance (frontend developer)** and your duty to lead multiple or highly complex services: converting team capacity into credible migration timelines, and defect counts into comparable rates, is how cross-team plans stay honest.
- **Cost comparison over time** maps to making and justifying high-impact decisions: tooling, platform and approach choices carry different cost shapes (per-seat, flat, one-off), and comparing them over a sensible horizon is the arithmetic beneath "identify appropriate technology".
- **Reading tables and percentiles** maps to **Communicating information**: when you represent the community's work to boards and large audiences, you are the person who must read the percentile table correctly the first time, and translate it faithfully.

### Practice questions

**Question 1 (easy) — Migration progress percentage**

Your design-system migration covers 180 components across the programme. So far, 45 have been migrated. What percentage of the migration is complete?

- A) 20%
- B) 25%
- C) 30%
- D) 40%

**Correct answer: B**

**Explanation:** Step 1: form the fraction complete: 45 ÷ 180. Step 2: simplify: 45 ÷ 180 = 0.25. Step 3: convert to a percentage: 0.25 × 100 = 25%. A quick mental route: 45 is a quarter of 180 because 45 × 4 = 180. When you report programme progress upwards, this is the headline number — but note for real reporting (a point the test cannot ask but your role does) that components rarely cost equal effort, so "25% of components" and "25% of the work" can differ; a lead who says which one they are reporting earns trust. For the test itself, the skill is speed with certainty on items like this, banking time for the harder questions ahead.

**Question 2 (easy) — Mean of a portfolio metric**

Five services report largest-contentful-paint times (75th percentile, in seconds) of 2.8, 2.4, 3.0, 2.2 and 2.6. What is the mean of these values?

- A) 2.5 s
- B) 2.55 s
- C) 2.6 s
- D) 2.7 s

**Correct answer: C**

**Explanation:** Step 1: sum the values: 2.8 + 2.4 = 5.2; 5.2 + 3.0 = 8.2; 8.2 + 2.2 = 10.4; 10.4 + 2.6 = 13.0. Step 2: divide by the count: 13.0 ÷ 5 = 2.6 s. Sanity check: the values span 2.2 to 3.0, and 2.6 sits comfortably inside. Worth noticing professionally: this is an unweighted mean of five services' percentiles, which treats a service with a million users and one with ten thousand as equal — fine for a quick portfolio glance, misleading for investment decisions, where the traffic-weighted view (as in the next questions) is the honest one. The test asks for the simple mean; your job asks you to know which mean you are looking at.

**Question 3 (easy) — Splitting effort by ratio**

Your shared component library team plans a 40-day quarter of effort split between bug fixes, new components and maintenance in the ratio 2 : 3 : 5. How many days go to new components?

- A) 8
- B) 10
- C) 12
- D) 20

**Correct answer: C**

**Explanation:** Step 1: total the ratio parts: 2 + 3 + 5 = 10. Step 2: one part = 40 ÷ 10 = 4 days. Step 3: new components take 3 parts: 3 × 4 = 12 days. Check the full split: bugs 8, new components 12, maintenance 20; 8 + 12 + 20 = 40, which matches. The distractors are the other categories (8 and 20) plus a tempting round number — always re-read which category the question wants before answering. Ratio splits are how a lead communicates investment intent to a shared team without micro-planning it, and being able to convert instantly between the ratio, the days and the percentages (20% / 30% / 50% here) keeps that conversation fluent in front of stakeholders.

**Question 4 (moderate) — Percentage points across a portfolio**

Across your programme, average frontend test coverage rises from 72% to 81% over two quarters. Which statement is accurate?

- A) Coverage rose 9%, a modest gain.
- B) Coverage rose 9 percentage points, a relative increase of 12.5%.
- C) Coverage rose 12.5 percentage points.
- D) Coverage rose 9 percentage points, a relative increase of 9%.

**Correct answer: B**

**Explanation:** Step 1: the absolute change is 81 − 72 = 9 percentage points. Step 2: the relative change is measured against the start: 9 ÷ 72 = 0.125 = 12.5%. So: nine points, twelve and a half percent relative. Option A's "9%" mislabels a points change as a relative one — technically wrong and rhetorically undersold; option D computes no division at all; option C swaps the two figures. As the person who presents portfolio quality trends to boards, this distinction is yours to police in both directions: a rise from 2% to 4% coverage is "100% improvement" in relative terms and still a disaster in absolute ones, while 72 to 81 is a solid nine-point gain that "9%" undersells. Leads who state both numbers, labelled correctly, make their dashboards resistant to spin — including their own.

**Question 5 (moderate) — Weighted defect rate across teams**

Three teams deliver in a quarter: Team A, 40 story points with 2.0 defects per 10 points; Team B, 60 points with 1.5 defects per 10 points; Team C, 100 points with 1.0 defect per 10 points. What is the programme's overall defect rate per 10 story points?

- A) 1.5
- B) 1.35
- C) 1.17
- D) 1.25

**Correct answer: B**

**Explanation:** Step 1: convert rates to counts. Team A: (40 ÷ 10) × 2.0 = 8 defects. Team B: (60 ÷ 10) × 1.5 = 9 defects. Team C: (100 ÷ 10) × 1.0 = 10 defects. Step 2: total defects: 8 + 9 + 10 = 27. Step 3: total points: 40 + 60 + 100 = 200. Step 4: overall rate: 27 ÷ (200 ÷ 10) = 27 ÷ 20 = 1.35 per 10 points. The distractor 1.5 is the unweighted mean of the three rates ((2.0 + 1.5 + 1.0) ÷ 3), which overstates the true rate because the largest team has the best quality. The general law: aggregate rates by re-deriving counts over totals, never by averaging the rates themselves. This arithmetic is your quality-assurance role in miniature — and note the leadership insight hiding in the numbers: the programme's rate is being carried by Team C's volume, so protecting whatever Team C is doing right matters more than the average suggests.

**Question 6 (moderate) — Comparing tooling costs over time**

You are choosing an accessibility testing tool for 40 developers. Tool A costs £15 per developer per month. Tool B costs £5,000 per year flat, plus a one-off £50 per developer onboarding cost in the first year. Over two years, which tool is cheaper, and by how much?

- A) Tool A, by £2,400
- B) Tool B, by £2,400
- C) Tool B, by £4,400
- D) They cost the same

**Correct answer: B**

**Explanation:** Cost Tool A: £15 × 40 developers = £600 per month; × 24 months = £14,400 over two years. Cost Tool B: flat £5,000 × 2 years = £10,000; plus one-off onboarding £50 × 40 = £2,000; total £12,000. Difference: £14,400 − £12,000 = £2,400 in Tool B's favour. The distractor £4,400 forgets the onboarding cost; option A gets the arithmetic right and the direction wrong — always re-read which option claims which winner. Two professional notes the test cannot ask but the role does: the horizon changes the answer's margin (year one alone: A £7,200 versus B £7,000 — nearly level; year two: A £7,200 versus B £5,000 — decisive), so state your horizon when you justify the decision; and per-seat costs scale with headcount growth while flat fees do not, which is the kind of sensitivity a board will probe. Making and justifying high-impact decisions means showing this working, not just the winner.

**Question 7 (moderate) — Reading a Core Web Vitals table**

The programme treats a service as passing the loading metric when its 75th percentile largest contentful paint is 2.5 seconds or under. The dashboard shows:

| Service | p50 | p75 | p95 |
|---|---|---|---|
| Licensing | 1.8 | 2.3 | 4.1 |
| Grants | 1.9 | 2.6 | 3.8 |
| Benefits | 1.6 | 2.4 | 5.2 |
| Passports | 2.1 | 2.9 | 4.4 |

How many services currently fail the loading metric?

- A) 1
- B) 2
- C) 3
- D) 4

**Correct answer: B**

**Explanation:** The rule reads the p75 column only, with a pass at 2.5 or under. Licensing 2.3 — pass. Grants 2.6 — fail. Benefits 2.4 — pass. Passports 2.9 — fail. Two failures. The traps are engineered: Benefits' alarming p95 of 5.2 tempts an extra failure, but the rule as stated does not consult p95; and Licensing's healthy p50 tempts complacency it happens to deserve. Rules name their column, and the discipline is reading only that column for the pass/fail question — then, as a professional, reading the rest for insight: Benefits' tail (p95 more than three times p50) suggests a subset of users on a much worse path, worth an investigation the pass/fail rule will never trigger. A lead reads the rule exactly and the table fully; the test rewards the first, your teams benefit from the second.

**Question 8 (moderate) — Sequential percentage changes**

Your frontend community had 500 active members at the start of the year. Membership grew 10% in the first half, then fell 10% in the second half. How many members are active at year end?

- A) 500
- B) 495
- C) 505
- D) 490

**Correct answer: B**

**Explanation:** Step 1: after 10% growth: 500 × 1.10 = 550. Step 2: after a 10% fall: 550 × 0.90 = 495. The tempting answer is 500 — up ten percent, down ten percent, surely home again — but the second change applies to the larger base, so the fall removes 55 members while the rise added only 50. In factor terms: 1.10 × 0.90 = 0.99, a net 1% decline, and the factor method makes the asymmetry visible instantly. The same asymmetry governs performance metrics (a 10% regression is not cancelled by a 10% improvement), budgets and traffic. It also underlies a rule worth teaching your community: sequential percentage changes never cancel unless you invert the factor (undoing +10% requires −9.09%). Small algebra, large immunity to dashboard misreadings.

**Question 9 (challenging) — Reverse percentage on a performance win**

A team reports: "After our optimisation work, the page's JavaScript payload is 208 KB — a 35% reduction." What was the payload before the work?

- A) 280.8 KB
- B) 297 KB
- C) 320 KB
- D) 343 KB

**Correct answer: C**

**Explanation:** After a 35% reduction, 208 KB represents 65% of the original. Step 1: original × 0.65 = 208. Step 2: original = 208 ÷ 0.65 = 320 KB. Step 3: verify forwards: 320 × 0.35 = 112; 320 − 112 = 208. Confirmed. The distractor 280.8 comes from adding 35% to the reduced figure (208 × 1.35), the classic reverse-percentage error — wrong because the 35% was taken from the larger original. As the lead who assures quality across teams, you will meet this exact sentence shape in show-and-tells and want the reconstruction reflex: the before-figure is the claim's anchor, and being able to recover it in your head ("208 over 0.65... 320") lets you ask the useful next question — 320 KB of what, and what remains in the 208? — while the slide is still up.

**Question 10 (challenging) — Capacity into a credible timeline**

Three teams will migrate 180 components to the new design system. Each team can migrate 12 components per two-week sprint at full capacity, but programme policy reserves 25% of every team's capacity for live-service support. How many sprints will the migration take, and how many weeks is that?

- A) 5 sprints — 10 weeks
- B) 6 sprints — 12 weeks
- C) 7 sprints — 14 weeks
- D) 8 sprints — 16 weeks

**Correct answer: C**

**Explanation:** Step 1: combined full capacity: 3 teams × 12 = 36 components per sprint. Step 2: apply the 25% reservation: 36 × 0.75 = 27 components per sprint. Step 3: sprints needed: 180 ÷ 27 = 6.67. Step 4: capacity comes in whole sprints, so round up: 7 sprints. Step 5: at two weeks per sprint: 14 weeks. The distractor 5 sprints (180 ÷ 36) forgets the reservation — the plan that looks best on a slide and fails in week three; 6 sprints commits the subtler sin of rounding 6.67 down, promising a fortnight that does not exist. Rounding partial sprints up is not pessimism, it is arithmetic honesty — and it is precisely the kind of number a lead is expected to defend: when a programme manager asks "can we say 12 weeks?", the answer is "only by un-reserving support capacity, and here is that trade-off in writing". Timelines built this way survive contact with delivery; timelines built the other way become your credibility problem.

**Question 11 (challenging) — Valuing an automation initiative**

Manual accessibility audits across three teams currently find an average of 4.8 defects per audit. In teams with automated checks embedded, audits find 1.2 defects per audit, because most issues are caught before audit. The three teams undergo 10 audits per year in total. If embedding automated checks brings the three teams to the embedded-teams' rate, how many fewer audit-stage defects per year should the programme expect?

- A) 12
- B) 36
- C) 48
- D) 3.6

**Correct answer: B**

**Explanation:** Step 1: current audit-stage defects: 4.8 × 10 = 48 per year. Step 2: projected: 1.2 × 10 = 12 per year. Step 3: reduction: 48 − 12 = 36 fewer defects reaching audit. The distractors are the intermediate values (48 and 12) and a decimal slip (3.6). Two disciplines sit on top of the arithmetic. First, the causal caveat: the embedded teams' 1.2 is an observed comparison, not a guaranteed transfer — differences between teams may explain part of the gap, so "should expect up to roughly 36" is the honest phrasing for a business case. Second, defects found at audit is a proxy: the real benefit is issues caught earlier and cheaper, plus the ones users never meet. When you champion this initiative — exactly the kind of investment a lead drives — the 36 gives the headline, and the caveats give it credibility under questioning. A board believes numbers more when their presenter volunteers the limits first.

**Question 12 (challenging) — A mix effect in redesign results**

A service redesign launches. Completion data, old versus new:

| Segment | Old completions / sessions | New completions / sessions |
|---|---|---|
| Desktop | 8,000 / 10,000 | 4,100 / 5,000 |
| Mobile | 2,000 / 5,000 | 4,200 / 10,000 |

A stakeholder says: "Overall completion fell from 66.7% to 55.3% — the redesign has failed." What does the data actually show?

- A) The stakeholder is right: completion fell overall, so the redesign performs worse.
- B) The redesign improved completion within both segments (desktop 80% to 82%, mobile 40% to 42%); the overall fall is explained by the traffic mix shifting toward mobile, which completes at a lower rate on any design.
- C) The data is contradictory and unusable.
- D) Desktop improved but mobile declined, and the two roughly cancelled.

**Correct answer: B**

**Explanation:** Compute each segment. Desktop old: 8,000 ÷ 10,000 = 80%; desktop new: 4,100 ÷ 5,000 = 82% — improved. Mobile old: 2,000 ÷ 5,000 = 40%; mobile new: 4,200 ÷ 10,000 = 42% — improved. Overall old: (8,000 + 2,000) ÷ 15,000 = 66.7%; overall new: (4,100 + 4,200) ÷ 15,000 = 8,300 ÷ 15,000 = 55.3% — down, exactly as the stakeholder says. Both things are true because the mix inverted: desktop sessions halved while mobile doubled, and mobile completes at roughly half desktop's rate under either design, so the aggregate is now dominated by the harder segment. This is a mix effect (Simpson's paradox), and option B is the only statement matching every number; D is factually wrong about mobile, and C mistakes "surprising" for "contradictory". The professional sequel matters: the redesign is working within segments, and the real questions are why traffic shifted (seasonality? a marketing change? mobile users previously locked out and now able to try?) and how to raise mobile completion. A lead who can perform this decomposition at the whiteboard, while the stakeholder watches, converts an incipient "roll it back" panic into an evidence-led plan — which is **Communicating information** and **Strategic thinking** doing arithmetic together.

### Preparation tips

- **Drill the core four, then the aggregation layer.** Percentage change, reverse percentage, rates and weighted averages first; then practise re-deriving aggregate rates from counts and totals, because portfolio questions live there.
- **Convert changes to factors by reflex.** +10% is ×1.1, −35% is ×0.65; chains multiply. The factor habit is the single highest-value technique for both speed and accuracy.
- **Verify backwards answers forwards.** Every reverse-percentage result can be checked in one multiplication. Ten seconds, near-total error protection.
- **Read the rule's column before the table.** Threshold questions name their metric; answer from that column alone, however alarming the neighbours look.
- **Practise on your own dashboards.** Take this quarter's real cross-team data and compute one weighted rate, one mix decomposition and one cost comparison. The test will feel like a quiet Tuesday.
- **Keep intermediate results labelled.** "Defects: 27; points: 200" survives time pressure; a scratchpad of naked numbers does not.

### Common pitfalls to avoid

- **Averaging rates instead of re-deriving them.** The unweighted mean of team rates is almost always among the options and almost never the answer. Counts over totals, every time.
- **Trusting aggregates across a changing mix.** When segments improve but the total worsens (or vice versa), check the mix before believing either story. The paradox is on the test because it is in your dashboards.
- **Forgetting one-off costs and reserved capacity.** Cost comparisons hide onboarding fees; timeline questions hide support reservations. Read for the clause that adjusts the headline rate.
- **Rounding partial sprints down.** Capacity arrives in whole units; 6.67 sprints is 7. Optimistic rounding is the most expensive arithmetic error a lead can publish.
- **Mislabelling points and percentages.** Nine points from 72% is 12.5% relative. State both, labelled, in tests and in board papers alike.
- **Answering the right calculation's wrong question.** Intermediate values (the old total, the new rate, one team's count) populate the distractors. Re-read what is asked after you finish computing.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what a piece of written material establishes. At lead level the material is accessibility regulation, design system and technical governance, service standards, supplier documentation and research reports — writing that allocates obligations and authority, and that you are frequently the person others rely on to read correctly.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, Cannot Say means neither — regardless of what you know professionally.

Your expertise is the principal hazard. You will know the right answer about accessibility, browsers and web standards while the passage in front of you is silent, and a confident wrong answer in this format is the same shape as a confident wrong answer in a governance meeting.

Three specifics matter at your level.

The first is that "must", "should" and "may" are terms of art in service standards and specifications, and your role includes advising on how standards apply. Reading "should" as mandatory means blocking work that was permitted; reading "must" as advisory means waiving something that was not.

The second is that governance documents allocate authority precisely. Approves, endorses, is consulted, may direct and is informed describe genuinely different arrangements, and your skills description names building consensus between independent stakeholders — which requires knowing whose agreement is actually needed.

The third is that exceptions define boundaries. An exception for one thing establishes that the rule applies to everything else, and says nothing about the neighbouring case.

### How this assessment maps to your role

- **Reading accessibility regulation precisely** maps to **Accessibility**, where you champion it to internal and external stakeholders.
- **Reading standards** maps to **Modern development standards**, where you advise on how standards apply.
- **Reading governance and authority** maps to **Leadership and guidance (frontend developer)**.
- **Reading supplier and interface documentation** maps to **Systems integration (frontend developer)**.
- **Reading strategy** maps to **Strategic thinking**.
- **Reading research** maps to **User focus (frontend developer)**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Services must work without JavaScript for all essential functions, unless the departmental technical design authority has agreed an exemption. Where an exemption is agreed, the service must still work with assistive technologies and must degrade gracefully when JavaScript fails to load. Services should be tested on the browsers used by at least 95% of the service's users, and must be tested with at least one screen reader on at least one desktop and one mobile platform. Testing on a physical device is preferred to emulation. Where a service is used predominantly on mobile, mobile testing should be prioritised accordingly."

**Question 1 (easy)**

Statement: A service with an agreed exemption need not work when JavaScript fails to load.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this. Even with an exemption, the service "must degrade gracefully when JavaScript fails to load". The exemption releases the service from working *without* JavaScript for essential functions; it does not release it from behaving acceptably when the script fails. The second sentence exists precisely to close that inference, and the distinction between "works without JavaScript" and "degrades gracefully when JavaScript fails" is one worth being able to articulate, because teams routinely treat an exemption as covering both.

**Question 2 (moderate)**

Statement: A service must be tested on the browsers used by at least 95% of its users.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage uses "should" for the 95% browser coverage and "must" for screen reader testing in the very next clause. The contrast within one sentence is deliberate, and the statement's "must" overstates the obligation. This matters practically: browser coverage is negotiable under delivery pressure and screen reader testing is not, and a lead who reads them as equivalent will trade away the wrong one.

**Question 3 (moderate)**

Statement: Emulated device testing does not satisfy the mobile screen reader requirement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says physical device testing "is preferred to emulation". A preference ranks two acceptable options; it does not establish that the lesser one fails to satisfy the requirement. Professionally you would be right that emulated screen reader testing is close to worthless — and the passage has not said so, which is the whole exercise.

**Question 4 (harder)**

Statement: A service used predominantly on desktop must still be tested with a mobile screen reader.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The screen reader requirement is unconditional: at least one screen reader on "at least one desktop and one mobile platform". The final sentence about prioritising mobile testing where usage is predominantly mobile adjusts emphasis between two required activities; it does not create an exemption from either. Reading a prioritisation clause as a conditional release is the trap, and it is the same shape as reading a preference as a prohibition in Question 3 — in both cases the passage is ranking rather than excluding.

*Passage B — for Questions 5 to 8*

"The technical design authority approves architectural decisions affecting more than one service. Decisions confined to a single service are made by that service's lead developer, who must notify the authority where the decision departs from a published pattern. The authority may direct that a single-service decision be brought to it for approval where in its view the decision sets a precedent. The head of engineering endorses the authority's decisions and may return a decision for reconsideration once, with reasons; a decision returned and reaffirmed by the authority stands."

**Question 5 (easy)**

Statement: A decision confined to a single service is made by that service's lead developer.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly. Two qualifications follow — a notification duty for pattern departures, and the authority's power to call a decision in — and neither changes who makes the decision by default.

**Question 6 (moderate)**

Statement: The head of engineering can overturn a decision of the technical design authority.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this. The head of engineering "endorses" decisions and "may return a decision for reconsideration once, with reasons", and "a decision returned and reaffirmed by the authority stands". That is a single power of return rather than a veto, and the final clause closes the inference explicitly. Reading endorsement as approval-with-power-to-refuse is the natural error.

**Question 7 (moderate)**

Statement: A lead developer making a single-service decision that follows a published pattern has no obligation to notify the authority.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The notification duty is qualified — notify "where the decision departs from a published pattern". Following the pattern means the condition is not met, so the obligation does not arise. The passage establishes this through the structure of the qualification. Note it says nothing about whether the authority might still call the decision in under its precedent power, which is an independent mechanism not dependent on notification.

**Question 8 (harder)**

Statement: The authority can require a single-service decision to come to it only where the decision departs from a published pattern.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts the word "only". The call-in power is conditioned on the authority's view that the decision "sets a precedent" — a different and independent test from departing from a published pattern. A decision could follow every pattern and still set a precedent, or depart from one without setting any. The statement imports the condition attached to the notification duty and applies it to the call-in power. Conflating conditions attached to two different mechanisms is a common and consequential misreading of governance text, and at your level it is the kind of error that produces confident wrong advice.

*Passage C — for Questions 9 to 12*

"A study of 62 participants compared two error-handling patterns on a benefits application form. Pattern A displayed errors inline beside each field; pattern B displayed an error summary at the top of the page with links to each field, and also displayed errors inline. Screen reader users completed the form more often with pattern B, at 88% against 61%. Sighted users showed no significant difference between patterns. The study did not measure completion time. Participants were recruited to include a range of assistive technology users. The research team recommends pattern B."

**Question 9 (moderate)**

Statement: Screen reader users completed the form more often with pattern B.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly with figures: 88% against 61%. True. Note the passage reports this for screen reader users specifically and separately reports no significant difference for sighted users, which is a well-structured finding — the next questions turn on respecting that separation.

**Question 10 (moderate)**

Statement: Pattern B is better for all users.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage establishes a large benefit for screen reader users and no significant difference for sighted users. "No significant difference" is not evidence of benefit, so the passage does not support "better for all users" — though it does support pattern B overall, since one group benefits substantially and the other is unaffected. That is a stronger and more precise thing to say than the statement claims, and being precise about it is what makes the recommendation credible when someone challenges it.

**Question 11 (moderate)**

Statement: Pattern B takes longer to complete than pattern A.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage states explicitly that "the study did not measure completion time". No evidence either way. A study that names what it did not measure is telling you where the evidence stops, and the useful professional habit is to reproduce that boundary when you cite the finding rather than letting it quietly disappear.

**Question 12 (harder)**

Statement: The 27-point difference for screen reader users was statistically significant.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage reports significance testing for the sighted-user comparison ("no significant difference") and reports the screen reader figures as raw percentages without any such statement. So significance is established for one comparison and not the other. The difference is large and the sub-group is smaller than 62, which cuts both ways — a large effect in a small group may or may not reach significance. Noticing that a passage applied a test to one comparison and not another is the kind of asymmetry worth catching, because it is exactly where an over-strong claim gets built.

### Preparation tips

- **Treat must, should and may as distinct obligations.**
- **Read a preference as ranking, not excluding.**
- **Read a prioritisation clause as emphasis, not exemption.**
- **Distinguish endorsement from veto and notification from approval.**
- **Check whether a condition attached to one mechanism has been imported into another.**
- **Read "no significant difference" as absence of evidence, not evidence of equivalence.**
- **Note which comparisons a study tested and which it merely reported.**
- **Reproduce a study's stated boundaries when citing it.**

### Common pitfalls to avoid

- **Treating an exemption from one obligation as an exemption from all.**
- **Reading "should" as mandatory in a passage that uses both.**
- **Reading "is preferred to" as prohibiting the alternative.**
- **Reading endorsement as a power of refusal.**
- **Applying the notification condition to a separate call-in power.**
- **Turning "no difference for group X" into "better for everyone".**
- **Assuming a reported percentage difference was significance tested.**
- **Answering from web standards knowledge rather than from the passage.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. At lead level the scenarios involve setting direction across teams you do not manage, assuring quality without becoming a bottleneck, mentoring, resolving disputes among peers, and advocating for users who are not in the room.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners at comparable levels, so the target is professional consensus.

Three patterns run through the strong answers at this level.

The first is that your authority is largely borrowed. Teams follow your direction because they respect the reasoning, and every time you spend that credibility on a preference you have less of it for something that matters.

The second is that you are frequently the most senior person present who understands what a design decision does to users with access needs. Silence from you is read as professional endorsement, and the people affected are never in the room to notice.

The third is that assurance across teams fails in one of two ways: too light and it changes nothing, too heavy and you become the queue everything waits in. The strong answers consistently look for the version that catches what matters without routing every decision through you.

### How this assessment maps to your role

- **Setting direction across teams** maps to setting direction and assuring quality of development across teams.
- **Resolving disputes** maps to **Leadership and guidance (frontend developer)**, where you build consensus among independent stakeholders.
- **Mentoring and community** maps to **Community collaboration** and providing coaching and mentoring.
- **Accessibility advocacy** maps to **Accessibility**.
- **Technology judgement** maps to identifying appropriate technology and approaches.
- **Strategy** maps to **Strategic thinking**.

### Practice questions

**Question 1 (easy) — Accessibility under a deadline**

Two days before release, you find a component across three services is not keyboard operable. Fixing it properly means restructuring it. What is the most effective response?

- A) Release and fix in the next sprint.
- B) State plainly what it means — keyboard and screen reader users cannot use this part of three services — and put the options to the service owners, including releasing without the component, releasing a simpler accessible version, or delaying.
- C) Refuse to release.
- D) Add keyboard handlers as a quick patch.

**Correct answer: B. Least effective: A**

**Explanation:** The decision belongs to the service owners and your job is to ensure it is made knowingly, in plain terms rather than as a technical finding. Option B also brings the middle option, which is frequently available and frequently unconsidered under time pressure. Option A is least effective because it releases a known barrier across three services, and next-sprint accessibility fixes have a poor record. Option C removes the owners from their own decision. Option D risks a patch that appears to work and fails for actual assistive technology users, which is worse than a visible gap because nobody looks again.

**Question 2 (easy) — A team's technology choice**

A team you set direction for wants to adopt a framework you would not have chosen. Their reasoning is sound. What is the most effective response?

- A) Direct them to the organisation's usual choice.
- B) Ask what problem it solves that the usual choice does not, and weigh the answer against the costs that fall on others — recruitment, shared components, support at 3am — because a defensible decision made by the team that will live with it is a good outcome even when it differs from yours.
- C) Let them proceed; it is their service.
- D) Ask them to trial it first.

**Correct answer: B. Least effective: A**

**Explanation:** "Defensible but different" is the normal and desired outcome of delegated technical judgement, and option B tests the one thing that is genuinely your business — the costs that land outside their team. Option A is least effective: overruling sound reasoning with the default teaches the team that your direction means guessing what you would have picked, and you will get less honest reasoning next time. Option C abandons the assurance role your level names. Option D is a reasonable step and does not by itself surface the cross-team costs.

**Question 3 (moderate) — Becoming the bottleneck**

Teams have started routing every frontend decision through you for approval, and you are the delay in several. What is the most effective response?

- A) Work through the queue faster.
- B) Define what genuinely needs your involvement and what does not — usually cross-cutting patterns, accessibility-critical components and shared code, and not internal implementation choices — and publish that, so teams can proceed on their own for most decisions.
- C) Delegate approvals to senior developers in each team.
- D) Stop approving and let teams decide.

**Correct answer: B. Least effective: A**

**Explanation:** Being consulted on everything is a structural problem and no amount of personal throughput fixes it. Option B addresses the cause by making the boundary explicit, which also tells teams what they are trusted with — the thing they usually want to know. Option A is least effective: working faster confirms the arrangement, and the queue reforms at your new speed. Option C is a good complement and, alone, distributes the bottleneck without defining what needs approving. Option D removes assurance rather than scoping it.

**Question 4 (moderate) — A dispute between two teams**

Two teams have built different components for the same purpose and each defends theirs. It has become slightly personal. What is the most effective response?

- A) Pick the better component and require both to use it.
- B) Get them together and establish what each component was built to do, because two teams defending positions usually have two different requirements that were never compared — and address the personal element separately, since it does not become acceptable because the technical disagreement was real.
- C) Let each keep its own.
- D) Escalate to their delivery managers.

**Correct answer: B. Least effective: C**

**Explanation:** There are two problems and option B is the only response that treats both. Components that look identical from outside frequently differ in the requirements that drove them, and comparing requirements usually either dissolves the dispute or makes it tractable. The conduct is a separate matter needing its own conversation. Option C is least effective: it accepts permanent duplication and leaves the relationship damaged. Option A resolves by fiat and creates a losing team. Option D escalates something your level exists to resolve.

**Question 5 (moderate) — Adapting feedback**

A developer you mentor has not acted on feedback you have given twice. What is the most effective response?

- A) Give the feedback again more firmly.
- B) Ask what has made it hard to act on — they may disagree and not have said so, may not have understood what you meant concretely, or may be constrained by something in their team — because feedback given twice without effect is usually a problem with the feedback rather than with their willingness.
- C) Raise it with their line manager.
- D) Stop giving that feedback.

**Correct answer: B. Least effective: C**

**Explanation:** Your skills description names adapting feedback to ensure it is effective and lasting, and this is what that means: the second failure is information about how you are giving it. Option B names the three realistic causes, each with a different remedy — disagreement needs discussion, vagueness needs an example, and a team constraint needs removing. Option C is least effective: escalating a mentoring conversation to a line manager converts a developmental relationship into a performance issue, and ends the mentoring. Option A repeats what has already not worked. Option D gives up on something you thought mattered.

**Question 6 (moderate) — A design that cannot be built accessibly**

A designer has produced an interaction that would be difficult to make accessible. What is the most effective response?

- A) Build it as specified and note the accessibility risk.
- B) Go to them early with the specific problem — which users would struggle and why — and work on an alternative together, because the interaction is usually achievable in a different form and a change to a design costs a fraction of a change to built code.
- C) Build a different interaction that is accessible.
- D) Ask them to redesign it.

**Correct answer: B. Least effective: A**

**Explanation:** Option B is early, specific and collaborative, which is the combination that gets designs changed. The cost argument is the practical one: the same change is cheap now and expensive after build. Option A is least effective because it knowingly builds a barrier and records the fact, which changes nothing for users and reads as covering yourself. Option C makes a design decision unilaterally, which is not yours and damages a relationship you need. Option D hands back a problem without the information that would let them solve it.

**Question 7 (harder) — Assuring a decision you disagree with**

A team's approach meets every standard you set but is not what you would have done. What is the most effective response?

- A) Pass it and record your concerns.
- B) Pass it, because assurance is against the standard and using it to enforce preference destroys the distinction between what is required and what you would prefer — and separately consider whether the gap means the standard is missing something worth adding.
- C) Pass it conditionally.
- D) Ask them to change it.

**Correct answer: B. Least effective: D**

**Explanation:** The integrity of assurance depends on predictability. A lead who fails or pressures compliant work on judgement makes the standard meaningless, and teams then optimise for the reviewer rather than the standard. Option B holds that line and does the genuinely useful thing with the disagreement — asking whether the standard should say something it does not. Option D is least effective as it uses assurance authority to impose preference. Option A registers displeasure on a pass, which pressures informally while changing nothing. Option C invents a category that does not exist.

**Question 8 (harder) — Pressure to drop a standard**

A delivery manager asks whether teams could move faster by dropping the progressive enhancement baseline, noting that "almost everyone has JavaScript". What is the most effective response?

- A) Explain that it is a government service standard requirement.
- B) Answer the speed question honestly — for some components the baseline costs real time, for many it costs almost nothing — and set against it the sessions where scripts fail for reasons unrelated to whether users "have JavaScript", with what those users would be unable to do.
- C) Explain that JavaScript fails more often than people think.
- D) Agree, provided critical journeys keep a baseline.

**Correct answer: B. Least effective: A**

**Explanation:** The delivery manager asked a reasonable question and deserves a real answer, including the part that concedes ground — the baseline genuinely does cost time on some components, and pretending otherwise is why these conversations go badly. Option B also reframes the risk correctly: script failure is about networks, proxies and errors rather than user choice. Option A is least effective because answering a cost question with an authority claim invites someone to go and seek an exemption. Option C is true and unquantified. Option D concedes the structure before the discussion has happened.

**Question 9 (harder) — Evidence against your own standard**

Data suggests a testing standard you introduced across four teams costs significant time and has not measurably reduced defects. What is the most effective response?

- A) Improve the measurement; some benefits are hard to capture.
- B) Publish the finding, including that it is your standard, and narrow it to where the benefit is demonstrable or withdraw it — because four teams paying daily for an unmeasurable benefit is a real cost, and withdrawing your own standard on evidence makes every remaining one more credible.
- C) Retain it; testing standards prevent problems that never appear in defect data.
- D) Reduce its scope quietly.

**Correct answer: B. Least effective: C**

**Explanation:** The cost is certain, distributed and daily; the benefit is unmeasured. Option B allows the right resolution — narrowing rather than abandoning — and gets the credibility benefit that only comes from doing it openly. Option C is least effective because it is unfalsifiable, which makes it the argument that keeps every unproductive standard in place indefinitely. Option D reaches a defensible outcome by a route that looks like concealment when noticed. Option A is legitimate in principle and indistinguishable from motivated reasoning when the person improving the measurement owns the standard.

**Question 10 (harder) — Contradicting a senior stakeholder**

In a large meeting, a director makes a technical claim that is wrong and that will lead to a poor decision. What is the most effective response?

- A) Correct it immediately; the decision matters.
- B) Add the correcting information without framing it as a correction — supplying the relevant fact and its implication — and follow up directly afterwards if the decision is still heading the wrong way, because the goal is the decision rather than the record of who was right.
- C) Say nothing and raise it afterwards.
- D) Ask a question that leads them to the correct position.

**Correct answer: B. Least effective: C**

**Explanation:** Option B gets the information into the room, which is necessary, without a public contradiction that makes retreat costly and hardens the position. The phrasing difference does most of the work: "worth noting that X, which would mean Y" lands where "that's not right" does not. Option C is least effective because large meetings are frequently where decisions are actually made, and afterwards means reopening something settled. Option D is a legitimate technique that can read as manipulative and often fails to get the fact stated. Option A prioritises correctness over outcome.

**Question 11 (harder) — A community that has stopped sharing**

The frontend community of practice you convene has become quiet, with few people contributing. What is the most effective response?

- A) Ask people to contribute more.
- B) Find out what changed — whether the sessions stopped being useful, whether the format rewards a few confident voices, or whether people are too busy to prepare something — because a community that was active and went quiet has a cause, and each of those has a different fix.
- C) Reduce the frequency of sessions.
- D) Present more yourself to restart momentum.

**Correct answer: B. Least effective: A**

**Explanation:** Your skills description names using the community to identify problems in team dynamics and stimulate the right responses, and that starts with diagnosing your own forum. Option B names the three usual causes: sessions that stopped being relevant, a format where preparing something feels high-stakes, and simple capacity. Option A is least effective — asking busy people to contribute more without changing anything produces guilt rather than contributions. Option D is a reasonable short-term measure that, sustained, converts a community into an audience. Option C may follow from the diagnosis and pre-empts it.

**Question 12 (harder) — Your own architectural decision has aged**

A frontend architecture you set two years ago is now the main source of friction for three teams. A newer developer proposes replacing it. What is the most effective response?

- A) Defend it; it was right at the time.
- B) Engage with the proposal on its merits, say plainly that the original assumptions have not held, quantify what the friction is costing, and get someone other than you to assess the options — because your view of your own architecture carries a discount you cannot argue away.
- C) Agree to the replacement.
- D) Ask them to write a full proposal.

**Correct answer: B. Least effective: A**

**Explanation:** The decision may well have been right when made and be wrong now, and both can be true without either being a defence. Option B does the analysis, is honest about it, and handles the credibility problem by removing yourself from the recommendation. Option A is least effective: it is the natural reaction, it usually wins because you have the authority, and it teaches three teams that the friction is permanent and that raising things is pointless. Option C over-corrects without the cost analysis. Option D is a fair process step that reads as delay if it substitutes for a view.

### Preparation tips

- **Put accessibility decisions to the owner in plain terms, with options.**
- **Define what needs your approval and publish it.**
- **Move disputing teams from positions to requirements.**
- **Treat feedback that did not land twice as a problem with the feedback.**
- **Assure against the standard; change the standard if it is wrong.**
- **Answer cost questions with costs, not with authority.**
- **Withdraw your own standards openly when the evidence says so.**
- **Get an independent assessment when the subject is your own past decision.**

### Common pitfalls to avoid

- **Patching an accessibility failure so it appears fixed.**
- **Overruling sound reasoning with the default choice.**
- **Working through an approval queue faster instead of scoping it.**
- **Accepting duplicate components to end a dispute.**
- **Escalating a mentoring conversation to a line manager.**
- **Recording an accessibility risk instead of preventing it.**
- **Defending a standard on unmeasurable benefits.**
- **Contradicting a senior stakeholder publicly.**

## Conclusion

You have worked through four assessments pitched at lead frontend developer, and the threads are worth drawing together.

The cognitive section kept returning to structure and failure: whether a problem is an instance or a pattern, what happens when the script does not run, and why effort spent reconstructing native behaviour is a signal that an earlier decision was wrong.

The numeric section was about not being misled by your own metrics — weighting by traffic, converting percentages into people, scaling sampled counts, and the asymmetry that makes bytes of JavaScript far more expensive than bytes of image data on the devices your users actually hold.

The verbal section was an exercise in reading precisely the documents that define what is required of you and what you may decide. "Should" is not "must". A preference is not a prohibition. Endorsement is not a veto. And "no significant difference for sighted users" supports a careful claim rather than a sweeping one.

The situational judgement section circled the particular position of a lead: enough standing to set direction, not enough authority to compel, and frequently the only person present who can see what a decision does to users with access needs. The strong answers scoped assurance rather than accelerating it, moved disputes from positions to requirements, treated unheeded feedback as a problem with the feedback, and — twice — subjected the lead's own standard and own architecture to the same scrutiny as everyone else's.

If one thread runs through all four, it is that this role runs on being believed. Teams accept direction from someone whose reasoning they can check. Delivery managers accept a standard from someone who concedes its cost honestly. That credibility takes years to build and one preference enforced as a requirement to start spending.

Good luck. You are in a role where careful reasoning compounds across teams and services, and the time you have given this is well spent.
