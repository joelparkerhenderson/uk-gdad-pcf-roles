# Performance Analyst (Senior Performance Analyst) - Psychometric Assessment Resources

## Introduction

Welcome. This document is a practical, encouraging companion for you as a senior performance analyst working within the UK Government Digital and Data (GDAD) profession. It has been designed to help you prepare for, practise, and reflect on the four psychometric assessment types most commonly used for analytical roles at your level: cognitive ability, numeric reasoning, verbal reasoning, and situational judgement.

Psychometric assessments are structured, standardised exercises that measure how you think, reason, and decide. Rather than testing what you already know about a specific tool or dataset, they measure the underlying capabilities that make you effective day to day: spotting patterns in performance data, drawing sound conclusions from dense policy documents, working accurately with percentages and ratios under time pressure, and choosing wise courses of action when stakeholders pull in different directions. Employers use them because they are objective, fair, and strongly predictive of on-the-job performance — and because, for a role like yours, they mirror the real work remarkably closely.

Why do these assessments matter for you specifically? As a senior performance analyst, you lead the development of performance measurement frameworks and Key Performance Indicators (KPIs), you carry out increasingly complex analysis, you assure the quality of data and analysis, and you turn complex data into compelling, clear and actionable stories for stakeholders. You may also manage other performance analysts, contribute to the performance analysis community across your organisation, and forge links with other analytical disciplines. Every one of those responsibilities draws directly on the capabilities these assessments measure. Preparing for them is therefore not just interview preparation — it is genuine professional development.

This document is organised into four main assessment sections, each following the same structure:

- **About this assessment** — what it measures, why it matters for your role, and the typical format and timing.
- **What it measures for your role** — an explicit mapping to the GDAD skills for a senior performance analyst.
- **Practice questions** — realistic, role-specific questions with full scenarios, answer options, correct answers, and worked explanations.
- **Preparation tips** — practical advice tailored to this assessment type and to your seniority.
- **Common pitfalls** — the mistakes candidates most often make, and how to avoid them.

How should you use it? Work through the practice questions honestly, under light time pressure, before reading the explanations. Use the explanations to understand the reasoning, not just to check the answer. Reflect on which question types felt effortless and which felt effortful — that self-knowledge is valuable whether you are sitting an assessment next week or coaching one of your own analysts through one next year. Take your time, be kind to yourself, and treat every question as a small rehearsal of the real job.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive ability assessment is a targeted psychometric test that measures the exact mental processes needed for your role — not abstract intelligence, but applied thinking. Unlike a generic IQ test, it uses practical workplace scenarios and data formats drawn from the everyday work of a senior performance analyst: dashboards, KPI frameworks, analytics reports, data pipelines, and service performance reviews. The purpose is to predict how well you will reason, prioritise, diagnose, and solve problems when confronted with the real artefacts of your job.

Typical format and timing: these assessments are usually delivered online and timed, most commonly 15 to 30 minutes for 20 to 30 questions. You will normally receive short, ungraded practice questions first so you can get comfortable with the interface. Some modern platforms are adaptive, adjusting question difficulty based on your previous answers, so do not be alarmed if the questions seem to get harder — that often means you are doing well. Scoring is objective: your results are compared against a benchmark or norm group, and many employers receive a breakdown of speed versus accuracy rather than a single number.

For a senior performance analyst, the cognitive assessment matters because your role is fundamentally about structured thinking under complexity. You design measurement frameworks that must be logically coherent. You diagnose why a KPI has moved — separating genuine service change from tracking faults, seasonality, or data quality issues. You check other analysts' work for errors before it reaches decision-makers. You prioritise competing analytical requests from multiple teams. A cognitive assessment simply compresses those daily demands into a short, standardised exercise.

### What it measures for your role

Each cognitive dimension maps directly onto the GDAD skills defined for your role:

- **Pattern recognition and logical deduction** map to your **Analysis and insight** skill: understanding and helping teams apply a range of techniques to analyse data and provide insight, and applying innovative approaches to resolve problems. Spotting that a weekly completion-rate series has a structural break, or deducing which pipeline stage introduced an anomaly, is pattern recognition in action.
- **Error checking** maps to your **Quality assurance of data and analysis** skill: specifying how data should be cleansed and prepared, bringing data together from different sources, and communicating the limitations of data. As a technical specialist senior performance analyst, you are responsible for the accuracy and quality of data and analysis — error checking is the cognitive core of that responsibility.
- **Prioritisation and problem solving** map to your **Understanding analysis across the product life cycle** skill: recognising when to move forward and when to stop, recognising the appropriate deliverables, and identifying which tools and techniques should be used at each stage.
- **Systems thinking** maps to your **Technical understanding** skill: showing a deep understanding of technical concepts and how they fit into the wider technical landscape, including the limitations of digital technology.
- **Framework logic** maps to your **Performance measurement** skill: leading the development of KPI frameworks and turning business goals into tangible performance measures — which demands rigorous deductive reasoning about what a metric can and cannot tell you.

### Practice questions

Work through each question before reading the answer. Note the difficulty labels — a well-designed assessment mixes levels, and so does this set.

**Question 1 (easy) — Pattern recognition in a KPI series**

You are reviewing weekly digital take-up figures for a licence renewal service. The percentage of renewals completed online over eight consecutive weeks is: 62%, 64%, 66%, 68%, 70%, 72%, 61%, 63%. Assuming the underlying pattern before week 7 continues in parallel after the disruption, which is the most reasonable expectation for week 9?

- A) 74%
- B) 65%
- C) 61%
- D) 71%

**Correct answer: B) 65%.**

**Explanation:** Weeks 1-6 show a steady rise of 2 percentage points per week. Week 7 drops sharply by 11 points to 61%, and week 8 resumes the +2 pattern from the new, lower base (61% to 63%). The most defensible short-term expectation is that the +2 trend continues from the new base: 63% + 2 = 65%. Option A assumes the disruption never happened; option C assumes the trend has stopped; option D has no basis in the series. In real work, your next step would be to investigate the week 7 step change — a tracking tag failure, a channel shift, or a policy change — before publishing any forecast. The cognitive skill being tested is your ability to separate trend from disruption, exactly what you do when assuring a KPI series.

**Question 2 (easy) — Logical deduction about metric definitions**

Your team's measurement framework states: "All KPIs must map to at least one business goal. All business goals must have at least one KPI. Some KPIs are also health metrics, but no health metric may be reported to the programme board." A colleague proposes reporting the KPI "median transaction completion time" to the programme board. Which single fact would make this proposal non-compliant with the framework?

- A) The KPI maps to two business goals rather than one.
- B) The KPI is also classified as a health metric.
- C) The business goal it maps to has three other KPIs.
- D) The KPI is measured weekly rather than monthly.

**Correct answer: B.**

**Explanation:** The framework's only prohibition on board reporting is that "no health metric may be reported to the programme board". If the KPI is also a health metric, reporting it would breach that rule. Option A is compliant ("at least one" permits more). Option C is compliant for the same reason. Option D concerns frequency, about which the framework says nothing. This is a pure deduction exercise: apply the stated rules exactly, adding nothing. When you lead the development of performance measurement frameworks, this kind of precise rule-application is what keeps governance clean.

**Question 3 (moderate) — Error checking a data pipeline output**

