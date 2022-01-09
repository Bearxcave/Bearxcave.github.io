---
layout:     post
title:      Cheatsheet for PostgreSQL
date:       2022-01-08
author:     Bearx
header-img: img/post-bg-grand-canyon.jpg
catalog: true
tags:
    - cheatsheet
    - postgresql
---

### Cheatsheet for PostgreSQL

* Fundamental:

```
SELECT * FROM table1;
SELECT column1, column2 FROM table1;
SELECT DISTINCT column1 FROM table1;

SELECT AGGREGATION_FUNCTION(*) FROM table1;
SELECT AGGREGATION_FUNCTION(column1) FROM table1;
SELECT AGGREGATION_FUNCTION(column1)/column1 AS new_name_col FROM table1;

SELECT column1, column2 FROM table1
WHERE conditions;

SELECT column1, column2 FROM table1
ORDER BY column1 ASC/DESC
LIMIT number_of_line;

SELECT category_col, AGGREGATION_FUNCTION(data_col) FROM table1
WHERE category_conditions
GROUP BY category_col
HAVING data_aggregation_conditions;
```

* Joins:

```
SELECT columns, table1.column_match, table2.column_match
FROM table1 INNER JOIN table2 ON table1.column_match = table2.column_match;
FROM table1 FULL OUTER JOIN table2 ON table1.column_match = table2.column_match;
FROM table1 FULL OUTER JOIN table2 ON table1.column_match = table2.column_match WHERE table1.id IS null OR table2.id IS null;
FROM table1 LEFT OUTER JOIN/LEFT JOIN table2 ON table1.column_match = table2.column_match;
FROM table1 RIGHT OUTER JOIN/RIGHT JOIN table2 ON table1.column_match = table2.column_match;

SELECT columns FROM table1
UNION
SELECT columns FROM table2;
```

* Operation:

```
AND OR NOT

value >= low AND value <= high
value BETWEEN low AND high
value < low AND value > high
value NOT BETWEEN low AND high

value IN (option1, option2, ...)

string LIKE/ILIKE string_pattern -- ILIKE is case insensitive, string_pattern can be something like '%boy_'
```

* Aggregation function:

```
AVG() COUNT() MAX() MIN() SUM()
```
