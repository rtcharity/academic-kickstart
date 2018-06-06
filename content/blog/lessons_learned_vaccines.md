+++

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
categories = ["vaccines", "global health"]

# author = ["Marcus A. Davis"]
tags = ["vaccines", "global health"]
date = 2018-06-05
draft = false
description = "What did we take away from our work on vaccines"
# featured = "pic03.jpg"
# featuredalt = "Pic 3"
featuredpath = "date"
linktitle = ""
title = "Lessons for estimating cost-effectiveness (of vaccines) more effectively"
type = "post"
preview = true
# summary = "We investigated the cost-effectiveness of vaccine research and development to learn about how cost-effectiveness estimates are made and where they might go wrong. By doing this, we became far more wary of taking these estimates literally. Many people will do things like reducing their cost-effectiveness estimate by a factor of 10x and call this a conservative estimate, but in light of this exercise and other examples, this is not enough. Furthermore, our research underscored that donating to the Against Malaria Foundation (AMF) may be a really hard baseline to beat and that it is important to do some degree of investigation before assuming things beat AMF."

+++

*This essay was jointly written by Peter Hurford and Marcus A. Davis.*

**Summary:** We investigated the cost-effectiveness of vaccine research and development to learn about how cost-effectiveness estimates are made and where they might go wrong. By doing this, we became far more wary of taking these estimates literally. Many people will do things like reducing their cost-effectiveness estimate by a factor of 10x and call this a conservative estimate, but in light of this exercise and other examples, this is not enough. Furthermore, our research underscored that donating to the Against Malaria Foundation (AMF) may be a really hard baseline to beat and that it is important to do some degree of investigation before assuming things beat AMF. Lastly, our research has some implications for biosecurity that merit further exploration.

**Introduction**

