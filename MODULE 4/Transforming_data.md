# Transforming data with excel 

<details><summary>Objectives 🕵️ </summary>

Introduction / Reflection


Step four for me was all about getting data ready for analysis. I realised that datasets often have blank rows, wrong formats, or messed-up entries, and if I don’t fix these, my analysis can go completely wrong. Working through this module, I used Excel to import, clean, and prepare data, which made me understand how important it is to start with clean, organised data before doing anything else.


What I Learned


I learned how to transform data properly in Excel. I practiced sorting and filtering, changing data formats, using conditional formatting, and combining datasets, which helped me see how each step makes the dataset easier to work with. Using formulas and functions taught me how to calculate and transform data efficiently, instead of doing it all manually. Finally, working with pivot tables showed me how I can summarise, explore, and present data clearly, which gave me a better idea of how to spot trends and patterns in a dataset.
Overall, this module taught me that preparing and cleaning data isn’t just boring busy work — it’s essential for accurate analysis, and learning these Excel skills has made me feel much more confident handling real-world datasets.


</details>

<details><summary> LAB - using excel to sort and filer data </summary>

Objectives / Reflection


In this lab, I learnt the basics of sorting and filtering data in Excel. I used a sample dataset to practise organising and exploring data, which helped me see how much easier it is to analyse data when it’s structured properly.


Part 1: Download and Prepare a Sample Data Set


I opened the Bike Sales CSV file in Excel and adjusted the column widths so I could see everything properly. I also froze the top row so the headings stayed visible while I scrolled down. Doing this made me realise how small presentation changes can make large datasets much easier to work with and read.


Part 2: Sort the Data


Next, I learnt how to sort data. I selected all the data and used Custom Sort to organise it by Country and then by Sub-category in ascending order. This showed me how quickly Excel can group information and make patterns obvious. I also learned how to clear sorting and filters when I wanted to start fresh.


Part 3: Filter the Data


Then, I converted the data into a table and applied filters. Using the drop-down arrows, I could show only specific groups, like Young Adults in the Age_Group column. I realised that filtering doesn’t move the data—it just hides rows temporarily, which is really useful for focusing on the information I need.


Reflection / What I Learned


Sorting and filtering taught me how to make sense of large datasets without changing the original data. I could answer questions like how many Senior customers there were in December, which days in Germany had the highest profit, and which US state made the most sales. Overall, this lab helped me understand that cleaning, sorting, and filtering data are essential first steps before any analysis, and it made me feel more confident using Excel to explore and present data.


</details>

<details><summary> Combining Datasets </summary>

| Part of Formula | Explanation |
|-----------------|------------|
| `INDEX` | This is the formula function that pulls a value from a table. |
| `ProductSales` | This is the table we want to get the information from. |
| `1` | This is the lookup value. |
| `($A2` | This contains the country name we want to match. |
| `0` | This specifies the type of match — 0 means an exact match. |
| `MATCH` | This finds what we want to match from our ProductProfit table to get the info. |
| `*` | This joins the two lookups together. |
| `3` | This is the column in the table where we want to put the matched value. |
| `($B2` | This contains the product description we want to match. |


</details>

<details><summary>Lab Manipulate Data </summary>


In this lab I learnt how to format and adjust data in Excel which made me realise that small changes can make a big difference. 

I practiced combining columns and highlighting data which helped me understand the data faster and made it easier to see patterns. 

I also noticed how formulas can save a lot of time compared to doing things manually.


Part 1 Combine Data in an Excel Spreadsheet


I opened the Bike Sales CSV file and looked at the columns. The product description and size were separate but for the analysis I needed them together.


I added a new column and typed the formula =L2&", "&M2 to combine model, colour, and size. I dragged it down the column to apply it to every row. 


Then I copied the column and pasted values over the original column so it was real text not formulas. I deleted the helper columns I didn’t need anymore. 


Doing this taught me that formulas are powerful but you need to convert them to values when you want to keep the data. I also realised that combining data makes it so much easier to sort, filter, and analyse later, instead of trying to keep track of multiple columns.


Part 2 Conditional Data Formatting


Step 1 Numeric values


I highlighted the Revenue column with colours based on how big the numbers were: green for very high, red for medium, yellow for low. 


This made it really easy to see which sales were performing well. Sorting the sheet by Revenue after that made the patterns even more obvious. I noticed that seeing things visually really speeds up understanding and helps spot important numbers quickly.


Step 2 Above average profit


I cleared the previous formatting and highlighted all Profit values above average. I noticed that the highlighting updates automatically if numbers change which is really useful when dealing with live data. 

It made me think about how this feature would be helpful if I was presenting to a team because they would always see up-to-date information without me having to redo the formatting.

Step 3 Text values


I cleared formatting again and highlighted all the rows with Australia in the Country column. The country stood out immediately. This made me realise that even simple text formatting can help spot trends or focus on specific groups in a big dataset. I also learned to check for spaces or hidden characters because otherwise the formatting wouldn’t work correctly.

Reflection


I’ve learnt that combining data and using conditional formatting isn’t just about making the sheet look nice. It actually makes it much easier to understand the data, find patterns, and focus on important values. I also realised that dynamic formatting, like highlighting above average profits, is really useful for keeping data accurate when things change. This lab made me feel more confident using Excel to clean, prepare, and explore data before any analysis or presentation. I can see how these skills will be useful in real work situations when I need to quickly make sense of large datasets.

</details>


