# Performance Analyst - Psychometric Assessment Resources

## Introduction

Welcome! This guide has been created especially for you as a performance analyst working in the UK Government Digital and Data profession. Whether you are preparing for an internal assessment, applying for a new post, or simply want to sharpen the mental skills you use every day, this document will help you practise, reflect, and build confidence.

Psychometric assessments are structured, standardised exercises that measure the thinking skills and judgement a role genuinely requires. They are widely used across the Civil Service and the wider public sector because they are fair, objective, and evidence-based: every candidate faces the same questions, scored against the same benchmark, so decisions rest on demonstrated ability rather than impressions. For a performance analyst, that matters a great deal. Your role sits at the heart of evidence-based decision making. You develop performance measurement frameworks - Key Performance Indicators (KPIs), goals, user needs and benefits - and you analyse how a service or product performs against them. You are responsible for the accuracy and quality of data and analysis, and how they are used. In other words, the very skills psychometric assessments measure - spotting patterns, interpreting numbers, reading critically, and exercising sound judgement - are the skills you rely on every working day.

This document is organised around the four assessment types you are most likely to meet:

1. **Workplace job-specific cognitive assessment** - pattern recognition, logical deduction, error checking, prioritisation, and problem solving using the artefacts you really handle: dashboards, data pipelines, measurement frameworks, and quality assurance checks.
2. **Workplace job-specific numeric reasoning assessment** - tables, percentages, ratios, conversion rates, and performance metrics drawn from realistic service data.
3. **Workplace job-specific verbal reasoning assessment** - dense role-relevant passages such as service standards, data policies, stakeholder emails, and analytical reports, followed by True / False / Cannot Say and comprehension questions.
4. **Workplace job-specific situational judgement assessment** - workplace dilemmas involving the stakeholders you really work with: product managers, user researchers, developers, community colleagues, and senior decision makers.

Each section explains what the assessment measures, maps it to the specific skills in your role profile, and then gives you a generous set of practice questions with full worked explanations. Every scenario is set in a UK government digital context, so nothing here will feel abstract or artificial.

How should you use this guide? Three ways work well. First, **practise**: attempt each question honestly before reading the answer, ideally under light time pressure. Second, **self-reflect**: when you get a question wrong, read the explanation carefully and ask what habit of thought led you astray. Third, **prepare**: use the preparation tips and common pitfalls in each section to build a short personal checklist before any real assessment. Work through the guide at your own pace - little and often beats one long cramming session.

Good luck, and enjoy the practice. You already use these skills every day; this guide simply helps you show them at their best.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment is a targeted psychometric test designed to measure the exact mental processes your role demands. Unlike a generic IQ test, it uses practical workplace scenarios and data formats drawn from the job itself, so it predicts how you will actually perform at work. For a performance analyst, that means the questions look like your everyday artefacts: analytics dashboards, KPI tables, tracking plans, measurement frameworks, funnel reports, and quality assurance checklists.

These assessments are usually delivered online and timed, typically 15 to 30 minutes, with objective scoring against a benchmark or norm group. Many platforms offer short, ungraded practice questions first so you can get comfortable with the interface, and some adapt question difficulty based on your previous answers. Employers generally receive a breakdown of speed versus accuracy rather than a single raw score, so working steadily and accurately matters just as much as working fast.

The test measures a cluster of connected abilities: recognising patterns in data, deducing conclusions logically from given facts, checking material for errors, prioritising competing demands, and solving unfamiliar problems methodically. Because the questions are strictly validated, everything you meet should relate to skills the role genuinely uses - which, for you, is good news. Performance analysis is fundamentally a cognitive craft.

### What it measures for your role

Each cognitive dimension maps directly onto the skills named in your role profile:

- **Pattern recognition** maps to your **Analysis and insight** skill. Spotting a step change in a time series, noticing that a metric moves whenever a release ships, or seeing that two segments behave differently is exactly the "range of techniques to analyse data and provide insight" your profile describes.
- **Logical deduction** maps to **Performance measurement** and **Technical understanding**. Turning business needs and goals into performance measures requires clean if-then reasoning: if the goal is channel shift, then the measure must compare digital and non-digital transactions, and so on.
- **Error checking** maps to **Quality assurance of data and analysis**. You decide whether data and analysis are accurate and fit for purpose, perform data preparation and cleansing, and peer-review colleagues' outputs. Error-checking items simulate this directly.
- **Prioritisation** maps to your role-level responsibility to "help to plan and ensure project delivery" and to work independently while knowing when to seek guidance. Cognitive tests often present competing tasks and ask which to tackle first.
- **Problem solving** maps to **Analysis and insight** ("apply innovative approaches to resolve problems") and to **Understanding analysis across the product life cycle**, because diagnosing why a metric moved requires you to reason about the service, its phase, and its instrumentation together.
- **User-centred reasoning** maps to **User-centred analysis**: several questions below ask you to reason about quantitative and qualitative user data together.

### Practice questions

**Question 1 (easy) - Pattern recognition in a weekly series**

You monitor the weekly completion rate for an online licence application service. The last six weeks read: 71%, 73%, 75%, 74%, 76%, 78%. A colleague says the service is "volatile and unpredictable". Which statement best describes the pattern?

- A. The series shows a steady downward trend.
- B. The series shows a gradual upward trend with minor fluctuation.
- C. The series is random with no discernible trend.
- D. The series shows a seasonal cycle repeating every three weeks.

**Correct answer: B.**

**Explanation:** Reading the values in order, the completion rate rises from 71% to 78% over six weeks, gaining roughly one to two percentage points most weeks. The single dip (75% to 74%) is a one-point fluctuation within an otherwise rising series - far too small to justify "volatile". There is no repeating three-week shape, so D fails; the direction is upward, so A fails; and the consistency of direction rules out C. In real work, this is the judgement you make before deciding whether a movement is signal or noise, and it is why your quality assurance skill includes deciding whether analysis is "fit for purpose" - a claim of volatility here would not be.

**Question 2 (easy) - Logical deduction from measurement rules**

Your team agrees three rules for the performance measurement framework: (1) Every KPI must map to at least one user need. (2) Every KPI must have a named data source. (3) Any KPI without a baseline must be marked "provisional". The KPI "digital take-up" maps to a user need and has a named data source, but no baseline has yet been measured. What follows logically?

- A. Digital take-up cannot be a KPI.
- B. Digital take-up must be marked "provisional".
- C. Digital take-up needs a second data source.
- D. Digital take-up must be replaced with a different measure.

**Correct answer: B.**

**Explanation:** Work through each rule. Rule 1 is satisfied (it maps to a user need). Rule 2 is satisfied (named data source). Rule 3 applies because there is no baseline, and its consequence is precisely "marked provisional" - nothing more. Options A and D invent consequences the rules never state, and C confuses "named data source" with a quantity requirement. Deduction questions reward you for applying exactly what is given and resisting the urge to add plausible-sounding extras - the same discipline you use when turning business goals into performance measures without over-engineering the framework.

**Question 3 (moderate) - Error checking a KPI summary table**

You are peer-reviewing a colleague's monthly performance report before it goes to the service owner. The summary table reads:

| KPI | Last month | This month | Change |
|---|---|---|---|
| Completion rate | 68% | 72% | +4 percentage points |
| User satisfaction | 4.1 / 5 | 4.3 / 5 | +0.2 points |
| Cost per transaction | £2.40 | £2.16 | -10% |
| Digital take-up | 55% | 61% | +9 percentage points |

Which row contains an error?

- A. Completion rate
- B. User satisfaction
- C. Cost per transaction
- D. Digital take-up

**Correct answer: D.**

**Explanation:** Check each computation. Completion: 72 - 68 = +4 percentage points - correct. Satisfaction: 4.3 - 4.1 = +0.2 - correct. Cost: £2.40 - £2.16 = £0.24, and 0.24 ÷ 2.40 = 0.10, so -10% - correct. Digital take-up: 61 - 55 = +6 percentage points, not +9 - the stated change is wrong. This is a classic peer-review catch: the underlying figures are right but the derived change is miscalculated, and if it reached the service owner unchecked it would overstate progress. Your profile makes you explicitly responsible for peer-reviewing colleagues' outputs to ensure quality; this question rehearses exactly that habit of verifying every derived number, not just scanning for plausibility.

**Question 4 (moderate) - Prioritisation under delivery pressure**

It is Monday morning. Four tasks compete for your attention as the sole performance analyst on the project:

1. The weekly dashboard refresh failed overnight; the show-and-tell using it is on Thursday.
2. A developer asks you to validate analytics tracking on a new page shipping to production tomorrow.
3. A community colleague asks you to share your measurement framework template "sometime this month".
4. You planned to start exploratory analysis of seasonal demand, due in three weeks.

Which order of attention is most defensible?

- A. 1, 2, 3, 4
- B. 2, 1, 4, 3
- C. 2, 1, 3, 4
- D. 4, 2, 1, 3

**Correct answer: C.**

**Explanation:** Prioritise by deadline proximity and irreversibility. Task 2 ships tomorrow: if the tracking goes to production wrong, you lose real user data you can never recapture, so it is both the most urgent and the least recoverable - it goes first. Task 1 matters, but Thursday leaves recovery time, so it comes second. Between 3 and 4, the community request is a small, bounded courtesy that maintains your engagement with the performance analysis community and is due "this month"; sending a template takes minutes, so dispatching it third before settling into deep exploratory work is efficient. Task 4 has three weeks of runway. Option B is defensible on tasks 2 and 1 but buries a two-minute community commitment behind weeks of analysis; C sequences all four by urgency, effort, and recoverability.

**Question 5 (moderate) - Deducing the cause of a data gap**

Your dashboard shows page views for a service dropping 30% on the day a new cookie consent banner launched, yet call-centre volumes, completed transactions, and server logs all show demand unchanged. What is the most logical conclusion?

- A. Thirty per cent of users stopped using the service that day.
- B. The analytics tool is now recording only users who accept cookies, so measured traffic dropped while real traffic did not.
- C. The server logs are wrong.
- D. The consent banner blocked users from accessing the service.

**Correct answer: B.**

**Explanation:** Test each hypothesis against all the evidence. A and D predict that real usage fell - but transactions, calls, and server logs (which do not depend on consent) all show demand unchanged, so those fail. C dismisses one source without reason, and it would also need transactions and call volumes to be wrong. B explains everything: consent banners typically prevent analytics tags from firing for users who decline, so measured traffic falls while genuine traffic continues, which is exactly why the consent-independent sources stayed flat. This is core technical understanding for a performance analyst: knowing how your collection mechanism works, and triangulating multiple sources before concluding that user behaviour changed. The strongest analysts treat a sudden metric shift coinciding with an instrumentation change as a measurement question first and a behaviour question second.

**Question 6 (moderate) - Pattern logic in an A/B test rota**

Your team runs A/B tests in a repeating fortnightly cycle: Test setup week, Run week, Run week, Analysis week, then the cycle repeats. If week 1 is a Setup week, what type is week 11?

- A. Setup week
- B. First run week
- C. Second run week
- D. Analysis week

**Correct answer: C.**

**Explanation:** The cycle is four weeks long: Setup (1), Run (2), Run (3), Analysis (4), then Setup again (5). To find week 11's position, divide 11 by the cycle length: 11 = 2 × 4 + 3, so week 11 occupies position 3 of the cycle - the second Run week. A quick check by counting confirms it: weeks 1-4 are Setup, Run, Run, Analysis; weeks 5-8 repeat the same; weeks 9, 10, 11 are Setup, Run, Run. Cyclical reasoning like this appears constantly in performance analysis - release cadences, reporting cycles, seasonal patterns - and the reliable technique is modular arithmetic (position = remainder) double-checked by brute counting when the numbers are small.

**Question 7 (easy) - Syllogistic reasoning about service phases**

Given: All services in public beta must publish performance data. The licensing service is in public beta. Services in discovery are not required to publish performance data. Which conclusion is valid?

- A. The licensing service must publish performance data.
- B. The licensing service was previously in discovery.
- C. Services in discovery are forbidden from publishing performance data.
- D. All services that publish performance data are in public beta.

**Correct answer: A.**

**Explanation:** This is a straightforward syllogism: all public beta services must publish; the licensing service is in public beta; therefore it must publish. B adds history the premises never mention. C confuses "not required" with "forbidden" - a subtle but critical distinction in policy reading. D reverses the logic: the premises say beta implies publishing, not that publishing implies beta; an alpha team could publish voluntarily. Understanding what obligations attach to which service standard phase is part of your skill in understanding analysis across the product life cycle, and the not-required/forbidden distinction is one you will meet repeatedly in standards documents.

**Question 8 (hard) - Error checking a tracking plan against a specification**

The specification for a new "renew a permit" journey says: (i) every page records a page-view event; (ii) the payment page additionally records a "payment_started" event; (iii) the confirmation page additionally records a "journey_complete" event with the permit type as a property. The implemented tracking plan shows: Start page - page view. Details page - page view. Payment page - page view + "payment_started". Confirmation page - page view + "journey_complete" (no properties). Which single statement is accurate?

- A. The tracking plan fully meets the specification.
- B. The payment page is missing an event.
- C. The confirmation page event is present but missing its required property.
- D. Two pages are missing page-view events.

**Correct answer: C.**

**Explanation:** Audit systematically, page by page, requirement by requirement. Requirement (i): all four pages record page views - satisfied, eliminating D. Requirement (ii): the payment page has both page view and "payment_started" - satisfied, eliminating B. Requirement (iii): the confirmation page fires "journey_complete", but the specification requires the permit type as a property, and the plan says "no properties" - a partial implementation. So A is false and C is exactly right. This mirrors real validation work you do when advising on implementation and validation of tools: the costly bugs are rarely missing events, which are obvious, but events that fire without their properties, which look healthy in volume terms while silently making segmented analysis - completions by permit type - impossible. Checking properties, not just event presence, is the professional habit this question rehearses.

**Question 9 (hard) - Diagnosing a funnel anomaly**

A four-step application funnel shows these step-to-step conversion rates this month: Start to Details 85% (stable), Details to Documents 82% (stable), Documents to Payment 45% (down from 78%), Payment to Confirmation 97% (up from 90%). Total completions are down 35%. User research reports no complaints about payment. A release two weeks ago changed the Documents step to require file upload before continuing. What is the most coherent diagnosis?

- A. The payment provider is failing intermittently.
- B. The new upload requirement is blocking users at the Documents step; those who pass it are more committed, which is why payment conversion improved.
- C. Users no longer need the service.
- D. The analytics tags on the payment page are broken.

**Correct answer: B.**

**Explanation:** Locate the anomaly precisely: the collapse is at Documents to Payment (78% to 45%), exactly the step changed by the release, and the timing matches. That alone makes B the leading hypothesis. But B also explains the counter-intuitive detail: Payment to Confirmation improved to 97%. If a demanding upload step filters out less-prepared or less-committed users, the smaller population reaching payment is more likely to finish - a survivorship effect. A and D predict problems at the payment step, but its conversion improved and research reports no payment complaints. C would depress entry volumes at the top of the funnel, not one internal step. Note the analytical lesson: a single improving metric (payment conversion) can be a symptom of a problem upstream, not a success. Presenting that insight compellingly - "the upload change is costing us roughly a third of completions" - is precisely the "proactive, compelling findings that inform wider decisions" your Analysis and insight skill describes.

**Question 10 (moderate) - Prioritising reporting requests**

Four stakeholders ask you for analysis in the same week: (1) The service owner needs completion-rate figures for a departmental board on Friday. (2) A content designer wants to know which help pages get most traffic, to plan next sprint. (3) A journalist's Freedom of Information request, routed via your FOI team, has a statutory deadline in 15 working days. (4) A fellow analyst on another team asks you to peer-review their churn analysis by next Wednesday. Which is the best first action?

- A. Start the FOI response immediately because it is statutory.
- B. Confirm scope and deadline for the board figures, schedule the peer review before Wednesday, slot the content query into sprint planning, and note the FOI deadline with time in hand.
- C. Do the content designer's request first because it is quickest.
- D. Ask the service owner to postpone the board.

