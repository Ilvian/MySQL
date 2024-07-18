### Exercise 3

**Table: World**

| Column Name | Type    |
|-------------|---------|
| name        | varchar |
| continent   | varchar |
| area        | int     |
| population  | int     |
| gdp         | bigint  |

- `name` is the primary key (column with unique values) for this table.
- Each row of this table gives information about the name of a country, the continent to which it belongs, its area, the population, and its GDP value.

**A country is big if:**

1. It has an area of at least three million (i.e., 3000000 km²), or
2. It has a population of at least twenty-five million (i.e., 25000000).

**Write a solution to find the name, population, and area of the big countries.**

Return the result table in any order.

```sql
SELECT name, population, area
FROM World
WHERE area >= 3000000 OR population >= 25000000;
```

- **`SELECT name, population, area`**: Retrieves the `name`, `population`, and `area` columns from the `World` table.
- **`FROM World`**: Specifies the `World` table as the source of data.
- **`WHERE area >= 3000000 OR population >= 25000000`**: Filters the rows to include countries that have an area of at least 3 million km² or a population of at least 25 million.