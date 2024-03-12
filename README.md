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
7) Closing and loading changes to the data model
   
-------------------------------------------------------------------------------
### 7 Jan 2024   

Power BI:   
Went over different storage and connection modes of Import, DirectQuery, Composite Model, and Live Connection   
Connecting to a database (i.e., MySQL)  
Extracting data from the web (practice example was scraping a table from a Wikipedia page into Power BI)  
<img src="https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-07+231909.png">  
Data Profiling Tools: column quality, column distribution, and column profile   
Rescanning column quality (initial 1000 rows) to the entire dataset for higher accuracy rather than a sample, then filtering to reach 100% validity.  
Viewing the errors in column quality (i.e., if there is a conversion issue to whole number, invalid birthdates, etc).  
Explored column distributing to view sample distribution -- distinct and unique values   

-------------------------------------------------------------------------------
### 8 Jan 2024   

Text tools - splitting text columns (i.e, based on delimiter or attributes), formatting text columns, and extracting characters from the text   
Formatted columns to Capitalize the first letter, then combined columns with space being the separator. Example 3 columns MR. | DANIEL | JONES => Mr. | Daniel | Jones => Mr. Daniel Jones  
Completed an assignment to collect domain names of customer email addresses in a 18,000+ row table. Used in-between delimiter to extract text between "@" and ".", replaced hyphens with spaces, and formatted as each word capitalized.  
Result: Example" jon24@adventure=works.com => Adventure Works   

-------------------------------------------------------------------------------
### 9 Jan 2024   

Numeric Tools - Primarily explored statistics and standard functions.   
Completed assignment given the tasks of:   
Finding average product cost (average statistic)  
How many colors the product is sold in (count distinct values statistic)  
How many distinct customers there are (used the column from the earlier day which appended title, first name, and last name. However, there needs to be the assumption that people may have the same first and last names by chance, therefore count distinct values on the Customer Key is most accurate as each key is unique).   
Maximal annual customer income (Maximum value statistic on income column)  

-------------------------------------------------------------------------------
### 10 Jan 2024   

Very little today, reviewed text/numeric tool slides.  
Read through the time/date tool slides, watch the lectures tomorrow, and do the practice assignment at the library. 

-------------------------------------------------------------------------------
### 11 Jan 2024   

Continued with date and time tool lectures. Focused on manipulating date columns to display a variety of date options.   
Used start of the week, the start of the month, month name alone, etc based on the original date in yyyy-mm-dd format (and explored options to change the formatting of these dates).   
Noted that locale can make a difference, for instance, retrieving a data set from another country may require format adjusting (otherwise Power BI might recognize a month as a day and have errors looking for a 13th month).   
Used blank query and created a rolling calendar that updates each time the M code is run.   
<img src="https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-11+191637.png">  
Completed an assignment in which given a column of dates (yyyy-mm-dd format) I had to:   
1) Return the month name (simple date/time month function)  
2) Month number (function for this as well in the date section)  
3) Start of the year (function for this too)  
4) Year (function for this too).  
After this, I explored indexed columns which are pretty well similar to the primary key in SQL as I can tell, unique IDs.  
Went over conditional columns which used if/then statements for columns. For instance in an order quantity column if value "equals" 1 then return "Single Item", > 1 return "Multiple Items", else "Other" (to catch any error).   
Finally, reviewed calculated column best practices -- most ideal to have column calculations happen at data source > power query > Power BI front end > published reports to optimize speed.

-------------------------------------------------------------------------------
### 12 Jan 2024   

Power BI: The main topics today were grouping & aggregating, pivoting & unpivoting, and merging queries. Grouping was a similar concept learned during my PostgreSQL course, where for instance a total quantity of products was being grouped by product key using the Group By and then Sum operation. Also explored was the advanced option which was grouping by Total Quantity of products by Product Key and Customer Key. Again, similar concepts to PostgreSQL's group. Next, I went over pivoting and unpivoting which was essentially rotating distinct row values into columns (pivoting), or distinct columns into rows. Reviewed the transpose option as well, which was somewhat similar but didn't recognize unique values. Transformed the entire table so that each row becomes a column or vice versa. Finally, learned about merging queries which was similar to PostgreSQL. Completed a left outer join using the merge queries option based on a product key column shared in two different tables. The goal tomorrow is to complete this "Connecting & Shaping Data" section and move on to "Creating a Data Model".