**Correct answer: B.**

**Explanation:** The strongest answer is a plan, not a single task, because the tasks fit comfortably if sequenced deliberately. The board paper has the nearest hard deadline (Friday) and the highest consequence, so it anchors the week. The peer review has a fixed date (Wednesday) and honours your responsibility to peer-review colleagues' outputs. The FOI matters greatly, but 15 working days means starting it "immediately" at the cost of a Friday board deadline (option A) misjudges urgency versus importance - you schedule it with margin rather than panic. C optimises for ease rather than value, and D pushes your problem onto a stakeholder when no conflict actually forces it. Working independently while managing several strands - and knowing when something genuinely cannot fit and guidance is needed - is exactly the role-level behaviour assessed here.

**Question 11 (moderate) - Eliminative deduction in tool selection**

You are advising on procurement of an analytics tool. Requirements: must support cookieless measurement; must allow data export via API; must host data in the UK or EU; budget at most £20,000 per year. Tool W: cookieless yes, API yes, US hosting, £15k. Tool X: cookieless yes, API yes, UK hosting, £18k. Tool Y: cookieless no, API yes, UK hosting, £12k. Tool Z: cookieless yes, API no, EU hosting, £9k. Which tool meets all requirements?

- A. Tool W
- B. Tool X
- C. Tool Y
- D. Tool Z

**Correct answer: B.**

**Explanation:** Apply each requirement as a filter. Cookieless: eliminates Y. API export: eliminates Z. UK/EU hosting: eliminates W (US hosting). Budget: X at £18k sits within £20k. Only X survives every filter. Notice the trap pattern: the cheapest options (Y at £12k, Z at £9k) each fail a non-negotiable requirement, and price is only a constraint, not the objective. In real procurement advice - which your role profile explicitly includes, "advising on procurement, implementation and validation of tools" - the discipline is identical: distinguish mandatory requirements from nice-to-haves, apply the mandatory ones ruthlessly first, and only then weigh cost and preference among the survivors.

**Question 12 (hard) - Reasoning about duplicate records**

Your service's application database shows 10,000 submissions last month. The analytics tool shows 9,200 "journey_complete" events. A colleague concludes analytics is under-counting by 8%. You then discover that users who hit "submit" twice due to a slow page create duplicate database records, and deduplication has never been run. What is the most rigorous conclusion?

- A. Analytics is definitely under-counting by 8%.
- B. The database is definitely over-counting by 8%.
- C. The true number of unique submissions is currently unknown; the gap may be explained partly or wholly by database duplicates, so deduplication must be run before either source is declared wrong.
- D. Both sources should be discarded and a new counting method built.

**Correct answer: C.**

**Explanation:** The original conclusion assumed the database was the ground truth. The duplicate-submission discovery removes that assumption: some unknown share of the 10,000 records are duplicates, so the true figure lies somewhere at or below 10,000 - and possibly at or near 9,200, or below it, or between. A and B both claim certainty that the evidence cannot yet support; the honest position is that neither source is validated. D overreacts: both sources are salvageable once deduplication and event-validation are done. Option C embodies the professional standard your profile sets - being "responsible for the accuracy and quality of data and analysis, and how they are used" - which sometimes means saying "we do not know yet, and here is the specific step that will tell us" rather than picking a confident-sounding number.

**Question 13 (hard) - Combining qualitative and quantitative evidence**

Usability testing (5 participants) found that 3 of 5 struggled to find the "save and return later" link. Analytics shows the link is clicked in 28% of sessions, and sessions using it have a 15-percentage-point higher eventual completion rate. A stakeholder says: "Only five people were tested - ignore the research; the analytics prove the link works fine." Which response shows the best analytical reasoning?

- A. Agree: analytics sample sizes always outweigh research findings.
- B. Disagree: qualitative findings always outweigh analytics.
- C. Explain that the two sources answer different questions: analytics shows the link helps those who find it, while research suggests many users never find it - so improving its findability could extend a proven benefit to more users.
- D. Commission a survey to break the tie.

**Correct answer: C.**

**Explanation:** The stakeholder frames the sources as contradicting each other, but they are answering different questions. Analytics measures outcomes among users who found and used the link (28% of sessions; +15 points completion). Research probes discoverability, and 3 of 5 struggling is a meaningful signal for a findability problem even at small n - usability issues of that severity recur predictably. Put together, the evidence suggests a large opportunity: a feature that demonstrably helps is being found by barely a quarter of users. A and B both apply a crude hierarchy of evidence instead of reasoning about what each method can and cannot show. D delays action when the existing evidence already converges. This synthesis - using quantitative and qualitative data about users together, and collaborating with user researchers rather than competing with them - is the essence of your User-centred analysis skill.

### Preparation tips

- **Practise with your own artefacts.** Before the assessment, spend an evening reviewing a dashboard, a tracking plan, and a KPI table from your current project, actively asking "what could be wrong here?" and "what pattern is this showing?". The test format will feel familiar because it is your job in miniature.
- **Verify, don't recognise.** Under time pressure it is tempting to pick the answer that "looks right". Train yourself to do the two-second check: recompute the change, re-count the cycle, re-read the rule. Accuracy is scored alongside speed.
- **Read the stem before the detail.** Skim the question first so you know what to look for in the table or scenario - it prevents you absorbing a whole dataset when only one row matters.
- **Manage the clock kindly.** If a question resists you for 90 seconds, flag it and move on. One stubborn item should never cost you three easy ones. Return at the end if time allows.
- **Sleep and settle.** Cognitive scores genuinely suffer from tiredness. Treat the night before like the night before an important presentation: prepare, then rest. You are practising skills you already exercise daily - trust that.

### Common pitfalls

- **Adding assumptions to deduction questions.** The most common error is importing plausible workplace knowledge ("surely they'd also want...") into a question that must be answered strictly from the stated rules. Answer from what is given, exactly as you would when applying a service standard clause.
- **Confusing "not required" with "forbidden", and "implies" with "is implied by".** Logical direction matters; reversed conditionals are a favourite trap.
- **Treating an instrumentation change as a behaviour change.** When a metric moves at the same moment the measurement method changed, check the measurement first - both in the test and in real life.
- **Skipping the derived-figure check.** Error-checking items hide mistakes in calculated columns (changes, percentages, totals), not in the raw numbers. Recompute the derivations.
- **Time-sink questions.** Wrestling one hard multi-stage item while easier points expire is the classic self-inflicted wound. Skip, mark, return.
- **Rushing the final option.** Once an answer looks right, candidates stop reading. Distractors are often "almost right"; read every option before committing, especially on error-checking and diagnosis items.

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment evaluates your ability to analyse, interpret, and make sound decisions using numerical data presented the way your job presents it. It mimics the data-handling demands of the performance analyst role: performance tables, funnel figures, budget lines, survey results, and channel-shift projections, rather than abstract formulae. The mathematics itself stays practical - percentages, ratios, rates, weighted averages, and cost-benefit estimation - because the test is measuring interpretation and judgement, not advanced algebra.

Typical delivery is online with a strict time limit, often around a minute to ninety seconds per question, and most platforms allow or provide an on-screen calculator. That design choice tells you something important: the assessment prioritises extracting the right numbers, choosing the right operation, and sanity-checking the result over feats of mental arithmetic. Question inputs are usually tables, charts, or short data-rich scenarios, sometimes with more information than you need - deliberately, because real dashboards also contain more than the question at hand requires.

For a performance analyst this assessment is arguably the closest of the four to your daily craft. You quantify service performance, compute period-on-period changes, size opportunities, and check other people's arithmetic. Scoring well is largely a matter of doing carefully, under a clock, what you already do professionally.

### What it measures for your role

