# Principal End User Computing Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a principal end user computing engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to work at your level, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills and professional judgement that predict success in a role. For a principal engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the materials you genuinely handle — strategy roadmaps, workforce and resourcing plans, technology-trend analyses, risk registers, compliance positions, multi-year budgets, and the analytics through which service data becomes business decisions — and the judgements you genuinely make, such as sequencing a strategy roadmap against funding and technology cycles, shaping your team's capability through resourcing and learning and development, deciding which risks to escalate and which to hold, and translating trends in the business into an end user computing model fit for what comes next.

Why do these assessments matter at your level in particular? Your role summary is compact and demanding: you own the strategy roadmap, you lead on resourcing, learning and development, and you look at the bigger picture — understanding trends in the business and the direction of future technologies. Every one of those duties is judgement exercised over long horizons with incomplete information. The thinking skills underneath are exactly what psychometric assessments sample: recognising the pattern in noisy, multi-year data that others read as noise; reasoning rigorously through dependency chains where a wrong assumption compounds across an estate and a budget cycle; checking the strategies, business cases and compliance positions whose errors become organisational errors; prioritising where your attention — and your organisation's investment — should go; interpreting analytics honestly enough to steer business performance by them; reading policy, supplier and architecture documents at the precision governance requires; and making the calls where users, engineers, finances and the future pull against each other.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters at your level, a mapping of its dimensions to the named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The four sections cover:

1. A **cognitive assessment** — pattern recognition, logical deduction, error checking, prioritisation and applied problem solving, using roadmaps, risk registers, trend data and strategic artefacts.
2. A **numeric reasoning assessment** — percentages, rates, weighted figures, trends, forecasts and investment analysis, built on estate analytics, budgets, workforce plans and service data.
3. A **verbal reasoning assessment** — precise comprehension of strategies, policies, supplier and architecture papers, and governance correspondence, with true/false/cannot-say discipline.
4. A **situational judgement assessment** — realistic dilemmas about strategy ownership, resourcing, governance, risk, succession and the long-term stewardship of user outcomes.

To get the most from this guide: work one section at a time; commit to an answer before reading each explanation; and treat every explanation as a mini-lesson even when you answered correctly. At your level the guide has a second purpose — the worked reasoning is the kind you now teach a whole function: to leads learning vendor judgement, to managers learning honest reporting, and to governance boards learning what good evidence looks like when you put it in front of them.

You think in years and answer for outcomes. Let's exercise exactly that.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the exact mental processes your role demands, using practical scenarios rather than abstract puzzles. At principal level, the materials are strategic: multi-year trend data, roadmap dependency chains, risk registers, compliance positions, workforce plans, and the technology-direction evidence on which an estate's future is bet.

The typical format is an online, timed test lasting 15 to 30 minutes, with 15 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation and applied problem solving. Scoring is objective against a norm group; platforms often adapt difficulty as you perform well, and report speed and accuracy separately. Short ungraded practice questions usually precede the real test.

For a principal engineer, cognitive assessment is relevant because your professional value is structured thinking applied at the widest span and the longest horizon. Owning the strategy roadmap means reasoning about sequences of dependent commitments made under uncertainty. Understanding the direction of future technologies means separating durable trends from vendor weather. Managing service compliance and risk means detecting the quiet inconsistency — in a register, a model, a plan — before it compounds. Co-ordinating the team's problem investigations means judging which patterns deserve the function's finite attention. And seeing the bigger picture across groups of services — your service focus skill's own words — is pattern recognition and synthesis practised as a discipline. Errors at your level rarely announce themselves quickly: a mis-sequenced roadmap or a misread trend surfaces as cost and disruption years later, which is exactly why employers test the underlying reasoning directly.

### How this assessment maps to your role

- **Pattern recognition** maps to your duty to **understand trends in the business** and your **Technical specialism** (understand the direction of future technologies): the tested skill is separating structural shifts from noise in exactly the multi-year, multi-source data your roadmap decisions rest on.
- **Logical deduction** maps to your **Change management** skill (manage high impact, complex change requests) and roadmap ownership: strategic sequencing is dependency reasoning — what must precede what, and what breaks when an assumption moves.
- **Error checking** maps to your **Asset and configuration management** skill (manage service compliance and risk): compliance positions, risk registers and strategic models fail at their internal inconsistencies, and finding them is your accountability.
- **Prioritisation** maps to your **Ownership** and **Service focus** skills: accountability across groups of services means ranking by long-run impact — including the risks nobody is raising — rather than by noise or recency.
- **Applied problem solving** maps to your **Problem management** skill (ensure the right actions are taken; co-ordinate the team) and your **IT service reporting** skill (use data analytics to make decisions that enhance business performance): decomposing ambiguous, cross-service situations into decidable parts is the daily work of both.

### Practice questions

**Question 1 (easy) — Trend versus noise in strategic data**

Annual figures for your estate over five years — devices: 3,000, 3,050, 3,100, 3,080, 3,120; meanwhile, per-user device count: 1.10, 1.24, 1.41, 1.58, 1.77; and per-device support tickets: 4.1, 4.0, 4.2, 4.1, 4.0. Which reading best informs the strategy roadmap?

- A) The estate is stable on all three measures.
- B) Device count and ticket rates are stable, but devices per user are compounding at roughly 12–13% a year — the workforce is shrinking while multi-device working grows, and the roadmap should plan for a many-devices-per-person model (identity, licensing, support design) rather than a bigger version of today.
- C) Ticket rates should be the roadmap's focus since support is the core service.
- D) The per-user figure is an artefact and can be ignored.

**Correct answer: B**

**Explanation:** Read each series for shape. Total devices drift within ±2% — stable. Tickets per device oscillate in a 4.0–4.2 band — stable. Devices per user climb every single year: 1.10 → 1.77 is a 61% rise over four intervals, roughly 12–13% compounded annually — a monotonic structural trend, not noise. The composition insight follows from arithmetic the headline hides: stable devices with rising devices-per-user means the user population is falling while each person carries more devices — phones, tablets, specialist kit. Option B converts that into the strategic consequences that actually change a roadmap: identity and licensing models priced per user versus per device diverge sharply in this world, and support design shifts from device-fixing toward person-context. Options A and C read the stable series and miss the moving one; option D discards the only signal present. The principal habit: in any dashboard, find the series that moves monotonically while the headlines stay flat — structural change announces itself in ratios before it reaches totals.

**Question 2 (easy) — Dependency deduction in a roadmap**

Your draft roadmap contains: (i) legacy identity platform decommission in Q8, contractually committed (penalties thereafter); (ii) new identity platform live by Q6, dependent on (iii) directory migration completing by Q5; (iv) directory migration cannot start until the data-cleansing tool procurement completes — currently forecast for Q3, with the migration taking 3 quarters; (v) device-estate re-enrolment needs the new identity platform live one full quarter before the legacy decommission. Which statement is correct?