-------------------------------------------------------------------------------
### 13 Jan 2024   

Explored the append query on my work lunch break. This was similar to merging queries but instead of expanding horizontally, the table is expanding vertically by adding more rows. The tables have to be quite comparable (i.e., same columns with compatible data types), otherwise, error or null values could occur. The first append was done by connecting 3 different .csv files and then merging them. This caused the merged table to have a dependency on the 3 individual tables, they could not be deleted. And redundant tables showing in the Queries tab. The next option explored was connecting to the Folder data type which contained the 3 tables for a more clean method to get a similar result as using the append option.

-------------------------------------------------------------------------------
### 14 Jan 2024   

Power BI: Completed connecting and shaping data section. Today I went over data source settings, which was acknowledging that if something changed with the data source (i.e., changing a file name or path the query would break). Walked through steps to make Power BI look at the new updated data source whether it be a new path or name in the dats source settings. Next briefly went over managing different data source parameters to dynamically manage and update connection paths. Looked into refreshing queries which explained toggling off the "Include in report refresh". By default Power BI refreshes data for all queries. Disabling the refresh may be useful for tables that are static/updated infrequently, simply to save time.   
Looked into importing Excel models into Power BI which explained that if there is preferenc to do some work in Excel, it's possible to import the model. The benefit here is that the calculations, relationships, etc. in Excel will carry into Power BI which you can then use for modeling.   
Finally, completed a quiz on the section. 
<img src="https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-14+234937.png">

-------------------------------------------------------------------------------
### 15 Jan 2024   

Power BI: Started the introduction for creating data models. The introduction focused on the point that even in the Power BI model view, currently there are no data models at this point. Reason being, no relationships between tables have been connected yet. Briefly went over the topic of data normalization. This process helps for eliminating redundant data, minimizing errors, and simplifying queries. This points to one reason why each table should have their own distinct purpose, and then relationships can be set up as needed. 

-------------------------------------------------------------------------------
### 16 Jan 2024  

Power BI:  
Continued through the creating a data model section, over 50% complete now.   
Topics completed today:   
• Fact ("data") tables vs dimension ("lookup") tables  
• Primary & foreign keys  
• The difference between creating relationships vs merging tables)   
• The overall model view of Power BI   
• Created table relationships for the first time   
• Practiced managing and editing relationships (deleting, activating/deactivating)  
• The star scheme and the snowflake schema  
• Completed an assignment to independently create relationships between tables using star star schema for 5 specified tables, and the snowflake schema for 3 specified tables and then using a matrix visual to confirm order quantities were working through relationships  
<img src="https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-16+234216.png">  
<img src="https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-16+234612.png">  
• Reviewed the rules of active and inactive relationships  
• Relationship cardinality (one-to-many, one-to-one, many-to-many)  
• Connecting multiple fact tables  
• Filter context & flow (filter context gets passed downstream)  

-------------------------------------------------------------------------------
### 17 Jan 2024  

Power BI:   
• Completed an assignment in which *someone* messed with relationships causing Product Keys to disappear. Replicated the issue by temporarily changing relationships between the Product Lookup table's Product Key and Return Data table's Product Key to a bidirectional relationship. Replicated the error in which Product Key #338 was missing, changed relationship back to single direction.  
• Went over creating new layouts to add specific tables I'd want to see rather than viewing all tables as the same time  
• Completed formatting dates to short-date 
• Completed formatting prices from 4+ decimal places to 2 decimal places
• Completed categorizing country and continent columns to their respective data categories

Frontend: Reviewed JS questions today via GreatFrontEnd. Questions practiced:  
• Explaining use cases for using the ES6 arrow function syntax  
• Explaining why generally it's better to position CSS '<link>'s between '<head></head>' and JS '<script>'s just before '</body>'  
• Describing event bubbling
• Describing event delegation.  

Moving forward, aiming to keep going through at least a few JS/React questions daily to stay sharp/refresh concepts. 

-------------------------------------------------------------------------------
### 18 Jan 2024

No progress today due to personal matters.

-------------------------------------------------------------------------------
### 19 Jan 2024

No progress today due to personal matters.

-------------------------------------------------------------------------------
### 20 Jan 2024
Back today with Power BI, finished off the "Creating a Data Model" section, next up is working on "Calculated Fields with DAX"!   
Topics covered today:  
• Went over hierarchies and how to create them  
• Completed assignment to creeate hierarchy within the Calendar table and add to hierachy by Start of Year > Start of Month > Start of Week > Date  
• Reviewed data model best practices (focusing on building a normalized model from the start, organizing dimension tables above data tables (downstream visual), avoiding complex relationships unless necessary, and hiding fields from report view to prevent invalid filter context).  
• Ended the section with a quiz  
https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-20+232844.png

-------------------------------------------------------------------------------
### 21 Jan 2024  
More Power BI with starting with the Calculated Fiekds with DAX section  
Topics completed today  
• M Code vs DAX  
• Calculated columns intro  
• DAX measures intro  
• Implicit vs Explicit measures  
• Quick measures  

-------------------------------------------------------------------------------
### 22 Jan 2024  
Power BI topics completed today:  
• Using dedicated measure tables  
• Understanding filter context  
• Going step by step through DAX measure calculations in an example  
• Understanding DAX syntax and operators  

-------------------------------------------------------------------------------
### 23 Jan 2024  
Power BI topics completed today:    
• Went over the common DAX function categories   
• Explored math and stats functions   

-------------------------------------------------------------------------------
### 24 Jan 2024  
Short day for Power BI today, completed topic of:  
• Counting Functions 

-------------------------------------------------------------------------------
### 25 Jan 2024   
Power BI:   
• Completed assignment to create new measures to determine how many unique customers are within a table -- (Used DISTINCTCOUNT on the Customer Key in Customers table) and the return rate of products -- (Used DIVIDE on quantity returned and quantity sold).
-------------------------------------------------------------------------------
### 26 Jan 2024   
Power BI:    
• Went over logical/conditional operators in DAX with some examples.
• Went over the SWITCH operator along with it's restrictions for instance only being able to use strings -- workaround was to use TRUE()  
• Completed assignments to i) Create a new column marking 'Customer Priority' based on income with > $100,000 being high priority, otherwise marked as standard. ii) Separating customers into different income levels of Very High, High, Average, and Low based on annual income. iii) Creating a column based on customer education levels 

-------------------------------------------------------------------------------
### 27 Jan 2024   
Power BI:    
• Went through common text functions: LEN, CONCATENATE, UPPER/LOWER, LEFT/MID/RIGHT, SUBSTITUTE, SEARCH   
• Completed an assignment based on text functions. i) To create a new calendar column that would return the first 3 characters for each month (Used LEFT 'Calendar Lookup'Month Name, 3 and wrapped this in the UPPER function). ii) Part two was to extract any number of characters before the first hyphen in a SKU (Used SEARCH function which was wrapped between the Product Lookup SKU and "-1").

-------------------------------------------------------------------------------
### 28 Jan 2024   
No progress today.

-------------------------------------------------------------------------------
### 29 Jan 2024   
No progress today.

-------------------------------------------------------------------------------
### 30 Jan 2024  
Power BI: 
• Explored basic time/date functions (TODAY/NOW, DAY/MONTH/YEAR, HOUR/MINUTE/SECOND, WEEKDAY/WEEKNUM, EOMONTH, DATEDIFF) 
• Worked through practice problems assigning days of the week with with WEEKDAY, and creating a column  specifying weekend or weekday 
• Completed an assignment to extract birth years from a customer table 
• Practiced and learned how to use RELATED()  

