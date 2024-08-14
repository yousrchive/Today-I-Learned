# WITH grammar and CTE(Common Table Expressions)

The WITH clause in SQL is used to define `Common Table Expressions` (CTEs), which can make complex queries easier to read and write. CTEs are useful for breaking down complicated queries into simpler parts, improving readability, and reusing intermediate results within a query.

``` sql
WITH DailyTips AS (
    SELECT
        day,
        ROUND(SUM(tip), 2) AS tip_daily
    FROM
        WaitersTips
    GROUP BY
        day
)
SELECT
    day,
    tip_daily
FROM
    DailyTips
ORDER BY
    tip_daily DESC
LIMIT 1;
```

To define new table from the original source data,
`WITH` grammar can be called in advance to call `SELECT`

```
WITH {new_table_name} AS (
    SELECT
    FROM
    GROUPBY
)

SELECT
{columns in new_table_name}
FROM 
    {new_table_name}
ORDERBY
    col1 DESC
LIMIT 1;
```

Don't necessarily have to use MAX func;

[Practice Source](https://solvesql.com/problems/best-working-day/)