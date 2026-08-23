# Head of Frontend Development - Psychometric Assessment Resources

## Introduction

Welcome. This guide is written for you as a head of frontend development in the UK Government Digital and Data profession — an expert practitioner with broad industry experience, either expert across many technical areas or a specialist with very deep knowledge in one. Your role summary names defining and assuring best practice while influencing, leading and mentoring others; influencing and developing organisational strategy and priorities in collaboration with counterparts across government; ensuring the right conditions and environment for frontend developers to work effectively; and developing departmental capability through internal mobility, career paths and recruitment.

The skills attached to the level are unusually broad. You lead on strategy for the whole organisation, marrying business needs with innovative analysis. You make and justify decisions characterised by high levels of risk, impact and complexity. You build consensus between organisations and highly independent stakeholders, solve and unblock issues between teams or departments at the highest level, understand the psychology of a team, mediate, and coach the organisation on team dynamics and conflict resolution. You also speak on behalf of and represent the community to large audiences inside and outside government.

That last cluster is worth pausing on, because it is what makes this role distinctive among senior technical posts. A great deal of your effect is achieved through other people's willingness — teams adopt your standards because they are good and because they trust you, not because you can compel them. And accessibility, which sits at the centre of frontend practice in government, is a legal obligation and a moral one that you are frequently the most senior advocate for in any given room.

You may be preparing for a formal assessment, or you may want to re-examine judgement that has become fluent. Fluency is the risk at this level: your conclusions are usually right, very few people can check them, and the feedback loops on organisational decisions are long enough that a wrong pattern can persist for years.

The document has four assessment sections — cognitive, numeric reasoning, verbal reasoning and situational judgement — each with an overview, a mapping to your named skills, twelve practice questions with full explanations, preparation tips and common pitfalls.

Commit to an answer before reading each explanation, and pay attention where you were quick.

Let's begin.

## Advisory

This assessment information is created by AI and is work in progress for educational purposes. If you intend to use it in any way, please consult with your organization's appropriate teammates, such as with human resources staff, or people and organizational development staff, or legal compliance staff.

## Workplace job-specific cognitive assessment

### About this assessment

A workplace job-specific cognitive assessment measures the reasoning your role demands, presented through material drawn from the role. At head-of-profession level that means organisational strategy, standards and assurance decisions, capability planning, cross-government coordination and technical judgements whose consequences are distributed across many teams.

The format is typically fifteen to thirty minutes online, covering deduction, pattern recognition, error checking, prioritisation and applied problem solving, scored against a norm group of comparable seniority.

Three things distinguish this section at your level.

The first is that standards you set are paid for by everyone, daily, for as long as they stand — so the useful question about a standard is not whether it describes good practice but whether the benefit exceeds the distributed cost of compliance.

The second is that adoption is a design problem. A practice that is better and harder to follow loses to one that is worse and easier, every time, and treating that as a discipline failure rather than a design failure is the characteristic error at this level.

The third is that you are usually reasoning from second-hand information. What reaches you has been filtered through people with a view, and the strong responses consistently include a step to check the picture rather than acting on the version that arrived.

### How this assessment maps to your role

- **Standards and assurance reasoning** maps to defining and assuring best practice, and to **Modern development standards**.
- **Organisational diagnosis** maps to ensuring the right conditions and environment for frontend developers.
- **Strategy reasoning** maps to **Strategic thinking**, where you lead design and implementation of strategy.
- **Capability reasoning** maps to internal mobility, career paths and recruitment.
- **Accessibility judgement** maps to **Accessibility**, where you advocate and offer design solutions.
- **Conflict and consensus** map to **Leadership and guidance (frontend developer)** and **Community collaboration**.

### Practice questions

**Question 1 (easy) — Deduction from an assurance rule**

Your standard states: "A service may not pass its assurance review with any outstanding critical accessibility issue, unless a time-bound remediation plan has been agreed with the accessibility lead." A service passed its review with an outstanding critical issue. Which must be true?

- A) The standard was breached.
- B) A remediation plan was agreed.
- C) Either a time-bound remediation plan was agreed with the accessibility lead, or the standard was breached.
- D) The pass should be revoked.

**Correct answer: C**

**Explanation:** A rule with an exception, plus a fact silent on the exception, licenses only the disjunction. Options A and B each pick a branch. Option D prescribes rather than deduces. There is a practical point behind the logic: if agreed remediation plans are not recorded against the review, your standard cannot be audited — you cannot tell a compliant pass from a breach — and that is a defect in a standard you own.

**Question 2 (easy) — Adoption as a design problem**

You publish a set of accessible component patterns. Six months on, most teams are still building their own. What is the strongest reading?

- A) Teams need reminding that the patterns exist.
- B) Capable teams building their own after the patterns were published indicates that using them is harder than not — most likely they are hard to find, hard to integrate into existing build setups, or missing the variants teams actually need — so the fix is in the friction rather than in the communication.
- C) The patterns should be mandated.
- D) Teams prefer building things.

**Correct answer: B**

**Explanation:** Reuse loses to rebuilding whenever rebuilding is cheaper for the team making the choice, and it usually is unless someone has worked hard to make it otherwise. Option B names the three usual frictions, each with a different remedy: discoverability needs a catalogue people actually reach, integration needs distribution that fits existing tooling, and missing variants need the patterns extending. Option C mandates without removing the cost, which produces copies with a compliance label. Option A assumes ignorance among people who work in this area. Option D is a stereotype rather than a diagnosis.

**Question 3 (moderate) — A standard's distributed cost**

You are considering mandating a manual screen reader test before every release across fourteen teams. What is the strongest analysis?

- A) Mandate it; screen reader testing catches what automated tools miss.
- B) Price it across the volume — fourteen teams releasing, say, twice a week each, at an hour per test, is roughly 1,450 hours a year — and then ask whether the same benefit is available more cheaply, for instance by testing at the component level once rather than at every release of every service.
- C) Mandate it for major releases only.
- D) Recommend rather than mandate it.

**Correct answer: B**

**Explanation:** The premise in option A is true and does not settle the question, because the cost is a large recurring number that nobody has computed. Option B computes it and then asks the more useful question, which is where in the pipeline the testing gives most value per hour — testing shared components thoroughly once catches the great majority of issues that repeated per-release testing would find, at a fraction of the cost. Option C is a sensible refinement needing a definition of major. Option D avoids the mandate and thereby loses most of the benefit, since voluntary testing is done by the teams who need it least.

**Question 4 (moderate) — Second-hand information**

A delivery director tells you that one of your frontend teams is "blocking progress" on a programme. What is the strongest first step?

