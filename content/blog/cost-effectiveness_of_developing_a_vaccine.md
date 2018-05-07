+++

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
categories = ["vaccines", "global health"]

# author = ["Marcus A. Davis"]
tags = ["vaccines", "global health"]
date = 2018-05-06
draft = false
description = "How many dollars are spent per DALY and what are the uncertainties"
# featured = "pic03.jpg"
# featuredalt = "Pic 3"
featuredpath = "date"
linktitle = ""
title = "What is the cost-effectiveness of developing a vaccine?"
type = "post"
preview = true
# summary = "Summary: We looked at academic literature for vaccine cost-effectiveness as a whole and we also performed individual case studies on seven contemporary and historical vaccines to try to estimate the total cost-effectiveness of researching and developing a vaccine from scratch. Looking back historically, we find a range of $0.50 to $1600 per DALY, depending on the vaccine. Using this historical information, we derive an estimate for the total cost-effectiveness of developing and rolling out a “typical” / ”average” vaccine as being $18 - $7000 / DALY. The smallpox vaccine, malaria vaccine, and rotavirus vaccine may all be more cost-effective investments in total than marginal investments in distributing bednets (see Appendix C), especially when pursued to the point of completely eradicating the disease. However, there are many important assumptions made by these models, and changing them could strengthen or undermine these conclusions. [Section 1](#costs-and-benefits) and [2](#cost-effectiveness) detail the raw cost-effectiveness figures, [section 3](#variance-and-assumptions) provides a detailed analysis of all the key assumptions and model uncertainty, and [section 4](#takeaways) provides our takeaways. [Appendix A](#appendixa) provides an analysis of comparing our models to other models in the literature, [Appendix B](#appendixb) provides an estimate of the cost-effectiveness of the Ebola vaccine, [Appendix C](#appendixc) compares vaccination cost-effectiveness to distributing bednets, and [Appendix D](#appendixd) provides a rough assessment and comparison of some estimates of the cost-effectiveness of GAVI."

+++

Summary: We looked at academic literature for vaccine cost-effectiveness as a whole and we also performed individual case studies on seven contemporary and historical vaccines to try to estimate the total cost-effectiveness of researching and developing a vaccine from scratch. Looking back historically, we find a range of $0.50 to $1600 per DALY, depending on the vaccine. Using this historical information, we derive an estimate for the total cost-effectiveness of developing and rolling out a “typical” / ”average” vaccine as being $18 - $7000 / DALY. The smallpox vaccine, malaria vaccine, and rotavirus vaccine may all be more cost-effective investments in total than marginal investments in distributing bednets (see Appendix C), especially when pursued to the point of completely eradicating the disease. However, there are many important assumptions made by these models, and changing them could strengthen or undermine these conclusions.

[Section 1](#costs-and-benefits) and [2](#cost-effectiveness) detail the raw cost-effectiveness figures, [section 3](#variance-and-assumptions) provides a detailed analysis of all the key assumptions and model uncertainty, and [section 4](#takeaways) provides our takeaways. [Appendix A](#appendixa) provides an analysis of comparing our models to other models in the literature, [Appendix B](#appendixb) provides an estimate of the cost-effectiveness of the Ebola vaccine, [Appendix C](#appendixc) compares vaccination cost-effectiveness to distributing bednets, and [Appendix D](#appendixd) provides a rough assessment and comparison of some estimates of the cost-effectiveness of GAVI.

# Table of contents
1. [What are the costs and benefits?](#costs-and-benefits)
2. [What is the cost-effectiveness?](#cost-effectiveness)
	1. [Scenario 1: Vaccinate 60% of the relevant populations in SSA](#sixtypercentssa)
	2. [Scenario 2: Eradicate the disease completely](#eradication)
	3. [Individual Vaccines](#individualvaccines)
		1. [Smallpox Vaccine](#smallpox)
		2. [Measles Vaccine](#measles)
		3. [Rotavirus Vaccine](#rotavirus)
		4. [HPV Vaccine](#hpv)
		5. [HIV Vaccine](#hiv)
		6. [Malaria Vaccine](#malaria)
3. [Why do these estimates vary? What assumptions are we making?](#variance-and-assumptions) 
	1. [What population are you targeting?](#whatpopulation)
	2. [How are you calculating the DALY burden for that population?](#dalycalc)
	3. [How do you want to handle benefits that are not captured by DALYs?](#nondalyhandle)
	4. [How effective are you assuming the vaccine will be?](#vaccine-effectiveness)
	5. [How expensive do you assume the roll-out will be?](#roll-out-costs)
	6. [What assumptions are you making about the R&D cost?](#randdcosts)
	7. [How will population and DALY burden change over time?](#populationchange)
	8. [How do you consider “leveraged funds” / “unlocking funding” / “crowding out funding”?](#leveragefunding)
	9. [How do you handle discount rates, if at all?](#discountrates)
	10. [For how many years should you consider benefits?](#yearsofbenefits)
	11. [How do you adjust for counterfactuals?](#counterfactuals)
4. [Our Takeaways](#takeaways)
5. [Appendices](#appendices)
	1. [Appendix A: What Do Other Articles Say?](#appendixa)
	2. [Appendix B: Forecasting Cost-Effectiveness for Ebola](#appendixb)
	3. [Appendix C: Comparing to Against Malaria Foundation](#appendixc)
	4. [Appendix D: Cost-Effectiveness of GAVI](#appendixd)
6. [Endnotes](#endnotes)
  

## <a name="costs-and-benefits">1. What are the costs and benefits?</a>

While developing a vaccine is a huge accomplishment, it is not really of any significant humanitarian benefit until the vaccine is scaled up and rolled out to a significant population. Thus, spending a lot of money to develop a vaccine merely “unlocks” the opportunity to roll out the vaccine and the hope is that this roll-out is cost-effective enough to make up for the cost of the R&D once amortized across the entire vaccinated population.

We, therefore, take the following as our equation for the total cost-effectiveness of vaccine R&D:

Total cost-effectiveness of vaccine R&D ($/DALY) = ((Total R&D costs of making vaccine) + (Total roll-out costs of vaccine)) / ((DALY burden of disease) * (% reduction in disease attributable to the vaccine))

Note here that we’re looking at the total cost-effectiveness across the entire investment in R&D, which requires us to also look at the total investment across vaccine roll-out too. We’re not looking at the marginal investment, or the cost-effectiveness you would get if you added more funding to vaccines today, which could be a very different number (see section 3.8 for details).

To try to answer this question, we previously modeled [how long it would take to develop a new vaccine]({{< ref "blog/how_long_to_research_develop_vaccine.md" >}}), [how much it costs to research and develop a vaccine]({{< ref "blog/cost_to_research_and_develop_vaccine.md" >}}), [how much it costs to roll-out that vaccine]({{< ref "blog/how_much_does_it_cost_to_roll-out_vaccine.md" >}}), and then [how beneficial we can expect vaccines to be]({{< ref "blog/how_beneficial_have_vaccines_been.md" >}}).

These data were calculated from available evidence about vaccines generally and also for specific case studies: smallpox (which was chosen as it was one of the first vaccines and the only human disease successfully eradicated by vaccination); measles (which was chosen as it was one of the first vaccines); HIV, malaria, and Ebola vaccines as they are modern and under current development, and rotavirus and HPV as they recently finished vaccine licensing. For each of these vaccines, we calculated how much they would cost for both R&D and roll-out, and then what benefits we would expect.

We aggregated all this data [in a spreadsheet](https://drive.google.com/open?id=18zUqZMrV7UvzYGXmOowSLvdS1pX5_GA8dgIxd8A2_yM) that makes all the calculations between the multiple sections much more clear, with a good amount of detail. Based on that data, we come to the following conclusions. (For more detail, see the spreadsheet and the previous articles.)

Vaccine

R&D Costs

Roll-out Costs

Smallpox

$5.58M

$0.73-$47.62 / child

Measles

$38.3M

$1-$38 / child

Rotavirus

$1,140M

$3-$28 / child

HPV

?

$2.55-$22.71 / child

HIV

$24,500M

$50-$160 / child

Malaria

$605M

$22 / child + $293M

Ebola

$1,500M

?

“Typical” vaccine

$460M - $1900M

$13.21-$53.05 / child

  
  
  

Vaccine

DALYs per vaccinated person in 2016a

Yearly DALYs at 60% vaccination rate in 2016 SSA

Yearly DALYs if eradicationb

Smallpox

0.14037

7,437,600

44,653,000

Measles

0.20793

34,105,842

99,341,000

Rotavirus

0.17990

4,589,392

Not possible

HPV

0.01250

327,522

5,173,000c

HIV

0.26343

9,655,005

57,575,000

Malaria

0.40619

10,362,216

56,201,000

Ebolad

0.07502

92,685

309,000

A - Estimates for DALYs prevented per person vaccinated over a 20 year period.

B - These figures, except for smallpox and measles, are derived from their 2016 global DALY burdens from [Global Burden of Disease, Results Tool (2016e)](http://ghdx.healthdata.org/gbd-results-tool?params=gbd-api-2016-permalink/d8ac743867dc9c03ba8e196b585d7b0d)

C - This figure is 70% of the 2016 global burden from cervical cancer of 7,390,002.82.

D - All Ebola estimates here are a 5 year average from 2012-2016 and assumes a vaccine that is 50% effective.

  
  
  

## <a name="cost-effectiveness">2. What is the cost-effectiveness?</a>

Based on the data in the above tables and the considerations we’ve made, we can then apply our formula: Total cost-effectiveness of vaccine R&D ($/DALY) = ((Total R&D costs of making vaccine) + (Total roll-out costs of vaccine)) / ((DALY burden of disease) * (% reduction in disease attributable to the vaccine))

As stated before, these calculations were originally derived from research in prior articles (e.g., for R&D costs, roll-out costs, and total benefits) for a particular basket of vaccines. We then aggregated all this data [in a spreadsheet](https://drive.google.com/open?id=18zUqZMrV7UvzYGXmOowSLvdS1pX5_GA8dgIxd8A2_yM), used the spreadsheet to create individual Guesstimate models for each vaccine, and created 90% confidence intervals from each model. We made calculations for each of our vaccines, except for Ebola, where we felt like there was insufficient information to make a confident calculation. (We still attempt to estimate for Ebola in [Appendix B](#appendixb).)

The models varied targeted populations across two scenarios -- one where 60% of the relevant population in Sub-saharan Africa (SSA) is vaccinated and another where the disease is completely eradicated. We also varied assumptions about the DALY burden, vaccine effectiveness, roll-out costs, and R&D costs. We then created these 90% confidence intervals.

  
  

### <a name="sixtypercentssa">2.1) Scenario 1: Vaccinate 60% of the relevant populations in SSA</a>

For this scenario, we assume that there is a one-time fixed cost investment for researching and developing the vaccine and building infrastructure for rolling out the vaccine that is amortized over a time period to consider benefits for (in our model, we cap it at 20 years), then an annual cost to keep rolling out the vaccine to the relevant population. Then, every year, we save a certain amount of DALYs from preventing that disease via the vaccine. Together, we can use this to calculate DALYs averted over the benefits time period compared to the cost spent during the time period.

Vaccine

Roll-out Cost-effectiveness

Roll-out + R&D Cost-effectiveness

Guesstimate[^1]

Smallpox

$4.30 - $66 / DALY

$4.40 - $67 / DALY

[Link](https://www.getguesstimate.com/models/10600)

Measles

$8 - $320 / DALY

$9 - $320 / DALY

[Link](https://www.getguesstimate.com/models/10590)

Rotavirus

$6 - $59 / DALY

$10 - $64 / DALY

[Link](https://www.getguesstimate.com/models/10589)

HPV

$240 - $1300 / DALY

$370 - $1600 / DALY

[Link](https://www.getguesstimate.com/models/10586)

HIV

$85 - $550 / DALY

$210 - $690 / DALY

[Link](https://www.getguesstimate.com/models/10583)

Malaria

$21 - $49 / DALY

$23 - $52 / DALY

[Link](https://www.getguesstimate.com/models/10588)

Ebola

?

?

 

“Typical / average vaccine”[^2]

$12 - $6700 / DALY

$18 - $7000 / DALY

[Link](https://www.getguesstimate.com/models/10616)

  
  

### <a name="eradication">2.2) Scenario 2: Eradicate the disease completely</a>

For this scenario, we consider one-time costs for researching and developing the vaccine and then rolling out the vaccine enough to achieve eradication. In the case of smallpox, as it really has been eradicated, real estimates of spending and disease burden were used. In all other cases, extrapolations were made from the estimated costs of vaccination per person and the intended target population of the vaccination[^3]. The population targeted was different depending on the disease, with HPV and HIV roughly targeting reproductive age populations and malaria and measles targeting children under 5. The efficacy of the vaccines was also assumed to be high enough to achieve eradication at the time eradication is attempted[^4].

After eradication is achieved, we assume that ongoing costs are essentially $0[^5]. We then consider this large cost compared to a period of accrued benefits from the eradication (in our model, we cap it at 20 years; see discussion below on this cap).

Vaccine

Roll-out Cost-effectiveness

Roll-out + R&D Cost-effectiveness

Guesstimate[^1]

Smallpox

$0.44 - $5.80 / DALY

$0.44 - $5.80 / DALY

[Link](https://www.getguesstimate.com/models/10606)

Measles

$0.36 - $13 / DALY

$0.37 - $13 / DALY

[Link](https://www.getguesstimate.com/models/10605)

Rotavirus

Not possible

Not possible

 

HPV

$65 - $340 / DALY

$80 - $370 / DALY

[Link](https://www.getguesstimate.com/models/10604)

HIV

$270 - $1600 / DALY

$300 - $1600 / DALY

[Link](https://www.getguesstimate.com/models/10603)

Malaria

$12 - $23 / DALY

$13 - $23 / DALY

[Link](https://www.getguesstimate.com/models/10601)

Ebola

?

?

 

“Typical” / average vaccine[^2]

$8 - $8200 / DALY

$10 - $8100 / DALY

[Link](https://www.getguesstimate.com/models/10618)

  
  

### <a name="individualvaccines">2.3) Individual Vaccines</a>

#### <a name="smallpox">2.3.1.) Smallpox Vaccine</a>


When making direct estimates using inputs from [Fenner, et al. (1988)](http://apps.who.int/iris/handle/10665/39485), [by our estimation](https://docs.google.com/spreadsheets/d/1wGC8m8rYCZdIXakvHyYcf61YKeBXEWYOO7_Sjjt9hJs/edit#gid=1790767923) before the eradication campaign in the early 1960s, smallpox prevented a DALY from death for ~$20-64 in developing countries and ~$1550-3800 in developed countries. Weighting this by population in each region, this implies a total cost per DALY of $527 for both roll-out costs alone and roll-out costs plus R&D costs. Over the full population since eradication, not accounting for post-eradication prevention spending, the eradication campaign cost $26-70 per death prevented, $3.30-11 per case prevented, and $0.44-3.80 per DALY prevented at the rates of death and disease of 1967.

These estimates are absolute as they are not compared to the cost of maintaining the 1967 vaccination and monitoring costs. As smallpox is eradicated, these figures will fall over time, unless and until there is a new smallpox outbreak or significant enough threat of an outbreak to cause an increase in spending.  
  
Assuming the pre-vaccination world would be like the pre-eradication world of smallpox endemic countries in the 1960s, given a case rate of roughly 1% and a death rate between 5 and 20% per case of smallpox, [our Guesstimate](https://www.getguesstimate.com/models/10600) suggests a cost per DALY prevented of $4-62 with or without the R&D costs included.

  
  

#### <a name="measles">2.3.2.) Measles Vaccine</a>

Assuming a very rough conversion that a life saved from a measles death is ~30 DALYs[^6], this would imply very rough figures of $9-320/DALY in general, given a cost range per person vaccinated of $1-38, weighted so cheaper prices are more likely. In areas with pre-existing strong vaccine infrastructure such that measles vaccines cost about $2 a dose, the price would be roughly $9 per DALY. Given the wide range of possible cost per person, it should be noted that holding everything else constant, the cost-effectiveness including R&D cost scales roughly linearly with the price of vaccination per person.

Perhaps we could make sense of these figures by further untangling marginal vaccine costs from the investments needed to make vaccine pathways. If we assume a one-time investment of $100M, similar to the more directly estimated fixed costs of the malaria vaccine, is sufficient to get all lower income countries to a point where marginal vaccination costs $2 per child in total vaccine and logistics costs, and we assume that we’re rolling out the measles vaccine to 96.3M people, the population of 60% of children under 5 in SSA, and we take our prior estimate that the measles vaccine cost $38.3M in R&D, the total yearly costs are ~$151M for the vaccinations at ~$10/DALY, only slightly higher than with no investment spending at all. Given our earlier calculations, this would avert about 177K measles deaths or 5.3M DALYs.

A more worse-case analysis assuming $23 per child, with the same $38.3M in R&D, and rolling out to the same population, the total cost would be $587M at $110/DALY.

  
  

#### <a name="rotavirus">2.3.3.) Rotavirus Vaccine</a>

Given vaccine efficacy of 39-85% ([RotaCouncil, 2016](http://rotacouncil.org/wp-content/uploads/2016/03/White-paper-FINAL-v2.pdf), p11) and a reduction of diarrhea of 30-54% ([Madhim et al., 2010](http://www.nejm.org/doi/full/10.1056/NEJMoa0904797#t=article), [Msimang, et al., 2013](https://journals.lww.com/pidj/Fulltext/2013/12000/Impact_of_Rotavirus_Vaccine_on_Childhood_Diarrheal.22.aspx)), if we assume we can achieve a 60% vaccination rate of the under-five population in SSA, vaccinating 96.3M children (see [Population Pyramid](https://www.populationpyramid.net/sub-saharan-africa/2016/)), we would avert ~7.5-13M DALYs per year using the 2005 DALY rate or 4.6-8.3M DALYs using the 2016 rate. Assuming an initial $50-100M investment in building the pipeline to roll out the vaccine, with a per person cost between $3-7 that would be $6-63/DALY looking just at roll-out costs and $10-68/DALY when adding in R&D costs.

There’s great uncertainty about these estimates given fixed roll-out costs are a guess and the efficacy of the vaccine is fairly wide.

  
  

#### <a name="hpv">2.3.4.) HPV Vaccine</a>

If the HPV vaccine was rolled out to all children aged 5-15 in SSA with a 60% vaccination rate and given ~780,000 DALYs in women aged 15-49 ([Global Burden of Disease, Results Tool, 2016b](http://ghdx.healthdata.org/gbd-results-tool?params=gbd-api-2016-permalink/c3c9f8ef3f09237e684ebfbfa7ac95cc))[^7] then the HPV vaccine could prevent ~328,000 DALYs per year in SSA. With a fixed roll-out cost guessed to be an additional $50M, at $3-13.50 per person this would imply $240-1300 per DALY based on just roll-out costs and $370-1600 per DALY when including R&D costs.

  
  

#### <a name="hiv">2.3.5.) HIV Vaccine</a>

Given estimates of a vaccine that is 50% effective (or more) and distributed to 60% of the eligible population in SSA, it would avert 30% of all HIV, saving 9.7M DALYs. Relative to other vaccines, many of the parameters for our HIV estimates vary widely, particularly our estimated cost per person of $30-160. Ultimately, our model suggests an estimated cost-effectiveness of $180-570 per DALY. Our individual scenarios indicate the final cost-effectiveness depends significantly on which population that vaccine is ultimately distributed to and the cost of per person of vaccination[^9].

  
  

#### <a name="malaria">2.3.6.) Malaria Vaccine</a>

Previously we noted that the malaria vaccine involved [spending ~$605M in fixed costs](/ea/1l4/how_much_does_it_cost_to_research_and_develop_a/) to unlock the ability to [roll out the vaccine for $22/child](/ea/1l5/how_much_does_it_cost_to_rollout_a_vaccine/). The Global Burden of Disease estimated a yearly malaria burden of 56.2M DALYs, with 44.3M global DALYs for those under five, and 42.1M of those in SSA ([Global Burden of Disease,  Results Tool, 2016c](http://ghdx.healthdata.org/gbd-results-tool?params=gbd-api-2016-permalink/a5fdf7803b03487a8b851317d76fc5d2)). Modeling in Guesstimate, accounting for uncertainty by using a range of vaccine efficacy between 39-75% (the upper end of which is closer to vaccine efficacy for established vaccines), an expected R&D cost between $600-1,000M and a cost per person between $18-25, we get an estimate of $12-23/DALY for roll-out costs alone and $13-33/DALY including R&D costs.

## <a name="variance-and-assumptions">3. Why do these estimates vary? What assumptions are we making?</a>

How do we assess the cost-effectiveness of developing a new vaccine, from scratch, before anything is known about the vaccine? As mentioned by [Dalton (2016)](https://docs.google.com/document/d/1Jmp1LQEem9E29ynSrqYrkiCsFFMrvyZLPqPl3Itdaak/edit) (p13), research is “by nature the exploration of the unknown” and thus is naturally difficult to estimate.

For our models, we constructed ranges for cost-effectiveness estimates instead of point values, because there was a wide range of assumptions for each vaccine and it wasn’t clear which assumption would be most correct. When looking at cost-effectiveness, we should consider all the ways in which the cost-effectiveness of a vaccine may differ and what assumptions are being made.

Throughout our modeling, we identified eleven key sources of variation and assumption-making:

Assumption

How do we account for it?

Overall impact on estimate

What population are you targeting?

Not accounted for in individual models, but tested over several modeled scenarios

Individual range could be off by 20 - 100% in either direction when applied to a different population.

How are you calculating the DALY burden for that population?

Mostly accounted for in individual models via Guesstimate range parameter

The true cost-effectiveness may be worse than the model range makes it appear (that is, the range is biased downwards) due to this effect.

How do you want to handle benefits that are not captured by DALYs?

Not accounted for by Guesstimate models

The true cost-effectiveness may be better than the model range makes it appear (that is, the range is biased upwards) due to this effect.

How effective are you assuming the vaccine will be?

Accounted for in individual models via Guesstimate range parameter

Should be accounted for within estimate range.

How expensive do you assume the roll-out will be?

Accounted for in individual models via Guesstimate range parameter

Should be accounted for within estimate range, but the true cost-effectiveness has some risk of being worse due to this effect.

What assumptions are you making about the R&D cost?

Mostly accounted for in individual models via Guesstimate range parameter

Should be accounted for within estimate range, but the true cost-effectiveness has some risk of being worse due to this effect.

How do you want to account for changing population and DALY burden into the future?

Not accounted for by Guesstimate models

The true cost-effectiveness has some risk of being worse than the model range makes it appear because of a shrinking DALY burden per person, but also some risk of being better than the model range makes it appear due to a growing population.

How do you want to handle "leveraged funding"?

Not accounted for by Guesstimate models (models take a total “all costs” approach)

The true cost-effectiveness may be better than the model range makes it appear due to this effect, perhaps by a factor of 25% to 100%, though a risk of being biased upwards by this effect is also possible.

How do you want to handle discount rates?

Not accounted for by Guesstimate models (models take a total “all costs” approach)

The true cost-effectiveness may be worse than the model range makes it appear due to this effect.

For how many years should you consider benefits?

Variation in this assumption is not accounted for by Guesstimate models. Guesstimate models assume 20 years of consideration.

Final range by model could be off by a large amount in either direction, depending on whether you think more or fewer years of benefits should be taken into account. It’s not clear which direction this goes in, though, as assuming both more and fewer years of benefits is reasonable.

How do you adjust for other counterfactuals?

Not accounted for by Guesstimate model (models take a total “all costs” approach)

The true cost-effectiveness may be worse than the model range makes it appear due to this effect.

Taking all of this into account is essentially some attempt to itemize our model uncertainty, and it suggests that the true 90% confidence interval for our model would be much wider than the ones offered by our models.

For example, while our standard model gives a 90% confidence interval for the cost-effectiveness of the malaria vaccine as $23 - $52 / DALY, changes in these above assumptions could justify numbers perhaps as low as $0.30 / DALY using very optimistic assumptions across the board, and as perhaps high as $3500 / DALY using very pessimistic assumptions across the board.

This doesn’t necessarily mean that our model is wrong or that our 90% interval is not a true 90% interval -- it just means that you have to be careful about your assumptions and what you are defining when you’re talking about “cost-effectiveness” in a particular context. A very wide notion of “all things considered” cost-effectiveness that captures all the variations in these assumptions is likely not useful, but itemizing and considering these assumptions is. Further exploration of these parameters is available in the discussion below and in the comparison to other literature found in [Appendix A](#appendixa).

  
  

### <a name="whatpopulation">3.1.) What population are you targeting?</a>

The overall cost-effectiveness of a vaccine can vary a lot depending on what population you are targeting. We explored two different scenarios -- targeting enough people in SSA to achieve a 60% vaccination rate and targeting enough people for complete eradication. However, there are many possibilities. For example, one could try to target just an especially high-risk population, and this may be more cost-effective per person though help less people. Additionally, one could try to achieve more vaccination than just 60% of the SSA, though less than outright eradication. Depending on the precision and scale of the targeting and the DALY burden per person of the targeted population, the ultimate cost-effectiveness could differ.

For one concrete example, consider this table varying the targeting of the malaria vaccine. We look at our estimates for our two scenarios -- vaccinating 60% of SSA and outright eradication, but we also consider a third, more targeted scenario -- vaccinating 60% of a country with high malaria prevalence, like the Democratic Republic of the Congo.

Population

Cost-effectiveness

Cost-effectiveness, excluding R&D costs

Guesstimate

60% of DR Congo

$31 - $140 / DALY

$18 - $84 / DALY

[Link](https://www.getguesstimate.com/models/10607)

60% SSA

$23 - $52 / DALY

$21 - $49 / DALY

[Link](https://www.getguesstimate.com/models/10588)

Eradication

$11 - $18 / DALY

$11 - $18 / DALY

[Link](https://www.getguesstimate.com/models/10601)

A more targeted roll-out can be more cost-effective by eliminating more DALYs per person but could be less cost-effective when including R&D costs, as the R&D costs are spread across fewer people. On the other hand, the savings from outright eradication could make targeting the most people more cost-effective, even on a per person basis. For another exploration of how targeting can change cost-effectiveness estimates, see [Appendix B](#appendixb) on estimating the cost-effectiveness of Ebola.

  
  

### <a name="dalycalc">3.2.) How are you calculating the DALY burden for that population?</a>

The DALY burden per person can change how cost-effective a particular vaccination is, so calculating the burden correctly is important. \[We have dedicated an entire article to exploring that.\](link) However, it can be tricky to figure out what the correct burden should be for our vaccine scenarios. We’re trying to model the amount of DALYs that vaccines would reduce but we can’t always use the DALY figures as of today since some of these vaccines in reality already exist and thus already have dramatically reduced the DALY burden of diseases. For example, smallpox has been completely eliminated, so the current DALY burden is 0! Thus we have to carefully rewind the clock and extrapolate to what the DALY burden would be. On the other hand, we do need to include the impact of modern trends in vaccine alternatives, like how the malaria DALY burden has been substantially reduced by bednets.

For our calculations, we try to either estimate the DALYs, such as in the cases of smallpox and measles, or we try to use a range of DALYs from [Global Burden of Disease (2016d)](http://ghdx.healthdata.org/gbd-results-tool). We think this helps capture uncertainty in the correct DALY burden to use, but that it risks overestimating the size of the DALY burden, especially extrapolating into the future.

  
  

### <a name="nondalyhandle">3.3.) How do you want to handle benefits that are not captured by DALYs?</a>

As reviewed in our \[assessment of the benefits of vaccines\](link), there are multiple economic benefits from health savings due to reduced health care costs and reduced spending on combating the disease. Similarly, there may be substantial medium-term benefits from economic development via a healthier population. None of these effects are accounted for in our DALY-based modeling.

Additionally, if we vaccinate enough to achieve a significant degree of herd immunity but not enough to outright eradicate a disease, the benefit of this herd immunity is also not accounted for in our models. This would likely not affect our 60% SSA estimate much but may affect our eradication estimate.

We found these benefits to be too hard to pin down to be worth directly modeling, but we must note that their exclusion likely biases our estimate downward (making it appear less cost-effective than it should) to some degree.

Lastly, and this goes without saying, long-term effects such as the ramifications of shifting population change, or the effect of economic development on the trajectory of civilization, are not accounted for. It’s not clear what the impact of these longer-term effects would be.

  
  

### <a name="vaccine-effectiveness">3.4.) How effective are you assuming the vaccine will be?</a>

Vaccine effectiveness rates are empirical values that can be assessed using trials. For example, the current malaria vaccine candidate in Phase III trials has an effectiveness of 13.7% - 46.9% after four years ([Winskill, Walker, Griffin, and Ghani, 2017](http://gh.bmj.com/content/2/1/e000090)). However, vaccines usually aren’t rolled out with such low efficacy, and vaccines tend to increase in effectiveness over time with further R&D, and this effect is not fully accounted for in the current value.

On the other hand, it may not make sense to extrapolate the current efficacy of the rotavirus vaccine (or other very new vaccines like HPV and malaria) as anything other than the initial efficacy. Vaccines are improved and refined in part by being actually implemented and manipulating the timing of the shots, the number of shots, and by learning from impact in a real population. Accounting for this would change the estimate of roll-out DALYs prevented since it may be preferable, in such a modeling exercise, to use a longer time horizon and some probability distributions on the potential efficacy of the given vaccine over time.

Additionally, taking the efficacy of a new vaccine literally may risk extrapolating it too far. For example, our models estimate the benefits across a twenty-year time horizon, but the efficacy of the malaria vaccine has currently only been established for a four-year time horizon (Winskill, Walker, Griffin, and Ghani, 2017). It’s possible that the overall efficacy across the twenty-year time horizon could decline.

Our Guesstimates use ranges for effectiveness that include the empirical values, but with an assumption that these vaccines will become more effective with time. Some of the vaccines that are experimental and haven’t yet been rolled out, like the malaria vaccine, have very wide ranges for the estimate of effectiveness. We think it’s possible this extrapolation for the newer vaccines (e.g., HIV, malaria, Ebola) could be overestimating or underestimating the final vaccine efficacy found on actual roll-out due to these discussed factors.

  
  

### <a name="roll-out-costs">3.5.) How expensive do you assume the roll-out will be?</a>

The roll-out costs of a vaccine are empirical values [that we have estimated](/ea/1l5/how_much_does_it_cost_to_rollout_a_vaccine/), but they also tend to decrease over time with further R&D and further price negotiations, especially as the costs of the vaccine get recouped by the vaccine companies. The roll-out cost can also be very sensitive to the remoteness of the regions being targeted, and thus can vary depending on the population being targeted.

We have tried to account for these effects using a range of estimates for the roll-out costs. However, there still remains some risk that our model overcorrects for the remoteness of populations, as we did not fully research how those costs break down in our targeted population. There is also some risk that we have not adequately accounted for the declining cost of roll-out in our estimates.

  
  

### <a name="randdcosts">3.6.) What assumptions are you making about the R&D cost?</a>

Similar to roll-out costs, the R&D costs of a vaccine are empirical values [that we have estimated](/ea/1l4/how_much_does_it_cost_to_research_and_develop_a/) (or at least guessed, where historical data was more sparse). R&D costs do not decrease over time, but they decrease per person and per DALY saved as the cost can be spread (amortized) across more people. Thus vaccinating a larger population will spread costs further and be “penalized” less by a high R&D cost. This should be fully accounted for in our models and scenario testing.

What we don’t take into account, however, is the degree to which R&D costs might be double counted in the roll-out costs. If the roll-out costs include a price per dose and the price per dose is meant to compensate companies for R&D into these vaccines (even explicitly so in the case of an [advanced market commitment](http://www.who.int/immunization/newsroom/amcs/en/)), we would count the R&D costs twice.

On the other hand, we’re unsure if the price of the vaccine does adequately capture the R&D cost or would be sufficient to incentivize the creation of the vaccine without additional outside philanthropy. Empirically, we observe philanthropy going to both vaccine R&D and vaccine roll-out, regardless of the existence of what should be a vaccine market that could incentivize R&D on its own. [Outterson (2006)](http://www.cptech.org/ip/health/prizefund/files/outterson-buyouts.pdf) cites research that estimates the “cost recovery percentage” of R&D to be only 17%, which would suggest that we still should substantially consider R&D costs in our model, but it’s not clear how representative this estimate is of the particular vaccines we are attempting to model.

Overall, this might bias our model upwards (making our model appear less cost-effective than it should), but it’s not clear by how much. Given that R&D costs seem to be a very small component of the model and are typically dominated by much higher roll-out costs, it’s likely this bias is small.

  
  

### <a name="populationchange">3.7.) How will population and DALY burden change over time?</a>

Population growth proved very difficult to model, as it depends on the growth specifically of the population that would receive the vaccine in the areas the vaccine is delivered, which may differ substantially from the more general population statistics that are freely available and that we used to calculate the DALY burden. We’re unsure how an increasing population and decreasing DALY burden will interact over our 20 year time span and to what degree each effect will dominate.

  
  

### <a name="leveragefunding">3.8.) How do you consider “leveraged funds” / “unlocking funding” / “crowding out funding”?</a>

So far, we’ve attempted to look at creating rough estimates for the total pool of funding to create the vaccine and bring it to the necessary population, including some fixed cost to build up delivery infrastructure and then compared it to the total benefits. However, if we were an individual financial actor or institution in the wide web of vaccine funding, we would have to consider much more than the total rate.

This might be similar to a distinction made by Dalton (2016), which differentiates between the question “how cost-effective is it to spend an extra dollar on projects you can contribute to today”, called marginal ex-ante analysis versus “how cost-effective, on average, have all total contributions been to the project historically?”, called average ex-post analysis. There are likely huge differences in the two numbers, and just because something may look ineffective in average ex-post analysis does not mean it might be ineffective on a marginal ex-ante analysis (and vice versa). Since new philanthropic investments are made on a marginal ex-ante basis, we should put substantial effort into figuring out how marginal funding might be different than total funding. Considerations like leverage help with this.

A good model for this is discussed by [Snowden (2018)](https://blog.givewell.org/2018/02/13/revisiting-leverage/), where we might itemize all the individual funders contributing to the vaccine and decide what they would have donated to instead, and then increase or reduce the cost-effectiveness estimate accordingly. We could then consider a dependency web of funding, figuring out to what degree some funding “unlocks” other funding or “crowds out” other funding. However, actually carrying this out in detail is beyond the scope of this article, outright impossible for earlier vaccines where detailed funder information is unknown, and still exceedingly difficult for modern vaccines, like malaria, that do itemize all the relevant funders.

Current mechanisms for funding vaccines involve substantial “co-funding” from the governments of the countries receiving the vaccines and the foreign aid departments of developed nations. Thus private philanthropic investment (say by the Bill and Melinda Gates Foundation) could net “unlock” significant amounts of government funding that would likely be spent on net less cost-effective pursuits. On the other hand, [difficulty in finding funding opportunities](https://blog.givewell.org/2016/07/06/dont-currently-recommend-charities-focused-vaccine-distribution/) and the general perception that there is no “room for more funding” in this area could suggest that funding actually just “crowds out” funding from other would-be interested donors.

Our general intuitions are that, taking these two effects together, we’d guess overall that this net effect points more toward “unlocking” than “crowding out”, for a total effect that could substantially reduce the cost-effectiveness of a vaccine to be around 25% to 100% better (i.e., the adjusted cost effectiveness would be somewhere between 4/5ths to half the original unadjusted value) than what it would be if you did not consider this effect, from the point of view of a private foundation donor (or a private donor pooling their individual donation with such a foundation). We’re unsure of this, however, and the real effect could be substantially in the other direction.

Additionally, our analysis doesn’t offer a way to evaluate the impact of existing vaccination charities or interventions operating given existing vaccination delivery infrastructure and commitments from governments and non-state actors. For example, a charity that increased the efficiency of vaccination distribution through public outreach would not be responsible for the costs of vaccination doses. Instead, they would only be responsible for their personal staff costs and costs spent on outreach, and thus the cost-effectiveness of that charity would not be within the scope of our analysis of the cost-effectiveness of vaccines themselves.

We [adapted the Guesstimate for malaria to include a leverage factor](https://www.getguesstimate.com/models/10679) and explored some possible ranges:

R&D Leverage

Roll-out Leverage

Total cost-effectiveness

1 (Normal)

1 (Normal)

$23 - $53 / DALY

1 (Normal)

1.25 (Crowd out by 25%)

$28 - $66 / DALY

1 (Normal)

0.75 (Unlock 25%)

$18 - $41 / DALY

1 (Normal)

0.5 - 0.75 (Unlock 25-50%)

$14 - $35 / DALY

1 (Normal)

0.5 (Unlock 50%)

$12 - $28 / DALY

0.75 (Unlock 25%)

0.5 (Unlock 50%)

$12 - $28 / DALY

0.5 (Unlock 50%)

1 (Normal)

$22 - $52 / DALY

1 (Normal)

0 (Unlock 100%)

$1.50 - $3.60 / DALY

From this exploration, we can see that leverage on the roll-out costs dominates any leverage on the R&D costs.

  
  

### <a name="discountrates">3.9.) How do you handle discount rates, if at all?</a>

When making this model, we did not apply any discount rate to future benefits. Furthermore, we don’t think a discount rate should be applied here, despite it being fairly standard to do so, for reasons discussed in [Ord and Wiblin (2013)](https://www.givingwhatwecan.org/sites/givingwhatwecan.org/files/attachments/discounting-health2.pdf). We hope that the lack of discount rate and the fact that we also did not consider population growth will roughly cancel each other out.

  
  

### <a name="yearsofbenefits">3.10.) For how many years should you consider benefits?</a>

It is not clear for how long we should continue to consider benefits, since the benefits of vaccines would potentially continue indefinitely for hundreds of years. Perhaps these benefits would eventually be offset by some other future technology, and we could try to model that. Or perhaps we should consider a discount rate into the future, though we don’t find that idea appealing.

Instead, we decided to cap at an arbitrary fixed amount of years set to 20 by default, though adjustable as a variable in our spreadsheet model (or by copying and modifying our Guesstimate models). We picked 20 because it felt like a significant enough amount of time for technology and other dynamics to shift.

It’s important to think through what cap makes the most sense, though, as it can have a large effect on the final model, as seen in this table where we explore the ramifications of smallpox eradication with different benefit thresholds:

Smallpox Eradication Cost-effectiveness

Benefits Considered

Cost-effectiveness

Guesstimate

10 Years

$0.79 - $7.30 / DALY

[Link](https://www.getguesstimate.com/models/10645)

20 Years

$0.41 - $3.50 / DALY

[Link](https://www.getguesstimate.com/models/10606)

30 Years

$0.26 - $2.40 / DALY

See “10 years”

50 Years

$0.16 - $1.50 / DALY

See “10 years”

Malaria 60% SSA Cost-effectiveness

Benefits Considered

Cost-effectiveness

Guesstimate

10 Years

$24 - $56 / DALY

[Link](https://www.getguesstimate.com/models/10680)

20 Years

$23 - $53 / DALY

[Link](https://www.getguesstimate.com/models/10588)

30 Years

$20 - $47 / DALY

See “10 years”

50 Years

$19 - $45 / DALY

See “10 years”

  
  

The longer you consider for your benefits window, the better a vaccine will be. For smallpox eradication, the increased cost per year is considered to be ~$0 and the benefits in our model scale linearly. However, for the malaria 60% SSA model, the costs and benefits both scale with the window, leading to a much steadier increase in cost-effectiveness as the benefits window is increased.

It’s not clear that this consideration biases the model in any direction, making it systematically more likely to be an overestimate or an underestimate, but taking variability in this assumption into account should widen our confidence bars more than is reflected in our models. It seems reasonable one could make an argument for a lower benefits window (perhaps via a discussion of counterfactuals, see below) or a larger benefits window. Perhaps a more robust model may taper benefits over time due to other medical advances.

  
  

### <a name="counterfactuals">3.11.) How do you adjust for counterfactuals?</a>

Some previous analysis, such as Dalton (2016), has looked at the benefits of funding a vaccine by assuming that this vaccine would have eventually been funded anyway by someone else, and that one’s philanthropy is merely “bringing the vaccine forward”, or making the vaccine available a few years earlier than it otherwise would have inevitably been made available by someone else, later. For example, if Salk hadn’t developed his polio vaccine, [Sabin’s vaccine was just under six years away](https://www.sciencehistory.org/historical-profile/jonas-salk-and-albert-bruce-sabin). Thus, Salk only “brought forward” a polio vaccine by about six years. This may be a big deal to the extra people spared polio over those years of additional vaccine time, but it limits the overall impact of Salk’s work.

This can be explicitly considered in our model by changing the “years to consider benefits” variable to the number of years you think the vaccine will be brought forward. However, we’re not sure that thinking in terms of bringing the vaccine forward is a good way to think about it, as any funding of a vaccine by a philanthropist now will forever free up the funding that a future philanthropist would have spent, allowing the philanthropist to instead spend money on something else potentially worthwhile, assuming that philanthropist would spend the money as effectively (or more) as you would. Thus this is not really a question of bringing the vaccine forward, but rather a special subset of the question of “crowding out” funding that we discussed earlier (see section 3.8).

  
  

## <a name="takeaways">4.) Our Takeaways</a>

Overall then, ignoring the economic benefits of vaccination, the total cost-effectiveness of the vaccines we observed varies widely from under $0.50 to over $1600 per DALY. Averaging out all the values we consider reasonable, produces a range of $18 - $7000 / DALY for the cost-effectiveness of a “typical” / average vaccine. Further changes in assumptions and contexts could dramatically change these numbers further in both directions.

In all cases, there was considerable variability both within and between vaccines based on uncertain inputs. This became especially difficult when trying to determine the historic impact of vaccines, as in the case of measles and smallpox, as there are many assumptions and decisions that need to be made in order to estimate the cost-effectiveness of vaccines across time. These assumptions can highly alter the final cost-effectiveness analysis and thus the best our analysis can do is justify narrowing the range of possible cost-effectiveness for these vaccines, as opposed to reaching a narrow answer with high confidence. We detailed a large section on model uncertainty to understand these comparisons and tried to compare against other analyses (see [Appendix A](#appendixa)).  
  
Overall, while vaccination does have some clear wins, it does not seem to be a universal “best buy” 100% across the board. Smallpox eradication appears to be one of the most cost-effective interventions of all time, but HPV and Ebola vaccination (and even eradication) do not appear competitive with current opportunities in global health (see [Appendix B](#appendixb) for Ebola forecasting, [Appendix C](#appendixc) for comparisons between vaccination and current opportunities, and [Appendix D](#appendixd) for some analysis of GAVI). The only ongoing vaccine that could appear competitive to current global health opportunities is work on the malaria vaccine (see [Appendix C](#appendixc)), though other considerations could potentially make some other vaccine-related work more effective (see Appendix D). However, the multiple ways in which funding a concrete charity on the margin may differ from the abstract total cost-effectiveness of vaccination may make this comparison somewhat misleading altogether.

The desirability of funding a vaccine at the outset then seems to vary heavily on the underlying burden of the disease, but also on how efficiently a vaccine can be brought to market. If the cost of creating a vaccine is very high, as in the case of HIV, or the underlying burden of the disease is relatively low, as is the case with HPV or Ebola, the ultimate cost-effectiveness will suffer.

There are a lot of additional potential takeaways here, such as general lessons learned about cost-effectiveness modeling, which we’ll discuss in a final wrap-up essay.

  
# <a name="appendixa">Appendices</a>

## <a name="appendixa">Appendix A: What Do Other Articles Say?</a>

To compare our findings to other articles, we looked at some other articles that we could find comparing the cost-effectiveness of different vaccines[^10]. Comparing across all these studies gives further confidence in our estimates and understanding of model assumptions and model uncertainty.

Here’s what we end up concluding:

Study

Vaccines compared

Results

[Fesenfeld, Hutubessy, and Jit (2013)](https://www.ncbi.nlm.nih.gov/pubmed/23830973)

HPV

Our range fits inside their much wider range. Their range is much wider because they include a much wider range of assumptions for cost per dose.

[Levine, Kremer, & Albright (2005)](https://www.cgdev.org/doc/books/vaccine/MakingMarkets-complete.pdf)

Malaria

Their model is notably close to ours, despite different assumptions. When we change our model to match their assumptions, we are still close, but not exact.

[Winskill, Walker, Griffin, and Ghani (2017)](http://gh.bmj.com/content/2/1/e000090)

Malaria

Their model is more pessimistic than our model. However, they assume much lower efficacy for the malaria vaccine because they are modeling the vaccine as it currently is, while we are modeling the vaccine as we estimate it will be rolled out. When we change our model to match their assumptions, our ranges end up being very similar.

[Galactionova, et al. (2017)](https://www.sciencedirect.com/science/article/pii/S0264410X16311033?via%3Dihub)

Malaria

Their model starts with a very wide range. When we remove outlier countries with low information that create the wide range, we get a new range that falls within the range of our model when adjusting for the change in assumptions (similar to above).

[Seo, Baker, and Ngo (2004)](https://malariajournal.biomedcentral.com/articles/10.1186/1475-2875-13-66)

Malaria

They assume much lower efficacy for the malaria vaccine because they are modeling the vaccine as it currently is, while we are modeling the vaccine as we estimate it will be rolled out. However, they also assume a much wider variety in final price. Together, this makes a range that overlaps our range, but is wider and more pessimistic on average. When we change our model to match their assumptions, our ranges end up being very similar.

[Penny, et al. (2016)](https://www.sciencedirect.com/science/article/pii/S0140673615007254)

Malaria

They model the vaccine with a lower efficacy than we do, but not as lower as the other studies we compare against. When we change our model to match their assumptions, our ranges end up being very similar.

[Atherly, et al. (2009)](https://www.ncbi.nlm.nih.gov/pubmed/19817610)

Rotavirus

Their estimate falls within our range.

[Ozawa, et al. (2012)](https://www.sciencedirect.com/science/article/pii/S0264410X12015769)

HIV, HPV, Malaria, and Rotavirus

They provide a meta-analysis with many different ranges for many different vaccines. They generally match our ranges and the estimates that don’t are not from the same region we model (SSA).

[Dalton (2014)](https://www.fhi.ox.ac.uk/research-into-neglected-diseases/)

Malaria, HIV, and overall “typical” vaccine estimate

The malaria and overall estimates fall within our model ranges, but their HIV estimate is more optimistic than our model. Their model does not consider substantial roll-out costs, but also assumes far more R&D costs than our model.

[Dalton (2016)](https://docs.google.com/document/d/1Jmp1LQEem9E29ynSrqYrkiCsFFMrvyZLPqPl3Itdaak/edit)

Malaria, HIV, and overall “typical” vaccine estimate

The malaria and overall estimates fall within our model ranges, but their HIV estimate is more optimistic than our model. Their model does not consider substantial roll-out costs, but also assumes far more R&D costs than our model.

For details of the individual studies, see below.

  
  

### A.1.) Cost-effectiveness of HPV -- Fessenfeld, Hutubessy, and Jit (2013)  
  

[Fesenfeld, Hutubessy, and Jit (2013)](https://www.ncbi.nlm.nih.gov/pubmed/23830973) did a meta-analysis and found a cost-effectiveness of $146 to $34,382 per QALY in inflation-adjusted international dollars for the HPV vaccine (see Table 1) based on studies in Thailand and Mexico[^8]. [Our model for HPV finds](https://www.getguesstimate.com/models/10586) a cost-effectiveness of $370 - $1600 / DALY. Our estimate seems to fit snugly within their wide range.

But why does Fesenfeld, Hutubessy, and Jit (2013) have such a large range with such large values? Part of the reason for the large difference in estimations between sources and between the estimates given above are significant differences in cost estimation rather than fundamental methodological problems, as in these studies cost per HPV series estimates range from $49 to $511. In our model, if we use the more worst-case scenarios of cost per vaccine of $23 in the developing world, the cost-effectiveness of roll-out would be about $1964 per DALY while $49 per series yields an estimate of over $4000 per DALY.

Since prices in the developed world [can be as high as $400](http://kff.org/womens-health-policy/fact-sheet/the-hpv-vaccine-access-and-use-in/), the price per vaccine used would, naturally, significantly change the cost-effectiveness. Indeed, in the United States, cost-effectiveness has been benchmarked between $4,894 to $18,447 per QALY (adjusted for inflation between 2005 dollars to 2017 dollars) by [Chesson, Ekwueme, Saraiya, and Markowitz (2008)](https://wwwnc.cdc.gov/eid/article/14/2/pdfs/07-0499.pdf) and benchmarked at $31,441/QALY (after conversion from 2001 dollars) by [Sanders and Tiara (2003)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2873748/). If our model were scaled to have a $400 roll-out cost per person, it would agree with this, suggesting ~$35K/DALY.

Thus our model matches with the same parameters, but we don’t find the same need to be as uncertain about our assumptions of cost per dose.

  
  

### A.2.) Making Markets for Vaccines - Levine, Kremer, & Albright (2005)

[Levine, Kremer, & Albright (2005)](https://www.cgdev.org/doc/books/vaccine/MakingMarkets-complete.pdf) look at the cost-effectiveness of encouraging vaccine development for malaria, HIV, and tuberculosis. They explore the idea of creating an “advanced market commitment”, which is a legal commitment to purchase vaccines at a certain preset price once that vaccine is researched and developed, incentivizing that research to happen by providing a return that could be reasonably guaranteed and known in advance.

They estimate a $3B market in 2004 dollars would be necessary ($4B in 2018 dollars), assume that the cost of capital (interest rate) of 8%, discount DALYs at 3% per year, assume three doses of the vaccine will provide protection for five years, assume vaccines are 60% effective, and assume a vaccine price of $15 per vaccine and delivery costs of $0.75 per dose ($2.25 total) in 2004 dollars ($23 per person in 2018 dollars). The malaria vaccine is then modeled as returning $15/DALY in 2004 dollars, or ~$20/DALY in 2018 dollars. Levine, Kremer, & Albright (2005) [released a spreadsheet model of their calculations](https://www.cgdev.org/page/cost-effectiveness-tool).

On one hand, our estimates are very close, which is reassuring. Our models suggested malaria had a return of [$23 - $52 / DALY if vaccinating 60% of SSA](https://www.getguesstimate.com/models/10588) and [$11 - 18/DALY if vaccinating to eradication](https://www.getguesstimate.com/models/10601). These estimates are notably close to the $20/DALY given by Levine, Kremer, & Albright (2005). The $3B market size suggested by Levine, Kremer, & Albright (2005) is also shockingly close to the $3.17B we estimated would be needed to research, develop, and roll out a malaria vaccine.

On the other hand, our methodologies are different, and this is worth discussing in light of model uncertainty. Levine, Kremer, & Albright (2005) are modeling vaccinating 200M people in targeted areas. This is much larger than our SSA 60% scenario, which is modeled for ~96M children under 5 in the first year plus another ~22M children a year for every year after, and much smaller than our eradication scenario modeled for 675M people. Our model does not take into account an [advanced market commitment](http://www.who.int/immunization/newsroom/amcs/en/), models for a range of estimates for efficacy, and assumes a roll-out cost of $22 per person. When [we adjust our model to factor in the price, delivery costs, efficacy, and vaccinated population as Levine, Kremer, & Albright (2005)](https://www.getguesstimate.com/models/10646), we get $12 - $19 / DALY, which is more optimistic than Levine, Kremer, & Albright (2005) projects.  
  

Malaria Vaccine Cost-Effectiveness

Levine, Kremer & Albright (2005)

Our model -- 60% SSA scenario

Our model with LKA parameters

$20 / DALY

$23 - $52 / DALY

$12 - 19 / DALY

  
  
  

### A.3.) Modelling the cost-effectiveness of introducing the RTS,S malaria vaccine relative to scaling up other malaria interventions in sub-Saharan Africa -- Winskill, Walker, Griffin, and Ghani (2017)

[Winskill, Walker, Griffin, and Ghani (2017)](http://gh.bmj.com/content/2/1/e000090) set out to compare introducing the malaria vaccine to other malaria treatments like distributing bednets. We make a similar comparison in [Appendix C](#appendixc). They look directly at [the large phase III trial of the RTS,S malaria vaccine across 11 sites in Africa](http://www.who.int/malaria/media/rtss-phase-3-trial-qa/en/), which vaccinated ~15,500 children. Per Winskill, Walker, Griffin, and Ghani (2017)’s numbers, the vaccine had efficacy defined by a range between 13.7%-46.9% and cost $20 per child to administer. Given the observed transmission levels, they concluded an incremental cost-effectiveness ratio (ICER) of $44–$279 per DALY.

They also found a ICER per DALY of $27 ($8.15-$110/DALY) for long-lasting insecticide-treated nets (LLINs), $143/DALY (range $135-$150/DALY) for indoor residual spraying (IRS), and $68/DALY (range $62-$75/DALY) for seasonal malaria chemoprevention. By comparing ranges, distributing bednets came out ahead, but note that this may not hold as diminishing marginal returns are experienced by scaling up.

Malaria Vaccine Cost-Effectiveness

Winskill, Walker, Griffin, & Ghani (2017)

Our model -- 60% SSA scenario

Our model with WWGG parameters (roll out costs only)[^11]

$44 - $279 / DALY

$23 - $52 / DALY

$54 - 230 / DALY

  
  

Again, while our estimates look very different, it comes down to assumptions. When [we adjust our model to factor in the price, delivery costs, efficacy, and vaccinated population as Winskill, Walker, Griffin, & Ghani (2017)](https://www.getguesstimate.com/models/10654), we get $54 - $230 / DALY, which is very similar to their range. Winskill, Walker, Griffin, & Ghani (2017) made similar assumptions as us with regard to vaccine cost, but only considered four years of benefits (compared to us considering twenty), used a technically more accurate but much less optimistic vaccine effectiveness rate (we assume the rate would get better over time), uses a significantly smaller sample population (just that of the actual Phase III trial) and does not consider factoring in any fixed roll-out costs or R&D costs. Together, all of these changes in assumptions, except the last one, greatly increase the cost-effectiveness estimate.

Essentially, Winskill, Walker, Griffin, & Ghani (2017) is looking at the cost-effectiveness of rolling out the malaria vaccine as it exists right now, whereas we are looking at the cost-effectiveness of developing and rolling-out a future malaria vaccine that would likely reach higher efficacy targets more in line with existing vaccines and established cut-offs for minimum efficacy needed to have a viable vaccine.

  
  

### A.4.) Country-specific predictions of the cost-effectiveness of malaria vaccine -- Galactionova, et al. (2017)

[Galactionova, et al. (2017)](https://www.sciencedirect.com/science/article/pii/S0264410X16311033?via%3Dihub) models the existing RTS,S malaria vaccine and finds a median cost-effectiveness ratio of $188 per DALY averted, though with a very wide range of range of $78 - $22,448 / DALY. Assumptions made by Galactionova, et al. (2017) were similar to that of Winskill, Walker, Griffin, and Ghani (2017).

The range is so wide because of the inclusion of four countries where the predicted impact is highly imprecise due to a limitation of data. When those countries are excluded, the range is greatly reduced to between $115 and $220 / DALY (Galactionova, et al., 2017, section 3.2). This smaller range fits snugly within our model with parameters adapted from Winskill, Walker, Griffin, and Ghani (2017).

Malaria Vaccine Cost-Effectiveness

Galactionova, et al. (2017)

Galactionova, et al. (2017) -- narrower range

Our model -- 60% SSA scenario

Our model with WWGG parameters

$78 - $22,448 / DALY

$115 - $220 / DALY

$23 - $52 / DALY

$54 - 230 / DALY

  
  
  

Cost-effectiveness analysis of vaccinating children in Malawi with RTS,S vaccines in comparison with long-lasting insecticide-treated nets -- Seo, Baker, & Ngo (2004)

[Seo, Baker, and Ngo (2004)](https://malariajournal.biomedcentral.com/articles/10.1186/1475-2875-13-66) use data from the RTS,S trials and do a sensitivity analysis, varying time horizon, discount rates, vaccine efficacy, and price. While they do not directly state a confidence interval resulting from this sensitivity analysis, they headline a figure of $145.03 / DALY but suggest a range of $8 - $329.78 / DALY.

Malaria Vaccine Cost-Effectiveness

Seo, Baker, and Ngo (2004)

Our model -- 60% SSA scenario

Our model with WWGG parameters

$8 - $330 / DALY

$23 - $52 / DALY

$54 - 230 / DALY

The assumptions are similar to Winskill, Walker, Griffin, and Ghani (2017), which ends making the range given by Seo, Baker, and Ngo (2004) a close match for the range constructed from the parameters from Winskill, Walker, Griffin, and Ghani (2017) -- the maximums of the range are nearly the same. However, Seo, Baker, and Ngo (2004) is more optimistic because they consider possibilities such as $1/dose ($4/person roll-out cost, or ~18% of what we project in our model) in their sensitivity analysis.

  
  

### A.5.) Public health impact and cost-effectiveness of the RTS,S/AS01 malaria vaccine: a systematic comparison of predictions from four mathematical models -- Penny, et al. (2016)

[Penny, et al. (2016)](https://www.sciencedirect.com/science/article/pii/S0140673615007254) is of particular importance because its estimates form the basis for much of the GAVI (2016) report on malaria that we rely on for a lot of our models. Like the previous articles we considered, Penny, et al. (2016) looks at the data from the RTS,S trials. However, unlike these previous articles, they attempt to extrapolate the data from this trial to future cost-effectiveness using multiple models. This matches much closer to what we intend to do, but still doesn’t fully match our assumptions of large potential future increases in vaccine efficacy following further R&D spending prior to achieving licensing and large-scale roll-out of a future vaccine.

Focusing on their four-dose model, their model captures ten years of benefits and uses a declining exponential decay curve of efficacy with a mean of ~6% - ~25% over those ten years, depending on the model used (see Figure S2.1). They also vary the price between $8-$40 per fully vaccinated child. [Integrating these efficacy and price figures into our model](https://www.getguesstimate.com/models/10666) for a population of 100,000 vaccinated children over ten years gives us a result of $28 - $270 / DALY, which is a slightly wider range but captures all the values found from Penny, et. al. (2016)’s range.

Penny, et al. (2016)

Our model -- 60% SSA scenario

Our model with Penny parameters

$48 - $244 / DALY

$23 - $52 / DALY

$28 - $270 / DALY

  
  
  

### A.6.) Rotavirus vaccination: cost-effectiveness -- Atherly, et al. (2009)

[Atherly, et al. (2009)](https://www.ncbi.nlm.nih.gov/pubmed/19817610) looks at the cost-effectiveness of rotavirus across most of the GAVI-eligible countries using a demand forecast model was used to predict adoption, and then modeling health outcomes of a hypothetical birth cohort in the target population, and finds increasing cost-effectiveness of distributing the rotavirus vaccine over time, ultimately resulting in a cumulative figure of “$43 per DALY averted during 2008-2025”. This estimate is within the range we give for our estimate, despite differences in methodology and context.

Rotavirus Vaccine Cost-Effectiveness

Atherly, et al. (2009)

Our model

(60% SSA scenario, roll out costs only)

$43 / DALY

$6 - $59 / DALY

  
  
  

### A.7.) Cost-effectiveness and economic benefits of vaccines in low- and middle-income countries: A systematic review -- Ozawa, et al., 2012

[Ozawa, et al. (2012)](https://www.sciencedirect.com/science/article/pii/S0264410X12015769) does a meta-analysis of vaccine cost-effectiveness, finding 44 articles that reported costs per DALY averted. Data available in Table 1 gives a variety of ranges for many vaccines -- the ones that overlap with vaccines we considered include HIV, HPV, malaria, and rotavirus.

Vaccine

Our 60% SSA Range (roll out costs only)

Ranges Given in Ozawaa, et al., 2012 Meta-Analysis

HIV

$85 - $550 / DALY

$108 - $1308 / DALY

$123 - $1350 / DALY

$393 - $2108 / DALY

HPV

$240 - $1300 / DALY

<$152/DALY

<$304/DALY

<$304/DALY

<$759/DALY

<$759/DALY

<$1214/DALY

<$438/DALY

Malaria

$21 - $49 / DALY

$10 - $15/DALY

$16 - $27/DALY

$31 - $49/DALY

$44 - $72/DALY

$58 - $95/DALY

$72 - $118/DALY

$141 - $233/DALY

Rotavirus

$6 - $59 / DALY

$5-82/DALY (SSA)

$33/DALY (SSA)

$46 - $169/DALY (LMIC)

$36 - $550/DALY (LMIC)

While the HIV range does overlap some, Ozawa, et al. (2012) points to much more pessimistic HIV ranges than our estimate. It’s hard to figure out why without digging into the underlying study, but one likely reason is simply context -- the HIV estimates in Ozawa, et al. (2012) come from Thailand, instead of SSA.

The HPV estimates from Ozawa, et al. (2012) frustratingly only give upper bounds, and while they are generally more optimistic than our range, all but one of them do fit in our range.

The malaria estimates from Ozawa, et al. (2012) are nicely clustered around our estimate. The reason why they vary is because each estimate has been constructed from a different assumption about vaccine price per dose. When you take the estimate that matches our projection of price per dose at $4-5/dose, you end up with the estimate that is $31 - $49/DALY, which is an incredibly close match to our actual estimate of $21 - $49 / DALY.

Ozawa, et al. (2012) cites 105 different rotavirus cost-effectiveness estimates from around the world, so we don’t cite them all in the table. Instead, we picked the estimates that were specifically for SSA countries or for lower and middle-income countries (LMIC) generally. For those who had point estimates that varied by dose, we changed them to a range. The first two estimates from SSA countries were very close to our estimate and the two estimates for LMIC generally overlapped with our estimate but were more pessimistic. This is likely because LMIC generally are wealthier and have a lower disease burden than SSC specifically.

  
  

### A.8.) Dalton (2014)

[Dalton (2014)](https://www.fhi.ox.ac.uk/research-into-neglected-diseases/) models “the marginal, ex-ante cost-effectiveness of funding medical research” as a “problem of unknown difficulty” ([Cotton-Barrat 2014a](http://www.fhi.ox.ac.uk/how-to-treat-problems-of-unknown-difficulty/), [Cotton-Barrat 2014b](http://www.fhi.ox.ac.uk/estimating-cost-effectiveness/)), which assumes a discrete, fixed outcome (e.g., the vaccine is made) will be achieved after an unknown amount of resources (e.g., money, staff time, randomized controlled trials) are used. We model this discrete jump from 0 to 1 as a continuous probability curve over time and then estimate this probability curve with a lognormal distribution.

When applying this to funding for neglected tropical diseases, Dalton (2014) considers additional funding as “bringing forward the date of technological discovery, and therefore shifting forward the roll-out of the vaccine/drug” to the point of total eradication and that therefore “the gain of shifting forward vaccine discovery by a year equals the current annual disease burden”. Dalton (2014) finds a median impact of 13.9 DALYs/$1000 ($71.94 / DALY).

To compare with our work, we both modeled for HIV and malaria specifically. Dalton (2014) calculated these to be 11.2 DALYs / $1000 ($89.29 / DALY) for HIV and 22 DALYs / $1000 ($45.45 / DALY) for malaria ([see calculations in their associated spreadsheet](https://docs.google.com/spreadsheet/ccc?key=0AuSyxcRgBGt3dFJXMFczelpyRkFRRVJvX1NYeDB6Z2c&usp=sharing)). On the other hand, our models suggested malaria had a return of [$23 - $52 / DALY if vaccinating 60% of SSA](https://www.getguesstimate.com/models/10588) and [$11 - 18/DALY if vaccinating to eradication](https://www.getguesstimate.com/models/10601) and HIV was [$210 - $690 / DALY for 60% of SSA](https://www.getguesstimate.com/models/10583) and [$300 - $1600 / DALY for eradication](https://www.getguesstimate.com/models/10603).

Vaccine

Dalton (2014)

60% SSA scenario

Eradication scenario

Malaria

$45.45 / DALY

$23 - $52 / DALY

$11 - 18 / DALY

HIV

$89.29 / DALY

$210 - $690 / DALY

$300 - $1600 / DALY

“Typical” Vaccine

$71.94 / DALY

$18 - $7000 / DALY

$10 - $8100 / DALY

  
  

Dalton (2014) was solidly in our 60% SSA range for the malaria vaccine, but optimistic compared to both our ranges on HIV vaccine. (It was within the same range as our “typical” vaccine too, but that’s a very big range.) Where might that discrepancy lie?

Dalton (2014)’s analysis is a completely different kind of model than our analysis, so a direct comparison is difficult. Notably, Dalton (2014) notes that the “\[c\]osts of distribution were not accounted for”, which for complete eradication of a disease is very considerable. Our estimate is this would add roughly $3.6B-$5B for vaccinating 60% of SSA for malaria, $13B-$18B for eradicating malaria, $19B-$100B for vaccinating 60% of SSA for HIV, and $180B-$960B for eradicating HIV.

On the other hand, Dalton (2014) also models the spending on research and development for malaria using data from [GFinder (2013)](http://www.policycures.org/downloads/04_GF_report13_web_Findings%E2%80%93Funding%20by%20Disease.pdf), which includes all R&D spending -- including not only vaccines, but also other drugs, microbicides, diagnostics, and basic research. Given that Dalton (2014) intended to model the returns of research as a whole this seems appropriate but reduces the ability to compare meaningfully to our work to model the cost-effectiveness of vaccine R&D in particular.

Furthermore, [GFinder (2013)](http://www.policycures.org/downloads/04_GF_report13_web_Findings%E2%80%93Funding%20by%20Disease.pdf) also uses a total for malaria vaccine research that is higher than the total documented in [GAVI (2016)](http://www.gavi.org/about/governance/gavi-board/minutes/2016/22-june/minutes/09---malaria-vaccine-pilots---appendices/) that we rely on for our estimate. In total, we assume that a malaria vaccine [could be created with an investment of $605M](/ea/1l4/how_much_does_it_cost_to_research_and_develop_a/), whereas GFinder (2013) assumes a total spend of over $3B[^12], and Dalton (2014) extrapolates to a total R&D spend of over $67B on malaria, over 100x our estimate for malaria R&D costs and over 4x our estimate for all costs for malaria eradication.

Given that in our model, for HIV the R&D costs are much more prominent than for malaria, the underestimation in roll-out costs and the overestimation in R&D costs by Dalton (2014) relative to our model would explain the discrepancy.

  
  

### A.9.) Dalton (2016)’s Novel Model Adapted from Karnofsky (2014).

Dalton (2016) produces a novel model based on [Karnofsky (2014)](https://www.openphilanthropy.org/blog/returns-life-sciences-funding)’s work. This model assumes that the entire DALY burden of a disease will eventually be eliminated and that new research will be responsible for 50% of this reduction. The benefits would have a lag of 50 years and require discounting at a 3% annual rate, but benefits will grow with population growth. Applying this gave a mean of $51.91/DALY for HIV and $44.14/DALY for malaria ([see spreadsheet here](https://docs.google.com/spreadsheets/d/1B7MPlhSnGRifioy_4RCZe8tPuRtQBqSUwZ9SmeKnmeA/edit#gid=0)).

Vaccine

Dalton (2014)

Dalton (2016)

60% SSA

Eradication

Malaria

$45.45 / DALY

$44.14 / DALY

$23 - $52 / DALY

$11 - 18 / DALY

HIV

$89.29 / DALY

$51.91 / DALY

$210 - $690 / DALY

$300 - $1600 / DALY

“Typical” / Median

$71.94 / DALY

$34.37 / DALY

$18 - $7000 / DALY

$10 - $8100 / DALY

  
  

As Dalton (2016) admits, this is a relatively simplistic model. Like Dalton (2014), this model is hard to compare to our model as it works very differently. The dynamics are also very similar -- like Dalton (2014), Dalton (2016) does not directly consider vaccine roll-out costs, except insofar as this may be responsible for assuming that new research is only responsible for 50% of the total reduction. Moreover, Dalton (2016)’s novel model, like Dalton (2014), uses data from GFinder (2013) that may be misleading for the particular application.

  
  

## <a name="appendixb">Appendix B: Forecasting Cost-Effectiveness for Ebola</a>

Based on the cost-effectiveness modeling in this essay, we could consider using our model to forecast the cost-effectiveness of the Ebola vaccine, which is currently under active development and relatively unknown. We previously found the Ebola vaccine to likely cost ~$1.5B in R&D and to become licensed in ~2022, but we do not know much about the relevant roll-out costs. We’ve also estimated Ebola vaccination to potentially avert 92,685 DALYs per year if rolled out to 60% of the relevant SSA population, assuming the average DALY burden of the last five years, and to prevent ~308,900 DALYs given these assumptions if Ebola were eradicated. Assuming the much higher burden seen during the 2014 outbreak of ~1.3M DALYs per year, ~388,000 DALYs could be prevented by vaccinating 60% of the relevant population[^13].

Based on our model, we can create guesses for Ebola based on a variety of potential costs of the Ebola vaccine. We can also vary how focused the population targeted for vaccination is. A broad distribution of the Ebola vaccine may be highly unrealistic. [Merler, et al. (2016)](http://journals.plos.org/plosntds/article?id=10.1371/journal.pntd.0005093), for example, advocates for “ring vaccination,” which targets (in some combination) those who have been in direct contact with someone infected, contacts of contacts, and the population in geographic rings around them. The population in the [Henao-Restrepo, et al. (2016)](http://www.thelancet.com/journals/lancet/article/PIIS0140-6736(16)32621-6/fulltext) Ebola trial was vaccinated on this basis and smallpox was eradicated in part due to such measures ([Strassburg, 1982](https://www.ncbi.nlm.nih.gov/pubmed/7044193)). Also, as Merler, et al. (2016) mentions, future Ebola outbreaks in different regions could have a different basic reproduction number (the number of cases an infected person generates, on average, over their infection period), implying a different approach to be taken.  It’s unclear to us what this suggests about the population needed for eradication.

We assume that our above calculations are right, that the vaccine will be 50% effective[^14], and that there is a $100M fixed cost associated with developing vaccination infrastructure.

Ebola Eradication Cost-effectiveness

Vaccination Strategy

Population Scenario

Cost-effectiveness

Guesstimate

Ring

60% SSA

$88 - $1100 / DALY

[Link](https://www.getguesstimate.com/models/10611)

Widespread

60% SSA

$280 - $6200 / DALY

[Link](https://www.getguesstimate.com/models/10612)

Ring

Global Eradication

$70 - $850 / DALY

[Link](https://www.getguesstimate.com/models/10613)

Widespread

Global Eradication

$130 - $2200 / DALY

[Link](https://www.getguesstimate.com/models/10617)

  
  
  

## <a name="appendixc">Appendix C: Comparing to Against Malaria Foundation</a>

GiveWell has pretty thoroughly vetted the Against Malaria Foundation and found it to create the equivalent value of saving the life of a child under 5 for $764 to $3057 (average $2087) ([GiveWell, 2018](https://www.givewell.org/how-we-work/our-criteria/cost-effectiveness/cost-effectiveness-models)). While GiveWell would not want us crudely converting this figure to DALYs, we need to do so to have a remotely comparable analysis, so we consider saving the life of a child under 5 to allow them to live to the typical life expectancy of SSA -- [59 years total](https://data.worldbank.org/indicator/SP.DYN.LE00.IN?locations=ZG), or an additional 53 years -- at full health, which would be 53 DALYs averted. Thus, AMF would be at ~$15 - $58 per DALY averted (average $39).

  
  

Scenario 1: Vaccinate 60% of the relevant populations in SSA

Opportunity

Cost-effectiveness range

Mean estimate

Smallpox vaccine

$4 - $67 / DALY

$22 / DALY

Malaria vaccine

$23 - $52 / DALY

$34 / DALY

Rotavirus vaccine

$10 - $64 / DALY

$36 / DALY

Donate to AMF

$15 - $58 / DALY

$39 / DALY

Measles vaccine

$9 - $320 / DALY

$73 / DALY

Ebola vaccine - ring

$88 - $1100 / DALY

$380 / DALY

HIV vaccine

$210 - $690 / DALY

$410 / DALY

HPV vaccine

$370 - $1600 / DALY

$900 / DALY

Ebola vaccine - widespread

$280 - $6.2K / DALY

$1.7K / DALY

  
  

Scenario 2: Eradicate the disease completely

Opportunity

Cost-effectiveness range

Mean estimate

Smallpox vaccine

$0.44 - $5.80 / DALY

$1.20 / DALY

Measles vaccine

$0.37 - $13 / DALY

$3 / DALY

Malaria vaccine

$13 - $23 / DALY

$17 / DALY

Donate to AMF

$15 - $58 / DALY

$39 / DALY

HPV vaccine

$80 - $370 / DALY

$200 / DALY

Ebola vaccine - ring

$70 - $850 / DALY

$300 / DALY

Ebola vaccine - widespread

$130 - $2200 / DALY

$660 / DALY

HIV vaccine

$300 - $1600 / DALY

$900 / DALY

  
  

If you take this analysis literally, donating to AMF may be more attractive on an average $ / DALY basis than helping eradicate HPV, HIV, or Ebola, but not compared to eradicating smallpox, malaria, or measles. Donating to AMF also emerges better than helping research, develop, and roll-out all vaccines we examined that stop short of eradication except for malaria smallpox, and rotavirus.

However, the estimate of the malaria vaccine compared to donating to AMF are substantially close and the range overlaps. Thus the conclusion could be very sensitive to our particular assumptions. Notably, the current academic literature suggests that increasing bednets is more cost-effective than rolling out existing malaria vaccines ([Penny, et al., 2016;](https://www.sciencedirect.com/science/article/pii/S0140673615007254) [Winskill, Walker, Griffin, & Ghani, 2017)](http://gh.bmj.com/content/2/1/e000090).

While the comparison between bednet distribution and the malaria vaccine is interesting, it is unclear how meaningful this comparison is. It’s worth noting that the calculations for AMF are likely more robust, which could favor AMF further if a Bayesian adjustment framework were used (for examples, see [Karnofsky (2011)](https://blog.givewell.org/2011/08/18/why-we-cant-take-expected-value-estimates-literally-even-when-theyre-unbiased/) and [Dickens (2016)](/ea/vo/expected_value_estimates_you_can_maybe_take/)).

Additionally, charities themselves, like a charity set up to fund and distribute a malaria vaccine, could differ in marginal cost-effectiveness from the abstract intervention in a way that would undermine the comparison further and make AMF more or less appealing.

  
  

## <a name="appendixd">Appendix D: Cost-Effectiveness of GAVI</a>

[GAVI](https://www.gavi.org/), a global organization that helps distribute vaccines, is considered to be very cost-effective. A full analysis of the cost-effectiveness of GAVI is greatly beyond the scope of this article, as the use of “leveraged funding” and the difference between marginal vs. total costing approaches, makes the cost-effectiveness estimate vary greatly from that of individual vaccines (see discussion in our discussion of assumptions).

However, we can look at three sources: [Francis (2010)](http://gsid.org/downloads/successes_and_failures_final.pdf) quotes GAVI as averting 5M deaths against $3.7B in funding, for a cost-effectiveness of $740 per life saved. [Lob-Levyt (2011)](http://rstb.royalsocietypublishing.org/content/royptb/366/1579/2743.full.pdf) quotes GAVI as averting 5.4M vaccine-related deaths against $4491M in vaccine-related spending or $831.67 per life saved. Lastly, a [GAVI press release](http://www.gavi.org/library/news/press-releases/2010/gavi-alliance-set-to-save-four-million-lives-by-2015/) quotes GAVI as saving 4M lives against $3.7B or $925 per life saved. When we take these estimates literally, and consider a figure of 30 DALYs per life saved[^6], and compare this on a table to our estimates of vaccines, GAVI comes out more cost-effective than the distribution for all of the vaccines except smallpox at 60% of SSA.

Opportunity

Cost-effectiveness range

Mean estimate

Smallpox vaccine

$4 - $67 / DALY

$22 / DALY

Francis (2010) estimate of GAVI

 

$24.66 / DALY

Lob-Levyt (2011) estimate of GAVI

 

$27.72 / DALY

GAVI estimate of GAVI

 

$30.83 / DALY

Malaria vaccine

$23 - $52 / DALY

$34 / DALY

Rotavirus vaccine

$10 - $64 / DALY

$36 / DALY

Donate to AMF

$15 - $58 / DALY

$39 / DALY

Measles vaccine

$9 - $320 / DALY

$73 / DALY

Ebola vaccine - ring

$88 - $1100 / DALY

$380 / DALY

HIV vaccine

$210 - $690 / DALY

$410 / DALY

HPV vaccine

$370 - $1600 / DALY

$900 / DALY

Ebola vaccine - widespread

$280 - $6.2K / DALY

$1.7K / DALY

The fact that these estimates of GAVI appear more cost-effective than the individual vaccines is not unbelievable, due to massive use of “leveraged funding” and the use of vaccines that may well be very cost-effective that we did not model (e.g., the meningitis A vaccine, the pneumococcal vaccine).

# <a name="endnotes">Endnotes</a>

[^1]: Note that because Guesstimate uses a pseudo-random Monte Carlo simulation to explore inputs to create intervals, the intervals in the model may not precisely match the inputs in the table. Also, the $/DALY values from Guesstimate may differ some from the $/DALY values in the spreadsheet due to Guesstimate aggregating ranges rather than point estimates. Also, some of the spreadsheet rows are exploring particular scenarios that are not necessary to consider for an overall estimate. When the Guesstimate and spreadsheet differ, the Guesstimate should be considered more accurate.

[^2]: This Guesstimate was constructed by combining the lower and upper bounds of all the ranges of vaccines we looked at. R&D costs and roll-out costs were calculated for a “typical” vaccine in the respective previous posts (see[R&D costs](/ea/1l4/how_much_does_it_cost_to_research_and_develop_a/) and [roll-out costs](/ea/1l5/how_much_does_it_cost_to_rollout_a_vaccine/) analysis). Note that this estimate is a mere extrapolation from vaccines that we considered (and believe to be representative), but may not be indicative of other vaccines we did not consider.

[^3]: If you calculate the expected expenditures for the eradication of smallpox, at an inflation-adjusted $0.73, for an approximate 977 million people, you come up with roughly $900 million, which is a significant underestimate of the nearly $2.1 billion the eradication actually costs after adjusting for inflation (Fenner, et al., 1988). This is likely because the eradication did not take place all at once, but was distributed over a 13 year period. To produce that figure, assuming the same vaccination costs per person, the actual the number of people vaccinated would have to have been roughly 2.4 billion. To adjust for this, we have increased the upper ranges on the population and roll out costs.

[^4]: The efficacy used to estimate the initial cost-effectiveness is low enough that it is unlikely that herd immunity could be achieved or that an eradication program could prove effective. For example, the vaccine efficacy needed to help eradicate malaria is likely far higher than the current efficacy of 39%, or the 50% guess we used to help estimate the cost-effectiveness of the roll-out of the malaria vaccine. It might need to be, say, 80% to be effective enough to suppress malaria incidence enough to make eradication feasible. Our eradication estimates, unlike the roll-out estimates, simply assume vaccine efficacy would be sufficiently high to make eradication possible. The actual vaccine efficacy at the time of any such attempt at eradication would heavily impact how many people need to be vaccinated, and thus our final end line estimate of eradication costs. For a more thorough view of how herd immunity impacts the effectiveness of vaccination campaigns see [Fine, Eames, and Heymann (2011)](https://academic.oup.com/cid/article/52/7/911/299077).

[^5]: Even if eradication is achieved, there still will be some ongoing costs related to disease surveillance and to ensure eradication, plus some continued development of the vaccine to protect against possible new outbreaks.

[^6]: It’s unclear what the correct DALYs per death figure should be. We follow [Karnofsky (2007)](https://blog.givewell.org/2007/12/04/what-a-life-saved-means/) which estimated that a “life saved” in SSA for a child under five gives them a 50% chance of living another 60 years, or an expected value of 30 years (see [more here](https://www.givewell.org/international/technical/additional/life-expectancy-in-SSA)). However, reverse engineering a DALY/death figure from [Global Burden of Disease (2016e)](http://ghdx.healthdata.org/gbd-results-tool?params=gbd-api-2016-permalink/d272971954dccd2dc5db017a825e3485) suggests a DALY per death figure of 84 DALYs/death, which seems intuitively high.

[^7]: Forsythe is estimating initial costs but there’s reason to believe that the initial prices won’t be steady. For example, the HPV vaccines currently cost ~$48 for developing countries or $13.50 for full vaccination by GAVI. Forsythe notes the initial international median price was ~$465 per patient. Even at the higher estimate of current price, that's a ~90% decline from the initial median price.

[^8]: Some studies included comparisons of vaccination to screening for cervical cancer and to no preventative treatment. Both the upper and lower ends given are from the same study in Mexico with the upper-end figure of $34,382 per QALY ($31,600 in 2011 international dollars) from comparing screening and the $146 ($134 in 2011 international dollars) from vaccination compared to no treatment. The full range of cost per QALY in the cited studies for vaccination compared to no prevention is $146 to $13,709 while the range for vaccination compared to screening is $12,655 to $34,382 ($11,631to $31,600 in 2011 international dollars).

[^9]: Given it’s a disease that is most burdensome on those of reproductive age, the population aged 15-49 may be targeted. However, a much larger group of everyone over 10 could feasibly be targeted, particularly in the initial phase of the roll-out. As for the cost per person, [Forsythe, 2011](http://www.copenhagenconsensus.com/sites/default/files/forsythe.pdf) suggests the price of roll-out of the vaccine could be between $60 and $465\. Our Guesstimate model incorporated this uncertainty of the population of interest and the cost per person of vaccination.

[^10]: Articles were found by searching Google Scholar for various keywords like “[vaccine name] cost-effectiveness” and “[vaccine name] DALY”, in addition to  considering all the articles and models mentioned in Dalton (2016).

[^11]: We only consider roll-out costs here because (1) the population of 15500 is too small to meaningfully amortize vaccine R&D costs and (2) the original study (Winskill, Walker, Griffin, & Ghani (2017)) does not consider R&D costs in their model.

[^12]: GFinder (2013) has a total spend $3.2B on all research for malaria from 2007 to 2012, 33% of which is spent on vaccines, for a total of $1B.

[^13]: These estimates are not adjusted for the difference in population between 2014 and 2016 in the outbreak regions possibly producing a different, and higher, overall burden of disease.

[^14]: [While an initial trial of Ebola found 100% efficacy](https://www.nytimes.com/2016/12/22/health/ebola-vaccine.html) (see[Henao-Restrepo, et al., (2016)](http://www.thelancet.com/journals/lancet/article/PIIS0140-6736(16)32621-6/fulltext) for the study), this was a low sample size and had [other methodological shortcomings](https://www.wired.com/2015/08/100-percent-effective-means-ebola-vaccine/), so we still default to a prior guess of 50%.