# Principal Infrastructure Operations Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a principal infrastructure operations engineer working within the UK Government Digital and Data profession. Whether you are preparing for a formal assessment, benchmarking yourself against the most senior technical leadership demands of the profession, or refining the standards you set for the teams and leads you direct, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. At principal level, the prediction target is distinctive: not whether you can execute operations, nor even whether you can lead a team, but whether you can direct an operational capability — set strategy, govern risk, own supplier relationships at portfolio level, and make the long-horizon judgements on which an organisation's technology investments succeed or fail. The assessments described here are job-specific to that altitude. They draw on the artefacts you genuinely handle: strategic and tactical technology roadmaps, investment appraisals and total-cost models, supplier portfolios and their contractual and regulatory obligations, compliance and risk registers, capacity strategies spanning groups of services, and the governance papers through which operational reality reaches boards. And they exercise the judgements you genuinely make: sequencing technology transitions so services stay reliable while platforms change beneath them; deciding when a supplier relationship needs remediation, renegotiation, or exit; balancing investment between the estate you run and the estate you must build; and ensuring that what your organisation reports about its operations is true.

Why do these assessments matter at your level? Because principal-level failure modes are reasoning failures at scale. A misread trend becomes a roadmap that future-proofs against the wrong future. An unchallenged supplier figure becomes a contractual position surrendered. A weighted-average error in a board pack becomes a misallocated budget. A governance paper that overstates readiness becomes an organisational commitment nobody can keep. The four assessments here — cognitive, numeric, verbal, and situational — map directly onto the daily mechanics of strategic operations leadership, and practising them sharpens precisely the capabilities your role turns on.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why it matters at your level, a mapping of the assessment's dimensions to the specific skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid.

To get the most from it: attempt every question honestly, committing before reading the explanation; treat each explanation as method made explicit — at principal level the margin lies in disciplined judgement under ambiguity, and the walkthroughs surface the discipline; and read with your governance hat on, because much of this material converts directly into the standards you set — for escalations, for board papers, for supplier reviews, and for the leads you develop toward your own role. Revisit after an interval: judgement consolidates through spaced practice at every level, including this one.

The questions progress from easy through moderate to hard, and the hard questions are genuinely hard. That is deliberate. Take your time, work honestly, and enjoy the practice. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using practical scenarios rather than abstract puzzles. For a principal infrastructure operations engineer, the scenarios operate at portfolio altitude: reading trends across groups of services rather than single systems, tracing the consequences of strategic decisions through technical, contractual, and organisational dependency chains, detecting the inconsistency in an investment case or a compliance report, and sequencing multi-year transitions under interacting constraints.

The typical format is an online, timed test of 15 to 30 minutes with 20 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group, frequently adaptive, with accuracy and speed reported separately. Ungraded practice questions usually precede the scored test.

At principal level, cognitive assessment measures the capability your role names in its first line: developing strategic and tactical roadmaps for technologies and services, ensuring they are future-proofed and the organisation derives maximum value from its investment. Every clause of that sentence is a reasoning task. Roadmaps are dependency-and-sequencing problems spanning years. Future-proofing is trend extrapolation done honestly — distinguishing durable direction from fashionable noise, and knowing which uncertainties a strategy must survive rather than predict. Maximum value from investment is comparative reasoning across options whose costs and benefits arrive on different schedules and rest on different assumptions. And beneath all of it sits the portfolio habit your service focus skill names: seeing the bigger picture by taking groups of services and investigating how to get the best from the underlying services — which is pattern recognition and deduction performed across an estate rather than a server. The questions below reproduce these demands in miniature; the techniques they reward are the ones your real artefacts require.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Service focus** skill — seeing the bigger picture across groups of services means detecting estate-level patterns invisible at single-service altitude — and to your **Technical specialism** skill of understanding the direction of future technologies, which is trend-reading disciplined by evidence.
- **Logical deduction** maps to your **Problem management** skill (ensuring the right actions are taken to investigate, resolve and anticipate problems — anticipation being deduction about the future) and your **Incident management** skill of leading investigation and resolution at the level where incidents cross service and supplier boundaries.
- **Error checking** maps to your **Asset and configuration management** skill — managing configuration items, service compliance and risk means detecting where records, obligations, and reality diverge — and to your **Change management** duty to ensure release policies and processes are applied, which requires spotting non-conformity before it ships.
- **Prioritisation** maps to your **Availability and capacity management** skill (identifying capacity issues and initiating remedial action across an estate means ranking risks that compete for finite response) and to your roadmap duty, where sequencing is prioritisation extended through time.
- **Applied problem solving** maps to your **Technical specialism** duty to deliver a model that supports future technologies while coexisting with the current environment — the defining principal-level design problem — and to your **Ownership and topic** skill of proactively searching for potential problems before they occur.

### Practice questions

**Question 1 (easy) — Estate-level pattern in incident distribution**

Reviewing annual major-incident data across your estate's five platform groups:

| Platform group | Major incidents | Services hosted | Age profile |
|---|---|---|---|
| Cloud compute | 6 | 40 | 0–3 years |
| Virtualised estate | 8 | 55 | 3–8 years |
| Legacy midrange | 9 | 6 | 12–20 years |
| Network core | 4 | all traverse | 2–10 years |
| Storage estate | 5 | all use | 1–9 years |

Which reading best identifies the estate's concentration of operational risk?

- A) The virtualised estate — it has the most major incidents.
- B) Legacy midrange — 9 major incidents across only 6 services is an incident density more than tenfold the cloud and virtualised groups, concentrated on the oldest platforms.
- C) Cloud compute — new platforms are always the riskiest.
- D) Network core — everything traverses it, so it must be the greatest risk.

**Correct answer: B**

**Explanation:** Normalise before concluding. Incidents per hosted service: cloud 6 ÷ 40 = 0.15; virtualised 8 ÷ 55 = 0.145; legacy midrange 9 ÷ 6 = 1.5 — an order of magnitude above the modern platforms, on the estate's oldest technology. Option A reads the raw count that platform size, not platform risk, produces. Option C substitutes a prejudice for the data, which shows cloud at the lowest density. Option D raises a real structural point — shared infrastructure concentrates consequence — but the network's incident record (4 events across everything that traverses it) does not show it as the current generator of risk; consequence-if-failed and frequency-of-failure are different risk axes, and the question asks where risk is concentrating in the observed data. The principal-level reading in option B also carries the strategic implication: incident density clustered on a 12–20-year-old platform hosting few services is the classic signature of an estate segment past its reliability knee — exactly what a technology roadmap exists to retire, and exactly the evidence an investment case for that retirement should lead with. Seeing the bigger picture across groups of services begins with denominators.

**Question 2 (easy) — Deduction from a compliance rule**

Your compliance framework states: "Any service processing personal data must have a completed data protection impact assessment (DPIA) before go-live. A service may go live without a completed DPIA only where the data protection officer (DPO) has granted a documented deferral." Service S went live last month and processes personal data. Which conclusion must be true?

- A) Service S had a completed DPIA before go-live.
- B) The DPO granted a documented deferral for Service S.
- C) Either Service S had a completed DPIA before go-live, or the DPO granted a documented deferral, or the framework was breached.
- D) The framework was breached.

**Correct answer: C**

**Explanation:** The rule admits exactly two compliant paths for a personal-data service going live — completed DPIA, or documented DPO deferral — and the facts given establish only that the service went live and processes personal data. Which path it took, or whether it took neither, is unknown; so A, B, and D each assert one branch of an unresolved disjunction, while C states the complete disjunction that must hold in every consistent scenario. The governance reflex this rehearses: managing service compliance and risk — your asset and configuration skill's explicit phrase — means converting rules plus partial facts into precisely the verification question the case requires ("show me the DPIA or the deferral"), rather than into either accusation or assumption. At principal level you also read the rule's design: the deferral path exists because absolute gates get bypassed informally when they meet immovable deadlines — a documented exception route is what keeps the record honest. Auditing the exception register, not just the rule, is where assurance actually lives.

**Question 3 (easy) — Error checking an investment case's logic**

An investment paper for replacing your backup platform argues: "Option A (renew incumbent): £900k over five years, no migration risk. Option B (new platform): £700k over five years including migration, plus modern features. Option B is £200k cheaper and strictly superior; we recommend B. Note: Option B pricing assumes decommissioning the incumbent by month 9; the incumbent contract's minimum term runs to month 18, with early-exit fees of £150k." What is the paper's defect?

- A) Option A's figure is probably inflated.
- B) The recommendation's £200k advantage ignores a cost its own note discloses: exiting the incumbent at month 9 incurs £150k early-exit fees (or retaining it to month 18 incurs parallel-running costs), so the true gap is at most £50k — and possibly negative — before "strictly superior" can be claimed.
- C) Five years is the wrong appraisal horizon.
- D) Modern features are overvalued in the comparison.

**Correct answer: B**

**Explanation:** The defect is internal inconsistency — the paper's own note defeats its own headline. Option B's £700k depends on decommissioning at month 9; the disclosed contractual position makes month 9 exit cost £150k in fees, or alternatively forces parallel running to month 18 (two platforms' costs for nine months — plausibly more than £150k). Either way the £200k advantage shrinks to £50k or less, and "strictly superior" collapses into "possibly marginally cheaper, with migration risk". Options A, C and D are challenges one could investigate, but they import assumptions; option B needs nothing beyond the paper's own sentences. This is the reviewing discipline on which "maximum value from investment in technologies" — your roadmap duty's phrase — actually depends: most broken cases are not arithmetically wrong but structurally inconsistent, and the inconsistency usually hides in a note, an assumption, or a footnote that the executive summary forgot. Principal review reads the notes first.

**Question 4 (easy) — Prioritising remedial capacity actions**

Your capacity review across the estate surfaces four findings:

1. The payments platform will exhaust database connections in ~3 weeks at current growth; remediation is a configuration change, tested, ready to schedule.
2. The analytics cluster will exhaust storage in ~8 months; expansion requires procurement (~4-month lead time).
3. The intranet is over-provisioned by ~40%, wasting ~£30k/year; rightsizing is a low-risk change.
4. A dashboard gap: no capacity metrics exist for the new API gateway, which launched three months ago and is growing fast by anecdote.

What is the soundest ordering of action?

- A) 1 (schedule now), 4 (instrument now — unmeasured fast growth is an unbounded risk), 2 (start procurement this quarter), 3 (rightsizing when convenient).
- B) 3 first — realising savings funds everything else.
- C) 2 first — procurement lead times dominate everything.
- D) 1 only — the rest can wait for next year's review.

**Correct answer: A**

**Explanation:** Rank by proximity-to-harm adjusted for response lead time and uncertainty. Item 1 is closest to harm (3 weeks) with the shortest remediation path (tested change) — schedule immediately; cheap insurance against a hard outage. Item 4 is the subtle second: an unmeasured, reportedly fast-growing service is a risk of unknown proximity — it could be item 1 in disguise — and instrumenting it is quick; unknown-but-knowable risks get converted to known ones early, because everything else in capacity management depends on measurement. Item 2's deadline is 8 months minus 4 months' procurement = a decision needed within roughly a quarter — start now-ish, but after the two immediate actions. Item 3 is genuine value with no deadline pressure. Option B funds pennies while a three-week fuse burns; option C misapplies a true principle (lead times dominate) to the wrong item — item 2's lead time still leaves months of margin, item 1's fuse does not; option D confuses "most urgent" with "only". The principal-level content is item 4's placement: identifying capacity issues — your availability and capacity skill — presupposes visibility, and the estate's biggest capacity risk is routinely the service nobody instrumented. Measurement gaps are findings, not footnotes.

**Question 5 (moderate) — Deduction across a technology transition**

Your roadmap migrates services from the legacy midrange platform to cloud in three tranches. Facts: (i) Tranche 1 (non-critical services) completed successfully six months ago; (ii) Tranche 2 (important services) begins next month; (iii) the legacy platform's vendor support contract expires in 14 months and the vendor has announced no renewal will be offered; (iv) Tranche 3 contains the two most critical services, and its migration is planned to take 6 months once begun; (v) tranches cannot overlap, and Tranche 2 is planned at 6 months. Which conclusion about schedule risk must be true?

- A) The plan is comfortable — 14 months exceeds 6 + 6.
- B) The plan has at most 2 months of total slack across Tranches 2 and 3 before the most critical services are running on an unsupported platform — so any slip beyond 2 months converts the estate's most critical services into its least protected ones.
- C) Tranche 3 should be moved before Tranche 2.
- D) The vendor will likely extend support if asked.

**Correct answer: B**

**Explanation:** Compute the schedule spine: Tranche 2 (6 months, starting next month) plus Tranche 3 (6 months, non-overlapping) = 12 months of planned work against a 14-month support horizon — leaving 2 months of total slack, minus the one month before Tranche 2 starts, if that month is idle (the strict answer holds at "at most 2 months"). Option A does the same arithmetic and stops before the risk reading: 2 months of slack across 12 months of migration work is thin — migrations slip, and the structure places the most critical services last, so every slip lands on them; if the schedule overruns, the organisation's most important workloads are precisely the ones left on a platform with no vendor support. That inversion — criticality migrating last, risk accumulating on the most critical — is the conclusion that must be true and must be surfaced. Option C mistakes the observation for a directive: resequencing has its own logic (Tranche 1 and 2 de-risk the method before the critical services move — a defensible design), and the facts do not establish that moving Tranche 3 earlier is net-better; the mandatory conclusion is the slack arithmetic, not a specific re-plan. Option D is hope, contradicted by the announced non-renewal. Roadmap reasoning at principal level is exactly this: dependency arithmetic first, then the honest statement of where the residual risk pools — plus the contingency planning (slip triggers, interim risk mitigations for an unsupported platform) that a 2-month-slack plan owes its governance board.

**Question 6 (moderate) — Pattern versus noise in technology trend data**

You are refreshing the technology roadmap. Four signals are in front of you:

1. Your container platform's usage has grown from 15% to 60% of new deployments over three years, with every one of your six development teams now deploying to it by default.
2. A market analyst report names a new orchestration technology "the future of infrastructure", citing three early-adopter case studies.
3. Your virtualised estate's new-deployment share has fallen from 70% to 25% over the same three years, though it still hosts 55 production services.
4. A conference keynote you attended predicts serverless will "eliminate infrastructure operations within five years".

Which combination should most shape the roadmap's platform strategy?

- A) Signals 2 and 4 — external sources see further than internal data.
- B) Signals 1 and 3 — three years of consistent, estate-wide behavioural data showing where your own demand is actually going, with the corollary that 55 production services need a managed path off a platform new demand has abandoned.
- C) Signal 4 alone — the boldest prediction deserves the biggest bet.
- D) All four signals weighted equally.

**Correct answer: B**

**Explanation:** Grade the signals by evidential weight and relevance. Signals 1 and 3 are longitudinal, internal, behavioural, and mutually confirming: your own organisation's revealed preference has moved decisively to containers, and the virtualised platform is becoming a legacy estate in real time — 55 production services on a platform with collapsing new demand is tomorrow's stranded estate unless the roadmap manages the transition deliberately. Signals 2 and 4 are directional inputs worth monitoring, but an analyst's three case studies and a keynote's elimination prophecy are weak evidence for committing an estate — option A inverts the evidence hierarchy (external narrative over internal behaviour), option C bets the roadmap on the least-evidenced claim, and option D's equal weighting is abdication dressed as balance: weighting is the analysis. Understanding the direction of future technologies — your technical specialism — is not collecting predictions; it is triangulating durable direction from strong evidence, using weak signals as hypotheses to test cheaply (a serverless pilot, a watching brief on the new orchestrator) rather than destinations to commit to. The roadmap that results holds committed transitions where evidence is strong and options where it is weak — future-proofing means surviving multiple futures, not predicting one.

**Question 7 (moderate) — Error checking a supplier's compliance attestation**

Your hosting supplier's annual attestation states: "All customer environments are patched to vendor-supported levels. Certification: our platform holds [industry certification], renewed this January. Note: certification scope covers our primary data centre; the secondary data centre, added to your service in March following the DR expansion, will be included at the next annual audit." Your regulated workloads fail over to the secondary data centre, and your regulator requires certified environments for these workloads at all times. What is the critical finding?

- A) The patching claim cannot be verified.
- B) Between March and the next audit, your regulated workloads' failover destination is an uncertified environment — so a DR invocation would move regulated workloads into non-compliance at exactly the moment of maximum scrutiny, and the gap needs remediation (accelerated certification, interim controls agreed with the regulator, or failover redirection) now, not at the next audit cycle.
- C) The certification renewal in January is suspicious.
- D) Nothing — the supplier has disclosed the gap transparently, so the risk is managed.

**Correct answer: B**

**Explanation:** Intersect three facts: the secondary DC is outside certification scope until the next audit; your regulated workloads fail over to it; your regulator requires certification "at all times" for those workloads. The intersection is a live compliance gap with a nasty trigger profile — it materialises precisely when DR is invoked, i.e. during an incident, when regulatory attention is highest and remediation options are fewest. Option B names the gap and the remediation set: accelerate scope extension, agree interim compensating controls with the regulator, or redirect the failover path for regulated workloads until certification lands. Option D commits the disclosure fallacy: a transparently disclosed risk is an identified risk, not a managed one — disclosure transfers knowledge, not accountability, and "will be included at the next annual audit" is the supplier's convenience, not your regulator's requirement. Options A and C manufacture suspicion where the document gives none. This is your role's supplier-ownership duty in its most consequential form: owning operational relationships with suppliers, ensuring services are aligned to regulatory and contractual requirements, means reading attestations for what their scope notes exclude — the finding is almost always in the scope note — and then driving the remediation rather than filing the attestation.

**Question 8 (moderate) — Applied problem solving: coexistence architecture**

Your organisation is adopting a new cloud data platform over three years, but two major systems cannot migrate: one legacy database underpins a critical service and is certified only on midrange hardware; the other belongs to a shared cross-government service outside your control. The programme proposes "everything migrates; the stragglers will be forced by decommissioning dates". As principal, which alternative model is soundest?

- A) Endorse the programme's approach — forcing functions work.
- B) Design an explicit coexistence model: the two non-migratable systems get a defined long-stay environment with named support arrangements, integration contracts (interfaces, data flows, latency budgets) between old and new platforms, its own security and compliance treatment, and a review trigger tied to real events (certification change, the shared service's own roadmap) — while everything genuinely migratable proceeds on the programme's schedule.
- C) Delay the entire migration until the two systems can move.
- D) Migrate the two systems anyway and accept the certification and control gaps.

**Correct answer: B**

**Explanation:** The programme's premise — universal migration enforced by decommissioning dates — fails on contact with the two stated facts: a certification constraint (the legacy database is supported only on midrange) and an authority constraint (the shared service's roadmap is not yours to set). Forcing functions cannot force what certification forbids or what other organisations control; option A's decommissioning dates would arrive with the systems still there, converting a planning fiction into an unplanned risk. Option D breaks certification on a critical service — trading a known, supported configuration for an unsupported one to satisfy a slide. Option C lets the least movable 5% freeze the movable 95% — surrendering three years of value to symmetry. Option B is the answer your technical specialism skill describes verbatim: delivering a model to support and maintain future technologies and any databases that coexist in the current environment. The content of that model is what makes it real rather than a euphemism for drift: named support (who fixes the long-stay environment at 3 a.m.), integration contracts (so the new platform's evolution cannot silently break the old systems' interfaces), distinct compliance treatment (long-stay environments age out of default assumptions), and event-driven review triggers (so "long-stay" ends when its reasons end, not never). Principal-level architecture is mostly this: designing the exception's home as carefully as the rule's, because unmanaged exceptions are where estates rot.

**Question 9 (moderate) — Prioritisation under governance and delivery tension**

Four items compete for your week:

1. The annual infrastructure strategy paper is due to the technology board in ten days; your draft needs two solid days.
2. A supplier's quarterly service review is tomorrow; their performance has degraded two quarters running, and you own the relationship — preparation needs half a day to marshal the evidence.
3. A P1 post-incident review for last week's cross-platform outage awaits your chairing decision: this week (memories fresh) or next (calendars easier).
4. A lead engineer you are developing has asked you to joint-review their first major roadmap contribution — an hour, movable.

What is the most defensible plan?

- A) Strategy paper all week; move everything else.
- B) Prepare and hold the supplier review (the degradation trend makes tomorrow's session consequential); chair the post-incident review this week while evidence is fresh; give the lead their hour early in the week; build the strategy paper across the remaining days — it has ten days of runway.
- C) Delegate the supplier review to a lead and focus on the strategy paper.
- D) Postpone the post-incident review to next week and use the freed time for the paper.

**Correct answer: B**

**Explanation:** Sequence by immovability and consequence, not by document size. The supplier review is tomorrow, and its stakes are set by the trend: two quarters of degradation makes this the session where the relationship either corrects or slides toward formal remediation — and you own the relationship; option C's delegation sends exactly the wrong signal at exactly the escalation point (delegating routine reviews is healthy; delegating the difficult one you own is abdication). The post-incident review's quality is time-sensitive in a way calendars are not: cross-platform outage evidence — what people remember, what logs retain — decays within days, and "calendars easier next week" purchases convenience with diagnostic quality; option D makes that trade explicit and wrong. The lead's hour is small, movable, and disproportionately valuable — reviewing their first roadmap contribution is succession-building, the quiet duty of every principal — so it gets scheduled, not squeezed out. The strategy paper, largest but with ten days of runway, flexes around the fixed points; option A treats the biggest artefact as the most urgent, which is the classic seniority inversion — papers have runway, incidents and relationships have moments. The principal-level pattern: your calendar's fixed points are set by other people's decay rates — evidence, relationships, development moments — and the flagship document fits the gaps, not the reverse.

**Question 10 (hard) — Cross-boundary incident deduction**

A cross-government authentication service your estate consumes degraded for three hours yesterday, breaking sign-in for two of your services. Facts assembled this morning: (i) the authentication provider's status page reported "degraded performance" from 09:40; (ii) your two affected services began erroring at 09:10, thirty minutes earlier; (iii) your third service using the same provider was unaffected all day; (iv) the affected pair share a network egress route through a regional gateway, which the unaffected service does not use; (v) the gateway's error logs show intermittent packet loss from 09:05; (vi) the provider's incident report, published overnight, attributes their degradation to a database issue from 09:40 and closes the matter. What does the evidence support?

- A) The provider's incident fully explains your outage; close your incident aligned to theirs.
- B) Two distinct faults overlapped: your services' errors began 35 minutes before the provider's incident, correlate with packet loss on the shared egress gateway (which the unaffected service bypasses), so your primary cause is likely the gateway path, with the provider's later degradation compounding it — your investigation stays open, focused on the gateway, whatever the provider's report says.
- C) The provider's report is wrong and should be formally disputed.
- D) The unaffected service proves the provider was never the problem.

**Correct answer: B**

**Explanation:** Run the timeline and the differential together. Timeline: your errors start 09:10; the provider's incident starts 09:40 — a 30-minute gap the provider's explanation cannot cover (their database issue cannot reach backward in time). Differential: the affected/unaffected split tracks the egress route, not the provider — all three services share the provider; only the two that traverse the regional gateway failed, and the gateway logs packet loss from 09:05, five minutes before your first errors. The evidence therefore supports two overlapping events: a network-path fault (yours to fix) from ~09:05, and a genuine provider degradation (theirs, from 09:40) that likely worsened the middle hour. Option A is the convenient closure — an external incident report is an explanation-shaped object, and aligning to it buries your gateway fault until it recurs without a provider incident to hide behind. Option D over-rotates: the provider's degradation was real (status page, their own diagnosis) and plausibly contributed after 09:40; exonerating them entirely misreads the overlap. Option C picks a fight the evidence does not require — their report may be accurate about their fault and simply irrelevant to your first 30 minutes; the professional move is a technical query about the timeline discrepancy, not a formal dispute. This is principal-level incident leadership: ensuring the right actions are taken to investigate — your problem management skill — includes refusing the completed-looking explanation when your own evidence says the boundary of causes lies elsewhere. Attribution across organisational boundaries follows evidence, not press releases.

**Question 11 (hard) — Multi-constraint sequencing of a strategic programme**

Your three-year infrastructure strategy contains five workstreams: network refresh (N), identity platform replacement (I), data centre exit (D), observability platform (O), and legacy midrange retirement (L). Constraints: (i) D cannot complete until N completes — the new network must carry the migrated traffic; (ii) L cannot complete until I completes — legacy services' authentication must move off the platform before retirement; (iii) O must complete before D begins its final migration wave, because the exit's cutover risk is unmanageable without unified observability; (iv) the organisation can run at most two workstreams concurrently; (v) each workstream takes one year; (vi) I cannot start in year 1 (procurement). Which schedule completes everything in three years?

- A) Year 1: N + O; Year 2: I + D; Year 3: L (+ contingency)
- B) Year 1: N + I; Year 2: O + D; Year 3: L
- C) Year 1: D + O; Year 2: N + I; Year 3: L
- D) Year 1: N + L; Year 2: I + O; Year 3: D

**Correct answer: A**

**Explanation:** Verify option A against every constraint. Year 1: N and O run (two streams — (iv) satisfied; neither is I — (vi) satisfied). Year 2: I and D run — D requires N complete ((i): N finished year 1 ✓) and O complete before D's final wave ((iii): O finished year 1 ✓). Year 3: L runs — L requires I complete ((ii): I finished year 2 ✓). All five streams fit in three years with year 3 running a single stream — spare concurrency that is genuine contingency. Now the rivals: B breaks (vi) — I starts in year 1. C breaks (i) and (iii) — D runs in year 1 before N and effectively alongside O rather than after it. D breaks (ii) — L runs in year 1, before I has even started. The solving method scales to real strategy work: identify the constrained-start items (I cannot start early) and the terminal dependencies (L after I; D after N and O), place the unconstrained enablers earliest (N, O are pure prerequisites — they unlock everything and depend on nothing), and let the dependent streams cascade. Note what the correct schedule quietly embodies: enabling infrastructure first, dependent transformations second, retirements last — with slack landing at the end, where slips accumulate. That shape — enablers, transitions, retirements — is the canonical architecture of infrastructure roadmaps, and recognising it converts scheduling puzzles from search problems into pattern matches.

**Question 12 (hard) — The strategy assumption stress-test**

Your draft strategy commits to consolidating all infrastructure operations tooling onto a single vendor's integrated suite, on four stated grounds: (a) 30% licence saving versus the current multi-vendor estate; (b) reduced integration maintenance; (c) the vendor's roadmap alignment with your cloud direction; (d) simplified skills requirements. A challenge session asks: "What must remain true for five years for this to stay the right call?" Which answer demonstrates the strongest strategic reasoning?

- A) "The savings are contractually locked, so the decision is safe regardless."
- B) "Four assumptions carry the strategy: the vendor's pricing power stays benign after we are consolidated (single-vendor dependence historically invites renewal-cycle price recovery — so we need contractual protections extending beyond the initial term, and a costed exit path to preserve negotiating position); the vendor's roadmap actually tracks ours (needs annual verification against delivery, not slideware); integration savings are not offset by the suite's weaker best-of-breed capabilities in monitoring depth (needs a capability floor defined per domain); and our skills simplification does not become a skills monoculture that cannot evaluate alternatives (needs deliberate horizon-scanning capability retained). The strategy stands, with those four hedges built in and reviewed annually."
- C) "Nothing needs to remain true — strategies are reviewed annually anyway."
- D) "The consolidation should be abandoned — single-vendor risk is always disqualifying."

**Correct answer: B**

**Explanation:** The question tests whether you can hold a commitment and its fragility simultaneously — the defining posture of durable strategy. Option B enumerates the load-bearing assumptions and attaches to each a monitoring mechanism or hedge: pricing power (the consolidator's classic trap — the 30% saving is the entry price; the renewal after switching costs are sunk is where single-vendor economics bite — hedged contractually and by maintaining a credible exit); roadmap alignment (verified against shipped delivery annually, because vendor roadmaps are marketing documents until delivered); capability floors (integrated suites win on integration and routinely lose on depth — the strategy must define the minimum per-domain capability below which the suite fails the estate); and skills monoculture (a subtle one: an organisation trained only on one suite loses the ability to know when to leave it — so horizon-scanning is retained deliberately). This is future-proofing as your roadmap duty actually means it: not predicting that the assumptions hold, but instrumenting them so their failure is detected early and survivable. Option A confuses a contract with a future — locked savings do not lock roadmap alignment, capability adequacy, or renewal-cycle behaviour. Option C outsources thinking to the review calendar; annual reviews catch what someone thought to measure, and option B is the list of what to measure. Option D replaces judgement with a slogan — single-vendor consolidation is sometimes right; unhedged consolidation is what is wrong. Assessments and challenge sessions alike reward the same structure: commit, name the assumptions, instrument them, and keep the exit priced.

### Preparation tips

- **Normalise everything, then read the residue strategically.** Incidents per service, cost per workload, failures per change: at principal level the denominator question is reflexive, and the second question — "what does the normalised pattern imply for the roadmap?" — is where your answers should land.
- **Read papers from the notes upward.** Investment cases, attestations, and programme papers hide their defects in scope notes, assumptions, and footnotes. Practise reading the caveats first and testing the headline against them — most structural inconsistencies fall out in seconds.
- **Compute schedule spines and name where slack pools.** For any multi-phase plan: total the critical path, subtract from the hard horizon, and state explicitly which phase — and which services — absorb the residual risk. The arithmetic is easy; the honest statement of where risk pools is the skill.
- **Grade evidence before weighting it.** Internal longitudinal behaviour beats analyst narrative beats keynote prophecy. Practise sorting trend inputs into commit-grade, monitor-grade, and hypothesis-grade before letting any of them touch a roadmap.
- **Rehearse the assumption stress-test.** For any strategy or major decision, practise answering "what must remain true?" with named assumptions, each carrying a detection mechanism and a hedge. This one structure serves challenge sessions, board papers, and hard assessment questions identically.
- **Sequence by decay rates.** Evidence decays, relationships decay at inflection points, development moments pass; documents have runway. Practising this ordering on your real calendar is direct preparation for prioritisation questions — and better weeks.

### Common pitfalls to avoid

- **Raw counts at portfolio altitude.** Estate-level data misleads exactly as team-level data does, with bigger consequences. Density, rates, and per-unit figures — always — before any strategic conclusion.
- **The completed-looking explanation.** Supplier incident reports, programme assurances, and vendor roadmaps arrive shaped like answers. Timeline gaps and differential evidence outrank narrative completeness; keep your investigation open when your own data disagrees.
- **Disclosure mistaken for management.** A risk transparently disclosed — by a supplier, a paper, a programme — is identified, not handled. The scored answers (and the safe estates) drive remediation; they do not file the disclosure.
- **Betting roadmaps on the loudest signal.** Keynotes and analyst reports are hypothesis generators. Committing an estate on monitor-grade evidence — or ignoring three years of internal behavioural data because a prediction is bolder — fails both tests and futures.
- **Universal rules with unplanned exceptions.** "Everything migrates" strategies fail at their exceptions. Design the coexistence model deliberately — support, interfaces, compliance, review triggers — or the exceptions design themselves as drift.
- **Slack invisible, risk unstated.** Plans presented without their slack arithmetic, and strategies without their load-bearing assumptions, look strong and govern badly. State where the risk pools; instrument what must remain true.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with quantitative material: percentages, ratios, weighted averages, rates, projections, and data in tables and charts. At principal level the material is the arithmetic of strategy and governance: multi-year investment comparisons, total cost of ownership, supplier portfolio economics, estate-wide KPI consolidations, risk quantification, and the capacity and demand models on which roadmaps rest.

The typical format is an online, timed test of 20 to 35 minutes with 15 to 25 questions; an on-screen calculator is normally available. Principal-level variants weight interpretation and challenge heavily: the question behind most questions is "is this stated conclusion sound, and what does the correct figure imply for the decision?"

Why does numeracy matter at your altitude? Because you are the last technical checkpoint before numbers become commitments. Investment cases reach approval carrying the arithmetic their authors chose; your review is where horizons, baselines, and discount conventions get challenged — after approval, the numbers govern you. Supplier portfolio decisions — renewal, remediation, exit — rest on cost and performance figures that suppliers themselves supply; the recomputation habit is the control. Board packs consolidate estate KPIs, and every consolidation choice (weights, denominators, periods) is an editorial decision someone should have made deliberately — at your level, that someone is you. And roadmaps are quantitative objects: demand curves, capacity steps, migration rates, and the lead times that convert event dates into decision deadlines. Your role's own language — maximum value from investment in technologies, service compliance and risk, identifying capacity issues and initiating remedial action — is a list of numerical duties wearing prose.

As at every level, the mathematics itself never exceeds confident arithmetic: the four operations, percentages, and averages. The difficulty lives in setup, baselines, horizons, and interpretation — which is precisely why these questions are worth practising: the calculation is the easy half of every figure you sign.

### How this assessment maps to your role

- **Investment and total-cost arithmetic** maps to your roadmap duty of ensuring **maximum value from investment in technologies**: multi-year comparisons, crossover analysis, and the horizon and baseline choices that decide options papers.
- **Supplier portfolio economics** map to your duty to **own operational relationships with suppliers**: contract-year arithmetic, service credit regimes, concentration risk, and the cost cases behind remediation or exit decisions.
- **Estate-level consolidation** maps to your **Service focus** skill of taking groups of services and getting the best from them: weighted KPIs, per-service densities, and honest aggregation across unequal populations.
- **Demand and capacity modelling** maps to your **Availability and capacity management** skill: compound demand curves, stepped capacity, lead-time subtraction, and the decision deadlines that make capacity governance real.
- **Risk quantification** maps to your **Asset and configuration management** duty of managing service compliance and risk, and your **Testing** skill of managing risks and taking preventative action when risks become unacceptable — "unacceptable" being, wherever possible, a computed judgement.

### Practice questions

**Question 1 (easy) — Estate availability in downtime terms**

Your flagship service's availability target rises from 99.9% to 99.95% under a new agreement, measured monthly over a 43,200-minute month. By how many minutes does the monthly downtime budget shrink?

- A) 43.2 to 21.6 — a reduction of 21.6 minutes
- B) 43.2 to 4.32 — a reduction of 38.9 minutes
- C) 21.6 to 4.32 — a reduction of 17.3 minutes
- D) 43.2 to 2.16 — a reduction of 41 minutes

**Correct answer: A**

**Explanation:** Compute both budgets. At 99.9%: downtime allowance = 0.1% × 43,200 = 43.2 minutes. At 99.95%: allowance = 0.05% × 43,200 = 21.6 minutes. The budget halves — from 43.2 to 21.6, a reduction of 21.6 minutes. The halving follows directly from the target arithmetic: 0.05% is half of 0.1%. Option B mistakes 99.95% for 99.99% (which would give 4.32). The governance translation is the principal-level point: agreeing "99.9 to 99.95" in a negotiation sounds incremental — a 0.05-point concession — but it halves the error budget, which may require redundancy investment, faster failover, or change-freeze discipline that costs real money. Availability points are logarithmic in cost; the arithmetic is how you price a courtesy-sounding concession before agreeing it.

**Question 2 (easy) — Supplier spend concentration**

Your infrastructure supplier portfolio spends: Supplier A £2.4M, Supplier B £1.2M, Supplier C £0.9M, Supplier D £0.5M, others combined £1.0M. What percentage of total spend sits with Supplier A?

- A) 30%
- B) 35%
- C) 40%
- D) 45%

**Correct answer: C**

**Explanation:** Total = 2.4 + 1.2 + 0.9 + 0.5 + 1.0 = £6.0M. Supplier A share = 2.4 ÷ 6.0 = 0.40 = 40%. Sense-check: 2.4 is a little under half of 6.0's half (3.0), so 40% fits. The portfolio reading: 40% concentration with one supplier is a dependency figure that belongs in your risk register with a stated tolerance — concentration is not automatically wrong (scale discounts are real), but it prices your negotiating position and your exposure to that supplier's failure, and the number should be a managed quantity, not a discovered one. Owning supplier relationships at principal level starts with knowing this figure for your own portfolio without looking it up.

**Question 3 (easy) — Weighted estate availability**

Three service groups report monthly availability: critical services (12 services) 99.8%; standard services (30 services) 99.5%; internal tools (18 services) 98.9%. Weighting by service count, what is the estate-wide average availability?

- A) 99.40%
- B) 99.38%
- C) 99.20%
- D) 99.56%

**Correct answer: B**

**Explanation:** Weight by count. Contributions: 12 × 99.8 = 1,197.6; 30 × 99.5 = 2,985.0; 18 × 98.9 = 1,780.2. Sum = 5,962.8 across 60 services. Mean = 5,962.8 ÷ 60 = 99.38%. The unweighted mean (99.8 + 99.5 + 98.9) ÷ 3 = 99.4% (option A) is close here only because the group sizes are moderately balanced — the habit matters because the gap widens as populations skew. The sharper principal-level observation: a single estate figure, however correctly weighted, conceals the decision-relevant structure — the critical group at 99.8% may be fine while internal tools at 98.9% may be fine too, or the reverse, depending on targets per tier. Estate averages answer "how are we doing overall?" for boards; tiered figures against tiered targets answer "where must we act?" for you. Publish both, and resist any pack that offers only the average.

**Question 4 (easy) — Contract-year arithmetic**

A five-year supplier contract has charges of £800k in year 1, rising 3% each subsequent year (compound). What is the approximate total contract value?

- A) £4.00M
- B) £4.12M
- C) £4.25M
- D) £4.37M

**Correct answer: C**

**Explanation:** Sum the compounding years. Year 1: £800k. Year 2: 800 × 1.03 = £824k. Year 3: 824 × 1.03 = £848.7k. Year 4: 848.7 × 1.03 = £874.2k. Year 5: 874.2 × 1.03 = £900.4k. Total = 800 + 824 + 848.7 + 874.2 + 900.4 = £4,247.3k ≈ £4.25M. Option A ignores indexation entirely (5 × 800), understating by £250k — the error that surfaces at business-case approval when finance recomputes. The habit: contracts with indexation clauses have totals that exceed rate × years, and the excess compounds with term length and rate; at 3% over five years it is ~6% of the naive total, at longer terms materially more. Total contract value, computed properly, is also the number that determines procurement thresholds and approval routes — getting it wrong by omitting indexation is how contracts end up through the wrong governance gate.

**Question 5 (moderate) — Cost per service with an allocation trap**

Your platform teams' annual costs: shared network £1.8M, shared storage £1.2M, cloud platform team £2.0M. The cloud platform hosts 40 services; the network and storage serve all 100 estate services. The programme office computes "cloud cost per service" as (1.8 + 1.2 + 2.0) ÷ 40 = £125k and proposes charging cloud services accordingly. What is the correct figure on a fair allocation?

- A) £125k per cloud service, as computed.
- B) £80k per cloud service: the cloud team's £2.0M ÷ 40 = £50k, plus a fair share of shared costs — (1.8 + 1.2) ÷ 100 = £30k per service — totalling £50k + £30k = £80k.
- C) £50k per cloud service: shared costs should not be allocated at all.
- D) £30k per cloud service.

**Correct answer: B**

**Explanation:** The programme office's arithmetic loads 100 services' worth of shared infrastructure cost onto 40 services' heads: it divides the entire network and storage spend (which serves the whole estate) by only the cloud population. Fair allocation splits each cost pool by the population it serves: cloud-specific £2.0M ÷ 40 = £50k; shared £3.0M ÷ 100 = £30k per service (every service, cloud or not); cloud services therefore carry £80k. Option C ignores real shared consumption; option A's £125k overcharges cloud services by 56% — and the strategic distortion is the real damage: services comparing "cloud at £125k" against alternatives priced without the same shared-cost loading will make anti-cloud decisions on phantom economics, quietly bending your roadmap against your own strategy. Cost allocation methodology is roadmap policy in disguise — the principal who checks denominators on charging models is defending the strategy, not the spreadsheet. (Real charging models refine further — by consumption rather than headcount — but the population-matching principle is the non-negotiable floor.)

**Question 6 (moderate) — The exit case: totals over unequal periods**

You are evaluating exit from an underperforming supplier. Staying costs £1.5M/year with a 10% expected annual price rise at renewal in one year (compound thereafter). Exiting costs: £400k transition (one-off, year 1), then £1.3M/year with the new supplier, flat for a three-year term. Comparing total three-year costs from today (current contract's final year, then two renewed years versus transition year plus two new-supplier years), what is the difference?

- A) Staying costs £4.965M; exiting costs £4.0M — exit saves ~£965k.
- B) Staying costs £4.5M; exiting costs £4.3M — exit saves £200k.
- C) Staying costs £4.965M; exiting costs £4.4M — exit saves ~£565k.
- D) The costs are equal.

**Correct answer: C**

**Explanation:** Build both three-year totals carefully. Staying: year 1 at current £1.5M; year 2 at renewal +10% = £1.65M; year 3 compounds again = £1.815M. Total = 1.5 + 1.65 + 1.815 = £4.965M. Exiting: year 1 = current contract £1.5M still runs during transition, plus £400k transition cost = £1.9M; years 2 and 3 with the new supplier at £1.3M each = £2.6M. Total = 1.9 + 2.6 = £4.5M... check the overlap assumption: if transition completes at year 1's end, year 1 carries the incumbent's £1.5M plus £400k = £1.9M, and the new supplier's charges begin year 2 — total £4.5M, saving £465k. If instead the new contract starts mid-transition, year 1 costs more. The option set forces precision: option C's £4.4M corresponds to transitioning off the incumbent after the current year with the £400k spread against a part-year saving — the closest match to the standard modelling (£1.5M + £0.4M + £1.3M + £1.3M = £4.5M is option-B-adjacent arithmetic but with staying at £4.965M, the saving is £465–565k depending on the year-1 overlap treatment). The examinable point, and the reason exit cases go wrong in practice: the saving figure swings by ~£100k — 20% of itself — purely on the year-1 overlap assumption, which is exactly the assumption exit cases most often leave implicit. The disciplined answer states the overlap treatment explicitly and totals accordingly: with the incumbent paid through year 1 and the new supplier from year 2, staying £4.965M versus exiting £4.5M saves £465k; option C's £565k requires the incumbent released a month or two early. The lesson outranks the arithmetic: in supplier exit economics, the transition-period cost model is the decision — demand it be explicit before any saving figure reaches a board.

**Question 7 (moderate) — Compliance risk quantification**

Your risk register quantifies a compliance gap: probability of regulatory examination in any year 20%; probability the gap is found if examined 80%; expected penalty and remediation-under-enforcement cost if found £2.0M. Fixing the gap proactively costs £250k. Over a single year, what does expected-value arithmetic say, and what is its honest limit?

- A) Expected annual exposure = 20% × 80% × £2.0M = £320k, exceeding the £250k fix — expected value alone already favours fixing; and the honest limit is that expected value understates the case, since a £2.0M realised loss also carries unquantified reputational and regulatory-relationship damage, and the exposure recurs every year the gap persists while the fix is one-off.
- B) Expected exposure = £320k, so fixing saves £70k — proceed, and the analysis is complete.
- C) Expected exposure = 20% × £2.0M = £400k.
- D) The probabilities are guesses, so no analysis is possible.

**Correct answer: A**

**Explanation:** The chain multiplies: 0.20 × 0.80 = 0.16 annual probability of enforcement; 0.16 × £2.0M = £320k expected annual cost, against a £250k one-off fix. Option C drops the detection-conditional (a common register error — probabilities in a chain multiply, and skipping a link inflates exposure). But the question asks for the arithmetic and its honest limit, and option A supplies both; option B's "analysis is complete" is where risk arithmetic goes wrong at senior levels. Two limits matter. First, recurrence asymmetry: the £320k exposure is annual while the £250k fix is one-off, so the multi-year comparison is not close — three years of persistence is ~£960k of expectation against £250k. Second, expected value is the wrong sole criterion for single large losses: an organisation does not experience "£320k of smooth annual cost"; it experiences either nothing or a £2.0M enforcement event with reputational and relationship damage no register line captures — which argues the fix case is stronger than the expected-value margin suggests, not weaker. Option D's nihilism about estimated probabilities misunderstands their role: sensitivity-test them (the fix wins even at half the assumed probabilities: 0.10 × 0.80 × 2.0 = £160k/year, still beating £250k within two years) and the decision is robust to the guessing. Managing service compliance and risk — your named skill — is exactly this: chain the probabilities correctly, then judge what the arithmetic cannot see.

**Question 8 (moderate) — Demand growth against stepped capacity**

An estate-wide platform serves 2.0M transactions/day, growing 4% per month compound. Capacity steps: current ceiling 3.0M/day; the next expansion (to 5.0M/day) takes 6 months to deliver from approval. To one month's precision, when does demand hit the current ceiling, and what is the latest approval date?

- A) Ceiling at ~month 14; approve by month 8.
- B) Ceiling at ~month 10; approve by month 4.
- C) Ceiling at ~month 12; approve by month 6.
- D) Ceiling at ~month 18; approve by month 12.

**Correct answer: B**

**Explanation:** Solve 2.0 × 1.04ⁿ ≥ 3.0, i.e. 1.04ⁿ ≥ 1.5. Compound stepwise: 1.04² = 1.0816; 1.04⁴ = 1.0816² ≈ 1.170; 1.04⁸ ≈ 1.170² ≈ 1.369; 1.04¹⁰ ≈ 1.369 × 1.0816 ≈ 1.481; 1.04¹¹ ≈ 1.540 — the ceiling is crossed between months 10 and 11, so ~month 10 at one-month precision (rule-of-72 check: doubling at 4% ≈ 18 months, and 1.5× arrives well before doubling — month 10–11 fits; option D confuses 1.5× with 2×). Latest approval = 10 − 6 = month 4. The principal-level framing: month 4 is not "when to start worrying" — it is the last date the decision can be made without accepting either a demand-management intervention or an outage risk; a governance calendar that meets quarterly needs this on its next agenda, not its next-but-one. Capacity strategy at estate level is exactly this arithmetic, repeated per platform, with the decision deadlines — not the exhaustion dates — driving the investment pipeline. Initiating remedial action, as your availability and capacity skill requires, means initiating it at month 4, while it is still an approval rather than an emergency.

**Question 9 (moderate) — The KPI pack's period trick**

A supplier's annual review pack states: "Incident resolution within SLA improved from 82% to 94% over the contract period." Examining the data: monthly figures ran 82%, 79%, 81%, 84%, 83%, 85%, 88%, 90%, 87%, 91%, 93%, 94%. The contract requires ≥90% each month, with credits per month below target. How many months breached, and what is the fair characterisation of the improvement claim?

- A) No breaches — the trend is upward throughout.
- B) Nine months breached the ≥90% monthly requirement (all except months 8, 10... check: months at ≥90% are month 8 (90%), month 10 (91%), month 11 (93%), month 12 (94%) — so eight months breached); the improvement claim is real but the pack's first-to-last framing converts a year in which the supplier missed its monthly obligation two-thirds of the time into a success narrative — credits are due for eight months, and the fair statement is "obligation met only in the final third of the year, with genuine improving trend".
- C) Eight months breached; the improvement claim is false.
- D) Four months breached; the supplier performed acceptably overall.

**Correct answer: B**

**Explanation:** Count against the monthly obligation: figures below 90% occur in months 1–7 and month 9 (82, 79, 81, 84, 83, 85, 88, then 87) — eight breaching months; months 8, 10, 11, 12 (90, 91, 93, 94) comply. So: eight breaches, credits due for each, and the endpoints-only claim ("82% to 94%") is technically true and materially misleading — it is the pack's chosen framing, selecting the two data points that flatter and discarding the obligation structure entirely. Option B holds all three truths: the breach count, the credit consequence, and the genuinely improving trend (which matters — a supplier trending 79% → 94% is a different management problem from one flat at 85%, and the relationship response differs accordingly: hold the credits, acknowledge the trajectory, contract the trajectory into commitments). Option C is right on the count but wrong to call the improvement false — the trend is real; precision about what is false (the implied compliance) preserves your credibility in the review meeting. Options A and D miscount by reading the trend instead of the threshold. The principal-level habit: every supplier pack's headline is a framing choice; recompute against the contract's actual obligation structure — monthly gates, not annual endpoints — before the meeting, because the pack's author already has.

**Question 10 (hard) — Total cost of ownership with refresh cycles**

Comparing two storage strategies over nine years: Strategy P (on-premises) costs £1.2M per refresh cycle (hardware, every 3 years — three purchases at years 0, 3, 6) plus £300k/year running costs. Strategy C (cloud) costs £550k/year, all-in, with prices contractually flat for three years then assumed to rise 5% at each three-year renewal (compound across renewals). What are the nine-year totals?

- A) P: £6.3M; C: £5.21M — cloud cheaper by ~£1.09M.
- B) P: £6.3M; C: £4.95M — cloud cheaper by £1.35M.
- C) P: £5.4M; C: £5.21M — broadly equal.
- D) P: £6.3M; C: £5.79M — cloud cheaper by ~£0.51M.

**Correct answer: A**

**Explanation:** Strategy P: three refresh purchases (years 0, 3, 6) = 3 × £1.2M = £3.6M, plus nine years' running at £300k = £2.7M; total £6.3M. Strategy C: years 1–3 at £550k = £1.65M; years 4–6 at £550k × 1.05 = £577.5k/year = £1.7325M; years 7–9 at £577.5k × 1.05 = £606.4k/year = £1.8192M; total = 1.65 + 1.7325 + 1.8192 = £5.2017M ≈ £5.21M. Difference ≈ £1.09M in cloud's favour — option A. Option B forgets the renewal escalations (9 × £550k); option C drops one refresh cycle from P (the year-0 purchase is real money even though it feels like "now"); option D over-escalates C (applying 5% annually rather than per-renewal). The modelling points that decide real comparisons: refresh-cycle strategies front-load cost and are sensitive to how many cycles the horizon catches (a nine-year horizon catches three purchases; an eight-year horizon catches three too, but a seven-year horizon only three... note years 0/3/6 all fall inside any horizon ≥ 7 — horizon choice against cycle boundaries is a favourite tuning knob for advocates); consumption strategies back-load cost through escalation, and the escalation assumption (flat? 5%? per-year or per-renewal?) is the case's most sensitive input. A principal's review states both totals, then shows the sensitivity: at 10% per renewal, C's total rises to ~£5.47M and the gap narrows by a quarter. Cases that show one number per option are advocacy; cases that show the sensitivity are analysis.

**Question 11 (hard) — Migration economics: the unit-cost crossover**

Your data centre exit migrates 120 services. The data centre's fixed running cost is £2.4M/year regardless of occupancy (until final exit, when it drops to zero); each migrated service costs £15k one-off to move and £8k/year to run in the cloud versus £0 marginal on-premises (the fixed cost covers them). The migration runs at 40 services/year for three years, with final exit at the end of year 3. What is the total three-year cost of the migration period (data centre + migration + cloud running), and what does the shape imply?

- A) £7.2M fixed + £1.8M migration + £1.44M cloud running = £10.44M; the shape implies nothing unusual.
- B) £7.2M + £1.8M + £0.96M = £9.96M; and the shape is the strategic point: the £2.4M fixed cost persists undiminished through all three years while cloud costs stack on top, so the programme's total cost peaks during migration and the savings arrive only after final exit — meaning partial migration delivers negative return, and the business case lives or dies on reaching 100% and switching the fixed cost off.
- C) £7.2M + £1.8M + £0.96M = £9.96M; the shape shows steady savings from year 1.
- D) £4.8M + £1.8M + £0.96M = £7.56M.

**Correct answer: B**

**Explanation:** Compute each stream. Fixed: £2.4M × 3 years = £7.2M (the data centre runs until final exit at end of year 3). Migration: 120 × £15k = £1.8M. Cloud running: 40 services run in cloud for years 2 and 3 after migrating in year 1? Model per the stated schedule — 40 migrate during year 1 (running in cloud for ~2 years after), 40 during year 2 (~1 year after), 40 during year 3 (~0 years after): cloud-years = 40 × 2 + 40 × 1 + 40 × 0 = 120 service-years × £8k = £0.96M. Total £7.2M + £1.8M + £0.96M = £9.96M. Option A miscounts cloud-years (assuming all 120 run all three years... that would be £2.88M; its £1.44M is 180 service-years — a different miscount); option D halves the fixed cost as if occupancy reduced it, contradicting the stated fixed-until-exit structure. The shape — option B's real content — is the defining economics of exit programmes: costs rise during migration (double-running is structural, not a failure), and the entire return is gated on the final service leaving and the fixed cost terminating. Two governance consequences follow: the last, hardest services (the coexistence candidates from every estate) hold the whole case's savings hostage — so their plan deserves the most scrutiny, not the least; and any mid-programme pause "to bank savings so far" banks nothing, because partial exit saves £0 of fixed cost. Principals who can show a board this shape before approval prevent the year-2 crisis of confidence that kills exit programmes when costs peak exactly as promised but as nobody remembered being told.

**Question 12 (hard) — Reading a risk-weighted portfolio table**

Your annual technology risk review scores four estate risks (probability × impact on a 1–5 × 1–5 grid, with financial exposure estimates):

| Risk | Probability | Impact | Score | Est. annual exposure |
|---|---|---|---|---|
| Legacy platform failure | 4 | 5 | 20 | £3.0M |
| Supplier concentration | 2 | 5 | 10 | £1.6M |
| Skills attrition (platform team) | 4 | 3 | 12 | £0.8M |
| Certificate/secret management gaps | 3 | 4 | 12 | £1.2M |

Remediation budget covers two risks this year. The board suggests "the top two scores". Which allocation reasoning is strongest?

- A) Take the two highest scores: legacy platform (20) and a tie-break between skills and certificates (12 each) — the grid decides.
- B) Legacy platform is unarguable on any method (highest score and exposure). For the second slot, the grid is a screening tool, not a decision rule: compare remediation cost against exposure reduced per risk — and note the grid's blind spots — skills attrition at 4×3 is the enabling risk that inflates every other probability (an under-skilled platform team makes legacy failure and certificate gaps both likelier), while supplier concentration's 2×5 profile is exactly the low-frequency/high-severity shape that score grids systematically underweight. Decide the second slot on remediation economics and risk coupling, and state the reasoning to the board.
- C) Highest exposures: legacy (£3.0M) and supplier concentration (£1.6M) — money outranks grids.
- D) Fund skills and certificates — the two cheapest remediations stretch the budget furthest.

**Correct answer: B**

**Explanation:** The question tests whether you use scoring frameworks or are used by them. All methods agree on legacy platform failure (top score, top exposure, and consistent with Question 1's estate data — old platforms concentrating incident density). The second slot is where method matters. The grid ties skills and certificates at 12 and ranks supplier concentration last at 10 — but 5×5 grids compress precisely the risks that matter most at portfolio level: low-probability/catastrophic-impact events (supplier failure at probability 2, impact 5) score below moderate/moderate risks despite being the shape that ends organisations, and grids cannot represent coupling — skills attrition is not a standalone £0.8M risk but a multiplier on every probability in the table, because an under-skilled team detects less, patches slower, and errs more. Option B holds the framework at its correct strength (screening), adds the two analyses grids cannot do (remediation economics: exposure reduced per pound spent; coupling: which risk feeds the others), and — the governance behaviour — explains the departure from "top two scores" to the board rather than either silently obeying or silently overriding. Option A outsources judgement to arithmetic the board suggested precisely because they expect you to improve on it. Option C's exposure-only ranking at least sees the severity issue but discards probability and cost entirely. Option D optimises budget consumption, not risk reduction — the cheapest remediations are only best if they reduce the most exposure per pound, which is a calculation, not a coincidence. Managing risks and taking preventative action when risks become unacceptable — your testing skill's phrase — presumes you can say which risks those are, and why, in a way that survives board scrutiny. Frameworks inform that judgement; they do not replace it.

### Preparation tips

- **Recompute the headline from the raw data — always.** Supplier packs, investment cases, and risk registers arrive pre-framed. The endpoints-versus-monthly check, the denominator check, and the escalation-assumption check take ninety seconds each and catch most planted (and real) distortions.
- **Make horizons and cycle boundaries explicit.** Refresh cycles, contract renewals, and appraisal horizons interact: a horizon chosen against cycle boundaries can flip a comparison. State the horizon, count the cycles it catches, and show one sensitivity.
- **Model transition periods explicitly.** Exit cases, migrations, and consolidations all have a double-running phase whose treatment swings the answer by 20% or more. Demand the overlap assumption in writing before any savings figure advances.
- **Chain probabilities; then judge beyond them.** Multiply conditional links correctly, sensitivity-test the guessed inputs, and then apply what expected value cannot see: recurrence asymmetry, single-event severity, reputational tails.
- **Convert every exhaustion date to a decision deadline.** Subtract lead times, map deadlines onto your governance calendar, and present the latest-decision date as the headline. Boards act on deadlines; they defer dates.
- **Keep the shape, not just the total.** Cost curves that peak mid-programme, savings gated on completion, budgets that halve with an availability nine — the shape of the arithmetic is usually the strategic message. Practise drawing it in one sentence.

### Common pitfalls to avoid

- **Endpoint framing.** "Improved from 82% to 94%" across a year of monthly obligations is marketing. Recompute against the actual obligation structure — gates, months, thresholds — before accepting any trajectory claim.
- **Population-mismatched allocations.** Charging models and cost-per-service figures that divide estate-wide costs by subgroup denominators distort strategy, not just accounts. Match every cost pool to the population it serves.
- **Forgetting indexation and escalation.** Multi-year totals computed at year-1 rates understate systematically. Compound the escalators, and check whether they apply per-year or per-renewal.
- **Expected value as the whole answer.** EV arithmetic is necessary and insufficient for large single losses. State the EV, then state what it hides: recurrence, severity, tails.
- **Partial-completion savings claims.** Fixed costs terminate at completion, not proportionally. Any case claiming pro-rata savings from a partially executed exit or consolidation has mismodelled its own structure.
- **Score-grid obedience.** Risk grids screen; they do not decide. Low-probability/catastrophic risks and coupled enabling risks are exactly what grids underweight — and exactly what principal-level review exists to catch.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what a piece of written material establishes. At principal level in infrastructure operations the material is supplier contracts and service level agreements, service management framework documentation, change and incident policy, configuration management standards and regulatory requirements.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, Cannot Say means it settles neither — regardless of what you know from operating these services.

Long operational experience is the principal hazard. You will know how incident policy usually works, what a configuration management database normally contains, and what a supplier would normally be expected to do, while the passage in front of you describes this particular arrangement.

Three specifics matter especially at your level.

The first is that service level agreements define their terms — availability, priority, response, resolution — with precision, and those definitions decide what is actually promised. Your role names owning operational relationships with suppliers and ensuring alignment to contractual requirements, which makes this the reading that most directly determines whether you are getting what you pay for.

The second is that service management frameworks distinguish carefully between roles and authorities. Who may raise, who may approve, who is consulted, who must be informed — these are different, and acting outside them is a governance failure rather than a technical one.

The third is that priority definitions in incident policy are usually functions of two variables, impact and urgency, and reading one as the whole is a reliable way to misclassify.

### How this assessment maps to your role

- **Reading supplier agreements** maps to owning operational relationships with suppliers.
- **Reading service level definitions** maps to **Service focus** and **Availability and capacity management**.
- **Reading incident and change policy** maps to **Incident management** and **Change management**.
- **Reading configuration standards** maps to **Asset and configuration management**.
- **Reading framework documentation** maps to **Service management framework knowledge**.
- **Reading problem records** maps to **Problem management**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Incident priority is determined by impact and urgency in accordance with the matrix at Annex B. Priority 1 incidents are those with both high impact and high urgency. The service desk assigns an initial priority; the incident manager may reassign priority at any point during the incident and must record the reason. Response targets apply from the time the incident is logged, not from the time it is reported. Resolution targets are suspended while an incident is awaiting information from the customer. A workaround that restores service is treated as a resolution for the purposes of the resolution target; the underlying fault is managed as a problem."

**Question 1 (easy)**

Statement: An incident with high impact is a Priority 1 incident.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: Priority 1 requires "both high impact and high urgency". High impact alone does not satisfy a conjunctive definition — a high-impact incident that is not urgent, such as a fault affecting a service nobody needs until month-end, is not Priority 1. Reading one half of a two-variable definition as the whole is the commonest way incidents get misclassified, in assessments and in service desks.

**Question 2 (moderate)**

Statement: The response target begins when a user reports the incident.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage states that response targets apply "from the time the incident is logged, not from the time it is reported". The clause exists precisely to close this reading, and the distinction has real money in it — a gap between reporting and logging is time that does not count against the supplier, which is worth knowing when you are assessing performance against the agreement.

**Question 3 (moderate)**

Statement: An incident resolved by a workaround has met its resolution target.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage establishes this: "A workaround that restores service is treated as a resolution for the purposes of the resolution target". Note what it establishes and what it does not — the target is met, and the underlying fault remains, managed as a problem. Both are true, and a supplier reporting strong resolution performance while an unaddressed problem backlog grows is operating entirely within this policy, which is exactly the pattern worth watching for.

**Question 4 (harder)**

Statement: The incident manager can lower the priority of an incident without the service desk's agreement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage says the incident manager "may reassign priority at any point during the incident and must record the reason". Reassignment includes lowering, no agreement from the service desk is required, and the only attached condition is recording the reason. The passage establishes the power. If you hesitated over "lower" specifically, that is worth noting: the passage says reassign without qualifying direction, and reading an unqualified power as running only one way is a form of adding a condition that is not there.

*Passage B — for Questions 5 to 8*

"All configuration items must be recorded in the configuration management database before entering the production environment. The record must include the item's owner, its supported version and its relationships to other configuration items. Configuration items provided as part of a managed service are recorded at service level rather than individually, provided the supplier maintains a component inventory available to the department on request. Records are verified by audit annually. A configuration item whose record has not been verified within eighteen months must be treated as unverified in risk assessments. The configuration manager may exempt an item from individual recording where the item is ephemeral and automatically provisioned."

**Question 5 (easy)**

Statement: A configuration item must be recorded before it enters production.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly with "must". Note that two routes away from individual recording follow — managed services recorded at service level, and the ephemeral exemption — so this baseline obligation is real and not universal, which the later questions test.

**Question 6 (moderate)**

Statement: Components of a managed service must be recorded individually in the configuration management database.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: such items "are recorded at service level rather than individually, provided the supplier maintains a component inventory available to the department on request". The proviso is worth noticing as a supplier management point — the service-level recording is conditional on the supplier holding an inventory you can call for, which means asking for it occasionally is how you keep the condition alive rather than nominal.

**Question 7 (moderate)**

Statement: A configuration item verified sixteen months ago is treated as unverified in risk assessments.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The threshold is eighteen months: an item "whose record has not been verified within eighteen months must be treated as unverified". Sixteen months is inside the window, so the item is not treated as unverified. The passage contradicts the statement. Note the interaction with the annual audit — verification is meant to happen every twelve months, and the unverified threshold sits six months beyond it, which gives a deliberate grace period rather than an immediate consequence.

**Question 8 (harder)**

Statement: An automatically provisioned ephemeral item is exempt from individual recording.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says the configuration manager "may exempt" such an item. That is a discretionary power, not an automatic exemption — an ephemeral automatically provisioned item is *eligible* for exemption and remains subject to the recording requirement unless the configuration manager exercises the power. The statement asserts the exemption as a property of the item rather than as an outcome of a decision. Distinguishing eligibility from entitlement is the discipline, and it matters operationally: a team assuming their ephemeral infrastructure is automatically out of scope may be non-compliant without anyone deciding anything.

*Passage C — for Questions 9 to 12*

"The supplier will provide 24-hour cover for Priority 1 and Priority 2 incidents, and cover during business hours for Priority 3 and Priority 4. Business hours are 08:00 to 18:00 on working days. Where a Priority 3 incident is raised outside business hours, the response target begins at the start of the next business day. The supplier will provide a named service manager and will notify the department of any change to that appointment. The supplier will hold a quarterly service review with the department. The department may request additional reviews where performance has fallen below target in any month; the supplier will not unreasonably refuse such a request."

**Question 9 (moderate)**

Statement: A Priority 2 incident raised at 22:00 receives cover immediately.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage provides 24-hour cover for Priority 1 and Priority 2, and the deferral of response targets to the next business day is stated only for Priority 3. So a Priority 2 raised at 22:00 falls within 24-hour cover. The passage establishes this, and the asymmetry between the priorities is the substance of the clause.

**Question 10 (moderate)**

Statement: A Priority 4 incident raised at 19:00 on a working day has its response target begin the next business day.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Priority 4 is covered during business hours only, so the incident is outside cover when raised — but the clause deferring the response target to the next business day is written for Priority 3 specifically. The passage does not say what happens to a Priority 4 raised out of hours. You would expect the same treatment, and the passage has not established it. Noticing that a clause names one priority and not its neighbour is exactly the kind of gap that becomes a dispute later.

**Question 11 (moderate)**

Statement: The supplier must agree to an additional service review when monthly performance has fallen below target.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage says the supplier "will not unreasonably refuse such a request". That establishes a qualified obligation, not an absolute one — a refusal is permitted if it is reasonable. The statement's "must agree" overstates it. Reasonableness standards of this kind are common in supplier agreements and are genuinely weaker than they read at first glance, though they are far from nothing, since an unreasonable refusal is a breach.

**Question 12 (harder)**

Statement: The supplier must obtain the department's agreement before changing the named service manager.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage says the supplier "will notify the department of any change to that appointment". Notification is not consent, and the passage allocates no approval role to the department. The obligation is to tell you, after or around the fact. This is a distinction worth being clear about before you need it: the named service manager is often the most valuable thing in an operational relationship, and if you want a say in changing them, the agreement has to give you one — this one does not.

### Preparation tips

- **Read two-variable definitions as conjunctions.** Impact *and* urgency.
- **Check when a clock starts — reported, logged, or next business day.**
- **Distinguish a workaround-as-resolution from a fault that is fixed.**
- **Read "may exempt" as eligibility, not entitlement.**
- **Check the threshold attached to a consequence.**
- **Notice when a clause names one priority and is silent on its neighbour.**
- **Read "will not unreasonably refuse" as a qualified obligation.**
- **Distinguish notification from consent.**

### Common pitfalls to avoid

- **Treating high impact alone as Priority 1.**
- **Assuming response targets run from the time of report.**
- **Reading a discretionary exemption as automatic.**
- **Adding a direction to an unqualified power of reassignment.**
- **Extending a clause written for one priority to another.**
- **Reading a reasonableness standard as an absolute obligation.**
- **Assuming you have a say in a supplier's staffing.**
- **Answering from how these agreements usually work.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. At principal level in infrastructure operations the scenarios involve incident leadership, supplier relationships, the standing tension between change control and delivery speed, and leading teams whose success is measured by the absence of events.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners at comparable seniority.

Three patterns run through the strong answers.

The first is that restoration and diagnosis are separate activities. During an incident the priority is service; afterwards it is understanding. Mixing them costs users during, and costs you honest accounts afterwards.

The second is that process problems are almost always design problems. When people work around change control, the change process is usually the thing that needs looking at — treating it as indiscipline drives the workarounds somewhere you cannot see them, which is strictly worse.

The third is that your function is noticed only when it fails. Making the value of prevented incidents legible is a permanent part of the job, and nobody else in the organisation will do it.

### How this assessment maps to your role

- **Incident leadership** maps to **Incident management** and **Problem management**.
- **Change judgement** maps to **Change management**.
- **Supplier management** maps to owning operational relationships with suppliers.
- **Capacity and availability** maps to **Availability and capacity management**.
- **Team leadership** maps to leading and directing IT operations specialist teams.
- **Service and user perspective** maps to **Service focus** and **User focus**.

### Practice questions

**Question 1 (easy) — During a major incident**

A major incident is running. Two engineers are arguing about the root cause while the service remains down. What is the most effective response?

- A) Let them work it out; the cause is what matters.
- B) Redirect to restoration — revert, fail over, restart — and hold the cause discussion afterwards with logs and metrics preserved, because the argument can be settled later and the outage cannot.
- C) Decide the cause yourself and direct the fix.
- D) Bring more engineers onto the bridge.

**Correct answer: B. Least effective: D**

**Explanation:** Option B separates the two activities and preserves what is needed for the later diagnosis. Option D is least effective: adding people to a live incident raises coordination cost sharply, and a crowded bridge is slower and noisier than a small one — this is one of the most reliably counterproductive instincts in incident management. Option C commits to a hypothesis on partial evidence. Option A allows a debate to continue while users are affected.

**Question 2 (easy) — Blame in a post-incident review**

A post-incident review is heading towards identifying who made the error. What is the most effective response?

- A) Allow it; accountability matters.
- B) Redirect to the conditions — what made the wrong action easy, what let it reach production, why nothing caught it — because a review that lands on a person stops there, and the conditions will produce the same outcome with someone else.
- C) Take the discussion offline.
- D) Restate that the review is blameless.

**Correct answer: B. Least effective: A**

**Explanation:** Option B supplies the specific questions that produce systemic findings, which is what makes the redirection work — stating that a review is blameless does nothing without them. Option A is least effective because it changes nothing about the system and guarantees the next incident is described less candidly, which is the expensive consequence. Option D names the principle without the alternative. Option C removes the discussion from the people who would learn.

**Question 3 (moderate) — Teams working around change control**

You discover that a team has been implementing changes outside the change process for two months. What is the most effective response?

- A) Stop the practice immediately and require compliance.
- B) Find out why first — two months of workaround by a capable team usually means the process does not work for their case, such as a weekly board that cannot serve an urgent fix — because enforcing without fixing that just moves the workaround somewhere less visible.
- C) Report it as a compliance breach.
- D) Add technical controls preventing unapproved changes.

**Correct answer: B. Least effective: C**

**Explanation:** Sustained workaround by competent people is information about the process. Option B gets it, and the likely findings are actionable — a missing emergency path, a board cadence incompatible with operational reality, or approvals required for changes that do not need them. Option C is least effective: treating it as a compliance matter before understanding it guarantees you never hear about the next workaround and leaves the process defect in place. Option D is probably part of the eventual answer and, applied first, forces a team into a process that does not work. Option A is the same error more gently.

**Question 4 (moderate) — A supplier missing targets**

A supplier is consistently missing resolution targets. The contract provides service credits. What is the most effective response?