- A) Speak to the team's lead about unblocking it.
- B) Get the team's account before doing anything, because "blocking" is what it looks like from outside when a team is refusing to ship something they believe is unsafe or inaccessible — and if that is what is happening, the useful response is the opposite of unblocking them.
- C) Ask the director what specifically is blocked.
- D) Escalate to the programme's technical lead.

**Correct answer: B**

**Explanation:** The word "blocking" describes an effect, not a cause, and the two most common causes point in opposite directions: a team being unreasonable, or a team holding a line they are right to hold. Acting before you know which is how a head of profession undermines their own people. Option C is a good question and gets the same account you already have, from the same source. Option B goes to the party whose version is missing. Option A assumes the framing. Option D acts on one account and adds a person.

**Question 5 (moderate) — Capability development**

You have three strong mid-level frontend developers and no senior vacancies. All three are being approached by other organisations. What is the strongest response?

- A) Make a case for creating senior posts.
- B) Be honest with each about what is and is not available here, and work the routes that exist — scope that stretches them, roles elsewhere in the department, secondments across government — because keeping a strong person in the organisation is a much better outcome than losing them, and a head who helps people move internally is told about approaches early.
- C) Focus on retaining the strongest of the three.
- D) Accept it; people move on.

**Correct answer: B**

**Explanation:** Your role names facilitating internal mobility explicitly, and this is what it is for. Option B is honest about the constraint, which is what makes anything else you say credible, and it widens the frame from your team to the department and to government — which is where the opportunities actually are. The second-order effect matters: people tell you they are being approached when they expect help rather than a retention conversation. Option C picks a favourite in a way the other two will notice. Option A is worth doing and slow, and will not arrive before their decisions. Option D declines the responsibility your role names.

**Question 6 (moderate) — Reading a pattern across services**

Accessibility audits across nine services find the same three issue types accounting for most findings: unlabelled form controls, insufficient contrast on secondary buttons, and modals that do not manage focus. What is the strongest conclusion?

- A) Teams need accessibility training.
- B) Three issue types recurring across nine independent teams indicates a supply problem rather than a knowledge problem — the components teams are using do not handle these cases correctly, or the design tooling permits non-compliant colours — so fixing the shared components and the colour palette removes the issues at source.
- C) Audits should be more frequent.
- D) The design system should be mandated.

**Correct answer: B**

**Explanation:** Nine teams independently producing the same three defects is a supply signal. Each of the three has a source-level fix: a form component that requires a label to render, a palette that does not contain a failing secondary button colour, and a modal component that manages focus correctly. Fix those and the findings stop appearing across all nine services without anyone learning anything new. Option A treats a systemic pattern as a knowledge deficit, which is both slower and less durable — trained people still use components that do the wrong thing. Option C detects the same issues more often. Option D may follow and does not by itself fix the components.

**Question 7 (harder) — A cross-government commitment**

Counterparts in three other departments propose a shared component library. Your department already has one that works well. What is the strongest analysis?

- A) Decline; your library works and migration would be costly.
- B) Weigh what sharing actually buys against what it costs in decision speed — a shared library means your teams' needs compete with three other departments' priorities, which is a real ongoing cost — and look for the middle option of sharing the parts where duplication is genuinely wasteful, such as accessibility-critical components, while keeping departmental control of the rest.
- C) Join; cross-government reuse is the right direction.
- D) Propose that the others adopt yours.

**Correct answer: B**

**Explanation:** The cost that decides these arrangements is rarely migration; it is that changes now require consensus among four parties, and a team that needs a variant next month may wait a quarter. Option B names that cost and identifies the partial-sharing option, which is where most successful cross-government collaboration actually lands. Option D is worth raising as part of the conversation and, offered as the response, reads as exactly the departmental parochialism these initiatives are meant to overcome. Option C accepts a principle without pricing it. Option A declines without exploring the middle.

**Question 8 (harder) — An organisational condition problem**

Frontend developers across your department report that they are brought into projects after designs are finalised. What is the strongest response?

- A) Ask delivery managers to involve developers earlier.
- B) Find out what determines when they are brought in — usually a funding or governance stage that releases development resource only after a design phase completes — because if the sequencing is structural then asking people to behave differently within it will not work, and the fix is to change the stage definition or the resourcing model.
- C) Add a design review step involving frontend developers.
- D) Train designers in frontend constraints.

**Correct answer: B**

**Explanation:** Your role names ensuring the right conditions and environment for frontend developers, and this is a conditions problem. When a behaviour is consistent across a whole department it is almost always structural rather than cultural, and the usual structure is a funding or assurance gate that treats design and development as sequential phases. Option B looks for it. Option A asks individuals to act against the incentives they face. Option C adds a step inside the broken sequence, which produces a review of decisions already made. Option D is useful and does not change when developers arrive.

**Question 9 (harder) — Assuring a decision you disagree with**

A service you are assuring has taken a technical approach you consider poor but that meets every standard. What is the strongest response?

- A) Pass the assurance and note your concerns.
- B) Pass it, because assurance is against the standard and using it to enforce preferences destroys the distinction between what is required and what you would prefer — and separately consider whether the gap between the standard and your view means the standard is missing something worth adding.
- C) Pass it conditionally.
- D) Fail it; poor approaches should not pass.

**Correct answer: B**

**Explanation:** The integrity of an assurance process depends on it being predictable, and a reviewer who fails compliant work on judgement makes the standard meaningless — teams then optimise for the reviewer rather than the standard. Option B holds that line and does the genuinely useful thing with the disagreement, which is to ask whether the standard should say something it currently does not. Option A is close and weaker: noting concerns on a pass is a way of registering displeasure that changes nothing and pressures the team informally. Option C invents a category that does not exist. Option D substitutes your preference for the published rule.

**Question 10 (harder) — Competing accounts of a conflict**

Two teams are in conflict over a shared component. Each lead has given you an account and they are incompatible. What is the strongest approach?

- A) Determine which account is accurate.
- B) Treat both accounts as accurate descriptions of each party's experience and look for the structural cause that generates both — most commonly an unclear ownership boundary where each team believes the other is responsible for something — because adjudicating between accounts creates a loser and leaves the generator in place.
- C) Assign ownership to one team.
- D) Bring in a mediator.

**Correct answer: B**

**Explanation:** Incompatible accounts of the same events usually mean two parties experiencing different consequences of one unresolved structural question, and both are describing something real. Option B looks for the generator, which is nearly always an ownership or decision-rights ambiguity. Your skills description names coaching the organisation on team dynamics and conflict resolution, and this is the substance of it. Option A is the instinctive move and produces a verdict, a loser and a recurrence. Option C may be part of the fix and arrives before the diagnosis. Option D outsources something your role names as yours.