-------------------------------------------------------------------------------
### 31 Jan 2024  
• Worked on using the CALCULATE() function and ran through some examples. i) To calculate "Bulk Orders" for products, being products with order quantities > 1.  ii) To calculate the number of orders completed on weekends versus weekdays.

-------------------------------------------------------------------------------  
### 1 Feb 2024  
Changed it up today with some Javascript Practice/Review questions from Github user: sudheerj  
Questions reviewed:  
• Explaining arrow functions  
• Explaining what a first class function is  
• Explaining what a first order function is  
• Explaining what a higher order function is   
• Explaining what a unary function is  
• Explaining what currying function is  
• Explaining what a pure function is  
• Explaining the purpose of theft keyword  
• The difference between let and var  
• The reason to choose the name let as a keyword  
• How to redeclare variables in a switch block without an error  

-------------------------------------------------------------------------------  
### 2 Feb 2024  
Continued some Javascript practice questions, reviewed: 
• How to decode/encode a URL in JS  
• Explaining what memoization is  
• Explaining hoisting
• Explaining what classes in ES6 are
• Explaining closures  
• Describing modules and why they are needed
• Scope in JS 
• Manipulating the DOM using a service worker 
• How to reuse information across service worker restarts  
• Describing IndexedDB 
• Went over web storage (local storage and session storage)
• Explaining what a post message is  
• Explaining what a cookie is, why they're needed, the options in them, and how to delete them 

-------------------------------------------------------------------------------  
### 3 Feb 2024   
Continued some Javascript practice questions, reviewed: 
• Compared cookies, local storage, and dession storage features  
• Described the main difference between local and session storage  
• How to access web storage  
• Went over the metrhods available on web storage 
• Explained what a storage event and its event handler are    
• Explained why we need web storage     

-------------------------------------------------------------------------------  
### 4 Feb 2024     
Continued some Javascript practice questions, reviewed:   
• How to check web storage browser support    
• How to check web workers browser support   
• The restrictions of web workers on the DOM   
• Reviewed promises, why they're needed, and the three states of them (pendidng, fulfilled, rejected)   

-------------------------------------------------------------------------------    
### 5 Feb 2024  
Only reviewed callbacks today  
• Describing what a callback function is   
• Explaining why we need callbacks   
• What callback hell is  

-------------------------------------------------------------------------------    
### 6 Feb 2024  
Continued some more JS questions/review   
• Explaining what server-sent events are   
• Receiving server-sent event notifications  
• How to check browser support for server-sent events  
• Comparing the events available for server sent events   
• Explaining the main rules of a promise   
• Explaining what a callback in a callback is   
• Explaining promise chaining   
• Explaining what promise.all is   
• What the prupose of the race method in promise is  

-------------------------------------------------------------------------------    
### 7 Feb 2024  
Very brief JS review day: 
• Reviewed strict mode  
• Why strict mode is needed  
• How to declare strict mode  

-------------------------------------------------------------------------------      
### 8 Feb 2024  
Continued JS questions/review:   
• Explaining the purpose of double exclamation    
• Explaining the purpose of the delete operator    
• Explaining what the typeof operator is    
• Defining the undefined property  
• Defining what null value is    
• Comparing the differences between null and undefined   
• Explaining what eval() is   
• Comparing the differences between window and document  
• How to access history in Javascript  
• How to detect caps lock key turned on or not  
• Explaining what NaN is  
• Explaining what the differences between undeclared and undefined variables is  
• Describing what global variables are  
• Explaining the problems with global variables  
• Explaining what a NaN propert is  

-------------------------------------------------------------------------------      
### 9 Feb 2024   
Continued JS questions/review:     
• Explaining what the purpose of isFinite function is  
• Explaining what an event flow is  
• Describing event bubbling  
• Describing event capturing  

-------------------------------------------------------------------------------      
### 10 Feb 2024   
Short JS day review day
• Submitting forms using Javascript  
• How to find operating system details in JS  
• Comparing the difference between document load and DOMContentLoaded events  
• Explaining how to submit a form using JS 

