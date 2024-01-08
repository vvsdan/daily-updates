# daily-updates

This repo/README file is meant to serve as a journey for documenting work I do daily, problems solved, tasks completed, or challenges faced in my learning. 

### 1 Jan 2024 

In the comfy store project, there was a NaN error being produced when adding items to the cart. In the web application, the error appeared in the Navbar Cart icon which was to indicate the number of items in the cart. The same error carried over for other dynamic values such as in the checkout page, when calculating the shipping totals (everything produced NaN except the static shipping price). 
Initially, I thought this error was in the store.js file OR the cartSlice.js file where state values were stored, or being incremented, edited, etc. 
Solution: In App.jsx the path for "Orders" was incorrect
<img src='https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-02+121816.png'>
-------------------------------------------------------------------------------
### 2 Jan 2024

Spent some of the day reviewing the end of Jose Portilla's SQL course. Reviewed topics of NULLIF, Views, and Import-Export of files. 
Went back to work on the Comfy Store and the bug resurfaced. Tried to look through the code to see areas of error. Still think that this error must occur right upon action dispatch.
Will try again when possible, will maybe try utilizing breakpoints to pinpoint the error. Just as before, the cart icon is returning NaN, as are the cart totals. 
-------------------------------------------------------------------------------
### 3 Jan 2024 

Didn't have a chance to make meaningful progress - was asked to come into work as the team was short-staffed today. 
Will continue bugfixing, and ideally make meaningful progress with Power BI. 
-------------------------------------------------------------------------------
### 4 Jan 2024 

No luck with bugfixing today, and to finish the project it needs to be completed. 
To try again this weekend.
Progress made with Power BI: 
Learning the differences (and similarities) between it and Excel -- also noting that they're built on top of the same analytics engine. 
A high-level overview of "Back-end" (Power Query Editor) and "Front-end" (Model view, data view, and report view) workflow.
Went over different types of data connectors (flat files, databases, azure, online services, etc.) to see what is available. Will be working with .csv files for the course though. 
Completed an introductory quiz:
<img src="https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-04+230325.png">
-------------------------------------------------------------------------------
### 5 Jan 2024 
No progress today, work + application, and personal responsibilities to attend to. 
-------------------------------------------------------------------------------
### 6 Jan 2024 
Power BI: 
Exploring Query Editing Tools
Basic table transformations
Overview of M-Code 
Loading first .csv file into Power BI 
Learned the Applied Steps of how Power BI determines data types in table columns
Practiced changing data types, removing columns
Completed practice #1 assignment of: 
1) Creating queries to connect to two new .csv files
2) Renaming the queries
3) Confirming that column headers and data types are correct upon connecting
4) Adding a new column to extract all characters before a dash ("-") - delimiter
5) Manipulated column in step 4) to return all characters before a second dash ("-") using advanced options -> scan for the delimiter from the start of the input and skip 1 delimiter
6) Replacing all zeroes (0) with "NA" within a column
7) Closing and loading changes to data model
-------------------------------------------------------------------------------
### 7 Jan 2024 
Power BI: 
Went over different storage and connection modes of: Import, DirectQuery, Composite Model, and Live Connection 
Connecting to a database (i.e., MySQL)
Extracting data from the web (practice example was scraping a table from a wikipedia page into Power BI)
<img src="https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-07+231909.png">
Data Profiling Tools: column quality, column distribution, and column profile 
Rescanning column quality (initial 1000 rows) to entire dataset for higher accuracy rather than sample, then filtering to reach 100% validity.
Viewing the errors in column quality (i.e., if there is conversion issue to whole number, invalid birthdates, etc).
Explored column distributing to view sample distribution -- distinct and unique values 