**Question 11 (harder) — A strategy with no exclusions**

You are asked to write a frontend strategy for the department. What most determines whether it has any effect?

- A) That it is endorsed by senior leadership.
- B) That it says what the department will not do — which frameworks will not be supported, which patterns are out of scope, which needs will not be met centrally — because a strategy that only affirms good things gives nobody a basis for declining anything and therefore changes no decision.
- C) That it aligns with the wider government service standard.
- D) That teams are consulted in writing it.

**Correct answer: B**

**Explanation:** A strategy exists to settle questions in advance so individual cases do not have to be argued from scratch, and it can only do that by excluding. A document listing approved approaches without saying what happens to unapproved ones produces the same debate every time. Options A, C and D are all genuinely necessary — an unendorsed strategy is a document, a misaligned one gets overridden, and an unconsulted one is ignored — but they are conditions for effect rather than the thing that creates it.

**Question 12 (harder) — Representing the community publicly**

You are asked to speak publicly about your department's accessibility work. The reality is mixed: strong in some services, poor in others. What is the strongest approach?

- A) Present the strong examples; the talk is about what works.
- B) Present the strong work and be specific about what has not worked and why, because an honest account is more useful to the audience, more credible, and protects you from the discovery that the poor services exist — and because your own community will hear it and know whether you described their reality.
- C) Speak in general terms about the challenges.
- D) Decline until the picture improves.

**Correct answer: B**

**Explanation:** Two audiences are listening and option B is the only response that serves both. The external audience gets something useful, since the failures are the part other departments can learn from and the successes are the part they cannot easily copy. Your own community hears whether their head of profession described the department they actually work in, and a talk that presents only the good services is noticed immediately by everyone working on the others. Option A is what most such talks do. Option C avoids the risk and conveys nothing. Option D forgoes influence indefinitely, since the picture is always mixed.

### Preparation tips

- **Price a standard across the annual volume of compliance before mandating it.**
- **Read non-adoption by capable teams as friction, not ignorance.**
- **Get the missing account before acting on a characterisation.**
- **Look for the source-level fix when the same defects recur across teams.**
- **Assure against the standard, and change the standard if it is wrong.**
- **Treat consistent department-wide behaviour as structural.**
- **Define a strategy by what it excludes.**
- **Price a shared arrangement in decision speed, not just migration.**

### Common pitfalls to avoid

- **Mandating a practice without computing its recurring cost.**
- **Responding to non-adoption with communication.**
- **Acting on one party's characterisation of another team.**
- **Treating a recurring cross-team defect as a training need.**
- **Failing compliant work on preference.**
- **Adjudicating between two incompatible accounts.**
- **Writing a strategy that only says yes.**
- **Presenting only the successful services to an external audience.**

## Workplace job-specific numeric reasoning assessment

### About this assessment

A workplace job-specific numeric reasoning assessment tests whether you can reach a defensible conclusion from data at speed. At head-of-profession level the data is service-wide performance and accessibility metrics, capability and recruitment figures, the cost of standards across many teams, and the business cases you are asked to support or challenge.

The format is typically fifteen to twenty-five minutes with a calculator, mixing computation with interpretation. Interpretation dominates at your level, because most of the numbers you see were produced by someone making a case.

Three habits are worth naming.

The first is that percentages of a large public user base are people, and the conversion is the single most persuasive thing you can do with a number in front of a senior stakeholder.

The second is that any practice you mandate has a cost equal to its per-instance cost multiplied by the number of teams and the frequency, and you are the only person in the room likely to compute it.

The third is that aggregate service metrics hide the users your role exists to represent. A department-level accessibility score tells you almost nothing about whether a screen reader user can complete a particular journey.

### How this assessment maps to your role

- **Accessibility metrics** map to **Accessibility**, where you advocate for users with access needs.
- **Performance data** maps to **Web performance optimisation**, where you collect data from multiple tools.
- **Cost of standards** maps to defining and assuring best practice.
- **Capability and recruitment figures** map to developing departmental capability.
- **Portfolio metrics** map to **Strategic thinking**.
- **Presenting figures** maps to **Communicating information**.

### Practice questions

*Table 1 — Accessibility audit results across six services*

| Service | Annual users | Pages audited | Critical issues | Serious issues |
|---|---|---|---|---|
| Apply | 1,200,000 | 34 | 3 | 18 |
| Check | 480,000 | 12 | 0 | 4 |
| Register | 2,400,000 | 51 | 9 | 41 |
| Renew | 890,000 | 22 | 1 | 11 |
| Report | 160,000 | 18 | 4 | 9 |
| Update | 640,000 | 15 | 2 | 7 |

**Question 1 (easy) — Reading a table**

Which service has the most critical issues?

- A) Apply
- B) Register
- C) Report
- D) Update

**Correct answer: B**

**Explanation:** Register has 9 critical issues, ahead of Report's 4 and Apply's 3. Register is also the largest service by users and has the most pages audited, so before concluding anything note that a larger audit surface will tend to produce more findings — which the next questions address.

**Question 2 (easy) — Total exposure**

Approximately how many annual users are served by the services with at least one critical issue?

- A) About 5.3 million
- B) About 5.8 million
- C) About 4.4 million
- D) About 2.4 million

**Correct answer: A**

**Explanation:** All services except Check have at least one critical issue: 1,200,000 + 2,400,000 + 890,000 + 160,000 + 640,000 = 5,290,000, so about 5.3 million. That figure — five and a quarter million people using services with known critical accessibility issues — is the sentence that gets attention in a governance meeting, and it is more useful than any count of issues.

**Question 3 (moderate) — Normalising by audit surface**

Which service has the highest rate of critical issues per page audited?

- A) Register
- B) Report
- C) Apply
- D) Update

**Correct answer: B**

**Explanation:** Register 9/51 = 0.18; Report 4/18 = 0.22; Apply 3/34 = 0.09; Update 2/15 = 0.13. Report has the highest rate at 0.22 per page, slightly ahead of Register. Normalising by pages audited is the right correction, since a larger audit finds more issues at the same quality — and it changes the answer from Question 1, which is the point. Note that Report is also the smallest service by users, so the service with the worst rate affects the fewest people, which is a genuine tension in prioritisation rather than a contradiction.

**Question 4 (moderate) — Prioritising remediation**

Which service should be prioritised for remediation, and on what basis?

- A) Register, because it has the most critical issues.
- B) Register, because it combines the second-highest defect rate with 2.4 million users — so the number of people encountering a critical barrier is far larger there than anywhere else — although the honest caveat is that neither the table nor issue counts tell you which journeys are blocked, and one critical issue on a mandatory step matters more than five on a rarely-visited page.
- C) Report, because it has the highest defect rate.
- D) All six equally.

