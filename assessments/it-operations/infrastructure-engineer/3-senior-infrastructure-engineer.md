# Senior Infrastructure Engineer - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a senior infrastructure engineer working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply curious about how psychometric assessments relate to your day-to-day work, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the mental capabilities and behavioural tendencies that predict success in a role. For a senior infrastructure engineer, that means far more than abstract puzzles. The assessments described here are job-specific: they use the kinds of artefacts you genuinely handle — architectural designs awaiting translation into operations, design review packs, integration build plans, test condition sets, capacity and budget inputs, supplier performance data — and the kinds of decisions you genuinely make: designing systems of medium risk and complexity, selecting design standards and ensuring they are applied, reviewing the designs of others, coordinating build activities across systems, initiating investigations into patterns and trends, and determining resolutions and preventative measures.

Why do these assessments matter for your role in particular? At senior level you occupy the hinge point between architecture and operations. Technical architects hand you designs; you make them run. Junior engineers hand you their designs and their problems; you review, guide, and unblock. Management asks for your input on workforce, budget, technology roadmaps, projects, and tasks. Every one of those flows demands the abilities these assessments measure: rapid, accurate pattern analysis across complex artefacts; valid deduction from standards and constraints; disciplined reading of dense technical and contractual text; and sound judgement about people, priorities, and risk. Practising them sharpens exactly what your role runs on.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and why employers use it for this role, a mapping of the assessment dimensions to the specific named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. Questions progress from easy through moderate to hard, and the harder items deliberately reflect senior-level texture: reviewing others' work, weighing competing constraints, leading small teams through ambiguity, and consulting specialists at the right moment.

Here is how to get the most from it. First, read each "About this assessment" section so the format holds no surprises. Second, attempt every practice question honestly — commit to an answer before reading the explanation. Third, mine the explanations even when you were right: each one demonstrates a transferable technique and ties it back to a specific senior responsibility. Fourth, use the preparation tips and pitfalls for self-reflection — several are really about how you review, coordinate, and lead, which is where senior engineers earn their title.

Assessment performance and senior engineering excellence draw on the same well: calm, structured, evidence-led thinking under time pressure. The practice you do here is practice for the job itself. Take your time, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment measures the exact mental processes your role demands, using practical workplace scenarios rather than abstract puzzles. For a senior infrastructure engineer, the materials are the ones that cross your desk daily: architectural design documents, resilience and capacity specifications, integration sequence plans, test condition matrices, monitoring trend data, and the design work of less experienced colleagues awaiting your review.

The typical format is an online, timed test lasting 15 to 30 minutes, with 20 to 30 questions covering pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group of professionals at a comparable level; adaptive difficulty is common, and employers usually receive speed and accuracy separately, so disciplined precision is rewarded alongside pace.

At senior level, the cognitive demand shifts in a particular way: you are less often the person producing the artefact and more often the person verifying it, integrating it, or deciding on the strength of it. Reviewing a colleague's system design for appropriate technology selection and efficient resource use is sustained error checking against multiple simultaneous criteria. Translating an architect's design into operations is deduction — what must physically and procedurally follow from these stated properties? Initiating investigations into patterns and trends is inductive reasoning over noisy operational data. Coordinating build activities across systems is constraint satisfaction with real deadlines. Employers assess cognition at this level because a senior engineer's errors are multiplied by the teams and systems downstream of them — and because the role's defining moves, review and integration, are precisely the moves these tests isolate.

### How this assessment maps to your role

The assessment dimensions map directly to the named skills in your role summary:

- **Pattern recognition** maps to your **Problem management** skill: initiating and monitoring actions to investigate patterns and trends means detecting recurring signatures across incidents, metrics, and time — separating genuine signal from coincidence.
- **Logical deduction** maps to your **Systems design** skill (designing systems of medium risk, impact, and complexity requires reasoning validly from requirements and standards to consequences) and to your role-level duty to work with technical architects to translate architectural designs into operations.
- **Error checking** maps to your **Systems design** review duty — reviewing the systems designs of others to ensure appropriate technology selection, efficient use of resources, and integration of multiple systems — and to your **Testing** skill of reviewing requirements and specifications and defining test conditions.
- **Prioritisation** maps to your **Ownership and topic** skill (owning issues until resolution or handover) and your duty to provide input into overall management — workforce, budget, technology roadmaps, projects, and tasks — which is prioritisation formalised.
- **Applied problem solving** maps to your **Troubleshooting and problem resolution** skill: breaking a problem down into its component parts to identify and diagnose root causes, across different technology capabilities.
- **Structural reasoning about integration** maps to your **Systems integration** skill: defining the integration build and coordinating build activities across systems is dependency and sequence logic under resource constraints.

### Practice questions

**Question 1 (easy) — Pattern recognition across an incident history**

You are reviewing six months of priority incidents for a service to decide whether to initiate a problem investigation:

| Month | Incidents | Notes |
|---|---|---|
| March | 2 | Both storage latency, last week of month |
| April | 1 | Network failover test issue |
| May | 3 | All storage latency, last week of month |
| June | 1 | Application defect |
| July | 2 | Both storage latency, last week of month |
| August | 3 | All storage latency, last week of month |

Which pattern most warrants a problem investigation?

- A) Incident counts are rising month on month
- B) Storage latency incidents recur in the last week of each month, and their frequency is growing
- C) Network failover testing is unreliable
- D) Application defects are the dominant incident type

**Correct answer: B**

**Explanation:** Separate the recurring signature from the noise. Storage latency appears in four of six months — always in the last week, with counts moving 2, 3, 2, 3 — a repeating time-locked pattern with a mild upward drift. That combination (recurrence, time correlation, growth) is precisely what your **Problem management** skill exists to catch: a month-end process — reporting runs, billing batches, archive jobs — is plausibly saturating storage, and the trend says it will worsen. Option A is false: counts go 2, 1, 3, 1, 2, 3 — not monotonic. Options C and D each generalise from a single incident. The technique: tabulate by type and by time before judging; patterns invisible in a chronological list leap out of a cross-tabulation. Seniors add the judgement layer — one-off incidents get fixed, recurring signatures get problem records — and knowing which is which is the difference between firefighting and problem management.

**Question 2 (easy) — Deduction from an architectural requirement**

An architect's design states: "The service must survive the loss of any single data centre without user-visible interruption. Session state must not be lost during such an event." The current operational proposal runs two application servers, both in Data Centre 1, with session state held in each server's local memory. Which conclusion must be true?

- A) The proposal fails both requirements: a Data Centre 1 loss interrupts the service, and local session state would be lost.
- B) The proposal meets the requirements because two servers provide redundancy.
- C) The proposal meets the availability requirement but not the session requirement.
- D) The requirements cannot be met with only two servers.

**Correct answer: A**

**Explanation:** Test the proposal against each requirement independently. Requirement 1: survive loss of any single data centre. Both servers sit in Data Centre 1, so losing that centre removes every server — the service stops. Failed. Requirement 2: session state survives such an event. State lives in the memory of servers that would all be lost. Failed. Both requirements fail: option A. Option B mistakes server-level redundancy for site-level redundancy — the failure domain the requirement names is the data centre, not the server, and redundancy only counts when instances sit in different failure domains. Option D overreaches: two servers in different centres with externalised session state (a replicated session store) could satisfy both requirements — the count is not the problem, the placement and state design are. This is the exact reasoning of your duty to translate architectural designs into operations: extract each stated property, identify its failure domain, and verify the physical arrangement preserves it.

**Question 3 (easy) — Error checking a test condition set**

The requirement reads: "Users in the Finance group can read and write to the ledger share. Users in the Audit group can read but not write. Users in neither group have no access." A junior colleague drafts these test conditions: (1) Finance user can write — expect success. (2) Audit user can read — expect success. (3) Audit user can write — expect failure. (4) Finance user can read — expect success. Which important condition is missing?

- A) Finance user attempts to delete the share
- B) A user in neither group attempts to read — expect failure
- C) Audit user reads twice in succession
- D) Finance user writes a large file

**Correct answer: B**

**Explanation:** Map the conditions against the requirement's three clauses. Finance read/write: covered by conditions 1 and 4. Audit read allowed, write denied: covered by 2 and 3. "Users in neither group have no access": untested — nothing verifies that an outsider is denied. That is the gap, and it is the most security-significant clause in the requirement: the failure mode it guards against is unauthorised access to a ledger. Negative-path conditions — verifying that forbidden things fail — are systematically under-written by inexperienced testers, because intuition tests what should work. Options A, C, and D add volume, repetition, or destructive cases the requirement does not mention; they might belong in a fuller suite, but none addresses a stated clause. This is your **Testing** skill operating at review altitude: reviewing requirements and specifications and defining test conditions means checking coverage clause by clause, with special attention to every "not" and "no" in the text.

**Question 4 (easy) — Prioritisation across senior responsibilities**

Four items reach you on Monday morning: (1) a P3 problem investigation you own has new evidence available; (2) a junior engineer is blocked on a production change scheduled for tonight, awaiting your design review; (3) the monthly capacity report you contribute to management is due Friday; (4) a technical architect requests a meeting this week about operationalising a new design. What should you address first?

- A) Item 1 — problem investigations underpin prevention
- B) Item 2 — a colleague is blocked now on work with a hard deadline tonight
- C) Item 3 — management reporting takes precedence
- D) Item 4 — architects outrank other stakeholders

**Correct answer: B**

**Explanation:** Apply impact-weighted urgency. Item 2 combines a hard same-day deadline (tonight's change window) with a blocked person — every hour of your delay consumes their preparation time and raises tonight's risk, and unblocking others is a defining senior duty. Items 3 and 4 have week-scale deadlines that permit scheduling: a reply proposing a meeting slot for the architect and a calendar block for the report cost minutes. Item 1's evidence will keep; problems are important precisely because they are not urgent in the incident sense. Options C and D rank by stakeholder seniority — a heuristic that fails whenever a junior colleague's blocked change outweighs a movable meeting, which is often. The senior-level refinement worth noticing: the correct sequence is not just "2 first" but "2 now, then two-minute scheduling responses to 3 and 4, then 1" — prioritisation at this level is mostly about cheap early communication that converts waiting stakeholders into scheduled ones.

**Question 5 (moderate) — Pattern recognition in capacity trend data**

Reviewing quarterly storage consumption for four services, you see: Service W: 10 TB, 11 TB, 12 TB, 13 TB. Service X: 8 TB, 8 TB, 9 TB, 8 TB. Service Y: 5 TB, 7 TB, 10 TB, 14 TB. Service Z: 20 TB, 20 TB, 21 TB, 20 TB. Which service presents the most pressing capacity planning concern?

- A) Service W — it grows every quarter
- B) Service X — its consumption is unstable
- C) Service Y — its growth is accelerating
- D) Service Z — it consumes the most storage

**Correct answer: C**

**Explanation:** Distinguish level, linear growth, and acceleration. Service Z has the highest level but is flat — a budget line, not a planning risk. Service W grows linearly at 1 TB per quarter — predictable, easily planned. Service X oscillates within 1 TB — noise. Service Y's increments are 2, 3, 4 TB — growth that is itself growing. Extrapolate the pattern: next increments of roughly 5 and 6 TB take it to about 25 TB in two quarters — from smallest consumer to largest, and accelerating curves defeat the straight-line assumptions procurement plans are usually built on. Option C. The reasoning habit — look at differences between periods, then differences of the differences — takes seconds and changes conclusions. This feeds directly into your role-level duty to provide input into budgets and technology roadmaps: the service that needs money next year is identified by curvature today, and the senior engineer who reports "Y is accelerating" rather than "Z is biggest" is the one whose management input is worth having.

**Question 6 (moderate) — Deduction through integration sequencing**

You are defining the integration build for a new case-management service touching four systems. Constraints: (i) the identity integration must be complete before user-acceptance testing (UAT) of any other integration; (ii) the document-store integration needs three weeks of build; (iii) the notification integration needs one week of build and shares a build team with the document-store work, so they cannot run in parallel; (iv) identity needs two weeks of build, done by a separate team, and its own one week of UAT; (v) each non-identity integration needs one week of UAT after both its build and the identity UAT are complete. Builds may start immediately. What is the earliest week by which all UAT can finish?

- A) End of week 5
- B) End of week 6
- C) End of week 7
- D) End of week 8

**Correct answer: A**

**Explanation:** Schedule each track. Identity team: build weeks 1–2, UAT week 3 — identity UAT complete end of week 3. Shared build team: the two builds cannot overlap; order them document-store first (weeks 1–3) then notification (week 4), or notification first (week 1) then document-store (weeks 2–4) — either way the shared team finishes building at end of week 4. UAT for each non-identity integration needs its build done and identity UAT done (end of week 3). Take notification-first ordering: notification build done end of week 1, but its UAT must wait for identity UAT, so it runs week 4; document-store build done end of week 4, UAT week 5. All UAT complete end of week 5 — option A. Check the other ordering: document-store UAT week 4, notification build done week 4, UAT week 5 — same result. The senior insight: the shared team is the true constraint (four weeks of serialised build), and the identity prerequisite costs nothing extra because it completes inside that shadow. Defining the integration build — your **Systems integration** skill — is exactly this: find the binding constraint, sequence around it, and refuse to accept option C or D timescales that unexamined intuition suggests.

**Question 7 (moderate) — Error checking a design review submission**

A junior engineer submits a design for a departmental file service: "Two file servers in an active-passive pair using synchronous replication between Data Centre 1 and Data Centre 2. Failover is manual, performed by the on-call engineer following runbook FS-12, expected completion 15 minutes. The service tier requires recovery within 30 minutes (RTO) with zero data loss (RPO). Backups run nightly to meet the zero-data-loss requirement."

Which statement in the design is internally inconsistent with the stated requirements?

- A) The claim that manual failover meets the 30-minute RTO
- B) The claim that nightly backups meet the zero-data-loss requirement
- C) The use of active-passive rather than active-active
- D) The use of synchronous replication between data centres

**Correct answer: B**

**Explanation:** Check each claim against the requirement it cites. RTO 30 minutes: manual failover at 15 minutes expected leaves margin — tight if the on-call engineer is slow to respond, worth a comment, but not internally inconsistent as claimed (option A is a judgement point, not a contradiction). Active-passive (option C) and synchronous replication (option D) are legitimate choices — indeed synchronous replication is what actually delivers zero data loss for committed writes. The inconsistency is option B: nightly backups protect against data loss of up to 24 hours, so they cannot "meet the zero-data-loss requirement" — the design attributes the RPO to the wrong mechanism. The correction: synchronous replication meets the RPO; backups serve a different purpose (corruption, deletion, ransomware recovery) and should be justified as such. This is the essence of your design review duty: verify not only that each requirement is addressed, but that it is addressed by a mechanism actually capable of delivering it — misattributed compliance is the subtlest and most common review finding, because every requirement appears to have an answer.

**Question 8 (moderate) — Root-cause decomposition**

A nightly data transfer to an external partner has failed three times in two weeks, each time with a different symptom: once a timeout, once a certificate error, once a partial file. The junior engineer investigating proposes: "Three different errors means three different problems — we should raise three problem records." As the senior engineer, which response reflects the best diagnostic reasoning?

- A) Agree — distinct symptoms imply distinct causes.
- B) Disagree — three failures of one interface in two weeks suggests looking for a common underlying factor first, such as a change in the network path, an expiring credential chain, or an unstable connection, with the varied symptoms as different downstream expressions of it.
- C) Disagree — the most recent error is the only one worth investigating.
- D) Agree, but investigate only the certificate error because security matters most.

**Correct answer: B**

**Explanation:** Symptom diversity does not imply cause diversity. A single unstable network path can produce a timeout (connection stalls), a partial file (connection drops mid-transfer), and even a certificate error (handshake interrupted or failing over to a host presenting a different certificate). Base rates matter too: one interface failing three times in a fortnight after presumably long stability makes one new underlying factor more probable than three independent new faults arriving together. The diagnostic method — your **Troubleshooting and problem resolution** skill's "break a problem down into its component parts" — starts by laying the three failures on a common timeline against changes (network, certificates, partner-side maintenance), looking for the shared layer in the stack, and only splitting into multiple investigations when a common factor is positively excluded. Option A multiplies process before thought. Option C discards two-thirds of the evidence — the variety itself is diagnostic. Option D lets category importance override causal reasoning. The mentoring dimension is real, too: how you correct this proposal teaches the junior engineer inference, not just this week's answer — consult, explain the reasoning, and let them run the timeline exercise.

**Question 9 (moderate) — Prioritisation of preventative measures**

Your problem investigation into recurring authentication slowdowns identifies four contributing factors, with an estimate of implementation effort and recurrence reduction for each remedy: (1) increase directory server memory — 1 day effort, prevents ~30% of recurrences; (2) re-time the replication schedule away from peak logins — 2 days effort, prevents ~50% of recurrences; (3) replace the ageing directory servers — 40 days effort and capital spend, prevents ~90% of recurrences; (4) add monitoring alerts for replication lag — 1 day effort, prevents no recurrences but cuts detection time from hours to minutes. Which implementation order is most defensible?

- A) 3 first — it prevents the most
- B) 4, 2, 1, then propose 3 through the roadmap: quick detection first, then the highest-value cheap preventions, with the capital replacement planned properly
- C) 1, 2, 3, 4 — ascending effort order
- D) 2 only — it prevents the majority, so the rest are unnecessary

**Correct answer: B**

**Explanation:** Rank by value density (benefit per unit of effort and delay) while respecting decision boundaries. Item 4 costs one day and transforms every future occurrence — including those during the weeks before other remedies land — from a long outage into a short one; detection improvements pay out immediately and are almost never wrong to do first. Item 2 is the prevention bargain: two days for half the recurrences. Item 1 adds another 30% for a day. Item 3 is the right long-term answer but is a capital project: forty days and spend of that scale belong in the technology roadmap and budget process — exactly the management input your role level provides — not in a problem record's immediate actions; option A would leave users exposed for weeks while the big fix mobilises. Option C sequences by effort while ignoring that 4's benefit is categorically different (detection versus prevention) and 2 dominates 1. Option D confuses "majority" with "sufficient" — the remaining recurrences still hurt, and the marginal day for item 1 is cheap. This layered remedy thinking — determine the appropriate resolution and preventative measures, staged by value and governance — is your **Problem management** skill exercised at senior level.

**Question 10 (hard) — Deduction across interacting constraints**

You must place six virtual machines (A–F) across two hosts (Host 1 and Host 2) subject to: (i) A and B are a resilient pair and must be on different hosts; (ii) C must be co-located with A for latency; (iii) D must not share a host with B, due to licence terms; (iv) E and F must be together on either host; (v) each host can hold at most four VMs. Which placement is valid?

- A) Host 1: A, C, D, E — Host 2: B, F
- B) Host 1: A, C, D — Host 2: B, E, F
- C) Host 1: B, C, D — Host 2: A, E, F
- D) Host 1: A, C, E, F — Host 2: B, D

**Correct answer: B**

**Explanation:** Apply each constraint to each option, eliminating on the first violation. Option A: E and F are split across hosts — violates (iv). Option C: C sits with B on Host 1 while A is on Host 2 — violates (ii); additionally D shares Host 1 with B — violates (iii). Twice invalid. Option D: A, C, E, F on Host 1 satisfies (i), (ii), (iv), and the count of four is within (v) — but D sits on Host 2 with B, violating (iii). Option B: A and B on different hosts ✔ (i); C with A ✔ (ii); D on Host 1, B on Host 2 — not sharing ✔ (iii); E and F together on Host 2 ✔ (iv); counts 3 and 3 ✔ (v). Valid. The efficient technique is constraint propagation rather than option-checking from scratch: fix A on Host 1 (symmetry allows it), then B is forced to Host 2 by (i), C to Host 1 by (ii), D to Host 1 by (iii), and E and F must go together wherever capacity remains — Host 2 — reproducing option B directly. Placement problems with anti-affinity, affinity, and licence constraints are literal daily work in virtualisation management, and the deduce-forced-moves-first method scales to the twenty-VM versions the real world supplies.

**Question 11 (hard) — Evaluating evidence quality in an investigation**

Investigating intermittent database timeouts, you have four pieces of evidence: (i) timeouts cluster between 08:30 and 09:30 on weekdays; (ii) a colleague recalls that "the SAN always struggles in the mornings"; (iii) storage latency metrics for the database volumes show flat, healthy values across all times; (iv) application connection-pool metrics show pool exhaustion coinciding with each timeout cluster. Which conclusion best respects the evidence?

- A) The SAN is the likely cause, consistent with the colleague's experience.
- B) The evidence is contradictory, so no investigation direction can be chosen.
- C) The measured evidence points away from storage and towards connection-pool exhaustion under morning login load; the recollection should be noted but not allowed to outweigh the metrics.
- D) The timeouts are random and the morning clustering is coincidence.

**Correct answer: C**

**Explanation:** Weigh evidence by its epistemic quality. Items (i), (iii), and (iv) are measurements; item (ii) is an unquantified recollection — honestly offered, possibly rooted in past reality, but it concerns the SAN in general while (iii) directly measures the relevant volumes and finds them healthy. Where a specific measurement and a general memory conflict, the measurement wins — though the professional move is to note the recollection and verify the SAN metrics' coverage rather than dismiss the colleague. The positive case: (iv) shows pool exhaustion coinciding with every cluster, and (i)'s timing matches the morning login surge — mechanism and timing cohere, giving a testable hypothesis (raise pool limits or stagger logins in a controlled way and observe). Option A privileges anecdote over instrumentation — the commonest failure in real investigations, because anecdotes arrive with confidence attached. Option B mistakes "one weak source disagrees" for contradiction. Option D ignores (i)'s strong regularity. Your **Problem management** skill's "effectively consult specialists where required" includes this calibration: consult widely, weigh what you hear by how it was known, and let instrumented evidence arbitrate.

**Question 12 (hard) — Operationalising a design under constraint conflict**

A technical architect's design for a new service specifies: (i) all inter-site replication traffic must be encrypted; (ii) replication lag must not exceed 5 seconds; (iii) the existing inter-site link must be used, with 200 Mbps of the link reserved for replication. Your operational testing finds: encrypted replication over the reserved 200 Mbps sustains the required data rate but with lag spiking to 12 seconds at peak write times; unencrypted replication meets the 5-second lag comfortably; upgrading the link or its encryption hardware is possible but needs procurement. Which response best fulfils your role?

- A) Deploy unencrypted replication — the lag requirement is operationally decisive.
- B) Deploy encrypted replication as designed and accept the 12-second lag without further action.
- C) Document the conflict with your test evidence, take it back to the architect with quantified options — hardware acceleration, link upgrade, write-shaping, or a formally accepted revised lag target — and implement the agreed resolution; meanwhile do not deploy a configuration that silently breaches either requirement.
- D) Deploy encrypted replication but change the recorded lag requirement in the design document to 15 seconds so the deployment complies.

**Correct answer: C**

**Explanation:** The testing has discovered that requirements (i) and (ii) cannot both be met under constraint (iii) — a genuine design conflict, and resolving requirement conflicts is a design authority decision, not an operational one. Option C is the role-faithful response your level's duty describes: "work with technical architects to translate architectural designs into operations" cuts both ways — you carry designs into operation, and you carry operational evidence back into design. Bringing quantified options rather than a bare problem is what makes the conversation productive, and refusing to deploy a silently non-compliant configuration in the interim protects the service's integrity either way. Option A unilaterally discards a security requirement — encryption mandates usually trace to information-security policy, and no lag figure licenses an engineer to waive them. Option B silently accepts a 140% breach of a stated requirement; systems downstream may depend on the 5-second bound. Option D is falsification: editing a requirement to match an implementation inverts the entire relationship between design and operations and destroys the document's authority. The general pattern for seniors: when reality refutes a design, escalate the refutation with evidence and options — never absorb it in silence, never paper over it in the record.

### Preparation tips

- **Practise review, not just production.** Take a design, a test plan, or a runbook a colleague wrote and verify it clause against requirement. Reviewing others' work — your daily senior duty — is precisely the error-checking skill the test samples.
- **Tabulate before judging.** Incident histories, capacity series, and constraint sets give up their patterns to a quick table or difference sequence. Build the reflex of restructuring data before reasoning about it.
- **Work forced moves first in constraint problems.** Fix one element, propagate what it forces, and most placement or sequencing questions collapse. Option-by-option checking is the slow fallback.
- **Demand mechanism-plus-timing from causes.** In diagnostic questions, the right answer explains onset, recovery, scope, and pathway. Reject candidates that fit only one dimension.
- **Rank remedies by value density.** Benefit per unit of effort and delay, with detection improvements treated as a separate, usually first, category. This mirrors both test questions and real problem-record actions.
- **Time-box under mild pressure.** Aim for 60–90 seconds per question in practice. Senior candidates rarely lack accuracy; deliberate pacing practice buys the speed without sacrificing it.
- **Use your own estate as the gym.** Yesterday's monitoring data, last month's incident list, and the current design pack are richer practice material than any generic question bank — and studying them is simply doing your job attentively.

### Common pitfalls to avoid

