# Kickstarting with Excel

## Overview of Project
The Client is planning to start a crowdfunding campaign to help fund her play, "Fever." She is estimating a budget of over $10,000. Louise required our help in finding critical factors of a successful outcome.

### Purpose
The purpose of the analysis is to determine whether specific factors make a project's campaign successful. <br>
These insights will help the client to plan her own set it up for success. The excel data for this analysis is located [here](https://github.com/Takomochi/kickstarter-analysis/blob/main/Kickstarter_Challenge.zip)
  
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
For the analysis of Outcomes based on launch date, created a Pivot table first. The pivot table shows the number of Successful, failed and canceled outcomes by each month of the year. The table has filters, Parent category and Years.  Below is the line chart created for the analysis. The Parent category "theater" is already filtered in this chart.<br>
<br>
May has the highest number of successful outcomes. Overall, between May and June have relatively high successful outcomes compared to other months. On the other hand, December has almost the same number of failed outcomes as the number of successful outcomes. The number of canceled outcomes is constantly low for each month.

[Theater Outcoms Based on Launch Date - Chart](https://github.com/Takomochi/kickstarter-analysis/blob/main/resources/Theater_Outcomes_vs_Launch.png)

<img src="https://user-images.githubusercontent.com/85041697/139329947-45b63d2d-d881-4706-9e4d-f959a9027817.png" width="700">


### Analysis of Outcomes Based on Goals
For the analysis of Outcomes based on goals, created a table. The table has eight columns (Goal, Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed and Percentage Canceled). The goal column is created by grouping the goal into 12 ranges. Then, fill out the number of each outcome using the COUNTIFS function. The function needs to contain three criteria (Outcome, Range of goal amount and Subcategory). Set the subcategory as "Plays." The SUM function completes the total Projects column. Finally, the percentage of each outcome is the number of the outcome divided by Total projects.<br>
<br>
The line chart shows that less than 5000 of goal amount has the highest successful outcome rate. As the goal amount increases, the successful outcome rate decrease. However, the successful outcome rate increases up to 67 % when the goal amount is between 35000 to 45000. Then the rate decreases significantly when the goal amount is more than 45000.

[Outocomes Based on Goal - Chart](https://github.com/Takomochi/kickstarter-analysis/blob/main/resources/Outcomes_vs_Goals.png)

<img src="https://user-images.githubusercontent.com/85041697/139330635-b9aa059a-754e-4b73-a778-085fa933123f.png" width="700">


### Challenges and Difficulties Encountered
One of the challenges was to find the easiest and fastest way to fill out the calculation in the Outcomes based on goals table. I found out that I needed to repeat the same calculation for the percentage of each outcome column. I noticed that column E, "Total Projects" will not change for each calculation.  Therefore, I used relative reference on cell F2 and locked the column E. The formula in cell F2 is now "=IFERROR((B2/$E2),0)". In this way, I can drag the F2 cell through the other outcome columns and fill out the rest of the values instantly.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date? <br>
  - The month of May and June have more than 65 % of successful outcome rates.<br>
    Therefore, the client should consider launching the project between May and June.
    
  - The month of October and December have more than 40% of failed outcome rates.<br>
    Therefore, the client should avoid launching the project in October and December.


- What can you conclude about the Outcomes based on Goals?<br>
  - The goal amount of less than 5000 is likely to be successful. The goal amount of more than 50000 is highly expected to be the failed outcome.<br> 
    We need more analysis on the    goal amount between 35000 to 45000 and find a reason for the high success rate.

- What are some limitations of this dataset?<br>
  - It is difficult to say that the dataset is new and reliable because it contains years between 2009 and 2017. Trends might have changed since 2018.

- What are some other possible tables and/or graphs that we could create?<br>
  - Backers count for each outcome grouped by subcategory would help us understand which subcategory is likely to get more backers and be successful.<br>
  - Create box plots to compare the distribution of campaign goals and the distribution of total amounts pledged for plays in the US. Also, find out outliers for better analysis.

 
