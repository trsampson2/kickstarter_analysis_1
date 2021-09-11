# kickstarter_analysis_1
Analysis of Kickstarter data to show outcomes based on launch date and goal
## Overview of Project
Louise, a playwright, has used Kickstarter to raise money to fund her play.  She has come close to her fundraising goal in a short amount of time and now wants to look at how different campaigns performed in relation of their launch dates and their funding goals. 
## Purpose
This project will analyze the data of 4113 campaigns to find their outcomes based on launch dates and funding goals.
## Analysis and Challenges:
### Analysis of Theater Outcomes by Launch Date
Date Conversion:  When looking at launch dates, a conversion of the “launched_at” column is needed to use the data for analysis.  I used the formula “ =(((J2/60)/60)/24+DATE(1970,1,1))” to convert the dates in the column to create the “Date Created Conversion” column.  
![Date_Conversion](https://user-images.githubusercontent.com/86331812/132948517-29e6ad79-11d9-471c-bbcc-36e77523f3a3.png)
Using the date, I was able to isolate the year and the month of the creation date.  To isolate the year, I used the “=YEAR(S2)” formula.
![Date_Conversion_Years](https://user-images.githubusercontent.com/86331812/132948530-dce576cb-d032-4905-9857-e30b991abba3.png)
To isolate the month, I used “=TEXT(S522, "MMM")”.  This formula displaced the first 3 letters of the month. 
![Date_Conversion_Months](https://user-images.githubusercontent.com/86331812/132948538-f4ef1b8d-dde2-4e7b-8b9c-8687fb3d2e42.png)
Pivot Chart Creation: Once I created the “Months” and “Years” columns, I was able to use create a pivot table that would display the outcomes of each category by month.
My PivotTable Fields are shown below. 

![Outcome_vs_Goals_pivot](https://user-images.githubusercontent.com/86331812/132948549-a90aaaae-8fc6-4767-9f3c-aa562e47f5f3.png)

The following table was displayed to create the final analysis chart. 
![Outcome_vs_Goals_pivotTable](https://user-images.githubusercontent.com/86331812/132948567-303f682d-a3b5-409e-b602-255aff3b5bda.png)

### Analysis of Outcomes Based on Goals
When looking at outcomes based on goals, goal ranges were determined and placed in the table.  I used COUNTIFS formulas to determine the number of successful, failed, or cancelled play campaigns. ![CountIFS_Calc](https://user-images.githubusercontent.com/86331812/132948888-944588e1-6284-45f5-b205-7a0616746af3.png)
I calculated the sum of the projects to find the total projects.
![SUM_Calc](https://user-images.githubusercontent.com/86331812/132948910-46e60774-b097-4169-9e75-848f56e95e05.png)
I used the total to find the percentage of projects in each category. 
![Percentage_Calc](https://user-images.githubusercontent.com/86331812/132948920-8dccd746-e85b-4f0b-a402-8baae604c65f.png)
### Challenges and Difficulties Enountered
The challenges that could be encountered when entering the date conversion formula. The year and month isolations are also challenging formulations.  They weren’t known to me before this course and I expected a more difficult formula to create these isolations. When creating the pivot table, it could be challenging when trying to figuring what fields to put in each area (Filters, columns, rows, and values.  I had issues with sorting the campaign outcomes in descending order. It was a simple selection, but I had a hard time figuring out what to select to get it to go into descending order.  

## Results
### Theater Outcomes by Launch Date  
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/86331812/132949216-2a952e26-8620-456b-8ce0-3c5701446973.png)
From the data, May was the first month to launch a successful campaign.  I would suggest launching a campaign for Theater in May.  The lowest number of successful campaigns were launched in December. It is also a one of the lowest months for failed campaigns.  I wouldn’t recommend launching a campaign in December.  That is the lowest month for launched campaigns overall. 
### Outcomes based on Goals
Looking at the data, it shows there are 3 points where the percentage of plays that were successful and failure are equal.   There are more successful play campaign that had a lower goal of less than 1000 at 76%, but that isn’t enough money to fund the play. I would recommend launching the campaign between 1000 and 4999.  The data shows that the 73% of plays have successful campaigns in that range. 
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/86331812/132949261-4720bb4e-0013-4945-bbdf-2f8e1f129277.png)
### Limitations
The limitations of the dataset are its origination and the limited time frame that it encompasses. 
### Recommendations for addtional tables or graphs. 
I would recommend creating a chart that analyzes the outcome based on duration of the campaign.  I think that is important when thinking about how successful a project will be.  If left open too short a time, the campaigner might lose out on money.  
