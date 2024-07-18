### Exercise 2

**Table: Customer**

| Column Name | Type    |
|-------------|---------|
| id          | int     |
| name        | varchar |
| referee_id  | int     |

- `id` is the primary key column for this table.
- Each row of this table indicates the id of a customer, their name, and the id of the customer who referred them.

**Find the names of the customers that are not referred by the customer with id = 2.**

Return the result table in any order.

```sql
SELECT name
FROM Customer
WHERE referee_id != 2 OR referee_id IS NULL;
```

- **`SELECT name`**: This retrieves the `name` column from the `Customer` table.
- **`FROM Customer`**: Specifies the `Customer` table as the source of data.
- **`WHERE referee_id != 2 OR referee_id IS NULL`**: Filters the rows to include customers whose `referee_id` is not 2, or where `referee_id` is `NULL` (i.e., they were not referred by anyone).