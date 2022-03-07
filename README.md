# UNC-VIRT-DATA-PT-02-2022-U-B
An Analysis of Kickstarter Campaigns

Overview of Project

A dataset, called Kickstarter, was used to help a client with a funding campaign for a theatrical production.  Our client, Louise, was interested in learning how others fared in their own funding campaigns, and specifically those campaigns that were similar in scope and type to her venture. Kickstarter provided data on thousands of crowdfunding projects allowing for specific insights to be gained related to campaign outcomes based on length of time and meeting funding goals.  
Analysis and Challenges
The dataset was initially assessed to determine if the type of data present would be useful for the analysis needed, and how it might be organized for ease of understanding.  After determining the usefulness of the data for our purposes, the following actions taken were:
Convert Unix Timestamps into Standard Format
The dates in the Deadline and Launched columns were not in a readable format and needed to be converted.  Both columns contain Unix timestamps rather than dates in a standard format.  While working with Unix timestamps was new for me, it was not difficult to follow the steps to make it readable.  A converter tool was used to interpret the timestamp and change it into the date and time assigned. This verified that we were working with Unix timestamps, and what remained was to make it into a format that was readable. This required use of an advanced Excel formula.  For example, Unix time 1361250539 was converted to 2/19/2013 with the following formula: 
=(((J2/60)/60)/24)+DATE(1970,1,1)
Create Pivot Table for Outcomes Based on Launch Date

By creating summary tables, we were able to see the outcomes of all the categories, but first we had to consider which data we wanted to see summarized and how we want the data to be presented.  We determined that what was most relevant to Louise were outcomes found in the Theater category based on launch date month.  The following is a table called Theater Outcomes by Launch Date:
This analysis shows the outcomes of successful, failed and canceled theater campaigns, based on their launch date. To start, a ‘years’ column was added to the Kickstarter dataset to extract the year from the ‘date created conversion’ column. Next, a pivot table was created to include filters for ‘parent category’ and ‘years,’ a row for ‘date created conversion,’ and ‘outcomes’ placed in the columns and values fields. Given that I have never worked with Pivot Tables before, extra time was needed to learn the steps and then apply them several times.  Now, I am much more comfortable with Pivot Tables and find them to be effective for creating useful summarization of data, and then providing for further visualizations.

Create Pivot Chart for Outcomes Based on Launch Date

To visualize the data from the Pivot Table, a line chart was created to show the relationship between theater campaign outcomes and their launch month.  The following helps to tell a part of the story:
![image](https://user-images.githubusercontent.com/100803302/157012728-a6e09f1b-f98c-4f12-9ec6-0fd0c2aea82b.png)
Create Pivot Table for Outcomes Based on Goals

This analysis shows the number and percentage of successful, failed and canceled plays based on the funding goal. First, a new sheet was created in Kickstarter showing campaign outcomes based on campaign funding goals. The COUNTIFS formula was used to find this data. Most of my time on this project was spent on COUNTIFS.  Finding the correct formulas for outcomes based on dollar range was exhaustive. After several attempts at trying on my own, including use of internet resources, I got a breakthrough when I received help during course office hours.  My difficulties related to improper filtering on the main Kickstarter sheet and formulas that lacked necessary criteria. 
Referencing the below table, here is a formula for finding the number of successful outcomes with a goal of 1000 to 4999: =COUNTIFS(Kickstarter!$D:$D, ">=1000", Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays", Kickstarter!$D:$D, "<5000").  Once I had the correct outcome numbers, finding total projects and outcome percentages was not difficult. With the summary table in place, a line chart was also created to visualize the data.
 
Create Pivot Chart for Outcomes Based on Goals
![image](https://user-images.githubusercontent.com/100803302/157013048-28187980-1b6b-484c-933c-5d0f9285a805.png)
Results
•Based on data for every year of Kickstarter for Theaters, the most notable findings are 1) The most successful campaigns begin in May and June and 2) Less than 3% of total campaigns were ever canceled.  While May and June saw the launch of 111 and 110 successful campaigns respectively, those months also reflected highs for failed campaigns.  The final note related to Theater campaigns is that successful campaigns steadily declined from October through December.
•Based on data for the funding goals of campaigns for Plays, two conclusions are 1) The greatest number of successful campaigns occur when funding goals are less than $5000 and 2) As the dollar amount of funding goals increases above $5000 there is mostly a decrease in the number of successful campaigns.
•The gathering of some qualitative data may have helped to better explain why some campaigns succeeded and others failed.  For example, how well were any marketing tools used such as social media or other advertisement, and how much time did the client put into their project.  
•A graph showing the countries that backers come from might be useful for targeting resources.  For example, a bar chart that shows the relation between backer and country and successful campaigns.

Recommendations

The good news for Louise is that Plays, by far, are the most successful sub-category of crowdfunding campaigns. I would encourage my client to start her bid for funding in May or June and target donors for smaller amounts ranging from $100 to $5000 to find the most success.



