# Kickstarter Analysis
Excel excercise to create two new analysis.
## Overview of Project
To know how different campaigns fared in relation to their launch dates and their funding goals.
### Purpose
The purpose of this challenge is to visualize campaign outcomes based on launch dates and funding goals with the kickstarter dataset
## Analysis of Outcomes Based on Launch Date
- A new column "Years" is created and the YEAR() function is used to extract the year from the “Date Created Conversion” column.
- A pivot table is created in the new sheet and named as "Theater Outcomes by Launch Date."
- The pivot table is filtered based on th "Parent Category" and "Years", and appropriate pivot table fields in columns,rows and values are placed.
- Default items in the row fields are removed so as to get the months of the year in the "Row Labels" in the pivot table.

![pivot1](https://user-images.githubusercontent.com/95719819/147899708-65106a14-564f-4c63-8226-eb09b7ac9e51.JPG)

- Then the "Parent category" is filtered to show only "theater", and the campaign outcomes are sort in descending order.

![pivot2](https://user-images.githubusercontent.com/95719819/147899881-b5873739-6a51-442e-9c79-f6bbacc98edc.JPG)

- A line chart is created from the pivot table to visualize the relationship between outcomes and launch month.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/95719819/147887542-45f8c4d2-b4d1-4ea2-b02b-9f669f5d6c4d.png)
## Analysis of Outcomes Based on Goals
- A new sheet "Outcomes Based on Goals" is created with the following columns
  - Goal
  - Number Successful
  - Number Failed 
  - Number Canceled
  - Total Projects
  - Percentage Successful
  - Percentage Failed
  - Percentage Canceled
- The goal column is created with the following dollar amount ranges
 
 ![Goal](https://user-images.githubusercontent.com/95719819/147900865-c9e7808e-9976-4045-80c2-b6a85b6fc322.JPG)
 - "COUNTIFS()" function is used to populate the "Number Successful," "Number Failed," and "Number Canceled" columns by filtering on the Kickstarter "outcome" column, on the "goal" amount column using the ranges in the goals column, and on the "Subcategory" column using "plays" as the criteria.
 - The SUM() function is used to populate the "Total Projects" column with the number of successful, failed, and canceled projects for each row.
 - The percentage of successful, failed, and canceled projects for each row is populated with the "ROUND()" function.
 -  A line chart titled "Outcomes Based on Goal" is created to visualize the relationship between the goal-amount ranges on the x-axis and the percentage of successful, failed, or canceled projects on the y-axis.
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/95719819/147887485-3041faf9-a9c5-4dff-9746-558c6573a13f.png)

### Challenges and Difficulties Encountered
- In analysis of outcomes based on launch date, the challenge was to get the months of the year in the row label. By removing the default items added in the row field while creating the pivot table the required output was achieved.

- In analyzing the outcomes based on goal the challenge was in getting the percentage display in the y axis. By setting the category to Percentage in the number on the "Format Axis" the required output was achieved.
## Results
- By analyzing the "Theater Outcomes by Launch Date" we visualize that successful outcomes are highest in all the month and the canceled outcomes are very few in every month.
- Also, we see that the highest succcessful outcome is in the month of May and no canceled outcomes in the month of October.


- By Analyzing the "Outcomes Based on Goals" the canceled outcome is zero based on goal for the "play" subcategory.
- Also, we see that for the goal between 45000 to 50000, the percentage of failed outcome is 100%, so the percentage of successful coutcome is 0%.
## Limitations
The main limitation with the given dataset is that the dataset is too large to manually analyze the data.

## Other possible Charts
Some other possible charts that can be created are bar charts, pie charts(2D,3D)
