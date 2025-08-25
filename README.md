# Data Analytics Portfolio

This repository documents my journey through the TDM Data Analytics Level 4 course, including labs, projects, and reflections on the skills I have developed and applied. It also links my academic and professional experiences to my growth as a data analyst.

## About Me

I began my academic journey studying for a BSc in Psychology, developing a strong understanding of human behaviour. Early in my career, I joined TSB as an anti-fraud advisor. This role sparked my interest in enforcing policies and protecting others, combining analytical skills with a focus on security and prevention.  

Realising I wanted to build on my psychology knowledge in a more applied and investigative way, I pursued a Master's in Forensic Psychology. Once I graduated, I took the opportunity to join the West Midlands Police, where their values and commitment to serving the public aligned with my own.  

The apprenticeship with TDM, in collaboration with the Level 4 Data Analytics provider, has given me the chance to formalise and expand my analytical skills while applying them to real-world policing and security challenges.

## Course Overview

This portfolio captures the following modules and the key skills learned:

- **Module 1: Data Analytics Projects**  
  Exploring real-time analytics, building a project portfolio, documenting work, and sharing outputs.

- **Module 2: Getting Started with Data Gathering and Investigation**  
  Collecting, evaluating, and understanding datasets for analysis.

- **Module 3: Preparing and Cleaning Data for Analysis**  
  Correcting errors, standardising formats, and preparing data for accurate analysis.

- **Module 4: Transforming Data with Excel**  
  Applying formulas, functions, and charts to manipulate data and produce visualisations.

- **Module 5: Analyse the Data Using Statistics**  
  Using descriptive and inferential statistics to uncover insights and identify trends.

- **Module 6: Introduction to Relational Databases and SQL**  
  Understanding database structures and retrieving data efficiently using queries.

- **Module 7: Introduction to Structured Queries**  
  Using SQL to explore datasets, aggregate information, and generate actionable insights.

- **Module 8: Introduction to Tableau**  
  Creating interactive dashboards for visual storytelling and decision support.

- **Module 9: Ethics and Bias in Data**  
  Recognising ethical considerations, identifying bias, and ensuring fair and accurate analysis.

- **Module 10: Take the Next Steps**  
  Applying analytical skills to practical projects and planning further professional development.

## My Data Analytics Journey

My journey connects psychology, fraud prevention, and policing:

- Understanding human behaviour through psychology underpins my analytical reasoning.  
- Experience in anti-fraud taught me the importance of protecting people by enforcing policies.  
- Forensic psychology expanded my understanding of investigative processes and critical thinking.  
- Working with the West Midlands Police allows me to apply data analysis in real operational contexts to support law enforcement and public safety.  
- The TDM Level 4 Data Analytics course provides formal training to enhance my ability to analyse, interpret, and communicate data effectively.  

This portfolio reflects both my practical experience and the analytical skills I have developed through structured learning and applied projects.

## Using This Repository

- **Labs and Exercises**: Step-by-step exercises to build technical and analytical skills.  
- **Projects**: Applied examples connecting datasets to real-world policing and fraud prevention scenarios.  
- **Reflections**: Notes and reasoning behind analytical decisions.  
- **Visualisations and Statistics**: Charts, graphs, and summaries supporting insights from the data.

## Future Goals

- Deepen SQL and Tableau skills to handle larger and more complex datasets.  
- Explore predictive and prescriptive analytics to anticipate patterns and support proactive decision-making.  
- Continue building a professional portfolio that demonstrates both technical ability and reflective thinking in real-world contexts.

<details><summary> Best Practices </summary>

# Best Practices for Using SQL and Minimising Errors

Through my Cisco practicals, I’ve seen how easy it is to make small mistakes in SQL that cause either errors or misleading results. Below is a breakdown of best practices I’ve built up to help me minimise errors and write cleaner, more reliable queries.  

## 1. Be specific with SELECT  
Avoid using SELECT * unless I truly need every field. Writing out the exact column names keeps results clear and prevents issues if the table structure changes later.  

## 2. Watch spaces and formatting  
Extra or missing spaces can cause errors, especially when keywords or column names blend together. For example, SELECTtitle will fail, while SELECT title works. Consistent formatting, like capitalising keywords such as SELECT, WHERE, ORDER BY, makes the query easier to read and debug.  

## 3. Use commas carefully  
Forgetting a comma between column names is one of the easiest mistakes to make.  
Correct: SELECT title, year FROM Movie;  
Wrong: SELECT title year FROM Movie;  

## 4. Always end with a semicolon  
Some systems don’t mind if you forget the semicolon, but many do. It’s safer to always end queries properly so I don’t hit errors in environments that require it.  

## 5. Double-check spelling and case  
Table and column names must be exact. If a column is called MovieId, typing movieid might not work in certain databases. Cross-checking names in the schema avoids unnecessary debugging.  

## 6. Build queries step by step  
Start small and add pieces gradually.  

First run: SELECT title FROM Movie;  

Then add: WHERE year > 1976;  

Finally add: ORDER BY title ASC;  

This approach makes it clear where something goes wrong.  

## 7. Use comments to explain  
Adding -- for comments above tricky parts of a query means I can come back later and understand why I made certain choices.  

## 8. Handle conditions with care  
Using WHERE correctly is vital. Mixing up = with LIKE, or forgetting parentheses in combined conditions with AND or OR, can change the meaning of a query completely. Slow, logical thinking helps avoid subtle mistakes.  

## 9. Manage results with ORDER BY and LIMIT  
Large outputs are hard to check. Ordering results and limiting rows lets me confirm the query works before running it on the full dataset.  

## 10. Think beyond syntax  
Just because a query runs doesn’t mean it’s correct. I always pause to ask: does this output actually answer the question? If not, I revisit my logic.  

## Reflection  

Most of my errors in SQL have come from small details: missing spaces, commas, or semicolons. These are easy to overlook but critical for making queries work. The other big risk is logical mistakes like combining conditions incorrectly, which can give the wrong data without throwing an error. By slowing down, formatting queries clearly, and building them step by step, I’ve started to catch these mistakes early. Over time, these practices will help me write queries that are not just functional, but meaningful and trusted.  


</details>
