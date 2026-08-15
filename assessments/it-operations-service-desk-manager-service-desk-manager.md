# Service Desk Manager - Psychometric Assessment Resources

## Introduction

Welcome. This guide has been prepared for you as a service desk manager working within the UK Government Digital and Data profession. You may be preparing for an internal assessment or promotion board, benchmarking yourself against your role profile, or simply interested in how psychometric assessment connects to the leadership work you do. Whatever the motivation, this document offers structured, role-specific practice with full worked reasoning.

Psychometric assessments are standardised exercises measuring the cognitive capabilities and professional judgement that predict success in a role. At your level, well-designed assessments move beyond generic aptitude testing: they draw on the materials a service desk manager genuinely commands — service performance dashboards, transition plans, problem trend analyses, customer satisfaction data, automation business cases, resourcing models — and the decisions you genuinely make: identifying emerging issues before they mature into outages, allocating scarce analyst capacity, deciding which processes to automate, coordinating service transition, and converting lessons learnt into continual service improvement.

Your role occupies a distinctive position. You are the desk's knowledge expert and its accountable owner: responsible for resourcing and developing the team, for preparing and coordinating service transition activities, and for the quality of outcomes users actually experience. The four assessments in this guide map onto that territory directly. Cognitive questions test the pattern detection and structured reasoning behind "identifies emerging issues" — reading weak signals in ticket data, checking transition plans for logical gaps, prioritising across competing operational and developmental demands. Numeric questions use the data your decisions rest on: satisfaction scores, cost-per-contact, SLA aggregates across sites, automation benefit projections, and capacity models. Verbal questions use the documents you write and approve — transition readiness criteria, improvement proposals, satisfaction survey reports, ITIL-aligned process definitions — where a misread clause becomes a mismanaged service. Situational judgement questions probe the manager's characteristic dilemmas: accountability without blame, automation against jobs anxiety, championing user research when operational pressure argues otherwise, and escalating honestly when the numbers disappoint.

The document is organised into four main assessment sections, each following the same pattern: an overview of what the assessment measures and how it is typically administered; a mapping of its dimensions to the named skills in your role summary — customer service management, IT service reporting, problem management, ownership, service focus, user focus, asset and configuration management, and service management framework knowledge; a substantial set of practice questions progressing from easy to challenging, each with a complete worked explanation; practical preparation tips; and common pitfalls.

To extract full value: commit to an answer before reading any explanation, and treat each explanation as a technique note rather than a verdict — most encode a habit (decompose the aggregate, test the mechanism, read the exception clause) that transfers directly to your management practice. Many questions also make useful development material for your senior analysts, which turns your preparation into theirs.

A final framing point. Assessment performance is a snapshot under particular conditions, not a measure of your worth or a ceiling on your trajectory. What practice reliably changes is familiarity: formats stop being novel, traps become visible, and your genuine capability — the capability your team already relies on — shows through cleanly. Take your time, and let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the mental processes your role demands, using realistic managerial material rather than abstract puzzles. For a service desk manager, that means questions built from performance dashboards, transition checklists, problem records, escalation frameworks, and resourcing constraints — reasoning tasks with the same structure as your working decisions, compressed into minutes.

The typical format is an online, timed test of 15 to 30 minutes with 15 to 30 questions spanning pattern recognition, logical deduction, error checking, prioritisation, and applied problem solving. Scoring is objective against a norm group, frequently adaptive (difficulty rises as you succeed — experienced candidates should read late-test difficulty as a good sign, not a warning), and usually reported to employers as a speed-accuracy profile rather than a single figure. Ungraded practice items normally precede scoring.

Cognitive assessment carries particular weight at your level for two reasons. First, your defining duty — identifying emerging issues — is applied pattern recognition under noise: distinguishing a developing problem from ordinary variation in ticket flows, satisfaction scores, and analyst performance, early enough for intervention to be cheap. Second, you are the desk's knowledge expert and final checker: transition plans, automation proposals, and process changes cross your desk for approval, and the logical gap you miss becomes the incident your team handles at 3am. A well-designed cognitive test rehearses both capabilities in miniature: signal detection and structural verification, at pace, with consequences attached to precision.

### How this assessment maps to your role

- **Pattern recognition** maps to your defining duty to **identify emerging issues** and to your **Problem management** skill: "initiate and monitor actions to investigate patterns and trends" presumes you can see the pattern before anyone else does.
- **Logical deduction** maps to your **Service management framework knowledge**: ITIL lifecycle and capability elements are systems of conditional rules, and applying them to real transitions and incidents is deduction with operational stakes.
- **Error checking** maps to your **Asset and configuration management** skill and your role in **service transition**: reviewing readiness checklists, configuration records, and cutover plans for internal contradictions is the manager's quality gate.
- **Prioritisation** maps to your responsibility for **resourcing and development**: allocating analysts, budget, and your own attention across operational demand, improvement work, and people development is the job's central recurring decision.
- **Applied problem solving** maps to your **Ownership** skill — "take accountability for issues that occur and be proactive in searching for potential problems" — and to your **Customer service management** duty to investigate which processes can be automated: both require decomposing messy situations into mechanisms you can act on.

### Practice questions

**Question 1 (easy) — Pattern recognition in a service dashboard**

Your morning dashboard shows four metrics against their normal ranges: call volume 460 (normal 420-480); average wait 3.1 minutes (normal 2.5-3.5); FCR 61% (normal 66-72%); priority 1 incidents 0 (normal 0-1). Which metric most warrants investigation?

- A) Call volume
- B) Average wait
- C) First-contact resolution
- D) Priority 1 incidents

**Correct answer: C**

**Explanation:** Test each value against its own range. Call volume (460) sits inside 420-480; average wait (3.1) sits inside 2.5-3.5; priority 1 count (0) sits inside 0-1. FCR at 61% falls below its normal floor of 66% — the only out-of-range value, and a five-point breach is substantial for a rate metric. The subtlety worth noticing: the dashboard looks calm — no queue, no majors — which is precisely when an FCR drift is easiest to miss and most informative, since it is not explained by pressure. Plausible mechanisms (a new fault type analysts cannot resolve first time, a knowledge gap after a change, new starters) all reward early investigation. This is "identify emerging issues" in its simplest testable form: anomaly detection is always relative to each metric's own baseline, not to the general mood of the morning.

**Question 2 (easy) — Deduction from transition criteria**

Your service transition checklist states: "A new service may enter pilot support only if (i) the knowledge articles are published, and (ii) at least four analysts have completed training. It may enter full support only after a pilot of at least two weeks with FCR above 60%." The HR-system replacement has published articles, six trained analysts, and completed a one-week pilot with 71% FCR. What is its correct status?

- A) Eligible for full support — FCR exceeds the threshold.
- B) Eligible for pilot support, but not full support — the pilot has not yet run two weeks.
- C) Not eligible for pilot support — training is insufficient.
- D) Not eligible for either — the checklist is failed.

**Correct answer: B**

**Explanation:** Apply each condition separately. Pilot entry requires published articles (yes) and four trained analysts (six — yes): pilot eligibility is satisfied, eliminating C and D. Full support requires two conditions joined by "after": a pilot of at least two weeks AND FCR above 60%. FCR (71%) passes, but the pilot has run one week of the required two — the duration condition fails, so full support is not yet permitted, eliminating A. The correct status is B. The tested habit is refusing to let one impressive number (71%) satisfy a compound requirement it only half-meets: duration thresholds exist because early pilot performance is unrepresentative — the enthusiastic-user effect and the small-sample effect both flatter week one. As the coordinator of transition activities, you are the person who holds the line on exactly this distinction when a programme manager argues that 71% "obviously" justifies early cutover.

**Question 3 (easy) — Error checking a cutover plan**

A transition plan for moving the desk's telephony to a new platform reads: "Step 1: Freeze changes to the old platform from Friday 18:00. Step 2: Migrate call-routing configuration Saturday morning. Step 3: Test inbound routing Saturday afternoon. Step 4: Update the old platform's routing tables Sunday morning to add the new bank holiday schedule. Step 5: Go live Monday 08:00." Which step contradicts the plan's own logic?

- A) Step 2
- B) Step 3
- C) Step 4
- D) Step 5

**Correct answer: C**

**Explanation:** Step 1 freezes changes to the old platform from Friday evening — yet Step 4 schedules a change to the old platform's routing tables on Sunday, inside the freeze window. The plan violates its own control. Worse, the change is also operationally doubtful: updating the old platform's schedule the day before go-live either wastes effort (if cutover succeeds) or reveals an unstated rollback assumption (if it exists to keep the old platform current as a fallback — in which case the plan should say so and exempt it from the freeze explicitly). Steps 2, 3, and 5 follow the migrate-test-live sequence correctly. Internal contradiction — a plan breaking rules the same plan established — is the most common defect in transition documents, and the manager's review is often the last chance to catch it: read every later step against every earlier control, not just against common sense.

**Question 4 (moderate) — Prioritisation across a manager's Monday**

Four items compete for your Monday morning:

1. The dashboard shows FCR five points below normal for a third consecutive day, cause unknown.
2. A director's office asks for desk performance figures for a board pack, needed Thursday.
3. Interviews for two analyst vacancies are scheduled Wednesday; your interview questions are not yet finalised.
4. A team leader reports two analysts had a heated argument in front of colleagues an hour ago; both are now working in silence.

Which order of attention is most defensible?

- A) 2, 1, 3, 4 — external stakeholders outrank internal matters
- B) 4, 1, 3, 2 — the live people issue first, then the deteriorating unexplained metric, then Wednesday's interviews, then Thursday's figures
- C) 1, 4, 2, 3 — metrics first, people second
- D) 4, 3, 2, 1 — people matters first and last

**Correct answer: B**

**Explanation:** Rank by what degrades with delay. The conflict (item 4) is an hour old and publicly witnessed: unaddressed, it hardens into faction and silence-as-normal by the afternoon, and early intervention — separate, calm conversations — is cheap now and expensive later; live people situations decay fastest. Item 1 is next: a three-day unexplained FCR decline is an emerging issue by your role's literal definition, and each further day makes both diagnosis (memories fade, data ages) and impact worse — it outranks items with fixed future deadlines because it is deteriorating now. Item 3 precedes item 2 on deadline order (Wednesday before Thursday) and because interview quality determines two hires you will live with for years, while the board figures are a known, boundable task. Option A defers a live conflict and a live decline to a Thursday deadline; option C inverts the decay rates — the metric will still be diagnosable at 11:00, but the conflict is setting now; option D clusters "people" without asking what actually degrades. The managerial principle: sequence by rate of deterioration, not by category or seniority of requester.

**Question 5 (moderate) — Pattern separation in satisfaction data**

Monthly satisfaction (CSAT) scores for the desk: Jan 4.2, Feb 4.2, Mar 4.1, Apr 4.2, May 3.6, Jun 4.1. In May, a major email outage generated 30% of that month's survey responses. Excluding outage-related responses, May's CSAT was 4.15. Which reading is most accurate?

- A) Service quality declined sharply in May and recovered in June.
- B) Underlying satisfaction was stable throughout; May's dip reflects one high-volume negative event, which merits its own review rather than a general service-quality response.
- C) The May figure should be deleted from reporting as an outlier.
- D) June's recovery proves the desk fixed its May quality problems.

**Correct answer: B**

**Explanation:** Decompose before diagnosing. The unadjusted series shows a single-month dip (3.6) between stable neighbours (4.1-4.2); the adjusted May figure (4.15, excluding outage responses) sits squarely in the normal band. Together these establish that everyday service quality never moved — the dip is composition, not deterioration: one bad event, heavily represented in the sample, dragged the average. The correct managerial response follows from the mechanism: review the outage (and the experience users had during it) specifically, rather than launching a general quality initiative aimed at a decline that did not happen. Option A misreads composition as trend. Option C confuses understanding an outlier with hiding it — the honest report shows both figures with the explanation, because outage months are part of the service users received. Option D invents a fix for the non-existent general problem. This decomposition habit — is it the service, or the mix of respondents? — is the core skill behind "reviewing customer service satisfaction" with data analytics rather than impressions.

**Question 6 (moderate) — Deduction in problem escalation**

Your problem escalation framework says: (i) problems open more than 60 days require a documented action plan; (ii) problems touching more than one department's services require a named specialist consultant; (iii) any problem meeting both conditions must be reported to the monthly service governance board. Problem PR-118 has been open 45 days and affects services in three departments. Problem PR-121 has been open 70 days and affects one department, and has no documented action plan. Which statement is correct?

- A) PR-118 must go to the governance board.
- B) PR-121 requires a specialist consultant.
- C) PR-118 requires a specialist consultant; PR-121 breaches the action-plan rule; neither currently requires board reporting.
- D) Both must go to the governance board.

**Correct answer: C**

**Explanation:** Apply each rule to each record. PR-118: 45 days (under 60 — rule (i) not triggered); three departments (rule (ii) triggered — specialist required); board reporting needs both conditions, and only one holds — not board-reportable. PR-121: 70 days (rule (i) triggered — action plan required, and none exists: a live breach); one department (rule (ii) not triggered); again only one condition — not board-reportable. So C captures the full position, and options A and D fail on the conjunction: "meeting both conditions" is an AND, not an OR. The practical layer matters as much as the logic: PR-121's breach is the actionable finding (commission the plan now), and PR-118 is one department away from board visibility if scope creeps — the kind of forward reading a manager adds to mechanical rule-checking. Framework knowledge at your level means both: precise application, plus anticipation of which records are trending toward the next threshold.

**Question 7 (moderate) — Error checking an automation proposal**

A vendor proposal for automated password reset states: "The desk receives 1,200 password tickets monthly, each costing £8 to handle, so automation saves £9,600 per month. The tool costs £4,000 monthly, yielding a net £5,600 saving. Industry experience shows 70% of password tickets are automatable." Which is the most significant flaw in the calculation?

- A) The £8 per-ticket cost is too high.
- B) The saving assumes 100% of tickets are automated, but the proposal's own figure says only 70% are automatable — the gross saving should be about £6,720, and the net about £2,720.
- C) The tool cost should be annual, not monthly.
- D) Password tickets are not really worth £8 each.

**Correct answer: B**

**Explanation:** The proposal contradicts itself. It computes savings on all 1,200 tickets (1,200 × £8 = £9,600) while simultaneously stating that only 70% are automatable. Consistent arithmetic: automatable tickets = 1,200 × 0.70 = 840; gross saving = 840 × £8 = £6,720; net = £6,720 − £4,000 = £2,720 per month — roughly half the claimed £5,600. The proposal remains positive, but the margin for error shrinks dramatically: if real automation uptake runs at 50% rather than 70% (common early in rollout), the case approaches break-even (600 × £8 = £4,800 − £4,000 = £800). Options A and D dispute an input with no evidence either way; option C invents a fact. The tested skill is your named duty — "investigate which processes can be automated and the ways to automate them" — exercised as a reviewer: check a business case's internal consistency before its assumptions, because a case that contradicts itself has not yet earned scrutiny of its inputs. Vendors' headline numbers are marketing until reconciled line by line.

**Question 8 (moderate) — Emerging issue or noise?**

In the past ten days you observe: (i) reopened-ticket rate has risen from 4% to 7%; (ii) three analysts independently mention that a recent knowledge base reorganisation makes articles harder to find; (iii) average handling time is up 40 seconds; (iv) CSAT is unchanged; (v) call volume is normal. What is the most coherent reading?

- A) Nothing is wrong — CSAT is stable, so users are unaffected.
- B) The signals cohere around one mechanism: analysts struggling to locate knowledge — producing longer calls and more incomplete first fixes (reopens) — which merits prompt investigation of the KB reorganisation before user-visible impact grows.
- C) Analysts are resisting change and complaining; performance-manage the three who raised it.
- D) The reopen rise and handling-time rise are unrelated coincidences.

**Correct answer: B**

**Explanation:** Assemble the signals into a mechanism rather than judging each alone. A knowledge base made harder to navigate would produce precisely this signature: fixes attempted without the right article are slower (fact iii) and more often incomplete, surfacing later as reopens (fact i — a 75% relative rise in a quality-critical metric); and the analysts closest to the work are saying exactly this in plain words (fact ii). CSAT stability (fact iv) does not contradict the mechanism — reopened tickets and slightly longer calls erode satisfaction with a lag, which is what makes this an emerging issue rather than a mature one: the window where investigation is cheap and users are still unharmed. Option A uses the lagging indicator to dismiss the leading ones — backwards. Option C converts frontline evidence into insubordination, which both misreads the data and teaches the team to stop reporting problems. Option D asserts coincidence against a coherent single-cause explanation, violating parsimony. This question is your role's headline duty in miniature: emerging issues announce themselves as converging weak signals plus corroborating testimony, and the manager's craft is crediting the pattern before the lagging metrics confirm it.

**Question 9 (challenging) — Multi-constraint resourcing**

You must staff a four-week service transition (the new case-management rollout) with exactly two analysts seconded half-time, while keeping the desk at its minimum of eight full-time-equivalent (FTE) analysts on phones. Your ten analysts: six are transition-trained; of those six, two are your only Welsh-language call handlers (the desk must always have at least one Welsh speaker on phones); one trained analyst is on parental leave weeks 2-4; one trained analyst is the desk's sole payroll-system specialist during month-end (week 4). Which pairing survives all four weeks?

- A) The two Welsh speakers
- B) The parental-leave analyst and the payroll specialist
- C) One Welsh speaker and the payroll specialist
- D) The two trained analysts who are neither Welsh speakers, on leave, nor the payroll specialist

**Correct answer: D**

**Explanation:** Eliminate by constraint. Option A seconds both Welsh speakers half-time; whenever both are simultaneously in transition work, the phones can lack a Welsh speaker — with careful shift-splitting it might be survivable, but it hard-wires a daily scheduling fragility into four weeks, and any sickness breaks it. Option B fails outright: the parental-leave analyst is absent weeks 2-4 and cannot deliver a four-week secondment. Option C survives weeks 1-3 but collides in week 4, when the payroll specialist must be fully available for month-end — a half-time secondment cannot be honoured that week. Option D — the two trained analysts carrying no competing constraint — is the only pairing that holds for all four weeks; the arithmetic also works: ten analysts minus two half-time secondments leaves nine FTE on phones, above the minimum of eight. Method over memory: list each candidate's constraints as unavailability windows, then choose the pair whose windows are empty. This is the resourcing half of your role reduced to its logical skeleton — and the reason experienced managers keep skills matrices current: the feasible pairing was only findable because the constraints were known in advance.

**Question 10 (challenging) — Root cause reasoning across a change boundary**

Following Saturday's network firmware update, Monday brings three complaint types: (i) intermittent VPN drops (38 reports, all remote workers); (ii) slow file opening on the shared drive (12 reports, all one office); (iii) a broken macro in the finance spreadsheet (2 reports). The firmware update's documented scope covers VPN concentrators and office network switches, not application software. Which triage is best reasoned?

- A) Attribute all three to the firmware update and roll it back immediately.
- B) Treat (i) and (ii) as plausibly firmware-related — matching the update's scope and timing — and investigate them against it; treat (iii) as probably coincidental, since spreadsheet macros are outside the change's mechanism, and route it normally.
- C) Treat all three as unrelated to the update, since correlation is not causation.
- D) Wait a week to see which symptoms persist.

**Correct answer: B**

**Explanation:** Causal triage runs on mechanism, not just timing. The VPN drops (i) sit dead-centre in the update's scope — VPN concentrators were changed, and the affected population (remote workers) matches the component. The shared-drive slowness (ii) plausibly traces to office switches — also in scope — and its single-office footprint matches switch-level changes. The macro fault (iii) has timing but no mechanism: firmware on network hardware does not alter spreadsheet code, so Monday's two reports are far more plausibly the ordinary Monday discovery of an unrelated fault. Option A overcorrects: rollback is a heavyweight intervention that should follow a confirmed causal link — and rolling back for the macro would fix nothing. Option C wields "correlation is not causation" as a thought-terminator: correlation plus mechanism plus matching scope is legitimate grounds for directed investigation, which is all B claims. Option D spends a week of user pain to avoid an hour of analysis. The framework point: change-related incident triage is your service transition and problem management skills meeting — the change record's documented scope is the causal map, and reading it precisely is what separates targeted investigation from superstition.

**Question 11 (challenging) — Logical audit of an improvement claim**

A team leader's quarterly review states: "Our coaching programme works: the ten analysts who received coaching improved their FCR by an average of 6 points, while the ten who declined coaching improved by only 1 point." What is the strongest logical objection?

- A) Six points is too small an improvement to matter.
- B) The comparison is undermined by self-selection: analysts chose whether to take coaching, so the coached group likely differs systematically (in motivation, in room to improve) from the decliners — the 5-point gap cannot be attributed to coaching alone.
- C) FCR is the wrong metric for measuring coaching.
- D) The sample of twenty analysts is too small to conclude anything.

**Correct answer: B**

**Explanation:** The comparison's fatal feature is that the groups assigned themselves. Analysts who accept coaching plausibly differ from decliners in ways that independently predict improvement — motivation, self-awareness, starting point (those with more headroom may seek help more readily) — so the observed gap confounds the programme's effect with the choosers' characteristics. The claim "coaching works" needs like-for-like comparison: matched starting FCR, or better, offer-based comparison rather than uptake-based. Option A is backwards — 6 points is operationally meaningful if real. Option C is unargued: FCR is a reasonable coaching outcome. Option D gestures at sample size, a genuine but secondary concern — with self-selection unaddressed, even two hundred analysts would not rescue the inference, so B is the stronger objection. The managerial relevance is sharp: your role uses data analytics "to make decisions that enhance business performance", and the most common analytic failure in management reporting is not arithmetic but design — comparing groups that were never comparable. Praise the team leader's instinct to measure; fix the comparison before funding the conclusion.

### Preparation tips

- Practise anomaly detection against baselines: take your own dashboard and, for each metric, articulate its normal range before looking at today's value. The habit of range-first reading transfers directly to test questions and morning reviews alike.
- Read compound conditions as logic: circle AND, OR, "only if", "after", and "unless" in any rule question — and in your own transition criteria. Most deduction errors are conjunction errors.
- Audit documents for internal consistency first: before judging a plan or proposal's assumptions, check whether it contradicts itself. Self-contradiction is the fastest legitimate kill, in tests and in vendor meetings.
- When two events correlate in time, demand a mechanism before assigning cause — and when a comparison flatters a programme, ask how the groups were formed.
- Rehearse constraint-based resourcing on paper: list people as rows, weeks as columns, constraints as blocked cells. Feasibility questions become visual and fast.
- For the test itself: rest well, use the ungraded warm-up items, and treat rising difficulty as evidence of success on adaptive platforms.