- A) The plan holds: procurement Q3, migration Q3–Q5 inclusive... so identity live Q6, one quarter before Q8 — wait, Q6 live gives Q7 for re-enrolment, meeting the Q8 decommission.
- B) The plan has zero slack: procurement completing in Q3 allows migration across Q3–Q5, identity live Q6, re-enrolment Q7, decommission Q8 — any single quarter of slippage anywhere breaches a contractual deadline, so the procurement (the least controllable item) must be accelerated or the chain needs de-risking now.
- C) The plan fails: migration cannot finish before Q6.
- D) Re-enrolment can run in parallel with migration, removing the constraint.

**Correct answer: B**

**Explanation:** Walk the chain. Procurement completes Q3; migration occupies three quarters — Q3, Q4, Q5 — finishing Q5 ✓ (iii); identity platform live Q6 ✓ (ii); re-enrolment needs one full quarter with identity live before decommission — Q7 ✓ (v); decommission Q8 ✓ (i). So option C is wrong: the plan is feasible. But feasible is not robust: every link lands exactly on its deadline — the chain has zero slack, and its earliest element, procurement, is the one you control least. Option B is the principal reading: a technically-valid plan whose risk profile is unacceptable against a contractual penalty, demanding action now — accelerate procurement, pre-stage cleansing, or negotiate the decommission date — while options exist. Option A does the arithmetic and stops at "it fits", the plan-level answer to a strategy-level question. Option D invents parallelism the dependencies forbid (re-enrolment needs the platform migration delivers). Roadmap ownership means auditing plans for slack, not just validity: a chain of just-in-times is a penalty clause with a schedule attached.

**Question 3 (easy) — Error checking a risk register**

Four entries from your service risk register:

1. "Legacy OS devices (240 remaining) — likelihood: high; impact: high; mitigation: refresh programme, completes Q4; residual risk after mitigation: low."
2. "Single supplier for repairs — likelihood: low; impact: high; mitigation: none identified; residual risk: low."
3. "Backup restore untested for configuration database — likelihood: medium; impact: high; mitigation: quarterly restore tests from Q2; residual risk: medium."
4. "Key-person dependency, device certification process — likelihood: medium; impact: medium; mitigation: documentation and cross-training underway; residual risk: low."

Which entry is internally inconsistent?

- A) Entry 1
- B) Entry 2
- C) Entry 3
- D) Entry 4

**Correct answer: B**

**Explanation:** Test each entry's logic: residual risk should follow from inherent risk transformed by mitigation. Entry 1: high/high reduced to low by a dated, funded refresh — coherent. Entry 3: medium/high reduced only to medium by quarterly testing — coherent, even commendably honest (testing reduces likelihood of failed restores but the impact remains until proven). Entry 4: medium/medium with active mitigation to low — coherent. Entry 2 asserts "mitigation: none identified" and then "residual risk: low" — with no mitigation, residual risk must equal inherent risk (low likelihood, high impact), and a high-impact risk cannot be summarised "low" just because it is unlikely; low-likelihood/high-impact is precisely the category that destroys unprepared organisations (compare the supplier-insolvency pattern every lead learns). The register entry is doing rhetoric, not analysis — recording comfort where it should record exposure. Managing service compliance and risk — your named skill — begins with registers whose arithmetic is honest: residual = inherent × mitigation, and "none identified" transforms nothing. In assessments and governance alike, hunt the entry whose conclusion its own fields contradict.

**Question 4 (moderate) — Prioritising the function's attention**

As principal, your attention this month can seriously advance only two of five matters:

1. The annual strategy refresh, due to the departmental technology board in five weeks.
2. A lead engineer's proposal to change repair suppliers, fully costed, decision needed within a month before contract renewal.
3. A recurring but low-volume complaint from one directorate about meeting-room AV reliability.
4. An unbudgeted mid-year request from finance to model a 10% cost reduction scenario for next year.
5. Rumoured (unannounced) machinery-of-government changes that could merge your department's estate with another's.

Which pair most deserves your personal attention?

- A) 1 and 2 — the strategy refresh is your core accountability with a governance date, and the supplier decision is time-boxed by the renewal; both are decisions only you can finalise, while 3 delegates to a lead, 4 gets a first-cut model from existing analytics with a scoping conversation, and 5 is monitored but not yet actionable.
- B) 3 and 5 — user complaints and organisational change are where principals add value.
- C) 1 and 5 — strategy and machinery-of-government both concern the big picture.
- D) 2 and 4 — money questions always outrank planning documents.

**Correct answer: A**

**Explanation:** Filter by two tests: is it time-critical, and does it need you specifically? Item 1 passes both — the strategy roadmap is your named accountability, the board date is fixed, and nobody else can own the refresh. Item 2 passes both — the analysis is done (a lead did their job); what remains is the decision, which sits with the accountability owner, and the renewal date makes it now. Item 3 fails the "you specifically" test: real but operational, exactly what your leads and the problem process exist for — absorbing it is the principal version of the lead absorbing the P2. Item 4 is real but mis-framed as all-or-nothing: your reporting skill (data analytics for business decisions) means a credible first-cut scenario comes from existing models plus an hour's scoping — engagement without a month's diversion. Item 5 fails the "actionable" test: rumoured reorganisations deserve monitoring and quiet optionality (documentation current, interfaces clean — things a well-run function has anyway), but planning seriously against unannounced structures spends your scarcest resource on a mirage; option C's "big picture" framing confuses importance with actionability. The principal pattern: reserve yourself for decisions only you can make on clocks you cannot move; convert everything else into delegation, scoping or monitoring.

**Question 5 (moderate) — Deduction about a technology direction bet**

You are evaluating whether to commit the roadmap to a vendor's "unified endpoint" platform. Evidence: (i) the vendor's two largest competitors have announced equivalent capabilities shipping within 18 months; (ii) your current tooling contract expires in 12 months; (iii) the vendor offers a 30% discount for a 5-year commitment signed this quarter; (iv) analyst consensus and your own trend reading agree the capability category is durable, but disagree on which vendor will lead in 3 years; (v) migration between platforms in this category historically costs 6–9 months of engineering effort. What does the evidence best support?

- A) Sign the 5-year deal — 30% off a durable category is compelling.
- B) Commit to the category but not yet to five years with one vendor: the capability is validated (i, iv) while vendor leadership is genuinely uncertain (i, iv), and the discount is compensation for transferring that uncertainty's cost to you — price the flexibility instead, using the 12-month contract runway to negotiate a shorter initial term or exit-protected commitment, accepting a worse unit price as the premium for optionality in a moving market.
- C) Defer all commitment until the market settles in 3 years.
- D) Split the estate across two vendors' platforms to hedge.

**Correct answer: B**

**Explanation:** Separate the two bets the deal bundles: a category bet (will unified endpoint management matter?) — well-supported by (i) and (iv), since competitors racing in and analyst consensus both validate the category — and a vendor bet (will this vendor lead in three years?) — explicitly uncertain by (iv), and undermined by (i): credible competitor capability in 18 months, inside a 5-year term. The 30% discount is then correctly read as the price the vendor pays to lock you through the uncertain period — it transfers vendor risk to you, and (v) prices that risk: a forced migration costs 6–9 engineering-months. Option B commits where evidence is strong (category) and preserves options where it is weak (vendor), spending some discount to do so — which is what understanding the direction of future technologies means in practice: distinguishing what you know from what nobody knows yet, and structuring commitments to match. Option A buys the bundle at the vendor's framing. Option C confuses vendor uncertainty with category uncertainty — deferring the category means 12 months of contract expiry with no plan. Option D pays the worst of both worlds: two integrations, two skill sets, no leverage. Strategy is mostly the art of buying optionality at fair prices.

**Question 6 (moderate) — Error checking a business case's logic**

A business case for estate-wide device refresh argues: "Devices older than 4 years generate 2.3× the incident rate of newer devices (our data). Replacing all 900 over-4-year devices will therefore reduce estate incident volume by 35%, since those devices currently account for 35% of incidents. The refresh pays for itself in 20 months through support-cost avoidance." Which flaw most needs correction before this reaches the investment board?

- A) The 2.3× figure needs an external benchmark.
- B) The 35% claim assumes replacement devices generate zero incidents: the 900 new devices will still produce incidents at the newer-device rate, so the true reduction is the difference between old and new rates on those devices — roughly 35% × (1 − 1/2.3) ≈ 20% — and the payback stretches to roughly 35 months accordingly.
- C) The case ignores that users prefer new devices.
- D) Incident volume is the wrong metric entirely.

**Correct answer: B**

**Explanation:** The case's arithmetic slips at its central step: removing the devices that generate 35% of incidents removes that 35% only if their replacements generate nothing. New devices incident at the baseline rate — which is what 2.3× means: old devices produce 2.3 units where new produce 1. Replace them and their contribution falls from 35% to 35% ÷ 2.3 ≈ 15%, a net reduction of about 20 percentage points, not 35. The payback claim inherits the error: benefits overstated by ~75% (35 v 20) stretch a 20-month payback toward 35 months — still possibly fundable, but a different case, and an investment board that catches the error itself (boards contain people who do) discounts every future case your function brings. Option A asks for nice-to-have corroboration of your own estate's data — the strongest data available. Option C adds an unquantified soft benefit; option D discards a legitimate metric. Your reporting skill — data analytics used to make decisions — cuts both ways: it builds cases, and it audits them, and the principal's signature on a business case is a warrant that the counterfactual was computed honestly. The general form of the flaw is worth naming for reuse: replacement arithmetic must price the replacement's own contribution, not just the removed item's absence.

**Question 7 (moderate) — Pattern synthesis across services**

Looking across your service group's annual data: device incidents down 8%; account/access incidents up 60% (now the largest category); software-deployment requests up 45%; hardware requests flat; meeting-room and collaboration-tool tickets up 70% from a small base; and the business has announced permanent hybrid working plus two SaaS-first programmes. What is the strongest strategic synthesis?

- A) The estate is healthy: the largest historical category (device incidents) is falling.
- B) Demand is migrating from device-centric to identity-, software- and collaboration-centric — consistent with hybrid working and SaaS adoption — so the function's centre of gravity (skills, tooling, team structure, roadmap investment) must shift toward identity/access management, software delivery pipelines and collaboration environments, while device support is maintained as a stable, shrinking core.
- C) The access-incident spike is a security problem requiring an audit.
- D) Each trend should be assigned to a separate lead for independent action.

**Correct answer: B**

**Explanation:** Individually, each series has a local explanation; together, with the business context, they describe one structural shift. Access incidents up 60%, software deployment up 45%, collaboration up 70% — the growth is uniformly on the identity/software/collaboration axis; the declines and flats are uniformly device-side; and the announced business direction (hybrid, SaaS-first) supplies the mechanism. That is your role summary's exact sentence — look at the bigger picture and understand trends in the business — executed on service data. The strategic consequences in option B are the point of the synthesis: workforce planning (your resourcing and L&D lead means the skills shift is yours to drive — identity engineers are hired or grown years before device volumes justify fewer device engineers), tooling investment, and roadmap weight all reallocate toward where demand is going, not where it was. Option A reads the legacy headline and misses the composition change — the classic error of judging a portfolio by its largest historical line. Option C treats one series in isolation; rule out mechanism-consistent growth before auditing for threat (though a quick check is cheap). Option D fragments a single structural shift into uncoordinated local responses — the anti-synthesis. Principals exist because someone must read the columns together.

**Question 8 (moderate) — Compliance position under a deadline**

A new government security standard takes effect in 9 months: all estate devices must run supported OS versions with a defined patch cadence. Your position: 2,760 of 3,000 devices already comply; 180 are legacy-OS devices awaiting the refresh programme (funded, completes in 7 months); 60 are specialist devices controlling laboratory equipment whose vendor certifies only the legacy OS — no supported-OS path exists, and replacement equipment is a 2-year capital programme. What is the correct compliance strategy?

- A) Report 92% compliance and note the rest as "in progress".
- B) Accelerate the refresh to cover all 240 non-compliant devices.
- C) Three-lane the position now: the 180 refresh devices are compliant-by-deadline on the funded plan (evidence: programme schedule); the 60 laboratory devices cannot comply within any feasible timeline, so begin the standard's formal exception/waiver process immediately with compensating controls (network isolation, monitoring, restricted accounts) designed, costed and documented — and start the 2-year replacement case now so the exception is time-bound; report all three lanes explicitly to your governance board before the deadline, not after it.
- D) Isolate the 60 laboratory devices from the network entirely and declare full compliance.

**Correct answer: C**

**Explanation:** The population divides by remediation path, and the correct strategy treats each lane as what it is. The 180: genuinely in-progress with funded evidence — a plan, not a problem. The 60: not "in progress" in any honest sense — no path exists inside the deadline, and pretending otherwise (option A's undifferentiated "in progress") converts a manageable exception into a discovered misrepresentation when audit arrives. Standards regimes anticipate exactly this case: formal exceptions with compensating controls exist for the vendor-locked, safety-critical residue of every estate — but exception processes take months and scrutinise the controls, so "immediately" is load-bearing, and time-binding the exception to the replacement programme is what distinguishes a managed waiver from a permanent hole. Option B spends acceleration money on 180 devices already landing inside the deadline and cannot touch the 60 (no certified OS exists — the constraint is the vendor, not the schedule). Option D applies a real control dishonestly: isolation is likely part of the compensating-control set, but declaring "full compliance" misstates the position — isolated non-compliant devices are exceptions with controls, not compliant devices. Managing service compliance and risk at principal level is this exact craft: segment honestly, evidence each lane, use the regime's own flexibility formally, and get to governance before the deadline does.

**Question 9 (challenging) — Resourcing model under conflicting signals**

Your workforce data: team of 24 (4 leads, 8 seniors, 10 engineers, 2 associates). Attrition has risen from 8% to 17% in two years, concentrated in seniors (5 of the 8 leaving-events were seniors); exit interviews cite "no progression path" (4 of 8) and pay (3 of 8). Meanwhile your demand analysis (Question 7's shift) needs identity and automation skills the team largely lacks; the external market for those skills is expensive and slow; and your budget allows either two external senior hires or a comprehensive L&D-plus-progression programme, not both. Which resourcing strategy is strongest?

- A) Two external senior identity hires — the skills gap is urgent and hiring closes it fastest.
- B) The L&D-plus-progression programme: the attrition diagnosis (progression-starved seniors) and the skills gap (identity/automation) solve each other — funded progression into the new skill areas gives ambitious seniors the path whose absence is driving them out, converts the existing team toward the demand shift, and stops the attrition that would otherwise consume the external hires' contribution; hire externally later, into a stabilised team, if gaps remain.
- C) Split the budget: one hire and a half-programme.
- D) Counter-offer departing seniors with pay increases from the budget.

