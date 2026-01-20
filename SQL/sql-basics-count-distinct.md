# SQL Exercises – COUNT() and DISTINCT

This document contains SQL practice exercises focused on the use of `COUNT()` and `DISTINCT`, completed on DataCamp and documented for learning and portfolio purposes.

---

## SQL Exercise – COUNT()

### Question
What does the following query return?

```sql
SELECT COUNT(film_id) AS count_film_id
FROM reviews;

Correct Answer

The number of records containing a film_id.

Explanation

COUNT(column_name) counts non-NULL values in that column.

It does not count unique values (that would require COUNT(DISTINCT film_id)).

It does not sum values (that would be SUM(film_id)).

It may differ from COUNT(*) if the column contains NULLs.

Key Takeaways

COUNT(*) → total number of rows in a table

COUNT(column) → number of non-NULL values

COUNT(DISTINCT column) → number of unique non-NULL values

SQL Exercise – COUNT() Practice
1️⃣ Total records in people
SELECT COUNT(*) AS count_records
FROM people;

2️⃣ Records with birthdate in people
SELECT COUNT(birthdate) AS count_birthdate
FROM people;

3️⃣ Records for languages and countries in films
SELECT 
  COUNT(language) AS count_languages,
  COUNT(country) AS count_countries
FROM films;

Learning Summary

COUNT(*) counts all rows

COUNT(column) ignores NULL values

Multiple COUNT() functions can be used in the same query

SQL Exercise – SELECT DISTINCT (DataCamp)
Context

Query results may contain duplicate values. The DISTINCT keyword is used to return or count unique values from a column.

Instruction 1/2

Return the unique countries represented in the films table.

SELECT DISTINCT country
FROM films;

Instruction 2/2

Return the number of unique countries represented in the films table.

SELECT COUNT(DISTINCT country) AS count_distinct_countries
FROM films;

Final Notes

DISTINCT is used to eliminate duplicate values

COUNT(DISTINCT column) is useful for counting categories such as country, language, or genre

Exercises completed on DataCamp and documented for continuous learning
