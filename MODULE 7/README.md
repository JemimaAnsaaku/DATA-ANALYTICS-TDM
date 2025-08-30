# Relational database structures

<details><summary>Relational Database Structures</summary>


Relational databases are powerful because they let me store data in different but related tables. This prevents repeating the same info all over the place and stops mistakes from showing up everywhere. Honestly, it feels like a huge time saver once I get it.
In the Movies database example, there’s a Movies table, a People table for actors and directors, tables that connect people to movies, and extra tables for gross income and reviews. I like how clean this is compared to dumping everything in one giant table.
With SQL, I can query one table easily, like getting all movies from 1984 or people from Spain. But if I want something more complex, like the nationalities of actors in a specific movie or directors of movies with average review scores above 9, I need to pull info from multiple tables.
That’s why I have to understand the database schema first. The schema tells me: what tables exist, what fields are in each table, how the tables connect, and what data types each field has. Without knowing this, trying to get the info I want would be chaos.

Table: This is where data lives, in rows and columns. Each row is a record, each column is a field. Easy enough to picture.

Field: One piece of info about a record. Column headings are the field names. For Movies, fields are MovieId, Title, and Year.

Record: One row in a table. Example: “Jaws” would be a record with its own MovieId, title, and year.

The schema doesn’t just tell me about fields and records. It also defines keys, relationships, and data types. These are critical because they keep everything connected and accurate.


### Keys
Data is spread across tables, and relationships help me put it together when I need it.

Example: Gross Income table stores the money each movie made every month of every year. I can’t repeat all movie info in this table, so I need a way to know which movie each row is about.

MovieId is unique in the Movies table. No two movies share the same MovieId. This is the primary key (PK). It defines a specific movie and prevents duplicates. I love that it makes things unambiguous.

I can use MovieId in Gross Income as a foreign key (FK). This points to the exact movie for each row without repeating all movie info.

Primary Key (PK): A column (or combo of columns) that uniquely identifies each record in the table. It can be one column or multiple columns combined.

Foreign Key (FK): A column (or combo) in one table that points to the primary key in another table. This links the tables.

Sometimes one field isn’t enough to make a row unique. In Gross Income, the combination of MovieId + Month + Year is unique, so this combo is the primary key. That makes sense because one movie can have many rows for different months and years.

If I make a new table, Gross_Income_Country, I’d use the original Gross Income PK as a FK, then add Country and Amount. The PK for this new table would be MovieId + Month + Year + Country, because that combination makes each row unique. It’s logic I can follow once I see it broken down.


### Database Relationships

A single movie can have many gross income rows. A single gross income row can have multiple Gross_Income_Country rows. This is a One-to-Many relationship. One MovieId appears in many Gross Income rows, but each Gross Income row points back to one movie.

Movies and Movie_Actor have a Many-to-Many relationship. One movie can have many actors, and one actor can be in many movies. This one took me a while to visualise, but thinking of actors moving between movies helps.

A movie can have one loan, and one loan applies to one movie. That’s a One-to-One relationship. I like this because it’s the simplest kind of relationship.

### Data Types

Each field has a type that tells the database what kind of info it can hold.

CHAR(size) – fixed-length text

VARCHAR(size) – variable-length text

TEXT – long text

INT – whole numbers

DECIMAL / FLOAT – numbers with decimals

DATETIME – date and time

This makes sure the database doesn’t accept nonsense, like putting letters where a number should go. It feels strict but necessary.

 </details>

 <details><summary> Using SQL with Multiple tables </summary>

## Joining Tables

Databases store info in tables, and tables are connected through keys. Sometimes the info I want isn’t all in one table, so I need a way to pull stuff together. That’s what a JOIN does.
Think of it like this: I have two lists. One list is movies, one list is reviews. The reviews have a number that says which movie they belong to. If I want a table that shows the movie title and the review info together, I need to “match” the right movie with the right review. That’s what the database does with JOIN.

### INNER JOIN: 