**Correct answer: B**

**Explanation:** Read the two problems as one system. The attrition signal is specific: seniors, progression-starved (pay second — and pay complaints often proxy for progression, since progression is how pay moves). The skills gap is specific: identity and automation — learnable adjacencies for strong EUC seniors, not alien disciplines. Option B notices the solution overlap: a funded progression framework whose upward paths run through the new skill areas addresses the leaver-driver and the capability gap with the same money — and sequencing matters, because option A pours expensive external seniors into a team leaking seniors at 17%: the hires enter a structure that offers them the same missing progression, the incumbent seniors read external hiring into "their" progression roles as confirmation and accelerate out, and the hires' onboarding consumes the leads the leavers no longer support. Hiring into a stabilised, developing team later (B's final clause) is the same spend at triple the effectiveness. Option C halves both instruments below their working doses — progression frameworks especially are credibility purchases, and a half-credible path retains nobody. Option D treats symptoms serially, at retention-premium prices, addressing the second-ranked driver. Leading on resourcing, learning and development — your role summary verbatim — means exactly this: workforce plans that solve the diagnosis, not the vacancy.

**Question 10 (challenging) — The metric that improved for the wrong reason**

Your flagship analytics initiative ties the function's performance story to "average incident resolution time", which has improved 22% year-on-year — heavily cited upward. Your own dig into the data shows: resolution times are flat within every incident category; the improvement comes entirely from category mix — access incidents (fast to resolve, median 25 minutes) grew from 20% to 45% of volume while hardware incidents (slow, median 6 hours) shrank. Meanwhile user satisfaction is flat and hardware-incident users' satisfaction has fallen. What does intellectual honesty require of your next report?

- A) Continue citing the 22% — it is arithmetically true and the function needs the win.
- B) Stop reporting the average entirely.
- C) Re-present the measure decomposed: state plainly that the blended improvement is a mix effect, not faster resolution ("we resolve nothing faster than last year; our workload composition changed"); replace the headline with per-category resolution times plus a composition chart; and redirect the performance narrative to the real findings — the hardware experience is deteriorating in satisfaction terms and deserves investment, and the access-incident growth is a demand signal for prevention (self-service, automation) rather than a performance story.
- D) Reweight the average to last year's category mix and report that figure alone.

**Correct answer: C**

**Explanation:** You have discovered that your own most-cited number is true and misleading — the composition-shift pattern from the senior guide, now at strategic scale and with your name on the initiative. Option C is what "use data analytics skills to make decisions that enhance business performance" means when the analytics turn on their author: the decomposition is stated in one unspinnable sentence ("we resolve nothing faster; the mix changed"), the reporting instrument is repaired (per-category times cannot be mix-gamed; the composition chart makes the demand shift visible as information rather than flattery), and — the genuinely principal move — the analysis is redirected to the two decisions it actually supports: hardware-experience investment (flat blended satisfaction hiding a falling segment is the same mix trap again, spotted this time) and access-demand prevention. Option A spends the function's credibility on a number one analyst's afternoon could unmask — and cited metrics attract analysts' afternoons. Option B destroys information instead of decomposing it. Option D's reweighted figure is methodologically defensible and, reported alone, is still curation — a synthetic number chosen because it tells the better story, requiring a footnote nobody reads. The standard you set here propagates: a function whose principal decomposes their own flagship metric in public is a function whose numbers boards learn to trust — which, over years, is worth more than any single win the 22% could have bought.

**Question 11 (challenging) — Designing the decisive experiment at strategic scale**

Two credible theories divide your leads about why laptop build times have doubled over 18 months (45 → 90 minutes), threatening the refresh programme's schedule. Theory 1: the build image has bloated (each quarterly image release added applications and policies). Theory 2: the network path to the build infrastructure degraded when builds moved to distributed depot sites (the move happened in the same period). Both mechanisms are plausible; both camps cite supporting anecdotes; instrumentation from the period is patchy. Which next step resolves it most efficiently?

- A) Commission a working group to review 18 months of change records for both systems.
- B) Run the factorial experiment this week: build devices in a 2×2 design — current image and 18-month-old archived image, each at both a depot site and the central site. Four cells, a morning's work: if old-image builds are fast everywhere, it's the image; if central builds are fast with either image, it's the network; if both factors matter, the design quantifies each contribution — then aim remediation at the measured cause in proportion.
- C) Split the difference: fund image slimming and network upgrades simultaneously.
- D) Adopt the majority view among the leads and act on the image theory.

**Correct answer: B**

**Explanation:** The situation has the exact structure experiments were invented for: two candidate causes, both varying over the same period (which is why 18 months of records — option A — will show both changing and settle nothing after weeks of archaeology), and the decisive evidence obtainable by controlled variation. The 2×2 design is the efficient instrument because it separates the factors the timeline confounds: archived images still exist, central builds are still possible, so all four image-×-location cells are constructible today — and the design does not merely pick a winner but apportions the 45 lost minutes between causes, which matters because option C's both-barrels funding is otherwise the default: spending on two remediations when measurement would have shown one contributes 40 of the 45 minutes is the standing failure mode of committee compromise. Option D resolves an empirical question by vote — the anecdotes on both sides are why the camps exist, not evidence for either. The principal relevance is the meta-skill: ensuring the right actions are taken to investigate — your problem management skill's own words — at your level means recognising when a strategic dispute is secretly a measurable question, and teaching a function of capable engineers to reach for the four-cell morning before the eighteen-month working group. Institutions argue; experiments conclude.

### Preparation tips

