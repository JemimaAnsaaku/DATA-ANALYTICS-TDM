<details><summary> Objectives ✅ </summary>

During this module, I learned how to describe the various sources of data that are used in data analytics. I became able to describe various types of structured and unstructured data files. Finally, I was able to configure data according to the requirements of an analysis.
</details>

<details><summary> Selecting relevant data 🔎 </summary>

Selecting relevant data is vital in ensuring the validity and reliability of data analysis. It may be necessary to establish new procedures to collect the data required or could also involve combining data from multiple sources into a format that can be analysed. 
</details>

<details><summary> What should I ask myself when collecting a data source? </summary>

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

