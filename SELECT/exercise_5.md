### Exercise 5

**Table: Tweets**

| Column Name | Type    |
|-------------|---------|
| tweet_id    | int     |
| content     | varchar |

- `tweet_id` is the primary key (column with unique values) for this table.
- This table contains all the tweets in a social media app.

**Write a solution to find the IDs of the invalid tweets. The tweet is invalid if the number of characters used in the content of the tweet is strictly greater than 15.**

Return the result table in any order.

```sql
SELECT tweet_id
FROM Tweets
WHERE LENGTH(content) > 15;
```

- **`SELECT tweet_id`**: Retrieves the `tweet_id` column from the `Tweets` table.
- **`FROM Tweets`**: Specifies the `Tweets` table as the source of data.
- **`WHERE LENGTH(content) > 15`**: Filters the rows to include only those where the length of the `content` column exceeds 15 characters.