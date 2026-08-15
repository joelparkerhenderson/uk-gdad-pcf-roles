# Principal Application Operations Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created for you as a principal application operations engineer working within the UK Government Digital and Data profession. At your level, the role is organisational as much as technical: you own the application strategy outright; you lead on resourcing, learning and development for your team; you carry accountability for vendor and supplier management; you bring expert technical understanding — including the direction of future technologies — to bear on decisions whose consequences run for years; and you remain close enough to delivery to manage aspects of an application when a project's complexity and business impact demand your direct involvement. Whether you are preparing for a senior selection process, benchmarking yourself against the capability framework, or modelling deliberate professional practice for the leaders you are developing, this document offers structured, role-specific material to practise with.

Psychometric assessments are structured, standardised exercises measuring the cognitive capabilities and professional judgement that predict success in a role. At principal level, the relevant assessments are emphatically not abstract puzzles: they draw on the artefacts and decisions that fill your actual working month — multi-year strategy papers, supplier performance regimes and contract clauses, portfolio risk and compliance positions, capacity investment cases, workforce and skills plans, governance submissions, and the incident and problem records of an estate you answer for. The four assessment types covered here — cognitive, numeric reasoning, verbal reasoning, and situational judgement — map onto the four faces of principal-level work: structured reasoning across systems, quantitative command of investment and performance, precise reading and writing of binding text, and judgement where strategy, people, suppliers, and integrity intersect.

Why practise, at your level? Three reasons. First, senior selection processes in government genuinely use these instruments, often with demanding norm groups, and familiarity converts ability into demonstrated ability. Second, the skills they measure are perishable: fluency with compounding forecasts, clause-level reading, and disciplined inference all sharpen with deliberate use and dull without it. Third — and perhaps most valuable — working through well-constructed scenarios with full reasoning is a rehearsal of the judgement your role exists to supply, and several of the scenarios in this guide are designed to be worth discussing with the leads and senior engineers you develop: calibrating their judgement is part of your resourcing and development remit, and these materials can serve it.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and its typical format, a mapping of its dimensions to the named skills in your role summary, a substantial set of practice questions with fully worked explanations, practical preparation tips, and common pitfalls to avoid. Attempt each question honestly, commit before reading the explanation, and interrogate the reasoning even where you agree with the answer — especially where you agree with the answer. The habit of auditing one's own agreement is, at principal level, the difference between experience and expertise.

Take your time. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using practical scenarios rather than abstract puzzles. At principal level, it presents the materials of strategic operations — portfolio risk matrices, supplier performance data, technology roadmaps, capacity investment options, governance rules — and asks you to reason about them with speed and precision: recognising patterns across services and years, deducing consequences from interacting policies and contracts, detecting the inconsistency buried in a compliance return, prioritising across a portfolio, and solving problems whose constraints span technology, commercial terms, and people.

The typical format is an online, timed test of 15 to 30 minutes with 20 to 30 questions of graduated difficulty, scored objectively against a norm group — for senior roles, often a demanding one. Adaptive platforms adjust difficulty to performance, and employers typically receive a speed-versus-accuracy profile. Principal-level question design favours multi-step, multi-source reasoning: reconciling a rule set with a dataset, tracing a decision's consequences through several systems, and identifying which of several defensible-sounding conclusions actually follows.

For your role, the relevance is direct. Owning the application strategy means deducing where technology directions, supplier lifecycles, and departmental mandates converge — and where they collide. Accountability for supplier management means reasoning precisely from contract and performance data. Seeing the bigger picture across groups of services — your **Service focus** skill — is pattern recognition at portfolio scale. And ensuring the right actions are taken on problems means auditing other people's reasoning as often as producing your own: a principal's cognitive errors are rarely private, because an organisation is downstream of them.

### How this assessment maps to your role

- **Pattern recognition** maps to **Service focus** and **Problem management**: taking groups of services and investigating how to get the best of underlying services means seeing shared structure — common dependencies, correlated failures, duplicated capability — across an estate; anticipating problems means seeing the pattern before it completes.
- **Logical deduction** maps to **Change management** and your vendor accountability: managing high-impact, complex change requests and reasoning from contract terms both require deriving exactly what rules permit, require, and imply — no more, no less.
- **Error checking** maps to **Asset and configuration management**: managing service compliance and risk means detecting the return, record, or attestation that contradicts reality or itself — at portfolio scale, where errors hide in aggregation.
- **Prioritisation** maps to **Ownership and topic** and **Availability and capacity management**: accountability across an estate demands defensible ranking of competing risks, and initiating remedial action means knowing which capacity issue moves first.
- **Applied problem solving** maps to **Technical specialism** and **Testing**: delivering a model to support future technologies alongside coexisting databases, and managing risks with preventative action when they become unacceptable, are constraint-satisfaction problems spanning years and budgets.

### Practice questions

**Question 1 (easy) — Pattern recognition across a service group**

Reviewing annual incident summaries for the five services in your group, you note the services' major-incident counts and their underlying platforms:

| Service | Major incidents | Database platform | Hosting |
|---|---|---|---|
| Casework | 6 | Platform D1 | On-premise |
| Grants | 1 | Platform D2 | Cloud |
| Licensing | 5 | Platform D1 | Cloud |
| Referrals | 7 | Platform D1 | On-premise |
| Notifications | 1 | Platform D2 | Cloud |

Which factor most plausibly warrants investigation as the common thread?

- A) Hosting location — on-premise services have more incidents.
- B) Database platform — all three high-incident services share Platform D1, while both D2 services had one incident each, and D1's association holds across both hosting types.
- C) Service size — bigger services have more incidents.
- D) Nothing — five services is too small a sample for any conclusion.

**Correct answer: B**

**Explanation:** Test each candidate factor against the whole table. Hosting (A) fails on Licensing: a cloud-hosted service with 5 major incidents breaks the on-premise pattern, while Grants and Notifications (cloud, 1 each) only ever supported it weakly. Platform (B) is consistent across every row: the three D1 services account for 18 of 20 major incidents, and — decisively — the association survives the hosting split, appearing in both on-premise and cloud contexts, which is what distinguishes a candidate common cause from a confounded one. Service size (C) is not in the data at all; importing it is speculation. Option D mistakes investigation for conclusion: five services cannot *prove* causation, but your **Problem management** duty — ensuring the right actions are taken to investigate and anticipate problems — requires exactly this: forming the best-supported hypothesis and directing investigation at it. This is portfolio-level pattern work, your **Service focus** skill in action: individual service teams each see their own incidents; only the principal sees the column that lines up.

**Question 2 (easy) — Deduction from contract and policy together**

Your supplier contract states: "Scheduled maintenance requires 10 working days' notice to the customer." Your department's policy states: "No supplier maintenance may occur during the last five working days of a financial quarter." The supplier emails notice on 20 March (a Monday) of maintenance planned for 3 April. The financial quarter ends 31 March. Assume all weekdays are working days. Which statement must be true?

- A) The maintenance breaches the contract's notice requirement.
- B) The maintenance breaches the departmental policy.
- C) The maintenance breaches neither the notice requirement nor the policy.
- D) The maintenance breaches both.

**Correct answer: C**

**Explanation:** Check each rule independently. Notice: from Monday 20 March, ten working days run 21, 22, 23, 24, 27, 28, 29, 30, 31 March, 3 April — the tenth working day after notice lands on 3 April itself, meaning ten full working days' notice has been given for maintenance on 3 April... verify by counting notice days *before* the event: 21-24 March (4), 27-31 March (5) = 9 clear working days, with the maintenance on the 10th. Whether "10 working days' notice" requires ten clear days or maintenance on the tenth day is exactly the kind of ambiguity contracts generate — but on the standard reading (notice given 10 working days before the event, i.e. the event occurring on or after the tenth subsequent working day), 3 April qualifies. Policy: the last five working days of the quarter are 27-31 March; the maintenance is on 3 April, in the *next* quarter, so the policy is untouched. Hence C. The question's real lesson is the method: two rule sources, checked separately, each against a carefully constructed calendar — and an honest flag where wording is ambiguous. As the accountable owner of supplier management, you will resolve such ambiguities *in the contract's definitions section* before they matter, which is what the strongest principals do with every "working days" clause they inherit.

**Question 3 (easy) — Error checking a compliance return**

Your quarterly compliance return asserts: (i) "All 12 production applications have completed annual security review." (ii) "The register shows 11 applications with review dates within the last 12 months." (iii) "One application, LegacyPay, was decommissioned in month 10 of the reporting period." (iv) "LegacyPay's last review was 14 months ago." Which is the most accurate assessment of the return?

- A) Consistent: 11 current reviews plus one decommissioned application accounts for all 12.
- B) Inconsistent: if LegacyPay is one of the 12 production applications, statement (i) is false — its review is 14 months old; if it was decommissioned, it should not be counted among 12 *production* applications, making the totals wrong either way. The return needs its population defined before its claim can be true.
- C) Consistent, provided LegacyPay is excluded.
- D) The return is fine because decommissioned systems need no review.

**Correct answer: B**

**Explanation:** Chase the arithmetic of the population. If the "12 production applications" includes LegacyPay: statement (i) claims all 12 completed annual review, but (iv) puts LegacyPay's last review at 14 months — (i) is false. If the 12 excludes LegacyPay (decommissioned in month 10): then (ii)'s 11 current reviews leave one *other* application unaccounted for — which application, and where is its review? Either reading breaks the return; the defect is an undefined population being asserted over. Option A performs the comforting but invalid arithmetic (11 + 1 = 12) that mixes the two populations — the exact aggregation sleight that makes bad compliance returns look good. Option C hides the missing twelfth application. Option D answers a different question — LegacyPay's review obligation while live is unaffected by its later decommissioning. Managing service compliance and risk (**Asset and configuration management**) at principal level is largely this: refusing to sign aggregate claims until the population, the period, and the criterion are each pinned down — because your signature converts the return's ambiguity into your attestation.

**Question 4 (moderate) — Portfolio risk prioritisation**

Four risks compete for your remediation budget and attention this quarter:

1. R1: A supplier's platform goes end-of-support in 8 months; migration takes an estimated 6 months. Impact if unmanaged: unsupported production software for a citizen-facing service.
2. R2: A capacity shortfall projected to breach a KPI in 3 weeks on an internal reporting service; fix is a 2-week infrastructure change.
3. R3: A key-person dependency — only one engineer understands the payments integration; they have just resigned with 4 weeks' notice.
4. R4: An audit finding (due for management response in 6 weeks) about incomplete configuration records, no service impact yet observed.

Which ordering of initiation is most defensible?

- A) R2, R3, R1, R4 — start the capacity fix and knowledge transfer immediately in parallel, initiate the migration programme this quarter, schedule the audit response within its deadline
- B) R1, R2, R3, R4 — biggest impact first
- C) R4, R2, R3, R1 — audit findings carry reputational risk
- D) R3, R1, R4, R2 — people risks always dominate

**Correct answer: A**

**Explanation:** Rank by *decision urgency* — the date by which failing to start makes the outcome materially worse — not by impact alone. R2's clock is shortest: a 2-week fix against a 3-week breach leaves one week of margin; start now or accept the breach. R3's clock is nearly as hard and wholly unforgiving: four weeks of the departing engineer's time is a wasting asset — every day not spent on structured knowledge transfer, documentation, and pairing is unrecoverable; it starts immediately, in parallel, because it consumes different resources (the engineer's calendar, a successor's time) than R2's infrastructure change. R1 is the *largest* risk but has the longest runway: 8 months minus 6 months' migration leaves a 2-month decision window — initiating the migration programme this quarter is fully adequate, and note that "initiate" is the correct verb: the principal's move is mobilising the programme, not doing the migration. R4 has a defined 6-week deadline, no current service impact, and a bounded response effort: scheduled, not scrambled. Option B confuses impact with urgency and burns R3's wasting asset. Option C promotes reputational discomfort over service reality. Option D's absolutism starts well (R3 genuinely is urgent) then leaves R2 to breach last. The principal-level pattern: sequence by last responsible start date, run non-competing workstreams in parallel, and reserve your own attention for the items where accountability cannot be delegated — which here is R1's programme mobilisation and R3's succession, while R2 and R4 need your sponsorship, not your hands.

**Question 5 (moderate) — Deduction across a technology roadmap**

Facts: (i) your strategic database platform will drop support for the legacy API your casework application uses, in its version 12, expected in two years; (ii) the casework application's modernisation to the new API is scoped at 15 months; (iii) your department mandates that production databases run supported platform versions within 12 months of release; (iv) platform version 11, retaining the legacy API, will be supported for three years after version 12 releases. What is the latest the casework modernisation can start while guaranteeing continuous compliance and support?

- A) Immediately — there is no slack.
- B) Within 9 months: version 12 releases in ~24 months, the mandate requires upgrading to it by ~36 months, and the modernisation (15 months) must complete by then, so it must start by month 21 — but option timing must also respect that version 11's support ends at month 60, which is not the binding constraint; the binding constraint is the 36-month mandate, giving a latest start of month 21, i.e. within 21 months.
- C) Within 21 months: the mandate to run version 12 bites at month 36 (release at 24 + 12-month grace); modernisation takes 15 months; 36 − 15 = 21.
- D) Any time within 45 months, since version 11 is supported until month 60.

**Correct answer: C**

**Explanation:** Build the timeline from the constraints. Version 12 releases at month ~24. The departmental mandate (iii) requires production databases to be on supported *and mandated-current* versions within 12 months of release — so the casework application must be off the legacy API and on version 12 by month 36. The modernisation takes 15 months, so its last safe start is month 36 − 15 = 21: option C. Option D reads only the vendor's support horizon (version 11 supported to month 60) and misses that your own department's 12-month currency mandate bites first — a classic error in strategy work: the binding constraint on your timeline is frequently internal policy, not vendor lifecycle, and option D's answer would leave you 24 months non-compliant while feeling vendor-safe. Option A overcorrects into false urgency, which has real costs: starting "immediately" without need pre-empts this year's committed work. Option B reasons to the correct month-21 answer and then mislabels it "within 9 months" — in assessments, an option whose working is right and whose conclusion mis-states the working is still wrong; read options to their end. Owning the application strategy is exactly this discipline: intersect vendor roadmaps (your **Technical specialism** duty to understand future technology direction) with internal mandates, find the earliest-binding constraint, and schedule against *it* with the last responsible start date explicit — so the strategy document says "start modernisation no later than month 21", a sentence a successor can execute.

**Question 6 (moderate) — Error checking supplier performance data**

Your supplier's quarterly service report claims: "Availability target (99.5%) met in all three months: April 99.6%, May 99.7%, June 99.6%. Quarterly availability: 99.63%. All 4 severity 1 incidents resolved within the 4-hour contractual target: resolution times 3.2h, 3.8h, 2.9h, and one incident excluded from calculation as customer-caused. Penalty position: no penalties due." Your own records show the June "customer-caused" exclusion refers to an incident triggered by your team applying a configuration the supplier's own runbook specified. What is the soundest assessment?

- A) Accept the report — three resolution times beat the target and the availability figures are green.
- B) The availability figures may stand, but the excluded incident is disputed: if the configuration followed the supplier's own runbook, the "customer-caused" classification fails, the incident (duration unknown from this report) re-enters both the severity 1 resolution calculation and possibly the availability figures — challenge the exclusion with the runbook evidence before accepting the penalty position.
- C) Reject the whole report as unreliable.
- D) Accept the report but informally ask the supplier to be more careful with classifications.

**Correct answer: B**

**Explanation:** Locate exactly what the disputed fact contaminates. The exclusion's basis — "customer-caused" — collapses if the customer's action implemented the supplier's own runbook: an instruction-following customer is the supplier's agent in any sane contractual reading, and most contracts say so explicitly. What follows is surgical, not total: the fourth incident re-enters the severity 1 resolution dataset (was it inside 4 hours? the report is silent — conspicuously); its duration may also belong in June's availability arithmetic (99.6% claimed; a materially long incident could unmake it); and the "no penalties due" conclusion inherits every one of those doubts. Option A accepts a conclusion built on a classification you hold direct evidence against. Option C overcorrects — the April and May figures are not implicated, and wholesale rejection squanders your challenge's precision and credibility. Option D treats a possibly penalty-avoiding misclassification as an etiquette lapse; accountability for supplier management means the challenge is formal, evidenced (the runbook), and resolved before the penalty position is accepted — this quarter, because accepted reports harden into precedent. The general principle for principal-level assurance: when one datum in a report is known-bad, trace its dependency graph through the report's conclusions and challenge precisely those — the skill is knowing what the error touches.

**Question 7 (moderate) — Framework reasoning at expert level**

Your organisation is designing its operating model for a new shared-services group. Three design claims are on the table: (1) "Problem management should report through the incident management function, since problems come from incidents." (2) "Change enablement should sit with the delivery teams entirely, since they know their changes best." (3) "Continual improvement should be a standing capability with its own backlog, not a year-end exercise." Drawing on service management framework principles, which assessment is soundest?

- A) All three claims are sound.
- B) Claim 3 is sound; claim 1 conflates a data flow with a reporting line — problems draw on incident data but need independence to challenge recurring-incident tolerance, and many problems are identified proactively, not from incidents at all; claim 2 captures a real principle (decentralised change authority for low-risk changes) but overstates it — high-impact and cross-team changes still need co-ordination and standards that pure team autonomy cannot supply.
- C) Claims 1 and 2 are sound; claim 3 is bureaucratic.
- D) None of the claims is sound.

**Correct answer: B**

**Explanation:** Take each claim on its merits — the expert answer is rarely all-or-nothing. Claim 1's error is structural: incident management's mission is fast restoration; problem management's mission is root-cause elimination, and the two trade off (a workaround that restores service quickly can reduce pressure to fix the cause). Subordinating problem management to incident management gives the restoration mission authority over the elimination mission — the fox reporting to the henhouse's throughput manager — and, as your role summary's **Problem management** skill notes, problems are also *anticipated* proactively, a function with no incident parent at all. Claim 2 contains the genuinely modern principle — current framework thinking pushes change authority toward teams for standard, low-risk changes — but "entirely" is where it breaks: your own **Change management** duty (high-impact, complex changes; release policies *applied*) exists precisely because cross-team impact and organisational risk appetite are not visible from inside any single delivery team. Claim 3 states the mature position: improvement as a standing, backlogged capability rather than an annual confession. Option B threads all three correctly. The assessment point, and the expert-certificate point (**Service management framework knowledge**), is the same: frameworks are bodies of *reasoned* practice — the expert can say why each structure exists, which is what lets them judge when a proposed deviation is innovation and when it is a category error.

**Question 8 (moderate) — Pattern in workforce data**

Your team's skills matrix shows coverage (number of engineers able to support each system) and each system's strategic status:

| System | Engineers able to support | Strategic status |
|---|---|---|
| Case platform | 6 | Core, growing |
| Legacy payments | 2 | Migrating away, 3-year horizon |
| Grants service | 5 | Core, stable |
| Data exchange | 1 | Core, growing |
| Notifications | 4 | Core, stable |

Leading on resourcing and development, which finding demands action first, and what shape should the action take?

- A) Legacy payments (2 engineers) — hire two more payments specialists.
- B) Data exchange (1 engineer) — a single point of failure on a core, *growing* system: cross-train two engineers now via pairing and documented runbooks; for legacy payments, maintain coverage at 2 with succession awareness but do not invest in growth, since the system is leaving the estate.
- C) Case platform — its 6 engineers are over-provisioned; redeploy them.
- D) All systems need more coverage; request budget for five hires.

**Correct answer: B**

**Explanation:** Read the two columns *together* — coverage numbers mean nothing without strategic direction. Data exchange combines the worst coverage (1 — a bus-factor of one) with the worst possible status for that coverage (core and growing: demand will rise, and a single resignation, illness, or holiday makes a growing core system unsupportable). It acts first, and the action's shape matters: cross-training and runbook documentation convert existing capacity, faster and cheaper than hiring, and pairing on live work is how tacit operational knowledge actually transfers. Legacy payments *looks* like the same problem (2 engineers) but the strategic column inverts the response: investing specialist growth in a system with a 3-year exit horizon buys depreciating capability — the right posture is maintain-and-monitor, with the migration itself as the true remedy. Option A makes exactly that inverted investment. Option C misreads healthy coverage on the estate's biggest growing system as waste — six engineers on a core growing platform is resilience, not surplus. Option D converts a prioritisation question into an undifferentiated budget request, which is what resourcing leadership exists to avoid. This is your resourcing-and-development remit exercised as portfolio analysis: skills coverage is a risk surface, and it is priced against the strategy — which you own — not against headcount symmetry.

**Question 9 (hard) — Multi-constraint strategy sequencing**

Your five-year application strategy must sequence four programmes: (P1) migrate the casework database to the strategic platform — 18 months, requires the data exchange modernisation (P2) to be complete first; (P2) data exchange modernisation — 12 months; (P3) supplier transition for hosting — 12 months, cannot overlap with P1's migration (both consume the same operations capacity), and the incumbent hosting contract expires at month 42 with a one-time 12-month extension available at a 40% cost premium; (P4) reporting consolidation — 9 months, can run any time after P2, alongside anything. Programmes start only at quarter boundaries (months 0, 3, 6...). What is the optimal sequence that avoids the contract extension premium?

- A) P2 (0-12), P1 (12-30), P3 (30-42), P4 (12-21)
- B) P2 (0-12), P3 (12-24), P1 (24-42), P4 (24-33)
- C) P3 (0-12), P2 (12-24), P1 (24-42), P4 (24-33)
- D) The premium is unavoidable; take the extension.

**Correct answer: B**

**Explanation:** Encode the constraints first: P1 after P2; P1 and P3 disjoint in time; P3 complete by month 42 or pay the 40% premium; quarter-boundary starts. Now test. Option C fails on dominance: starting with P3 (0-12) is legal, but it spends the earliest, least-constrained year on the hosting transition *before* the modernisation (P2) that the critical chain depends on — its P1 and P4 timings end up identical to option B's, so it offers B's schedule with strictly worse sequencing risk: any P2 overrun now delays the entire dependent chain with no compensating benefit. Option D pays 40% for a constraint that feasible schedules satisfy. That leaves A and B, and both are mechanically feasible with no premium: in A, P2 runs 0-12, P1 runs 12-30, P3 runs 30-42 (disjoint from P1, done exactly at expiry), P4 runs 12-21; in B, P2 runs 0-12, P3 runs 12-24, P1 runs 24-42, P4 runs 24-33. The discriminator is where each schedule puts its slack. Option A drives the critical path hard — casework migrated by month 30 — but parks the hosting transition flush against the contract cliff: P3 completes at month 42 with *zero* margin, so any overrun at all forces the 40% premium the question asks you to avoid. Option B banks the hosting transition early, leaving 18 months of contract margin against the only constraint with a price tag, and accepts the casework migration completing at the strategy horizon — a slip there costs schedule, not money, and the stem states no external deadline for P1. A premium-avoidance plan with no margin is a premium-payment plan that hasn't happened yet; B is the robust avoider, and the answer. Two principal-level lessons follow. First, mechanical feasibility is the entry ticket, not the answer: when several schedules satisfy the letter of the constraints, the choice between them is margin allocation — put slack against the constraint whose breach costs money or law, and let flexible constraints absorb the risk. Second, notice that the "obvious" answer (critical path first) survived every check except *where does the risk land if something slips?* — which is precisely the question your strategy's governance board will ask, and the one your five-year paper should answer in its own text.

**Question 10 (hard) — Anticipating a problem from three trend lines**

Three independent trends cross your desk in the same month: (a) the data exchange service's message volumes are growing 8% per quarter; (b) its 95th-percentile processing latency has crept from 1.2s to 1.9s over four quarters; (c) the downstream casework service has begun timing out intermittently on exchange calls, with timeouts set at 2.0s. No incident has been declared. What is the most complete reading?

- A) Three separate observations for three separate teams' backlogs.
- B) A compound problem completing itself: volume growth is driving latency growth toward the downstream timeout threshold — at current trajectory the 95th percentile crosses 2.0s within a quarter, converting intermittent timeouts into systematic failure; this warrants problem-record creation now, co-ordinated investigation (is latency growth linear with volume, or worsening?), capacity remediation on the exchange, and a co-ordinated review of downstream timeout/retry policies — before it becomes the major incident it is currently rehearsing.
- C) The casework team should simply raise its timeout to 3 seconds.
- D) Wait for a declared incident to establish impact before acting.

**Correct answer: B**

**Explanation:** Connect the trends into a mechanism: rising volume (a) is the plausible driver of rising latency (b), and latency's 95th percentile at 1.9s against a 2.0s downstream timeout (c) explains the intermittent failures arithmetically — 5% of calls already run close enough that ordinary variance crosses the line. Extrapolate honestly: four quarters took latency from 1.2s to 1.9s (~0.175s/quarter, and plausibly *accelerating* if latency is superlinear in volume — queueing effects usually are); the 95th percentile crosses the threshold within a quarter, at which point "intermittent" becomes "systematic" and a citizen-facing casework outage arrives with your name pre-attached, because the signals were all on your desk. Option B is your role summary rendered as a checklist: *anticipate* problems, *co-ordinate the team* to investigate, implement solutions, take preventative measures (**Problem management**); *identify capacity issues and initiate remedial action* (**Availability and capacity management**). Option A shatters a compound mechanism across three backlogs where no one owns the interaction — the precise failure your **Service focus** skill ("groups of services… underlying services") exists to prevent. Option C treats one symptom: raising the timeout buys a quarter or two while making each casework call slower and masking the underlying growth problem — as a *conscious element* of B's co-ordinated response it might feature; as the whole answer it is a snooze button. Option D waits for the harm to purchase the evidence, inverting the entire proactive premise of principal-level ownership. The signature principal skill here is owning the *interaction* between services — everything else in the scenario already had an owner.

**Question 11 (hard) — Vendor lock-in reasoning**

Your strategy must choose between two paths for a critical application suite: Path L — deepen use of the incumbent supplier's proprietary platform features (20% cheaper to run, faster feature delivery, but each adopted proprietary feature raises exit costs; current estimated exit cost £2m, rising ~£0.5m per year of deepening); Path N — re-platform onto open standards over two years (£3m programme cost, run-costs equal to today's, exit costs thereafter near zero). The supplier's contract renews in three years. Departmental guidance requires "demonstrable supplier exit viability" at each renewal. Which analysis is soundest?

- A) Path L — 20% cheaper is decisive; exit viability is a paper exercise.
- B) Path N — lock-in must always be eliminated regardless of cost.
- C) The decision hinges on the renewal test: under Path L, exit cost at renewal is ~£3.5m and rising, weakening negotiating position and possibly failing the exit-viability requirement — the run-cost saving is partly a lock-in premium being banked by the supplier against renewal; under Path N, £3m spent once buys exit viability, negotiating leverage at renewal, and flat exit costs. Model the renewal negotiation explicitly: if Path L's weakened position concedes even 10-15% at renewal, its run-cost advantage largely evaporates — and Path L fails the guidance as written. Path N, or a hybrid that caps proprietary adoption at reversible features, is the defensible strategy.
- D) Defer the decision to the renewal point in three years.

**Correct answer: C**

**Explanation:** The scenario's centre of gravity is that Path L's economics are not static: its 20% saving is priced *by the supplier who collects the exit costs* — cheap-to-adopt, expensive-to-leave is not a coincidence of proprietary platforms, it is their business model, and the £0.5m/year exit-cost growth is the negotiating leverage you hand across the table at renewal. Option C models the decision where it will actually be decided — the renewal negotiation: a supplier facing a customer with £3.5m exit costs and rising prices accordingly, and the departmental exit-viability requirement (which exists precisely to prevent this position) is failed *by construction*, not by paperwork. Path N's £3m converts into three assets: compliance, leverage, and optionality — including the option to *stay* with the incumbent at a fairly negotiated price, which is the paradox of exit viability: you buy it in order to not need it. Option A dismisses as paperwork the exact clause your accountability for vendor and supplier management answers to. Option B is ideology: lock-in is a cost to be *priced*, not a sin to be purged at any price — which is why C's hybrid clause (proprietary adoption capped at reversible features) belongs in the answer; some proprietary value is worth its exit cost, if the exit cost is known, bounded, and consciously accepted. Option D is Path L by default — three more years of deepening — wearing neutrality. Understanding future technology direction (**Technical specialism**) at principal level includes understanding the *commercial* trajectory of technology choices: the strategy you own must price its options at the point of least leverage, which is always the renewal table.

**Question 12 (hard) — Auditing a plausible analysis**

A capable lead on your team submits an analysis: "Our incident reviews show 70% of major incidents involve a change made in the previous 72 hours. Conclusion: changes are our dominant incident cause. Recommendation: halve our change frequency to reduce major incidents by up to a third." The lead's figures are accurate. As the principal auditing this reasoning before it reaches governance, what is the soundest response?

- A) Endorse it — the correlation is strong and the recommendation flows from it.
- B) The 70% is uninterpretable without a base rate: if changes occur so frequently that 70% of *all* 72-hour windows contain a recent change, then major incidents are no more change-associated than random days — the analysis needs the comparison rate (what fraction of incident-free periods also follow changes within 72 hours?) and a causal read of the actual incident reviews; separately, halving change frequency has known perverse effects — larger, rarer changes carry more risk each — so even a confirmed causal link would point at change *quality* (smaller batches, better testing, staged rollout), not change *scarcity*. Return the analysis with those two questions, and credit the lead's initiative while teaching the method.
- C) Reject the analysis — correlation is not causation, so nothing can be concluded.
- D) Endorse the conclusion but soften the recommendation to a 25% change reduction.

**Correct answer: B**

**Explanation:** Two distinct flaws, each fatal alone. The evidential flaw: "70% of incidents follow changes" is meaningless without knowing how often *anything* follows changes — in an estate deploying daily, virtually every 72-hour window contains a change, so 70% could be *below* baseline, making changes look protective; the analysis needs the denominator (the base rate) and, better, the incident reviews' actual causal findings rather than temporal association. The remedial flaw: even granting causation, frequency-halving forces batching — larger changesets, each carrying more concurrent risk, less rehearsed rollback, and slower user value — the well-documented failure mode of change-scarcity regimes, and the reason mature practice targets change *quality and size*, not count. Option A forwards both flaws to governance under your endorsement. Option C wields "correlation is not causation" as a thought-terminator — the phrase licenses *investigation*, not dismissal, and rejecting capable initiative without teaching the missing method wastes both the analysis and the analyst. Option D negotiates the number while inheriting the logic — a smaller dose of an unproven medicine. Option B does the three things the principal role uniquely owes this moment: protect governance from confident error (*ensure the right actions are taken* — **Problem management**), improve the analysis rather than merely grade it, and develop the lead — your learning-and-development remit — by returning questions rather than verdicts. A principal's highest-leverage cognitive act is rarely their own analysis; it is the audit that upgrades everyone else's.

### Preparation tips

- **Practise base-rate interrogation.** For every "X% of incidents involve Y" claim you meet this month — in this guide, in vendor reports, in your own team's analyses — ask for the comparison rate. It is the single highest-yield habit for both assessments and governance.
- **Sequence by last responsible start date.** For prioritisation questions, compute each item's decision deadline (impact date minus lead time minus margin), not its impact size. Wasting-asset items — departing people, expiring windows — jump queues.
- **Check both rule sources.** Contract and policy, vendor lifecycle and internal mandate, standard and exception: principal-level deduction questions almost always intersect two rule systems, and the binding constraint is usually the less obvious one.
- **Trace known-bad data through conclusions.** When a question stipulates that one datum is wrong, map exactly which downstream figures and conclusions it contaminates — no more, no less. Surgical challenge is the scored skill.
- **Audit your agreement.** When an option matches your first instinct, spend ten seconds seeking the disconfirming fact before selecting it. The hardest questions are built around plausible near-misses.
- **Rehearse margin allocation.** In sequencing problems with multiple feasible answers, ask where each schedule puts its slack — and choose the one whose slack shields the constraint with financial or legal teeth.

### Common pitfalls to avoid

- **Ranking by impact instead of decision urgency.** The biggest risk with the longest runway starts after the modest risk with the three-week fuse. Impact sets stakes; lead times set order.
- **Reading only the vendor's clock.** Support horizons flatter your timeline; internal currency mandates, contract renewals, and governance cycles usually bite first. Intersect all the clocks.
- **Accepting aggregate claims over undefined populations.** "All 12", "70% of incidents", "no penalties due" — until the population, period, and criterion are pinned, the claim is not yet checkable, and your endorsement launders it.
- **All-or-nothing framework judgements.** Real design claims are usually part-right; the expert answer separates the sound principle from its overstatement. Options offering total acceptance or rejection are typically decoys.
- **Treating remedies as implied by diagnoses.** "Changes cause incidents, therefore fewer changes" and "coverage is low, therefore hire" both skip the remedial reasoning. Confirm the mechanism, then choose the intervention that targets it.
- **Endorsing capable people's flawed logic.** The costliest errors reaching governance arrive well-formatted, from your best people, containing accurate figures and invalid inferences. Audit reasoning independently of your trust in its author — then teach, don't just correct.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and strategically you work with the quantitative material a principal's decisions run on: multi-year cost models, supplier performance and penalty calculations, portfolio availability and risk figures, capacity investment cases, workforce and development budgets, and user outcome data. The arithmetic itself — percentages, ratios, weighted averages, compounding, rates — is deliberately standard; the principal-level content is in the modelling and the interpretation: which figure governs the decision, what the number commits the organisation to, and where a well-presented calculation is quietly wrong.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 data-based questions, calculators permitted. Senior-level variants routinely present multiple data sources to reconcile — a contract clause and a performance table, a forecast and a budget envelope, a before and an after — because reconciliation is what principals actually do with numbers: your signature turns a calculation into a commitment.

Why do employers use numeric assessments for this role? Because at principal level, your numbers move money and set direction. The supplier penalty you calculate (or fail to) is real revenue; the capacity investment case you sign shapes next year's budget; the availability commitment in your strategy becomes your successor's KPI; the resourcing model you present determines who gets hired and developed. Your role summary makes you accountable for vendor and supplier management, for identifying capacity issues and initiating remedial action, and for leading on resourcing — every one of which is, at its core, arithmetic performed in public with consequences attached. A principal whose models are transparent and whose figures survive challenge becomes the person whose papers govern; the questions below rehearse exactly that standard, with all working shown.

### How this assessment maps to your role

- **Contract and penalty arithmetic** maps to your **vendor and supplier management accountability**: service credit calculations, penalty thresholds, and cost comparisons across contract structures are where supplier accountability becomes cash.
- **Capacity and investment modelling** maps to **Availability and capacity management** and **Technical specialism**: identifying capacity issues, initiating remedial action, and delivering a model that supports future technologies all rest on defensible projections — compounding growth, step changes, lead times, and cost curves.
- **Portfolio performance figures** map to **Service focus** and **Asset and configuration management**: seeing the bigger picture across service groups means normalised comparison, and managing compliance and risk means knowing what an aggregate figure conceals.
- **Resourcing and development numbers** map to your **resourcing, learning and development leadership**: coverage ratios, training investment returns, and succession timelines are workforce strategy expressed numerically.
- **Test and risk figures** map to **Testing**: managing risks and taking preventative action when they become unacceptable requires quantifying "unacceptable" — defect trends, coverage gaps, and the cost curves of acting late.
- **User outcome data** maps to **User focus**: representing users internally at governance level means carrying their experience as numbers that survive scrutiny — adoption, completion, satisfaction — with definitions intact.

### Practice questions

**Question 1 (easy) — Service credit calculation**

Your supplier contract provides: "For each month availability falls below 99.5%, a service credit of 5% of that month's charge applies; below 99.0%, the credit is 12%." Monthly charge: £80,000. This quarter's availability: April 99.7%, May 99.2%, June 98.8%. What total service credit is due?

- A) £4,000
- B) £13,600
- C) £9,600
- D) £16,000

**Correct answer: B**

**Explanation:** Apply the credit schedule month by month. April: 99.7% is at or above 99.5% — no credit. May: 99.2% is below 99.5% but not below 99.0% — 5% of £80,000 = £4,000. June: 98.8% is below 99.0% — 12% of £80,000 = £9,600. Total: £4,000 + £9,600 = £13,600. Option A takes May only; option C takes June only; option D applies 5% + 12% to a single month. Note the schedule's structure — the 12% band *replaces* the 5% band rather than stacking on it, which is how such clauses are conventionally drafted and read; if your contract's wording is ambiguous on stacking, that is a definitions conversation to have *before* a bad month, not during one. Supplier accountability begins with being the person in the room who has already done this arithmetic when the quarterly review opens.

**Question 2 (easy) — Cost per transaction across the portfolio**

Two services process citizen applications. Service A costs £1.2m per year and processed 400,000 applications. Service B costs £450,000 per year and processed 90,000 applications. Which has the lower cost per transaction, and what are the figures?

- A) Service A: £3.00 versus Service B's £5.00
- B) Service B: £2.00 versus Service A's £4.44
- C) Service A: £30 versus Service B's £50
- D) They are equal at £3.00

**Correct answer: A**

**Explanation:** Compute each unit cost. Service A: £1,200,000 ÷ 400,000 = £3.00 per application. Service B: £450,000 ÷ 90,000 = £5.00 per application. Service A is markedly cheaper per transaction despite the larger total budget — the recurring lesson that absolute cost and unit cost rank differently, and portfolio decisions (consolidation, investment, decommissioning) belong to unit economics read alongside strategic factors. Option C misplaces the decimal by a factor of ten — always sanity-check unit costs against intuition (a £30 cost to process one routine application should feel wrong). This is **Service focus** arithmetic: "taking groups of services and investigating how to get the best of underlying services" starts with knowing what each service's output actually costs, because a 67% unit-cost difference between comparable services is either an efficiency finding or a scope difference — and finding out which is your next question.

**Question 3 (easy) — Training budget allocation**

Your learning and development budget is £60,000 for a team of 15 engineers. You have committed: £1,400 per engineer for core professional development (all 15), plus a service management expert-certification programme at £3,500 each for 4 engineers, plus a £6,000 team-wide incident-leadership workshop. How much remains unallocated?

- A) £19,000
- B) £13,000
- C) £25,000
- D) £7,000

**Correct answer: A**

**Explanation:** Sum the commitments stepwise. Core development: 15 × £1,400 = £21,000. Certifications: 4 × £3,500 = £14,000. Workshop: £6,000. Total committed: £21,000 + £14,000 + £6,000 = £41,000. Remaining: £60,000 − £41,000 = £19,000. The management content sits behind the arithmetic: the uncommitted £19,000 (32% of budget) is your in-year flexibility for emerging needs — the cross-training that Question 8 of the cognitive section identified, a conference that matters, a departing specialist's knowledge-capture. Leading on learning and development means holding this arithmetic live through the year: fully-allocated January budgets and fully-unspent December budgets are the two classic failures of development leadership, and both are visible in this simple running subtraction.

**Question 4 (moderate) — Comparing contract pricing structures**

Two suppliers bid for a five-year hosting contract. Supplier X: £900,000 per year, flat. Supplier Y: £700,000 in year 1, rising 8% per year thereafter. Which supplier is cheaper over the full five years, and by roughly how much?

- A) Supplier Y, by about £394,000
- B) Supplier X, by about £150,000
- C) Supplier Y, by about £893,000
- D) They are within £20,000 of each other

**Correct answer: A**

**Explanation:** Supplier X: 5 × £900,000 = £4,500,000. Supplier Y compounds from £700,000: year 1 £700,000; year 2 £700,000 × 1.08 = £756,000; year 3 £756,000 × 1.08 = £816,480; year 4 £816,480 × 1.08 = £881,798; year 5 £881,798 × 1.08 = £952,342. Sum: 700,000 + 756,000 = 1,456,000; + 816,480 = 2,272,480; + 881,798 = 3,154,278; + 952,342 = £4,106,620. Difference: £4,500,000 − £4,106,620 = £393,380 ≈ £394,000 in Supplier Y's favour. Option C is the error of applying 8% non-compounding or mis-summing; option D is what a hasty "8% will surely catch up" intuition produces. Two supplier-management observations complete the analysis: first, Y's year-5 price (£952,000) has crossed above X's flat £900,000 — so a five-year win becomes a year-6 loss if the escalator survives renewal, which is exactly what Y's pricing is designed to do; second, the crossover arithmetic (Y exceeds X in year 5) is your negotiating datum — cap the escalator at year 4 levels or price the year-6 exposure now. Principal-level procurement numeracy is compounding fluency plus the habit of asking what happens *after* the comparison window.

**Question 5 (moderate) — Availability aggregation across a service chain**

A citizen journey depends on three services in series: identity (99.9% available), casework (99.5%), and notifications (99.8%). Assuming independent failures, what is the end-to-end availability of the journey, and what does it imply?

- A) 99.5% — the chain is as available as its weakest link, no better and no worse.
- B) About 99.2% — availabilities in series multiply (0.999 × 0.995 × 0.998 ≈ 0.9920), so the journey is *less* available than its weakest component, and end-to-end targets cannot simply be inherited from component targets.
- C) 99.73% — the average of the three figures.
- D) 99.9% — the strongest component protects the chain.

**Correct answer: B**

**Explanation:** Series availability multiplies: 0.999 × 0.995 = 0.994005; × 0.998 = 0.992017 — approximately 99.2%. The journey fails if *any* component fails, so the chain is strictly weaker than its weakest link (option A's "no worse" is the seductive error — the weakest-link heuristic gives an upper bound, not the answer). Option C's averaging has no physical meaning; option D inverts the logic entirely. The strategic implication is the question's real content: if the business sets a 99.5% end-to-end target for the citizen journey, *no* component may be as weak as 99.5% — the component budgets must be tighter than the journey target, which is precisely the kind of standards-setting your **Availability and capacity management** skill ("ensure the correct implementation of availability and capacity management standards") exists to do. This multiplication is also your **Service focus** skill in a formula: the bigger picture across groups of services is exactly the recognition that users experience the *product* of your components, not the best of them — and it is why the principal, not any single service team, must own the end-to-end number.

**Question 6 (moderate) — Capacity investment options**

A growing service needs capacity. Current infrastructure handles 100,000 daily transactions; demand is 80,000 today, growing 20% per year (compounding). Option 1: incremental upgrades at £150,000 now, adding 50% capacity (to 150,000). Option 2: re-architecture at £600,000, taking one year, after which capacity is effectively unconstrained for the planning horizon. When does demand exhaust each option's capacity, and which investment does the arithmetic favour for a five-year horizon?

- A) Option 1 exhausts in year 5; Option 1 suffices for the horizon.
- B) Demand hits 100,000 within ~1.2 years and 150,000 within ~3.5 years; Option 1 buys only ~2 more years, so within the five-year horizon you would pay for Option 1 *and then* still need Option 2 — total £750,000; starting Option 2 now (£600,000, ready inside the ~1.2-year runway) is cheaper overall and avoids a double migration.
- C) Option 2 is always better regardless of numbers.
- D) Demand never reaches 150,000 in five years, so Option 1 wins.

**Correct answer: B**

**Explanation:** Project demand first: 80,000 × 1.2 = 96,000 (year 1); × 1.2 = 115,200 (year 2); × 1.2 = 138,240 (year 3); × 1.2 = 165,888 (year 4); × 1.2 = 199,066 (year 5). Current capacity (100,000) is exceeded between years 1 and 2 — interpolating, at roughly 1.2 years. Option 1's 150,000 is exceeded between years 3 and 4 — roughly 3.5 years (option D is simply wrong: 165,888 > 150,000 in year 4). So Option 1, bought now, buys about 2.3 extra years of headroom, after which — still inside the five-year horizon — the re-architecture becomes necessary anyway: total spend £150,000 + £600,000 = £750,000, plus two migrations' worth of disruption. Option 2 started now completes at year 1, just inside the ~1.2-year runway (tight — the margin analysis belongs in your paper), and costs £600,000 once. The arithmetic favours Option 2 by £150,000 *and* by risk shape — though option C's "always" is exactly what your working refuses to claim: had growth been 8%, Option 1 would have covered the horizon and won. This is **Availability and capacity management** ("identify capacity issues and implement the required changes") at investment scale: the recurring principal-level pattern is that interim fixes purchased against compounding demand are frequently money spent to arrive at the same decision later, poorer — and the way to *know* rather than assert that is the year-by-year table above.

**Question 7 (moderate) — Defect discovery economics**

Your testing data across recent releases shows: defects found in development cost on average £400 to fix; defects found in system testing cost £2,100; defects found in production cost £13,500 (including incident response and rework). A proposed investment of £120,000 per year in earlier automated testing is projected to shift 60 defects per year from production discovery to development discovery, and a further 40 from system-test discovery to development discovery. What is the projected annual net benefit?

- A) £666,000
- B) £854,000
- C) £734,000
- D) £546,000

**Correct answer: C**

**Explanation:** Value each shift by its cost *difference*, not its endpoint cost. Production-to-development shift: 60 defects × (£13,500 − £400) = 60 × £13,100 = £786,000. System-test-to-development shift: 40 × (£2,100 − £400) = 40 × £1,700 = £68,000. Gross benefit: £786,000 + £68,000 = £854,000 (option B is this figure — the gross, forgetting the investment). Net of the £120,000 investment: £854,000 − £120,000 = £734,000 — option C. Option A uses full endpoint costs for the second shift or mis-subtracts; option D double-counts the investment. Beyond the arithmetic, this is the business case for your **Testing** skill's risk-management clause: "take preventative action when risks become unacceptable" is usually argued qualitatively and loses to this year's feature list — argued as £734,000 per year, it wins. The honest paper also states its assumptions' fragility: the 60-defect shift is a projection, so build the case with a sensitivity line (at half the projected shift, net benefit is still £307,000) — a case that survives its assumptions being halved is a case a governance board can trust.

**Question 8 (moderate) — Supplier performance trend with a definitions change**

Your supplier's monthly report shows first-time-fix rates: Jan 71%, Feb 72%, Mar 74%, Apr 81%, May 82%, Jun 83%. A footnote on April's report states: "From April, first-time-fix excludes tickets requiring customer information, per agreed definition change." What can you validly conclude about the supplier's underlying performance improvement?

- A) Performance improved by 12 percentage points over the half year.
- B) The January-March trend shows modest genuine improvement (+3 points); the April jump (+7 points) coincides with the definition change and cannot be attributed to performance without recomputing April-June on the old definition — request the like-for-like series before crediting the improvement.
- C) Performance has not improved at all; the definition change explains everything.
- D) The definition change is irrelevant since it was agreed.

**Correct answer: B**

**Explanation:** Partition the series at the discontinuity. Jan-Mar, one definition: 71 → 74, a real +3-point drift. Mar-Apr, spanning the change: +7 points in one month — precisely when the denominator shrank by excluding a category of tickets (and note the excluded category, customer-information-dependent tickets, is plausibly *enriched* in non-first-time fixes, so its removal mechanically inflates the rate). Apr-Jun, new definition: 81 → 83, again a real +2-point drift. So the defensible conclusions are: modest genuine improvement within each regime, and an unquantified discontinuity between them — option B, with the like-for-like recomputation as the operative request; a supplier who agreed the definition change can compute both series, and a customer who signs the report without asking has converted a measurement change into a performance narrative. Option A reads across the discontinuity as if it were performance. Option C overclaims in the other direction — the within-regime drifts are real. Option D confuses *agreeing a definition* with *agreeing to blur history*: agreed changes still require restated baselines, which is the sentence to put in the service review minutes. Vendor accountability is substantially the discipline of never letting a metric's definition move without its history moving with it.

**Question 9 (hard) — Penalty threshold edge case**

Your contract states: "If severity 1 incident count exceeds 6 in any rolling 3-month window, a performance review is triggered; if the count exceeds 6 in two consecutive rolling windows, a 10% service credit applies to the third month's charge." Monthly severity 1 counts: Jan 2, Feb 3, Mar 2, Apr 1, May 4, Jun 3. Monthly charge £90,000. Which windows trigger, and what credit applies?

- A) No window exceeds 6; no trigger, no credit.
- B) Jan-Mar (7) triggers a review; Feb-Apr (6) does not exceed 6; no consecutive breach, so no credit.
- C) Jan-Mar (7) and Feb-Apr (6) both breach; £9,000 credit.
- D) Jan-Mar (7), Apr-Jun (8) both breach; £9,000 credit.

**Correct answer: B**

**Explanation:** Compute every rolling window, then read the clause's operators exactly. Jan-Mar: 2 + 3 + 2 = 7 — *exceeds* 6: review triggered. Feb-Apr: 3 + 2 + 1 = 6 — equals 6, and "exceeds 6" means strictly greater than 6, so *no* breach. Mar-May: 2 + 1 + 4 = 7 — exceeds 6: a second review trigger. Apr-Jun: 1 + 4 + 3 = 8 — exceeds 6: a third. Now the credit clause: it requires breaches in two *consecutive* rolling windows. The breaching windows are Jan-Mar, Mar-May, and Apr-Jun. Jan-Mar and Feb-Apr are consecutive windows, but Feb-Apr did not breach — so the first pair fails. Mar-May and Apr-Jun *are* consecutive rolling windows, and both breach — so the credit clause fires after all... unless the contract means consecutive *calendar-quarter* windows rather than consecutive rolling ones. Read the options against the strict rolling-window reading: Mar-May (7) and Apr-Jun (8) are consecutive and both exceed 6, which would yield a £9,000 credit — but no option offers that pairing; option D pairs Jan-Mar with Apr-Jun, which are not consecutive windows. The best-supported listed answer is B, which correctly identifies the Jan-Mar trigger and correctly rejects Feb-Apr — and the gap between B and the full rolling analysis is this question's deliberate sting: *the answer depends on window semantics the clause never defines*. In an assessment, choose the option whose stated reasoning contains no error — B's reasoning is accurate as far as it goes, while C and D assert false window arithmetic. In your contracts, this question is a to-do item: "rolling window", "consecutive", and "exceeds" must each be defined with worked examples in the schedule, because the difference between readings is £9,000 per occurrence and an argument you will otherwise have during an incident review. Principals who write worked examples into contract schedules never have this argument.

**Question 10 (hard) — Cost of attrition versus development investment**

Your 15-engineer team has averaged 20% annual attrition. Each departure costs an estimated £45,000 (recruitment, onboarding, and six months of reduced productivity). An engagement-and-development programme costing £75,000 per year is projected to reduce attrition to 12%. What is the projected annual net saving, and what is the soundest framing of the case?

- A) Net saving £33,000 per year: attrition falls from 3.0 to 1.8 departures (saving 1.2 × £45,000 = £54,000)... which is less than £75,000, so actually a net cost of £21,000 — the programme fails on direct savings and should be rejected.
- B) Direct arithmetic: 20% of 15 = 3.0 departures; 12% of 15 = 1.8; the 1.2 avoided departures save 1.2 × £45,000 = £54,000 against £75,000 — a direct net cost of £21,000 — so the case must rest honestly on the benefits the model excludes: retained tacit knowledge, team stability, reduced key-person risk, and delivery continuity; present it as "£21,000 net cost buys these named risk reductions", not as a cash-positive case.
- C) Net saving £54,000 — the programme pays for itself.
- D) Attrition figures are too uncertain to model; decide on instinct.

**Correct answer: B**

**Explanation:** The arithmetic: 20% × 15 = 3.0 expected departures; 12% × 15 = 1.8; avoided departures 1.2; direct saving 1.2 × £45,000 = £54,000; against £75,000 cost, direct net = −£21,000. Option C stops at the gross saving. Option A performs the same arithmetic and then draws the falsely decisive conclusion — rejection — as if the £45,000 unit cost captured a departure's full price, which it explicitly does not: it prices recruitment and ramp-up, not the walked-out-the-door knowledge of the payments integration (recall the key-person risks in your own portfolio), not the churn-begets-churn dynamic, not the delivery commitments that slip. Option B does what principal-level cases must: runs the honest arithmetic, *loses* the narrow cash argument, and then makes the real argument on named, ownable grounds — a £21,000 annual premium purchasing specified risk reductions is a legitimate, governable proposition, and framing it that way survives the finance partner's scrutiny in a way a massaged cash-positive version never would. Option D abandons quantification because it is incomplete — but incomplete models bound decisions usefully; instinct bounds nothing. Leading on resourcing means making exactly these cases, and the credibility rule is permanent: never torture a people-case into cash-positivity — name the premium, name what it buys, and let governance decide with true numbers.

**Question 11 (hard) — User outcome data for a strategy decision**

Two services deliver a similar citizen outcome. Your strategy must pick one as the target platform. Data: Service P — 240,000 users/year, 78% task completion, 4.1/5 satisfaction (survey n=8,200), and completion has risen 2 points/year for three years. Service Q — 60,000 users/year, 85% task completion, 4.4/5 satisfaction (survey n=310), completion flat for three years. A stakeholder argues: "Q outperforms P on both completion and satisfaction — consolidate onto Q." What is the soundest analytical response?

- A) The stakeholder is right: 85% beats 78% and 4.4 beats 4.1.
- B) Q's headline figures lead, but the decision needs three corrections first: (1) scale — P serves 4× the users, so per-year, P completes ~187,200 tasks versus Q's 51,000, and P's failures (52,800) dwarf Q's user base; consolidation means Q's design absorbing 4× its current load, an untested claim; (2) trajectory — P is improving 2 points/year while Q is flat, so the gap (7 points) closes within ~4 years on trend; (3) evidence weight — Q's satisfaction rests on n=310 (0.5% of its users) versus P's n=8,200; the Q figure carries far more sampling uncertainty and plausible self-selection. The right next step is a structured comparison: task-level analysis of *why* P's 22% fail, and load-realistic evaluation of Q — before either platform is anointed.
- C) Consolidate onto P immediately, since it is bigger.
- D) Run both indefinitely to preserve choice.

**Correct answer: B**

**Explanation:** Each correction is decision-relevant, not pedantic. Scale: percentages abstract away volume, but consolidation is a volume event — the operative question is not "which service scores better?" but "which service, carrying 300,000 users/year, produces the most completed tasks?", and Q has never been tested within an order of magnitude of that load (its 85% may be *because* of its scale: smaller services often serve narrower, more homogeneous user groups — a **User focus** insight about who the users actually are). Trajectory: strategy decisions bind for years, so trend lines belong beside snapshots — a 7-point gap closing at 2 points/year vanishes inside the consolidation programme's own delivery window. Evidence weight: n=310 self-selected respondents from 60,000 users is a satisfaction *indication*, not a measurement to bet a platform on; distinguishing evidence grades is precisely the "quantitative and qualitative data" fluency your **User focus** skill demands of the person who represents users internally. Option A takes headline numbers at face value across all three corrections. Option C replaces one unexamined heuristic (higher score wins) with another (bigger wins). Option D deserves respect as an option — but "indefinitely" concedes the strategy's job, which is to decide; preserving optionality has a cost (duplicate run-costs, split development) that the strategy owner must price, not ignore. B's close — decide *after* failure analysis and load-realistic evaluation — is what "prioritise and define approaches to understand the user story" looks like when the user story is about to be consolidated.

**Question 12 (hard) — Reading a portfolio dashboard honestly**

Your portfolio dashboard summarises the year: total incidents down 18%; mean time to restore down from 4.1h to 3.2h; change success rate up from 91% to 96%; availability up in four services of five. The fifth service — the data exchange — shows: incidents up 40% (from 10 to 14), availability down from 99.9% to 99.6%, and it now sits on the critical path of three other services' user journeys. Your governance summary is due. What is the soundest headline?

- A) "Portfolio performance improved across all major indicators" — the aggregates support it.
- B) "Portfolio performance improved on every aggregate measure; however, the data exchange service deteriorated materially (incidents +40%, availability 99.9% → 99.6%) and, because three user journeys now depend on it, its 0.3-point availability fall degrades the end-to-end experience of most of the portfolio's users — remediation is the year's priority investment despite the green aggregates."
- C) "Mixed results this year; some services improved, others declined."
- D) "The data exchange decline shows the portfolio is failing; the aggregate improvements are not meaningful."

**Correct answer: B**

**Explanation:** The aggregates are genuinely good and genuinely misleading, and the honest headline carries both facts with their *weights*. The dashboard's arithmetic conceals a structural fact it was never designed to see: the deteriorating service is the one on the critical path — recall the series-availability multiplication from Question 5: a 0.3-point fall in a component that three journeys traverse degrades *every one of those journeys' end-to-end availability by roughly the same amount*, so the portfolio's users experience the fifth service's decline far more than the four services' improvements. Weight by user exposure, not by service count. Option A is true of the aggregates and false of the user experience — and it silently spends the credibility your dashboards will need next year. Option C is the coward's accuracy: "mixed" conveys no structure, no priority, and no decision — governance summaries exist to allocate attention, and C allocates none. Option D inverts A's error, discarding real improvements to dramatise the exception. Option B is the principal's sentence: aggregates credited, the exception quantified, the *mechanism* of its importance explained (critical-path dependency — your **Service focus** bigger-picture duty made legible to a board), and the conclusion converted into an investment priority. The deepest numeric skill this guide can rehearse is exactly this: the numbers' final form is a sentence with a decision in it, and the sentence must be one that remains true when someone recomputes everything underneath it.

### Preparation tips

- **Model in years and steps, not formulas.** Compounding growth, escalating contracts, and capacity exhaustion all yield to a simple year-by-year table. Build the table first; insight and error-resistance both live there.
- **Value shifts by differences.** Defect-stage economics, attrition savings, option comparisons — the benefit of moving something is the *difference* between states, and the net requires subtracting the investment. Gross-benefit options are always among the decoys.
- **Multiply series availability.** Any user journey crossing components is a product, not a minimum. Memorise the reflex: three nines in series is not three nines.
- **Partition at every discontinuity.** Definition changes, remedies, regime shifts: compute within segments, never across them, and demand restated baselines when definitions move.
- **Read comparison operators as written.** "Exceeds 6" excludes 6; "consecutive windows" needs a definition; "within 14 days" needs a start date. Contract arithmetic is exact arithmetic on exact words.
- **End every calculation in a sentence.** Practise converting each result into the one-line decision it supports, with its main caveat attached. That conversion is the actual principal-level skill being assessed — and the one your governance papers live by.

### Common pitfalls to avoid

- **Signing gross numbers.** Benefits without their costs, savings without their investments, credits without checking the band structure — the incomplete version of every figure is always the flattering one.
- **Comparing across a definitions change.** A 12-point improvement spanning a denominator change is a measurement artefact wearing a trend's clothes. Partition first.
- **Trusting percentages divorced from volumes.** An 85% completion rate on 60,000 users and a 78% rate on 240,000 users rank one way as percentages and the other way as outcomes. Carry both.
- **Letting aggregates absolve exceptions.** Portfolio-level greens can coexist with a critical-path red that dominates user experience. Weight by exposure before headlining.
- **Torturing people-cases into cash-positivity.** When the direct arithmetic loses, say so, and argue the named risk reductions honestly. Massaged cases are discovered, and their discoverers remember.
- **Answering edge cases the contract hasn't defined.** When your working exposes an ambiguity ("exceeds", "rolling", "consecutive"), the assessment answer is the option with error-free reasoning — and the workplace answer is fixing the schedule's definitions before the edge case costs money.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you extract meaning, obligation, and implication from the binding and consequential text your role runs on: contracts and schedules, departmental mandates, strategy papers, audit reports, governance submissions, and supplier correspondence. The core format presents a passage followed by statements to classify as **True** (supported), **False** (contradicted), or **Cannot say** (insufficient basis); complementary formats test inference, best-summary judgement, and the evaluation of written argument and drafting quality.

The typical format is an online, timed test of 15 to 25 minutes with 20 to 30 statements across several passages, often with senior norm groups. The discipline — answer from the passage alone — is hardest for the most experienced readers, and that is by design: principals carry decades of pattern knowledge about how contracts, audit findings, and strategies *usually* read, and the test detects whether you read the instant document or your priors about documents like it. The professional stakes of that discipline are highest at your level: the clause that deviates from convention is precisely the one your counterparty's lawyers drafted deliberately, and the audit finding that says less than it seems to is precisely the one whose management response you must calibrate.

Why do employers use verbal reasoning assessments for this role? Because principal-level work is substantially the production and consumption of consequential text. You own a strategy others will execute from its words; you are accountable for supplier relationships that live in schedules and definitions; you respond to audits where the difference between "we accept the finding" and "we accept the recommendation" is material; and you write the governance papers in which your organisation's understanding of its own estate is constituted. Reading exactly, inferring soundly, and writing what you mean are not adjacent skills to this work — they are the work.

The passages below reflect your genuine document diet: a supplier contract schedule, an internal audit extract with a management response, and a strategy consultation exchange. Read each as text you are about to be held to.

### How this assessment maps to your role

- **Contractual precision** maps to your **vendor and supplier management accountability**: obligations, carve-outs, thresholds, and definitions are where supplier performance is actually decided — reading them exactly is the precondition of enforcing them.
- **Audit and compliance comprehension** maps to **Asset and configuration management**: managing service compliance and risk includes reading findings for what they establish, what they merely suggest, and what a management response commits you to.
- **Strategy and mandate reading** maps to **Technical specialism** and **Service focus**: intersecting departmental mandates with technology direction, and seeing the bigger picture across services, both begin with exact comprehension of what the governing documents actually require.
- **Framework definitional fluency** maps to **Service management framework knowledge**: expert-level certification is, in large part, examined definitional precision — the habit generalises to every defined term you meet.
- **Inference discipline** maps to **Problem management** and **Incident management**: ensuring the right investigative actions and leading incident resolution both require the stated/implied/unexcluded distinction under pressure.
- **Writing and argument judgement** maps to your strategy ownership and **User focus** advocacy: the papers you write — and the user evidence you carry into governance — succeed exactly insofar as they cannot be reasonably misread or discounted.

### Practice questions

**Passage 1 — Supplier contract schedule extract**

*"Schedule 4, clause 7: The Supplier shall resolve severity 1 incidents within four hours of notification. Time consumed awaiting information that the Supplier has reasonably requested from the Customer shall be excluded from the resolution time calculation ('the clock is stopped'). The Supplier shall notify the Customer in writing when the clock is stopped and when it resumes. Failure to meet the resolution target in any calendar month triggers service credits per Schedule 5, save where the failure arises from a Force Majeure Event or from defects in Customer-provided infrastructure. The Supplier's obligation under this clause is conditional on the Customer maintaining the notification contact register in accordance with clause 12. For the avoidance of doubt, resolution means restoration of service to users; it does not require root cause remediation, which is addressed in clause 8."*

**Question 1 (easy) — True, false, or cannot say**

Statement: "The supplier must fix the root cause of a severity 1 incident within four hours."

- A) True
- B) False
- C) Cannot say
- D) True, unless the clock is stopped

**Correct answer: B**

**Explanation:** The clause's final sentence resolves it explicitly: "resolution means restoration of service to users; it does not require root cause remediation, which is addressed in clause 8." The four-hour obligation attaches to restoration, not to root cause — the statement is contradicted: False. The "for the avoidance of doubt" sentence exists precisely because this conflation is common and expensive: a customer who believes four hours buys root cause will accept workaround-plus-closure as breach, souring a compliant relationship, or worse, will fail to chase clause 8's separate remediation obligations because they believe clause 7 covered them. Option D grafts the clock-stop mechanism onto a misread obligation — decorating an error does not repair it. Reading definitions before obligations is the first rule of contract comprehension: the defined term "resolution" does the clause's real work, and your accountability for supplier management is exercised one defined term at a time.

**Question 2 (easy) — True, false, or cannot say**

Statement: "If the customer's notification contact register is out of date, the supplier may not be bound by the four-hour resolution obligation."

- A) True
- B) False
- C) Cannot say
- D) False — supplier obligations cannot depend on customer behaviour

**Correct answer: A**

**Explanation:** The clause states: "The Supplier's obligation under this clause is conditional on the Customer maintaining the notification contact register in accordance with clause 12." A conditional obligation lapses (or is at least disputable) when its condition fails — so an out-of-date register genuinely jeopardises the four-hour commitment: True, and the cautious "may not be bound" matches the conditionality precisely. Option D asserts a principle contracts flatly refute daily: supplier obligations routinely depend on customer performance, and such conditions are among the first places a supplier's lawyers look when resisting a service credit claim. The operational moral belongs on your risk register: buried customer obligations — a contact register, an access provision, a data feed — are *your* compliance surface (**Asset and configuration management**: manage service compliance and risk), and the time to inventory them is at signature, not during the first disputed severity 1. Principals who maintain a "customer obligations register" for each contract never discover a lapsed condition from the supplier's rejection letter.

**Question 3 (moderate) — True, false, or cannot say**

Statement: "A severity 1 incident that took six clock-hours to resolve, including two hours awaiting information the supplier had reasonably requested from the customer, meets the contractual target."

- A) True
- B) False
- C) Cannot say
- D) False — six hours exceeds four hours

**Correct answer: C**

**Explanation:** Run the calculation the clause defines: six clock-hours minus two excluded hours (reasonably requested customer information) = four hours of counted resolution time, and the target is resolution "within four hours". Exactly four hours against a "within four hours" obligation — does "within" include the boundary? Conventionally yes, and on that reading the target is met. But the passage contains a second, unresolved condition: the supplier "shall notify the Customer in writing when the clock is stopped and when it resumes" — and the statement is silent on whether written notification occurred. If the notification duty is a *precondition* of the exclusion, an unnotified clock-stop may not count, making the time six hours and the target missed; if it is a freestanding duty whose breach doesn't void the exclusion, the target is met. The passage does not settle which reading governs, and the statement omits the fact needed to apply either. With the outcome genuinely dependent on unstated facts and an unresolved construction, the answer is Cannot say. Option D ignores the exclusion mechanism entirely; option A assumes both the boundary reading and the notification compliance. This is the highest verbal discipline: recognising when a confident-sounding calculation rests on facts the text has not supplied — the same discipline that stops you accepting (or rejecting) a supplier's monthly figures before asking to see the clock-stop notices.

**Question 4 (moderate) — Inference from the schedule**

Which one of the following can properly be inferred from the passage?

- A) Service credits are calculated as a percentage of monthly charges.
- B) The contract's architecture separates restoration (clause 7) from root cause remediation (clause 8) and prices only restoration failures through Schedule 5's credits — so persistent root-cause neglect would need to be pursued through clause 8's own mechanisms, whatever they are, rather than through this clause's credits.
- C) Force Majeure Events are defined in Schedule 4.
- D) The supplier has previously failed to meet the four-hour target.

**Correct answer: B**

**Explanation:** Option B assembles only what the passage states — resolution excludes root cause remediation (final sentence); credits attach to resolution-target failures (Schedule 5 trigger); root cause lives in clause 8 — into the structural consequence those facts compel: this clause's financial teeth bite restoration failures only, so a supplier could meet every four-hour target while root causes recur indefinitely, and the remedy for *that* pattern must be found in clause 8, about whose content the inference carefully claims nothing ("whatever they are"). That is inference done properly: architecture from stated parts, no imported facts. Option A invents the credit mechanism's shape — Schedule 5 is referenced, never described. Option C invents a definition's location. Option D invents history. The professional payoff of inference B is a reading checklist: having seen that clause 7's credits cannot touch recurring root causes, your next act is to read clause 8 *for its teeth* — if it turns out to contain obligations without remedies, you have found the contract's soft spot before the supplier's commercial team relies on it. Reading a contract as an architecture of incentives, not a list of promises, is the principal-level version of this assessment skill.

**Passage 2 — Internal audit extract and management response**

*"Finding 3 (Moderate): Of 40 sampled production changes, 37 had complete approval records. Three changes, all emergency changes implemented by the applications team during major incidents, lacked evidence of retrospective approval within the required five working days; approvals were recorded 8, 11 and 15 working days after implementation respectively. We did not identify any adverse service impact from these three changes. The control design is adequate; the exception relates to operating effectiveness under incident conditions. Recommendation: implement a compensating checkpoint to ensure retrospective approvals are obtained within the required period following emergency changes. Management response (Principal Application Operations Engineer): Accepted. A weekly review of open emergency-change approvals will be added to the operations governance meeting from next month, with escalation to the service owner for any approval outstanding beyond five working days. Target date: end of Q2."*

**Question 5 (moderate) — True, false, or cannot say**

Statement: "The audit found that emergency changes caused service impact because approvals were late."

- A) True
- B) False
- C) Cannot say
- D) True — that is why the finding is rated Moderate

**Correct answer: B**

**Explanation:** The finding states the reverse on both elements: "We did not identify any adverse service impact from these three changes" — so no impact was found, and *a fortiori* no causal chain from late approval to impact was asserted. The statement is contradicted twice over: False. Option D reasons backwards from the rating, but audit ratings price *control weaknesses* — the risk a lapse represents — not realised harm; a Moderate rating with zero observed impact is perfectly coherent (and common), because the audit's question is "would this control catch the bad day?", not "has the bad day happened?". This distinction disciplines your management responses (**Asset and configuration management**: manage service compliance and risk): responding to findings as if they alleged harm produces defensive, over-engineered responses; responding to them as control-effectiveness observations — as the actual response in the passage does, with a proportionate compensating checkpoint — produces governance that auditors and operators can both live with. Reading audit language for what it *establishes* versus what it *prices* is a distinct comprehension register, and assessments at senior levels sample it deliberately.

**Question 6 (moderate) — True, false, or cannot say**

Statement: "The audit concluded that the emergency change control is badly designed."

- A) True
- B) False
- C) Cannot say
- D) True — three failures in forty proves poor design

**Correct answer: B**

**Explanation:** The finding draws the design/effectiveness distinction explicitly: "The control design is adequate; the exception relates to operating effectiveness under incident conditions." The audit's conclusion is thus the opposite of the statement's claim — the design passed; the *operation* of the control lapsed under incident pressure: False. This vocabulary is load-bearing in audit practice: a design deficiency means the control, even perfectly operated, would not achieve its objective (remedy: redesign); an operating effectiveness exception means the control works as designed but was not consistently performed (remedy: operational reinforcement — which is exactly what the management response supplies, a weekly review with escalation rather than a new control regime). Option D's "three failures prove poor design" commits the category error the distinction exists to prevent — failure frequency speaks to operation, not design, unless the failures trace to the control's structure. Your expert service management certification (**Service management framework knowledge**) examines precisely such definitional pairs, and the practical stakes recur every audit cycle: management responses that misdiagnose effectiveness exceptions as design flaws buy expensive redesigns of adequate controls, while the actual lapse — humans under incident pressure — goes unaddressed.

**Question 7 (hard) — Evaluating the management response**

Which is the most accurate critical assessment of the management response as drafted?

- A) It is inadequate because it does not prevent late approvals, only detects them.
- B) It is proportionate and answers the recommendation: a weekly review cycle detects any approval outstanding early in the five-working-day window and adds escalation force; however, two drafting gaps remain — a weekly cadence can leave an approval undetected for up to ~5 working days if the lapse begins just after a meeting (marginal against a five-day requirement), and the response names no owner for producing the open-approvals list, which is the operational step most likely to silently fail.
- C) It is excessive: three exceptions with no impact require no response.
- D) It is inadequate because the target date should be immediate.

**Correct answer: B**

**Explanation:** Assess the response against the recommendation's own terms — a "compensating checkpoint to ensure retrospective approvals are obtained within the required period". A weekly governance-meeting review is a checkpoint; escalation to the service owner adds consequence; and the audit itself rated the design adequate, so reinforcement rather than redesign is the *correct* register (which disposes of option A: the recommendation asked for a compensating detective checkpoint, not prevention — criticising the response for matching the ask misreads the ask; prevention during a major incident is exactly what the emergency-change route exists to relax). Option C refuses an accepted Moderate finding — a position a principal can take, but then the honest response is "risk accepted" with justification, not silent under-delivery; having written "Accepted", the commitment must be real. Option D manufactures urgency the finding does not carry. Option B's two residual criticisms are the genuinely expert content: the cadence arithmetic (a weekly check against a five-working-day requirement leaves worst-case windows where a lapse completes before detection — the fix is checking approvals *raised* since the last meeting, not just outstanding ones) and the unnamed list-producer (governance meetings review what someone prepares; unowned preparation is how compensating controls quietly die, and the next audit finds the checkpoint itself lapsed). Reading your own commitments as an auditor will read them — cadence against requirement, owner against task — is the drafting standard this question rehearses, on a document type you sign several times a year.

**Passage 3 — Strategy consultation exchange**

*"Extract from the draft application strategy: 'By 2030, the casework estate will consolidate from four applications to two, both cloud-hosted on the strategic platform. The consolidation is expected to reduce run costs by 30% and requires the completion of the data exchange modernisation as a precondition. Should the modernisation be delayed beyond 2027, the consolidation timeline will be re-baselined rather than compressed, as compression was assessed as carrying unacceptable delivery risk.'*

*Consultation comment from the Head of Casework Operations: 'The 30% figure is presented without a baseline year and without stating whether it is net of migration costs. My teams also note that the two retained applications are not named, which makes workforce planning impossible. We support consolidation in principle but cannot plan against this draft.'*

*Author's note appended to the draft: 'Baseline and cost treatment to be added in v0.9. Application selection follows the Q3 options analysis; naming them now would pre-empt it.'"*

**Question 8 (moderate) — True, false, or cannot say**

Statement: "If the data exchange modernisation slips to 2028, the strategy commits to compressing the consolidation schedule to hold the 2030 date."

- A) True
- B) False
- C) Cannot say
- D) True — 2030 is stated as a firm commitment

**Correct answer: B**

**Explanation:** The strategy pre-answers this exact contingency, in the opposite direction: "Should the modernisation be delayed beyond 2027, the consolidation timeline will be re-baselined rather than compressed, as compression was assessed as carrying unacceptable delivery risk." A slip to 2028 is a delay beyond 2027; the committed response is re-baselining — moving the date — not compression: the statement is contradicted, False. Option D elevates the 2030 ambition over the document's own contingency clause, a misreading with a real-world signature: stakeholders remember headline dates and forget the conditionality attached to them, then experience the re-baseline as a broken promise. That is why well-drafted strategies state their contingency behaviour *in the text*, as this one does — and why, as the strategy's owner, you will repeat the conditionality every time you present the date. A strategy that pre-decides its response to foreseeable slippage — and documents that compression was *assessed* and rejected, not merely disliked — is exhibiting the drafting standard your own papers should meet: the governance board that approved this text has already approved the re-baseline, which converts a future bad month into an executed plan rather than a crisis meeting.

**Question 9 (hard) — True, false, or cannot say**

Statement: "The consultation comment disputes the value of consolidating the casework estate."

- A) True
- B) False
- C) Cannot say
- D) True — the comment says planning against the draft is impossible

**Correct answer: B**

**Explanation:** Read the comment's actual position: "We support consolidation in principle but cannot plan against this draft." The objection targets the draft's *specification* — an unbaselined 30%, unstated cost treatment, unnamed retained applications — not the consolidation's value, which the comment explicitly endorses. The statement is contradicted: False. Option D quotes the comment's strongest phrase while inverting its object: "cannot plan against this draft" criticises the draft's plannability, not the strategy's merit. This distinction — challenge-to-substance versus challenge-to-specification — is among the most consequential a strategy owner can draw, because the two demand opposite responses: substance challenges need persuasion or decision; specification challenges need *drafting work*, and treating the latter as the former (defending the strategy's value to someone who already supports it) is how consultations curdle. The Head of Casework Operations is, in fact, the strategy's ideal reader: a supporter demanding the precision that would let them execute it. The author's note answers one specification gap credibly (naming applications would pre-empt the Q3 options analysis — a legitimate sequencing reason, honestly stated) and defers the other to v0.9. Your consultation responses, like your reading of this one, should sort every comment into substance or specification before replying — the sort determines the reply.

**Question 10 (hard) — Inference from the exchange**

Which one of the following can properly be inferred from the exchange?

- A) The 30% run-cost reduction figure is wrong.
- B) The strategy's author has confused run costs with total costs.
- C) As drafted, the 30% claim is unverifiable and unauditable: without a baseline year and a stated cost treatment, no future reader can determine whether the reduction was achieved — so the figure currently functions as ambition, not measurement, and v0.9's additions are what will convert it into a testable commitment.
- D) The consolidation will save less than 30% once migration costs are included.

**Correct answer: C**

**Explanation:** Options A, B and D all assert facts about the *true* costs or the author's *understanding* — matters on which the exchange is silent: the 30% may be right, conservatively right, or wrong; the author may hold a perfectly clear cost model whose parameters simply are not yet in the text. What the exchange does establish is a property of the claim *as drafted*: a percentage without a baseline year ("30% less than *what*, measured *when*?") and without cost treatment ("net of the migration spend, or gross?") cannot be verified by any future reader against any future actuals — which is exactly the consultation comment's substance, and the author's note concedes it by scheduling the fix. Inference C states that property and its consequence (ambition versus testable commitment) without asserting anything the text withholds. The distinction being rehearsed — between *the claim is false* and *the claim is not yet checkable* — is the auditor's distinction from Passage 2 wearing strategic clothes, and it is one your role applies in both directions: to claims you receive (a supplier's "40% faster", a programme's "£2m saved") and to claims you make. The strategy you own should contain no number that a sceptical successor, five years hence, cannot test against a stated baseline — because that successor's audit of your strategy is, eventually, the measure of it.

**Question 11 (hard) — Best summary of the exchange for a governance board**

Which option best summarises the consultation exchange for the strategy's governance board?

- A) "Casework operations opposes the consolidation strategy; resolution required."
- B) "Consultation feedback is being handled; no board attention needed."
- C) "Casework operations supports consolidation in principle. Their comment identifies two specification gaps: the 30% saving lacks a baseline and cost treatment (author will fix in v0.9), and the retained applications are unnamed (deliberately — selection follows Q3's options analysis, though this defers their workforce planning). Board attention: confirm the v0.9 additions land, and note that workforce planning remains blocked until the Q3 selection — a sequencing cost the board should consciously accept or accelerate."
- D) "The strategy draft contains errors in its savings figures which are being corrected."

**Correct answer: C**

**Explanation:** Score each candidate against what a governance board needs: accurate positions, real issues, their handling status, and the residual decisions that belong to the board. Option A misreports a supporter as an opponent — the substance/specification confusion from Question 9, now propagated into governance record, where it would manufacture a conflict and poison the strategy's most useful critical friend. Option D converts "unverifiable as drafted" into "contains errors" — the inference discipline of Question 10 failed in summary form; the board would carry a false belief about its own strategy's accuracy. Option B is the subtler failure: "no board attention needed" is false, because the exchange contains a genuine board-level trade-off — the Q3 sequencing decision blocks a stakeholder's workforce planning, and *someone with authority* should consciously own that cost rather than let it ride as a drafting footnote. Option C reports the support accurately, states both gaps with their handling, and — its distinguishing move — converts the residue into explicit board asks: verify the fix lands, and *decide* on the sequencing cost. Summaries that end in named decisions are how principals use governance rather than merely report to it; summaries that end in reassurance are how boards discover problems late. The drafting standard generalises to every paper you write: a governance summary's quality is measured by the decisions it makes possible, not the calm it projects.

**Question 12 (hard) — Clear-writing judgement in strategy drafting**

The v0.9 revision must restate the savings claim properly. Which drafting best serves the strategy's readers?

- A) "The consolidation will deliver significant run-cost savings, currently estimated at approximately 30%, subject to detailed analysis and prevailing conditions."
- B) "Run costs for the four-application casework estate were £8.2m in FY2025-26 (baseline). Post-consolidation run costs are modelled at £5.7m per year (a 30% reduction against baseline) from the first full year after migration completes. This figure is gross of one-off migration costs, modelled at £3.1m and shown separately in Annex C; net cumulative saving becomes positive in year 3. Model assumptions and sensitivities: Annex C, section 2."
- C) "Savings of £2.5m per annum will be achieved."
- D) "The consolidation business case demonstrates compelling value for money across the appraisal period, in line with Green Book methodology."

**Correct answer: B**

**Explanation:** Apply the test that Question 10 established: can a sceptical future reader verify the claim? Option B, alone, survives it — and notice *how*: a named baseline year with its figure (£8.2m, FY2025-26), the target state in absolute and percentage terms, the timing convention ("first full year after migration completes" — the phrase that prevents year-1 disappointment being read as failure), the gross/net distinction with the migration cost stated and located, the payback year, and a pointer to assumptions. Every element answers a question the consultation comment asked or a question a successor will. Option A is the anti-draft: "approximately", "subject to", and "prevailing conditions" are solvent applied to accountability — it restates the ambition while armouring it against ever being tested, and a Head of Casework Operations reading it would correctly conclude the comment was managed, not answered. Option C states a verifiable number while deleting the baseline, timing, and cost treatment that make it interpretable — precision without context is option A's failure wearing confidence. Option D outsources the claim to a methodology's reputation: invoking Green Book compliance is not evidence, and strategies that cite frameworks in place of figures teach boards to stop reading. The principal drafting principle, worth carrying from this guide into your next strategy revision: write every quantified commitment so that the person who must verify it in five years — a successor, an auditor, a select committee — can do so from the document itself. That reader is the strategy's real audience, and your **Ownership and topic** accountability, projected forward in time.

### Preparation tips

- **Read definitions before obligations.** In any contract or standard, the defined terms ("resolution", "working days", "consecutive") carry the clauses. Find the definitions first; the obligations then read differently — and correctly.
- **Inventory conditions on the other party's duties.** Every "conditional on", "provided that", and "save where" is a place an obligation can escape. Practise extracting them into a two-column list: their duties, your conditions.
- **Hold the audit vocabulary precisely.** Design versus operating effectiveness, finding versus recommendation, impact observed versus risk priced, accepted versus risk-accepted. Statements and management responses that blur any pair are wrong — in tests and in your signature block.
- **Sort challenges before answering them.** Substance or specification? Support with conditions, or opposition? Reply to what the text actually says, not to its strongest-sounding phrase.
- **Practise the unverifiability finding.** For each claim you read this week, ask: could a stranger test this against stated baselines from the document alone? "Not yet checkable" is a distinct and powerful verdict — use it where it applies, in both directions.
- **Audit your own priors mid-passage.** When a clause reads exactly as you expected, re-read it once: the deviation you skimmed past is where senior-level questions — and counterparty lawyers — live.

### Common pitfalls to avoid

- **Answering from convention instead of the clause.** The more contracts you have read, the stronger the pull. This schedule, this finding, this draft — the instant text governs, and the deviations from convention are deliberate.
- **Confusing rating with harm.** A Moderate finding with no observed impact is coherent; ratings price control risk, not realised damage. Statements equating them are False.
- **Quoting a comment against its own position.** "Cannot plan against this draft" from a supporter is not opposition. Attribute positions from whole texts, not from their sharpest phrases.
- **Completing calculations the text left incomplete.** When an outcome depends on unstated facts (was the clock-stop notified?) or unresolved constructions (does "within" include the boundary?), the confident answer is Cannot say — and the workplace answer is fixing the definition.
- **Reading ambition as commitment, or vice versa.** Unbaselined percentages are ambitions; baselined, cost-treated figures are commitments. Summaries that promote one into the other propagate error into governance.
- **Preferring polished evasion in drafting questions.** "Subject to prevailing conditions" and "in line with methodology" are professional-sounding refusals to be testable. The best-drafted option is always the most verifiable one, not the most elegant.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace dilemmas and asks you to evaluate possible responses — most effective, least effective, or full rankings. At principal level, the scenario space shifts decisively toward the organisational: supplier relationships under strain, strategy under political pressure, integrity of governance information, development and succession of the leaders beneath you, and the long-term stewardship of culture, capability, and user outcomes. The options are rarely right-versus-wrong; they are competing goods — pace against margin, loyalty against evidence, this quarter against this decade — and the assessment measures which goods you serve first, and how skilfully you serve several at once.

The typical format is 12 to 20 scenarios, untimed or generously timed, four responses each, scored against the pooled judgement of experienced senior practitioners and the organisation's professional behaviours: accountability, honesty, user focus, collaboration across boundaries, developing others, and proportionate use of authority and governance. Principal-level scoring discriminates hardest on three things: whether you act at the right *altitude* (systems and people, not tasks); whether your choices are *durable* (would this response still look right in the post-incident review, the audit, the select committee?); and whether you build capability and trust as you act, or spend them.

Why do employers use SJTs for principal roles? Because at your level, judgement is the deliverable. Your role summary hands you ownership of the strategy, accountability for suppliers, leadership of resourcing and development, and — through **Ownership and topic** — accountability for issues that occur across an estate, with a proactive duty toward those that have not yet occurred. Every scenario below is drawn from that territory, and each explanation names the professional behaviours it turns on, so the practice doubles as a vocabulary for discussing judgement with the leads you develop.

As you work through, notice the recurring anatomy of strong principal answers: they protect users and truth first; they act through systems, standards, and people rather than personal heroics; they keep governance informed at the moment information becomes decision-relevant; they treat suppliers and peers as long-term relationships governed by evidence; and they convert every crisis into capability. Weak answers protect appearances, hoard decisions, spend trust for convenience, or optimise the quarter at the decade's expense.

### How this assessment maps to your role

- **Supplier crisis and negotiation scenarios** map to your **vendor and supplier management accountability**: performance failures, disputed classifications, commercial pressure, and relationship repair — handled with evidence, contract fluency, and proportionality.
- **Strategy-under-pressure scenarios** map to your ownership of the application strategy and **Technical specialism**: defending long-term positions against short-term raids, revising them honestly when facts change, and knowing which is which.
- **Governance and integrity scenarios** map to **Asset and configuration management** (compliance and risk) and **Change management**: what you sign, what you report, and what you allow to be reported are the currency of your accountability.
- **People and succession scenarios** map to your **resourcing, learning and development leadership**: growing leads, handling underperformance honestly, distributing opportunity, and building teams that outlast you.
- **Incident and problem command scenarios** map to **Incident management**, **Problem management**, and **Ownership and topic**: leading through your people during the worst hours, and owning the estate's latent risks before they mature.
- **User advocacy scenarios** map to **User focus**: representing users at the tables where they are absent, with evidence that survives seniority.

### Practice questions

**Question 1 (easy) — The supplier's commercial escalation**

Your supplier has missed its severity 1 resolution target three times this quarter; per the contract, £42,000 of service credits are due. The supplier's account director calls: "We're partners — invoking credits feels adversarial. We'd rather invest that amount in service improvements for you. Can we set the credits aside?" What is the most effective response?

- A) Waive the credits — the improvement investment is worth more than the cash, and the relationship matters.
- B) Apply the credits per the contract, and separately welcome an improvement plan on its own merits: state that credits are the contract's non-negotiable performance signal, that waiving them would misreport the quarter's performance in both organisations' records, and that a credible improvement plan is what you expect *in addition* — then review the plan's substance at the next service review.
- C) Split the difference: take half the credits.
- D) Escalate to commercial colleagues to terminate the relationship.

**Correct answer: B**

**Explanation:** Decompose the account director's offer: it converts a contractual entitlement (cash, certain, now) into a discretionary promise (improvements, unspecified, later) while — the quiet part — removing the performance failure from both organisations' financial records, which is worth more to the supplier's internal reporting than £42,000. Option B refuses the conversion while accepting the genuinely good half: improvement investment is welcome, *and* the credits apply — the two were never actually alternatives, and a supplier serious about improvement funds it anyway. The framing matters as much as the position: "the contract's non-negotiable performance signal" depersonalises the decision (it is not you being adversarial; it is the mechanism both parties agreed doing its job), which is how the relationship survives the firmness. Option A trades your successor's negotiating position for this quarter's warmth — waived credits become precedent, and precedent becomes the expectation that credits are an opening bid. Option C is the worst of both: half the money, all of the precedent. Option D detonates a functioning relationship over a quarter that the contract's own remedies are handling — proportionality is a scored behaviour, and termination is the remedy for relationships whose mechanisms have *failed*, not ones currently working as designed. Vendor accountability at principal level is exactly this: warm relationships, cold mechanisms, and the discipline never to let the first buy out the second.

**Question 2 (easy) — The strategy raid**

Mid-year, a director facing budget pressure proposes taking £400,000 from your funded application modernisation programme "just for this year — the legacy systems have run fine for a decade, one more year won't hurt". The modernisation exists because those legacy systems' supplier support ends in three years, and the programme's timeline already has only six months of margin. What is the most effective response?

- A) Concede — directors control budgets, and the programme can compress later.
- B) Refuse outright and copy your objection to the director's superior.
- C) Respond with the timeline arithmetic: the support cliff is fixed, the programme's six-month margin cannot absorb a year's delay, so the "one year" costs either an unsupported citizen-facing estate or an emergency-priced compression later; offer genuine alternatives if the budget pressure is real (descoping the programme's enhancement tier, deferring a lower-risk initiative), and ask that any decision to accept the risk be made explicitly at the governance board that owns the strategy — with the risk quantified in the paper.
- D) Agree publicly but quietly slow other spending to protect the programme.

**Correct answer: C**

**Explanation:** The proposal's engine is a false premise — "ran fine for a decade" reasons from past stability to future safety across a *known future discontinuity* (the support cliff), and the principal's first move is to correct the arithmetic, not to contest the authority: the money is takeable; what is not takeable is the consequence-free version of taking it. Option C does the three things this moment requires. It re-prices the request truthfully (the year costs an unsupported estate or emergency compression — recall that your own strategy assessed compression as unacceptable risk). It treats the director's budget problem as real, offering alternatives you actually control — which converts you from obstacle to partner and tests whether the pressure is genuine or merely shopping for the least-defended budget. And it routes the residual decision to the governance board that owns the strategy, because a director *can* legitimately decide to accept a quantified risk — but explicitly, on the record, at the table where the strategy was approved, not in a corridor against an unquantified one. Option A concedes a falsely-priced request and mortgages the estate. Option B escalates before persuading — spending the relationship and the issue's credibility at once. Option D is the honesty failure wearing loyalty's clothes: covert counter-budgeting, once discovered, ends careers and — worse — validates every future raid, since your public agreements are now known to be negotiable in private. Strategy ownership means the strategy is defended with arithmetic, alternatives, and explicit governance — never with concession or concealment.

**Question 3 (moderate) — Your lead's flawed governance paper**

A lead you have been developing submits their first major governance paper — a capacity investment case — for your review before Thursday's board. The technical analysis is strong, but the financial model contains an error that overstates the benefits by roughly 30%, and the paper's recommendation depends on the inflated figure. The lead has told colleagues how proud they are of the paper. What is the most effective response?

- A) Correct the model yourself tonight and submit the fixed paper under their name — protecting their debut and the board's timetable.
- B) Return it to the lead directly: walk through the error together, let them rework the model and re-derive the recommendation (which may change), and — if the rework cannot make Thursday — have them request the deferral themselves; frame the episode privately as the normal price of doing consequential work, and note that the technical analysis is genuinely strong.
- C) Submit the paper as-is to protect their confidence, and correct the figures verbally at the board.
- D) Submit it as-is; a 30% benefits overstatement is within normal estimating uncertainty.

**Correct answer: B**

**Explanation:** Two duties converge — the board must receive true figures, and the lead must actually develop — and option B is the only response serving both. The board duty first: options C and D put a known-false figure into governance under your review; D's "estimating uncertainty" defence fails because uncertainty is a property of honest estimates, not of identified errors — an error you have found and left in place is, from the moment of finding, a misrepresentation. C compounds it with the worst of both worlds: the written record (which outlives the meeting) stays wrong while your verbal correction publicly undercuts the lead anyway. The development duty next: option A fixes the paper and silently steals the learning — the lead presents a model they did not build, cannot defend under board questioning (a real risk to them, not a kindness), and remains one error away from repeating this at higher stakes; rescue is not development, a lesson that recurs at every level of leadership. Option B's mechanics are the craft: the error walked through *together* (diagnosis is the transferable skill), the rework *theirs* (as is the possibly-changed recommendation — let them experience evidence moving a conclusion), the deferral request *theirs* (owning timetable consequences is part of the job being learned), and the framing *generous* (error-in-review is the system working; the strong analysis is real and said so). Your learning-and-development leadership is precisely this transaction, repeated: standards held absolutely, people grown through — never around — their mistakes.

**Question 4 (moderate) — The incident spanning your suppliers**

A major outage is forty minutes old. Your application is down; your hosting supplier blames your database supplier's storage layer; the database supplier blames the hosting network. Each is technically credible, neither will commit engineering effort to the other's hypothesis, and your own team's lead is running the incident competently but cannot compel either supplier. Users — including an emergency casework unit — are down. What is the most effective response?

- A) Let the suppliers argue it out; the contract post-mortem will assign fault and costs afterwards.
- B) Join the incident yourself at the co-ordination level: convene both suppliers' duty managers on one bridge, invoke each contract's major-incident co-operation clause, direct a joint diagnostic plan that tests both hypotheses in parallel rather than sequentially, keep your lead in tactical command, and open the stakeholder channel to the casework unit with honest status and a workaround if one exists.
- C) Take over tactical command from your lead — this is too big for them.
- D) Pick the more likely hypothesis yourself and direct all effort at it to avoid splitting resources.

**Correct answer: B**

**Explanation:** Diagnose what is actually failing: not the technical investigation (your lead has it) but the *inter-organisational* layer — two suppliers optimising for non-attribution while the clock runs, a failure mode only authority applied at the commercial-relationship level can unlock. That is precisely the altitude your role occupies, and option B works it: duty managers on one bridge collapses the blame-by-correspondence game; the co-operation clauses (this is what they were negotiated for — invoke them by name) convert goodwill requests into contractual obligations; parallel hypothesis testing spends compute and engineers to buy time, the correct trade in a major outage (option D's efficiency instinct optimises the wrong variable — sequential testing is cheaper only if you guess right, and you have two credible hypotheses precisely because guessing is not yet possible); and the casework unit's honest status recognises that **User focus** during an outage means the users' operational continuity, not just their eventual service restoration. Option A treats attribution as the goal — the post-mortem will indeed assign costs, but users are down *now*, and "the contract will sort it out later" is abdication with paperwork. Option C pays the classic seniority tax: decapitating competent tactical command to feel useful, when the incident's actual gap is above the tactical layer, not in it — your lead commands the investigation; you command the conditions that let it succeed. The principal's incident question is always: *which layer of this failure is mine?* — and the answer is rarely the keyboard.

**Question 5 (moderate) — The compliance attestation**

The annual security compliance return is due in five days, requiring your attestation that all production applications meet the department's access-control standard. Your team's final checks reveal that one application — a low-traffic internal tool, but one processing citizen data — has a service account whose credentials have not rotated in three years, breaching the standard. Rotation requires a supplier change with a two-week lead time. Your head of function mentions the department "expects clean returns this year". What is the most effective response?

- A) Attest cleanly — the gap will be fixed two weeks after the return, and one service account on an internal tool is immaterial.
- B) Attest cleanly but keep an internal note of the exception in case questions arise.
- C) Submit the return with the exception declared: the specific non-conformance, its risk assessment (citizen data — not immaterial, whatever the traffic), the remediation already initiated with its two-week date, and interim mitigations applied now (restrict the account's scope, enhance monitoring); tell your head of function before submission that a clean return was available only as a false one.
- D) Delay the return until the rotation completes, then attest cleanly.

**Correct answer: C**

**Explanation:** Strip the scenario to its transaction: you are being asked what your signature is worth. Option A prices it at one awkward conversation — and misprices the gap itself, because "low-traffic internal tool" describes exposure *likelihood* while "citizen data" defines exposure *consequence*; three-year-old service credentials on citizen data is a textbook finding, and attestations are precisely the mechanism by which such findings surface. Option B is A plus evidence of knowledge — the internal note converts an error into a documented decision to misattest, the single worst artefact you can create. Option D games the calendar: the return describes the estate *as at the reporting date*, and delaying to launder the answer misrepresents by omission while also missing the deadline — two failures dressed as diligence. Option C is what compliance regimes are actually for: declared exceptions with risk assessments, initiated remediation, and interim mitigations are the system *working* — a return with one honest exception is more credible, not less, than a suspiciously clean one, and every auditor knows it. The conversation with your head of function belongs *before* submission and in exactly the form stated: "clean was available only as false" respects their expectation while making the integrity boundary unmistakable — and note that their "expects clean returns" was pressure, not instruction; answering it with truth *before the fact* protects them too. **Asset and configuration management** at principal level — manage service compliance and risk — is ultimately this: your attestation is the load-bearing joint between the estate's reality and the department's knowledge of it, and it bears load only while it is true.

**Question 6 (moderate) — Succession and the indispensable you**

Your head of function offers you a six-month secondment leading a cross-government programme — career-defining, starting in eight weeks. Honest stocktake: your deputy could cover strategy governance with support; your two leads can run operations; but supplier relationships live almost entirely in your head — undocumented, personally held, and mid-way through a difficult renewal. What is the most effective response?

- A) Decline the secondment — the renewal is too important to leave.
- B) Accept, and spend the eight weeks in intensive succession mode: document the supplier relationship history and strategy, bring your deputy into every renewal session as co-lead immediately, formally delegate decision authorities with written boundaries and escalation routes to you (time-boxed and rare), and treat the remaining gaps as the development opportunities they are — telling your head of function honestly which risks remain and how they are mitigated.
- C) Accept and handle the renewal remotely yourself during the secondment.
- D) Accept, and advise your deputy to pause the renewal until you return.

**Correct answer: B**

**Explanation:** Read the scenario's mirror first: supplier relationships living "almost entirely in your head" is not a fact about the secondment — it is a pre-existing organisational defect the secondment has merely exposed. A principal accountable for vendor management who is also a single point of failure *for* vendor management has a bus-factor problem identical to the one-engineer data exchange system in the cognitive section, and option A, declining, preserves the defect while sacrificing the career opportunity — the worst available trade, since eight weeks is genuinely enough for structured transfer if treated as the sprint it is. Option B is succession leadership under a deadline: documentation converts personal capital into organisational capital; *co-leading* the live renewal sessions transfers the relationships themselves, not just their records (relationships transfer through witnessed interaction, never through handover notes); written authority boundaries with rare, time-boxed escalation give the deputy real power plus a safety valve — delegation that keeps all decisions on your phone is option C wearing B's clothes. And the honest residual-risk conversation with your head of function makes them a party to the mitigation rather than a discoverer of the gaps. Option C guarantees a distracted programme *and* a stunted deputy — remote-controlling the renewal means the relationships still live in your head, just further away. Option D hands your counterpart's commercial team a six-month gift of drift and deadline pressure. Leading on resourcing and development includes the hardest case: developing your own replacement, on purpose, ahead of need — the principals who cannot be promoted are the ones who made themselves impossible to absent.

**Question 7 (moderate) — Least effective: the user research your strategy dislikes**

Commissioned user research on your flagship consolidated service returns findings that complicate your strategy: two user groups experience materially worse task completion on the strategic platform than on the legacy system it replaces, though overall averages improved. The research is methodologically sound. Your strategy refresh is due at the board next month. Which response is LEAST effective?

- A) Publish the findings internally as delivered, and commission targeted analysis of the two groups' task failures to inform remediation options in the strategy refresh.
- B) Present the findings at the board alongside the refresh: overall improvement, two groups worse off, remediation funded in the plan — letting the strategy absorb the evidence visibly.
- C) Ask the research team to reframe the report around the improved averages, moving the two groups' results to an annex, so the findings do not "distract" the board from the strategy's momentum.
- D) Meet the affected user groups' representatives to understand the failures qualitatively before finalising remediation.

**Correct answer: C**

**Explanation:** Polarity first: LEAST effective. Options A, B and D compose the honest playbook — publish as delivered, analyse the failures, hear the affected users directly, and put the evidence *in front of* the board attached to funded remediation; B in particular is strategy ownership at its best, a strategy visibly metabolising inconvenient evidence, which is what makes boards trust the convenient evidence too. Option C is the failure, and its mechanism deserves naming precisely because it is genteel: nothing is falsified — the averages are real, annexes are legitimate — yet the *reframing instruction* converts independent research into advocacy, and every future report from that team now carries the question of what else was reframed. It also specifically betrays your **User focus** remit: "champion user research to focus on *all* users" is the skill statement, and the two groups worse off are the entire reason averages are insufficient — burying distributional harm under aggregate improvement is the exact failure mode the skill exists to prevent (and a familiar one in public services, where the groups who fare worst on digital platforms are often those with least voice elsewhere). The deeper cost is epistemic: organisations whose leaders curate evidence stop producing true evidence — researchers learn what is wanted, and the strategy loses its sensory organs. A principal's power over what gets reported is held in trust for the organisation's ability to know things; option C spends it on a smoother meeting.

**Question 8 (hard) — The technology bet under uncertainty**

Your strategy must position the estate for the next decade. Your platform supplier is pushing aggressive adoption of its new AI-operations suite — auto-remediation, predictive scaling — with steep early-adopter discounts expiring in six months. Your assessment: the capabilities are promising but immature (two reference customers, both smaller than you), your team lacks the skills to operate them safely, and the department has no assurance framework for automated production interventions yet. The discount is worth ~£300,000 over three years. What is the most effective response?

- A) Adopt now across the estate — the discount is material, the direction is clearly right, and skills can follow.
- B) Decline engagement entirely until the technology matures and departmental assurance exists.
- C) Structure a bounded adoption: pilot the suite on one non-critical service with human-in-the-loop controls only, negotiate the discount against the pilot plus pre-agreed expansion pricing (declining the estate-wide commitment the discount is designed to force), invest in team skills in parallel, and contribute your pilot's evidence to the department's nascent assurance thinking — positioning the estate to scale adoption when maturity, skills, and assurance converge.
- D) Wait for the department's assurance framework, then follow whatever it permits.

**Correct answer: C**

**Explanation:** Name the discount's function first: expiring early-adopter pricing is a commercial instrument designed to convert your *evaluation* timeline into the supplier's *sales* timeline — the £300,000 is real, but it prices your option to decide later, and recognising that is your vendor accountability applied to procurement psychology. Option A pays for the discount with three unhedged risks the stem itemises: immaturity (two smaller references — your scale is the experiment), a skills gap (auto-remediation operated by a team that cannot audit it is automation of incidents), and an assurance vacuum (automated production interventions on citizen services without a departmental framework is the audit finding of 2028, pre-written). Option B avoids all three by forfeiting the learning: "understand the direction of future technologies" — your **Technical specialism** skill verbatim — is not satisfied by watching from shore, and estates that only ever fast-follow pay in perpetual lag. Option D outsources your judgement to a framework that does not exist yet — and note the inversion: your pilot evidence is precisely what the department's assurance thinking needs; principals *feed* emerging governance, they do not queue behind it. Option C is the strategist's structure: bounded exposure (one non-critical service, human-in-the-loop — the automation proposes, your people dispose, which is also how the skills gap closes), the commercial counter (pilot pricing plus pre-agreed expansion rates — testing whether the supplier's belief in its product survives the removal of the forcing function), and the deliberate convergence plan for maturity, skills, and assurance. The deep pattern, worth carrying into every emerging-technology decision your strategy will face: under uncertainty, the principal's job is not to pick the future but to buy cheap, bounded options on several futures — and to make sure the option's price is set by your timeline, not the vendor's.

**Question 9 (hard) — Ranking: the inherited misrepresentation**

Three weeks into a new principal post, you discover that your predecessor's flagship achievement — a migration reported to the board as "complete" eight months ago — is not: roughly 15% of records were never migrated, a reconciliation workaround runs nightly to mask the gap, two of your leads have known since before the report, and the workaround's failure would corrupt live casework data. Your predecessor now works for the departmental CIO. Rank these responses from most to least effective:

1. Stabilise first, then correct the record: commission an immediate risk assessment of the workaround, fund its hardening this week, then inform your head of function and the board with a factual paper — completion status, risk, remediation plan and cost — framed without personal attribution, while separately talking with the two leads about why they carried this silently and what safety would have let them speak.
2. Inform the board immediately and fully, this week, before any remediation work, so the record is corrected at the earliest possible moment.
3. Quietly complete the remaining 15% over the coming months under "data quality improvement", correcting the estate without reopening the reported history.
4. Report the situation first to the departmental CIO's office, since your predecessor's conduct is the central issue and their current employer should handle it.

- A) 1, 2, 3, 4
- B) 2, 1, 4, 3
- C) 1, 2, 4, 3
- D) 1, 3, 2, 4

**Correct answer: C**

**Explanation:** Response 1 leads because it sequences the three duties correctly: the *live risk* (a masking workaround whose failure corrupts casework data) outranks everything by days-not-months urgency, so assessment and hardening come first; the *record* is corrected promptly but with a remediation plan attached — a board told "the migration was misreported, here is the completion plan, cost, and hardened interim state" can govern, whereas a bare confession invites panic-directed remediation; and the *people* dimension is handled at the right depth — the leads' silence is treated as information about psychological safety under your predecessor, not merely as individual failure, while the paper's non-attributive framing keeps the correction about the estate, not the person (the conduct question is real, but it is your head of function's to route onward, informed by your factual paper — which is why response 4 is mis-sequenced rather than wholly wrong). Response 2 ranks second: its instinct — earliest correction of the record — is honourable and close to right; it loses to 1 only on the stabilisation gap (a week of workaround-hardening before the paper is risk management, not concealment, provided the paper is genuinely days away) — and 2 remains far ahead of the remaining options because its error is one of sequencing, not of integrity. Ranking 4 above 3 is the discriminating call: response 4 gets the *audience* wrong (leapfrogging your own head of function to report a predecessor to their current employer converts an estate-integrity issue into a personnel pursuit, and makes you the new principal whose first act was prosecution) — but it does *correct the record with someone*; response 3 corrects the *estate* while deliberately extending the record's falsehood indefinitely, making you the second consecutive principal to know and not say — the moment its "data quality improvement" label is understood (and labels are always understood eventually), your integrity is retroactively spent on your predecessor's behalf. A misdirected disclosure outranks a permanent concealment: 1, 2, 4, 3 — option C. The scenario's core teaching is the sequencing rule for inherited misrepresentation: *stabilise the risk, correct the record, address the people* — in that order, at pace, with the attribution question routed upward rather than seized. And its quiet corollary belongs in your first-hundred-days practice: the discovery was possible because you looked — new principals who audit what they inherit before praising it find these things while they are still someone else's misreport.

**Question 10 (hard) — The peer principal's failing service**

A peer principal's service — outside your portfolio — is visibly failing: public incidents, missed KPIs, and now two of their senior engineers have applied for roles in your team, both citing "chaos" in confidence. Your own portfolio depends on their service for one critical integration. Your director asks you informally: "Things look rough over there — what's your read?" What is the most effective response?

- A) Share your full read, including what the two applicants told you in confidence — the director needs the complete picture.
- B) Decline to comment on a peer's service — it is not your portfolio.
- C) Give the director your evidence-based operational read: the integration-level facts your own portfolio observes directly (incident correlation, dependency risk, your mitigations), and your offer of concrete peer support; hold back the applicants' confidential characterisations, and separately tell your peer directly what you see from the integration boundary and what help you can give.
- D) Use the moment: suggest the failing service's critical components migrate into your portfolio, where they would be better run.

**Correct answer: C**

**Explanation:** Partition what you hold: *directly observed operational evidence* (your integration's incident correlation, dependency exposure — legitimately yours to report, and the director is entitled to it), *confidential personal disclosures* (two applicants' characterisations, given in the context of recruitment — not yours to repurpose as intelligence), and *inference* (your overall "read" — offerable only as clearly-labelled inference). Option C reports the first, protects the second, labels the third, and adds the two moves that distinguish stewardship from spectating: concrete peer support offered, and — the harder one — direct honesty *with the peer* about what the integration boundary shows; principals who tell directors what they will not tell the colleague are conducting surveillance, not collaboration. Option A converts recruitment confidences into upward reporting — the immediate briefing gain costs you every future candidate's candour (word travels) and weaponises what vulnerable people told you while job-seeking; note that declining to share it is not concealment, because the operational facts you *do* share carry the substantive picture. Option B is false modesty with a real cost: your portfolio has genuine, direct evidence about a dependency risk — "not my portfolio" withholds decision-relevant information your director legitimately needs, and your **Service focus** bigger-picture duty runs exactly through such integration seams. Option D converts a colleague's crisis into an acquisition bid — even where consolidation might eventually be right, proposing it *in this conversation* poisons the motive assessment of every future restructuring argument you make. The scored behaviour is information stewardship under political temptation: report what you own, protect what you hold in trust, help before you judge, and say nothing upward you have not said across.

**Question 11 (hard) — The underperforming loyal lead**

One of your leads — twelve years in the organisation, deeply loyal, personally kind, and the person who kept operations alive through the pandemic years — is now clearly out of depth: their portfolio's problem backlog is growing, two strong engineers have quietly asked to transfer out of their team, and their last two governance papers needed rewriting by others. Development support over the past year (coaching, a reduced portfolio, paired working) has not changed the trajectory. Your reorganisation gives you a natural moment to act. What is the most effective response?

- A) Protect them — restructure around them quietly, routing critical work to other leads while they keep the title; loyalty like theirs has earned it.
- B) Have the honest conversation before the reorganisation lands: the trajectory, the evidence, and the year of support are named; the outcome is a move to a role matching their genuine strengths — with the move done respectfully, at their pace where possible, and with their contribution publicly honoured; the lead role is refilled on capability.
- C) Use the reorganisation to make their role redundant, avoiding the difficult conversation.
- D) Give the development plan one more year — the engineers can be retained with counter-offers, and the papers can keep being quietly rewritten.

**Correct answer: B**

**Explanation:** Total the true cost of each kindness. Option A's protection is paid by others: the engineers transferring out are your talent pipeline voting with their feet against a leadership vacuum; the colleagues rewriting papers are subsidising a title invisibly; and the lead themselves lives the daily corrosion of a role they can feel exceeding them — protected failure is not kind, it is slow and public. Option D is A with a clock attached and the evidence already in: the stem stipulates a *year* of genuine, well-designed support (coaching, scope reduction, pairing) that has not moved the trajectory — at some point continued "development" becomes a decision not to decide, and counter-offering engineers to stay under the same conditions rents their patience without addressing why it ran out. Option C is the cruellest option wearing procedure's clothes: redundancy-by-reorganisation avoids your discomfort by converting a capability conversation into a career termination, denying twelve loyal years even the respect of honesty. Option B is the leadership answer because it refuses the false choice between kindness and standards: the conversation is honest (trajectory, evidence, the support already given — no ambush, no euphemism), the outcome is a *match* rather than an exit (out-of-depth at lead level and genuinely valuable are compatible facts; the organisation almost certainly has a role their strengths fit), the execution protects dignity (pace, public honouring of real contribution — the pandemic years were real), and the lead role is refilled on the only criterion that is fair to everyone downstream of it: capability. Leading on resourcing means holding both truths at once — people are owed honesty and dignity; roles are owed capability — and the principals who can deliver both in the same conversation are the ones whose difficult decisions leave the culture stronger.

**Question 12 (hard) — The minister's deadline and the release you own**

A ministerial announcement in nine days commits your department to launching a new citizen-facing feature. The programme is late; the feature reached your operations acceptance gate yesterday with: performance testing complete only for half the projected launch traffic, two known defects (one with a workaround, one intermittent and undiagnosed), and no rehearsed rollback for the data migration component. The programme director, backed by the digital director, asks you to waive the acceptance gate: "It's nine days. The announcement is made. Make it work." What is the most effective response?

- A) Waive the gate — the announcement is a political fact, and operations must serve the department's commitments.
- B) Hold the gate absolutely: the criteria exist for exactly this pressure, and the launch moves when the criteria are met, announcement or no announcement.
- C) Re-scope the risk rather than waive the gate: propose a constrained launch that meets the announcement — feature live behind a controlled rollout (a capped percentage of traffic, within the tested envelope), the workaround-defect accepted with monitoring, launch contingent on two non-negotiables achievable in nine days (rehearsed rollback for the migration; diagnosis or containment of the intermittent defect) — with the residual risk written down, decided at director level with your explicit advice on the record, and a joint agreement on the full-traffic criteria.
- D) Escalate over both directors to the permanent secretary's office, warning that the launch endangers citizen data.

**Correct answer: C**

**Explanation:** Locate the real decision space first: the announcement is fixed (a political fact, as option A says), but "launch" is not one thing — traffic shape, rollout speed, and risk acceptance are all variables, and the principal's expertise is precisely knowing which variables move. Option C moves them: a capped rollout keeps launch-day traffic *inside the tested half* of the envelope, converting the performance unknown into a non-issue on day one; the workaround-defect is a normal, monitorable risk acceptance; and the two genuine red lines are chosen exactly (an unrehearsed data-migration rollback means an unrecoverable bad day — that is not schedule pressure, that is the difference between an incident and a catastrophe; an *undiagnosed* intermittent defect is a risk you cannot even size, so it needs diagnosis or containment before it rides to full scale). Both are achievable in nine days, which is what makes them demands rather than obstruction. The governance completes it: residual risk written down and *decided at director level with your advice on the record* — you are the accountable operations authority, and the record of "advised, decided above" is what accountability looks like when authority and expertise sit in different chairs. Option A waives the one gate that exists for this exact pressure and inherits every unknown at full traffic on announcement day. Option B mistakes rigidity for integrity: gates protect outcomes, not their own criteria, and a gate that cannot express risk in any currency except "wait" will simply be overridden — after which it protects nothing ever again. Option D detonates the escalation ladder while options remain: the permanent secretary is the move *after* a written risk advice is overridden on something unconscionable, not the reflex before negotiation — and "endangers citizen data" is, in option C's world, exactly what the rehearsed-rollback red line prevents, without the grenade. The final synthesis this guide can offer: principal-level judgement under pressure is neither yes nor no — it is the engineered *conditional yes*, with the conditions chosen by expertise, priced honestly, and decided at the level that owns the risk. That is your **Ownership and topic**, your **Change management**, your **Testing** risk-management, and your **User focus** — operating as one skill, which at your level they are.

### Preparation tips

- **Rehearse the conditional yes.** For any pressure scenario, practise constructing the bounded version: what caps, controls, red lines, and written risk decisions would make the demanded thing safe enough? The strongest principal answers are almost never yes or no.
- **Partition what you hold before you speak.** Direct evidence, confidences, inference — decide which is which before the director asks. Information stewardship failures happen in the moment; the sort must be pre-done.
- **Sequence inherited problems: risk, record, people.** Stabilise the live danger, correct the official record with a plan attached, address conduct through the right channel. Any other order converts stewardship into either panic or concealment.
- **Price kindness honestly.** In people scenarios, total who actually pays for each protective option — usually the protected person's colleagues, successors, and the protected person themselves. The respectful-honest option almost always wins the scoring.
- **Keep mechanisms cold and relationships warm.** Credits apply, gates hold, attestations are true — *and* the conversation is generous, the improvement plan welcomed, the counterpart respected. Practise doing both in the same response; that combination is the principal signature.
- **Discuss these scenarios with your leads.** Your judgement is also your legacy: an hour on two of these dilemmas with your leadership group develops them, calibrates you, and turns assessment preparation into the learning-and-development duty you already own.

### Common pitfalls to avoid

- **Serving the quarter at the decade's expense.** Waived credits, raided programmes, clean-but-false returns, buried research — every trap in this section trades a durable asset (precedent, margin, trust, truth) for a temporary comfort. Name the trade before choosing.
- **Heroics at the wrong altitude.** Taking tactical command, remote-controlling the renewal, rewriting the lead's paper yourself — principal-level value is created through systems and people; personal seizure is the seductive wrong answer at every level, and at yours it also stunts a successor.
- **Confusing rigidity with integrity.** Gates, contracts, and processes protect outcomes. The option that can only say "no" or "wait" — refusing all engagement, all negotiation, all bounded risk — scores nearly as poorly as capitulation.
- **Spending held-in-trust information.** Confidences from applicants, research you can reframe, records you can quietly amend — power over information is the principal's most audited asset. If you would not describe the use aloud to the person it concerns, it is a trap option.
- **Escalating past unexhausted options.** The permanent secretary, the CIO's office, the director's superior — top-of-ladder moves before evidence, negotiation, and direct conversation are spent read as political, not principled.
- **Letting loyalty and sunk virtue override evidence.** Twelve good years, a flagship reported complete, a supplier's partnership language — past merit is real and is not exculpatory. The scored discipline is gratitude expressed *alongside* the honest decision, never instead of it.

<!-- APPEND -->
