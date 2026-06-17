# SQL & Database Querying Mission

## Student Name: Deepika S

## Overview
This project demonstrates SQL concepts including SELECT, WHERE, ORDER BY, Aggregate Functions, GROUP BY, HAVING, INNER JOIN, LEFT JOIN, RIGHT JOIN, Subqueries, and CASE Statements using movie and box office datasets.
SQL & Database Querying Mission

Query 1 - SELECT

SQL:
SELECT * FROM movies;

Documentation:
This query retrieves all columns and rows from the movies table. It is used to view the complete dataset and understand the available movie information.

Result:
Displays all movie records including ID, title, director, release year, and duration.

---

Query 2 - WHERE

SQL:
SELECT * FROM movies WHERE year > 2005;

Documentation:
This query filters the movie records based on a condition. Only movies released after the year 2005 are displayed.

Result:
Displays movies released after 2005.

---

Query 3 - ORDER BY

SQL:
SELECT title, year FROM movies ORDER BY year ASC;

Documentation:
This query sorts the movie records in ascending order of release year. It helps in analyzing movies chronologically.

Result:
Displays movies arranged from oldest to newest release year.

---

Query 4 - COUNT

SQL:
SELECT COUNT(*) AS TotalMovies FROM movies;

Documentation:
This query uses the COUNT aggregate function to determine the total number of movies available in the table.

Result:
Displays the total count of movies.

---

Query 5 - AVG

SQL:
SELECT AVG(length_minutes) FROM movies;

Documentation:
This query calculates the average duration of all movies using the AVG aggregate function.

Result:
Displays the average movie length in minutes.

---

Query 6 - GROUP BY

SQL:
SELECT director, COUNT(*) FROM movies GROUP BY director;

Documentation:
This query groups movies according to their directors and counts how many movies each director has directed.

Result:
Displays each director along with the number of movies directed.

---

Query 7 - HAVING

SQL:
SELECT director, COUNT() FROM movies GROUP BY director HAVING COUNT() > 1;

Documentation:
This query filters grouped results using the HAVING clause. It displays only directors who have directed more than one movie.

Result:
Displays directors with multiple movies.

---

Query 8 - INNER JOIN

SQL:
SELECT movies.title, boxoffice.rating FROM movies INNER JOIN boxoffice ON movies.id = boxoffice.movie_id;

Documentation:
This query combines data from the movies and boxoffice tables using INNER JOIN. Only matching records from both tables are displayed.

Result:
Displays movie titles along with their ratings.

---

Query 9 - LEFT JOIN

SQL:
SELECT movies.title, boxoffice.rating FROM movies LEFT JOIN boxoffice ON movies.id = boxoffice.movie_id;

Documentation:
This query returns all records from the movies table and matching records from the boxoffice table. If no match exists, NULL values are returned.

Result:
Displays all movies and their ratings where available.

---

Query 10 - RIGHT JOIN

SQL:
SELECT movies.title, boxoffice.rating FROM movies RIGHT JOIN boxoffice ON movies.id = boxoffice.movie_id;

Documentation:
This query returns all records from the boxoffice table and matching records from the movies table. It is useful for identifying box office records even if movie details are unavailable.

Result:
Displays all box office entries with corresponding movie titles.

---

Query 11 - SUM

SQL:
SELECT SUM(domestic_sales) FROM boxoffice;

Documentation:
This query calculates the total domestic sales revenue of all movies using the SUM aggregate function.

Result:
Displays the total domestic sales amount.

---

Query 12 - Subquery

SQL:
SELECT title FROM movies WHERE year >(SELECT AVG(year) FROM movies);

Documentation:
This query uses a subquery to calculate the average release year and then retrieves movies released after that average year.

Result:
Displays movies released later than the average release year.

---

Query 13 - CASE Statement

SQL:
SELECT title,rating,CASE WHEN rating >= 8 THEN 'Excellent' WHEN rating >= 7 THEN 'Good' ELSE 'Average' END AS Category FROM movies INNER JOIN boxoffice ON movies.id = boxoffice.movie_id;

Documentation:
This query uses the CASE statement to classify movies into categories based on their ratings. It helps in creating meaningful labels from numeric values.

Result:
Displays movie titles, ratings, and their corresponding rating category (Excellent, Good, or Average).

---

Conclusion

This project demonstrates the use of SQL concepts such as SELECT, WHERE, ORDER BY, Aggregate Functions (COUNT, SUM, AVG), GROUP BY, HAVING, INNER JOIN, LEFT JOIN, RIGHT JOIN, Subqueries, and CASE Statements. These queries were executed to analyze movie and box office data and understand relational database operations.
