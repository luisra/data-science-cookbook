# SQL to Pandas

#### Shortcuts (in progress...)

| Query  | SQL                                    | Pandas                               |
|--------|----------------------------------------|--------------------------------------|
| Select | SELECT * FROM df                       | df                                   |
| Select | SELECT DISTINCT * FROM df              | df.drop_duplicates()                 |
| Select | SELECT * FROM df LIMIT 5               | df.head()                            |
| Select | SELECT a,b,c FROM df                   | df[['a','b','c']]                    |
| Where  | SELECT * FROM df WHERE a = 1           | df[df['a'] == 1]                     |
| And    | SELECT * FROM df WHERE a = 1 AND b = 2 | df[(df['a'] == 1) & (df['b'] == 2)]  |
| Or     | SELECT * FROM df WHERE a = 1 OR b = 2  | df[(df['a'] == 1)  <code>&#124;</code> (df['b'] == 2)]  |
| Not    | SELECT * FROM df WHERE a != 1          | df[df['a'] != 1]                     |

#### SQL

Interview Prep: https://www.w3schools.com/sql/

Practice Problems: https://www.richardtwatson.com/dm6e/Reader/ClassicModels.html


#### Pandas

Interview Prep:

Practice Problems:
