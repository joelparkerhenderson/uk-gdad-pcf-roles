# Senior Quality Assurance Test Analyst - Psychometric Assessment Resources

## Introduction

Welcome. This guide has been created for you as a senior quality assurance test analyst working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, positioning yourself for a lead role, benchmarking your capability against the framework, or refining the judgement you bring to your teams, this document offers structured practice grounded in the realities of your work.

Psychometric assessments are standardised exercises measuring the cognitive capabilities and professional judgement that predict success in a role. At your level, the assessments worth taking seriously are job-specific, and this guide is built accordingly: its questions use the artefacts you genuinely handle — cross-team defect trend data, test approach documents, organisational standards, environment strategies, stakeholder communications at senior level — and the decisions you genuinely make: whether an approach should change given effort and risk, how to read a defect pattern spanning several teams, how to manage expectations during a difficult defect resolution, and how to coach others without doing their thinking for them.

Why do these assessments matter at your level in particular? Because seniority in quality assurance is largely the migration of your attention from artefacts to systems. You still analyse — but the objects of analysis are now portfolios of risk, patterns across teams, and the business impact of testing outcomes. You coordinate quality assurance activities in a defined area, which means your reasoning errors no longer cost one test's accuracy; they propagate through the teams you guide and the stakeholders whose expectations you manage. Cognitive assessment at this level probes exactly that systemic reasoning: multi-constraint scheduling, pattern interpretation across noisy data, and deduction through layered governance rules. Numeric reasoning probes the quantitative judgement behind your recommendations — trend analysis, weighted aggregation, detection rates, and the discipline of denominators — because at senior level your numbers move decisions. Verbal reasoning probes precision with standards, policies and senior correspondence, where a misread qualifier can commit teams to obligations they do not hold. And situational judgement probes the terrain where senior work is genuinely hard: influencing without authority, guiding others through their mistakes rather than around them, escalating across team boundaries, and holding professional lines with diverse senior stakeholders.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters at your level, a mapping of assessment dimensions to the named skills in your capability framework, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls.

To get the most from it: attempt every question in earnest and commit to an answer before reading the explanation — commitment is where the diagnostic value lives. Read the explanations even for questions you answer correctly; they frequently articulate the principle beneath the technique, which is precisely what you need when coaching others in test analysis. And treat the situational judgement section as a mirror rather than a quiz: the scenarios are drawn from the genuinely contested moments of senior practice, and your reactions to them are information about your own defaults.

You have spent years building the judgement this guide exercises. The aim now is to make that judgement explicit, examined, and transferable — to your assessments, and to the people you guide. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands using realistic materials rather than abstract puzzles. At senior level, the emphasis shifts: less pure speed, more multi-constraint reasoning, pattern interpretation under noise, and deduction through layered rules — the thinking that coordinating quality assurance across a defined area actually requires.

The typical format remains an online, timed test of 15 to 30 minutes covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group — for senior roles, often a norm group of comparable seniority — and adaptive platforms will push difficulty upward as you perform, so expect the later questions to feel genuinely hard. Employers typically receive speed and accuracy separately; at senior level, accuracy under complexity is usually the more scrutinised figure, because your role's costliest errors are considered judgements made confidently, not hasty slips.

Why does this matter for your role? Consider what your duties actually demand cognitively. Using the most appropriate tools and techniques to analyse artefacts — products, services, processes and change — to identify risks early is structured decomposition plus pattern recognition, performed across more surface area than any one team presents. Determining whether an approach needs to change based on effort and risk is a portfolio judgement: holding cost curves, risk distributions and delivery constraints simultaneously and noticing when their balance has shifted. Managing and escalating dependencies, defects and risks across teams requires you to reason accurately about chains of cause, consequence and ownership that span organisational boundaries — where the most expensive reasoning failure is the dependency nobody traced. And guiding others in quality assurance tools and techniques demands something subtler: the ability to articulate why an inference is valid or flawed, because coaching transmits reasoning, not just answers. A well-designed cognitive assessment rehearses all of this in miniature, and — usefully for a coach — practising it rebuilds your explicit awareness of techniques you now apply tacitly.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to **Managing, reporting and resolving defects** ("use defect patterns and trends to make recommendations on testing and quality approaches") and **Test analysis**: reading cross-team defect distributions, distinguishing signal from noise in trend data, and spotting the systemic weakness behind clustered failures are senior pattern work.
- **Logical deduction** maps to **Test analysis** ("use multiple techniques to analyse complex information to identify risks") and to your duty to contribute to, and enable others to follow, quality assurance and testing standards: applying layered rules correctly — and explaining their application — is deduction made professional.
- **Error checking** maps to **Designing and executing tests** ("contribute to developing and implementing standards") and **Test engineering**: reviewing others' test designs, approach documents and automation architectures for internal inconsistency is now a larger share of your work than producing artefacts yourself.
- **Prioritisation** maps to **Test analysis** ("determine if an approach needs to change based on effort and risk") and **Test and quality planning**: allocating attention and effort across teams, and knowing when a plan's assumptions have expired, is prioritisation at portfolio scale.
- **Applied problem solving** maps to **Designing and executing tests** ("improve test types and techniques through a structured process") and your coaching duty: diagnosing why a team's testing is underperforming — and designing the intervention — is problem solving whose object is the testing system itself.

### Practice questions

**Question 1 (easy) — Pattern in cross-team defect distribution**

Four teams in your area report last quarter's defects by root cause:

| Team | Requirements gaps | Code defects | Environment issues | Test data issues |
|---|---|---|---|---|
| Alpha | 4 | 22 | 6 | 5 |
| Beta | 5 | 19 | 7 | 4 |
| Gamma | 18 | 8 | 5 | 6 |
| Delta | 3 | 21 | 6 | 5 |

Which observation most warrants your attention as the senior analyst for the area?

- A) Alpha has the most code defects.
- B) Gamma's profile inverts the area pattern — requirements gaps dominate where code defects dominate elsewhere — suggesting a problem upstream of testing in how Gamma's requirements are defined or analysed.
- C) Environment issues are roughly equal everywhere, proving environments are fine.
- D) Delta has the fewest requirements gaps, so Delta's analysts are the strongest.

**Correct answer: B**

**Explanation:** Three teams share a profile: code defects dominate (19-22), requirements gaps are minor (3-5). Gamma inverts it: 18 requirements gaps against 8 code defects. An inversion of the area-wide pattern is the highest-value signal in a table like this, because it points to a cause specific to one team's upstream process — perhaps stories reach Gamma's testers unrefined, perhaps Gamma's analysts are not embedded in refinement, perhaps the product owner defines acceptance criteria differently. Note what the inversion is not evidence of: Gamma's testers failing (finding requirements gaps is testing succeeding — the question is why there are so many to find). Option A reads a maximum without context — 22 against a 19-22 cluster is unremarkable. Option C overreads uniformity: equal counts suggest a common environmental baseline, not absence of a problem. Option D commits the inverse error of B, treating a low count as team quality when it more likely reflects upstream process quality. This is precisely your skill of using defect patterns to make recommendations: the recommendation here is an early-engagement intervention in Gamma's refinement process — ensuring test needs and analysis are implemented early — not more testing downstream.

**Question 2 (easy) — Deduction through a governance rule**

Your area's testing standard states: "Teams may self-certify releases where all three conditions hold: (i) no Severity 1 or 2 defects open; (ii) regression coverage of changed components at or above the agreed threshold; (iii) no changes to shared platform components. Releases failing any condition require independent QA review." Team Beta's release has no Severity 1 or 2 defects open, regression coverage above threshold, and includes a change to the shared authentication component. Beta's lead argues: "Two of three conditions passed, and the auth change is tiny." What does the standard require?

- A) Self-certification — two of three conditions suffice.
- B) Independent QA review — the shared-component condition fails, and the standard makes any failed condition decisive regardless of the change's size.
- C) The test manager may waive the review.
- D) The standard is ambiguous on this case.

**Correct answer: B**

**Explanation:** The standard's logic is a conjunction: self-certification requires all three conditions, and "releases failing any condition require independent QA review". Condition (iii) fails — the release changes a shared platform component — so review is required. The standard contains no materiality qualifier ("tiny" appears nowhere) and no waiver route (option C invents one; if a waiver mechanism exists, it is not in this text). Option D mistakes an unwelcome answer for an ambiguous one — the text is entirely determinate. The senior-level substance here is twofold. First, the deduction itself is elementary, but the pressure is not: "two of three" is a persuasive-sounding misreading you will hear in real governance conversations, and your duty to enable others to follow standards means being able to show, kindly and precisely, why conjunctions do not average. Second, the standard's design deserves notice: shared-component changes get independent review precisely because their blast radius crosses team boundaries — the "tiny" auth change is the exact case the rule exists for. When you contribute to developing standards, this is the drafting lesson: rules that must hold under pressure need their conditions explicit and their exceptions absent or explicit — never implied.

**Question 3 (moderate) — Error checking a team's test approach document**

Reviewing a team's draft test approach, you find these statements in different sections: (1) "All regression testing will be automated by the end of Q2." (2) "The regression pack will include the manual visual comparison checks for PDF outputs, which cannot be reliably automated with current tooling." (3) "From Q3, regression will run nightly with no manual effort." (4) "Exploratory testing will be timeboxed at two days per release." Which statements are in conflict?

- A) 1 and 4
- B) 2 with both 1 and 3
- C) 3 and 4
- D) 1 and 3

**Correct answer: B**

**Explanation:** Trace each claim's commitments. Statement 1 commits to full regression automation by end of Q2. Statement 3 depends on that commitment: nightly runs with no manual effort. Statement 2 contradicts both: it places manual visual PDF checks inside the regression pack and states they cannot be reliably automated with current tooling. If 2 is true, then 1 is unachievable as written and 3's "no manual effort" is false. Statements 1 and 3 are mutually consistent (D is wrong — they fail together, not against each other), and 4 concerns exploratory testing, a different activity entirely. The correction is not to delete statement 2 — it records a genuine constraint — but to scope statements 1 and 3 honestly: "all regression except the manual PDF visual checks", with the manual residue explicitly planned. This is the reviewing skill your role now leans on: internal consistency checking across a document's sections, where each section was locally plausible when written and the conflict lives in the joins. Approach documents that overpromise automation coverage fail in exactly this pattern, and the senior reviewer who catches the join — before the plan meets Q3 — saves the team from discovering it as a missed commitment. Leading others in designing and maintaining tests includes leading the honesty of the documents that frame them.

**Question 4 (moderate) — Prioritisation across an area**

You coordinate QA across four teams. Monday brings four demands. The area's release train departs Thursday. Which sequence is most defensible?

1. Team Alpha's analyst asks you to review their risk assessment for Thursday's release — they flag genuine uncertainty about a payments integration.
2. Team Gamma's automation has been red for four days; their analyst has not investigated, saying "it's probably the environment again".
3. The head of delivery wants your input to a quality metrics slide for next Monday's programme board.
4. A recruitment panel needs your interview feedback written up by Wednesday for a candidate offer decision.

- A) 1, 2, 4, 3 — release-critical review first, then the unexamined red suite, then the offer deadline, then the board slide
- B) 3, 1, 2, 4 — the programme board outranks team-level work
- C) 2, 1, 4, 3 — red automation always comes first
- D) 1, 4, 3, 2 — Gamma's suite is probably just the environment

**Correct answer: A**

**Explanation:** Weigh impact, urgency and — at senior level — the risk hidden in unexamined assumptions. Item 1 leads: it is release-critical (Thursday), the uncertainty is flagged in a payments integration (high consequence), and reviewing others' risk assessments is precisely your coordinating function. Item 2 comes second, and the reasoning matters: four days of red with no investigation is not an automation problem, it is a verification gap plus a practice problem — "probably the environment" is exactly the assumption that lets real regressions ride into a Thursday release unseen. Your intervention is a coaching moment (guide the analyst to triage red runs within a day, and to distinguish diagnosis from dismissal) as much as a technical one. Item 4 has a hard Wednesday deadline affecting a person's offer — real but bounded effort, so it precedes item 3, whose Monday deadline leaves the week. Option B mistakes audience seniority for urgency; the board slide is important and comfortably schedulable. Option C elevates a heuristic ("red first") over the actual risk comparison — the release review is both nearer and larger. Option D adopts the very assumption item 2 needs challenged, which is how four days becomes eight. The senior pattern: sequence by risk-weighted urgency, and treat unexamined assumptions in your area as risks in their own right.

**Question 5 (moderate) — Interpreting a noisy trend**

A team you guide shows escaped defects (found in production) per release over eight releases: 3, 5, 2, 4, 3, 11, 3, 4. The spike release (11) coincided with an emergency regulatory change delivered in half the usual cycle time. The team's delivery manager says: "Ignoring the outlier, we're stable — no action needed." What is the most analytically sound response?

- A) Agree fully — outliers should always be excluded from trend analysis.
- B) Disagree with the framing: the spike is not noise to discard but signal about a specific vulnerability — compressed cycles overwhelm the team's quality practices — so the stable baseline and the conditional failure mode are both real findings, and the action is building a pre-agreed fast-cycle quality approach before the next emergency, not ignoring the case.
- C) Disagree — the spike proves the team's quality is generally poor.
- D) The data is insufficient to say anything.

**Correct answer: B**

**Explanation:** Distinguish two questions the delivery manager has merged: "what is the team's typical performance?" and "what does the spike mean?" For the first, excluding the outlier is legitimate: the remaining seven releases (2-5 escapes) describe a stable baseline. But "ignore the outlier" answers only the first question. The spike has a known, recurring cause — emergency changes on compressed timelines will happen again in a regulated service — and 11 escapes under those conditions is a measured observation of how the team's quality system behaves under compression: nearly triple the baseline. That is not noise; it is the most informative data point in the series. The senior response treats it accordingly: keep the baseline conclusion, and convert the spike into preparation — a pre-agreed emergency-cycle approach (risk-ranked minimal regression, mandatory exploratory hours on changed areas, explicit residual-risk acceptance) so the next compressed cycle is met with a plan rather than improvisation. Option A elevates a data-cleaning habit into a thinking error. Option C overgeneralises from one conditioned case against seven contrary observations. Option D understates eight points with an explained anomaly — small data with known causes supports careful conclusions. This is "determine if an approach needs to change based on effort and risk" in action: the approach need not change for normal cycles, and must exist for abnormal ones.

**Question 6 (moderate) — Deduction about dependency chains across teams**

Release R depends on: Team A's API change, which depends on Team B's schema migration; and Team C's frontend change, which depends on Team A's API change being deployed to TEST. Team B's migration completes and deploys to TEST on day 3. Team A needs 2 days of development after B's migration is on TEST, then 1 day of API testing before their change deploys to TEST. Team C needs 2 days of development and testing after A's change is on TEST. What is the earliest day Release R can be ready, and which handoff is on the critical path's final link?

- A) Day 8; the final link is C's work following A's TEST deployment
- B) Day 6; the final link is A's testing
- C) Day 10; the final link is B's migration
- D) Day 8; the final link is B's migration

**Correct answer: A**

**Explanation:** Chain the dependencies forward. B's migration is on TEST at day 3. A's development: days 4-5. A's API testing: day 6, after which A's change deploys to TEST (end of day 6). C's development and testing: days 7-8. Release R is ready at day 8, and the final link in the chain — the handoff whose slippage directly moves the release — is C's two days following A's TEST deployment. Option B stops the chain at A, forgetting C consumes A's output. Options C and D misplace the critical link: B's migration is the chain's first link, already complete in the timeline given; its risk has passed. The senior-level point is the second half of the question: knowing the earliest date matters less than knowing which link currently carries the schedule. Managing and escalating dependencies across teams — your named skill — is largely the discipline of maintaining this chain in your head (or better, visibly for everyone), knowing that day-6 slippage by A costs the release day-for-day, and that on day 7 the watch item is C's progress, not A's. Escalation timed by chain position ("A's testing slipped this morning; R moves unless we parallelise C's setup today") is what distinguishes dependency management from dependency observation.

**Question 7 (hard) — Diagnosing a testing system's underperformance**

A team you guide has good practices on paper — risk-based test design, automation at 60%, exploratory sessions each release — yet their escaped-defect rate is twice the area average. You observe their work for a sprint and gather: (i) their test cases faithfully cover documented acceptance criteria; (ii) their escaped defects overwhelmingly involve interactions with an adjacent team's service, and undocumented behaviours of it; (iii) their exploratory charters target their own service's screens; (iv) their automation runs against a stubbed version of the adjacent service, with stubs written from that service's documentation. What is the root diagnosis?

- A) The team's testers lack skill and need basic retraining.
- B) The team's entire quality system is anchored to documented, own-service behaviour, while their actual risk lives at the integration boundary with the adjacent service's real, undocumented behaviour — the practices are good but aimed at the wrong target.
- C) The adjacent team should fix their documentation, and until then nothing can improve.
- D) Automation should be increased to 80%.

**Correct answer: B**

**Explanation:** Synthesise the four observations: acceptance-criteria coverage (i), stubs from documentation (iv), own-service exploratory charters (iii) — every layer of the quality system validates against the documented model of the world. But observation (ii) says the escapes come from where the real world departs from the documented model: the adjacent service's actual behaviour at the integration boundary. The system is well-built and mis-aimed — each practice individually sound, collectively blind in the one direction that matters. The interventions follow directly: exploratory charters targeted at the integration boundary; contract tests validated against the real adjacent service, not its documentation; periodic integrated-environment runs to catch stub drift; and a working relationship with the adjacent team so behavioural changes propagate before they escape. Option A misreads a system-aiming problem as an individual-skill problem — the commonest and most damaging mislocation, and the coaching error your role must avoid: these testers execute well within the frame they were given; the frame is the defect. Option C outsources the fix to another team's documentation habits — legitimate to pursue, hopeless as a dependency for improvement. Option D increases investment in the mis-aimed instrument. This question is your role in miniature: assessing the business impact of testing outcomes, using insights to improve quality assurance processes — and diagnosing systems rather than blaming people.

**Question 8 (hard) — Multi-constraint scheduling with a coaching dimension**

You must staff three concurrent needs across a two-week window with your area's three available senior-capable people (yourself, Priya, and Marcus): (a) a high-risk payments release needing experienced test analysis throughout both weeks; (b) a new team's test approach workshop, needing two consecutive days of an experienced facilitator in week 1; (c) an audit evidence review, needing three days in week 2, which regulators require to be performed by someone independent of the payments work. Priya is the strongest payments specialist. Marcus has never facilitated a workshop but wants to develop facilitation, and is competent at audit review. You are experienced at all three. Which allocation best serves both delivery and capability development?

- A) Priya on payments both weeks; you facilitate the workshop alone in week 1 and do the audit review in week 2; Marcus shadows you at the workshop.
- B) Priya on payments both weeks; you and Marcus co-facilitate the workshop in week 1 with Marcus leading sections under your support; Marcus does the audit review in week 2 — he is independent of payments — while you stay available to payments as senior cover and quality-check the audit evidence pack informally.
- C) Marcus on payments both weeks for the stretch; Priya facilitates the workshop; you do the audit.
- D) You take payments both weeks; Priya facilitates; Marcus does the audit unsupported.

**Correct answer: B**

**Explanation:** Check constraints first, then optimise development. Independence: the audit reviewer must be independent of payments — anyone on payments is disqualified from (c). Option B satisfies everything: Priya's specialism goes where risk concentrates; the workshop gets an experienced facilitator (you) while Marcus gets genuine development — co-facilitating with led sections, which is how facilitation is actually learned, not by shadowing (option A gives Marcus passive observation, the weakest development mode) and not by unsupported solo delivery; Marcus's audit independence holds since he never touches payments; and your week 2 stays flexible for the area's highest-risk item. Option A concentrates all senior delivery in you and develops nobody — the classic senior anti-pattern of buying short-term certainty with long-term capability stagnation. Option C sends the least payments-experienced person to the highest-risk payments work — development stretch belongs where failure is survivable, and a high-risk regulated release is not that place. Option D staffs adequately but abandons both development opportunities and puts your strongest payments specialist in a facilitation room while you — needed nowhere specific in week 1 — absorb the payments work. The senior discipline being assessed: coaching others in test analysis and guiding teams means designing work allocations where capability grows in the safe places and experience covers the dangerous ones — simultaneously, deliberately, every time you staff anything.

**Question 9 (hard) — Spotting the flaw in a proposed quality metric**

A programme office proposes a new area-wide metric: "Test effectiveness = defects found in testing ÷ test cases executed. Teams will be ranked monthly; the top team's practices will be adopted as standard." As senior analyst, you are asked to comment. What is the strongest analytical objection?

- A) The metric is fine but should be quarterly.
- B) The ratio is not comparable across teams and creates perverse incentives: it penalises stabilised products and effective prevention (fewer defects to find), rewards teams whose upstream quality is worst, is manipulable by executing fewer or coarser test cases, and ranking on it would drive test design toward the metric rather than toward risk — so effectiveness needs a basket of contextualised measures, not a single ranked ratio.
- C) Defects should be weighted by severity, which would fix the metric.
- D) The metric is invalid because testing cannot be measured.

**Correct answer: B**

**Explanation:** Interrogate the metric's behaviour, not just its formula. Numerator: defects found in testing varies with upstream quality — a team receiving poor code finds many defects and scores as "effective", while a team whose early engagement prevents defects (the outcome you actually want, and which your role advocates) scores as ineffective. Denominator: test cases executed is under each team's definitional control — merge ten checks into one case and the ratio rises; the ranking converts that from quirk to incentive. Cross-team comparability fails because both terms are context-dependent; monthly ranking adds noise-chasing; and standardising the "top" team's practices institutionalises whatever gamed best. The mature counter-proposal in option B matters as much as the critique: escaped-defect rates, detection percentage by phase, risk coverage of changed components — a contextualised basket, trended per team rather than ranked across teams. Option C fixes one flaw among five: severity weighting improves the numerator's meaning but leaves incomparability, gaming, and the prevention penalty intact. Option D surrenders measurement entirely, which is both false and, for a senior analyst, professionally self-defeating: implementing ways to capture data to drive continuous improvement is your named skill — the position is never "don't measure", it is "measure what you mean, and know what your metric will do when people are paid attention on it". Goodhart's law is a testing tool: apply it to every metric before it is adopted, because you will be the one managing its consequences.

**Question 10 (hard) — Reasoning about early risk identification in change**

Your organisation is replacing a legacy casework system in three phases: Phase 1 migrates read-only case viewing; Phase 2 migrates case creation and editing; Phase 3 migrates payments and decommissions the legacy system. During Phase 1 testing, you notice the migrated viewing service renders certain historical case records (roughly 2% of the sample, all predating a 2019 data model change) with missing fields — cosmetic in a read-only context, and Phase 1's acceptance criteria pass. What does senior-level risk analysis conclude?

- A) Phase 1 passes its criteria; note the cosmetic issue as low severity and move on.
- B) The rendering gaps are a low-impact symptom of a high-impact cause: pre-2019 records are not mapping cleanly to the new data model. In Phase 2 those same records will be edited and saved through that model, and in Phase 3 payments will run on it — where today's missing display fields become tomorrow's corrupted or mispaid cases. Escalate now as a migration data-model risk requiring investigation before Phase 2 designs freeze.
- C) Refuse to pass Phase 1 until all rendering is perfect.
- D) The legacy system is the problem, and decommissioning it in Phase 3 will resolve the inconsistencies.

**Correct answer: B**

**Explanation:** The reasoning move is severity projection across phases: an issue's current impact (cosmetic, read-only) and its causal significance (the data model mishandles pre-2019 records) are different quantities, and phased migrations systematically widen the gap between them. The same mapping defect that drops display fields today will, in Phase 2, sit under write operations — records edited through an incomplete model risk silent data loss on save — and in Phase 3 under payment calculations, where the failure mode is citizens' money. The 2% rate and the clean pre/post-2019 boundary make this diagnosable now, cheaply, while the mapping layer is still open for correction; after Phase 2's design freeze, the same fix costs rework plus migration re-runs plus possibly data repair. Option A is the criteria-compliance trap: acceptance criteria encode anticipated risk, and this risk was not anticipated — passing criteria is evidence, not absolution; identifying risks early, explicitly your role-level duty, means exactly this projection beyond the current phase's frame. Option C misaims the response: blocking Phase 1 punishes the phase where the issue is harmless instead of protecting the phases where it is not — the escalation target is Phase 2's design inputs, not Phase 1's gate. Option D reverses the causality: the legacy system holds the correct data; the new model's mapping loses it — decommissioning the source makes the loss permanent. This is analysing products, services, processes and change to identify risks early, performed at the level your role demands: seeing through the artefact in front of you to the system behind it, and timing the escalation to the decision it must influence.

**Question 11 (hard) — Error checking an automation architecture claim**

A team proposes consolidating their test automation: "We will replace our 300 UI-level tests with 1,200 API-level tests plus 40 UI journey tests. API tests run 50 times faster and are far less flaky, so overall suite time and reliability will improve dramatically, with better coverage." Their figures: current UI suite, 300 tests × 90 seconds average = 7.5 hours, 8% flake rate. Proposed: 1,200 API tests × 2 seconds + 40 UI tests × 90 seconds = 40 minutes + 1 hour = 1.7 hours claimed, API flake ~0.5%, UI flake 8%. Which check most needs making before endorsing the proposal?

- A) The arithmetic: 1,200 × 2s = 40 minutes and 40 × 90s = 60 minutes, totalling 1.7 hours — verify the sums.
- B) Whether the 1,200 API tests plus 40 UI journeys actually preserve the risk coverage of the 300 UI tests — specifically which UI-level behaviours (rendering, client-side validation, accessibility, browser interactions) are covered by neither the API layer nor the 40 journeys — since speed and stability gains are worthless where coverage silently narrows.
- C) Whether 0.5% is achievable for API flake rates.
- D) Whether the team can write 1,200 tests on schedule.

**Correct answer: B**

**Explanation:** First dispose of the arithmetic: 1,200 × 2s = 2,400s = 40 minutes; 40 × 90s = 3,600s = 60 minutes; total 100 minutes ≈ 1.7 hours — the sums hold (option A is worth thirty seconds, and only thirty seconds). The load-bearing claim is elsewhere: "with better coverage". Test count is not coverage — 1,200 API tests can exhaustively cover the service layer while covering zero of what only the UI layer exhibits: rendering across browsers and viewports, client-side validation and error display, JavaScript behaviour, accessibility semantics, and the interaction glue where many real user-facing failures live. The proposal moves from 300 UI tests to 40; the essential review artefact is a mapping of what the departing 260 verified and where each behaviour lands — API layer, one of the 40 journeys, manual/exploratory coverage, or nowhere. "Nowhere" entries are the proposal's true cost, and they must be listed and accepted, not discovered in production. This is the test-pyramid migration done rightly versus wrongly: the architecture is sound in shape (options C and D are legitimate secondary diligence — benchmark the flake claim, plan the build — but neither is fatal if wrong), while an unexamined coverage claim is the failure that surfaces as escaped UI defects six months after everyone celebrated the faster pipeline. Contributing to standards for designing tests, and improving test types and techniques through a structured process, means institutionalising exactly this check: every consolidation proposal carries a coverage disposition map before it carries a schedule.

**Question 12 (hard) — Synthesising conflicting signals into a recommendation**

Three months of signals about a team you guide: escaped defects are down 40%; their test cycle time has grown from 3 to 5 days, drawing delivery manager complaints; their exploratory testing hours have doubled; automation coverage is flat; team survey shows testers report higher confidence but developers report "testing slows us down"; and two of the escaped defects that did occur were in areas the team had explicitly deprioritised in their risk-based approach, with documented rationale that stakeholders had accepted. As senior analyst, what is the soundest overall reading?

- A) The team is failing: cycle time and developer sentiment are deteriorating.
- B) The team is succeeding: escaped defects are the only metric that matters.
- C) The quality investment is working (fewer escapes, and the escapes that occurred were accepted risks behaving as documented — the risk process functioning, not failing), but it is being purchased with unscaled manual effort, visible as cycle-time growth and developer friction; the recommendation is to keep the exploratory investment while attacking cycle time through automation growth and earlier test involvement, so the quality gains hold at sustainable speed.
- D) The signals contradict each other, so another quarter of data is needed before any conclusion.

**Correct answer: C**

**Explanation:** Senior synthesis means refusing both single-metric stories. The quality story is real: 40% fewer escapes, and — the subtle signal most readers miss — the two escapes that occurred fell in explicitly deprioritised areas with stakeholder-accepted rationale. That is not two failures; that is the risk-based approach performing exactly as designed: risk was assessed, accepted, documented, and the accepted risk materialised at documented scale. Treating accepted-risk escapes as process failures (option A's arithmetic) teaches teams to stop documenting risk acceptance — a corrosive lesson. The cost story is equally real: doubled exploratory hours with flat automation means the improvement rides on manual effort that does not scale; 3-to-5-day cycles and "testing slows us down" are that cost surfacing as delivery friction and relationship erosion — which, unaddressed, will eventually purchase pressure to cut exactly the practices producing the quality gains. Option C holds both truths and aims the intervention at the cost side without sacrificing the benefit side: automation growth to absorb the repeatable load, earlier involvement to shrink the end-of-cycle bulge — and, implicitly, a narrative for stakeholders that connects the cycle-time investment to the escape reduction they are enjoying. Option B's single metric ignores a sustainability problem compounding in plain sight. Option D mistakes tension for contradiction: the signals are not conflicting — they are one coherent story about benefit and cost, fully readable now. Determining whether an approach needs to change based on effort and risk is this exact judgement, and managing stakeholder expectations means telling the delivery managers the whole of it: what the five days are buying, and the plan to buy it cheaper.

### Preparation tips

- **Practise synthesis, not just analysis.** Senior-level questions increasingly hand you multiple signals and ask for the reading. Rehearse with your own area's data: take this month's metrics, trends and complaints, and write the three-sentence synthesis. The assessment version is the same act with unfamiliar numbers.
- **Interrogate every rule's structure before applying it.** Conjunctions, exceptions, scopes, and waiver routes — governance questions are lost by candidates who apply the gist. Map the rule's logic explicitly, then apply.
- **Trace chains to their current link.** Dependency and scheduling questions reward knowing not just the end date but which handoff carries it now. Practise by narrating your real programmes' critical paths from memory, then checking.
- **Name the system before the person.** In diagnostic questions, test the hypothesis "the practices are aimed wrong" before "the people are weak". It is usually righter, and it is always the more useful place to start — in assessments and in coaching alike.
- **Apply Goodhart's law to every metric you meet.** Ask what behaviour the measure would produce if people optimised it. This single habit answers most metric-design questions and improves every dashboard you govern.
- **Manage your pace by question weight.** Adaptive senior assessments back-load complexity. Bank the early questions efficiently to buy thinking time for the multi-signal items where accuracy is the differentiator.

### Common pitfalls to avoid

- **Reading maxima and minima without context.** The biggest number in a table is rarely the finding; the broken pattern is. Compare shapes before magnitudes.
- **Discarding explained outliers.** "Ignore the spike" answers the baseline question and buries the conditional one. Outliers with known, recurring causes are findings about system behaviour under those conditions.
- **Letting criteria compliance close your analysis.** Passing acceptance criteria bounds anticipated risk only. The senior question is always: what does this observation imply beyond the current phase's frame?
- **Accepting count-based coverage claims.** More tests is not more coverage; faster is not safer. Demand the disposition map: what did the old coverage verify, and where does each behaviour now live?
- **Averaging your way past conjunctions.** "Two of three conditions" fails a three-condition rule. Under stakeholder pressure this misreading sounds reasonable — which is exactly why it appears in assessments and governance meetings alike.
- **Concluding "insufficient data" when the data is merely uncomfortable.** Small, noisy, or tension-filled signal sets often support careful conclusions. The senior skill is stating what can be concluded, at what confidence, and what would change it — not deferring judgement until certainty arrives, because it never does.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures accuracy and judgement with the quantitative material your role genuinely produces and consumes. The operations remain accessible — percentages, ratios, weighted averages, rates, trend arithmetic — but at senior level the questions weight interpretation as heavily as calculation: choosing the right denominator, normalising before comparing, projecting trends honestly, and recognising what a figure legitimately supports.

The typical format is an online, timed test of 20 to 35 minutes with 15 to 20 questions built around tables, charts and short data narratives. Calculators are generally permitted; rough paper is essential. Scoring is objective against a norm group, reflecting accuracy and pace, with adaptive difficulty on many platforms.

For a senior quality assurance test analyst, numeric fluency is the load-bearing structure under most of your influence. You assess the business impact of testing outcomes — an inherently quantitative act: escape rates, detection percentages, cost of defect phases, availability losses, coverage against risk. You use defect patterns and trends to make recommendations, which means your credibility travels with your arithmetic: a recommendation resting on a mis-normalised comparison is not merely wrong, it is discoverably wrong, in front of the stakeholders whose expectations you manage. You implement ways to capture data that drives continuous improvement, which requires designing metrics whose denominators mean something and whose incentives point the right way. And you guide other analysts, who will inherit your numeric habits — including the bad ones — through every report of yours they imitate.

There is a further senior-specific dimension: you are frequently the numerate reviewer of other people's figures. Programme dashboards, vendor claims, team self-assessments and improvement business cases arrive containing arithmetic that nobody else will check. Several questions below are built in exactly that shape — a plausible figure with a flaw in its construction — because finding those flaws quickly, and articulating them without condescension, is a distinctly senior contribution. Work every question on paper, keep your intermediate values labelled, and hold each answer against the bounds the context implies before you commit. The habits are the same ones your reports should exhibit; the practice serves both.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Trend analysis and rate arithmetic** map to **Managing, reporting and resolving defects** ("use defect patterns and trends to make recommendations"): escape rates, discovery-to-closure flows and phase-detection percentages are the numeric substance of your recommendations.
- **Weighted aggregation** maps to your coordinating duties across a defined area: combining suite results, team metrics and multi-team figures without averaging averages is the difference between an area view and an area distortion.
- **Comparative normalisation** maps to **Test analysis** ("use multiple techniques to analyse complex information to identify risks"): comparing teams, releases, or periods honestly requires per-unit rates — per test executed, per release, per tester-day — before any conclusion.
- **Business-case arithmetic** maps to **Designing and executing tests** ("improve test types and techniques through a structured process") and **Test and quality planning**: automation investments, environment spending and process changes are argued in hours, costs and payback periods you must construct and defend.
- **Metric design judgement** maps to **Test and quality planning** ("implement ways to capture data to drive continuous improvement"): knowing what a proposed measure will actually reward is numeric reasoning applied prospectively.
- **Numeric communication** maps to **Communicating between the technical and non-technical**: managing the expectations of diverse senior stakeholders depends on presenting figures with their denominators, bounds and honest uncertainty attached.

### Practice questions

**Question 1 (easy) — Area-level escape rate**

Across your area last quarter, the four teams shipped: Alpha, 12 releases with 6 escaped defects; Beta, 8 releases with 6 escapes; Gamma, 10 releases with 5 escapes; Delta, 10 releases with 3 escapes. What was the area's overall escaped-defect rate per release?

- A) 0.50 per release
- B) 0.55 per release
- C) 0.60 per release
- D) 0.45 per release

**Correct answer: A**

**Explanation:** Aggregate raw totals first, then divide once. Total escapes: 6 + 6 + 5 + 3 = 20. Total releases: 12 + 8 + 10 + 10 = 40. Rate: 20 ÷ 40 = 0.50 escapes per release. The tempting alternative — averaging the four team rates (0.50, 0.75, 0.50, 0.30), which gives 0.5125 — is wrong in method even when close in value, because teams with different release counts deserve different weights; here the error is small, but with unequal team sizes it grows unpredictably in either direction. The professional habit: area-level figures always rebuild from raw counts, and your reports should show the counts alongside the rate so any reader can reconstruct it. As the person who guides others in quality assurance reporting, the version of this that matters most is the one you catch in a team's slide before the programme board does.

**Question 2 (easy) — Detection percentage by phase**

One team's defects for a release were found: 22 in unit and integration testing, 14 in system testing, 9 in user acceptance testing, and 5 in production (first month). What percentage of all defects were detected before production?

- A) 88%
- B) 90%
- C) 92%
- D) 85%

**Correct answer: B**

**Explanation:** Total defects: 22 + 14 + 9 + 5 = 50. Found before production: 22 + 14 + 9 = 45. Detection percentage: 45 ÷ 50 = 0.90 = 90%. With a base of 50, each defect is worth 2 percentage points — a convenient mental check. Two senior notes attach to this staple metric. First, its denominator is honest only over time: production defects accrue beyond the first month, so early-quoted detection percentages flatter, and your reports should state the observation window ("90% at one month post-release"). Second, the phase distribution itself carries the more actionable story: 22 caught at unit/integration level is the cheap-detection zone working, and shifting the 14 system-test finds earlier is usually worth more than perfecting the headline figure. When you use trends to make recommendations, the phase mix — not the single percentage — is where recommendations live.

**Question 3 (easy) — Environment cost of lost capacity**

Your area's shared TEST environment was unavailable for 22 hours of scheduled time last month. On average, 6 testers across the teams are blocked when it is down, and a tester-hour is costed internally at £55. What was the month's direct cost of the lost capacity?

- A) £1,210
- B) £7,260
- C) £6,050
- D) £13,200

**Correct answer: B**

**Explanation:** Lost tester-hours: 22 hours × 6 blocked testers = 132 tester-hours. Cost: 132 × £55 = £7,260. Work the multiplication carefully: 132 × 55 = 132 × 50 + 132 × 5 = 6,600 + 660 = 7,260. Option A prices only the 22 environment-hours, forgetting the multiplication across blocked people — the exact error that makes environment problems look cheap in programme discussions. Option D doubles the tester count. The senior-level use of this arithmetic is advocacy: "22 hours of downtime cost roughly £7,300 in blocked effort last month, before rework and schedule effects" converts a chronic grumble into a business case line, which is how ensuring test needs — environments included — are implemented early actually gets funded. Note the honest framing "before rework and schedule effects": direct-cost figures are floors, not totals, and saying so protects your credibility when someone probes the number.

**Question 4 (moderate) — Weighted automation coverage across teams**

Automation coverage of regression scope by team: Alpha 80% of 400 tests; Beta 60% of 250 tests; Gamma 75% of 200 tests; Delta 40% of 150 tests. What is the area's overall automation coverage?

- A) 63.8%
- B) 66.5%
- C) 68.0%
- D) 70.2%

**Correct answer: C**

**Explanation:** Convert to counts, sum, divide once. Automated tests: Alpha 0.80 × 400 = 320; Beta 0.60 × 250 = 150; Gamma 0.75 × 200 = 150; Delta 0.40 × 150 = 60. Total automated: 320 + 150 + 150 + 60 = 680. Total tests: 400 + 250 + 200 + 150 = 1,000. Coverage: 680 ÷ 1,000 = 68.0%. The unweighted average of the four percentages — (80 + 60 + 75 + 40) ÷ 4 = 63.75%, option A — understates the true figure because the largest team also has the highest coverage. Notice the direction of the distortion is not fixed: had Delta been the largest team, the unweighted average would have flattered instead. This is why "never average averages" is a rule and not a preference: the error's sign is unpredictable, which makes it uncorrectable by intuition. Area-level coverage figures feed strategy conversations and investment cases; rebuilding them from counts is thirty seconds of arithmetic that keeps your area's headline number defensible under any scrutiny.

**Question 5 (moderate) — Percentage-point versus percentage change**

A team's escaped-defect detection percentage improved from 84% to 91% over two quarters. Their delivery manager's slide says: "Detection improved by 7%." What is the accurate characterisation?

- A) The slide is correct: a 7% improvement.
- B) Detection improved by 7 percentage points, which is an 8.3% relative improvement — and the distinction matters because "7%" understates the achievement and, in other contexts, the same conflation can dramatically overstate changes.
- C) Detection improved by 8.3 percentage points.
- D) The improvement cannot be quantified without raw counts.

**Correct answer: B**

**Explanation:** Two different quantities hide in "improved by 7%". The absolute change is 91 − 84 = 7 percentage points. The relative change is 7 ÷ 84 = 0.0833 = 8.3%. The slide's phrasing names the relative measure ("improved by 7%") while meaning the absolute one — here a mild understatement, but the conflation is dangerous in general: a metric moving from 2% to 4% is "up 2 percentage points" and also "up 100%", and which phrasing a report chooses can manufacture alarm or complacency from identical data. Senior analysts police this distinction in both directions: in your own reports, write "percentage points" for absolute moves and reserve "%" changes for relative ones; in others' reports — especially vendor claims and programme dashboards — ask which is meant before accepting the impression. Option D overreaches: the two characterisations are computable from the percentages alone; raw counts would add confidence about scale and significance, which is a fair further request but not a bar to quantification. Precision of this kind is part of managing expectations: stakeholders remember the impression your numbers created, not the caveats they skimmed.

**Question 6 (moderate) — Defect flow and backlog projection**

A team's defect backlog stands at 60. Over the last four sprints, defects raised per sprint were 24, 26, 25, 25, and defects closed per sprint were 20, 21, 19, 20. The delivery manager asks: "If nothing changes, where is the backlog in six sprints, and what closure rate would hold it flat?" What do you tell them?

- A) About 90 in six sprints; closing 25 per sprint holds it flat.
- B) About 60 in six sprints; the current rate holds it flat.
- C) About 90 in six sprints; closing 20 per sprint holds it flat.
- D) About 30 in six sprints; the backlog is shrinking.

**Correct answer: A**

**Explanation:** Establish the flows from the recent averages: raised ≈ (24 + 26 + 25 + 25) ÷ 4 = 100 ÷ 4 = 25 per sprint; closed ≈ (20 + 21 + 19 + 20) ÷ 4 = 80 ÷ 4 = 20 per sprint. Net growth: +5 per sprint. Six sprints: 60 + (6 × 5) = 90. To hold the backlog flat, closure must equal arrival: 25 per sprint. Both halves of option A follow directly; the other options mix up stocks and flows in various ways. The stock-and-flow frame is the senior contribution here — backlogs are levels driven by rate differences, and most backlog conversations go wrong by discussing the level ("90 is too many!") without the rates that determine it. Your projection also carries an implicit recommendation menu: raise closure capacity by 5 per sprint, reduce arrivals (upstream quality work), or explicitly accept growth with severity-based triage protecting what matters. Presenting the arithmetic with those levers attached is what turns a forecast into a management conversation — and note the honest hedge "about 90": four sprints of history projects a trend, not a promise, and your phrasing should keep that visible.

**Question 7 (moderate) — Normalising vendor performance claims**

A tool vendor claims their platform "reduced regression time by 75% at a comparable government department". Your due diligence finds the department's figures: regression went from 12 hours to 3 hours — but simultaneously, the department cut its regression scope from 800 tests to 500 as part of a risk-based review. What is the fair like-for-like assessment of the tool's contribution?

- A) The 75% claim stands — 12 hours to 3 hours is a 75% reduction.
- B) Per-test time fell from 54 seconds to 21.6 seconds — a 60% per-test improvement attributable to tooling and process together, with the remaining headline gain explained by the 37.5% scope cut; a real improvement, but materially smaller than the headline once normalised.
- C) The tool contributed nothing; the scope cut explains everything.
- D) The claim cannot be assessed.

**Correct answer: B**

**Explanation:** Normalise before attributing. Per-test time before: 12 hours = 43,200 seconds ÷ 800 tests = 54 seconds per test. After: 3 hours = 10,800 seconds ÷ 500 tests = 21.6 seconds per test. Per-test improvement: (54 − 21.6) ÷ 54 = 32.4 ÷ 54 = 0.60 = 60%. Check the decomposition: had scope stayed at 800 with the new per-test time, regression would take 800 × 21.6s = 4.8 hours — a 60% time reduction from tooling-and-process; the further fall to 3 hours comes from running 37.5% fewer tests. So the headline 75% bundles two decisions, and only one of them is purchasable from the vendor. Option A accepts the bundle uncritically — the standard shape of tooling case studies, which report end states without controlling for concurrent changes. Option C overcorrects into the opposite error. Option D is unnecessary surrender: the figures given support exactly this decomposition. Two senior cautions complete the analysis: "attributable to tooling and process together" matters, because adoption usually arrives with process cleanup whose gains the tool absorbs credit for; and the scope cut itself may have been sound risk-based practice — but its benefit belongs to the department's analysts, not the vendor's brochure. This is the arithmetic of evaluating claims before your teams inherit them.

**Question 8 (moderate) — Cost distribution of defects by phase**

Your organisation's finance-agreed figures: a defect fixed during development costs £150; during system testing £700; during user acceptance £1,800; in production £6,500. Last quarter one team's 48 defects were found: 20 in development, 18 in system testing, 7 in UAT, 3 in production. What was the quarter's total defect cost, and what percentage of it came from the 3 production defects?

- A) £47,700 total; 41% from production
- B) £41,800 total; 47% from production
- C) £47,700 total; 14% from production
- D) £53,900 total; 36% from production