- **Reviewing for presence, not sufficiency.** The subtle design flaw is a requirement answered by a mechanism that cannot deliver it. Check what each mechanism can actually do.
- **Letting anecdote outweigh instrumentation.** Confident recollection is data about memory, not about systems. Weigh evidence by how it was obtained.
- **Equating symptom diversity with cause diversity.** Multiple different failures of one component in a short window usually share a factor. Exclude the common cause before multiplying investigations.
- **Ranking by stakeholder seniority.** Architects and management matter, but impact-weighted urgency decides sequence — and the blocked junior with tonight's change often comes first.
- **Choosing the biggest fix first.** Capital-scale remedies belong in roadmaps; the test (and the job) rewards staging quick detection and cheap prevention ahead of them.
- **Silently absorbing requirement conflicts.** When constraints cannot all be met, the failing option is any that hides the fact — by breaching quietly, waiving unilaterally, or editing the record. Escalate with evidence.
- **Skipping the negative paths.** In any coverage question — tests, permissions, monitoring — the missing item is usually the "must not" clause. Hunt the negations.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the quantities your role genuinely handles — and at senior level, that set widens considerably. Alongside the engineer's staples of capacity, utilisation, availability, and throughput, you now contribute to workforce planning, budget inputs, technology roadmaps, and supplier performance assessment. The underlying mathematics remains deliberately accessible — percentages, ratios, averages, rates, weighted combinations, and reading tables and charts — but the data is denser, the questions demand more interpretation, and the answers feed decisions with money and people attached.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions, each presenting a realistic data set — a capacity trend, a cost comparison, an SLA report, a team utilisation table — followed by a multiple-choice question. Calculators are generally permitted, rough paper is essential, and scoring compares accuracy and speed against a norm group at a comparable level, often adaptively.

Why do employers assess numeric reasoning for senior infrastructure engineers? Because at this level your numbers become other people's decisions. Your capacity forecast shapes next year's budget bid. Your availability analysis determines whether a supplier earns or loses at contract review. Your sizing calculations get built — by teams you lead — into systems the department depends on. Your input to management on workforce and projects is credible only if the arithmetic beneath it survives scrutiny. A senior engineer who misreads a weighted average or projects a trend from the wrong baseline does not just drop a mark; they misdirect investment. The assessment samples, in miniature, exactly the numerical judgement the role exercises at scale — and, like every skill in this guide, it improves rapidly with deliberate practice.

### How this assessment maps to your role

- **Capacity and sizing arithmetic** maps to your **Systems design** skill: designing systems of medium risk and complexity, and reviewing others' designs for efficient use of resources, means deriving and verifying node counts, storage volumes, and throughput figures rather than accepting them.
- **Trend analysis and forecasting** maps to your **Problem management** skill (initiating investigations into patterns and trends) and your role-level duty to provide input into technology roadmaps: quantified trends are what turn monitoring history into roadmap and budget lines.
- **Availability and SLA calculations** map to your duty to ensure services are integrated, delivered, and operated as required, and to your work with third parties: supplier performance is judged in percentages, minutes, and credits, and you must be able to check every figure.
- **Cost and comparison arithmetic** maps to your input into overall management — budget, projects, and tasks — where option comparisons, run-rate projections, and per-unit costs are the standard currency.
- **Test and defect metrics** map to your **Testing** skill: analysing and reporting test activities and results means working with pass rates, defect densities, and coverage percentages accurately.
- **Workload and team figures** map to your role-level duty to provide input into workforce planning and, on the managerial path, to lead infrastructure specialist teams: rota coverage, utilisation, and effort estimates are ratio problems with people in them.

### Practice questions

**Question 1 (easy) — Utilisation headroom**

A virtualisation cluster has 512 GB of usable memory across its hosts, with 384 GB currently allocated. What percentage headroom remains?

- A) 20%
- B) 25%
- C) 30%
- D) 33%

**Correct answer: B**

**Explanation:** Step 1: free memory = 512 − 384 = 128 GB. Step 2: headroom percentage = 128 ÷ 512 × 100. Step 3: 128 ÷ 512 = 0.25, so 25%. Sanity check via the complement: allocated fraction = 384 ÷ 512 = 0.75 = 75%, and 100 − 75 = 25 ✔. Note the phrasing discipline: the question asks for headroom (free ÷ total), not utilisation (used ÷ total) — option D (33%) is the classic error of computing free as a percentage of used (128 ÷ 384) rather than of total. In cluster management the distinction matters operationally too: headroom against total capacity is what determines whether the cluster can absorb a host failure, which is the figure your design reviews should be checking.

**Question 2 (easy) — Mean time between failures**

A tape library failed on 4 occasions during 200 days of continuous operation. What is its mean time between failures (MTBF) in days?

- A) 40 days
- B) 50 days
- C) 60 days
- D) 80 days

**Correct answer: B**

**Explanation:** MTBF = operating time ÷ number of failures = 200 ÷ 4 = 50 days. The common slip is dividing by failures-plus-one (200 ÷ 5 = 40, option A) on the intuition that four failures create five intervals — a defensible model in some statistics texts, but the standard operational MTBF convention, and the one assessments use, is time divided by failure count. Keep the interpretation honest too: an MTBF of 50 days is an average over a small sample of four events — it does not promise 50 failure-free days, and the next failure could be tomorrow. When you use figures like this to support replacement proposals in roadmap discussions — a genuine senior task — quote the sample size alongside the average, because a decision-maker who later sees two failures in a week deserves to have known how thin the data was.

**Question 3 (easy) — Availability target conversion**

A service has a 99.9% availability target measured monthly. In a 30-day month (43,200 minutes), what is the maximum permitted downtime?

- A) 14.4 minutes
- B) 43.2 minutes
- C) 144 minutes
- D) 432 minutes

**Correct answer: B**

**Explanation:** Permitted downtime = (100% − 99.9%) × total minutes = 0.1% × 43,200. Step 1: convert the percentage to a fraction: 0.1% = 0.001. Step 2: 0.001 × 43,200 = 43.2 minutes. Options A, C, and D are all decimal-placement errors — treating 0.1% as 0.0333%, 0.333%, or 1% — and misplacing the decimal in the percentage-to-fraction conversion is the single most common error in availability arithmetic, which is why writing the fraction explicitly before multiplying is worth the extra two seconds. A senior habit worth forming: memorise the anchor conversions — 99.9% monthly ≈ 43 minutes, 99.5% ≈ 3.6 hours, 99% ≈ 7.2 hours — because in supplier meetings and design reviews you will need to translate targets into felt downtime instantly, and the engineer who can say "99.9% means one 43-minute outage a month, is that acceptable to the business?" moves the conversation from abstraction to decision.

**Question 4 (easy) — Reading a supplier performance table**

A supplier's quarterly report shows response-time performance against a 30-minute target for P1 incidents:

| Month | P1 incidents | Responded within target |
|---|---|---|
| April | 8 | 7 |
| May | 5 | 5 |
| June | 12 | 9 |

The contract requires 90% within target, measured quarterly. Did the supplier meet the quarterly requirement?

- A) Yes — 84% is within tolerance
- B) Yes — two of three months individually exceeded 90%
- C) No — quarterly performance was 84%, below the 90% requirement
- D) No — quarterly performance was 87.5%, below the 90% requirement

**Correct answer: C**

**Explanation:** The contract measures quarterly, so aggregate the raw counts — never average the monthly percentages. Step 1: total P1 incidents = 8 + 5 + 12 = 25. Step 2: total within target = 7 + 5 + 9 = 21. Step 3: quarterly performance = 21 ÷ 25 = 0.84 = 84%. Against a 90% requirement, the supplier missed — option C. Option B commits the measurement-period error: monthly figures (87.5%, 100%, 75%) are informative for diagnosis — June is where performance collapsed — but the contractual test is the quarterly aggregate. Option D is the unweighted mean of the monthly percentages ((87.5 + 100 + 75) ÷ 3 = 87.5%), wrong because the months carry different incident volumes. Reading contracts' measurement definitions and computing accordingly is core to your duty to work with and support third parties: suppliers will naturally present whichever cut flatters them, and the senior engineer at the service review must be able to reproduce the contractual figure from raw counts before the meeting.

**Question 5 (moderate) — Growth projection with a step change**

A backup repository holds 60 TB, growing at 2 TB per month. A new service onboarding at the start of month 4 will add an immediate 10 TB and increase ongoing growth to 3 TB per month from month 4 onwards. The repository's capacity is 100 TB. At the end of which month does the repository first reach full capacity?

- A) Month 9
- B) Month 11
- C) Month 12
- D) Month 14

**Correct answer: B**

**Explanation:** Model the two phases separately and add the step change at its stated boundary. Phase 1 (months 1–3 at 2 TB/month): end of month 3 = 60 + (3 × 2) = 66 TB. Phase 2: the onboarding adds 10 TB at the start of month 4 (66 + 10 = 76 TB), and growth runs at 3 TB/month from month 4, so end of month 4 = 79 TB. Remaining headroom: 100 − 79 = 21 TB, consumed at 3 TB/month in 21 ÷ 3 = 7 further months — end of month 11. Verify with the month-by-month table: m5 = 82, m6 = 85, m7 = 88, m8 = 91, m9 = 94, m10 = 97, m11 = 100. Option B. Option D (month 14) is what you get by forgetting the immediate 10 TB step; option C by applying the new growth rate but adding the step a month late; option A by applying the 3 TB rate from month 1. The general lessons for roadmap input: step changes must land exactly at their stated boundary, rate changes apply from their stated month, and the month-by-month table is worth its thirty seconds — reviewers can check a table at a glance, and a projection like this one (full in under a year) is precisely what justifies a procurement line in next year's budget.

**Question 6 (moderate) — Test metrics for a release decision**

Your team's integration testing for a release executed 240 test conditions: 216 passed, 18 failed, 6 blocked (could not run because of environment faults). Policy requires a 95% pass rate of executed-and-completed tests, with no blocked tests outstanding, before release. Which statement is correct?

- A) Pass rate is 90%, so the release fails on pass rate alone.
- B) Pass rate is 92.3%, and the blocked tests also prevent release.
- C) Pass rate is 92.3%, which meets the threshold, but the blocked tests prevent release.
- D) Pass rate is 90%, and blocked tests do not matter because they were not executed.

**Correct answer: B**

**Explanation:** Compute the pass rate on the correct base: "executed-and-completed" excludes the blocked tests, so the base is 240 − 6 = 234. Step 1: 216 ÷ 234 = 0.923 = 92.3%. Step 2: compare with the 95% threshold: 92.3% < 95% — the pass-rate requirement fails. Step 3: the policy separately requires no blocked tests outstanding, and 6 remain — a second, independent failure. Both conditions fail: option B. Option A uses the wrong base (216 ÷ 240 = 90%). Option C mis-compares 92.3% with 95%. Option D gets the base wrong and waves away a stated requirement. The senior lessons: first, every rate needs its base defined before calculation — "pass rate" is meaningless until you know what sits in the denominator; second, blocked tests are unexamined risk, not neutral absences — the six conditions nobody could run may hide precisely the defect that matters. Analysing and reporting test activities and results — your **Testing** skill — means reporting all three numbers (pass, fail, blocked) with their bases, and resisting any summary that quietly folds blocked into passed.

**Question 7 (moderate) — Cost comparison with growth**

You are comparing two storage options for a service currently needing 40 TB, growing about 20% per year. Option 1: on-premises array, £120,000 up front, covering all growth for three years, plus £10,000 per year support. Option 2: cloud storage at £75 per TB per month, billed on actual usage; modelling gives average usage of 44 TB in year 1, 53 TB in year 2, and 63 TB in year 3. Which option is cheaper over three years, and by how much?

- A) Option 1, by £6,000
- B) Option 2, by £6,000
- C) Option 2, by £30,000
- D) They are within £500 of each other

**Correct answer: B**

**Explanation:** Cost each option fully over the same three-year horizon. Option 1: £120,000 + (3 × £10,000) = £150,000. Option 2: each year's cost = average TB × £75 × 12 = average TB × £900. Year 1: 44 × £900 = £39,600. Year 2: 53 × £900 = £47,700. Year 3: 63 × £900 = £56,700. Total: £39,600 + £47,700 = £87,300; £87,300 + £56,700 = £144,000. Comparison: £150,000 − £144,000 = £6,000 in Option 2's favour — option B. Option A reverses the direction — the transposition-of-conclusion error that survives even correct arithmetic when the final subtraction is rushed. Option C is what emerges if year 2 and year 3 growth is ignored and year 1's cost is simply tripled (3 × £39,600 = £118,800, about £30,000 under Option 1) — the classic flat-usage error in a growth scenario. Note how close the honest answer is: £6,000 on £150,000 is a 4% difference, well within the error bars of a three-year usage model — so the senior recommendation would present the options as broadly cost-equivalent and decide on other factors (procurement lead time, exit flexibility, data residency, operational effort), stating exactly that. Recomputing totals from unit rates, and knowing when a difference is smaller than its own uncertainty, are the twin disciplines of credible budget input at your level.

**Question 8 (moderate) — Rota coverage ratio**

Your team must provide on-call cover every night of a 28-day period. Policy limits each engineer to at most 7 on-call nights in the period, and engineers must not be on call more than 2 consecutive nights. What is the minimum number of engineers needed to cover the period within policy?

- A) 3
- B) 4
- C) 5
- D) 6

**Correct answer: B**

**Explanation:** Two constraints bind. Volume: 28 nights at a maximum of 7 nights per engineer gives a lower bound of 28 ÷ 7 = 4 engineers. Pattern feasibility: with 4 engineers each doing exactly 7 nights, can the no-more-than-2-consecutive rule be satisfied? Yes — for example, rotate in pairs of nights: engineer 1 takes nights 1–2, engineer 2 nights 3–4, engineer 3 nights 5–6, engineer 4 nights 7–8, then repeat; each engineer works 2 consecutive nights at a time, 7 nights total per 28 (three pairs and one single, e.g. by breaking one pair), never exceeding 2 in a row. Both constraints satisfiable at 4, and 3 engineers cannot cover (3 × 7 = 21 < 28 nights). Option B. The method — compute the volume bound first, then verify a feasible pattern exists at that bound — appears in every workforce calculation your role-level management input touches: rota design, leave planning, project staffing. Note the duty of care embedded in such policies: the consecutive-nights limit exists for wellbeing, and a senior engineer building rotas (or reviewing a lead's) checks feasibility rather than quietly breaching the pattern rule to make the volume arithmetic work.

**Question 9 (moderate) — Interpreting a latency distribution**

A service's response-time report shows: mean response 180 ms; median response 95 ms; 95th percentile 850 ms; 99th percentile 2,400 ms. The service target is "typical responses under 200 ms". A stakeholder reads the mean and declares the target met. What is the most accurate senior assessment?

- A) The stakeholder is right — the mean is under 200 ms, so the target is met and no action is needed.
- B) The distribution is heavily skewed: most requests are fast (median 95 ms) but a small tail is very slow (99th percentile 2.4 s), inflating the mean; typical experience meets the target, but the tail deserves investigation.
- C) The target is missed because the 99th percentile exceeds 200 ms.
- D) The figures are contradictory — the median cannot be below the mean.

**Correct answer: B**

**Explanation:** Read the distribution's shape from the summary statistics. Median 95 ms says half of requests complete in under 95 ms — the typical experience is comfortably within target. Mean 180 ms sitting nearly double the median signals right-skew: a minority of very slow requests (850 ms at the 95th percentile, 2.4 s at the 99th) drag the average up. Option D has it backwards — mean above median is the signature of exactly this skew, entirely consistent. Option A stops at the mean and misses that around 1 in 20 requests takes over 850 ms — those are real users having a bad experience, and tails like this often point at a specific cause (a slow dependency, lock contention, garbage collection) that your **Troubleshooting and problem resolution** skill would decompose. Option C over-interprets "typical" as "every request": percentile targets and typical-response targets are different contracts, and reading which one the service actually has is a verbal precision point as much as a numeric one. The senior contribution is option B's both-halves framing: confirm the target's letter is met, and surface the tail with evidence — because the stakeholder's users judge the service by their slowest interactions, not the mean.

**Question 10 (hard) — Weighted downtime attribution**

Last quarter a service suffered 300 minutes of downtime across four causes: supplier network faults 120 minutes; departmental change errors 90 minutes; hardware failures 60 minutes; unknown causes 30 minutes. The supplier is contractually responsible only for supplier network faults. The supplier's report claims: "We caused only 40% of downtime, and departmental changes caused nearly as much (30%), so shared responsibility is appropriate." Verify the percentages and evaluate the claim. Which response is soundest?

- A) The percentages are correct (40% and 30%), and the arithmetic being right makes the shared-responsibility conclusion right too.
- B) The percentages are correct (40% and 30%), but the conclusion does not follow: contractual responsibility attaches to the supplier's 120 minutes regardless of what other causes contributed, so their credits are assessed on their 40% alone.
- C) The percentages are wrong: supplier faults were 50% of downtime.
- D) The unknown 30 minutes should be attributed to the supplier, making their share 50%.

**Correct answer: B**

**Explanation:** Verify first: 120 ÷ 300 = 0.40 = 40% ✔; 90 ÷ 300 = 0.30 = 30% ✔; hardware 60 ÷ 300 = 20%; unknown 30 ÷ 300 = 10%. The supplier's arithmetic is accurate — and the conclusion still fails, which is the question's point. Contractual responsibility is not comparative: the supplier owes performance on the causes assigned to them, and 120 minutes of supplier-caused downtime triggers whatever the contract specifies for 120 minutes, whether other parties contributed 0 or 900 minutes besides. "Others failed too" is rhetorically effective and contractually irrelevant. Option A commits the assessment's central trap — correct arithmetic validating an invalid inference; always evaluate the two separately. Option D invents an attribution rule: unknown causes are investigated, not assigned by default to whichever party is being reviewed — attributing them without evidence would be exactly the unfairness the supplier's rhetoric commits in reverse. This calibration — check the numbers, then check what the numbers do and do not entail — is the numeric heart of supplier management at your level, and rehearsing it prepares you for real service reviews where well-presented percentages arrive attached to well-crafted non-sequiturs.

**Question 11 (hard) — Budget option analysis with utilisation**

You provide input on renewing compute capacity. Current estate: 10 hosts, each costing £8,000 per year to run, at an average 30% utilisation. Option 1: renew all 10 hosts — £80,000 per year. Option 2: consolidate to 4 new hosts at £11,000 per year each, which modelling shows would run at about 75% utilisation. Policy caps planned utilisation at 80% to preserve failure headroom. Which statement best supports a recommendation?

- A) Option 2 saves £36,000 per year and stays within the utilisation cap, but the recommendation should note that 75% planned utilisation leaves little headroom for growth and for host failure, so growth projections must be checked before committing.
- B) Option 2 saves £36,000 per year and should be adopted without caveats.
- C) Option 1 is safer and cost is irrelevant to safety.
- D) Option 2 is invalid because 75% exceeds the utilisation cap.

**Correct answer: A**

**Explanation:** Cost the options: Option 1 = 10 × £8,000 = £80,000. Option 2 = 4 × £11,000 = £44,000. Saving = £80,000 − £44,000 = £36,000 per year. Check the policy: 75% ≤ 80%, so option D is simply misreading the cap. But a senior recommendation weighs what the arithmetic implies beyond the pass mark: at 75% planned utilisation on 4 hosts, losing one host pushes the survivors to roughly 75% × 4 ÷ 3 = 100% — saturation during any single failure — and only 5 percentage points of the cap remain for growth, so the modelling's assumptions (current load, growth rate) become load-bearing. Option A carries the saving and surfaces exactly these conditions — the failure-headroom arithmetic is the kind of second-order check your **Systems design** review duty ("efficient use of resources" and appropriate integration) exists to apply. Option B recommends on first-order arithmetic alone. Option C retreats from quantification entirely; public money makes cost always relevant, and safety is quantifiable through the headroom calculation rather than invoked as a veto. The pattern for management input at your level: verified saving, explicit conditions, named assumptions — recommendations built that way survive scrutiny and deserve to.

**Question 12 (hard) — Reconciling conflicting figures**

Preparing the quarterly service report, you find the monitoring platform recorded 99.62% availability for a service, while the service desk's incident records imply 99.80% (only one 87-minute outage logged in the 43,200-minute month). Investigation shows the monitoring platform counted a 78-minute planned maintenance window as downtime. The contract states planned maintenance within agreed windows is excluded from availability measurement. What availability should the report state, and what does the discrepancy tell you? (Verify with arithmetic.)

- A) 99.62% — the monitoring platform is the authoritative source.
- B) 99.80% — after excluding the 78 planned minutes, the remaining recorded downtime matches the incident record's 87 minutes; the monitoring platform's exclusion rules need correcting so future reports agree by construction.
- C) 99.71% — average the two figures since both sources are partly right.
- D) 99.80% — but no follow-up is needed since the correct figure has been found.

**Correct answer: B**

**Explanation:** Reconcile with arithmetic. Monitoring's 99.62% implies downtime of (100 − 99.62)% × 43,200 = 0.38% × 43,200 = 164.16 ≈ 164 minutes. Subtract the wrongly counted planned window: 164 − 78 = 86 ≈ 87 minutes (rounding in the availability figure accounts for the single minute). The incident record's 87 minutes gives (43,200 − 87) ÷ 43,200 = 43,113 ÷ 43,200 = 0.99799 ≈ 99.80% — and the contract's exclusion rule makes this the correct contractual figure: option B, whose second half matters as much as its first. The residual arithmetic proves the two sources agree once the classification error is removed — a genuine reconciliation, not a preference between sources. Option A elevates a tool above the measurement definition it violates; tools implement contracts, not the reverse. Option C's averaging is indefensible — where figures conflict, the task is to find the cause, and splitting differences institutionalises error. Option D fixes the number and leaves the generator of wrong numbers running: next quarter the same mismatch returns, and unexplained restatements corrode a report's credibility. The senior pattern, useful in every reporting cycle: quantify the discrepancy, identify the classification or definition difference that produces it exactly, correct the figure per the governing definition, and fix the source so agreement becomes automatic.

### Preparation tips

- **Define every base before dividing.** Pass rates, availability, compliance, headroom — each has a specific denominator set by policy or contract. Reading the measurement definition is half the question.
- **Aggregate counts, never percentages.** Quarterly and estate-wide figures come from summed raw numbers. The unweighted mean of period percentages is the assessment's favourite trap and real reporting's commonest error.
- **Memorise availability anchors.** 99.9% monthly ≈ 43 minutes; 99.5% ≈ 3.6 hours; 99% ≈ 7.2 hours. Instant conversion frees working memory for the question's real content.
- **Model phase changes explicitly.** Step increases, onboarding events, and rate changes need a month-by-month or phase-by-phase table. Formulas silently misplace boundaries; tables expose them.
- **Check second-order implications.** After the headline arithmetic, ask what it implies under failure or growth — the N-1 utilisation, the tail percentile, the assumption that must hold. Senior questions hide their real content there.
- **Recompute from unit rates.** In cost questions, rebuild totals from the per-unit figures rather than trusting any pre-computed total — in the test and in every option paper you review.
- **Practise on your own reports.** Take last quarter's service report and reproduce every figure from raw data. Discrepancies you find are both practice and genuine findings.

### Common pitfalls to avoid

- **Averaging percentages across unequal periods or groups.** Different denominators make simple means wrong. Return to counts.
- **Misplacing the decimal in small percentages.** 0.1% of 43,200 is 43.2, not 432. Write the fraction (0.001) explicitly before multiplying.
- **Computing the complement of the wrong thing.** Headroom is free-over-total; the free-over-used figure looks plausible and is wrong. Label numerator and denominator.
- **Letting correct arithmetic validate invalid conclusions.** A true 40% does not entail "shared responsibility". Verify numbers and inferences as separate acts.
- **Treating blocked, unknown, or excluded items as favourable by default.** Blocked tests are unexamined risk; unknown causes are uninvestigated, not attributable; exclusions apply only where the governing definition grants them.
- **Projecting from the wrong baseline.** Trends project from the last actual figure, with intervals counted between data points — and step changes added at their stated boundary.
- **Presenting a single number where a distribution matters.** Means conceal tails; report medians and percentiles when experience varies — one figure per question is an exam convention, not a reporting standard.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how accurately you understand, evaluate, and act on written information of the kind a senior infrastructure engineer handles daily: architectural design documents, departmental policies and standards, supplier contracts and service schedules, security advisories, governance papers, and the specifications and test documentation your team produces for your review. The dominant format presents a passage followed by statements to judge as **True** (supported), **False** (contradicted), or **Cannot say** (neither), alongside inference questions, best-summary items, argument-evaluation questions, and clear-writing judgements.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions. The governing discipline is unchanged from earlier career stages but harder to maintain at yours: judge strictly from the passage, not from expertise. Senior engineers carry the most background knowledge and are therefore the most prone to reading into a passage what experience says should be there.

Why do employers use verbal reasoning tests at this level? Because seniority multiplies the consequences of misreading — and of writing that is misread. You translate architects' documents into operational reality: a misparsed constraint becomes a misbuilt system. You review specifications and define test conditions from them: a missed "not" becomes an untested failure path. You work with third-party contracts where obligations assemble across separated clauses, and at review meetings your reading is the department's position. And the words now flow outward with authority: your design review comments direct other engineers' work, your management input shapes decisions, your problem records become the team's institutional memory. Verbal assessment samples both directions — precision of comprehension and judgement about clarity — because at senior level, language is one of your primary engineering tools.

### How this assessment maps to your role

- **Parsing design and requirement language** maps to your role-level duty to work with technical architects to translate architectural designs into operations, and to your **Testing** skill of reviewing requirements and specifications and defining test conditions: every test condition begins as a precisely read sentence.
- **Reading policy and standards exactly** maps to your **IT infrastructure** skill (designing and implementing solutions according to departmental policy) and your **Modern development standards** skill: applying standards and supporting others in applying them presumes you can state exactly what they require.
- **Contract and supplier comprehension** maps to your duty to work with and support third parties: schedules, exclusions, measurement definitions, and remedy clauses reward — and punish — reading at the clause level.
- **Separating observation from inference** maps to your **Problem management** skill: initiating investigations and determining resolutions depends on records that distinguish what was seen from what is supposed, and on reading others' records with the same discipline.
- **Evaluating arguments** maps to your **Ownership and topic** and management-input duties: proposals, business cases, and pushback arrive as prose arguments whose evidence and logic you must weigh before the department commits resources.
- **Judging and producing clear writing** maps to your **Systems design** documentation standards and your review role: recognising ambiguous, incomplete, or misleading text in others' work — and never producing it in your own — is a senior quality gate.

