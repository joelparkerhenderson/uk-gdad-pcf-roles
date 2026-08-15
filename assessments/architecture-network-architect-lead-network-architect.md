# Network Architect (Lead Network Architect) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, self-contained preparation resource for psychometric assessments, written specifically for you as a lead network architect working within the UK Government Digital and Data profession. Whether you are preparing for an internal progression board, a move to another department, a formal capability review, or you simply want to sharpen the mental skills your role demands every day, this guide is designed to help you practise with confidence.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and make decisions. They are widely used across the Civil Service and the wider public sector because they are objective: they compare your performance against a consistent benchmark rather than relying on impressions formed in an interview. For a role as senior as yours, they are rarely about raw speed alone. Assessors want evidence that you can absorb complex technical and organisational information, identify the signal within the noise, weigh competing priorities, and exercise sound judgement under pressure — precisely the capabilities you draw on when you act as a point of escalation, contribute to governance forums that determine IT strategy, and represent network architects internally and externally.

This document is organised into four assessment areas, each aligned to a recognised psychometric format:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, and prioritisation using artefacts you genuinely handle: network designs, firewall rule sets, change schedules, and escalation queues.
2. **Workplace job-specific numeric reasoning assessment** — interpreting bandwidth figures, capacity plans, budgets, availability targets, and procurement comparisons.
3. **Workplace job-specific verbal reasoning assessment** — extracting precise meaning from standards documents, governance papers, policy extracts, and stakeholder correspondence.
4. **Workplace job-specific situational judgement assessment** — realistic dilemmas involving the stakeholders you work with: architects you mentor, design authorities, suppliers, service teams, and senior non-technical leaders.

Each section explains what the assessment measures, maps it to the skills in your role profile — governance and assurance, IT infrastructure, systems design, systems integration, and troubleshooting and problem resolution — then gives you a substantial set of practice questions with worked answers, followed by preparation tips and common pitfalls.

How should you use it? Three ways work well. First, as practice: attempt the questions under light time pressure before reading the explanations. Second, as self-reflection: notice which question types feel effortful, because that tells you where to focus. Third, as preparation: re-read the tips shortly before any real assessment. Work through it at your own pace, and treat every mistake as useful information rather than a setback. You already use these reasoning skills daily; this guide simply helps you demonstrate them deliberately.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment is a targeted psychometric test that measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. Unlike a generic IQ test, every question is built from the artefacts and situations a lead network architect actually encounters: network topology diagrams, VLAN allocation tables, firewall rule sets, change advisory board schedules, and escalation queues. The format is usually online and timed, typically 15 to 30 minutes, with objective scoring against a benchmark norm group. Questions are validated so that they predict genuine job performance without bias, and reports often show your speed and accuracy separately rather than collapsing everything into a single score.

For you, this assessment matters because your role sits at the point where technical complexity meets organisational consequence. You are accountable for designs and networks representing your business area, you are a point of escalation when others are stuck, and you champion new technologies and solutions. Each of those responsibilities depends on fast, accurate reasoning: spotting the inconsistency in a design pack before it reaches a design authority, deducing the root cause from a partial set of symptoms, and deciding which of five competing demands genuinely needs your attention first. A cognitive assessment simply makes those everyday capabilities visible and measurable.

Expect a mixture of question styles: pattern recognition across sequences of configurations or events, logical deduction from a set of stated constraints, error checking between two versions of a technical document, prioritisation of tasks against criteria, and structured problem solving. At lead level, assessors will calibrate difficulty upwards: scenarios involve more variables, more ambiguity, and more organisational context than at practitioner level.

### What it measures for your role

Mapping the assessment dimensions to the skills named in your role profile:

- **Troubleshooting and problem resolution.** Your profile requires you to break a problem down into its component parts to identify and diagnose root causes, and to troubleshoot across different technology capabilities. Logical deduction and fault-isolation questions test exactly this: given symptoms across LAN, WAN, wifi, and cloud networks, can you eliminate impossible causes and converge on the true one?
- **Systems design.** You design systems characterised by high levels of risk, impact, and business or technical complexity, and you control system design practice within an enterprise architecture. Pattern recognition and consistency-checking questions mirror the design assurance work of spotting where a proposed design breaks an established pattern or standard.
- **Systems integration.** You define the integration build and co-ordinate build activities across systems. Sequencing and dependency questions — deciding the valid order of build steps under stated constraints — draw directly on this skill.
- **Governance and assurance.** You ensure appropriate and proportionate governance is in place and guide teams through assurance processes such as service assessments. Error-checking questions using governance artefacts (risk registers, decision logs, assessment criteria) test the meticulous attention that assurance work demands.
- **IT infrastructure.** You lead teams in the design, implementation, administration and support of infrastructure solutions. Prioritisation questions reflect the daily reality of ordering escalations, changes, and coaching commitments across an infrastructure portfolio.

### Practice questions

**Question 1 (easy) — Pattern recognition in VLAN allocation**

Your team allocates VLANs to new sites using a consistent scheme. The last four sites were allocated as follows:

- Site A: management VLAN 110, voice VLAN 210, data VLAN 310, guest VLAN 410
- Site B: management VLAN 120, voice VLAN 220, data VLAN 320, guest VLAN 420
- Site C: management VLAN 130, voice VLAN 230, data VLAN 330, guest VLAN 430
- Site D: management VLAN 140, voice VLAN 240, data VLAN 340, guest VLAN 440

A junior architect proposes for Site E: management VLAN 150, voice VLAN 250, data VLAN 340, guest VLAN 450. Which allocation breaks the pattern?

A) Management VLAN 150
B) Voice VLAN 250
C) Data VLAN 340
D) Guest VLAN 450

**Correct answer: C.**

**Explanation:** Each VLAN category increments by 10 per site: management runs 110, 120, 130, 140, so Site E should be 150 (correct); voice should be 250 (correct); data should be 350, but 340 has been proposed — and worse, 340 is already assigned to Site D, creating a duplicate allocation; guest should be 450 (correct). This is the kind of quiet inconsistency that, unspotted at design review, becomes an integration defect later. In an assessment, verify each element against the rule rather than skimming for what "looks right".

**Question 2 (easy) — Logical deduction from monitoring alerts**

At 09:14 your network management solution raises three alerts: (1) all wifi access points at the Leeds office show unreachable; (2) the Leeds core switch shows reachable and healthy; (3) users in Leeds report wired desktops working normally. The access points connect to two dedicated PoE access switches, which uplink to the core switch. What is the most logical first hypothesis?

A) A WAN circuit failure between Leeds and the data centre
B) A fault affecting the PoE access switches or their uplinks
C) A wireless controller licence expiry affecting all sites
D) A power failure across the whole Leeds office

**Correct answer: B.**

**Explanation:** Deduce by elimination. A WAN failure (A) would make the core switch unreachable from the monitoring platform, but it reports healthy. A whole-office power failure (D) would take down the wired desktops too, yet they work. A controller licence expiry (C) would typically affect access points at all sites, not just Leeds — and nothing in the evidence mentions other sites being affected. The common element unique to the failed devices is the pair of PoE access switches they connect through, so B is the hypothesis that best fits every observation. This mirrors your role's requirement to break a problem into component parts and isolate the root cause.

**Question 3 (moderate) — Error checking a firewall change request**

A change request submitted to you for approval states:

*"Permit TCP 443 from subnet 10.20.4.0/24 (Finance user VLAN) to 10.60.8.15 (new HR SaaS proxy). Business justification: HR self-service rollout. Rollback: remove rule. Duration: permanent. Firewall: DC-EDGE-01. Requested rule position: above the final deny-all."*

The accompanying design document states the HR proxy address is 10.60.8.51, the source should be all user VLANs (10.20.0.0/16), and the rule should be reviewed after 12 months. How many discrepancies exist between the change request and the design document?

A) One
B) Two
C) Three
D) Four

**Correct answer: C.**

**Explanation:** Compare systematically, field by field. Destination address: change says 10.60.8.15, design says 10.60.8.51 — a transposed-digit discrepancy (one). Source scope: change says 10.20.4.0/24 only, design says 10.20.0.0/16 — a scope discrepancy (two). Duration: change says permanent, design says review after 12 months (three). Protocol and port (TCP 443) match, and rule position is not contradicted by the design document. So three discrepancies. Transposition errors such as .15 versus .51 are exactly what error-checking questions test, because they are what real change reviews must catch before a mis-punched rule exposes the wrong server.

**Question 4 (moderate) — Prioritisation of an escalation queue**

It is Monday 08:45. As the point of escalation, you have five items waiting:

1. A P2 incident: intermittent packet loss on the WAN link serving a contact centre that opens at 09:00, with a workaround (failover to secondary circuit) not yet invoked.
2. A design authority paper due Thursday, needing your comments by Wednesday.
3. An associate network architect asking for 30 minutes of coaching on a routing design, no deadline given.
4. A supplier meeting invitation for 10:00 today about a telephony contract renewal that expires in six months.
5. A security team query about a remote access design, flagged "respond within 5 working days", received Friday.

Which is the most defensible order to address them this morning?

A) 1, 4, 3, 5, 2
B) 1, 4, 5, 3, 2
C) 4, 1, 2, 5, 3
D) 1, 2, 4, 5, 3

**Correct answer: A.**

**Explanation:** Item 1 is urgent and important: a citizen-facing contact centre opens in 15 minutes and a known workaround has not been invoked — directing the failover (or delegating it with clear instructions) comes first. Item 4 is fixed in time (10:00 today), so it must be handled next regardless of its lower strategic urgency; you attend or delegate before it occurs. Item 3, the coaching request, is short, unblocks a colleague's work, and reflects your accountability for developing network architects — reasonable to fit in during the morning. Item 5 has a five-day clock with days remaining, so it follows. Item 2 is important but its effective deadline is Wednesday, making it the item most safely scheduled later. Option B undervalues coaching, which at lead level is core work rather than a favour; C lets a scheduled meeting displace an active incident; D brings forward work with the most slack. Assessors look for reasoning that balances urgency, fixed time constraints, and role responsibilities — not just "incidents first, paperwork last".

**Question 5 (moderate) — Sequencing an integration build**

You are defining the integration build for a new data centre LAN pod. The constraints are:

- The out-of-band management network must exist before any production switch is configured.
- Core switches must be configured before distribution switches.
- Distribution switches must be configured before access switches.
- Integration testing of routing cannot start until core and distribution are complete.
- The firewall pair must be integrated after the core but before routing integration testing, because test traffic must traverse it.

Which sequence is valid?

A) Management network → core → access → distribution → firewalls → routing testing
B) Core → management network → distribution → firewalls → routing testing → access
C) Management network → core → distribution → firewalls → routing testing → access
D) Management network → core → firewalls → routing testing → distribution → access

**Correct answer: C.**

**Explanation:** Walk each option against the constraints. A configures access before distribution, violating the distribution-before-access rule. B configures the core before the management network exists, violating the first rule. D runs routing integration testing before distribution is complete, violating the testing prerequisite. C satisfies every constraint: management first; core before distribution; firewalls after core and before testing; testing after core and distribution; access last (nothing requires access before testing). Note that a valid sequence need not be the only sensible one — the question asks which sequence breaches no constraint. This mirrors defining the integration build and co-ordinating build activities across systems: the discipline is checking dependencies exhaustively, not assuming the familiar order.

**Question 6 (moderate) — Pattern recognition in incident timing**

Reviewing three months of problem records, you notice wifi authentication failures at the Bristol office occurred on: 6 January (Tuesday), 20 January (Tuesday), 3 February (Tuesday), 17 February (Tuesday), and 3 March (Tuesday). Each incident began at approximately 02:10 and self-resolved by 02:40. Which line of investigation does the pattern most strongly support?

A) User error during morning login peaks
B) A scheduled fortnightly overnight process, such as a certificate service restart or maintenance job
C) Random hardware degradation on access points
D) A cyber attack timed to business hours

**Correct answer: B.**

**Explanation:** The intervals are exactly 14 days, always the same weekday, always the same 30-minute overnight window. Random hardware faults (C) do not respect calendars. Morning login peaks (A) and business-hours attacks (D) contradict the 02:10 timing. A fortnightly scheduled task — for example, a maintenance window, certificate revocation list refresh, or RADIUS-dependent service restart — fits period, day, and time precisely. Recognising periodicity in noisy operational data is a core diagnostic pattern skill: the strength of a hypothesis is how much of the evidence it explains, and B explains all of it.

**Question 7 (moderate) — Logical deduction with governance constraints**

Your governance forum operates these rules: (1) any design touching citizen data requires a security architecture review; (2) any design costing over £500,000 requires investment board approval; (3) designs requiring both reviews must go to security architecture first; (4) SD-WAN designs additionally require design authority endorsement, which must come last.

You receive an SD-WAN design costing £650,000 that carries citizen data. Which is the correct governance path?

A) Investment board → security architecture review → design authority endorsement
B) Security architecture review → investment board → design authority endorsement
C) Design authority endorsement → security architecture review → investment board
D) Security architecture review → design authority endorsement → investment board

**Correct answer: B.**

**Explanation:** The design triggers all three gates: citizen data → security review (rule 1); £650,000 > £500,000 → investment board (rule 2); SD-WAN → design authority endorsement (rule 4). Rule 3 forces security review before investment board. Rule 4 forces endorsement last. The only ordering satisfying both is security review, then investment board, then endorsement — option B. Options A and D break rule 3 or rule 4's "last" requirement; C puts endorsement first. Applying rule sets mechanically and completely, without letting familiarity suggest shortcuts, is exactly the discipline you use when guiding teams through governance and assurance processes.

**Question 8 (hard) — Fault isolation across technology capabilities**

Users of a hybrid cloud service report intermittent application timeouts. You gather the following facts: (1) on-premises users connecting via the data centre LAN experience timeouts; (2) remote users connecting via the remote access VPN experience identical timeouts; (3) users of a second application hosted in the same cloud virtual network experience no problems; (4) the cloud provider's status page shows no incidents; (5) packet captures show TCP retransmissions only on flows to the affected application's load balancer address.

Which component is the strongest candidate for root cause?

A) The corporate WAN
B) The remote access VPN concentrator
C) The affected application's load balancer or its immediate network path
D) The data centre LAN

**Correct answer: C.**

**Explanation:** Use the intersection method: the fault must lie on the path common to everyone affected and absent from paths of those unaffected. On-premises and VPN users take different paths through the WAN, LAN, and VPN concentrator, yet both see the fault — so components unique to one population (B, D, and largely A) are weak candidates. The second application shares the same cloud virtual network but is unaffected, which pushes suspicion past the shared cloud fabric down to something specific to the affected application: its load balancer or the path immediately around it. Fact 5 corroborates this — retransmissions appear only on flows to that load balancer address. This is the layered elimination you practise when troubleshooting across LAN, WAN, remote access, and cloud capabilities: identify what all failing paths share that all healthy paths avoid.

**Question 9 (hard) — Deduction from standards constraints**

Your organisation's network standards state: (1) every branch site must have two independent WAN transports; (2) sites classified "critical" must have transports from two different suppliers; (3) 4G/5G wireless may serve as the second transport only at sites classified "standard"; (4) any site hosting telephony gateways is automatically classified "critical".

A proposed design for a new site includes one fibre circuit from Supplier X, one 4G service from Supplier Y, and an on-site telephony gateway. How many standards does the design breach?

A) None
B) One
C) Two
D) Three

**Correct answer: B.**

**Explanation:** Apply the rules in order. Rule 4: the telephony gateway makes the site "critical". Rule 1: two independent transports exist (fibre plus 4G) — satisfied. Rule 2: the transports come from Supplier X and Supplier Y — two different suppliers, satisfied. Rule 3: 4G may be the second transport only at "standard" sites, but this site is critical — breached. So exactly one breach. The trap is double-counting: once you realise the site is critical, it is tempting to see both a supplier problem and a 4G problem, but the supplier diversity rule is genuinely met. Careful, rule-by-rule evaluation prevents both under-counting and over-counting — the same discipline you apply when ensuring adherence to technical strategies, policies, and standards.

**Question 10 (hard) — Prioritisation under strategic ambiguity**

Your director asks you to reduce your team's commitments because two architects have left. You currently support: (1) an SD-WAN rollout at 60% completion with contractual milestones; (2) a discovery project exploring wifi 7 for a single office refurbishment; (3) mandatory input to a cross-government secure connectivity standard, where you are the department's sole representative; (4) monthly coaching sessions for four associate architects; (5) a proof of concept for network automation tooling you personally championed.

Applying the principle of protecting contractual obligations, statutory or cross-government duties, and people development, which commitment is the strongest candidate to pause?

A) The SD-WAN rollout
B) The wifi 7 discovery project
C) The cross-government standard input
D) The coaching sessions

**Correct answer: B.**

**Explanation:** The SD-WAN rollout (A) carries contractual milestones; pausing it creates supplier and financial exposure. The cross-government input (C) is a duty where you are the sole departmental voice — pausing it removes your organisation from decisions that will bind it later. Coaching (D) is explicitly part of your role's accountabilities and is how the team recovers capacity in the medium term; cutting development to solve a capacity problem deepens the problem. The wifi 7 discovery (B) is exploratory, tied to a single office, and can restart later with little lost value — it fails no contractual, cross-government, or development test. Note that the automation proof of concept (5) is also a candidate, but the question asks for the strongest among the options offered, and personal sponsorship of an initiative is not a reason to protect it — assessors sometimes include your own pet project precisely to test that. Recognise, though, that option 5's absence from the answer list is deliberate: read the options offered, not the scenario alone.

**Question 11 (moderate) — Error checking a design document table**

A high-level design lists four data centre interconnect links:

| Link | A-end | B-end | Bandwidth | Latency budget |
|------|-------|-------|-----------|----------------|
| DCI-1 | London DC | Manchester DC | 100 Gbps | 5 ms |
| DCI-2 | Manchester DC | London DC | 100 Gbps | 5 ms |
| DCI-3 | London DC | Cardiff DC | 40 Gbps | 4 ms |
| DCI-4 | Cardiff DC | Manchester DC | 40 Gbps | 4 ms |

The accompanying text states: "All interconnects are diverse pairs; each city pair is served by two links; total interconnect capacity is 280 Gbps; the longest latency budget on any link is 5 ms." Which claim in the text is inconsistent with the table?

A) Each city pair is served by two links
B) Total interconnect capacity is 280 Gbps
C) The longest latency budget is 5 ms
D) All the claims are consistent

**Correct answer: A.**

**Explanation:** Check each claim. Capacity: 100 + 100 + 40 + 40 = 280 Gbps — consistent. Longest latency budget: the maximum in the table is 5 ms — consistent. City pairs: London–Manchester has two links (DCI-1, DCI-2), but London–Cardiff has only one (DCI-3) and Cardiff–Manchester only one (DCI-4). So the claim that each city pair is served by two links is false. The plausible-sounding aggregate figures are correct precisely to lure you into skipping the structural check. When assuring designs for high-risk systems, verify the claims that carry resilience implications, not just the ones that are easy to add up.

**Question 12 (hard) — Problem solving with competing constraints**

You must schedule three disruptive changes in one maintenance window (22:00–04:00, six hours): a core switch software upgrade (2 hours, must complete before any routing changes), a routing protocol migration (3 hours, cannot overlap the firewall work because both teams share the same senior engineer), and a firewall cluster upgrade (2 hours, must finish by 03:00 to allow a payment file transfer at 03:15 to be tested). Can all three fit, and if so which start order works?

A) They cannot all fit in the window
B) Core upgrade 22:00–00:00; firewall 22:00–00:00 in parallel; routing 00:00–03:00
C) Firewall 22:00–00:00; core 22:00–00:00 in parallel; routing 00:30–03:30
D) Core upgrade 22:00–00:00; routing 00:00–03:00; firewall 03:00–05:00

**Correct answer: B.**

**Explanation:** Test each option against the three constraints: core before routing; routing and firewall must not overlap (shared engineer); firewall finished by 03:00. Nothing forbids the core upgrade and the firewall running in parallel — they involve different teams and no stated dependency. Option B: core 22:00–00:00 and firewall 22:00–00:00 in parallel (allowed); firewall finishes at 00:00, comfortably before 03:00; routing 00:00–03:00 starts after the core completes and never overlaps the firewall work. All constraints are met, with the window closing an hour after the last task ends. Option D breaches two constraints at once: the firewall runs 03:00–05:00, missing the 03:00 payment-transfer deadline and overrunning the 04:00 window. Option A is disproved by B's existence. Option C is the deliberate near-miss: it also parallelises core and firewall and breaches no hard constraint on overlap, but routing at 00:30–03:30 leaves an unexplained 30-minute gap after the core finishes and ends only 30 minutes inside the window, so between two feasible schedules the assessment credits the one that completes earliest and preserves the most contingency — B. The lesson: when two options look feasible, classify every option's status explicitly rather than stopping at the first schedule that works, then apply the tiebreaker the scenario implies (here, maximum contingency inside a fixed window).

**Question 13 (hard) — Recognising a flawed inference in a strategy paper**

A draft paper to your governance forum argues: "Departments that adopted SD-WAN reported 30% lower circuit costs. Our circuit costs are rising. Therefore adopting SD-WAN will cut our circuit costs by 30%." As the subject matter expert, which is the strongest logical criticism?

A) SD-WAN is an outdated technology
B) The paper assumes results transfer directly, ignoring differences in estate, contracts, and baseline costs between departments
C) Circuit costs are irrelevant to SD-WAN decisions
D) The paper should quote a higher figure to strengthen the business case

**Correct answer: B.**

**Explanation:** The argument generalises from other departments' outcomes to a precise prediction for yours without establishing comparability: their savings depended on their starting contracts, site counts, traffic profiles, and negotiating positions. That is the classic flaw of treating a correlational, self-reported figure as a guaranteed causal effect in a different context. Option A is an opinion, not a logical criticism, and is not supported. Option C is false — circuit economics are central to SD-WAN cases. Option D invites fabrication, the opposite of assurance. Spotting unsupported inferential leaps is central to your governance role: you are the person the forum trusts to separate evidence from advocacy before strategy is set.

### Preparation tips

- **Practise with your own artefacts.** Take a recent design pack, change request, or problem record and interrogate it: what rule does each element follow, what would an inconsistency look like, what does each symptom eliminate? You will build the exact muscles the assessment measures.
- **Verbalise your elimination logic.** For deduction questions, consciously state why each wrong option fails. Under time pressure, structured elimination is faster and more reliable than intuition, and it is how you already reason through escalations.
- **Time-box ruthlessly.** With 15 to 30 minutes for the whole test, no single question deserves more than about 90 seconds. Flag and move on — an unanswered easy question costs the same as an unanswered hard one.
- **Do the checking pass in a fixed order.** For error-checking items, compare field by field in the same sequence every time (source, destination, value, duration, position). A fixed routine catches transpositions that free-form scanning misses.
- **Rest and rehearse the interface.** Most platforms provide ungraded practice questions before the timed section; always take them, and sit the assessment fresh rather than at the end of a heavy day. At your level the differentiator is sustained accuracy, not bursts of speed.

### Common pitfalls

- **Skimming for the familiar.** Lead architects have seen hundreds of designs, and pattern familiarity tempts you to assume rather than verify. The Site D/Site E duplicate VLAN in Question 1 is caught only by checking, not by recognising.
- **Stopping at the first plausible answer.** As Question 12 showed, assessments include near-miss distractors. Confirm the other options fail before committing.
- **Letting seniority bias prioritisation.** Coaching and governance duties are core lead-level work; treating them as automatically deferrable is a scoring error as well as a leadership one.
- **Over-engineering simple items.** Some questions really are easy. Spending three minutes suspecting a trick in a straightforward sequence question is a time sink — a pitfall the test designers explicitly anticipate.
- **Ignoring the stated constraints in favour of real-world knowledge.** Answer from the rules given in the question, even where your operational experience suggests exceptions; the assessment measures reasoning from stated premises.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data of the kind your role genuinely produces: bandwidth and capacity figures, availability percentages, circuit and cloud cost tables, budget breakdowns, and performance dashboards. It is business mathematics rather than abstract formulae — percentages, ratios, unit conversions, and cost-benefit estimations applied to realistic tables and charts. Most versions are calculator-friendly, because they prioritise interpretation over mental arithmetic, but they impose strict time limits, so quick and accurate data extraction matters as much as computation.

For a lead network architect this assessment carries particular weight. You develop implementation and procurement strategies consistent with business needs, which means comparing supplier quotes, whole-life costs, and capacity headroom with rigour. You are accountable for networks representing your business area, so you must read utilisation trends and availability statistics accurately enough to defend investment decisions at governance forums. And because you communicate network concepts to non-technical stakeholders, you must translate raw figures into defensible conclusions — a skill the assessment tests every time it asks "which option is cheapest per unit?" rather than "what is the total?".

Typical formats present a table or chart followed by three to five multiple-choice questions, with under a minute to ninety seconds per question. Expect data with distractors built in: mixed units (Mbps and Gbps), figures quoted "per month" versus "per annum", and totals that reward estimation before precise calculation.

### What it measures for your role

- **Systems design.** Designing systems with high levels of risk and complexity requires sizing them: converting user counts into bandwidth demand, applying growth rates, and checking that designs stay within capacity limits. Percentage-growth and capacity-headroom questions test exactly this.
- **Systems design (procurement strand) and IT infrastructure.** Developing effective implementation and procurement strategies means whole-life cost comparison: installation charges, monthly rentals, contract terms, and exit costs. Cost-per-unit and total-cost-of-ownership questions mirror the analysis you perform before recommending a supplier.
- **Governance and assurance.** Assurance work is quantitative more often than people expect: availability targets, error budgets, service assessment metrics, and risk exposure figures. Questions on availability percentages and downtime minutes reflect the numbers you check when assuring that standards are met.
- **Systems integration.** Co-ordinating build activities across systems involves schedule and throughput arithmetic — migration rates, parallel workstreams, and completion projections.
- **Troubleshooting and problem resolution.** Diagnosing capacity-related problems means reading utilisation data correctly: peak versus average, percentiles versus means, and trend extrapolation.

### Practice questions

**Question 1 (easy) — Percentage utilisation**

A 10 Gbps data centre LAN uplink shows a peak throughput of 6.8 Gbps in the monthly report. Your standard requires upgrade planning to begin when peak utilisation exceeds 70%. Has the threshold been crossed, and what is the peak utilisation percentage?

A) No — 62%
B) No — 68%
C) Yes — 68%
D) Yes — 71%

**Correct answer: B.**

**Explanation:** Utilisation = peak throughput ÷ capacity × 100 = 6.8 ÷ 10 × 100 = 68%. The threshold is "exceeds 70%", and 68% does not exceed 70%, so upgrade planning is not yet triggered. The distractor C offers the right arithmetic with the wrong conclusion — always read the decision rule as carefully as the numbers. A one-step percentage like this is deliberately easy; bank it quickly and move on.

**Question 2 (easy) — Downtime from an availability target**

Your WAN service has a contractual availability target of 99.9% measured monthly. Taking a 30-day month (43,200 minutes), what is the maximum downtime permitted before the supplier breaches the target?

A) 4.32 minutes
B) 43.2 minutes
C) 432 minutes
D) 4,320 minutes

**Correct answer: B.**

**Explanation:** Permitted downtime = (100% − 99.9%) × total minutes = 0.1% × 43,200 = 0.001 × 43,200 = 43.2 minutes. A common error is slipping a decimal place: 0.1% is one part in a thousand, not one in a hundred. As the person who holds suppliers to account at escalation, you will recognise this as the arithmetic behind every service credit conversation — 99.9% sounds generous until you see it is under three-quarters of an hour a month.

**Question 3 (moderate) — Comparing circuit costs per Mbps**

You are evaluating three WAN circuit options for a large site:

| Option | Bandwidth | Installation (one-off) | Monthly rental |
|--------|-----------|------------------------|----------------|
| Fibre A | 1 Gbps | £2,400 | £850 |
| Fibre B | 500 Mbps | £0 | £520 |
| Fibre C | 2 Gbps | £6,000 | £1,400 |

Over a 36-month contract, which option has the lowest total cost per Mbps of bandwidth?

A) Fibre A
B) Fibre B
C) Fibre C
D) They are equal

**Correct answer: C.**

**Explanation:** Compute 36-month totals first. Fibre A: £2,400 + 36 × £850 = £2,400 + £30,600 = £33,000 for 1,000 Mbps = £33.00 per Mbps. Fibre B: 36 × £520 = £18,720 for 500 Mbps = £37.44 per Mbps. Fibre C: £6,000 + 36 × £1,400 = £6,000 + £50,400 = £56,400 for 2,000 Mbps = £28.20 per Mbps. Fibre C is the lowest per Mbps despite the highest headline cost. This is the procurement-strategy trap in miniature: cheapest total and cheapest per unit are different questions, and the assessment (like a real business case) will tell you which one it is asking. Note the unit discipline too — Fibre B is quoted in Mbps while A and C are in Gbps.

**Question 4 (moderate) — Budget variance**

Your network architecture programme has an annual budget of £3.2 million. At the end of quarter three you have spent £2.56 million. Spending is assumed to be even across quarters. What is the projected full-year variance against budget?

A) £160,000 overspend
B) £213,333 overspend
C) £160,000 underspend
D) On budget exactly

**Correct answer: B.**

**Explanation:** Quarterly run rate = £2.56m ÷ 3 = £853,333 per quarter. Projected full year = £853,333 × 4 = £3,413,333 (equivalently, £2.56m × 4 ÷ 3 = £10.24m ÷ 3). Variance = £3,413,333 − £3,200,000 = £213,333 overspend. The £160,000 distractors come from a different, tempting method: comparing spend to date against the three-quarter budget (¾ × £3.2m = £2.4m) gives £2.56m − £2.4m = £160,000 — but that is the year-to-date variance, not the projected full-year variance the question asked for. Read which variance is requested before choosing a method; in programme reporting these two figures answer different governance questions, and mixing them up in a real forum undermines the credibility of an otherwise sound investment case.

**Question 5 (moderate) — Wifi capacity planning**

An office refurbishment will house 720 staff. Your wifi design standard assumes 60% of staff are present at peak, each present person uses an average of 2.5 devices, and each access point should serve no more than 45 concurrent devices. How many access points does the standard require?

A) 20
B) 24
C) 27
D) 40

**Correct answer: B.**

**Explanation:** Peak occupancy = 720 × 0.60 = 432 people. Concurrent devices = 432 × 2.5 = 1,080. Access points = 1,080 ÷ 45 = 24. Because 24 is exact, no rounding is needed; had the division produced a fraction, you would round up (you cannot deploy part of an access point, and rounding down would breach the standard). Multi-step chains like this reward writing intermediate results down: each step is trivial, but under time pressure candidates who calculate in their heads tend to drop a factor — usually the 2.5 devices per person.

**Question 6 (moderate) — Cloud network egress costs**

A service in your business area transfers data out of its cloud region as follows: 18 TB per month to the internet at £0.07 per GB, and 6 TB per month over a private interconnect at £0.02 per GB. A proposed redesign routes 12 of the 18 internet terabytes over the interconnect instead. Using 1 TB = 1,000 GB, what is the monthly saving?

A) £600
B) £840
C) £1,260
D) £1,440

**Correct answer: A.**

**Explanation:** Only the redirected 12 TB changes cost. Current cost of that 12 TB via internet = 12,000 GB × £0.07 = £840. New cost via interconnect = 12,000 GB × £0.02 = £240. Saving = £840 − £240 = £600. Distractor B is the old cost of the moved traffic (forgetting the new path still costs money); D applies the saving rate of £0.05 to all 24 TB rather than the 12 TB that moves. Isolate what actually changes — the same discipline as costing a migration option in a cloud network design.

**Question 7 (moderate) — Ratio reasoning in team capacity**

Your team of 12 network architects divides its time between project design work, assurance reviews, and operational escalations in the ratio 7:3:2. The organisation mandates that assurance effort must rise to 25% of total capacity without reducing the absolute effort on escalations. If total team capacity stays fixed at 12 full-time equivalents (FTE), how many FTE will remain for project design work?

A) 6.0
B) 6.5
C) 7.0
D) 7.5

**Correct answer: C.**

**Explanation:** Current split: ratio parts total 7 + 3 + 2 = 12, conveniently matching 12 FTE, so design = 7 FTE, assurance = 3 FTE, escalations = 2 FTE. New requirement: assurance = 25% × 12 = 3 FTE... careful — 25% of 12 is 3, which equals the current assurance effort. Re-read: current assurance is 3 of 12 FTE = 25% already. So nothing needs to change and design keeps 7 FTE. The question tests whether you convert a ratio to percentages before reacting: 3:12 is already 25%. Candidates who skip that check subtract capacity from design unnecessarily — exactly the error that, in real resource planning, quietly starves project work in response to a mandate the team already meets.

**Question 8 (hard) — Migration throughput projection**

Your team is migrating 480 branch sites from legacy WAN circuits to SD-WAN. In the first 8 weeks, 96 sites were completed. A supplier constraint then reduces the migration rate by 25% for the remainder of the programme. How many further weeks will the remaining sites take?

A) 32 weeks
B) 36 weeks
C) 40 weeks
D) 42.7 weeks

**Correct answer: D.**

**Explanation:** Initial rate = 96 sites ÷ 8 weeks = 12 sites per week. Reduced rate = 12 × 0.75 = 9 sites per week. Remaining sites = 480 − 96 = 384. Time = 384 ÷ 9 = 42.67 weeks, which matches option D (42.7 weeks). In practice you would report "43 weeks" to a programme board, but numeric reasoning tests usually expect the calculated value as presented in the options; only round when the question asks for whole units (as with access points in Question 5). Distractor A comes from forgetting the rate reduction (384 ÷ 12 = 32); B from applying the 25% cut to the time rather than deriving the new rate correctly.

**Question 9 (hard) — Weighted availability across a path**

A citizen-facing service depends on a chain of three independently failing components: the data centre LAN (availability 99.95%), the WAN (99.9%), and the cloud interconnect (99.8%). To one decimal place of a percent, what is the approximate end-to-end availability of the chain, and does it meet the service's 99.7% target?

A) 99.9% — meets the target
B) 99.7% — meets the target
C) 99.65% — misses the target
D) 99.5% — misses the target

**Correct answer: C.**

**Explanation:** For components in series, multiply availabilities: 0.9995 × 0.999 × 0.998. Step one: 0.9995 × 0.999 = 0.9985 (to four decimal places). Step two: 0.9985 × 0.998 = 0.99650. End-to-end availability ≈ 99.65%, which is below the 99.7% target, so the chain misses it. A quicker approximation for high availabilities is to add the unavailabilities: 0.05% + 0.1% + 0.2% = 0.35% unavailable, giving 99.65% — the same answer with far less arithmetic, and a technique worth mastering for timed tests. The design implication is one you will recognise from systems design at high levels of risk: individually respectable components can jointly breach a target, which is why end-to-end analysis belongs in every design pack you assure.

**Question 10 (hard) — Procurement option with growth**

A five-year telephony contract offers two pricing models for your 4,000 users. Model A: flat £6.50 per user per month for all five years. Model B: £5.00 per user per month for years one and two, then £8.00 per user per month for years three to five. User numbers are expected to stay constant. Which model is cheaper over five years, and by how much?

A) Model A, by £216,000
B) Model A, by £72,000
C) Model B, by £72,000
D) They cost the same

**Correct answer: B.**

**Explanation:** Work per user across the full term, then scale. Model A: £6.50 × 60 months = £390 per user. Model B: £5.00 × 24 months + £8.00 × 36 months = £120 + £288 = £408 per user. Difference = £408 − £390 = £18 per user in Model A's favour, so total = £18 × 4,000 users = £72,000, and Model A is cheaper — option B. Distractor C has the right magnitude but the wrong direction: candidates who subtract £390 − £408 and lose track of the sign conclude Model B wins, so always restate the conclusion in words ("A is cheaper") before answering. Distractor A comes from comparing only the expensive years: (£8.00 − £6.50) × 36 months × 4,000 users = £216,000, ignoring Model B's two discounted years — the mirror image of a supplier's own selective framing. Whole-life comparison across every period of a variable-price contract is precisely the analysis your procurement strategies must survive at an investment board.

**Question 11 (moderate) — Reading a performance dashboard**

Your network management solution reports the following monthly figures for four regional WANs:

| Region | Circuits | Incidents | Mean time to repair (hours) | Availability |
|--------|----------|-----------|------------------------------|--------------|
| North | 120 | 18 | 4.0 | 99.92% |
| South | 200 | 24 | 3.5 | 99.95% |
| East | 80 | 16 | 6.0 | 99.88% |
| West | 100 | 12 | 5.0 | 99.93% |

Which region has the highest incident rate per circuit?

A) North
B) South
C) East
D) West

**Correct answer: C.**

**Explanation:** Incident rate per circuit: North = 18 ÷ 120 = 0.15; South = 24 ÷ 200 = 0.12; East = 16 ÷ 80 = 0.20; West = 12 ÷ 100 = 0.12. East is highest at 0.20 incidents per circuit despite having the fewest incidents in absolute terms — the classic normalisation point. South has the most incidents (24) but the largest estate, so its rate is joint lowest. When you present regional comparisons to a governance forum, normalised rates are what make the comparison fair; the assessment checks that you reach for the ratio, not the raw count. Note that mean time to repair and availability are decoy columns here — extracting only the data the question needs is itself a timed-test skill.

**Question 12 (hard) — Compound growth in traffic**

Internet-bound traffic through your secure web gateway is 4.0 Gbps at peak today and has grown at 20% per year for the past three years. If that compound growth continues, approximately what peak will you need to design for in three years' time?

A) 6.4 Gbps
B) 6.9 Gbps
C) 7.2 Gbps
D) 8.0 Gbps

**Correct answer: B.**

**Explanation:** Compound growth: 4.0 × 1.2³ = 4.0 × 1.728 = 6.912 ≈ 6.9 Gbps. Distractor C comes from simple (linear) growth: 20% of 4.0 is 0.8, and 4.0 + 3 × 0.8 = 6.4 — which is actually option A; option C (7.2) is 4.0 × 1.8, a mangled hybrid. The difference between linear and compound assumptions widens every year, which is why capacity plans built on linear extrapolation run out early. When a question says growth "per year" continuing over multiple years, multiply by the growth factor raised to the power of the years; mental shortcut: 1.2³ ≈ 1.73.

**Question 13 (moderate) — Percentage points versus percentages**

An assurance report states: "Following the remote access redesign, VPN connection success rose from 92% to 96%." Which statement about the improvement is accurate?

A) Success improved by 4%
B) Success improved by 4 percentage points, which is a 4.3% relative improvement
C) Success improved by 4 percentage points, and the failure rate halved
D) Both B and C are accurate

**Correct answer: D.**

**Explanation:** The rise from 92% to 96% is 4 percentage points. As a relative change in the success rate it is 4 ÷ 92 = 4.35% ≈ 4.3%, so B is accurate. Meanwhile the failure rate fell from 8% to 4% — exactly halved — so C is also accurate, making D correct. Option A confuses percentage points with percent, the single most common numerical error in management reporting. As the person who shares assurance results so stakeholders trust the team, precise phrasing of improvements is part of your credibility: "we halved the failure rate" and "we improved success by 4.3%" describe the same change with very different force.

**Question 14 (moderate) — Data centre power and cooling budget**

A new data centre LAN pod will contain 8 switches drawing 1.1 kW each and 2 firewalls drawing 0.9 kW each. Cooling overhead adds 40% on top of equipment power. Electricity costs £0.25 per kWh. To the nearest hundred pounds, what is the pod's annual electricity cost? (Use 8,760 hours per year.)

A) £23,200
B) £26,000
C) £32,500
D) £36,500

**Correct answer: C.**

**Explanation:** Equipment power = 8 × 1.1 + 2 × 0.9 = 8.8 + 1.8 = 10.6 kW. With 40% cooling overhead: 10.6 × 1.4 = 14.84 kW total draw. Annual energy = 14.84 × 8,760 = 129,998.4 kWh. Cost = 129,998.4 × £0.25 = £32,499.60, which rounds to £32,500 — option C. Distractor A omits the cooling overhead entirely (10.6 × 8,760 × 0.25 = £23,214 ≈ £23,200). Whole-life infrastructure costing includes power and cooling, and business cases that forget the 40% multiplier understate running costs by exactly the margin between options A and C.

**Question 15 (hard) — Risk exposure weighting for a governance forum**

Your risk register quantifies three network risks. Risk 1: probability 10%, impact £900,000. Risk 2: probability 40%, impact £150,000. Risk 3: probability 25%, impact £320,000. The forum can fund mitigation for only one risk this quarter, and each mitigation halves its risk's probability. Which mitigation reduces expected loss the most?

A) Risk 1
B) Risk 2
C) Risk 3
D) All three reduce expected loss equally

**Correct answer: A.**

**Explanation:** Expected loss = probability × impact. Risk 1: 0.10 × £900,000 = £90,000; halving probability saves £45,000. Risk 2: 0.40 × £150,000 = £60,000; halving saves £30,000. Risk 3: 0.25 × £320,000 = £80,000; halving saves £40,000. Risk 1's mitigation saves the most (£45,000), despite Risk 2 having the highest probability and Risk 3 a superficially balanced profile. Because every mitigation halves its risk, the saving is always half the expected loss, so ranking expected losses suffices — spotting that structure avoids three redundant calculations. Quantified risk comparison of exactly this kind underpins the proportionate governance your role profile asks you to ensure: funding decisions should follow expected-loss arithmetic, not the loudest probability.

**Question 16 (moderate) — Unified communications sizing**

Your unified communications design must support concurrent voice calls across a WAN link. Each call consumes 100 kbps including overhead. The site has 900 staff; your design assumption is that at the busiest hour, 15% of staff are on external calls simultaneously. Voice traffic must not exceed 30% of the link's capacity, to protect data traffic. What is the minimum link capacity that satisfies the design rule?

A) 13.5 Mbps
B) 27 Mbps
C) 45 Mbps
D) 90 Mbps

**Correct answer: C.**

**Explanation:** Concurrent calls = 900 × 0.15 = 135. Voice bandwidth = 135 × 100 kbps = 13,500 kbps = 13.5 Mbps. The design rule caps voice at 30% of link capacity, so the link must satisfy: capacity × 0.30 ≥ 13.5 Mbps, giving capacity ≥ 13.5 ÷ 0.3 = 45 Mbps. Distractor A stops at the voice bandwidth itself, ignoring the 30% rule entirely; B applies a half-capacity rule that appears nowhere in the question; D divides by 15% instead of 30%, mixing up the two percentages in the scenario. Two-percentage questions like this reward labelling each figure as you extract it — "15% = who is calling, 30% = share of the link" — because under time pressure the unlabelled numbers blur. This is also genuine telephony design arithmetic: quality-of-service policies reserve link shares, and the sizing must be derived from the reservation, not from the raw demand.

- **Rebuild the classics until they are reflexes.** Percentages of totals, percentage change, ratios, unit cost, and compound growth cover most questions. Ten minutes of drill a day for two weeks beats a weekend cram.
- **Practise unit hygiene.** Mbps versus Gbps, GB versus TB, monthly versus annual: before calculating, convert everything to one unit and write it down. Most wrong answers in this domain are unit errors, not arithmetic errors.
- **Learn the estimation shortcuts.** Adding unavailabilities instead of multiplying availabilities, 1.2³ ≈ 1.73, and rounding to check the order of magnitude will let you sanity-check options in seconds.
- **Use real artefacts for practice.** Take last quarter's capacity report or a genuine supplier quote and generate your own questions: cost per Mbps, projected utilisation, downtime allowance. Familiar data lowers cognitive load in the real test.
- **Decide your calculator workflow in advance.** If an onscreen calculator is provided, practise with one rather than your phone; keystroke fumbles under time pressure are a silent score killer.
- **Answer the question asked.** Year-to-date variance versus projected variance, total cost versus unit cost, percentage versus percentage points: at lead level the arithmetic is rarely the hard part — the reading is.

### Common pitfalls

- **Misreading scale qualifiers.** Tables quoting "in thousands" or mixing Mbps with Gbps are standard traps; the data is designed so that ignoring the qualifier produces one of the wrong options.
- **Over-calculating.** If options differ by large margins, estimate first. Computing 0.9995 × 0.999 × 0.998 to six decimal places when adding unavailabilities gives the answer is a time sink.
- **The time-sink question.** One deliberately laborious multi-stage item can absorb five minutes. Flag it, guess strategically from eliminated options if needed, and return only if time remains.
- **Normalisation blindness.** Comparing raw counts across differently sized estates (incidents per region, cost per site) without dividing by the base — the East region trap in Question 11.
- **Anchoring on headline figures.** The cheapest total is not the cheapest per unit; the lowest monthly rental is not the lowest whole-life cost. Procurement questions exploit this because real supplier pricing does too.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information — mirroring the exact reading demands of your role. The passages use the material you genuinely work with: technical standards, governance papers, service assessment reports, security policies, supplier correspondence, and strategy documents. The dominant format is a dense passage followed by statements you must classify as **True** (the passage says so), **False** (the passage contradicts it), or **Cannot Say** (the passage provides insufficient information either way), supplemented by multiple-choice comprehension questions about main arguments, obligations, and tone. Timing is tight — typically less than a minute per question — because workplace reading happens under deadline pressure too.

The cardinal rule is fact-based logic: answer strictly from the text provided, setting aside your own expert knowledge. This is harder for you than for a junior colleague, precisely because you know so much about networks — when a passage says something incomplete or debatable about SD-WAN, your expertise will whisper an answer the text does not support. Assessors know this, and senior-level verbal tests deliberately exploit it.

Why does this matter for your role? You cascade messages, standards and best practice from other architecture teams and design authorities to your team — which requires you to extract exactly what a standard obliges, permits, and forbids, without adding or losing meaning in transmission. You input into governance forums where a misread clause becomes a misdirected strategy. You act as a subject matter expert whose interpretations others rely on, and you communicate network concepts to technical and non-technical stakeholders alike, which demands precision about what a document actually establishes versus what it merely suggests.

### What it measures for your role

- **Governance and assurance.** Guiding teams through service assessments and assurance processes means parsing assessment criteria, standards, and report findings exactly. True/False/Cannot Say discipline is the psychometric version of reading an assessment report without inferring conclusions it never reached.
- **Systems design.** Ensuring adherence to relevant technical strategies, policies, standards and practices starts with correctly determining what those documents require. Questions on obligation language — "must", "should", "may" — test the close reading that separates a mandatory control from a recommendation.
- **Systems integration.** Defining integration builds from multiple suppliers' documents requires reconciling texts that use different terms for the same thing, and spotting where they genuinely conflict rather than merely differ in emphasis.
- **IT infrastructure and leadership duties.** Cascading standards and representing your team externally depend on faithful summarisation: multiple-choice "main point" questions measure whether you can compress a document without distorting it.
- **Troubleshooting and problem resolution.** Root cause analysis often turns on written evidence — incident timelines, vendor advisories, change records. Distinguishing what a report states from what it implies is the same skill as classifying a statement Cannot Say.

### Practice questions

**Passage A — extract from a departmental network standard**

*"All new wide area network circuits must be ordered with a minimum contractual availability of 99.9%. Circuits serving sites designated business-critical must additionally be provisioned as diverse pairs, with each circuit of the pair terminating on physically separate equipment. Software-defined WAN overlay services may be deployed over any compliant underlay circuit. Where a site cannot be served by two fixed-line circuits at proportionate cost, a wireless service may be used as the secondary circuit, subject to approval by the network design authority. This standard applies to all new orders placed after 1 April; existing circuits are exempt until contract renewal."*

**Question 1 (easy) — True / False / Cannot Say**

Statement: "Existing circuits must be upgraded to 99.9% availability immediately."

A) True
B) False
C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The final sentence states existing circuits "are exempt until contract renewal", which directly contradicts any immediate obligation. When a passage contains an explicit exemption, a statement asserting the opposite is False, not Cannot Say. Locate the governing sentence and match its scope — "existing circuits" — to the statement's subject before answering.

**Question 2 (moderate) — True / False / Cannot Say**

Statement: "A business-critical site may use a wireless service as its secondary circuit if the design authority approves."

A) True
B) False
C) Cannot Say

**Correct answer: A (True).**

**Explanation:** The wireless provision applies "where a site cannot be served by two fixed-line circuits at proportionate cost... subject to approval by the network design authority". The passage does not exclude business-critical sites from this provision — the diverse-pair requirement concerns physical termination separation, and nothing states the second circuit must be fixed-line for business-critical sites. Careful reading shows the wireless clause applies to sites generally, so with approval (and the cost condition) a business-critical site may use it: True. Your operational instincts might protest that wireless backup at a critical site is poor practice — but the question asks what the standard permits, and the text permits it. This is the expertise trap in action.

**Question 3 (moderate) — True / False / Cannot Say**

Statement: "SD-WAN overlay services require design authority approval."

A) True
B) False
C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The passage says SD-WAN overlays "may be deployed over any compliant underlay circuit" — permission with a compliance condition, and no approval requirement attached. The only design authority approval in the passage attaches to wireless secondary circuits. Because the passage grants deployment permission without approval, a statement asserting approval is required contradicts the text: False. Note the contrast with Cannot Say: had the passage simply never mentioned SD-WAN, the answer would be Cannot Say; here it addresses SD-WAN and imposes no such condition, and "may be deployed" is the operative grant.

**Question 4 (hard) — Multiple choice**

Which of the following orders would comply with the standard without any approval being needed?

A) A business-critical site served by one fibre circuit at 99.9% availability
B) A standard site served by one fibre circuit at 99.95% availability plus a wireless secondary
C) A business-critical site served by two fibre circuits at 99.9% each, terminating on physically separate equipment
D) A standard site served by one fibre circuit at 99.5% availability

**Correct answer: C.**

**Explanation:** Option A fails the diverse-pair requirement for business-critical sites (only one circuit). Option B includes a wireless secondary, which is permitted only "subject to approval" — so it can comply, but not "without any approval being needed", which the question stem requires. Option D breaches the 99.9% minimum availability. Option C satisfies every applicable clause: availability at the minimum, diverse pair present, physically separate termination. The question rewards reading the stem as carefully as the options — "without any approval" is the discriminator that eliminates B.

**Passage B — email from the enterprise design authority**

*"Colleagues — following last month's review, the design authority has agreed that all future network designs submitted for endorsement must include an integration test plan covering inter-system dependencies, and a rollback statement for each disruptive implementation step. Designs lacking either element will be returned without review. We expect this to add no more than two days to design preparation. Please note that the requirement for a security architecture opinion remains unchanged, and that designs previously endorsed do not need to be resubmitted. We are also considering whether to require capacity modelling for designs above £250,000, and will consult lead architects before deciding."*

**Question 5 (easy) — True / False / Cannot Say**

Statement: "Designs submitted without a rollback statement will be reviewed but not endorsed."

A) True
B) False
C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The email states such designs "will be returned without review" — they are not reviewed at all. The statement claims they will be reviewed (but not endorsed), which contradicts the text directly. Watch for statements that soften or partially restate a consequence; "returned without review" and "reviewed but not endorsed" describe different processes, and the difference matters to a team planning submission timelines.

**Question 6 (moderate) — True / False / Cannot Say**

Statement: "Capacity modelling is now required for designs above £250,000."

A) True
B) False
C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The email says the authority is "considering whether to require" capacity modelling and "will consult lead architects before deciding". A consideration is not a requirement, and the text makes clear no decision has been taken — so the statement that it "is now required" contradicts the passage: False. This distinction — proposal versus decision — is one you manage constantly when cascading messages from design authorities: transmitting a consultation as a mandate would misdirect your whole team, which is why verbal tests probe it.

**Question 7 (hard) — True / False / Cannot Say**

Statement: "The new submission requirements will delay most designs by two days."

A) True
B) False
C) Cannot Say

**Correct answer: C (Cannot Say).**

**Explanation:** The email says the authority "expect[s] this to add no more than two days to design preparation". That is an expectation of an upper bound, not a claim about the typical delay: designs might be delayed by two days, by less, or conceivably by more if the expectation proves wrong — and "most designs" introduces a distribution the text never addresses. The passage neither confirms nor contradicts the statement, so Cannot Say. Two traps coexist here: treating an expectation as a fact (pushing you toward True) and treating "no more than two days" as inconsistent with "two days" (pushing you toward False). The text simply does not determine the truth of the statement.

**Question 8 (moderate) — Multiple choice**

What is the main purpose of the design authority's email?

A) To announce a decision on capacity modelling thresholds
B) To notify architects of new mandatory elements in design submissions and their consequences
C) To require previously endorsed designs to be resubmitted with test plans
D) To remove the requirement for a security architecture opinion

**Correct answer: B.**

**Explanation:** The core message is the new mandatory elements (integration test plan, rollback statement) and the consequence of omission (returned without review). Option A describes the item still under consultation; C and D directly contradict the text ("do not need to be resubmitted"; "remains unchanged"). Main-purpose questions reward asking: which option, if deleted, would gut the email? Only B. The wrong options are all built from real fragments of the passage — familiar words do not make a faithful summary, a caution that applies equally when you summarise authority decisions for your own team.

**Passage C — extract from a service assessment report**

*"The panel found that the team's network design meets the security and resilience expectations of the Service Standard at this phase. However, the panel was not shown evidence that the remote access solution had been tested with users who rely on assistive technology, and the team acknowledged that accessibility testing of the administrator portal is planned but not yet complete. The panel also noted that the team's reliance on a single named engineer for firewall changes presents a continuity risk. The service may proceed to private beta on condition that the accessibility testing is completed before public beta, and that the firewall knowledge is documented and shared across at least two additional engineers."*

**Question 9 (easy) — True / False / Cannot Say**

Statement: "The panel found the network design fails the Service Standard's resilience expectations."

A) True
B) False
C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The first sentence states the design "meets the security and resilience expectations of the Service Standard at this phase" — the direct opposite of the statement. The qualifier "at this phase" limits the finding's scope but does not turn a pass into a fail. Answer from the finding as written.

**Question 10 (hard) — True / False / Cannot Say**

Statement: "The remote access solution is not accessible to users of assistive technology."

A) True
B) False
C) Cannot Say

**Correct answer: C (Cannot Say).**

**Explanation:** The panel "was not shown evidence" that assistive technology testing had occurred. Absence of evidence of testing is not evidence of inaccessibility: the solution might work perfectly well with assistive technology, or it might not — the passage establishes only that testing evidence was missing. Candidates who jump to True conflate an assurance gap with a failure; candidates who choose False assume the solution is accessible, which the text equally fails to establish. This distinction is the daily bread of assurance work: an unevidenced control is a finding, not a proven defect, and reporting it accurately is what makes stakeholders trust your team's assessments.

**Question 11 (moderate) — Multiple choice**

Which of the following is a condition of proceeding to private beta?

A) Completing accessibility testing before private beta begins
B) Documenting firewall knowledge and sharing it across at least two additional engineers
C) Replacing the single named engineer responsible for firewall changes
D) Retesting the network design against the Service Standard

**Correct answer: B.**

**Explanation:** The conditions are: accessibility testing completed "before public beta" (not before private beta — option A misplaces the deadline), and firewall knowledge "documented and shared across at least two additional engineers" — option B, almost verbatim. Option C overshoots: the panel requires knowledge sharing, not replacing anyone. Option D is not mentioned. Deadline displacement (private versus public beta) is a classic distractor; in real assurance work that misreading would impose a condition a phase early, so the test's pedantry is the job's pedantry.

**Passage D — extract from a remote access security policy**

*"Remote administrative access to network infrastructure must be initiated through the centrally managed bastion service and authenticated using multi-factor authentication. Standing administrative sessions are prohibited: sessions must terminate after 30 minutes of inactivity. Emergency access outside the bastion service is permitted only during a declared major incident, must use the break-glass credential set, and must be reported to the security operations centre within 24 hours of use. The security operations centre will review all break-glass usage monthly and report unexplained usage to the chief security officer."*

**Question 12 (moderate) — True / False / Cannot Say**

Statement: "An engineer who uses break-glass credentials during a declared major incident has breached the policy."

A) True
B) False
C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The policy explicitly permits emergency access "during a declared major incident" using "the break-glass credential set". Using the credentials in exactly that circumstance is compliant conduct, not a breach — provided the other conditions (outside-bastion use limited to the incident, 24-hour reporting) are met; the statement as written describes permitted use, so it is contradicted by the text. Note the statement does not mention failing to report — do not import a hypothetical violation the statement never asserts. Answer the statement given, not a nearby harder one.

**Question 13 (hard) — True / False / Cannot Say**

Statement: "The security operations centre reports all break-glass usage to the chief security officer."

A) True
B) False
C) Cannot Say

**Correct answer: B (False).**

**Explanation:** The policy says the centre will "report unexplained usage" to the chief security officer — a subset, not all usage. The statement generalises "unexplained usage" to "all usage", which the text contradicts by specifying the narrower category. Quantifier substitution — all for some, must for may, always for monthly — is the most reliable trap in verbal reasoning at every level, and the most consequential error when you cascade policy obligations to your team: telling engineers that every break-glass use goes to the chief security officer misstates the escalation model.

**Question 14 (moderate) — Multiple choice, tone and intent**

A supplier's letter states: *"While we remain committed to the partnership, we must advise that continued delays in site access approvals are placing the migration schedule at risk, and we reserve our position regarding associated costs."* Which statement best captures the letter's intent?

A) The supplier is terminating the contract
B) The supplier is signalling a potential future claim for delay-related costs while keeping the relationship open
C) The supplier is accepting responsibility for the migration delays
D) The supplier is waiving any claim to additional costs

**Correct answer: B.**

**Explanation:** "We reserve our position regarding associated costs" is contractual signalling: it preserves the right to claim later without claiming now. "While we remain committed to the partnership" keeps the relationship open, and the letter attributes delay to "site access approvals" — the customer's side — the opposite of accepting responsibility (C). Nothing suggests termination (A) or waiver (D, which is the direct opposite of reserving a position). Reading commercial correspondence for its operative signals, beneath its courteous surface, is part of developing procurement strategies and representing your function externally — and verbal tests at senior level increasingly include exactly this register.

**Passage E — extract from a cloud connectivity strategy paper**

*"The department will adopt a cloud-first connectivity model. New services should connect to cloud environments via the shared interconnect platform rather than dedicated circuits, unless a service's throughput or latency requirements demonstrably exceed the platform's published capabilities. Teams choosing dedicated circuits must record the justification in the architecture decision log. The shared platform currently supports up to 10 Gbps per service and a latency of no more than 12 milliseconds to the primary cloud regions. The platform team intends to double the supported throughput within 18 months, subject to funding. Legacy dedicated circuits will be reviewed annually, and decommissioned where the shared platform can meet the service's requirements."*

**Question 15 (moderate) — True / False / Cannot Say**

Statement: "A new service requiring 8 Gbps and 10 milliseconds latency must use the shared interconnect platform."

A) True
B) False
C) Cannot Say

**Correct answer: B (False).**

**Explanation:** Careful with the obligation strength. The paper says new services "should" connect via the shared platform — a strong recommendation, not an absolute mandate — and provides an explicit route to choose dedicated circuits (record the justification in the decision log). A service within the platform's capabilities (8 Gbps ≤ 10 Gbps; 10 ms ≤ 12 ms) is expected to use it, but "must use" overstates what the text requires: the policy's own mechanism contemplates teams choosing otherwise with justification. Since the passage's "should... unless" plus a documented-exception route contradicts an unconditional "must", the statement is False. If the passage had said "must connect... unless", the analysis would change — one word carries the question.

**Question 16 (hard) — True / False / Cannot Say**

Statement: "In 18 months the shared platform will support 20 Gbps per service."

A) True
B) False
C) Cannot Say

**Correct answer: C (Cannot Say).**

**Explanation:** The platform team "intends to double the supported throughput within 18 months, subject to funding". An intention with an explicit funding condition establishes neither that the upgrade will happen nor that it will not: if funded, doubling 10 Gbps gives 20 Gbps as the statement says; if not funded, it does not happen. The passage cannot settle the statement's truth, so Cannot Say. The gravitational pull here is toward True, because the arithmetic (10 × 2 = 20) checks out — but correct arithmetic applied to a conditional intention still yields a conditional, and verbal reasoning scores the logic, not the sums. When you cascade roadmap commitments to your team or quote them in designs, the same discipline applies: "intends, subject to funding" must never be transmitted as "will".

**Question 17 (moderate) — Multiple choice on Passage E**

According to the passage, which of the following statements about legacy dedicated circuits is accurate?

A) They must all be migrated to the shared platform within 18 months
B) They will be reviewed annually and decommissioned where the shared platform can meet the service's requirements
C) They are exempt from the cloud-first connectivity model permanently
D) They must be recorded in the architecture decision log at the next review

**Correct answer: B.**

**Explanation:** Option B restates the passage's final sentence almost exactly: "Legacy dedicated circuits will be reviewed annually, and decommissioned where the shared platform can meet the service's requirements." Option A invents a deadline by borrowing the 18-month figure from the throughput roadmap — a different sentence about a different subject; cross-contamination between adjacent facts is a favourite distractor construction. Option C converts a conditional review regime into a permanent exemption, which the decommissioning clause contradicts. Option D misapplies the decision-log obligation, which the passage attaches to teams choosing dedicated circuits for new services, not to legacy reviews. Notice the general pattern across all four wrong answers in questions like this: each is assembled from genuine fragments of the passage, rearranged. The defence is always the same — return to the sentence that governs the statement's subject and check that every element (who, what, when, on what condition) matches before you accept the option.

- **Train the Cannot Say reflex.** Most wrong answers at senior level come from classifying Cannot Say statements as True. Before answering True, demand a sentence in the passage that states or entails the claim; before answering False, demand a sentence that contradicts it. No sentence, no verdict: Cannot Say.
- **Suppress your expertise deliberately.** You know more about networks than any passage will. Practise on passages about your own specialism precisely because that is where imported knowledge leaks in — the Question 2 wireless-backup trap is built for experts.
- **Highlight obligation language.** Circle must/should/may/prohibited/permitted as you read. Half the questions turn on the strength of an obligation, and marking it costs two seconds.
- **Watch quantifiers and deadlines.** All versus some, each versus most, before private beta versus before public beta. Verify the statement's quantifier and timing against the passage word by word.
- **Read the stem before the passage.** For multiple-choice items, knowing what is asked ("main purpose", "which complies", "which is a condition") lets you read the passage with purpose rather than re-reading it twice.
- **Practise on your real inbox.** Take a genuine standards document or assessment report and write three statements about it: one True, one False, one Cannot Say. Composing the trap teaches you to see it.

### Common pitfalls

- **Bringing outside knowledge.** The test measures reading, not networking. If the passage says something your experience disputes, the passage wins for the duration of the test.
- **Confusing likelihood with fact.** "The authority expects no more than two days' delay" does not establish what will happen — expectations, plans, and considerations are not outcomes.
- **Treating absence as denial.** A passage that never mentions approval requirements neither imposes nor removes them; but a passage that grants permission without conditions contradicts a claimed condition. Learn the difference — it separates Cannot Say from False.
- **Skimming dense text for keywords only.** Keyword matching finds the sentence but misses its qualifiers ("at this phase", "unexplained usage"). Read the whole governing sentence before answering.
- **Poor time allocation.** Reading a 200-word passage exhaustively before seeing the questions doubles your reading time. Skim for structure, read the stem, then read the relevant portion closely.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skill, and professional conduct through realistic workplace dilemmas. Unlike the cognitive, numeric, and verbal tests, there is usually no single objectively right answer: several responses may seem reasonable, and the assessment measures how well your behavioural choices align with the values of the organisation and the demands of the role. Response formats typically ask you to pick the **most effective** and **least effective** actions from a set, or to rank or rate all the options from best to worst. Timing is generous or absent, because the point is your natural judgement rather than your speed.

For a lead network architect, the scenarios are not about configuring routers — they are about the human and organisational systems around the technology. Your role profile is explicit: you are a point of escalation; you input into governance forums that determine IT strategy; you cascade standards from design authorities to your team; you coach and mentor network architects and associate network architects; you champion new technologies; and you represent network architects internally and externally as a strategic thinker who can communicate with technical and non-technical stakeholders. Every one of those is a judgement-rich activity where the difference between a good and poor choice is behavioural, not technical.

In a UK public sector context, effective answers tend to align with recognisable values: putting user needs first, transparency and honesty (especially when things go wrong), collaboration across teams and departments, accessibility and inclusion as obligations rather than afterthoughts, proportionate use of public money, and developing people. Options that delay action, quietly pass problems along, protect personal standing over service outcomes, or bypass legitimate governance tend to score poorly — even when they feel pragmatic.

### What it measures for your role

- **Governance and assurance.** Scenarios test whether you uphold proportionate governance under pressure — resisting the shortcut that skips a review, while also avoiding governance theatre that adds delay without value. Your profile asks you to ensure governance is "appropriate and proportionate", which is itself a judgement call.
- **IT infrastructure (leadership strand).** Leading teams through design, implementation, and support generates classic people dilemmas: underperformance, conflict, credit, and workload — especially in your coaching and mentoring duties.
- **Systems design.** Controlling design practice across an enterprise means handling disagreement with other architects, design authorities, and suppliers about high-risk designs, where how you disagree matters as much as whether you are right.
- **Systems integration.** Co-ordinating build activities across systems creates cross-team friction: slipping dependencies, contested priorities, and integration defects with unclear ownership.
- **Troubleshooting and problem resolution.** Escalation scenarios test composure and sequencing: stabilise the service, communicate honestly, then fix the root cause — in that order.

### Practice questions

**Question 1 (moderate) — The governance shortcut**

A programme director asks you to endorse a network design for a new citizen-facing service so procurement can start this week. The design has not been through the security architecture review that your governance framework requires for services handling citizen data. The director says: "You're the lead architect — your sign-off is surely enough. The review will only tell us what you already know."

Which is the MOST effective and which the LEAST effective response?

A) Endorse the design personally and note that the security review should follow later.
B) Refuse to engage until the review is complete, and tell the director the timeline is their problem.
C) Explain why the review is required, then work with the security team to arrange an expedited review and identify what procurement steps can proceed in parallel without commitment.
D) Escalate the director's request to their superior as an attempted governance breach.

**Most effective: C. Least effective: A.**

**Explanation:** Option C upholds the control while solving the director's real problem — pace. It is collaborative, transparent, and proportionate: expediting a review and sequencing procurement activities protects both the citizen data and the schedule. Option A is least effective because it substitutes personal authority for a required control on a citizen-data service; if the review later finds a flaw, procurement is committed and the governance framework you are accountable for improving has been undermined by its own guardian. Option B protects the control but abandons the relationship and the outcome — refusing to help find a legitimate path is passive and damages the trust your role profile says stakeholders should have in your processes. Option D leaps to escalation before attempting resolution; escalation is a tool for genuine impasses, not first contact. The pattern to internalise: the strongest answers hold the standard and help deliver.

**Question 2 (moderate) — The struggling associate architect**

An associate network architect you mentor has submitted a routing design with a significant flaw for the third time, despite your previous feedback. The team's delivery deadline is close, and a senior colleague suggests you "just redo it yourself — it's quicker."

Rank the following from most to least effective:

A) Redo the design yourself tonight and submit it without comment, to protect the deadline.
B) Sit with the associate, work through the flaw together against the previous feedback, and agree a short structured plan for closing the gap, while assessing whether the deadline needs a flag.
C) Return the design with written feedback for a fourth iteration and remind them the deadline is close.
D) Reassign the associate to simpler work and give the design to a senior architect.

**Most effective ranking: B, D, C, A.**

**Explanation:** B is strongest: it addresses the immediate defect, converts a failing feedback loop (written comments have not worked three times) into active coaching, and handles the delivery risk honestly by flagging it — coaching and mentoring are core accountabilities of your role, not luxuries for quiet weeks. D is second: it protects delivery and can be legitimate workload management, but it postpones the development problem and risks signalling lost confidence — acceptable, not ideal. C repeats an approach that has demonstrably failed three times, adds deadline pressure without support, and invites a fourth flawed iteration. A is worst: it hides the problem from everyone, teaches the associate nothing, sets an unsustainable precedent, and misleads the team about the design's provenance — quietly absorbing others' work is the passive option in leader's clothing. Situational judgement scoring penalises both avoidance and heroics; it rewards development with delivery honesty.

**Question 3 (hard) — Conflicting messages from design authorities**

You cascade standards from central design authorities to your network architecture team. This month, the enterprise architecture team's new pattern mandates routing all cloud-bound traffic through a central inspection service, while the cloud platform team's guidance tells service teams to connect directly to the cloud provider's private endpoints for performance. Two of your architects have asked which instruction to follow, and a project is blocked awaiting your answer.

Which is the MOST effective and which the LEAST effective response?

A) Tell your team to follow the enterprise architecture pattern, since enterprise architecture outranks platform guidance.
B) Raise the conflict with both authorities, ask for a joint position with a timescale, give your team a documented interim position for the blocked project based on its specific risk profile, and record the decision in the architecture decision log.
C) Tell your architects to use their own judgement case by case until the authorities sort it out.
D) Advise the blocked project to pause until the two authorities publish a reconciled position.

**Most effective: B. Least effective: C.**

**Explanation:** B does all four things a lead architect owes the situation: it surfaces the conflict to the people who own it (collaboration and transparency), it presses for a durable resolution, it unblocks the project now with a reasoned, documented interim decision — exactly what a subject matter expert and point of escalation is for — and the decision log makes the position auditable and reversible. A picks a side by org-chart heuristic rather than by risk and requirement, and leaves the underlying conflict festering for every future project. D protects you but sacrifices delivery: pausing a project you could safely unblock is disproportionate governance, the opposite of the "appropriate and proportionate" standard your profile sets. C is least effective because it abdicates precisely the responsibility your role exists to hold — it guarantees inconsistent designs across the team, pushes the conflict onto the least senior people, and forfeits the trust of both authorities and architects. When two legitimate authorities conflict, the lead's job is to broker, decide interim, and document.

**Question 4 (moderate) — The major incident escalation**

At 14:20, a WAN failure disconnects three offices, including one handling time-critical casework. The service desk has escalated to you as the senior network escalation point. Your team's on-call engineer believes a fix could take two hours; failing over to the backup circuit would restore service in twenty minutes but will disrupt the office's telephony for about five minutes during the switch. The head of the affected business unit calls demanding to know what is happening.

Which is the MOST effective immediate combination of actions?

A) Let the engineer attempt the two-hour fix to avoid any telephony disruption, and tell the business head you will update them when it is resolved.
B) Direct the failover, agree the five-minute telephony impact with the business head with a clear time estimate, keep the incident channel updated, and schedule root cause analysis for after service restoration.
C) Join the technical bridge yourself and take over the troubleshooting from the engineer, asking the business head to wait for the incident report.
D) Ask the business head to raise the priority formally with the service desk so the incident can be reclassified before action is taken.

**Correct answer: B.**

**Explanation:** B follows sound incident logic: restore service first via the known workaround, communicate the trade-off honestly to the affected stakeholder (a five-minute telephony hit against hours of casework outage is a decision the business can and should endorse in seconds), maintain transparent communication, and separate restoration from root cause. A prioritises avoiding a trivial disruption over a severe ongoing one and fobs off a legitimate stakeholder. C confuses seniority with utility: displacing the engineer adds no capability, removes coordination capacity, and leaves the business head unmanaged — as escalation point, your value is decisions and communication, not keyboard time. D is process theatre while offices sit disconnected — the passive option. Note how the scoring logic maps to public sector values: user needs (the casework) first, transparency with stakeholders, and proportionate action.

**Question 5 (hard) — Championing new technology responsibly**

You believe network automation tooling could remove a large amount of manual configuration work and error. You championed a proof of concept, and it went well. At the IT strategy governance forum, a senior director dismisses the proposal: "We tried automation years ago and it caused an outage. This is a solved argument." You know the earlier attempt used a different technology and failed largely through inadequate testing practices, which your proposal addresses directly.

Which is the MOST effective and which the LEAST effective response?

A) Accept the decision in the meeting and quietly continue expanding the proof of concept within your own team's networks.
B) Acknowledge the earlier failure's lessons, briefly distinguish the current proposal's testing and rollout controls from the previous attempt, and offer a short evidence paper with proof of concept results and a limited, reversible first deployment for the forum's next session.
C) Tell the director their information is out of date and press the forum to overturn the objection now.
D) Withdraw the proposal permanently, since senior opposition makes success unlikely.

**Most effective: B. Least effective: A.**

**Explanation:** B is how a strategic thinker champions technology: it treats the director's experience as evidence to be addressed rather than resistance to be defeated, converts the disagreement into a proposal with evidence, controls, and a reversible first step, and respects the forum's process by returning through it. C may be factually right but is behaviourally wrong: publicly contradicting a senior stakeholder and forcing an immediate decision entrenches opposition and marks you as an advocate rather than an adviser. D confuses one objection with a verdict; abandoning a well-evidenced improvement at the first pushback fails the "champion new technologies" accountability. A is least effective — worse than either arguing or withdrawing — because continuing a rejected initiative outside governance is a transparency failure: if it succeeds, you have taught your team that forums are optional; if it fails, you have engineered the exact ungoverned automation outage the director feared. Persistence through legitimate channels beats both surrender and stealth.

**Question 6 (moderate) — The integration blame boundary**

During integration testing for a new service, transactions fail intermittently. The application team insists "the network is dropping packets"; your network architect reports the network path is clean and believes the application's connection handling is at fault. The service manager emails both teams, copying your director: "Ten days to go-live. Network and application teams are blaming each other. I need this fixed."

Which is the MOST effective response?

A) Reply with the network monitoring evidence proving the network is clean, and state the problem must therefore be the application's.
B) Propose an immediate joint diagnostic session with both teams working from a shared timeline of evidence — packet captures, application logs, test results — with a single blended hypothesis list owned across both teams, and offer to convene it.
C) Ask your architect to re-run the network tests to be certain before responding to the email thread.
D) Suggest the service manager extend the go-live date until ownership of the fault is established.

**Correct answer: B.**

**Explanation:** B reframes the situation from adversarial to collaborative and applies your troubleshooting discipline — break the problem into component parts across technology capabilities using evidence from both sides of the boundary. Intermittent integration faults live disproportionately at interfaces (timeouts, keep-alives, MTU, asymmetric paths), where neither team's isolated view suffices; a shared evidence timeline is the fastest route to root cause, and convening it is exactly what a lead architect co-ordinating build activities across systems should do. A escalates the blame war with better ammunition — even if the network is clean, "not our fault" fixes nothing ten days out and corrodes a relationship the go-live depends on. C is quiet diligence but leaves the public deadlock standing and adds delay without collaboration. D concedes defeat before attempting the obvious joint step. Assessors consistently score boundary-spanning evidence-sharing above being provably right.

**Question 7 (moderate) — Representing the profession externally**

You are representing your department at a cross-government network architecture forum. Another department presents a remote access approach your department evaluated and rejected last year after it performed poorly for users with assistive technology. The presenter asks the room to endorse the approach as a cross-government pattern.

Which is the MOST effective and which the LEAST effective response?

A) Stay silent — criticising another department's work publicly is poor form, and your department can simply ignore the pattern.
B) Share your department's evaluation experience factually, including the assistive technology findings, and propose the pattern be endorsed only after accessibility testing evidence is added.
C) State that your department has already rejected this approach and will not adopt the pattern regardless of the forum's decision.
D) Raise your concerns privately with the presenter after the meeting, once the endorsement vote has taken place.

**Most effective: B. Least effective: A.**

**Explanation:** B treats evidence as a public good: your department paid for that learning, and cross-government collaboration exists precisely so departments do not repeat each other's mistakes. Framing the contribution around user needs and accessibility — statutory obligations for government services, not preferences — and proposing a constructive condition (endorse after evidence) improves the pattern rather than merely blocking it. C shares the information but weaponises it: "we will not adopt it regardless" pre-empts the forum's process and positions your department as unilateral. D shares the evidence only after it can no longer influence the decision — polite, and useless: a pattern with a known accessibility weakness would be endorsed for use across government while you waited for a corridor conversation. A is least effective because silence lets other departments ship a known accessibility problem to their users; representing network architects externally means contributing your hardest-won evidence, especially when it is unwelcome. Inclusion questions in UK public sector situational tests are rarely decorative — accessibility findings outrank meeting etiquette.

**Question 8 (hard) — The supplier relationship and the audit finding**

An internal audit of your business area's network finds that a managed service supplier has not been delivering the quarterly firewall rule reviews specified in the contract for over a year, though they have been invoicing for the full service. Your team should have noticed; the supplier's account manager, with whom you work well and who has been helpful in emergencies, asks you privately to "handle this between us — we'll do the missed reviews at no charge, and no one needs a formal finding."

Which is the MOST effective response?

A) Accept the offer — the outcome (reviews done, no cost) is the same as a formal route, without damaging a valuable relationship.
B) Decline the private arrangement; ensure the audit finding is recorded accurately, including your own team's monitoring gap; require a remediation plan through contract management covering the missed reviews and invoicing; and continue the professional relationship on transparent terms.
C) Report the supplier to your department's commercial team and push for contract termination to signal that non-delivery has consequences.
D) Record the finding but leave your own team's failure to notice out of the formal record, since the supplier's non-delivery is the substantive issue.

**Correct answer: B.**

**Explanation:** B is the only option that is fully transparent, proportionate, and honest in both directions. Suppressing an audit finding about invoiced-but-undelivered service on a public sector contract is not a relationship courtesy — it is concealing a financial irregularity involving public money, so A fails on integrity regardless of the practical remedy attached (and note how situational tests bait this trap by making the unethical option operationally convenient). C is disproportionate: termination for a failure the supplier has offered to remediate, on an otherwise functioning contract, punishes the service and its users to make a point — contract management exists for exactly this middle ground. D is the subtle one: it is B minus the self-declaration, and that omission matters, because governance you are accountable for improving only works when findings are complete — a monitoring gap that stays off the record will not get fixed and will recur with the next supplier. Owning your team's part of a failure is a scored behaviour in senior assessments, and in real life it is what makes stakeholders trust your assurance processes.

**Question 9 (moderate) — Strategic communication under pressure**

You are presenting the network strategy's resilience investment case to a board of non-technical senior leaders. Ten minutes before the session, the chair's office tells you your slot is cut from thirty minutes to ten, and the chair "wants the decision, not the technology". Your deck has eighteen technical slides.

Which is the MOST effective response?

A) Present the deck as designed but talk faster, since the technical evidence is what makes the case rigorous.
B) Open with the decision sought, the service and citizen impact of the current single points of failure, three options with costs and risks, and your recommendation — holding the technical detail for questions and a written annex.
C) Ask the chair's office to reschedule the item for a future board with a full thirty-minute slot.
D) Send the deck by email instead and offer to answer questions in writing, freeing the slot entirely.

**Correct answer: B.**

**Explanation:** B is the behaviour your role profile names explicitly: a strategic thinker who can communicate network concepts to non-technical stakeholders. Boards decide on outcomes, money, and risk; the eighteen technical slides are your evidence base, not your message, and relegating them to an annex loses nothing while respecting the board's format. A ignores an explicit steer from the decision-maker and buries the decision under compressed jargon — rigour that is not received is not rigorous. C trades a live decision opportunity for calendar risk: resilience investment delayed a board cycle is risk carried for months because the messenger preferred a longer slot. D abandons the advocacy, discussion, and immediate decision a board slot exists to provide. The general lesson for lead-level situational tests: adapt the communication to the audience and protect the decision, not the deck.

**Question 10 (hard) — Proportionate governance design**

You are accountable for improving your team's governance. A retrospective shows that small, low-risk network changes — a VLAN addition, a firewall rule for a well-understood service — take four weeks to traverse the same design review path as major architecture changes, and delivery teams have started making informal changes to avoid it. Two of your architects defend the single path: "One process means nothing slips through."

Which is the MOST effective response?

A) Keep the single path but add enforcement to stop informal changes, since circumvention is a discipline problem.
B) Introduce a risk-tiered process — pre-approved patterns and lightweight review for low-risk changes, full review for high-risk designs — with clear criteria for each tier, monitor outcomes, and address the informal changes by making the compliant route genuinely faster.
C) Exempt experienced engineers from review for small changes, trusting their judgement.
D) Escalate the informal changes to senior management so the delivery teams face consequences.

**Correct answer: B.**

**Explanation:** B is "appropriate and proportionate governance", verbatim from your role profile, turned into design: matching control weight to risk, using pre-approved patterns (which are themselves a governance artefact — standardisation doing the assuring), and treating circumvention as a signal about the process rather than only about the people. Governance that is faster to follow than to bypass enforces itself. A misreads the retrospective: when sensible people route around a control, enforcement alone drives the workaround deeper underground and the four-week queue remains — the root cause is disproportion, not indiscipline. C confuses tiering by risk with tiering by seniority; an experienced engineer's high-risk change still needs review, and an inexperienced engineer's pattern-conformant change may not — the criterion belongs on the change. D punishes the symptom while preserving the cause, and spends trust you will need for the redesign. This scenario rewards seeing governance as a system you engineer, which is precisely the shift expected between architect and lead architect.

### Preparation tips

- **Anchor on the role's accountabilities, not your instincts alone.** Before the assessment, re-read your role profile. Options that express coaching, proportionate governance, transparent escalation, and stakeholder communication align with what the test is calibrated to reward at lead level.
- **Look for the option that holds the standard and helps deliver.** In almost every well-written scenario, one option protects the principle while solving the practical problem. It is usually the keeper.
- **Judge actions, not intentions.** Ask what each option actually does to the service, the user, the team member, and the relationship — not what it feels like to choose it. "Redo it yourself tonight" feels helpful and behaves destructively.
- **Rehearse the ethical bright lines.** Public money, citizen data, accessibility obligations, and audit integrity are non-negotiable in UK public sector scoring. When one option quietly crosses such a line, no operational convenience redeems it.
- **Answer as the role, at the level.** The test asks what a lead network architect should do — decide interims, convene joint sessions, communicate trade-offs — not what a hands-on engineer or a detached executive would do.
- **Use most/least strategically.** Identifying the least effective option is often easier: look for concealment, abdication, blame, and disproportion first, then pick the most effective from what remains.

### Common pitfalls

- **Answering idealistically rather than effectively.** "Consult everyone and document everything" sounds virtuous but can be the passive option in disguise when a service is down or a decision is needed today.
- **Selecting passive options.** Waiting for authorities to reconcile, pausing projects, deferring to future meetings, handing problems upward unexamined — scoring keys consistently punish delay-and-defer patterns.
- **Over-escalating.** Escalation is a legitimate tool, but as a first move it signals inability to broker, coach, or decide — the capabilities your level exists to provide.
- **Protecting relationships over integrity.** The supplier scenario is the archetype: tests deliberately attach attractive practical outcomes to quiet arrangements. Transparency wins, every time.
- **Forgetting your own part.** Options that record others' failures but omit your team's (Question 8, option D) test whether your assurance instinct survives self-interest.
- **Ignoring the culture you are being tested for.** UK public sector scenarios reward user needs, openness, collaboration, and inclusion. If you find yourself choosing an option because it is fastest for the team but worse for the citizen, re-read the options.

## Conclusion

You have now worked through four substantial assessment areas — cognitive, numeric reasoning, verbal reasoning, and situational judgement — every one of them built from the real substance of your role: the designs you assure, the budgets and capacity figures you defend, the standards you cascade, and the judgement calls you make as a point of escalation and a mentor to your team.

A few closing thoughts. First, be encouraged by how much of this you already do. The elimination logic in the troubleshooting questions, the whole-life cost comparisons, the careful reading of obligation language, the instinct to hold a standard while helping a colleague deliver — these are not exam tricks; they are your professional practice made explicit. Preparing for a psychometric assessment is largely a matter of doing consciously, under a clock, what you do fluently every week.

Second, treat your practice results as a development map rather than a verdict. If Cannot Say statements kept catching you, that is a precision-of-reading muscle worth exercising before your next governance paper, not just your next test. If the prioritisation questions felt uncomfortable, that discomfort is useful information about how you triage competing demands in the real role. The assessments and the job improve together.

Third, keep perspective on assessment day. Rest beforehand, use the practice questions platforms provide, manage the clock deliberately, and remember that speed-accuracy reports reward steady, methodical work — the same temperament that makes a good lead architect. One difficult question, like one difficult meeting, does not define the outcome.

Finally, keep growing. Coaching your architects through these same question types is a powerful development exercise for them and for you; the best preparation for demonstrating judgement is a habit of reflecting on it. Wherever your next assessment, assurance panel, or governance forum takes you, approach it the way you approach a complex network design: understand the requirements, work systematically, check your reasoning, and communicate it clearly. You are well prepared — good luck.
