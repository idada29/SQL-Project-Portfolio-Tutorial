# <p align="center" style="margin-top: 0px;">  **`SQL Project Portfolio Tutorial`** 🏚️
## <p align="center"> Data Analysis

``` sql
-- ============================================================================
--	Question 1  What is the total amount each customer spent at the restaurant?
-- ============================================================================
SELECT
   A.customer_id,
   SUM(B.price) AS total_sales
FROM Case1_sales A
LEFT JOIN Case1_menu B 
ON A.product_id = B.product_id
GROUP BY
  A.customer_id;

``` 
| customer_id | total_sales  |
|-------------|--------------|
|      A      |      76      |
|      B      |      74      |
|      C      |      36      |


-- ============================================================================
--	Question 2  How many days has each customer visited the restaurant?
-- ============================================================================
 
```sql
SELECT 
  customer_id, 
  COUNT(DISTINCT order_date) AS visit_count
FROM case1_sales
GROUP BY customer_id;
```
| customer_id | visit_count |
|-------------|-------------|
|      A      |      4      |
|      B      |      6      |
|      C      |      2      |

