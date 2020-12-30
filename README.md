# kickstarter_analysis

## Overview

The client is looking to compare its active Kickstarter campaign that raised much of its funding goal in a short amount of time to others in the same segment. A review is conducted with the given Kickstarter data set to examine the relationship between the launch dates and funding goals. The examination is focused on specific category and subcategory by looking at its successful, failed, and canceled campaigns. By the end of the review, the report will be able to find an optimized date and funding goals in order to provide the best chance of success and will be compared to the current status of the client’s campaign.



## Analysis and Challenges
###### Outcomes Based on Launch Dates
One of the reviews being done is charting the success rates based on which quarter and specifically which month garnered the highest success rates in the category. Using the Kickstarter data, a pivot table is created to isolate the specific population needed.  Firstly, the Parent Category and Years are used as filters to gather only the “Theatre” population. It is then followed by the Outcomes set on the column and values section. Lastly, Date Created Conversion is placed into the rows portion of the pivot table. With these steps in mind, an adequate pivot table is created that highlights the relationship between the months of the year and its success, fail, and canceled rates. The pivot table is further analyzed using a line graph that visualizes the trends over the months. 
INSERT PICTURE HERE


###### Outcomes Based on Goals
The second analysis is finding the trends within the different funding goals and its success percentages. Firstly, the funding goals are divided into 12 different categories ranging from less than $1000 all the way to greater than $50000 in increments of $5000. This would subdivide all the variations in funding goals. The campaigns are then divided into the different success rates; successful, failed, and canceled. Total Projects, and the perspective percentage of each success rates are also taken by dividing the number of each cell to the total number of projects. To filter through the different types of success rates and its respective goals the COUNTIFS function is used. For example:
To find the number of successful campaigns in the 10000 to 14999 range, this code is used.
```
=COUNTIFS(Kickstarter!$F:$F, "successful", Kickstarter!$D:$D, ">=10000", Kickstarter!$D:$D, "<=14999")
```
Furthermore, to show the trends, a line chart is used. Through this chart, the percentage of success, fail, and canceled rates in comparison to its goals are visually identified. 
INSERT PICTURE HERE


###### Challenges
Throughout the challenge there are two specific areas of difficulties. First would be while creating the pivot table in the **Outcomes Based on Launch Dates** analysis. Deciding which criteria would be appropriate to go within the rows, columns, and value sections might prove challenging to others. One way to overcome this issue is to draw out the type of table that would make the most sense for the question being asked. For example, since the question is asking to show the trend of success rates throughout the year, it would make sense to put the Dates Created Conversion on the rows and the Outcomes on the column of the pivot table. 

The second and last difficulty that could be encountered on the **Outcomes Based on Goals** would be the differentiation between the COUNTIF vs COUNTIFS. Although a minor difference in the function, it becomes an issue when COUNTIF would only let you set a single range and criteria. Being thorough while reading the modules would show that the latter function is the one being asked. 



## Results
###### Conclusion
The research shows conclusive results regarding the optimum launch date and fund goals for the client’s campaign. The best launch dates belong in Q2 of the year with increasing success rates starting in April and peaks in the month of May. While the success rates all throughout the year stands much above the 50% mark, December would be the worst month to launch a campaign with the success rates standing at 49%.  

Following the launch dates, the trend specifies that funding success generally do better with lower goals. However, there are two key areas to avoid when setting up the goal. The numbers show that goals between $19999 to $35999 as well as goals above $44999 should be avoided.  Within these spectrums, the success rates significantly drop well below half the campaigns and more so in the latter.

###### Dataset Limitations
Although the data set given has a multitude of useful information that covered a span of 8 years, there is still a limitation. The data would be considered outdated given that the latest year recorded is only until 2017. Since the Kickstarter website has amassed a massive following over the years, it would be helpful to show the conversion percentage of each campaign. Meaning it would show the number of people that viewed the campaign as well since the set already includes how many people have donated.

###### Further Research
Nonetheless, there are further research that could be added to find the trends to design an optimized campaign for the client. Trends include:
  *Finding the number of plays that are successful/ failed / canceled throughout each year to figure out the popularity of the **Theatre/Plays**    segment on Kickstarter. This would show if Kickstarter would still be a viable platform to raise funds or should another platform be used.
  *Finding the optimal campaign length by finding the relationship between the length of the campaign and the success / success / failure / cancelation rates of each. This could be divided by the number of days that a campaign is active. 
  *Most importantly, finding checkpoints throughout the campaign that would give it an indicator whether it would be successful in raising its funds. This is done if more information is given as to which point of the campaign length are the funds successfully raised. This would be helpful to indicate not only in designing the campaign but the status as to the likelihood of success. 
  
In conclusion the analysis performed with the given data and the client’s needs are met, however there is more information that is left on the table that the client may be able to use that could help their Kickstarter campaign.  
