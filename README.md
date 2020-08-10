# Drug Use by Age
I chose the dataset "Drug Use by Age" from FiveThirtyEight's github, which can be found [here.](https://github.com/fivethirtyeight/data/tree/master/drug-use-by-age)

This data had information about the percentage of the respondents who reported using certain drugs within the past 12 months, and the frequency in which they used those drugs over the past 12 months. The data covers 13 different drugs across 17 age groups. The data came in one csv file that I put onto a google sheet. I then did the following to analyze the data:
* Sorted heroin use z-a to find the top groups were: 22-23 (1.1%), 20 (0.9%), and 24-25 (0.7%)
* Sorted hallucinogen use z-a to find the top groups: 19 (8.6%), 20 (7.4%), and 19 (7%). 
* Sorted hallucinogen frequency Z-A, to find the top groups: 12 (52), 50-64 (44), 13 (6)
* Sorted inhalant use Z-A, to find the top groups: 16 (3%), 14 (2.6%), 15 (2.5%) , 13 (2.5%)

An interesting finding here was that heroin was the oldest, hallucinogens were a bit younger but still within the usual drug experimentation age, and inhalants were youngest. This confirmed my suspicions that inhalants would be more popular among young people who may not have legal or illegal access to more 'serious' drugs. I also speculated that heroin was something people do after they've been doing drugs for a while, and is something older people are more likely to do as since it is done out of necessity rather than fun. This is in contrast to psychedelics which are rarely done habitually and are more for when you want to experiment and have fun, so they would attract a demographic that doesn't have quite as many formal responsibilities yet. Finally, a notable outlier was the 50-64 group in hallucinogen frequency. The hallucinogen use for this age group was only 0.3%, so I suspect there were a handful of people or maybe even one person who used them extremely frequently and skewed the data. 

I then became interested in comparing different drugs in pivot tables. I ran a pivot table comparing cocaine and meth use, cocaine and heroin use, and marijuana and alcohol use. The marijuana and alcohol was of particular interest to me, so I made a new sheet with just age, marijuana use, and alcohol use. I then exported this sheet into datawrapper and made a double column chart comparing the two, which can be viewed [here](https://www.datawrapper.de/_/KtiSm/), or below:

<iframe title="Marijuana and Alcohol Use By Age" aria-label="chart" id="datawrapper-chart-KtiSm" src="https://datawrapper.dwcdn.net/KtiSm/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="600"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

I was surprised to learn that alcohol was so much popular than marijuana amongst all age groups, with marjuana use routinely being half as popular (or less) than alcohol use. Most people I know either do both, or only use marijuana. I do, of course, live in California though, and since this data was taken nationally, I understand the discrepancy more. I was also surprised that more baby boomers, who lived through the sixties, didn't use marijuana, with 7.3% of the 50-64 age group using marijuana compared to 67.2% using alcohol, and 1.2% marijuana compared to 49.3% alcohol with the 65+ group. The highest marijuana use (34%) was with 20-year-olds, compared to 69.7% alcohol use, meaning that alcohol still beats marijuana by approximately 100% even amongst marijuana's most popular demographic.

I then wanted to find a way to group together the depressants and stimulants because I noticed they were each divided into multiple categories in the original data. I tried using OpenRefine to consolidate the groups together but could not figure out how to do this the way I wanted to, so I went back to google sheets and just made a seperate sheet. I made 5 columns: age, stimulant use total, stimulant frequency total, depressant use total, depressant frequency total. I lumped the categories like this:
* stimulants: crack, cocaine, stimulant, meth
* depressants: heroin, pain reliever, oxycontin, tranquilizer, sedative

I used formulas that just added the sum of each specific drug, for example: ``` ='drug-use-by-age'!G9+'drug-use-by-age'!I9+'drug-use-by-age'!W9+'drug-use-by-age'!Y9 ```

I did not include marijuana or alcohol in these categories as I felt both were too popular and I wanted to just look at less conventional drugs. 