INNER JOIN Template
- SELECT a.column1, a.column2, b.column3, b.column4
- FROM TableA AS a
- INNER JOIN TableB AS b
- ON a.KeyColumn = b.KeyColumn

Explanation for my notes:

SELECT a.column1, a.column2, b.column3, b.column4 → choose which columns from both tables I want to see.

FROM TableA AS a → start with the main table, alias it a to make referencing easier.

INNER JOIN TableB AS b → join the second table, but only rows that exist in both tables will appear.

ON a.KeyColumn = b.KeyColumn → define the rule for matching rows between the two tables.


INNER JOIN = “show only rows that exist in both tables.”

TableA is the base, TableB is added where there’s a match.

KeyColumn can be any column that connects the two tables, usually a primary key to foreign key.

### LEFT JOIN

LEFT JOIN Template

- SELECT a.column1, a.column2, b.column3, b.column4
- FROM TableA AS a
- LEFT JOIN TableB AS b
- ON a.KeyColumn = b.KeyColumn

Explanation for my notes:

- SELECT a.column1, a.column2, b.column3, b.column4 → pick columns I actually want to see

- FROM TableA AS a → start with the main table, alias it a to make referencing easier

- LEFT JOIN TableB AS b → keep all rows from TableA, add TableB where there’s a match

- ON a.KeyColumn = b.KeyColumn → match rows based on the connecting column

When to use / why:

Use when I need everything from TableA, even if there’s no match in TableB.

Example in my brain: I want all movies, and if they have reviews, show them; if not, still show the movie.

### RIGHT JOIN

- RIGHT JOIN Template
- SELECT a.column1, a.column2, b.column3, b.column4
- FROM TableA AS a
- RIGHT JOIN TableB AS b
- ON a.KeyColumn = b.KeyColumn

Explanation for my notes:

- SELECT a.column1, a.column2, b.column3, b.column4 → pick columns I actually want to see

- FROM TableA AS a → start with the main table, alias it a to make referencing easier

- RIGHT JOIN TableB AS b → keep all rows from TableB, add TableA where there’s a match

- ON a.KeyColumn = b.KeyColumn → match rows based on the connecting column

When to use / why:

Use when I need everything from TableB, even if there’s no match in TableA.

Example in my brain: I want all reviews, even if some movies are missing from the database for some reason.

### FULL OUTER JOIN

FULL OUTER JOIN Template

- SELECT a.column1, a.column2, b.column3, b.column4
- FROM TableA AS a
- FULL OUTER JOIN TableB AS b
- ON a.KeyColumn = b.KeyColumn

Explanation for my notes:

- SELECT a.column1, a.column2, b.column3, b.column4 → pick columns I actually want to see

- FROM TableA AS a → start with the main table, alias it a to make referencing easier

- FULL OUTER JOIN TableB AS b → keep all rows from both tables

- ON a.KeyColumn = b.KeyColumn → match rows based on the connecting column

When to use / why:

Use when I want everything from both tables, no matter if there’s a match.

Example in my brain: I want a complete list of movies and reviews, including movies with no reviews and reviews for movies that might not be in the database.

### NATURAL JOIN

NATURAL JOIN Template

- SELECT a.column1, a.column2, b.column3, b.column4
- FROM TableA AS a
- NATURAL JOIN TableB AS b

Explanation for my notes:

- SELECT a.column1, a.column2, b.column3, b.column4 → pick columns I actually want to see

- FROM TableA AS a → start with the main table, alias it a to make referencing easier

- NATURAL JOIN TableB AS b → automatically join on columns with the same name and type

When to use / why:

Use when I know the columns match exactly in name and type, and I don’t want to write the ON clause.

Quick, convenient, like a shortcut, but dangerous if column names match accidentally and mean different things.