**Correct answer: A**

**Explanation:** Compute each phase, then total. Development: 20 × £150 = £3,000. System testing: 18 × £700 = £12,600. UAT: 7 × £1,800 = £12,600. Production: 3 × £6,500 = £19,500. Total: 3,000 + 12,600 = 15,600; 15,600 + 12,600 = 28,200; 28,200 + 19,500 = £47,700. Production's share: 19,500 ÷ 47,700 = 0.409 ≈ 41%. Option C pairs the right total with production's share of the defect count (3 ÷ 48 ≈ 6%, generously rounded) rather than its share of cost — the distractor exists precisely because count-share and cost-share are wildly different here, and conflating them is the standard way defect economics get misread. That gap is the finding: three production defects — about 6% of the quarter's defect count — generate roughly 41% of its defect cost. This asymmetry is the entire numeric argument for early detection, and it is the figure your improvement recommendations should lead with: every defect moved from production discovery to development discovery saves roughly £6,350, so an intervention that prevents even one production escape per quarter funds a lot of earlier testing. When you assess the business impact of testing outcomes for stakeholders, phase-cost arithmetic like this is the translation layer between testing activity and money — the language in which quality investment cases are actually won.

**Question 9 (hard) — Statistical caution with small counts**

Two teams' production incident counts last quarter: Team P, 2 incidents from 9 releases; Team Q, 5 incidents from 11 releases. A programme report concludes: "Team Q's release quality is more than twice as bad as Team P's (0.45 vs 0.22 incidents per release)." What is the soundest senior assessment of this conclusion?

- A) The conclusion is correct: 0.45 is more than twice 0.22.
- B) The rates are correctly computed, but with counts this small (2 and 5 incidents) the difference is well within ordinary random variation — one incident more or fewer would move either rate by 9-11 points — so the data cannot support a confident quality ranking, though it can justify watching both trends over more quarters.
- C) The comparison is invalid because the teams have different release counts.
- D) Team P should be investigated for under-reporting incidents.

**Correct answer: B**

**Explanation:** The arithmetic is right: 2 ÷ 9 = 0.22; 5 ÷ 11 = 0.45. The inference is not. With single-digit incident counts, chance dominates: shift one incident and Team P becomes 3/9 = 0.33 or 1/9 = 0.11; Team Q becomes 4/11 = 0.36 or 6/11 = 0.55 — the "twice as bad" gap opens and closes on the movement of a single event. A rough rule for count data: the natural variability of a count n is on the order of √n, so Team Q's 5 incidents carries uncertainty of about ±2.2, and the two teams' plausible ranges overlap substantially. You need no formal statistics in the assessment — only the calibrated instinct that ratios of small counts are unstable, and rankings built on them are noise wearing a conclusion's clothes. Option C misfires: different denominators are exactly what rates exist to handle; the problem is count size, not count difference. Option D invents an accusation from nothing. The senior duty is the follow-through: reports like this drive real consequences — scrutiny, morale, resourcing — so your review comment should offer the constructive alternative: aggregate over more quarters, compare against each team's own trend, and treat cross-team rankings as meaningful only when the counts could survive a one-incident perturbation. Implementing data capture for continuous improvement includes protecting the organisation from its own dashboard's false confidence.

**Question 10 (hard) — Regression suite growth and maintenance drag**

A team's automated suite grows by 15 tests per sprint. Each test consumes an average of 6 minutes of maintenance effort per sprint (flake investigation, updates for UI changes, data upkeep). The team currently has 400 tests and budgets 50 hours per sprint for automation maintenance. In how many sprints does maintenance demand exceed budget, and what does the arithmetic imply for strategy?

- A) After about 7 sprints; the team should stop writing tests.
- B) Maintenance already exceeds budget; the strategy question is immediate.
- C) After about 6-7 sprints; the implication is not to stop growing but to attack the per-test maintenance cost and prune low-value tests, because at 6 minutes per test per sprint the suite's carrying cost grows linearly with its size.
- D) After 10 sprints; no action needed yet.

**Correct answer: C**

**Explanation:** Current demand: 400 tests × 6 minutes = 2,400 minutes = 40 hours per sprint — inside the 50-hour budget with 10 hours of headroom. Each sprint adds 15 tests × 6 minutes = 90 minutes = 1.5 hours of new permanent demand. Headroom exhausts at 10 ÷ 1.5 = 6.67 sprints — demand exceeds budget during sprint 7. Options A and D miscompute or misjudge; option B mistakes 40 for more than 50. The strategic half distinguishes the senior answer: the linear model (demand = 6 minutes × suite size) identifies two levers, and "stop growing" is the wrong one — new tests presumably cover new risk. The durable levers are the coefficient and the population: drive per-test maintenance below 6 minutes (stability engineering, better locators and waits, shared fixtures — **Test engineering** improvements), and prune tests whose risk coverage no longer earns their carrying cost, because a test's cost is perpetual while its value can expire with the risk it covered. The habit worth exporting to the teams you guide: every suite has a carrying-cost equation; teams that never compute it discover it as a crisis, in the sprint when maintenance quietly cannibalises new-test capacity and coverage growth stalls. Improve test types and techniques through a structured process — this arithmetic is the structure.

**Question 11 (hard) — Reading a two-way improvement table honestly**

An improvement programme reports before/after figures for the three teams that completed it:

| Team | Escapes per release (before) | Escapes per release (after) | Releases (after period) |
|---|---|---|---|
| K | 0.9 | 0.5 | 10 |
| L | 1.2 | 0.7 | 4 |
| M | 0.6 | 0.5 | 6 |

The programme claims: "Average improvement: 33%; the programme should be rolled out area-wide." Which assessment is most sound?

- A) The claim is sound: ((0.9→0.5 is 44%) + (1.2→0.7 is 42%) + (0.6→0.5 is 17%)) ÷ 3 ≈ 34%, confirming roughly 33%.
- B) The improvements are real but the evidence has three weaknesses before area-wide rollout: the after-period counts are small (L's rate rests on 4 releases ≈ 3 escapes); the three teams volunteered or were selected, so regression to the mean and selection effects may inflate apparent gains — the teams with worst "before" figures improved most, a classic mean-reversion signature; and no comparison teams are shown, so area-wide trends (better tooling, calmer quarter) could explain part of the change. Recommend rollout accompanied by comparison-group measurement rather than on this evidence alone.
- C) The programme failed for Team M and should be cancelled.
- D) The percentages should be weighted by release count, giving a different average that settles the question.

**Correct answer: B**

**Explanation:** Verify the claimed arithmetic first: K improved (0.9 − 0.5) ÷ 0.9 = 44%; L improved (1.2 − 0.7) ÷ 1.2 = 42%; M improved (0.6 − 0.5) ÷ 0.6 = 17%; simple average ≈ 34% — the "33%" is honestly computed (option A's check is right as arithmetic). The senior question is whether the number means what the rollout recommendation needs it to mean, and three flaws intervene. Small denominators: L's after-rate of 0.7 over 4 releases is about 3 escapes — a one-escape change moves it to 0.5 or 1.0, so its 42% is fragile. Mean reversion and selection: the biggest improvements sit exactly where the worst before-figures were, which is what random fluctuation plus selective enrolment produces even from an ineffective programme; without knowing how teams entered the programme, the pattern is uninterpretable. No control: if untreated teams also improved this period, the programme's marginal effect shrinks accordingly. None of this proves the programme worthless — the honest position is B's: plausible benefit, insufficient evidence for confident area-wide attribution, and a rollout design (with comparison measurement) that generates the missing evidence while proceeding. Option C misreads M: 17% from the area's best baseline may be the ceiling effect, not failure. Option D's weighting is a legitimate refinement that answers none of the three structural problems — recomputing a flawed comparison more precisely does not repair its flaws. This is the evaluation literacy your role's improvement-data duty implies: enthusiasm for improvement, rigour about what the numbers actually license.

**Question 12 (hard) — Composite risk-coverage arithmetic for a release decision**

For Thursday's area release, the changed scope decomposes into: 12 high-risk requirement areas, of which 10 are fully tested and 2 are partially tested at 50% of planned depth; 30 medium-risk areas, 24 fully tested, 6 untested; 40 low-risk areas, 20 fully tested, 20 untested. Your area's agreed weighting counts high-risk areas at 5, medium at 2, low at 1. What weighted risk-coverage percentage do you report, and which single fact most needs stating alongside it?

- A) 78%; alongside it, the two half-tested high-risk areas, because weighted aggregates conceal exactly which risk is uncovered
- B) 78%; alongside it, the 20 untested low-risk areas, because they are the largest count
- C) 84%; no single fact needed — the percentage speaks for itself
- D) 68%; alongside it, the six untested medium-risk areas

**Correct answer: A**

**Explanation:** Build the weighted arithmetic explicitly. Total weighted scope: high 12 × 5 = 60; medium 30 × 2 = 60; low 40 × 1 = 40; sum 160. Covered weight: high — 10 full × 5 = 50, plus 2 partial at 50% depth = 2 × 5 × 0.5 = 5, giving 55; medium — 24 × 2 = 48; low — 20 × 1 = 20. Covered total: 55 + 48 + 20 = 123. Coverage: 123 ÷ 160 = 0.769 ≈ 77%, nearest offered figure 78% (the options' rounding; the computation is the skill). The second half of the question is the senior half: which single fact must accompany the aggregate? The two half-tested high-risk areas — because a weighted percentage is a compression, and what it compresses away is location: 78% could describe a release missing only low-value corners or one missing half the depth on two high-risk areas, and those are different release decisions wearing the same number. Option B highlights the largest count, which the weighting has already correctly deprioritised; option D names a real gap but not the highest-weight one. Option C — "the percentage speaks for itself" — is the precise failure mode your reporting exists to prevent: aggregates never speak for themselves; they speak for whoever chose what to aggregate. The reporting pattern to institutionalise across your teams: headline figure, then the specific highest-weight uncovered items by name, then the recommendation. That is clearly communicating risk to stakeholders, arithmetically grounded and decision-shaped.

### Preparation tips

- **Rebuild every aggregate from raw counts.** Weighted averages, area rollups, blended rates — the method is always counts first, division last. Practise until averaging averages feels physically uncomfortable.
- **Say "percentage points" aloud.** Drill the absolute/relative distinction until your own reports never conflate them and your eye catches the conflation in others' within seconds.
- **Model stocks and flows.** Backlogs, suites, headroom: level now, rate in, rate out, time to threshold. Four numbers, one subtraction, one division — and most capacity questions in tests and in planning yield to them.
- **Normalise before attributing.** Any before/after claim spanning a concurrent change (scope cuts, team growth, tooling swaps) needs per-unit rates before the improvement is assigned a cause. Vendor case studies are your richest practice material.
- **Respect small counts.** Before ranking anything, perturb each figure by one event and see if the ranking survives. If it does not, the honest conclusion is a trend-watch, not a verdict.
- **Attach the location to every aggregate.** In practice and in tests, when you compute a composite figure, immediately name the most consequential item it conceals. The habit answers the hardest question format and upgrades every report you review or write.

### Common pitfalls to avoid

- **Averaging averages across unequal groups.** The senior version of the classic error: it creeps into area rollups, programme dashboards and improvement claims, and its sign is unpredictable — rebuild from counts, every time.
- **Confusing arithmetic correctness with inferential validity.** A correctly computed rate on 3 incidents, a faithful average of selected volunteers — the sums check out and the conclusion still fails. Verify the computation, then interrogate what it can support.
- **Accepting bundled attributions.** Headline improvements that span scope changes, process changes and tooling changes belong to the bundle, not to whichever component is being sold. Decompose before you endorse.
- **Quoting rates without observation windows.** Detection percentages, escape rates and incident counts mature over time; a figure without its window flatters systematically. State the window; expect others to have omitted it.
- **Letting linear costs surprise you.** Suite maintenance, backlog growth, capacity headroom — linear equations with known coefficients should never produce emergencies. If a threshold-crossing is computable, compute it before it arrives.
- **Publishing aggregates without their concealments.** Every composite number hides a distribution; the hidden tail is where release decisions go wrong. Pair each headline figure with the named, highest-consequence item it compresses away.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures precision in extracting, evaluating and acting on written information — using the document classes your role genuinely handles: organisational standards, governance policies, senior stakeholder correspondence, audit findings, supplier contracts and cross-team communications.

The typical format is an online, timed test of 15 to 25 minutes: short passages followed by questions, dominated by **true / false / cannot say** judgements — is a statement definitely supported, definitely contradicted, or undetermined by the passage alone? — supplemented by best-summary, inference, and clear-writing questions. Scoring is objective against a norm group, reflecting accuracy and pace.

At senior level, the stakes of this skill change character. You no longer merely read requirements; you interpret standards for others, and your interpretation propagates — a misread qualifier in a governance document becomes a dozen teams' misunderstanding once you have explained it in the community of practice. You draft and review the documents that constrain others: contributing to standards for defect management and test design means writing rules that must survive motivated misreading, and reviewing others' drafts for the ambiguities that will be exploited or stumbled over later. You operate in correspondence with diverse senior stakeholders, where what an email actually commits its sender to — and what your reply will commit you to — must be read and written with near-contractual care. And you manage communications during defect resolution, where the difference between "the supplier states the fix is deployed" and "the fix is deployed" can decide whether your area retests today or waits for evidence.

The true/false/cannot-say discipline is the formal rehearsal of all this: it trains the separation between what a text asserts, what it implies, what it merely permits you to suspect, and what it leaves genuinely open. Senior professionals are, if anything, more vulnerable than juniors to one specific failure mode here — expertise-driven gap-filling, where deep domain knowledge quietly supplies what the passage never said. The questions below are constructed to catch exactly that reflex, because the assessments will be, and because the habit of noticing your own inferences is the foundation of both accurate reading and honest reporting.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Precise extraction from standards and policies** maps to your duty to contribute to, and enable others to follow, quality assurance and testing standards: you cannot enable others to follow what you have not read exactly, and your explanations inherit your reading's precision.
- **True / false / cannot say discipline** maps to **Test analysis** ("use multiple techniques to analyse complex information to identify risks"): risk identification begins with separating what documents establish from what they leave open — the open items are usually where the risk lives.
- **Attribution and commitment tracking** maps to **Managing, reporting and resolving defects** ("manage stakeholder expectations and communications during defect resolution"): supplier claims, developer assurances and stakeholder requests must be read for what they actually commit, and replies drafted for what they actually promise.
- **Argument evaluation** maps to **Test analysis** and **Designing and executing tests** ("improve test types and techniques through a structured process"): proposals, business cases and post-incident narratives arrive as arguments; structured improvement requires testing their reasoning before adopting their conclusions.
- **Clear-writing judgement** maps to **Communicating between the technical and non-technical** ("listen to and interpret the needs of technical and non-technical stakeholders, and manage their expectations"; "support or host difficult discussions"): the sentences you choose in escalations, summaries and standards are instruments of expectation management — precision in them is the skill.

### Practice questions

For questions 1 to 6, read the passage, then judge each statement as **True** (stated or following necessarily), **False** (contradicted), or **Cannot say** (undetermined from the passage alone).

**Passage 1:**

> Extract from the organisation's Quality Assurance Standard, section 7 (Defect Management): Each delivery team must operate a defect management process conforming to this standard. Defects must be recorded in the organisation's designated tracking tool within one working day of discovery. Severity must be assigned using the four-level scheme in Annex B; severity assignments may be revised as understanding develops, and any revision must be recorded with a rationale. Severity 1 defects must be escalated to the area's senior quality assurance test analyst on the day of discovery. Where a defect's resolution requires change by a team other than the discovering team, the discovering team retains ownership of the defect record until resolution is verified. Annual audits will sample defect records for conformance; teams with conformance below 90% must submit an improvement plan.

**Question 1 (easy) — True / false / cannot say**

Statement: "A severity assignment, once recorded, may be changed if a rationale for the change is recorded."

- A) True
- B) False
- C) Cannot say
- D) True, but only within one working day

**Correct answer: A**

**Explanation:** The standard states: "severity assignments may be revised as understanding develops, and any revision must be recorded with a rationale." The statement matches both halves — revision is permitted, and the rationale requirement attaches to it — so it is True. Option D imports the one-working-day clause from the adjacent sentence, which governs initial recording of defects, not revision of severity; keeping each obligation attached to its own subject is the elementary discipline this question checks, and the one most commonly lost when standards are quoted from memory in meetings. Note the standard's design logic, worth articulating when you enable others to follow it: revisable severity with recorded rationale balances honesty (early ratings are estimates) against accountability (silent downgrades are the classic way inconvenient defects disappear from release visibility). When a team asks you "can we re-rate this?", the full answer is "yes, with a written why" — and the written why is what the annual audit will sample.

**Question 2 (easy) — True / false / cannot say**

Statement: "If Team X discovers a defect whose fix must be made by Team Y, ownership of the defect record transfers to Team Y once they accept the work."

- A) True
- B) False
- C) Cannot say
- D) True, if both teams agree

**Correct answer: B**

**Explanation:** The standard says the opposite: "the discovering team retains ownership of the defect record until resolution is verified." The statement's transfer-on-acceptance model contradicts the retention rule, so it is False — and option D's "if both teams agree" adds a consent mechanism the standard does not provide; a rule stating what "must" happen is not varied by bilateral agreement unless the standard says so. The design rationale is worth carrying into your cross-team practice, since managing dependencies and defects across teams is your named skill: retention-until-verification exists because handed-off defects orphan easily — the fixing team closes its change, nobody retests from the user's side, and the defect resurfaces in production with no owner. The discovering team's retained ownership keeps one accountable party watching until verification. When you guide teams through cross-team defect flows, this is the clause to make vivid: ownership is not about who does the work; it is about who cannot look away until the work is proven.

**Question 3 (moderate) — True / false / cannot say**

Statement: "A team whose audit conformance is 92% is not required to submit an improvement plan."

- A) True
- B) False
- C) Cannot say
- D) False — all teams must submit improvement plans annually

**Correct answer: A**

**Explanation:** The standard requires improvement plans from "teams with conformance below 90%". At 92%, the condition triggering the obligation is unmet, so the standard imposes no improvement-plan requirement on this team — the statement is True. Be precise about what makes this True rather than Cannot say: the statement claims only that the standard does not require a plan, and that follows directly from the conditional's structure — an obligation conditioned on "below 90%" is, by its own terms, not imposed at 92%. (Had the statement claimed the team "must not" or "will not" submit one, Cannot say would beckon — nothing stops a team submitting voluntarily, and other rules outside this extract might exist.) Option D invents a universal obligation the text conditions explicitly. This distinction — what a rule requires, what it permits, what it is merely silent about — is the exact grain of reading that standards governance runs on, and the one to model precisely when teams bring you their "do we have to?" questions: the answer distinguishes "the standard doesn't require it" from "you may not do it", and conflating those two is how organisations accumulate imaginary rules.

**Passage 2:**

> Email from a supplier's delivery director to your head of delivery, copied to you: "Further to Friday's incident, our engineering team has identified the probable cause as a race condition in the caching layer introduced in our 4.7 release. A fix has been developed and has passed our internal regression suite. We intend to deploy it to your staging environment on Wednesday, subject to completion of our internal change approval. We would welcome your team's verification before production deployment. Separately, we note that your team's test traffic during the incident investigation exceeded the volumes specified in the service agreement; we raise this for awareness rather than as a formal notice. We remain committed to the remediation timeline shared last week."

**Question 4 (moderate) — True / false / cannot say**

Statement: "The supplier has confirmed that the race condition in the caching layer caused Friday's incident."

- A) True
- B) False
- C) Cannot say
- D) True — they identified it and built a fix

**Correct answer: C**

**Explanation:** Read the modality exactly: the supplier's engineering team "has identified the probable cause" — probable, not confirmed. The email asserts a leading hypothesis with a developed fix, which is meaningfully different from a confirmed root cause, and the passage gives no further evidence upgrading probability to confirmation. So whether the race condition caused the incident remains undetermined on this text: Cannot say. Option D reasons that fix-building implies confirmation — but suppliers routinely fix probable causes while investigation continues, and the email's own word choice preserves exactly that uncertainty. The practical consequence is why this reading matters at your level: your verification plan on Wednesday should test both that the fix resolves the incident's failure mode and that the incident's symptoms cannot still be reproduced — because if the probable cause is the wrong cause, the fix will pass its own logic and the incident will recur. Managing communications during defect resolution means holding your stakeholders' understanding at the evidence's actual level: "the supplier's leading hypothesis, fix pending our verification" — not the more comfortable "cause found, fix coming" your head of delivery may prefer to hear.

**Question 5 (moderate) — True / false / cannot say**

Statement: "The fix will be deployed to staging on Wednesday."

- A) True
- B) False
- C) Cannot say
- D) True — the supplier has committed to Wednesday

**Correct answer: C**

**Explanation:** The email says the supplier "intend[s] to deploy it to your staging environment on Wednesday, subject to completion of our internal change approval." Two hedges stand between this sentence and the statement's confident future fact: intention (not commitment) and an explicit condition (their change approval, whose status is unstated). Whether deployment actually happens Wednesday is therefore undetermined: Cannot say. Option D upgrades "intend, subject to" into "committed" — precisely the strengthening this email is drafted to avoid, and supplier correspondence is drafted; treating its hedges as accidental is a reading error with contractual consequences. The senior skill here operates in both directions. Reading: your Wednesday verification resourcing should be provisional, with the condition tracked ("has their change approval completed?") rather than the date assumed. Writing: notice the technique for your own correspondence — when your teams cannot yet commit, "we intend to, subject to" is the honest construction, and when you need the counterparty's commitment, your reply should convert hedges to dates explicitly: "please confirm deployment will occur Wednesday" — because managing expectations across organisational boundaries is done one carefully-read, carefully-written sentence at a time.

**Question 6 (moderate) — True / false / cannot say**

Statement: "The supplier has issued a formal notice that your team breached the service agreement's test traffic volumes."

- A) True
- B) False
- C) Cannot say
- D) True in substance, though politely worded

**Correct answer: B**

**Explanation:** The email states the traffic point is raised "for awareness rather than as a formal notice" — an explicit disclaimer of exactly the status the statement asserts. The passage directly contradicts "has issued a formal notice": False. Option D — "true in substance" — deserves its own paragraph, because it embodies a sophisticated-sounding error: in contractual correspondence, the formal status of a communication is part of its substance. Suppliers place markers like this deliberately — an "awareness" mention creates a contemporaneous record of the volume excess without triggering the dispute-handling machinery a formal notice would engage, preserving the option to formalise later. Reading it as a notice overreacts; failing to register it at all under-reacts. The senior response threads between: note it, verify the volume facts internally, and ensure your own incident-investigation practices stay within agreement bounds — because the marker's existence means the topic may return. Managing stakeholder communications at your level includes reading the diplomatic layer accurately: what was said, what was pointedly not said, and what the difference is designed to preserve.

**Question 7 (moderate) — Best summary of a governance extract**

Read this extract from a programme quality governance paper:

> Quality gates exist to inform release decisions, not to make them. A gate assessment reports the state of the evidence: what has been tested, what has not, what was found, and what residual risk remains. The release decision itself weighs that evidence alongside factors outside the gate's scope — commercial commitments, policy deadlines, operational readiness — and is owned by the service owner. Accordingly, a gate may be reported as "not met" and a release may still proceed, provided the decision and its rationale are recorded. What a gate assessment may never do is misdescribe the evidence to fit the intended decision.

Which option best summarises the extract?

- A) Quality gates are advisory and can be ignored if deadlines demand it.
- B) Gate assessments report evidence and residual risk; release decisions weigh that evidence with wider factors and belong to the service owner; releasing against an unmet gate is legitimate if recorded — but falsifying the assessment to match the decision never is.
- C) The service owner may overrule testing, so gate assessments carry little weight.
- D) Releases must not proceed when a gate is not met, except with recorded rationale, which effectively means gates are binding.

**Correct answer: B**

**Explanation:** Track each of the extract's moves: gates inform rather than decide; assessments report evidence, gaps and residual risk; decisions integrate wider factors and belong to the service owner; unmet-gate releases are permitted with recorded rationale; misdescribing evidence is absolutely prohibited. Option B preserves all five at their stated strength — including the crucial asymmetry between the flexible decision layer and the inviolable evidence layer, which is the extract's entire architecture. Option A collapses that asymmetry into "can be ignored", losing both the recording requirement and the falsification prohibition — the two teeth the governance actually has. Option C reads the decision-rights allocation as a status insult to testing, which inverts the design: separating evidence from decision protects the assessment's integrity precisely by relieving it of decision pressure. Option D inverts the permission structure, rendering "may proceed provided recorded" as "must not except", a strengthening that misstates the default. This governance model is one you will administer and explain: when a team's gate is unmet and the release proceeds anyway, your community will ask whether testing "lost" — and the accurate answer, straight from this architecture, is that testing's role was fully discharged the moment the evidence was reported truthfully and the decision recorded against it. Enabling others to follow standards includes teaching them what the standard actually protects: not the decision they preferred, but the truth of the record.

**Question 8 (moderate) — Inference from an audit finding**

An internal audit report states: "In 7 of the 20 sampled defect records from Area N, severity had been revised downward within 48 hours of a release decision meeting, without recorded rationale. We make no finding as to intent. Conformance with the revision-rationale requirement was 65% against a 90% threshold." As the area's senior analyst, which conclusion is best supported?

- A) Teams in Area N deliberately downgraded defects to smooth releases.
- B) The audit establishes a conformance failure (65% against 90%) and a concerning pattern (downgrades clustering before release decisions, unrationalised); intent is explicitly not established — so the response must address both the process gap (rationale discipline) and the pattern's release-pressure context, without prosecuting individuals on evidence that does not support it.
- C) The audit proves severity revision itself is bad practice and should be banned.
- D) A 65% conformance rate on 20 records is statistically meaningless.

**Correct answer: B**

**Explanation:** Separate what the audit establishes from what it declines to establish — the report itself models the discipline by stating "we make no finding as to intent." Established: a conformance breach (65% versus the 90% threshold, triggering an improvement plan under the standard) and a temporal pattern (downgrades clustering within 48 hours of release decisions) that is legitimately concerning because it is the signature pressure-driven downgrading would leave. Not established: that pressure-driven downgrading occurred — innocent explanations exist (triage meetings before releases genuinely produce legitimate re-ratings as understanding matures; the failure may be recording discipline, not rating integrity). Option A converts a pattern consistent with misconduct into a finding of misconduct, exceeding the evidence and — if acted on as accusation — poisoning the area's reporting culture in exactly the way that produces more hiding, not less. Option C bans the mechanism (revision) whose controlled use the standard deliberately permits; the failure was the missing rationale, not the revision. Option D dismisses evidence that is perfectly adequate for a conformance finding — 13 of 20 records lacking required rationale is a fact about those records, whatever wider inferences await more data. The senior response in option B is the audit-literate one: fix the discipline, examine the pressure context (are release meetings implicitly demanding severity haircuts?), and protect individuals from conclusions the evidence does not carry. Contributing to standards for defect management includes responding to audits of those standards with exactly this calibration.

**Question 9 (hard) — Clear-writing judgement in a senior escalation**

You must escalate to the programme director: a cross-team dependency (Team R's API contract changes) has invalidated part of your area's completed regression testing for the release now scheduled in six days, and re-testing requires four days plus environment access you do not control. Which drafting communicates most effectively?

- A) "Due to upstream interdependency volatility, previously executed verification activities have been partially invalidated, necessitating re-execution within a constrained window contingent on environmental enablement."
- B) "Team R's late API changes have broken our testing and put the release at risk. We need environments immediately and the six-day timeline was always unrealistic."
- C) "Team R's API contract changes on Tuesday invalidated regression results for the three services that consume that API. Re-testing needs four days and access to the integrated TEST environment, which is currently allocated to Team S. With six days to release, this is achievable only if environment access begins by Thursday. Decision needed: either direct the environment reallocation by Thursday, or accept release with the three services unverified against the new contract — we recommend the former."
- D) "There may be some retesting implications from recent API changes; we are looking into options and will revert."

**Correct answer: C**

**Explanation:** Measure each draft against what a director-level escalation must accomplish: establish the facts, quantify the constraint, name the decision, and make the deadline for deciding explicit. Option C delivers all four in ninety words: cause (Tuesday's contract changes), precise scope (three consuming services), requirement (four days plus a named environment with its current holder identified), the binding constraint (access by Thursday or the maths fails), and — the senior signature — a decision framed as two honest options with a recommendation, so the director's next action is choosing, not interrogating. Option A is abstraction as evasion: "interdependency volatility" and "environmental enablement" survive the escalation without transmitting a single actionable fact — the reader must ask what happened, and directors correctly interpret such prose as either not understanding or not saying. Option B has the facts' skeleton but wraps them in blame ("broken our testing") and retrospective grievance ("always unrealistic"), converting a decision-request into a conflict artefact that will now circulate with Team R's name attacked in it — hosting difficult discussions at senior level means writing escalations the other team could read without the relationship burning. Option D is the deferral disguised as diligence: six days minus "we will revert" equals a decision made by calendar default. The pattern to institutionalise from option C — facts, constraint, options, recommendation, decision deadline — is the escalation grammar your role's "manage active and reactive communication" duty names, and the one your example teaches the analysts who will someday escalate to you.

**Question 10 (hard) — True / false / cannot say with interacting provisions**

Read this extract from a test data policy:

> Production data may not be copied to any test environment except under a Data Access Exemption (DAE). A DAE may be granted only by the Data Protection Officer (DPO), only for a named purpose, and lapses when that purpose completes or after 15 working days, whichever is earlier. Data obtained under a DAE must be destroyed within 2 working days of lapse, with destruction evidenced in the exemption log. The DPO may extend a DAE once, by up to 10 working days, where the named purpose remains incomplete; extension requests must be made before the original DAE lapses. A lapsed DAE may not be extended or renewed for the same purpose.

Statement: "A team whose DAE lapsed yesterday, with its named purpose incomplete, can obtain a 10-day extension from the DPO provided they apply today and evidence destruction of the data."

- A) True
- B) False
- C) Cannot say
- D) True, provided the DPO agrees the purpose remains incomplete

**Correct answer: B**

**Explanation:** Trace the extension machinery clause by clause. Extensions exist ("may extend a DAE once, by up to 10 working days, where the named purpose remains incomplete") — but carry a temporal condition: "extension requests must be made before the original DAE lapses." This DAE lapsed yesterday; today's application is after lapse. And the policy closes the recovery route explicitly: "a lapsed DAE may not be extended or renewed for the same purpose." The statement asserts an entitlement the policy forecloses twice over — False, regardless of the DPO's sympathy (option D's "provided the DPO agrees" cannot revive a power the policy has extinguished; discretion operates within rules, not over them). The destruction-evidencing clause in the statement is a decorative irrelevance to the extension question — destruction within 2 working days of lapse is now this team's obligation, not their bargaining chip. What the team can actually do sits outside the statement: seek a fresh DAE for a differently-named purpose if one genuinely exists, or complete the work without production data. The drafting lesson is the senior takeaway: this policy's teeth are its deadlines-before-deadlines (request extension before lapse) and its explicit foreclosures (no post-lapse revival) — exactly the constructions that make rules enforceable, and exactly what to look for first when you read any policy, because the interaction of provisions, not any single one, is where hard questions and real compliance failures both live. Your teams will hit this pattern with real DAEs; the senior analyst who has read the interaction in advance is the one who ensures extension requests go in on day 12, not day 16.

**Question 11 (hard) — Evaluating a post-incident narrative**

A team's post-incident review states: "The production incident occurred because UAT was compressed from five days to two by the delivery deadline. Had UAT run its full five days, the defect would have been caught. Therefore the incident's root cause is the deadline compression, and the corrective action is a policy that UAT is never compressed." Which is the strongest critical evaluation?

- A) The narrative is sound: compression caused the miss, so preventing compression prevents recurrence.
- B) The causal chain has an unverified central link — whether five-day UAT would have caught this defect depends on whether its test coverage addressed the defect's area at all, which the review does not establish; the compression is one plausible contributing factor among several unexamined ones (was the defect class covered by any planned test? why did earlier phases miss it?), and the proposed policy is both unenforceable against real deadline pressure and blind to the possibility that the coverage, not the calendar, was the gap.
- C) The narrative is wrong because incidents always have multiple causes, so no single corrective action is ever valid.
- D) The review should be rejected because it criticises the delivery deadline, which was a business decision.

**Correct answer: B**

**Explanation:** Test the argument's load-bearing link: "had UAT run five days, the defect would have been caught." This counterfactual is asserted, not evidenced — it holds only if the five-day plan included testing that would have exercised the defect's failure mode. If the defect lay outside planned coverage, ten days would have missed it identically, and the corrective policy protects nothing. The review also stops its causal analysis one convenient step early: why did unit, integration and system testing all miss the defect — was it a class of failure (concurrency, data-dependent, environmental) that the team's approach does not probe at any phase? A compressed UAT is a genuine finding worth recording; anointing it "root cause" forecloses the coverage question that may matter more. Option B also correctly diagnoses the corrective action's two flaws: "never compressed" policies collapse at first contact with the next ministerial deadline (unenforceable absolutes breed silent exceptions — worse than honest trade-off frameworks), and the action's premise remains unverified. Option C weaponises a truth ("multiple causes") into analytical nihilism — multi-causality demands better analysis, not no conclusions. Option D rejects on political grounds, the worst reviewing habit. The senior contribution to post-incident work is exactly this: hold the narrative's counterfactuals to evidence, push causation past the first comfortable stop, and shape corrective actions that survive both scrutiny and the next deadline. Using defect patterns and trends to make recommendations requires the patterns to be genuinely established — post-incident reviews are where that discipline is most tested and most often lost.

**Question 12 (hard) — Reconciling a standard, a contract, and a practice**

Three texts bear on your area's supplier-delivered service. The organisational standard: "All user-facing changes must receive accessibility testing before production deployment." The supplier contract: "The supplier shall test all changes in accordance with the supplier's quality procedures, which the customer has reviewed and accepted. The customer may conduct additional testing at its discretion." The observed practice: the supplier's quality procedures, as documented, include accessibility checks only for changes the supplier classifies as "UI-substantial", and the last four minor UI changes were deployed without accessibility testing by either party. Which analysis is most accurate?

- A) The supplier is in breach of contract, and formal remedies should be pursued.
- B) There is no problem: the contract's acceptance of supplier procedures supersedes the organisational standard.
- C) A compliance gap exists, but its location matters: the supplier is likely operating within the contract (following its accepted procedures), while the organisation is failing its own standard — the standard demands accessibility testing of all user-facing changes, the accepted supplier procedures deliver less than that, and nobody is filling the gap with the "additional testing" the contract permits. The remedy is internal first: either exercise the discretionary testing right for non-substantial UI changes, or renegotiate the procedures — pursuing the supplier for breach would fail, because the gap was accepted at contract review.
- D) The observed practice is acceptable because minor UI changes rarely have accessibility impact.

**Correct answer: C**

**Explanation:** Reconcile the three texts by asking of each obligation: who holds it, to whom, and what exactly does it require? The standard binds the organisation — all user-facing changes, accessibility-tested before production. The contract binds the supplier — but only to its own accepted procedures, which carve out non-"UI-substantial" changes from accessibility checks; on the given facts the supplier is honouring precisely what was agreed, so option A's breach theory collapses at its first element (and pursuing it would spend relationship capital on a losing claim). Option B commits the inverse error: a contract governs the supplier relationship; it does not amend the organisation's own standard, which continues to bind the organisation's deployments regardless of who tested what — the standard's obligation does not evaporate because a contract assigned part of the work elsewhere. The gap is therefore structural: an internal standard promising more than the accepted supplier procedures deliver, with the contract's "additional testing at its discretion" clause sitting unused — the exact mechanism designed to fill such gaps. Option C locates the failure honestly (the gap was accepted at procedure review — an internal governance miss, and a lesson for future contract reviews: map supplier procedures against organisational standards clause by clause before acceptance) and sequences the remedy correctly: immediate mitigation through discretionary testing of minor UI changes, structural fix through procedure renegotiation at the next contractual opportunity. Option D substitutes a probabilistic hunch for both texts — and for government services, accessibility failures in "minor" changes (a colour contrast tweak, a focus-order regression) are routinely how real users get excluded, which is why the standard says "all". This is multi-document reconciliation as your role practises it: obligations mapped to their holders, gaps located rather than litigated, and remedies aimed where the leverage actually is.

### Preparation tips

- **Read for modality first.** "Probable cause", "intend to, subject to", "for awareness rather than formal notice", "may extend, before lapse" — the operative content of professional documents lives in their hedges, conditions and status markers. Train yourself to underline modality before content.
- **Map obligations to holders.** For every "must", "may" and "shall", note who is bound and to whom. Multi-document questions — and real governance — are solved by the map, not by any single text.
- **Practise counterfactual scepticism.** "Had we done X, Y would not have happened" appears in post-incident reviews, business cases and assessments alike. Reflexively ask: what evidence supports the counterfactual's hidden premise?
- **Draft the escalation grammar until it is automatic.** Facts, constraint, options, recommendation, decision deadline. Rewrite one of your recent escalations into this shape; the exercise improves both your writing and your eye for the clear-writing questions.
- **Use your expertise as a hypothesis generator, never as evidence.** Senior domain knowledge fills textual gaps silently. When you catch yourself "knowing" something the passage has not said, you have found exactly the reflex the test — and honest reporting — requires you to control.
- **Review a standard you own with fresh eyes.** Take a document you helped write and hunt for the interactions — deadlines-before-deadlines, foreclosed recoveries, undefined classifications like "UI-substantial". What you find will sharpen both your test performance and the standard.

### Common pitfalls to avoid

- **Expertise-driven gap-filling.** The senior reader's signature error: supplying from experience what the passage never stated. The more you know about how these situations usually go, the more vigilantly you must separate "usually" from "stated here".
- **Upgrading hedged claims.** "Probable" to "confirmed", "intend" to "will", "raised for awareness" to "formal notice" — each upgrade feels like reasonable compression and each changes the answer, the risk position, and what you owe your stakeholders.
- **Treating formal status as decoration.** Whether a communication is a notice, a finding, an intention or a marker is substance, not politeness. Contractual and audit correspondence is drafted in those distinctions deliberately.
- **Reading provisions in isolation.** Hard questions and real compliance failures live in interactions: the extension that must precede the lapse, the contract that satisfies itself while the standard goes unmet. Always ask what the clauses do to each other.
- **Accepting counterfactuals as findings.** "Would have been caught" is a hypothesis about coverage, not a fact about time. Post-incident narratives lean on such links; evaluation means testing them.
- **Blame-shaped drafting.** In clear-writing questions and real escalations, prose that assigns fault while requesting decisions scores — and lands — worse than prose that states facts and names choices. Write escalations the named team could read; you will be in the room with them next quarter.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace scenarios and asks you to judge the effectiveness of possible responses. For senior roles, the scenarios shift decisively from "what should I do?" to "what should I enable, influence, or protect?" — because at your level, most of what you accomplish happens through other people, other teams, and the standards and expectations you shape.

The typical format is an online assessment of 20 to 40 minutes with 10 to 20 scenarios, each offering four or five responses. Question styles include most-effective, least-effective, most-and-least, and full ranking or rating formats. Scoring compares your judgements against experienced professionals' consensus and the behaviours the organisation values: in UK government digital and data settings, user focus, honesty about problems, cross-team collaboration, ownership, proportionate escalation, inclusion, and developing others.

Senior SJT scenarios are constructed around the genuine tensions of your role, and it is worth naming them before you practise. Influence without authority: you guide teams you do not manage, and coordinate quality across an area whose delivery decisions belong to others — responses that assume command generally score poorly, as do responses that mistake the absence of authority for the absence of responsibility. Coaching versus rescuing: when the analysts you guide struggle or err, taking over fixes today and weakens tomorrow; the high-scoring pattern develops the person while protecting the service. Standards versus relationships: you hold lines — on evidence integrity, on escalation, on user protection — with stakeholders whose goodwill your area needs; effectiveness lies in holding the line without burning the bridge. Visibility of your own errors: senior mistakes propagate further and are easier to hide; the assessments probe whether your disclosure standards survive your own seniority. And expectation management with diverse senior stakeholders: much of your scenario terrain is conversations where the technically true answer must also be the usable one.

A calibration note: at senior level, "most effective" rarely means the boldest or the most procedurally correct response. It usually means the response that gets the substantive problem solved, keeps decision rights where they belong, leaves relationships and reporting culture stronger, and develops someone where development is available. Read every option asking not "is this right?" but "what does this leave behind?"

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Coaching and developing others** maps to **Test analysis** ("coach others in test analysis") and **Designing and executing tests** ("lead others in designing, building, maintaining and executing tests"): scenarios probe whether you build capability or dependency when the people you guide struggle.
- **Cross-team influence and escalation** maps to **Managing, reporting and resolving defects** ("manage and escalate dependencies, defects and risks across teams") and your duty to communicate chosen approaches and outcomes to stakeholders: the scenarios test escalation timing, routing, and the difference between raising a risk and dumping one.
- **Expectation management under pressure** maps to **Communicating between the technical and non-technical** ("listen to and interpret the needs of technical and non-technical stakeholders, and manage their expectations"; "support or host difficult discussions within the team or with diverse senior stakeholders"): several scenarios turn on what you say, to whom, and when, during defect resolution and release pressure.
- **Standards stewardship** maps to your duty to contribute to, and enable others to follow, quality assurance and testing standards: scenarios test whether you apply standards with judgement — neither waiving them quietly nor wielding them rigidly.
- **Early risk advocacy** maps to **Test analysis** ("ensure test needs are implemented early") and **Test and quality planning** ("advocate for full team ownership of quality testing activities, encouraging early engagement"): the recurring theme of intervening upstream, before positions harden and options close.
- **Improvement leadership** maps to **Test and quality planning** ("implement ways to capture data to drive continuous improvement") and **Designing and executing tests** ("improve test types and techniques through a structured process"): scenarios reward evidence-led, consent-based change over both mandate and drift.

### Practice questions

**Question 1 (easy) — An analyst you coach wants you to fix it**

An analyst you coach messages you an hour before their team's triage meeting: "The developers are going to challenge my severity rating on the search defect again. Can you join and back me up? They listen to you." You have the hour free, and you know from experience the developers will indeed defer to you. What is the most effective response?

- A) Join the triage and argue the severity case yourself — the rating is probably right and your presence settles it fastest.
- B) Decline to attend, telling the analyst they need to learn to handle triage alone.
- C) Spend twenty minutes now helping them build their case — impact evidence, affected user volumes, the severity definitions — and rehearse the challenge they expect; let them run the triage themselves, and debrief with them afterwards.
- D) Contact the developers before triage and tell them to stop challenging severity ratings.

**Correct answer: C**

**Explanation:** The request contains its own diagnosis: "they listen to you" means the analyst is borrowing your authority instead of building their own, and every borrowing deepens the dependency. Option C converts the hour into capability: case-building (evidence, definitions, user impact) is the transferable skill; rehearsing the expected challenge converts anxiety into preparation; and the debrief closes the coaching loop. Crucially, the analyst walks into the room as the severity's owner — and when they win the argument themselves, the developers' future challenges will route to a person who has demonstrated they can meet them. Option A wins today's triage and guarantees next month's identical message; it also quietly teaches the developers that severity ratings are really negotiated at your level, undermining the analyst's standing in every future meeting you skip. Option B has the right destination and no bridge — coaching is not refusal; it is scaffolded withdrawal, and the scaffold is the twenty minutes option C spends. Option D protects the analyst by suppressing legitimate challenge: developers should test severity reasoning, and a triage where ratings go unchallenged is quality theatre. Your named skill is coaching others in test analysis; this is what it looks like under time pressure — invest in the person before the moment, stay out of the moment, learn from the moment together.

**Question 2 (easy) — A team wants to skip your area's standard "just this once"**

A delivery manager from a team in your area calls: "We need to release Thursday, and the defect management standard's verification step — discovering team retests before closure — will cost us a day we don't have. Can we skip it just this once? The fixes are simple." What is the most effective response?

- A) Agree — flexibility on process builds relationship capital for when it matters.
- B) Refuse flatly — standards are standards.
- C) Engage the substance: ask which defects are affected and what the fixes touch; if the risk genuinely is low, help them find a compliant faster path — timeboxed verification prioritised by severity, or pairing tester and developer to verify at merge — and if the day genuinely cannot be found, route the exception explicitly: the standard's owner and the release decision-maker accept the unverified-closure risk on the record, not in a phone call.
- D) Tell them to raise it with the head of profession.

**Correct answer: C**

