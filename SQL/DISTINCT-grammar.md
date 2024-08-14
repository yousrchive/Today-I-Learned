# DISTINCT-grammar

To see the distinct values of the quartet column in the points table, use the DISTINCT keyword in a SELECT statement. 


``` sql
SELECT DISTINCT quartet
FROM points;
```

This is how you can see values of a specific column

``` sql
SELECT 
  seller_id, 
  count(DISTINCT(order_id)) orders
FROM olist_order_items_dataset
GROUP BY seller_id
HAVING count(DISTINCT(order_id)) >= 100
```

To calculate count of total orders, it is necessary to use DISTINCT function as well. In case of many firms having order datasets, it is normal to divide the same orders into the distinct and different products. 