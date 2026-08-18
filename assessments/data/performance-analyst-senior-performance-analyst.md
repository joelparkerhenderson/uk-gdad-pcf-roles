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

