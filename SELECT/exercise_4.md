### Exercise 4

**Table: Views**

| Column Name | Type    |
|-------------|---------|
| article_id  | int     |
| author_id   | int     |
| viewer_id   | int     |
| view_date   | date    |

- There is no primary key (column with unique values) for this table; the table may have duplicate rows.
- Each row of this table indicates that some viewer viewed an article (written by some author) on some date. Note that equal `author_id` and `viewer_id` indicate the same person.

**Write a solution to find all the authors that viewed at least one of their own articles.**

Return the result table sorted by id in ascending order.

```sql
SELECT DISTINCT author_id AS id
FROM Views
WHERE author_id = viewer_id
ORDER BY author_id;
```

- **`SELECT DISTINCT author_id AS id`**: Retrieves unique `author_id` values from the `Views` table and renames the column to `id`.
- **`FROM Views`**: Specifies the `Views` table as the source of data.
- **`WHERE author_id = viewer_id`**: Filters the rows to include only those where the `author_id` is the same as the `viewer_id` (i.e., the author viewed their own article).
- **`ORDER BY author_id`**: Sorts the result by `author_id` in ascending order.