### Practice questions

**Question 1 (easy) — True/False/Cannot say on a design constraint**

Passage (from an architectural design): "The service will use the departmental platform's managed database service. Direct database administration access from outside the platform's management plane is not permitted. Application-level access is permitted only via the connection broker, which enforces per-service credentials rotated every 90 days."

Statement: "The design permits an engineer to connect a database administration tool directly to the database from their workstation, provided they use per-service credentials."

- A) True
- B) False
- C) Cannot say
- D) True, if the credentials were rotated within 90 days

**Correct answer: B**

**Explanation:** Two access channels are defined, each with its own rule. Administration access "from outside the platform's management plane is not permitted" — a workstation is outside the management plane, so direct administration access from it is prohibited outright. The per-service credential provision belongs to the other channel — application-level access via the connection broker — and cannot be transplanted to rescue an administration connection. The statement is contradicted: False, and option D fails for the same category reason. This channel-confusion trap mirrors a real review error: engineers frequently quote a document's permissive clause without checking which access class it governs. When you review designs or define test conditions from text like this — your **Testing** skill — treat each rule as bound to its stated subject, and test both channels separately: administration access blocked from outside the plane, application access working only through the broker.

**Question 2 (easy) — Comprehension of a security advisory**

Passage (advisory): "CVE-2026-1188 affects the cluster management daemon in versions 3.0 to 3.6 inclusive. Version 3.7 contains the fix. Exploitation requires network access to the management port and valid read-only credentials. Systems where the management port is restricted to the dedicated administration VLAN are still vulnerable but exploitable only from that VLAN. Patching to 3.7 is the only complete remediation."

Statement: "A system running version 3.6 with its management port restricted to the administration VLAN cannot be exploited."

- A) True
- B) False
- C) Cannot say
- D) True, because VLAN restriction prevents network access

**Correct answer: B**

**Explanation:** The advisory addresses this exact configuration: restricted systems "are still vulnerable but exploitable only from that VLAN". "Cannot be exploited" is therefore contradicted — exploitation remains possible from within the administration VLAN, by anyone (or any compromised host) with access to it plus read-only credentials. False, and option D repeats the error the advisory pre-empts. The reading skill is recognising scope-narrowing language: "exploitable only from that VLAN" narrows the attack surface without closing it — a materially different claim from "not exploitable". At senior level this distinction drives real decisions: a narrowed-but-open vulnerability may justify a scheduled patch rather than an emergency one, but never justifies no patch — and your **Information security** skill (using security practices and controls to contribute to protecting solutions) depends on briefing that difference accurately to whoever accepts the interim risk.

**Question 3 (easy) — Cannot say on a supplier report**

Passage (supplier quarterly report): "All 14 changes we implemented this quarter completed successfully within their approved windows. Our engineer attendance at scheduled maintenance was 100%. We responded to all Priority 1 incidents within contractual response times."

Statement: "The supplier resolved all Priority 1 incidents within contractual resolution times."

- A) True
- B) False
- C) Cannot say
- D) True, because response performance was fully compliant

**Correct answer: C**

**Explanation:** The report claims compliant response times — the interval to acknowledging and beginning work. Resolution times — the interval to restoring service — are a different contractual measure, and the report says nothing about them. No support, no contradiction: Cannot say. Option D commits the substitution the report's drafting invites: response and resolution are adjacent concepts, and a fluent paragraph of positives encourages the reader to extend the glow to measures not mentioned. This is not accidental in real supplier reporting — reports naturally foreground the metrics that flatter, and the silences are where the service review questions live. The senior discipline, exercised through your duty to work with and support third parties: list the contract's measures first, then read the report against the list, and treat every absent measure as an open question for the meeting — "response was compliant; what was resolution performance?" is the question this report is quietly hoping nobody asks.

**Question 4 (easy) — Judging review feedback quality**

A junior engineer's design document states: "Backups will be taken regularly and stored safely." As the senior reviewer, which written comment is most effective?

- A) "Vague — rewrite."
- B) "This needs to specify: backup frequency and type (e.g. nightly incremental, weekly full), retention period, storage location and its separation from the primary site, encryption requirements, and how restoration will be tested and how often. Each should trace to the service's RPO/RTO tier."
- C) "Fine at this stage — details can come later."
- D) "Please see me about this section."

**Correct answer: B**

**Explanation:** Review comments are teaching instruments and quality gates simultaneously, and option B performs both roles: it names each missing element (frequency, type, retention, location, encryption, restoration testing) and supplies the organising principle — trace to the RPO/RTO tier — that lets the engineer close this gap and never open it again. Option A is accurate and useless: "vague" identifies the symptom without transferring any knowledge of what sufficiency looks like; the engineer must guess, and the next draft will be vague differently. Option C waves through a section that is not detailed-later material — "stored safely" could conceal a same-site backup that fails exactly when needed; deferring specifics in a detailed design defeats the review's purpose. Option D may be a kind supplement but as the sole written record it leaves nothing in the document trail, and reviews that live only in conversations do not scale or survive. Your **Systems design** duty to review others' designs and your **Modern development standards** duty to support others in applying standards converge here: the best senior comments make the standard explicit, so each review permanently raises the team's baseline.

**Question 5 (moderate) — Inference across contract clauses**

Passage (contract extract): "Clause 12.1: The supplier shall complete hardware repairs within 8 working hours of fault confirmation. Clause 12.2: Where a repair requires parts not held in the supplier's UK depot, the repair period is extended to 3 working days. Clause 12.3: Faults confirmed after 14:00 are treated as confirmed at 09:00 the next working day. Clause 12.4: Repair periods for equipment at sites more than 100 miles from the supplier's depot are extended by 4 working hours."

A fault on equipment at a site 140 miles from the depot is confirmed at 15:30 on Monday. The repair requires only parts held in the UK depot. Working hours are 09:00–17:00. By when must the repair be complete?

- A) Tuesday 17:00
- B) Wednesday 13:00
- C) Tuesday 13:00
- D) Thursday 09:00

**Correct answer: B**

**Explanation:** Assemble the obligation clause by clause. Clause 12.3: confirmation at 15:30 Monday is after 14:00, so treat confirmation as 09:00 Tuesday. Clause 12.1: base period 8 working hours. Clause 12.4: site is 140 miles (> 100), adding 4 working hours — total 12 working hours. Clause 12.2 does not apply (parts are in the depot). Count 12 working hours from Tuesday 09:00 in an 8-hour working day: Tuesday 09:00–17:00 consumes 8 hours; the remaining 4 hours run Wednesday 09:00–13:00. Deadline: Wednesday 13:00 — option B. Option A forgets the distance extension; option C additionally ignores the after-14:00 reset; option D wrongly applies the parts extension. This is exactly how real support contracts compute: no single clause states the answer, and the deadline your department can enforce emerges only from correct assembly. Before any supplier escalation, a senior engineer performs precisely this calculation — because demanding a repair the contract does not yet owe spends credibility, while missing a breach the contract does establish forfeits remedy.

**Question 6 (moderate) — Reading a standards document's exception structure**

Passage: "All infrastructure changes must be implemented through the automated deployment pipeline. Exception 1: emergency changes during a declared major incident may be implemented manually, provided each command is logged and the change is reconciled into the pipeline's configuration repository within 5 working days. Exception 2: changes to the pipeline itself follow the pipeline-change procedure in Annex C. No other exceptions apply. Reconciliation failures are reported monthly to the service board."

Statement: "A manual change made during a declared major incident, with all commands logged, complies with the standard even if it is never reconciled into the configuration repository."

- A) True
- B) False
- C) Cannot say
- D) True, provided the failure is reported to the service board

**Correct answer: B**

**Explanation:** Exception 1 grants its permission on two conditions joined by "provided": command logging AND reconciliation within 5 working days. A change that is never reconciled fails the second condition, so the exception's protection lapses and the change stands non-compliant with the base rule: False. Option D misreads the final sentence — reporting reconciliation failures to the board is a monitoring mechanism that makes non-compliance visible; visibility is not absolution, and a reported breach is still a breach. The drafting pattern is worth internalising for your **Modern development standards** work: standards commonly pair a permission with trailing obligations precisely because the permission's moment (mid-incident) is when discipline is weakest and the follow-up (reconciliation) is most likely to be dropped — configuration drift between the repository and reality is the exact failure the condition guards against. When you lead others in applying standards, the coaching point is that "provided" clauses are load-bearing: the manual fix at 3 a.m. is only half the compliance; the reconciliation on Thursday is the other half.

**Question 7 (moderate) — Main point of a governance passage**

Passage: "Technology roadmaps fail less often from poor technical judgement than from poor connection to decisions. A roadmap that lists upgrade dates without linking them to budget cycles arrives as information, not as a proposal, and is noted rather than funded. The effective roadmap names, for each item, the decision it requires, the decision-maker, the date by which deciding is still cheap, and the cost of deciding late. Engineers drafting roadmaps should therefore spend as much care on the decision architecture as on the technology choices — the two are equally load-bearing."

What is the main point?

- A) Technology roadmaps usually contain poor technical judgement.
- B) Roadmaps succeed when they are structured around the decisions they require — decision, decider, deadline, and cost of delay — not just around technology choices.
- C) Budget cycles should be reformed to accommodate technology roadmaps.
- D) Engineers should delegate roadmap drafting to decision-makers.

**Correct answer: B**

**Explanation:** The passage's argument runs: the common failure is weak connection to decisions, not weak technology judgement (first sentence — which option A inverts); an unconnected roadmap is "noted rather than funded"; the remedy is the four-element decision architecture (decision, decision-maker, cheap-decision date, cost of lateness); and the conclusion assigns that architecture equal weight with the technical content. Option B captures exactly this. Option C proposes reforming budget cycles — the passage adapts roadmaps to cycles, not the reverse. Option D confuses naming decision-makers within the roadmap with handing them the pen. Beyond the comprehension exercise, absorb the content: your role-level duty to provide input into technology roadmaps is precisely the activity the passage addresses, and the four-element structure is directly usable — a hardware refresh proposal that states "decision needed by March, while migration can still ride the planned data-centre work; deciding in September doubles the cost" is management input that gets funded, which is the practical difference between writing roadmaps and writing lists.

**Question 8 (moderate) — Observation versus inference in a problem record**

Passage (problem record extract): "Between 2 May and 20 June, the virtualisation platform logged 11 unplanned guest restarts, all on hosts H3 and H4, all between 01:00 and 04:00. H3 and H4 are the only hosts fitted with network cards from Vendor Q. Firmware on those cards is two releases behind current. The overnight backup traffic peak occurs between 01:00 and 04:00. No guest restarts occurred on hosts H1, H2, or H5 in the period."

Which statement is supported by the passage?

- A) The Vendor Q network card firmware caused the guest restarts.
- B) The restarts cluster on the only two hosts with Vendor Q cards and coincide with the backup traffic peak — a correlation that makes the card firmware under load a strong hypothesis for investigation, though causation is not yet established.
- C) Updating the firmware will stop the restarts.
- D) Backup traffic caused the restarts, and the network cards are irrelevant.

**Correct answer: B**

**Explanation:** The passage supplies correlations of unusual quality: perfect host specificity (all 11 restarts on exactly the two Vendor Q hosts, none elsewhere) and consistent time-locking to the backup peak. That justifies exactly what option B claims — a strong, focused hypothesis (cards under load, plausibly addressed by the outdated firmware) awaiting confirmation. It does not establish causation: some third factor could distinguish H3/H4 (hardware batch, configuration, workload placement), and the passage tests whether you can hold strong correlation and unproven causation in the same sentence. Options A and C leap the gap — C doubly, converting unestablished cause into guaranteed cure. Option D discards half the evidence pattern to crown the other half. This calibration is the daily grammar of your **Problem management** skill: initiating and monitoring actions to investigate patterns and trends means writing records that say "correlates, hypothesis, next test" rather than "caused" — because records that overclaim get actioned as fact, and a firmware update deployed as the fix ends the investigation whether or not it ends the restarts.

**Question 9 (moderate) — Evaluating a proposal's argument**

Passage (proposal from a team member): "We should adopt the new container platform for all our services immediately. The pilot ran for a month with zero incidents, which proves the platform is more reliable than our current one. Also, Vendor R says most government departments are moving to containers, so we risk being left behind. Migrating everything this quarter avoids running two platforms in parallel, which would double our operational burden."

Which is the strongest criticism of the argument?

