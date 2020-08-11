# Analysis of Drug Use By Age

#### By Landon Iannamico

I chose the dataset "Drug Use by Age" from FiveThirtyEight's github, which can be found [here.](https://github.com/fivethirtyeight/data/blob/master/drug-use-by-age/drug-use-by-age.csv)

This data had information about the percentage of the respondents who reported using certain drugs within the past 12 months, and the frequency in which they used those drugs over the past 12 months. The data covers 13 different drugs across 17 age groups. The data came in one csv file that I put onto a google sheet. I then did the following to analyze the data:
* Sorted heroin use z-a to find the top groups were: 22-23 (1.1%), 20 (0.9%), and 24-25 (0.7%)
* Sorted hallucinogen use z-a to find the top groups: 19 (8.6%), 20 (7.4%), and 19 (7%). 
* Sorted hallucinogen frequency Z-A, to find the top groups: 12 (52), 50-64 (44), 13 (6)
* Sorted inhalant use Z-A, to find the top groups: 16 (3%), 14 (2.6%), 15 (2.5%) , 13 (2.5%)


An interesting finding here was that heroin was used by the oldest groups, hallucinogens were a bit younger but still within the usual drug experimentation age, and inhalants were the youngest. This confirmed my suspicions that inhalants would be more popular among young people who may not have legal or illegal access to more 'serious' drugs. I also speculated that heroin was something people do after they've been doing drugs for a while, and is something older people are more likely to do since it is usually done out of necessity rather than fun. This is in contrast to psychedelics which are rarely done habitually and are more often used for experimentation and fun, so they would attract a demographic that doesn't have quite as many formal responsibilities yet. Finally, a notable outlier was the 50-64 group in hallucinogen frequency. The hallucinogen use for this age group was only 0.3%, so I suspect there were a handful of people or maybe even one person who used them extremely frequently and skewed the data. 

I then became interested in comparing different drugs in pivot tables. I ran a pivot table comparing cocaine and meth use, cocaine and heroin use, and marijuana and alcohol use. The marijuana and alcohol was of particular interest to me, so I made a new sheet with just age, marijuana use, and alcohol use. I then exported this sheet into datawrapper and made a double column chart comparing the two, which can be viewed [here](https://www.datawrapper.de/_/KtiSm/), or below:

<iframe title="Marijuana and Alcohol Use By Age" aria-label="chart" id="datawrapper-chart-KtiSm" src="https://datawrapper.dwcdn.net/KtiSm/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="600"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

I was surprised to learn that alcohol was so much popular than marijuana amongst all age groups, with marjuana use routinely being half as popular (or less) as alcohol use. Most people I know either do both, or only use marijuana. I do, of course, live in California though, and since this data was taken nationally, it is possible that other states have different social norms about which drugs are more or less acceptable to use. I was also surprised that more baby boomers, who lived through the sixties, didn't use marijuana, with 7.3% of the 50-64 age group using marijuana compared to 67.2% using alcohol, and 1.2% marijuana compared to 49.3% alcohol with the 65+ group. The highest marijuana use (34%) was with 20-year-olds, compared to 69.7% alcohol use, meaning that alcohol still beats marijuana by approximately 100% even amongst marijuana's most popular demographic.

I then wanted to find a way to group together the depressants and stimulants because I noticed they were each divided into multiple categories in the original data. I tried using OpenRefine to consolidate the groups together but could not figure out how to do this the way I wanted to, so I went back to google sheets and just made a seperate sheet. I made 5 columns: age, stimulant use total, stimulant frequency total, depressant use total, depressant frequency total. I lumped the categories like this:
* stimulants: crack, cocaine, stimulant, meth
* depressants: heroin, pain reliever, oxycontin, tranquilizer, sedative

I used formulas that just added the sum of values for each specific drug, for example:

``` 
='drug-use-by-age'!G9+'drug-use-by-age'!I9+'drug-use-by-age'!W9+'drug-use-by-age'!Y9 
```

I made a table out of this on datawrapper, which can be viewed [here](https://www.datawrapper.de/_/jXH6S/), or below. It is important to note that these sums may not be an accurate reflection of the true percentage of the population that does each group of drugs and are rather approximate values used for comparison reasons. 

<iframe title="Stimulant And Depressant Total Use And Frequency By Age" aria-label="chart" id="datawrapper-chart-jXH6S" src="https://datawrapper.dwcdn.net/jXH6S/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="901"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

I did not include marijuana or alcohol in these categories as I felt both were too popular and I wanted to just look at less conventional drugs that more classically fell into the two categories of stimulant and depressant. My goal with this analysis was to see which age groups felt there was a benefit from the effects of stimulants (feeling awake, excited, productive) vs the effects of depressants (feeling sedated, sluggish, calmed down). My hunch was that younger people, who are busier and have more stamina, would be more inclined to use stimulants, and the older population would benefit more from depressants. There is also the myth that college students do adderall/other stimulants, and the older population is more likely to struggle with pain, which would lead to higher opiod use. I sorted z-a on all four columns to the following results:
* top stimulant use: age 20 (10.4), 21 (10), 22-23 (9.2), 19 (8.3)
* top depressant use: age 20 (18.5), 22-23 (17.4), 18 (16.6)
* top stimulant frequency: age 65+ (364), 35-49 (191), 50-64 (152), 19 (118.5)
* top depressant frequency: age 35-49 (320), 19 (210), 50-64 (172), 65+ (164)

From these results, my hunch is absolutely not true. Younger people tend to use both types of drugs more than older people, and older people tend to use stimulants more frequently. More interestingly though, I did notice that the 65+ age group had "0" under stimulant use, but somehow had 364 under stimulant frequency. This kind of pattern occurred on several other drugs, including heroin and sedatives, as well as the hallucinogen category that I noticed earlier. I first suspected this might've been a data error that happened when I changed blank cells/cells with '-' (no data) into '0''s, but when I checked back on the original data, all three of these categories originally had a zero, not a '-'. To inspect this further, I made a new sheet comparing the age groups 50-64. 65+, 20, and 21. I then made a bar chart comparing the use and frequencies of each age group, which can be viewed [here](https://www.datawrapper.de/_/ZqXhP/), or below. 

<iframe title="Use Vs. Frequency of Use of Drugs By Older And Younger Age Groups" aria-label="Split Bars" id="datawrapper-chart-ZqXhP" src="https://datawrapper.dwcdn.net/ZqXhP/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1003"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

As can be viewed in the chart, the older ages have more wide discrepancies between drug use and drug frequency. I highlighted several drugs where this was particularly prevalent, including some that had zero values under use and larger numbers under frequency. If it is to be assumed that these discrepancies aren't due to statistical errors and are instead representative of statistically insignificant low percentages of drug use for the older age groups, then the conclusion could once again be drawn that in older populations, although very few people use drugs, the ones that do use them use them very frequently. I believe this may be true because the pattern of higher discrepancy in the older age groups remains true even in use values that aren't 0, it is a consistent pattern that persists throughout all the different drugs. This could be because younger people have a more casual culture around drug use, while older people need to make more of an effort to get drugs. The older people that do get drugs must be more serious and commited about doing them, whether that be because of addiction/necessity, medical needs, or lifestyle choices. 

### Conclusion:

Inhalants are most popular among young to mid teens, hallucinogens are popular in the late teens and early twenties, and heroin is most popular in the early to mid twenties. Across virtually all age groups, alcohol is typically twice as popular or more as marijuana use, with older age groups having alcohol be much more popular. In general, while a larger segment of the young population uses drugs, they typically use them with less frequency than older people. 

