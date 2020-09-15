# Kickstarter Analysis
## Overview of Project
After the Lousie's play *Fever* came close to reaching its funding goal yet still failing, Louise became interested in how other kickstarters, especially theatre kickstarters, were affected by funding and the time at which they were launched.

Louise came to me wanting to analyze the outcome (success, failure, cancelation) of theatre Kickstarter campaigns based on when the campaign was launched as well as the outcome of kickstarter campaigns based on what percentage of their funding goal was met.  

## Analysis and Challenges
To start the analysis, I was provided with a global list of Kickstarter campaigns broken out by country, category, outcome, funding goals, start date, and funding actuals.

### Analysis of Outcomes Based on Launch Date

[Analysis of Outcomes Based on Launch Date](resources/Theater_Outcomes_vs_Launch.png)

The above link displays the breakdown of success and failures of kickstarter campaigns based on their launch date from 2009 through 2017. I extracted the date from the 'Date Created Conversion' field in the Kickstarter excel sheet. In total, there were 1,269 theatre kickstarter campaigns in that date range. The number of successful, failed, and canceled campaigns were broken out using a pivot table to analyse the data from the initial Kickstarter excel sheet. The  

### Analysis of Outcomes Based on Goals

[Analysis of Outcomes Based on Goals](resources/Outcomes_vs_Goals.png)

The above link will direct you to a visual breakdown of success or failure of kickstarter plays based on the percent of the funding goal that they obtained. To complete this analysis I calculated the number of successful plays and unsuccessful plays that fell into designated ranges of funding goals on the Kickstarter excel sheet. 

```
=COUNTIFS(Kickstarter!$D:$D, "<1000", Kickstarter!$R:$R, "plays", Kickstarter!$F:$F, "successful")
=COUNTIFS(Kickstarter!$D:$D, "<=4999", Kickstarter!$D:$D,">=1000", Kickstarter!$R:$R, "plays", Kickstarter!$F:$F, "successful")
```
After the successes, failures, and cancelations were enumerated in their columns using the `COUNTIFS` function, the total number of projects within each funding group was summed to determine what percentage of the kickstarters in the funding group were successful.

### Challenges and Difficulties Encountered



## Results

When analyzing the results of the Outcomes based on Launch Date for the theatre kickstarters, it appeared that campaigns that began in May were the most successful. This analysis looked at the outcome of theatre campaigns around the world. Louise is most interested in analyzing plays like *Fever* which was a U.S. based compaign. In the analysis of outcomes based on launch date, success could vary dependnging on region. 