### Common pitfalls to avoid

- **Letting one strong number satisfy a compound requirement.** A 71% FCR does not shorten a two-week pilot. Check every condition separately.
- **Reading composition effects as trends.** Satisfaction, FCR, and duration averages all move when the mix moves. Decompose before diagnosing.
- **Dismissing leading indicators because lagging ones are stable.** Stable CSAT today says nothing about the reopen rate's message about next month.
- **Accepting business cases at headline level.** Reconcile a proposal's own numbers against its own stated assumptions before debating the assumptions.
- **Using "correlation is not causation" to avoid analysis.** The disciplined move is directed investigation where mechanism and scope align — not blanket scepticism, not blanket attribution.
- **Trusting self-selected comparisons.** Groups that formed themselves cannot cleanly credit an intervention. Ask how the comparison was constructed before acting on it.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment measures your fluency with the quantitative material a service desk manager's decisions rest on: SLA aggregates across sites and priorities, satisfaction and quality metrics, cost-per-contact and automation economics, capacity and resourcing arithmetic, and trend analysis across months and quarters. The mathematics itself stays at percentages, ratios, weighted averages, rates, and projections — nothing beyond confident numeracy — but the questions increasingly test judgement about numbers: which base to divide by, which comparison is fair, which projection method suits the data, and what a figure can and cannot support.

The typical format is an online, timed test of 20 to 30 minutes with 15 to 20 questions built around tables and charts. An on-screen calculator is generally provided; rough working is expected and wise. Scoring profiles accuracy against speed relative to a norm group, often adaptively.

For a service desk manager, this assessment matters because your role summary makes numeracy an explicit management competence: "use data analytics skills to make decisions that enhance business performance". You are the person who converts desk data into resourcing cases, automation decisions, transition readiness judgements, and honest performance narratives for directors. You are also the quality gate for other people's numbers — vendor claims, team leaders' reviews, programme dashboards — and the questions below rehearse both roles: producing correct figures, and catching incorrect ones before they reach a decision.

### How this assessment maps to your role

- **Percentages, aggregates, and weighted combinations** map to your **IT service reporting** skill: desk-level truth is assembled from sites, priorities, and months of different sizes, and assembling it correctly is the difference between analytics and anecdote.
- **Cost and benefit arithmetic** maps to your **Customer service management** duty to investigate automation: automation decisions are cost-per-contact calculations with assumptions attached, and you own the assumptions.
- **Capacity and utilisation calculations** map to your responsibility for **resourcing** the team: converting demand forecasts into FTE requirements, and secondments into coverage effects, is recurring managerial arithmetic.
- **Trend measurement and projection** map to your **Problem management** and **Ownership** skills: "proactive in searching for potential problems" quantitatively means measuring drifts early and projecting them honestly.
- **Fair comparison across units** maps to your oversight of **customer service functions**: comparing sites, teams, and periods requires rate-based, mix-aware comparison — the numeric form of fairness.

### Practice questions

**Question 1 (easy) — Aggregate SLA across priorities**

Last month the desk resolved within SLA: 46 of 50 priority 1 incidents, 285 of 300 priority 2, and 583 of 650 priority 3. What was the overall within-SLA percentage across all incidents?

- A) 89.7%
- B) 91.4%
- C) 92.0%
- D) 93.1%

**Correct answer: B**

**Explanation:** Aggregate from totals. Step 1: incidents met = 46 + 285 + 583 = 914. Step 2: total incidents = 50 + 300 + 650 = 1,000. Step 3: overall = 914 ÷ 1,000 = 91.4%. The convenient total (1,000) is deliberate — the realistic trap is elsewhere: averaging the three percentages (92%, 95%, 89.7%) gives 92.2%, which overweights the tiny priority 1 category, with 50 incidents, to equal standing with priority 3's 650. Weighted aggregation from raw counts is the only honest desk-level figure. Worth internalising as the manager who signs the report: whenever someone hands you a "combined" percentage, your first question is whether it was built from counts or from averaged percentages — the two diverge exactly when category sizes differ, which is always.

**Question 2 (easy) — Cost per contact**

The desk's monthly operating cost is £96,000, covering all channels. Last month it handled 8,000 contacts: 5,600 calls, 1,900 portal tickets, and 500 emails. What was the overall cost per contact?

- A) £10
- B) £12
- C) £14
- D) £17

**Correct answer: B**

**Explanation:** Cost per contact = total cost ÷ total contacts = £96,000 ÷ 8,000 = £12. The channel split is context, not calculation — a common test device mirroring a common workplace reality: reports carry more numbers than the current question needs, and selecting the relevant ones is part of the skill. Where the split matters is the next managerial step: if a costed channel analysis later shows calls at £14 and portal tickets at £6, every contact shifted to the portal saves about £8 — the arithmetic on which channel-shift and automation cases are built. Cost per contact is also the desk's most quoted benchmarking figure, so producing it cleanly, and knowing what it hides (channel mix, complexity mix), is baseline manager numeracy.

**Question 3 (easy) — Satisfaction survey response arithmetic**

A satisfaction survey was sent for 2,400 resolved tickets; 360 responses arrived, of which 306 rated the service 4 or 5 out of 5. What was the response rate, and what percentage of respondents rated 4 or 5?

- A) 12% response rate; 88% rated 4-5
- B) 15% response rate; 85% rated 4-5
- C) 15% response rate; 88% rated 4-5
- D) 18% response rate; 82% rated 4-5

**Correct answer: B**

**Explanation:** Two divisions with two different bases. Step 1: response rate = 360 ÷ 2,400 = 0.15 = 15%. Step 2: satisfied share = 306 ÷ 360 = 0.85 = 85% — divided by respondents, not by surveys sent. Keeping the bases straight is the entire question, and the entire discipline: 306 ÷ 2,400 (12.75%) would be the share of all resolved tickets whose users responded positively, a different and much less flattering-sounding number that answers a different question. The managerial layer: a 15% response rate means 85% of experiences are unmeasured, and response samples skew toward strong feelings — so "85% satisfied" describes respondents, not users. Reviewing customer satisfaction, per your role summary, includes saying so in the report: precision about the base is precision about the claim.

**Question 4 (easy) — FTE arithmetic for a secondment**

Your desk has 11 analysts: nine full-time and two at 0.6 FTE each. You second one full-time analyst to a transition project at half-time for a quarter. What is the desk's phone-available FTE during the secondment?

- A) 9.4
- B) 9.7
- C) 10.2
- D) 10.7

**Correct answer: B**

**Explanation:** Step 1: baseline FTE = 9 × 1.0 + 2 × 0.6 = 9 + 1.2 = 10.2. Step 2: the secondment removes half of one full-timer: 10.2 − 0.5 = 9.7 FTE. Option C is the baseline with the secondment forgotten; option A subtracts a full FTE for a half-time secondment. Small sums, real consequences: rota planning, SLA forecasting, and recruitment cases all start from an accurate FTE position, and part-time contracts plus partial secondments are exactly where mental arithmetic slips. As the manager, you will present this number to justify backfill — "we are operating at 9.7 against a modelled need of 10" is a fundable sentence, and it is only as credible as its decimal.

**Question 5 (moderate) — Automation benefit with uptake assumptions**

Password reset automation is projected to divert tickets currently costing £8 each to a self-service route costing £1 each. Monthly password volume is 1,400 tickets. Uptake is projected at 40% in quarter one, rising to 70% from quarter two. The tool costs £3,500 per month. What is the projected net monthly saving in quarter one, and from quarter two?

- A) Q1: £420 net saving; Q2 onward: £3,360 net saving
- B) Q1: £560 net loss; Q2 onward: £2,860 net saving
- C) Q1: £420 net loss; Q2 onward: £3,360 net saving
- D) Q1: £3,920 net saving; Q2 onward: £6,860 net saving

**Correct answer: A**

**Explanation:** Saving per diverted ticket = £8 − £1 = £7 (the self-service route still costs something — forgetting the £1 produces option D's inflation). Quarter one: diverted tickets = 1,400 × 0.40 = 560; gross saving = 560 × £7 = £3,920; net = £3,920 − £3,500 = £420 per month — positive, barely. From quarter two: diverted = 1,400 × 0.70 = 980; gross = 980 × £7 = £6,860; net = £6,860 − £3,500 = £3,360 per month. So the case is marginal at launch and healthy at mature uptake — which is the actual managerial insight: the investment's success hinges on the uptake ramp, so the decision should fund uptake (promotion, portal placement, analyst signposting) as deliberately as it funds the tool, and the quarterly review should track uptake as the case's live variable. This is "investigate which processes can be automated" done numerically: not whether automation saves money, but under which assumptions, and which assumption to manage.

**Question 6 (moderate) — Percentage-point drift and run-rate**

The desk's within-SLA rate has declined steadily: April 94.0%, May 92.5%, June 91.0%. The contract requires "at least 88%" each month. If the decline continues at the same rate, in which month does the desk first fail the contractual requirement?

- A) July
- B) August
- C) September
- D) October

**Correct answer: C**

**Explanation:** Measure the drift first: 94.0 → 92.5 → 91.0 is a steady fall of 1.5 percentage points per month. Project forward: July = 91.0 − 1.5 = 89.5% — above 88, still compliant. August = 89.5 − 1.5 = 88.0% — and here the boundary convention decides everything: the contract requires "at least 88%", and 88.0% meets that requirement exactly, so August passes. September = 88.0 − 1.5 = 86.5% — the first month below the floor, and the first failure. The trap in option B is treating "touching the line" as failing; contracts written as "at least" include the boundary, while contracts written as "above" exclude it, and penalty clauses turn on precisely this wording. The managerial translation for your report: "at the current 1.5-point monthly drift we touch the floor in August and fall through it in September — recovery actions must land before August to preserve margin." Two habits are being tested and both are yours to model: measure the drift before projecting, and read the threshold's boundary behaviour before briefing anyone on when it bites.

**Question 7 (moderate) — Comparing sites fairly**

Two sites' monthly figures: Site A — 3,000 contacts, 2,760 within SLA, 8 complaints; Site B — 1,200 contacts, 1,092 within SLA, 5 complaints. Which statement is accurate?

- A) Site A performs better on SLA and complaints.
- B) Both sites have identical SLA performance (91%); Site A has the lower complaint rate (2.7 versus 4.2 per 1,000 contacts).
- C) Both sites have identical SLA performance (92%); Site B has the lower complaint rate.
- D) Site B performs better on both measures.

**Correct answer: A**