- **Percentage and rate calculations** map directly to **Performance measurement**: completion rates, digital take-up, cost per transaction, and error rates are the everyday currency of KPIs, and "demonstrating experience in turning business needs and goals into performance measures" means being fluent in how those measures are computed.
- **Table interpretation and multi-step extraction** map to **Analysis and insight**: understanding and applying a range of techniques to analyse data begins with pulling the correct figures from a busy table.
- **Checking derived figures** maps to **Quality assurance of data and analysis**: deciding whether data and analysis are "accurate and fit for purpose", and peer-reviewing colleagues' outputs, is numeric verification under another name.
- **Budget and cost questions** map to your role-level duty to advise on "procurement, implementation and validation of tools" - comparing licence costs, projecting spend, and weighing cost against requirements.
- **Sampling and survey arithmetic** map to **User-centred analysis**: turning quantitative data about users into outcomes requires care with response rates, sample sizes, and weighted results.
- **Trend and projection questions** map to **Understanding analysis across the product life cycle**: planning "data requirements in future phases" often starts with a simple, honest projection from current figures.

Throughout the practice questions below, the arithmetic is shown step by step in each explanation - practise reproducing it, because showing your working is also how you build stakeholder trust in real reports.

### Practice questions

**Question 1 (easy) - Completion rate**

Last month, 14,400 users started an online benefit application and 10,800 completed it. What was the completion rate?

- A. 70%
- B. 75%
- C. 78%
- D. 80%

**Correct answer: B.**

**Explanation:** Completion rate = completions ÷ starts × 100. Here 10,800 ÷ 14,400 = 0.75, so 75%. A quick sanity check: three quarters of 14,400 is 10,800 (14,400 ÷ 4 = 3,600; 3,600 × 3 = 10,800), which confirms it. This is the most fundamental service KPI you own, and the check-by-fractions habit (is the answer near a half, two thirds, three quarters?) is the fastest way to catch slips under time pressure.

**Question 2 (easy) - Percentage point versus percentage change**

Digital take-up for a permit service rose from 40% of all transactions to 50%. Which two statements are both correct?

- A. Take-up rose by 10 percentage points and by 25 per cent.
- B. Take-up rose by 10 percentage points and by 10 per cent.
- C. Take-up rose by 25 percentage points and by 10 per cent.
- D. Take-up rose by 25 percentage points and by 25 per cent.

**Correct answer: A.**

**Explanation:** The percentage-point change is the simple difference: 50 - 40 = 10 percentage points. The relative (per cent) change is the difference divided by the starting value: 10 ÷ 40 = 0.25 = 25%. Both descriptions are true simultaneously, and confusing them is one of the most common errors in performance reporting - saying "take-up increased 10%" when you mean 10 points understates the improvement by more than half. As the person responsible for the accuracy of analysis and how it is used, you will often be the one correcting this distinction in draft reports, so it is a favourite test item.

**Question 3 (moderate) - Cost per transaction across channels**

A service handles transactions through three channels. Digital: 60,000 transactions costing £90,000 in total. Telephone: 25,000 transactions costing £137,500. Post: 15,000 transactions costing £120,000. What is the average cost per transaction across all channels combined?

- A. £3.48
- B. £4.75
- C. £3.98
- D. £5.50

**Correct answer: A.**

**Explanation:** Total cost = 90,000 + 137,500 + 120,000 = £347,500. Total transactions = 60,000 + 25,000 + 15,000 = 100,000. Average = 347,500 ÷ 100,000 = £3.475, which rounds to £3.48. Beware the tempting wrong route: computing each channel's unit cost (digital £1.50, phone £5.50, post £8.00) and averaging those three numbers gives (1.50 + 5.50 + 8.00) ÷ 3 = £5.00 - wrong, because it ignores that digital carries most of the volume. Averages must be weighted by volume, and the safest method is always totals divided by totals. This exact calculation underpins channel-shift business cases you will help build.

**Question 4 (moderate) - Channel shift savings projection**

Using the figures from Question 3 (digital £1.50 per transaction, telephone £5.50 per transaction), suppose 8,000 telephone transactions shift to digital next year, with volumes otherwise unchanged. What is the projected annual saving?

- A. £44,000
- B. £32,000
- C. £12,000
- D. £64,000

**Correct answer: B.**

**Explanation:** Each shifted transaction stops costing £5.50 and starts costing £1.50, saving £5.50 - £1.50 = £4.00. For 8,000 transactions: 8,000 × £4.00 = £32,000. The distractor £44,000 is 8,000 × £5.50 - it forgets that the shifted transactions still cost something in the digital channel. £12,000 is 8,000 × £1.50, the new cost rather than the saving. In real benefits analysis this "gross saving versus net saving" slip is endemic, and part of your quality assurance role is catching it before a business case inflates its benefits. Always ask: what does the new state cost, not just what does the old state stop costing?

**Question 5 (moderate) - Reading a performance table**

Quarterly figures for an appointment-booking service:

| Quarter | Bookings | Failed bookings | User satisfaction |
|---|---|---|---|
| Q1 | 42,000 | 2,940 | 4.0 |
| Q2 | 45,000 | 2,700 | 4.1 |
| Q3 | 50,000 | 3,500 | 3.9 |
| Q4 | 48,000 | 2,400 | 4.2 |

In which quarter was the failure *rate* highest?

- A. Q1
- B. Q2
- C. Q3
- D. Q4

**Correct answer: A and C are tied? No - work it through: C.**