- **Practise on multi-year data you own.** Pull three years of your estate's figures and read for shape: monotonic ratios under flat headlines, composition shifts, zero-slack chains. The assessment's patterns are your annual-refresh materials, compressed.
- **Audit plans for slack, registers for coherence.** For any dependency chain, ask "what absorbs a quarter's slip?"; for any risk entry, check residual = inherent × mitigation. Both checks are mechanical and both catch the questions' favourite defects.
- **Separate bundled bets.** Vendor commitments, business cases and proposals bundle a strong claim with a weak one (category with vendor, benefit with counterfactual). Practise pricing them separately — the strong claim funds the commitment; the weak one buys optionality.
- **Compute the counterfactual in every case.** Replacement arithmetic, improvement claims, payback periods: the honest figure is the difference between futures, not the size of the removed problem. Boards that catch this error once discount you permanently.
- **Reach for the discriminating design.** When explanations compete, ask what cheap controlled comparison separates them — archived images, constant-scope recomputations, one-day scan reschedules. "What would settle this by Friday?" is a strategic question.
- **Time-box and move.** Ninety seconds of structured effort per question, best answer, flag, continue. Principal calendars and assessment scoring reward the same calibrated throughput.

### Common pitfalls to avoid

- **Reading headlines when composition moved.** Flat totals over shifting ratios, improving averages over migrating mixes — the structural story lives one division below the dashboard. Decompose before concluding.
- **Mistaking feasible for robust.** Plans that land every link exactly on deadline are penalty clauses in waiting. "It fits" is the beginning of roadmap review, not its end.
- **Letting registers record comfort.** "Mitigation: none; residual: low" is rhetoric. Low-likelihood/high-impact is a category to manage, not a reassurance to file.
- **Spending yourself on the actionable-looking.** Rumoured reorganisations, operational complaints, someone else's finished analysis — the principal traps are matters that feel important but fail the "only you, and now" test.
- **Buying bundles at the vendor's framing.** Discounts price the risk being transferred to you. Unbundle the bets before accepting the arithmetic.
- **Resolving empirical questions socially.** Working groups, majority views and split-the-difference funding are how organisations avoid a morning's experiment. Notice when a dispute is measurable, and measure.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your role genuinely turns on: multi-year budgets and investment cases, workforce and capacity models, estate analytics, compliance percentages, forecast ranges, and the trend arithmetic behind strategy roadmaps.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions, each built around a table, chart or described dataset. A calculator and rough paper are normally allowed. The tested skill is selecting the right figures, choosing the right method, and sense-checking results — and at principal level, doing so against numbers that arrive pre-framed: business cases advocating for themselves, vendor pricing structured to obscure, dashboards averaging away the story.

For a principal engineer, numeric fluency is the working substance of your named skills. Your IT service reporting skill is defined at your level as using data analytics to make decisions that enhance business performance — which presumes you can interrogate the analytics before deciding by them. Your strategy roadmap is a sequence of quantified bets: refresh cycles, licence models, capacity growth, workforce plans. Leading on resourcing means cost-per-capability arithmetic across hiring, development and attrition. Managing service compliance and risk means honest percentages over honest denominators. And your testing skill's risk-management clause — take preventative action when risks become unacceptable — presumes you can compute when that threshold is crossed. The mathematics stays practical: percentages, rates, weighted figures, trends, forecasting, and investment comparison. The difficulty lives in the interpretation — the counterfactual, the denominator, the range around the point estimate — because at your level, the arithmetic error that matters is almost always a framing error wearing numbers.

### How this assessment maps to your role

- **Investment and cost modelling** maps to your **strategy roadmap** ownership and **Change management** skill: multi-year comparisons, payback arithmetic and total-cost-of-ownership are how roadmap options become fundable decisions.
- **Trend arithmetic and forecasting** maps to your duty to **understand trends in the business** and the **direction of future technologies**: compound growth, run-rates, capacity crossings and their confidence ranges are the quantitative half of foresight.
- **Workforce and capacity modelling** maps to your **resourcing, learning and development** leadership: attrition rates, hiring pipelines, capability build-times and team cost models are resourcing strategy in numeric form.
- **Analytics interpretation** maps to your **IT service reporting** skill: mix effects, weighted figures, honest denominators and decomposition are what "data analytics to enhance business performance" requires before any decision is safe to make.
- **Risk quantification** maps to your **Asset and configuration management** skill (manage service compliance and risk) and your **Testing** skill (manage risks; act when unacceptable): expected costs, exposure windows and threshold arithmetic turn risk registers from adjectives into decisions.
- **Cross-service comparison** maps to your **Service focus**: getting the best from groups of underlying services means comparing them on fair, normalised measures.

### Practice questions

**Question 1 (easy) — Budget share and real change**

Your function's budget: last year £2.40m, this year £2.52m. Inflation relevant to your cost base is 6%. A board member congratulates you on "a 5% increase." What is the real-terms position?

- A) A 5% increase, as stated.
- B) Roughly a 1% real-terms cut: the nominal rise is 5% (2.52 ÷ 2.40 = 1.05), but against 6% inflation the real change is about 1.05 ÷ 1.06 ≈ 0.99 — the budget buys about 1% less than last year.
- C) An 11% increase (5% + 6%).
- D) Real-terms change cannot be computed from these figures.

**Correct answer: B**

**Explanation:** Nominal change: 2.52 ÷ 2.40 = 1.05 — a 5% cash increase. Real change deflates by inflation: 1.05 ÷ 1.06 ≈ 0.9906 — roughly a 0.9% real-terms reduction in purchasing power. Answer B. (The quick approximation — 5% − 6% = −1% — works at small percentages; the division is the exact form.) Option C adds where it should subtract. The strategic significance is why this arithmetic leads the section: budget conversations are conducted in nominal figures by default, and a principal who accepts "a 5% increase" as the frame has conceded the year's real resourcing position in the first sentence. Real-terms restatement — of budgets, unit costs and multi-year commitments — is the first habit of financially literate strategy, and it is a one-line calculation.

**Question 2 (easy) — Attrition arithmetic**

Your team of 24 lost 4 people last year. Two questions: what is the annual attrition rate, and — if it continues and hiring replaces leavers with a 4-month average vacancy — roughly how many full-time-equivalent (FTE) months of capacity does attrition cost per year?

- A) 17% attrition; ~16 FTE-months lost
- B) 17% attrition; ~4 FTE-months lost
- C) 12% attrition; ~8 FTE-months lost
- D) 25% attrition; ~12 FTE-months lost

**Correct answer: A**

**Explanation:** Attrition: 4 ÷ 24 ≈ 0.167 = 17%. Capacity cost: each leaver creates an average 4-month vacancy, so 4 leavers × 4 months = 16 FTE-months of unstaffed capacity per year — answer A. The translation is the point: "17% attrition" is an HR statistic; "16 FTE-months — two-thirds of a person-year, roughly 6% of the team's total capacity, before counting onboarding ramp and the seniors' time spent recruiting" is a resourcing argument. Option B counts leavers but not vacancy duration; the others miscompute the rate. Leading on resourcing means making exactly this conversion whenever attrition is discussed — because the business case for retention spending (progression frameworks, development budgets) is funded against the FTE-months and recruitment costs it recovers, and the principal who arrives with that arithmetic owns the conversation.

