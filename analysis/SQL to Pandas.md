# SQL to Pandas

#### Shortcuts (in progress...)

| Query  | SQL                                    | Pandas                               |
|--------|----------------------------------------|--------------------------------------|
| Select | SELECT * FROM df                       | <code> df </code>                                 |
| Select | SELECT DISTINCT * FROM df              | <code> df.drop_duplicates() </code>                |
| Select | SELECT * FROM df LIMIT 5               | <code> df.head() </code>                           |
| Select | SELECT a,b,c FROM df                   | <code> df[['a','b','c']] </code>                    |
| Where  | SELECT * FROM df WHERE a = 1           | <code> df[df['a'] == 1] </code>                     |
| And    | SELECT * FROM df WHERE a = 1 AND b = 2 | <code> df[(df['a'] == 1) & (df['b'] == 2)] </code>  |
| Or     | SELECT * FROM df WHERE a = 1 OR b = 2  | <code> df[(df['a'] == 1) &#124; (df['b'] == 2)] </code>  |
| Not    | SELECT * FROM df WHERE a != 1          | <code> df[df['a'] != 1] </code>                     |

#### SQL

Interview Prep: https://www.w3schools.com/sql/

Practice Problems: https://www.richardtwatson.com/dm6e/Reader/ClassicModels.html


#### Pandas

Interview Prep:

Practice Problems:
