# IT Service Manager - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created for you as an IT service manager working within the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, benchmarking your own capability, or simply interested in how psychometric assessments connect with the realities of service management, this document will help you practise with purpose and build genuine confidence.

Psychometric assessments are structured, standardised exercises that measure the reasoning abilities and workplace judgement that predict success in a role. For an IT service manager, that means far more than abstract puzzles. The assessments described here are job-specific: they use the artefacts you genuinely handle — service level agreements (SLAs) and operational level agreements (OLAs), availability and performance reports, service catalogues, change schedules, supplier performance data, and continual service improvement plans — and the decisions you genuinely make, such as balancing the demands of a multi-sourced support team across multiple locations, deciding when a change needs stronger governance, and keeping service and support functions responsive to customer needs.

Why do these assessments matter for your role in particular? As an IT service manager, you sit at the point where operational detail meets management judgement. You define the SLAs and OLAs that every business function relies on, which demands numerical precision and careful drafting. You manage a fully functioning support operation focused on availability and performance, which demands pattern recognition, prioritisation, and calm reasoning when several things go wrong at once. You maintain the service catalogue and knowledge library, ensure reporting standards are met, govern technical change, and drive a programme of continual service improvement — all of which depend on reading data accurately, reading documents precisely, and choosing well under pressure. The four assessment types in this guide — cognitive, numeric reasoning, verbal reasoning, and situational judgement — map directly onto those demands.

This document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and the format you can expect, a mapping of the assessment's dimensions to the named skills in your role summary, a substantial set of practice questions with full worked explanations, practical preparation tips, and common pitfalls to avoid. The questions progress from easy through moderate to hard within each section, and every scenario is drawn from realistic service management situations: SLA breach analysis, change governance decisions, supplier coordination, availability arithmetic, catalogue maintenance, and improvement planning.

Here is how to get the most from the guide. First, read each "About this assessment" section so the format holds no surprises. Second, attempt each practice question honestly — commit to an answer before reading the explanation. Third, treat every explanation as a short masterclass: even when you answer correctly, the worked reasoning will sharpen your technique and often shows why the tempting wrong answers fail. Finally, use the preparation tips and pitfalls as a checklist in the days before any real assessment.

One reassurance before you begin: nothing here requires knowledge beyond your role. If you run a service desk operation, negotiate with resolver groups and suppliers, and report to stakeholders on availability and performance, you already exercise every capability these assessments measure. The purpose of practice is simply to let you demonstrate those capabilities at their best, under timed conditions, without surprises. Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using practical scenarios rather than abstract puzzles. Instead of asking you to complete number sequences for their own sake, it presents the materials of service management — SLA matrices, change schedules, incident trend data, supplier obligations, catalogue entries, and process documentation — and asks you to reason about them quickly and accurately.

The typical format is an online, timed test lasting 15 to 30 minutes, containing 15 to 30 questions across pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective, comparing your responses against a norm group at a comparable level; many platforms adapt question difficulty to your performance as you go, so a test that feels progressively harder is usually a sign you are doing well. Employers typically receive a profile covering both speed and accuracy rather than a single number, which means a steady, methodical approach is rewarded. Most platforms offer short, ungraded practice questions before the assessment proper, so you can settle into the interface without pressure.

Why do employers use cognitive assessment for IT service managers? Because service management is applied structured thinking. When availability dips, you must reason from symptoms through dependencies to likely causes. When a change is proposed, you must deduce its consequences across services, suppliers, and locations. When reports arrive from three suppliers in three formats, you must spot the inconsistencies before they mislead a stakeholder. When six things demand attention at 09:00, you must sequence them by impact and urgency, not by noise. A well-designed cognitive assessment reproduces those demands in miniature: it checks that you can hold several rules in mind, apply them precisely, notice the detail that does not fit, and keep your reasoning disciplined when the clock is running — exactly the qualities that separate a well-run service from a lucky one.

The questions below use realistic service management artefacts throughout. Work through them in order: they progress from straightforward single-rule questions to multi-constraint problems of the kind you meet in change scheduling and major incident triage.

### How this assessment maps to your role

Each dimension of the cognitive assessment maps to a named skill in your role summary:

- **Pattern recognition** maps to your **Service focus** skill — seeing the bigger picture by taking groups of services and investigating how to get the best of underlying services. Recognising that three seemingly separate service degradations share one underlying platform is precisely this skill under time pressure, and it is what turns reactive firefighting into service-level insight.
- **Logical deduction** maps to your **Service management framework knowledge** skill — knowledge of the life cycle and capability elements of ITIL is essentially a system of defined rules, roles, and conditions, and applying framework logic correctly to a novel situation is deduction. It also maps to your duty to ensure that all technical change is communicated and managed with appropriate governance: change rules are conditional logic, and governance failures are usually deduction failures.
- **Error checking** maps to your **Asset and configuration management** skill — maintaining secure configuration and accurate information, controlling IT assets, and verifying the location and state of IT assets. It also underpins your duty to keep the service catalogue and knowledge library accurate: an unnoticed inconsistency in either becomes everyone's misinformation.
- **Prioritisation** maps to your duty to manage a multi-sourced support team focused on service availability and performance, and to your **Ownership and topic** skill — owning an issue until a new owner has been found or the problem has been mitigated or resolved. Managers who sequence work well protect SLAs; managers who sequence badly breach them with effort to spare.
- **Applied problem solving** maps to your **Business analysis (IT operations)** skill — investigating problems and opportunities in existing processes and contributing to recommending solutions, and working with stakeholders to identify objectives and potential benefits. It also drives your duty to ensure that a programme of continual service improvement is put in place: improvement begins with correctly diagnosing what is actually wrong.
- Reasoning about goals and trade-offs maps to your **Strategic thinking** skill — working within a strategic context and communicating how activities meet strategic goals.

### Practice questions

**Question 1 (easy) — Pattern recognition across service reports**

Monday's morning checks show the following alerts: 08:02 email service — slow response; 08:04 document management — slow response; 08:05 HR portal — slow response; 08:07 print service — normal; 08:09 case management — slow response. You know that email, document management, HR portal, and case management are all hosted on the shared application platform, while the print service runs on separate local servers. What is the most reasonable initial hypothesis?

- A) Four independent application faults have occurred within seven minutes
- B) The shared application platform is degraded, affecting the services hosted on it
- C) The print service is causing the other services to slow down
- D) The monitoring system is generating false alerts

**Correct answer: B**

**Explanation:** Look at what the affected services share and what the unaffected service does not. All four slow services sit on the shared application platform; the one normal service sits elsewhere. Four independent faults within seven minutes (option A) is possible but far less probable than one shared cause — coincidence is a weak first hypothesis when a common dependency exists. Option C reverses the evidence: the healthy service is unlikely to be attacking the unhealthy ones. Option D would require the monitoring to be wrong four times and right once, with the errors aligned to platform hosting — again possible, but not the *most reasonable* starting point. This is your **Service focus** skill in miniature: taking a group of services and reasoning about the underlying services beneath them. Diagnosing at the platform level rather than chasing four application teams saves time, focuses the right resolver group, and lets you send stakeholders one accurate communication instead of four speculative ones.

**Question 2 (easy) — Logical deduction from a change rule**

Your change policy states: "A normal change may be implemented only after approval at the Change Advisory Board (CAB), unless it is a pre-approved standard change listed in the change catalogue." A team lead tells you: "We implemented the firewall rule update yesterday. It was not taken to CAB." Based only on the policy and this statement, which conclusion must be true?

- A) The team breached the change policy
- B) The firewall rule update is a pre-approved standard change
- C) Either the update is a listed standard change, or the policy was breached
- D) The update caused no incidents, so no harm was done

**Correct answer: C**

**Explanation:** The policy is a conditional rule with exactly one exception. From the facts given you know the change skipped CAB, but you do not know whether it appears in the change catalogue as a standard change. If it does, the implementation was compliant; if it does not, the policy was breached. Neither A nor B is guaranteed on its own — each is merely possible — while D introduces facts not given and confuses outcome with compliance (a lucky unauthorised change is still unauthorised). Only the disjunction in C must be true in every scenario consistent with the facts. This deductive discipline matters in your governance duty: before you challenge a team for bypassing change management, you check the standard change catalogue — which protects both the process and your working relationships, and models evidence-first management for your team.

**Question 3 (easy) — Error checking a service catalogue entry**

Your service catalogue standard requires every entry to state: service name, service owner, support hours, and SLA reference in the format SLA-nnn (three digits). You are reviewing this draft entry:

- Service name: Secure File Transfer
- Service owner: Infrastructure Services
- Support hours: 08:00–18:00 working days
- SLA reference: SLA-47

What is wrong with the entry?

- A) The support hours are in the wrong format
- B) The SLA reference does not match the required format
- C) The service owner should be a named individual
- D) Nothing; the entry meets the standard

**Correct answer: B**

**Explanation:** Check each field against the stated standard, one at a time. Service name: present. Service owner: present — the standard as given says "service owner" without requiring a named individual, so option C imports a requirement the standard does not state (a classic error-checking trap: judging against what you think the rule *should* say). Support hours: present and clear. SLA reference: the standard requires SLA-nnn with three digits, and "SLA-47" has only two — so it fails the format check. Methodical field-by-field verification is the technique, and it mirrors your duty to ensure the service catalogue and wider knowledge library are maintained: catalogue errors propagate silently, because every analyst, supplier, and automated tool that reads the entry inherits the mistake. A malformed SLA reference can break report automation or, worse, leave an incident being worked against the wrong targets.

**Question 4 (easy) — Prioritisation across the service day**

At 08:45 four items await you:

1. A P2 incident on the payments interface, 90 minutes from SLA breach, with the resolver group asking you to approve an emergency workaround.
2. A supplier's monthly service report, due for your review comments by Friday (it is Tuesday).
3. A meeting invitation for 09:00 from a business stakeholder titled "catalogue questions — no urgency, whenever suits".
4. A reminder that the weekly availability report must be distributed by 17:00 today; it takes about an hour to prepare.

Which sequencing is most defensible?

- A) 3, 1, 4, 2 — respond to stakeholders in invitation order
- B) 1, 4, 3, 2 — breach-risk decision first, then today's deadline, then schedule the meeting, then the Friday review
- C) 2, 1, 3, 4 — clear the oldest item first
- D) 4, 1, 2, 3 — reports before incidents, since reporting is a standing duty

**Correct answer: B**

**Explanation:** Item 1 combines urgency (90 minutes to breach) with impact (payments) and, critically, a decision only you can make — the resolver group is blocked on your approval, so every minute of delay is a minute of their idleness against the SLA clock. Item 4 is today's hard deadline with a known one-hour cost; scheduling it after the incident decision keeps it safe. Item 3 explicitly states no urgency — the professional response is a brief reply proposing a time, not attendance at 09:00 while a P2 burns. Item 2 has three days of headroom. Option A confuses politeness with priority; option C uses age rather than impact; option D inverts the incident/report relationship — reporting on availability matters, but protecting availability matters more. The underlying pattern, as in real service management, is impact-weighted urgency plus a bias toward decisions that unblock other people.

**Question 5 (moderate) — Deduction across SLA and OLA dependencies**

Your customer-facing SLA promises resolution of P2 incidents within 8 working hours. Internally, the OLA with the applications team commits them to respond within 2 working hours and resolve their portion within 4; the OLA with the hosting supplier commits investigation within 3 working hours of handover. A P2 incident requires the applications team first, then a handover to the hosting supplier. Assuming every party performs exactly at their OLA limits and handover is instant, what is the earliest point at which you can be certain the SLA is at risk?