-------------------------------------------------------------------------------        
### 11 Feb 2024    
Another short day for JS review  
• Explaining the difference betwen native, host, and user objects  
• Listing tools/techniques used for debugging JS code   
• Comparing the pros and cons of promises over callbacks  

-------------------------------------------------------------------------------        
### 12 Feb 2024  
Some JS today
• Comparing differences between attributes and properties
• Explaining same-origin policy
• Explaining the purpose of void 0

-------------------------------------------------------------------------------        
### 13 Feb 2024    
Some JS questions/review  
• Explaining that JS is an interpreted language 
• Explaining that JS is case sensitive language
• Explaining that there is no relationship between Java and Javascript
• Explaining what events are  

-------------------------------------------------------------------------------        
### 14 Feb 2024   
No progress today

-------------------------------------------------------------------------------        
### 15 Feb 2024 
JS today:   
• Learned who create JS   
• Explaining the use of preventDefault method    
• Explaining the use of stopPropagation method  
• Explaining the steps involved in return false usage  
• Explaining what the BOM is  
• Explaining the use of setTimeout  
• Explaining the use of setInterval  

-------------------------------------------------------------------------------        
### 16 Feb 2024 
No progress today.

-------------------------------------------------------------------------------        
### 17 Feb 2024 
JS questions/review for today: 
• Explaining why JS is treated as Single threaded
• Explaining event delegation
• Explaining what ECMAScript is
• Explaining what JSON is 
• Explaining the syntax rules of JSON
• Explaining the purpose of JSON stringify
• Explaining how to parse JSON string
• Explaining why JSON is needed
• Explaining what PWAs are
• Explainign the purpose of clearTimeout method
• Explaining the purpose of clearInterval method

-------------------------------------------------------------------------------        
### 18 Feb 2024 
No progress today.

-------------------------------------------------------------------------------        
### 19 Feb 2024 
No progress today.

-------------------------------------------------------------------------------        
### 20 Feb 2024  
Got back to JS today with questions/review completed:    
• Redirecting to a new page in Javascript  
• How to check whether a string contains a substring  
• Validating an email in JS   
• How ot get the current URL with Javascript  
• The various URL properties of location object  
• How to get query string values in JS  
• Explaining hwo to check if a key exists in an object  
• How to loop through or enumerate JS objects  
• How to test for an empty object 
• Explaining what an arguments object is  
• How to make the first letter of a string in uppercase  
• Comparing the pros and cons of the for loop   

-------------------------------------------------------------------------------          
### 21 Feb 2024   
JS review/questions:
• Displaying current time in Javascript    
• Comparing two date objects  
• Checking if a string starts with another stirng  
• Trimming a string in JS     
• Adding a key valur pair in JS  
• Explaining !-- notation  
• Assigning default values to variables  
• Defining multiline strings  
• Explaining what an app shell model is   
• Defining properties for functions  

-------------------------------------------------------------------------------           
### 22 Feb 2024     
More JS review/questions today:  
• Determining finding the number of parameters expected by a function  
• Explaining what a polyfill is  
• Explaining break and continue statements  
• Explaining what JS labels are   
• Listing benefits of keeping declarationsa at the top  

-------------------------------------------------------------------------------           
### 23 Feb 2024     
JS review/questions today:   
• Benefits of initializing variables   
• Reviewing the recommendations for creating a new object   
• Defining JSON arrays   
• Generating random integers  

-------------------------------------------------------------------------------           
### 24 Feb 2024     
No progress today.

-------------------------------------------------------------------------------           
### 25 Feb 2024     
No progress today.

-------------------------------------------------------------------------------           
### 26 Feb 2024     
No progress today.

-------------------------------------------------------------------------------           
### 27 Feb 2024    
Back to JS with a few questions today: 
Other thoughts: Will continue Power BI this week and try to finish course within the first half of may then gear focus towards completing AWS cert along with continuing practice questions. 
• Explaining how to write a random integer function to print integers within a range
• Explaining tree shaking
• Explaining the need of tree shaking
• Explaining why it isnt recommended to use eval