- A) Container platforms are inherently less secure, so the proposal should be rejected.
- B) A one-month, presumably small-scale pilot cannot "prove" superior reliability against a production platform's track record; the vendor's claim is both self-interested and irrelevant to this department's needs; and big-bang migration trades a manageable parallel-running burden for concentrated cutover risk — the argument's three supports are all weaker than presented.
- C) The team member lacks the seniority to make proposals.
- D) Zero incidents in the pilot proves the pilot was not tested hard enough.

**Correct answer: B**

**Explanation:** Audit each support. First: "zero incidents in a month proves more reliable" — a pilot differs from production in scale, load, workload diversity, and duration; absence of incidents in a small sample is weak evidence, not proof (though genuinely encouraging). Second: the vendor's "most departments are moving" is an appeal to popularity from a self-interested source, and other departments' choices do not establish this department's fit. Third: the parallel-running argument counts one cost while omitting the alternative's — migrating everything in a quarter concentrates risk, compresses learning, and removes the incremental rollback that phased migration preserves; parallel running is a cost buying risk reduction. Option B catches all three. Option A rejects via an unargued generalisation — the mirror image of the proposal's own flaws. Option D overcorrects: zero incidents does not prove inadequate testing, and the criticism must not overclaim either. Option C attacks the person. The senior skill — reviewing proposals as your management-input duty requires — is to name each weakness precisely while preserving what survives: the right response endorses a phased expansion of the pilot, which the evidence does support.

**Question 10 (hard) — Interacting policy documents**

Passage: "Departmental policy P-14: Production data must not leave the production environment. Anonymised extracts are exempt, provided anonymisation follows Standard S-9. Platform guideline G-3: Test environments should use realistic data volumes; teams may request production-scale synthetic data generation, or S-9-compliant anonymised extracts, through the data management team. A project's test plan states: 'Performance testing will use a copy of the production customer database, imported directly into the test environment, with anonymisation to follow in a later phase once the urgent performance deadline has passed.'"

Which assessment of the test plan is correct?

- A) Compliant — G-3 permits realistic data in test environments.
- B) Compliant — anonymisation is planned, satisfying P-14's exemption.
- C) Non-compliant — the plan moves un-anonymised production data out of production, breaching P-14; the exemption applies only to extracts anonymised per S-9 before leaving, and G-3 offers the compliant alternatives the plan should use.
- D) Cannot be assessed without knowing the performance deadline.

**Correct answer: C**

**Explanation:** Sequence is the crux. P-14 prohibits production data leaving production; the exemption covers "anonymised extracts" — data that is already anonymised (per S-9) when it leaves. The plan imports the raw customer database first and anonymises "in a later phase": at the moment of import, un-anonymised production data has left production — the breach is complete, and later anonymisation cannot retroactively unmake it. Option B fails on exactly this tense: planned anonymisation is not the exemption's condition; completed anonymisation is. Option A misuses G-3: the guideline's "realistic data" is satisfied through the two compliant routes it names — synthetic generation or S-9-compliant extracts — and a guideline cannot override a policy prohibition anyway; document hierarchy matters. Option D mistakes urgency for relevance: no deadline modifies P-14, and "the deadline made us" is the opening sentence of half the data-incident reports ever written. The senior duties converge here: reviewing test plans (your **Testing** skill), applying security practice (**Information security**), and the constructive close — the correct review comment rejects the import and routes the team to G-3's synthetic-data service, solving their performance-testing need inside the rules.

**Question 11 (hard) — Precision across a long operational passage**

Passage: "The data centre exit programme will migrate 180 services in three tranches. Tranche 1 (60 services, complete) targeted services with no dependencies outside their own tranche. Tranche 2 (80 services, in progress, due end of November) includes all services with dependencies on shared platforms, which were themselves migrated at the end of Tranche 1. Tranche 3 (40 services) contains only services awaiting contractual novation with their suppliers, and its start date will be set when the last novation completes; legal advises novations complete 'by January at the earliest'. Any service failing its post-migration verification is rolled back and rejoins the schedule at the next tranche boundary. Two Tranche 2 services have so far failed verification and been rolled back."

Which statement is supported by the passage?

- A) Tranche 3 will start in January.
- B) The two rolled-back services will be re-migrated within Tranche 2 before the end of November.
- C) The shared platforms were migrated before any Tranche 2 service, and the two rolled-back services' next migration opportunity is the Tranche 2/3 boundary — meaning their re-migration timing inherits Tranche 3's novation-dependent uncertainty.
- D) Exactly 118 services have successfully migrated so far.

**Correct answer: C**

**Explanation:** Verify each option against the text's exact machinery. Option A converts "by January at the earliest" — a floor on completion of novations, which then permits setting a start date — into a January start: doubly unsupported. Option B contradicts the rollback rule: failed services rejoin "at the next tranche boundary", not within their original tranche. Option D miscounts: Tranche 1's 60 are complete, but Tranche 2 is "in progress" with an unstated number migrated so far (only the two failures are quantified), so no completion total is derivable. Option C assembles only stated facts: shared platforms "migrated at the end of Tranche 1" — before Tranche 2's dependent services; the rolled-back pair's next boundary is Tranche 2/3; and Tranche 3's start awaits novations of uncertain date — so the pair's re-migration inherits that uncertainty. Notice the chain's practical sting, which a senior reader should surface: two services sit un-migrated for an unbounded period on account of a legal process unrelated to them — exactly the kind of second-order schedule risk your programme-support role exists to spot and raise. Long-passage questions reward the same method as long programme documents: extract the rules, then run the specific case through them mechanically.

**Question 12 (hard) — Judging an escalation communication**

Your team's overnight change failed and was rolled back cleanly; the service ran normally throughout, but the failure consumed the quarter's last agreed maintenance window, and the postponed upgrade now blocks a dependent programme's milestone. You must email the service owner and the programme manager. Which draft is most effective?

- A) "Last night's change encountered an unexpected issue and was rolled back successfully with no service impact. We will reschedule in due course and keep you informed."
- B) "Last night's upgrade failed at the storage firmware step and was rolled back per plan; the service was unaffected throughout. However, this consumed the quarter's final agreed window, and the upgrade now blocks Programme X's data migration milestone (due 15th). Options: (1) an emergency window next week — needs service owner approval by Thursday, brings the milestone back on track, carries standard change risk with the failure cause now understood and fixed; (2) wait for next quarter's windows — no additional change risk, milestone slips ~6 weeks. The failure cause was a firmware/driver mismatch our pre-checks missed; the check is now added. Recommendation: option 1. Please confirm by Thursday."
- C) "The change failed due to circumstances beyond our control. The programme's milestone may be affected. We are investigating and will report when investigations conclude."
- D) "Full incident timeline attached (14 pages). All decisions on rescheduling rest with the service owner and programme manager; we await your instructions."

**Correct answer: B**

**Explanation:** Judge each draft by whether its recipients can decide and act. Option B delivers the complete decision package: what happened and its true status (failed step, clean rollback, no service impact — accurate reassurance first); the consequence that makes this their business (window consumed, named milestone blocked, date attached); genuine options with the decision-relevant attributes of each (risk, timing, approval needed, deadline); the cause and its closure (mismatch found, pre-check added — which converts the failure into evidence of a learning team); and a recommendation with a response deadline that keeps option 1 achievable. Option A is soothing vagueness: "in due course" conceals the milestone impact — which the programme manager will discover later, with interest. Option C is worse than silence: "beyond our control" deflects, "may be affected" hedges a known consequence, and "when investigations conclude" leaves the Thursday-shaped decision window closing silently. Option D drowns the decision in data and mistakes abdication for deference — recipients own the decision, but the engineer owns making it decidable. This is your role level's communication standard: bad news travels fastest, fullest, and with options attached — the email that lets a service owner decide well in four minutes is a senior engineering artefact as surely as any design.

### Preparation tips

- **Read at clause level under time.** Practise on contracts and standards from your own environment: extract each obligation, its conditions, and its tense (completed versus planned) — the tense distinction alone decides several hard questions.
- **Track which subject each rule binds.** Access classes, tranches, exception scopes: mis-transplanting a clause from one subject to another is the designed trap in passage after passage.
- **Rehearse the correlation/causation sentence.** "X correlates with Y, making Z a strong hypothesis; causation is not established." Statements calibrated exactly like this are usually the supported ones.
- **List the measures, then read the report.** For supplier and service passages, name the expected metrics first; the question frequently lives in a measure the passage conspicuously omits.
- **Audit arguments support by support.** Proposals bundle two or three justifications; evaluate each independently (sample size, source interest, counted-versus-omitted costs) before judging the whole.
- **Write review comments that teach.** Practise converting "vague" into a named list of missing elements plus the organising principle — the same specificity the clear-writing questions reward.
- **Draft the decision-package email.** Take a real recent setback and write the five-part structure: status, consequence, options with attributes, cause and closure, recommendation with deadline. This is the outbound skill the test's judgement items sample.

### Common pitfalls to avoid

- **Expertise contamination.** The more you know, the more you must verify the passage actually says it. Seniors fail verbal items by reading in what experience expects.
- **Tense-blindness in exemptions.** "Anonymised extracts", "approved classifications", "completed reconciliation" — conditions stated in the completed form are not met by plans to complete them.
- **Extending praise across measures.** Compliant response times imply nothing about resolution times. Adjacent metrics are different metrics.
- **Floors read as dates.** "By January at the earliest", "no earlier than", "at least" set boundaries, not schedules.
- **Visibility mistaken for permission.** Reporting a breach to a board makes it visible, not compliant. Monitoring clauses do not absolve.
- **Overclaiming in both directions.** "Proves" and "caused" overclaim; but so does "proves the testing was inadequate". Calibrated statements win; check your chosen option does not exceed the evidence either way.
- **Guideline-policy hierarchy errors.** A guideline's flexibility cannot override a policy's prohibition. Note each document's authority before combining them.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace scenarios and asks you to evaluate possible responses — most-effective, most-and-least-effective, full ranking, or independent effectiveness ratings. Scoring reflects the consensus of experienced professionals and the organisation's valued behaviours. The typical format is an online test of 15 to 25 minutes with 10 to 20 scenarios, usually generously timed, because it measures judgement rather than speed.

At senior level, the scenarios change character. They assume your technical competence and probe the judgement that surrounds it: how you review work you could have done better yourself, how you handle a team member's mistake versus your own, when you overrule and when you coach, how you manage third parties who underperform, how you respond when management pressure meets engineering evidence, and how you balance delivery, risk, and people when they pull apart. The distractor options are correspondingly subtler — competent-looking responses that quietly hoard authority, skip a stakeholder, teach nothing, or optimise this week at the team's long-term expense.

Why do employers use SJTs for senior infrastructure engineers? Because at this level judgement is the job. Your role summary carries duties no test of technical knowledge can sample: leading and directing infrastructure specialist teams, working with and supporting third parties, consulting specialists effectively, owning issues to resolution, providing management input, and reviewing others' work. Each is a stream of judgement calls, made with incomplete information, in front of people who will calibrate their own behaviour on yours. The behaviours that score well are consistent: protect users and services first; keep records honest; escalate and delegate proportionately; correct work firmly and people kindly; give credit and take responsibility; and treat every incident, review, and supplier failure as material for prevention and learning. This section rehearses those behaviours in scenarios with senior-level texture.

### How this assessment maps to your role

- **Leading and reviewing** maps to your role-level duty to lead and direct infrastructure specialist teams and your **Systems design** duty to review the designs of others: scenarios test whether your corrections build capability or dependency.
- **Ownership at scale** maps to your **Ownership and topic** skill: owning issues until resolution or handover now includes issues surfaced by your team, your suppliers, and your own past decisions.
- **Consulting and escalating** maps to your **Problem management** skill — effectively consulting specialists where required, determining resolutions and preventative measures — and to knowing when a decision belongs above you.
- **Third-party judgement** maps to your duty to work with and support third parties in providing infrastructure services: scenarios probe constructive challenge, contractual awareness, and proportionate escalation.
- **Operational integrity under pressure** maps to your **IT infrastructure** and **Information security** skills: scenarios test whether policy, security controls, and honest records survive deadlines and seniority.
- **Management input** maps to your duty to provide input into workforce, budget, roadmaps, projects, and tasks: scenarios test candour, evidence, and the courage to give unwelcome advice well.

### Practice questions

**Question 1 (easy) — Reviewing work you would have done differently**

A capable engineer on your team submits a design for a monitoring deployment. It is sound, meets every requirement, and will work — but it uses a layout you personally find inelegant; your own approach would be marginally tidier with no material difference in outcome, cost, or risk. What is the most effective response?

- A) Require them to rework it to your approach — consistency with the senior engineer's style keeps the estate uniform.
- B) Approve it, noting anything genuinely important, and keep your stylistic preference to yourself or offer it explicitly as an optional observation, clearly separated from the approval.
- C) Approve it but redo it your way yourself after hours.
- D) Approve it while making clear you would have done better.

**Correct answer: B**