You have specified a cleansing rule: "Remove sessions with duration under 2 seconds; deduplicate on session ID; then join to the survey table on session ID." An analyst on your team runs the pipeline and reports: raw sessions 84,200; after duration filter 79,950; after deduplication 81,100; after join 61,300 rows. Which figure is logically impossible?

- A) 79,950 after the duration filter
- B) 81,100 after deduplication
- C) 61,300 after the join
- D) None — all figures are possible

**Correct answer: B.**

**Explanation:** Deduplication can only remove rows or leave the count unchanged; it can never increase a row count. Going from 79,950 to 81,100 is therefore impossible if the steps ran in the stated order. The duration filter reducing 84,200 to 79,950 is plausible (about 5% short sessions). The join reducing rows to 61,300 is plausible if it is an inner join and not every session has a survey response. The likely real-world causes are steps run out of order, a join accidentally executed before deduplication, or a many-to-many join inflating rows. As the person responsible for the accuracy and quality of data and analysis, spotting "impossible numbers" quickly — before stakeholders do — is one of your most valuable habits.

**Question 4 (moderate) — Prioritisation under competing demands**

It is Monday morning. Four requests are in your queue:

1. The head of performance analysis needs your input to the quarterly strategy pack by Thursday.
2. A product manager reports that yesterday's dashboard shows zero transactions — almost certainly a tracking failure that is currently losing data.
3. A junior analyst you manage has asked for a 30-minute review of their first funnel analysis, due to be presented Wednesday.
4. Another department has asked you to speak at a performance analysis community session in three weeks.

Which order of action is most cognitively sound for today?

- A) 1, 2, 3, 4
- B) 2, 3, 1, 4
- C) 2, 1, 3, 4
- D) 3, 2, 4, 1

**Correct answer: B.**

**Explanation:** Request 2 is the only item where delay causes irreversible harm: while tracking is broken, data is being lost permanently, and every hour matters. It comes first. Request 3 has the next-nearest hard deadline (Wednesday) and is quick (30 minutes), and unblocking someone you manage multiplies team output — a senior analyst delegates and upskills, so investing in the junior analyst early is both efficient and good leadership. Request 1 is important but has runway until Thursday and benefits from a clear head after the urgent fire is out. Request 4 is genuinely valuable community contribution but is weeks away. Option C is defensible but delays a cheap, high-leverage unblock; options A and D leave data loss running. The tested skill is triage: distinguishing urgency (irreversibility) from importance (impact).

**Question 5 (moderate) — Diagnosing a metric anomaly**

A service's "user satisfaction" KPI dropped from 82% to 71% in one week. You establish four facts: (i) the survey invitation was moved from the confirmation page to a follow-up email on Monday; (ii) survey response volume fell from 1,900 to 400; (iii) the service itself had no releases that week; (iv) complaint volumes to the call centre were flat. What is the most logical primary hypothesis?

- A) Service quality genuinely deteriorated.
- B) The change in survey placement altered who responds, so the two weeks are not comparable.
- C) The call centre is suppressing complaints.
- D) Random variation fully explains the drop.

**Correct answer: B.**

**Explanation:** Fact (i) is a measurement change that coincides exactly with the KPI movement, and fact (ii) shows the respondent population collapsed by nearly 80% — a classic selection-effect signature, since people who respond to a follow-up email differ systematically from people who respond in the moment of completion. Facts (iii) and (iv) both argue against a genuine quality change: nothing shipped, and no complaint signal corroborates deterioration. Option D is weak because a fall from 82% to 71% on 400 responses is possible noise, but the coincident methodology change is a far stronger explanation and must be ruled out first. This is user-centred analysis discipline: integrate the quantitative signal with knowledge of how the data is collected, and communicate the limitations of the data before anyone acts on it.

**Question 6 (moderate) — Framework logic**

A business goal states: "Reduce avoidable contact to the call centre." Which of the following is the strongest KPI to turn this goal into a tangible performance measure?

- A) Total calls received per month
- B) Calls per 1,000 completed digital transactions, segmented by call reason
- C) Call centre staff utilisation percentage
- D) Number of digital transactions per month

**Correct answer: B.**

**Explanation:** The goal has two components: contact volume and avoidability. Option B normalises calls against service demand (so growth in users does not masquerade as failure) and segments by reason (so you can isolate avoidable contact — "where is my application?" — from unavoidable contact). Option A confounds demand growth with performance: total calls could rise simply because more people use the service. Option C measures workforce efficiency, not user behaviour. Option D measures digital uptake but says nothing about contact. Turning business goals into tangible, decision-ready measures is the heart of your performance measurement skill, and the reasoning here — normalise, segment, align to the goal's actual wording — is the pattern to internalise.

**Question 7 (hard) — Multi-step logical deduction across data sources**

You bring together three data sources for a cross-government report:

- Source X (web analytics): sessions and completions, updated daily, excludes users who decline cookies (roughly 20% of users).
- Source Y (case management system): all completed applications, updated weekly on Fridays.
- Source Z (user survey): satisfaction, collected continuously, but only from users who completed.

On Wednesday, a director asks: "What proportion of people who started an application this week abandoned it, and were the abandoners dissatisfied?" Which statement is correct?

- A) You can answer both parts accurately from the three sources.
- B) You can estimate starts and completions with known limitations, but you cannot measure abandoners' satisfaction at all from these sources.
- C) You can measure abandoners' satisfaction from Source Z but not abandonment volume.
- D) You cannot answer any part of the question until Friday.

**Correct answer: B.**

**Explanation:** Work through each part deductively. Abandonment estimate: Source X gives starts and completions daily, so a mid-week estimate is possible — but it excludes the roughly 20% who decline cookies, so it is an estimate with a known coverage limitation, and Source Y cannot help mid-week because it updates on Fridays. Abandoners' satisfaction: Source Z surveys only users who completed, so by construction it contains zero abandoners; no analysis of Z can ever describe them. Option A ignores both limitations. Option C reverses the logic — Z is precisely the source that cannot describe abandoners. Option D is too pessimistic: partial, caveated answers are available now. The professional move, matching your quality assurance skill, is to give the director the caveated abandonment estimate immediately, state plainly that abandoners' satisfaction is unmeasurable with current instruments, and propose an exit survey or user research to close the gap.

**Question 8 (hard) — Spotting the flaw in an analytical argument**

A performance analyst on your team presents this argument: "Users who watch the tutorial video complete their application at 91%, versus 74% for users who do not. Therefore, making the video mandatory will raise overall completion to roughly 91%." What is the primary logical flaw?

- A) The sample sizes are not stated.
- B) The argument assumes correlation implies causation — motivated users may both watch the video and complete at higher rates.
- C) The percentages should be medians, not means.
- D) Completion rate is the wrong metric for a tutorial video.

**Correct answer: B.**

**Explanation:** The comparison is between self-selected groups. Users who voluntarily watch a tutorial are plausibly more motivated, more digitally confident, or further along in intent — characteristics that would raise their completion rate whether or not the video helps. Forcing everyone to watch the video does not transfer those characteristics, and could even add friction that lowers completion. Option A is a fair secondary critique but not the primary flaw — even with enormous samples the selection problem remains. Options C and D are red herrings: percentages are neither means nor medians in the offending sense, and completion is a reasonable outcome metric. The senior-analyst response is to propose a controlled test — an A/B experiment or staged rollout — which reflects your skill in integrating digital analytics with qualitative data to develop hypotheses for testing rather than accepting observational stories.

**Question 9 (hard) — Problem solving across the product life cycle**

Your organisation is deciding whether a service in public beta should move to live. The framework requires: (i) all four mandatory KPIs baselined for at least 8 weeks; (ii) completion rate at or above 65% for the last 4 consecutive weeks; (iii) no severity-1 data quality issues open. Current state: KPIs baselined for 9 weeks; completion rates for the last 5 weeks were 63%, 66%, 67%, 68%, 69%; one severity-1 issue was closed yesterday; one severity-2 issue remains open. Does the service meet the framework criteria?

- A) No — completion was 63% five weeks ago.
- B) No — a data quality issue is still open.
- C) Yes — all three criteria are met.
- D) Cannot tell — the framework is ambiguous about severity-2 issues.

**Correct answer: C.**

**Explanation:** Test each criterion exactly as written. (i) Nine weeks of baseline exceeds eight — met. (ii) The requirement is the last 4 consecutive weeks at or above 65%: those are 66%, 67%, 68%, 69% — all pass; the 63% was five weeks ago and falls outside the window — met. (iii) The prohibition covers severity-1 issues only; the sole severity-1 issue is closed, and the open severity-2 issue is simply not covered by the criterion — met. Option A misreads the window; option B upgrades a severity-2 into scope; option D invents ambiguity where the rule is silent but precise. Note the professional nuance: meeting the letter of the criteria does not stop you flagging the severity-2 issue in your recommendation — recognising when to move forward while communicating residual risk is exactly what your product life cycle skill describes.

**Question 10 (moderate) — Pattern recognition in segmentation**

You segment a service's completion rate by channel and device. Desktop: 81%. Mobile: 58%. Overall: 74%. A stakeholder says: "Mobile is failing — fix mobile and overall completion will approach 81%." Roughly what share of traffic is mobile, and is the stakeholder's expectation arithmetically sound?

- A) Mobile is about 30% of traffic; raising mobile to 81% would lift overall to about 81%.
- B) Mobile is about 30% of traffic; raising mobile to 81% would lift overall to about 81%, but only if desktop traffic falls.
- C) Mobile is about 70% of traffic; the overall rate would rise to about 65%.
- D) Mobile share cannot be inferred from these figures.

**Correct answer: A.**

**Explanation:** Let m be the mobile share. Then 81(1 − m) + 58m = 74, so 81 − 23m = 74, giving m = 7/23 ≈ 30%. If mobile completion rose to 81%, every segment would sit at 81%, so the overall rate would be 81% regardless of mix — the stakeholder's arithmetic is sound (whether "fixing mobile" to desktop parity is realistic is a separate, empirical question). Option B adds an unnecessary condition; option C inverts the weights; option D is wrong because a weighted average with two known segment values and the overall value pins down the mix exactly. This blend of deduction and mental arithmetic — recovering hidden quantities from a weighted average — appears constantly in real dashboard conversations.

**Question 11 (hard) — Technical systems reasoning**

Your analytics platform samples data when a property exceeds 500,000 sessions per month. Reports built on sampled data show an "estimate" flag. This month a report shows: sessions 620,000 (flagged as estimated), completions 41,000 (unflagged, from the transaction database), and a completion rate of 6.6% computed by dividing the two. A colleague asks whether the 6.6% is trustworthy. What is the most accurate assessment?

- A) Fully trustworthy — both inputs come from production systems.
- B) Untrustworthy in principle: it divides an estimated numerator source into a precise denominator source drawn from different collection systems, so both sampling error and systematic coverage differences apply.
- C) Trustworthy as long as sampling is random, because random sampling never biases a ratio.
- D) Untrustworthy solely because 620,000 exceeds the sampling threshold.

**Correct answer: B.**

**Explanation:** Two distinct problems stack here. First, the session figure is a sample-based estimate, so the ratio inherits sampling error. Second — and more important — the numerator and denominator come from different systems with different coverage: web analytics loses users who decline cookies or block scripts, while the transaction database records every completion. Mixing collection systems in one ratio introduces a systematic bias that no sample size fixes; the honest move is to present the rate with its limitations, or compute both numerator and denominator within a single system for consistency. Option A ignores both issues; option C is false because random sampling still leaves the cross-system coverage mismatch; option D identifies a symptom, not the reasoning. Understanding the limitations of digital technology — precisely this kind of limitation — is named in your technical understanding skill.

**Question 12 (moderate) — Prioritising analytical deliverables**

A discovery-phase team asks you for: (1) a real-time dashboard, (2) a benchmark of comparable services' KPIs, (3) analysis of existing call-centre contact reasons, and (4) a conversion funnel for the yet-to-be-built service. Which two deliverables fit the discovery stage, and why?

- A) 1 and 4 — teams need dashboards and funnels from day one.
- B) 2 and 3 — discovery is about understanding the problem space and existing user behaviour, before anything is built.
- C) 1 and 2 — dashboards plus benchmarks give the fullest picture.
- D) 3 and 4 — contact reasons and funnels are both user-behaviour data.

**Correct answer: B.**

**Explanation:** In discovery there is no service to instrument, so a real-time dashboard (1) and a funnel for an unbuilt service (4) are physically impossible or premature. What discovery needs is evidence about the problem: how comparable services perform (2) sets realistic expectations and candidate KPIs, and call-centre contact reasons (3) reveal existing user needs and failure demand in current channels. Recognising the appropriate deliverables at each stage — and having the confidence to say "not yet" to a dashboard request — is a defining behaviour of your product life cycle skill. Option D pairs one right answer with one impossible one; that half-right pattern is a common trap in cognitive tests, so always evaluate each element of a paired option independently.

**Question 13 (hard) — Deduction from incomplete information**

Three analysts each own one dashboard: Amina, Ben, and Chloe own the payments, passports, and appeals dashboards, in some order. You know three facts: Amina does not own payments; the passports dashboard owner joined the team most recently; and Ben has been on the team longer than Amina, who has been on the team longer than Chloe. Who owns which dashboard?

- A) Amina: passports; Ben: appeals; Chloe: payments
- B) Amina: appeals; Ben: payments; Chloe: passports
- C) Amina: passports; Ben: payments; Chloe: appeals
- D) Cannot be determined from the information given

**Correct answer: B.**

**Explanation:** Chain the tenure facts first: Ben has been on the team longer than Amina, and Amina longer than Chloe, so Chloe is the most recent joiner. The passports owner joined most recently, so Chloe owns passports. Amina does not own payments, and passports is taken, so Amina owns appeals. That leaves Ben with payments. Every clue is used exactly once and the assignment is forced — the answer is B, not D. Options A and C both put someone other than Chloe on passports, contradicting the tenure chain. The method matters more than the puzzle: convert each clue into a hard constraint, apply the most restrictive constraint first (here, the tenure chain pins the most recent joiner uniquely), and let eliminations cascade. This is the same systematic reasoning you use when reconciling ownership, tenure, and responsibility across a team you manage, or when deducing which of several upstream systems could have produced a data defect: write the constraints down and test candidate assignments methodically rather than holding them in your head under time pressure.

### Preparation tips

- **Rehearse with your own artefacts.** Before an assessment, spend an evening reviewing a real dashboard, a real pipeline specification, and a real KPI framework, and ask of each: what could be wrong here, and how would I know? Cognitive tests for this role reward exactly that habit of structured suspicion.
- **Practise separating trend, seasonality, and disruption.** Many pattern questions hinge on noticing a step change and reasoning from the new baseline. Sketch series mentally as "level + slope + shocks".
- **Do arithmetic on weighted averages until it is reflexive.** Segment-mix questions (like Question 10) are cheap marks once the algebra is automatic.
- **Read rules like a lawyer.** Framework and criteria questions (Questions 2 and 9) are won by applying exactly what is written — no more, no less. Underline scope words: "all", "some", "only", "at least", "severity-1".
- **Manage your time deliberately.** At your level, accuracy expectations are high, but so is the question difficulty ceiling. Bank the easy questions fast, flag the hard ones, and return. A senior candidate who scores well on 85% of questions attempted beats one who stalls on question 4.
- **Sleep and settings matter.** Do the test on a proper screen, with a quiet room, paper for working, and the practice questions taken seriously — interface familiarity is free marks.

### Common pitfalls

- **Treating it like a generic IQ test.** These assessments mimic your job's actual data formats. Candidates who slow down to read the scenario — the pipeline order, the framework wording — outperform candidates who pattern-match superficially.
- **Half-right paired options.** As in Question 12, options often bundle one correct element with one wrong one. Evaluate every element.
- **Ignoring speed-versus-accuracy reporting.** Many platforms report both. Wild guessing to finish inflates speed but craters accuracy; unfinished perfectionism does the opposite. Aim for steady, checked progress.
- **Assuming the data is clean.** In this role's tests, the twist is often a measurement artefact (Questions 3, 5, 11). If a number looks dramatic, your first hypothesis should be "how is this measured?" — in the test and in real life.
- **Letting adaptivity rattle you.** If questions get harder, the algorithm thinks you are good. Keep your rhythm.


## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can reach a defensible conclusion from data under time pressure. As a senior performance analyst the data is exactly what you work with daily: service volumes, conversion and completion rates, satisfaction scores, cost per transaction, and the figures other people produce and ask you to interpret.

The format is typically fifteen to twenty-five minutes with a calculator permitted, presenting tables and charts followed by multiple-choice items. Some questions are computational; others ask what the data does and does not support, and the second kind carries more weight at your level, because much of your job is judging other people's arithmetic.

Three habits matter particularly.

The first is that a rate and a count answer different questions, and a rate improving while a count falls is one of the most common shapes in service data. Checking both before interpreting either is the discipline that prevents the commonest misreading in the profession.

The second is that averages across dissimilar groups mislead. A mean satisfaction score across channels, a mean handling time across case types, a mean completion rate across user groups — each hides the distribution that contains the actual finding.

The third is that you increasingly carry out complex analysis and supervise others doing the same, which means you need to be quick enough at the underlying arithmetic to notice when a figure is wrong by an order of magnitude. The magnitude check is worth more than the precise answer.

### What it measures for your role

- **Rate and volume reasoning** maps to **Performance measurement** and setting up frameworks.
- **Distribution and segmentation** maps to **Analysis and insight** and carrying out increasingly complex analysis.
- **Assurance arithmetic** maps to **Quality assurance of data and analysis**.
- **Sampling and estimation** maps to **Technical understanding (performance analyst)**.
- **Cost and benefit figures** maps to **Understanding analysis across the product life cycle**.
- **Presenting figures** maps to **Communicating analysis and insight**.

### Practice questions

*Table 1 — Service performance by channel, last quarter*

| Channel | Transactions started | Completion rate | Mean satisfaction (of 5) | Cost per completed transaction |
|---|---|---|---|---|
| Digital self-service | 84,000 | 71% | 4.3 | £1.20 |
| Assisted digital | 12,000 | 88% | 4.6 | £14.00 |
| Telephone | 31,000 | 92% | 4.1 | £22.50 |
| Paper | 9,000 | 79% | 3.4 | £31.00 |

**Question 1 (easy) — Reading a table**

Which channel has the highest completion rate?

- A) Digital self-service
- B) Assisted digital
- C) Telephone
- D) Paper

**Correct answer: C**

**Explanation:** Telephone at 92%, ahead of assisted digital at 88%. Worth noting before drawing any conclusion that the channels serve different people — telephone users have reached a human who guides them through, which is a substantial reason for a high completion rate that has nothing to do with the channel being better designed.

**Question 2 (easy) — Completions by channel**

Approximately how many transactions were completed through digital self-service?

- A) 59,600
- B) 71,000
- C) 84,000
- D) 46,200

**Correct answer: A**

**Explanation:** 84,000 × 0.71 = 59,640, so about 59,600. This is the calculation that converts a rate into people, and it is the one to do first on any table like this — the digital channel has the lowest completion rate and completes more transactions than all the other channels combined, which is not visible from the rate column.

**Question 3 (moderate) — Total completions**

Approximately how many transactions were completed across all four channels?

- A) About 88,000
- B) About 106,000
- C) About 136,000
- D) About 120,000

**Correct answer: B**

**Explanation:** Digital 84,000 × 0.71 = 59,640; assisted digital 12,000 × 0.88 = 10,560; telephone 31,000 × 0.92 = 28,520; paper 9,000 × 0.79 = 7,110. Total = 105,830, about 106,000. Establishing this denominator early is worth the time, because every share, cost and percentage that follows is measured against it.

**Question 4 (moderate) — Overall completion rate**

What is the approximate overall completion rate across all channels?

- A) 82.5%
- B) 77.6%
- C) 71.0%
- D) 88.0%

**Correct answer: B**

**Explanation:** 105,830 completions from 136,000 starts = 77.8%, so about 77.6% as the nearest option. The unweighted mean of the four channel rates is (71 + 88 + 92 + 79) / 4 = 82.5%, which is option A and the standard trap — it treats the 9,000 paper transactions as equal in weight to the 84,000 digital ones. Whenever you aggregate rates across groups of different sizes, weight by size or recompute from the underlying counts.

**Question 5 (moderate) — Total cost**

Approximately what did telephone completions cost in the quarter?

- A) About £642,000
- B) About £698,000
- C) About £450,000
- D) About £312,000

**Correct answer: A**

**Explanation:** 31,000 starts × 0.92 = 28,520 completions × £22.50 = £641,700, so about £642,000. Note the cost figure is per *completed* transaction, so it applies to completions rather than starts — reading that qualifier correctly is the difference between £642,000 and £697,500, which is option B and what you get by multiplying starts instead.

**Question 6 (harder) — Cost of a channel shift**

If 10% of telephone starts moved to digital self-service and completed at the digital rate, what is the approximate change in total completions?

- A) About 130 fewer completions
- B) About 650 fewer completions
- C) About 130 more completions
- D) No change

**Correct answer: B**

**Explanation:** 10% of 31,000 telephone starts is 3,100. At the telephone rate they produce 3,100 × 0.92 = 2,852 completions; at the digital rate, 3,100 × 0.71 = 2,201. The difference is 651 fewer completions. This is the arithmetic behind one of the most consequential decisions in public service design: shifting volume to a cheaper channel saves money and, at these completion rates, means around 650 people per quarter who would have completed do not. Being able to produce both numbers is what makes the trade-off explicit rather than assumed.

**Question 7 (harder) — Cost saving against that shift**

Using the same shift, what is the approximate cost change?

- A) About £61,600 saved
- B) About £64,200 saved
- C) About £2,600 saved
- D) About £70,000 saved

**Correct answer: A**

**Explanation:** Telephone cost removed: 2,852 completions × £22.50 = £64,170. Digital cost added: 2,201 × £1.20 = £2,641. Net saving: £61,529, about £61,600. So the shift saves roughly £61,600 per quarter and costs about 650 completions — which works out at roughly £95 of saving per person who no longer completes. Expressing it that way is what turns a channel strategy into a decision someone has to own.

**Question 8 (moderate) — Weighted satisfaction**

What is the approximate completion-weighted mean satisfaction across all channels?

- A) 4.10
- B) 4.30
- C) 4.25
- D) 4.60

**Correct answer: C**

**Explanation:** Weight each score by completions: (59,640 × 4.3) + (10,560 × 4.6) + (28,520 × 4.1) + (7,110 × 3.4) = 256,452 + 48,576 + 116,932 + 24,174 = 446,134. Divide by 105,830 completions = 4.216, so about 4.25 as the nearest option. The unweighted mean is (4.3 + 4.6 + 4.1 + 3.4) / 4 = 4.10, which is option A. Note also that satisfaction here is measured among people who completed, so it says nothing about the roughly 30,000 who did not.

**Question 9 (harder) — What the data supports**

What is the strongest conclusion from Table 1 about the digital self-service channel?

- A) It performs worst, having the lowest completion rate.
- B) It has the lowest completion rate and delivers more than half of all completions at around a twentieth of the cost per transaction of telephone — but the channels serve different people, so the rate difference may reflect who uses each channel rather than how well each works.
- C) It should be improved to match telephone's completion rate.
- D) It is the most successful channel.

**Correct answer: B**

**Explanation:** Option B states the three facts the table actually supports and then names the confound that governs all of them. The self-selection point is decisive: people who can complete online do, and those who cannot use assisted digital or telephone, so comparing raw completion rates across channels compares populations as much as channels. Option A picks one column. Option D picks two. Option C prescribes a target that may be unreachable precisely because of the population difference.

**Question 10 (harder) — A change over time**

Digital completion rate rose from 68% to 71% over two quarters while digital starts rose from 79,000 to 84,000. What is the strongest statement?

- A) Completions rose by about 6,000, from roughly 53,700 to 59,640 — a rise driven by both more people starting and a higher proportion finishing.
- B) Completion improved by 3 percentage points.
- C) Completions rose by about 4.4%.
- D) The improvement cannot be assessed without satisfaction data.

**Correct answer: A**

**Explanation:** Before: 79,000 × 0.68 = 53,720. After: 84,000 × 0.71 = 59,640. A rise of 5,920 completions, or about 11%. Option A gives both the count and the two contributing factors, which is what a decision-maker needs — a rate rise and a volume rise are different achievements with different causes. Option B reports the rate movement alone. Option C is the increase in starts, not completions. Option D declines an assessment the data supports.

**Question 11 (harder) — Significance and practical importance**

An A/B test on 60,000 users finds a 0.3 percentage point difference in completion, significant at p < 0.05. What is the strongest reading?

- A) The difference is real and worth implementing.
- B) The difference is probably real, and whether 0.3 points justifies the change depends on the implementation and maintenance cost — a large sample detects real but trivial effects, so significance and importance are separate questions.
- C) The difference is too small to be real.
- D) The test needs more users.

**Correct answer: B**

**Explanation:** Statistical significance tells you an effect is distinguishable from zero; it says nothing about whether the effect is worth having. At 60,000 users a test has power to detect differences well below the threshold at which anyone should act — here, 0.3 points on the digital channel's volume would be roughly 250 additional completions a quarter, which may or may not repay the work. Option B separates the two questions and names the criterion. Option C misunderstands what significance means. Option D asks for more of what is already sufficient.

**Question 12 (harder) — Trend against variation**

Monthly completions over eight months: 19,400, 20,100, 19,800, 21,300, 19,200, 20,600, 19,900, 21,000. A stakeholder asks whether completions are trending upward. What is the strongest answer?

- A) Yes; the series ends higher than it began.
- B) The series moves between 19,200 and 21,300 with no clear direction — the first four average 20,150 and the last four 20,175, a difference well inside the month-to-month variation — so completions are essentially flat and the apparent rise depends entirely on which months you compare.
- C) No; completions are falling.
- D) There is insufficient data.

**Correct answer: B**

**Explanation:** First-to-last comparison suggests a rise of 1,600; comparing the two halves gives a difference of 25, which is nothing. The range within each half is far larger than the difference between them. Option B characterises the variation and states what the data supports, which is what the stakeholder actually needs. Option A picks the two endpoints that tell the preferred story, which is the single most common misuse of a time series in performance reporting. Option D declines to characterise data that can be characterised.

**Question 13 (harder) — Estimating from a sample**

A survey of 400 users of a service with 105,000 quarterly completions finds 62% rating it good or very good, with a margin of error of about ±5 points. The target is 65%. What is the strongest statement?

- A) The service is missing its target.
- B) The point estimate of 62% is below the 65% target, and the interval of roughly 57% to 67% includes the target — so the survey neither confirms the target is being met nor establishes that it is being missed, and a larger sample would be needed to distinguish them.
- C) The service is meeting its target.
- D) The survey is too small to be useful.

**Correct answer: B**

**Explanation:** With a ±5 point margin, 62% corresponds to an interval of about 57% to 67%, which straddles the 65% target. Reporting "we are missing the target" treats a point estimate as a measurement, and reporting "we are meeting it" does the same in the other direction. Option B states the honest position and what would resolve it. Option D over-corrects — 400 responses is genuinely informative, just not precise enough to separate 62% from 65%.

### Preparation tips

- **Convert rates into counts before interpreting them.**
- **Weight averages by group size, or recompute from underlying counts.**
- **Check whether a per-unit cost applies to starts or completions.**
- **Compute both sides of a channel shift: money saved and people lost.**
- **Separate statistical significance from practical importance.**
- **Compare halves of a time series rather than endpoints.**
- **Report a survey estimate with its interval against the target.**
- **Check magnitudes before precision.**

### Common pitfalls

- **Taking the unweighted mean of rates across groups of very different sizes.**
- **Comparing channel completion rates without noting who uses each channel.**
- **Reporting a rate improvement without the volume behind it.**
- **Reading "statistically significant" as "important".**
- **Reporting first-to-last change in a noisy series.**
- **Treating a survey point estimate as a measurement.**
- **Multiplying a per-completion cost by starts.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what a piece of written material establishes. As a senior performance analyst the material is metric definitions and measurement frameworks, data quality documentation, tool and supplier terms, research reports, and the summaries other people write about your team's analysis.

The commonest format presents a passage followed by statements to be marked True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, and Cannot Say means it settles neither — regardless of what you know professionally.

Your expertise is the main hazard. You will know how a metric is usually calculated and what a movement usually means, while the passage in front of you describes this particular case — and at your level your reading frequently becomes the team's reading.

Three specifics matter particularly.

The first is that claims are routinely attributed rather than established. "The supplier states", "the review found", "the report recommends" — each tells you the source and nothing about whether it is true. You supervise others' analysis, so spotting the difference is something you need to model as well as practise.

