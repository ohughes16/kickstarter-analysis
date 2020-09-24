# Kickstarter Analysis
## Overview of Project
After the Lousie's play *Fever* came close to reaching its funding goal yet still failing, Louise became interested in how other kickstarters, especially theatre kickstarters, were affected by funding and the time at which they were launched.

Louise came to me wanting to analyze the outcome (success, failure, cancelation) of theatre Kickstarter campaigns based on when the campaign was launched as well as the outcome of kickstarter campaigns based on what percentage of their funding goal was met.  

## Analysis and Challenges
To start the analysis, I was provided with a global list of Kickstarter campaigns broken out by country, category, outcome, funding goals, start date, and funding actuals. The category that this analysis will focus on is the parent category of theatre which contains three subcategories: plays, musicals, and spaces.

### Analysis of Outcomes Based on Launch Date

[Analysis of Outcomes Based on Launch Date](resources/Theater_Outcomes_vs_Launch.png)

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/64506842/94173215-7444fc80-fe48-11ea-829a-fb2cbdb28331.png)

The above link displays the breakdown of success and failures of theatre kickstarter campaigns based on their launch date from 2009 through 2017. I extracted the date from the 'Date Created Conversion' field in the Kickstarter excel sheet. In total, there were 1,269 theatre kickstarter campaigns in that date range. The number of successful, failed, and canceled campaigns were broken out using a pivot table to analyse the data from the initial Kickstarter excel sheet. Louise was curious to know if there were certain months that were more or less successful for starting a theatre campaign. 

### Analysis of Outcomes Based on Goals

[Analysis of Outcomes Based on Goals](resources/Outcomes_vs_Goals.png)

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/64506842/94173205-6e4f1b80-fe48-11ea-9171-31b44cbe8dd5.png)


The above link will direct you to a visual breakdown of success or failure of kickstarter plays based on the percent of their funding goal that they obtained. Plays is a subcategory to the parent category of theatre. To complete this analysis I calculated the number of successful plays and unsuccessful plays that fell into designated ranges of funding goals on the Kickstarter excel sheet. In total, there were 1,047 kickstarters that fell into the subcategory of plays that were analyzed.

```
=COUNTIFS(Kickstarter!$D:$D, "<1000", Kickstarter!$R:$R, "plays", Kickstarter!$F:$F, "successful")
=COUNTIFS(Kickstarter!$D:$D, "<=4999", Kickstarter!$D:$D,">=1000", Kickstarter!$R:$R, "plays", Kickstarter!$F:$F, "successful")
```
After the successes, failures, and cancelations were enumerated in their columns using the `COUNTIFS` function, the total number of projects within each funding group was summed to determine what percentage of the kickstarters in the funding group were successful. This analysis included all kickstarter plays globally. This resulted in having twelve different currencies involved within each funding goal (see below image). The funding goals were not normalized to a single currency and therefore may not provide the best representation of normalized funding for the play campaigns.

![Currency](https://user-images.githubusercontent.com/64506842/94173192-65f6e080-fe48-11ea-80a2-18fbb6c42a17.png)

### Challenges and Difficulties Encountered

There were some challenges on focusing on the desired outcome of the analysis. The data provided with the Kickstarter excel sheet had a lot of data that was irrelavant to what Lousie wanted to focus on with the ability to dive into multiple analyses. If Louise wanted to focus on productions like *Fever*, a more defined description of what attributes those kickstarters should have would have helpful. Should I have focused on U.S. based kickstarters? Should I have included the subcategory 'spaces' in the analysis? Should we have looked at the length of the campaign and how that affected success or failure? 

## Results

When analyzing the results of the Outcomes based on Launch Date for the theatre kickstarters, it appeared that campaigns that began in May were the most successful. This analysis looked at the outcome of theatre campaigns around the world. Louise is most interested in analyzing plays like *Fever* which was specifically a U.S. based compaign. In the analysis of outcomes based on launch date, success could vary dependnging on region and therefore I would recommend analyzing success of plays within the U.S. for better results.

When analyzing the funding of the plays, I would recommend normalizing the currencies to the evivalent in U.S. dollars when comparing theatre kickstarter campaigns globally. As is, the goal funding data is skewed to the left when looking at a range of funding from 0-50,000. Louise's play *Fever* had a goal of $2,885. If Louise wants to look at other plays similar to *Fever* I would recommend her focusing the analysis on plays ranging from 0-20,000 in funding to focus her study with tighter funding brackets.

I would recommend using the same analysis parameters on both graphics in the future. Either expanding the analysis on funding goals to include all parent category 'theatre' subgroups in the analysis or limiting the analysis on kickstarter start date to just the subcategory plays you would isolate the category of plays in both analyses. This would help isolate the variable that Louise is trying to focus on when comparing campaigns like *Fever*.