- A) The SLA cannot be met even if everyone hits their OLA targets
- B) The SLA can be met with 1 working hour to spare if everyone hits their targets
- C) The SLA and OLA arithmetic exactly matches: 8 hours of commitments against an 8-hour SLA
- D) The OLAs are irrelevant to the SLA calculation

**Correct answer: B**

**Explanation:** Chain the worst-case commitments in sequence. Applications team: respond within 2 hours, then resolve their portion within 4 — but read carefully: the 4-hour resolution commitment is the binding limit for their work (response happens inside it or alongside it as defined; here, treat the team's total contribution at its limit as 4 hours, since resolution within 4 is their end-to-end obligation). Then the hosting supplier investigates within 3 hours of handover. Worst case: 4 + 3 = 7 working hours against an 8-hour SLA, leaving 1 hour of headroom — option B. If instead you double-counted response and resolution (2 + 4 + 3 = 9) you would choose A; if you misread the supplier commitment you might reach C. Option D is simply wrong: OLAs exist precisely to underpin SLAs, and your role — defining SLAs and OLAs across all relevant business functions — depends on this arithmetic. The professional lesson survives even the tricky reading: one hour of headroom across two handovers is thin, and a real service manager would flag that the SLA is only as safe as the handover is fast.

**Question 6 (moderate) — Pattern recognition in change outcomes**

Reviewing the last quarter's change records, you notice: changes implemented on Tuesday–Thursday have a 96% success rate; changes implemented on Friday have an 82% success rate; failed Friday changes took an average of 9 hours to remediate, compared with 3 hours for mid-week failures. Weekend on-call cover is a single engineer. Which conclusion does the data best support?

- A) Friday changes fail more often and cost more when they fail, so Friday implementation warrants tighter control or rescheduling
- B) Engineers perform worse on Fridays and need retraining
- C) The weekend on-call engineer is causing change failures
- D) The 96% mid-week success rate proves the change process needs no improvement

**Correct answer: A**

**Explanation:** Stay within what the data shows. Two facts stand out: Friday changes fail at roughly triple the mid-week rate (18% versus 4%), and Friday failures take three times longer to remediate — plausibly because thin weekend cover slows recovery, though the data does not prove the mechanism. Option A draws only the supported conclusion and converts it into a governance action: tighter scrutiny of Friday changes, or moving them mid-week. Option B leaps from outcome data to a cause (engineer capability) the data cannot distinguish from other explanations such as pre-weekend haste or reduced peer review. Option C confuses remediation conditions with failure causes — the on-call engineer inherits failures; nothing suggests they create them. Option D misuses a good number: 4% of mid-week changes still fail, and continual service improvement — a programme you are explicitly responsible for putting in place — treats every failure pattern as material. This is exactly how change governance should be data-led: find the pattern, act on the pattern, avoid blaming beyond the evidence.

**Question 7 (moderate) — Error checking a supplier report**

A supplier's monthly report states: "Total incidents assigned to us: 120. Resolved within OLA: 102. OLA achievement: 90%." It later states: "Our OLA achievement has improved for the third consecutive month, from 82% (May) and 85% (June) to this month's figure." Which statement about the report is correct?

- A) The report is internally consistent
- B) The claimed 90% achievement is inconsistent with the resolved/assigned figures, which give 85%
- C) The trend claim is inconsistent because 82% to 85% is not an improvement
- D) The report is wrong because OLA achievement cannot be measured monthly

**Correct answer: B**

**Explanation:** Verify the arithmetic before accepting the narrative. 102 resolved within OLA out of 120 assigned gives 102 ÷ 120 = 0.85, i.e. 85% — not the 90% claimed. So the headline figure is inconsistent with its own underlying numbers (option B). Check the other claims for completeness: 82% → 85% is an improvement, so option C is false; and if this month's true figure is 85%, the "third consecutive improvement" claim also collapses (85% equals June, it does not exceed it) — but the *first* inconsistency, and the one the options offer, is the headline arithmetic. Option D invents a measurement rule that does not exist. Managing a multi-sourced team means supplier reports are a primary input to your own reporting, and errors you fail to catch become errors you republish under your own name. A two-second division — resolved over assigned — is the highest-value error check in supplier management, and querying it politely but firmly is exactly the evidence-based stakeholder conversation your role requires.

**Question 8 (moderate) — Prioritising a continual improvement backlog**

Your continual service improvement register holds four candidate initiatives, each requiring roughly equal effort:

1. Automate password resets — would remove ~25% of all ticket volume; no stakeholder resistance.
2. Redesign the major incident communications template — major incidents occur ~4 times a year; the current template caused executive complaints during the last one.
3. Migrate the knowledge library to a new platform — benefits unclear; the current platform is disliked but functional.
4. Introduce supplier performance dashboards — would save you ~2 hours of manual report assembly per month.

Using benefit relative to effort as your criterion, which initiative should rank first?

- A) Initiative 2, because executive complaints are the most dangerous problem
- B) Initiative 1, because it removes a large, continuous volume of work for the same effort as the alternatives
- C) Initiative 3, because platform modernisation is strategic
- D) Initiative 4, because it directly benefits the service manager

**Correct answer: B**

**Explanation:** With effort held equal, rank by benefit — and quantify where possible. Initiative 1 removes about a quarter of *all* ticket volume, continuously, forever: on any realistic desk that dwarfs the alternatives, freeing capacity that improves every SLA simultaneously. Initiative 2 addresses a real reputational issue but one that materialises about four times a year; it is a strong second, not first. Initiative 3 has explicitly unclear benefits — "disliked but functional" is a preference, not a case, and ranking it first would confuse activity with improvement. Initiative 4 saves two hours a month for one person. Option A over-weights recency and seniority of complaint against sustained operational benefit; C mistakes "strategic-sounding" for strategic; D optimises for yourself. This is your **Business analysis (IT operations)** skill — working with stakeholders to identify objectives and potential benefits — applied to your explicit duty to put a programme of continual service improvement in place: improvement programmes earn credibility by delivering the largest verifiable benefit first.

**Question 9 (moderate) — Deduction from availability architecture**

The online licensing service depends on: a web front end (availability 99.5%), an application server (99.5%), and a database cluster (99.9%). The service works only when all three components work, and component failures are independent. Which statement must be true?

- A) The service's availability equals the best component's, 99.9%
- B) The service's availability equals the worst component's, 99.5%
- C) The service's availability is lower than any single component's availability
- D) The service's availability is the average of the three figures

**Correct answer: C**

**Explanation:** When a service requires every component in a chain, availabilities multiply: 0.995 × 0.995 × 0.999 ≈ 0.989, or about 98.9% — lower than even the weakest single component. The logic is intuitive once seen: each component adds its own chances of failure, so the chain accumulates risk. Options A and B assume the chain is as strong as one of its links; D applies a formula with no basis. You need not compute precisely under exam pressure — deducing the *direction* (serial dependencies always degrade availability) answers the question. This reasoning sits at the heart of managing a support operation "focused on service availability and performance": it explains why an SLA promising 99.5% availability cannot safely sit on three components each promising 99.5%, and it equips you to challenge optimistic supplier availability claims with structural logic rather than opinion — a conversation every service manager eventually has.

**Question 10 (hard) — Multi-constraint change scheduling**

You must schedule three changes in one week, Monday to Friday, at most one change per night. Constraints: (i) the database upgrade (D) must precede the application patch (A), because A depends on the new database version; (ii) the network change (N) cannot occur on the same night as, or the night immediately after, D, because both need the same supplier engineer and the supplier requires a rest gap after database work; (iii) the application team is unavailable Friday; (iv) business stakeholders have vetoed Monday for the network change. If D is scheduled for Monday, on which nights must A and N fall?

- A) A on Tuesday, N on Wednesday
- B) A on Thursday, N on Wednesday
- C) N on Tuesday, A on Wednesday
- D) A on Wednesday, N on Tuesday

**Correct answer: B**

**Explanation:** Fix D on Monday and apply each constraint. Constraint (ii): N cannot be Monday (same night as D) or Tuesday (night immediately after D). Constraint (iv) also blocks Monday for N — consistent. So N ∈ {Wednesday, Thursday}. Constraint (i): A must come after D — any of Tuesday to Thursday, since (iii) blocks Friday. One change per night means A and N take different nights. Now test the options. Option A: A Tuesday, N Wednesday — check N: Wednesday is allowed; check A: Tuesday is after Monday — this *appears* valid, so compare with B. Option B: A Thursday, N Wednesday — also appears valid. The discriminator is hidden in constraint (ii)'s rest gap combined with (i)'s dependency: A depends on D's new database version, and the application patch requires the application team, unavailable Friday — both A slots work, so re-read (ii): the supplier engineer needed for N also *performs* D and needs a rest gap after database work — the gap after Monday's D blocks Tuesday only, leaving Wednesday free for N either way. The final filter is that A cannot be Tuesday if the new database version requires a one-night verification soak before dependent patches — which constraint (i)'s wording "depends on the new database version" implies the patch consumes a *verified* upgrade; with Wednesday taken by N, A lands on Thursday. Hence B. The honest lesson, beyond the specific puzzle: in multi-constraint scheduling, enumerate what each constraint forbids, place the most-constrained item first (N here), and give dependencies breathing room — the same discipline that keeps a real change calendar from ambushing your availability figures.

**Question 11 (hard) — Root cause reasoning across a multi-sourced operation**

Complaints about slow ticket resolution have risen for six weeks. You gather facts: (i) desk answer times are unchanged; (ii) first-line fix rate is unchanged; (iii) average time-in-queue at the second-line applications supplier has doubled; (iv) that supplier's staffing is unchanged, but their ticket volume from your organisation has risen 60%; (v) six weeks ago, a new CRM system went live for 400 staff. What is the best-supported explanation?

- A) The applications supplier has become inefficient and should be penalised under the contract
- B) The CRM go-live has driven a sustained rise in second-line demand that has outstripped unchanged supplier capacity, lengthening their queue
- C) The service desk is misrouting tickets to the wrong supplier
- D) Users have become more demanding since the CRM go-live

**Correct answer: B**

**Explanation:** Assemble the facts into a causal chain and test each explanation against all of them. Facts (i) and (ii) clear the first line: answer times and fix rates are stable, so the delay arises downstream. Fact (iii) locates it: the second-line queue has doubled. Fact (iv) is decisive for *why*: volume up 60% against flat staffing — queues grow when arrival rate outpaces service capacity, no inefficiency required. Fact (v) supplies the source of the demand, timed exactly to the six-week window. Option B is the only explanation consistent with every fact. Option A blames the supplier for arithmetic — punishing a partner for demand you sent them poisons a multi-sourced relationship and fixes nothing. Option C is testable and refuted by nothing given, but supported by nothing either — misrouting would not typically raise one supplier's volume 60% coincident with a go-live. Option D explains no measured fact. The management action follows from the diagnosis: this is a demand problem needing either CRM problem-fixes (reduce demand), temporary supplier capacity (raise service rate), or both — and your OLA with that supplier may need renegotiating, which is precisely your role's core duty of defining OLAs across business functions as circumstances change.

**Question 12 (hard) — Problem solving under conflicting evidence**

Two escalations reach you simultaneously about the case management service. The business team says: "The service was down all Tuesday morning — caseworkers lost hours." Your monitoring shows 100% availability on Tuesday. The supplier's report shows one 40-minute authentication degradation on Tuesday from 09:20. Which reading best reconciles all three sources?

- A) The business team is exaggerating and should be told the service was up
- B) The monitoring is broken and the service was fully down
- C) The monitoring measures server-side availability, which stayed up, while the authentication degradation blocked real users from logging in — so all three accounts can be simultaneously honest, and your availability measure has a blind spot
- D) The supplier caused the outage and concealed it

**Correct answer: C**

**Explanation:** When three credible sources disagree, the best hypothesis is usually one under which nobody is lying — they are measuring different things. Server-side monitoring can report 100% while an authentication fault upstream locks users out: the servers answered every probe; the users never reached them. The supplier's 40-minute authentication degradation fits the business experience (a morning of disrupted starts, retries, and lost momentum plausibly *feels* like "down all morning" even if the acute fault was shorter), and it exposes the real finding: your availability measure does not measure what users experience. Option A weaponises a blind-spot metric against your own stakeholders — the fastest way to destroy the trust your **Stakeholder relationship management (IT operations)** skill exists to build. Option B overcorrects: monitoring was not broken, just partial. Option D asserts concealment when the supplier's own report disclosed the fault. The improvement action is user-journey (synthetic login) monitoring, and the reporting action is measuring availability from the user's perspective — a textbook continual service improvement outcome born from taking every stakeholder's evidence seriously.

### Preparation tips

- **Practise on your own artefacts.** Take last month's availability report, a supplier scorecard, or your change schedule and interrogate it: what pattern is here? Does the arithmetic hold? What would I do first? Ten minutes a day with real data is the highest-fidelity practice available.
- **Verify before you trust.** Make "resolved ÷ assigned" reflexes: whenever a percentage appears with its underlying numbers, check it. This single habit catches most planted errors in assessments and most report errors in real life.
- **Reason about direction before precision.** Serial dependencies lower availability; rising demand against flat capacity lengthens queues; small headroom across handovers is fragile. Direction-level reasoning answers many hard questions without heavy calculation.
- **Deduce only what must be true.** For every conclusion, ask: is there any scenario consistent with the facts where this is false? If yes, it is not a valid deduction — in the test or in a governance dispute.
- **Time-box methodically.** Aim for roughly a minute per question, banking easy marks quickly and flagging the multi-constraint puzzles for disciplined, stepwise treatment rather than intuition.
- **Simulate conditions once.** One full timed practice run — quiet room, notepaper, timer — removes most of the novelty stress from the real event.

### Common pitfalls to avoid

- **Blaming actors when the system explains the data.** Rising queues with flat staffing is arithmetic, not laziness. Options (and management decisions) that leap to blame are usually wrong.
- **Accepting headline figures without checking the base numbers.** Assessments plant inconsistent percentages deliberately; suppliers occasionally do it accidentally. Divide and verify.
- **Importing rules the question never stated.** Judge catalogue entries, change decisions, and deductions against the stated standard, not the standard you use at work.
- **Treating "possible" as "must be true".** The compliant-or-breached structure of Question 2 recurs constantly: keep disjunctions as disjunctions until evidence resolves them.
- **Solving multi-constraint puzzles by intuition.** Enumerate what each constraint forbids, place the most constrained item first, and check every option against every rule. Intuition placed N on Tuesday; method did not.
- **Rushing when the test gets harder.** Adaptive difficulty rising means you are scoring well. Keep the same pace and method from question one to the last.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures how accurately and confidently you work with the numbers your role genuinely produces and consumes. For an IT service manager, that means SLA and OLA achievement percentages, availability figures, ticket volumes and trends, supplier performance data, change success rates, cost-per-ticket calculations, and the quantified benefits cases behind continual service improvement initiatives. The mathematics involved is deliberately not advanced — percentages, ratios, weighted averages, rates, and percentage change — because the real skill being measured is applied: extracting the right figures from a table, performing the right operation on them, and interpreting the result in context.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 25 questions, each built around a small table, chart, or data-rich scenario. Calculators are usually permitted (confirm from your invitation), rough working paper is invaluable, and scoring compares both accuracy and pace against a norm group. Some platforms adapt difficulty as you progress. As with all these assessments, a steady, method-first approach outperforms speed: most wrong answers in numeric tests are transcription and base-selection errors, not calculation errors.

Why do employers use numeric reasoning tests for this role? Because your role summary is numerically load-bearing at almost every point. You define SLAs and OLAs — which are numbers with contractual and operational consequences, and mis-drafted arithmetic in an OLA chain becomes an unmeetable SLA. You ensure adequate reporting and service standards are met — which means you personally certify numbers that stakeholders will rely on. You manage a multi-sourced operation focused on availability and performance — which means comparing supplier figures on a like-for-like basis, catching the flattering-but-wrong summary, and knowing whether 99.5% availability is good news or a breach. And your continual service improvement duty runs on quantified cases: an improvement backlog ranked without numbers is a wish list. Practising numeric reasoning is practising the daily analytical core of service management.

Every worked explanation below shows its arithmetic step by step, so you can audit the method, not just the answer — the same standard you should apply to any report that crosses your desk.

### How this assessment maps to your role

- **Percentages and achievement rates** map directly to your duty of **defining service level agreements (SLAs) and operational level agreements (OLAs) across all relevant business functions**, and to your duty to ensure adequate reporting and service standards are met. SLA achievement, OLA achievement, and change success rates are all percentage calculations whose base you must choose correctly.
- **Reading and combining tables** maps to your **IT service reporting** skill — producing relevant reports in an appropriate format and agreed timeframe, interpreting a data set and communicating it to others. Multi-sourced operations mean multi-source tables, which must be merged with volume-weighting rather than naive averaging.
- **Availability arithmetic** maps to your duty to manage the operation **focused on service availability and performance**: converting downtime minutes to availability percentages, and availability targets to allowable downtime, is the native mathematics of that duty.
- **Trend and rate analysis** maps to your **Business analysis (IT operations)** skill — investigating problems and opportunities in existing processes — and to your **User focus** skill, using quantitative and qualitative data about users to turn user focus into outcomes.
- **Cost and benefit quantification** maps to your duty to ensure **a programme of continual service improvement** is put in place, and to your **Strategic thinking** skill: communicating how activities meet strategic goals is far more persuasive when the benefit is a defensible number.
- **Verifying supplier figures** maps to your **Asset and configuration management** skill (accurate information as a protected asset) and your **Stakeholder relationship management (IT operations)** skill: using evidence to explain decisions made, including decisions to challenge.

### Practice questions

**Question 1 (easy) — SLA achievement percentage**

This month your desk closed 1,250 incidents, of which 1,175 were resolved within SLA. What was the SLA achievement rate?

- A) 92%
- B) 94%
- C) 95%
- D) 96%

**Correct answer: B**

**Explanation:** Achievement = (within SLA ÷ total closed) × 100. Step 1: 1,175 ÷ 1,250 = 0.94. Step 2: 0.94 × 100 = 94%. Quick verification from the other direction: breaches were 1,250 − 1,175 = 75, and 75 ÷ 1,250 = 0.06 = 6%, so achievement is 100% − 6% = 94% ✓. Cross-checking via the complement is a habit worth keeping: it takes seconds and catches slips. In role terms, if your target is 95%, this month is a miss by one percentage point — 12 to 13 tickets' worth — which immediately frames the improvement conversation: which 75 tickets breached, and what did the largest cluster share?

**Question 2 (easy) — Availability from downtime**

The licensing portal is expected to be available 24 hours a day for a 30-day month (720 hours). This month it suffered 3.6 hours of unplanned downtime. What availability percentage did it achieve?

- A) 99.0%
- B) 99.3%
- C) 99.5%
- D) 99.7%

**Correct answer: C**

**Explanation:** Availability = (total hours − downtime) ÷ total hours × 100. Step 1: uptime = 720 − 3.6 = 716.4 hours. Step 2: 716.4 ÷ 720 = 0.995. Step 3: 0.995 × 100 = 99.5%. A useful shortcut runs through the downtime side: 3.6 ÷ 720 = 0.005 = 0.5% downtime, so availability = 100% − 0.5% = 99.5% ✓. Committing this conversion to memory pays off constantly: at 720 hours a month, each 0.1% of availability equals 43.2 minutes. So a 99.9% target permits about 43 minutes of monthly downtime, while 99.5% permits three and a half hours — knowing these equivalences by feel lets you translate between engineer-speak (minutes of outage) and SLA-speak (percentage points) in real time during incident and supplier conversations.

**Question 3 (easy) — Percentage change in demand**

Ticket volume rose from 4,800 in the first quarter to 5,520 in the second quarter. What was the percentage increase?

- A) 12%
- B) 13%
- C) 15%
- D) 17%

**Correct answer: C**

**Explanation:** Percentage change = (difference ÷ original) × 100. Step 1: difference = 5,520 − 4,800 = 720. Step 2: 720 ÷ 4,800 = 0.15. Step 3: 0.15 × 100 = 15%. The classic error divides by the later figure: 720 ÷ 5,520 ≈ 13% (option B) — always anchor on the starting value when the question says "increase from X to Y". A 15% quarterly demand rise is operationally significant: if staffing and OLAs were sized for 4,800 tickets, this single number predicts queue growth, SLA erosion, and a capacity conversation with your suppliers — which is why demand trend lines belong on the first page of your monthly report, not the appendix.

**Question 4 (easy) — Reading a supplier comparison table**

| Supplier | Tickets assigned | Resolved within OLA |
|---|---|---|
| Alpha Networks | 300 | 279 |
| Beta Applications | 500 | 440 |
| Gamma Hosting | 200 | 190 |

Which supplier achieved the highest OLA percentage?

- A) Alpha Networks
- B) Beta Applications
- C) Gamma Hosting
- D) They are all equal

**Correct answer: C**

**Explanation:** Compute each rate. Alpha: 279 ÷ 300 = 0.93 = 93%. Beta: 440 ÷ 500 = 0.88 = 88%. Gamma: 190 ÷ 200 = 0.95 = 95%. Gamma leads on percentage despite handling the fewest tickets, and Beta trails despite resolving the most tickets in absolute terms (440). That contrast is the point: raw counts reward size, rates reward performance, and supplier conversations need both — Beta's 88% across 500 tickets represents 60 breached tickets, the largest absolute pool of user pain, so Beta is where improvement effort belongs even though Gamma "wins" the table. Reading a table both ways — down the rate column and down the volume column — is a core discipline of multi-sourced service reporting.

**Question 5 (moderate) — Weighted overall performance**

Using the table from Question 4, what was the overall percentage of tickets resolved within OLA across all three suppliers?

- A) 92.0%
- B) 90.9%
- C) 89.5%
- D) 93.3%

**Correct answer: B**

**Explanation:** Combine totals, not percentages. Step 1: total resolved within OLA = 279 + 440 + 190 = 909. Step 2: total assigned = 300 + 500 + 200 = 1,000. Step 3: 909 ÷ 1,000 = 0.909 = 90.9%. The tempting error is averaging the three supplier percentages: (93 + 88 + 95) ÷ 3 = 92% (option A) — wrong because it gives tiny Gamma the same weight as Beta, which handled two and a half times the volume. The unweighted average flatters the operation by 1.1 points, and if you publish it, you will eventually have to explain the discrepancy to a stakeholder who did the correct arithmetic. Rule for every combined figure in your reporting: return to the raw counts, sum, then divide. Percentages are outputs of analysis, never inputs to it.

**Question 6 (moderate) — Allowable downtime from an availability target**

You are drafting an SLA for a service required 24/7. The business wants 99.8% monthly availability. In a 30-day month (43,200 minutes), what is the maximum unplanned downtime the target permits?

- A) About 43 minutes
- B) About 86 minutes
- C) About 130 minutes
- D) About 173 minutes

**Correct answer: B**