**Explanation:** "Just this once" phone calls are how standards actually die — not by decision but by accumulated quiet exceptions, each individually reasonable, collectively establishing that the standard binds only when convenient. But option B's flat refusal fails differently: it treats the standard as self-justifying, learns nothing about the actual risk, and teaches the area that the QA function is an obstacle to route around rather than a partner to consult — the next team simply won't call. Option C does what senior standards stewardship actually requires: it engages the specific risk (which defects? what do the fixes touch?), it works the problem (verification can often be compressed legitimately — severity-prioritised timeboxing and verify-at-merge pairing are real techniques, and offering them converts you from gatekeeper to problem-solver), and where the exception truly is needed, it moves the decision into the light: recorded, owned by the people who own the risk. That last step is the load-bearing one — an exception granted informally by you becomes your personal waiver of a standard you do not own alone; an exception recorded and risk-accepted is governance functioning. Option A purchases relationship warmth with the standard's credibility, an asset you hold in trust for the area. Option D escalates what engagement could resolve, spending senior attention on a question you are equipped to shape. Enabling others to follow standards — your named duty — includes making the compliant path as fast as it can honestly be, and making the exception path honest when it must exist.

**Question 3 (easy) — Credit for your analyst's work**

At a programme showcase, a delivery manager presents your area's halved escape rate as "the delivery team's quality push", with no mention of the analyst you coach who designed and drove the risk-based approach behind it. The analyst is present and visibly deflated. What is the most effective response?

- A) Interrupt the presentation to correct the record.
- B) Say nothing — outcomes matter, credit doesn't.
- C) In the open questions, add context appreciatively: "Worth adding that the risk-based approach behind this was designed by [analyst] — happy to share the method with other teams." Then, separately, mention the analyst's contribution to their line manager and encourage the analyst to write it up for the community of practice.
- D) Complain to the delivery manager afterwards about credit-taking.

**Correct answer: C**

**Explanation:** Three interests need serving: the analyst's recognition and morale, the accuracy of the organisational record (misattributed successes distort future resourcing — if "the delivery push" did it, why fund QA capability?), and the relationship with a delivery manager who may have compressed rather than stolen. Option C serves all three with the lightest touch: the correction is public but appreciative, framed as adding value ("happy to share the method") rather than claiming turf; the line-manager mention converts a showcase moment into performance-review evidence, which outlasts applause; and the community write-up turns the analyst's work into visible professional identity — the deepest form of credit. Option A wins the point and loses the room: interruptions convert attribution errors into public confrontations, and the analyst becomes the cause of an awkward scene rather than the author of a method. Option B is half-true and fully corrosive: outcomes do matter, and credit is how organisations decide who to develop, fund and promote — a senior who lets coached analysts' work vanish into others' slides will coach increasingly guarded analysts. Option D addresses the past privately while leaving the public record wrong and the analyst unrestored. The senior pattern: developing others includes being the person who makes their work visible — advocacy is not vanity management; it is capability retention.

**Question 4 (moderate) — Discovering an analyst's shortcut**

Reviewing a team's release evidence, you find that an experienced analyst you guide has marked forty regression tests "passed" with identical timestamps two minutes apart — almost certainly bulk-marked without execution. The release shipped a week ago; no incidents so far. The analyst is capable, well-liked, and currently carrying a heavy workload. What is the most effective response?

- A) Report it to their line manager immediately as a conduct issue.
- B) Speak with the analyst directly and privately first: show what you found, ask for their account, and make the substance non-negotiable — the affected coverage gets verified now against production, and the false records are corrected with an honest note. Then address the conditions (workload, deadline pressure) and the seriousness: this cannot recur, and if their account doesn't hold or it happens again, it becomes a formal matter.
- C) Quietly re-run the forty tests yourself and say nothing — the analyst is overloaded and no harm has resulted.
- D) Raise it at the area's community meeting as an anonymised example of bad practice.

**Correct answer: B**

**Explanation:** Hold two truths simultaneously: falsified test records are among the most serious professional breaches in quality assurance — the entire value of testing is that its records are true — and the response that best protects the record's integrity long-term is the one that starts with a direct, private conversation rather than a formal detonation. Option B sequences correctly. Substance first: production exposure is live (forty unverified tests, a week shipped), so verification happens now regardless of anyone's feelings, and the records are corrected honestly — the evidence trail must end true. Account second: "almost certainly" is not certainly; perhaps a tooling migration bulk-updated statuses, perhaps the tests ran elsewhere — asking first is both fair and diagnostic, because how they answer tells you what you are dealing with. Conditions third: overload does not excuse falsification, but it predicts recurrence in others, and a senior who fixes only the person leaves the pressure that will produce the next case. Boundary last and explicit: this conversation is the alternative to formality only once. Option A may eventually be right, but as the first move it forfeits the information the direct conversation yields and converts a possibly-recoverable professional into a defended case. Option C is the worst answer wearing kindness: it completes the cover-up, makes you co-author of false records, and teaches nothing to anyone — the analyst doesn't even learn they were caught. Option D humiliates by anonymity that won't hold (the team will decode it) while never actually resolving the exposure. Guiding others in quality assurance includes this: the standard is absolute, the first response is human, and the two are not in tension — they are the sequence.

**Question 5 (moderate) — Your risk assessment is being reframed upward**

You provided the programme board a written assessment: "Payments migration testing is complete for standard cases; concurrency testing under peak load could not be completed because the performance environment lacks production-scale data — residual risk: unquantified behaviour under month-end peak volumes." You learn the programme director's board slide renders this as: "QA confirms payments migration tested successfully; minor environment caveats noted." The board meets tomorrow morning. What is the most effective response?

- A) Let it go — directors summarise, and the caveat is technically mentioned.
- B) Contact the programme director today: state specifically that the slide's rendering materially changes your assessment — "tested successfully" plus "minor caveats" does not communicate an unquantified peak-load risk in a payments system — and provide replacement wording at slide length: "Standard-case testing complete; peak-load behaviour unverified due to environment limits; risk window is month-end." If the slide goes forward unchanged, tell the director you will need to state the assessment accurately when the board discusses it.
- C) Email your accurate assessment directly to all board members tonight.
- D) Attend the board and contradict the slide when it is presented.

**Correct answer: B**

**Explanation:** The scenario's engine is the gap between technical truth ("caveats noted") and communicated truth: the slide's impression — success with footnotes — will drive a different board decision than your assessment — unverified behaviour under the exact conditions (month-end peaks) where payment systems break. Impression management of this kind is how governance fails while every document stays technically defensible; your written assessment protects you, but the assessment exists to protect the service, and it is about to be neutralised. Option B intervenes at the right point with the right tools: today, not mid-board; with the specific materiality argument (why this rendering changes the decision), not a general complaint about summarising; with usable replacement wording at slide length — the senior move that makes accuracy easy to adopt, because directors compress for real reasons and your 25-word version solves their problem and yours; and with an honest, non-threatening statement of what happens otherwise — you will answer accurately in the room, said in advance so it is predictable professional consistency rather than ambush. Option A rationalises: "technically mentioned" is the standard you hold others' slides to failing. Option C routes around the director pre-emptively, converting a correctable drafting issue into a trust breach that will define the relationship — the direct conversation has not even been attempted. Option D chooses the maximally public correction after declining the private one, spending both the director's standing and the board's confidence in programme coherence. Managing expectations of diverse senior stakeholders — your named skill — is precisely this: the truth, delivered upstream of the decision, in the format power actually uses.

**Question 6 (moderate) — Least effective: two teams' defect standoff**

A defect sits unresolved for three weeks: Team F says the fault is in Team G's API; Team G's analysis says F's service calls it incorrectly; each has "proved" the other responsible, users are intermittently affected, and both teams' delivery managers have stopped engaging. As the area's senior analyst, which response is **least** effective?

- A) Convene a joint working session with both teams' engineers and analysts: reproduce the failure together against the actual contract documentation, with the goal framed as "find the fix" not "find the culprit".
- B) Add the defect to your area's risk log with both teams' positions documented, and escalate jointly to both delivery managers that user impact continues while attribution is debated.
- C) Review both teams' evidence yourself and issue a written determination of which team is responsible, copied to both delivery managers.
- D) Propose the teams jointly fund a temporary mitigation (retry logic) while root cause is pursued, decoupling user protection from the attribution question.

**Correct answer: C**

**Explanation:** Rank what each response leaves behind. Option A attacks the actual failure condition: three weeks of positional analysis means each team has been proving its own innocence against its own reading of the contract — joint reproduction against the documented contract is the classic resolution because interface defects usually live in the contract's ambiguity, which neither side can see from inside its own assumptions; "find the fix" framing lets both teams stand down from their trenches. Option D is the underrated senior move: user impact and root cause are separable problems, and mitigation-first sequencing protects citizens while removing the urgency that makes attribution arguments bitter. Option B is legitimate governance: documented positions and joint escalation re-engage the managers who have disengaged, without taking sides. Option C is least effective, and the reasons compound: you likely lack the evidence to adjudicate correctly (three weeks of contradictory "proof" means the truth needs reproduction, not review); a written verdict converts you from the area's trusted broker into a party — the "losing" team will now relitigate against your determination, adding a third front to the dispute; it resolves attribution (maybe, wrongly) while fixing nothing for users; and it spends your cross-team standing — the asset your dependency-management role runs on — on a question (blame) whose answer helps nobody ship a fix. The deep senior principle: in cross-team conflict, your power is convening power, and issuing verdicts is how conveners demote themselves to combatants. Managing and escalating dependencies, defects and risks across teams means exactly the A/D/B toolkit — reproduce jointly, mitigate immediately, escalate transparently — and almost never the gavel.

**Question 7 (moderate) — The retro-fitted test evidence request**

A delivery manager asks you, late Friday: "The audit needs evidence that accessibility testing happened for the March release. We know it happened — Dev did it informally — but nothing was documented. Can your team write up the test evidence this weekend, dated appropriately, so the file is complete?" What is the most effective response?

- A) Decline the dating but offer the honest equivalent: document now, dated now, what can be established about March — who tested what, findings, any contemporaneous artefacts (messages, tickets, screenshots) — clearly labelled as retrospective reconstruction; and tell the audit the truth: testing occurred informally, contemporaneous documentation was not made, corrective process now in place.
- B) Write the evidence as requested — the testing genuinely happened, so the documents merely record truth.
- C) Refuse and report the delivery manager to the audit team for attempted falsification.
- D) Decline involvement entirely and let the delivery manager handle the audit as they see fit.

**Correct answer: A**

**Explanation:** Separate the three things the request bundles: a true fact (testing apparently occurred), a real problem (no contemporaneous record), and a falsification (documents "dated appropriately" — i.e., backdated to simulate contemporaneous evidence). Option B's seduction is the true fact: "merely recording truth" — but backdated documents assert a second claim beyond their content, namely when they were created, and that claim would be false in documents whose entire audit function is contemporaneity. If the informal testing is later questioned, fabricated-date evidence converts a documentation gap into an integrity finding that engulfs every record your area has ever produced — audit trust, once lost, is lost wholesale. Option A gives the delivery manager everything honesty can give, which is more than they expect: retrospective reconstruction is a legitimate audit artefact when labelled as such; contemporaneous fragments (chat messages, tickets) often substantiate more than people assume; and "gap found, practice corrected" is a finding auditors process routinely — organisations survive documentation gaps; they are damaged by fabrication discovered. Option C leaps to reporting a request that a firm, helpful decline resolves — the delivery manager under audit pressure asked a bad question; they have not yet done a bad thing, and converting them into a case forecloses the honest path option A opens. Option D washes your hands while leaving the falsification option live on the table — silence from the area's senior quality figure reads as licence. The senior line: your area's records are trustworthy precisely because there is no price at which they are adjusted, and the way you hold that line — offering the honest alternative rather than only the refusal — determines whether people keep bringing you their pressures or start routing around you.

**Question 8 (moderate) — Introducing improvement to a resistant senior peer**

You want your area's teams to adopt contract testing for their service integrations — the escape data clearly supports it. The most influential team's lead engineer, a senior peer with deep organisational tenure, dismissed it at the community meeting: "We tried consumer contracts in 2019; it was overhead with no payoff. Our integration tests cover this." Several teams will follow his lead. What is the most effective response?

- A) Roll it out via the teams that are willing, and let his team's escape metrics make the argument eventually.
- B) Ask him for an hour: start with what happened in 2019 — the specifics of why it failed — and with what his integration tests do catch; then look together at the recent boundary escapes and whether today's tooling addresses the 2019 failure modes. If he engages, propose a bounded pilot on one troublesome interface, designed jointly, with his named concerns as the evaluation criteria.
- C) Present the escape data at the next community meeting with a direct rebuttal of his position.
- D) Ask the head of profession to mandate contract testing area-wide.

**Correct answer: B**

**Explanation:** Read the resistance accurately before choosing tools: this is not obstruction — it is evidence-based scepticism from someone who paid adoption costs once and got nothing back, and "we tried it in 2019" is data you do not have. Option B treats it accordingly, and each element earns its place: asking about 2019 first is both genuine inquiry (2019-era contract tooling was harder to operate; his failure modes may be exactly what current practice fixed — or may reveal a local constraint still true) and the only opening that does not require him to have been wrong; examining what his integration tests do catch respects the existing investment and locates the actual gap rather than asserting it; the boundary-escape data enters as a shared puzzle, not a prosecution exhibit; and the pilot design — bounded, joint, evaluated against his named concerns — converts the area's most credible sceptic into the experiment's co-author, which means whichever way the pilot goes, the area learns something it will believe. That is the deep mechanic: his influence is not an obstacle to route around but the distribution channel — persuade the sceptic and adoption is free. Option A cedes the most influential team and consigns the improvement to permanent minority practice while waiting for escape metrics to embarrass a senior peer — a strategy that reads as passive and lands as hostile when noticed. Option C wins the meeting and loses the man: public rebuttal of tenured expertise entrenches the very following you need to move. Option D spends profession-level authority to force what influence hasn't earned — mandated practices without local conviction get implemented as compliance theatre, the 2019 experience repeats itself by self-fulfilment, and you have taught the area that your improvements arrive by decree. Improving test types and techniques through a structured process — your named skill — is at senior level mostly this: the structure is social before it is technical.

**Question 9 (hard) — The finding that implicates your own earlier guidance**

Eighteen months ago you designed the risk-based regression approach your area's teams now follow, and you have coached it into three teams. Analysing this quarter's escapes, you find a pattern: a rising share of escaped defects fall in a category your approach explicitly deprioritises — cross-service data consistency checks — because your original risk model assumed service boundaries would remain stable, and they have not: the area has decomposed two services since. The approach bearing your name is now systematically under-testing a growing risk class. What is the most effective response?

- A) Adjust your coaching quietly, steering teams toward consistency checks without flagging the model's obsolescence — the correction happens without unsettling confidence in the approach.
- B) Bring the analysis to the area openly, exactly as you would for anyone's approach: here is the escape pattern, here is why — the model's boundary-stability assumption expired when the decompositions began — here is the proposed revision, and here is the meta-lesson worth institutionalising: risk models carry assumptions with expiry conditions, and ours now get review triggers tied to architectural change.
- C) Commission one of the analysts you coach to "independently review" the approach, positioning the correction as their finding.
- D) Present the escape pattern as caused by the service decompositions, recommending teams increase consistency testing, without connecting it to the approach's design.

**Correct answer: B**