**Correct answer: B**

**Explanation:** The right basis combines rate with exposure, and Register dominates on the combination: a defect rate close to the worst, applied to a user base fifteen times larger than Report's. Option B reaches that conclusion and then names the limitation that matters most, which is that issue counts are not weighted by where the issue sits. That caveat is not hedging — it is the thing that should shape what you ask for next, which is a journey-level rather than a page-level view. Option A picks the raw count. Option C picks the rate alone. Option D declines to prioritise.

**Question 5 (moderate) — Cost of a mandated practice**

You are considering mandating two hours of accessibility testing per release. Fourteen teams release an average of 90 times a year each. What is the approximate annual cost in developer time?

- A) About 1,260 hours
- B) About 2,520 hours
- C) About 630 hours
- D) About 5,040 hours

**Correct answer: B**

**Explanation:** 14 teams × 90 releases = 1,260 releases a year. At two hours each: 2,520 hours, or roughly 1.4 full-time equivalents indefinitely. That is a real and permanent commitment, and it is the number nobody computes before mandating a practice. Whether it is worth it depends on what the testing catches that cheaper measures do not — but the conversation cannot happen honestly until the figure is on the table.

*Table 2 — Frontend capability, current position*

| Level | Posts | Filled | Average months in post |
|---|---|---|---|
| Junior | 12 | 7 | 9 |
| Mid-level | 26 | 24 | 21 |
| Senior | 14 | 9 | 34 |
| Lead | 5 | 5 | 41 |

**Question 6 (moderate) — Vacancy rate**

What is the overall vacancy rate across frontend posts?

- A) About 12%
- B) About 21%
- C) About 28%
- D) About 16%

**Correct answer: B**

**Explanation:** Total posts: 12 + 26 + 14 + 5 = 57. Filled: 7 + 24 + 9 + 5 = 45. Vacancies: 12, which is 12/57 = 21.1%. More than one post in five is unfilled, and the distribution matters more than the total: junior is 42% vacant and senior is 36% vacant, while mid-level is nearly full. That shape — a hollow at the bottom and at the top with a bulge in the middle — is a specific and diagnosable capability problem.

**Question 7 (harder) — What the shape shows**

What is the strongest interpretation of the distribution in Table 2?

- A) Recruitment is failing across the board.
- B) The pattern is consistent with a pipeline problem in both directions — junior posts unfilled means nothing is coming in, senior posts unfilled with mid-level nearly full means people are not progressing or are leaving before they do — and the 21-month average at mid-level against 34 at senior suggests mid-level turnover is the pressure point.
- C) Too many posts have been created.
- D) Senior recruitment should be prioritised.

**Correct answer: B**

**Explanation:** The two vacancy concentrations have different causes and the middle bulge connects them. A nearly-full mid-level tier with a third of senior posts vacant means either that mid-level people are not being promoted or that they leave before they are — and 21 months' average tenure at mid-level, against 34 at senior, points at the second. Option B reads the whole shape. Option A treats it as uniform when it plainly is not. Option D addresses the symptom by recruiting externally into posts your own mid-level people could fill, which would make the mid-level tenure figure worse.

**Question 8 (harder) — Recruitment arithmetic**

To fill the 5 senior vacancies externally, historical data shows an average of 40 applications per post, 6 shortlisted, 1.4 appointable, and 0.7 appointments made. Roughly how many campaigns are needed?

- A) 5
- B) 7
- C) 3
- D) 10

**Correct answer: B**

**Explanation:** At 0.7 appointments per campaign, filling 5 posts needs 5 / 0.7 = 7.1 campaigns. Each campaign consumes panel time, advertising and several weeks of elapsed time, so seven campaigns is a substantial commitment likely to run over a year. The value of the calculation is that it makes internal development a visible alternative rather than a vague aspiration — promoting three mid-level developers with support costs far less than four and a half campaigns, and addresses the tenure problem from Question 7 at the same time.

**Question 9 (harder) — A performance claim**

A supplier claims their optimisation service will improve Largest Contentful Paint by 30% across your services. Current 75th percentile LCP is 4.2s. What is the strongest assessment?

- A) That would bring LCP to 2.94s, which passes the 2.5s "good" threshold.
- B) A 30% improvement on 4.2s gives 2.94s, which still fails the 2.5s threshold at the 75th percentile — so even if the claim holds in full, the services would remain in the "needs improvement" band, and the question is whether that partial gain justifies the cost.
- C) The claim cannot be assessed without more information.
- D) A 30% improvement is implausible.

**Correct answer: B**

**Explanation:** 4.2 × 0.7 = 2.94s. Option A does the arithmetic correctly and gets the threshold wrong, which is the trap — 2.94s is above 2.5s, so it does not pass. Option B does both and draws the conclusion that matters: buying this does not get you to "good", so it needs justifying on its own terms rather than on reaching a threshold it does not reach. Knowing the Core Web Vitals thresholds (LCP 2.5s good, 4.0s poor, measured at the 75th percentile) well enough to apply them instantly is worth the memorisation at your level.

**Question 10 (harder) — Trend or noise**

Quarterly count of critical accessibility issues found across the department: 21, 17, 24, 15, 19, 14. A director asks whether accessibility is improving. What is the strongest answer?

- A) Yes; the count has fallen from 21 to 14.
- B) The series moves between 14 and 24 with a slight downward drift — the first three average 20.7 and the last three 16 — but the count depends on how much auditing was done each quarter, so without normalising by pages audited the series may be measuring audit activity rather than accessibility.
- C) No; the variation is too large.
- D) Yes, and the trend should continue.

**Correct answer: B**

**Explanation:** Two problems and option B names both. The statistical one is that six noisy points with a range of ten barely support a 23% difference between halves. The measurement one is more serious and specific to this metric: issues found is a function of issues present and looking, so a quarter with less auditing produces a lower count and looks like improvement. That is a metric that will be gamed unintentionally, which is worth flagging before it becomes a departmental target. Option A picks two endpoints. Option D extrapolates.

**Question 11 (harder) — Users behind a browser decision**

A browser accounts for 0.9% of sessions across services totalling 5.8 million annual users. Supporting a feature in it across all six services would take about fifteen developer-days. What is the strongest framing?

- A) 0.9% is too small to justify fifteen days.
- B) 0.9% of 5.8 million is about 52,000 users a year, so the decision turns on what those people cannot do without the work — if the baseline experience still lets them complete the task, fifteen days is poor value, and if it does not, 52,000 people annually is a strong case irrespective of the percentage.
- C) All browsers should be supported.
- D) 52,000 users justifies fifteen days.

**Correct answer: B**

**Explanation:** Neither the percentage nor the count settles it; what settles it is whether those users can complete their task through the baseline. Option B holds both facts and applies the right test — which is also an argument for progressive enhancement as an organisational standard, since a department that builds that way can answer this question calmly instead of arguing about market share. Option A treats the percentage as decisive; option D treats the count as decisive; option C ignores cost.

**Question 12 (harder) — Presenting to a board**

You have ten minutes with a departmental board to make the case for accessibility investment. Which figure leads best?

- A) The department's average accessibility audit score.
- B) The number of people using services with known critical barriers — around 5.3 million annually — alongside one concrete example of what a barrier means for one person trying to complete one task.
- C) The number of critical and serious issues outstanding.
- D) The legal risk of non-compliance.

**Correct answer: B**

**Explanation:** Option B pairs the number that establishes scale with the example that establishes meaning, and boards need both — a count of people without an example is abstract, and an example without a count is anecdote. Option C counts defects, which requires the board to understand what a critical issue is. Option A averages away everything of interest. Option D is real and belongs later in the ten minutes rather than first: leading with legal risk invites a compliance-minimising response, whereas leading with users invites a service-improving one, and you will get the compliance benefit either way.

### Preparation tips

- **Convert percentages into annual user counts.**
- **Normalise defect counts by audit surface before comparing services.**
- **Combine rate and exposure when prioritising remediation.**
- **Multiply a mandated practice by teams and frequency before proposing it.**
- **Know the Core Web Vitals thresholds and apply them to the 75th percentile.**
- **Read a vacancy distribution as a shape, not a total.**
- **Compute campaigns needed before assuming external recruitment is the route.**
- **Ask whether a count metric is measuring the thing or the looking.**

### Common pitfalls to avoid

- **Comparing raw issue counts across services with different audit sizes.**
- **Mandating a practice without its annual hour cost.**
- **Reading 2.94s as passing a 2.5s threshold.**
- **Treating "issues found" as a measure of issues present.**
- **Recruiting externally into senior posts while mid-level tenure is short.**
- **Leading a board conversation with legal risk.**
- **Presenting an average audit score as evidence about users.**

## Workplace job-specific verbal reasoning assessment

### About this assessment

A workplace job-specific verbal reasoning assessment tests whether you can determine exactly what written material establishes. At head-of-profession level the material is legislation and regulations, accessibility standards, cross-government agreements, assurance frameworks and departmental policy.

The commonest format gives a passage and asks you to mark statements True, False or Cannot Say. True means the passage establishes it, False means it contradicts it, and Cannot Say means neither — regardless of what you know. Deep expertise is the main hazard here, because you will supply from experience what the passage has left unsaid, and you will do it confidently.

Three specifics matter at your level.

The first is that accessibility regulations attach obligations with precise scope, timing and exemptions, and you are frequently the person other people rely on to read them correctly.

The second is that governance documents allocate authority in language that looks interchangeable and is not: approves, endorses, is consulted, is informed, may direct.

The third is that cross-government agreements are usually voluntary in their operative clauses however firm their preambles sound, and telling the difference determines what you can commit your department to.

### How this assessment maps to your role

- **Reading accessibility regulation** maps to **Accessibility**, where you advocate and assure.
- **Reading governance and assurance frameworks** maps to defining and assuring best practice.
- **Reading cross-government agreements** maps to collaborating with counterparts across government.
- **Reading strategy** maps to **Strategic thinking**.
- **Reading employment and capability guidance** maps to developing departmental capability.
- **Precision in public statements** maps to **Communicating information**.

### Practice questions

*Passage A — for Questions 1 to 4*

"Public sector bodies must ensure that their websites meet accessibility requirements and must publish an accessibility statement. Where meeting a particular requirement would impose a disproportionate burden, the body may rely on that exemption, provided it has carried out and documented an assessment of the burden and has stated the reliance in its accessibility statement. The disproportionate burden exemption does not apply to content that is essential to the use of the service. Pre-recorded time-based media published before 23 September 2020 is exempt. The assessment of disproportionate burden must consider the body's size and resources, the estimated costs and benefits, and the needs of disabled users."

**Question 1 (easy)**

Statement: A public sector body must publish an accessibility statement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly with "must", and unconditionally — the disproportionate burden exemption relates to meeting requirements, not to publishing the statement. Indeed the statement is where reliance on the exemption has to be declared, so the obligation is reinforced rather than reduced by the exemption.

**Question 2 (moderate)**

Statement: A body relying on the disproportionate burden exemption need not document its assessment provided it states the reliance in its accessibility statement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: the exemption is available "provided it has carried out and documented an assessment of the burden **and** has stated the reliance". Both conditions are required, joined conjunctively. The statement treats one of two conjuncts as sufficient, which is the commonest way conditions get misread. In practice this is the distinction between a defensible reliance and an indefensible one.

**Question 3 (moderate)**

Statement: A body can rely on the disproportionate burden exemption for a form that users must complete to access the service.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage states that the exemption "does not apply to content that is essential to the use of the service". A form users must complete to access the service is essential by definition. The passage contradicts the statement. This is the most consequential clause in the passage and the one most often overlooked, because disproportionate burden is usually invoked precisely when something core is expensive to fix.

**Question 4 (harder)**

Statement: A video published in 2021 is exempt from accessibility requirements if it is pre-recorded.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The exemption is for pre-recorded time-based media "published before 23 September 2020". A 2021 publication falls after that date, so the exemption does not reach it. The statement drops the date condition and keeps only "pre-recorded", which is exactly how this exemption is misapplied in practice — teams remember that old video is exempt and forget which video is old. Note the exemption is defined by publication date, not by recording date.

*Passage B — for Questions 5 to 8*

"The departmental assurance framework provides that services must pass a service assessment before entering public beta and before entering live. The head of frontend development is a standing member of the assessment panel for services with significant user-facing components, and may nominate a deputy. Panel decisions are reached by consensus; where consensus cannot be reached, the lead assessor decides and must record the dissenting views. A service that does not meet the standard is given a list of required actions and may be reassessed once the actions are complete. There is no limit on the number of reassessments. The framework is reviewed every two years."

**Question 5 (easy)**

Statement: Services must pass a service assessment before entering live.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** Stated directly, as one of two mandatory assessment points. Straightforward.

**Question 6 (moderate)**

Statement: The head of frontend development can block a panel decision they disagree with.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this. Decisions are reached by consensus, and "where consensus cannot be reached, the lead assessor decides and must record the dissenting views". So a standing member who withholds agreement does not block the decision; they produce a recorded dissent and the lead assessor decides. The mechanism is designed precisely so that one member cannot veto, and the recording of dissent is the compensation for that.

