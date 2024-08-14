# How to handle STRING Dtype

``` sql
SELECT year,
UPPER(substr(city, 1, 3)) AS city
FROM games
ORDER BY city DESC;
```

Substr receives 3 indicators, which is the name of column that the function is applied to, where it starts, and where it ends. UPPER function let the receivables be upper spellings.

String Functions

`CONCAT()`

Purpose: Concatenates two or more strings.
Example: SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM employees;

`SUBSTR()`

Purpose: Extracts a substring from a string.
Example: SELECT SUBSTR(name, 1, 3) FROM employees;

`LENGTH()`

Purpose: Returns the length of a string.
Example: SELECT LENGTH(name) FROM employees;

Date Functions
`NOW()`

Purpose: Returns the current date and time.
Example: SELECT NOW();

`DATE()`

Purpose: Formats a date.
Example: SELECT DATE(order_date) FROM orders;

`DATE_ADD()`

Purpose: Adds a specified interval to a date.
Example: `SELECT DATE_ADD(order_date, INTERVAL 7 DAY) FROM orders;`

`DATEDIFF()`

Purpose: Calculates the difference between two dates.
Example: SELECT DATEDIFF(CURDATE(), order_date) FROM orders;

`EXTRACT()`

Purpose: Extracts a `specific part of a date, such as year, month, or day.`
Example: SELECT EXTRACT(YEAR FROM order_date) FROM orders;

# Mathematical Functions

`ROUND()`

Purpose: Rounds a number to the nearest integer or specified `decimal` places.
Example: SELECT ROUND(price, 2) FROM products;

`CEIL()`

Purpose: Rounds a number `up` to the `nearest integer`.
Example: SELECT CEIL(price) FROM products;

FLOOR()

Purpose: Rounds a number down to the nearest integer.
Example: SELECT FLOOR(price) FROM products;

`ABS()`

Purpose: Returns the absolute value of a number.
Example: SELECT ABS(discount) FROM products;

`RAND()`

Purpose: Returns a random number between 0 and 1.
Example: SELECT RAND();

# Additional Functions

`GROUP_CONCAT()`

Purpose: Concatenates values from multiple rows into a single string.
Example: SELECT GROUP_CONCAT(product_name) FROM orders GROUP BY customer_id;

COUNT(DISTINCT)

Purpose: Counts the number of unique non-null values.
Example: SELECT COUNT(DISTINCT customer_id) FROM orders;

VARIANCE()

Purpose: Calculates the variance of a set of values.
Example: SELECT VARIANCE(salary) FROM employees;

`STDDEV()`

Purpose: Calculates the standard deviation of a set of values.
Example: SELECT STDDEV(salary) FROM employees;

`TRIM()`

Purpose: Removes leading and trailing spaces from a string.
Example: SELECT TRIM(name) FROM employees;

`REPLACE()`

Purpose: Replaces occurrences of a substring with another substring.
Example: SELECT REPLACE(description, 'old', 'new') FROM products;

`INSTR()`

Purpose: Returns the `position` of a substring within a string.
Example: SELECT INSTR(name, 'abc') FROM products;

`CHAR_LENGTH()`

Purpose: Returns the length of a string.
Example: SELECT CHAR_LENGTH(name) FROM products;

LEFT()

Purpose: Extracts a specified number of characters from the left side of a string.
Example: SELECT LEFT(name, 5) FROM products;

RIGHT()

Purpose: Extracts a specified number of characters from the right side of a string.
Example: SELECT RIGHT(name, 5) FROM products;

YEAR()

Purpose: Extracts the year from a date.
Example: SELECT YEAR(order_date) FROM orders;

MONTH()

Purpose: Extracts the month from a date.
Example: SELECT MONTH(order_date) FROM orders;

DAY()

Purpose: Extracts the day of the month from a date.
Example: SELECT DAY(order_date) FROM orders;

`WEEKDAY()`

Purpose: Returns the day of the week for a date `(0 for Sunday)`.
Example: SELECT WEEKDAY(order_date) FROM orders;

`DATE_FORMAT()`

Purpose: Formats a date according to a specified format.
Example: SELECT `DATE_FORMAT(order_date, '%Y-%m-%d')` FROM orders;

`TIMESTAMPDIFF()`

Purpose: Calculates the difference between two timestamps.
Example: SELECT TIMESTAMPDIFF(DAY, order_date, delivery_date) FROM orders;

# Mathematical Functions

`POW()`

Purpose: Raises a number to a specified power.
Example: SELECT POW(2, 3); (Result: 8)

SQRT()

Purpose: Returns the square root of a number.
Example: SELECT SQRT(16); (Result: 4)

EXP()

Purpose: Returns the exponential value of a number.
Example: SELECT EXP(1); (Result: 2.71828)

LOG()

Purpose: Returns the natural logarithm of a number.
Example: SELECT LOG(10);

SIGN()

Purpose: Returns the sign of a number (-1, 0, 1).
Example: SELECT SIGN(-10); (Result: -1)

# IF

`CASE`

Purpose: Returns a value based on conditions.
Example:
``` sql

SELECT 
    CASE 
        WHEN salary > 5000 THEN 'High'
        WHEN salary BETWEEN 3000 AND 5000 THEN 'Medium'
        ELSE 'Low'
    END AS salary_level
FROM employees;

```

`IFNULL()`

Purpose: Replaces NULL with a specified value.
Example: `SELECT IFNULL(discount, 0) FROM products;`

`COALESCE()`

Purpose: Returns the first non-null value from a list.
Example: SELECT COALESCE(discount, 0, 5) FROM products;

CAST()

Purpose: Converts data to a specified type.
Example: SELECT CAST(price AS DECIMAL(10, 2)) FROM products;

CONVERT()

Purpose: Converts data to a specified type (MySQL-specific).
Example: SELECT CONVERT(price, DECIMAL(10, 2)) FROM products;

RANDOM()

Purpose: Generates a random number.
Example: SELECT RANDOM();

REVERSE()

Purpose: Returns the string in reverse order.
Example: SELECT REVERSE(name) FROM employees; (This function is supported in MySQL.)