**Explanation:** Compute every rate before judging. SLA: Site A = 2,760 ÷ 3,000 = 92%; Site B = 1,092 ÷ 1,200 = 91% — Site A leads by one point. Complaint rates per 1,000 contacts: Site A = 8 ÷ 3,000 × 1,000 = 2.67; Site B = 5 ÷ 1,200 × 1,000 = 4.17 — Site A's rate is markedly lower despite its higher raw count. So Site A is ahead on both measures: option A. Eliminate the rest against the computed figures: option B claims identical SLA at 91% (false — A is 92%); option C claims identical SLA at 92% and a lower complaint rate for B (false on both); option D claims B leads on both (false on both). The deliberate texture worth absorbing: raw complaint counts (8 versus 5) point the opposite way to complaint rates (2.67 versus 4.17) because Site A handles two and a half times the volume — normalisation reverses the naive reading, exactly as in real multi-site oversight. Overseeing customer service functions across sites means never comparing raw counts across different denominators: rates first, then judgement — and when a colleague's slide ranks sites by complaint count, yours is the voice that asks for the per-thousand column.

**Question 8 (moderate) — Capacity model for a demand increase**

A department of 1,800 staff generates desk demand of 0.9 contacts per person per month. A machinery-of-government change adds 600 staff whose previous desk experienced 1.2 contacts per person per month. Each analyst handles 640 contacts per month. How many analysts does the combined demand require (round up)?

- A) 3
- B) 4
- C) 5
- D) 6

**Correct answer: B**

**Explanation:** Step 1: existing demand = 1,800 × 0.9 = 1,620 contacts per month. Step 2: incoming demand = 600 × 1.2 = 720 contacts per month (use the incoming population's own observed rate — assuming they will instantly match your 0.9 is optimism, not modelling; transitions typically raise contact rates before settling). Step 3: combined = 1,620 + 720 = 2,340 contacts. Step 4: analysts required = 2,340 ÷ 640 = 3.66, rounding up to 4 — you cannot staff a fraction, and rounding down builds a permanent queue. The managerial notes attached: the 720 may spike higher in the first months (unfamiliar systems, migration issues), so 4 is a floor with a case for temporary surge cover; and the differing contact rates (0.9 versus 1.2) are themselves diagnostic — worth investigating whether the incoming population's higher rate reflects service culture, tooling, or unmet self-service, since converging them is an improvement opportunity. Capacity models earn their keep in the assumptions, not the division.

**Question 9 (challenging) — Backlog burn-down with net flow**

The desk carries a backlog of 900 aged tickets. Weekly inflow is 1,150 new tickets; the team's ordinary weekly resolution capacity is 1,100. A recovery initiative adds temporary capacity of 120 resolutions per week. Under the initiative, how many weeks until the backlog clears, and what happens when the temporary capacity ends?

- A) 9 weeks; the backlog stays cleared afterwards.
- B) 13 weeks; after the initiative ends, the backlog regrows at 50 tickets per week.
- C) 13 weeks; the backlog stays cleared afterwards.
- D) 9 weeks; after the initiative ends, the backlog regrows at 50 tickets per week.

**Correct answer: B**

**Explanation:** Work the flows. Ordinary net flow = capacity − inflow = 1,100 − 1,150 = −50: the desk loses ground by 50 tickets weekly, which is how the 900 backlog accumulated. With the initiative: total capacity = 1,100 + 120 = 1,220; net = 1,220 − 1,150 = +70 per week of backlog reduction. Time to clear 900 at 70 per week = 900 ÷ 70 = 12.86 → 13 weeks. Then the decisive part: when the temporary capacity ends, the underlying arithmetic reasserts itself — inflow 1,150 against capacity 1,100 — and the backlog regrows at 50 per week, reaching 900 again in 18 weeks. Option B alone contains both truths. The managerial lesson is structural: a backlog is a symptom of negative net flow, and surge capacity treats the accumulation, not the cause; a recovery plan is only complete when paired with a permanent change — 50+ tickets of weekly capacity (staffing, automation, deflection) or reduced inflow (problem fixes at source). Presenting the burn-down without the regrowth forecast is the kind of half-true chart your ownership duty exists to catch: "proactive in searching for potential problems" includes the one your own recovery plan is scheduled to recreate.

**Question 10 (challenging) — Weighted CSAT across channels with a mix shift**

Channel CSAT last quarter: phone 4.3 (3,000 responses), portal 3.8 (1,000 responses). This quarter, identical channel scores — phone 4.3, portal 3.8 — but the mix shifted: phone 2,000 responses, portal 2,000. What happened to overall CSAT, and what should the report say?

- A) Overall fell from 4.18 to 4.05; service quality deteriorated.
- B) Overall fell from 4.18 to 4.05; per-channel quality is unchanged and the fall is entirely the channel mix shifting toward the lower-scoring portal — the report should show both channel scores and flag portal experience as the improvement target.
- C) Overall is unchanged at 4.3; no action needed.
- D) Overall rose because portal responses doubled.

**Correct answer: B**

**Explanation:** Compute the weighted overalls. Last quarter: (4.3 × 3,000 + 3.8 × 1,000) ÷ 4,000 = (12,900 + 3,800) ÷ 4,000 = 16,700 ÷ 4,000 = 4.175 ≈ 4.18. This quarter: (4.3 × 2,000 + 3.8 × 2,000) ÷ 4,000 = (8,600 + 7,600) ÷ 4,000 = 16,200 ÷ 4,000 = 4.05. The overall fell 0.13 while both channel scores stood still — a pure composition effect: more of the experience now happens on the weaker-scoring channel. Option A's arithmetic is right and its diagnosis wrong; "deteriorated" would trigger the wrong response (a general quality drive) when the data points at a specific one (the portal's 3.8 is now half the experience and was tolerable only while it was a quarter of it). Option B carries the correct figures, the correct mechanism, and the correct managerial conclusion. This pattern — aggregate moves, components don't — recurs across desk metrics whenever channel shift or automation changes the mix, and it will intensify as your own automation initiatives migrate simple contacts away from the phone: expect phone CSAT to face harder average calls, portal volumes to grow, and every aggregate to need decomposition before briefing. Data analytics for decisions, per your role summary, is mostly this: refusing to let a blended number tell an unblended story.

**Question 11 (challenging) — Reading a trend table for an emerging issue**

Quarterly figures for a service the desk supports:

| Metric | Q1 | Q2 | Q3 |
|---|---|---|---|
| Incidents | 400 | 380 | 365 |
| Of which: recurring category X | 40 | 57 | 84 |
| Average resolution time (hours) | 6.0 | 6.1 | 6.9 |

Total incidents are falling. What is the most important finding for a manager?

- A) The service is improving — incidents fell 9% over two quarters.
- B) Category X is growing about 45-47% per quarter and now represents 23% of all incidents (up from 10%); its growth is masked by the falling total, and rising resolution times suggest X may also be harder to fix — X needs problem investigation now.
- C) Resolution time is the only concern.
- D) The data is contradictory and cannot support conclusions.

**Correct answer: B**

**Explanation:** Read the components against the headline. Category X: 40 → 57 → 84 — growth of 42.5% then 47.4% per quarter, roughly compounding; as a share of incidents: 40 ÷ 400 = 10%, 57 ÷ 380 = 15%, 84 ÷ 365 = 23%. Meanwhile non-X incidents fell from 360 to 281 — genuine improvement that more than offsets X's rise in the total, which is precisely how a compounding problem hides inside a falling aggregate. The resolution-time drift (6.0 → 6.9 hours) is consistent with the mix shifting toward a harder category, corroborating rather than competing with the X story. Project one quarter at the current growth rate: X reaches roughly 120-125 incidents while the non-X decline continues — the total turns upward and the "improving" narrative collapses publicly. Option A reads only the headline; option C notices the corroborating signal and misses its cause; option D gives up on data that is perfectly coherent once decomposed. This is the numeric skeleton of your defining duty: emerging issues live in the components, headline metrics are where they hide, and "initiate and monitor actions to investigate patterns and trends" begins with the decomposition that makes the pattern visible one quarter before it becomes an explanation you owe a director.

### Preparation tips

- Build every aggregate from raw counts, and decompose every aggregate you receive. Weighted combination and its inverse are the two moves behind most manager-level questions — and most manager-level briefings.
- State your base aloud before dividing: per contact, per respondent, per thousand, per FTE. Base errors survive review because the arithmetic looks clean; naming the base catches them.
- For any threshold or floor, resolve the boundary convention first: does touching the line pass or fail? Contracts, SLAs, and test questions all turn on "at least" versus "above".
- Model flows, not snapshots, for backlogs and queues: net flow per period explains the past and predicts the future; a snapshot does neither.
- Attach the assumption to every projection you practise: uptake rates, contact rates, growth rates. The habit of writing "at the current rate of..." keeps both test answers and board papers honest.
- Rehearse with your own desk's data: recompute last month's headline figures from their components. Discrepancies you find are both practice and management information.

### Common pitfalls to avoid

- **Averaging percentages across different-sized categories.** Aggregate from counts, always. The error flatters whichever small category performs best.
- **Switching bases mid-analysis.** Response rate uses surveys sent; satisfaction uses responses received. One question, one base.
- **Forgetting the residual cost in savings cases.** Automation diverts tickets to a cheaper channel, not a free one — the saving is the difference, not the whole.
- **Projecting from headlines while components diverge.** A falling total with a compounding subcategory is a deterioration wearing an improvement's clothes.
- **Treating surge capacity as a cure.** Burn-down arithmetic without the post-initiative net flow forecasts a relapse you will own. Pair recovery with permanent change.
- **Rounding people down.** Capacity requirements round up; the fraction you shave off becomes a queue with users in it.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment measures how precisely you read, interpret, and communicate the written material a service desk manager works with daily: service management framework definitions, contract and SLA clauses, transition documentation, satisfaction survey reports, user research summaries, supplier correspondence, and departmental policy. The dominant format presents a passage followed by statements to judge as **True** (the passage supports it), **False** (the passage contradicts it), or **Cannot say** (the passage is insufficient to decide). Complementary formats test best-summary selection, inference discipline, and clear-writing judgement — choosing the version of a sentence or message that communicates most accurately for a given audience.

The typical format is an online, timed test of 15 to 25 minutes with 20 to 30 statements across several passages. The governing discipline is answering from the passage alone: your framework knowledge and operational experience must inform your reading without supplying your answers. For knowledgeable managers this restraint is the core skill under test — and the most transferable, because it is also the discipline of accurate reporting.

Verbal precision at your level is consequential in a specific way: you operate at the boundary where operational reality is converted into words for decision-makers, and words from decision-makers are converted back into operational instruction. A misread SLA clause becomes a mispriced commitment; an overclaimed research finding becomes a misdirected improvement programme; an ambiguous transition criterion becomes a go-live argument at the worst possible moment. Equally, your own writing — readiness assessments, improvement cases, satisfaction narratives — is read by people who will act on exactly what you wrote, not what you meant. Employers test verbal reasoning at manager level because the written channel is where your judgement becomes organisationally real.

### How this assessment maps to your role

- **Precise comprehension of framework and contract text** maps to your **Service management framework knowledge**: ITIL lifecycle and capability concepts are defined terms, and applying them correctly begins with reading them exactly.
- **True/False/Cannot-say discipline** maps to your **IT service reporting** skill: "use data analytics skills to make decisions" presumes the verbal counterpart — distinguishing what evidence establishes from what it merely suggests.
- **Reading research without overclaiming** maps to your **User focus** skill: collaborating with user researchers, distinguishing user needs from desires, and championing research all require handling findings at their supported strength and no more.
- **Faithful summary for senior audiences** maps to your reporting and **Customer service management** duties: satisfaction reviews and improvement cases live or die on compression without distortion.
- **Clear-writing judgement** maps to your ownership of process documentation and transition criteria: the standards you approve are executed as written, by people under pressure, which makes ambiguity an operational defect.

### Practice questions

**Passage A (for Questions 1-3):** From a support contract schedule: "The supplier will provide second-line support for the case management service during core hours (08:00-18:00, working days). Priority 1 incidents will be accepted outside core hours via the emergency line, subject to a response time of one hour. For all other priorities, incidents reported outside core hours are deemed received at the start of the next core-hours period. Response time targets are: priority 1 — 30 minutes within core hours; priority 2 — 4 core hours; priority 3 — 8 core hours. 'Response' means a qualified engineer has begun diagnosis, not resolution of the incident. Service credits accrue only where the monthly achievement of any response target falls below 90%."

**Question 1 (easy) — True, False, or Cannot say**

Statement: "A priority 2 incident reported at 20:00 on Tuesday is deemed received at 08:00 on Wednesday, assuming Wednesday is a working day."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** The passage states that for all priorities other than priority 1, incidents reported outside core hours "are deemed received at the start of the next core-hours period". 20:00 Tuesday is outside core hours (which end at 18:00); the next core-hours period starts at 08:00 Wednesday if Wednesday is a working day — which the statement itself stipulates. The statement tracks the clause exactly: True. The clause matters operationally because the "deemed received" mechanism restarts the response clock: a priority 2 reported at 20:00 Tuesday has a 4-core-hour target expiring at 12:00 Wednesday, not at midnight Tuesday. Managers who miss deeming provisions either wrongly accuse suppliers of breaches or wrongly reassure users about overnight response — both expensive in credibility. Contract reading is clause-by-clause work, and deeming language ("deemed", "treated as", "considered to be") always changes how the clock runs.

**Question 2 (easy) — True, False, or Cannot say**

Statement: "If the supplier's engineer begins diagnosing a priority 1 incident 25 minutes after it is reported during core hours, the response target is met even if resolution takes three days."

- A) True
- B) False
- C) Cannot say

**Correct answer: A**

**Explanation:** Two clauses combine. The priority 1 core-hours response target is 30 minutes; 25 minutes is within it. And the definition clause states that "'Response' means a qualified engineer has begun diagnosis, not resolution" — so a three-day resolution, however painful, is irrelevant to whether the response target was met. The statement is True, and its sting is the point: response targets and resolution expectations are different obligations, and this contract as excerpted contains only response targets. A manager who reads "30-minute response" and hears "fast fixes" has bought something the words do not say — and will discover the gap during a major incident, in front of stakeholders. The defined-terms habit — checking what quoted words mean in this document rather than in ordinary usage — is the single highest-value contract-reading discipline, and verbal tests probe it constantly because real suppliers rely on it.

**Question 3 (easy) — True, False, or Cannot say**

Statement: "The supplier consistently meets its priority 3 response target."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** The passage defines the priority 3 target (8 core hours) and the credit mechanism (credits below 90% monthly achievement), but reports no performance data whatsoever — no achievement figures, no history, no assessment. "Consistently meets" is an empirical claim about performance, and the passage contains only obligations. Cannot say. The trap is the document-type inference: contract schedules describe what should happen so concretely that readers absorb it as what does happen. The same slip occurs in real management when process documentation is cited as evidence of practice — "the process requires a post-incident review" morphs into "we do post-incident reviews". Your reporting discipline depends on keeping the normative (what documents require) and the empirical (what data shows) in separate mental columns, and this question type is that discipline in miniature.

**Passage B (for Questions 4-6):** From a user research summary commissioned before a portal redesign: "We conducted contextual interviews with 15 caseworkers and 9 field officers, and analysed 4,000 portal sessions. Caseworkers frequently articulated a desire for a live chat channel. However, session analysis shows that 62% of failed portal journeys broke down at the service categorisation step, where users must choose among 14 categories whose labels reflect internal team structures rather than user tasks. Field officers, who work primarily on mobile devices, abandoned portal journeys at twice the rate of desktop users. We recommend restructuring categorisation around user tasks before investing in new channels. Chat may have value, but the evidence suggests users' underlying need is to complete existing journeys successfully, not to access an additional channel."

**Question 4 (easy) — Needs versus desires**

Which option best expresses the passage's central distinction?

- A) Users desire live chat, but the evidenced need is fixable journey failure — chiefly a categorisation structure that mirrors the organisation instead of user tasks.
- B) Users need live chat and desire better categorisation.
- C) Field officers need desktop computers instead of mobile devices.
- D) The research shows chat would have no value.

**Correct answer: A**

**Explanation:** The passage's architecture is exactly the user-focus distinction your role summary names — "explain the difference between user needs and the desires of the user". The desire is articulated (caseworkers ask for chat); the need is evidenced (62% of failed journeys break at categorisation, whose labels serve internal structure). The recommendation follows the evidence: fix the need before funding the desire. Option B inverts the pairing. Option C mistakes a finding (mobile abandonment is higher) for a prescription the passage never makes — the mobile finding indicts the portal's mobile experience, not the officers' devices. Option D overstates: the passage says chat "may have value" and subordinates it, which is prioritisation, not dismissal. Note the passage's method as a model for your own commissioning: triangulating stated preferences (interviews) against behavioural data (sessions) is precisely how "use quantitative and qualitative data about users" produces decisions rather than wish-lists.

**Question 5 (moderate) — True, False, or Cannot say**

Statement: "Most failed portal journeys involved field officers."

- A) True
- B) False
- C) Cannot say

**Correct answer: C**

**Explanation:** Inventory what the passage establishes: 62% of failed journeys broke at the categorisation step (a claim about where journeys fail, not who fails them); field officers abandoned at twice the rate of desktop users (a claim about relative rates, not absolute counts). Neither fact, nor their combination, tells you what share of failed journeys involved field officers: a rate twice as high applied to a possibly small field-officer population could yield a small minority of total failures — or, if field officers dominate portal use, a majority. The population sizes are absent, so the statement cannot be evaluated: Cannot say. This rate-versus-share confusion is among the most consequential in management reading — "group X fails at twice the rate" and "group X accounts for most failures" license entirely different investments — and survey summaries routinely blur it. The disciplined reader converts every quantitative claim to its exact form (a rate? a share? a count?) before letting it support anything.

**Question 6 (moderate) — Best summary for an investment board**

You must compress Passage B into one sentence for a portfolio board deciding between funding chat or funding the redesign. Which is best?

- A) "Research found users want chat, so we should fund it."
- B) "Research triangulating 24 interviews with 4,000 sessions found the dominant failure is task-misaligned categorisation (62% of failed journeys) with acute mobile impact; it recommends fixing categorisation before new channels, noting chat's value is unproven rather than absent."
- C) "The portal is broken for everyone and needs a complete rebuild before any other work."
- D) "Users don't really want chat; the research recommends categorisation work instead."

**Correct answer: B**

**Explanation:** Option B preserves the four load-bearing elements: the method's strength (triangulation, with scale), the central finding with its figure and mechanism (62%, categorisation, task misalignment), the differential impact (mobile), and the recommendation with its exact epistemic status (chat unproven, not worthless). Each rival distorts along a classic axis. Option A reports the desire and discards the evidence — the summary a chat vendor would write. Option D misreports the interviews (users did want chat; the research subordinates rather than denies the desire) — and boards notice when a summary contradicts a finding someone else has read. Option C inflates a specific, fixable defect into a catastrophe, which typically forfeits funding for both options. Summary-writing for boards is a compression exercise with a fidelity constraint: every omitted detail is a judgement call, and the details you must never omit are the ones the decision turns on — here, the figure, the mechanism, and the recommendation's conditionality. "Champion user research" sometimes means exactly this: carrying its precision, not just its conclusion, into the room where the money is.

**Passage C (for Questions 7-9):** From a draft transition readiness standard you are reviewing: "A service is ready for desk support when all mandatory criteria are met. Mandatory: knowledge articles published and reviewed by a senior analyst; at least 30% of desk analysts trained, including at least one per shift pattern; support model documented, naming second- and third-line resolver groups with agreed response times; and a rollback procedure documented and tested. Desirable: a pilot period of two weeks; automated monitoring feeding the desk dashboard. Where a desirable criterion is not met, the service desk manager may accept the service with a documented risk acceptance. Where any mandatory criterion is not met, go-live must be deferred; the service desk manager may not waive mandatory criteria."

**Question 7 (moderate) — True, False, or Cannot say**

Statement: "A service with published and reviewed knowledge articles, 35% of analysts trained across all shift patterns, a documented support model with agreed response times, and a documented but untested rollback procedure may go live if the service desk manager documents a risk acceptance."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Audit the service against the mandatory list: articles — met; training — met (35% exceeds 30%, all shift patterns covered); support model — met; rollback — the criterion requires "documented and tested", and this rollback is documented but untested: a mandatory criterion is unmet. The standard's final clauses then govern: mandatory failures defer go-live, and "the service desk manager may not waive mandatory criteria" — the risk-acceptance mechanism belongs exclusively to desirable criteria. The statement asserts a permission the standard explicitly withholds: False. The near-miss construction is deliberate: three and three-quarter criteria met, with the shortfall hiding inside a two-part requirement ("documented and tested") whose first half glitters. Real go-live pressure works exactly this way — "the rollback is written up, testing is scheduled for Thursday, the programme board meets Tuesday" — and the standard you are reviewing exists precisely to make the answer impersonal. Reading conjunctions inside criteria ("and tested") as strictly as criteria themselves is what makes a readiness standard enforceable, in tests and at boards.

**Question 8 (moderate) — Clear-writing judgement on a standard's clause**

The draft also contains this clause: "Training completion should ideally be considered as being achieved when analysts have, where practicable, engaged with the relevant materials and can be regarded as broadly familiar with the new service." As the reviewing manager, which replacement is best?

- A) "An analyst counts as trained when they have completed the e-learning module and passed the service's knowledge check."
- B) "Training is achieved through meaningful engagement with the learning pathway."
- C) "Analysts should familiarise themselves with the new service to an appropriate standard."
- D) Keep the draft — flexibility helps operational teams apply judgement.

**Correct answer: A**

**Explanation:** The clause exists to make a mandatory criterion auditable — "at least 30% of analysts trained" is only checkable if "trained" has a binary, observable definition. Option A supplies one: a completion event and a pass event, both recorded by systems, leaving nothing to argue about at a readiness review. The draft is unenforceable by construction: "should ideally", "where practicable", "can be regarded as", and "broadly familiar" are four escape hatches in one sentence, and a criterion with escape hatches is a desirable criterion wearing mandatory clothing. Options B and C swap hedges for abstractions ("meaningful engagement", "appropriate standard") — different words, same unauditability. Option D mistakes ambiguity for flexibility: operational judgement belongs in decisions the standard assigns to people (like risk acceptances), not in the definitions the standard is built from — flexible definitions do not empower teams, they relocate arguments to go-live week. The reviewing habit: for every criterion, ask "could two reasonable people disagree about whether this is met?" If yes, the criterion is not yet written.

**Question 9 (challenging) — Inference from the standard's structure**

Considering Passage C as a whole, which inference about the standard's design is best supported?