We set out to figure out [how cost-effective it would be to create a new vaccine](http://effective-altruism.com/ea/1o6/what_is_the_costeffectiveness_of_researching/). After a lot of work, we came to a reasonable conclusion. The next question after doing all this is ...why?

We certainly don’t plan to manufacture our own vaccine anytime soon and weren’t thinking of funding others who might. This might puzzle people as to why we did all this research. The reason: it was a good sandbox to get our start in. We were hoping to learn more about cost-effectiveness estimation in a domain where the answer was not known but the data and sources were relatively plentiful and it was easy to compare to other academic work. If we can’t create meaningful cost-effectiveness estimates for vaccine research and development, what kind of cost-effectiveness estimates might we be able to make?

**Lesson #1: The chance of error is substantial and all estimates should be suspect!**

One of the major lessons we take away from this is in a historical analysis, even when the underlying issue is well documented, model uncertainty can be very high. **Many people will do things like reducing their cost-effectiveness estimate by a factor of 10x and call this a conservative estimate, but this is not enough.** Throughout our time working on vaccine cost-effectiveness, we would regularly see our estimate change by a factor of 6x because we misplaced a parenthetical, then see our estimate change by a factor of 20x (!!!) in the other direction because we forgot a crucial consideration.

Additionally, these assumptions really matter -- while our 90% confidence interval only varied by one order of magnitude, additional changes in fundamental underlying assumptions could very well have change the endline estimate by another two orders of magnitude in either direction. If we were working in a less established domain, we would not be surprised to find our estimate being off by many orders of magnitude.

And it’s not just novices like us that are likely to make sizable errors like this:  


- The DCP2 estimates of deworming, done by multiple well credentialed economists, [were off by multiple orders of magnitude](https://blog.givewell.org/2011/09/29/errors-in-dcp2-cost-effectiveness-estimate-for-deworming/).
- When rating bonds, Moody’s thought they were being careful by adding a 50% buffer, giving them a lot of room to be off in their errors. ...[They were off by 20,000% right before the 2008 financial crisis](https://www.gpo.gov/fdsys/pkg/GPO-FCIC/pdf/GPO-FCIC.pdf).  
- [Freakonomic’s famous headline claim of abortion’s impact on declining crime rates](https://www.economist.com/node/5246700) ended up being completely wrong due to a spreadsheet error.
- The Princeton Election Consortium [gave Hillary Clinton a 99% chance of victory over Donald Trump](https://www.independent.co.uk/news/world/americas/sam-wang-princeton-election-consortium-poll-hillary-clinton-donald-trump-victory-a7399671.html). We all know how that turned out.
- GiveWell originally thought [Village Reach would save a life for $1000](http://www.givewell.org/international/top-charities/villagereach/December-2009-review#Whatdoyougetforyourdollar), but now they’re not sure[if Village Reach even worked at all](https://blog.givewell.org/2012/07/26/rethinking-villagereachs-pilot-project/).  
- Effective altruists originally thought the Fred Hollows Foundation [could avert blindness for $50](https://www.thelifeyoucansave.org/where-to-donate/fred-hollows-foundation). But GiveWell [found those estimates suspect](http://blog.givewell.org/2008/07/21/preventing-blindness/).  
- Effective altruists (sadly, including one of us) [previously thought that leaflets could avert a year of nonhuman animal suffering for as little as two cents](http://everydayutilitarian.com/essays/how-much-does-it-cost-to-buy-a-vegetarian/)! Now [we’re unsure if leafleting has any effect at all](https://animalcharityevaluators.org/advocacy-interventions/interventions/leafleting/#report).
- GiveDirectly, thought to be one of the easiest to understand interventions in improving global poverty that even served as the benchmark by GiveWell for understanding other interventions, [ended up being potentially more confusing and less effective than we originally thought](https://blog.givewell.org/2018/05/04/new-research-on-cash-transfers/).

In general, this exercise has made us witness the above first hand as we corrected as we thought we were finally right, only to then discover a bunch of errors.

At nearly every stage of modeling there are some possible tradeoffs between reasonable inputs where decisions have to be made. Questions like “how many deaths have a given vaccine prevented over period X?” involve making a number of choices about accounting for leverage, counterfactuals about the case and death rates in the absence of a vaccine, and knowledge of vaccine rate, efficacy, and population at all times in the given period. For example, holding all other inputs [in our model](http://effective-altruism.com/ea/1o6/what_is_the_costeffectiveness_of_researching/) constant, [if we raise the estimated efficacy](https://docs.google.com/spreadsheets/d/18zUqZMrV7UvzYGXmOowSLvdS1pX5_GA8dgIxd8A2_yM/edit#gid=0) of the malaria vaccine from 39%, which current studies suggest it is, to 75%, a figure more in line with other licensed vaccines, the cost effectiveness nearly doubles from ~$58 per DALY to ~$30 a DALY.  Similar differences occur when changing the estimated price per person of vaccines.

Extrapolating from these initial inputs to try to estimate cost-effectiveness brings another round of uncertain decisions on how to count roll out costs, what is the fixed cost when rolling out a vaccine, what is the population to be targeted, how to count health spending by governments that lead to more direct research and development spending, and what is an economic benefit. Narrowing or widening definitions at each of these steps can change the results of your analysis significantly. Further, all of these inputs can be difficult to trace, particularly research and development spending, even in a field as well-documented as vaccination. This gives us reason to think that, at most, our analysis narrowed the range of possible values for the value of vaccination. The uncertainty around many of these key inputs also underscores the need to clearly identify and highlight the key logic and assumptions of the model.

**Lesson #2: It’s good to look at the problem from multiple angles**

So if we’re overwhelmingly likely to make a few errors in our estimates that make us off by a large amount, what can we do to guard against this? One idea is to look at things from multiple angles. When constructing our estimate, we looked at things from four key angles and made sure they all matched up or we understood why they were wrong:

*   A Guesstimate model for each vaccine we wanted to model
*   A spreadsheet with scenario-specific estimates with a more simple model
*   Reference to academic literature that established their own estimates with their own models
*   Reference to our own intuitions for what feels right

If any of these four disagreed, we would explore why. Differences between the Guesstimate and the spreadsheet were helpful for finding typos in our equations and differences between our estimates and academic literature were helpful for finding crucial considerations that we missed.

  
We also made concrete predictions about the future and we can wait to see if they come true.

**Lesson #3: You should clearly itemize your assumptions**

When assessing how our estimate could change, we found it very helpful to carefully itemize all of the key assumptions we are making, our thoughts about them, whether they were explicitly captured in our model or not, and how they would presumably affect the model. We wish more people did this as it makes it much easier to quickly understand what the model is built upon, how uncertain it is, and how someone might have arrived at different conclusions. Also, if we’re wrong or missing something, it is very easy for people to point that out.

**Lesson #4: It’s easier in a team**

Working with a team helped make it easier to stay motivated at identifying potential mistakes. There were multiple times when either of us felt like stopping and not investigating a particular error instead of pressing further, but the other one was able to keep us on track. It was also a lot more fun.

**Lesson #5: It’s good to work in a well researched field**

It’s hard to reconcile your conclusions against existing academic research if there is no existing academic research. One of the primary benefits of estimating cost-effectiveness within a field like vaccination is there are many other studies in the field and comparing your results to this research theoretically provides very useful checks on your work. By looking at the work of others you can see where you may have gone wrong by comparing assumptions and checking that your model doesn’t leave out considerations that were important factors in other models. Seeing multiple models using various assumptions underlines the importance of making your assumptions very clear and thoroughly documenting them, not only for your own clarification but so that others could compare their work to your work.

However, making such comparisons is often very difficult to do. For example, when estimating the cost-effectiveness of a vaccine it’s difficult to try to compare the end results of different models even holding the vaccine-specific variables constant if the models were based on different populations. Different populations, across regions or time, can have a very different DALY burden per person which can produce cost-effectiveness estimates that differ by an order of magnitude or more.

When there isn’t any academic research, getting feedback and independent estimates from other experts may be your next best bet.

**Lesson #6: Technical understanding is helpful**

While neither of us our experts on vaccination, we both came into this project with some familiarity with vaccines given our prior work in the area that we believed helped limit errors. It’s easy to make mistakes in model inputs given unfamiliarity with a field. To take a simple example, cost estimates for vaccinations are sometimes given in cost per dose and other times in cost per vaccination series. Further, for a given vaccine, there are sometimes competing vaccination schedules which include different numbers of doses given per person and these may be given a different ages sometimes leading to different overall efficacy. This underscores the importance of having considerable understanding of the field you are attempting to evaluate for cost-effectiveness. As technical complications mount the probability of making an error that alters your end-line conclusions increases. That there are benefits to having domain knowledge of a field you are attempting to assess is hardly an earth-shattering insight or something we hadn’t considered before launching our analysis yet we came away from this project more convinced that it’s an important factor in producing reliable outputs.

**Lesson #7: Vaccination is great, but not a slam dunk win**

A while ago, Holden Karnofsky declared that [the Open Philanthropy Project is dedicated to “hits-based giving”](http://www.openphilanthropy.org/blog/hits-based-giving), a framework that accepts “philanthropic risk” where 90% of grants have zero impact but the number of grants that do have impact have sufficient impact to make the entire project worthwhile. This could be compared to the more traditional approach of GiveWell, where all grants made are to organizations where the expected value is relatively well known ([even if the organizations may still have zero impact](http://blog.givewell.org/2016/07/26/deworming-might-huge-impact-might-close-zero-impact/)).

On one plausible reading of hits-based giving the research and development of vaccines should have been a clear “hit,” an intervention so cost-effective it would make up for other funding that didn’t produce much positive. However, while our research would suggest that while some vaccines we covered were extremely cost-effective, and other vaccines currently in development have the potential to be so—consistent with hits-based giving—overall this basket of vaccines wasn’t clearly superior to other possible health interventions currently available to donors, with our estimate suggesting some vaccines may be orders magnitude worse than donating to the Against Malaria Foundation (AMF).

There are obvious limitations with generalizing from our basket of vaccines, and with comparing these results to AMF, but our research would suggest to reach a similar level of cost-effectiveness as AMF, vaccine research would need to produce a potentially an unrealistic dollar spent per DALY averted with few if any vaccine research programs that lead to little success. Moreover, if there are many AMF-level interventions that need funding, and vaccine research doesn’t reach this level of cost-effectiveness, this would seem to cut against philanthropic funding of vaccinations. On the other hand, it’s important to note that vaccine development likely increased our understanding of several diseases and likely opened other health interventions, possibly including some of the best interventions available today. That is to say, it’s plausible, for example, that bednets wouldn’t be as effective today if smallpox wasn’t eliminated given the health and economic benefits that resulted from the development of the smallpox vaccine.

Further, on a different reading of hits-based giving, it’s plausible that that the goal isn’t merely to uncover interventions as cost-effective as AMF, but rather hit the level of effectiveness probably achieved by, say, water sanitization. So, in this sense, even the development of an intervention as cost-effective as vaccines appear to be in our research wouldn’t be a hit but other interventions, particularly those that prevented an existential risk could qualify. So, if hits-based giving produced the occasional intervention as cost-effective as vaccines, while also having many interventions that resulted in little progress, and the rare intervention that was a tremendous success this approach could still be highly promising. Of course, in the absence of the large success, it will be very difficult to judge the total cost-effectiveness of this approach and it’s still early to know if interventions as cost-effective as vaccines will be produced using this approach.

In short, hits-based giving would suggest vaccines would definitely be a hit, but it turned out upon detailed analysis to merely be “okay”. **This further underscores that AMF may be a really hard baseline to beat and that it is important to do some degree of investigation before assuming things are hits.**

**Lesson #8: Maybe we should eradicate more diseases?**

If we were to try to draw some specific conclusions on vaccines, we would suggest, tentatively, a few things. Firstly, it seems clear to us, as it has to others who’ve examined the topic, that the smallpox eradication campaign was a really good idea. We would more hesitantly add to this claim that, where it is possible, eradication is a good idea and typically much more cost-effective than vaccination efforts that stop short of eradication. Of course, the pure costs or cost-effectiveness of attempting eradication are only part of the reason such efforts are or are not made, but we’d tentatively suggest perhaps were it is biologically feasible we’d favor making the attempt for vaccine-preventable diseases.

Further, for modern vaccines, bringing down the per dose cost paid is very important and it appears rolling out vaccines is cost-effective relative to other possible interventions but after adding in research costs this cost-effectiveness falls considerably.

**Lesson #9: If there’s a biosecurity nightmare, it may be a decade before a vaccine can be available**

Our work on estimating vaccine costs and timelines may also have some implications for biosecurity. If we urgently needed to make a new vaccine, how quickly and cheaply could we make it? $1.5B [was enough money](http://effective-altruism.com/ea/1l4/how_much_does_it_cost_to_research_and_develop_a/) to get [eight different Ebola candidates off the ground](https://en.wikipedia.org/wiki/Ebola_vaccine), at least [one of which](https://en.wikipedia.org/wiki/RVSV-ZEBOV_vaccine) had sufficient effectiveness that while it is not yet licensed, it could be used for emergency procedures.

The real question is not of budget, but of time. As many businesses learn in fits of frustration, you can’t always throw more money at something to make it go faster. The Ebola vaccine [technically took ~46 years](http://effective-altruism.com/ea/1c5/how_long_does_it_take_to_research_and_develop_a/), but it wasn’t actively developed for much of that time. Most of the Ebola vaccines have only seen [15-20 years of active development](https://en.wikipedia.org/wiki/RVSV-ZEBOV_vaccine), and I’d roughly guess that money could have sped it up so that we go from nothing to a workable vaccine in ~10 years. While the licensing process only [tends to add 5-7 years on average to the vaccine development timeline](/ea/1c5/how_long_does_it_take_to_research_and_develop_a/), I’d hope that a biosecurity emergency would allow us to cut through a lot of this if the benefits outweigh the risk.

We also may have thought more explicitly about doing a more detailed analysis of the implications of our vaccine timeline research on biosecurity. It would be great to know how quickly, at what cost, and with what efficacy humanity could develop a vaccine in the event one urgently needed to created. While we can draw some limited lessons from the recent push since the 2014 outbreak of Ebola to create a vaccine, obviously with a sample size of 1 the case of Ebola doesn’t necessarily generalize to what may happen in a more dire scenario.

**Conclusion**

All in all, we found this project to be good practice. Sandboxing within a fairly well-known and knowable domain allowed us to gain insight from the work of others. We think that following a specific basket of vaccines, though it limits extrapolation, allowed us to create concrete case-studies which was very helpful. We also believe looking at multiple different approaches to estimating inputs and outputs improved our understanding of the field as a whole though this process takes a considerable amount of time.

Given another chance to do this analysis, there are issues we believe we would have addressed differently. We may have spent more time thinking explicitly about the likelihood that all the best opportunities for vaccination are already taken, the good highly leveraged opportunities could do today, and how often there is a new serious disease.