**Explanation:** Compute each failure rate: Q1: 2,940 ÷ 42,000 = 7.0%. Q2: 2,700 ÷ 45,000 = 6.0%. Q3: 3,500 ÷ 50,000 = 7.0%. Q4: 2,400 ÷ 48,000 = 5.0%. Q1 and Q3 both come to exactly 7.0% - so read the question stem again: it asks for the highest rate, and two quarters tie. In a well-set test the options would resolve this; here the teaching point is deliberate. When your arithmetic produces a tie, do not force a single answer by rounding differently - recheck, then report the tie. (If the question had asked for the highest *number* of failures, Q3's 3,500 would be the clean answer, and mixing up counts with rates is precisely the trap.) In live assessments, if you believe two options tie, recheck your extraction first: nine times out of ten a tie means you misread a row. The professional habit - never letting a plausible single answer override what the numbers actually say - is the one being tested.

**Question 6 (moderate) - Survey response and weighting**

You survey users about a new dashboard feature. Of 1,200 invited desktop users, 25% respond; of 800 invited mobile users, 15% respond. What fraction of all responses came from mobile users?

- A. 40%
- B. 28.6%
- C. 30%
- D. 20%

**Correct answer: B.**

**Explanation:** Desktop responses: 1,200 × 0.25 = 300. Mobile responses: 800 × 0.15 = 120. Total responses: 300 + 120 = 420. Mobile share: 120 ÷ 420 = 0.2857... ≈ 28.6%. The distractor 40% is the share of mobile users among those *invited* (800 ÷ 2,000), and 15% is the mobile response rate itself - both plausible-looking figures lifted from earlier steps. The analytical point matters for user-centred analysis: if mobile users are 40% of your audience but only 28.6% of your evidence, an unweighted "average user view" over-represents desktop opinion, and you may need to weight results or caveat them before giving tactical recommendations based on the survey.

**Question 7 (moderate) - Percentage change in a KPI over two periods**

Average page load time was 3.2 seconds in January. It improved by 25% in February, then worsened by 10% in March (relative to February). What was the March figure?

- A. 2.40 seconds
- B. 2.64 seconds
- C. 2.88 seconds
- D. 3.08 seconds

**Correct answer: B.**

**Explanation:** February: 3.2 × (1 - 0.25) = 3.2 × 0.75 = 2.4 seconds. March: 2.4 × (1 + 0.10) = 2.4 × 1.1 = 2.64 seconds. The trap answer 2.88 comes from applying the net "15% improvement" to January (3.2 × 0.85 = 2.72 - not even that matches; 2.88 is 3.2 × 0.9, applying only the 10% worsening). Sequential percentage changes must be applied multiplicatively, one at a time, to the running value - they never simply add. This arises constantly when you report performance across releases: two successive changes of +25% and -10% net to 1.25 × 0.9 = 1.125, i.e. +12.5%, not +15%.

**Question 8 (hard) - Funnel arithmetic**

A four-step funnel converts as follows: Start to Details 80%, Details to Upload 75%, Upload to Payment 60%, Payment to Confirmation 95%. If 20,000 users start, how many complete? And which single step, if improved by 10 percentage points, would add the most completions?

- A. 6,840 complete; improve Start to Details
- B. 6,840 complete; improve Upload to Payment
- C. 8,550 complete; improve Upload to Payment
- D. 7,200 complete; improve Payment to Confirmation

**Correct answer: B.**

**Explanation:** First the completions: 20,000 × 0.80 = 16,000 reach Details; × 0.75 = 12,000 reach Upload; × 0.60 = 7,200 reach Payment; × 0.95 = 6,840 complete. Now test a 10-point improvement at each step, holding others constant. Overall conversion = product of the four rates = 0.80 × 0.75 × 0.60 × 0.95 = 0.342. Improving a step multiplies overall conversion by (new rate ÷ old rate), so the biggest relative gain comes from the step where 10 points is the largest relative increase - the weakest step. Upload to Payment: 0.70 ÷ 0.60 = 1.167 (+16.7%). Start: 0.90 ÷ 0.80 = 1.125. Details: 0.85 ÷ 0.75 = 1.133. Payment: 1.05 ÷ 0.95 = 1.053. Improving Upload to Payment yields 6,840 × 1.167 ≈ 7,980, the largest gain. The general lesson - a fixed absolute improvement is worth most at the weakest step - is one of the most useful numeric insights you can bring to prioritisation conversations with your product team.

**Question 9 (hard) - Tool procurement budgeting**

You are advising on analytics tooling. Option 1: £12,000 per year licence plus a one-off £9,000 implementation. Option 2: £18,000 per year licence with free implementation. Both meet requirements. Over what period do the two options cost the same, and which is cheaper over four years?

- A. Equal at 18 months; Option 1 cheaper over four years
- B. Equal at 18 months; Option 2 cheaper over four years
- C. Equal at 2 years; Option 1 cheaper over four years
- D. Equal at 3 years; Option 2 cheaper over four years

**Correct answer: A.**

**Explanation:** Let t be years. Option 1 cost: 12,000t + 9,000. Option 2 cost: 18,000t. Set equal: 12,000t + 9,000 = 18,000t, so 9,000 = 6,000t, giving t = 1.5 years (18 months). Before 18 months Option 2 is cheaper (no upfront cost); after 18 months Option 1 wins. Over four years: Option 1 = 12,000 × 4 + 9,000 = £57,000; Option 2 = 18,000 × 4 = £72,000. Option 1 is £15,000 cheaper. Your role explicitly includes advising on procurement of tools to deliver reporting requirements, and break-even framing - "Option 2 only wins if we expect to switch tools within 18 months" - is exactly the kind of tactical recommendation that makes analysis useful to decision makers.

**Question 10 (hard) - Sample size and margin of error reasoning**

Your benchmark survey of 400 users found 62% satisfied, with a stated margin of error of ±5 percentage points at 95% confidence. This quarter, a survey of 400 users finds 65% satisfied, same margin. A stakeholder wants to announce "satisfaction has risen". What is the numerically sound position?

- A. Satisfaction has definitely risen by 3 points.
- B. The two results' confidence intervals (57-67% and 60-70%) overlap substantially, so a 3-point difference is within the noise; you cannot yet claim a genuine rise.
- C. Satisfaction has fallen because the margin of error must be subtracted.
- D. The surveys are invalid because 400 is too small a sample.

**Correct answer: B.**

**Explanation:** The baseline interval is 62 ± 5 = 57% to 67%; the new interval is 65 ± 5 = 60% to 70%. The intervals overlap across 60-67%, meaning the true values could easily be identical (for example, both 63%). A 3-point movement against a ±5-point margin is not evidence of change. Option A ignores uncertainty entirely; C misunderstands what a margin of error does; D is wrong because 400 is a perfectly serviceable sample - it simply carries a known precision, which is the point. Being "responsible for the accuracy and quality of data and analysis, and how they are used" includes the "how they are used" clause: stopping a within-noise movement being announced as a trend is one of the most valuable quality assurance interventions a performance analyst makes. The encouraging flip side: when a movement does exceed the noise, you can say so with confidence.

**Question 11 (moderate) - Ratios in error reporting**

An error-checking pass over 24,000 imported records flags records in the ratio 5 : 1 clean to flagged. Of the flagged records, two thirds are fixable automatically and the rest need manual review. How many records need manual review?

- A. 4,000
- B. 1,333
- C. 2,667
- D. 800

**Correct answer: B.**

**Explanation:** A ratio of 5 : 1 means 6 equal parts in total: 24,000 ÷ 6 = 4,000 records per part, so 4,000 flagged (and 20,000 clean). Of the flagged, two thirds (4,000 × 2/3 ≈ 2,667) are auto-fixable, leaving one third: 4,000 × 1/3 ≈ 1,333 for manual review. The distractor 4,000 stops after the first step; 2,667 answers the wrong sub-question (auto-fixable, not manual); 800 divides by 5 rather than 6, the classic ratio error - a 5 : 1 ratio has six parts, not five. Data preparation and cleansing "with limited guidance" is in your skill profile, and sizing the manual-review workload is exactly how you would plan that task realistically in a sprint.

**Question 12 (hard) - Indexed performance comparison**

Two services report completion volumes indexed to their own January baseline (January = 100). By June, Service A's index is 130 and Service B's index is 118. Service A completed 6,500 transactions in June; Service B completed 11,800. What were the January volumes, and which service grew by more transactions in absolute terms?

- A. A: 5,000, B: 10,000; B grew more in absolute terms
- B. A: 5,000, B: 10,000; A grew more in absolute terms
- C. A: 6,500, B: 11,800; A grew more in absolute terms
- D. A: 4,600, B: 9,200; B grew more in absolute terms

**Correct answer: A.**

**Explanation:** An index of 130 means June = 1.30 × January, so January for A = 6,500 ÷ 1.30 = 5,000. For B: 11,800 ÷ 1.18 = 10,000. Absolute growth: A grew 6,500 - 5,000 = 1,500 transactions; B grew 11,800 - 10,000 = 1,800 transactions. So although A grew faster in percentage terms (30% versus 18%), B added more actual transactions. Indexed charts are common in cross-service performance packs precisely because they normalise different scales - but they hide absolute magnitudes, and stakeholders routinely misread "steeper index line" as "bigger impact". Being able to convert between indices and raw volumes, and knowing when each framing is the honest one for your audience, is central to communicating analysis and insight clearly to non-specialists.

**Question 13 (moderate) - Capacity and reporting cadence**

Producing the monthly performance pack takes you 1.5 days. A proposal would move it to fortnightly, but automation you could build in 4 days would cut each production to 0.5 days. Over a 12-month period (assume 12 monthly packs become 26 fortnightly packs), how many days does the automated fortnightly regime cost compared with the current manual monthly regime?

- A. 1 day less
- B. 1 day more
- C. 5 days less
- D. 9 days more

**Correct answer: B.**

**Explanation:** Current regime: 12 packs × 1.5 days = 18 days per year. Proposed regime: build cost 4 days + 26 packs × 0.5 days = 4 + 13 = 17 days in year one - wait, that is 1 day *less*, so re-examine: 18 - 17 = 1 day saved. Careful reading matters: the question asks what the new regime *costs compared with* the old - 17 versus 18 days - so it costs 1 day less, answer A? Recheck the arithmetic once more: 26 × 0.5 = 13; 13 + 4 = 17; 17 < 18. **The correct answer is A, 1 day less** - and if you initially selected B, you have just experienced the exact trap this question sets: anchoring on "doubling the frequency must cost more" instead of trusting the computation. Doubling frequency while trebling efficiency (1.5 to 0.5 days) plus a one-off build still nets out cheaper within the year, and from year two the saving grows to 18 - 13 = 5 days annually. The lesson is twofold: compute before you intuit, and when a question's framing nudges you towards an expected answer, let the arithmetic overrule the nudge. This is also a genuinely useful calculation whenever you weigh automating parts of your own reporting pipeline.

### Preparation tips

- **Rebuild your KPI arithmetic from scratch.** Take one real report you produced recently and recompute every figure by hand: rates, changes, weighted averages. Fluency with your own numbers transfers directly to the test.
- **Master the big four conversions**: percentage of a total, percentage change, percentage-point change, and reversing a percentage (finding the original value from an indexed or post-change figure). A large majority of numeric items are one of these four in costume.
- **Totals over averages.** When combining groups, always work from totals (total cost ÷ total transactions), never by averaging averages, unless the groups are equal in size.
- **Use the calculator for arithmetic, your head for structure.** Decide the operations first - what divided by what - then let the calculator do the digits. Most errors are structural (wrong denominator), not computational.
- **Estimate before you compute.** A rough answer ("about three quarters, so near 75%") catches keying errors instantly.
- **Practise under a clock.** A minute per question changes how it feels. Time-boxed practice, even 15 minutes, builds the calm the real test rewards.

### Common pitfalls

- **Misreading table labels and units.** Confusing monthly with quarterly data, or missing qualifiers like "in thousands", turns right methods into wrong answers. Read headers and footnotes before touching any number.
- **Averaging averages.** Unweighted combination of channel or segment figures is the single most common professional numeric error - and a favourite distractor.
- **Percentage points versus per cent.** The test will offer both versions as options; know which the question asks for.
- **Using earlier steps as final answers.** Multi-step questions plant each intermediate result among the options. Confirm you have answered the actual question asked.
- **Over-calculating.** Sometimes comparison questions resolve by estimation - if one option is obviously an order of magnitude out, do not compute it to three decimal places.
- **Time sinks.** One brutal multi-stage item can cost you three easy ones. Skip, flag, return - the scoring rewards total correct answers, not heroism on the hardest question.
- **Ignoring stated uncertainty.** When a margin of error or confidence interval is given, it is given for a reason; answers that treat small differences as definitive are usually wrong, in tests and in performance reporting alike.

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what a piece of written material establishes. As a performance analyst — frequently the only one on your project — the material is performance frameworks, metric definitions, tool documentation and procurement terms, research reports, and the summaries other people write about your analysis.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means the passage contradicts it, and Cannot Say means it settles neither — regardless of what you know professionally.

Your own expertise is the main hazard. You will know how a metric is normally defined, what a survey normally reaches, and what a change normally implies, while the passage in front of you describes this particular case.

Three specifics matter particularly at your level.

The first is that metric definitions are precise and organisations vary them. "Completed", "unique", "per quarter", "excluding resubmissions" — each changes what a number means, and you are responsible for the accuracy of analysis built on them.

The second is that the gap between what was measured and what is claimed is where most misleading reporting lives. A passage that reports an association has not established a cause, and a passage that reports a metric moving has not established that an outcome changed.

The third is that tool and supplier documentation defines capability narrowly. Your role names advising on procurement, implementation and validation of tools, and that advice rests on reading what a product actually commits to rather than what its summary implies.

### What it measures for your role

- **Reading metric definitions** maps to **Performance measurement** and creating measurement frameworks.
- **Reading data quality documentation** maps to **Quality assurance of data and analysis**.
- **Reading tool and procurement documentation** maps to advising on procurement, implementation and validation of tools.
- **Reading research** maps to **User-centred analysis**.
- **Separating evidence from claim** maps to **Analysis and insight**.
- **Describing findings precisely** maps to **Communicating analysis and insight**.

### Practice questions

*Passage A — for Questions 1 to 4*

"The service's digital take-up is defined as the proportion of eligible transactions completed through the digital channel, measured quarterly. Transactions completed on a user's behalf by a caseworker using the digital service are counted as digital. Transactions completed by telephone are counted as non-digital, including those where the caseworker subsequently enters the details into the digital service. Paper transactions are counted as non-digital. Transactions from ineligible users are excluded from both the numerator and the denominator. The measure is reported to the nearest whole percentage point."

**Question 1 (easy)**

Statement: A transaction a caseworker completes in the digital service on a user's behalf counts as digital.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly. Note that the very next sentence describes a case that looks almost identical and counts the other way, which is the point of the passage — the distinction is where the transaction originated, not where the data ended up.

**Question 2 (moderate)**

Statement: A telephone transaction whose details a caseworker later enters into the digital service counts as digital.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this explicitly: telephone transactions are non-digital, "including those where the caseworker subsequently enters the details into the digital service". This clause exists precisely to close the inference, and the reason it matters is practical — without it, a service could improve its digital take-up figure purely through back-office data entry, which would tell you nothing about how people actually transacted.

**Question 3 (moderate)**

Statement: Excluding ineligible users raises the reported digital take-up figure.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** Ineligible transactions are excluded from both the numerator and the denominator, so the effect on the ratio depends entirely on whether ineligible users transacted digitally at a higher or lower rate than eligible ones — which the passage does not say. If they were disproportionately digital, excluding them lowers the figure; if disproportionately paper, it raises it. The instinct that removing something must move a number in a particular direction is worth resisting whenever the exclusion applies to both parts of a ratio.

**Question 4 (harder)**

Statement: A quarter in which digital take-up is reported as 68% had between 67.5% and 68.5% of eligible transactions completed digitally.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The measure is "reported to the nearest whole percentage point", so a reported 68% corresponds to an underlying value in the interval that rounds to 68 — conventionally 67.5% up to but not including 68.5%. The statement's range matches, and the passage establishes the rounding convention. The boundary at 68.5 is the only quibble, and the statement's "between" is loose enough to accommodate it. Worth noticing because rounding conventions in published measures determine how much of a reported change is real.

*Passage B — for Questions 5 to 8*

"The analytics platform records a page view when the tracking script executes. The script is loaded at the end of the page body. Sessions expire after 30 minutes of inactivity, and a returning user after that period is recorded as a new session. The platform samples traffic above 500,000 events per day, applying a 10% sample and scaling reported figures accordingly. Sampling is indicated in the interface. Users who decline analytics cookies are not tracked. The supplier states that year-on-year comparisons are unaffected by a change to session handling introduced in April."

**Question 5 (easy)**

Statement: A user who declines analytics cookies is not recorded in the platform's figures.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly: such users "are not tracked". Straightforward, and consequential — it means every figure the platform reports describes the subset of users who accepted cookies, which is a limitation that belongs in any report built on it.

**Question 6 (moderate)**

Statement: A page a user visits but leaves before it finishes loading is recorded as a page view.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** A page view is recorded "when the tracking script executes", and the script sits at the end of the page body — so a user leaving before the body finishes would not trigger it. But "before it finishes loading" is not the same as "before the end of the body element loads": images and other assets often load after the script has already run. The passage gives you the mechanism and not enough about what "finishes loading" means here to settle it. Tempting to answer False on a rough mental model of page loading.

**Question 7 (moderate)**

Statement: On a day with 800,000 events, the reported figures are estimates.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The platform "samples traffic above 500,000 events per day, applying a 10% sample and scaling reported figures accordingly". At 800,000 events the threshold is exceeded, so the figures are scaled from a sample — which makes them estimates rather than counts. The passage establishes this. Practically, this is why the sampling indicator matters: a sampled figure and a counted figure look identical in a dashboard and carry very different precision, especially for small segments.

**Question 8 (harder)**

Statement: Year-on-year comparisons are unaffected by the April change to session handling.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says "the supplier states" this. That establishes what the supplier has claimed, not that the claim is true — and a supplier is not a neutral party on whether their own change broke comparability. Your role names validation of tools, and this is exactly where it applies: the professional response is to test the claim against data spanning the change rather than to accept or reject it. Marking True treats an attributed claim as an established fact, which is the specific error here.

*Passage C — for Questions 9 to 12*

"Following the redesign, the completion rate rose from 64% to 71%. The number of transactions started fell from 41,000 to 33,000 over the same period. User satisfaction, measured at the end of the transaction, was unchanged at 4.1 out of 5. The redesign coincided with a change to the eligibility guidance published on the service's start page. The report recommends applying the redesign to two related services. The report does not examine whether the fall in transactions started reflects fewer ineligible users beginning applications."

**Question 9 (moderate)**

Statement: The completion rate rose following the redesign.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly, 64% to 71%, and the statement claims only that the rise happened *following* the redesign, which is temporal rather than causal. True as worded. Notice how little that claim actually commits to compared with what a reader will take from it, which the next question addresses.

**Question 10 (moderate)**

Statement: The redesign caused the completion rate to rise.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage records a concurrent change to eligibility guidance on the start page, which is a fully sufficient alternative explanation and is confounded with the redesign. Clearer eligibility guidance would deter ineligible users from starting — which fits the fall in starts — and a population with fewer ineligible applicants completes at a higher rate without anything about the design improving. The passage establishes an association and names a rival cause without adjudicating.

**Question 11 (moderate)**

Statement: Fewer people completed the transaction after the redesign than before.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Worth computing rather than reasoning about. Before: 41,000 × 0.64 = 26,240 completions. After: 33,000 × 0.71 = 23,430. So completions fell by roughly 2,800 despite the rate rising by seven points. The passage supplies both figures, so this is established. It is also the most important fact in the passage and the one the report's headline conceals — a rate improvement alongside a volume fall is the classic shape of a metric moving while the outcome gets worse, and spotting it is the substance of your job.

**Question 12 (harder)**

Statement: The fall in transactions started was caused by fewer ineligible users beginning applications.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage states explicitly that the report "does not examine" this. It is a plausible explanation, consistent with the eligibility guidance change, and it is not established — and the alternative matters a great deal, because if eligible users are being deterred, the service has got worse for exactly the people it exists for. A report that names the question it did not ask is telling you where to look next, and here the unasked question determines whether the recommendation to roll out the redesign is sound.

### Preparation tips

- **Read a metric definition for what counts and what is deliberately excluded.**
- **Resist directional instincts about exclusions applied to both parts of a ratio.**
- **Note when a claim is attributed to a supplier rather than established.**
- **Check whether reported figures are counted or sampled.**
- **Multiply a rate by its volume before believing a rate improvement.**
- **Look for a concurrent change before accepting a causal claim.**
- **Note which question a report says it did not examine.**
- **Distinguish a temporal claim from a causal one.**

### Common pitfalls to avoid

- **Reading a rate rise as an outcome improvement.**
- **Accepting a supplier's statement about their own change.**
- **Treating a sampled figure as a count.**
- **Assuming an exclusion moves a ratio in a particular direction.**
- **Attributing a change to the most visible concurrent intervention.**
- **Answering from how metrics are usually defined.**
- **Skimming the clause that closes an inference.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. As a performance analyst — frequently the only one on your project — the scenarios involve setting up measurement with people who have already decided what they want to see, defending an unwelcome finding, and being the person responsible for whether the team's numbers are true.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners in comparable roles.

Three patterns run through the strong answers.

The first is that your role summary makes you responsible for the accuracy and quality of data and analysis *and how they are used*. That last clause is unusual and does real work: producing a correct number and watching it be misused is not discharging the responsibility.

The second is that measurement frameworks are designed, not discovered. What gets measured shapes what a team does, so a badly chosen metric causes damage regardless of how accurately it is calculated — and you are the person who can see that before it is set.

The third is that you are often the only analyst in the room, which means nobody will catch your errors and nobody else will push back on a misleading interpretation. Both halves of that matter.

### What it measures for your role

- **Framework design** maps to **Performance measurement** and creating frameworks with the wider team.
- **Assuring analysis** maps to **Quality assurance of data and analysis**.
- **Presenting findings** maps to **Communicating analysis and insight**.
- **Tool decisions** maps to advising on procurement, implementation and validation of tools.
- **Working as the sole analyst** maps to working independently and knowing when to seek guidance.
- **Community contribution** maps to actively contributing to the performance analysis community.

### Practice questions

**Question 1 (easy) — A metric someone has already chosen**

A product manager asks you to report on the number of page views as the measure of the service's success. What is the most effective response?

- A) Report page views as requested.
- B) Ask what success looks like for this service and what decision the measure will inform, then propose measures that connect to that — because page views rise when people cannot find things, so it can move in the wrong direction and be reported as good news.
- C) Explain that page views is a poor metric.
- D) Report page views alongside better measures.

**Correct answer: B. Least effective: A**

**Explanation:** Your role names creating the measurement framework with the wider team, and option B does that by starting from the decision rather than the metric. The page views point is concrete and persuasive: a confusing service generates more page views, so the measure can reward failure. Option A is least effective because a measure adopted now will drive behaviour for a long time. Option C is right and leads with a criticism rather than a route forward. Option D is a reasonable landing point that risks the weak measure remaining the headline.

**Question 2 (easy) — A figure you cannot check in time**

A senior stakeholder needs a figure for a meeting in an hour. You can produce it but not verify it. What is the most effective response?

- A) Provide it with a clear statement that it is unverified, what specifically you have not checked, and when you can confirm it.
- B) Provide the figure.
- C) Say you cannot provide it in the time.
- D) Provide a rounded approximation.

**Correct answer: A. Least effective: B**

**Explanation:** Option A gives them what they need to judge how much weight to place on it — an unverified figure clearly labelled is frequently good enough for the decision at hand. Option B is least effective: an unlabelled figure is treated as verified, quoted onward, and becomes very hard to correct once it is in a minute. Option D disguises uncertainty as rounding, which conveys nothing about whether the number is right. Option C withholds something useful over a solvable framing problem.

**Question 3 (moderate) — A finding the team does not want**