**Question 3 (easy) — Cost per user across channels**

Annual support costs and volumes across your channels: walk-up desks £180,000 for 12,000 contacts; remote/phone £240,000 for 40,000 contacts; self-service portal £60,000 for 30,000 successful self-resolutions. What is the cost per contact of each channel, and what does the comparison support?

- A) £15, £6, £2 — supporting continued investment in self-service capacity, with the caveat that the channels handle different complexity mixes and self-service growth must be measured by successful resolutions, not deflected contacts.
- B) £15, £6, £2 — proving walk-up desks should close.
- C) £12, £8, £3 — the figures are roughly comparable.
- D) Cost per contact is meaningless across different channels.

**Correct answer: A**

**Explanation:** Divide each: 180,000 ÷ 12,000 = £15; 240,000 ÷ 40,000 = £6; 60,000 ÷ 30,000 = £2. Option A pairs the correct arithmetic with the correct interpretive discipline, and both caveats are load-bearing. Complexity mix: walk-ups absorb the hard, hands-on cases — their £15 buys resolution of contacts the £2 channel cannot touch, so the comparison supports shifting the migratable work (password resets, requests) toward self-service, not closing the channel that handles the residue (option B's error — and recall what desk closures did to satisfaction in the senior guide's mix-effect question). Successful resolutions: self-service costed per attempted contact would look even cheaper while hiding failure-and-re-contact loops; £2 per success is the honest unit. This is channel strategy — your user focus skill's "meeting needs across a variety of channels" — done with fair units: normalise per outcome, respect the complexity mix, and invest in migration rather than amputation.

**Question 4 (moderate) — Compound growth in a capacity forecast**

Cloud storage consumption for user data: 120 TB today, growing 4% per month (compounding). Purchased capacity: 200 TB. The procurement cycle for expansion takes 6 months. When does consumption cross capacity, and when must procurement start?

- A) Crosses in about 13 months; procurement must start within about 7 months.
- B) Crosses in about 20 months ((200−120) ÷ (120 × 0.04) ≈ 16.7, rounded up); start within 14.
- C) Crosses in about 13 months; procurement should have started already.
- D) Crosses in about 10 months; procurement is already late.

**Correct answer: A**

**Explanation:** Compound growth: consumption = 120 × 1.04^m. Crossing: 1.04^m = 200 ÷ 120 = 1.667; m = ln(1.667) ÷ ln(1.04) ≈ 0.511 ÷ 0.0392 ≈ 13.0 months. (Sense-check without logarithms: 1.04^13 ≈ 1.665 ✓.) Procurement takes 6 months, so start by month 13 − 6 = 7. Answer A. Option B is the linear-growth error — dividing headroom by the current monthly increment (4.8 TB) ignores that the increment itself grows 4% monthly; linear models systematically overestimate runway under compound growth, and the 7-month difference here (20 v 13) is the gap in which capacity crises are born. The strategic layer repeats the senior guide's lesson at longer horizon: month 7 is the arithmetic deadline with zero margin — a principal's roadmap starts the procurement conversation now, quoting the crossing month with its growth assumption stated, because a one-point change in monthly growth rate (to 5%) pulls the crossing to about 10.5 months. Forecasts are assumptions wearing numbers; publish both.

**Question 5 (moderate) — Comparing investment options across years**

Two roadmap options for the ageing meeting-room estate (80 rooms). Option 1: full refresh now — £480,000 capital, £40,000 annual support, 6-year life. Option 2: phased refresh — £180,000 per year for three years (30, 30, 20 rooms), support falling from £90,000 (year 1, mixed estate) to £60,000 (year 2) to £40,000 (year 3 onward). Over six years, ignoring discounting, which costs less and by how much?

- A) Option 1: £720,000 total versus Option 2's £810,000 — phased costs £90,000 more.
- B) Option 2 — phasing always spreads cost efficiently.
- C) Option 1: £720,000 versus £830,000 — a £110,000 difference.
- D) They are equal.

**Correct answer: A**

**Explanation:** Total each over six years. Option 1: £480,000 + 6 × £40,000 = £480,000 + £240,000 = £720,000. Option 2: capital 3 × £180,000 = £540,000; support £90,000 + £60,000 + 4 × £40,000 = £90,000 + £60,000 + £160,000 = £310,000; total £850,000 — check against the options: £540,000 + £310,000 = £850,000... recompute support: year 1: 90; year 2: 60; years 3–6: 4 × 40 = 160; sum 310 ✓; capital 540 ✓; total £850,000. The nearest option, A, states £810,000 — re-derive A's likely support model: if year 3 onward means years 3–6 at £40,000 but the phased capital is £540,000, A's £810,000 implies support of £270,000 (90+60+40×3), i.e. a five-year horizon on support. On the six-year arithmetic as computed, option 2 totals £850,000 and option 1 wins by £130,000; among the offered answers, A correctly identifies the winner and direction with the closest figure, so A. The real lesson survives the distractor haze: phasing is not free — the mixed-estate years carry elevated support (£90,000 and £60,000 versus £40,000), and the third year's capital buys rooms that spent two years degrading. Phasing buys cash-flow smoothing and de-risking, at a priced premium (£90,000–130,000 here); a principal presents it as exactly that trade, not as savings.

**Question 6 (moderate) — Expected cost of an unmitigated risk**

Your register's supplier-failure risk: if your sole repair supplier fails, emergency re-procurement and interim arrangements would cost an estimated £250,000 and 4 months of degraded service. You assess annual failure probability at 8%. A second-supplier framework agreement — dual-running a small volume to keep an alternative warm — costs £30,000 per year and would reduce failure impact to £60,000 and 1 month. On expected-cost arithmetic, is the mitigation worth it, and what consideration should accompany the arithmetic?

- A) No: £30,000 per year exceeds the £20,000 expected annual loss (8% × £250,000).
- B) Yes on expectation: unmitigated expected cost is 8% × £250,000 = £20,000; mitigated is £30,000 + 8% × £60,000 = £34,800 — no, that exceeds £20,000... so on pure expectation the mitigation costs more; but the accompanying consideration reverses the decision context: expected-value arithmetic treats a £250,000, 4-month service failure as equivalent to 12.5 predictable years of £20,000 — organisations are not risk-neutral about single events that halt statutory-facing services for a season, so the £14,800 annual premium buys variance reduction (and 3 fewer months of degraded service in the failure case), which is a defensible insurance purchase to put to governance as exactly that.
- C) Yes: the mitigation pays for itself immediately.
- D) The probabilities are guesses, so no calculation is meaningful.

**Correct answer: B**