| JOIN Type         | What it shows                               | Unmatched rows                   | When I use it                                                      |
|------------------|--------------------------------------------|---------------------------------|-------------------------------------------------------------------|
| INNER JOIN        | Only rows that exist in both tables        | Ignored                          | When I only care about records that match in both tables          |
| LEFT JOIN         | All rows from the left table, matches from right | Right table columns = NULL      | When I want everything from the left table, even if right table has no data |
| RIGHT JOIN        | All rows from the right table, matches from left | Left table columns = NULL       | When I want everything from the right table, even if left table has no data |
| FULL OUTER JOIN   | All rows from both tables                  | Missing columns = NULL           | When I want a complete view of both tables, including unmatched rows |
| NATURAL JOIN      | Only rows where same-named columns match  | Ignored                          | When I want a shortcut join on identical column names, must be sure names/types match |


<details><summary> Data Manupulation Language </summary>

### Data Manipulation Language (DML)


Okay, so DML is basically how I actually put data into a database or mess with it. 

SELECT queries are useless if there’s nothing there to select, right?

INSERT: This is me adding a new row of data. Makes sense because the table is like an empty sheet, and I need to put info somewhere.

DELETE: Removes stuff I don’t need. I get why this exists, but I have to be careful—if I mess up the WHERE clause, I could wipe out the wrong row. That’s scary.

UPDATE and SET: Change something already there. I like that SET is explicit—it forces me to say exactly what I’m changing, which reduces mistakes.

LOCK: Stops others from touching a table while I’m working. This seems super important if multiple people are editing at once, but also feels restrictive if I just want to peek at something.


Why this matters: Without DML, the database is just an empty structure. I need these commands to make the database useful and dynamic.

### Data Definition Language (DDL)

DDL is like building the shelves before putting books on them. Makes sense—I can’t insert data if the table doesn’t exist.

CREATE: Makes a new table. Okay, this is obvious. I can define column names, types, primary keys. It’s like saying “this is what my data will look like.”

DROP: Deletes tables. Dangerous, like burning the shelves. I see why it exists, but I probably won’t use it casually.

ALTER: Change the table structure. Good for evolving data. I understand why this is critical because data requirements change over time.

RENAME: Rename tables. Useful but seems minor; maybe more for organization than functionality.

Understanding why: I get that DDL is foundational. Without it, there’s no “place” to put the data. DML and DDL go hand-in-hand: first build it (DDL), then fill and manage it (DML).


### Distributed Data and NoSQL

Okay, now it gets tricky. Relational databases are fine for small to medium stuff, but with massive datasets like web logs or social media, one server just can’t cut it. Makes sense—processing and storage are physical limits.

Distributed processing: Break data into chunks, give them to multiple computers, each handles its piece. Now I see why cloud computing is such a big deal—it’s basically teamwork for data.

NoSQL databases: These are weird but necessary. They don’t need rigid tables. I get why this is appealing—sometimes data is messy or constantly changing, so forcing it into a table is like trying to stuff a sofa into a suitcase.

Types of NoSQL:

Key-Value Stores: Each key is unique, value can be anything. Cool for things like user sessions where data doesn’t fit neatly into a table. Efficient, but I notice it probably can’t handle complex relationships well.

Document Databases: Stores JSON-like documents. Flexible. Makes sense if I don’t want to redesign my table every time I add a new field. But probably slower for relational queries.

Graph Databases: Store nodes and connections. This clicks—networks are naturally graphs. Social media or maps would be clunky in a normal table.

Wide Column Stores: Huge tables with mostly empty cells. Weird, but actually smart for sparse data like which users watched which movies. Normal relational tables would be inefficient.

Critical evaluation:

I get that NoSQL is fast and flexible, but it sacrifices accuracy, consistency, and standards. That makes me nervous for serious business stuff. Relational databases might be slower but feel safer.

So, NoSQL is great for huge, changing, messy data. Relational is great for structured, stable, accurate data. I can see why companies use both depending on their needs.

Overall takeaway in my own words:

DML is “playing with the data” – adding, changing, removing.

DDL is “building the containers” – tables, schemas, structure.

NoSQL and distributed databases exist because traditional RDBMS can’t handle massive, messy, or highly connected data efficiently. I understand the trade-offs: speed and flexibility vs safety and consistency.

