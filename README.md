# Kickstarting with Excel

## Overview of Project

### Purpose

To put on her play "Fever" Louise is conducting a fundraising campaign. The purpose of this analysis was to give Louise the best chance at success in reaching her fundraising goal. To accomplish this, Louise wanted to know how other campaigns fared in relation to their launch date and funding goals. I analyzed a large dataset containing information on fundraising campaigns from Kickstarter, a crowdfunding platform. I then created a data visualization for both of the analyses Louise asked for in order to make my findings consumable and easy to understand.

## Analysis and Challenges

This analysis was relatively straightforward, with Microsoft Excel being the only tool I required. In Excel, I used a variety of tools including pivot tables, pivot charts, and numerous functions to manipulate the data, perform calculations, uncover trends, and create visualizations.

### Analysis of Outcomes Based on Launch Date

#### Purpose

This analysis was performed to examine if the month that a fundraising campaign is launched has a significant impact on its outcome and, if so, which month(s) Louise should target for launch and which months she should avoid.

#### Process

The first step in this analysis was to use YEAR() Excel function to extract the year each campaign was launched into a new Years column. Next, I created a pivot table, with the month of launch date as my rows, outcomes as my columns, count of outcomes as my values, and parent category and years as my filters. I utilized the parent category filter to only show theater fundraising campaigns, since these are the most relevant for Louise. The final step of this analysis was to generate a line chart displaying the count of outcomes on the y-axis and the month of launch date on the x-axis. This chart displays how many theater campaigns were successful, how many failed, and how many were cancelled based on the month they were launched.

### Analysis of Outcomes Based on Goals

#### Purpose

This analysis was performed to examine if the funding goal of a campaign has a significant impact on the campaign outcome and, if so, what goals have a higher rate of success and which have a lower rate of success.

#### Process

The first step in this analysis was to create a new sheet called "Outcomes Based on Goals" with 8 columns for goal, number successful, number failed, number canceled, total projects, percentage successful, percentage failed, and percentage canceled. The goal column was separated into 12 ranges, the lowest being less than $1000, the highest being greater than $50000, and the middle 10 being $5000 increments. I used the Excel COUNTIFS() function to populate the Number Successful, Number Failed, and Number Canceled columns from the Kickstarter data worksheet. This function allows you to filter data by multiple conditions in the same function, and then counts the data that meets those conditions. The filters I used were the outcomes, the different ranges, and the plays subcategories. Next, I used the SUM() Excel function to calculate the total projects in each fundraising goal range. Then, I calculated the percentage successful, percentage failed, and percentage canceled by dividing the number of each campaign by the total, and switching the column formats to percentage. The final step of this analysis was to generate a line chart displaying the percentage of each outcome on the y-axis and each range of fundraising goals on the x-axis.

### Challenges and Difficulties Encountered

#### Analysis of Outcomes Based on Launch Date

I found this analysis less difficult than the goals analysis, with no significant challenges. One step that could be a possible challenge for others would be converting unix timestamps into a readable format so that our YEARS() function could be used. The best way to overcome this is to do an internet search on the process which will bring up multiple results that have step by step instructions to follow.

#### Analysis of Outcomes Based on Goals

This analysis was also straightforward for the most part, but the COUNTIFS() function was a bit challenging. It is not the most intuitive function in terms of how to format each parameter you want to filter by. However, I overcame this by googling tutorials on the function and watching/reading a couple of them.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

### Conclusion 1

May is the best month to launch a fundraising campaign, followed closely by June.

### Conclusion 2

December is the worst month to start a campaign. I say this despite most other months having a higher total number of failures, because those other months also have a greater total number of campaigns launched. The number of failed campaigns in December is nearly equal to the number of successful ones, which is not the case in any other month. If we looked at the percentage of campaigns that succeeded, failed, and were canceled by month, December would have the highest rate of failure.

### Graph of Results
![alt text](https://github.com/[ksdisch]/[kickstarter-analysis]/blob/[main]/resources/resources/Theater_Outcomes_vs_Launch.png)
!(/resources/Theater_Outcomes_vs_Launch.png)

- What can you conclude about the Outcomes based on Goals?

### Conclusion 1

The most obvious conclusion from this analysis is that a campaign's chances of succeeding drop immensely if the goal is $45,000 or greater.

### Conclusion 2

The highest rate of success was for less than $1,000, which makes sense but is not very helpful because that fundraising total will not go very far in putting on a successful play. The most valuable conclusion I draw from this analysis is that setting the goal between $35,000 and $44,999 is the best option. The percentage of these campaigns that were successful (66.67%) was only slightly lower than that of less than $1,000 (75.81%) and $1,000 to $4,999 (72.66%), and you can put on a much better play with that larger sum of money.

### Graph of Results

!(/resources/Theater_Outcomes_vs_Goals.png)

- What are some limitations of this dataset?

### Limitation 1

One limitation of this dataset is how broad the geographic data is. With the broad range of fundraising goals and results, many of these campaigns are not going to be released/performed nationwide. And in these countries there is vast differences in the financial statuses of populations from state to state and especially if you look more locally than that. With all of that being said, I believe that having data that is grouped as locally as possible would be very helpful for determining how you should run a fundraising campaign in different communities. If you had an area with a lower average financial status, you would probably have a better chance at success if you set your campaign goal lower. On the other hand, if you are fundraising nationwide or in a community that is more well off on average, it may be wise to set your fundraising goal higher.

### Limitation 2

Another limitation that applies specifically to Louise's campaign is that it would be helpful to have data on different genres of plays. With the music parent category we have subcategories for the genre of music, and I think it would be valuable information to have that for plays as well. We could see if musicals, classic plays, etc., have higher rates of success with their fundraising campaigns and how to increase those chances of success.

- What are some other possible tables and/or graphs that we could create?

### Graph 1

One graph I think would be helpful for the Outcomes based on Launch Date analysis is an outcomes by percentage graph to at least go along with, the outcomes by total count graph. I think the percentages are more valuable than the totals because of my example that I used. If you only looked at the number of failures by month, December would look like a good month to start a campaign, because it has one of the lowest number of failures. But that is because the total campaigns is lower, and the percentage of success would show us the chances of success by month more directly than looking at totals.

### Graph 2

On the other hand, I think a chart of totals for the Outcomes Based on Goal analysis would add valuable context to the percentage graph. I say this because looking at the percentage graph, the $45,000 to $49,999 range has a 0% success rate, but there was only one play with a goal in that range, and it is difficult to draw conclusions with a sample size that small. We could probably just add labels of the totals to the chart instead of an entire new graph.

### Graph 3

One more graph I think would be valuable for Louise would be to look at the rate of outcomes based on the length of campaigns. Since we determined the ideal launch date of a campaign to be May or June, this would give her an idea when to set her campaign deadline for based on the month of launch date.
