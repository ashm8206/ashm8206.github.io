---
layout: post
title:  "US Primaries Sentiment Analysis"
date:   2016-07-29 08:43:59
author:  Aishwarya Mali
cover: "/assets/US-Primaries-Sentiment-Analysis/cover.jpg"
categories: datascience

---

The USA campaigns have been a trending topic for quite some time now. I thought of pulling
some stats from twitter text, to gauge for myself some key insights of the campaign. The analysis below was performed immediately after RNC and DNC conventions. Historically there have been spikes in candidate Approval-ratings post Party [Conventions.](http://www.economist.com/blogs/graphicdetail/2016/08/daily-chart-2)
Performing this analysis post Conventions was key as there was a high chance of plotting interesting patterns now that both party VP tickets were announced. Below are some graphs plotted using Seaborn and Matplotlib. Sentiment Analysis was performed using Textblob Library.
					
<img src = "/assets/US-Primaries-Sentiment-Analysis/mean_cltr.png" alt="Mean">
Lets look at Mean first. We can see that almost all comments about Trump are negative since the Mean is closer to zero. Value for each data point can be -1 to 1, where -1 means negative comment, and 1 means positive comment. The closer the Mean is to zero the more negative the comments about the candidate. An interesting point to note is that Trump-Pence ticket choice is appreciated a lot more than Clinton-Kain. Will it come down to the choice of VP between Clinton and Trump? It remains to be seen as the above Mean is just a Random Sample Mean.
<img src = "/assets/US-Primaries-Sentiment-Analysis/stadard_devi.png" alt="Standard Deviation">
With the Standard Deviation chart we can see that our data collected is not very dispersed, we will need to collect more data to qualify the Mean chart.Data could be collected at various times of the day, this would lead to collecting data from twitters from varied age-groups.[Here is my Twitter Scraper Code](https://github.com/ashm8206/ClintonTrumpPostConventions/blob/master/scraper.py)
<img src = "/assets/US-Primaries-Sentiment-Analysis/year_candi.png">
This map is stacked for number of Clinton tweets vs Trump tweets as per twitter account age. It is safe to say that for this sample candidate Donald Trump has maximum number of tweets, from the new twitter account holders and again from older 8 year old account holders.
Thus, the 35-49 year olds are likely to tweet about Trump [as nearly 20% of all twitter users that joint the site in 2008(8 years back)were aged between 25-34.](http://www.pewinternet.org/2009/02/12/twitter-and-status-updating) Also, 18-29 year olds are much more likely to tweet about Trump as is clear 2016 twitter demographics [where they make up nearly 37% of the twitter population.](https://blog.hootsuite.com/top-social-media-sites-matter-to-marketers/)
[Read more..](https://github.com/ashm8206/ClintonTrumpPostConventions/blob/master/ClintonTrumpPostConventions.ipynb)