- A) The standard treats verification more strictly than documentation: several criteria require evidence of review, testing, or coverage, not just the existence of artefacts.
- B) The standard's authors believe pilots are unnecessary.
- C) The standard gives the service desk manager authority to accelerate go-lives when programmes are under time pressure.
- D) The standard requires all analysts to be trained before go-live.

**Correct answer: A**

**Explanation:** Test each inference against the text's structure. The mandatory criteria repeatedly pair artefacts with verification: articles "published and reviewed", rollback "documented and tested", training with a coverage condition ("at least one per shift pattern"), support model with "agreed" response times. The pattern — existence plus evidence — is consistent enough to support option A as a design principle. Option B over-reads classification as disbelief: placing the pilot among desirables subordinates it, but "desirable" plus a formal risk-acceptance mechanism signals valued-but-tradeable, not unnecessary. Option C inverts the text: the manager's only discretion is accepting desirable gaps; mandatory criteria are explicitly unwaivable, so the standard constrains acceleration rather than enabling it. Option D contradicts the stated threshold (30%, not all). Structural inference — reading what a document's architecture implies about its intent — is a senior verbal skill: it lets you defend a standard's philosophy ("we verify, we don't just collect documents") when negotiating exceptions, and lets you spot when a proposed amendment quietly breaks the design rather than merely adding a clause.

**Passage D (for Questions 10-11):** An email from a programme director: "Thanks for your readiness assessment on the licensing service. I understand your concerns about the untested rollback and the training coverage on nights. However, the Minister has announced the service publicly for the 1st, and moving that date is not an option I can take to the board. I'd ask you to look again at whether your criteria genuinely apply to a service of this size — it's small, low-volume, and the supplier is confident. Happy to discuss risk-sharing arrangements. Can you confirm by Friday that the desk will support go-live on the 1st?"

**Question 10 (challenging) — True, False, or Cannot say**

Statement: "The programme director has stated that the go-live date cannot be changed."

- A) True
- B) False
- C) Cannot say

**Correct answer: B**

**Explanation:** Read the sentence exactly: "moving that date is not an option I can take to the board." That is a statement about what the director is willing or able to propose, not about what is possible — the date could, as far as this email establishes, be changed by the board, by the Minister's office, or by the director choosing to take the option forward after all. The statement's paraphrase — "cannot be changed" — converts a positional claim into a factual one, which the text as written does not support and, by its own careful framing, implicitly contradicts: a genuinely immovable date would not need the framing "not an option I can take". False. This is not pedantry; it is negotiation literacy. Pressure correspondence routinely presents choices as facts ("the date is fixed", "there is no budget", "the supplier cannot attend"), and the manager who reads the modality precisely — who said it, with what qualifier, about whose choices — knows where the actual decision points sit. Your written reply can then address the real structure: the director's constraint is board-facing presentability, which risk-sharing language and a documented mitigation plan might solve without moving either the date or your criteria.

**Question 11 (challenging) — Choosing the reply**

Which reply to the programme director is most effective?

- A) "Confirmed — the desk will support go-live on the 1st. We'll manage the risks as they arise."
- B) "Our criteria are not negotiable and the desk will not support this go-live. The date must move."
- C) "Thank you — I understand the date's significance. Our two open items are specific and closable: the rollback needs one test (the supplier can run it next week) and night-shift coverage needs two analysts trained (bookable within days). If both close before the 1st, the desk supports go-live; if either remains open, I cannot waive a mandatory criterion, and I'd want us to jointly present the board a short options paper — including your risk-sharing suggestion — rather than have the desk absorb an undocumented risk. Can we take 30 minutes tomorrow?"
- D) "I'll defer to your judgement on whether the criteria apply, given the service's size — you know the programme best."

**Correct answer: C**

**Explanation:** Option C does what strong boundary-holding correspondence does: it separates the immovable from the solvable, and then works the solvable hard. It reframes the standoff — not "criteria versus date" but "two specific gaps versus ten days" — and makes closing them the shared project, which honours both the standard and the director's genuine constraint. It states the limit of authority factually ("I cannot waive a mandatory criterion" — which the standard in Passage C makes literally true, converting a personal refusal into an institutional one), and it answers the risk-sharing overture by relocating it to where it belongs: a documented, board-visible decision rather than a quiet transfer of unowned risk onto the desk. Option A trades the desk's users and analysts for Friday's comfort — and "manage risks as they arise" is what untested rollbacks make impossible. Option B may be substantively right about the criteria but is rhetorically constructed to fail: it offers no path, so it invites escalation over your head rather than resolution through you. Option D abandons the standard's design under exactly the pressure it was designed for — the criteria's applicability is not the director's call, and "the supplier is confident" is not a verification event. The tested capability is your ownership skill in written form: accountability that neither capitulates nor stonewalls, but converts pressure into a documented, decidable, shared problem. That is also, not incidentally, how service desk managers keep programme directors as allies.

### Preparation tips

- Practise on your own contracts and standards: pick a clause, write three statements about it (one true, one false, one cannot-say), and check your verdicts against the exact wording a day later. Defined terms and deeming provisions make the best practice material.
- Keep normative and empirical claims in separate columns as you read: what documents require versus what data shows. Most manager-level Cannot-say questions live in the gap.
- Convert every quantitative claim to its exact form before using it: a rate, a share, or a count. "Twice the rate" and "most of the failures" are different sentences.
- Read modality precisely in pressure correspondence: who is the subject of "can't", and what qualifier is attached? Positional claims dressed as facts are where negotiations actually live.
- For summary questions, identify what the decision turns on before compressing — the figure, the mechanism, the conditionality — and treat those as incompressible.
- Apply the two-reasonable-people test to any definition you write or approve: if they could disagree about whether it is met, it is not finished.

### Common pitfalls to avoid

- **Importing operational knowledge into the passage.** You know how support contracts usually work; the question asks what this one says. Text only.
- **Reading obligations as performance.** A target's existence is not its achievement. Contracts and process documents describe requirements, not results.
- **Blurring rates, shares, and counts.** Each licenses different conclusions and different investments; summaries that swap them mislead boards efficiently.
- **Missing conjunctions inside criteria.** "Documented and tested" fails on either half. Near-miss constructions are the favourite trap of both test-writers and go-live advocates.
- **Treating hedged text as flexible rather than broken.** "Ideally", "where practicable", and "broadly" in a standard are defects to fix at review, not latitude to enjoy at go-live.
- **Matching the pressure's frame in your reply.** The strong response neither confirms nor refuses on the asker's binary; it restructures — specific gaps, closable actions, documented decisions.

## Workplace job-specific situational judgement assessment

### About this assessment

A situational judgement test (SJT) presents realistic workplace dilemmas and asks you to evaluate possible responses — selecting the most effective, identifying most and least effective, ranking options, or rating each on a scale. It measures professional judgement rather than knowledge: how you weigh users, staff, suppliers, governance, and truth when they pull against each other, which at manager level they reliably do.

The typical format is an online test of 20 to 40 minutes with 10 to 20 scenarios, usually generously timed. Scoring compares your responses against a key calibrated by experienced practitioners and aligned with organisational values — in UK government, behaviours such as taking accountability, user focus, honesty in reporting, developing people, inclusion, and escalating well.

At service desk manager level, SJT scenarios acquire three characteristic properties worth recognising before you begin. First, accountability is non-transferable: scenarios probe whether you own outcomes — including your team's failures and your own past decisions — without either absorbing blame theatrically or deflecting it operationally. Second, your decisions set systems, not just outcomes: how you handle one analyst's error, one supplier's slip, or one satisfaction dip teaches your whole team what happens next time, and strong answers price in that teaching effect. Third, the dilemmas are structurally two-audience: nearly every scenario has an upward-facing dimension (directors, programmes, suppliers) and a downward-facing one (analysts, team leaders, users), and the tempting wrong answers usually sacrifice one audience to the other. Your role summary's own language — "take accountability for issues that occur", "be proactive in searching for potential problems", "achieve excellent user outcomes" — is close to a scoring key already. Answer as your realistic best professional self, consistently.

### How this assessment maps to your role

- **Accountability under scrutiny** maps to your **Ownership** skill: taking accountability for issues, including publicly and upwards, while fixing systems rather than assigning blame.
- **Continual improvement instincts** map to your **Customer service management** skill: "translate lessons learnt into continual service improvement" — scenarios test whether incidents become learning or merely endings.
- **Evidence-led decisions under pressure** map to your **IT service reporting** and **Problem management** skills: choosing investigation over assumption, and honest numbers over comfortable ones, when stakes are high.
- **People development and inclusion** map to your responsibility for **resourcing and development of the team**: scenarios probe fairness in opportunity, support in underperformance, and courage in conflict.
- **Championing users** maps to your **User focus** skill: representing users internally, distinguishing needs from desires, and holding user outcomes steady when organisational convenience argues otherwise.
- **Transition stewardship** maps to your duty to prepare and coordinate **service transition activities**: holding readiness lines, negotiating pressure, and handing risk to those entitled to accept it.

### Practice questions

**Question 1 (easy) — The outage and the director's question**

A four-hour outage of the case management service yesterday was prolonged because your desk escalated it to the wrong resolver group, losing 90 minutes. This morning a director asks you directly: "What went wrong?" What is the most effective response?

- A) Explain that the supplier's documentation was confusing, which caused the misrouting.
- B) Give the facts including the desk's misrouting and the 90 minutes it cost, alongside the other factors; state what is already changing (routing matrix corrected, resolver groups validated) and when the full review will report.
- C) Keep the answer high-level — "a combination of factors, under review" — until the formal review completes.
- D) Name the analyst who misrouted the escalation and describe their corrective training.

**Correct answer: B**

**Explanation:** Option B is accountability in its load-bearing form: accurate facts including the part that is yours, delivered unprompted, with correction already in motion — which is the only version of "what went wrong" that builds rather than spends credibility, because directors invariably learn the full story eventually, and the manager who told it first becomes the manager whose accounts are trusted. Option A may be partially true but leads with deflection; if supplier documentation contributed, it belongs in the factual account B gives, not as the headline. Option C defers truth you already possess — reviews refine understanding, they do not license withholding known facts from an accountable stakeholder. Option D converts a systems answer into a person answer: the director asked what went wrong, not who; naming an individual upward both misdiagnoses (a routing matrix an analyst could get wrong is the defect) and teaches your team that errors reach directors with names attached — after which errors stop being reported. "Take accountability for issues that occur" is your role summary's phrase, and its test is precisely this moment: the account you give when the room is senior and the failure is partly yours.

**Question 2 (easy) — The satisfaction dip and the board pack**

Quarterly CSAT has dipped from 4.2 to 3.9, driven by a painful email migration. The dip is explainable, and recovery actions are working. A colleague preparing the board pack suggests: "Show the six-month rolling average — it smooths the dip to 4.1 and avoids questions." What is the most effective response?

- A) Agree — the rolling average is a legitimate statistical choice and the dip is temporary anyway.
- B) Show the quarterly figure with the dip, alongside its cause, the recovery actions, and early evidence they are working; include the rolling average only as agreed standard presentation, not as a substitute introduced this quarter.
- C) Show both figures and let the board choose which to believe.
- D) Escalate the colleague's suggestion to their manager as attempted misrepresentation.

