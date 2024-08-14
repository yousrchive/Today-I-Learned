# VAR FUNCTION

To calculate the required statistics (mean and sample variance) for each subset of the Anscombe's quartet data in the points table, you can use the following SQL query. This query computes the mean and sample variance for both x and y columns, grouped by the quartet column, and rounds the results to three decimal places.

``` sql
SELECT
    p.quartet,
    ROUND(AVG(p.x), 2) AS x_mean,
    ROUND(SUM((p.x - sub.x_mean) * (p.x - sub.x_mean)) / (COUNT(p.x) - 1), 2) AS x_var,
    ROUND(AVG(p.y), 2) AS y_mean,
    ROUND(SUM((p.y - sub.y_mean) * (p.y - sub.y_mean)) / (COUNT(p.y) - 1), 2) AS y_var
FROM
    points p
JOIN
    (SELECT 
        quartet, 
        AVG(x) AS x_mean, 
        AVG(y) AS y_mean 
     FROM points 
     GROUP BY quartet) AS sub
ON p.quartet = sub.quartet
GROUP BY
    p.quartet;
```

On SQLite, function of refering to standard deviation is different with others as PostgreSQL, MySQL.

For MySQL and PostgreSQL,

``` sql
SELECT
    quartet,
    ROUND(AVG(x), 3) AS x_mean,
    ROUND(VAR_SAMP(x), 3) AS x_var,
    ROUND(AVG(y), 3) AS y_mean,
    ROUND(VAR_SAMP(y), 3) AS y_var
FROM
    points
GROUP BY
    quartet;
```

Utilizing the function `VAR_SAMP` is all we have to do to grab the standard deviation.