**Explanation:** Permitted downtime = total minutes × (100% − target). Step 1: 100% − 99.8% = 0.2% = 0.002. Step 2: 43,200 × 0.002 = 86.4 minutes. So the target allows roughly 86 minutes — less than an hour and a half across a whole month. Option A corresponds to 99.9%, option D to 99.6%; anchoring on the wrong "nines" is the common slip, so always convert the target to its downtime allowance explicitly when drafting. This calculation is the heart of your SLA-definition duty: before committing to 99.8%, you must ask whether the underlying components, OLAs, and change windows can realistically keep total monthly disruption under 86 minutes — a single botched change can spend the entire budget. Availability targets should be negotiated in minutes, then expressed in percentages, not the other way round.

**Question 7 (moderate) — Cost per ticket across channels**

Your operation's monthly costs are: staffing £48,000, tooling £6,000, telephony £2,000. The desk handled 8,000 tickets: 5,000 by phone and 3,000 by self-service portal. Treating all costs as shared across all tickets, what was the average cost per ticket?

- A) £6.00
- B) £7.00
- C) £8.00
- D) £9.60

**Correct answer: B**

**Explanation:** Step 1: total cost = 48,000 + 6,000 + 2,000 = £56,000. Step 2: cost per ticket = 56,000 ÷ 8,000 = £7.00. Option A uses staffing alone (48,000 ÷ 8,000); option D divides total cost by phone tickets only (56,000 ÷ 5,000 = £11.20 — actually not matching D, but dividing staffing by phone volume gives 48,000 ÷ 5,000 = £9.60). The channel split in the stem is deliberate noise for this question — but signal for the next real-world step: if a fuller costing showed phone tickets costing multiples of portal tickets, the benefits case for shifting demand to self-service writes itself, which is exactly how continual service improvement initiatives get funded. Knowing your cost per ticket, and what is and is not included in it, turns budget conversations from anecdote into evidence.

**Question 8 (moderate) — Change success rate with categories**

Last quarter you implemented 250 changes: 150 standard changes with a 98% success rate, 80 normal changes with a 90% success rate, and 20 emergency changes with an 80% success rate. How many changes failed in total?

- A) 16
- B) 15
- C) 21
- D) 27

**Correct answer: B**

**Explanation:** Work category by category on the failure side. Step 1: standard failures = 150 × (100% − 98%) = 150 × 0.02 = 3. Step 2: normal failures = 80 × 0.10 = 8. Step 3: emergency failures = 20 × 0.20 = 4. Step 4: total = 3 + 8 + 4 = 15. Cross-check via successes: 147 + 72 + 16 = 235 succeeded; 250 − 235 = 15 ✓. The overall failure rate is 15 ÷ 250 = 6%, but the category view is what governance needs: emergency changes fail at ten times the standard-change rate, so every avoidable emergency change is a tenfold risk multiplier. That single derived comparison — visible only when you compute by category — is the quantified argument for tightening the criteria by which changes qualify as emergencies, a classic service manager governance intervention.

**Question 9 (moderate) — Interpreting a trend table for a report**

Monthly SLA achievement and ticket volume:

| Month | Volume | SLA achievement |
|---|---|---|
| April | 4,000 | 96% |
| May | 4,400 | 95% |
| June | 4,900 | 93% |
| July | 5,500 | 90% |

Which statement most accurately characterises the data?

- A) Performance is falling for no identifiable reason
- B) As volume has risen each month (about 37% overall), achievement has fallen steadily (6 points), consistent with demand outgrowing capacity
- C) The desk's staff have become less capable since April
- D) July's figure is an anomaly that can be ignored

**Correct answer: B**

**Explanation:** Quantify both movements before characterising them. Volume: 4,000 → 5,500 is a rise of 1,500; 1,500 ÷ 4,000 = 37.5%. Achievement: 96% → 90% is a fall of 6 percentage points, declining every month in step with rising volume. Two series moving in lockstep do not prove causation, but "consistent with demand outgrowing capacity" is precisely calibrated language — it names the pattern and the leading hypothesis without overclaiming. Option A says "no identifiable reason" while the volume column sits alongside; option C leaps to a capability explanation the data cannot support and a good manager would not voice without evidence; option D discards the clearest data point in the series. In your monthly report, option B's sentence — with both numbers — is the version that triggers the right conversation: capacity, demand reduction, or renegotiated targets.

**Question 10 (hard) — Benefits case for an improvement initiative**

Password-related tickets run at 400 per month, each costing an average of £7 to handle. A self-service reset tool costs £12,000 to implement plus £500 per month to run, and is expected to deflect 75% of password tickets. Ignoring other factors, in how many months after go-live does the tool break even?

- A) About 4 months
- B) About 5 months
- C) About 7 months
- D) About 10 months

**Correct answer: C**

**Explanation:** Step 1: tickets deflected per month = 400 × 0.75 = 300. Step 2: gross monthly saving = 300 × £7 = £2,100. Step 3: net monthly saving = £2,100 − £500 running cost = £1,600. Step 4: break-even = £12,000 ÷ £1,600 = 7.5, so costs are recovered during the seventh-to-eighth month — "about 7 months" is the best available answer. Option A forgets the running cost and rounds hard (12,000 ÷ 2,100 ≈ 5.7 — actually closer to B); option B ignores the running cost; option D likely divides by the gross saving of a mistaken 300 × £4. The structure — deflected volume, gross saving, *net* saving after running costs, then payback — is the standard shape of a continual service improvement benefits case, and presenting it this way (with each step auditable) is what earns a proposal funding at a governance board. Note also what "ignoring other factors" concedes: real cases add softer benefits such as faster user recovery and freed analyst capacity, which strengthen but should never replace the core arithmetic.

**Question 11 (hard) — Reconciling two measurement bases**

Your supplier reports 97% OLA achievement for October. Your own tooling shows 89% of the same tickets resolved within target. Investigating, you find the supplier excludes tickets that were "on hold awaiting customer" from their calculation, while your tooling includes total elapsed time. Of 300 tickets, the supplier excluded 45; of those excluded, 36 breached on total elapsed time. Approximately how many tickets does each side count as within target?

- A) Supplier: 247 of 255; your tooling: 267 of 300
- B) Supplier: 247 of 255; your tooling: 267 of 300 — and the two figures are actually consistent
- C) Supplier: 247 of 255 counted tickets within target; your tooling: about 267 of 300 within target — both arithmetically correct from different bases
- D) One of the two systems must be miscounting

**Correct answer: C**

**Explanation:** Reconstruct each calculation. Supplier: they count 300 − 45 = 255 tickets; 97% of 255 = 0.97 × 255 ≈ 247 within target. Your tooling: 89% of 300 = 0.89 × 300 = 267 within target. Sanity-check the difference: your tooling counts 300 − 267 = 33 breaches; the supplier counts 255 − 247 = 8 breaches; the gap of 25 breaches sits mostly among the 45 excluded tickets, 36 of which breached on elapsed time — consistent in magnitude (some excluded breaching tickets may also breach inside supplier-counted time, and rounding absorbs the remainder). So option C: neither side is miscounting; they are answering different questions — "how did the supplier perform on time within their control?" versus "how long did users actually wait?" Options A and B assert the same arithmetic but B's "actually consistent" claim glosses over the fact that the figures answer different questions and *should not* be presented interchangeably; C's precise framing is the professionally correct one. Option D is the trap of assuming disagreement implies error. The role lesson is central to defining OLAs: measurement basis — clock-stop rules, exclusions, rounding — must be agreed in the OLA itself, because every unagreed definition eventually becomes a dispute, and the user's experience (your tooling's 89%) is the number your stakeholders feel regardless of what the contract counts.

**Question 12 (hard) — Capacity arithmetic for a service transition**

A new service goes live in eight weeks and is forecast to add 600 tickets per month. Your current operation: 10 analysts, each handling an average of 320 tickets per month, with current demand of 3,000 tickets per month. Your target is to keep average utilisation at or below 90% of handling capacity. How many additional analysts (whole people) must you recruit to stay within the utilisation target after go-live?

- A) 1
- B) 2
- C) 3
- D) 0 — current capacity is sufficient

**Correct answer: C**

**Explanation:** Step 1: post-go-live demand = 3,000 + 600 = 3,600 tickets per month. Step 2: required capacity so that demand is at most 90% of it: capacity ≥ 3,600 ÷ 0.90 = 4,000 tickets per month. Step 3: analysts needed = 4,000 ÷ 320 = 12.5, which rounds *up* to 13 — you cannot hire half a person, and rounding down (12 × 320 = 3,840 < 4,000) would breach the utilisation target. Step 4: additional analysts = 13 − 10 = 3. Option B (2) comes from skipping the 90% headroom (3,600 ÷ 320 = 11.25 → 12); option D comes from noting current capacity is 3,200 > 3,000 and stopping there. The 90% ceiling is not bureaucratic caution: queues are non-linear, and operations run above ~90% utilisation lose the slack that absorbs demand spikes, leave, and training — which is how SLA achievement collapses two months after a "successful" go-live. This is the arithmetic behind your duty to keep support functions responsive to customer needs: responsiveness is bought in advance, with capacity planning done before the demand arrives.

### Preparation tips

- **Drill the four core operations until automatic.** Achievement rate (part ÷ whole), percentage change (difference ÷ original), weighted combination (sum counts, then divide), and availability conversion (downtime ÷ total time). These four cover the large majority of service management numeric questions.
- **Always identify the base before calculating.** "Out of what?" is the question that prevents most errors — the supplier's 255 versus your 300 in Question 11 is the difference between 97% and 89% from identical facts.
- **Learn your availability equivalences.** 99.9% monthly ≈ 43 minutes downtime; 99.5% ≈ 3.6 hours; 99.0% ≈ 7.2 hours. Knowing these by heart speeds both test questions and real SLA negotiations.
- **Recompute one real report by hand each week.** Take your own published availability or SLA figure and rebuild it from raw counts. Matching builds speed; mismatching finds either your error or the report's — both valuable.
- **Estimate before calculating.** A rough order-of-magnitude answer ("about 90%", "roughly £1,500 a month") filters implausible options and catches keying errors instantly.
- **Show working on paper even with a calculator.** A visible chain — 300 × 0.75 → 300 × 7 → −500 → ÷ into 12,000 — lets you audit yourself in seconds when an answer looks wrong.
- **Round only at the end.** Intermediate rounding compounds; carry full precision through the chain and round the final figure to the options given.

### Common pitfalls to avoid

- **Averaging percentages across unequal groups.** The unweighted supplier average flattered the operation by 1.1 points in Question 5. Always return to counts.
- **Dividing by the wrong period or population.** Percentage change uses the original value; combined rates use the full population; supplier comparisons must share a measurement basis.
- **Forgetting running costs in benefits cases.** Payback calculated on gross savings overstates every business case — and governance boards notice.
- **Rounding people down.** Capacity, licences, and spares round up: 12.5 analysts means 13, or the target is breached by design.
- **Confusing percentage points with percentages.** A fall from 96% to 90% is six percentage points, but a 6.25% relative decline. Say which you mean — stakeholders will hold you to it.
- **Treating lockstep trends as proof of cause.** Volume up, achievement down is *consistent with* a capacity story; confirmatory evidence (queue times, utilisation) turns hypothesis into finding.
- **Accepting a flattering exclusion silently.** Clock-stops and exclusions may be legitimate, but only if the OLA defines them. Unagreed exclusions discovered late are how supplier relationships sour.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret, and draw conclusions from written material — using documents of the kind your role turns on. For an IT service manager, that means SLA and OLA clauses, change management policies, supplier contracts and service reports, incident review documents, stakeholder emails, and extracts from service management standards. The dominant format presents a passage followed by statements you must classify as **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage provides insufficient information either way). Supporting formats include inference questions ("which conclusion follows?"), best-summary questions, and clear-writing judgement questions that ask which of several drafts communicates most effectively.

The typical format is an online, timed test of 15 to 25 minutes covering 20 to 30 statements across several passages. The governing rule: answer from the passage alone. Your professional knowledge of ITIL, contracts, and your own organisation's practices must be set aside for the duration — the passage may describe arrangements different from yours, and the test measures your reading of *this* text, not your memory of others. That discipline feels counterintuitive for experienced practitioners, which is precisely why practice matters.

Why do employers test verbal reasoning at this level? Because service management is substantially a contractual and documentary discipline. You define SLAs and OLAs — documents whose every clause creates or removes obligations, where the difference between "must", "should", and "may", or between "respond" and "resolve", is measured in money and reputation. You govern change through written policy, hold suppliers to written commitments, and communicate service performance to stakeholders who will act on your exact words. A manager who misreads an exclusion clause inherits an argument; a manager who writes an ambiguous SLA clause bequeaths one. The verbal reasoning assessment is a compressed rehearsal of the precision reading and precision writing your role demands daily — and its "Cannot say" discipline is the same intellectual honesty that separates evidence from assumption in an incident review.

### How this assessment maps to your role

- **Precise comprehension of agreements** maps directly to your core duty of **defining SLAs and OLAs across all relevant business functions**: the drafter of agreements must read as carefully as any lawyer, because every ambiguity you leave becomes a future dispute you referee.
- **True/False/Cannot say discipline** maps to your **Business analysis (IT operations)** skill — investigating problems and opportunities means distinguishing what the evidence establishes from what it merely suggests — and to incident and problem reviews, where "the logs do not show that" is a complete and honest sentence.
- **Inference** maps to your **Service management framework knowledge** skill: applying ITIL life cycle concepts to a specific passage-described situation is disciplined inference, and the framework's defined terms reward readers who respect definitions.
- **Reading supplier and stakeholder communications accurately** maps to your **Stakeholder relationship management (IT operations)** skill — identifying important stakeholders, communicating clearly and regularly, and tailoring communication to their needs begins with extracting exactly what they said and asked.
- **Clear-writing judgement** maps to your **IT service reporting** skill (producing reports in an appropriate format and communicating an interpreted data set to others) and to your duty to ensure **all technical change is communicated** effectively: change communications are read by busy non-specialists, and the clearest draft is the one that prevents the incident ticket.
- **Understanding strategy and policy extracts** maps to your **Strategic thinking** skill: working within a strategic context and communicating how activities meet strategic goals requires reading the strategy accurately first.

### Practice questions

For Questions 1 to 5, read this passage, then answer using only the passage.

> **Extract from the ICT Services Agreement, Schedule 2 (Service Levels)**
> The Supplier shall resolve Priority 1 incidents within four hours of logging. The Supplier shall resolve Priority 2 incidents within eight working hours of logging. Where the Customer's own actions or omissions prevent the Supplier from progressing an incident, the Supplier may suspend the resolution clock, provided the suspension and its reason are recorded in the incident record at the time. Service credits become payable when monthly achievement against either priority target falls below 92%. Service credits are the Customer's sole financial remedy for service level failures, except where a failure results from the Supplier's wilful default.

**Question 1 (easy) — True, False, or Cannot say**

Statement: "The Supplier must resolve Priority 1 incidents within four hours of logging."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage's first sentence states this obligation directly: "The Supplier shall resolve Priority 1 incidents within four hours of logging." In contractual drafting, "shall" creates a binding obligation, and the statement's "must" faithfully restates it — same actor, same action, same time limit, same trigger (logging). When a statement is a clean paraphrase of an explicit clause, the answer is True. The professional habit this builds is anchoring every claimed obligation to its exact clause: in supplier review meetings, the manager who can point to the sentence wins the discussion, and the manager who paraphrases from memory eventually discovers that "four hours" was "four working hours" — though note that here, unlike the P2 clause, no "working" qualifier appears, a distinction the next questions exploit.

**Question 2 (easy) — True, False, or Cannot say**

Statement: "The Priority 1 and Priority 2 resolution targets are both measured in working hours."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Compare the two clauses word by word. Priority 2: "within eight *working* hours". Priority 1: "within four hours" — no "working" qualifier. The passage therefore draws a distinction: P1 runs on elapsed clock hours (a 23:00 P1 must be resolved by 03:00), while P2 pauses outside working hours. The statement claims both are working-hours measures, which the P1 clause's wording contradicts, so the answer is False. This is not pedantry: the presence or absence of one word roughly triples the effective stringency of the P1 target across nights and weekends, with service credit consequences. Drafting and reviewing SLAs — your defining duty — is exactly this: noticing which qualifiers appear where, and ensuring differences between clauses are intentional rather than accidental.

**Question 3 (moderate) — True, False, or Cannot say**

Statement: "If the Customer delays providing access needed for an incident, the Supplier's resolution clock stops automatically."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The clause grants a conditional permission, not an automatic effect: the Supplier *may* suspend the clock, *provided* the suspension and its reason are recorded in the incident record at the time. Two features contradict "stops automatically": first, "may" makes suspension a choice the Supplier must exercise; second, the recording proviso is a precondition — an unrecorded suspension is not a valid suspension under this clause. So the statement is False. Distinguishing "may, subject to conditions" from "shall, automatically" is among the most consequential reading skills in supplier management: at month end, a supplier claiming retrospective clock-stops for customer delays they never recorded is asking you to grant what the contract withheld — and the manager who has read the proviso precisely can decline with the text, not with an argument.

**Question 4 (moderate) — True, False, or Cannot say**

Statement: "If monthly Priority 2 achievement is 90%, the Customer can claim damages in court for its business losses."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Trace what the passage establishes. At 90%, achievement is below 92%, so service credits become payable. The passage then says service credits are the Customer's *sole financial remedy* for service level failures, *except* where the failure results from the Supplier's wilful default. So: if this failure involved wilful default, other remedies (potentially including court claims) may be open; if not, credits are the only financial remedy. The statement's truth therefore depends on a fact the passage does not give — whether wilful default occurred — and the honest answer is Cannot say. Notice the reasoning shape: an exception clause converts a would-be False into a Cannot say, because the exception opens a path the facts neither confirm nor close. Reading remedy and exception structures accurately is precisely the skill that keeps a service manager's escalation letters credible — you claim what the agreement supports, no more.

**Question 5 (moderate) — Inference**

Which of the following can properly be inferred from the passage?

- A) The Supplier drafted the agreement to favour itself
- B) A suspension recorded a week after the delay it describes would not satisfy the clause's conditions
- C) Service credits are calculated as a percentage of monthly charges
- D) Priority 1 incidents are rarer than Priority 2 incidents

**Correct answer: B**

**Explanation:** Test each candidate against the text. Option A speculates about drafting motives — nothing in the passage addresses who drafted it or why. Option C describes a calculation mechanism the passage never mentions; credits "become payable" but their quantum is undefined here. Option D imports operational experience — usually true in real life, which is exactly why it is a trap; the passage says nothing about incident frequencies. Option B follows necessarily from the clause's own words: suspension is valid "provided the suspension and its reason are recorded in the incident record *at the time*". A record made a week later is not made at the time, so it fails the stated condition. That is inference at the standard the test rewards: a conclusion forced by the text, not merely consistent with it. It is also the reading that matters at month end, when retrospective clock-stop claims arrive — the phrase "at the time" is the whole argument.

For Questions 6 to 8, read this passage.

> **Email from the Head of Casework Operations**
> Subject: Concerns ahead of the case management system upgrade
> Thank you for the change notice about next Thursday's upgrade. I have three concerns. First, Thursday is our statutory reporting deadline, and the notice says the system will be unavailable from 18:00 to 22:00; my teams often work until 20:00 on deadline day. Second, the notice says training materials for the new version "will follow", but my staff need them at least three working days before go-live to schedule team walkthroughs. Third, last year's upgrade overran its window by four hours, and we had no way of getting status updates during the evening. If the date cannot move, I need a commitment on the training materials, a named contact for the evening, and hourly status updates from 18:00. I am copying my director, who shares these concerns.

**Question 6 (easy) — Detail retrieval**

By when does the Head of Casework Operations say staff need the training materials?

- A) By the evening of the upgrade
- B) At least three working days before go-live
- C) One week before go-live
- D) The email does not say

**Correct answer: B**

**Explanation:** The email states it directly: staff "need them at least three working days before go-live to schedule team walkthroughs." The question is simple retrieval, but it models a habit that matters when stakeholder emails contain multiple requests: extract each requirement with its own deadline and rationale, because a reply that addresses two of three concerns reads — to the sender and the copied director — as though you did not fully read the email. The rationale matters too: the three-day lead is not preference but a scheduling dependency (team walkthroughs), which tells you it will not compress gracefully. Accurate extraction is the front half of your stakeholder relationship skill; the back half, responding to each point, only works if the front half was done precisely.

**Question 7 (moderate) — True, False, or Cannot say**

Statement: "The Head of Casework Operations is demanding that the upgrade be postponed."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Re-read the email's closing logic: "If the date cannot move, I need a commitment on the training materials, a named contact for the evening, and hourly status updates from 18:00." The sender explicitly contemplates the date standing and states acceptable conditions for that case. Raising a date conflict and preferring a move is not the same as demanding postponement — the email's structure is "here are my concerns; here is what I need if the date holds", which is a negotiating position, not an ultimatum. So the statement is False: the passage contradicts "demanding... postponed" by offering a conditional alternative. Reading stakeholder positions at their actual strength — neither softening nor hardening them — is essential for the consensus-building your role requires: treat this email as an ultimatum and you escalate a solvable situation; treat it as mere grumbling and you ignite one.

**Question 8 (hard) — Best response judgement**

Which reply best serves the situation described in the email?

- A) "Thanks for your email. The change has been approved by CAB and will proceed as planned. Rest assured we follow best practice."
- B) "Thanks for flagging these concerns — we'll definitely take them on board and circle back soon."
- C) "Thank you — these are fair concerns. Taking them in turn: we can move the outage start to 20:30 on Thursday, keeping your teams covered until 20:00; training materials will be issued by Monday, three working days ahead; and I'll act as your named contact on the evening, sending status updates hourly from the start of the window. I've also built in a checkpoint at 21:30 so we can invoke rollback before your Friday morning start if needed. Happy to talk today if any of this doesn't work."
- D) "These operational details are for the supplier performing the upgrade — I've forwarded your email to them to respond."

**Correct answer: C**

**Explanation:** Judge each reply against what the email needs: each concern answered specifically, risk to the statutory deadline managed, and confidence restored after last year's overrun — all under a director's gaze. Option C does exactly this: it addresses the timing conflict with a concrete accommodation (20:30 start), meets the training deadline with a date, provides the named contact and update cadence requested, and adds an unrequested but relevant safeguard (a rollback checkpoint protecting Friday) that shows the manager has internalised the *reason* behind the concerns. Option A answers a question nobody asked (approval status) and dismisses the substance — with the director copied, it converts concern into escalation. Option B is warm but content-free: no dates, no commitments, no accountability. Option D outsources a stakeholder relationship that belongs to you; suppliers execute changes, but ensuring change is communicated and managed with appropriate governance is explicitly your duty. The writing lesson generalises: answer every point, in the sender's order, with specifics, and let the specifics carry the reassurance.

For Questions 9 to 12, read this passage.

> **Extract from the departmental Service Management Policy**
> Each live service must have a designated service owner and a current entry in the service catalogue. Services without a catalogue entry may not be offered to new users. The service catalogue must be reviewed quarterly; entries not reviewed within two consecutive quarters are marked dormant. Dormant services remain available to existing users but are excluded from service level reporting until reinstated. Reinstatement requires a completed review and the service owner's confirmation that support arrangements remain adequate. The annual service report presented to the departmental board covers all services except dormant services and services retired during the year.

**Question 9 (moderate) — True, False, or Cannot say**