**Correct answer: B**

**Explanation:** The tell is timing: a rolling average adopted in the quarter it flatters is not a methodology but a concealment, whatever its statistical respectability — and boards, like directors, eventually meet the unsmoothed number. Option B reports the truth in decision-grade form: figure, cause, action, trajectory. That package converts a dip into evidence of a desk that measures honestly and recovers deliberately — genuinely better board material than an unexplained flat line. Option A launders the choice through "legitimate": presentation choices are legitimate when consistent, not when opportunistic. Option C abdicates the analyst's duty — boards are entitled to your interpretation, and "choose which to believe" outsources judgement you are paid for. Option D criminalises a colleague's first suggestion: the proportionate response to a bad idea offered openly is a better idea with reasons, escalating only if pressure persists. The habit under test is the reporting half of your role: "reviewing customer service satisfaction" means reporting it with its story, and the manager who shows unflattering numbers with their explanations is the manager whose flattering numbers get believed.

**Question 3 (easy) — The analyst error with user impact**

A well-regarded analyst bulk-closed 40 open tickets in error while tidying a queue; users received closure emails for unresolved faults. The analyst reported it themselves immediately, mortified. What is the most effective response?

- A) Thank them for reporting fast; make the priority reopening tickets and sending users a correction with apology; then look at why bulk-closure without confirmation was possible at all, and fix that.
- B) Formally document the error as a performance concern to ensure accountability.
- C) Reassure the analyst it happens to everyone and quietly reopen the tickets without user communication, to avoid alarming users.
- D) Require all future bulk operations to be approved personally by you.

**Correct answer: A**

**Explanation:** Sequence by harm: users currently believe their faults are being worked while nothing is happening — the reopening and the honest correction email come first, because undisclosed errors compound (users discover closures at their next chase, now with evidence the desk hid it). Then the system: an interface permitting an irreversible 40-ticket action without confirmation is the actual defect; the analyst is its first victim with reporting courage, not its cause. Option A's ordering — repair, disclose, fix the mechanism — is "translate lessons learnt into continual service improvement" executed at incident scale, and its treatment of the self-reporting analyst is the teaching moment: fast reporting must be visibly safe, or your desk's next error surfaces via user complaint instead. Option B punishes the exact behaviour (immediate self-reporting) the desk most needs, converting one error into a durable reporting chill. Option C hides harm from its owners — users are entitled to know their tickets stalled — and quiet fixes forfeit the trust that honest corrections build. Option D fixes a tooling defect with a bottleneck: routing all bulk operations through one person scales badly, teaches nothing, and substitutes your availability for a confirmation dialogue. Fix mechanisms, not throughput.

**Question 4 (moderate) — The automation announcement**

You are about to approve password-reset automation that will remove roughly 30% of first-line call volume within a year. Two analysts have privately asked whether it means redundancies; team mood is wary. Your honest assessment: no redundancies planned — natural turnover and redeployment to more complex work should absorb the change, though nothing is guaranteed. What is the most effective approach?

- A) Delay any team communication until the automation is live and its effects are measurable.
- B) Tell the team the truth as you hold it: the automation case, the honest jobs assessment including its uncertainty, the development path it opens (more complex, higher-skill work), and a commitment to share workforce planning as it firms up — inviting questions openly.
- C) Announce that jobs are completely safe, to settle the mood and protect morale.
- D) Announce the automation as a leadership decision that is not open for discussion, to prevent rumour cycles.

**Correct answer: B**

**Explanation:** The team's real question is not "what is automation?" but "am I safe, and does my manager tell me the truth?" — and option B answers both at the only sustainable price: honesty including its uncertainty. "No redundancies planned; turnover and redeployment should absorb it; nothing is guaranteed; here is the development path" is a statement the future cannot embarrass, and pairing it with the skills story converts threat into offer for at least some of the room. Option C mortgages your credibility to events you do not control — "completely safe" is remembered verbatim, and if funding or plans shift, every future assurance you give trades at a discount. Option A vacates the information space during maximum anxiety; teams fill silence with the worst available rumour, and the two analysts who asked privately are already the visible edge of a team-wide conversation happening without you. Option D suppresses the symptom (rumour) by confirming its cause (leadership that will not engage). The role connection is direct: "investigate which processes can be automated" is your named duty, and its people dimension — carrying a team through the change honestly — is what separates automation programmes that deliver from those that quietly generate resistance, attrition, and sabotage-by-lethargy.

**Question 5 (moderate) — The supplier's slipping quality**

Your second-line supplier's response performance has drifted down for three months: 94%, 91%, 88.5% against a 90% contractual target. Relationship is otherwise good; the account manager is personable and always has explanations. Your team leaders want to "give them another month". What is the most effective response?

- A) Give them another month — the relationship has value and the miss is small.
- B) Invoke the service credit clause immediately and formally, to establish seriousness.
- C) Raise it formally now — a documented performance review meeting with the data, causes, and a recovery plan with milestones — while separately verifying the desk's own escalation quality isn't contributing; treat credits as an outcome of the process, not the opening move.
- D) Begin sourcing a replacement supplier before raising the issue, to negotiate from strength.

**Correct answer: C**

**Explanation:** Read the shape: three months of monotonic decline through the contractual floor is a trend with momentum, not a blip — "another month" (option A) is how 88.5% becomes 85% with a quarter's delay purchased by personability, and account managers whose explanations always suffice are exactly how drifts institutionalise. Option C matches the response to the evidence: formal, documented, data-led, and forward-facing (recovery plan with milestones), which preserves the relationship precisely by keeping it professional — good suppliers respect structured challenge and are damaged instead by resentments that surface late. The self-audit half matters equally: if your desk's escalations have degraded (poor diagnostics, wrong priorities), the supplier's numbers partly measure your inputs, and discovering that in month one of a recovery plan is far cheaper than in month four of a dispute. Option B leads with the weapon: credits invoked before dialogue converts a solvable performance conversation into a contractual exchange, and money-first moves teach suppliers to manage to the letter. Option D prices a full re-procurement — cost, transition risk, knowledge loss — as a negotiating posture, which is disproportionate at 88.5% and dishonest as strategy. The escalation ladder — informal, formal, contractual, commercial — exists to be climbed rung by rung, with documentation at every step.

**Question 6 (moderate) — The user research you commissioned**

You championed research into why field officers underuse the support portal. The findings are uncomfortable: the top barrier is a categorisation structure your own team designed last year, and the report recommends unwinding it. Your team leader who led that design work calls the research "unrepresentative — they only spoke to 24 people". What is the most effective response?

- A) Accept the team leader's critique and shelve the report — 24 interviews is a small sample.
- B) Publish the findings as delivered, act on them, and note the design was your team's — modelling that research outranks authorship; engage the team leader on the fix, where their design knowledge is genuinely valuable, and address the sample-size question on its merits (triangulated with session data, appropriate for qualitative work).
- C) Soften the report's framing before wider circulation so the team is not demoralised.
- D) Commission a second, larger study before deciding anything.

**Correct answer: B**

**Explanation:** This scenario tests whether "champion user research" survives contact with research that indicts your own shop — the only condition under which championing costs anything. Option B pays the cost and collects the returns: acting on uncomfortable findings, with authorship acknowledged, is the single strongest signal a manager can send that evidence governs decisions — after which every future research exercise your desk runs is taken seriously. It also handles the sample critique honestly rather than politically: qualitative interviews triangulated against behavioural session data (the design from Passage B territory) is methodologically sound, and the team leader deserves that explanation, not a dismissal — while their redirect into the fix converts a defensive stakeholder into an invested one. Option A launders discomfort as methodology; sample-size objections that appear only when findings displease are tells, not critiques. Option C edits evidence for morale, which corrupts the information channel your decisions run on — and teams detect softened reports, learning that findings are negotiable. Option D purchases delay dressed as rigour: a second study to re-ask answered questions spends users' continued struggle as the currency. Needs versus desires applies internally too: your team desires vindication; users need the categorisation fixed.

**Question 7 (moderate) — The transition go-live vote**

At the go/no-go board for a new service, everything is green except one item you flagged: the out-of-hours support model is unstaffed — the supplier's overnight rota has two unfilled positions until next month. The programme director proposes going live anyway: "Overnight volume is tiny; day-one users are all office-hours staff." Other board members look to you. What is the most effective position?

- A) Agree unconditionally — the director's volume argument is sound.
- B) Refuse go-live until the rota is filled, since the support model criterion is unmet.
- C) Agree conditionally, converting the argument into managed risk: time-boxed acceptance (four weeks), an interim mitigation (your on-call escalation route with defined triggers), explicit board-minuted ownership of the residual risk, and a named checkpoint to verify the rota is filled — with the desk's support contingent on those conditions holding.
- D) Abstain, noting the decision belongs to the programme, not the desk.

**Correct answer: C**

**Explanation:** The director's argument has genuine content — overnight exposure is plausibly low for an office-hours user base — and the mature move is neither swallowing it (option A: an unstaffed support tier is a real gap whose cost arrives precisely when something breaks at 02:00, at maximum surprise) nor ignoring it (option B: readiness criteria protect outcomes, and a time-boxed, mitigated, owned risk can protect outcomes better than a month's delay protects them — deferral has user costs too). Option C is what "risk acceptance" means when done properly: the risk is quantified by argument, mitigated by an interim route with triggers (not a vague "we'll manage"), owned by the body entitled to own it (board-minuted, not absorbed silently by the desk), and time-boxed with verification (four weeks and a checkpoint, because "until next month" is a claim, not an event). The conditions convert the director's assertion into accountability. Option D is the abstention fallacy: the desk's readiness assessment is exactly what the board is convened to weigh, and "not our decision" is false — it is your input to a shared decision, and withholding judgement is withholding your role. Transition coordination, your named duty, is this craft: neither gatekeeper nor doormat, but the person who makes risk explicit, priced, mitigated, and signed for.

**Question 8 (moderate) — Most and least effective: the repeated near-miss**

Twice this month, analysts have caught themselves just before applying a decommissioned fix from the knowledge base — an article superseded six weeks ago but still surfacing first in search. No user harm has occurred yet. Four possible responses:

1. Treat the near-misses as free warnings: fix the superseded article's status today, audit the knowledge base for similar stale content, and add article review to the change checklist so decommissioned fixes are retired at source.
2. Remind analysts at the next team meeting to check article dates before applying fixes.
3. Log it as a risk in the risk register for quarterly review.
4. Wait for an actual incident, since near-misses with no harm don't justify diverting effort.

Which is the MOST effective and which is the LEAST effective response?

- A) Most: 1; Least: 4
- B) Most: 2; Least: 4
- C) Most: 1; Least: 3
- D) Most: 2; Least: 3

**Correct answer: A**

**Explanation:** Near-misses are the cheapest evidence a system ever produces: the defect's existence proven, the harm still hypothetical. Option 1 spends that evidence at full value — immediate correction (today's specific hazard), systematic sweep (the same mechanism has surely staled other articles), and root-cause closure (retirement wired into the change process so the class of defect stops regenerating). That triple structure — instance, class, mechanism — is "proactive in searching for potential problems" operating exactly as your role summary specifies. For least effective, compare 2, 3, and 4. Option 2 is weak but not worthless: awareness helps the analysts who heard it, briefly — though it quietly relocates a systems defect onto individual vigilance, which decays. Option 3 at least records the issue, but a quarterly register is a place near-misses go to await their incident. Option 4 is the worst by a distance: it explicitly prices user harm as the admission fee for action, inverts the entire logic of proactive management, and teaches the two analysts who reported near-misses that reporting achieves nothing. The general key: near-miss scenarios score responses by how far upstream they act — mechanism beats class, class beats instance, instance beats reminder, and "wait for the incident" is the floor.

