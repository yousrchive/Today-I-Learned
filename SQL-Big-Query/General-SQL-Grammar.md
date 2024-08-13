## General SQL Grammars

**Google SQL**

`SELECT`, `FROM`, `WHERE`

SELECT : columns to print out
Col1 AS new_name `*alias`
FROM Dataset.Table
WHERE : wanted `condition`
Col1 = 1

``` sql
SELECT *
FROM basic.pokemon
WHERE
type1 = "Fire"
```

**In case of dataset with big rows, selecting * is expense-consuming, not recommended.**

``` sql

SELECT *
EXCEPT {제외할 컬럼}

```
**`EXCEPT` frequently used with `JOIN`**

## Practice

``` sql
SELECT
* EXCEPT(eng_name)
FROM basic.pokemon AS p1
#projectid-dataset-table # If project is single, not needed
#Might be possible without
#alias without ''
WHERE 
type1 = 'Fire' or type2 = 'Fire'
ORDER BY id;

# You need to have a purpose for using the data to determine which parts to output
# Think carefully about the purpose
```

**Writing well-readable query does matter for collaboration**

`;` divides each cell, outcomes come as many as `;`

## Internal Order of Query Engine

**FROM > WHERE > SELECT**


## Summation and Grouping

Summation and Calculation
Calculation by Group

Including **Plus, Minus, Min, Max, Avg, Count**



