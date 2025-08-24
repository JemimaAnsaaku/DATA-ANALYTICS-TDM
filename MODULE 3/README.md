<details><summary> Objectives ✅ </summary>

During this module, I learned how to describe the various sources of data that are used in data analytics. I became able to describe various types of structured and unstructured data files. Finally, I was able to configure data according to the requirements of an analysis.

</details>

<details><summary> Selecting relevant data 🔎 </summary>

Selecting relevant data is vital in ensuring the validity and reliability of data analysis. It may be necessary to establish new procedures to collect the data required or could also involve combining data from multiple sources into a format that can be analysed. 
</details>

<details><summary> What should I ask myself when collecting a data source? 🤨  </summary>

1. what data points are necessary to inform my analysis?

2. do i already have access to this data or must i find a dataset from another source?

3. Where are reliable and verifiable sources of this data?

4. How relevant is the data collected and updated

5. How is the data licensed for use, and is there a cost

6. Is the data in a format that i can use, or convert to use with the tools i have available?
</details>

<details><summary> combining relevant data in excel </summary>

Data analytics involves pulling information from multiple sources, which can be challenging to keep synchronised. In the Lab practical, I used Excel's workbook links feature to connect one worksheet to others, which ensures that data stays up to date. 


External references are espcially useful when large models cannot be stored in a single workbook. This feature allows me to:

- Consolidate data from multiple workbooks (years, departments, products) for summaries, reports or graphs.

- create subsets of data by linking only relevant information instead of entire workbooks.

- split complex data into smaller, more manageable workbooks while still being able to generate summaries or combined reports.

</details>

<details><summaries> LAB: Part 1: Link Multiple Worksheets </summaries>


I started off with two seperate worksheet datasets containing data about the bike sales from two seperate years, 2021 and 2022. 


I then opened up a new worksheet that was blank, and renamed it 'BikeSales_Consolidated'. 


Within workbook 'BikeSales_Consolidated' I pressed the '=' in cell A1, selected the tab of the worksheet that I wanted to import, which was Bike_Sales_2021, went back onto BikeSales_Consolidated, the function then contained the url of the worksheet i was importing and i clicked enter. 


I then repeated the process for workbook Bike_sales_2022. 
</details>

<details><summary> Refreshing data in multiple sheets </summary>
**linked averages updated automatically when the source data changed**

i refreshed workbook links to sync data 
</details>

<details><summary> Reflection 🪞 </summary>
workbooks are useful when managing data across multioke files, this comes in handy for tasks such as consolidating departmental budgets, combining regional sales, tracking projects, or splitting large datasets as they keep everything synchronised.

</details>

<details><summary> Data types </summary>

- static - data that is recieved and stored prior to performing analyses on the data. 

- streaming - data is processed and analysed as it is recieved and subsequent results are used or stored.

- string - data that is treated as text and composed of letters. numbers are not to be used.

- integer - whole numbers or numbers that do not unclude decimals - may or may not use negative numbers depending on computer language

- floating point - numbers with decimal places - frequantly used

- date and time - important in recording when an observation in a dataset was made

- boolean - data that is treated as either true or false. typically writted as TRUE or FALSE to indicate a Boolean result instead of a string

</details>

<details><summary> Characteristics of Structured Data </summary>

- Structured data refers to the data that is entered and maintained in defined fields within a file or record.

- structured data is easily entered, classified, classified, queried and analysed by a computer - for example, when we submit our name address and billing info into a website, we are creating structured data.

- it is well defined and organised in structure

- can be stored in tables, usually within vertical columns and horizontal rows

- the content and format of the data is documented

- it is organised into files, records and fields

- it can be searched, sorted and queried

- input controls can reduce the possibility of invalid data
</details>

<details><summary> CSV Files </summary>

different applications save data in different formats, so universal formats are used to ensure compatibility.

- CSV: Plain text, uses commas (or other seperators) for columns and new lines for rows, this is common for spreadsheers, databases, analytics and visualisation. Remember, a special character in CSV is any that is not a number or letter and can be used to seperate columns in a data table.

- JSON: lightweight, human-readable, widely used for data exchange.

- XML: Markup language similar to HTML, supports structured data.

Converting data into these common formats makes it easier to combine and share across different tools and systems. 

</details>

<details><summary> Structured File Types </summary>

There are many, hold on in your seat.,

- relational database - collection of tables with columns and rows which are connected by pre-defined relationships.

- Logs - machine generated historical record of everything that happens within a system (think transactions, errors, even log ticker.)

- spreadsheets - flat file database, it stores and records in a single file with no hierarchical structure

- sensor readings - sensor output usually collected in a standardised format, which may very by manufacturer. Individual readings may be seperated only by a delimiter or may be time dependent (one output per second seperated by timestamps.)

- transactional records - records of transactions can be stored in many different formats depending on transaction tyoe and source.

</details>

<details><summary> Unstructured data </summary>

Lacks the organisation found in structured data. This is raw data, not organised in a predefined way. It doesnt't have a fixed schema that identifies the type of data or its format. 


examples include the contents of photos, audio, video, web pages, blogs, books journals, white papers, powerpoint presentations, word processing documents and text in general.

</details>

<details><summary> Sources of unstructured data </summary>

- NoSQL databases and Data Lakes - unrelational databases or in data lakes (centralised repositories for data obtained from IoT devices, websites, mobile apps, social media and other sources of raw data. they are used to store real-time data in its original format.

- web scraping - automatically extract various forms of data drom HTML pages using a bot or webcrawler to gather and copy specific data drom the web database or spreadsheet. The data can then be easily analysed.

- Application Program Interfaces (APIs) - Most common application is called RESTful which uses HTTP as their communication protocol and JSON files to store data. Allows data analysts and engineers to access subsets of the large amount of data they are constantly generating.

</details>

<details><summaries> Data preparation - ETL and ELT </summaries>

ETL and ELT are both ways to move data from one place to another. The letters stand for Extract, Transform, Load. The only difference is the order of the last two steps.


- In ETL, you take the data, clean it up/transform it, and then put it into storage. This is good when the data is messy or in lots of different formats, because you make it neat before saving.


- In ELT, you take the data, put it into storage right away, and then clean it later when you actually need to use it. This is better for huge or unstructured data, because you can just dump it all in first.
So basically:


ETL = clean first, then store.


ELT = store first, then clean.


- Extract - data is located and gathered from various sources and then converted into a single format.

- Transform - Before data can go into a data warehouse, it often needs to be transformed so it matches the format the database requires. This can mean changing measurements (like converting Imperial to Metric), joining data from different sources, summarising or sorting it, creating new calculated values, and checking it with validation rules. Part of this process is cleaning (or scrubbing) the data. This means fixing errors, removing blanks, and making sure things like dates, times, and locations all follow the same format. Cleaning makes the data consistent and reliable for analysis.

- Load - transformed data is then loaded intothe database for querying. load processes vary widely. Some organisations may also overwrite existing data with newer culmative data. this is the step where rules that have been defined in the database schema are applied. 
</details>

<details><summary> Preparing data lab </summary>

**skim data to spot anomalies** - essential step in data cleansing to ensure these weaknesses are spotted and corrected, otherwise analyses become unreliable and misleading.

**step 1 Find duplicates** - find and remove duplicate entries. 


Select the column or row you wish to check for duplicates (it is usually a variable that cannot have multiple of the same variables such as order number. 


Once selected click 'conditional formatting' within home toolbar then 'highlight cell rules' - then duplicates then done. 


This highlights duplicate values within the column or row in red. 


Formula-bar way to spot duplicates:


=COUNTIF(A:A,A2)>1

- counts how many times the value in A2 shows up in column A.

- >1 -  asks, “does it show up more than once?”


- If YES → formula shows TRUE (duplicate).

  
If NO → formula shows FALSE (unique).


Formula 2: Show only unique values


=UNIQUE(A:A)


This is a newer Excel function.


It looks at all of column A and automatically spits out only the values that aren’t repeated.




***Step 3: Finding Empty Cells***

Blank cells happen for lots of reasons: human error, copying data, etc.


You can highlight blanks using Conditional Formatting - Highlight Cell Rules - Blanks - Green fill.


Once highlighted, check if you can fill them from context or source data; if not, you might have to delete them.


Example: fill C11=5, G16=Youth, M22=Mountain-200 Black, 42, N23=4.

1. Check if a whole row has any blanks

   
Example: Row 2 has data across columns A to D.


=COUNTBLANK(A2:D2)>0


COUNTBLANK(A2:D2) → counts how many blank cells in that row.


>0 → TRUE if at least one blank.

**Step 4: Splitting Text into Columns (Parsing)**


Some cells have multiple pieces of info (like product descriptions).


Use Text to Columns to split them by commas or spaces:


First, split size into a new column.


Then, split color into another new column.


What’s left is the model.


Check if a whole column has any blanks


Example: Column A, rows 2–100.


=COUNTBLANK(A2:A100)>0


Tells you if that column has at least one blank cell.


***Step 5: Removing Extra Spaces***

Extra spaces mess up searches or counts.


Use LEN() to check length, TRIM() to remove extra spaces.
Copy TRIM results back into the original column as values, then delete helper columns.


Sometimes a cell isn’t empty, it just has hidden spaces.


=LEN(A2)=0


TRUE if it’s really empty.


But if it looks empty and you get FALSE → then the cell has spaces or invisible characters.


***Step 6: Changing Case***

1. LOWER()


=LOWER(A2)


Takes whatever text is in cell A2.


Turns ALL letters into lowercase.


Example: UNITED STATES → united states.


use when  data is in ALL CAPS and you need it cleaner.


3. UPPER()


=UPPER(A2)


Takes whatever text is in A2.


Turns ALL letters into uppercase.


Example: united states → UNITED STATES.


Use when you want consistency in uppercase (like codes, acronyms).


PROPER()


=PROPER(A2)


Takes whatever text is in A2.


Capitalises the first letter of every word.


Example: united states → United States.


Use when you want neat titles or names.


***Step 7: Highlight Possible Errors***


Instead of scanning with your eyes, you let Excel highlight them.

Select the desired column.

Go to Home → Conditional Formatting → Highlight Cell Rules → Equal To.

In the box, type 0.

Pick a bright color (like red fill).

potential errors will now be highlighted 


***Step 8: Find and Replace***


Replace shorthand data with full words for clarity:


F → Female, M → Male.


Use Find & Replace with “Match case” as an option. When it’s on, Excel only finds text that exactly matches the uppercase and lowercase letters you typed. 


You can select the entire column first, then use Find & Replace with Match Case. Excel will only search within the selected column, not the whole sheet.


Single Cell Replacement (Formula-Bar Version)
Formula:


=IF(A2="F","Female",IF(A2="M","Male",A2))


Breakdown:


= starts a formula in Excel.


IF(condition, value_if_true, value_if_false) → checks a condition.


Step 1: IF(A2="F","Female",IF(A2="M","Male",A2))


Checks if A2 = "F".


If TRUE → returns "Female".


If FALSE → goes to the second IF.


Step 2 (nested IF): IF(A2="M","Male",A2)


Checks if A2 = "M".


If TRUE → returns "Male".


If FALSE → returns A2 (keeps original value).


Other details:


, -separates the three parts of each IF.


() → wraps the arguments for each IF.


"" → indicates text strings.


Logic in plain English:


If A2 = F → show Female


Else if A2 = M → show Male


Else → keep original value in A2



Usage:


Put formula in first row (e.g., Q2)


Drag down → applies to all rows in that column


**Step 9: Spell Check**

Use Review - Spelling to catch typos in text columns.


Ignore column names, fix actual spelling errors.



**Step 10: Remove Formatting**


Remove weird formatting like alignment or colors using 


home - clear - clear formats


</details>

<details><summary> Quiz Reflection </summary>

Open data is nnot protected by intellectual property restrictions and may be used and redistributed without legal, technical or social restrictions. 

Web scraping tools automatically extract data from the HTML pages often using a bot or web crawwler to find and obtain data, which can be gathered and copied from the web into a database or spreadsheet


when choosing data for analysis, important considerations must be made to ensure that the data is releanct to the original busienss question and the data is current.

</details>