**Question 9 (challenging) — The inherited underperformer**

You inherit a team leader, fifteen years on the desk, widely liked, whose team's numbers have been the desk's weakest for two years. Your predecessor's appraisals rate them "good" throughout. In your first month you observe the gap is real: weak coaching, avoided conflict, stale processes. The team leader mentions how much they value the desk's "family feel". What is the most effective approach?

- A) Continue the predecessor's appraisal pattern for a year while you build relationship capital, then address performance.
- B) Begin an honest, structured process now: share the data and your observations directly and privately, hear their account, agree specific expectations with genuine support (coaching, training, mentoring) and review points — decoupling the person's worth from the performance question, and keeping the paper trail accurate from your first conversation.
- C) Restructure the teams so this leader's weaknesses matter less, avoiding the confrontation.
- D) Move quickly to formal capability procedures, since two years of evidence already exists.

**Correct answer: B**

**Explanation:** The trap structure: two years of inaccurate "good" appraisals mean the organisation has been lying to this person — and every colleague watching knows the numbers. Option A extends the lie for relationship reasons, making you complicit in the pattern you inherited and converting your eventual honesty into apparent betrayal ("you rated me good, then ambushed me"). Option D reads the two years of data as if it were two years of honest feedback: procedurally, the person has never been told there is a problem — capability processes built on falsified history collapse, deservedly, and would be experienced as persecution by the team leader and as ruthlessness by the desk. Option C is organisational design as conflict avoidance: it taxes every other team with a workaround, solves nothing for this leader's team, and models that problems get architected around rather than addressed. Option B is the only path that is simultaneously fair to the person (truth, account-hearing, real support, time), fair to their team (whose members have absorbed weak leadership for two years — they are stakeholders too), and fair to the record (accurate from your first conversation, which protects everyone including the team leader whichever way development goes). The senior insight the key rewards: kindness and honesty are not opposed — the predecessor's "kind" appraisals were the cruellest option available, because they spent the person's years of correctable time.

**Question 10 (challenging) — The whistle from below**

A junior analyst asks to speak privately and, visibly nervous, tells you that a team leader has been instructing analysts to "pause" aged tickets into a suspended status before month-end, removing them from the ageing report, then reactivate them after reporting — for at least six months. The team leader is your strongest operational performer and a personal ally from your own analyst days. What is the most effective response?

- A) Thank the analyst, promise confidentiality about their identity, verify the pattern independently in the ticket data (suspension timestamps against reporting dates), and if confirmed, address it as a data-integrity issue with the team leader directly and formally — correcting historical reporting upwards, whatever the personal cost.
- B) Tell the analyst you will watch the situation, and quietly change the report logic to include suspended tickets, closing the loophole without confrontation.
- C) Bring the analyst and team leader together to discuss the allegation openly, since fairness requires the accused to face their accuser.
- D) Ask the team leader informally whether there is anything they want to tell you about month-end practices.

**Correct answer: A**

**Explanation:** Structure the duties: to the reporter (protection), to the truth (verification), to the organisation (accurate history), to the accused (evidence before accusation) — option A serves all four in the right order. Verification first is not scepticism of the analyst; it is what makes any subsequent action just and unanswerable, and suspension-timestamp patterns are objectively checkable. Confidentiality is not a courtesy: a junior who reported their own team leader to the desk manager took the largest professional risk available to them, and how you protect them determines whether your desk ever hears the truth from below again. Formality with the team leader — ally or not — is what "take accountability" means when the account is painful: six months of gamed ageing reports means six months of decisions (staffing, escalation, board assurance) built on false data, and the upward correction is yours to make because the reports went out under your name. Option B is the deep trap: it fixes the metric while burying the conduct — leaving a team leader who instructs juniors to falsify records in post, unaddressed, with the analysts who obeyed learning that integrity is negotiable and the one who reported learning it was pointless. Option C is confrontation theatre that torches the reporter's confidentiality — power asymmetry makes "face your accuser" an instrument of retaliation here, and it is your role, not the junior's, to carry the challenge. Option D gives a six-month pattern the chance to become a tidy story and the timestamps a reason to be explained away; informality is proportionate for ambiguity, not for systematic instruction of juniors. The hardest scenarios in manager SJTs are precisely this shape — evidence, loyalty, and hierarchy in conflict — and the key rewards the response that protects the powerless, verifies before acting, and pays the personal cost of the correction.

**Question 11 (challenging) — The improvement budget**

You have secured £40,000 of improvement funding, usable once. Three worthy claims: (a) replace the desk's creaking remote-support tool, which analysts curse daily and which slows most calls slightly; (b) fund the portal categorisation redesign your user research recommends, which would remove the top failure point for field officers — a minority of users with the worst current experience; (c) fund advanced diagnostic training for all analysts, your team's own top request in the staff survey. All three cases are sound; you can fund one. What is the most effective basis for deciding?

- A) Fund the tool — it touches every call, so total benefit is largest.
- B) Fund the training — honouring the team's top request repays their engagement and builds lasting capability.
- C) Decide from evidenced user outcomes: quantify each option's impact on users (including the equity weight of option b's concentrated harm to the worst-served group), test cheaper partial routes for the others, and publish the reasoning to team and stakeholders — whichever option wins.
- D) Split the funding three ways so each claim receives something.

**Correct answer: C**

**Explanation:** The question asks for a basis, not a winner — and that is the test's point: at manager level, how you decide is the competence, because the specific numbers could favour any option. Option C names the right sovereign (user outcomes — "achieve excellent user outcomes" is your ownership skill's literal text), prices the equity dimension properly (option b's harm is concentrated on the worst-served minority, and public service weighting for the worst-served is principle, not sentiment), disciplines the comparison with quantification rather than salience (the tool is cursed daily by the people nearest you, which is exactly why its claim needs numbers, not volume), and — the governance layer — publishes the reasoning, which is what makes the two losing constituencies accept the outcome and trust the next allocation. Option A decides by aggregate without distribution: "touches every call slightly" can genuinely lose to "transforms the worst experience substantially", and only quantification says which. Option B decides by internal constituency: staff-requested capability matters, but the improvement budget's beneficiaries of record are users, and morale purchased with users' money inverts the desk's purpose — the honest version funds training when its user-outcome case wins. Option D is the classic allocation failure: three underfunded fractions delivering none of the three cases' thresholds, chosen to avoid disappointing anyone, disappointing everyone slowly. Continual service improvement, your named skill, is at bottom an allocation discipline: evidence in, reasoning visible, user outcomes sovereign.

### Preparation tips

- Reread your role summary before practising and convert each duty into its hardest question: accountability (when the failure is partly yours), championing research (when findings indict your team), automation (when your own people fear it). SJT keys live at exactly those pressure points.
- Apply the three-audience check to every option: what does it do to users, to your team's learning, and to upward trust? Manager-level wrong answers usually serve one audience by silently taxing another.
- Watch the teaching effect: every response to an error, a report, or a request trains your whole team's future behaviour. Options that get today right and tomorrow wrong (punishing self-reporting, softening research) are the key's favourite traps.
- Distinguish absorbing risk from owning it: strong answers make risk explicit, priced, mitigated, and signed for by whoever is entitled to accept it — never silently swallowed to keep a meeting pleasant.
- In most/least formats, locate the option that requires harm before acting, hides truth to preserve comfort, or converts a systems defect into a person's fault — one of these is usually the least effective.
- Calibrate with peers: talk through scenarios with fellow managers and compare reasoning, not conclusions. Divergent rationales are where your judgement sharpens fastest — and the same conversations are development gold for your team leaders.

### Common pitfalls to avoid

- **Deflecting upward, blaming downward.** Accounts to directors that lead with suppliers' faults, or that name analysts, fail the ownership test in both directions at once.
- **Purchasing comfort with credibility.** Absolute reassurances ("jobs are completely safe"), smoothed metrics, and softened findings all trade your future believability for present calm — the key prices that trade correctly.
- **Punishing the messenger's channel.** Any response that makes self-reporting, near-miss flagging, or speaking up from below less safe is scored as the systemic failure it is, whatever else it fixes.
- **Confusing formality with hostility.** Documented supplier reviews, structured performance processes, and minuted risk acceptances protect relationships; informality under real stakes protects only the avoidance.
- **Deciding by salience or constituency.** The loudest claim, the nearest team, and the most senior voice are all measurement errors. Evidence and user outcomes are the sovereigns the key recognises.
- **Splitting what should be chosen.** Dividing scarce resources to avoid disappointment is an allocation failure wearing fairness as a costume — thresholds unmet everywhere help no one.

## Conclusion

Well done for working through this guide in full — sustained, honest practice of this kind is uncommon, and it compounds in ways that show.

Consider the territory you have covered. The cognitive section rehearsed the manager's core mental moves: reading anomalies against baselines, holding compound transition criteria to every clause, catching plans that break their own freeze windows, sequencing a Monday by rate of deterioration, and refusing self-selected comparisons and mechanism-free causation. The numeric section worked the arithmetic your decisions stand on: weighted aggregation, cost-per-contact, automation cases with uptake assumptions attached, boundary-precise SLA projections, backlog flows that forecast their own relapse, and the decomposition that finds a compounding problem inside a falling total. The verbal section sharpened the reading and writing your role converts into commitments: deeming clauses and defined terms, needs versus desires, rates versus shares, auditable criteria versus hedged ones, and replies that hold a readiness line while giving a programme director a path. The situational judgement section rehearsed the dilemmas that define the level: accountability with the failure partly yours, honest numbers under board pressure, errors treated as system evidence, research that indicts your own design, risk signed for rather than swallowed, and the whistle from below answered with verification, protection, and personal cost.

The through-line deserves naming: none of this is assessment technique bolted onto your job — it is your job, compressed. "Identify emerging issues" is the anomaly and decomposition practice. "Use data analytics to make decisions" is the weighted averages and the self-selection critique. "Take accountability" is the director's question answered with your own 90 minutes included. Preparing for these assessments and deepening your management practice are the same investment, which is why the effort you have just made pays twice.

It pays a third time through your team. Nearly every question here converts directly into development material — dashboard anomalies for your senior analysts, the automation business case for your team leaders, the SJT dilemmas for your own succession conversations. Teaching these patterns is the strongest way to consolidate them, and building your team's judgement is, per your role summary, precisely what you are for.

If an assessment is imminent: trust the preparation, rest properly, use the platform's practice items, and read rising difficulty on adaptive tests as the compliment it usually is. If not, return to one section a month with your own desk's data and keep the instrument sharp.

A last word of perspective. An assessment is a structured snapshot of capabilities you exercise daily under less structured conditions. The judgement your users, analysts, and directors experience from you — measured, honest, evidence-led — is the real subject, and it is built exactly the way you built it here: deliberately, question by question. Keep going. Your desk, and the public it serves, are better for a manager who prepares like this.