The second is that measurement definitions turn on small words, and organisations vary them. Your role names setting up performance measurement frameworks, which means you are the person whose definitions other people will read this closely.

The third is that a report which names what it did not examine is telling you where the evidence stops, and the unexamined question is frequently the important one.

### What it measures for your role

- **Reading definitions precisely** maps to **Performance measurement** and setting up frameworks.
- **Reading data quality documentation** maps to **Quality assurance of data and analysis**.
- **Reading tool documentation** maps to **Technical understanding (performance analyst)**.
- **Distinguishing evidence from claim** maps to **Analysis and insight**.
- **Reading research** maps to **User-centred analysis**.
- **Summarising accurately** maps to **Communicating analysis and insight**.

### Practice questions

*Passage A — for Questions 1 to 4*

"The department's quality assurance framework requires that analysis informing an external publication is reviewed by a second analyst before release. Analysis informing internal decisions should be reviewed where the method is novel to the data source or where the analyst requests it. Reviewers must record the review in the analysis log. Where a reviewer identifies a material error, the analysis must not be released until the error is corrected and the corrected analysis re-reviewed. A reviewer may not review analysis they contributed to. The framework applies to all analytical professions in the department."

**Question 1 (easy)**

Statement: Analysis informing an external publication must be reviewed by a second analyst.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly with "must". Note the deliberate contrast with the next sentence, which uses "should" and attaches conditions for internal analysis — the framework distinguishes carefully between absolute and conditional obligations, and the following questions turn on that.

**Question 2 (moderate)**

Statement: Analysis informing an internal decision must be reviewed if the method is novel to the data source.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The framework says such analysis "should be reviewed" in that case. "Should" is a strong expectation permitting justified departure, and the statement's "must" overstates it — in a passage that uses "must" three times elsewhere, the choice of "should" here is clearly deliberate. As someone with quality assurance responsibility in your team, the practical consequence is that you can require this locally and the framework does not require it of everyone.

**Question 3 (moderate)**

Statement: An analyst who contributed to a piece of analysis can review it if they were not the main author.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The framework states that "a reviewer may not review analysis they contributed to". Contribution is the test, not authorship, so a secondary contributor is excluded just as a lead author would be. The passage contradicts the statement. This matters in small teams, where the only other person who understands the analysis is frequently the person who helped with it — and the framework has anticipated exactly that temptation.

**Question 4 (harder)**

Statement: Analysis containing an error that has been corrected can be released once the correcting analyst confirms the fix.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The framework requires that the analysis "must not be released until the error is corrected **and** the corrected analysis re-reviewed". Two conjunctive conditions; the statement satisfies only the first, and a self-confirmation is not a re-review — by the framework's own structure a review means a second analyst who did not contribute. Reading a two-part condition as a one-part condition is how quality assurance gets short-circuited under deadline pressure, which is exactly when it matters most.

*Passage B — for Questions 5 to 8*

"The analytics platform records an event when the tracking script executes. Sessions expire after 30 minutes of inactivity. The platform applies sampling above 500,000 events per day, using a 10% sample and scaling reported figures accordingly; sampling is flagged in the interface. Users who decline analytics cookies are not tracked. The supplier states that the consent banner change in June had no effect on measured traffic. Segment-level figures derived from sampled data carry wider uncertainty than headline totals."

**Question 5 (easy)**

Statement: Users who decline analytics cookies do not appear in the platform's figures.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly: such users "are not tracked". Straightforward and consequential — every figure the platform produces describes the subset of users who accepted cookies, which is a limitation belonging in any report built on it.

**Question 6 (moderate)**

Statement: The June consent banner change had no effect on measured traffic.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The passage says "the supplier states" this. That establishes what the supplier claims, not that the claim is true — and a supplier is not a neutral party on whether their own change affected measurement. A consent banner change is one of the most likely things to alter measured traffic, since it changes how many users are tracked at all. The professional response is to test the claim against data spanning June rather than accept or dismiss it.

**Question 7 (moderate)**

Statement: On a day with 700,000 events, a reported segment figure is an estimate.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Sampling applies above 500,000 events per day, and 700,000 exceeds the threshold, so figures are scaled from a 10% sample — which makes them estimates rather than counts. The passage also tells you that segment-level figures from sampled data carry wider uncertainty than headline totals, which is the practically important part: a scaled segment figure looks exactly as precise in a dashboard as a counted one.

**Question 8 (harder)**

Statement: A user who returns to the service after 45 minutes of inactivity is recorded as a new session.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Sessions "expire after 30 minutes of inactivity", and 45 minutes exceeds that, so the return begins a new session. The passage establishes this. Worth holding when interpreting session counts: a single person working through a long application with interruptions can generate several sessions, which is why session-based measures overstate the number of people involved.

*Passage C — for Questions 9 to 13*

"A review of the service's assisted digital channel examined 18 months of data. It found that users of the channel completed at a higher rate than digital self-service users, at 88% against 71%. Users were routed to assisted digital either by choosing it or by being referred after abandoning the self-service route. The review did not distinguish between these two groups. Satisfaction among assisted digital users was 4.6 out of 5, measured at the end of the transaction. The review recommends expanding assisted digital capacity. It notes that no data was available on users who abandoned both channels."

**Question 9 (moderate)**

Statement: Assisted digital users completed at a higher rate than digital self-service users.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly with figures, 88% against 71%. True as a description of the two groups. Note that this is a comparison of outcomes between two populations, not evidence about the effect of the channel — which the next question addresses.

**Question 10 (moderate)**

Statement: Assisted digital is more effective than digital self-service at helping users complete.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** The two populations differ systematically. Some assisted digital users chose it, and others arrived there after abandoning self-service — the second group having already demonstrated they were struggling, which would push the assisted digital rate down rather than up, while the first group self-selected. The review "did not distinguish between these two groups", so the composition is unknown and the causal comparison cannot be made. The rate difference is real; the attribution to the channel is not established.

**Question 11 (moderate)**

Statement: The satisfaction figure of 4.6 represents users of the assisted digital channel.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Satisfaction was "measured at the end of the transaction", so it reaches users who reached the end — the 88% who completed, not the 12% who did not. The figure represents completers rather than users of the channel, and the passage's own description of the method establishes the distinction. Given that dissatisfied users are disproportionately likely to be among those who did not finish, the direction of the bias is predictable.

**Question 12 (moderate)**

Statement: Expanding assisted digital capacity would raise the service's overall completion rate.

- A) True
- B) False
- C) Cannot Say

**Correct answer: C**

**Explanation:** This is the review's recommendation, and a recommendation is not a finding. Whether expansion raises the overall rate depends on the causal question the review could not answer — if the 88% reflects who uses the channel rather than what it does, adding capacity would not reproduce that rate for new users. The passage supplies the recommendation and, in the same breath, the reason it cannot be relied on.

**Question 13 (harder)**

Statement: The review's findings cover the full population of people who attempted the service.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The review "notes that no data was available on users who abandoned both channels". Those people attempted the service and are absent from the analysis entirely, so the findings do not cover the full population — the passage contradicts the statement by its own admission. This is the most important sentence in the passage: the group missing from the data is the group for whom the service failed completely, and any conclusion about how well the service works that excludes them is measuring the experience of the people it already worked for.

### Preparation tips