**Question 7 (moderate)**

Statement: The head of frontend development must personally attend assessments for services with significant user-facing components.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage says the head "is a standing member" and "may nominate a deputy". The power to nominate a deputy contradicts a requirement of personal attendance. Reading standing membership as a personal duty is the natural error, and the deputy clause exists to prevent it.

**Question 8 (harder)**

Statement: A service that fails an assessment twice cannot proceed to live.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage states that "there is no limit on the number of reassessments", which contradicts a bar after two failures. A service failing twice can be reassessed again, and again. That sentence exists to close exactly this inference, and it is worth noticing because the practical consequence runs against intuition — the framework has no failure ceiling, so a service is stopped by running out of time or appetite rather than by the rules.

*Passage C — for Questions 9 to 12*

"Departments participating in the cross-government frontend community agree to share reusable components where doing so does not conflict with departmental security requirements. Participation is voluntary and may be withdrawn on notice. The community maintains a register of shared components; inclusion in the register does not imply assurance by any department other than the contributing one. Departments are encouraged to align their frontend standards with the community's published guidance, and to notify the community where they diverge. The community's guidance is advisory and does not override departmental policy. Community meetings are held monthly and are open to all participating departments."

**Question 9 (moderate)**

Statement: A participating department must share its reusable components.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** Two features of the passage defeat "must". The sharing agreement is qualified — "where doing so does not conflict with departmental security requirements" — and participation itself "is voluntary and may be withdrawn on notice". An obligation that a party can exit at will, and that is conditioned on that party's own assessment of its security requirements, is not a requirement in the sense the statement asserts.

**Question 10 (moderate)**

Statement: A component in the register has been assured by the community.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage contradicts this: "inclusion in the register does not imply assurance by any department other than the contributing one". The clause exists to prevent exactly this reading, and it matters operationally — a team adopting a registered component is relying on the contributing department's assurance, not on a shared one, and needs to satisfy itself accordingly.

**Question 11 (moderate)**

Statement: A department must notify the community when it diverges from the community's guidance.

- A) True
- B) False
- C) Cannot Say

**Correct answer: B**

**Explanation:** The passage says departments "are encouraged to align ... and to notify the community where they diverge". Encouragement is not obligation, and the single verb "encouraged" governs both alignment and notification. The statement's "must" overstates it. In a passage that elsewhere uses "agree to" and "does not imply", the choice of "encouraged" is deliberate.

**Question 12 (harder)**

Statement: A department could adopt frontend standards that conflict with the community's guidance without breaching the agreement.

- A) True
- B) False
- C) Cannot Say

**Correct answer: A**

**Explanation:** The passage establishes this through two clauses working together: alignment is encouraged rather than required, and "the community's guidance is advisory and does not override departmental policy". A department adopting conflicting standards is therefore doing something the agreement permits — it is merely not doing something it was encouraged to do. Note this is True rather than Cannot Say because the passage explicitly settles the priority between community guidance and departmental policy, rather than leaving it open.

### Preparation tips

- **Treat conjunctive conditions as all required.**
- **Check the date qualifier on an exemption, not just its subject.**
- **Read "essential to the use of the service" as a hard limit on burden exemptions.**
- **Distinguish standing membership from personal attendance.**
- **Look for the clause that closes the obvious inference — it is usually there.**
- **Read "encouraged" as governing everything in its sentence.**
- **Note when a passage explicitly settles a priority — that makes a statement True, not Cannot Say.**
- **Check whether an obligation can be exited at will.**

### Common pitfalls to avoid

- **Treating one of two required conditions as sufficient.**
- **Applying a disproportionate burden exemption to essential content.**
- **Dropping the date from a time-based media exemption.**
- **Reading a standing panel seat as a veto.**
- **Assuming a failure limit that the framework does not contain.**
- **Reading register inclusion as shared assurance.**
- **Reading "encouraged to notify" as a notification duty.**

## Workplace job-specific situational judgement assessment

### About this assessment

A workplace job-specific situational judgement assessment presents realistic scenarios and asks you to identify effective and ineffective responses. At head-of-profession level the scenarios involve influence without direct authority, mediation between teams and departments, advocacy for users who are not in the room, and representing a community whose members will hear what you said.

The commonest formats ask for the most and least effective response, or for ratings of each. Scoring is against a key derived from experienced practitioners at comparable seniority, so the target is professional consensus.

Three patterns run through the strong answers.

The first is that your authority is mostly borrowed. Teams follow your standards because they respect them and you, and every time you spend that on something trivial you have less for something that matters.

The second is that you are frequently the only person present who represents users with access needs, which means silence from you is read as consent — and the people affected are never in the room to notice.

The third is that your community watches how you handle the difficult cases. Whether you defend a team under pressure, whether you tell an uncomfortable truth publicly, whether you hold a standard when holding it is expensive — these are the things that determine whether anyone brings you a problem next time.

### How this assessment maps to your role

- **Advocacy for users with access needs** maps to **Accessibility**.
- **Mediation and conflict resolution** maps to **Leadership and guidance** and **Community collaboration**.
- **Consensus across organisations** maps to building consensus between independent stakeholders.
- **Representing the community** maps to **Communicating information**.
- **Capability and career development** maps to internal mobility and career paths.
- **Standards leadership** maps to defining and assuring best practice.

### Practice questions

**Question 1 (easy) — A team under pressure from a programme**

One of your frontend teams is refusing to ship a component they say is inaccessible. The programme director is escalating to you. What is the most effective response?

- A) Ask the team to ship it and fix it afterwards.
- B) Get the specifics from the team, verify the claim quickly, and if they are right, back them publicly and take the conversation with the programme director yourself — because a team that holds a line correctly and is then overruled will not hold one again.
- C) Tell the programme director it is the team's decision.
- D) Broker a compromise.

**Correct answer: B. Least effective: A**

**Explanation:** The verification matters — you should not defend a position you have not checked — and once verified, the visible backing is the substance of the role. Taking the conversation yourself is the specific value you add: you can have a robust exchange with a programme director that a team lead cannot. Option A is least effective because it overrules a correct call and teaches the team that raising accessibility concerns produces trouble for them. Option C is technically accurate and leaves the team exposed. Option D presumes a middle exists before knowing whether the barrier is real.

**Question 2 (easy) — A standard nobody follows**

A coding standard you published eighteen months ago is widely ignored. What is the most effective response?

- A) Remind teams of the standard.
- B) Find out why it is not being followed before doing anything, since a standard ignored by capable teams for eighteen months is usually unworkable, unclear in scope, or more expensive than the alternative — and each of those has a different fix.
- C) Add it to the assurance criteria.
- D) Withdraw it.

