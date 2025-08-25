<details><summary> SQL Objectives </summary>

Introduction

Every day we create and use data through things like shopping online, posting on social media, or making bank transactions. All these actions generate records, which are stored in databases.

Relational databases are an important type of database where information is organised into tables. Each row is a record and each column holds a specific type of information. Understanding how these tables work is important because it shows how data is structured and how it can be connected to other information.

SQL, or Structured Query Language, is the tool used to ask questions to these databases. It allows me to retrieve exactly the data I need. Learning SQL is not just about remembering commands—it’s about understanding how to communicate with the data and how different tables relate to each other.

Reflecting on this, I realise that understanding data structure and learning to query it is essential. Without this understanding, analysing data could be slow, inaccurate, or incomplete. Thinking of SQL as a way to “talk to” the database helps me grasp why it is so important.

What Will I Learn in This Module?

Module title: Introduction to Structured Queries

The main goal is to learn how to write queries in SQL to get data from relational databases.

- A structured query is a precise question to the database to get specific information.  
- This is useful because large datasets are impossible to handle manually, and SQL helps retrieve relevant data quickly.  

Reflecting on this, the point is not just to run queries, but to understand why they work. Knowing why data is stored in certain ways and how queries interact with that structure helps me make sense of real-world datasets. This module lays the foundation for analysing data effectively.

</details>

<details><summary> Basic Data Management </summary>

# 6.1.1 Flat File Databases

Humans have been keeping records for thousands of years, mostly to track transactions like sales or payments. Early examples, like Babylonian cuneiform tablets, were essentially the first ledgers. I find it interesting that even today, we still use the same idea: we store information in rows and columns, just now on computers.  

Flat file databases are the digital version of these old ledgers. Each row is a record, and each column is a field that holds specific information. For example, a spreadsheet with movie titles, budgets, and release dates is a flat file database. CSV files work the same way, except they are plain text files where commas or other delimiters separate the data.  

Reflecting on this, I realise flat files are simple and easy to set up. They are fine for small datasets, but they start to break down as complexity grows. For example, if the same customer buys multiple items, their name is repeated each time. If a name is recorded differently, this creates inconsistencies. Adding new fields later is also hard, because it requires updating every row. This shows me that while flat files are a good starting point, they are not enough for complex or growing datasets.  

# 6.1.2 Limitations of Flat Files

Flat files are simple, but they don’t handle complex data well. For example, if I want to store a movie’s title, director, actors, monthly revenue, and reviews, a flat file becomes messy. I might try to add a column for every actor or a row for every month, but soon the file becomes too big and hard to manage.  

Reflecting on this, I understand why flat files are not used for large-scale operations. They create redundancy, data inconsistencies, and inefficiencies. This makes me appreciate the need for a better system when dealing with lots of connected data.  

# 6.1.3 Relational Databases

Relational databases solve the problems of flat files by separating data into multiple related tables. For the movie example, one table can store the movie title and release year, another table can store actors, another the directors, and another the reviews. Each table has a unique identifier that links it to the other tables.  

In a relational database, rows are still records and columns are fields, but the power comes from relationships between tables. For instance, a Person table can list each actor or director only once, and then link to the movies they are involved in. This avoids duplication and inconsistencies, which I now see as a major improvement over flat files.  

A schema documents the structure of all the tables, their fields, and how they relate. If I need to add a new field or table, I can do it easily without messing up the existing data. This reflection helps me see why relational databases are widely used—they make complex data manageable and more accurate.  

# 6.1.4 Relational Database Systems (RDBS)

To use relational databases, I need software called a Relational Database System (RDBS). Examples include MySQL, PostgreSQL, Oracle, and Microsoft SQL Server. These systems handle storing, retrieving, and managing the data efficiently.  

The advantages I notice are clear: relational databases store complex data efficiently, increase accuracy, reduce redundancy, and are better for large datasets. The challenges include cost, the need for specific skills, and potential performance issues if tables are very large or complex.  

Reflecting on this, I understand that relational databases are not perfect for every scenario, but they are essential for real-world data analysis. Learning how to use them, and how SQL queries interact with the tables, will be a crucial part of my journey to becoming a competent data analyst.  

</details>

<details><summary> SQL </summary>

Introduction to SQL

Once I have my relational database designed with all the tables and columns I need, I need a way to work with the data in it. That means I need to be able to add new data, read existing data, update data that changes, or delete anything that’s no longer needed. To do all of this, most relational databases use SQL, which stands for Structured Query Language. Every time I write a command in SQL to do something, that’s called a “query.”

SQL is made up of statements, and just like other programming languages, it has a defined syntax. I learned that syntax is basically the grammar and rules of the language. If I don’t follow the rules, the database won’t understand my query.  

 Reading Data with SELECT

For example, if I have a table called Movie  with columns MovieId, Title, and Year, and I want to see all the titles and years of the movies, I can write:

SELECT title, year FROM Movie;

The keyword SELECT tells the database that I want to read or “select” specific data. This is part of Data Manipulation Language (DML), which includes commands like SELECT, INSERT, UPDATE, and DELETE. These are the commands I use to work with the actual data in the tables.  

Reflecting on this, I realise that SELECT is the first tool I need to get any insight from a database. Without SELECT, I can’t even start analyzing data.

Data Definition Language (DDL)