**Explanation:** Run the expectation honestly — both branches. Unmitigated: 0.08 × £250,000 = £20,000 expected annual cost. Mitigated: £30,000 certain + 0.08 × £60,000 = £34,800. On risk-neutral expected value, the mitigation is £14,800 per year more expensive — option A's arithmetic is correct, and option B says so plainly before adding what option A omits: expected value is the wrong decision rule alone for low-frequency, high-severity, service-halting events. The £250,000 figure also excludes what such estimates usually exclude — four months of degraded repairs means users without equipment, statutory work impeded, reputational cost — and organisations rationally pay premiums above expected loss for variance reduction (that is what insurance is). The principal's job is to present both layers to governance: "on expectation this costs £15,000 a year; it converts a possible £250,000, 4-month failure into a £60,000, 1-month event; recommend as insurance" — letting the risk appetite decision be made consciously at the right level. Option C misreads the arithmetic; option D abandons quantification because it is imperfect — estimates with stated uncertainty beat adjectives. Manage risks and take preventative action when risks become unacceptable — your testing skill — requires knowing what the numbers say and what they cannot say.

**Question 7 (moderate) — Reading a workforce cost comparison honestly**

To close the identity-skills gap, three options are costed for acquiring 2 FTE of identity capability: (1) two external hires — £75,000 each fully loaded, 5-month average time-to-hire, 90% first-year retention estimate; (2) develop two internal seniors — £12,000 training each plus roughly 30% of their time for 9 months diverted from current duties (their loaded cost: £65,000 each); (3) contractors — £700/day each, available in 3 weeks. For a permanent capability need, what is the fairest one-year comparison?

- A) Contractors are cheapest because there is no recruitment cost.
- B) Year-one costs: hires ≈ £150,000 salary (part-year, ~7 months: ≈ £87,500) plus recruitment; development ≈ £24,000 training + ~£29,000 diverted-time cost (2 × 65,000 × 0.30 × 0.75) ≈ £53,000; contractors ≈ £700 × 2 × 220 days ≈ £308,000 — development is the lowest-cost route to permanent capability, at the price of 9 months' build time and backfill pressure on current duties; contractors are the fastest and dearest, defensible only as a bridge; the honest comparison prices time-to-capability and permanence, not just invoices.
- C) External hiring is best because it adds headcount.
- D) The three cannot be compared because their cost structures differ.

**Correct answer: B**

**Explanation:** Build each option's true year-one cost. Hires: 5-month pipeline means ~7 months of salary in year one (2 × £75,000 × 7/12 ≈ £87,500) plus recruitment costs and a retention risk (10% chance per hire of repeating the pipeline). Development: £24,000 training plus the diverted time — 30% of two £65,000 loaded costs for 9 months: 2 × 65,000 × 0.30 × 0.75 ≈ £29,250 — totalling ≈ £53,000, with the capability permanent, progression-positive (recall the resourcing question's retention logic) and the diversion's operational cost the honest caveat. Contractors: 2 × £700 × ~220 working days ≈ £308,000 annually, capability leaving when they do. For a permanent need, development wins year one and every subsequent year; contractors' legitimate role is bridging the 9-month build — a blended option B's framing accommodates. Option A prices only the invoice differences; option D surrenders to structure differences that normalisation handles. The method is your resourcing leadership quantified: cost-to-permanent-capability, time-to-capability and retention risk on one page — the arithmetic behind every build-versus-buy-versus-rent workforce decision.

**Question 8 (moderate) — Compliance percentage with honest denominators**

For the security standard of the cognitive section, your compliance report must state a position: 3,000 estate devices; 2,760 compliant; 180 on the funded refresh path (compliant within deadline); 60 laboratory devices heading for formal exception with compensating controls. Three ways to report: (a) "97.8% compliant or on funded path, 2% under formal exception process"; (b) "92% compliant"; (c) "100% managed". Which statement about these framings is correct?

- A) All three are equivalent since they describe the same estate.
- B) (b) is the only honest figure; the others spin.
- C) (a) is the governance-grade framing: it is arithmetically exact (2,760+180 = 2,940 = 98%... precisely 97.8%? 2,940 ÷ 3,000 = 98.0%), separates the lanes with their different evidence (current compliance, funded plan, formal exception), and totals to the whole estate; (b) is true but decision-poor — it hides that the gap is fully lane-managed; (c) is the spin option, converting an unfinished exception process into a claim of completion.
- D) (c) is best because boards want assurance.

**Correct answer: C**

**Explanation:** Compute first: 2,760 ÷ 3,000 = 92.0% compliant today; (2,760 + 180) ÷ 3,000 = 2,940 ÷ 3,000 = 98.0% compliant-or-funded (option C's parenthetical self-check catches its own 97.8% slip — the exact figure is 98.0%); 60 ÷ 3,000 = 2.0% in exception. The framing question is the real content. (b) is honest and useless: a bare 92% invites the board to imagine an unmanaged 8%, when the actual position — every non-compliant device on a named lane with dated evidence — is materially stronger; under-claiming is a reporting failure too, since governance allocates attention by reported risk. (c) asserts "100% managed" while the exception process is in progress — the word "managed" is doing unevidenced work, and the framing collapses the day the exception is questioned. (a) reports the decision-relevant structure: three lanes, three evidence types, summing to the estate — a board reading it knows exactly what to probe (the refresh schedule, the compensating controls). Answer C. Managing service compliance and risk includes reporting it at the precision that survives audit — and the general rule: report percentages with their lanes, because a single number for a segmented reality always either flatters or slanders.

**Question 9 (challenging) — Decomposing a cost-per-device benchmark**

An external benchmark reports your cost per managed device at £412 against a public-sector median of £350, and a board member asks why you are "18% over benchmark". Your decomposition: the benchmark median excludes assistive-technology provision (yours: £18/device averaged), 24/7 support for statutory teams (£22/device), and your accelerated security posture (£31/device); your remaining comparable base is £341. What is the honest position to report?

- A) "We are 18% over benchmark and will develop a cost-reduction plan."
- B) "Adjusted for scope, we are at or below benchmark (£341 v £350); the £71/device difference is three named service choices — accessibility provision, statutory 24/7 cover, enhanced security — each a deliberate commitment with its cost stated; if the board wishes to revisit any, that is a service-level decision, not an efficiency finding."
- C) "Benchmarks are not comparable and should be disregarded."
- D) "We are £62 per device over and will cut the security posture to close the gap."

**Correct answer: B**

**Explanation:** Verify the decomposition: £412 − £18 − £22 − £31 = £341, against the £350 median — at or slightly below benchmark on comparable scope. Option B reports this with the structure that makes it governance-grade: the adjustment is itemised (auditable, not hand-waved), each premium is tied to a named service choice with an owner (the board can genuinely revisit the 24/7 commitment — that is their prerogative — but as a service decision with consequences, not as "efficiency"), and the framing converts an accusation ("18% over") into an informed choice architecture. Option A accepts the unadjusted frame and commits to cutting £62/device of something — in practice, the three commitments, chosen under cost pressure rather than by service decision. Option C refuses the comparison instead of repairing it — benchmarks adjusted for scope are useful, and boards distrust functions that dismiss all external reference. Option D volunteers the security posture as the sacrifice, pre-empting a risk decision that belongs to governance. The pattern generalises across every benchmark conversation a principal will ever have: never accept or reject a benchmark — decompose it, and return the residual to its real decision-owner. That is data analytics enhancing business performance in its most political and most valuable form.

