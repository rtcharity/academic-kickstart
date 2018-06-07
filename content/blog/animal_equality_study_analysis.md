+++

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
categories = ["vaccines", "global health"]

# author = ["Marcus A. Davis"]
tags = ["animals", "farm animal welfare"]
date = 2018-06-07
draft = false
description = "How cost-effective is in person video advocacy for changing diets?"
# featured = "pic03.jpg"
# featuredalt = "Pic 3"
featuredpath = "date"
linktitle = ""
title = "Animal Equality showed that advocating for diet change works. But is it cost-effective?"
type = "post"
preview = true
# summary = "Animal Equality and Faunalytics put together a field study testing individual video outreach on belief and diet change. They found statistically significant results on both. Together with the Reducetarian study, we now think there is sufficient evidence to establish that individual outreach may work to produce positive change for nonhuman animals. However, evidence in this study points to an estimate of $310 per pig year saved (90% interval: $46 to $1100), which is worse than human-focused interventions even from a species neutral perspective. More analysis would be needed to see how individual outreach compares to other interventions in animal advocacy or in other cause areas."

+++

_This essay was jointly written by Peter Hurford and Marcus A. Davis. All code for analyses contained [is available on GitHub](https://github.com/peterhurford/personal/blob/gh-pages/tilde/files/ianimal/analysis.R)._

**Summary:** Animal Equality and Faunalytics put together a field study testing individual video outreach on belief and diet change. They found statistically significant results on both. Together with the Reducetarian study, we now think there is sufficient evidence to establish that individual outreach may work to produce positive change for nonhuman animals. However, evidence in this study points to an estimate of $310 per pig year saved (90% interval: $46 to $1100), which is worse than human-focused interventions even from a species neutral perspective. More analysis would be needed to see how individual outreach compares to other interventions in animal advocacy or in other cause areas.

## Introduction

Individual outreach for improving the lives of animals has [a lot of possible interventions](http://www.animalcharityevaluators.org/research/interventions/). While empirical evidence to help us understand and decide between these interventions has improved a lot over the past five years, there remain significant limitations in methodology. Previously, only the [the 2016 AWAL Newspaper Study](https://osf.io/nxrx3/) (see [announcements from the Reducetarian Foundation](http://www.awalab.org/2016/10/12/reducetarian-messaging-study/) and [from AWAL](http://www.awalab.org/2016/10/12/reducetarian-messaging-study/)) has the first statistically significant effect about individual outreach on actual meat reduction (as opposed to a proxy metric) using an actual control group with sufficient statistical power**[^1]**.

Now, a new study by Faunalytics, with cooperation from Animal Equality and Statistics Without Borders, enters the picture, purporting to find that video (in both 2D and 360-degree virtual reality) produces statistically significant diet change when compared with a control group (see [the full report](https://osf.io/r4zft/), [all the relevant data and code](https://osf.io/7wh93/), [Animal Equality announcement](https://www.animalequality.net/virtualreality-study), and the [Faunalytics announcement](https://faunalytics.org/video-outreach-impact-pork-consumption/)). Does this finding hold up?

## What is the basic methodology?

Participants were recruited across 35 different college campuses and across 86 days. Participants were placed into one of the three conditions (2D video, 3D video, or control / no video) based on a clustered RCT design, where each day each campus was randomized into a different condition for the entire campus-day. 3068 participants were initially recruited, received the treatment (or no treatment), and then filled out a questionnaire.

Participants were given up to seven email reminders and six text reminders to complete the survey, so non-response could be expected to be a sign of active disinterest rather than simply not remembering about the second survey. Participants were also incentivized with being entered into a lottery with the potential for one person to earn $1000\. 58% of people responded (1782 participants).

## What are the headline results?

Respondents were either shown a 2D video about the horrors of pig farming, a 360 VR video (using [new iAnimal technology](https://ianimal360.com/)), or no video (control group). Respondents in the two treatment groups were more likely to say that factory farming contributed to pigs’ suffering and that it was important to minimize the amount of pork one consumes compared to the control group at a follow up one month later. More importantly, the treatment group reported less consumption of pork at the follow-up. However, there was no statistically significant difference between the 2D and 360 VR video conditions.

## What are the results on attitudes, more specifically?

The study does a good job of mentioning which results are statistically significant and which are not and doing analysis controlling for a majority of factors. Given that we’re personally far more interested in whether video works as a medium rather than the difference between 2D and 360 VR video and given that the study did not find a significant effect between 2D and 360 VR, we found it much more convenient to pool the study into a single treatment and control group.

The study itself had two key measures of attitudes:

*   **Suffering attitude:** “Eating pork (bacon, ham, pork chops, spare ribs, bacon bits, etc.) directly contributes to the suffering of pigs.” (5-point Likert Scale, Strongly Disagree to Strongly Agree)

*   **Consumption attitude:** “It is important to minimize the amount of pork (bacon, ham, pork chops, spare ribs, bacon bits, etc.) a person consumes.” (5-point Likert Scale, Strongly Disagree to Strongly Agree)

_Impact on Suffering Attitude_

Immediately after the video, 67.0% of the control group and 79.4% of the treatment groups agreed or strongly agreed with the fact that eating pork contributed to suffering of pigs (p < 0.0001, Chi-squared test).

_Impact on Consumption Attitude_

Immediately after the video, 60.0% of the control group and 77.0% of the treatment groups agreed or strongly agreed with the fact that it is important to minimize pork eating (p < 0.0001, Chi-squared test).

## Did attitudes still hold at the one month follow up?

In a word: yes. Most of those who reported believing after watching a video that eating pigs contributed to their suffering and that it is important to minimize consumption still reported believing that one month later, and vice versa.

_Impact on Suffering Attitude_

At the one month follow up, 79.2% of the treatment group still agreed (compared to 79.4% on the baseline survey), while now 72.2% of the control group agreed in this statement (compared to 67.0% on the baseline survey). The difference remained statistically significant, even if it was smaller (p < 0.0001, Chi-squared test). However, we suspect that this uptick in the control group is not the result of a change in beliefs, but rather a change in who had responded to the second survey.

Of the 358 people in the treatment group who disagreed with the statement (remember this is after watching the video), 117 (32.7%) held their ground on the follow-up, 87 (24.3%) of them changed their mind, and 154 (43.0%) did not respond. Of the 1426 people in the treatment group who did agree, 798 (56.0%) of them still agreed, 113 (7.9%) had flipped to disagreeing, and 515 people (36.1%) did not respond.

Of the 390 people in the control group who disagreed with the statement (they did not see any video), 126 (32.3%) held their ground on the follow-up, 87 (22.3%) of them changed their mind, and 154 (39.5%) did not respond. Of the 1426 people in the treatment group who did agree, 798 (56.0%) of them still agreed, 113 (7.9%) had flipped to disagreeing, and 515 people (36.1%) did not respond.

Among both groups, agreement on the first survey was predictive of whether the respondent would respond on the follow-up survey (p < 0.0001, Chi-squared test).

_Impact on Consumption Attitude_

At the one month follow up, 75.8% of the treatment group still agreed (compared to 77.0% on the first survey), while now 67.0% of the control group agreed in this statement (compared to 60.0% on the first survey). This is the same story as before -- the difference is smaller now, but remains statistically significant (p < 0.0001, Chi-squared test), and appears to be largely driven by people dropping out between the two surveys instead of people changing their beliefs between the two surveys.

Of the 400 people in the treatment group who disagreed with the statement (remember this is after watching the video), 154 (38.5%) held their ground on the follow-up, 85 (21.3%) of them changed their mind, and 161 (40.3%) did not respond. Of the 1384 people in the treatment group who did agree, 761 (55.0%) of them still agreed, 116 (8.4%) had flipped to disagreeing, and 507 people (36.6%) did not respond.

I’ll spare you the same statistics for the control group, because as you can see this is basically a repeat. Obviously the people who didn’t answer about suffering attitude are the same people who didn’t answer about consumption attitude, because they didn’t answer any questions on the follow-up survey at all. However, even among those who did respond, the correlation between both attitudes is very high -- 0.457 on the baseline survey and 0.459 on the follow-up survey.

## What were the results on consumption, exactly?

But talk is cheap and what we want to see is whether talk translates into action. So let’s look at consumption change:

*   **Consumption change:** “Thinking about your diet over the past 30 DAYS, how often did you eat meals or snacks that contained ANY TYPE OF PORK (bacon, ham, pork chops, spare ribs, bacon bits, etc.)? NOTE: It is important that you report your food consumption as accurately as possible. Examples of meals include breakfast, lunch, dinner, etc. Also tell us about snacks between meals. Think about meals and snacks at home as well as outside the home. Please take your time and carefully consider your answer.” (Options: Never, 1-3 times per month, 1 time per week, 2-4 times per week, 5-6 times per week, 1 or more times per day)

Before any respondents were shown any video, they are asked retrospectively for the past thirty days, so presumably it should serve as a baseline, except insofar as they might have been primed or affected by social desirability bias to modify their baseline lower (more on this later). The follow up also asks about the last 30 days, so this would be the 30 days after the treatment (or lack thereof). We can thus calculate the change in diet between the baseline survey and the follow-up survey and compare this change between treatment and control groups to help factor out some of the baseline.

_Ordinal Scale Results_

The original study has this broken down by an ordinal scale. Looking at the mere difference in this scale between groups we get an average reduction of 0.144 on the scale from the control group and an average of 0.350 points from the treatment group (significant with p = 0.0004, two-sample t-test**[^2]**).

_Effect on Approximate Serving Sizes_

However, the ordinal scale is not very informative, since the steps between each point on the scale are very large… the difference between (1) Never and (2) 1-3 times a month is ~2 times a month, while the difference between (3) 2-4 times per week and (4) 5-6 times per week is ~10 times a month. To make things more complex for a moment, we offer up a simple transformation where each part of the scale is mapped to an average amount of times per month (Never -> 0, 1-3 times per month -> 2 times per month, 1 time per week -> 4 times per month, 2-4 times per week -> 12 times per month, 5-6 times per week -> 22 times per month, and 1 or more times per day -> 31 times per month). With this transformation, we can now extract a more meaningful statement -- the control group reduced ~1 time per month while the treatment groups reduced ~2 times per month (p = 0.0053, two sample t-test).

_Effect on Pork Elimination_

That being said, maybe we should reduce the complexity instead of increase it. How much do we really trust these self reports to be accurate? Do you remember how much pork you ate over the past thirty days? (Or, if you’re already vegetarian, try recalling the amount of times you ate spinach over the past thirty days.) Perhaps we can’t trust the absolute numbers, but we can trust one simple thing -- if people don’t eat any pork at all, they’d surely remember that. So we make a binary value -- 0 if they don’t eat pork at all and 1 if they report eating any amount of pork.

Looking at that, we find 33.4% of the control group and 31.6% of the treatment group report not eating pork on the first survey (a baseline since it asks about the time before the treatment and was answered before watching any video). On the follow-up one month later (reflecting retrospectively over the month since the study), the control group remains about the same now 32.5% not eating pork (a change of -0.9 percentage points), but the treatment group has jumped to 36.7% (a change of 5.1 percentage points). The differences between the groups are significant on the first survey (p < 0.0001, chi-squared test), significant on the follow-up survey but in the opposite direction (p < 0.0001, chi-squared test), and the overall difference in differences is significant (p < 0.0001, t-test). We can thus conclude that the treatment group does indeed report eating less pork than the control group, one month later.

_Effect on Pork Reduction_

And perhaps we can also look at reduction as a binary variable. The comparison in total servings of 1 per month by the control group and 2 per month by the treatment group may be misleading. It would be more accurate to say that the control group had 25.4% of people reduce an average of 9.96 times per month, 54.7% of people not change their diet, and 19.8% of people increase by an average of 7.69 times per month, whereas the treatment group had 32.8% of people reduce an average of 9.36 times per month, 54.2% of people not change their diet, and 13% of people increase an average of 7.84 times per month.

Comparatively, the amount of people not changing is roughly the same between both treatment and control, and the magnitude of increase and decrease being roughly the same between both treatment and control, but the treatment group having fewer increasers and more reducers. Looking just at reducers, we see 32.8% of the treatment group doing some amount of reduction (by 1 time or more) compared to 25.4% of the control group (p < 0.0001, Chi-squared test).

## But how does the differential non-response affect the consumption conclusions?

Astute readers will note that there was a significant effect of non-response on attitudes, where those who were less likely to agree with the attitudes were less likely to fill out the survey. Thus they got dropped, and the follow-up survey became overall more pig-friendly in part by selection bias. Could this mean that the difference in the treatment group is solely from pork-eating people still eating pork but not filling out the second survey?

_Differential Non-Response_

While non-response is an issue, it’s [differential non-response](https://en.wikipedia.org/wiki/Participation_bias), where the kinds of people who don’t respond are different from the kinds of people who do respond. ...That can really bias a study. For example, if those who were the least likely to think that eating pork contributes to pig suffering were the least likely to respond to the follow-up survey, then we’d expect some bias when assessing attitudes on the follow-up survey.

Unfortunately, there is a statistically significant effect going on here as well. Of the 1265 people in the treatment group who initially ate pork, 673 (53.2%) of them reported that they still ate some amount of pork, whereas 92 (7.3%) reported that they had now been 30 days pork-free. However, 500 pork-eating people in the treatment group (39.5%) did not respond. On the other hand, of the 532 people in the treatment group who already started out not eating any pork, 35 of them (6.6%) reported now eating pork, 319 (60.0%) reported staying pork-free, and 178 (33.5%) did not respond. The bottom line being that the non-response rate was much higher among those who initially ate pork. This effect is significant across both initial pork-eating status across both treatment and control (p < 0.0001, chi-squared test) and across treatment vs. control (p < 0.0001, chi-squared test).

_Re-looking at Pork Elimination_

So what can we do to analyze our results in light of this issue? We have the optimistic scenario, where we assume despite the above evidence that the non-response is random, and that we stick to our results as-is so far. But we also could make some assumptions about those who didn’t respond, such that they (a) did not change at all from the baseline or (b) they all ate pork between the baseline and follow-up and were too afraid to talk about it.

When we re-look at the pork vs. no pork results and assume that everyone who did not respond just didn’t change at all, there is now only a 3.2 percentage point shift instead of a 5.1 percentage point shift, but it remains significant (p < 0.0001, two sample t-test). This is encouraging and lends additional confidence to a significant effect of the treatment on reducing pork consumption.

However, if we assume that everyone who did not respond switched to or kept eating pork, we lose any significant effect (p = 0.44, two sample t-test). We’d strongly expect that this kind of shift would not have actually occurred, but it is useful for establishing a lower bound. We thus can confidently rule out hypotheses like “the treatment has a statistically significant backfiring effect of increasing pork consumption”.

Notably, the elimination has outsized effects over reduction. Of the people in the treatment group, people eliminating pork account for 5% of the treatment population but 24.1% of the total pork reduced among the treatment group. On the flip side, elimination is not the only aspect that matters, as the majority of the reduction in pork came from people reducing rather than eliminating.

_Re-looking at Approximate Serving Sizes_

When looking on a per-serving basis using our transformation described before but adding the assumption that everyone who did not respond underwent no reduction (and also no increase), we now arrive at a reduction of ~0.5 “serving” per person on average in the control group (down from ~1 before this adjustment) and ~1.3 per person on average in the treatment group (down from ~2 before this adjustment). The difference remains significant (p = 0.0004, two sample t-test).

_Re-looking at the Ordinal Scale_

We suppose we should also look back at the original ordinal scale -- while we think it is the least intuitive and the hardest to reason about of these three measures, it is how the question is actually asked, so it’s an important sanity check. When we assume that everyone who didn’t fill out the survey had no change on the ordinal scale, we see an average drop of 0.076 points on the scale among the control group (down from 0.144 among just the people in the without this adjustment) and an average drop of 0.218 points among the treatment group (down from 0.350 points) (significant with p < 0.0001, two-sample t-test).

## Are there any relevant confounders?

_Did the canopy matter?_

Much care was taken in the study analysis to look at potential confounders, and this is admirable. One particular debate was that of the canopy used to contain the study. The canopy was used to blind potential participants to the particular treatment, to prevent differential non-response. However, to keep conditions similar to how they would be in the field, a canopy with factory farming images was used, even in the control group. It is possible that this weakens the control group, since there is some exposure to negative factory farming images.

However, the exposure would still be much smaller for the control group than the treatment group, so while there may be some effect here, we are not that worried about this concern. If, for example, the average time watching the video of graphic animal suffering was ~5 minutes, and the average time spent focusing on images of suffering in the control condition is more like ~30 seconds as it isn’t a matter of directed attention or focus, there is a large difference in the amount of imagery being delivered between groups. Additionally, this can only work against the finding in this study, which would mean we are underestimating any potential effect, which makes our results even more robust.

A potential pilot might help us explore the impact of canopy. While 95% of participants were shown the typical canopy with animals, 2.8% of participants were shown a blank canopy with no pictures and 2.1% of participants were not shown any canopy. Pooling the typical canopy with animal pictures vs. the other two options does show a statistically significant effect on diet change (p = 0.036), but issues of statistical power and the fact that 85% of the times the non-typical canopy was used was during the treatment group skews this.  

Overall, we’d conclude that we should not worry about the effect of the canopy when interpreting these results.  

_Did spillover matter?_

While the clustered randomized design (where all participants on the same campus on the same day get the same condition) should limit the effect of spillover, the study still asked about whether people discussed the study with others. Only 3% of people said they did, so any spillover effect is likely quite small. There was no significant effect (p = 0.13), but any effect would likely have insignificant statistical power to detect at this size.

_Does watching to the end matter?_

The survey asked people if they watched to the end. 12.9% fessed up to not watching the entire video. Notably, people who did not watch to the end were less likely to fill out the follow-up survey, with only 49.6% of people who did not watch all the way responding, compared to 64.5% of those who did watch all the way (p < 0.0001, chi-squared test).

Contrary to what we may have expected, even when we assume non-responders had no diet change, there was no effect on watching the entire video and eating less pork (p = 0.47, two sample t-test). However, people who watched the video in entirety were less likely to agree that eating pork contributed to the suffering of pigs, with 79% of those who watched to the end agreeing vs. 86% of those who did not agreeing (p < 0.0001, Chi-squared test). Nearly identical effects were also obtained on the belief of minimizing pork, with 77% of those who watched to the end agreeing vs. 81% of those who did not watch to the end (p < 0.0001, Chi-squared test). This would be consistent with a hypothesis that those who did not watch to the end were not disinterested, but in fact overly interested and too emotionally invested to make it through all the footage. (Or the disinterested people who didn’t watch to the end just lied about it.)

_Did social desirability bias matter?_

A notable bias on surveys is that respondents just tell you what they think you want to hear. This is called [social desirability bias](https://en.wikipedia.org/wiki/Social_desirability_bias). It’s possible that this bias may inflate our results. To assess this, we can use a test called [the Marlowe-Crowne scale](http://faunalytics.org/social-desirability-bias/) that basically sees whether respondents will give more implausible but good sounding answers.

Marlowe-Crowne score had no connection to whether people reported eating less pork (p = 0.16, ANOVA) or whether people self-reported watching the entire video (p = 0.72, ANOVA). However, those higher in the Marlowe-Crowne score were slightly more likely to report believing that eating pork contributed to the suffering of pigs (p < 0.0001, ANOVA) and that it was important to minimize eating of pork (p < 0.0001, ANOVA), though the effect between those with a high Marlowe-Crowne score and those with a low Marlowe-Crowne score is less than one percentage point.

Another area social desirability bias may affect is whether people respond to the follow-up survey. Participants received as many as seven emails and six text message reminders sent over three weeks to get responses to the follow-up survey. This could lead to effects where those who didn’t respond initially could have been more likely to feel socially pressured if they did respond. In general, there could be differences in response between those who immediately responded and those that did not, particularly among baseline heavy pork-eaters. However, the connection between social desirability and answering the follow-up survey is not significant (p = 0.1939, ANOVA).

Overall, in so far as we can assess social desirability bias, we’d say it is not a huge factor in this study, but we’d still generally keep it in mind and watch out for it, as self-reported data about beliefs and diet change may be inherently suspect.

_Did west coast vs. east coast matter?_

The study tracked which coast they were recruiting from to see if there were any cultural differences. No statistically significant effect was obtained (p = 0.31, two sample t-test).

_Did the age of the participant matter?_

There was no effect by age on consumption (p = 0.31, ANOVA), but there were quite small yet statistically significant effects where older people were slightly more likely to believe that eating pork contributed to pig suffering (p < 0.0001, ANOVA) and that it is important to minimize the amount of pork one eats (p < 0.0001, ANOVA).

_Did the gender of the participant matter?_

As one would predict, men ate more pork (9 times per month on average) than other genders (6 times per month when pooled) on the baseline (p < 0.0001, two sample t-test) and this continued to be true after the 30 day follow-up with 6.7 times per month on average for men and 4.0 times per average for other genders (p < 0.0001, two sample t-test). However, there was no statistically significant difference in how much men reduced their meat intake in response to the treatment (p = 0.92, two sample t-test) or overall (p = 0.41, two sample t-test).

On the other hand, men were much less likely to endorse pro-pig beliefs, with 70% of men in the treatment group agreeing that it is important to minimize the amount of pork one eats compared to 83.2% of other genders (pooled) (p < 0.0001, two sample t-test) and 73.2% of men in the treatment group agreeing that eating pork contributes to the suffering of pigs compared to 84.9% of other genders (pooled) (p < 0.0001, two sample t-test).

The story is similar in the control group too, with 49% of men in the treatment group agreeing that it is important to minimize the amount of pork one eats compared to 69.2% of other genders (pooled) (p < 0.0001, two sample t-test) and 57.6% of men in the treatment group agreeing that eating pork contributes to the suffering of pigs compared to 74.8% of other genders (pooled) (p < 0.0001, two sample t-test).

_Does it matter that the population is overall so vegetarian to begin with?_

Notably, ~29.5% of the sample already did not eat pork throughout the entire past month at the baseline study. Relative to what would be expected of the general American public, this seems high. However, as the authors point out, “the representation of veg*ns in Animal Equality’s usual outreach is also unknown” ( [Faunalytics Study Report](https://osf.io/r4zft/), pg 28). We don’t know whether this is cause for concern or just typical of Animal Equality’s outreach.

There’s also an additional concern that these same trends may extend beyond those who ate no pork at all, to any who were attracted enough initially to complete the study. If the groups approached already heavily skew toward selecting for zero-pork eaters relative to the general population, it may also have heavily selected for people more susceptible to persuasion on the topic of meat-consumption. Again, this could help with generalizability to Animal Equality’s specific outreach but decrease the generalizability outside this domain. Moreover, given the scale of the study on each campus, it’s possible those most sympathetic in general to the study participated and there could be declining utility outside of such a target group.

Similarly there is some consideration of how those who rarely or never eat pork may bias the results downward and are not necessarily the primary targets of this type of intervention:

_“Figure 15 shows that the videos more frequently produced a decrease in pork consumption among high baseline consumers than low baseline consumers. This difference should not be surprising, in that those who rarely or never eat pork have little or no room to decrease their consumption further. This graph confirms that people who already consume little or no pork are, almost by definition, not the ideal target for this intervention.”_ - from [the Faunalytics Study Report](https://osf.io/r4zft/), pg 25

In the case of pork consumers who eat more than more than zero pork but less than average consumption among pork eaters, this could cut the other direction. People who already only consume a little pork could be more likely to cut it out since they may have already been more accepting of animal welfare considerations and have a smaller stake in sticking with current behaviors. On the other hand, these people have less room to decrease and obviously those already not eating pork can’t decrease at all! Without particular evidence to suggest otherwise, one might expect frequent pork consumers to rationalize their consumption when confronted with graphic footage suggesting direct harms.

## What is the cost-effectiveness? 

While it’s nice to know that these videos have a statistically significant effect on pork reduction, it doesn’t really matter unless the effect size is large enough that enough pork is reduced per dollar spent on the videos. We thus need to look at cost-effectiveness based on the amount of pigs spared per dollar spent.

_How much pork is not eaten?_

Figuring out the amount of pork not eaten due to the treatment is moderately straightforward as a result of the study. To do this, we can get the effect size of reduction of servings, convert from servings averted to actual amount of pig suffering averted, and then backtrack with the cost to run a video and get a cost-effectiveness estimate (in $USD per pig year averted) for running video.

The t-test for approximate serving size can give us a 95% confidence interval for the true difference in the treatment and control group. The initial analysis finds a range of 0.31 to 1.78 additional servings reduced by the treatment group, relative to the control group. After adjusting for non-response on the assumption that non-responders have no change, the new 95% interval is 0.33 to 1.16 additional servings reduced by the treatment group, relative to the control group. Given that the second interval is fully contained within the first interval and that there’s enough uncertainty about this, we can just go with the first interval.

_How long will the effects last?_

But how long will this effect last? We essentially want to translate the difference in pork eaten after one month to the lifetime difference among people in the control group. Animal Charity Evaluators [does a meta-analysis of two studies on vegetarian recidivism](https://animalcharityevaluators.org/research/dietary-impacts/vegetarian-recidivism/#report) and finds that the mean length of a vegetarianism period is 2.4 to 6.5 years.

Does that mean the effects of this study will last, as-is, for 2.4 to 6.5 years, on average? Maybe. It’s possible that the people in the study populations analyzed by ACE had a deeper conviction toward vegetarianism, on average, but it’s also possible that they don’t. Simply eating less pork is a much smaller commitment and easier to sustain, however it may be a much less strongly held conviction or it may not even be a consciously noticed choice at all. Thus while it is more sustainable, we don’t know if it more likely to actually be sustained.

It’s also possible that the typical vegetarianism period is the result of far more factors than just a video, and thus it would be unfair to assign the entire period to the video as we do here. On the other hand, it does feel a lot more plausible that maintaining pork reduction is a lot easier than maintaining vegetarianism. After all, [Faunalytics found](https://faunalytics.org/a-summary-of-faunalytics-study-of-current-and-former-vegetarians-and-vegans/) that lapsed vegetarians still ate less meat than people who were never vegetarian.

Taking all this together, we arbitrarily extend the range to assume a 90% confidence interval that the pork reduction observed in the study will last for a total of 1 to 12 years**[^3]**. We can then calculate the lifetime reduction of pork by multiplying this value and the amount of pork reduction per month. When we do so, we calculate that people in the treatment group will eat pork 58 fewer times than people in the control group (90% interval: 14 to 180).

_How much pig is not eaten?_

But how many pigs are saved when people eat pork 58 times less? Well, if we assume that each time someone eats pork they are [eating 2 to 6 ounces of it](https://fns-prod.azureedge.net/sites/default/files/fgp_sizes.pdf) and that [a typical pig produces 200-230 pounds of meat](http://reducing-suffering.org/how-much-direct-suffering-is-caused-by-various-animal-foods/) , that means the typical person eating pork 58 less times will be eating one sixteenth less of a pig in their life (90% interval: 0.013 to 0.21).

Lastly, we need to adjust for product elasticity -- the amount that the supply of pork will fall when demand for pork falls. A reduction of pork consumption reduces demand, but the effect on supply is not 1-to-1\. [Research by Animal Charity Evaluators into product elasticity](https://docs.google.com/spreadsheets/d/1iNDQIt9MRD4r1ws5M_2hQ-MNjMY-bcUra0fpOmF4Am0/edit#gid=0) finds that reducing demand for pigs by 1 pig will cause a corresponding decline in pigs supplied of 0.57 (90% interval: 0.42 to 0.87). Thus the reduction in demand of one sixteenth of a pig corresponds to sparing 0.03 pigs (90% interval: 0.0075 to 0.13).

Given that a typical pig lives about six months, each person in the treatment group is thus sparing ~1 week of pig suffering (90% interval: 1.3 days to 23.7 days).

_What are the costs?_

So we know the benefits… now we need to know the costs. This study did not use the common “pay per view model” where people are incentivized to watch the video with a nominal cash prize (typically $1), so that means the costs really are just staff pay of setting up and running the booth, plus the fixed costs of buying all the equipment amortized over each individual. If we’re being truly scrupulous, we may be inclined to include opportunity costs of the staff and volunteers as well.

It appears that for each tour group, there were 1-2 staff members and 2-3 volunteers. Also, the 2D video involved 8 tablets per tour and the 360 VR video involved 6 VR headsets per tour. While this study reached ~36 people per day, Che Green at Faunalytics says that when not encumbered by running a study, Animal Equality is typically able to reach 70-100 people a day, though the number can have a high degree of variation, going as low as 7 and as high as 219\. Assuming outreach is run ~200 days a year (my guess) and the reach is somewhere between 50-130 people, that would be 10K-20K people reached per year by each tour team.

Assuming equipment costs of [~$600 per VR headset](https://www.theverge.com/a/best-vr-headset-oculus-rift-samsung-gear-htc-vive-virtual-reality) and [$150 per tablet](https://www.laptopmag.com/articles/tablet-buying-guide) and assuming they last for about five years, each VR headset costs $0.60 per day used and each tablet costs $0.082 per day used. With 6 headsets used per day and reaching ~70 people per day, that works out to $0.051 per person reached in headset costs. With 8 tablets per day and reaching ~70 people per day, that works out to $0.009 per person reached in tablet costs. Assuming staff pay of $150 per day ($30K/yr over 200 days), that works out to $2.14 per person reached in staff costs -- equipment costs are negligible in comparison. Thus the costs to reach a person with 2D video is ~$2.15, whereas the costs to reach a person with 360 VR video is ~$2.19.

_So what’s the cost-effectiveness?_

Given that a person can be reached for ~$2 and that they spare ~1 pig week, that works out to $150 per pig saved (90% interval: $23 to $560) and, again assuming that each pig has a ~6 month lifespan, that works out to $310 per pig year saved (90% interval: $47 to $1100). To put this in context, Against Malaria Foundation can avert a year of human suffering from malaria for $39**[^4]**, this does not look very cost-effective.

This is all summarized [in this Guesstimate model](https://www.getguesstimate.com/models/10871).

_But what if it were chicken?_

A key part undermining the cost-effectiveness is that each pig produces so much pork. If we re-run the numbers assuming that the study was talking about chicken instead of pork and had the same results, but adjusted all the other numbers to be about chicken, we get $5.70 per chicken spared (90% interval: $0.71 to $32) and $50 per chicken year (90% interval: 6.3 to 280). This is better, but presumably still not as good as helping humans (even from a complete species-neutral point of view). This is summarized [in this additional Guesstimate model](https://www.getguesstimate.com/models/10897).

_How does this compare to the Reducetarian study?_

Previously, [one of us analyzed the Reducetarian study](http://effective-altruism.com/ea/14g/thoughts_on_the_reducetarian_labs_mturk_study/), which as far as we know is the only other sufficiently high-powered study with a sufficient control group, adequate methodology, and a focus on a diet-related outcome. In that study, participants were recruited via Amazon’s Mechanical Turk and in the treatment groups, on average, changed their diet to eat 0.8 less servings of turkey, pork, chicken, fish, and beef per week than those in the control group, or 3.2 total servings per month.

This is more than 3x the size of the effect found here in the Animal Equality study, but it was notably across all kinds of animals and not just pork. An analysis of the data from the Reducetarian study on just pork in particular finds a reduction of 0.241 servings among the treatment groups (pooled) and an increase of 0.104 servings among the control group (p = 0.009, two sample t-test). The 95% confidence interval is that the difference lies between 0.087 and 0.605 servings reduced by the treatment group after controlling for the effect on the control group, which is actually 2x less than what is found in the Animal Equality study. Thus the Animal Equality videos may be twice as effective (at least for pork) though twice as expensive to run.

We don’t really know what would happen if we were to extrapolate the results of the Animal Equality study to diet changes on all animals. It makes sense that the effect on pork would be higher than usual given that the treatment specifically focused on pigs. It is certainly possible that this effect would produce broader effects on reducing meat generally. However, it is also possible that there is a substitution effect where people eat less pork but start eating more chicken instead in a way that might actually be net negative. While some initial analysis like the Reducetarian study and [Faunalytics’s study of vegetarians](https://faunalytics.org/wp-content/uploads/2016/02/Faunalytics-Study-of-Current-and-Former-Vegetarians-and-Vegans-%E2%80%93-Secondary-Findings-.pdf) do not find a substitution effect when they could, we still don’t yet have enough evidence to rule this out.

_How does this compare to ACE’s assessment of Animal Equality?_

Animal Charity Evaluators produced [a comprehensive review of Animal Equality](https://animalcharityevaluators.org/charity-review/animal-equality/#comprehensive-review), including [this Guesstimate estimate](https://www.getguesstimate.com/models/9590?token=sSMogCCGAhX_PxpHvvOxEp_lP376AAmzJ3YL2XKYMqebUal1E8zL86vNw7-ZQRcPFKDkKAaATiN3g9CDuj5XVA). ACE used leafleting as their baseline for understanding the impact on animals, where each leaflet is taken to reduce ~4 farmed animal days on average (90% interval: -255.5 days to 324.85 days) (see cell SCI3 in the top right of the Guesstimate).

However, it is assumed by ACE that 2D video would be ~3x as impactful as leafleting (90% interval: 1x to 8.7x), which magnifies the effect to ~58 days (90% interval: -620.5 days to 1971 days) for 2D video. Furthermore, 360 VR video is assumed to be ~6x as impactful as leafleting (90% interval: 2.1x to 14x), which magnifies the effect to ~40 days (90% interval: -1314 days to 2591.5 days)**[^5]**. With a cost per person reached of ~$2.20 (90% interval: $1.90 to $2.60), that would work out to $500 per animal year saved from 2D video and $350 per animal year saved from 360 VR video.

While based on the results in this study, we think we can reject the hypothesis that 360 VR video is twice as effective per person as 2D video**[^6]**, it is notable that this calculation is not too different from what we established above.

## What did this study not find?

Notably, this study did not look at any effects other than pork, which could be problematic as it needlessly constrains the cost-effectiveness estimate to focus on the relatively expensive to help pigs compared to other animals, or even all animals as a whole. As the Reducetarian study found, broad reduction across all possible animal consumption would outweigh in effectiveness a reduction of consumption in any one animal.  

On the other hand, there still is an open question, as [the Faunalytics design document for this study notes](https://osf.io/g27xv/) , about how to handle the fact that self-reporting your diet across a ton of different animals is really hard. Certainly focusing on just pork does simplify things. More research on how people interact with these food frequency questionnaires and what questions to ask may be merited.

## How should we cautiously interpret these results?

It’s great to see a robust study of any sort that looks at diet change with sufficient statistical power from a large sample and that gets statistically significant effects that are robust from cutting the data under different approaches (e.g., binary elimination, converting to serving sizes, etc.) and almost entirely robust after correcting for multiple hypothesis testing**[^7]**. The fact that this study took place in the field with reasonably close conditions to what would obtain in reality, as opposed to being in Mechanical Turk, is all the more encouraging. At this point, we’d be willing to believe now that there is a substantial chance that at least some forms of individual animal advocacy work.

However, by “they work”, we mean that they produce net positive results. Whether they are genuinely cost-effective compared to our alternatives is still something that remains to be established, and this study establishes a discouraging initial cost-effectiveness estimate. It’s possible that some elements of the study design (such as the canopy or the survey itself) may have reduced the true effect of Animal Equality’s program. It’s also possible that looking at diet changes more expansively may produce more encouraging results. Perhaps it would be a good idea to replicate this study, but look more at all kinds of diet change to try to see if we can get evidence that establishes a better cost-effectiveness estimate.

It is still too early to say we should reconsider individual outreach. For one, it is hard to compare video to other individual outreach strategies -- or even non-outreach strategies for that matter -- given the lack of robust cost-effectiveness estimates for other areas. Also, it is possible that individual outreach may have important medium term effects and/or fit into a broader holistic strategy.

_Thanks to Jo Anderson, Che Green, and David Moss for reviewing this piece._

## Endnotes

[^1]: Other prior work is plentiful, but had either an insufficiently large sample size to find significant effects (e.g., [ACE 2013 Humane Education Study](http://www.animalcharityevaluators.org/research/interventions/humane-education/humane-education-study-fall-2013/);[MFA 2016 Online Ads Study](http://effective-altruism.com/ea/y2/more_thoughts_and_analysis_on_the_mercy_for/)), had an insufficient control group size (e.g., [ACE 2013 Leafleting Study](http://everydayutilitarian.com/essays/a-re-analysis-of-ace-leaflet-study/);[2014 FARM Pay-per-view Study](https://ds.lclark.edu/sge/wp-content/uploads/sites/121/2014/05/Broughton-Thesis-Final-PDF.pdf);[VO 2015 Leafleting Study](http://veganoutreach.org/les-fall-2016/); [Ferenbach, 2015](https://repository.asu.edu/attachments/158042/content/Fehrenbach_asu_0010E_15253.pdf); [Hennessy, 2016](https://www.ideals.illinois.edu/bitstream/handle/2142/92865/HENNESSY-THESIS-2016.pdf)), had no control group (e.g., [THL 2011 Online Ads Study](http://reducing-suffering.org/wp-content/uploads/2014/10/FacebookAdsSurveyResults2011.pdf); [THL 2012 Leafleting Study](https://ccc.farmsanctuary.org/the-powerful-impact-of-college-leafleting/); [THL 2014 Leafleting Study](http://www.humaneleaguelabs.org/blog/2014-05-20-what-elements-make-vegetarian-leaflet-more-effective/); [THL 2015 Leafleting Study](http://www.humaneleaguelabs.org/blog/2015-09-20-which-request-creates-most-diet-change/); [VO 2015 Pay-per-view Study](http://veganoutreach.org/les-fall-2016/); [James, 2015](https://mpra.ub.uni-muenchen.de/66737/1/MPRA_paper_66737.pdf); [Veganuary, 2015](https://veganuary.com/blog/many-animals-veganuary-save/); [Veganuary, 2016](https://veganuary.com/wp-content/uploads/2016/07/Veganuary-2016-Research-Results-Lives-Spared-Addendum.pdf); [Veganuary, 2017](https://veganuary.com/blog/did-veganuary-2017-help-animals/); [Mensink, 2017](https://osf.io/b3xzs/)), only measured intent to change diet rather than actual self-reported diet change (e.g., [Arbour, Signal, & Taylor, 2009](http://booksandjournals.brillonline.com/content/journals/10.1163/156853009x418073); [Jamieson, et. al, 2012](https://www.researchgate.net/profile/Lucy_Asher/publication/215570388_Measuring_the_success_of_a_farm_animal_welfare_education_event/links/0912f50ca8bd8ed5f1000000.pdf); [Rule & Zhbanova, 2012](https://link.springer.com/article/10.1007/s10643-012-0520-2); [MFA 2016 MTurk Study](http://www.mercyforanimals.org/welfare-reforms-survey); [2016 Retargeting Online Ad Study](http://effective-altruism.com/ea/xb/mfa_ad_study_targeting_former_vegetarians/)), or did not attempt to measure differences against a baseline prior to the intervention (e.g., [VO 2014 Leafleting Study](http://veganoutreach.org/pay-per-read-study-results/); [CAA 2015 VegFest Study](https://www.exploreveg.org/files/2015/12/StatcomReport-TCVegFest2014.pdf); [VO 2016 Leafleting Study](http://veganoutreach.org/ppr-2016/); [Ardnt, 2016](http://krex.k-state.edu/dspace/bitstream/handle/2097/32159/ChelseaSchnabelrauchArndt2016.pdf)). This is a list of all the relevant individual veg outreach research we know of, if you can name any more, we’d be happy to add them to this literature overview.

[^2]: We chose simpler (and arguably less correct) statistical tests than the ones used by Faunalytics as we wanted to see whether the effects still prevailed under them and because they were easier to reason about.

[^3]: This effect is modeled as a linear extrapolation where the effect remains constant for an amount of time and then immediately drops to 0\. This of course is unrealistic, but this is not a concern as it is mathematically equivalent to a declining curve of effect that is longer in duration.

[^4]: GiveWell has pretty thoroughly vetted the Against Malaria Foundation and found it to create the equivalent value of saving the life of a child under 5 for $764 to $3057 (average $2087) ([GiveWell, 2018](https://www.givewell.org/how-we-work/our-criteria/cost-effectiveness/cost-effectiveness-models)). While GiveWell would not want us crudely converting this figure to DALYs, we need to do so to have a remotely comparable analysis, so we consider saving the life of a child under 5 to allow them to live to the typical life expectancy of SSA – [59 years total](https://data.worldbank.org/indicator/SP.DYN.LE00.IN?locations=ZG), or an additional 53 years – at full health, which would be 53 DALYs averted. Thus, AMF would be at ~$15 - $58 per DALY averted (average $39).

[^5]: It is strange that this leads to us concluding that the 2D video is more effective than the 360 VR video, despite ACE explicitly giving the 360 VR video a higher multiplier. This is due to the fact that ACE estimates also include a substantial chance of negative effect and that this is also magnified by the multiplier.

[^6]: Of course, Animal Equality argues that while their 360 VR video may have lower short-term cost-effectiveness due to higher cost and no statistically significant increase in conversion rate, it makes up for this by being novel, thus drawing in larger crowds and being more likely to draw in people who may be more influential. This additional hypothesis is plausible but untested. Notably, staffing costs dominate the costs of equipment in the model, so running 360 VR may not be that much additional expense per person recruited, so it may not matter too much.

[^7]: Given that 38 statistical tests were conducted, following the [Benjamini-Hotchberg procedure](https://en.wikipedia.org/wiki/False_discovery_rate#Benjamini%E2%80%93Hochberg_procedure), we ideally should reject p-values above 0.0013\. The only statistically significant effect in this data with a p-value above that threshold is the difference between the amount of servings reduced between the control group and the treatment group (p = 0.0053, two sample t-test). However, this procedure for multiple hypothesis testing is very stringent.