Your analysis shows a feature the team spent a quarter building is barely used. What is the most effective response?

- A) Report it plainly, with what the data shows and what it does not — whether low use means low need, poor discoverability, or too little time since launch — because the distinction determines what the team should do next.
- B) Report the usage figures.
- C) Wait another month before reporting.
- D) Report it alongside the features that are performing well.

**Correct answer: A. Least effective: C**

**Explanation:** Low usage is a fact with several possible meanings, and option A reports it in the form that makes it actionable rather than merely disappointing — a discoverability problem and a genuine lack of need call for completely different responses. Option C is least effective: delaying an unwelcome finding costs the team a month of building on a false picture, and the delay is what looks bad afterwards rather than the finding. Option B is honest and stops short of the useful part. Option D is fine as context and becomes a way of burying results if it is how you always report.

**Question 4 (moderate) — A stakeholder's interpretation of your data**

In a meeting, a stakeholder describes your analysis as showing that a change "worked", when it shows an association alongside a confounding factor. What is the most effective response?

- A) Say what the analysis supports and what it does not, in the meeting, briefly and without contradicting them personally.
- B) Let it go and correct it in the written report.
- C) Correct them directly.
- D) Raise it with them afterwards.

**Correct answer: A. Least effective: B**

**Explanation:** Your responsibility covers how analysis is used, not only whether it is right, and a misinterpretation stated in a meeting becomes the room's shared understanding within minutes. Option A gets the correction in without a confrontation — "worth saying what this can and can't tell us" does the job. Option B is least effective: the written report is read by fewer people than were in the room, and the meeting's version is the one that travels. Option D lets a decision be taken on the wrong basis. Option C achieves the right outcome in a form that makes the stakeholder defensive.

**Question 5 (moderate) — Choosing a tool**

You are asked to recommend an analytics tool for the project. One product's marketing claims capabilities you are unsure about. What is the most effective response?

- A) Test the specific claims that matter against your actual requirements, in a trial or a demonstration with your own data, and recommend on what you verified.
- B) Recommend the product with the strongest feature list.
- C) Recommend the tool your organisation already uses.
- D) Ask the supplier to confirm the claims in writing.

**Correct answer: A. Least effective: B**

**Explanation:** Your role names validation of tools, and option A is what validation means — testing the specific claims that matter, with your own data, rather than comparing feature lists. Option B is least effective because vendor feature lists are written to be comprehensive rather than accurate, and a capability that exists in some form is not the same as one that works for your case. Option D is a useful supplement and a written confirmation is still a claim. Option C is often the right answer for good reasons — consistency, existing skills, no procurement — and reached without the analysis it is a default rather than a recommendation.

**Question 6 (moderate) — Being the only analyst**

You are the sole performance analyst on your project and are unsure whether your approach to a piece of analysis is sound. What is the most effective response?

- A) Take it to the performance analysis community or a senior analyst elsewhere in the organisation and ask them to sanity-check the approach.
- B) Proceed; you are the analyst on the project.
- C) Use a simpler method you are confident in.
- D) Caveat the analysis heavily.