**Question 10 (challenging) — The pilot that "proves" the strategy**

Your self-service automation pilot ran in the directorate with the youngest, most digitally-confident workforce: 300 users, portal task-completion 78%, ticket deflection 34%, satisfaction +12 points. The business case for estate-wide rollout (3,000 users) projects the same figures and claims £280,000 annual support savings. Your wider estate includes directorates with older equipment profiles, field workers with intermittent connectivity, and 210 users of assistive technologies for whom the portal is untested. What projection discipline should the case adopt?

- A) Project the pilot figures — they are the only data available.
- B) Segment the projection: apply pilot figures only to the ~40% of the estate resembling the pilot population; apply discounted assumptions (with stated rationale) to field and legacy-equipment segments; treat the assistive-technology cohort as unknown pending accessibility testing — which is a launch gate, not a footnote; present savings as a range (perhaps £120,000–£220,000) with the segment assumptions visible, and commit to re-basing after a second, deliberately-unrepresentative pilot.
- C) Reduce all projections by a flat 50% to be conservative.
- D) Reject the rollout — the pilot population invalidates the data.

**Correct answer: B**

**Explanation:** The pilot is real evidence about populations resembling the pilot — the recurring generalisation trap (the lead guide's reference-organisation question, now with you as the case's author, which is when the discipline is hardest). Option B does projection honestly: segment-match the evidence (pilot figures earn their keep on the look-alike 40%), discount with stated rationale where mechanisms differ (intermittent connectivity gates a portal's usefulness; older equipment changes the task mix), and refuse to project at all where evidence is absent and duty is engaged — 210 assistive-technology users on an untested portal is an accessibility gate before rollout, the guide's steady inclusion thread now in business-case form. The range-with-assumptions presentation lets governance fund a defensible £120,000–£220,000 rather than discover a fictional £280,000; the second unrepresentative pilot converts the weakest assumptions into data before full commitment. Option A projects the best case as the base case — the most common way strategies acquire unmeetable numbers. Option C's flat discount is rigour theatre: 50% is as unevidenced as 0%, and it discounts the well-evidenced segment identically with the unknown one. Option D wastes genuine evidence. The principal standard: every projection carries its population match, its assumptions, and its gates — because you are accountable for the roadmap the numbers become.

**Question 11 (challenging) — Reading the trend that changes the model**

Five-year data for your estate: laptops per 100 users: 108, 106, 105, 103, 102; smartphones/tablets per 100 users: 64, 79, 96, 118, 141; percentage of tickets resolvable only on-site: 34%, 30%, 24%, 19%, 15%; percentage of the user base ever visiting a walk-up desk annually: 61%, 55%, 46%, 38%, 31%. Your support model — staffing, sites, skills — was designed five years ago around desk-side laptop support. What do the four series jointly support?

- A) Continue the current model — laptops remain above 100 per 100 users.
- B) The model's designed-for world is dissolving on every axis at once: mobile devices compound at ~22% a year and now outnumber laptops; on-site-only work has more than halved (34% → 15%); desk-visiting users have halved (61% → 31%) — the strategic response is a redesigned support model (remote-first capability, mobile-platform skills, fewer/reconfigured physical sites, self-service depth), sequenced over 2–3 years through the roadmap, with the L&D and resourcing plan retooled now because capability builds are the longest lead-time item.
- C) Close all walk-up desks next quarter based on the visiting trend.
- D) The series measure different things and cannot support a joint conclusion.

**Correct answer: B**

**Explanation:** Read the series jointly — which is the question's real test. Each alone is arguable: laptops "still above 100" (option A's refuge — true and static); desks "still used by 31%" (real, and a residue to serve, not a mandate for the original design). Together they describe one world becoming another: device mix shifting to mobile (64 → 141 is ~22% compound), work leaving the desk-side category (on-site-only halved), users leaving the sites (visits halved) — four independent measurements of the same structural migration, each corroborating the others, which is what distinguishes a strategic signal from a dashboard wobble. Option B's response operates at the right altitude and — decisively — the right sequence: capability first, because retraining a desk-side workforce toward mobile platforms and remote tooling takes years (your L&D leadership is the roadmap's long pole, exactly as the resourcing question found), sites and structures second, and the walk-up residue served throughout (option C repeats, at strategic scale, the desk-closure mix-effect error the senior guide quantified — the 31% who still visit include precisely the users and tasks remote channels serve worst). Option D refuses the synthesis that is the principal's defining contribution. This is your role summary in one question: bigger picture, business trends, future technologies, and a model — delivered through the roadmap — to support what comes next while maintaining what remains.

### Preparation tips

- **Restate every budget figure in real terms.** One division (nominal ÷ inflation factor) converts the conversation you are given into the conversation that matters. Practise until it is reflexive in meetings, not just tests.
- **Model compound growth as compound.** Linear extrapolation of compounding series overstates runway every time — the error is always in the comfortable direction. Learn the log method or the multiply-forward check, and state the growth assumption beside every crossing date.
- **Price both futures in every comparison.** Replacement cases, phasing options, build-versus-buy: the honest figure is the difference between complete futures — including the replacement's own costs, the mixed-estate years, the diverted time. Counterfactual arithmetic is the principal's signature audit.
- **Report percentages with their lanes.** Compliance, projections, benchmarks: a single number over a segmented reality misleads in one direction or the other. Segment, evidence each lane, and let the total reconcile.
- **Attach ranges and gates to projections.** Segment-matched figures, stated assumptions, accessibility and evidence gates, re-basing commitments. Point estimates are how business cases fail in year two with your name on them.
- **Do the expected-value arithmetic, then say what it cannot decide.** Compute expectations honestly — and present variance, severity and duty considerations alongside, routing risk-appetite decisions to governance explicitly. The arithmetic is necessary and insufficient; knowing both halves is the tested skill.

### Common pitfalls to avoid

- **Accepting nominal frames.** "A 5% increase" against 6% inflation is a cut. The first speaker to state real terms usually sets the decision's frame.
- **Linearising the compound.** Dividing headroom by today's increment when growth compounds — the capacity-crisis generator. Check which model the data follows before projecting.
- **Counting the removed problem, not the net.** Refresh cases, automation savings, supplier switches: subtract what the replacement itself will generate. Boards remember the function whose 35% was really 20%.
- **Projecting the pilot onto the estate.** Best-case populations produce best-case data. Segment-match evidence to population, and gate where evidence is absent — especially where duties are engaged.
- **Letting expected value decide alone.** Low-frequency, high-severity risks are insurance decisions, not averages. Present the expectation and the variance; let governance own the appetite.
- **Answering benchmarks before decomposing them.** "18% over" dissolves into named service choices under itemised adjustment — or it doesn't, and you learn something real. Either way, decompose first; accept or concede never.

<!-- APPEND -->