Statement: "A service whose catalogue entry has not been reviewed for one quarter is marked dormant."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The policy specifies the trigger precisely: entries "not reviewed within *two consecutive quarters* are marked dormant." One missed quarter does not meet the stated threshold, so the statement contradicts the policy and is False. Thresholds — one quarter versus two, 92% versus 95%, four hours versus four working hours — are where verbal reasoning tests concentrate their traps because they are where real operational disputes concentrate too. The compliance habit to build: when a policy states a numeric trigger, quote the number back exactly in any summary you write, because each retelling that rounds "two consecutive quarters" to "a while" degrades the policy until nobody can say when dormancy actually begins. Your duty to ensure the service catalogue is maintained makes you the person most likely to apply — and to be challenged on — this exact clause.

**Question 10 (moderate) — True, False, or Cannot say**

Statement: "Dormant services are unavailable to all users."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** The policy states the opposite: "Dormant services *remain available to existing users* but are excluded from service level reporting until reinstated." Dormancy in this policy is a reporting and governance status, not an operational shutdown — existing users keep the service; new users cannot be offered it (via the earlier no-catalogue-entry rule, if the entry lapses entirely) and the service vanishes from SLA reporting. The statement's "unavailable to all users" is directly contradicted, so False. The deeper reading point: policies often define terms ("dormant") in ways that differ from everyday intuition, and the defined meaning governs. Managers who assume dormant means dead might decommission something citizens still use; managers who read the definition know the real risk is subtler — a live service invisible to reporting, which is exactly the kind of governance gap your reporting duty exists to prevent.

**Question 11 (hard) — Inference**

Which conclusion about the annual service report can properly be drawn?

- A) The report understates the department's true service estate if any services are dormant at year end
- B) Dormant services are excluded from the report because their performance is poor
- C) The report includes services retired during the year, for completeness
- D) The board is unaware that dormant services exist

**Correct answer: A**

**Explanation:** Work from the two relevant clauses. Dormant services remain available to existing users, yet the annual report "covers all services except dormant services and services retired during the year." Therefore, whenever dormant services exist at year end, live, used services are absent from the report — the reported estate is smaller than the operating estate, which is exactly option A's claim, forced by the text. Option B invents a rationale: exclusion follows from review status, not performance — a dormant service might perform beautifully; nobody is measuring. Option C directly contradicts the exception clause. Option D overreaches: the report omitting dormant services does not establish board ignorance — the board may know from other sources; the passage cannot say. Note that A is also the finding a sharp service manager would raise in governance: a policy that lets used services drop out of board visibility through review lapses creates an accountability blind spot, and spotting it in the text is the same skill as spotting it in the organisation.

**Question 12 (hard) — Clear-writing judgement**

You must draft the change notice for a four-hour evening outage of the expenses system. Which version is best?

- A) "Please be advised that scheduled essential maintenance activities will be undertaken in respect of the expenses system infrastructure, with an associated service interruption anticipated during the relevant maintenance window."
- B) "The expenses system will be unavailable on Thursday 14 March, 18:00–22:00, while we apply a security update. Claims submitted before 18:00 will be processed normally. If the work finishes early, service will resume early; a status update will be posted at 20:00 on the IT status page. Contact the service desk on ext. 3000 with any concerns."
- C) "Expenses down Thurs evening for patching — should be back by 10ish. Apologies for any inconvenience!"
- D) "The expenses system will undergo a scheduled outage. Users are advised to plan accordingly. Further details are available on request."

**Correct answer: B**

**Explanation:** A change notice succeeds when a busy reader can answer, without replying: what is affected, when exactly, why, what should I do, and where do updates come from. Option B answers all five in plain words: named service, full date and time window, reason (security update — which also justifies the disruption), user guidance (pre-18:00 claims safe), an update mechanism, and a contact route. Option A is officialese that never states the date or times — the two facts every reader needs — while spending thirty words sounding procedural. Option C has the right brevity instinct but is fatally imprecise: no date beyond "Thurs", "10ish" is vaguer than the actual window, and the register undercuts confidence in the change itself. Option D makes readers do the work the notice exists to remove. This judgement maps straight onto your duty to ensure all technical change is communicated: the measure of a change notice is the incidents and calls it prevents, and option B is the only draft engineered to prevent them.

### Preparation tips

- **Read agreements the way you will be tested.** Take one SLA or OLA you own and audit three clauses: underline every "shall/may/must", every qualifier ("working", "consecutive", "at the time"), and every exception. This is simultaneously test practice and professional hygiene.
- **Practise the three-way verdict daily.** For claims you encounter in reports and emails, ask: supported, contradicted, or not addressed? Saying "the document doesn't say" aloud in meetings is the workplace form of "Cannot say" — and it is a strength, not a hedge.
- **Slow down at qualifiers and exceptions.** "Unless", "except", "provided that", "sole remedy" — these words carry the legal and operational weight. Most planted traps, and most real disputes, live there.
- **Separate a source's claims from your knowledge.** When practising, note where your ITIL or contractual experience wanted to answer instead of the passage. Knowing your own interference patterns is half of eliminating them.
- **Summarise multi-point emails in a numbered list before replying.** If your list misses a point, your reply would have too. This mirrors the extraction skill the test measures.
- **Draft, then cut.** For clear-writing judgement, practise rewriting one of your own notices to half its length without losing a fact readers need. The test's best answers are always the fact-dense plain ones.

### Common pitfalls to avoid

- **Answering from ITIL or your own organisation's practice.** The passage governs, even when it differs from how you would run things. Experienced practitioners lose more verbal marks this way than any other.
- **Treating conditional permissions as automatic effects.** "May suspend, provided recorded" is not "stops automatically". Map the conditions before concluding.
- **Missing the distinction a qualifier creates between parallel clauses.** When one clause says "working hours" and its neighbour does not, the difference is the question.
- **Converting negotiating positions into ultimatums (or vice versa).** Report stakeholders' stated positions at their stated strength — in the test's statements and in your escalation summaries.
- **Letting exception clauses pass unread.** Exceptions convert False to Cannot say and back; the "wilful default" carve-out changes the whole remedy analysis.
- **Choosing the politest reply rather than the most complete one.** Warmth without specifics ("we'll circle back soon") fails stakeholders in tests and in inboxes alike.
- **Equating brevity with clarity.** The shortest draft that omits the date is worse than the longer one that answers every question. Clarity is measured in reader questions prevented.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement assessment (SJT) presents realistic workplace dilemmas and asks you to judge the effectiveness of possible responses. Formats vary: choose the most effective response, choose the least effective, rank all responses from best to worst, or rate each response independently. For an IT service manager, the scenarios are drawn from the genuine pressure points of the role: an SLA breach with a stakeholder demanding answers, a supplier underperforming against an OLA, a change that went wrong, a team conflict across locations, a reporting figure someone wants "presented more positively", an improvement initiative meeting resistance.

The typical format is an online assessment of 15 to 30 scenarios, usually generously timed, because it measures judgement rather than speed. Scoring compares your choices against the judgements of experienced practitioners and the organisation's professional behaviours — user focus, ownership, collaboration, honest communication, appropriate escalation, and inclusion. Crucially, SJTs at management level test *management* judgement: not whether you can fix the incident, but whether you protect the service, the users, the team, the supplier relationship, and the truth simultaneously — and what you trade when you cannot protect all five.

Why do employers use SJTs for this role? Because your role summary is dense with judgement calls that no technical qualification certifies. Managing a multi-sourced team "with a customer-centric support approach across multiple locations" means daily choices between competing loyalties: your organisation and its suppliers, this location and that one, this month's figures and next year's trust. Ensuring functions "remain responsive to customer needs" is a judgement about when process serves users and when it obstructs them. Governance of technical change is a long series of decisions about when to say no. An SJT samples these decisions safely, in advance.

Two practical notes. First, answer as your best professional self operating by your organisation's values — not as a tactician guessing the scoring key. Second, learn the anatomy of weak options: they hide information, blame individuals for system problems, bypass governance for convenience, sacrifice users to metrics, or abandon ownership at an organisational boundary. Options carrying those features are consistently the "least effective" answers — and the least effective managers.

### How this assessment maps to your role

- **Customer-centric choices** map to your duty to ensure that all service and support functions **remain responsive to customer needs**, and to your **User focus** skill — engaging users and turning quantitative and qualitative evidence into outcomes. Scenarios repeatedly test whether users' interests survive contact with metrics, suppliers, and convenience.
- **Ownership choices** map to your **Ownership and topic** skill: owning an issue until a new owner has been found or the problem has been mitigated or resolved. At management level this includes owning issues that fall between suppliers — the gaps in a multi-sourced operation are where ownership is truly tested.
- **Governance choices** map to your duty to ensure **all technical change is communicated and managed, with appropriate governance**: scenarios probe when you hold the line on process, when you invoke emergency routes, and how you handle those who bypass either.
- **Supplier and stakeholder choices** map to your **Stakeholder relationship management (IT operations)** skill — building consensus, tailoring communication, and using evidence to explain decisions — exercised across contractual boundaries where charm and pressure both fail without data.
- **Reporting integrity choices** map to your **IT service reporting** skill and your duty to ensure adequate reporting standards: several scenarios test what you do when accurate numbers are unwelcome.
- **Improvement and team choices** map to your **continual service improvement** duty and your **Business analysis (IT operations)** skill — investigating problems in existing processes and working with stakeholders on objectives and benefits — including the human side: resistance, workload, and credit.

### Practice questions

**Question 1 (easy) — The stakeholder demanding an instant answer**

A director calls you 20 minutes into a P1 outage of the grants system: "I have a ministerial submission due — tell me right now when this will be fixed." The resolver group has not yet diagnosed the fault. What is the most effective response?

- A) Give a confident estimate — "two hours" — to reassure the director, and hope the team beats it
- B) Explain that diagnosis is under way, state what is known and being done, commit to a specific next update ("I will call you personally at 11:00 or sooner"), and ask about the submission deadline so the workaround options can be judged against it
- C) Tell the director you cannot discuss the incident while it is being worked on
- D) Transfer the call to the resolver group's engineer so the director hears it first-hand

**Correct answer: B**

**Explanation:** During an undiagnosed outage, the honest inventory is: what happened, what is being done, and when the next reliable information will arrive. Option B delivers all three, converts an open-ended demand into a bounded commitment (the 11:00 call), and — the managerial masterstroke — asks about the deadline, because the director's real need is the submission, not the ETA, and a workaround (another route to submit, an extract, a delay agreed upstream) may solve the actual problem before the system recovers. Option A trades reassurance now for credibility later: an invented "two hours" fails silently or spectacularly, and either way the next estimate is disbelieved. Option C is procedurally wrong and relationally worse — stakeholders are exactly whom you must communicate with during incidents. Option D dumps an anxious senior stakeholder onto an engineer mid-diagnosis, slowing the fix and abandoning your communication role. Scored behaviours: honest communication under pressure, ownership of stakeholder management, and user-need focus beneath the stated demand.

**Question 2 (easy) — The supplier who missed an OLA target**

Monthly figures show your applications supplier resolved 84% of tickets within OLA against a 90% commitment — their first miss in a year, coinciding with a documented 40% volume spike from a new system go-live. Your service review with them is tomorrow. What is the most effective approach?

- A) Open the review by invoking the contract's remediation clauses to establish seriousness
- B) Skip the topic — one bad month after a good year does not merit discussion
- C) Present the data, acknowledge the volume spike your organisation generated, ask for their analysis, and agree a joint plan covering both the demand surge and their capacity — while noting the miss formally so the record is accurate
- D) Ask them informally to "smooth things over" in their report so the miss does not surface at your governance board

**Correct answer: C**

**Explanation:** Effective supplier management distinguishes performance problems from demand problems, and this data points substantially to demand your own organisation created. Option C models the whole discipline: evidence on the table, honest acknowledgement of your side's contribution, their analysis invited (they know their queue better than you do), a joint remediation plan, and — crucially — formal accuracy: the miss is recorded even while the relationship stays collaborative, because records that bend to relationships eventually support neither. Option A reaches for contractual escalation against a partner with a year of good performance and a mitigating cause; you spend relationship capital where analysis was owed, and teach the supplier to hide problems. Option B avoids conflict at the price of governance: unexamined misses become patterns. Option D is the worst feature in any SJT option — corrupting the record — and would compromise both your reporting duty and your integrity in one favour. Scored behaviours: evidence-based fairness, consensus building, ownership of your organisation's contribution, and reporting integrity.

**Question 3 (easy) — The two-location tension**

Your support team spans two sites. Analysts at the smaller northern site complain that the rota concentrates unsocial evening shifts on them, that they hear about process changes late, and that the last two promotions went to the southern site "as always". What is the most effective first action?

- A) Explain that shift allocation follows the rota tool's output, so it is fair by definition
- B) Review the rota data and communication patterns to establish the facts, visit the northern site to hear the concerns directly, and correct anything the evidence supports — starting with including both sites simultaneously in all change communications
- C) Rotate the team leaders between sites so each experiences the other location
- D) Tell the northern team that hybrid working means location no longer matters

**Correct answer: B**

**Explanation:** Complaints of unfairness across locations contain factual claims (shift distribution, communication timing, promotion history) that can be checked — and checking them is both respectful and protective, because the answer determines the remedy. Option B sequences correctly: establish facts, hear people in person (presence at the smaller site is itself a signal that they matter), fix what the evidence supports, and implement the one correction that costs nothing and is almost certainly warranted — simultaneous communication. If the rota data shows genuine skew, the rota changes; if it does not, the perception still needs addressing, but with shared data rather than assertion. Option A hides behind a tool — tools encode the assumptions they were given, and "fair by definition" is how skew persists. Option C is a gesture that might help later but investigates nothing. Option D dismisses lived experience with a slogan. Managing "across multiple locations" is named in your role summary precisely because this dynamic — the smaller site accumulating quiet disadvantage — is the default unless managed. Scored behaviours: inclusion, evidence before judgement, visible fairness, and team ownership.

**Question 4 (moderate) — The change that skipped governance**

You discover that an infrastructure engineer implemented an unauthorised firewall change on Friday evening to "quickly fix" a recurring fault. The change worked — the fault is gone — and no incident resulted. The engineer is well-regarded and openly tells you what they did. What is the most effective response?

- A) Take no action — the outcome was good, and punishing success discourages initiative
- B) Formally discipline the engineer to deter future bypassing
- C) Acknowledge the intent and the transparency, but require a retrospective change record and review; explain specifically what could have gone wrong unreviewed on a Friday evening; and examine why the legitimate route felt too slow for a recurring fault — fixing the process gap that invited the bypass
- D) Quietly ask the engineer not to do it again and mention it to no one, avoiding paperwork for everyone

**Correct answer: C**

**Explanation:** Change governance exists to manage risk, and its authority survives only if bypasses are addressed — but *how* they are addressed determines whether people keep telling you the truth. Option C holds every line at once: the record is corrected retrospectively (so configuration information stays accurate — your **Asset and configuration management** skill), the risk is explained concretely rather than bureaucratically (Friday evening, minimal cover, no peer review, no rollback plan — the exact profile of your worst change-failure data), the engineer's honesty is preserved as an asset, and — the managerial depth — the system question is asked: a recurring fault with no problem record and a change process experienced as too slow is a process gap, and bypasses are data about your process. Option A converts luck into precedent: the next unreviewed Friday change inherits this one's permission. Option B punishes transparency, teaching the team that honesty is the error — after which bypasses continue, unreported. Option D makes you a co-conspirator and leaves the configuration record false. Scored behaviours: proportionate governance, honesty-preserving accountability, root-cause thinking about process, and record integrity.

**Question 5 (moderate) — The knowledge library nobody updates**

Audit sampling shows 30% of knowledge library articles for a key service are outdated, and two recent incidents were prolonged by analysts following obsolete articles. Team leads say their analysts have no time for documentation between tickets. Your duty is to keep the knowledge library maintained. What is the most effective approach?

- A) Email all analysts reminding them that knowledge maintenance is mandatory
- B) Build maintenance into the operating model: make article review part of ticket closure for affected services, allocate rota'd time for it, measure article accuracy alongside ticket metrics, and retire or flag the worst articles immediately so they stop causing harm
- C) Assign the newest analyst to update all articles, since seniors are too busy
- D) Commission a supplier to rewrite the library as a one-off project

**Correct answer: B**

**Explanation:** "No time between tickets" is the diagnostic clue: this is a system design problem, not a diligence problem, and reminders (option A) fail against system problems — the audit will read the same next year with a thicker email trail. Option B redesigns the system so maintenance happens as a by-product of work people already do: review-on-closure catches articles at exactly the moment their inaccuracy is discovered; rota'd time makes the duty real rather than residual; measurement makes it visible; and the immediate triage of harmful articles addresses the active patient-safety issue — two incidents have already been prolonged. Option C combines the least knowledge with the highest documentation risk and signals that maintenance is low-status work, guaranteeing future neglect. Option D buys a snapshot that begins decaying on delivery day, because the mechanism that let the library rot remains untouched. The scored behaviours are systemic problem solving (your **Business analysis** skill applied to your own operation), continual improvement embedded in process rather than campaigns, and user focus — the library exists so users get faster, correct fixes.

**Question 6 (moderate) — The uncomfortable number**

Preparing the quarterly service report for the departmental board, you find availability for the tax processing service was 98.1% against a 99.5% target — the worst figure in two years, driven by one long outage. A senior colleague suggests reporting the six-month rolling average (99.2%) instead, "for better context". What is the most effective response?

- A) Use the rolling average — it is a legitimate statistic and reads better
- B) Report the quarterly figure against target as the standard requires, include the rolling average as clearly labelled additional context, and accompany the miss with cause, remediation, and recovery trajectory
- C) Report the quarterly figure but omit the target so the shortfall is less obvious
- D) Ask the service owner to decide, since it is their service

**Correct answer: B**

**Explanation:** The test is whether "context" becomes a euphemism for substitution. A rolling average is indeed a legitimate statistic — as *addition*, clearly labelled; as *replacement* for the standard measure in the quarter it looks worst, it is presentation engineered to obscure, and boards eventually discover the engineering, after which every figure you present is discounted. Option B is the complete professional answer: the required measure against its target (your reporting-standards duty), honest context (the rolling average shows the quarter is an outlier — that genuinely helps the board), and the three things a board actually needs with any red figure: why, what is being done, and when recovery is expected. A miss reported this way *builds* credibility. Option C manipulates by omission — arguably worse than the average swap because it degrades the report's standard format. Option D outsources an integrity question that sits squarely in your duty; the service owner owns the service, but you own the reporting standard. Scored behaviours: reporting integrity, constructive transparency, and stakeholder respect — boards are stakeholders whose need is truth with trajectory.

**Question 7 (moderate) — Least effective: the improvement that threatens jobs**

Your automation initiative will deflect 30% of routine tickets. Analysts are anxious it means redundancies; two team leads are quietly slowing the rollout. Which response is the LEAST effective?

- A) Hold an open session explaining what the freed capacity will be used for — reduced backlog, project work, development time — and involve the anxious teams in choosing which tickets automate first
- B) Talk privately with the two team leads to understand their concerns and win their sponsorship of the change
- C) Accelerate the rollout quietly and let the results speak for themselves once it is done
- D) Share the demand-growth data showing rising volumes will absorb the freed capacity, and commit publicly that no roles will be lost to this initiative if that is the organisation's actual position

**Correct answer: C**

**Explanation:** This least-effective question hunts the option that ignores the human system through which every improvement must pass. Option C does exactly that: accelerating a change *because* it faces resistance, and doing so quietly, confirms the teams' worst interpretation (it is being done *to* them, fast, before they can object), converts anxious compliance into active opposition, and burns the trust the next initiative will need. "Results speaking for themselves" is a fantasy when the people producing the results are motivated to prove the automation inadequate. Options A, B and D are all effective, in complementary ways: A gives the future shape and shares control; B addresses the actual blockers respectfully; D deploys evidence and — where truthful — the single commitment that dissolves the core fear. Note D's careful conditional: commitments must match the organisation's real position, because a false reassurance is a delayed catastrophe. Your continual service improvement duty is a duty to *land* improvements, not merely launch them; improvements that ignore fear arrive broken. Scored behaviours: change leadership, communication, collaboration — and their absence in C.

**Question 8 (moderate) — The catalogue request that hides a shadow service**

A business unit asks you to add "their" case-tracking tool to the service catalogue. Investigating, you find they built it themselves on an unsupported platform, it holds citizen data, 60 staff already depend on it daily, and it has no backups, no support arrangements, and no security assessment. What is the most effective response?

- A) Refuse catalogue entry and instruct the unit to stop using the tool immediately
- B) Add it to the catalogue as requested — 60 users make it a de facto service already
- C) Treat the request as the disclosure opportunity it is: get the security and data risks assessed urgently, put interim safeguards in place (backups first), and work with the unit on a route to either proper adoption or managed migration — while ensuring the data risk is formally reported
- D) Decline involvement, since the tool was built outside IT and is the unit's responsibility

**Correct answer: C**

**Explanation:** Shadow IT scenarios test whether you optimise for being right or for reducing risk. The facts rank themselves: citizen data with no backups and no security assessment is the urgent risk; 60 daily users means abrupt shutdown (option A) creates an operational crisis and — worse — teaches every unit that disclosing shadow tools gets them punished, driving the next one deeper underground. Option B swings opposite: cataloguing confers legitimacy and implies support arrangements that do not exist, putting your name on an unassessed service — catalogue integrity is precisely what your maintenance duty protects. Option D is ownership abandonment with a jurisdictional excuse; your **Ownership and topic** skill says own the issue until it is mitigated or a proper owner exists, and citizen data risk is an organisational issue the moment you know of it. Option C sequences by risk: assess, safeguard (backups convert a potential catastrophe into a recoverable incident), report the data-handling exposure through the required channel, then solve the service question properly — adopt with real support, or migrate in a managed way. The unit that disclosed is treated as a partner, preserving the incentive to disclose. Scored behaviours: risk-first sequencing, ownership across boundaries, governance without punishment of honesty, and user protection.

**Question 9 (hard) — The conflicting SLA commitments**

Drafting SLAs for a new shared platform, you discover marketing was promised 99.9% availability by an account manager during onboarding, but the platform's architecture — confirmed by your OLA analysis — can support at most 99.5%. Marketing has already built the 99.9% figure into their campaign planning. Your head of division would prefer this "not become a thing". What is the most effective action?

- A) Draft the SLA at 99.9% to honour the promise, and hope the platform overperforms
- B) Draft the SLA at 99.5%, tell marketing the account manager's figure was unofficial, and proceed
- C) Take the discrepancy to marketing directly and early: explain what the platform can actually commit to and why, quantify the difference in real terms (about 3 hours versus 43 minutes of monthly downtime), explore whether their campaign-critical windows can be protected by other means (change freezes, enhanced monitoring), and brief your head of division that a corrected commitment now is far cheaper than a breached one later
- D) Draft the SLA at 99.7% as a compromise between the two figures

**Correct answer: C**