There’s also Data Definition Language, or DDL. This is the part of SQL that lets me create and manage the structure of the database itself. With DDL I can create tables, define which columns they have, and set the type of data each column should hold (like numbers, text, or dates).  

Reflecting here, I see DDL as setting up the “rules” for the data. Without it, the database could get messy because there would be no structure or standards.

SQL is Universal

SQL is used by almost every relational database system (RDBS), so relational databases are often called “SQL databases.” Even though SQL is a standard, each system might have slightly different keywords or options. This reminds me to always check the documentation of the specific system I’m using.

Querying Specific Data

So far, using SELECT lets me get all the rows in a table, but in real life, I usually need a specific subset of data. For example, if I only want movies released after 1976, and I want them listed alphabetically, I can use a query like this:

SELECT title, year
FROM Movie
WHERE year > 1976
ORDER BY title ASC;

Here, I am using:

- WHERE to filter the rows. It’s like saying “only give me the rows that meet this condition.” I now understand this is essential because databases can have thousands or millions of rows, and I rarely want everything.
- ORDER BY to sort the results. ASC means ascending order (A-Z). I realise sorting helps me see patterns and makes the data easier to interpret.

Reflecting on this, I see that SQL lets me ask very specific questions. I’m no longer just staring at a big table hoping to notice patterns manually. With SELECT, WHERE, and ORDER BY, I can start exploring data more efficiently.

 Logic Operators in SQL

I also learned that SQL supports logic operators like =, <>, >, <, >=, <=, AND, OR, and NOT. These allow me to combine conditions in the WHERE clause and refine my queries. For example, I can ask for movies released after 1976 AND with a certain director, which makes the queries much more powerful.

Reflecting here, I see that mastering these operators will be crucial for more advanced analysis. They let me slice the data exactly how I need it, which is what data analysis is all about.


</details>

<details><summary> Using SQL to Query data </summary>

Using SQL to Query Data

As I start working more with SQL, I’m realising that while I can pull all the data from a table, in real data analysis I almost never want everything. Usually, I’m interested in just a specific subset of information that answers a question or helps me find a pattern.  

For example, in the Movies database I’ve been using, I first learned how to list every movie’s title and year. That’s fine for practice, but it’s not very useful if I only want recent movies or want to sort them in a specific way. This is where the power of SQL really shows.  


Breaking this down:  

- SELECT Command: This tells SQL which columns I want to see. In this case, I only want the title and year. I’m not pulling all the other columns like director or revenue because I don’t need them right now. This is efficient and keeps the output focused.  

- FROM Command: This defines the table I’m querying, here it’s Movie. I need to know the table structure first so I can pull the right columns.  

- WHERE Command: This allows me to filter the data. By using year > 1976, I’m only selecting rows that meet this condition. I like thinking of it as setting rules for which data to include.  

- **ORDER BY Command**: This sorts the results. title ASC means the titles will be in alphabetical order from A to Z. I could also use DESC if I wanted them in reverse order. Sorting is really helpful when scanning large outputs or preparing reports.  

Reflections:  

Working through this query makes me see how SQL is not just about getting data—it’s about controlling what you get and how it’s presented. I’m also starting to understand why logical operators like `>` (greater than), `<` (less than), `=` (equal), and `!=` (not equal) are so essential. They let me shape the data to answer the questions I actually care about.  

This feels very different from just scrolling through a spreadsheet. With SQL, I can ask very specific questions and get exactly what I need, which is essential when datasets are huge or constantly changing.

</details>

<details><summary> SQL Operators Summary </summary>

# SQL Operators Summary

| Operator | Meaning / Description | Why it is Important | Example |
|----------|--------------------|------------------|---------|
| =        | Equal to           | Used to match exact values in a column | `SELECT * FROM Movie WHERE year = 1995;` |
| != or <> | Not equal to       | Filters out specific values from results | `SELECT * FROM Movie WHERE year != 1995;` |
| >        | Greater than       | Finds values above a certain threshold | `SELECT title FROM Movie WHERE year > 2000;` |
| >=       | Greater than or equal to | Includes the threshold value in results | `SELECT title FROM Movie WHERE year >= 2000;` |
| <        | Less than          | Finds values below a certain threshold | `SELECT title FROM Movie WHERE year < 2000;` |
| <=       | Less than or equal to | Includes the threshold value in results | `SELECT title FROM Movie WHERE year <= 2000;` |
| BETWEEN  | Between a range of values | Filters results within a specific range, inclusive | `SELECT * FROM Movie WHERE year BETWEEN 1990 AND 2000;` |
| LIKE     | Pattern matching   | Finds values that match a text pattern, useful for partial matches | `SELECT * FROM Movie WHERE title LIKE 'Toy%';` |
| IN       | Matches any value in a list | Efficient for checking multiple possible matches | `SELECT * FROM Movie WHERE year IN (1995, 1996, 1997);` |
| AND      | Logical AND        | Combines multiple conditions, all must be true | `SELECT * FROM Movie WHERE year > 2000 AND revenue > 50000000;` |
| OR       | Logical OR         | Combines multiple conditions, any can be true | `SELECT * FROM Movie WHERE year < 1990 OR revenue > 50000000;` |
| IS NULL  | Checks for empty values | Filters records with missing or unknown values | `SELECT * FROM Movie WHERE revenue IS NULL;` |
| IS NOT NULL | Checks for non-empty values | Filters records that have actual values | `SELECT * FROM Movie WHERE revenue IS NOT NULL;` |

</details>