- **Read "must" and "should" as different obligations, especially in the same document.**
- **Check what a condition actually tests — contribution rather than authorship, for instance.**
- **Treat conjunctive conditions as all required.**
- **Note when a claim is attributed to an interested party.**
- **Check whether a figure is counted or sampled before slicing it.**
- **Ask who a satisfaction survey reaches.**
- **Look for self-selection when two groups are compared.**
- **Read the sentence naming what the analysis could not cover.**

### Common pitfalls

- **Reading "should be reviewed" as a requirement.**
- **Accepting a supplier's statement about their own change.**
- **Treating a sampled segment figure as precise.**
- **Attributing an outcome difference to a channel when the populations differ.**
- **Reading end-of-transaction satisfaction as representing all users.**
- **Treating a recommendation as an established remedy.**
- **Overlooking the group absent from the data.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. As a senior performance analyst the scenarios involve supervising others' analysis, deciding what to delegate or automate, presenting findings people do not want, and being the person whose judgement determines whether a team's numbers can be trusted.

The commonest formats ask for the most and least effective response, or for ratings. Scoring is against a key derived from experienced practitioners at comparable levels.

Three patterns run through the strong answers.

The first is that your role summary names delegating, automating or upskilling others "where possible and appropriate". Doing the analysis yourself is nearly always faster today and is the reason your team's capacity never grows.

The second is that you are responsible for the accuracy and quality of data and analysis *and for how they are used*. A correct number being misread is your problem, which means intervening at the point of interpretation rather than only at the point of calculation.

The third is that you are increasingly the person who says the unwelcome thing. Analysis that only ever confirms what people hoped is analysis nobody needs, and the credibility to be believed on the difficult findings is built on the ordinary ones.

### What it measures for your role

- **Delegation and upskilling** maps to your role level's description.
- **Supervising analysis** maps to **Quality assurance of data and analysis**.
- **Presenting findings** maps to **Communicating analysis and insight**.
- **Framework design** maps to **Performance measurement**.
- **Team capability** maps to ensuring the team has the required skills.
- **Community links** maps to contributing to the community and forging links with other analytical disciplines.

### Practice questions

**Question 1 (easy) — A piece of analysis you could do faster**

An analyst you supervise is working on something you could complete in an hour. It will take them a day. What is the most effective response?

- A) Do it yourself; the team is busy.
- B) Let them do it, checking in early enough to correct a wrong direction — because the hour you save today costs you the same hour every time the task recurs, and your role names upskilling others where possible.
- C) Do it together.
- D) Let them do it and review the result.

**Correct answer: B. Least effective: A**

**Explanation:** The arithmetic of delegation is that doing it yourself is faster once and slower forever. Option B adds the safeguard that makes it work — an early check catches a wrong direction before the day is spent, which is the main risk of delegating. Option A is least effective as a habit: it keeps the capability concentrated in you and is precisely what your role level asks you to stop doing. Option C is a good option for genuinely novel work and expensive for a routine task. Option D is fine and reviews only after a day has gone.

**Question 2 (easy) — A number being misused**

In a meeting, a service owner describes your analysis as showing that a change worked, when it shows an association with a confounding factor. What is the most effective response?

- A) Say briefly what the analysis supports and what it does not, in the meeting.
- B) Correct it afterwards in writing.
- C) Let it stand; the direction is probably right.
- D) Correct the service owner directly.

**Correct answer: A. Least effective: C**

**Explanation:** Your accountability covers how analysis is used, and a misinterpretation stated in a meeting becomes the room's shared understanding within minutes. Option A gets the correction in without a confrontation — "worth being clear what this can and can't tell us" does it. Option C is least effective: allowing a causal claim your analysis does not support is how your team's work ends up backing a conclusion you would not defend. Option B reaches fewer people than were in the room. Option D achieves the right outcome in a form that invites defensiveness.

**Question 3 (moderate) — An analyst's method you doubt**

An analyst you supervise has used an approach you think is wrong, and they have clearly thought about it. What is the most effective response?

- A) Ask what led them to it and what alternatives they weighed, then set out your concern with reasons — because they may have hit a constraint you cannot see, and if not, the reasoning is what transfers.
- B) Tell them to use the approach you would have used.
- C) Accept it; it is their analysis.
- D) Rework it yourself before it goes out.

**Correct answer: A. Least effective: D**

**Explanation:** Option A costs a conversation and buys the possibility that they are right plus an analyst who can make the judgement unaided. Option D is least effective — it removes the work, teaches nothing, and tells the team their analysis becomes yours when you disagree. Option B transfers a conclusion without reasoning, which works once. Option C declines the assurance responsibility you hold.

**Question 4 (moderate) — Automating a recurring task**

Your team spends significant time each month on a recurring report. Automating it would take about two weeks. What is the most effective response?

- A) Work out the annual hours it consumes against the two weeks, and if it pays back, make the case for the time with that figure attached.
- B) Automate it in spare time.
- C) Continue producing it manually; there is no capacity.
- D) Ask an analyst to automate it alongside their other work.

**Correct answer: A. Least effective: B**

**Explanation:** Option A turns an engineering instinct into a proposition somebody can approve, and recurring reports almost always pay back within a year once the arithmetic is done. Option B is least effective: unsanctioned work done in gaps makes both the automation and the committed work slower, is invisible if it succeeds, and looks like a missed estimate if it does not. Option D is the same problem delegated. Option C accepts a permanent cost without testing whether it is necessary.

**Question 5 (moderate) — A metric that will drive bad behaviour**

A delivery team proposes a target on average call handling time. What is the most effective response?

- A) Name how the target would be met — the cheapest way to reduce handling time is to close contacts before they are resolved, which raises repeat contacts and worsens service while the number improves — and propose pairing it with first contact resolution and repeat contact rate.
- B) Agree; handling time is a standard measure.
- C) Advise against measuring handling time.
- D) Agree, and monitor for unintended effects.

**Correct answer: A. Least effective: B**

**Explanation:** Option A names the mechanism rather than objecting in principle, which is what makes the argument land with people who need a throughput measure for legitimate reasons — and the paired measures are the remedy, because they are hard to move without genuine improvement. Option B is least effective because it adopts a target without asking how it will be met, which is the question your profession exists to ask. Option D detects the damage after real users have experienced it. Option C discards a measure that is useful for capacity planning when it is not a target.

**Question 6 (moderate) — A finding nobody wants**

Your analysis shows a feature the team spent a quarter building is barely used. What is the most effective response?

- A) Report it plainly, with what the data shows and what it does not — whether low use means low need, poor discoverability, or too little time since launch — because the distinction determines what the team does next.
- B) Report the usage figures.
- C) Wait another month before reporting.
- D) Report it alongside the features that performed well.

**Correct answer: A. Least effective: C**

**Explanation:** Low usage is a fact with several possible meanings, and option A reports it in the form that makes it actionable rather than merely disappointing. Option C is least effective: delaying an unwelcome finding costs the team a month of building on a false picture, and the delay looks worse afterwards than the finding. Option B stops short of the useful part. Option D is reasonable as context and becomes a way of burying results if it is your standard practice.

**Question 7 (harder) — Pressure on your method**

A programme lead challenges the method behind a finding that reflects badly on their programme. What is the most effective response?

- A) Take the challenge seriously and check it properly, then report what you find — whether it confirms, qualifies or overturns the original finding — because the challenge may be right and treating it seriously is what makes the confirmation credible.
- B) Defend the finding; the analysis was sound.
- C) Soften how the finding is presented.
- D) Add caveats acknowledging uncertainty.