**Explanation:** The review's purpose is to verify requirements, risk, and standards — all satisfied here. Option B approves on the merits and handles the preference honestly: either silence, or a clearly labelled "optional — your call" observation, which respects the engineer's ownership while sharing perspective. The senior failure modes are the other three. Option A converts personal taste into mandatory rework: it costs real time, teaches the team that approval depends on mimicking the reviewer, and suppresses the design diversity from which teams learn — style mandates are legitimate only when codified as team standards, which is the honest route if the preference truly matters. Option C is quiet contempt with overtime: the estate ends up with a design its named owner did not produce and cannot fully support. Option D approves while diminishing — extracting status from a subordinate's success. Review authority is held in trust for quality, not for taste; seniors who can approve work they would have done differently, without comment tax, are the ones whose genuine objections get heard — and whose engineers grow. That is the reviewing half of leading and directing a team.

**Question 2 (easy) — A team member's production mistake**

An engineer you direct makes an error during a routine change, causing a 20-minute outage to an internal service. They fix it, then come to you visibly shaken and tell you everything immediately and accurately. It is their first significant mistake; the change process they followed had no step that would have caught the error. What is the most effective response?

- A) Thank them for the immediate honest report, review what happened together, add the missing verification step to the change process, and make sure the incident record reflects the process gap as well as the action.
- B) Formally document the error in their performance record as a caution to others.
- C) Reassure them it does not matter and move on without further action.
- D) Take over their remaining changes for the next month to prevent recurrence.

**Correct answer: A**

**Explanation:** Two assets need protecting: the engineer's future candour and the system's future safety — option A protects both. Thanking the honest report first is not softness; it is incentive engineering: the team calibrates on what happens to the first person who self-reports, and punishing candour purchases a future of concealed errors, which are the expensive kind. The joint review converts the mistake into learning; fixing the process gap addresses the actual root cause (the scenario states the process could not have caught the error — so the process, not the person, is the reusable fix); and an incident record that names the process gap keeps organisational memory honest. Option B punishes exactly the behaviour you need repeated, for an error the process invited. Option C wastes the incident: no process fix, no learning, and "it does not matter" is false — it mattered 20 minutes' worth, and pretending otherwise teaches imprecision. Option D infantilises a capable engineer, doubles your load, and prevents the practice that builds their reliability. This is your **Problem management** skill applied to people: determine the preventative measure, and the preventative measure is almost never "fear".

**Question 3 (easy) — Supplier engineer bypassing agreed procedure**

During a scheduled maintenance visit, you observe a third-party engineer skipping the agreed pre-work verification checklist "because we did the same job last month and it was fine". The work itself is proceeding without apparent problems. What is the most effective response?

- A) Let the work continue — the engineer's experience substitutes for the checklist.
- B) Pause the work; require the checklist to be completed before proceeding; afterwards, raise the deviation with the supplier's service manager through the agreed route, factually and without personalising it.
- C) Say nothing now but log a formal complaint demanding a different engineer in future.
- D) Complete the checklist yourself while the engineer continues working.

**Correct answer: B**

**Explanation:** The checklist is part of the agreed method statement — the contractual and safety basis on which the supplier works on your infrastructure — and "last month was fine" is precisely the reasoning checklists exist to defeat: pre-work verification catches the state changes since last month (a failed redundant path, a drifted configuration) that make the same job unsafe this time. Option B acts at both required levels: operationally, pause-and-complete restores the control before risk accrues, courteously and immediately; contractually, the deviation goes to the supplier's service manager — because an engineer skipping agreed procedure is a supplier performance matter, and the service manager can address whether it is one engineer's habit or a systemic corner-cut. Option A substitutes confidence for verification — the exact trade the checklist forbids. Option C converts a correctable moment into a delayed grievance: the risk ran its course unchallenged, and demanding a different engineer punishes without correcting. Option D absorbs the supplier's obligation into your own workload, muddles accountability for the verification, and teaches the engineer that skipped steps get quietly backfilled. Working with and supporting third parties — your role-level duty — means holding the agreed standard warmly and immediately, and routing performance signals to where they can change behaviour.

**Question 4 (easy) — Credit for your team's work**

At a service review, a director praises the storage migration "you delivered" — but the design and the hardest implementation work came from two engineers on your team; you provided direction and reviews. What is the most effective response?

- A) Accept the praise — you led the work, and leaders represent their teams.
- B) Briefly and specifically credit the two engineers by name and contribution, then move on with the meeting's business.
- C) Deflect all credit entirely — "I did nothing, it was all the team".
- D) Say nothing now but tell the engineers privately that the director was pleased.

**Correct answer: B**

**Explanation:** Option B is accurate, proportionate, and consequential: specific, named credit in the room where reputations are made ("the replication design was Priya's; Marcus solved the cutover sequencing") costs fifteen seconds, corrects the record, and materially affects how directors perceive — and later develop and promote — your engineers. It also strengthens rather than weakens you: leaders who visibly grow strong people are read as strong leaders, and your team will hear what you said in a room they were not in, which buys more discretionary effort than any away-day. Option A quietly banks your team's work as your own — the single fastest way to teach good engineers that excellence under you is invisible. Option C over-rotates into false modesty: it discards the direction and review you genuinely contributed, sounds like fishing, and gives the director no usable information about who did what. Option D delivers the private half and withholds the public half — and the public half is where the career value lives. Credit allocation is a core mechanic of leading and directing teams: get it right reflexively, because every visible instance sets the price of working hard for you.

**Question 5 (moderate) — Pressure to understate a risk in management input**

You are finalising your input to the infrastructure roadmap. Your analysis shows the storage estate needs replacement within 18 months; beyond that, failure rates and unsupported firmware make a major incident materially likely. Your head of service, managing a difficult budget round, asks you to "soften the storage line — say it's a risk we're monitoring, not a hard requirement — so the roadmap doesn't look like a shopping list". What is the most effective response?

- A) Soften the wording as asked — budget strategy is their call, and the roadmap is their document.
- B) Refuse and submit your original wording over their objection without discussion.
- C) Keep the evidence and the 18-month requirement intact, and offer to reframe presentation, not substance — for example, phasing the spend, pairing it with the risk of deferral in incident-cost terms, and distinguishing "funded now" from "committed next cycle" — while being clear you cannot describe a hard requirement as optional monitoring.
- D) Soften the wording but keep a private copy of your original analysis as protection.

**Correct answer: C**

**Explanation:** Separate what is negotiable from what is not. Presentation — phasing, framing, sequencing against the budget cycle — is legitimately the head of service's craft, and option C engages with it genuinely: "phased replacement starting year 1, completing by month 18, with deferral costed at the incident impact" may well serve their budget strategy better than a bald demand. Substance — the evidence-based 18-month requirement — is yours to state accurately: management input that describes hard requirements as "monitored risks" is false input, and decisions built on it are built on sand; if the softened line prevails and the incident arrives in month 20, the department will ask, fairly, why its senior engineer's roadmap called the danger optional. Option A trades your professional accuracy for organisational comfort. Option B wins the wording and loses the relationship and probably the funding — refusal without engagement reads as inflexibility, and the head of service still controls the budget conversation. Option D is the worst of both: the official record misleads while a private file protects only you — evidence of knowing better, kept for the inquiry. The senior pattern for advice under pressure: flex the framing all the way, flex the facts not at all, and bring alternatives that make honesty affordable.

**Question 6 (moderate) — A specialist's advice contradicts your diagnosis**

Leading a problem investigation into database corruption events, you develop a hypothesis: a storage-layer caching fault. You consult the department's database specialist, who examines the evidence and disagrees — she believes the corruption pattern indicates an application-level defect in how transactions are retried, and points to features of the corrupted records your analysis did not explain. Her area is databases, not storage; yours is the reverse. What is the most effective response?

- A) Proceed with your hypothesis — you lead the investigation and storage is your domain.
- B) Defer entirely to her — specialists outrank generalists in their own area.
- C) Treat the disagreement as information: her observations explain evidence yours does not, so design the next investigative step to discriminate between the two hypotheses — for example, testing whether corruption occurs with retries disabled or on a different storage path — and follow the evidence.
- D) Escalate the disagreement to management to decide between the hypotheses.

**Correct answer: C**

**Explanation:** The scenario embeds the decisive detail: her hypothesis explains features of the evidence yours does not — in diagnostic reasoning, explanatory coverage is the currency, and a hypothesis that accounts for more of the pattern earns priority attention regardless of whose domain it sits in. But option C's real strength is refusing to resolve by authority in either direction: investigations are settled by discriminating tests, not by seniority (option A) or deference (option B) — and a well-designed next step (retries off, storage path varied) makes the evidence choose. Option A also carries a bias worth naming: investigators favour hypotheses in their own competence area because they can act on them — comfort is not likelihood. Option B abdicates the leadership the investigation needs; specialists advise within their frame, and the retry defect and a storage interaction could even be compounding, which only the investigation's leader is positioned to hold together. Option D escalates a question management cannot answer — hypothesis selection is technical, and what management needs is your consulted, tested conclusion. This is your **Problem management** skill's "effectively consult specialists where required", completed: consult genuinely, weigh explanatory power over territory, and let designed evidence arbitrate.

**Question 7 (moderate) — Deadline versus unresolved test failures**

Your team is implementing a network upgrade for a programme go-live in ten days. Integration testing has one persistent failure: under a specific failover condition, reconnection takes four minutes instead of the specified thirty seconds. The programme manager proposes: "Ship it — failover is rare, four minutes is survivable, and we can fix it after go-live." You judge the failure mode would, during business hours, disconnect around 400 case-workers mid-task. What is the most effective response?

- A) Accept the proposal — the programme manager owns the go-live decision.
- B) Block the go-live until the failure is fixed, regardless of the programme's constraints.
- C) Ensure the risk is decided at the right level with full information: quantify the exposure (probability of failover, 400 users, four-minute impact, working recovery), identify what a fix or mitigation costs in schedule, and put the accept/fix/mitigate decision to the service owner and programme board with your recommendation — recorded, whichever way it goes.
- D) Agree to ship, but quietly keep an engineer working on the fix without telling the programme.

**Correct answer: C**

**Explanation:** The disagreement is really about decision rights and information quality. The programme manager's framing minimises through vagueness ("rare", "survivable"); your quantification (400 case-workers, four minutes, mid-task) is the information that makes the risk decidable — but the decision to accept degraded failover on a production service belongs to whoever owns the service risk, informed by the programme's constraints, not to either of you unilaterally. Option C routes it there with the three genuine options (accept with eyes open, fix and slip, mitigate — perhaps constraining the failure window or pre-positioning recovery) and your recommendation, then records the outcome — the record being what makes an accepted risk a decision rather than a surprise. Note that C does not presume the answer is "delay": a board that accepts the risk knowingly has decided legitimately, and your role is fulfilled. Option A treats delivery authority as risk authority. Option B makes you the unilateral decider in the other direction — engineering veto without governance is still governance bypass, and "regardless of constraints" ignores information you do not hold. Option D splits the difference dishonestly: unrecorded risk, unmanaged expectations, and a fix competing secretly with whatever the engineer was meant to do. Ensuring services are integrated, delivered, and operated as required includes ensuring the risk decisions around them are made properly — that is the ownership your level carries.

**Question 8 (moderate) — Team member repeatedly bypassed by a stakeholder**

A project manager has begun routing all infrastructure requests directly to you, bypassing the engineer you assigned to their project — after two occasions where the engineer's answers were slower and more cautious than the manager wanted. The engineer has noticed and is demoralised. The manager's requests to you are reasonable in content. What is the most effective response?

- A) Keep answering — the work is flowing and the manager is satisfied.
- B) Redirect the manager back to the engineer, explain that the engineer speaks for infrastructure on this project, privately check whether the engineer's slower answers reflected a support gap you should close, and stay available to both as an escalation route.
- C) Tell the engineer to toughen up — stakeholder preferences are a fact of life.
- D) Confront the manager about undermining your team.

**Correct answer: B**

**Explanation:** The bypass is quietly expensive: it centralises project knowledge in you (who will be the bottleneck and the single point of failure), tells the engineer their assignment is nominal, and teaches every observing stakeholder that the way to faster answers is upward routing. Option B repairs the structure at both ends. To the manager: a courteous, firm re-point — the engineer is the project's infrastructure voice, with you as escalation — which preserves the relationship while restoring the channel. To the engineer: the diagnostic conversation option B embeds is the senior move — were the slow, cautious answers a confidence gap, a knowledge gap, or actually correct caution the manager disliked? Each has a different remedy (coaching, information, or backing the engineer publicly), and closing the real gap is what makes the redirect stick. Option A optimises this month's flow at the cost of the team's development and your own scalability — leading teams means building people stakeholders trust, not intercepting their chances to earn it. Option C hears the demoralisation and returns a slogan. Option D makes it adversarial before making it better; the manager's behaviour was rational given their experience — change the experience. Delegation that is defended and developed is the difference between directing a team and merely fronting one.

**Question 9 (moderate) — Discovering an undocumented dependency during planning**

Planning a decommissioning, you discover that a legacy server scheduled for shutdown next week still receives a nightly file from a payroll process — an undocumented dependency nobody on the current team knew existed. The decommissioning is part of a funded programme with a published schedule; delaying one server is possible but requires a change to the programme plan and will draw attention to the discovery. What is the most effective response?

- A) Shut it down on schedule — one nightly file is probably vestigial, and the schedule is published.
- B) Pause this server's decommissioning; trace the dependency to its owner and confirm whether it is live; if live, re-plan its migration properly and adjust the programme schedule through the change process — reporting the discovery, and checking what else the dependency-mapping missed.
- C) Shut it down but keep a recent backup so it can be restored if payroll complains.
- D) Delay quietly without telling the programme, absorbing the schedule slip into other tasks.

**Correct answer: B**

**Explanation:** "Nightly file from a payroll process" is among the most dangerous phrases in decommissioning: the consumer may be invisible until month-end, and payroll failures convert directly into people not being paid — a harm no published schedule outweighs. Option B follows the full professional arc. Pause the one server (not the programme). Trace to the owner and confirm liveness — "probably vestigial" (option A) is a hypothesis, and hypotheses about payroll get verified, not shipped. Re-plan through the change process, visibly: the schedule adjustment "drawing attention to the discovery" is a feature — programmes make good decisions on surfaced information, and your role-level duty to oversee such work includes keeping plans truthful. And the closing check — what else did the dependency-mapping miss? — converts one catch into systematic assurance, the **Problem management** move of treating the near-miss as evidence about the method. Option C is recovery theatre: restoring a decommissioned server after a missed payroll run repairs the server, not the pay run, and mid-restore is the worst place to rediscover a dependency. Option D fixes the risk while corrupting the record — quiet slips surface eventually as unexplained variance, spending the trust that visible, reasoned changes would have built. Proactive ownership means the discovery is treated as the programme's good luck, and handled so it stays that way.

**Question 10 (hard) — Your own past decision is the problem**

Two years ago you selected and implemented the backup platform the department now uses. A new engineer on your team, preparing a restore test, presents you with careful evidence that the platform's deduplication configuration — as you originally designed it — silently degrades restore performance as the estate grows, and restores of the largest systems would now breach their recovery time objectives by hours. The finding is correct; the design choice was yours; nobody else has connected it to you specifically. What is the most effective response?

- A) Validate the finding, credit the engineer, own the original decision openly — including to your head of service — and lead the remediation: quantify current exposure, mitigate the largest systems first, and fix the configuration pattern for the estate.
- B) Validate the finding and lead remediation, but present the original design choice as a collective decision of the time.
- C) Thank the engineer, downplay the urgency, and schedule remediation quietly across the next year to avoid drawing attention to the original choice.
- D) Challenge the methodology of the finding until the evidence is unanswerable.

**Correct answer: A**

**Explanation:** The engineering is straightforward — RTO breaches on the largest systems are a live continuity exposure demanding quantification and prioritised mitigation. The test is whether ego taxes the response, and option A pays no tax: validation on the evidence, named credit to the engineer (a new team member whose first major finding challenged the senior's own work — how you receive it will set their candour, and the team's, for years), open ownership of the decision including upward, and remediation led at the pace the exposure warrants. Owning it openly is not ceremonial: it models exactly the accountability you require of others (see how you handled their mistakes), it pre-empts the corrosive version where the connection surfaces later alongside evidence you knew, and it reframes the story as "our review process works" — which is true and creditable. Option B remediates fully but launders the authorship; collective camouflage is a small lie with a large signature, and the engineer holding the design documents knows whose name is on them. Option C prices reputation above recovery objectives — a year of quiet exposure so the author stays comfortable. Option D deploys seniority as friction against unwelcome evidence; the methodology deserves ordinary scrutiny, not adversarial exhaustion, and everyone watching learns whether evidence or rank wins here. Two years of estate growth changed the facts; the measure of a senior engineer is being harder on their own past work than anyone else would dare to be.

**Question 11 (hard) — Competing crises with a team to direct**

At 09:00 two situations land simultaneously: (1) the payments-supporting database cluster has lost one of its two nodes — service is running on the survivor with no redundancy, and the vendor needs diagnostic data within the hour to meet today's fix window; (2) a security advisory requires an emergency assessment of whether your internet-facing infrastructure is exposed to an actively exploited vulnerability, with the security team needing your infrastructure analysis by noon. You have two capable engineers available: one strong on databases, one strong on networks; you cannot personally drive both. What is the most effective response?

- A) Take the database issue yourself — payments outranks everything — and let the security assessment wait until it is done.
- B) Assign the database engineer to the cluster with the vendor deadline as their brief, assign the network engineer to the exposure assessment with the security team, define for each what done looks like and the escalation trigger that brings them back to you, and position yourself to supervise both, unblock either, and handle communications.
- C) Split both engineers across both tasks so each crisis has redundancy.
- D) Ask your head of service to decide which crisis matters more.

**Correct answer: B**

**Explanation:** The scenario is engineered so both demands are legitimate, deadlined, and parallel — the test is whether you multiply yourself through the team or collapse into the strongest individual contributor available. Option B is direction as your role level defines it: match specialists to their strengths, give each a crisp brief (deliverable, deadline, what "done" looks like), define escalation triggers in advance (the moment at which the database engineer pulls you in is decided at 09:05, not discovered at 10:40), and occupy the position only you can hold — cross-crisis awareness, unblocking, and stakeholder communication, so neither engineer burns diagnostic time writing updates. Option A abandons a same-day security deadline to do work your database engineer can do, converting a two-track morning into a one-track one with a senior engineer as the bottleneck — prioritisation between the crises was not actually required, only parallelisation. Option C halves everyone: four half-briefed part-assignments, two context-switching engineers, and no one accountable for either outcome. Option D escalates a question that is yours — this is exactly the operational direction seniors exist to provide, and the head of service's useful involvement is being informed via your communications, not deciding your dispatch. Note the quiet skill in B's design: the briefs make both engineers succeed without you, which is what "lead and direct infrastructure specialist teams" builds toward — a team that handles two crises well is the artefact of a senior who assigns well.

**Question 12 (hard) — Sustained under-resourcing versus quiet heroics**

For three months your team has covered a vacancy and a long-term absence by working substantially beyond sustainable levels — late changes, skipped improvement work, and two near-miss errors you attribute to fatigue. Management's view, based on green service dashboards, is that "the team is coping well". A major migration is now being scoped on the assumption that current output continues. Your instinct is to keep absorbing — the team takes pride in never dropping a service. What is the most effective response?

- A) Keep absorbing — the pride is real, the services are green, and the vacancy will eventually be filled.
- B) Present management with the true position, evidenced: the coverage cost (deferred maintenance, abandoned improvement work, the two fatigue-linked near-misses), the unsustainability trend, and the migration assumption it invalidates — with options (backfill, descope, re-sequence) and a recommendation; meanwhile, deliberately shed lower-value work to protect safety-critical attention.
- C) Unilaterally cut services back to sustainable levels and let the dashboards go amber until management notices.
- D) Tell the team to slow down quietly while continuing to report full capacity upward.

**Correct answer: B**

**Explanation:** The green dashboards are the trap: they are true about services and false about the system producing them, because the team is converting its own reserves — maintenance, improvement, rest — into service continuity, and the two near-misses are the leading indicators of where that conversion ends. Option B does the senior duty in full: workforce input is precisely your role level's remit ("provide input into overall management — workforce, budget..."), and input that lets a migration be scoped against phantom capacity is input withheld. The evidence structure matters — near-misses, deferred work, and trend turn "we're tired" into a risk narrative management can act on — and the options-plus-recommendation format makes acting easy. The interim measure (shedding lower-value work deliberately, visibly) is triage by decision rather than by fatigue-driven error. Option A extends the heroics until the near-misses stop being near — pride in never dropping a service is a genuine asset being spent as a concealment mechanism. Option C makes the point through service degradation: using users as signalling is the one move worse than silence, and it hands management a performance problem instead of a resourcing one. Option D falsifies upward while decelerating downward — the migration still gets scoped on capacity you are quietly not providing, landing the collision later and worse. Sustainable teams are a deliverable; the courage to report the true cost of green is what leading a team, rather than spending one, looks like.

### Preparation tips

- **Audit your review habits.** Before your next three design reviews, separate your comments into "requirement/risk/standard" and "personal preference" — and label the latter optional. The discipline transfers directly to review scenarios.
- **Rehearse receiving unwelcome evidence.** Practise the sequence — validate, credit, own, remediate — on small instances (a wrong estimate, a stale runbook) so it is available for large ones. Scenarios about your own past decisions are seniors' most-failed items.
- **Pre-define escalation triggers.** In real delegations this week, state the condition that should bring the work back to you. Options that include pre-agreed triggers are consistent high scorers, and the habit makes you the engineer those options describe.
- **Quantify before you argue.** In pressure scenarios — risk acceptance, resourcing, softened reports — the winning options carry numbers (users affected, minutes, near-misses). Practise converting instincts into quantified exposure.
- **Route decisions to their owners with a recommendation.** Neither seizing others' decisions nor abdicating your own scores well. For any live disagreement at work, ask: who owns this risk, and have I made it decidable for them?
- **Watch your credit and blame flows.** The scenarios probe both directions: credit given specifically and publicly, responsibility taken personally and upward. Notice what you did in the last real instance of each.
- **Read scenarios for the deliberately planted fact.** Senior SJT items embed the decisive detail — the documented safe pause, the process that could not have caught the error, the explanatory evidence you did not cover. Find it before choosing.

### Common pitfalls to avoid

- **Doing instead of directing.** Taking the crisis yourself when a capable specialist is available converts leadership into bottleneck. The strong options assign, brief, and supervise.
- **Taste enforced as standard.** Requiring rework to your personal style, redoing others' sound work, or approving with diminishment — review-authority misuse is a recurring designed distractor.
- **Punishing candour, rewarding concealment.** Any response that makes honest reporting more costly than silence — formal cautions for self-reported process-gap errors, softened records, private files — scores low and corrodes real teams.
- **Authority resolving what evidence should.** Domain seniority, specialist deference, and management escalation are all wrong answers to "which hypothesis is true". Discriminating tests decide.
- **Substance traded under presentation pressure.** Reframing, phasing, and sequencing are legitimate; describing hard requirements as optional, risks as monitored, or capacity as full is not. Know which side of the line each option sits on.
- **Quiet fixes of loud problems.** Unannounced schedule slips, secret remediation, dashboards kept green by team reserves — options that manage appearances while the record diverges from reality are the senior test's signature trap.
- **Heroics as a resourcing strategy.** Absorbing indefinitely, covering silently, and letting pride conceal cost all defer the collision and enlarge it. The high-scoring options make true costs visible with options attached.

## Conclusion

Congratulations — you have worked through a complete, senior-calibrated set of practice materials across the four assessment types you are most likely to meet: cognitive ability, numeric reasoning, verbal reasoning, and situational judgement. Pause and take stock of what you have exercised, because it is a fair portrait of the role itself.

In the cognitive section, you separated recurring incident signatures from noise, tested proposals against failure domains, found the missing negative-path test condition, propagated placement constraints to their forced conclusion, weighed anecdote against instrumentation, and carried an unresolvable requirement conflict back to its design authority with evidence and options. In the numeric section, you converted availability targets into felt minutes, projected growth through step changes, computed contractual figures from raw counts rather than flattering summaries, priced options from unit rates, and reconciled conflicting sources to the definition that governs them. In the verbal section, you held clauses to their stated subjects and tenses, assembled deadlines from scattered contract provisions, calibrated correlation against causation, and judged communications by the only standard that matters at your level — whether the recipient can decide well. In the situational judgement section, you rehearsed the judgement seniority actually consists of: approving work you would have done differently, protecting candour after mistakes, crediting your team in the rooms that matter, keeping substance intact under presentation pressure, directing parallel crises through others, and being harder on your own past decisions than anyone else would dare to be.

The through-line deserves stating: at senior level, these assessments measure the multiplication of your judgement through systems, suppliers, and people. Every technique this guide has drilled — verify mechanism against requirement, define the base before dividing, give conditional clauses full force, quantify before arguing, route decisions to their owners with recommendations — is simultaneously a test technique and a working discipline that your team will absorb by watching you.

As next steps: revisit the hardest questions in a week, when the explanations have composted into technique. Run one real artefact — this quarter's supplier report, the current design pack, your last roadmap input — through the relevant section's method and see what it yields; the findings will be real. And pick one behavioural pattern from the situational judgement section — perhaps pre-defined escalation triggers, or the validate-credit-own-remediate sequence — and use it deliberately this month.

If a live assessment is ahead, arrive rested, pace yourself deliberately, estimate before calculating, and let passages speak for themselves. The capabilities being sampled are ones you exercise every working day; preparation simply removes the friction between what you can do and what the test can see.

You make architects' designs run, you keep services operating, and you are building the engineers who will do the same. That is consequential work, done largely out of sight — and the care you have just invested in sharpening it is exactly the professionalism the role deserves. Good luck: you are thoroughly prepared.