**Explanation:** The scenario tests whether your analytical integrity survives its collision with your own authorship — and the options are a spectrum of self-protection dressed in increasingly good taste. Option B is what you would demand of any team whose approach your analysis implicated, applied to yourself without discount: the pattern named, the causal mechanism named (an assumption, reasonable when made, expired by architectural change — note this framing is both true and survivable: the model wasn't wrong; it aged), the revision proposed, and — the genuinely senior move — the failure converted into institutional capability: review triggers tying risk models to architectural change mean the area now catches expiring assumptions systematically, including in models you didn't write. Publicly revising your own approach on evidence is also the highest-leverage coaching act available to you: every analyst watching learns that in this area, the analysis outranks the author — which is the culture that makes their future honest findings speak-able. Option A corrects the testing while preserving the myth, leaving three teams following a model whose written form still misleads anyone who consults it — and quiet steering cannot scale to teams you don't personally coach. Option C is the subtle disgrace: manufacturing an "independent" finding launders your correction through a junior colleague's name — it spends their integrity to protect your image, inverts the mentorship relationship, and if detected (juniors talk), costs you precisely the credibility it was built to protect. Option D is technically-true deception: the decompositions did drive the risk, but the recommendation floats causeless, the approach's written deprioritisation stands uncorrected, and the area learns nothing about why its testing missed a shift its senior analyst's model had ruled out. Using insights to improve quality assurance processes — your role's definition — includes, hardest of all, the insights that improve your own.

**Question 10 (hard) — Most and least effective: the pre-emptied escalation**

You escalated in writing to your head of delivery: Team H's practice of merging without code review or test evidence — under sustained deadline pressure — has produced three near-miss incidents this quarter, and you recommended a delivery-pause conversation. Before any response, Team H's delivery manager corners you, furious: "You went over my head. We handle our own quality. Withdraw the escalation or our teams stop sharing defect data with your area reviews." Consider these responses:

1. Withdraw the escalation to preserve the working relationship, and pursue the concerns informally with Team H.
2. Hold the escalation, and engage the delivery manager directly on both fronts: acknowledge you should have told them the escalation was going in (if you hadn't) and repair that; but be clear the escalation stands because the pattern is a service risk, not a team insult — offer to walk them through the near-miss evidence, and to jointly own the remediation proposal so the fix arrives with their fingerprints on it. Separately, name the data-sharing threat calmly for what it is: withholding defect data harms the service's users, and you will treat it as its own escalation if it happens.
3. Report the delivery manager's threat immediately to the head of delivery as attempted coercion, appending it to the original escalation.
4. Hold the escalation but avoid the delivery manager until the head of delivery responds.

Which is the most effective response, and which is the least effective?

- A) Most: 2; Least: 1
- B) Most: 2; Least: 4
- C) Most: 3; Least: 1
- D) Most: 1; Least: 3

**Correct answer: A**

**Explanation:** Work the candidates. Response 2 is most effective because it decomposes a compound situation correctly: the relationship grievance may be partially legitimate (escalating without notifying the affected manager is a genuine process foul — if you committed it, owning it costs nothing and disarms much); the escalation's substance is non-negotiable because it was never about the manager — three near-misses from unreviewed, untested merges is a service risk trajectory, and withdrawing it under pressure would establish that your escalations are retractable by intimidation, a fact that would follow every future escalation you write; the joint-remediation offer gives the manager a dignified path from opposition to ownership; and the threat is handled with precise calibration — named, consequenced, but given room to be retracted in anger's cooling, rather than instantly criminalised. Response 1 is least effective, and specifically worse than the imperfect others: it converts coercion into a proven strategy (the manager has now learned exactly how to neutralise QA findings), abandons a documented risk trajectory to informal channels that three near-misses have already shown insufficient, and — the subtle cost — betrays the analysts whose evidence built the escalation, who will note that senior backing dissolves under pressure. Response 3 is premature but not baseless: the threat is real misconduct if executed, yet escalating it within the hour forecloses the far better outcome response 2 reaches — a heated manager talked back into partnership — and stacks a people-conflict onto a practice-conflict, ensuring both harden. Response 4 holds the line while abandoning the field: the escalation survives but the relationship rots unattended, the manager's narrative ("QA ambushed us") consolidates uncontested, and avoidance from the area's senior quality figure reads as either fear or contempt. The senior principles in ranked order: substance held under pressure; relationship repaired in parallel, not in exchange; threats named without being detonated; and escalations that end, wherever possible, with the escalated party co-owning the fix. That is supporting difficult discussions with diverse stakeholders — your named skill — practised at its hardest setting: when the difficulty is aimed at you.

**Question 11 (hard) — Capability gap surfaced by your own success**

Your coaching has made one analyst, Nadia, exceptional: she now leads the area's hardest test analysis, other teams request her, and her team's quality metrics are the area's best. Her delivery manager privately tells you they are structuring the team's entire quality function around her — no second analyst, no documentation of her methods, "because Nadia handles it". Nadia, separately, tells you she is applying for a lead role elsewhere in the organisation and asks you to keep it confidential until she decides. What is the most effective response?

- A) Honour the confidence completely and do nothing else — Nadia's career comes first, and the team's structure is the delivery manager's business.
- B) Tell the delivery manager about Nadia's application — they need to know before structuring everything around her.
- C) Keep Nadia's confidence strictly, and act on what you may freely act on: advise the delivery manager — on general resilience grounds you'd raise anywhere — that single-person quality functions are a critical dependency risk regardless of the person, recommending a second analyst and method documentation now; support Nadia's application as her coach; and accelerate the capability spread you should be driving anyway — get her methods into the community of practice, with her named as their author.
- D) Discourage Nadia from applying until the team's resilience improves — she owes the team a transition.

**Correct answer: C**

**Explanation:** The scenario braids three legitimate duties — confidentiality to a coachee, resilience stewardship for the area, and development advocacy for a person you coach — and tests whether you can honour all three without leaking any across the others. Option C's insight is that the resilience argument requires no confidential information: "your quality function is one resignation, one illness, one promotion away from collapse" is true of every single-person dependency everywhere, is standard senior advice you would owe this delivery manager if Nadia had never spoken to you, and — properly made on general grounds — is indistinguishable from routine counsel. The confidence stays sealed; the team gets protected anyway. Meanwhile the coaching duty points one direction only: a coach who develops people and then impedes their advancement (option D) has converted development into extraction — "she owes the team" inverts the actual debt, and analysts watching how you handle Nadia's rise will calibrate their own honesty with you accordingly. The method-documentation push does triple work: area capability spreads (your improvement duty), Nadia's authorship becomes portable reputation (her interests), and the team's dependency shrinks (their interest) — all before any resignation letter exists. Option B is the straightforward betrayal: it solves the delivery manager's problem with Nadia's confidence, and the news will reach her — coaching relationships across your area run on the credibility you would be spending. Option A treats confidentiality as licence for total passivity, letting a foreseeable, addressable structural risk ride toward the area you are responsible for — the confidence constrains what you may say, not what you may responsibly do. The senior discipline: when duties appear to conflict, decompose them — most conflicts dissolve once you locate the action each duty actually requires, and the actions rarely overlap as much as the anxieties do.

**Question 12 (hard) — The quiet quality decline you can see coming**

Programme leadership announces that to hit a statutory deadline nine months out, all four of your area's teams will move to monthly releases (from fortnightly... to weekly for the final three months), with a hiring freeze in effect. Your analysis of the area's current capacity is unambiguous: at weekly cadence with current staffing and automation levels, regression coverage will fall below the risk threshold for two teams, and the area's exploratory testing — which found 60% of last year's high-severity defects — will effectively cease. Nobody has asked for your assessment. What is the most effective response?

- A) Wait until asked — volunteering capacity concerns about a statutory deadline reads as obstruction, and the problems are seven months away.
- B) Produce the assessment now, unrequested, and frame it as delivery enablement: here is the quantified gap between the announced cadence and current quality capacity; here are the options that close it, costed and sequenced — automation investment in the next two months while cadence is still monthly, risk-threshold adjustments with explicit acceptance, cross-team test sharing, contractor cover within the freeze's exceptions; here is what each option buys, and here is the decision timeline — the enabling investments only work if started before the cadence increases. Take it to your head of profession and the programme's delivery leadership together, positioned as "how testing meets the deadline", not "why the deadline is a problem".
- C) Raise the concern verbally at the next area meeting so it is on record, and let programme leadership weigh it.
- D) Begin quietly optimising what you control — automation, test sharing — without a formal assessment, since leadership has signalled the deadline outranks quality concerns.

**Correct answer: B**

**Explanation:** The scenario's trap is its framing: "nobody has asked" — and the senior answer is that ensuring test needs are implemented early, your named duty, is precisely the mandate to speak before being asked, because the decision that determines month nine's quality is being made now, in month zero, by people who cannot see the capacity arithmetic you can. Option B's construction deserves study element by element. Timing: the enabling options (automation built during the monthly-cadence months, contractor exceptions, shared test infrastructure) have lead times — they exist as options only if the assessment arrives before the cadence rises; month seven's version of this document is a post-mortem draft. Framing: "how testing meets the deadline" is not spin — it is the accurate description of an assessment whose content is options rather than objections, and it determines whether the analysis is received as engineering or as resistance; statutory deadlines will not move, so the assessment that survives is the one that takes the deadline as fixed and solves within it. Quantification: "coverage falls below threshold for two teams" and "60% of high-severity finds cease" convert a mood ("we'll be stretched") into decision-grade facts with named consequences. Routing: head of profession plus delivery leadership jointly, because the options span both authorities — and going jointly means neither hears it second-hand. Explicit risk acceptance for whatever gap remains: if leadership chooses thinner coverage, that choice should exist on paper, owned — which is also what protects your teams when month nine's escapes are audited. Option A optimises for comfort against a foreseeable, quantified service risk — "reads as obstruction" is managed by framing, not by silence. Option C discharges conscience, not duty: a verbal mention creates deniable awareness, changes no resourcing, and starts no two-month automation build. Option D does real good at one-tenth scale while leaving the decision-makers uninformed — quiet optimisation inside a structurally impossible envelope is how conscientious areas arrive exhausted at failures leadership never knew were predicted. This is the role at full height: the senior analyst is the person who makes the quality consequences of delivery decisions visible before the decisions harden — invited or not, quantified, optioned, and aimed at the people who can still choose.

### Preparation tips

- **Rehearse the influence toolkit consciously.** Convene, reproduce jointly, pilot with sceptics as co-designers, offer replacement wording, joint escalation — senior scenarios reward specific influence mechanics over generic assertiveness. Name the tools as you practise so they surface under time pressure.
- **Check every response for what it teaches observers.** Analysts, teams and stakeholders learn your area's real standards from what you do in scenarios exactly like these. An option that solves today while teaching the wrong lesson — that escalations retract under threat, that records adjust under pressure — is rarely the scored answer.
- **Separate the substance from the relationship in every conflict scenario.** The high-scoring options almost always hold the substantive line while actively repairing or preserving the relationship — in parallel, never in exchange.
- **Apply your standards to yourself first.** Scenarios probing your own errors, your own approaches, your own credit are calibrated exactly like the others; the answer you would demand of a coached analyst is the answer for you. Practise noticing when authorship is biasing your option-ranking.
- **Sequence before selecting.** Many senior options contain the right actions in the wrong order — verdict before conversation, escalation before engagement, formality before inquiry. Check the sequence: private before public, substance secured before conditions addressed, options before mandates.
- **Ask "who owns this decision?" in every scenario.** Senior effectiveness lives in maximising the quality of decisions you do not own. Options that quietly assume ownership you lack — or shed responsibility you hold — are the two symmetric traps.

### Common pitfalls to avoid

- **Rescuing instead of coaching.** Taking the triage, fixing the tests, winning the argument for your analysts — every rescue is a small theft of their development and a large addition to your permanent workload. The scored options build the person.
- **Issuing verdicts from a broker's chair.** Adjudicating cross-team blame, rebutting sceptics publicly, determining fault in writing — the moment you rule, you stop convening. Your cross-team power is almost entirely the power to convene honestly.
- **Trading record integrity for anything.** Backdated evidence, softened assessments, withdrawn escalations, quiet corrections — the scenarios price these temptations attractively because reality does. The area's records and your word are the same asset; no exchange rate is acceptable.
- **Letting confidentiality justify passivity.** A confidence constrains disclosure, not action. When you cannot say, ask what you may still responsibly do — usually more than the paralysed option assumes.
- **Waiting to be asked.** Senior risk advocacy is pre-emptive by definition: the capacity assessment, the expiring assumption, the pre-board correction all matter only before the decision. "Nobody asked" is the pitfall's name, not a defence.
- **Winning encounters while losing cultures.** Public rebuttals, immediate formal reports, mandates from above — each wins its moment and degrades the openness, data-sharing and honest reporting your area's quality actually runs on. Score options by what remains after the encounter: the relationships, the norms, and what the next person in that situation will now do.

## Conclusion

You have worked through a demanding programme of practice — and if you engaged with it honestly, you will have noticed that very little of it was really about assessments.

Recap what you covered. The **cognitive assessment** section exercised the systemic reasoning your coordination role runs on: reading inverted patterns in cross-team defect data, holding governance conjunctions firm under persuasive pressure, checking approach documents for the conflicts that live in their joins, tracing dependency chains to their currently binding link, diagnosing mis-aimed quality systems without blaming the people inside them, and projecting a cosmetic Phase 1 symptom into its Phase 3 consequences. The **numeric reasoning** section drilled the quantitative honesty your recommendations depend on: aggregates rebuilt from raw counts, percentage points kept distinct from percentages, stocks separated from flows, vendor claims normalised before attribution, small counts respected for the noise they carry, and composite figures published with the specific risks they conceal named alongside. The **verbal reasoning** section sharpened the reading your standards work propagates: modality and attribution held at their written strength, provisions read for their interactions, counterfactuals in post-incident narratives tested rather than inherited, and escalations drafted in the grammar — facts, constraint, options, recommendation, deadline — that senior decisions actually consume. And the **situational judgement** section walked the contested ground where senior effectiveness is really decided: coaching instead of rescuing, convening instead of adjudicating, holding escalations under threat while repairing the relationships around them, revising your own celebrated approach in public, and producing the capacity assessment nobody asked for while it can still change the decision.

The pattern across all four sections is the one worth carrying: at your level, technique and integrity have merged. The denominator you check, the qualifier you refuse to soften, the assumption you flag as expired, the credit you route to its author — these are simultaneously the behaviours that score in assessments and the behaviours that make an area's quality culture real. There is no seniority-level trick to learn; there is only the discipline you already practise, made explicit and applied without exemption — including to yourself.

That last clause is the genuinely senior frontier, and this guide has pressed on it deliberately: your own approaches will age, your own records will contain errors, your own guidance will sometimes be the system's weak point. The professionals worth guiding are the ones who can see that clearly and act on it publicly — because everything else you teach, you teach by demonstration.

Return to these sections before any real assessment, and return to them occasionally regardless: the scenarios will read differently as your area hands you their real-world equivalents. Share the questions with the analysts you coach — working through them together is coaching, of exactly the kind your role names.

You carry significant responsibility, and you carry it through influence, evidence and example rather than authority. That is the hardest way to carry anything, and the most durable. Good luck — with the assessments, and with the more important work they rehearse.