**Correct answer: A. Least effective: C**

**Explanation:** A challenge from an interested party may still be correct, and checking costs little compared with the credibility of being able to say you did. Option A leaves you in the strongest position whichever way it turns out. Option C is least effective: softening the presentation of a finding you believe is right, under pressure, changes the analysis by another route and is how findings quietly stop meaning anything. Option D does the same more subtly. Option B may be correct and forgoes the check that would demonstrate it.

**Question 8 (harder) — A skills gap in your team**

You realise that only you can maintain the pipeline several of the team's reports depend on. What is the most effective response?

- A) Document it thoroughly.
- B) Have an analyst work through real maintenance with you — a change, a failure — because what you do without thinking is invisible to you, and documentation systematically misses exactly that.
- C) Simplify the pipeline.
- D) Ask for a second specialist to be recruited.

**Correct answer: B. Least effective: D**

**Explanation:** Your role names ensuring the team has the required skills, and tacit knowledge transfers through supervised practice rather than prose — you cannot document what you do not know you are doing. Option D is least effective as the primary response: it is slow, uncertain, expensive, and ends with the knowledge in two heads rather than distributed. Option C is often the best long-term answer and does nothing about the next quarter. Option A is worth doing alongside B and is reliably incomplete alone.

**Question 9 (harder) — An error already published**

You discover an error in analysis your team supplied three weeks ago, which has informed a decision. What is the most effective response?

- A) Notify the users immediately with the corrected figures and what the correction means for the decision they took.
- B) Correct it in the next report.
- C) Establish first whether the corrected figures would have changed the decision.
- D) Ask the analyst who produced it to notify them.

**Correct answer: A. Least effective: B**

**Explanation:** People are acting on the wrong number, which makes speed the priority. Option A includes the part that matters most to them — what it means for the decision — which is the difference between a useful disclosure and an alarming one. Option C is a sensible thing to work out and belongs *inside* the notification rather than before it. Option B is least effective: leaving a decision standing on a figure you know is wrong is the worst available option. Option D puts the most exposed person in front of the disclosure, which is yours to make.

**Question 10 (harder) — Setting up a framework**

You are asked to set up a measurement framework for a new service. The team already has a list of metrics they want. What is the most effective response?

- A) Start from what the service is for and what decisions the team will make, then work out which measures inform those — and compare that against their list, keeping what survives.
- B) Implement their list.
- C) Replace their list with a standard framework.
- D) Implement their list and add measures you think are missing.

**Correct answer: A. Least effective: C**

**Explanation:** Metrics are chosen before anyone has articulated what decisions they will inform, which is why so many dashboards go unused. Option A starts from the decision and treats their list as an input rather than a specification — some of it will survive, which also keeps them invested. Option C is least effective: replacing a team's thinking with an off-the-shelf framework produces something they did not choose, do not understand, and will not use. Option D produces a longer list without removing anything. Option B skips the question entirely.

**Question 11 (harder) — Links with another analytical profession**

A data science team is building a model whose outputs will be reported alongside your performance measures. What is the most effective response?

- A) Get involved early to agree what the model's outputs mean, how they will be described, and how uncertainty will be shown — because outputs presented next to measured figures will be read as equally certain unless someone makes the difference explicit.
- B) Report the model outputs as supplied.
- C) Keep the two reporting streams separate.
- D) Ask the data science team to document their method.

**Correct answer: A. Least effective: B**

**Explanation:** Your role names forging links with other analytical disciplines, and this is the concrete form of it. A predicted figure and a measured one look identical in a dashboard, and readers will not distinguish them unless the presentation does. Option A resolves that while the presentation is still being designed. Option B is least effective: publishing model outputs alongside measurements without distinction is the situation that produces confident decisions on estimates nobody knew were estimates. Option D is useful and does not address presentation. Option C avoids the problem by avoiding the collaboration.

**Question 12 (harder) — Evidence against your own approach**

A measurement approach you introduced last year is producing figures delivery teams do not trust and largely ignore. What is the most effective response?

- A) Raise it yourself, including that it was your approach, find out why the figures are not trusted, and change or withdraw it on what you find.
- B) Explain the approach again so teams understand it.
- C) Require teams to use the figures.
- D) Investigate quietly and adjust.

**Correct answer: A. Least effective: C**

**Explanation:** Distrust among the people closest to the work is usually informative — the figures may genuinely not reflect what they see, or the definitions may not match operational reality. Option A investigates and is honest about ownership, which is what makes it safe for anyone else to raise a problem with something you introduced. Option C is least effective: mandating figures people do not believe produces compliance without belief and hardens the distrust permanently. Option B assumes the problem is comprehension, which is the least likely explanation. Option D reaches a reasonable outcome by a route that looks like concealment if noticed.

### Preparation tips

- **Delegate with an early check rather than doing it yourself.**
- **Correct a misinterpretation in the room where it was made.**
- **Make the payback case for automation with the annual hours attached.**
- **Ask how a target would be met before agreeing to it.**
- **Take a methodological challenge seriously even from an interested party.**
- **Transfer tacit knowledge through supervised practice.**
- **Front your team's corrections yourself.**
- **Start a framework from the decisions it will inform.**

### Common pitfalls

- **Doing the analysis yourself because it is faster today.**
- **Automating in spare time rather than making the case.**
- **Reworking an analyst's method instead of discussing it.**
- **Softening a finding under pressure.**
- **Documenting a pipeline instead of teaching it.**
- **Analysing whether an error mattered before disclosing it.**
- **Replacing a team's metrics with a standard framework.**
- **Publishing model outputs alongside measurements without distinction.**

## Conclusion

You have worked through four assessments pitched at senior performance analyst, and it is worth drawing the threads together.

The cognitive section was about reading data structurally — finding the cause behind a pattern, following a definition through its conditions, and separating a measurement artefact from a change in the world.

The numeric section came back repeatedly to one discipline: convert rates into counts before interpreting them. A completion rate is a proportion of whoever turned up, and 71% of 84,000 people is a different fact from 92% of 31,000. The channel-shift questions made the trade-off explicit — roughly £61,600 saved per quarter and around 650 people who no longer complete — and that pair of numbers is exactly the kind of thing your role exists to put in front of a decision-maker.

The verbal section was an exercise in reading definitions, frameworks and attributed claims exactly. "Should" is not "must". A supplier's statement about their own change is a claim. And the sentence noting that no data was available on people who abandoned both channels is the most important line in that passage, because it names the group for whom the service failed entirely.

The situational judgement section was about the shift this level represents. You delegate, automate and upskill rather than doing everything yourself; you are accountable for how analysis is used as well as whether it is right; and you are increasingly the person who says the thing nobody wants to hear. The strong answers checked a hostile methodological challenge properly, corrected a misreading in the room, and treated distrust of a measure you introduced as evidence rather than as a comprehension problem.

If one thread runs through all four, it is that your value is in being right about uncomfortable things. Anyone can report a number that confirms what people hoped. The credibility to be believed when the finding is unwelcome is built slowly, on ordinary analysis that turned out to be accurate, and spent quickly by a single figure that was softened under pressure.

Good luck. This is work that determines what a whole organisation believes about the services it runs, and the care you have given this is exactly right for it.