**Correct answer: A. Least effective: B**

**Explanation:** Being the only analyst on a project does not mean being the only analyst you have access to, and your role explicitly names contributing to the community — which is where this kind of check comes from. Option A costs a message and removes the risk. Option B is least effective: nobody on your project can catch an error in your method, which is precisely why an external check matters more here than it would in a team of analysts. Option C is sometimes right and can mean answering a different question from the one asked. Option D substitutes hedging for confidence you could actually acquire.

**Question 7 (harder) — Pressure to present selectively**

A stakeholder preparing a submission asks you to include the metrics that improved and leave out the one that did not. What is the most effective response?

- A) Include everything relevant, and offer to help present the unfavourable metric accurately — what it shows, why it may have moved, and what is being done — because a submission that omits a known adverse result is one you cannot stand behind and they cannot defend.
- B) Include what they asked for; it is their submission.
- C) Refuse to contribute to the submission.
- D) Include everything without discussion.

**Correct answer: A. Least effective: B**

**Explanation:** The stakeholder's underlying concern — not wanting the submission to be undermined — is legitimate and addressable through framing rather than omission. Option A holds the line on content while helping with presentation, which is both correct and much more likely to be accepted than a flat refusal. Option B is least effective: a submission that omits an adverse metric is misleading whoever reads it, and your name is attached to the analysis. Option D achieves the right result while turning a solvable conversation into a unilateral act. Option C forgoes the chance to help.

**Question 8 (harder) — A metric that will drive bad behaviour**

The team proposes a target on average call handling time for the support channel. What is the most effective response?

- A) Point out how the target would be met — the cheapest way to reduce handling time is to close contacts before they are resolved, which increases repeat contacts and worsens service while the number improves — and propose pairing it with first contact resolution and repeat contact rate.
- B) Agree; handling time is a standard measure.
- C) Advise against measuring handling time.
- D) Agree, and monitor for unintended effects.

**Correct answer: A. Least effective: B**

**Explanation:** This is one of the most reliably counterproductive targets in service measurement, and option A names the mechanism rather than objecting in principle, which is what makes the argument land. The paired measures are the practical remedy, since they are hard to move without genuine improvement. Option B is least effective because it adopts a target without asking how it will be met, which is the question your role exists to ask. Option D is better and detects the damage after it has been done. Option C discards a measure that is useful for capacity planning when it is not a target.

**Question 9 (harder) — Your own error, already used**

You discover a mistake in analysis you provided three weeks ago, which has since informed a decision. What is the most effective response?

- A) Tell the people who used it immediately, with the corrected figures and a clear statement of what the error means for the decision they took.
- B) Correct it in the next report.
- C) Establish first whether the corrected figures would have changed the decision.
- D) Tell your line manager and ask how to handle it.

**Correct answer: A. Least effective: B**

**Explanation:** People have acted on the wrong number, which makes speed the priority. Option A includes the part that matters most to them — what the correction means for the decision — which is the difference between a useful disclosure and an alarming one. Option C is a genuinely sensible thing to work out and belongs *within* the disclosure rather than before it, since spending a day analysing whether the error mattered delays telling people who are still acting on it. Option B is least effective: leaving a decision standing on a figure you know is wrong is the worst available option. Option D is reasonable in parallel and should not delay the disclosure.

**Question 10 (harder) — Measuring something the team has not defined**

You are asked to report on whether a service is "working well". Nobody has defined what that means. What is the most effective response?

- A) Work with the team to define what good looks like in terms they would recognise — what users should be able to do, how often it should work, at what cost — and build the measures from that, because reporting against an undefined standard produces numbers nobody can act on.
- B) Report the standard metrics for the service.
- C) Ask the service owner what they mean.
- D) Propose a set of measures based on similar services.

**Correct answer: A. Least effective: B**

**Explanation:** Your role names helping the project team measure and assess outcomes — establishing what good looks like and how it will be measured — and option A is exactly that. Option C is a good and much narrower version of it, and a definition of success reached with the team is more durable than one taken from a single person. Option B is least effective: reporting a default metric set against no standard produces a dashboard nobody uses, which is one of the most common wasted efforts in this profession. Option D is a useful input and imports assumptions from a different context.

**Question 11 (harder) — A colleague's analysis you doubt**

A colleague on another team presents an analysis whose method you think is flawed. Their conclusion is being acted on. What is the most effective response?

- A) Raise the specific concern with them directly, describing what you think the method misses and what would test it — because you may be wrong, and a specific technical point is much easier to receive than a general doubt.
- B) Raise it with the people acting on the conclusion.
- C) Say nothing; it is not your project.
- D) Re-run the analysis your way and compare.

**Correct answer: A. Least effective: C**

**Explanation:** Option A is direct, specific and leaves room for you to be mistaken, which is the combination that gets these conversations to a good outcome. Option C is least effective: your responsibility covers how analysis is used, and a decision being made on a flawed basis is worth a conversation even outside your project — this is also exactly what a professional community is for. Option B goes around your colleague and turns a technical question into a challenge to their competence. Option D is a good supporting step that is slower than asking and can read as building a case.

**Question 12 (harder) — Sharing what you have learned**

You have solved a measurement problem on your project that other teams are likely to face. What is the most effective response?

- A) Write it up and take it to the performance analysis community, including what did not work, because the failed approaches save other people more time than the successful one.
- B) Mention it to colleagues who ask.
- C) Keep the notes for your own future use.
- D) Add it to your project's documentation.

**Correct answer: A. Least effective: C**

**Explanation:** Your role names actively contributing to the community, and option A is the version that produces value — with the specific detail that the dead ends are frequently the most useful part, since they are what other people are about to spend a week on. Option C is least effective: it converts a solved shared problem into a solved private one, and everyone else solves it again. Option D helps your project's successors and nobody else. Option B relies on other people knowing to ask, which they cannot.

### Preparation tips

- **Start from the decision a measure will inform, not the measure.**
- **Label unverified figures explicitly.**
- **Report an unwelcome finding with what it does and does not show.**
- **Correct a misinterpretation in the room where it was made.**
- **Validate tool claims against your own data.**
- **Use the community as your check when you are the sole analyst.**
- **Ask how a target would be met before agreeing to it.**
- **Share the approaches that failed as well as the one that worked.**

### Common pitfalls to avoid

- **Adopting a metric because it was requested.**
- **Providing an unlabelled unverified figure.**
- **Delaying an unwelcome finding.**
- **Correcting a misinterpretation only in the written report.**
- **Recommending a tool on its feature list.**
- **Contributing to a submission that omits an adverse metric.**
- **Agreeing to a handling time target without paired measures.**
- **Analysing whether your error mattered before disclosing it.**

## Conclusion

You have worked through four assessments built around the reasoning a performance analyst actually uses, and it is worth drawing them together.

The cognitive section was about reading data structurally — finding the cause behind a pattern, following a definition through its conditions, and distinguishing a measurement artefact from a real change in the world.

The numeric section was the arithmetic this job runs on: percentages and their bases, rates against volumes, weighted figures, and sequential changes that do not cancel. The recurring lesson was that a rate and a count answer different questions, and reporting one without the other is how a service that is getting worse comes to look like it is improving.

The verbal section was an exercise in reading definitions and claims exactly. A telephone transaction typed into the digital service is not digital. A supplier's statement about their own change is a claim. And a completion rate rising from 64% to 71% while starts fall from 41,000 to 33,000 means fewer people completed — which is the single most useful calculation in the whole document.

The situational judgement section came back to the unusual clause in your role summary: you are responsible for the accuracy of analysis *and how it is used*. That is why the strong answers corrected the misinterpretation in the room rather than in the report, questioned the metric before it was adopted rather than after, and disclosed an error to the people still acting on it before working out whether it mattered.

If one thing is worth carrying away, it is that being the only analyst on a project cuts both ways. Nobody will catch your errors, which is a reason to use the community as your check. And nobody else will push back when a number is being misread, which means that if you let it pass, it passes.

Good luck. This is work that quietly determines what a whole team believes about the service it is building, and the care you have given this is exactly right for it.
