# MySQL Practice README

Welcome to the MySQL Practice Repository! This guide will walk you through various SQL lessons with practical exercises, designed to enhance your skills in interacting with databases using MySQL.

## Table of Contents

1. [Introduction to SQL](#introduction-to-sql)
2. [SQL Lesson 1: SELECT queries 101](#sql-lesson-1-select-queries-101)
3. [SQL Lesson 2: Queries with constraints (Pt. 1)](#sql-lesson-2-queries-with-constraints-pt-1)
4. [SQL Lesson 3: Queries with constraints (Pt. 2)](#sql-lesson-3-queries-with-constraints-pt-2)
5. [SQL Lesson 4: Filtering and sorting Query results](#sql-lesson-4-filtering-and-sorting-query-results)
6. [SQL Review: Simple SELECT Queries](#sql-review-simple-select-queries)
7. [SQL Lesson 6: Multi-table queries with JOINs](#sql-lesson-6-multi-table-queries-with-joins)
8. [SQL Lesson 7: OUTER JOINs](#sql-lesson-7-outer-joins)
9. [SQL Lesson 8: A short note on NULLs](#sql-lesson-8-a-short-note-on-nulls)
10. [SQL Lesson 9: Queries with expressions](#sql-lesson-9-queries-with-expressions)
11. [SQL Lesson 10: Queries with aggregates (Pt. 1)](#sql-lesson-10-queries-with-aggregates-pt-1)
12. [SQL Lesson 11: Queries with aggregates (Pt. 2)](#sql-lesson-11-queries-with-aggregates-pt-2)
13. [SQL Lesson 12: Order of execution of a Query](#sql-lesson-12-order-of-execution-of-a-query)
14. [SQL Lesson 13: Inserting rows](#sql-lesson-13-inserting-rows)
15. [SQL Lesson 14: Updating rows](#sql-lesson-14-updating-rows)
16. [SQL Lesson 15: Deleting rows](#sql-lesson-15-deleting-rows)
17. [SQL Lesson 16: Creating tables](#sql-lesson-16-creating-tables)
18. [SQL Lesson 17: Altering tables](#sql-lesson-17-altering-tables)
19. [SQL Lesson 18: Dropping tables](#sql-lesson-18-dropping-tables)

## Introduction to SQL

In this section, you'll get a brief overview of SQL and its importance in managing and querying relational databases.
---

## SQL Lesson 1: SELECT queries 101

Learn the basics of retrieving data from a single table using SELECT statements.

 **SELECT QUERIES**

## Overview

This README offers a succinct introduction to the SQL table, "Movies." This table is designed to facilitate the storage and retrieval of comprehensive information regarding various films. It encompasses key data fields, including a unique identifier, film title, director, release year, and film duration in minutes.

## Table Structure

The "Movies" table is structured as follows:

- **Id**: An integer serving as the primary key and a unique identifier for each film in the database.
- **Title**: A text field representing the film's title.
- **Director**: A text field containing the name of the film's director.
- **Year**: An integer representing the film's release year.
- **Length_minutes**: An integer indicating the film's duration in minutes.

# Movie Database (Movies)

## Table Structure

## Sample Data

Here is a glimpse of the data stored in the "Movies" table:

| Id | Title           | Director        | Year | Length_minutes |
|----|-----------------|-----------------|------|----------------|
| 1  | Toy Story       | John Lasseter   | 1995 | 81             |
| 2  | A Bug's Life    | John Lasseter   | 1998 | 95             |
| 3  | Toy Story 2     | John Lasseter   | 1999 | 93             |
| 4  | Monsters, Inc.  | Pete Docter     | 2001 | 92             |
| 5  | Finding Nemo    | Andrew Stanton  | 2003 | 107            |
| 6  | The Incredibles | Brad Bird       | 2004 | 116            |
| 7  | Cars            | John Lasseter   | 2006 | 117            |
| 8  | Ratatouille     | Brad Bird       | 2007 | 115            |
| 9  | WALL-E          | Andrew Stanton  | 2008 | 104            |
| 10 | Up              | Pete Docter     | 2009 | 101            |

## Task List

This section outlines a series of SQL queries that can be executed on the "Movies" table to retrieve specific information. These tasks are particularly valuable in exploring the dataset and gaining insights into the films it contains.

### Task 1: Find the Title of Each Film


SELECT Title FROM Movies;

### Task 2: Find the Director of Each Film


SELECT Director FROM Movies;

### Task 3: Find the Title and Director of Each Film


SELECT Title, Director FROM Movies;

### Task 4:Find the Title and Year of Each Film


SELECT Title, Year FROM Movies;

### Task 5:Find All Information About Each Film


SELECT * FROM Movies;

## Task List

This section provides a set of SQL queries that can be executed on the "Movies" table to retrieve specific information. These tasks are especially valuable for exploring the dataset and gaining insights into the films it contains.

- 🎬 **Task 1:** Find the Title of Each Film
- 🎥 **Task 2:** Find the Director of Each Film
- 🎬🎥**Task 3:** Find the Title and Director of Each Film
- 📅🎬**Task 4:** Find the Title and Year of Each Film
- 📚**Task 5:** Find All Information About Each Film

---

## Lesson 2: Queries with constraints

Explore the use of WHERE clause to filter data based on specific conditions.

**QUERIES WITH CONSTRAINTS**

# Useful Numerical Operators

Below are some useful operators that you can use for numerical data (i.e., integers or floating-point numbers) in SQL queries, along with MySQL examples:

- **Standard Numerical Operators**: These operators are used for standard numerical comparisons:

   - `=`: Equal to
     
   - `!=`: Not equal to
     
   - `<`: Less than
     e.g. 
     SELECT column_name
     FROM table_name
     WHERE column_name < 42;
     
   - `<=`: Less than or equal to
     e.g.
     SELECT column_name
     FROM table_name
     WHERE column_name <= 42;
     
   - `>`: Greater than
     e.g.
     SELECT column_name
     FROM table_name
     WHERE column_name > 42;
     
   - `>=`: Greater than or equal to
     e.g.
     SELECT column_name
     FROM table_name
     WHERE column_name >= 42;
   
   - **BETWEEN ... AND ...**: Number is within the range of two values (inclusive)
     e.g.
     SELECT column_name
     FROM table_name
     WHERE col_name BETWEEN 1.5 AND 10.5;
     
   - **NOT BETWEEN ... AND ...**: Number is not within the range of two values (inclusive)
     e.g.
     SELECT column_name
     FROM table_name
     WHERE col_name NOT BETWEEN 1 AND 10;
    
   - **IN (...)**: Number exists in ...
     e.g.
     SELECT column_name
     FROM table_name
     WHERE col_name IN (2, 4, 6);
     
   - **NOT IN (...)**: Number does not exist in a list
     e.g.
     SELECT column_name
     FROM table_name
     WHERE col_name NOT IN (1, 3, 5);
    
   - **LIKE**: Case insensitive exact string comparison
    e.g.
     SELECT First_Name
     FROM table_name
     WHERE First_Name LIKE "HIRUT";
     
   - **NOT LIKE**: Case insensitive exact string inequality comparison
     e.g.
     SELECT First_Name
     FROM table_name
     WHERE First_Name NOT LIKE "HIRUT";
  
   - **%**: Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)
     SELECT col_name
     FROM table_name
     WHERE col_name LIKE "%AT%";

Using the right constraints, find the information we need from the Movies table for each task below

Table: Movies

| Id  | Title               | Director         | Year | Length_minutes |
| --- | ------------------- | ---------------- | ---- | -------------- |
| 1   | Toy Story           | John Lasseter    | 1995 | 81             |
| 2   | A Bug Life        | John Lasseter    | 1998 | 95             |
| 3   | Toy Story 2         | John Lasseter    | 1999 | 93             |
| 4   | Monsters, Inc.      | Pete Docter      | 2001 | 92             |
| 5   | Finding Nemo        | Andrew Stanton   | 2003 | 107            |
| 6   | The Incredibles     | Brad Bird        | 2004 | 116            |
| 7   | Cars                | John Lasseter    | 2006 | 117            |
| 8   | Ratatouille         | Brad Bird        | 2007 | 115            |
| 9   | WALL-E              | Andrew Stanton   | 2008 | 104            |
| 10  | Up                  | Pete Docter      | 2009 | 101            |
| 11  | Toy Story 3         | Lee Unkrich      | 2010 | 103            |
| 12  | Cars 2              | John Lasseter    | 2011 | 120            |
| 13  | Brave               | Brenda Chapman   | 2012 | 102            |
| 14  | Monsters University | Dan Scanlon      | 2013 | 110            |

## Task List

### Task 1: Find the movie with a row id of 6:

```sql
SELECT * FROM Movies
WHERE Id = 6;
```

### Task 2: Find the movies released in the years between 2000 and 2010:

```sql
SELECT * FROM Movies
WHERE Year
BETWEEN 2000 AND 2010;
```

### Task 3: Find the movies not released in the years between 2000 and 2010:

```sql
SELECT * FROM Movies
WHERE Year
NOT BETWEEN 2000 AND 2010;
```

### Task 4:Find the first 5 Pixar movies and their release year:

```sql
SELECT title, year FROM movies
WHERE year <= 2003;
```

## SQL Lesson 3: Queries with constraints (Pt. 2)

Continue working with constraints, introducing logical operators.

Table: Movies

| Id  | Title               | Director         | Year | Length_minutes |
| --- | ------------------- | ---------------- | ---- | -------------- |
| 1   | Toy Story           | John Lasseter    | 1995 | 81             |
| 2   | A Bug's Life        | John Lasseter    | 1998 | 95             |
| 3   | Toy Story 2         | John Lasseter    | 1999 | 93             |
| 4   | Monsters, Inc.      | Pete Docter      | 2001 | 92             |
| 5   | Finding Nemo        | Andrew Stanton   | 2003 | 107            |
| 6   | The Incredibles     | Brad Bird        | 2004 | 116            |
| 7   | Cars                | John Lasseter    | 2006 | 117            |
| 8   | Ratatouille         | Brad Bird        | 2007 | 115            |
| 9   | WALL-E              | Andrew Stanton   | 2008 | 104            |
| 10  | Up                  | Pete Docter      | 2009 | 101            |
| 11  | Toy Story 3         | Lee Unkrich      | 2010 | 103            |
| 12  | Cars 2              | John Lasseter    | 2011 | 120            |
| 13  | Brave               | Brenda Chapman   | 2012 | 102            |
| 14  | Monsters University | Dan Scanlon      | 2013 | 110            |
| 87  | WALL-G              | Brenda Chapman   | 2042 | 97             |

## Task List

### Task 1: Find all the Toy Story movies

```sql
SELECT title, director FROM movies
WHERE title LIKE "Toy Story%";

### Task 2: Find all the movies directed by John Lasseter

```sql
SELECT * FROM Movies
WHERE Director Like "john Lasseter";

### Task 3: Find all the movies (and director) not directed by John Lasseter

```sql
SELECT * FROM Movies
WHERE Director NOT LIKE 'john Lasseter';

### Task 4: Find all the WALL-* movies

```sql
SELECT * FROM Movies
WHERE Title LIKE 'WALL%';

---
## SQL Lesson 4: Filtering and sorting Query results

Learn how to order and filter query results to meet specific requirements.

4.1 Select query with unique results (DISTINCT remove duplicates)

- SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);

4.2 Select query with unique results (DISTINCT remove duplicates)

-SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC;

4.3 Select query with limited rows

-SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;;

### Exercise:

Table: Movies

| Id  | Title                         | Director                  | Year | Length_minutes |
| --- | -------------------         | ----------------            | ----    | -------------- |
| 1   | Finding Nemo         | Andrew Stanton      | 2003 | 107            |
| 2   | WALL-E                  | Andrew Stanton       | 2008 | 104            |
| 3   | A Bug's Life            | John Lasseter           | 1998 | 95             |
| 4   | Monsters, Inc.         | Pete Docter             | 2001 | 92             |
| 5   | Monsters University| Dan Scanlon      | 2013 | 110            |
| 6   | Toy Story 3              | Lee Unkrich      | 2010 | 103            |
| 7   | Cars 2                     | John Lasseter    | 2011 | 120            |
| 8   | Ratatouille               | Brad Bird        | 2007 | 115            |
| 9   | Cars                         | John Lasseter    | 2006 | 117            |
| 10  | The Incredibles       | Brad Bird        | 2004 | 116            |
| 11  | Toy Story                 | John Lasseter    | 1995 | 81             |
| 12  | Brave                      | Brenda Chapman   | 2012 | 102            |
| 13  | Toy Story 2              | John Lasseter    | 1999 | 93             |
| 14  | Up                           | Pete Docter      | 2009 | 101            |

## Task List

### Task 1: List all directors of Pixar movies (alphabetically), without duplicates

```sql
SELECT DISTINCT director FROM movies
ORDER BY director ASC;

### Task 2: List the last four Pixar movies released (ordered from most recent to least)

```sql
SELECT title, year FROM movies
ORDER BY year DESC
LIMIT 4;


### Task 3: List the first five Pixar movies sorted alphabetically

```sql
SELECT * FROM Movies
ORDER BY Title ASC
LIMIT 5;

### Task 4:List the next five Pixar movies sorted alphabetically

```sql
SELECT title FROM movies
ORDER BY title ASC
LIMIT 5 OFFSET 5;

### Task 5: List five movies starting from the 4th row:

```sql
SELECT *FROM movies
ORDER BY title ASC
LIMIT 5 OFFSET 3;

SUMMARY EXERCISES

Table: North_american_cities
| City                | Country         | Population | Latitude   | Longitude   |
| ------------------- | --------------- | ---------- | ---------- | ----------- |
| Guadalajara         | Mexico          | 1,500,800  | 20.659699  | -103.349609 |
| Toronto             | Canada          | 2,795,060  | 43.653226  | -79.383184  |
| Houston             | United States   | 2,195,914  | 29.760427  | -95.369803  |
| New York            | United States   | 8,405,837  | 40.712784  | -74.005941  |
| Philadelphia        | United States   | 1,553,165  | 39.952584  | -75.165222  |
| Havana              | Cuba            | 2,106,146  | 23.054070  | -82.345189  |
| Mexico City         | Mexico          | 8,555,500  | 19.432608  | -99.133208  |
| Phoenix             | United States   | 1,513,367  | 33.448377  | -112.074037 |
| Los Angeles         | United States   | 3,884,307  | 34.052234  | -118.243685 |
| Ecatepec de Morelos | Mexico          | 1,742,000  | 19.601841  | -99.050674  |
| Montreal            | Canada          | 1,717,767  | 45.501689  | -73.567256  |
| Chicago             | United States   | 2,718,782  | 41.878114  | -87.629798  |

## Task List

### Task 1: List all the Canadian cities and their populations

**Note**: above task can be answered using two options

**Option 1**
```sql
SELECT city, Population
FROM North_american_cities
WHERE country LIKE 'Canada';

**Option 2**

SELECT City, Population FROM North_american_cities
WHERE Country = 'Canada';

### Task 2:Order all the cities in the United States by their latitude from north to south

```sql
SELECT city, latitude FROM north_american_cities
WHERE country = "United States"
ORDER BY latitude DESC;

### Task 3: List all the cities west of Chicago, ordered from west to east

**option 1**
```sql
SELECT city, longitude FROM north_american_cities
WHERE longitude < -87.629798
ORDER BY longitude ASC;

**option 2**

SELECT City, Longitude FROM North_american_cities
WHERE Longitude < (SELECT Longitude FROM North_american_cities WHERE City = 'Chicago')
ORDER BY Longitude ASC;

### Task 4:List the two largest cities in Mexico (by population)

```sql
SELECT city, population FROM north_american_cities
WHERE country LIKE "Mexico"
ORDER BY population DESC
LIMIT 2;



### Task 5:List the third and fourth largest cities (by population) in the United States and their population

**option 1**
```sql
SELECT city, population FROM north_american_cities
WHERE country LIKE "United States"
ORDER BY population DESC
LIMIT 2 OFFSET 2;

**option 2**
```sql
SELECT City, Population FROM North_american_cities
WHERE Country = 'United States'
ORDER BY Population DESC
LIMIT 2 OFFSET 2;
---

## SQL Lesson 6:

So far, we've been dealing with one table. In the real world, information about things is often divided and spread across different tables. This process is called normalization.

6.1 Multi-table queries with JOINs
Explore JOIN operations to retrieve data from multiple tables.

Tables that share information about a single entity need to have a primary key that identifies that entity uniquely across the database. One common primary key type is an auto-incrementing integer (because they are space efficient), but it can also be a string, hashed value, so long as it is unique.

Using the JOIN clause in a query, we can combine row data across two separate tables using this unique key. The first of the joins that we will introduce is the INNER JOIN.

**usage**
Select query with INNER JOIN on multiple tables

SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;

The INNER JOIN is a process that matches rows from the first table and the second table which have the same key (as defined by the ON constraint) to create a result row with the combined columns from both tables. After the tables are joined, the other clauses we learned previously are then applied.

### Exercise:

We've added a new table to the Pixar database so that you can try practicing some joins. The BoxOffice table stores information about the ratings and sales of each particular Pixar movie, and the Movie_id column in that table corresponds with the Id column in the Movies table 1-to-1. Try and solve the tasks below using the INNER JOIN introduced above.

Table: Movies (Read-Only)
| Id | Title           | Director       | Year | Length_minutes |
|----|-----------------|-----------------|------|----------------|
| 1  | Toy Story       | John Lasseter   | 1995 | 81             |
| 2  | A Bug's Life    | John Lasseter   | 1998 | 95             |
| 3  | Toy Story 2     | John Lasseter   | 1999 | 93             |
| 4  | Monsters, Inc.  | Pete Docter     | 2001 | 92             |

---

Table: Boxoffice (Read-Only)

| Movie_id | Rating | Domestic_sales | International_sales |
|----------|--------|-----------------|----------------------|
| 5        | 8.2    | 380,843,261     | 555,900,000          |
| 14       | 7.4    | 268,492,764     | 475,066,843          |
| 8        | 8      | 206,445,654     | 417,277,164          |
| 12       | 6.4    | 191,452,396     | 368,400,000          |
| 3        | 7.9    | 245,852,179     | 239,163,000          |
| 6        | 8      | 261,441,092     | 370,001,000          |
| 9        | 8.5    | 223,808,164     | 297,503,696          |
| 11       | 8.4    | 415,004,880     | 648,167,031          |
| 1        | 8.3    | 191,796,233     | 170,162,503          |
| 7        | 7.2    | 244,082,982     | 217,900,167          |
| 10       | 8.3    | 293,004,164     | 438,338,580          |
| 4        | 8.1    | 289,916,256     | 272,900,000          |
| 2        | 7.2    | 162,798,565     | 200,600,000          |
| 13       | 7.2    | 237,283,207     | 301,700,000          |

---

Exercise 6 — Tasks

1. Find the domestic and international sales for each movie

```sql
SELECT title, domestic_sales, international_sales
FROM movies
  JOIN boxoffice
    ON movies.id = boxoffice.movie_id;

2. Show the sales numbers for each movie that did better internationally rather than domestically

SELECT title, domestic_sales, international_sales
FROM movies
  JOIN boxoffice
    ON movies.id = boxoffice.movie_id
WHERE international_sales > domestic_sales;

3. List all the movies by their ratings in descending order

SELECT title, rating
FROM movies
  JOIN boxoffice
    ON movies.id = boxoffice.movie_id
ORDER BY rating DESC;

---

## SQL Lesson 7: OUTER JOINs

Understand and practice using OUTER JOINs to include unmatched rows in the result set. Depending on how you want to analyze the data, the INNER JOIN we used last lesson might not be sufficient because the resulting table only contains data that belongs in both of the tables.

If the two tables have asymmetric data, which can easily happen when data is entered in different stages, then we would have to use a LEFT JOIN, RIGHT JOIN or FULL JOIN instead to ensure that the data you need is not left out of the results.
### Exercise:
List all customers and their orders, including those with no orders.

**Usage**:Select query with LEFT/RIGHT/FULL JOINs on multiple tables

SELECT column, another_column, …
FROM mytable
INNER/LEFT/RIGHT/FULL JOIN another_table
    ON mytable.id = another_table.matching_id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;

### Exercise 7:

In this exercise, you are going to be working with a new table which stores fictional data about Employees in the film studio and their assigned office Buildings. Some of the buildings are new, so they don't have any employees in them yet, but we need to find some information about them regardless.

Since our browser SQL database is somewhat limited, only the LEFT JOIN is supported in the exercise below.

Table: Buildings (Read-Only)

| Building_name | Capacity |
|---------------|----------|
| 1e            | 24       |
| 1w            | 32       |
| 2e            | 16       |
| 2w            | 20       |

---

Table: Employees (Read-Only)

| Role     | Name         | Building | Years_employed |
|----------|--------------|----------|----------------|
| Engineer | Becky A.     | 1e       | 4              |
| Engineer | Dan B.       | 1e       | 2              |
| Engineer | Sharon F.    | 1e       | 6              |
| Engineer | Dan M.       | 1e       | 4              |
| Engineer | Malcom S.    | 1e       | 1              |
| Artist   | Tylar S.     | 2w       | 2              |
| Artist   | Sherman D.   | 2w       | 8              |
| Artist   | Jakob J.     | 2w       | 6              |
| Artist   | Lillia A.    | 2w       | 7              |
| Artist   | Brandon J.   | 2w       | 7              |
| Manager  | Scott K.     | 1e       | 9              |
| Manager  | Shirlee M.   | 1e       | 3              |
| Manager  | Daria O.     | 2w       | 6              |

---

Exercise 7 — Tasks

1.Find the list of all buildings that have employees

SELECT DISTINCT building FROM employees;

2.Find the list of all buildings and their capacity

SELECT Building, Capacity
FROM buildings;

3. List all buildings and the distinct employee roles in each building (including empty buildings)

SELECT DISTINCT building_name, role
FROM buildings
  LEFT JOIN employees
    ON building_name = building;

---

## SQL Lesson 8: A short note on NULLs

t's always good to reduce the possibility of NULL values in databases because they require special attention when constructing queries, constraints (certain functions behave differently with null values) and when processing the results.

An alternative to NULL values in your database is to have data-type appropriate default values, like 0 for numerical data, empty strings for text data, etc. But if your database needs to store incomplete data, then NULL values can be appropriate if the default values will skew later analysis (for example, when taking averages of numerical data).

Sometimes, it's also not possible to avoid NULL values, as we saw in the last lesson when outer-joining two tables with asymmetric data. In these cases, you can test a column for NULL values in a WHERE clause by using either the IS NULL or IS NOT NULL constraint.

**Usage**:Select query with constraints on NULL values
SELECT column, another_column, …
FROM mytable
WHERE column IS/IS NOT NULL
AND/OR another_condition
AND/OR …;

### Exercise 8:

This exercise will be a sort of review of the last few lessons. We're using the same Employees and Buildings table from the last lesson, but we've hired a few more people, who haven't yet been assigned a building.

Table: Buildings

| Building_name | Capacity |
|---------------|----------|
| 1e            | 24       |
| 1w            | 32       |
| 2e            | 16       |
| 2w            | 20       |

---

Table: Employees

| Role     | Name         | Building | Years_employed |
|----------|--------------|----------|----------------|
| Engineer | Becky A.     | 1e       | 4              |
| Engineer | Dan B.       | 1e       | 2              |
| Engineer | Sharon F.    | 1e       | 6              |
| Engineer | Dan M.       | 1e       | 4              |
| Engineer | Malcom S.    | 1e       | 1              |
| Artist   | Tylar S.     | 2w       | 2              |
| Artist   | Sherman D.   | 2w       | 8              |
| Artist   | Jakob J.     | 2w       | 6              |
| Artist   | Lillia A.    | 2w       | 7              |
| Artist   | Brandon J.   | 2w       | 7              |
| Manager  | Scott K.     | 1e       | 9              |
| Manager  | Shirlee M.   | 1e       | 3              |
| Manager  | Daria O.     | 2w       | 6              |
| Engineer | Yancy I.     |          | 0              |
| Artist   | Oliver P.    |          | 0              |

---

Exercise 8 — Tasks

1. Find the name and role of all employees who have not been assigned to a building

SELECT name, role FROM employees
WHERE building IS NULL;

2. Find the names of the buildings that hold no employees

SELECT DISTINCT building_name
FROM buildings
  LEFT JOIN employees
    ON building_name = building
WHERE role IS NULL;

## SQL Lesson 9: Queries with expressions

Use expressions in SELECT statements to perform calculations on retrieved data.The use of expressions can save time and extra post-processing of the result data, but can also make the query harder to read, so we recommend that when expressions are used in the SELECT part of the query, that they are also given a descriptive alias using the AS keyword.

**Usage**:Select query with expression aliases

1.
SELECT col_expression AS expr_description, …
FROM mytable;

2.
SELECT column AS better_column_name, …
FROM a_long_widgets_table_name AS mywidgets
INNER JOIN widget_sales
  ON mywidgets.id = widget_sales.widget_id;

---

### Exercise 9:
You are going to have to use expressions to transform the BoxOffice data into something easier to understand for the tasks below.

Table: Movies

| Id  | Title                 | Director         | Year | Length_minutes |
|---- |---------------------- |----------------- |-----| -------------- |
| 1   | Toy Story             | John Lasseter    | 1995| 81             |
| 2   | A Bug's Life          | John Lasseter    | 1998| 95             |
| 3   | Toy Story 2           | John Lasseter    | 1999| 93             |
| 4   | Monsters, Inc.        | Pete Docter      | 2001| 92             |
| 5   | Finding Nemo          | Andrew Stanton   | 2003| 107            |
| 6   | The Incredibles       | Brad Bird        | 2004| 116            |
| 7   | Cars                  | John Lasseter    | 2006| 117            |
| 8   | Ratatouille           | Brad Bird        | 2007| 115            |
| 9   | WALL-E                | Andrew Stanton   | 2008| 104            |
| 10  | Up                    | Pete Docter      | 2009| 101            |
| 11  | Toy Story 3           | Lee Unkrich      | 2010| 103            |
| 12  | Cars 2                | John Lasseter    | 2011| 120            |
| 13  | Brave                 | Brenda Chapman   | 2012| 102            |
| 14  | Monsters University   | Dan Scanlon      | 2013| 110            |

---

Table: Boxoffice

| Movie_id | Rating | Domestic_sales | International_sales |
|----------|--------|-----------------|---------------------|
| 5        | 8.2    | 380,843,261     | 555,900,000         |
| 14       | 7.4    | 268,492,764     | 475,066,843         |
| 8        | 8      | 206,445,654     | 417,277,164         |
| 12       | 6.4    | 191,452,396     | 368,400,000         |
| 3        | 7.9    | 245,852,179     | 239,163,000         |
| 6        | 8      | 261,441,092     | 370,001,000         |
| 9        | 8.5    | 223,808,164     | 297,503,696         |
| 11       | 8.4    | 415,004,880     | 648,167,031         |
| 1        | 8.3    | 191,796,233     | 170,162,503         |
| 7        | 7.2    | 244,082,982     | 217,900,167         |
| 10       | 8.3    | 293,004,164     | 438,338,580         |
| 4        | 8.1    | 289,916,256     | 272,900,000         |
| 2        | 7.2    | 162,798,565     | 200,600,000         |
| 13       | 7.2    | 237,283,207     | -                   |

---

### Exercise 9 — Tasks

1. List all movies and their combined sales in millions of dollars

SELECT title, (domestic_sales + international_sales) / 1000000 AS gross_sales_millions
FROM movies
  JOIN boxoffice
    ON movies.id = boxoffice.movie_id;

2. List all movies and their ratings in percent

SELECT title, rating * 10 AS rating_percent
FROM movies
  JOIN boxoffice
    ON movies.id = boxoffice.movie_id;

3. List all movies that were released on even number years
## SQL Lesson 10: Queries with aggregates (Pt. 1)

SELECT title, year
FROM movies
WHERE year % 2 = 0;
Introduce aggregate functions for summarizing data.

---

## SQL Lesson 10: Queries with aggregates (Pt. 1)

### 10.1 Common aggregate functions

- **Count():** A common function used to count the number of rows in the group if no column name is specified. Otherwise, it counts the number of rows in the group with non-NULL values in the specified column.

- **Count(column):** Counts the number of rows in the group with non-NULL values in the specified column.

- **MIN(column):** Finds the smallest numerical value in the specified column for all rows in the group.

- **MAX(column):** Finds the largest numerical value in the specified column for all rows in the group.

- **AVG(column):** Finds the average numerical value in the specified column for all rows in the group.

- **SUM(column):** Finds the sum of all numerical values in the specified column for the rows in the group.

### 10.2 Grouped aggregate functions

In addition to aggregating across all the rows, you can instead apply the aggregate functions to individual groups of data within that group (ie. box office sales for Comedies vs Action movies).
This would then create as many results as there are unique groups defined as by the GROUP BY clause.

**Usage**:Select query with aggregate functions over groups

SELECT AGG_FUNC(column_or_expression) AS aggregate_description, …
FROM mytable
WHERE constraint_expression
GROUP BY column;

### Exercise 10:

For this exercise, we are going to work with our Employees table. Notice how the rows in this table have shared data, which will give us an opportunity to use aggregate functions to summarize some high-level metrics about the teams. Go ahead and give it a shot.

Table: Employees

| Role     | Name         | Building | Years Employed |
|----------|--------------|----------|----------------|
| Engineer | Becky A.     | 1e       | 4              |
| Engineer | Dan B.       | 1e       | 2              |
| Engineer | Sharon F.    | 1e       | 6              |
| Engineer | Dan M.       | 1e       | 4              |
| Engineer | Malcom S.    | 1e       | 1              |
| Artist   | Tylar S.     | 2w       | 2              |
| Artist   | Sherman D.   | 2w       | 8              |
| Artist   | Jakob J.     | 2w       | 6              |
| Artist   | Lillia A.    | 2w       | 7              |
| Artist   | Brandon J.   | 2w       | 7              |
| Manager  | Scott K.     | 1e       | 9              |
| Manager  | Shirlee M.   | 1e       | 3              |
| Manager  | Daria O.     | 2w       | 6              |

---

Exercise 10 — Tasks

1. Find the longest time that an employee has been at the studio

SELECT MAX(years_employed) as Max_years_employed
FROM employees;

2. For each role, find the average number of years employed by employees in that role

SELECT role, AVG(years_employed) as Average_years_employed
FROM employees
GROUP BY role;

3. Find the total number of employee years worked in each building

SELECT building, SUM(years_employed) as Total_years_employed
FROM employees
GROUP BY building;

---

## SQL Lesson 11: Queries with aggregates (Pt. 2)

Our queries are getting fairly complex, but we have nearly introduced all the important parts of a SELECT query. One thing that you might have noticed is that if the GROUP BY clause is executed after the WHERE clause (which filters the rows which are to be grouped), then how exactly do we filter the grouped rows?

Luckily, SQL allows us to do this by adding an additional HAVING clause which is used specifically with the GROUP BY clause to allow us to filter grouped rows from the result set.

**Usage**:Select query with HAVING constraint

SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, …
FROM mytable
WHERE condition
GROUP BY column
HAVING group_condition;

Exercise

For this exercise, you are going to dive deeper into Employee data at the film studio. Think about the different clauses you want to apply for each task.

Table: Employees

| Role     | Name         | Building | Years Employed |
|----------|--------------|----------|----------------|
| Engineer | Becky A.     | 1e       | 4              |
| Engineer | Dan B.       | 1e       | 2              |
| Engineer | Sharon F.    | 1e       | 6              |
| Engineer | Dan M.       | 1e       | 4              |
| Engineer | Malcom S.    | 1e       | 1              |
| Artist   | Tylar S.     | 2w       | 2              |
| Artist   | Sherman D.   | 2w       | 8              |
| Artist   | Jakob J.     | 2w       | 6              |
| Artist   | Lillia A.    | 2w       | 7              |
| Artist   | Brandon J.   | 2w       | 7              |
| Manager  | Scott K.     | 1e       | 9              |
| Manager  | Shirlee M.   | 1e       | 3              |
| Manager  | Daria O.     | 2w       | 6              |

Exercise — Tasks

1. Find the number of Artists in the studio (without a HAVING clause)

SELECT role, COUNT(*) as Number_of_artists
FROM employees
WHERE role = "Artist";

2. Find the number of Employees of each role in the studio

SELECT role, COUNT(*)
FROM employees
GROUP BY role;

3. Find the total number of years employed by all Engineers

SELECT role, SUM(years_employed)
FROM employees
GROUP BY role
HAVING role = "Engineer";

---

## SQL Lesson 12: Order of execution of a Query

Understand the logical order in which a SQL query is processed.

***Usage**:Complete SELECT query

SELECT DISTINCT column, AGG_FUNC(column_or_expression), …
FROM mytable
    JOIN another_table
      ON mytable.column = another_table.column
    WHERE constraint_expression
    GROUP BY column
    HAVING constraint_expression
    ORDER BY column ASC/DESC
    LIMIT count OFFSET COUNT;

### Exercise 12:

Table: Movies

| Id  | Title                 | Director         | Year | Length (minutes) |
|---- |---------------------- |----------------- |-----| ----------------- |
| 1   | Toy Story             | John Lasseter    | 1995| 81                |
| 2   | A Bug's Life          | John Lasseter    | 1998| 95                |
| 3   | Toy Story 2           | John Lasseter    | 1999| 93                |
| 4   | Monsters, Inc.        | Pete Docter      | 2001| 92                |
| 5   | Finding Nemo          | Andrew Stanton   | 2003| 107               |
| 6   | The Incredibles       | Brad Bird        | 2004| 116               |
| 7   | Cars                  | John Lasseter    | 2006| 117               |
| 8   | Ratatouille           | Brad Bird        | 2007| 115               |
| 9   | WALL-E                | Andrew Stanton   | 2008| 104               |
| 10  | Up                    | Pete Docter      | 2009| 101               |
| 11  | Toy Story 3           | Lee Unkrich      | 2010| 103               |
| 12  | Cars 2                | John Lasseter    | 2011| 120               |
| 13  | Brave                 | Brenda Chapman   | 2012| 102               |
| 14  | Monsters University   | Dan Scanlon      | 2013| 110               |

---

Table: Boxoffice

| Movie_id | Rating | Domestic_sales | International_sales |
|----------|--------|-----------------|----------------------|
| 5        | 8.2    | 380,843,261     | 555,900,000          |
| 14       | 7.4    | 268,492,764     | 475,066,843          |
| 8        | 8.0    | 206,445,654     | 417,277,164          |
| 12       | 6.4    | 191,452,396     | 368,400,000          |
| 3        | 7.9    | 245,852,179     | 239,163,000          |
| 6        | 8.0    | 261,441,092     | 370,001,000          |
| 9        | 8.5    | 223,808,164     | 297,503,696          |
| 11       | 8.4    | 415,004,880     | 648,167,031          |
| 1        | 8.3    | 191,796,233     | 170,162,503          |
| 7        | 7.2    | 244,082,982     | 217,900,167          |
| 10       | 8.3    | 293,004,164     | 438,338,580          |
| 4        | 8.1    | 289,916,256     | 272,900,000          |
| 2        | 7.2    | 162,798,565     | 200,600,000          |
| 13       | 7.2    | 237,283,207     | 301,700,000          |

---

Exercise 12 — Tasks

1. Find the number of movies each director has directed

SELECT director, COUNT(id) as Num_movies_directed
FROM movies
GROUP BY director;

2. Find the total domestic and international sales that can be attributed to each director

SELECT director, SUM(domestic_sales + international_sales) as Cumulative_sales_from_all_movies
FROM movies
    INNER JOIN boxoffice
        ON movies.id = boxoffice.movie_id
GROUP BY director;

## SQL Lesson 13: Inserting rows

Learn how to insert new records into a table.

**Usage**:Insert statement with values for all columns

1. Insert statement with values for all columns

INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;

2. Insert statement with specific columns

INSERT INTO mytable
(column, another_column, …)
VALUES (value_or_expr, another_value_or_expr, …),
      (value_or_expr_2, another_value_or_expr_2, …),
      …;

3. Example Insert statement with expressions

INSERT INTO boxoffice
(movie_id, rating, sales_in_millions)
VALUES (1, 9.9, 283742034 / 1000000);

Exercise 13

In this exercise, we are going to play studio executive and add a few movies to the Movies to our portfolio. In this table, the Id is an auto-incrementing integer, so you can try inserting a row with only the other columns defined.

Since the following lessons will modify the database, you'll have to manually run each query once they are ready to go.

Table: Movies

| Id | Title         | Director       | Year | Length_minutes |
|----|---------------|----------------|------|----------------|
| 1  | Toy Story     | John Lasseter  | 1995 | 81             |
| 2  | A Bug's Life  | John Lasseter  | 1998 | 95             |
| 3  | Toy Story 2   | John Lasseter  | 1999 | 93             |

---

| Movie_id | Rating | Domestic_sales | International_sales |
|----------|--------|-----------------|----------------------|
| 3        | 7.9    | 245,852,179     | 239,163,000          |
| 1        | 8.3    | 191,796,233     | 170,162,503          |
| 2        | 7.2    | 162,798,565     | -                    |

Exercise 13 — Tasks
1. Add the studio's new production, Toy Story 4 to the list of movies (you can use any director)

INSERT INTO movies VALUES (4, "Toy Story 4", "El Directore", 2015, 90);

2. Toy Story 4 has been released to critical acclaim! It had a rating of 8.7, and made 340 million domestically and 270 million internationally. Add the record to the BoxOffice table.

INSERT INTO boxoffice VALUES (4, 8.7, 340000000, 270000000);

---

## SQL Lesson 14: Updating rows

In addition to adding new data, a common task is to update existing data, which can be done using an UPDATE statement. Similar to the INSERT statement, you have to specify exactly which table, columns, and rows to update. In addition, the data you are updating has to match the data type of the columns in the table schema.

**Usage**:Update statement with values

### Exercise 14:

t looks like some of the information in our Movies database might be incorrect, so go ahead and fix them through the exercises below.

Table: Movies

| Id  | Title                 | Director          | Year | Length_minutes |
|----:|:----------------------|:------------------|-----:|---------------:|
| 1   | Toy Story             | John Lasseter     | 1995 | 81             |
| 2   | A Bug's Life          | El Directore      | 1998 | 95             |
| 3   | Toy Story 2           | John Lasseter     | 1899 | 93             |
| 4   | Monsters, Inc.        | Pete Docter       | 2001 | 92             |
| 5   | Finding Nemo          | Andrew Stanton    | 2003 | 107            |
| 6   | The Incredibles       | Brad Bird         | 2004 | 116            |
| 7   | Cars                  | John Lasseter     | 2006 | 117            |
| 8   | Ratatouille           | Brad Bird         | 2007 | 115            |
| 9   | WALL-E                | Andrew Stanton    | 2008 | 104            |
| 10  | Up                    | Pete Docter       | 2009 | 101            |
| 11  | Toy Story 8           | El Directore      | 2010 | 103            |
| 12  | Cars 2                | John Lasseter     | 2011 | 120            |
| 13  | Brave                 | Brenda Chapman    | 2012 | 102            |
| 14  | Monsters University   | Dan Scanlon       | 2013 | 110            |

---

Exercise 14 — Tasks

1. The director for A Bug's Life is incorrect, it was actually directed by John Lasseter

UPDATE movies
SET director = "John Lasseter"
WHERE id = 2;

2. The year that Toy Story 2 was released is incorrect, it was actually released in 1999

UPDATE movies
SET director = "John Lasseter"
WHERE id = 2;

3. Both the title and director for Toy Story 8 is incorrect! The title should be "Toy Story 3" and it was directed by Lee Unkrich

UPDATE movies
SET title = "Toy Story 3", director = "Lee Unkrich"
WHERE id = 11;

---

## SQL Lesson 15: Deleting rows

Explore the process of deleting records from a table.

**Usage**:Delete statement with condition

DELETE FROM mytable
WHERE condition;

### Exercise 15:

DELETE FROM mytable
WHERE condition;

Table: Movies

| Id  | Title                 | Director         | Year | Length_minutes |
|----:|-----------------------|------------------|------|----------------|
| 1   | Toy Story             | John Lasseter    | 1995 | 81             |
| 2   | A Bug's Life          | John Lasseter    | 1998 | 95             |
| 3   | Toy Story 2           | John Lasseter    | 1999 | 93             |
| 4   | Monsters, Inc.        | Pete Docter      | 2001 | 92             |
| 5   | Finding Nemo          | Andrew Stanton   | 2003 | 107            |
| 6   | The Incredibles       | Brad Bird        | 2004 | 116            |
| 7   | Cars                  | John Lasseter    | 2006 | 117            |
| 8   | Ratatouille           | Brad Bird        | 2007 | 115            |
| 9   | WALL-E                | Andrew Stanton   | 2008 | 104            |
| 10  | Up                    | Pete Docter      | 2009 | 101            |
| 11  | Toy Story 3           | Lee Unkrich      | 2010 | 103            |
| 12  | Cars 2                | John Lasseter    | 2011 | 120            |
| 13  | Brave                 | Brenda Chapman   | 2012 | 102            |
| 14  | Monsters University   | Dan Scanlon      | 2013 | 110            |

---

Exercise 15 — Tasks

1. This database is getting too big, lets remove all movies that were released before 2005.

DELETE FROM movies
where year < 2005;

2. Andrew Stanton has also left the studio, so please remove all movies directed by him.

DELETE FROM movies
where director = "Andrew Stanton";

---

## SQL Lesson 16: Creating tables

Understand the basics of creating new tables.

**Usage**:Create table statement w/ optional table constraint and default value

CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);

### Data types in MySQL

1. String data type

| Data Type        | Description                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| CHAR(size)       | A FIXED length string (can contain letters, numbers, and special characters). The size parameter specifies the column length in characters - can be from 0 to 255. Default is 1. |
| VARCHAR(size)    | A VARIABLE length string (can contain letters, numbers, and special characters). The size parameter specifies the maximum column length in characters - can be from 0 to 65535. |
| BINARY(size)     | Equal to CHAR(), but stores binary byte strings. The size parameter specifies the column length in bytes. Default is 1. |
| VARBINARY(size)  | Equal to VARCHAR(), but stores binary byte strings. The size parameter specifies the maximum column length in bytes. |
| TINYBLOB         | For BLOBs (Binary Large OBjects). Max length: 255 bytes.                                                        |
| TINYTEXT         | Holds a string with a maximum length of 255 characters.                                                         |
| TEXT(size)       | Holds a string with a maximum length of 65,535 bytes.                                                            |
| BLOB(size)       | For BLOBs (Binary Large OBjects). Holds up to 65,535 bytes of data.                                             |
| MEDIUMTEXT       | Holds a string with a maximum length of 16,777,215 characters.                                                   |
| MEDIUMBLOB       | For BLOBs (Binary Large OBjects). Holds up to 16,777,215 bytes of data.                                         |
| LONGTEXT         | Holds a string with a maximum length of 4,294,967,295 characters.                                               |
| LONGBLOB         | For BLOBs (Binary Large OBjects). Holds up to 4,294,967,295 bytes of data.                                     |
| ENUM(val1, ...)  | A string object that can have only one value, chosen from a list of possible values. You can list up to 65535 values in an ENUM list. If a value is inserted that is not in the list, a blank value will be inserted. The values are sorted in the order you enter them. |
| SET(val1, ...)   | A string object that can have 0 or more values, chosen from a list of possible values. You can list up to 64 values in a SET list. |

---

2. Numeric Data Types

| Data Type            | Description                                                                                                                                                                                              |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BIT(size)            | A bit-value type. The number of bits per value is specified in size. The size parameter can hold a value from 1 to 64. The default value for size is 1.                                                        |
| TINYINT(size)        | A very small integer. Signed range is from -128 to 127. Unsigned range is from 0 to 255. The size parameter specifies the maximum display width (which is 255).                                              |
| BOOL                 | Zero is considered as false, nonzero values are considered as true.                                                                                                                                         |
| BOOLEAN              | Equal to BOOL.                                                                                                                                                                                               |
| SMALLINT(size)       | A small integer. Signed range is from -32768 to 32767. Unsigned range is from 0 to 65535. The size parameter specifies the maximum display width (which is 255).                                           |
| MEDIUMINT(size)      | A medium integer. Signed range is from -8388608 to 8388607. Unsigned range is from 0 to 16777215. The size parameter specifies the maximum display width (which is 255).                                    |
| INT(size)            | A medium integer. Signed range is from -2147483648 to 2147483647. Unsigned range is from 0 to 4294967295. The size parameter specifies the maximum display width (which is 255).                             |
| INTEGER(size)        | Equal to INT(size).                                                                                                                                                                                         |
| BIGINT(size)         | A large integer. Signed range is from -9223372036854775808 to 9223372036854775807. Unsigned range is from 0 to 18446744073709551615. The size parameter specifies the maximum display width (which is 255). |
| FLOAT(size, d)       | A floating point number. The total number of digits is specified in size. The number of digits after the decimal point is specified in the d parameter. This syntax is deprecated in MySQL 8.0.17 and will be removed in future MySQL versions. |
| FLOAT(p)             | A floating point number. MySQL uses the p value to determine whether to use FLOAT or DOUBLE for the resulting data type. If p is from 0 to 24, the data type becomes FLOAT(). If p is from 25 to 53, the data type becomes DOUBLE(). |
| DOUBLE(size, d)      | A normal-size floating point number. The total number of digits is specified in size. The number of digits after the decimal point is specified in the d parameter.                                          |
| DOUBLE PRECISION(size, d) |                                                                                                                                            |
| DECIMAL(size, d)     | An exact fixed-point number. The total number of digits is specified in size. The number of digits after the decimal point is specified in the d parameter. The maximum number for size is 65. The maximum number for d is 30. The default value for size is 10. The default value for d is 0. |
| DEC(size, d)         | Equal to DECIMAL(size,d).                                                     3. Date and Time Data Types

| Data Type          | Description                                                                                                                                                                                                                                                           |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DATE               | A date. Format: YYYY-MM-DD. The supported range is from '1000-01-01' to '9999-12-31'.                                                                                                                                                                               |
| DATETIME(fsp)      | A date and time combination. Format: YYYY-MM-DD hh:mm:ss. The supported range is from '1000-01-01 00:00:00' to '9999-12-31 23:59:59'. Adding DEFAULT and ON UPDATE in the column definition to get automatic initialization and updating to the current date and time. |
| TIMESTAMP(fsp)     | A timestamp. TIMESTAMP values are stored as the number of seconds since the Unix epoch ('1970-01-01 00:00:00' UTC). Format: YYYY-MM-DD hh:mm:ss. The supported range is from '1970-01-01 00:00:01' UTC to '2038-01-09 03:14:07' UTC. Automatic initialization and updating to the current date and time can be specified using DEFAULT CURRENT_TIMESTAMP and ON UPDATE CURRENT_TIMESTAMP in the column definition. |
| TIME(fsp)          | A time. Format: hh:mm:ss. The supported range is from '-838:59:59' to '838:59:59'.                                                                                                                                                                 |
| YEAR               | A year in four-digit format. Values allowed in four-digit format: 1901 to 2155, and 0000. MySQL 8.0 does not support the year in two-digit format.                                                                                                                   |

---

### Exercise 16 - Tasks:

1. Create a new table named Database with the following columns:
– Name A string (text) describing the name of the database
– Version A number (floating point) of the latest version of this database
– Download_count An integer count of the number of times this database was downloaded

CREATE TABLE Database (
    Name TEXT,
    Version FLOAT,
    Download_count INTEGER
);

## SQL Lesson 17: Altering tables

As your data changes over time, SQL provides a way for you to update your corresponding tables and database schemas by using the ALTER TABLE statement to add, remove, or modify columns and table constraints.

1. Adding columns

**Usage**: Altering table to add new column(s)

ALTER TABLE mytable
ADD column DataType OptionalTableConstraint
    DEFAULT default_value;

2. Removing columns

**Usage**: Altering table to remove column(s)

ALTER TABLE mytable
DROP column_to_be_deleted;

3. Renaming the table

**Usage**: Altering table name

ALTER TABLE mytable
RENAME TO new_table_name;

### Exercise 17:

Table: Movies

| Id  | Title                  | Director          | Year | Length_minutes |
|----|------------------------|-------------------|------|----------------|
| 1  | Toy Story              | John Lasseter     | 1995 | 81             |
| 2  | A Bug's Life           | John Lasseter     | 1998 | 95             |
| 3  | Toy Story 2            | John Lasseter     | 1999 | 93             |
| 4  | Monsters, Inc.         | Pete Docter       | 2001 | 92             |
| 5  | Finding Nemo           | Andrew Stanton    | 2003 | 107            |
| 6  | The Incredibles        | Brad Bird         | 2004 | 116            |
| 7  | Cars                   | John Lasseter     | 2006 | 117            |
| 8  | Ratatouille            | Brad Bird         | 2007 | 115            |
| 9  | WALL-E                 | Andrew Stanton    | 2008 | 104            |
| 10 | Up                     | Pete Docter       | 2009 | 101            |
| 11 | Toy Story 3            | Lee Unkrich       | 2010 | 103            |
| 12 | Cars 2                 | John Lasseter     | 2011 | 120            |
| 13 | Brave                  | Brenda Chapman    | 2012 | 102            |
| 14 | Monsters University    | Dan Scanlon       | 2013 | 110            |

Exercise 17 — Tasks

1. Add a column named Aspect_ratio with a FLOAT data type to store the aspect-ratio each movie was released in.

ALTER TABLE Movies
  ADD COLUMN Aspect_ratio FLOAT DEFAULT 2.39;

2. Add another column named Language with a TEXT data type to store the language that the movie was released in. Ensure that the default for this language is English.

ALTER TABLE Movies
  ADD COLUMN Language TEXT DEFAULT "English";

---

## SQL Lesson 18: Dropping tables

In some rare cases, you may want to remove an entire table including all of its data and metadata, and to do so, you can use the DROP TABLE statement, which differs from the DELETE statement in that it also removes the table schema from the database entirely.

**Usage**:Drop table statement

DROP TABLE IF EXISTS mytable;

**NOTE**: Like the CREATE TABLE statement, the database may throw an error if the specified table does not exist, and to suppress that error, you can use the IF EXISTS clause.


### Exercise 18:

Table: Movies

| Id  | Title                 | Director          | Year | Length_minutes |
|----|-----------------------|-------------------|------|----------------|
| 1  | Toy Story             | John Lasseter     | 1995 | 81             |
| 2  | A Bug's Life          | John Lasseter     | 1998 | 95             |
| 3  | Toy Story 2           | John Lasseter     | 1999 | 93             |
| 4  | Monsters, Inc.        | Pete Docter       | 2001 | 92             |
| 5  | Finding Nemo          | Andrew Stanton    | 2003 | 107            |
| 6  | The Incredibles       | Brad Bird         | 2004 | 116            |
| 7  | Cars                  | John Lasseter     | 2006 | 117            |
| 8  | Ratatouille           | Brad Bird         | 2007 | 115            |
| 9  | WALL-E                | Andrew Stanton    | 2008 | 104            |
| 10 | Up                    | Pete Docter       | 2009 | 101            |
| 11 | Toy Story 3           | Lee Unkrich       | 2010 | 103            |
| 12 | Cars 2                | John Lasseter     | 2011 | 120            |
| 13 | Brave                 | Brenda Chapman    | 2012 | 102            |
| 14 | Monsters University   | Dan Scanlon       | 2013 | 110            |

---

Table: Boxoffice

| Movie_id | Rating | Domestic_sales | International_sales |
|----------|--------|-----------------|---------------------|
| 5        | 8.2    | 380,843,261     | 555,900,000         |
| 14       | 7.4    | 268,492,764     | 475,066,843         |
| 8        | 8      | 206,445,654     | 417,277,164         |
| 12       | 6.4    | 191,452,396     | 368,400,000         |
| 3        | 7.9    | 245,852,179     | 239,163,000         |
| 6        | 8      | 261,441,092     | 370,001,000         |
| 9        | 8.5    | 223,808,164     | 297,503,696         |
| 11       | 8.4    | 415,004,880     | 648,167,031         |
| 1        | 8.3    | 191,796,233     | 170,162,503         |
| 7        | 7.2    | 244,082,982     | 217,900,167         |
| 10       | 8.3    | 293,004,164     | 438,338,580         |
| 4        | 8.1    | 289,916,256     | 272,900,000         |
| 2        | 7.2    | 162,798,565     | 200,600,000         |
| 13       | 7.2    | 237,283,207     | 301,700,000         |

---

Exercise 18 — Tasks

1. We've sadly reached the end of our lessons, lets clean up by removing the Movies table

DROP TABLE Movies;

2. And drop the BoxOffice table as well

DROP TABLE BoxOffice;