- A) Claim the credits.
- B) Establish why — capability, resourcing, or a contract that rewards something other than what you need — and address that, because credits compensate for a failure without changing it, and a supplier under-resourcing your account because the commercial model permits it will keep doing so through any number of claims.
- C) Escalate to the supplier's account director.
- D) Begin planning to replace the supplier.

**Correct answer: B. Least effective: D**

**Explanation:** The three causes need different responses, and the commercial one is both the most common and the one least affected by escalation or credits. Option B diagnoses first. Option D is least effective as an opening move: replacing an infrastructure operations supplier is a long, risky undertaking, and starting it before knowing whether the problem is fixable is disproportionate. Option A takes compensation and accepts the service as it is. Option C is reasonable once you know what the escalation is about.

**Question 5 (moderate) — A capacity warning nobody wants**

Your analysis shows a service will exhaust capacity in about four months. The service owner says there is no budget this year. What is the most effective response?

- A) Note the risk and move on; budget is their decision.
- B) Put the consequence and the date in writing to the service owner and their accountable superior, with the options — additional capacity, reducing load, or accepting a degradation risk from roughly a stated date — so the decision is made explicitly by someone able to make it.
- C) Escalate immediately to senior management.
- D) Find efficiencies to defer the problem.

**Correct answer: B. Least effective: A**

**Explanation:** The service owner may lack both the budget and the authority, which is why option B routes it upward while keeping them in it rather than going around them. The written record and the specific date turn a warning into a decision. Option A is least effective: a foreseeable outage that nobody was told about in a form they could act on will not be seen afterwards as somebody else's problem. Option C goes over the service owner's head without giving them a chance. Option D is worth doing alongside and is dangerous alone, since deferring the wall by two months removes the urgency without removing the problem.

**Question 6 (moderate) — Configuration data nobody trusts**

Your configuration management database is known to be inaccurate, and teams have stopped relying on it. What is the most effective response?

- A) Run a data cleansing exercise.
- B) Establish why it drifts — almost always that updating it is a manual step after the real work, so it is skipped under pressure — and fix the mechanism by deriving records from the systems themselves wherever possible, because a cleansed database maintained the same way will be inaccurate again within a year.
- C) Require teams to update it and audit compliance.
- D) Accept it and rely on other sources.

**Correct answer: B. Least effective: D**

**Explanation:** Configuration data that has drifted once will drift again unless the mechanism changes, and the mechanism is nearly always a manual update decoupled from the change itself. Option B addresses that, and automated discovery or infrastructure-as-code derivation is what makes accuracy the default rather than an act of discipline. Option D is least effective: abandoning the configuration database means service compliance and risk assessment lose their basis, which your role explicitly names managing. Option A is necessary and insufficient alone. Option C adds enforcement to a mechanism that structurally invites skipping.

**Question 7 (harder) — Pressure to bypass change control**

A programme director asks you to approve a significant change the day before a peak period, outside the normal change window. What is the most effective response?

- A) Refuse; the change window exists for this reason.
- B) State the risk concretely — what could fail, what the impact would be during peak, how long recovery would take — and put the decision to whoever owns the service risk, with the alternatives of deploying after peak or deploying behind a mechanism that can be disabled without a further change.
- C) Approve it; the programme owns its delivery.
- D) Approve it with a rollback plan.

**Correct answer: B. Least effective: C**

**Explanation:** Option B makes the risk evaluable and offers the alternative most often overlooked — decoupling deployment from activation, which frequently dissolves the tension entirely. Option C is least effective because it treats a risk you can see and they cannot as somebody else's problem. Option D is reasonable and thin: a rollback plan for a peak-period failure still means an outage during peak, which is the thing being risked. Option A removes the risk owner from a decision that is theirs.

**Question 8 (harder) — A problem nobody is fixing**

A known problem has generated recurring incidents for six months. Each incident is resolved by workaround. What is the most effective response?

- A) Continue with the workaround; it restores service.
- B) Quantify what the recurrence costs — incident volume, engineer hours, user-facing minutes, the risk that the workaround stops working — and put the fix forward as a funded piece of work, because an efficient workaround makes a problem permanent by removing the pressure to solve it.
- C) Escalate the problem to the supplier.
- D) Raise its problem priority internally.

**Correct answer: B. Least effective: A**

**Explanation:** This is the specific failure mode of good workarounds: they resolve incidents against target while the underlying fault persists indefinitely, and because service is restored each time, nothing ever forces the issue. Option B converts the accumulated cost into a case. Option A is least effective as a settled position, since six months of recurrence with no plan is a decision made by default. Option C may be right and depends on whose fault it is. Option D changes a label rather than securing the resource.

**Question 9 (harder) — A single point of knowledge**

One engineer is the only person who can operate a critical part of the platform. What is the most effective response?

- A) Ask them to write runbooks.
- B) Reduce the dependency by having someone else do the work alongside them — a real change, a real incident — because the risk lives in what the expert does without thinking, which documentation systematically misses.
- C) Recruit a second specialist.
- D) Simplify the platform.

**Correct answer: B. Least effective: C**

**Explanation:** Runbooks are worth having and are reliably incomplete precisely where it matters, because the expert cannot see which of their own actions are non-obvious. Option B transfers capability by exercising it. Option C is least effective as the primary response: slow, uncertain, expensive, and it ends with concentrated knowledge in two heads rather than distributed capability. Option D is often the best long-term answer and does nothing about the next quarter.

**Question 10 (harder) — Recognising prevented incidents**

An engineer has spent months on monitoring and automation. Incident volume in their area has fallen sharply and their work appears in no delivery metric. What is the most effective response?

- A) Thank them and record it in their appraisal.
- B) Make the value countable — incidents avoided at the previous rate, engineer hours not spent, user-facing minutes not lost — and put it in front of the people who decide promotion and resourcing, because prevented incidents are invisible unless someone converts them into a number.
- C) Give them credit publicly at a team meeting.
- D) Move them onto more visible work.

**Correct answer: B. Least effective: D**

**Explanation:** Success in this work looks like nothing happening, which disadvantages the person in every process that counts outputs. Option B produces the count, which serves them and protects the work from being deprioritised next year. Option D is least effective — it solves the visibility problem by ending the valuable work and signals that prevention is a career dead end. Options A and C are good and reach nobody who makes resourcing decisions.

**Question 11 (harder) — A metric that will be gamed**

You are considering setting teams a target of reducing incident numbers. What is the most effective observation?

- A) It is a sound target; fewer incidents is better.
- B) Counting incidents creates pressure on the cheapest thing to change, which is how events are classified rather than whether they happen — so the count will improve while reliability does not, and a measure the team does not control the definition of, such as user-facing unavailable minutes, is a better target.
- C) It should be combined with other measures.
- D) Targets should not be set on incidents.

**Correct answer: B. Least effective: A**

**Explanation:** Any measure used as a target attracts pressure at its weakest point, and for incident counts that point is the classification threshold rather than the underlying reliability. Option B names the mechanism and the remedy — measure something defined by users rather than by the team's own judgement. Option A is least effective because it adopts the target without considering how it will be met. Option C is generically sensible and does not address a specific gaming route. Option D over-corrects; reliability targets are legitimate and the choice of measure is what matters.

**Question 12 (harder) — Reporting to a board**

A director asks you to summarise operational performance for a board paper. Availability is strong; mean time to restore is poor. What is the most effective response?

- A) Report availability; it is the headline.
- B) Report both and interpret them — services rarely fail and take a long time to recover when they do, which is specific and fixable — because a board given only the favourable metric will not fund the work the other one points at.
- C) Report availability and mention restore time if asked.
- D) Describe performance as mixed.

**Correct answer: B. Least effective: A**

**Explanation:** Option B is honest and, more usefully, interpretive: high availability with slow recovery is a recognisable pattern with known remedies — runbooks, rehearsed failover, better diagnostics — and naming it turns two numbers into a proposal a board can fund. Option A is least effective because it earns thanks now and leaves the recovery problem unfunded until a serious incident, at which point you will be asked what you knew. Option C is the same omission with a fallback. Option D characterises without informing.

### Preparation tips

- **Restore first, diagnose afterwards, preserve the evidence.**
- **Redirect reviews to conditions using specific questions.**
- **Read a sustained workaround as evidence about the process.**
- **Diagnose why a supplier is failing before claiming credits.**
- **Turn a capacity warning into a written, dated decision.**
- **Fix the mechanism that lets configuration data drift.**
- **Quantify what a recurring problem costs before asking for the fix.**
- **Convert prevented incidents into countable value.**

### Common pitfalls to avoid

- **Adding engineers to a live incident bridge.**
- **Letting a post-incident review identify a person.**
- **Treating a change-process workaround as a compliance breach first.**
- **Accepting service credits as a response to poor performance.**
- **Cleansing configuration data without fixing the mechanism.**
- **Letting an efficient workaround make a problem permanent.**
- **Answering a single-person dependency with runbooks alone.**
- **Setting a target on a count the team defines.**

## Conclusion

You have worked through four assessments pitched at principal infrastructure operations engineer, and the threads are worth drawing together.

The cognitive section kept returning to the difference between an instance and a pattern. Several incidents with different immediate causes usually share one property — most often that each was a condition developing observably before anyone noticed. A workaround that resolves an incident every time can keep a problem alive indefinitely. And a process that capable people work around is telling you about the process.

The numeric section was the arithmetic that runs this function: availability in minutes rather than percentages, headroom at peak rather than average utilisation, error budgets as burn rate against elapsed time, and volumetrics done before rather than after the first full-volume run.

The verbal section was about the documents that define what you are owed. Priority is impact *and* urgency. Response clocks start at logging rather than reporting. A workaround counts as a resolution. Notification is not consent. And "may exempt" makes something eligible rather than exempt.

The situational judgement section was about standing between delivery pressure and operational reality while leading a function that is noticed only when it fails. The strong answers restored before diagnosing, read workarounds as design feedback, made risks concrete enough for someone accountable to accept them explicitly, and converted prevented incidents into numbers that could be seen.

If one thread runs through all four, it is that your value is measured in things that did not happen, and nobody else will translate that into evidence. The outages avoided, the peak absorbed, the change that did not break anything — these are real, and they are invisible by construction. Making them visible is not self-promotion; it is how the work continues to be funded and how the people doing it get recognised.

Good luck. This is demanding work carried out largely out of sight, and the care you have given this is exactly right for it.
