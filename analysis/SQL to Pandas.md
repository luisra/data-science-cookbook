# SQL to Pandas

#### Shortcuts

| Query           | SQL                                                        | Pandas                                                       |
|-----------------|------------------------------------------------------------|--------------------------------------------------------------|
| Select All      | <code> SELECT * FROM df </code>                                           | <code> df </code>                                                         |
| Select          | <code> SELECT a,b,c FROM df </code>                                   | <code> df[['a','b','c']] </code>                                           |
| Select Distinct | <code> SELECT DISTINCT * FROM df </code>                                  | <code> df.drop_duplicates() </code>                                        |
| Select Top      | SELECT * FROM df LIMIT 5                                   | <code> df.head() </code>                                                    |
| Where           | SELECT * FROM df WHERE a = 1                               | <code> df[df['a'] == 1] </code>                                              |
| And             | SELECT * FROM df WHERE a = 1 AND b = 2                     | <code> df[(df['a'] == 1) & (df['b'] == 2)] </code>                          |
| Or              | SELECT * FROM df WHERE a = 1 OR b = 2                      | <code> df[(df['a'] == 1) <code>&#124;</code> (df['b'] == 2)] </code>                         |
| Not             | SELECT * FROM df WHERE a != 1                              | <code> df[df['a'] != 1] </code>                                            |
| Order By        | SELECT * FROM df ORDER BY a                                | <code> df.sort_values(by=['a'], ascending=True) </code>                    |
| Null            | SELECT * FROM df WHERE a IS NULL                           | <code> df[df['a'].isna()] </code>                                        |
| Not Null        | SELECT * FROM df WHERE a IS NOT NULL                       | <code> df[df['a'].notnull()] </code>                                      |
| Min             | SELECT MIN(a) FROM df                                      | <code> df['a'].min() </code>                                               |
| Max             | SELECT MAX(a) FROM df                                      | <code> df['a'].max() </code>                                               |
| Count           | SELECT COUNT(*) FROM df                                    | <code> df.shape[0] </code>                                                 |
| Average         | SELECT AVG(a) FROM df                                      | <code> df['a'].mean() </code>                                               |
| Sum             | SELECT SUM(a) FROM df                                      | <code> df['a'].sum() </code>                                               |
| In              | SELECT * FROM df WHERE a IN (1,2,3)                        | <code> df[df['a'].isin([1,2,3]) </code>                                    |
| Between         | SELECT * FROM df WHERE a BETWEEN 1 AND 5                   | <code> df[(df['a'] >= 1) & (df['a'] <= 5)] </code>                          |
| Inner Join      | SELECT * FROM df JOIN df_two ON df_two.a = df.a            | <code> pd.merge(df, df_two, how='inner', on='a') </code>                   |
| Left Join       | SELECT * FROM df LEFT JOIN df_two ON df_two.a = df.a       | <code> pd.merge(df, df_two, how='left', left_on='a', right_on='a') </code>  |
| Right Join      | SELECT * FROM df RIGHT JOIN df_two ON df_two.a = df.a      | <code> pd.merge(df, df_two, how='right', left_on='a', right_on='a') </code> |
| Full Outer Join | SELECT * FROM df FULL OUTER JOIN df_two ON df_two.a = df.a | <code> pd.merge(df, df_two, how='outer', on='a') </code>                    |
| Union All       | SELECT a,b,c FROM df UNION ALL SELECT d,e,f FROM df_two    | <code> pd.concat([df, df_two]) </code>                                      |
| Union           | SELECT a,b,c FROM df UNION SELECT d,e,f FROM df_two        | <code> pd.concat([df, df_two]).drop_duplicates() </code>                    |
| Group By        | SELECT a, COUNT(*) FROM df GROUP BY a                      | <code> df.groupby(['a']).size().reset_index(name='count') </code>           |

#### SQL

Interview Prep: https://www.w3schools.com/sql/

Practice Problems: https://www.richardtwatson.com/dm6e/Reader/ClassicModels.html


#### Pandas

Interview Prep:

Practice Problems:
