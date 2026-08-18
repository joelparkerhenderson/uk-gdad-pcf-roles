# Network Architect (Associate Network Architect) - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been written especially for you as an associate network architect working in UK government digital and data. Whether you are preparing for a formal assessment, exploring a promotion opportunity, or simply want to sharpen the thinking skills you use every day, this document is here to help you practise, reflect, and build confidence.

First, a quick word about what psychometric assessments actually are. A psychometric assessment is a structured, standardised way of measuring how you think, reason, and make decisions. It is not a test of what you have memorised, and it is definitely not a judgement of your worth as a person or a professional. Instead, it looks at the mental skills that matter in your role: spotting patterns, working with numbers, reading carefully, and choosing sensible actions in tricky workplace situations.

Why do these assessments matter for your role in particular? As an associate network architect, you work alongside network architects on designs and specifications, with guidance. Day to day, that means checking network diagrams for errors, working out capacity figures, reading service level agreements (SLAs) and design standards, and collaborating with engineers to make sure systems are practically designed. Every one of those tasks draws on the exact abilities that psychometric assessments measure. Employers use these assessments because they are a fair, consistent way to see how ready someone is for the reasoning demands of a role — and practising for them genuinely strengthens the skills themselves.

This document is organised into four main assessment sections, each matched to your role:

1. **Workplace job-specific cognitive assessment** — pattern recognition, logical deduction, error checking, and problem solving using the network artefacts you really handle.
2. **Workplace job-specific numeric reasoning assessment** — bandwidth figures, capacity tables, budgets, and SLA percentages, with the arithmetic worked through step by step.
3. **Workplace job-specific verbal reasoning assessment** — dense passages drawn from design policies, standards, and stakeholder emails, with True / False / Cannot Say questions.
4. **Workplace job-specific situational judgement assessment** — realistic dilemmas involving the engineers, architects, and service teams you work with.

Each section explains what the assessment measures, maps it to the specific skills in your role profile (governance and assurance, IT infrastructure, systems design, systems integration, and troubleshooting and problem resolution), and then gives you plenty of practice questions with full answers and explanations. Each section finishes with preparation tips and common pitfalls.

How should you use this guide? Take it at your own pace. Try the practice questions honestly before reading the answers. Use the explanations to understand the reasoning, not just to check whether you were right. Revisit sections after a few days — spaced practice works far better than cramming. And remember: at associate level, nobody expects you to know everything. Curiosity and steady practice are exactly what this stage of your career is about. Good luck — you have got this!

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment is a targeted psychometric test that measures the exact mental processes you need as an associate network architect. Unlike a generic IQ test, it uses practical workplace scenarios and data — the kind you meet in real network design work — to predict how well you will perform on the job. Instead of abstract puzzles about shapes and letters, you will see questions built around network diagrams, device inventories, firewall rule tables, change schedules, and design documents.

The typical format is an online, timed test lasting 15 to 30 minutes. You will usually get short, ungraded practice questions first so you can get comfortable with the interface — so do not panic when the screen looks unfamiliar. Some modern platforms are adaptive, which means the questions get a little harder when you answer correctly and a little easier when you do not. That is normal and nothing to worry about: it simply helps the test find your level efficiently. Scoring is objective, and your results are usually compared against a benchmark group rather than judged in isolation. Many employers also look at your speed versus your accuracy separately, so working carefully is just as valuable as working quickly.

Why does this matter for your role? An associate network architect spends much of the day doing exactly what this assessment measures: checking that a physical design faithfully reflects the logical design, spotting the one wrong VLAN number in a table of forty, working out which change must happen before another, and reasoning logically about why traffic is not reaching a server. Strong cognitive skills mean fewer design errors, faster troubleshooting, and better collaboration with the engineers who build what you draw.

### What it measures for your role

The assessment dimensions map directly onto the skills in your role profile:

- **Pattern recognition** supports your **systems design** skill. When you translate logical designs into physical designs and produce detailed designs, you must notice naming conventions, addressing schemes, and repeating structures — and spot when something breaks the pattern.
- **Logical deduction** supports your **troubleshooting and problem resolution** skill. Identifying problems across different technology capabilities is essentially structured elimination: if the LAN switch is healthy and the WAN link is healthy, where else could the fault be?
- **Error checking** supports your **governance and assurance** skill. Following governance and assurance processes under supervision means checking documents, configurations, and design records against required standards, methods and tools, and catching discrepancies before they reach an assurance board.
- **Prioritisation** supports your work ensuring designs meet **SLAs (service level agreements)**. You must judge which tasks, risks, and fixes matter most when everything feels urgent.
- **Problem solving** supports your **IT infrastructure** and **systems integration** skills. Building, configuring and supporting infrastructure solutions — and explaining the challenges of designing, building and testing interfaces between systems — both demand step-by-step reasoning with well understood technology and appropriate patterns.

### Practice questions

Work through these honestly before checking the answers. They are set in a fictional UK government department, but every artefact is the kind you genuinely handle.

**Question 1 (easy) — Pattern recognition in a device naming convention**

Your department names its network switches using this convention: `<site>-<floor>-SW-<number>`. You see the following inventory list for the Leeds office:

- LDS-01-SW-01
- LDS-01-SW-02
- LDS-02-SW-01
- LDS-02-SW-02
- LDS-03-SW-01
- LDS-3-SW-02

Which entry breaks the naming convention?

A) LDS-01-SW-02
B) LDS-02-SW-01
C) LDS-03-SW-01
D) LDS-3-SW-02

**Correct answer: D**

**Explanation:** The convention uses a two-digit floor number with a leading zero (01, 02, 03). Entry D uses "3" instead of "03". This is exactly the kind of small inconsistency that causes automated monitoring tools and inventory scripts to miss a device. At associate level, catching these details in documentation is a core part of effectively documenting all work using required standards. Notice how the wrong entry is easy to skim past — assessments (and real audits) rely on you slowing down just enough to check each field.

**Question 2 (easy) — Logical deduction from uptime facts**

Your team supports three services. You know the following facts are all true:

- Every service hosted in the Crown Hosting data centre has a resilient power feed.
- The payments service is hosted in the Crown Hosting data centre.
- The licensing service does not have a resilient power feed.

Which conclusion must be true?

A) The payments service has a resilient power feed.
B) The licensing service is hosted in the Crown Hosting data centre.
C) All services with resilient power feeds are in the Crown Hosting data centre.
D) The payments service and the licensing service are hosted in the same place.

**Correct answer: A**

**Explanation:** This is a classic syllogism. If every service in the data centre has resilient power, and payments is in the data centre, payments must have resilient power. Option B must actually be false — if licensing were in the Crown Hosting data centre, it would have a resilient feed, and we are told it does not. Option C reverses the logic: the rule says data centre hosting guarantees resilient power, not that resilient power guarantees data centre hosting. Option D is not supported by anything stated. In troubleshooting, this discipline — only concluding what the facts force you to conclude — keeps you from chasing the wrong fault.

**Question 3 (moderate) — Error checking an IP addressing table**

You are checking a draft physical design before it goes to a design assurance review. The addressing table for four wifi access points reads:

| Device | IP address | Subnet mask | Default gateway |
|---|---|---|---|
| AP-EAST-01 | 10.20.30.11 | 255.255.255.0 | 10.20.30.1 |
| AP-EAST-02 | 10.20.30.12 | 255.255.255.0 | 10.20.30.1 |
| AP-EAST-03 | 10.20.31.13 | 255.255.255.0 | 10.20.30.1 |
| AP-EAST-04 | 10.20.30.14 | 255.255.255.0 | 10.20.30.1 |

All four access points should sit on the same subnet. Which row contains an error, and what is the error?

A) Row 1 — the IP address ends in .11, which is reserved
B) Row 2 — the subnet mask should be 255.255.0.0
C) Row 3 — the IP address is on a different subnet from its gateway
D) Row 4 — the gateway should end in .254

**Correct answer: C**

**Explanation:** With a 255.255.255.0 mask, the subnet is defined by the first three octets. AP-EAST-03 has address 10.20.31.13 — the third octet is 31, not 30 — so it sits on the 10.20.31.0 network while its gateway (10.20.30.1) sits on 10.20.30.0. The device would not be able to reach its own gateway. Options A, B, and D describe rules that do not exist in this design: nothing states .11 is reserved, the mask is consistent across all rows, and the gateway convention here is clearly .1. Error checking questions reward comparing each row against the pattern set by the majority — three rows agree, one deviates.

**Question 4 (moderate) — Prioritisation against SLAs**

It is 09:15 on a Tuesday. You have four tasks in front of you. Your service SLAs commit the department to restoring "critical" services within 4 hours and responding to design review requests within 5 working days.

1. A critical service outage ticket raised at 08:45: a WAN link failure has taken a public-facing service offline.
2. A design review request submitted yesterday for a new office LAN.
3. A network plan document that needs updating before a meeting next Monday.
4. An email from an engineer asking a clarifying question about a cable infrastructure run you specified; the install is scheduled for tomorrow morning.

What is the most sensible order in which to address these?

A) 1, 4, 2, 3
B) 2, 1, 4, 3
C) 1, 2, 3, 4
D) 4, 1, 2, 3

**Correct answer: A**

**Explanation:** The outage (task 1) is under a 4-hour SLA clock that started at 08:45 — it is unambiguously first, even though at associate level your part may be to support a senior colleague and gather information. Task 4 comes next: the engineer's install is tomorrow morning, so an unanswered question today could block work or cause a wrongly routed infrastructure run. Task 2 has a 5-working-day SLA and was submitted yesterday, so it is important but not urgent today. Task 3 has the longest runway (next Monday). Option C fails because it treats the list order as the priority order; option D puts a tomorrow-deadline task ahead of a live outage. Prioritisation questions test whether you separate urgency (deadline pressure) from importance (impact) — and whether you notice SLA clocks that are already running.

**Question 5 (moderate) — Sequencing a change correctly**

You are drafting the implementation plan for replacing an old core switch. The steps, in no particular order, are:

1. Take a verified backup of the old switch configuration.
2. Physically install the new switch in the rack.
3. Schedule and announce the change window to affected teams.
4. Migrate the uplinks from the old switch to the new switch.
5. Confirm the new switch passes health checks with the engineering team.

Which order is correct?

A) 3, 1, 2, 4, 5
B) 1, 2, 3, 4, 5
C) 3, 2, 1, 5, 4
D) 2, 1, 3, 5, 4

**Correct answer: A**

**Explanation:** Governance comes first: the change window must be scheduled and announced (step 3) before disruptive work begins — this reflects following governance and assurance processes. Backing up the old configuration (step 1) must precede any physical change so you can roll back. The new switch is installed (2), the uplinks migrated (4), and only then can meaningful health checks confirm the migration succeeded (5). Option C is tempting, but health checks on a switch with no uplinks migrated would not validate the actual service. Sequencing questions mirror real change planning: ask yourself "what does each step depend on?" and the order usually falls out naturally.

**Question 6 (moderate) — Logical deduction in troubleshooting**

Users on floor 2 report they cannot reach an internal application. You establish these facts:

- Users on floor 3, on the same core switch but a different floor switch, can reach the application.
- Floor 2 users can print to the printer on floor 2 (which is on the same floor switch as the users).
- Floor 2 users cannot reach any service beyond their floor switch.

Which component is the most logical place to investigate first?

A) The application server
B) The uplink between the floor 2 switch and the core switch
C) The users' laptops
D) The core switch

**Correct answer: B**

**Explanation:** Work by elimination. The application server is fine, because floor 3 reaches it (rules out A). The core switch is passing floor 3 traffic correctly (weakens D). The laptops can reach the local printer, so their own connections to the floor switch work (rules out C). The one path that fits all facts is the uplink from the floor 2 switch to the core: local traffic works, everything beyond the floor fails. This is textbook fault isolation — the troubleshooting and problem resolution skill in your profile is largely about drawing these boundaries: "everything on this side works; everything on that side fails; the fault sits at the boundary."

**Question 7 (moderate) — Pattern recognition in VLAN allocation**

Your department allocates VLAN IDs by site and function. You observe:

- Bristol data VLAN: 110. Bristol voice VLAN: 111. Bristol guest wifi VLAN: 119.
- Cardiff data VLAN: 120. Cardiff voice VLAN: 121. Cardiff guest wifi VLAN: 129.
- Glasgow data VLAN: 130. Glasgow voice VLAN: 131.

Following the pattern, what should the Glasgow guest wifi VLAN be?

A) 132
B) 139
C) 140
D) 191

**Correct answer: B**

**Explanation:** Each site owns a block of ten VLAN IDs: Bristol 110–119, Cardiff 120–129, Glasgow 130–139. Within each block, data takes x0, voice takes x1, and guest wifi takes x9 (the last ID in the block). So Glasgow guest wifi is 139. Option A assumes guest wifi simply follows voice sequentially, but Bristol (119, not 112) and Cardiff (129, not 122) disprove that. Recognising allocation schemes like this is central to translating logical designs into physical designs: a good scheme is predictable, and a good associate architect can both follow it and spot when someone else has not.

**Question 8 (moderate) — Error checking a firewall rule table**

A senior architect asks you to sanity-check a draft firewall rule set for a new service integration. The design document says: "The web tier may talk to the application tier on port 8443 only. The application tier may talk to the database tier on port 5432 only. No tier may talk directly to any non-adjacent tier."

The draft rules are:

1. Allow web tier to application tier on port 8443
2. Allow application tier to database tier on port 5432
3. Allow web tier to database tier on port 5432
4. Deny all other traffic

Which rule contradicts the design document?

A) Rule 1
B) Rule 2
C) Rule 3
D) Rule 4

**Correct answer: C**

**Explanation:** The design says no tier may talk directly to any non-adjacent tier. The web tier and database tier are non-adjacent (the application tier sits between them), so rule 3 directly violates the stated policy. Rules 1 and 2 restate the document faithfully, and rule 4 is the standard safety net. This is the essence of design assurance work at your level: you are not being asked to invent policy, you are being asked to verify that an artefact matches its specification, line by line. In an assessment, underline or note each constraint from the specification first, then test every rule against each constraint.

**Question 9 (hard) — Deduction across multiple constraints**

You are planning infrastructure runs for a small refurbished office. The constraints are:

- The comms room must be on the ground floor.
- Each floor switch must be within 90 metres of cable run from the comms room.
- Floor 1 requires a run of 40 metres to reach its switch location; floor 2 requires 70 metres; floor 3 requires 95 metres.
- A repeater or intermediate cabinet may be added on any floor, resetting the 90-metre limit from that point, but the budget allows at most one intermediate cabinet.

Which statement must be true of any valid design?

A) Floor 3 cannot be served at all.
B) The intermediate cabinet must be used on the path serving floor 3.
C) The intermediate cabinet should be placed on floor 1.
D) Floors 1 and 2 both need intermediate cabinets.

**Correct answer: B**

**Explanation:** Floors 1 and 2 are within the 90-metre limit directly (40 m and 70 m), so they need nothing extra — which rules out D immediately. Floor 3 needs 95 metres, which exceeds the 90-metre limit, so it cannot be served directly — but it can be served with an intermediate cabinet that resets the limit partway, so A is false. Since only one cabinet is available and floor 3 is the only floor that needs one, any valid design must spend that cabinet on floor 3's path — which is option B. Option C names a specific placement that might work (a cabinet on floor 1 along the riser could reset the run), but the question asks what must be true, and the cabinet could equally sit on floor 2. Distinguishing "must be true" from "could be true" is one of the most commonly tested skills in logical reasoning — and one of the most valuable habits in design work, where confusing the two leads to over-constrained specifications.

**Question 10 (hard) — Problem solving with a capacity pattern**

A monitoring dashboard shows utilisation of a WAN link sampled at the same time each day: Monday 42%, Tuesday 46%, Wednesday 50%, Thursday 54%, Friday 58%. A senior colleague asks you to estimate when the link will first breach the department's 70% planning threshold if the trend continues at the same daily rate (assume the trend continues across working days only).

A) The following Monday
B) The following Tuesday
C) The following Wednesday
D) The following Friday

**Correct answer: C**

**Explanation:** The utilisation rises 4 percentage points per working day. Continuing from Friday's 58%: Monday 62%, Tuesday 66%, Wednesday 70%. The threshold is breached when utilisation first reaches 70%, which happens on Wednesday. A common slip is to stop at Tuesday (66%) by miscounting the days, or to jump to Friday by assuming weekend days also add 4 points each — but the question says working days only. Trend extrapolation like this feeds real capacity recommendations: drafting recommendations for network support and maintaining network plans often starts with exactly this kind of simple linear projection, clearly stated so a senior architect can challenge the assumption.

**Question 11 (hard) — Spotting the inconsistency between two artefacts**

A logical design states: "All guest wifi traffic must be isolated from the corporate LAN and must egress directly to the internet through the dedicated guest firewall."

The draft physical design shows: guest wifi access points connect to the floor switches; guest traffic is tagged on VLAN 139; VLAN 139 is trunked to the core switch; the core switch routes VLAN 139 to the corporate firewall, which forwards guest traffic to the internet.

Which element of the physical design contradicts the logical design?

A) Guest access points connecting to floor switches
B) Tagging guest traffic on VLAN 139
C) Trunking VLAN 139 to the core switch
D) Routing guest traffic through the corporate firewall

**Correct answer: D**

**Explanation:** The logical design requires guest traffic to egress through the dedicated guest firewall. The physical design sends it through the corporate firewall instead — a direct contradiction. Options A, B, and C are all legitimate ways to carry isolated guest traffic across shared physical infrastructure: VLAN tagging is precisely how logical isolation is achieved on shared switches, so sharing floor switches and trunks does not by itself break the isolation requirement. This question rewards understanding the difference between logical isolation (which VLANs provide) and the specific egress path requirement (which the design got wrong). Translating logical designs into physical designs — your systems design skill — is exactly this discipline: every sentence of the logical design must be traceable to a physical decision.

**Question 12 (hard) — Prioritising risks for a design review**

You are preparing the risk section of a detailed design for review. Four risks have been identified, each scored for likelihood and impact on a 1–5 scale:

- Risk W: likelihood 4, impact 2 (single supplier for switch hardware may delay delivery)
- Risk X: likelihood 2, impact 5 (data centre LAN failure during migration could breach the availability SLA)
- Risk Y: likelihood 3, impact 3 (wifi coverage may be weak in the basement)
- Risk Z: likelihood 1, impact 2 (label printer unavailable for cable labelling)

Using likelihood × impact as the score, and escalating any risk that touches an SLA regardless of score, which two risks should head the register?

A) W and Y
B) X and W
C) X and Y
D) Y and Z

**Correct answer: C**

**Explanation:** Compute the scores: W = 4 × 2 = 8, X = 2 × 5 = 10, Y = 3 × 3 = 9, Z = 1 × 2 = 2. The top two by score are X (10) and Y (9). The SLA escalation rule reinforces X's position at the top but does not change the arithmetic here. Option B is the trap for people who see "likelihood 4" and instinctively rank W high without multiplying. This mirrors real governance practice: risk registers use simple scoring so that reviewers can see why risks are ordered as they are, and ensuring designs meet SLAs means SLA-linked risks always get named attention in your documentation.

**Question 13 (hard) — Multi-step fault isolation across capabilities**

A unified comms service (voice and video) is degraded for one office. You gather these facts:

- Voice calls within the office are fine.
- Video calls to other offices are choppy; voice calls to other offices are fine.
- A file transfer test to another office achieves full expected throughput.
- The WAN provider reports the link healthy with no packet loss.
- Video traffic is marked with a specific QoS (quality of service) class; voice has its own class; file transfers use the default class.

What is the most logical hypothesis to investigate first?

A) The WAN link is over capacity.
B) The video QoS class is misconfigured somewhere on the path between offices.
C) The office LAN switches are failing.
D) Users' video cameras are faulty.

**Correct answer: B**

**Explanation:** Eliminate systematically. Full-throughput file transfers and a healthy provider report make raw capacity or link faults unlikely (rules out A). Local voice and local traffic are fine, so the LAN is delivering packets correctly (weakens C). Faulty cameras would degrade local video too, and the fault pattern is specifically about calls to other offices (rules out D). What distinguishes the failing traffic from the working traffic? It crosses the WAN and it uses the video QoS class — voice crosses the WAN happily in its own class, and file transfer crosses the WAN happily in the default class. The single variable left is the video QoS class treatment on the inter-office path. This is troubleshooting across different technology capabilities in miniature: LAN, WAN, telephony, and QoS all appear, and the skill is holding them apart in your head while the evidence narrows the search.

### Preparation tips

- **Practise with real artefacts.** Spend ten minutes a day reading addressing tables, VLAN plans, and firewall rules from your own team's (non-sensitive) design documents, actively hunting for inconsistencies. The assessment format will then feel familiar rather than artificial.
- **Learn to find the pattern before the exception.** In error-checking questions, first work out what the rule is (the convention, the subnet, the block allocation), then test each item against it. Trying to spot "something odd" without naming the rule first is slower and less reliable.
- **Say the logic out loud when practising.** For deduction questions, phrases like "this rules out A because..." force you to justify each elimination. In the real test you will do this silently, but the habit keeps you honest.
- **Time-box each question.** With 15 to 30 minutes for the whole test, give yourself roughly 60 to 90 seconds per question in practice. If you are stuck at the 90-second mark, flag it, pick your best remaining option, and move on.
- **Do not fear adaptive tests.** If questions feel like they are getting harder, that usually means you are doing well. Treat difficulty as feedback, not threat.
- **Rest properly beforehand.** Cognitive assessments measure processing speed and accuracy, and both degrade badly with tiredness. A good night's sleep is worth more than a final late-night practice session.
- **Be kind to yourself at associate level.** You are early in your architecture career, and these assessments are usually benchmarked accordingly. Steady, careful reasoning matters more than knowing every technology in the framework list — remember your role profile only expects an understanding of one or two network technologies.

### Common pitfalls

- **Skimming instead of checking.** The most common failure in error-checking questions is reading at normal speed. Design documents and assessments both punish this; deliberately slow down on tables.
- **Concluding more than the facts allow.** In deduction questions, watch for options that reverse an implication ("all X are Y" does not mean "all Y are X") or that merely could be true. Only choose what must be true.
- **Getting stuck on one hard question.** As the assessment specifications warn, a single time-sink question can wreck an otherwise good performance. Skipping is a strategy, not a failure.
- **Ignoring stated constraints.** Questions often include a quietly decisive constraint ("working days only", "at most one intermediate cabinet", "same subnet"). Train yourself to list constraints before answering.
- **Letting real-world knowledge override the question.** You might know a better firewall design than the one described — but the question asks about the design as written. Answer the artefact in front of you, exactly as you would in a formal design assurance review.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data. It deliberately mimics the data-handling demands of your actual role, so instead of abstract formulas you will meet bandwidth tables, capacity figures, project budgets, SLA percentages, and equipment cost comparisons — business maths, not exam maths.

The key characteristics are reassuringly practical. Question inputs are real-world artefacts: graphs, cost tables, utilisation dashboards, and project schedules. The maths itself centres on percentages, ratios, unit conversions, and cost-benefit estimations — nothing beyond confident GCSE-level arithmetic. Most assessments allow or provide an onscreen calculator, because they care about interpretation rather than mental arithmetic gymnastics. The main challenge is the strict time limit: you typically need to extract the right numbers quickly from a table or chart, choose the right operation, and avoid careless slips.

For an associate network architect, numeric reasoning is quietly everywhere. When you draft recommendations for network support, you compare supplier costs. When you create and maintain network plans, you forecast port counts and bandwidth growth. When you plan infrastructure runs, you calculate cable lengths, cabinet space, and power budgets. When you ensure designs meet SLAs, you translate availability percentages like 99.9% into real minutes of allowable downtime. And when you collaborate with engineers, you sanity-check throughput and capacity figures so systems are practically designed rather than theoretically hopeful. Practising these calculations does double duty: it prepares you for the assessment and makes you a more useful colleague.

### What it measures for your role

Each numeric skill in the assessment maps onto your role profile:

- **Percentages and availability arithmetic** map to ensuring designs meet **SLAs (service level agreements)**. Converting "99.5% availability" into hours of downtime per month is a bread-and-butter associate task.
- **Tables and cost comparison** map to drafting **recommendations for network support** and awareness of new technology solutions. Recommendations live or die on clear like-for-like cost arithmetic.
- **Capacity and utilisation figures** map to creating and maintaining **network plans** and to your **IT infrastructure** skill — port counts, bandwidth headroom, and growth projections for LAN, WAN, wifi and data centre LAN estates.
- **Ratios and unit conversions** map to **planning infrastructure runs** and translating logical designs into physical designs (your **systems design** skill): cable lengths, rack units, power draw, and megabits versus megabytes.
- **Multi-step problem solving** maps to **systems integration** and **troubleshooting and problem resolution**: working through linked figures (throughput, loss, budget) in the right order without losing track.

### Practice questions

An onscreen calculator is assumed to be allowed. Try each question before reading the worked answer, and check the arithmetic line by line — the working is where the learning is.

**Question 1 (easy) — Percentage utilisation**

A LAN switch has 48 ports. 36 ports are currently in use. What is the percentage utilisation of the switch?

A) 36%
B) 66%
C) 75%
D) 80%

**Correct answer: C**

**Explanation:** Utilisation = ports in use ÷ total ports × 100 = 36 ÷ 48 × 100. 36 ÷ 48 = 0.75, and 0.75 × 100 = 75%. Option A is the trap for anyone who reads "36" and stops thinking. A quick sense-check: 36 is three-quarters of 48, and three-quarters is 75%. Port utilisation like this feeds directly into network plans — many departments trigger a capacity review when switches pass 80%, so knowing a switch is at 75% tells you it is approaching, but has not yet reached, the review threshold.

**Question 2 (easy) — Unit conversion for a file transfer**

An engineer asks you to estimate how long a 3,000 megabyte (MB) backup will take over a link that reliably delivers 200 megabits per second (Mbps). Using 8 bits per byte and ignoring overheads, what is the estimate?

A) 15 seconds
B) 120 seconds
C) 200 seconds
D) 24 seconds

**Correct answer: B**

**Explanation:** First convert megabytes to megabits: 3,000 MB × 8 = 24,000 megabits. Then divide by the link speed: 24,000 ÷ 200 = 120 seconds (2 minutes). Option A comes from dividing 3,000 by 200 and forgetting the bits/bytes conversion entirely — the single most common numeric error in network work. Option D comes from converting the wrong way (dividing by 8 instead of multiplying). Remember the rule: storage is usually quoted in bytes (MB, GB), links in bits (Mbps, Gbps), and bytes are eight times bigger. Writing the conversion as its own line prevents the slip.

**Question 3 (easy) — Reading a capacity table**

Your team's wifi plan shows the following access point (AP) counts and concurrent user capacity:

| Floor | APs installed | Max concurrent users per AP |
|---|---|---|
| Ground | 6 | 30 |
| First | 8 | 30 |
| Second | 4 | 30 |

The second floor is being refitted for 150 desk-based staff, and the design assumption is that at peak, 80% of staff connect concurrently. How many additional APs does the second floor need?

A) 0
B) 1
C) 2
D) 4

**Correct answer: A**

**Explanation:** The two-step chain is: (1) apply the 80% concurrency assumption to headcount, 150 × 0.80 = 120 peak concurrent users; (2) compare with installed capacity, 4 APs × 30 users = 120. Required capacity exactly equals current capacity, so zero additional APs are needed on pure capacity grounds. Option D tempts those who match AP counts to the first floor without calculating, and option C tempts those who assume a refit must always mean more kit. Note the question asks what is needed, not what would be comfortable: in a real design you would answer "zero" and then note in your documentation that zero headroom is a risk worth flagging to your senior architect. Capacity maths answers the question asked; good governance records the caveat alongside it.

**Question 4 (moderate) — SLA availability in real minutes**

Your department's WAN service has a 99.5% monthly availability SLA. Using a 30-day month (43,200 minutes), what is the maximum downtime allowed per month within the SLA?

A) 43.2 minutes
B) 216 minutes
C) 2,160 minutes
D) 21.6 minutes

**Correct answer: B**

**Explanation:** Allowed downtime = (100% − 99.5%) × total minutes = 0.5% × 43,200 = 0.005 × 43,200 = 216 minutes, which is 3 hours 36 minutes. Option A results from using 0.1% (which would be a 99.9% SLA), option C from using 5% (a 95% SLA), and option D from a misplaced decimal point. Decimal placement is the whole game with availability percentages: write the "unavailability" as a decimal first (0.5% = 0.005), then multiply. Ensuring designs meet SLAs starts with being able to state, in plain minutes, what the SLA actually permits — stakeholders understand "about three and a half hours a month" far better than "99.5%".

**Question 5 (moderate) — Comparing supplier costs for a recommendation**

You are drafting a recommendation for network support hardware. Two suppliers quote for 12 identical switches:

- Supplier A: £1,850 per switch, with a 10% discount on the total order.
- Supplier B: £1,700 per switch, plus a fixed £2,100 delivery and staging charge.

Which supplier is cheaper for the full order, and by how much?

A) Supplier A, by £2,520
B) Supplier B, by £2,520
C) Supplier A, by £1,800
D) Supplier B, by £300

**Correct answer: A**

**Explanation:** Work each total in full. Supplier A: 12 × £1,850 = £22,200; the 10% discount is £2,220; total = £22,200 − £2,220 = £19,980. Supplier B: 12 × £1,700 = £20,400; add the fixed £2,100 charge; total = £22,500. Supplier A is cheaper by £22,500 − £19,980 = £2,520. The per-switch prices point the other way — B looks cheaper at £1,700 versus £1,850 — which is exactly the trap: the percentage discount on A's larger base outweighs B's lower unit price once the fixed charge lands. Option C comes from comparing the raw pre-discount totals (£22,200 versus £20,400) and misattributing the winner; option D from ignoring the discount entirely. When drafting real procurement comparisons, showing both full totals explicitly (£19,980 versus £22,500) is precisely what makes your recommendation auditable under governance and assurance processes — a reviewer can re-run your arithmetic in seconds.

**Question 6 (moderate) — Ratio for infrastructure runs**

A cable specification requires that for every 4 data outlets installed, 1 spare outlet is provisioned. A refurbished floor needs 96 active data outlets. How many outlets must be installed in total?

A) 100
B) 120
C) 124
D) 96

**Correct answer: B**

**Explanation:** The ratio of active to spare is 4:1, so spares = 96 ÷ 4 = 24. Total = 96 + 24 = 120. Option C comes from adding a spare for the spares (24 + 4), which the specification does not require; option A comes from guessing "about 4 more". Ratios in infrastructure planning are usually stated as "per N units" — translate them into a division, then an addition, and write both steps down. Planning infrastructure runs regularly involves exactly this arithmetic, and getting it wrong in a design means either costly re-cabling or wasted budget.

**Question 7 (moderate) — Percentage change in utilisation**

A monthly report shows a data centre LAN uplink averaged 3.2 Gbps utilisation in June and 4.0 Gbps in July. What is the percentage increase from June to July?

A) 8%
B) 20%
C) 25%
D) 80%

**Correct answer: C**

**Explanation:** Percentage increase = (new − old) ÷ old × 100 = (4.0 − 3.2) ÷ 3.2 × 100 = 0.8 ÷ 3.2 × 100 = 25%. Option B is the classic error of dividing by the new value instead of the old one (0.8 ÷ 4.0 = 20%). The denominator is always the starting value when you describe growth. This matters in capacity planning narratives: "utilisation grew 25% month on month" triggers a very different conversation with your senior architect than "20%", and over several months compounding makes the difference bigger still.

**Question 8 (moderate) — Rack space and power budgeting**

You are planning a small comms room. The cabinet has 42U of rack space and a power budget of 3,000 watts. You must install:

- 4 switches, each 1U and 150 W
- 2 routers, each 2U and 250 W
- 1 firewall pair, together 2U and 400 W
- 1 UPS, 4U and drawing no budget (it supplies power)

After installation, how much rack space and power budget remain?

A) 28U and 1,500 W
B) 28U and 1,400 W
C) 32U and 1,400 W
D) 30U and 1,500 W

**Correct answer: A**

**Explanation:** Itemise each device on its own line. Rack space used: switches 4 × 1U = 4U; routers 2 × 2U = 4U; firewall pair 2U; UPS 4U. Total = 4 + 4 + 2 + 4 = 14U, leaving 42 − 14 = 28U. Power used: switches 4 × 150 = 600 W; routers 2 × 250 = 500 W; firewall pair 400 W; UPS 0 W. Total = 600 + 500 + 400 = 1,500 W, leaving 3,000 − 1,500 = 1,500 W. So 28U and 1,500 W remain. Each wrong option contains one deliberate slip: option B invents a UPS power draw of 100 W; option C forgets the UPS's 4U of rack space; option D counts the firewall pair as two separate 2U devices. The lesson for both assessments and real cabinet planning is the same: list every device with its space and power on its own line, total each column once, and subtract once. Comms room planning is part of planning infrastructure runs, and an arithmetic slip here becomes a physically impossible install day for the engineers.

**Question 9 (hard) — Weighted downtime across services**

Three services share a WAN link. Last month the link suffered two outages: one of 90 minutes and one of 30 minutes. The month contained 43,200 minutes. The availability SLA is 99.7%. Did the link meet its SLA, and what availability did it achieve (to two decimal places)?

A) Yes — 99.72% achieved
B) No — 99.72% achieved
C) Yes — 99.86% achieved
D) No — 99.60% achieved

**Correct answer: A**

**Explanation:** Total downtime = 90 + 30 = 120 minutes. Availability = (43,200 − 120) ÷ 43,200 × 100 = 43,080 ÷ 43,200 × 100 = 99.7222...%, which rounds to 99.72%. The SLA requires at least 99.7%, and 99.72% ≥ 99.70%, so the SLA was met — option A. Option B has the right arithmetic but the wrong comparison (99.72 is above 99.7, not below). Option C halves the downtime by counting only one outage. Option D uses 173 minutes of downtime, a misreading. Two habits protect you here: add all downtime events before dividing, and compare the achieved figure against the target explicitly, digit by digit. When you ensure designs meet SLAs, this end-of-month arithmetic is exactly how performance gets reported to service owners.

**Question 10 (hard) — Bandwidth headroom with growth**

A data centre LAN uplink is a 10 Gbps link currently peaking at 6.4 Gbps. Traffic is forecast to grow 15% per year, compounding. Will the link still have at least 10% headroom (peak no more than 9 Gbps) after two years of growth?

A) Yes — the peak will be about 8.5 Gbps
B) No — the peak will be about 9.2 Gbps
C) Yes — the peak will be exactly 9.0 Gbps
D) No — the peak will be about 10.6 Gbps

**Correct answer: A**

**Explanation:** Compound growth means multiplying by 1.15 each year. Year 1: 6.4 × 1.15 = 7.36 Gbps. Year 2: 7.36 × 1.15 = 8.464 Gbps, about 8.5 Gbps. Since 8.5 ≤ 9.0, the 10% headroom requirement is still met — option A. Option B comes from adding 15% of the original figure twice (6.4 + 0.96 + 0.96 = 8.32, then mis-adding); more precisely, simple (non-compound) growth gives 6.4 × 1.30 = 8.32, which also stays under 9, so the trap in B is arithmetic rather than method. Option D applies two years of growth to the link capacity instead of the traffic. Compounding questions reward doing one year at a time and writing each intermediate value down. This is the arithmetic behind maintaining network plans: a two-line projection tells your team the uplink survives two years, and a third year (8.464 × 1.15 = 9.73 Gbps) shows when the upgrade conversation must start.

**Question 11 (hard) — Cost per unit of capacity**

You are comparing two WAN upgrade options for a recommendation:

- Option 1: upgrade to 500 Mbps for £18,000 per year.
- Option 2: upgrade to 1 Gbps (1,000 Mbps) for £30,000 per year.

Which option gives the lower cost per Mbps per year, and what is that figure?

A) Option 1, at £36 per Mbps
B) Option 2, at £30 per Mbps
C) Option 1, at £30 per Mbps
D) Option 2, at £36 per Mbps

**Correct answer: B**

**Explanation:** Option 1: £18,000 ÷ 500 Mbps = £36 per Mbps per year. Option 2: £30,000 ÷ 1,000 Mbps = £30 per Mbps per year. Option 2 is cheaper per unit of capacity at £30 per Mbps. Note the subtlety for your written recommendation: Option 2 is better value per megabit but costs £12,000 more per year in absolute terms — if the department will never use more than 500 Mbps, the "better value" option wastes money. A strong associate-level recommendation presents both figures (unit cost and total cost) and lets the decision-maker weigh them against forecast demand. Assessments test the division; real governance tests whether you know which division matters.

**Question 12 (hard) — Multi-step: packet loss and effective throughput**

An engineer reports that a 200 Mbps WAN link is experiencing 2% packet loss, and that retransmissions mean effective useful throughput is reduced by roughly five times the loss percentage. Using that rule of thumb, what is the approximate effective throughput?

A) 196 Mbps
B) 190 Mbps
C) 180 Mbps
D) 100 Mbps

**Correct answer: C**

**Explanation:** The rule of thumb says the throughput reduction is 5 × 2% = 10%. Effective throughput = 200 × (1 − 0.10) = 200 × 0.90 = 180 Mbps. Option A subtracts only the raw loss (2% of 200 = 4 Mbps), ignoring the stated multiplier; option B subtracts 5% instead of 10%; option D dramatises the problem. The question is really testing whether you apply the rule given rather than a rule you know. Assessments (and design standards) often supply their own approximation — your job is to follow the stated method faithfully and save the debate about whether the rule is accurate for the design review discussion, where challenging assumptions is genuinely welcome.

**Question 13 (hard) — Interpreting a monitoring table under time pressure**

A monthly performance dashboard shows four sites. Figures are averages; "peak" is the busiest hour.

| Site | Link size | Average use | Peak use | Packet loss at peak |
|---|---|---|---|---|
| Newcastle | 100 Mbps | 40 Mbps | 85 Mbps | 0.1% |
| Swansea | 200 Mbps | 90 Mbps | 190 Mbps | 1.8% |
| Norwich | 100 Mbps | 70 Mbps | 80 Mbps | 0.0% |
| Belfast | 500 Mbps | 150 Mbps | 260 Mbps | 0.1% |

Department policy: a link must be upgraded when peak use exceeds 90% of link size, or when packet loss at peak exceeds 1%. Which site or sites require an upgrade under the policy?

A) Swansea only
B) Swansea and Norwich
C) Newcastle and Swansea
D) Norwich only

**Correct answer: A**

**Explanation:** Compute the 90% thresholds: Newcastle 90 Mbps, Swansea 180 Mbps, Norwich 90 Mbps, Belfast 450 Mbps. Compare peaks: Newcastle 85 < 90 (no); Swansea 190 > 180 (yes); Norwich 80 < 90 (no); Belfast 260 < 450 (no). Then the loss test: only Swansea (1.8%) exceeds 1%. Swansea fails both tests; nobody else fails either. Option B is the trap for readers who compare Norwich's average (70) against a mental "70% feels high" instinct rather than the stated 90%-of-peak rule; option C is for those who misread Newcastle's 85 as 95. Two disciplines win here: compute each threshold explicitly rather than eyeballing, and apply only the policy as written. This is also a genuinely realistic artefact — drafting upgrade recommendations from monitoring dashboards is core associate network architect work, and the policy thresholds come straight from the kind of network design policy your role helps produce.

**Question 14 (moderate) — Budget share for a network programme**

A network refresh programme has a total budget of £240,000, allocated as: 45% hardware, 25% professional services, 20% cabling and infrastructure runs, and the remainder held as contingency. Midway through, hardware comes in £10,800 under its allocation, and the programme board agrees to move that saving into contingency. What is the new contingency amount?

A) £24,000
B) £34,800
C) £10,800
D) £45,600

**Correct answer: B**

**Explanation:** First find the original contingency percentage: 100% − 45% − 25% − 20% = 10%. Original contingency = 10% of £240,000 = £24,000. The hardware saving of £10,800 is added to it: £24,000 + £10,800 = £34,800. Option A stops after the first step and forgets the transfer; option C reports only the saving; option D is the answer if you mistakenly treat contingency as 19% by mis-adding the percentages. Two habits help: make the "remainder" percentage explicit by subtracting from 100 before computing anything, and treat each movement of money as its own line. Associate network architects rarely own budgets, but you will feed figures like these into business cases and programme updates, and being the person whose percentages reliably add up to 100 builds trust quickly.

### Preparation tips

- **Rebuild your percentage reflexes.** Availability, utilisation, growth, and discounts are all percentages. Practise converting between forms quickly: 99.5% availability means 0.5% downtime means multiply by 0.005. Ten minutes of drills, a few times a week, makes these automatic.
- **Master the bits/bytes conversion cold.** It appears constantly in network arithmetic and is the most common source of an eight-times error. Say it as a rule: storage in bytes, links in bits, multiply bytes by 8 to get bits.
- **Show your working even in practice.** Write each step on paper exactly as the explanations above do. Under time pressure, written intermediate values stop you re-computing and catch slips early.
- **Read the table headers first.** Before touching any numbers, note the units (Mbps or MB? monthly or annual? averages or peaks?) and any qualifiers. Most wrong answers in table questions are extraction errors, not calculation errors.
- **Use the calculator for arithmetic, your head for method.** The calculator cannot choose the denominator in a percentage-change question or decide whether growth compounds. Decide the method first, then compute.
- **Estimate before you calculate.** A rough answer ("about three-quarters, so about 75%") catches decimal-point disasters instantly.
- **Practise with your own team's dashboards.** Utilisation reports and capacity plans from your real environment (kept non-sensitive) are ideal practice material and build job knowledge at the same time.

### Common pitfalls

- **Misreading chart and table labels.** Confusing monthly with annual figures, averages with peaks, or missing qualifiers like "in thousands" — the assessment specifications call this out as the most frequent failure, and network dashboards are full of such qualifiers.
- **Over-calculating.** Sometimes a quick estimate or a comparison of two ratios answers the question without long-hand arithmetic. If two options differ hugely, rounding is your friend.
- **Time-sink questions.** A multi-stage problem you cannot crack in 90 seconds should be flagged and skipped. Banking three easy questions beats wrestling one hard one.
- **The wrong denominator.** Percentage change uses the original value as the base; unit cost uses capacity as the base; availability uses total minutes. Ask "per what?" before dividing.
- **Ignoring stated rules of thumb.** When the question supplies its own approximation or policy threshold, use it exactly as given — even if you know a more precise method from your day job.
- **Forgetting the sanity check.** A backup that transfers in 15 seconds, a switch at 120% utilisation, or a negative headroom figure should ring alarm bells. One second of "does this make sense?" saves marks.
- **Compound versus simple growth confusion.** When a question says growth "compounds", multiply year by year; when it says a fixed amount or a percentage "of the original", add. Mixing the two methods produces answers that are close enough to feel right but wrong enough to lose the mark — and, in a capacity plan, wrong enough to mistime an upgrade by a year.
- **Carrying figures in your head across steps.** Multi-stage questions (convert units, then divide, then compare against a threshold) punish mental juggling. Write each intermediate value down with its unit attached; the unit label alone catches most transposition errors, because "24,000 megabits" and "24,000 megabytes" refuse to look the same on paper.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment evaluates how well you understand, analyse, and draw correct conclusions from written business information. It mirrors the exact reading demands of your role, so the passages you will meet look like the documents on your desk right now: network design policies, technical standards, SLA schedules, change notices, supplier statements, and emails from engineers and service managers.

The format has a few defining characteristics. Passages are context-specific and often deliberately dense. Questions are fact-based: you must answer based strictly on the text provided, setting aside everything you happen to know from your own experience. The classic question type offers three options — **True** (the passage says or logically guarantees it), **False** (the passage contradicts it), or **Cannot Say** (the passage gives insufficient information either way). Some questions are multiple-choice comprehension instead, asking for the best summary or the correct application of a stated rule. Timing is tight — usually less than a minute per question — because workplaces are tight on time too.

Why does this matter so much for an associate network architect? Because your role is steeped in careful reading. Producing network design policy means writing text others will interpret strictly — so you must first learn to read text strictly. Following governance and assurance processes under supervision means understanding exactly what a standard requires, not roughly what it requires. Ensuring designs meet SLAs means parsing contractual language where "must", "should", and "may" carry very different weights. And documenting all work using required standards means noticing when your own words could be misread. Verbal precision is not a nice-to-have in architecture; it is the raw material of the job.

### What it measures for your role

- **Extracting rules from policy text** maps to your **governance and assurance** skill: explaining why governance matters and following assurance processes both begin with reading the process documents accurately.
- **Distinguishing facts from assumptions** maps to **systems design**: a detailed design must record what is known and flag what is assumed, and the True / False / Cannot Say discipline is exactly that distinction in miniature.
- **Parsing conditional and qualified language** ("unless", "only if", "except where") maps to ensuring designs meet **SLAs** and to producing **network design policy**, where a single conditional clause can change an obligation entirely.
- **Comprehending technical correspondence** maps to your collaboration with engineers (**IT infrastructure** and **systems integration**): emails and handover notes must be understood the first time, especially during incidents.
- **Identifying what a text does not say** maps to **troubleshooting and problem resolution**: incident reports rarely contain everything, and knowing what is missing directs your next question.

### Practice questions

For each passage, answer strictly from the text. Your outside knowledge of networks is deliberately irrelevant — and sometimes a trap.

**Passage A — from a departmental network design policy**

"All new local area network (LAN) designs must segment user devices, servers, and building management systems into separate VLANs. Guest wireless traffic must not traverse the corporate LAN and must egress via the dedicated guest internet connection. Designs for sites with more than 200 users must include a resilient pair of core switches; smaller sites may use a single core switch provided the business owner formally accepts the availability risk. All designs must be reviewed by the design assurance board before procurement begins."

**Question 1 (easy).** True, False, or Cannot Say: "New LAN designs must place servers and user devices in separate VLANs."

**Correct answer: True**

**Explanation:** The first sentence requires user devices, servers, and building management systems to be segmented "into separate VLANs". Separating servers from user devices is explicitly part of that requirement. This is a direct-lookup question: the answer sits in one sentence, and your only job is to find it and match the wording. Around a third of verbal reasoning questions are this straightforward — bank them quickly to buy time for harder ones.

**Question 2 (easy).** True, False, or Cannot Say: "A site with 150 users is forbidden from installing a resilient pair of core switches."

**Correct answer: False**

**Explanation:** The policy says smaller sites "may use a single core switch" if the risk is formally accepted. "May" grants permission for the cheaper option; it does not forbid the resilient option. Nothing in the passage prevents a 150-user site choosing resilient cores. This is the classic modal-verb trap: "may do X" never means "must do X" and never means "must not do Y". As someone who will help produce network design policy, notice how much work that one word does — and how easily a careless reader inverts it.

**Question 3 (moderate).** True, False, or Cannot Say: "The design assurance board must review designs within ten working days."

**Correct answer: Cannot Say**

**Explanation:** The passage requires review "before procurement begins" but says nothing about how quickly the board must act. Ten working days may well be the real-world standard in some departments — which is precisely why this question is dangerous. If you have seen such a target in your own organisation, your memory supplies what the passage does not. Cannot Say is the correct answer whenever the claim is neither stated, guaranteed, nor contradicted by the text. Treat every passage as the only document in the world.

**Question 4 (moderate).** True, False, or Cannot Say: "Guest wireless traffic may cross the corporate LAN if it is encrypted."

**Correct answer: False**

**Explanation:** The policy states guest traffic "must not traverse the corporate LAN" — with no exceptions listed. The question invents a condition (encryption) that the passage never offers. When a passage states an absolute prohibition and a question adds "if...", check whether the passage itself contains that exception; if it does not, the prohibition stands and the claim is False. Reading for the presence or absence of exception clauses is a core skill when you check designs against policy in assurance reviews.

**Question 5 (moderate) — multiple choice.** Which of the following designs complies with the policy as written?

A) A 300-user site with a single core switch, where the business owner has accepted the risk in writing.
B) A 120-user site with a single core switch and formal risk acceptance, reviewed by the design assurance board before procurement.
C) A 250-user site with resilient core switches, procured before design assurance review to meet a deadline.
D) A 180-user site where guest wifi egresses through the corporate internet connection for cost reasons.

**Correct answer: B**

**Explanation:** Test each option against every policy clause. Option A fails because sites over 200 users must have resilient cores — risk acceptance is only available to smaller sites. Option C has the right hardware but breaks the sequencing rule: review must happen before procurement begins, with no deadline exception offered. Option D violates the guest egress requirement regardless of motive. Option B satisfies everything: under 200 users, single core permitted with formal acceptance, and review completed before procurement. Compliance questions reward methodical elimination — check each option against each rule, and never let a plausible-sounding justification ("to meet a deadline", "for cost reasons") excuse a breach the text does not excuse.

**Passage B — from a WAN service level agreement schedule**

"The supplier shall provide the WAN service with a monthly availability of at least 99.7%, measured per site. Planned maintenance, notified at least five working days in advance and performed between 22:00 and 06:00, is excluded from the availability calculation. Where availability at a site falls below 99.7% in a calendar month, the customer shall be entitled to service credits equal to 5% of that site's monthly charge, rising to 10% where availability falls below 99.0%. Service credits are the customer's sole financial remedy for availability failures, and must be claimed within 30 days of the month's end."

**Question 6 (moderate).** True, False, or Cannot Say: "An unannounced maintenance outage at 23:00 is excluded from the availability calculation."

**Correct answer: False**

**Explanation:** The exclusion has two cumulative conditions: notification at least five working days in advance and performance between 22:00 and 06:00. An unannounced outage fails the first condition, so it counts against availability even though the timing fits the second. Compound conditions joined by "and" require every part to be satisfied — a detail that decides real disputes about SLA breaches, and exactly the kind of clause you will check when ensuring designs and services meet SLAs.

**Question 7 (moderate).** True, False, or Cannot Say: "A site with 99.4% availability in a month is entitled to a 10% service credit."

**Correct answer: False**

**Explanation:** Read the thresholds carefully: below 99.7% earns 5%; the credit rises to 10% only where availability falls below 99.0%. At 99.4%, availability is below 99.7% but not below 99.0%, so the entitlement is 5%, not 10%. The claim states the wrong tier, so it is False rather than Cannot Say — the passage gives you everything needed to refute it. Banded thresholds like these appear constantly in SLA schedules, and misreading which band applies is one of the most common (and expensive) contractual mistakes.

**Question 8 (hard).** True, False, or Cannot Say: "If the supplier's failure causes the customer significant business losses, the customer can recover those losses in addition to service credits."

**Correct answer: False**

**Explanation:** The passage states that service credits are "the customer's sole financial remedy for availability failures". "Sole" excludes additional financial recovery for those failures, so the claim contradicts the text. Be careful of the sympathy trap: the claim describes an outcome that feels fair, and many candidates drift toward Cannot Say because the passage does not discuss business losses explicitly. It does not need to — "sole financial remedy" settles the matter. One decisive word can outweigh a paragraph of silence, which is why contract language rewards slow, deliberate reading.

**Passage C — email from a senior network engineer**

"Hi — quick update before tomorrow's install. We walked the riser this afternoon and the containment on floors 1 and 2 is fine, but floor 3's tray is full. We can either share the electrical containment (needs building management sign-off, and they usually take a week) or run a new tray section, which the contractor can do Thursday for about £900. Either way, tomorrow we can still do floors 1 and 2 as planned. Also, the switch delivery arrived but one of the six units has a dented chassis — I have asked the supplier for a replacement and flagged it in the asset register. Can you update the plan and let the project manager know? Thanks."

**Question 9 (moderate).** True, False, or Cannot Say: "The installation on floors 1 and 2 can proceed tomorrow."

**Correct answer: True**

**Explanation:** The engineer states directly: "tomorrow we can still do floors 1 and 2 as planned." The distractors in this passage are the floor 3 problem and the dented switch, which affect other parts of the plan but not tomorrow's work on floors 1 and 2 — the engineer explicitly separates them. Operational emails bury the key facts among caveats; the skill is matching each fact to its scope. This is exactly the collaboration-with-engineers reading your role demands: engineers tell you what is practically possible, and your plans must capture it faithfully.

**Question 10 (hard).** True, False, or Cannot Say: "Running a new tray section is the faster option for floor 3."

**Correct answer: Cannot Say**

**Explanation:** Tempting to say True: sign-off "usually" takes a week, and the contractor can fit the tray on Thursday. But "usually a week" is not "always a week" — sign-off could conceivably come faster — and the passage does not state which day "Thursday" falls relative to the potential sign-off date, nor whether tray installation is the only step in that option. The passage makes the new tray look faster without guaranteeing it. When a conclusion depends on stacking probabilities ("usually") and unstated dates, the strict answer is Cannot Say. This distinction — between what a text implies and what it establishes — is the single most examined skill in verbal reasoning, and the most valuable habit in reading engineering updates: likely is not certain, and plans that treat "usually" as "always" fail on the exception.

**Question 11 (moderate).** True, False, or Cannot Say: "Five of the six delivered switches are undamaged."

**Correct answer: Cannot Say**

**Explanation:** Careful. The engineer says one of the six units has a dented chassis. It is natural to conclude the other five are fine — but the passage only reports one observed defect; it does not state that the remaining five were inspected and found undamaged. A dent is visible; other damage might not be. Strictly, the text supports "at least one unit is damaged", not "exactly five are undamaged". This is a hard discipline, because everyday reading fills the gap automatically. Assessments deliberately exploit that reflex. In asset and quality records — like the register the engineer updated — the same discipline applies: record what was verified, not what was assumed.

**Question 12 (moderate) — multiple choice.** Which action does the engineer explicitly ask you to take?

A) Obtain building management sign-off for shared containment.
B) Order a replacement switch from the supplier.
C) Update the plan and inform the project manager.
D) Approve the £900 contractor cost for the new tray.

**Correct answer: C**

**Explanation:** The email's closing line is a direct request: "Can you update the plan and let the project manager know?" The engineer has already handled the supplier replacement (option B) and presents the containment choices as options rather than asking you to pursue either one (options A and D describe decisions not yet made, and the email does not ask you to make them alone). Requests hide at the ends of emails; actions already taken hide in the middle. Separating "done", "decision needed", and "asked of me" is a reading habit that keeps projects moving and makes you a dependable collaborator — and it is tested here in exactly the form your inbox tests it daily.

**Passage D — from a technical standard on remote access**

"Remote access to the departmental network shall be permitted only via the approved virtual private network (VPN) client with multi-factor authentication enabled. Personal devices shall not be granted remote access unless they are enrolled in the department's device management service and meet the minimum security baseline. Third-party support organisations may be granted time-limited remote access for specific maintenance activities, subject to a signed access agreement and monitoring of all session activity. Access rights not used for 90 consecutive days shall be automatically revoked."

**Question 13 (moderate).** True, False, or Cannot Say: "A personal device enrolled in the device management service is automatically granted remote access."

**Correct answer: False**

**Explanation:** The standard says personal devices shall not be granted access "unless they are enrolled... and meet the minimum security baseline." Enrolment alone satisfies only half of a two-part condition — the device must also meet the baseline — and even then the sentence removes a prohibition rather than promising a grant. "Not X unless Y" means Y is necessary for X, never that Y is sufficient. Confusing necessary with sufficient conditions is a top-three error in verbal reasoning and in real policy reading alike; remote access standards, of the kind your role profile expects you to understand, are written almost entirely in this conditional grammar.

**Question 14 (hard).** True, False, or Cannot Say: "A third-party support engineer's remote session must be monitored."

**Correct answer: True**

**Explanation:** Third-party access is available "subject to a signed access agreement and monitoring of all session activity." "Subject to" makes both conditions mandatory features of any granted access — so if a third-party engineer has a remote session at all, monitoring applies to it. Note the reasoning pattern: the claim is guaranteed by the text's conditions rather than stated as a standalone sentence, which is what lifts this question to hard. True does not always mean "quoted verbatim"; it means the text logically commits to the claim.

**Question 15 (hard).** True, False, or Cannot Say: "An account unused for 60 days will be revoked if the user is on long-term leave."

**Correct answer: Cannot Say**

**Explanation:** Unpack it slowly. The automatic rule triggers at 90 consecutive days, so it does not require revocation at 60 days — that much argues against True. But the passage also never states that 90-day inactivity is the only way access can be revoked, so it cannot contradict the possibility that some other process (a leave procedure, a manager's request) revokes the account — that argues against False. With the claim neither guaranteed nor contradicted, Cannot Say stands. Many candidates answer False here, reasoning "the rule says 90, so 60 must not be revoked" — but the rule's silence about other revocation routes is the deciding observation. Questions like this reward mapping the claim onto exactly what the text commits to, clause by clause, before choosing a label.

**Passage E — from a design review board's written feedback**

"The board thanks the team for a well-documented submission. The logical design is approved. The physical design is approved subject to two conditions: first, the proposed software-defined (SD) WAN pilot must be limited to the two named sites until a security review of the vendor's management platform is complete; second, the telephony migration plan must be resubmitted with a rollback procedure, as the current draft describes rollback for data services only. The board notes, without making it a condition, that the unified communications capacity assumptions appear optimistic and suggests the team revisit them before implementation."

**Question 16 (moderate).** True, False, or Cannot Say: "The physical design has been rejected."

**Correct answer: False**

**Explanation:** The board approved the physical design "subject to two conditions". Conditional approval is still approval — the design has not been rejected; it has been approved with strings attached. Candidates who skim often collapse the three possible outcomes (approved, approved with conditions, rejected) into two. Governance documents use these gradations deliberately, and reading them correctly determines what your team may do next: here, work can proceed provided the conditions are met, which is a very different position from rejection.

**Question 17 (hard).** True, False, or Cannot Say: "The team is required to revise the unified communications capacity assumptions."

**Correct answer: False**

**Explanation:** The board explicitly frames this point as a note made "without making it a condition" and a suggestion. A suggestion is not a requirement, and the passage goes out of its way to say so. The claim asserts an obligation the text expressly declines to create, so it is False rather than Cannot Say. Contrast this with the two genuine conditions (the SD-WAN site limit and the telephony rollback resubmission), which are requirements. Distinguishing conditions from advisory notes is precisely the reading skill you need when your own designs come back from assurance boards — acting on suggestions is wise, but knowing what is mandatory tells you what gates your implementation.

### Preparation tips

- **Read the question's claim twice, the passage's relevant sentence three times.** Most errors come from matching a claim to a half-remembered version of the text. Physically point at the sentence if it helps — nobody can see you.
- **Learn the modal verbs as a vocabulary list.** Must, shall, should, may, must not, unless, subject to, sole, only. Each has a precise force in policy and contract language. Practise translating them: "may" = permitted, "shall" = obliged, "unless" = necessary condition, "sole" = excludes alternatives.
- **Rehearse the Cannot Say discipline daily.** Take any work document and write three claims about it: one True, one False, one Cannot Say. Building the third category into your instincts is the highest-value preparation you can do, because untrained readers barely use it.
- **Quarantine your expertise.** You know networks; the test only permits the passage. Before answering, ask: "is my evidence in the text, or in my head?" If it is in your head, it does not count.
- **Practise on your own governance documents.** Design policies, assurance checklists, and SLA schedules from your department (non-sensitive ones) are perfect training material — and reading them closely doubles as professional development for your governance and assurance skill.
- **Manage the clock by scanning with purpose.** Read the claim first, then scan the passage for its key terms, then read that region carefully. Reading the full passage slowly before seeing any question wastes your tightest resource.
- **Stay calm about dense text.** At associate level, dense standards can feel intimidating — but the assessment never requires background knowledge, only careful reading. Every answer is on the page. That is genuinely reassuring once you believe it: the test is not asking whether you have read every departmental standard, it is asking whether you can read this one, right now, with care. That skill is entirely within your control, and it improves measurably with every week of deliberate practice.

### Common pitfalls

- **Making assumptions from outside knowledge.** The specification lists this as the top pitfall, and for technologists it is doubly dangerous: the more you know about VPNs, SLAs, and VLANs, the more your brain volunteers "facts" the passage never stated.
- **Confusing "likely" with "stated".** A passage that makes an outcome probable ("usually takes a week") has not made it certain. Likely outcomes are Cannot Say territory unless the text commits.
- **Inverting modal verbs.** Reading "may" as "must", or "not unless" as "if", silently rewrites the rule. Slow down whenever a claim hinges on one of these words.
- **Missing compound conditions.** "Subject to a signed agreement and monitoring" means both. Tick each condition separately before concluding.
- **Poor time management.** Spending three minutes perfecting one Cannot Say while four easy questions go unanswered is a net loss. Flag, guess sensibly, move on.
- **Answering the passage you wish existed.** When a rule seems inefficient or unfair, candidates sometimes answer as if it were better written. In assurance work as in assessments, you must first read what the document actually says — improving it comes afterwards, through the proper review channels.
- **Treating False and Cannot Say as interchangeable.** They are opposites in an important sense: False requires positive evidence of contradiction in the text, while Cannot Say requires an absence of evidence either way. If you cannot point to the words that contradict the claim, you have not earned a False. Candidates who default to False whenever a claim "feels unsupported" leak marks steadily across a whole test.
- **Losing the thread in long sentences.** Policy sentences often stack three or four clauses ("subject to X, and provided Y, except where Z"). Break them into their parts mentally — obligation, condition, exception — before judging any claim against them. A clause you skimmed past is usually the one the question turns on, because question writers read the same sentence and chose it for exactly that reason.

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment evaluates your decision-making, interpersonal skills, and professional conduct. Unlike the logic and maths tests earlier in this guide, it presents realistic workplace dilemmas — the awkward, in-between situations that fill real working weeks — and asks how you would respond. There is usually no single objectively right answer in the mathematical sense; instead, some responses fit the role, the organisation's values, and good professional practice better than others.

The format is scenario-based: a short description of a workplace situation, followed by three to five possible actions. You will typically be asked either to pick the **most effective** and **least effective** actions, or to rank or rate all the options from best to worst. Timing is usually generous or absent, because the assessment cares about your natural judgement rather than your speed. That makes it feel gentler than the timed tests — but do not mistake gentle pacing for low stakes. For roles like yours, employers often weight situational judgement heavily, because an associate architect's real value lies in how they collaborate, escalate, and handle uncertainty.

For your role, the scenarios revolve around your real working relationships: the network architects who guide you, the engineers who build from your designs, the service managers who own SLAs, the project managers tracking delivery, the assurance boards that review your work, and the suppliers who provide kit and connectivity. The dilemmas test judgement in the situations your role profile creates: you work "with guidance", so when do you ask for help versus act? You follow governance "under supervision", so what do you do when a shortcut is tempting? You collaborate with engineers, so how do you handle disagreement about whether a design is practical?

Throughout, strong answers align with UK public sector values: putting user needs first, being transparent about problems and mistakes, collaborating across teams rather than protecting territory, and taking accessibility and inclusion seriously in both design decisions and everyday behaviour.

### What it measures for your role

- **Knowing when to escalate** maps to your role level itself — an associate works "with guidance", and mature judgement about when to use that guidance is the defining associate skill.
- **Integrity under pressure** maps to **governance and assurance**: following processes under supervision is easy on quiet days; the assessment probes what you do when deadlines and processes collide.
- **Collaborative problem solving** maps to your duty to **collaborate with engineers to ensure systems are practically designed** — handling disagreement, feedback, and shared ownership of problems.
- **Service focus** maps to ensuring designs meet **SLAs**: weighing user impact and service continuity when choosing between actions.
- **Honest communication about problems** maps to **troubleshooting and problem resolution**: incidents are handled well by people who share information early and accurately, even when the news is bad.

### Practice questions

For each scenario, decide your answer before reading the discussion. Where the format is most/least effective, identify both.

**Scenario 1 (easy) — The unclear design task**

Your senior network architect asks you to draft the physical design for a small office LAN and then leaves for two days of workshops. Partway through, you realise the logical design does not specify whether the office needs a separate VLAN for building management systems, and departmental policy requires one where such systems exist. You do not know whether this office has any.

Possible actions:

A) Pause the whole design until the architect returns and can answer.
B) Add the VLAN anyway — better to have it and not need it.
C) Check the site survey documents and ask the office's facilities contact; if still unclear, note the open question in the draft and continue with the rest of the design.
D) Leave the VLAN out and assume the architect would have mentioned it if it mattered.

**Most effective: C. Least effective: D.**

**Explanation:** Option C shows exactly the associate-level judgement employers want: you try the available information sources yourself, you keep the work moving, and you make the uncertainty visible in the document rather than hiding it. Option A is safe but passive — two days of lost progress over a question you could probably resolve, and "pausing everything" scales badly. Option B is action without information; adding unneeded segments creates complexity and cost, and normalises guessing in design documents. Option D is the least effective because it converts your uncertainty into a silent assumption — the design will look complete while resting on an unverified guess, which is precisely how errors reach assurance boards. Working "with guidance" does not mean waiting for guidance on everything; it means exhausting reasonable self-service first and flagging what remains, transparently.

**Scenario 2 (easy) — The mistake in your own work**

While preparing for tomorrow's design assurance review, you notice that the addressing table you produced last week — already circulated to the review board — contains a subnet error that would prevent two floors from routing correctly. Nobody else has spotted it.

Possible actions:

A) Say nothing and hope to correct it quietly after the review.
B) Email the board and your senior architect today, owning the error, attaching a corrected table, and briefly explaining the fix.
C) Mention it verbally at the start of tomorrow's review.
D) Correct the table in the master document tonight without telling anyone, since the fix is simple.

**Most effective: B. Least effective: A.**

**Explanation:** Option B is transparent, prompt, and practical: the board reviews the corrected artefact instead of wasting time on a flawed one, your senior architect is never blindsided, and you demonstrate that you check your own work. Option C is honest but late — board members may have already read the flawed table, and a verbal correction of a numeric artefact invites transcription errors. Option D fixes the data but corrupts the process: documents under review must not change silently, and version integrity is a governance fundamental. Option A is least effective because it prioritises your comfort over the service and the truth; in public sector culture, hiding known errors is far more damaging to trust than making them. Everyone makes addressing mistakes; careers are shaped by what happens in the ten minutes after you find one.

**Scenario 3 (moderate) — The engineer who says your design will not work**

An experienced field engineer reviews your detailed design for a wifi refresh and says, bluntly, "This AP placement is wrong — whoever drew this has never pulled cable above a suspended ceiling." You worked hard on the placement using the vendor's planning tool, and their tone stings.

Possible actions:

A) Defend the design: the planning tool is industry standard, and the survey data supports your placements.
B) Ask the engineer to walk you through the practical problems floor by floor, and offer to revise the design together where the concerns hold up.
C) Escalate to your senior architect that the engineer is being obstructive.
D) Accept all the engineer's changes to keep the relationship positive.

**Most effective: B. Least effective: C.**

**Explanation:** Your role profile says you collaborate with engineers "to ensure systems are practically designed" — option B is that duty in action. The engineer holds practical knowledge your planning tool lacks (containment routes, ceiling voids, install effort), and inviting a walk-through converts friction into a better design and a stronger working relationship. It also does not capitulate: "where the concerns hold up" keeps the survey data in play. Option A treats design as a status contest and tools as trump cards; even if you are partly right, you learn nothing. Option D swings the other way — abandoning your evidence wholesale teaches the engineer that pushing hard beats reasoning, and may reintroduce genuine coverage problems. Option C is least effective: escalating a first disagreement as "obstruction" wastes your architect's time, damages your reputation with the engineering team, and skips the collaboration your role exists to perform. Blunt feedback is uncomfortable, but it is also free expertise — the tone is theirs to improve; the content is yours to mine.

**Scenario 4 (moderate) — The tempting shortcut past assurance**

A project manager tells you their office move will miss its date unless switch procurement starts this week. The design assurance board does not meet for nine days. The PM says: "Just order the kit — it's the same switches we always use. We'll take it through the board afterwards. I'll take responsibility."

Possible actions:

A) Agree — the hardware choice genuinely is standard, and the PM has accepted responsibility.
B) Refuse and tell the PM the project will simply have to slip.
C) Tell your senior architect immediately, and ask whether the board's chair can consider an out-of-cycle or expedited review given the deadline.
D) Order the kit but document in writing that the PM instructed it.

**Most effective: C. Least effective: A.**

**Explanation:** The policy you work under says designs are reviewed before procurement begins, and you follow governance and assurance processes under supervision — which means when the process pinches, you bring in your supervisor rather than bend it yourself. Option C does that and does more: it looks for the legitimate fast path. Most governance regimes have exception routes (chair's action, expedited review) precisely for this situation, and proposing one serves both the project and the process. Option B respects the rule but with no effort to help — governance as a wall rather than a service, which erodes support for governance itself. Option D is the subtle trap: a paper trail does not make an unauthorised procurement authorised, and "I wrote down that someone told me to" is not how public accountability works — accepting responsibility is not the PM's gift to give. Option A is least effective because it treats familiarity ("the same switches we always use") as a substitute for assurance; the board exists to catch exactly the assumptions everyone stopped checking. Transparency and proper process, pursued with urgency, is the public sector answer.

**Scenario 5 (moderate) — Conflicting requests, one of you**

At 14:00, three requests land at once. A service manager asks for utilisation data for a report due at 17:00 today. An engineer on site asks you to confirm a patching detail — the team is standing idle until you answer. Your senior architect, in meetings all afternoon, has asked for review comments on a design "by end of day if possible".

Possible actions:

A) Work in arrival order: service manager, engineer, architect.
B) Answer the engineer's patching question first, then the service manager's data request, then the review comments — messaging the architect that comments may arrive first thing tomorrow if time runs out.
C) Do the architect's review first, since your reporting line matters most.
D) Ask the service manager and the engineer to agree between themselves whose need is greater.

**Most effective: B. Least effective: D.**

**Explanation:** Option B sequences by real-world cost and constraint. The idle install team is burning money and schedule every minute — a patching confirmation is likely quick and unblocks several people (high urgency, low effort). The 17:00 report is a hard deadline with adequate remaining time. The review is explicitly flexible ("if possible"), and option B's proactive message manages that expectation honestly rather than silently dropping it. Option A mistakes arrival order for priority. Option C mistakes hierarchy for priority — your architect asked for something flexible and would not thank you for idling a site crew to deliver it. Option D is least effective: it outsources your prioritisation to two people who lack the full picture, delays both of them, and signals that you cannot triage — a core capability for anyone drafting plans and supporting live services. Notice the pattern that generalises: unblock others first, meet hard deadlines second, flex the flexible last, and communicate whenever you flex.

**Scenario 6 (moderate) — The accessibility objection**

In a design workshop for a new office network, a colleague proposes saving money by placing the only bookable video-conferencing room on a mezzanine floor accessible solely by stairs. Nobody else comments. You are the most junior person in the room.

Possible actions:

A) Stay quiet — accessibility is not a network architecture concern, and you are junior.
B) Raise it in the meeting: note that the proposal would exclude colleagues and visitors with mobility impairments, and ask whether an accessible location has been costed.
C) Say nothing in the meeting but mention it privately to your senior architect afterwards.
D) Report the colleague to HR for proposing an inaccessible design.

**Most effective: B. Least effective: A.**

**Explanation:** Inclusion is an explicit public sector value, and option B applies it in the moment it matters — while the decision is still open. The framing matters too: B raises the impact and asks a constructive question rather than accusing anyone; the colleague almost certainly overlooked the issue rather than dismissed it. Seniority does not gate this: pointing out that a proposal excludes people is always in scope, and workshops exist to catch exactly these problems. Option C is better than silence but risks the decision being minuted and momentum building before anyone revisits it; it also quietly teaches you that inclusion is someone else's job to voice. Option D wildly misreads the situation — an oversight in a workshop is an issue to raise, not misconduct to report, and jumping to formal escalation poisons collaboration. Option A is least effective because silence here has real victims: colleagues who cannot attend meetings in their own office. Speaking up early, factually, and kindly is a skill assessments reward and workplaces remember.

**Scenario 7 (hard) — Bad news near the deadline**

Your team is migrating an office to a new WAN service this weekend. On Thursday afternoon, while double-checking the plan you maintain, you find that the new circuit's delivered bandwidth is 100 Mbps, but the design — approved months ago, before you joined — assumed 200 Mbps. Peak usage data suggests the office will saturate the link on Monday morning. The migration has been announced, engineers are booked, and your senior architect is on leave until Monday.

Possible actions:

A) Proceed — the design was approved by people senior to you, and the migration is announced.
B) Contact the architect covering your senior's leave (or the duty design authority), present the figures, and recommend a decision on delaying or adding mitigations before the weekend.
C) Quietly configure traffic shaping to squeeze the peak into 100 Mbps and let the migration proceed as planned.
D) Email your senior architect, who is on leave, and proceed if no reply comes by Friday noon.

**Most effective: B. Least effective: A.**

**Explanation:** This scenario tests whether you understand that discovering the problem creates a duty to surface it to someone who can decide — before the point of no return. Option B does precisely that: it finds the live decision-maker (leave cover and duty authorities exist for exactly this), brings evidence rather than alarm, and offers options. It is also honest about your level: an associate should not unilaterally cancel a migration, and should not unilaterally proceed past a known saturation risk either. Option C is a technically flavoured version of hiding the problem — shaping might help, but deciding alone, silently, to run a degraded Monday for a whole office bypasses both governance and the service owner, and if it fails, no one upstream even knew there was a risk. Option D looks diligent but is escalation theatre: a no-reply deadline to someone on leave is consent manufactured from silence. Option A is least effective — "it was approved" describes the past, and approvals are only as good as their assumptions; you now hold evidence that a key assumption is false. Public sector values point one way here: transparency about problems, early, to the people accountable for the decision. Bad news does not improve with age.

**Scenario 8 (hard) — The supplier's friendly offer**

You are gathering information for a recommendation on network management tooling. A supplier's account manager, keen to win the contract, offers you and a friend tickets to a Premier League match "just to say thanks for engaging with us — no strings attached". Your recommendation draft is due next week.

Possible actions:

A) Accept — it is explicitly no-strings, and refusing seems rude.
B) Decline politely, check your department's gifts and hospitality policy, and record the offer in the register if the policy requires it; mention it to your senior architect.
C) Accept, but declare the tickets in the hospitality register.
D) Decline and drop the supplier from the evaluation for attempting to influence you.

**Most effective: B. Least effective: A.**

**Explanation:** You are actively evaluating this supplier: any significant hospitality accepted now could reasonably be seen to compromise — or appear to compromise — your impartiality, and in public procurement, appearance matters almost as much as fact. Option B declines, verifies the policy rather than guessing, creates the transparency record, and keeps your supervisor informed: every element models governance behaviour. Option C misunderstands registers — declaring a conflict does not neutralise it; hospitality from a supplier under live evaluation is generally to be refused, not merely logged. Option D overcorrects: a common (if clumsy) sales gesture is not grounds to skew a fair evaluation by excluding a potentially strong option, and doing so would itself make the evaluation unfair. Option A is least effective because "no strings attached" is not the supplier's call to make — the strings are structural, not stated. Note the general shape: integrity answers combine refusal of the risk, transparency about the event, and preservation of fairness in the process.

**Scenario 9 (hard) — Credit and the shared fix**

During a priority incident, you spot that a recent change added a routing entry that is black-holing traffic — the key insight that resolves a four-hour outage. In the wash-up meeting, the incident manager attributes the fix entirely to the on-call engineer, who says nothing to correct it. Your senior architect was not involved and does not know.

Possible actions:

A) Interrupt the meeting to set the record straight in detail.
B) Let it go entirely — outcomes matter, credit does not.
C) After the meeting, mention your contribution factually to the incident manager for the record, and tell your senior architect what you learned from the incident, focusing on the diagnostic method.
D) Post in the team channel that the fix was actually yours.

**Most effective: C. Least effective: D.**

**Explanation:** This is a judgement question about self-advocacy — a real skill, with real failure modes on both sides. Option C gets the record corrected through the right person (the incident manager owns the incident report), keeps the tone factual rather than aggrieved, and — importantly for an associate — converts the incident into visible professional development with your architect, which matters more for your growth than one meeting's applause. Option A makes a status contest out of a wash-up whose purpose is learning; even when you are right, the room remembers the interruption. Option B sounds noble but compounds over time: incident records inform recognition, progression, and who gets trusted with what, and systematically invisible contributions are a well-known career trap, especially for quieter team members — accuracy in records is not vanity. Option D is least effective: a public claim of credit in a team channel reads as grievance, puts the engineer on the defensive in front of everyone, and fixes nothing in the actual record. Accurate, low-drama, through-the-right-channel: that is the pattern.

**Scenario 10 (hard) — Ranking under pressure: the unauthorised workaround**

You discover that an engineer, frustrated by a slow firewall change process, has quietly installed a small unmanaged switch under a desk to bypass port restrictions for a project team. It works, the project team is delighted, and the engineer asks you to "keep it between us until the proper change goes through next month".

Rank these four actions from most to least effective:

1. Tell the engineer you cannot keep it quiet, and that it needs to be surfaced; encourage them to raise it themselves today, offering to help write the risk into the change request so the proper fix is expedited.
2. Report the device to the security team immediately without speaking to the engineer first.
3. Agree to stay quiet since the proper change is already in progress.
4. Remove the switch yourself as soon as the engineer walks away.

**Correct ranking: 1, 2, 4, 3.**

**Explanation:** Action 1 leads because it refuses the cover-up while preserving the relationship and accelerating the legitimate fix — surfacing the issue via the person who created it is both fair and effective, and your offer to help turns a confrontation into collaboration. Action 2 ranks second: it gets the security risk addressed, which is the non-negotiable core, but skipping the conversation costs trust unnecessarily when a same-day conversation was available — right outcome, avoidable collateral. Action 4 is third: it removes the risk but unilaterally, without understanding what depends on the link (you might break the project team's work mid-task), and it still leaves nothing on the record — a physical fix to a governance problem. Action 3 is last and decisively so: an unmanaged, undocumented device bypassing security controls is a live vulnerability, and "for a month" is a long time to knowingly conceal one; agreeing also makes you a party to it. The discriminating insight assessors look for: transparency is the fixed point, and the ranking among the rest turns on how much collaboration and process each option preserves while getting there.

**Scenario 11 (moderate) — The user who bypasses the service desk**

A senior civil servant from a policy team emails you directly: "The wifi in our wing has been dreadful all week and IT keeps closing our tickets. You're a network person — can you just fix it?" You check and see two closed tickets marked "no fault found", and you know a wifi survey for that wing was proposed but never funded.

Possible actions:

A) Reply that they must go through the service desk, and leave it there.
B) Quietly spend your afternoon investigating the wing's wifi yourself.
C) Reply promptly and warmly: explain what the closed tickets show, commit to raising the recurring pattern with the service desk and your senior architect, and mention the unfunded survey as relevant context the service owner should know.
D) Forward the email to the service desk manager with the comment "another complaint about your team".

**Most effective: C. Least effective: D.**

**Explanation:** Option C treats the user's experience as real data — two "no fault found" closures plus a persistent complaint plus a never-funded survey is a pattern, and patterns are exactly what an associate architect should surface to the people who own the service. It also respects the process without hiding behind it: the user gets a genuine response and a named next step, not a door. Option A is procedurally correct and practically useless; "raise another ticket" without addressing why tickets keep closing invites a fourth identical outcome and teaches senior stakeholders that the network team cannot help. Option B has generous instincts but poor judgement: unplanned solo investigation duplicates the service desk's role, bypasses your own team's priorities, and if you change anything, does so outside change control. Option D is least effective — it converts a service problem into an inter-team grievance, is disrespectful to colleagues, and would be mortifying if forwarded onwards, as emails often are. User needs first, transparency about what is known, collaboration between teams: option C is those values, operationalised.

**Scenario 12 (moderate) — Guidance that seems wrong**

Your senior architect, reviewing your draft, tells you to change a design to use a network pattern that you believe was deprecated by a departmental standard published last month — you read the standard carefully when it came out. The architect seems confident and is about to go into another meeting.

Possible actions:

A) Make the change as instructed — they are senior and presumably know better.
B) Say briefly: "I think last month's standard deprecated that pattern — can I send you the reference before I make the change?" and then follow whatever they decide with the reference in front of them.
C) Ignore the instruction and keep your original design, since the standard supports it.
D) Ask another senior architect whether your architect is right.

**Most effective: B. Least effective: C.**

**Explanation:** Option B is respectful challenge in its healthiest form: one sentence, evidence-based, perfectly timed (before the change is made), and it leaves the decision with the senior person once they have the reference — which is exactly how "with guidance" is supposed to work in both directions. Standards change monthly; seniors miss memos; associates who read carefully are valuable precisely because they catch this. Option A discards information you are confident about and lets a possible error flow into a governed document — deference is not diligence. Option C is the mirror error and the least effective: silently disobeying an explicit instruction breaks trust regardless of who is right about the standard, and being right in secret helps nobody at the review. Option D, done as a first resort, routes around your architect rather than talking to them — reasonable only after a direct conversation fails. The pattern to remember: raise evidence directly, promptly, and once; then commit to the informed decision.

### Preparation tips

- **Rehearse your role's relationships.** Before an assessment, spend time thinking about how an associate should interact with each stakeholder: seniors (use guidance actively, challenge with evidence), engineers (collaborate, respect practical knowledge), service desks and PMs (help through process, not around it), suppliers (friendly, fair, arm's length).
- **Learn the shape of strong answers.** Across the scenarios above, the most effective options share features: they act promptly, surface problems transparently, use the right channel, keep others informed, and move the work forward. The least effective options hide things, delay, personalise, or bypass.
- **Answer as your best professional self — not a fantasy self.** Choose what a conscientious associate would actually do, not what a heroic lone expert would do. Options where you single-handedly fix everything are usually traps at your level; options where you escalate thoughtfully usually are not.
- **Read the question format carefully.** "Most and least effective" asks for the two ends, not your favourite. Ranking asks for a full ordering. Marks are often available for the least-effective judgement even when the most-effective choice is debatable.
- **Reflect on real dilemmas you have seen.** Think back over your own weeks at work: a missed handover, a tense review, a tempting shortcut. Asking "what would the strongest response have been?" builds the judgement the test samples.
- **Do not over-strategise.** These assessments are validated against how effective professionals actually behave. Answering honestly, with public sector values in mind, beats trying to reverse-engineer a personality.

### Common pitfalls

- **Answering idealistically instead of practically.** "Convene a workshop to align all stakeholders" sounds lovely and is often the weak option when a five-minute conversation solves the problem. Effectiveness includes speed and proportion.
- **Selecting passive options.** The specification flags this directly: options that delay action, pass the problem wholesale to someone else, or wait for the situation to resolve itself are consistently rated poorly — waiting for a senior's return while a site crew stands idle is not humility, it is inaction.
- **Ignoring the values context.** In UK public sector scenarios, transparency, user needs, accessibility, and fair process are not tie-breakers — they are often the core of what is being tested. An operationally clever answer that hides information will score badly.
- **Overcorrecting into escalation.** Reporting a colleague to HR or security as a first move, when a direct conversation was available and safe, reads as poor judgement rather than strong ethics. Escalation is a tool, not a reflex — save the immediate formal route for genuine safety, security, or integrity red lines.
- **Confusing loyalty with silence.** Keeping a teammate's risky workaround secret, or letting an error stand to avoid embarrassment, fails both the teammate and the service. The strong options combine honesty about the problem with kindness toward the person.
- **Forgetting your level.** Some options are wrong not in substance but in station: unilaterally cancelling migrations, dropping suppliers, or overriding approved designs are not associate calls to make alone. The best associate answers pair initiative with appropriate escalation.

## Conclusion

Well done for working through this guide — that was a substantial piece of professional development, and you should feel genuinely proud of the effort.

You have now practised the four kinds of thinking that matter most in your work as an associate network architect. In the cognitive section, you spotted broken naming conventions, isolated faults by elimination, and checked designs against their specifications. In the numeric section, you converted SLA percentages into real minutes, projected capacity growth, and compared supplier costs the way an auditable recommendation demands. In the verbal section, you read policies, SLA schedules, standards, and engineers' emails with the strict, evidence-only discipline that assurance work requires. And in the situational judgement section, you rehearsed the trickiest part of any early-career role: knowing when to act, when to ask, when to challenge, and how to be transparent when things go wrong.

Notice how often the same themes recurred across all four sections: find the rule before hunting the exception; show your working; trust the text, not your assumptions; surface problems early; and pair initiative with honest escalation. Those are not just test techniques — they are the habits of an architect people trust, and practising them here strengthens them at your desk too.

What next? Little and often beats rarely and long: return to a handful of these questions in a week and see how much more quickly the reasoning comes. Practise on real (non-sensitive) artefacts from your own team — a design document, a monitoring dashboard, an SLA schedule — and quiz yourself the way this guide has. Talk to your senior network architect about which skills to stretch next, and consider keeping a short log of real workplace dilemmas and how they were handled; it is wonderful raw material for both assessments and your own growth.

Remember that assessments are a snapshot, never a verdict. Every skill in this guide is learnable, and at associate level you are exactly where learning happens fastest. Approach your assessment rested, curious, and unhurried — you have prepared well, and you have every reason to walk in with confidence. Good luck, and enjoy the career you are building.

---

Professional development tip: revisit this resource regularly. Skills compound — a few practice questions each week will do more for you than an occasional marathon session.