-------------------------------------------------------------------------------           
### 28 Feb 2024   
Continuing JS questions:  
• Explaining what a regular expression is  
• Explaining which string methods are available in regular expression  
• Explaining what modifiers are in regular expression  
• Going over regular expression patterns  
• Explaining what RegExp object is  
• Determining how to search a string for a pattern  
• Explaining the purpose of exec method  
• Explaining how to change the style of an HTML element  
• Determining what the result of: 1 + 2 " '3' would be   
• Explaining what a debugger statement is  
• Explainign the purpose of breakpoints in debugging  
• Explaining why reserved words cannot be used as identifiers  

-------------------------------------------------------------------------------           
### 29 Feb 2024  
Leap Year! 🥳   
Continued with a few JS questions:   
• Detecting a mobile browser  
• Detecting a mobile browser without regexp  
• Explaining how to get image width and height using JS  

-------------------------------------------------------------------------------           
### 1 March 2024  
Changed things up again today! Other projects/review/prep are temporarily on hold.
Creating a vanilla JS project which I will potentially be presenting in front of an audience. 
The due date is 8 March 2024 so I started right away.
Completed today:
• Selected font to fit portfolio
• Adjusted global CSS settings
• Created navbar
• Chose color palette to use throughout the site 
• Added hover effect to navbar links (working on add/remove active class based on page user is on)
• Created base layout for pages -- portrait/landscape/about/contact 

-------------------------------------------------------------------------------           
### 2 March 2024 
Continued portfolio work. Finished the text in the 'About Me' section, and resolved the issue by trying to highlight the active page in the navbar. The next big step is implementing images.

-------------------------------------------------------------------------------           
### 3 March 2024
No progress today, work, and other responsibilities. 
-------------------------------------------------------------------------------           
### 4 March 2024
Spent some more time on the portfolio project.
• Went through and started the first round of collecting photos from Google Drive
• Cropped and compressed images to be at least <500kb
• Uploaded my portraits into an S3 bucket 
• Added images to portfolio website
• Added responsive hamburger menu for tablet/mobile displays 
• Fixed alignment of navbar links
• Added Favicon 

-------------------------------------------------------------------------------           
### 5 March 2024
Continued to work on the portfolio project  
• Uploaded the rest of the photos for the primary portrait page (~total around 60 portraits)
• Made nav sticky upon scrolling with some opacity  
• Updated the "Projects" page with 2 sets of different photosets
• Added some landscape photos (~9 images)
• Minor bug fixes around the navbar, particularly in the smallest device size media query 

 Next goals:  
 • Revisit the "About Me" page, add an image of myself, and see if potential to add a fun API element.
 • Complete the contact page (perhaps a fun API element could go here) 
 • Add one more project to the "Projects" page

 Bonuses if there is time: 
 • Put some of the projects into a carousel built with JS 
 • Make and add a logo to the navbar 
 • Create a light mode version (very extra) 

 -------------------------------------------------------------------------------           
### 6 March 2024
Continued to work on the portfolio project 
• Added Ecosusi project
• Finished "About Me" page revisions with an added contact button 
• Completed contact form 

At this point, the portfolio project is pretty well done. 
May just add a small easter egg API giving either a fun fact about space (in my about page), or something along these lines. 
Next is creating a power point about this project!

 -------------------------------------------------------------------------------           
### 7 March 2024
No new progress for today.

 -------------------------------------------------------------------------------           
### 8 March 2024
Completed first draft of photography portfolio website and uploaded to Netlify: 
The live project is found [here](https://isodan.netlify.app)
Just a starter, certainly room to improve. Made with plain HTML/CSS/JS. 

 -------------------------------------------------------------------------------           
### 9 March 2024
No progress today.
 
 -------------------------------------------------------------------------------           
### 10 March 2024
No progress today.

 -------------------------------------------------------------------------------           
### 11 March 2024
No progress today.