**Correct answer: B. Least effective: A**

**Explanation:** Widespread non-compliance over that timescale is evidence about the standard, and the three candidate causes lead to different remedies: an unclear standard needs rewriting, an unworkable one needs relaxing, and an expensive one needs the cost removing, usually by supplying tooling that makes the compliant path the easy one. Option A is least effective because a reminder about an unworkable standard produces a fortnight of compliance and then the same position, while teaching everyone that your standards are advisory. Option C enforces before diagnosing. Option D discards a possibly-real need.

**Question 3 (moderate) — Conflict between two departments**

Your department and another are in dispute over a shared component, and it has reached your level. Both sides have dug in. What is the most effective response?

- A) Propose that your department maintains it.
- B) Get both parties to state what they each need the component to do, rather than what they want the arrangement to be — because entrenched positions about ownership usually conceal two sets of requirements that were never compared, and comparing them often shows the dispute is about something resolvable.
- C) Propose a shared maintenance arrangement.
- D) Suggest both departments maintain their own.

**Correct answer: B. Least effective: D**

**Explanation:** Your skills description names building consensus between highly independent stakeholders and unblocking issues between departments, and the technique that works is moving parties from positions to requirements. Two departments arguing about who owns a component frequently turn out to need different things from it, at which point the ownership question dissolves or becomes tractable. Option D is least effective because forking is the outcome that costs both departments permanently and looks like a resolution. Options A and C are proposals about arrangement, offered before anyone has established what is actually needed.

**Question 4 (moderate) — Accessibility in a room that has moved on**

In a senior meeting, a decision is being taken quickly that will make a service harder for screen reader users. Nobody else has raised it and the meeting is running late. What is the most effective response?

- A) Raise it now, briefly and specifically.
- B) Raise it now with the specific consequence and an estimate of what addressing it would cost — because silence from you is taken as professional endorsement, the people affected have no other representative in the room, and a decision taken now is far cheaper to influence than one revisited later.
- C) Raise it afterwards with the decision owner.
- D) Note it and address it during implementation.

**Correct answer: B. Least effective: D**

**Explanation:** Option A is right and option B is stronger for one reason: adding the cost estimate turns an objection into a decision the meeting can actually take in the time available. Without it, a late-running meeting will defer. Option D is least effective because "address it during implementation" for a decision that creates the barrier means designing around it at much greater cost, and often means not addressing it. Option C loses the room and the moment, and requires the decision owner to reopen something already settled.

**Question 5 (moderate) — A strong developer wants to leave the department**

An excellent senior frontend developer tells you they are leaving because the work has stopped being interesting. What is the most effective response?

- A) Offer them different work.
- B) Take the reason seriously and explore honestly what is available — different services, a cross-government secondment, a piece of community or standards work — and if nothing here genuinely fits, help them find the right thing elsewhere in government rather than losing them entirely.
- C) Ask what would keep them.
- D) Accept it and start recruitment.

**Correct answer: B. Least effective: D**

**Explanation:** Your role names facilitating internal mobility, and the widest useful frame is government rather than your department. Option B is honest about whether a fit exists here, which is what makes the offer credible, and treats keeping them in government as a real success rather than a consolation. Option D is least effective: starting recruitment before exploring anything both loses a strong person and signals to everyone else that departures are administrative events. Option C is a good question and, asked alone, invites a negotiation rather than an exploration. Option A offers a remedy before understanding what stopped being interesting.

**Question 6 (moderate) — Being asked to endorse something you have not seen**

A director asks you to add your name to a statement about the department's accessibility maturity, to be published externally. You have not seen the underlying evidence. What is the most effective response?

- A) Add your name; the director has asked.
- B) Ask to see the evidence first and say plainly that you will endorse what it supports — because your name on an accessibility claim is the department's main assurance that it is true, and it is worth exactly as much as your willingness to withhold it.
- C) Decline.
- D) Add your name with a caveat.

**Correct answer: B. Least effective: A**

**Explanation:** The endorsement's entire value is that you would not give it if it were false, which means checking is not an inconvenience but the thing itself. Option B is also constructive rather than obstructive — you are agreeing to endorse what is true, which is usually most of it. Option A is least effective because it converts your professional standing into a rubber stamp, and the first time a claim is challenged, both you and the department are exposed. Option D attaches a caveat that will be dropped. Option C refuses before looking.

**Question 7 (harder) — A cross-government commitment you cannot keep**

At a cross-government meeting, counterparts are converging on a commitment your department cannot realistically meet this year. Agreement is close and you are the only hesitation. What is the most effective response?

- A) Agree; a commitment is aspirational and others are in the same position.
- B) Say plainly what your department can commit to and by when, and why the fuller commitment is not achievable this year — because a commitment you know you will miss costs more than the awkwardness of saying so, and it is likely that at least one other department is in the same position and waiting for someone to say it first.
- C) Abstain from the commitment.
- D) Ask for the timeline to be extended.

**Correct answer: B. Least effective: A**

**Explanation:** Option B offers a real commitment instead of a nominal one, which is more useful to the group than unanimous agreement nobody meets — and the observation about other departments is usually true, since these commitments are rarely broken by only one party. Option A is least effective because it produces a collective agreement that quietly fails, which erodes the credibility of the whole forum. Option D is a reasonable move and is a request rather than a position, so it works better once you have stated what you can actually do. Option C withholds without contributing.

**Question 8 (harder) — Mediating between team members**

Two senior developers in your community are in a public and increasingly personal disagreement in a shared channel. What is the most effective response?

- A) Ask them both to stop and take it offline.
- B) Move it out of the channel immediately and then deal with the two things separately — the technical question, which is probably resolvable, and the conduct, which needs addressing on its own terms and does not become acceptable because the technical disagreement was genuine.
- C) Resolve the technical question so the argument ends.
- D) Speak to each of them privately.

**Correct answer: B. Least effective: C**

**Explanation:** Your skills description names understanding the psychology of a team and coaching the organisation on conflict resolution, and the substance is exactly this separation. Option B stops the public damage first — everyone in the channel is learning what is tolerated — then treats the two problems as two problems. Option C is least effective: settling the technical question rewards the escalation and leaves both of them believing the conduct worked. Option D is a necessary part of B and incomplete alone, since it does not stop the channel conversation. Option A stops the symptom without addressing either problem.

**Question 9 (harder) — Evidence against your own standard**

Data shows that a testing standard you introduced across fourteen teams costs substantial time and has not measurably reduced defects. What is the most effective response?

- A) Improve the measurement; some benefits are hard to capture.
- B) Publish the finding, including that it is your standard, and narrow it to where the benefit is demonstrable or withdraw it — because fourteen teams paying daily for an unmeasurable benefit is a real cost, and a head of profession who withdraws their own standard on evidence makes every remaining standard more credible.
- C) Retain it; testing standards prevent problems that never appear in defect data.
- D) Reduce its scope quietly.

**Correct answer: B. Least effective: C**

**Explanation:** The cost is certain and distributed; the benefit is unmeasured. Option B allows the right resolution — narrowing rather than abandoning — and gets the credibility benefit that comes from doing it openly. Option C is least effective because it is unfalsifiable, which makes it the argument that keeps every unproductive standard in place forever. Option D reaches a defensible outcome by a route that looks like concealment when noticed, and forgoes the demonstration that evidence changes your mind. Option A is legitimate in principle and indistinguishable from motivated reasoning when the person improving the measurement owns the standard.

**Question 10 (harder) — A supplier's inaccessible product**

A department-wide product being procured has significant accessibility problems. Procurement is well advanced and the business case is strong on other grounds. What is the most effective response?

- A) Raise the accessibility problems as a reason to stop the procurement.
- B) Set out the specific failures, what they mean for affected staff or users, and what the department's obligations are — then work the routes that exist at this stage, which are contractual remediation commitments with dates, an accessibility statement that reflects reality, and a documented decision by whoever accepts the risk.
- C) Accept it; the business case is strong.
- D) Escalate to the accessibility lead.

**Correct answer: B. Least effective: C**

**Explanation:** Late procurement is rarely stopped by an accessibility objection alone, and option B works the levers that genuinely exist at that stage — supplier remediation commitments written into the contract are the most effective of them, because a supplier facing a signature is more responsive than one holding one. The named risk acceptance matters too, since it ensures the decision is made by someone accountable rather than absorbed silently. Option C is least effective as it accepts a legal obligation being unmet without recording it. Option A is likely to fail and to be the last time you are consulted early. Option D is a good addition rather than a response.

**Question 11 (harder) — Speaking publicly about a failure**

A service in your department has been publicly criticised for accessibility failures. You are asked to speak about it at a cross-government event. What is the most effective response?

- A) Decline; it would be inappropriate while the issues are being fixed.
- B) Speak, and be specific about what went wrong and why — what the process missed and what has changed — because a candid account of a failure is the most useful thing anyone can offer that audience, and evasion in front of colleagues who already know what happened costs more than the failure did.
- C) Speak in general terms about accessibility challenges.
- D) Speak, focusing on the remediation work.

**Correct answer: B. Least effective: C**

**Explanation:** The audience already knows about the criticism, which removes the option of concealment and leaves only the question of whether you are useful about it. Option B treats the failure as material other departments can learn from, which is the genuine contribution, and it is also what your own community needs to hear from you. Option C is least effective — vague talk about challenges in front of people who know the specifics reads as evasion and damages your standing more than the original failure. Option D is a partial version that skips the part with the learning in it. Option A forgoes the influence.

**Question 12 (harder) — A senior colleague dismisses accessibility**

In a leadership meeting, a peer characterises accessibility requirements as "gold-plating" that slows delivery. What is the most effective response?

- A) Correct them firmly; accessibility is a legal requirement.
- B) Respond with the substance rather than the framing — what proportion of users are affected, what the legal position actually is, and the observation that most accessibility cost comes from retrofitting rather than from building accessibly — and follow up privately, since a peer who says this in a meeting is likely to act on it in decisions you are not in the room for.
- C) Let it go; arguing in the meeting will not help.
- D) Raise it with their line manager.

**Correct answer: B. Least effective: D**

**Explanation:** The remark needs answering in the room, because unanswered it stands as the meeting's position, and other people present will calibrate to it. Option B answers with facts rather than indignation, and includes the argument most likely to land with someone worried about delivery — that the expense they are objecting to is largely created by leaving it late. The private follow-up addresses the durable problem, which is the decisions they make elsewhere. Option D is least effective: going to a peer's line manager over a remark escalates a disagreement you have not yet had. Option A is right on the law and adversarial in a way that hardens the position. Option C leaves the framing unchallenged.

### Preparation tips

- **Verify a team's position, then back it visibly.**
- **Read long-standing non-compliance as evidence about the standard.**
- **Move disputing parties from positions to requirements.**
- **Raise an accessibility consequence with a cost estimate attached.**
- **Treat keeping someone in government as a success.**
- **Endorse only what you have seen the evidence for.**
- **Separate the technical question from the conduct.**
- **Withdraw your own standards openly when the evidence says so.**

### Common pitfalls to avoid

- **Overruling a team that held a correct line.**
- **Responding to non-adoption with a reminder.**
- **Letting a fork settle a cross-department dispute.**
- **Staying silent on an accessibility consequence in a late-running meeting.**
- **Lending your name to a claim you have not checked.**
- **Agreeing to a cross-government commitment you expect to miss.**
- **Resolving a technical question to end a personal argument.**
- **Speaking in general terms to an audience that knows the specifics.**

## Conclusion

You have worked through four assessments pitched at head of frontend development, and the themes are worth drawing together.

The cognitive section kept returning to the fact that everything you mandate is paid for by everyone. A standard's cost is its per-instance cost times fourteen teams times the release frequency, and computing that is your job because nobody else will. Non-adoption by capable people is friction rather than ignorance. The same three defects across nine services is a supply problem with a source-level fix. And a strategy that only says yes has changed no decision.

The numeric section was about making the invisible visible: 5.3 million people using services with known critical barriers; a vacancy distribution that is a shape rather than a total; seven recruitment campaigns to fill five posts; and the trap of a metric that counts issues found, which measures how much you looked as much as what is there.

The verbal section was about reading the documents that create your obligations. Both conjuncts of a condition are required. A disproportionate burden exemption does not reach content essential to using the service. A time-based media exemption is defined by publication date. A standing seat is not a veto, and register inclusion is not shared assurance.

The situational judgement section was about the borrowed authority the role runs on. The strong answers verified a team's position and then backed it publicly, raised accessibility consequences with costs attached so a late-running meeting could still decide, separated conduct from the technical disagreement underneath it, and — twice — told an uncomfortable truth in public because the alternative cost more.

If one thread runs through all of it, it is that your effectiveness is almost entirely a function of whether people believe you. Teams comply with standards set by someone who withdraws their own when the evidence turns. Programme directors listen to someone who checked before defending. Cross-government forums work when someone says what their department can actually deliver. That credibility takes years to build and a single rubber-stamped endorsement to spend.

Good luck. You are in a role where the people who most depend on your judgement are never in the room, and the care you have taken here is the right kind.
