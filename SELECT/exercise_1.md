### Exercise 1

**Table: Products**

| Column Name | Type    |
|-------------|---------|
| product_id  | int     |
| low_fats    | enum    |
| recyclable  | enum    |

- `product_id` is the primary key (column with unique values) for this table.
- `low_fats` is an ENUM (category) of type ('Y', 'N') where 'Y' means this product is low fat and 'N' means it is not.
- `recyclable` is an ENUM (category) of types ('Y', 'N') where 'Y' means this product is recyclable and 'N' means it is not.

**Write a solution to find the ids of products that are both low fat and recyclable.**

Return the result table in any order.

```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y' AND recyclable = 'Y';
```

- **`SELECT product_id`**: This tells MySQL to retrieve the `product_id` column from the table.
- **`FROM Products`**: Specifies the `Products` table as the source of data.
- **`WHERE low_fats = 'Y' AND recyclable = 'Y'`**: Filters the rows to include only those where `low_fats` is 'Y' and `recyclable` is 'Y'.