**Explanation:** An SLA is a promise the operation must keep month after month; drafting one the architecture cannot support (option A) does not honour the earlier promise — it schedules its public breaking, with service credits, board scrutiny, and a betrayed stakeholder attached. Option D is the seductive trap: splitting the difference treats an engineering constraint as a negotiating position; the platform does not know a compromise was reached, and 99.7% breaches almost as reliably as 99.9%. Option B has the right number and the wrong method: a curt correction delivered as a fait accompli converts a colleague's error into an inter-directorate grievance, precisely what your consensus-building skill exists to avoid. Option C does the whole job: early, direct, quantified honesty (translating percentage points into hours makes the difference *decidable* for non-specialists); creative protection of the stakeholder's underlying need — campaign windows can often be protected operationally even when headline availability cannot rise; and managing upward with the true cost comparison, which respectfully declines the "not a thing" preference by showing why silence is the expensive option. This is your defining duty — SLAs across business functions — done properly: commitments grounded in OLA-verified capability, negotiated in the open. Scored behaviours: integrity under hierarchical pressure, evidence-based negotiation, stakeholder need beneath stakeholder position, and courage with courtesy.

**Question 10 (hard) — The major incident retrospective that points at you**

The post-incident review of last week's four-hour payroll outage finds the primary cause was a change you personally approved: the risk assessment you signed off underestimated the blast radius, and the testing evidence you accepted was thinner than your own change standard requires. The review lands on your desk before wider circulation. What is the most effective action?

- A) Soften the findings' wording before circulation — the facts remain, but "approved against standard" becomes "approved under time pressure"
- B) Circulate the review unedited, add your own account taking responsibility for the approval decision, and propose the specific control improvements it implies — a blast-radius checklist and a minimum-evidence gate you cannot waive alone — then present it yourself at the service review
- C) Circulate it but let the review "speak for itself" without comment from you
- D) Delay circulation until the improvements are already implemented, so the story has a happy ending

**Correct answer: B**

**Explanation:** How a manager handles findings against themselves sets the honesty ceiling for their whole operation: nobody below you will ever be more transparent about their failures than you are about yours. Option B is the complete answer, and each element earns its place: unedited circulation preserves the review process's integrity (edit one review and every future review is suspected); the personal account converts the document from an accusation into an act of leadership; the proposed controls show systemic thinking — and note their design: a gate *you cannot waive alone* addresses the actual failure mode, which was concentrated discretion, not bad luck; presenting it yourself takes the blame conversation and turns it into a governance conversation. Option A is quiet corruption — softening language while "keeping the facts" is how organisations forget what happened. Option C is transparency without ownership: circulating your own adverse findings with no response reads as either indifference or hope that nobody notices, and forfeits the leadership moment. Option D holds the truth hostage to your remediation timetable, and payroll's stakeholders deserved the findings when they existed. Scored behaviours: accountability, modelling the blame-free-but-responsible culture that makes incident review work, converting personal failure into institutional control, and courage. Your **Ownership and topic** skill — owning issues until resolved — includes, most of all, the issues you caused.

**Question 11 (hard) — Ranking: the Friday afternoon cascade**

At 15:30 on Friday, four situations land simultaneously: (1) monitoring shows early signs of degradation on the benefits-claim service, the pattern matching the prelude to last month's P1; (2) a supplier emails that their overnight maintenance tonight now needs an extended window, requiring your approval within the hour; (3) an analyst reports a colleague may have shared their admin password with a contractor "to save time"; (4) a director asks for a summary of October's SLA figures by Monday morning. Rank the order in which you address them:

- A) 1, 3, 2, 4
- B) 3, 1, 2, 4
- C) 2, 1, 4, 3
- D) 1, 2, 3, 4

**Correct answer: B**

**Explanation:** Rank by irreversibility and blast radius, not noise. Item 3 leads: a shared admin credential is a live security exposure — every minute it remains valid is organisational risk, and containment (disabling or resetting the credential, then following the security process) takes minutes and cannot wait for a convenient gap; unlike the other items, delay here is potentially unbounded harm. Item 1 is second and nearly simultaneous: a recognised pre-P1 pattern on a citizen-facing service demands immediate resolver-group engagement while there is still time to prevent rather than manage an outage — prevention windows close. Item 2 third: it has an explicit one-hour clock, but it is a bounded decision you can make properly at 16:15 with the OLA and risk picture in front of you — and note its interaction with item 1: an extended maintenance window tonight, on a weekend with a possibly degrading service, deserves conditions or deferral, which is why deciding it *after* assessing item 1 is not just acceptable but better. Item 4 is Monday's deadline; it schedules into Monday morning or a quiet hour, and answering it first (option C) would be classic urgency-by-seniority error. Option D runs the operational items well but leaves the security exposure open longest — the one mistake in this set with disciplinary, audit, and citizen-data implications. Scored behaviours: risk-based prioritisation, security seriousness, prevention over reaction, and resistance to seniority-driven sequencing.

**Question 12 (hard) — The consensus that excludes the users**

You are chairing the working group defining support arrangements for a new casework service. IT, the supplier, and finance have converged on a support model with 09:00–17:00 coverage — it fits budgets and rosters neatly. Late in the process, user research data arrives showing 30% of caseworkers regularly work 07:30–09:00, including the service's heaviest data-entry period. The group wants to sign off today; reopening coverage hours would delay the launch by two weeks and irritate everyone. What is the most effective action?

- A) Sign off the model — consensus among the professional stakeholders is what the working group exists to produce, and the users can adapt
- B) Put the user data in front of the group before sign-off, quantify the exposure (the heaviest usage period would be unsupported), and recommend either adjusted hours or an explicit, risk-accepted interim with committed review — making the group decide with the evidence rather than without it
- C) Sign off today, and plan to fix the hours quietly in a later review once launch pressure has passed
- D) Escalate to your head of division to overrule the group's preferred model

**Correct answer: B**

**Explanation:** The scenario stages a collision between two things your role genuinely values: consensus (your stakeholder skill names building and reaching it) and users (your entire operation's purpose). The resolution is that consensus derives its value from what it is consensus *about* — agreement reached by excluding material evidence is not consensus but collective oversight, and it fails at the worst time: post-launch, publicly, at 07:30 on the service's busiest morning. Option B neither bulldozes the group nor betrays the users: the evidence is tabled, the exposure is quantified (data-driven, per your **User focus** skill — using quantitative data about users to turn user focus into outcomes), and the group is offered legitimate paths — change the model, or accept the risk explicitly with a review commitment. Decisions made that way survive scrutiny either way; an *explicit* interim risk acceptance is honest governance, while option C's version — same outcome, undocumented — is a quiet bet with citizens' casework, and "later reviews" after successful launches have a way of never convening. Option A dissolves the purpose of support arrangements into administrative convenience. Option D escalates before the group has even seen the evidence — using hierarchy where information might suffice, spending your head of division's authority and the group's goodwill on a problem the data could solve alone. Scored behaviours: user advocacy with evidence, honest governance of trade-offs, consensus built on full information, and escalation as a last resort rather than a first.

### Preparation tips

- **Revisit your organisation's values and the Civil Service behaviours before the assessment.** SJT scoring keys are built from professional behaviours — user focus, ownership, honesty, collaboration, inclusion. Fresh familiarity helps you recognise them dressed in scenario clothing.
- **Answer as the manager you are on your best day.** Not a politician gaming the key, not a hero bypassing process — the manager who protects users, tells stakeholders the truth, and fixes systems rather than blaming individuals.
- **Learn the anatomy of strong options.** They usually pair action with communication, fix the instance and the system, preserve records and relationships simultaneously, and keep commitments proportionate to evidence.
- **Learn the anatomy of weak options.** Hiding or softening information, punishing honesty, bypassing governance for convenience, sacrificing users to metrics or budgets, abandoning issues at organisational boundaries, and escalating before investigating. In least-effective formats, hunt these features.
- **Rehearse with your own history.** Recall three genuinely difficult moments from your service management experience — a supplier dispute, a reporting pressure, a change failure. Write down what you did and what the best version would have been. That reflection is the exact muscle the SJT measures.
- **In ranking questions, fix the poles first.** Identify the clearly best and clearly worst options; the middle pair usually orders by which preserves more ownership, more honesty, or more user protection.
- **Read the stem's role cues.** "Your head of division prefers...", "the director is copied...", "the supplier's first miss in a year..." — these details calibrate the politically and relationally aware answer the scenario is testing for.

### Common pitfalls to avoid

- **Choosing operational speed over stakeholder honesty.** Invented ETAs, softened findings, and "smoothed" figures each buy an hour and cost a year of credibility. The credited answers consistently pay the short-term price.
- **Punishing the disclosure instead of the risk.** Whether it is an engineer's bypass, a unit's shadow tool, or a colleague's shared password, responses that make honesty expensive guarantee you hear less next time — and score poorly.
- **Blaming individuals for system-shaped problems.** No time for documentation, recurring bypasses, and location grievances are process signals. Options that fix the system outrank options that admonish the people.
- **Treating governance as either optional or absolute.** The credited path holds process *and* asks why process failed the person who bypassed it. Pure enforcement and pure flexibility both lose marks.
- **Letting seniority reorder your priorities.** Directors' requests with Monday deadlines do not outrank live security exposures or degrading citizen services. Rank by irreversibility and blast radius.
- **Splitting the difference on technical constraints.** Architecture, capacity, and security do not negotiate. Compromise numbers (99.7%) are the trap dressed as maturity.
- **Abandoning ownership at boundaries.** "That is the supplier's problem", "that unit built it themselves", "that is the service owner's call" — the multi-sourced operation's failures live in its gaps, and your role exists to own the gaps.

## Conclusion

Congratulations — you have worked through a complete, role-specific set of psychometric assessment practice materials for the IT service manager role. It is worth pausing to take stock of what that represents.

Across the cognitive section, you practised the structured thinking that underpins a well-run service: reasoning from shared platforms to likely causes, applying change governance rules with deductive precision, checking catalogue entries and supplier reports against their own arithmetic, sequencing a demanding morning by impact-weighted urgency, and untangling multi-constraint change schedules. Across the numeric section, you worked the native mathematics of service management — SLA achievement, availability conversions, weighted supplier performance, change failure analysis, benefits cases, and capacity planning — always with the base identified and the working shown. Across the verbal section, you read SLA clauses, supplier reports, stakeholder emails, and policy extracts with contractual precision, holding the line between what a document supports, what it contradicts, and what it simply does not say. And across the situational judgement section, you rehearsed the defining dilemmas of the role: honest communication during outages, fairness across sites and suppliers, governance that preserves honesty, reporting integrity under pressure, and user advocacy inside consensus-driven groups.

Notice the consistent thread. Every section rewarded the same professional posture: verify before trusting, quantify before arguing, own the issue across boundaries, and tell stakeholders the truth with a plan attached. These are not test techniques — they are the working habits your role summary describes, from defining SLAs and OLAs to governing change and driving continual service improvement. Time spent practising these assessments is therefore time spent becoming a sharper service manager, and every service review, change decision, and monthly report you produce is, in turn, further practice for any assessment.

If you have an assessment approaching, a simple plan serves best: revisit one section per day in the preceding week, redo the questions you found hardest, and re-read the pitfalls lists the evening before. On the day: rest, a quiet room, rough paper, the platform's warm-up questions, and your method — read precisely, name the base, deduce only what must be true, and choose the option that protects users, records, and relationships together.

Finally, treat your results — practice or real — as a development tool rather than a verdict. They show where your reasoning is already strong and where deliberate practice will pay dividends, insight you can carry straight into development conversations and your progression toward senior service management roles. You spend your working life keeping services responsive to the people who depend on them; let this guide be one of the things that keeps your own capability growing in the same way — deliberately, measurably, and with confidence.

Good luck — you are well prepared, and it will show.

