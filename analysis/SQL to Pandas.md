# SQL to Pandas

#### Shortcuts

| Query           | SQL                                                        | Pandas                                                       |
|-----------------|------------------------------------------------------------|--------------------------------------------------------------|
| Select All      | <code> SELECT * FROM df </code>                                           | <code> df </code>                                                         |
| Select          | <code> SELECT a,b,c FROM df </code>                                   | <code> df[['a','b','c']] </code>                                           |
| Select Distinct | <code> SELECT DISTINCT * FROM df </code>                                  | <code> df.drop_duplicates() </code>                                        |
| Select Top      | <code> SELECT * FROM df LIMIT 5 </code>                                   | <code> df.head() </code>                                                    |
| Where           | <code> SELECT * FROM df WHERE a = 1 </code>                               | <code> df[df['a'] == 1] </code>                                              |
| And             | <code> SELECT * FROM df WHERE a = 1 AND b = 2 </code>                     | <code> df[(df['a'] == 1) & (df['b'] == 2)] </code>                          |
| Or              | <code> SELECT * FROM df WHERE a = 1 OR b = 2 </code>                      | <code> df[(df['a'] == 1) <code>&#124;</code> (df['b'] == 2)] </code>                         |
| Not             | <code> SELECT * FROM df WHERE a != 1 </code>                              | <code> df[df['a'] != 1] </code>                                            |
| Order By        | <code> SELECT * FROM df ORDER BY a </code>                               | <code> df.sort_values(by=['a'], ascending=True) </code>                    |
| Null            | <code> SELECT * FROM df WHERE a IS NULL </code>                           | <code> df[df['a'].isna()] </code>                                        |
| Not Null        | <code> SELECT * FROM df WHERE a IS NOT NULL </code>                       | <code> df[df['a'].notnull()] </code>                                      |
| Min             | <code> SELECT MIN(a) FROM df </code>                                      | <code> df['a'].min() </code>                                               |
| Max             | <code> SELECT MAX(a) FROM df </code>                                      | <code> df['a'].max() </code>                                               |
| Count           | <code> SELECT COUNT(*) FROM df </code>                                    | <code> df.shape[0] </code>                                                 |
| Average         | <code> SELECT AVG(a) FROM df </code>                                      | <code> df['a'].mean() </code>                                               |
| Sum             | <code> SELECT SUM(a) FROM df </code>                                      | <code> df['a'].sum() </code>                                               |
| In              | <code> SELECT * FROM df WHERE a IN (1,2,3) </code>                        | <code> df[df['a'].isin([1,2,3]) </code>                                    |
| Between         | <code> SELECT * FROM df WHERE a BETWEEN 1 AND 5 </code>                   | <code> df[(df['a'] >= 1) & (df['a'] <= 5)] </code>                          |
| Inner Join      | <code> SELECT * FROM df JOIN df_two ON df_two.a = df.a </code>           | <code> pd.merge(df, df_two, how='inner', on='a') </code>                   |
| Left Join       | <code> SELECT * FROM df LEFT JOIN df_two ON df_two.a = df.a </code>      | <code> pd.merge(df, df_two, how='left', left_on='a', right_on='a') </code>  |
| Right Join      | <code> SELECT * FROM df RIGHT JOIN df_two ON df_two.a = df.a </code>      | <code> pd.merge(df, df_two, how='right', left_on='a', right_on='a') </code> |
| Full Outer Join | <code> SELECT * FROM df FULL OUTER JOIN df_two ON df_two.a = df.a </code | <code> pd.merge(df, df_two, how='outer', on='a') </code>                    |
| Union All       | <code> SELECT a,b,c FROM df UNION ALL SELECT d,e,f FROM df_two </code>    | <code> pd.concat([df, df_two]) </code>                                      |
| Union           | <code> SELECT a,b,c FROM df UNION SELECT d,e,f FROM df_two </code>        | <code> pd.concat([df, df_two]).drop_duplicates() </code>                    |
| Group By        | <code> SELECT a, COUNT(*) FROM df GROUP BY a </code>                      | <code> df.groupby(['a']).size().reset_index(name='count') </code>           |

#### SQL

Interview Prep: https://www.w3schools.com/sql/

Practice Problems: https://www.richardtwatson.com/dm6e/Reader/ClassicModels.html


#### Pandas

Interview Prep:

Practice Problems:
