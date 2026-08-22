# Network Architect - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a network architect working within the UK Government Digital and Data profession. Whether you are preparing for an internal progression board, applying for a new post, or simply want to sharpen the mental skills you use every day, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills behind good job performance. They are widely used across the Civil Service and the wider public sector because they are fair, evidence-based, and focused on capability rather than background. For a network architect, they matter because your role sits at the intersection of deep technical judgement and broad stakeholder engagement: you design networks and specifications that support business strategies, you research new technologies and assure them appropriately, you agree service level agreements with third party vendors, you co-ordinate programme activities, and you coach associate network architects. Every one of those duties draws on the four ability areas covered in this document.

This guide is organised into four main assessment sections, each of which mirrors a common workplace psychometric test:

1. **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you really handle: network diagrams, IP addressing plans, design review comments, and change schedules.
2. **Workplace job-specific numeric reasoning assessment** - interpreting bandwidth figures, availability percentages, vendor pricing tables, capacity forecasts, and programme budgets.
3. **Workplace job-specific verbal reasoning assessment** - reading dense passages such as network standards, SLA clauses, governance policies, and vendor correspondence, then answering strictly from the text.
4. **Workplace job-specific situational judgement assessment** - realistic dilemmas involving engineers, vendors, associate architects, security teams, and programme stakeholders, where you judge which responses are most and least effective.

Each section explains what the assessment measures, maps it explicitly to the skills in your role profile (governance and assurance, IT infrastructure, systems design, systems integration, and troubleshooting and problem resolution), provides a generous set of practice questions with full worked explanations, and closes with preparation tips and common pitfalls.

How should you use this guide? Work through it at your own pace. Attempt each question before reading the answer, note where your reasoning differed from the explanation, and revisit the sections that feel least comfortable. Treat it as practice, self-reflection, and preparation combined. There is no pass mark here - the aim is growth. You already use these skills daily; this guide simply helps you demonstrate them under assessment conditions. Good luck, and enjoy the practice!

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes needed for your role, using practical workplace scenarios rather than abstract puzzles. Unlike a generic IQ test, the questions mimic the everyday tasks and data formats of a network architect's job: reading network topology descriptions, spotting inconsistencies in design documents, deducing the cause of a fault from a set of symptoms, and deciding what to do first when several demands compete.

Typical delivery is online and timed, usually 15 to 30 minutes, with objective scoring against a benchmark or norm group. Modern platforms may adapt question difficulty to your answers, and employers usually receive a breakdown of speed versus accuracy rather than a single score. Most providers offer short, ungraded practice questions first so you can get used to the interface - always take these.

For you, this assessment matters because network architecture is fundamentally a reasoning discipline. When you design a system characterised by medium levels of risk, impact, and business or technical complexity, you are performing structured logical deduction. When you review the systems designs of others to check technology selection and efficient use of resources, you are error checking. When you break a problem down into its component parts to identify root causes, you are doing exactly what a cognitive test measures - just with routers, firewalls, and cloud networks instead of shapes and sequences.

### What it measures for your role

- **Pattern recognition** maps to your **IT infrastructure** skill: recognising recurring structures in LAN, WAN, wifi, data-centre LAN and software-defined network designs, spotting the addressing scheme behind a set of subnets, and seeing where a proposed cloud network departs from an established pattern.
- **Logical deduction** maps to your **troubleshooting and problem resolution** skill: breaking a problem into component parts, ruling causes in or out from evidence, and diagnosing faults across different technology capabilities.
- **Error checking** maps to your **systems design** skill: reviewing the designs of others to ensure appropriate technology selection, efficient use of resources, and correct integration of multiple systems and technologies.
- **Prioritisation and planning** maps to your programme duties: planning, directing and co-ordinating activities, engaging stakeholders, and sequencing an integration build so dependencies are respected.
- **Rule application** maps to your **governance and assurance** skill: applying design standards and assurance processes consistently, and identifying where a document breaches an agreed rule.

### Practice questions

**Question 1 (easy) - Pattern recognition in an addressing plan**

Your department allocates site subnets in a consistent pattern: Site A uses 10.1.0.0/16, Site B uses 10.2.0.0/16, Site C uses 10.3.0.0/16. Within each site, user VLANs take the .10 to .19 third octet, printers take .20 to .29, and building management systems take .30 to .39. An associate architect proposes 10.4.25.0/24 for a new user VLAN at Site D.

Which statement is correct?

A) The proposal is consistent with the pattern.
B) The site octet is wrong but the VLAN range is right.
C) The site octet is right but the range .25 is reserved for printers, not users.
D) Both the site octet and the range are wrong.

**Correct answer: C.**

**Explanation:** Sites follow 10.N.0.0/16 in sequence, so Site D correctly takes 10.4.0.0/16 - the second octet is fine. However, the third octet 25 falls within the .20 to .29 range, which the pattern reserves for printers. A user VLAN should use .10 to .19, for example 10.4.12.0/24. This is exactly the kind of quiet inconsistency you catch when reviewing the designs of others: nothing is technically broken, but the standard is not being applied, which will confuse operations teams later.

**Question 2 (easy) - Logical deduction from monitoring evidence**

Your network management solution reports: all users at the Leeds office have lost access to a cloud-hosted service; users at Manchester and Bristol can reach it normally; Leeds users can still reach on-premises services and the internet generally. The cloud service provider reports no incidents.

Which is the most logical first hypothesis?

A) The cloud service is down.
B) The Leeds local area network has failed.
C) A route, firewall rule, or proxy path specific to Leeds-to-cloud traffic has changed.
D) The wide area network link at Leeds is down.

**Correct answer: C.**

**Explanation:** Deduce by elimination. The cloud service cannot simply be down (A), because Manchester and Bristol reach it and the provider reports no incident. The Leeds LAN cannot have failed entirely (B), because Leeds users still reach on-premises services. The Leeds WAN link cannot be fully down (D), because general internet access still works from Leeds. What remains is something specific to the path between Leeds and that cloud service - a routing change, a firewall or security policy rule, or a proxy configuration. This is textbook root-cause isolation: break the problem into components (site, LAN, WAN, path, destination) and rule each in or out with the evidence.

**Question 3 (moderate) - Error checking a design specification**

You are reviewing a high-level design produced by a supplier. It contains these four statements:

1. "Each of the two data centres will host one firewall; the pair operates in active/passive mode to remove any single point of failure."
2. "The SD-WAN overlay will carry voice traffic marked EF and will prioritise it over bulk data."
3. "All switch management interfaces will be reachable only from the dedicated management VLAN."
4. "The wireless design provides 2.4 GHz and 5 GHz coverage; legacy 2.4 GHz-only devices will connect via the 5 GHz radio when signal is weak."

Which statement contains an internal contradiction or impossibility?

A) Statement 1
B) Statement 2
C) Statement 3
D) Statement 4

**Correct answer: D.**

**Explanation:** A 2.4 GHz-only device by definition cannot connect via a 5 GHz radio, whatever the signal strength - the statement is physically impossible as written. Statement 1 is arguably weak design practice to debate (an active/passive pair spread across two data centres deserves scrutiny about failover behaviour), but it is not self-contradictory. Statements 2 and 3 are coherent and standard. In a live design assurance review you would flag D as an error to correct and might raise 1 as a question. Cognitive error-checking questions reward reading each claim literally and testing it for internal consistency before judging its wisdom.

**Question 4 (moderate) - Sequencing an integration build**

You are defining the integration build for a new data-centre LAN. Five activities remain:

- P: Physical cabling and rack power
- Q: Core switch installation and base configuration
- R: Firewall policy deployment
- S: Integration testing with the application platform
- T: Connecting the firewall pair to the core switches

Rules: Q requires P. T requires Q and the firewalls to be racked (part of P). R requires T. S requires R.

Which sequence is valid?

A) P, Q, R, T, S
B) P, Q, T, R, S
C) Q, P, T, R, S
D) P, T, Q, R, S

**Correct answer: B.**

**Explanation:** Work through the dependency chain: P must come first (both Q and the firewall racking depend on it). Q needs P, so Q is second. T needs Q, so T is third. R needs T, so R is fourth. S needs R, so S is last. That gives P, Q, T, R, S - option B. Option A deploys firewall policy (R) before the firewalls are connected (T); option C configures switches before cabling and power exist; option D connects firewalls to core switches that have not been installed. Defining the integration build and co-ordinating build activities across systems is a named duty of your role, and assessments frequently test it as a pure dependency-ordering puzzle.

**Question 5 (moderate) - Rule application in governance**

Your design assurance process states: "Any design introducing a new remote access technology must be reviewed by the security architecture board before procurement. Designs that reuse an approved remote access pattern need only a peer review. All designs, without exception, require a completed risk log before build."

Four project situations arise. Which one breaches the process?

A) A project reusing the approved always-on VPN pattern completes a peer review and a risk log, then starts the build.
B) A project introducing a new zero-trust network access product completes a peer review and a risk log, then starts procurement.
C) A project introducing a new zero-trust network access product obtains security architecture board review, then starts procurement while the risk log is still in draft.
D) A project reusing the approved VPN pattern obtains a full security architecture board review plus a risk log, then builds.

**Correct answer: B.**

**Explanation:** Take each rule literally. B introduces a new remote access technology but goes to procurement with only a peer review - the process demands security architecture board review before procurement, so B breaches it. C is compliant so far: board review happened before procurement, and the risk log rule bites "before build", not before procurement - the build has not started. D exceeds the minimum requirement, which is allowed; doing more assurance than required is not a breach. A follows the reuse route correctly. Developing, applying and supporting others in following governance and assurance processes means reading rules precisely - including noticing which stage each rule attaches to.

**Question 6 (moderate) - Pattern recognition in performance data**

Over six consecutive Mondays, the WAN link to a regional office shows peak utilisation of 42%, 47%, 52%, 57%, 62%, and 67%. Nothing else about the office has changed.

If the pattern continues, on which future Monday (counting from the last measurement) will utilisation first exceed 90%?

A) The 4th Monday
B) The 5th Monday
C) The 6th Monday
D) The 7th Monday

**Correct answer: B.**

**Explanation:** The series rises by exactly 5 percentage points each week. From 67%: Monday 1 = 72%, Monday 2 = 77%, Monday 3 = 82%, Monday 4 = 87%, Monday 5 = 92%. The first value exceeding 90% occurs on the 5th Monday. Recognising a linear trend and projecting it forward is a routine part of capacity planning for LAN and WAN estates, and it is one of the most common cognitive test formats: identify the rule, extend the sequence, check the boundary condition carefully (exceed 90%, not reach it - 87% on the 4th Monday does not qualify).

**Question 7 (moderate) - Logical deduction with vendor SLAs**

Three third party vendors support parts of your network. The contracts state:

- Vendor X responds to priority 1 incidents within 30 minutes, but only during business hours.
- Vendor Y responds within 2 hours, 24/7.
- Vendor Z responds within 1 hour, 24/7, but only for the data-centre LAN.

A priority 1 incident occurs at 02:00 on the campus wifi. Which is the fastest contractual response you can rely on?

A) 30 minutes, from Vendor X
B) 1 hour, from Vendor Z
C) 2 hours, from Vendor Y
D) No vendor is obliged to respond

**Correct answer: C.**

**Explanation:** Apply each constraint. Vendor X's 30-minute promise does not apply at 02:00 because it is limited to business hours. Vendor Z responds around the clock, but only for the data-centre LAN - campus wifi is out of scope. Vendor Y covers 24/7 with no scope restriction stated, so its 2-hour commitment is the fastest response you can contractually rely on. D is wrong because Y is obliged. Agreeing SLAs and engaging with third party vendors is a core duty of this role, and assessments love this structure: several rules, each with a qualifier, where the right answer comes from applying every qualifier rather than grabbing the smallest number.

**Question 8 (moderate) - Error checking a change schedule**

A change schedule for a firewall migration weekend reads:

- 20:00 Freeze all other network changes
- 20:30 Take configuration backups of both old firewalls
- 21:00 Cut over site traffic to the new firewall pair
- 21:30 Decommission the old firewalls and wipe their configurations
- 22:00 Run the full integration test plan
- 22:30 Declare success or invoke rollback to the old firewalls

Which is the most serious logical flaw?

A) The freeze at 20:00 is unnecessary.
B) Backups should be taken after cutover, not before.
C) The old firewalls are wiped at 21:30, but the plan still offers rollback to them at 22:30.
D) Integration testing should happen before the freeze.

**Correct answer: C.**

**Explanation:** The plan destroys its own safety net: once the old firewalls are decommissioned and wiped at 21:30, "rollback to the old firewalls" at 22:30 is impossible. Decommissioning must move to after the success declaration - typically days later, after a stability period. A is wrong because freezing other changes during a major migration is good practice, reducing confounding variables if troubleshooting is needed. B is backwards - backups must precede risky work. D is wrong because you cannot integration-test a cutover that has not happened. Spotting the step that invalidates a later step is classic error checking, and precisely what you do when reviewing implementation plans with engineers to ensure systems are practically designed.

**Question 9 (hard) - Root cause isolation across capabilities**

Users report that voice calls on the unified communications platform break up every weekday between 09:00 and 09:30, then recover. You gather these facts:

1. WAN utilisation peaks at 95% during 09:00-09:30 as laptops run cloud backups on login.
2. Voice packets are marked EF, and the WAN routers are configured to prioritise EF.
3. A packet capture shows voice packets arriving at the far end with correct EF markings but high jitter.
4. The wifi controller shows no congestion on the voice VLAN's SSID.
5. Six months ago the WAN circuit was upgraded, and the provider confirmed the new circuit carries QoS markings transparently.

Which hypothesis best fits all the evidence?

A) The wifi network is dropping voice packets.
B) QoS is misconfigured such that EF traffic is marked but not actually prioritised at the congestion point.
C) The unified communications platform is overloaded at 09:00.
D) The WAN provider is stripping QoS markings.

**Correct answer: B.**

**Explanation:** Test each hypothesis against every fact. A fails: fact 4 shows no wifi congestion. D fails: fact 3 shows markings arrive intact at the far end. C is weakened because the problem correlates exactly with WAN saturation (fact 1) and expresses as jitter in transit (fact 3), not as platform errors. B fits everything: the link saturates (fact 1), markings survive end to end (facts 3 and 5), yet voice still suffers jitter - so something in the queuing path is not honouring the EF priority in practice, even though configuration says it should (fact 2). Perhaps the policy is applied to the wrong interface or the priority queue is undersized. The discipline here - a hypothesis must explain all the evidence, not most of it - is the heart of troubleshooting and problem resolution.

**Question 10 (hard) - Prioritisation under competing demands**

It is 09:00 Monday. Four items compete for your day:

1. A programme board at 14:00 needs your network design decision paper, currently 80% complete; without it, a procurement decision slips a month.
2. An associate network architect you mentor has asked for an hour to walk through their first solo design before their 11:00 review.
3. A vendor has emailed offering a demonstration of a new SD-WAN feature, available today or in three weeks.
4. Operations report a minor but recurring wifi authentication fault affecting one meeting room; a workaround exists.

Which ordering best reflects sound prioritisation?

A) 3, 1, 2, 4
B) 1, 2, 4, 3
C) 2, 1, 3, 4
D) 1, 4, 2, 3

**Correct answer: C.**

**Explanation:** Both items 1 and 2 are urgent today, but item 2 has the earlier immovable deadline (11:00 versus 14:00) and takes a bounded hour; helping first still leaves the morning and early afternoon to finish a paper that is already 80% complete. Coaching and mentoring associate architects is a stated responsibility, not a favour. Item 1 follows immediately - its consequence (a month's procurement slip) is the largest. Item 3 explicitly offers a three-week alternative, so deferring costs nothing; researching new technologies matters, but not today. Item 4 has a workaround and low impact, so it can be scheduled or delegated - though "delegated with a ticket" beats "forgotten". Option B fails because rigidly doing the paper first risks missing the associate's 11:00 review entirely. Good prioritisation weighs deadline, impact, and reversibility together.

**Question 11 (hard) - Deduction from an incomplete topology description**

A design document states: "Every site connects to at least one of the two hub data centres. Sites classified critical connect to both hubs. Site Alpha connects only to Hub North. Site Beta is classified critical. Hub South has exactly three site connections: Beta, Gamma, and Delta."

Which statement must be true?

A) Gamma is classified critical.
B) Alpha is not classified critical.
C) Delta connects to Hub North.
D) Beta connects only to Hub South.

**Correct answer: B.**

**Explanation:** Critical sites connect to both hubs. Alpha connects only to Hub North, so Alpha cannot be critical - B must be true. A is not forced: Gamma connects to Hub South, but nothing says whether it also connects to Hub North, so its classification is undetermined. C is not forced: Delta might connect only to Hub South, which satisfies "at least one hub" if Delta is not critical. D is false: Beta is critical, so it must connect to both hubs, not only South. Assessments reward distinguishing what must be true from what merely could be true - the same discipline you apply when a design document is silent on a detail and you must not assume it.

**Question 12 (hard) - Resource-efficiency review**

You review a design that proposes: dedicated physical firewalls at each of 12 small branch offices; a separate wifi controller per branch; and a full-mesh WAN so every branch connects directly to every other branch. Traffic analysis shows 96% of branch traffic goes to the data centres or the cloud, and branches average 25 users.

Which review finding best challenges the design's efficiency?

A) The design lacks redundancy.
B) The full mesh and per-branch controllers add cost and complexity that the traffic pattern (96% to hub) does not justify; hub-and-spoke with centralised or cloud-managed controllers would fit better.
C) Physical firewalls are always wrong at branches.
D) 25 users per branch is too few to justify any firewall.

**Correct answer: B.**

**Explanation:** A full mesh of 12 branches needs 66 branch-to-branch paths, almost none of which the traffic justifies when 96% of flows go to the hubs; hub-and-spoke (or an SD-WAN overlay with dynamic tunnels) matches the actual pattern. Per-branch wifi controllers similarly multiply cost and management burden that a centralised or cloud-managed model avoids for 25-user sites. A is wrong - if anything the design is over-engineered, not under-redundant. C and D are absolutes that no evidence supports; branch firewalls may be right in some designs. Reviewing others' designs for "efficient use of resources" means matching architecture to evidence, and cognitive tests probe whether you can pick the finding that follows from the data given rather than from dogma.

**Question 13 (moderate) - Odd one out in technology grouping**

Which of the following is the odd one out as a category?

A) Software-defined WAN
B) Data-centre LAN
C) Service level agreement
D) Unified communications

**Correct answer: C.**

**Explanation:** Options A, B and D are network technology domains you are expected to understand at this role level. A service level agreement is a commercial and contractual construct - something you agree with third party vendors - not a technology. Classification questions like this appear simple, but under time pressure candidates often pick D because "communications" feels less network-like than the others. Slow down for two seconds and sort by kind (technology versus contract), not by surface familiarity.

**Question 14 (hard) - Problem solving within change windows**

Your change policy allows network changes only in these windows: Tuesday 22:00-02:00 and Saturday 20:00-06:00. A WAN migration needs three sequential steps: Step 1 takes 3 hours; Step 2 takes 5 hours and must start within 48 hours of Step 1 finishing; Step 3 takes 2 hours and must complete within 24 hours of Step 2 finishing. Steps cannot be split across windows.

Which plan works?

A) Step 1 Tuesday window, Step 2 Saturday window, Step 3 the following Tuesday window.
B) Steps 1 and 2 in one Saturday window, Step 3 the following Tuesday window.
C) Step 1 Saturday window, Step 2 the following Tuesday window, Step 3 the same Tuesday window.
D) All three steps in a single Saturday window, run sequentially.

**Correct answer: D.**

**Explanation:** Check the durations against the windows first. The Tuesday window is 4 hours long, so Step 2 (5 hours) can never run on a Tuesday - that eliminates A and C immediately. Option B fits Steps 1 and 2 into Saturday's 10-hour window (3 + 5 = 8 hours), but then Step 3 must complete within 24 hours of Step 2 finishing; the next Tuesday window opens roughly three days later, far outside 24 hours - eliminated. Option D: all three steps total 3 + 5 + 2 = 10 hours, exactly filling the Saturday 20:00-06:00 window; run sequentially, every constraint is met - Step 2 starts immediately after Step 1 (well within 48 hours) and Step 3 completes immediately after Step 2 (well within 24 hours). The exam skill is elimination by hardest constraint first (Step 2's length), then verifying the survivor completely, including the tight 10-hours-in-10-hours fit. The workplace skill is identical: when you plan and co-ordinate implementation activities, the binding constraint is usually one step's duration against one window, and finding it early saves redesigning the whole schedule later.

### Preparation tips

- **Practise with your own artefacts.** Take a real (suitably anonymised) design document and actively hunt for internal contradictions, unstated assumptions, and standard breaches. Ten minutes of deliberate error-hunting a day builds exactly the muscle these tests measure.
- **Verbalise your deductions.** When troubleshooting, narrate the elimination: "It cannot be the WAN because... it cannot be the LAN because...". Assessments reward systematic elimination, and narrating makes it habitual.
- **Rehearse dependency ordering.** Sketch build sequences for a small integration and check each step's prerequisites. Question formats like Question 4 become fast and easy once dependency-checking is automatic.
- **Time yourself.** Do practice sets at roughly one minute per question. Accuracy under time pressure improves quickly with rehearsal, and the interface familiarity alone removes a layer of stress.
- **Read the boundary conditions.** "Exceeds 90%" is not "reaches 90%"; "before procurement" is not "before build". Many wrong answers are right answers to a slightly different question.

### Common pitfalls

- **Answering from experience instead of the question.** You know more about networks than any test scenario contains - but the correct answer must follow from the facts given. If the scenario says nothing about redundancy, do not deduct marks for it in your head.
- **Grabbing the smallest number or the strongest word.** In SLA-style logic questions, qualifiers (business hours only, data-centre only) change the answer. Read every clause.
- **Time sink questions.** If a hard deduction is eating your clock, flag it, answer the easier ones, and return. A cognitive test scores total correct answers, not heroism on one item.
- **Confusing "could be true" with "must be true".** Under pressure, plausible inferences feel proven. Check whether the text forces the conclusion.
- **Skipping the practice questions on the platform.** They are ungraded and exist to remove interface surprises. Never skip them.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make logical decisions using numerical data drawn from the real demands of your role. It is business mathematics, not abstract algebra: the inputs are tables, charts, budgets, capacity figures and performance metrics, and the operations are percentages, ratios, rates, conversions, and cost-benefit estimations. Most assessments allow or provide an onscreen calculator, because they prioritise interpretation over mental arithmetic - the skill being measured is extracting the right numbers and combining them correctly, quickly, under a strict time limit.

For a network architect, numbers are everywhere. You agree SLAs with third party vendors, which means converting availability percentages into minutes of allowable downtime and checking penalty clauses. You plan and co-ordinate programme activities, which means budgets, day rates, and schedule arithmetic. You design LAN, WAN, wifi and cloud networks, which means bandwidth, throughput, capacity headroom, growth projections, port counts, and licensing. You review others' designs for efficient use of resources, which is often a numbers-versus-requirements comparison. This assessment measures whether you can do that quickly and accurately.

### What it measures for your role

- **Capacity and utilisation arithmetic** maps to your **IT infrastructure** skill: bandwidth, throughput, port counts, wireless client densities, and data-centre LAN sizing.
- **SLA and availability calculations** map to your duty to **agree SLAs and engage with third party vendors**: converting "nines" into downtime minutes, calculating service credits, and comparing vendor offers.
- **Budget and cost comparison** maps to your programme duties: comparing total cost across options, tracking spend against forecast, and evaluating cloud versus on-premises costs in **systems design** reviews.
- **Growth projection and trend interpretation** maps to **systems design**: designing for medium-term demand rather than today's snapshot.
- **Test and defect metrics** map to **systems integration**: reading integration test pass rates and defect discovery trends to judge readiness.

### Practice questions

**Question 1 (easy) - Availability into downtime**

A vendor offers an SLA of 99.9% availability for a WAN service, measured monthly. Assume a 30-day month.

How many minutes of downtime per month does 99.9% permit?

A) 14.4 minutes
B) 43.2 minutes
C) 72 minutes
D) 4.32 minutes

**Correct answer: B.**

**Explanation:** A 30-day month contains 30 × 24 × 60 = 43,200 minutes. Allowable downtime is the unavailable fraction: 100% − 99.9% = 0.1% = 0.001. Then 43,200 × 0.001 = 43.2 minutes. Option A (14.4) is what you get if you mistakenly use 0.0333% (a "three nines plus" confusion with 99.99% at 4.32 minutes, option D). Knowing instantly that 99.9% monthly means roughly three-quarters of an hour of permitted downtime is bread-and-butter for agreeing SLAs - and for explaining to stakeholders why "99.9% sounds high" does not mean "never down".

**Question 2 (easy) - Percentage utilisation headroom**

A 10 Gbps data-centre LAN uplink currently peaks at 6.8 Gbps. Your design standard requires that peak utilisation stay below 70% of link capacity.

By how much (in Gbps) does the current peak exceed the standard's threshold?

A) It does not exceed it
B) 0.2 Gbps
C) 0.8 Gbps
D) 1.2 Gbps

**Correct answer: A - but only just.**

**Explanation:** Careful: the threshold is 70% of 10 Gbps = 7.0 Gbps. The current peak of 6.8 Gbps is below 7.0 Gbps, so the standard is not yet breached; there is 0.2 Gbps of headroom remaining (which is what option B represents - the margin, not an excess). Numeric tests often plant the "reverse" answer among the options. Read the question stem twice: it asks by how much the peak exceeds the threshold, and the correct response is that it does not. In a real design review you would still flag that 68% utilisation against a 70% standard means an upgrade decision is imminent.

**Question 3 (moderate) - Growth projection to a breach date**

That same uplink's peak grows by 0.4 Gbps per quarter. It currently peaks at 6.8 Gbps against the 7.0 Gbps (70%) design threshold.

In how many quarters will the peak first exceed the 70% threshold?

A) 1 quarter
B) 2 quarters
C) 3 quarters
D) 4 quarters

**Correct answer: A.**

**Explanation:** After one quarter: 6.8 + 0.4 = 7.2 Gbps, which exceeds 7.0 Gbps. So the threshold is breached after just one quarter. The arithmetic is trivial; the value of the question is the planning insight - procurement and change lead times for WAN and data-centre upgrades are often longer than a quarter, so "one quarter to breach" means the upgrade activity needed to start already. Assessments pair small numbers with realistic consequences to check you interpret, not just calculate.

**Question 4 (moderate) - Vendor cost comparison over a contract term**

You are comparing two third party vendor offers for managed SD-WAN across 40 sites over 3 years:

- Vendor A: £180 per site per month, plus a one-off transition charge of £45,000.
- Vendor B: £205 per site per month, with no transition charge.

Which vendor is cheaper over the full 3-year term, and by how much?

A) Vendor A, by £27,000
B) Vendor B, by £9,000
C) Vendor A, by £72,000
D) Vendor B, by £27,000

**Correct answer: B.**

**Explanation:** Compute both totals in full. Months in 3 years: 36. Vendor A: £180 × 40 sites = £7,200 per month; £7,200 × 36 = £259,200; plus the £45,000 transition charge gives £304,200. Vendor B: £205 × 40 = £8,200 per month; £8,200 × 36 = £295,200, with nothing to add. Difference: £304,200 − £295,200 = £9,000 in Vendor B's favour. The trap is anchoring on Vendor A's lower monthly rate. The £25 per-site monthly saving is £1,000 per month, which over 36 months recovers £36,000 - less than the £45,000 transition charge, so the cheaper rate never pays back within the term. This mirrors the most common real-world error in vendor comparisons: comparing rates instead of whole-term totals. Always total every cost component over the same period before deciding - and in a live negotiation, you would also test what happens if the contract extends to year 4, where Vendor A would eventually pull ahead.

**Question 5 (moderate) - Service credit calculation**

Your SLA with a vendor states: if monthly availability falls below 99.5%, the vendor pays a service credit of 5% of the monthly charge for each full 0.1 percentage point below the target, capped at 25%. The monthly charge is £22,000. This month, availability was 99.13%.

What service credit is due?

A) £1,100
B) £3,300
C) £4,070
D) £5,500

**Correct answer: B.**

**Explanation:** The shortfall is 99.5% − 99.13% = 0.37 percentage points. Only full 0.1-point steps count: 0.37 contains three full steps (0.3), not four. Credit = 3 × 5% = 15% of £22,000 = £3,300. Option C (£4,070) comes from applying 18.5% (treating 0.37 as 3.7 steps), and D from rounding 0.37 up to 0.4. The lesson for your vendor engagement duty: credit mechanisms hinge on exact wording like "each full 0.1 percentage point", and the arithmetic must follow the words. In negotiations, you would also note the 25% cap means credits stop growing once availability drops 0.5 points below target - a real design consideration when judging whether an SLA genuinely protects the business.

**Question 6 (moderate) - Wireless capacity ratio**

A new office floor will seat 360 staff. Your wifi design standard assumes 2.2 devices per person and a maximum of 55 devices per access point for acceptable performance.

How many access points does the floor need, at minimum?

A) 14
B) 15
C) 16
D) 18

**Correct answer: B.**

**Explanation:** Total devices: 360 × 2.2 = 792. Access points: 792 ÷ 55 = 14.4. You cannot deploy 0.4 of an access point, and 14 APs would carry 14 × 55 = 770 devices - 22 short. So round up to 15. Option A is the round-down trap; D pads without justification. Capacity questions in numeric tests almost always include a rounding decision, and for infrastructure the rule is: capacity requirements round up. In a real design you would then add coverage (not just capacity) analysis and growth headroom, but the question only asks for the standard's minimum - answer what is asked.

**Question 7 (moderate) - Programme budget burn rate**

Your network transformation programme has a £1.44 million budget for a 12-month delivery. At the end of month 5, spend to date is £684,000.

If spending continues at the same average monthly rate, by approximately how much will the programme overspend or underspend at month 12?

A) Overspend by about £201,600
B) Overspend by about £136,800
C) Underspend by about £115,200
D) Overspend by about £48,000

**Correct answer: A.**

**Explanation:** Average monthly spend so far: £684,000 ÷ 5 = £136,800 per month. Projected 12-month total: £136,800 × 12 = £1,641,600. Against the £1,440,000 budget, that is an overspend of £1,641,600 − £1,440,000 = £201,600. Option B is the monthly rate itself, planted for candidates who stop mid-calculation. As the architect planning, directing and co-ordinating programme activities, this projection is the moment to act - rescoping, re-phasing, or seeking approval - seven months before the overspend materialises, not after.

**Question 8 (moderate) - Integration test pass rates**

Integration testing for a new data-centre network reports the following across three test cycles:

| Cycle | Tests run | Tests passed |
|-------|-----------|--------------|
| 1     | 240       | 168          |
| 2     | 240       | 204          |
| 3     | 260       | 234          |

What was the percentage-point improvement in pass rate between cycle 1 and cycle 3?

A) 15 percentage points
B) 20 percentage points
C) 66 percentage points
D) 90 percentage points

**Correct answer: B.**

**Explanation:** Cycle 1 pass rate: 168 ÷ 240 = 0.70 = 70%. Cycle 3: 234 ÷ 260 = 0.90 = 90%. Improvement: 90 − 70 = 20 percentage points. Note the units: percentage points, not percent change (the relative change would be 20 ÷ 70 ≈ 28.6%). Option D is the cycle 3 rate alone; option C is a decoy for misreading. Supporting integration testing activities is part of your systems integration skill, and distinguishing percentage points from percent change matters whenever you report test progress to a programme board - the two figures tell different stories from the same data.

**Question 9 (hard) - Cloud versus on-premises cost model**

You are evaluating moving a service's network egress from an on-premises data centre to a cloud platform.

- On-premises: fixed circuit cost £8,400 per month, handling up to 500 TB per month (no per-TB charge).
- Cloud: no fixed cost, but egress charged at £35 per TB for the first 100 TB each month and £22 per TB beyond that.

At a monthly volume of 300 TB, which option is cheaper, and by how much per month?

A) Cloud, by £500
B) On-premises, by £500
C) On-premises, by £2,900
D) Cloud, by £1,100

**Correct answer: A.**

**Explanation:** Cloud cost at 300 TB uses tiered pricing: the first 100 TB at £35 = £3,500; the remaining 200 TB at £22 = £4,400; total £3,500 + £4,400 = £7,900. On-premises is a flat £8,400. Difference: £8,400 − £7,900 = £500 in the cloud option's favour. Option C (£2,900) is the trap for pricing all 300 TB at £35 (£10,500 − wrong tier handling would then be compared incorrectly); option B tests whether you kept the direction of the comparison straight - when two options differ only in direction, recompute rather than trusting your first pass. Tiered pricing is exactly how cloud network egress is billed, so this structure will feel familiar. Note the break-even insight worth raising in a real design review: each additional TB beyond 300 costs the cloud option £22 while on-premises stays flat up to 500 TB, so at roughly 323 TB (£7,900 + 23 × £22 ≈ £8,406) the answer flips. A recommendation that is cheaper today but flips within the growth forecast is precisely the nuance your systems design reviews should surface.

**Question 10 (hard) - Weighted uptime across a composite service**

A business service depends on three network components in series (all must work). Last month their individual availabilities were: WAN 99.95%, data-centre LAN 99.98%, remote access platform 99.90%.

What was the approximate availability of the composite service?

A) 99.95%
B) 99.83%
C) 99.90%
D) 99.98%

**Correct answer: B.**

**Explanation:** Components in series multiply: 0.9995 × 0.9998 × 0.9990. Step by step: 0.9995 × 0.9998 = 0.99930 (approximately). Then 0.99930 × 0.9990 = 0.99830 (approximately) = 99.83%. A quick approximation: add the unavailabilities - 0.05% + 0.02% + 0.10% = 0.17%, so availability ≈ 100% − 0.17% = 99.83%. The traps are picking the best component (D), the worst component (C), or the first (A). This calculation is fundamental to agreeing sensible SLAs: if the business demands 99.9% end to end, no single component target of 99.9% can deliver it when components stack in series - each must be better than the end-to-end goal.

**Question 11 (hard) - Ratio reasoning in traffic engineering**

A WAN link carries three traffic classes in the ratio 5:3:2 (data : voice : video). The link runs at 800 Mbps total. A new video conferencing rollout will double the video traffic while data and voice stay constant.

What will video's share of total traffic be after the rollout?

A) 20%
B) 25%
C) 33.3%
D) 40%

**Correct answer: C.**

**Explanation:** Current split of 800 Mbps in ratio 5:3:2 (total 10 parts): data = 400 Mbps, voice = 240 Mbps, video = 160 Mbps. Doubling video: 320 Mbps. New total: 400 + 240 + 320 = 960 Mbps. Video share: 320 ÷ 960 = 1/3 ≈ 33.3%. The trap is option D: doubling video's share from 20% to 40% ignores that the total also grows. Shares are relative - when one component grows, every share shifts. This matters when you size QoS policies: a class's percentage allocation must be recalculated against the new total, not doubled in place. (You would also note 960 Mbps exceeds 800 Mbps - the link itself needs attention before the rollout.)

**Question 12 (hard) - Multi-step upgrade cost per user**

An office LAN refresh covers 3 floors. Each floor needs 4 access switches at £2,150 each, and the building needs 2 core switches at £9,800 each. Installation labour is quoted at 15% of total hardware cost. The building serves 620 staff.

What is the approximate total cost per member of staff?

A) £71
B) £75
C) £79
D) £84

**Correct answer: D.**

**Explanation:** Take it in stages and write each result down. Hardware: access switches 3 floors × 4 switches × £2,150 = £25,800; core switches 2 × £9,800 = £19,600; hardware total £25,800 + £19,600 = £45,400. Labour: 15% × £45,400 = £6,810. Grand total: £45,400 + £6,810 = £52,210. Per staff member: £52,210 ÷ 620 = £84.21, so approximately £84 - option D. Option B (£75) is the trap for forgetting the labour uplift entirely: £45,400 ÷ 620 = £73.23, which a hurried candidate rounds towards £75. Option A comes from forgetting one floor of access switches. The wider lesson: multi-step cost questions reward writing intermediate results down (per-floor cost, hardware subtotal, labour uplift) - candidates who chain the whole thing mentally introduce compounding errors, and each distractor here corresponds to exactly one missed step. Cost-per-user is also a genuinely useful design-review metric: it lets you compare refresh proposals across buildings of very different sizes on a like-for-like basis.

**Question 13 (moderate) - Reading a utilisation table**

Peak utilisation (% of capacity) across four sites over three months:

| Site       | June | July | August |
|------------|------|------|--------|
| Croydon    | 55   | 61   | 67     |
| Darlington | 72   | 70   | 71     |
| Glasgow    | 48   | 59   | 74     |
| Newport    | 63   | 64   | 66     |

Which site shows the fastest-growing utilisation trend and therefore the most urgent capacity review?

A) Croydon
B) Darlington
C) Glasgow
D) Newport

**Correct answer: C.**

**Explanation:** Compute each site's change from June to August: Croydon +12 points (6 per month, steady); Darlington −1 point (flat, though highest starting level); Glasgow +26 points (48 to 74, accelerating: +11 then +15); Newport +3 points. Glasgow combines the largest rise and an accelerating pattern - at +15 points per month it would pass 89% next month. The distractor is Darlington: its absolute level (71%) is high, but it is stable; the question asks about the fastest-growing trend. In capacity management you watch both level and slope, but read the question stem to see which one is being asked - assessments regularly split those into separate questions to catch skim-readers.

**Question 14 (moderate) - Subnet sizing**

A new site needs a subnet for 500 devices, and your standard requires at least 20% spare address capacity beyond the requirement. Usable host addresses per subnet size: a /24 provides 254, a /23 provides 510, a /22 provides 1,022.

Which is the smallest subnet that meets the standard?

A) /24
B) /23
C) /22
D) None of these

**Correct answer: C.**

**Explanation:** The requirement with 20% headroom is 500 × 1.2 = 600 usable addresses. A /24 (254) fails outright. A /23 (510) covers the 500 devices but not the headroom - 510 < 600, so it fails the standard even though it "works" today. A /22 provides 1,022, comfortably above 600, so C is the smallest compliant choice. The trap is option B, for candidates who check the raw requirement and forget the headroom multiplier; assessments frequently attach a policy percentage to a technical figure precisely to see whether you combine them. In real addressing plans this is also where you balance headroom against address conservation - a /22 for 500 devices is compliant but worth a comment in design review about whether the site will ever grow into it.

**Question 15 (moderate) - Cost of downtime versus mitigation**

A public-facing service loses an estimated £9,500 per hour of network outage. Historical data shows the current single-circuit design causes an average of 6 hours of outage per year. Adding a resilient second circuit costs £14,400 per year and is expected to reduce outage to an average of 1 hour per year.

On these figures, what is the expected net annual benefit of adding the second circuit?

A) £33,100
B) £47,500
C) £42,500
D) £19,900

**Correct answer: A.**

**Explanation:** Outage cost today: 6 × £9,500 = £57,000 per year. With resilience: 1 × £9,500 = £9,500. Gross saving: £57,000 − £9,500 = £47,500 (option B, planted for those who stop early). Net benefit subtracts the mitigation cost: £47,500 − £14,400 = £33,100. Option C forgets that one outage hour remains even after the upgrade; option D miscombines the figures. This is the business case arithmetic behind every resilience recommendation you make: designs that support business strategies must be justified in the business's own currency, and a resilient path that costs less than the downtime it prevents is the cleanest justification there is. Notice, too, how sensitive the case is to the outage estimate - halve the £9,500 and the net benefit drops to £9,350, still positive but far less compelling - which is why assumptions belong in the design document.

**Question 16 (hard) - Licence true-up with growth**

A network management platform is licensed per managed device. You hold 1,200 device licences at £38 each per year. The estate currently has 1,050 managed devices and is growing at 4% per quarter (compound). The vendor charges £48 per year for each device above the licensed count, applied at year end.

Approximately how many devices will exceed the licence count after four quarters, and what excess charge results?

A) About 28 devices, charging about £1,344
B) About 178 devices, charging about £8,544
C) No excess - the estate stays within 1,200
D) About 78 devices, charging about £3,744

**Correct answer: A.**

**Explanation:** Compound 4% growth over four quarters: 1,050 × 1.04 = 1,092; × 1.04 = 1,135.7; × 1.04 = 1,181.1; × 1.04 = 1,228.3 - call it 1,228 devices. Excess over the 1,200 licensed: 1,228 − 1,200 = 28 devices (approximately). Charge: 28 × £48 = £1,344. Option D comes from compounding one quarter too many: a fifth multiplication gives 1,228 × 1.04 ≈ 1,278, an excess of 78 devices and £3,744. Option C is the answer if you stop compounding a quarter early (1,181 < 1,200). Both distractors are off-by-one-period errors - the most common mistake in compound growth questions, so count your multiplications on your fingers if you must. The practical point for vendor engagement: the £48 overage rate is 26% above the £38 list rate, so pre-purchasing roughly 30 additional licences at £38 (£1,140) would cost less than the £1,344 true-up - exactly the kind of small arithmetic that makes you a sharper negotiator when you agree contract terms.

**Question 17 (easy) - Latency budget**

An application team tells you their transaction must complete a network round trip within 120 ms to meet its user experience target. The path crosses three segments with measured round-trip contributions of: campus LAN 4 ms, WAN 62 ms, cloud interconnect 38 ms.

How much latency budget remains for any additional network component on the path?

A) 16 ms
B) 20 ms
C) 26 ms
D) 104 ms

**Correct answer: A.**

**Explanation:** Sum the known contributions: 4 + 62 + 38 = 104 ms. Remaining budget: 120 − 104 = 16 ms. Option D is the subtotal itself, planted for candidates who answer the intermediate step; option B comes from dropping the LAN's 4 ms as negligible - a habit worth breaking, because latency budgets are consumed milliseconds at a time. Latency budgeting is a staple of practical systems design: when you collaborate with engineers on where to place a security inspection point or a proxy, "does its added latency fit the remaining 16 ms?" is often the deciding question, and being able to answer it instantly - in a meeting, without a spreadsheet - is part of what makes a design review move quickly and well.

### Preparation tips

- **Drill the availability table.** Memorise the downtime equivalents: 99% ≈ 7.3 hours/month, 99.5% ≈ 3.65 hours, 99.9% ≈ 43.8 minutes (43.2 on a 30-day month), 99.99% ≈ 4.4 minutes. Instant recall frees time for the harder questions and serves you daily in vendor negotiations.
- **Write down intermediate values.** Multi-step questions (hardware + labour ÷ users) punish mental chaining. Two seconds of jotting prevents thirty seconds of rework.
- **Practise percentage points versus percent change.** Test and utilisation reporting uses both; know which is which and compute each from a small table until it is automatic.
- **Use the on-screen calculator early in practice.** Its ergonomics differ from your phone; familiarity is free marks.
- **Estimate before you calculate.** A rough order-of-magnitude guess (is the answer nearer £50k or £500k?) catches keying errors instantly.

### Common pitfalls

- **Misreading scale qualifiers.** "In thousands", Mbps versus Gbps, monthly versus annual: a single missed unit multiplies your error by 1,000. Read the table header and the axis label every time.
- **Anchoring on the prominent number.** The lower monthly rate is not the lower total cost; the highest utilisation is not the fastest-growing. Compute totals and trends before comparing.
- **Over-calculating.** Where options are far apart, estimation and rounding get you there faster; save precision for near-neighbour options.
- **Time sink questions.** A four-stage cost model can devour five minutes. If it stalls, flag it, bank the quicker questions, and return.
- **Ignoring rounding direction.** Access points, switches, and licences round up; anything that "counts full steps" (like SLA credit bands) rounds down. The words in the question decide the direction - not habit.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. It mirrors the exact reading demands of your role: dense passages built from network standards, SLA clauses, governance policies, vendor emails, assurance reports, and design documents. The defining rule is fact-based logic - you must answer strictly from the text provided, ignoring everything you know from outside it. Most questions require a choice between **True** (the passage states or logically entails it), **False** (the passage contradicts it), or **Cannot Say** (the passage gives insufficient information either way). Some assessments add multiple-choice comprehension questions about the main point or a specific detail. Timing is tight - typically under a minute per question - to simulate workplace deadlines.

Why does this matter for a network architect? Because your role runs on precise reading. An SLA clause that says "response within 30 minutes during business hours" is a different contract from "response within 30 minutes". A governance process that requires review "before procurement" is not one that requires review "before build". A vendor proposal that says a feature is "roadmapped" has not said it exists. When you agree SLAs, develop assurance processes, review design documents, and co-ordinate programme communications, misreading a single qualifier can cost real money and real service outages. This assessment measures the reading precision your duties demand.

### What it measures for your role

- **Extracting rules from policy text** maps to your **governance and assurance** skill: developing, improving, and supporting others in following governance processes requires reading exactly what a process does and does not require.
- **Spotting contractual qualifiers** maps to your duty to **agree SLAs and engage with third party vendors**: scope limits, time windows, exclusions, and remedies live in the wording.
- **Comprehending technical prose** maps to your **IT infrastructure** and **systems design** skills: standards documents, design rationales, and review comments must be understood as written before you assess them.
- **Distinguishing stated fact from implication** maps to your **research** duty: evaluating new technologies and vendor claims means separating what a document proves from what it merely suggests.
- **Reading integration and test reports accurately** maps to your **systems integration** skill: a report's precise claims determine whether a build proceeds.

### Practice questions

**Passage 1 (for Questions 1-4) - Extract from a departmental network standard**

"All new wide area network circuits must be ordered with a minimum bandwidth of 100 Mbps and must present a resilient path where the site is classified as business critical. Sites not classified as business critical may be served by a single circuit, provided that a documented recovery plan exists. Software-defined WAN overlay is the preferred transport for all new sites; exceptions require approval from the technical design authority. Circuits delivered before January 2025 are exempt from the minimum bandwidth requirement until their contract renewal date. Nothing in this standard removes the requirement for all circuits, regardless of age, to comply with the department's encryption policy."

**Question 1 (easy)**

True, False, or Cannot Say: "A new circuit for a business critical site may be delivered without a resilient path if a recovery plan exists."

**Correct answer: False.**

**Explanation:** The passage says circuits "must present a resilient path where the site is classified as business critical" - no exception is offered for business critical sites. The recovery-plan provision applies only to "sites not classified as business critical". The statement contradicts the text, so it is False. The trap is blending two adjacent rules into one; verbal tests constantly check whether you keep each rule attached to its own condition.

**Question 2 (easy)**

True, False, or Cannot Say: "A circuit delivered in 2023 must comply with the encryption policy."

**Correct answer: True.**

**Explanation:** The final sentence states that "all circuits, regardless of age" must comply with the encryption policy, and explicitly says nothing in the standard removes that requirement. A 2023 circuit is a circuit; regardless of age covers it. Note how the passage anticipates the confusion with the bandwidth exemption - older circuits are exempt from the minimum bandwidth until renewal, but not from encryption. Answering True here requires connecting the general rule to the specific case, which the text fully supports.

**Question 3 (moderate)**

True, False, or Cannot Say: "The technical design authority has approved at least one exception to the SD-WAN preference."

**Correct answer: Cannot Say.**

**Explanation:** The passage establishes a mechanism - exceptions require technical design authority approval - but says nothing about whether any exception has ever been requested or granted. The existence of a rule does not tell you it has been exercised. This is the classic Cannot Say pattern: the statement is perfectly consistent with the passage, and also perfectly consistent with its opposite. If you cannot point to wording that proves or contradicts the claim, the answer is Cannot Say.

**Question 4 (moderate)**

True, False, or Cannot Say: "A non-critical site with no documented recovery plan must be served by more than one circuit."

**Correct answer: True.**

**Explanation:** The passage permits a single circuit for non-critical sites only "provided that a documented recovery plan exists". Remove the recovery plan and the permission for a single circuit falls away, leaving the site needing more than one circuit to comply. This is a conditional-logic question: the text grants X only under condition Y; without Y, X is not permitted. Candidates often answer Cannot Say here because the consequence is stated indirectly - but the entailment is strict, and verbal tests at this level expect you to follow one step of implication from an explicit conditional.

**Passage 2 (for Questions 5-8) - Vendor email about an SLA negotiation**

"Thank you for your comments on the draft agreement. We can confirm that the proposed service credits will apply to the managed LAN service and the managed wifi service. Credits for the SD-WAN service remain under commercial review and we hope to confirm our position by the end of the month. Our standard response time for priority 1 incidents is 30 minutes, measured from ticket creation to first meaningful human response; automated acknowledgements do not stop the clock. Please note that response times are measured only where the incident is logged through our service portal. Incidents reported by telephone will be logged by our staff on your behalf, at which point the measurement begins."

**Question 5 (easy)**

True, False, or Cannot Say: "Service credits will apply to the managed wifi service."

**Correct answer: True.**

**Explanation:** The email confirms exactly this: credits "will apply to the managed LAN service and the managed wifi service". Direct statement, direct match. Easy marks like this exist in every test - bank them quickly and spend your saved seconds on the harder inference questions.

**Question 6 (moderate)**

True, False, or Cannot Say: "An automated acknowledgement within 30 minutes satisfies the vendor's priority 1 response commitment."

**Correct answer: False.**

**Explanation:** The email defines response as "first meaningful human response" and states explicitly that "automated acknowledgements do not stop the clock". An automated acknowledgement therefore cannot satisfy the commitment. This is precisely the clause you would fight for when agreeing SLAs - vendors' draft agreements often let an auto-reply stop the clock - and the question tests whether you registered the definitional sentence rather than just the headline "30 minutes".

**Question 7 (hard)**

True, False, or Cannot Say: "If an incident is reported by telephone, the 30-minute measurement begins at the moment of the call."

**Correct answer: False.**

**Explanation:** Read the last sentence closely: telephone incidents "will be logged by our staff on your behalf, at which point the measurement begins". Measurement starts when the vendor's staff log the ticket, not when the call is made. Any delay between your call and their logging is unmeasured - a subtle but commercially significant gap. The statement asserts measurement begins at the moment of the call, which the text contradicts, so it is False. Candidates who answer Cannot Say have spotted the ambiguity of how long logging takes, but the claim as worded is directly contradicted; Cannot Say is for silence, not for contradiction.

**Question 8 (hard)**

True, False, or Cannot Say: "The vendor has refused to offer service credits for the SD-WAN service."

**Correct answer: False.**

**Explanation:** The email says SD-WAN credits "remain under commercial review" with a position to be confirmed by month end. Under review is not a refusal - the email contradicts the claim that a refusal has happened, because it describes the matter as undecided. Careful: many candidates answer Cannot Say, reasoning that the final outcome is unknown. But the statement is about whether a refusal has occurred, and the text's description of an open review contradicts that. Compare with Question 3: there, the text was silent on the fact claimed; here, the text speaks to it and says otherwise. That distinction - silence versus contradiction - is the single most examined skill in True/False/Cannot Say formats.

**Passage 3 (for Questions 9-11) - Extract from a design assurance report**

"The review board assessed the proposed data-centre network design against the department's design standards. The design meets the standards for segregation and management access. The board was unable to assess the resilience claims because the failover test evidence supplied related to a previous software version. The proposed use of a single vendor for switching and firewalls was noted as a commercial risk rather than a technical one, and is a matter for the commercial team. The board recommends conditional approval: build may commence, but no production traffic may be carried until failover evidence from the current software version has been reviewed and accepted."

**Question 9 (moderate)**

True, False, or Cannot Say: "The review board found that the design fails the resilience standard."

**Correct answer: False.**

**Explanation:** The board did not find a failure; it was "unable to assess" resilience because the evidence related to the wrong software version. Not assessed is not failed. The text describes an evidence gap, not a design defect. This mirrors real assurance practice, where the difference between "non-compliant" and "not yet evidenced" determines whether a design is reworked or merely re-tested - and the question checks you preserve that difference under time pressure.

**Question 10 (moderate)**

True, False, or Cannot Say: "Under the board's recommendation, the project may begin building the network before the new failover evidence is accepted."

**Correct answer: True.**

**Explanation:** The recommendation is explicit: "build may commence, but no production traffic may be carried until failover evidence from the current software version has been reviewed and accepted". Building before evidence acceptance is exactly what conditional approval permits; the condition gates production traffic, not build. Verbal questions often hinge on which activity a condition attaches to - the same reading skill as governance Question 5 in the cognitive section, and the same skill you use when you support others in following assurance processes.

**Question 11 (hard)**

True, False, or Cannot Say: "The commercial team has accepted the single-vendor risk."

**Correct answer: Cannot Say.**

**Explanation:** The board classified the single-vendor concern as commercial and referred it - "a matter for the commercial team". Whether that team has considered it, let alone accepted it, is entirely outside the passage. Nothing proves acceptance; nothing contradicts it. Cannot Say. The pull towards True comes from the passage's calm tone ("noted as a commercial risk rather than a technical one"), which can feel like the risk was waved through - but tone is not fact, and referral is not resolution.

**Passage 4 (for Questions 12-14) - Internal briefing on a unified communications migration**

"The programme will migrate 14,000 users from the legacy telephony platform to the cloud unified communications service in four waves. Wave one, covering 2,000 users in the two smallest regions, completed in June with call quality metrics within tolerance. Wave two is scheduled for September and includes the contact centre, which handles calls from vulnerable members of the public. The contact centre cannot tolerate the brief registration outage that affected wave one, and the network team has therefore designed an overlapping registration approach for wave two. Waves three and four will be scheduled once wave two has been reviewed. Mobile solution users will remain on their current service throughout, as the mobile estate is out of scope for this programme."

**Question 12 (easy) - Multiple choice**

What is the main reason the network team designed an overlapping registration approach for wave two?

A) Wave one's call quality metrics were out of tolerance.
B) Wave two includes the contact centre, which cannot tolerate the registration outage seen in wave one.
C) The mobile estate is out of scope.
D) Waves three and four have not yet been scheduled.

**Correct answer: B.**

**Explanation:** The passage links the design decision directly to the contact centre's intolerance of the brief registration outage that affected wave one. Option A contradicts the text (wave one's metrics were within tolerance); C and D are true statements from the passage but irrelevant to the design decision - a classic multiple-choice decoy pattern where true-but-irrelevant options tempt candidates who match words rather than logic.

**Question 13 (moderate)**

True, False, or Cannot Say: "More than 2,000 users will migrate in wave two."

**Correct answer: Cannot Say.**

**Explanation:** The passage gives wave one's size (2,000 users) and the total (14,000), and says wave two includes the contact centre - but it never states wave two's size. The remaining 12,000 users are split across three waves in unknown proportions; wave two could be larger or smaller than 2,000. The temptation to answer True comes from assuming waves grow or that a contact centre is large - outside knowledge and plausible guesswork, exactly what the format forbids.

**Question 14 (moderate)**

True, False, or Cannot Say: "Users of the mobile solution will be migrated in wave four."

**Correct answer: False.**

**Explanation:** The passage states mobile users "will remain on their current service throughout, as the mobile estate is out of scope". Migrating them in wave four would contradict both clauses. This checks scope-reading: out of scope means not in any wave. In programme communications, scope sentences are where misunderstandings breed, and reading them precisely is part of engaging stakeholders well.

**Question 15 (hard) - Multiple choice, inference**

Which statement is best supported by Passage 4 as a whole?

A) The programme is running behind schedule.
B) The programme adapts its technical approach based on evidence from earlier waves.
C) Cloud unified communications is unsuitable for contact centres.
D) The legacy telephony platform will be decommissioned in September.

**Correct answer: B.**

**Explanation:** The passage shows exactly this pattern: wave one surfaced a registration outage; the team designed an overlapping registration approach for wave two in response; waves three and four await wave two's review before scheduling. That is evidence-driven adaptation. A has no support - no dates are described as slipped. C overreaches: the passage says the contact centre cannot tolerate one specific outage, not that the technology is unsuitable; indeed the mitigation implies suitability. D is never stated - decommissioning is not mentioned at all. "Best supported" questions reward the option the whole passage points to, not an option one sentence might permit.

**Passage 5 (for Questions 16-19) - Extract from a cloud network connectivity policy**

"Departmental workloads hosted in public cloud must connect to the departmental network via an approved private interconnect, except where the workload is classified as internet-facing, in which case connection via the departmental internet gateway is permitted. Approved private interconnects are listed in the cloud connectivity catalogue, which is maintained by the network architecture team and reviewed quarterly. Where a project requires an interconnect type not in the catalogue, the project must fund a technical evaluation; interconnect types that pass evaluation will be added to the catalogue at the next quarterly review. Bandwidth on shared interconnects is allocated on request, subject to available capacity, and unused allocations may be reclaimed after 90 days of inactivity. Projects should note that catalogue inclusion indicates technical approval only and does not constitute funding approval, which remains a matter for each project's business case."

**Question 16 (easy)**

True, False, or Cannot Say: "An internet-facing workload in public cloud may connect via the departmental internet gateway."

**Correct answer: True.**

**Explanation:** The exception clause states this directly: internet-facing workloads are excused from the private-interconnect rule, "in which case connection via the departmental internet gateway is permitted". The claim restates the exception almost word for word. When a question looks this easy, check you have matched the right clause to the right subject - then take the mark and move on.

**Question 17 (moderate)**

True, False, or Cannot Say: "If an interconnect type passes technical evaluation, it becomes available for immediate use."

**Correct answer: False.**

**Explanation:** The passage says passing types "will be added to the catalogue at the next quarterly review" - not immediately. Since workloads must use approved interconnects from the catalogue, a type that has passed evaluation but not yet been added is not yet usable under the policy. The statement's word "immediate" is what makes it False; a version saying "eventually becomes available" would be True. Single-word precision of this kind is exactly what distinguishes verbal reasoning at this level, and exactly what you apply when drafting governance documents - as the author of assurance processes, you would also spot the operational consequence: a project could wait up to a quarter, which may be worth an expedite mechanism.

**Question 18 (moderate)**

True, False, or Cannot Say: "A bandwidth allocation unused for 60 days will be reclaimed."

**Correct answer: False.**

**Explanation:** Two separate checks both fail the claim. First, the threshold: reclamation applies "after 90 days of inactivity", and 60 days is short of that, so a 60-day-idle allocation is not yet eligible - the text contradicts reclamation at 60 days. Second, even at 90 days the passage says allocations "may be reclaimed", not "will be" - reclamation is discretionary, not automatic. The claim fails on the number alone, which is sufficient for False. Candidates who spot only the may/will distinction sometimes answer Cannot Say; but the 60-versus-90 contradiction is decisive. When two defects exist, the direct contradiction wins the classification.

**Question 19 (hard)**

True, False, or Cannot Say: "A project whose interconnect type is in the catalogue has secured the funding needed to use it."

**Correct answer: False.**

**Explanation:** The final sentence anticipates precisely this misreading: "catalogue inclusion indicates technical approval only and does not constitute funding approval, which remains a matter for each project's business case". The claim asserts that catalogue presence secures funding; the text explicitly severs the two. This is the pattern to watch for in policy documents - a sentence added specifically because readers kept conflating two approvals - and it appears in verbal tests because real-world governance failures so often stem from exactly this conflation. As someone who develops governance processes, note the drafting lesson too: the clearest policies name the misreading they are preventing.

**Question 20 (moderate) - Multiple choice on Passage 5**

According to the passage, which statement accurately describes the cloud connectivity catalogue?

A) It is maintained by each project and reviewed annually.
B) It lists approved private interconnects, is maintained by the network architecture team, and is reviewed quarterly.
C) It lists all interconnect types that have ever been evaluated, whether or not they passed.
D) It records the bandwidth allocations granted on shared interconnects.

**Correct answer: B.**

**Explanation:** Option B assembles three facts stated directly in the second sentence: the catalogue lists approved private interconnects, the network architecture team maintains it, and it is reviewed quarterly. Option A inverts both facts (wrong maintainer, wrong review cycle). Option C overreaches: the passage says types that pass evaluation are added; it never says failed evaluations are recorded there - and note that even for passed types, only those added at a quarterly review are present, so "ever been evaluated" is doubly wrong. Option D confuses the catalogue with bandwidth administration, which the passage treats as a separate request-based process. Composite multiple-choice questions like this reward candidates who verify each clause of the option against the text - one wrong clause sinks the whole option, however accurate the rest of it is. That is also a useful habit when you review design documents: a paragraph that is 80% correct still needs the 20% flagged, because downstream readers will treat the whole paragraph as approved. As the team that would own such a catalogue in real life, you might also notice what the passage leaves unspecified - who may request an evaluation, and what happens to interconnects removed from the catalogue - the kind of gap analysis that turns careful reading into better governance drafting.

### Preparation tips

- **Read the question before re-reading the passage.** Skim the passage once for structure, then let each question send you back to the exact sentence. Hunting with a purpose is faster than memorising.
- **Underline qualifiers mentally.** Words like "only", "unless", "provided that", "regardless of", "at which point" carry the whole meaning of contractual and policy text. Train yourself to slow down for half a second on each one.
- **Master the silence/contradiction distinction.** Cannot Say means the text is silent; False means the text speaks and disagrees. Rehearse with pairs like Questions 3 and 8 above until the difference is instinctive.
- **Practise with your real documents.** Take an SLA schedule or a design standard from work, write five True/False/Cannot Say statements about it, and check them against the wording. This doubles as genuinely useful contract review practice.
- **Keep your expertise on a leash.** You know how SD-WAN and failover really behave; the test only cares what the passage says. If your knowledge and the passage conflict, the passage wins.
- **Build a two-pass rhythm.** First pass: answer everything you can prove in under a minute each. Second pass: return to the flagged items with your remaining time. Verbal tests distribute easy and hard questions unevenly across passages, so committing to one pass in strict order almost always strands easy marks at the end of the paper.

### Common pitfalls

- **Bringing in outside knowledge.** The most common error for experienced professionals. The passage is the entire universe; a technically true statement is still Cannot Say if the text does not support it.
- **Confusing likelihood with fact.** "We hope to confirm by month end" is not a confirmation; "under review" is not a decision; "roadmapped" is not delivered. Treat stated intentions as intentions only.
- **Blending adjacent rules.** Conditions attach to specific clauses. The recovery-plan provision for non-critical sites does not soften the resilience rule for critical sites.
- **Answering the gist instead of the words.** A calm tone about a risk does not mean the risk was accepted; a positive-sounding report can still deny approval. Point to the sentence that proves your answer before you commit.
- **Poor time management.** Spending three minutes perfecting one Cannot Say while four easy True questions go unanswered is a net loss. Move, bank, return.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct through realistic workplace dilemmas. Unlike logic or numeric tests, there is often no single objectively right answer: several responses may seem reasonable, but one aligns best with the organisation's values and the demands of the role. You will typically be asked to pick the **most effective** and **least effective** responses, or to rank or rate all the options from best to worst. Timing is usually generous or untimed, because the assessment is measuring your natural judgement rather than your speed.

For a network architect in UK government, the values behind the scoring key are well documented: put user needs first, work in the open and be transparent, collaborate across disciplines, take accessibility and inclusion seriously, spend public money responsibly, and manage risk honestly rather than hiding it. Your role profile supplies the cast of characters: the engineers you collaborate with to ensure systems are practically designed, the associate network architects you coach and mentor, the third party vendors you hold to SLAs, the stakeholders you engage while planning and co-ordinating a programme, and the governance and assurance processes you develop and support others in following. Every scenario below is built from those relationships.

### What it measures for your role

- **Stakeholder engagement and programme judgement** maps to your duty to **plan, direct and co-ordinate activities, engaging with other stakeholders**: balancing pace, transparency, and consultation.
- **Vendor management judgement** maps to **agree SLAs and engage with third party vendors**: firmness on contracts without burning relationships, and honesty about commercial risk.
- **Coaching judgement** maps to **coach and mentor associate network architects**: growing people rather than doing their work for them, and correcting without undermining.
- **Collaboration with engineers** maps to **collaborate with engineers to ensure systems are practically designed**: valuing build and operations expertise instead of designing in an ivory tower.
- **Integrity in governance** maps to your **governance and assurance** skill: following the processes you expect others to follow, even under delivery pressure.

### Practice questions

**Question 1 (moderate) - The tempting shortcut**

Your programme board wants a new remote access solution live in six weeks to support a policy announcement. The governance process you helped develop requires security architecture board review before procurement, and the next board slot is in three weeks. The programme director asks you to "just start procurement now and get the review done retrospectively - you wrote the process, so you can flex it."

Rate the responses:

A) Agree - as the process author you can grant yourself an exception this once.
B) Refuse and tell the programme director the launch will simply have to move.
C) Explain why the review protects the programme, ask the board chair for an expedited or out-of-committee review given the deadline, and update the director on the realistic path.
D) Start procurement quietly without telling the security architecture board, planning to present it as a done deal.

**Most effective: C. Least effective: D.**

**Explanation:** C upholds the process while solving the director's actual problem: most assurance boards have an exception or expedited route, and pursuing it openly demonstrates both integrity and delivery focus - transparency and collaboration in action. A corrodes the credibility of a process you are supposed to champion; if the author flexes it under pressure, nobody else will follow it, which directly undermines your duty to support others in applying governance. B protects the process but abandons the stakeholder - it treats governance as a wall rather than a service, and skips the obvious middle path. D is the worst: it combines the governance breach of A with concealment, destroying trust with the security team and exposing the programme to unmanaged risk. In public sector scoring keys, concealment options are almost always the least effective.

**Question 2 (moderate) - The struggling associate**

An associate network architect you mentor has produced their first solo LAN design for a small office. Reviewing it the day before their design review, you find several errors: an addressing clash with an existing site and a missing management VLAN. The associate has worked hard and is visibly nervous about the review.

Rate the responses:

A) Rewrite the design yourself tonight so it passes, and tell them what you changed afterwards.
B) Walk through the errors with them now, ask questions that help them find the fixes themselves, and let them decide whether to fix tonight or ask to reschedule the review.
C) Say nothing - the review board will find the errors, and failing publicly is how people learn.
D) Tell them the design is fine to spare their nerves.

**Most effective: B. Least effective: D.**

**Explanation:** B is coaching as your role defines it: the associate keeps ownership, learns to spot the error classes (clash-checking against the address plan, standard VLAN complement), and practises a professional judgement call about readiness. A fixes the artefact but not the architect - they learn that you will rescue them, and the review board assesses work that is not theirs, which is quietly dishonest. C confuses accountability with ambush; letting a mentee walk into a preventable public failure when you had the information is a mentoring failure and wastes the board's time. D is worst because it is actively false: it guarantees the failure of C while adding a betrayal of trust when they discover you knew. Effective coaching options in SJTs consistently combine honesty, ownership retention, and support - look for the option that does all three.

**Question 3 (hard) - The vendor's missed SLAs**

A third party vendor has missed its priority 1 response SLA three times this quarter. Their account manager, with whom you have an excellent relationship, asks you over coffee to "log those three as priority 2 retrospectively - the service credits will trigger a contract review and that helps nobody."

Rate the responses:

A) Agree - the relationship is worth more than three service credits, and the incidents are resolved anyway.
B) Decline, apply the credits per the contract, and separately offer a service review meeting to address the underlying causes of the missed responses.
C) Decline and immediately escalate to terminate the contract for the pattern of failures.
D) Say you will think about it, then quietly ask your service desk whether reclassification is technically possible.

**Most effective: B. Least effective: A (with D close behind).**

**Explanation:** B separates the two things that must be separated: contractual facts (the incidents were priority 1; the credits are due; public money and accurate records are involved) and the relationship (a service review is the constructive channel for fixing root causes). This is exactly what engaging with third party vendors and agreeing SLAs means in practice - the SLA only protects the department if it is enforced accurately. A falsifies service records to benefit a supplier: an integrity breach with public funds, and the least effective by a distance. D is nearly as bad - it treats the falsification as an open question and involves more staff in it. C is disproportionate: three missed responses warrant credits and a review, not immediate termination, and jumping to the most aggressive option scores poorly because it ignores remediation steps and the cost of re-procurement. SJT keys reward proportionate escalation ladders.

**Question 4 (moderate) - The impractical design**

You have produced an elegant data-centre network design using a software-defined approach. In the build-planning session, a senior network engineer says bluntly: "This will be a nightmare to operate - we have no tooling or training for this platform, and at 3 a.m. during an incident nobody will understand it."

Rate the responses:

A) Thank them, and explore the concern: what tooling, training, and operational documentation would make the design supportable, and does the timeline allow it - adjusting the design if not.
B) Explain that the design meets the standards and passed assurance review, so operability is the operations team's problem to solve.
C) Withdraw the software-defined approach immediately and revert to the legacy pattern the engineers know.
D) Escalate to the engineer's manager that they are blocking the programme.

**Most effective: A. Least effective: D.**

**Explanation:** Your role profile is explicit: collaborate with engineers to ensure systems are practically designed. A treats operability as a first-class design requirement - which it is - and turns the objection into a concrete gap analysis (tooling, training, documentation, timeline) with a real possibility of design change. That is collaboration, not capitulation. B is the ivory-tower answer the role profile exists to prevent; a design that cannot be operated at 3 a.m. does not meet user needs, whatever the assurance paperwork says. C overcorrects: abandoning a strategically chosen technology at the first objection wastes its benefits and treats the engineer's concern as a veto rather than an input - the concern was supportability, not the technology itself. D punishes candour, which teaches every engineer to stay silent in future reviews; options that suppress professional challenge are reliably scored least effective in public sector SJTs.

**Question 5 (hard) - The discovered assurance gap**

While preparing an unrelated document, you discover that a network change you approved two months ago was implemented without the firewall rule review the assurance process requires. The service has run without incident since. Nobody else has noticed.

Rate the responses:

A) Do nothing - the service is stable, and raising it now only creates paperwork and embarrassment.
B) Quietly ask a friendly engineer to review the rules informally, and log nothing.
C) Log the gap through the proper route, arrange the missed review promptly, and check whether the process needs a control to stop approvals proceeding without the review step.
D) Log the gap and suspend the service until the review is complete.

**Most effective: C. Least effective: A.**

**Explanation:** C does three things the scoring key wants: transparency (the gap goes on the record), risk management (the review actually happens, promptly), and process improvement (your governance and assurance skill includes identifying and recommending improvements - a missed step that nobody caught for two months is a process weakness, not just a one-off). A is the least effective: it leaves an unreviewed firewall change in production and normalises concealment; "stable so far" is not evidence of security. B gets the technical review but sacrifices the record - assurance that is not documented does not exist, and it implicates a colleague in the informality. D is honest but disproportionate: suspending a stable service inflicts certain user harm to mitigate an unquantified risk; proportionate sequencing (review fast, act on findings) serves users better. The pattern to learn: transparent, proportionate, improvement-minded options beat both concealment and overreaction.

**Question 6 (moderate) - Competing stakeholders in a programme**

You are co-ordinating a WAN migration programme. The finance director wants sites migrated in order of circuit cost savings; the operations director wants the troublesome sites with the worst incident records done first; and the accessibility lead reminds you that two sites host assistive-technology services that cannot tolerate the standard cutover window.

Rate the responses:

A) Follow the finance ordering - money talks, and finance funds the programme.
B) Build a sequencing proposal that weighs savings and incident pain, explicitly plans non-standard cutovers for the two assistive-technology sites, and take it back to all three stakeholders for agreement.
C) Let the three stakeholders fight it out and implement whatever emerges.
D) Sequence by cost savings but promise the accessibility lead you will "take extra care" during the standard windows at their two sites.

**Most effective: B. Least effective: D.**

**Explanation:** B is programme co-ordination as the role demands: it synthesises competing legitimate interests into a transparent proposal and secures agreement rather than imposing or abdicating. Crucially, it treats the accessibility constraint as a hard requirement with a concrete plan (non-standard cutover), not a sentiment. D is the least effective - and deliberately seductive - because it sounds accommodating while actually overriding an accessibility need with a vague reassurance; users of assistive technology would bear the consequence, which directly violates inclusion values. A ignores two stakeholders entirely; single-lens optimisation is poor engagement even when the lens is money. C abdicates the co-ordination role you hold; "letting stakeholders fight" delays the programme and usually rewards the loudest voice rather than the strongest case. Watch for D-style options in real SJTs: warm words attached to no changed action.

**Question 7 (moderate) - The unproven technology**

You are researching solutions for a new branch connectivity requirement. A vendor demonstrates an impressive new SD-WAN feature that would simplify your design significantly. It was released three weeks ago, has no public sector reference customers, and the vendor offers you a 40% discount to become the flagship early adopter, announcing at their conference.

Rate the responses:

A) Adopt it - the discount saves public money and the design simplification is real.
B) Reject it and never revisit - government should not take technology risks.
C) Evaluate it through your assurance process: define the risk appetite for this service, run a bounded pilot or reference-site trial, and make adoption conditional on the evidence - while treating the discount and announcement as separate commercial questions to weigh transparently.
D) Adopt it for all sites but keep the old solution's licences as a fallback, doubling the licence spend quietly.

**Most effective: C. Least effective: A.**

**Explanation:** Your role explicitly pairs "research new technologies and solutions" with "ensure appropriate levels of assurance" - C is that pairing made concrete. A bounded pilot converts an unknown risk into evidence; separating the technical decision from the discount and the marketing announcement prevents commercial sweeteners from steering an architecture choice - a transparency essential when spending public money. A is least effective because it accepts an unproven, three-week-old product estate-wide on the strength of a discount; if it fails, the discount is irrelevant and branch connectivity - a live public service dependency - suffers. D hedges by hiding a doubled cost, failing both value-for-money and openness. B fails differently: blanket risk-refusal is not assurance, it is stagnation, and it abandons the research duty. The key rewards evidence-based, transparent, appetite-aware adoption - neither recklessness nor reflexive refusal.

**Question 8 (hard) - Credit for the design**

At a programme showcase, the programme director publicly credits you for the resilient network design that kept services running through a recent power incident. In fact, the failover element that worked was designed by an associate network architect you mentor, building on your review comments. The associate is in the audience.

Rate the responses:

A) Accept the praise gracefully - as their mentor, their work is partly yours anyway.
B) Publicly correct the record on the spot: name the associate as the designer of the failover element and describe your role as reviewer.
C) Say nothing publicly, but tell the associate afterwards that you know it was really their work.
D) Accept the praise, then privately email the director later mentioning the associate "also contributed".

**Most effective: B. Least effective: A.**

**Explanation:** B costs you a moment of mild awkwardness and gains almost everything: the associate receives accurate public recognition (powerful for the career of someone you are charged with developing), the record is truthful, and everyone watching learns that credit flows accurately in your team - which encourages honest attribution across the profession. A is least effective: absorbing a mentee's credit inverts the mentoring relationship and, done in front of them, teaches them that seniority appropriates work. C acknowledges privately what you allowed to be misstated publicly - the associate still watches you keep their credit. D is a weak half-measure: "also contributed" understates their role and the correction reaches one person instead of the audience that heard the error. SJT keys in collaborative cultures consistently reward accurate, generous, public attribution; be alert to options that let you keep unearned credit while feeling honest.

**Question 9 (moderate) - The 3 a.m. escalation**

You are woken at 3 a.m.: a data-centre LAN fault has taken down a public-facing service. The on-call engineer has isolated the fault to a switch pair you designed and asks whether to fail over to the secondary path - but admits they are not confident the secondary path was ever tested end to end. Restoring service quickly matters; so does not making things worse.

Rate the responses:

A) Tell them to fail over immediately - the secondary path exists for exactly this.
B) Ask two or three sharp diagnostic questions (what exactly failed, what does monitoring show on the secondary path, can a single low-risk service be failed over first), then agree a stepped plan with a rollback point, staying on the call.
C) Tell them to wait until the morning team can review the design documents.
D) Tell them it is an operational decision and go back to sleep.

**Most effective: B. Least effective: D.**

**Explanation:** B applies your troubleshooting and problem resolution skill exactly as the framework describes it - break the problem into component parts, verify before acting - while respecting operational urgency: a stepped failover with a rollback point restores service progressively without betting everything on an untested path. Staying on the call is the collaboration your role owes engineers at the worst hour. A gambles a degraded-but-diagnosable situation on an untested path; if the secondary fails differently, you now have two faults and a longer outage. C leaves a public service down for hours to gain document-reading comfort - users first means acting, carefully, now. D is least effective: the designer of the affected system declining to help at the moment their knowledge matters most is an abdication that no scoring key forgives. Afterwards, the honest follow-up is to fix the real root cause: an untested failover path is an assurance gap you log and remedy.

**Question 10 (hard) - The optimistic report**

Your programme manager drafts a highlight report for the senior responsible owner stating the network workstream is "green: integration testing on track". In fact, integration testing is 40% behind plan because a vendor's test environment was delivered late; you believe the time can be recovered, but only if the next fortnight goes perfectly.

Rate the responses:

A) Let the report go out - you genuinely believe you will recover, and amber ratings attract unhelpful attention.
B) Ask the programme manager to report amber with a clear recovery plan, the vendor delay named as cause, and the conditions under which it returns to green.
C) Email the senior responsible owner directly contradicting the programme manager's report.
D) Insist on red, since testing is objectively behind plan.

**Most effective: B. Least effective: A.**

**Explanation:** B tells the truth in the format governance exists for: amber-with-recovery-plan is precisely the honest state ("behind, recoverable, here are the conditions"), it names the vendor cause factually - relevant to your SLA and vendor engagement duties - and it routes through the programme manager, correcting the report rather than the person. A is the classic watermelon report (green outside, red inside) and the least effective: if the fortnight goes imperfectly, the SRO discovers both a slip and a concealment, and your assurance credibility funds the difference. Transparency about delivery status is a core public sector value precisely because early honesty enables early help - an SRO can lean on the vendor now, not after failure. C bypasses and publicly undermines a colleague when a direct conversation had not yet been tried; escalation is for when correction fails, not before. D overstates as much as A understates - false alarms erode trust in the ratings just as false greens do. Accurate, routed, plan-backed reporting wins.

**Question 11 (moderate) - The exclusionary meeting pattern**

You run a weekly design authority meeting. A talented engineer who uses a screen reader tells you privately that the meeting is hard to participate in: diagrams are pasted as images with no description, decisions are made by pointing at screens, and papers arrive minutes before the meeting.

Rate the responses:

A) Thank them, and change the meeting's working pattern: papers and diagrams circulated in advance in accessible formats, verbal description of visuals as standard practice, decisions recorded in text - and ask them whether the changes work.
B) Offer to give them a personal summary after each meeting.
C) Suggest they raise it with HR as a workplace adjustment request.
D) Explain that network architecture is inherently visual and diagrams cannot be avoided.

**Most effective: A. Least effective: D.**

**Explanation:** A fixes the meeting for everyone, permanently, and closes the loop by checking the changes actually work - inclusion as practice, not gesture; advance papers and text decisions improve the meeting for all attendees, which is the usual signature of a genuinely accessible fix. B keeps the engineer excluded from participation - they can hear about decisions but not influence them, which is the actual harm. C outsources to a process what you can fix yourself this week; adjustments processes have their place, but a chair who controls the meeting format does not need HR's permission to circulate papers in advance. D is least effective: it treats the current format as immutable when the barriers described (undescribed images, late papers, pointing) are all fixable habits, and it tells a skilled colleague their participation matters less than your slide style. Accessibility and inclusion are explicit values in UK government digital work, and SJT keys reward structural fixes over side-channel accommodations.

**Question 12 (hard) - The design review conflict**

You are reviewing another architect's WAN design under the peer review process. The design conflicts with the department's standard in one area - it proposes a non-standard routing protocol - but the architect's justification is technically strong for their unusual case, and following the standard would genuinely degrade the service. The architect is senior to you.

Rate the responses:

A) Approve it silently - their seniority means they know what they are doing.
B) Reject it - standards are standards, whatever the justification.
C) Record the conflict openly: support the deviation on its technical merits through the standard's exception route, and flag to the design authority that the standard may need a documented exception pattern for such cases.
D) Approve it but leave the standards conflict out of your written review to avoid friction.

**Most effective: C. Least effective: D.**

**Explanation:** C handles all three duties in play. As reviewer, you judge the design honestly on its merits - which here favour the deviation. As a supporter of governance, you route the deviation through the exception mechanism rather than around it, keeping the standard meaningful. As an improver of assurance processes, you feed the case back: a standard that repeatedly needs the same justified exception should evolve - identifying and recommending such improvements is in your skill profile. D is least effective, narrowly worse than A: it creates a written review that actively conceals a known standards conflict, corrupting the assurance record that future architects and auditors will rely on; A at least does not falsify a document, though deference to seniority over evidence is still poor reviewing. B mistakes rigidity for rigour - standards serve service quality, and an exception route exists precisely because reality sometimes justifies deviation. Openness about the conflict, whatever you decide, is the non-negotiable element.

### Preparation tips

- **Learn the values, not scripts.** UK public sector keys reward user needs first, transparency, proportionality, collaboration, inclusion, and honest risk reporting. Before the test, re-read your organisation's values and the GDAD framework; during the test, ask which option best embodies them.
- **Look for the option that solves the problem and preserves the relationship.** Most-effective answers usually do both; least-effective answers usually sacrifice one completely (or hide something).
- **Rehearse your own dilemmas.** Think back over vendor disputes, design conflicts, and mentoring moments from your real work. What did you do? What would the best version of you have done? That reflection is the highest-value preparation an SJT allows.
- **Answer as the professional you are at work, not an idealised saint or a cynic.** Keys are calibrated to effective real-world behaviour: honest, proportionate, and active.
- **Read every option before rating any.** Options are often designed in near-pairs (public versus private correction, review versus suspend); the differences between them are where the marks live.

### Common pitfalls

- **Choosing idealistic over effective.** "Suspend the service until fully reviewed" sounds principled but harms users disproportionately. Keys reward practical judgement, not maximal caution.
- **Selecting passive or avoidant options.** Waiting for morning, referring the person to HR, letting stakeholders fight it out, going back to sleep - options that delay, deflect, or abdicate are reliably scored low.
- **Underrating concealment.** Any option that hides, omits, or falsifies - quiet procurement, watermelon reports, unlogged reviews, sanitised written records - is almost always the least effective, even when well-intentioned. If you hesitate between two "least effective" candidates, pick the one that conceals.
- **Overrating escalation.** Terminating the contract, insisting on red, emailing the SRO directly - jumping past proportionate steps scores poorly. Effective options usually exhaust the direct, constructive route first.
- **Ignoring your role's specific duties.** You are the mentor, the process author, the designer on call. Options that shrug off those specific responsibilities ("it's an operational decision") are penalised more heavily for you than they would be for a bystander.

## Conclusion

Well done for working through this guide! You have covered a great deal of ground: cognitive reasoning with addressing plans, design reviews, dependency sequencing, and root-cause isolation; numeric reasoning with SLAs, availability mathematics, vendor pricing, capacity forecasts, and programme budgets; verbal reasoning with standards, contracts, assurance reports, and programme briefings; and situational judgement across the full cast of your working life - engineers, vendors, associate architects, stakeholders, and the governance processes that hold it all together.

Two themes are worth carrying away. First, none of this was artificial: every question was built from the actual duties of a network architect in the UK Government Digital and Data profession. The precision you practised in the verbal section is the precision you will use on your next SLA schedule; the elimination discipline from the cognitive section is tomorrow's troubleshooting call; the values behind the situational judgement answers - transparency, proportionality, user needs, inclusion - are the values your real decisions are already measured against. Preparing for these assessments and getting better at your job turn out to be the same activity, which is the best possible news.

Second, these are learnable skills. Nobody is born knowing that 99.9% monthly availability permits 43.2 minutes of downtime, or that Cannot Say means silence while False means contradiction. Every hour of practice genuinely moves your score - so if some sections felt harder than others, that is simply your development plan writing itself. Revisit the sections that stretched you, build the small daily habits from the preparation tips, and consider working through a question or two with the associate architects you mentor: explaining reasoning aloud is the fastest way to make it permanent, and it doubles as the coaching your role asks of you.

If you have an assessment coming up: sleep well the night before, take the ungraded practice questions, keep an eye on the clock without letting it own you, and trust the reasoning habits you have rehearsed here. You spend your working life making networks reliable under pressure - you already know how to do the same for yourself. Good luck, and keep growing!
