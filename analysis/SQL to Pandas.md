# SQL to Pandas

#### Shortcuts (in progress...)

| Query           | SQL                                                        | Pandas                                                       |
|-----------------|------------------------------------------------------------|--------------------------------------------------------------|
| Select All      | SELECT * FROM df                                           | df                                                           |
| Select          | SELECT a,b,c FROM df                                       | df[['a','b','c']]                                            |
| Select Distinct | SELECT DISTINCT * FROM df                                  | df.drop_duplicates()                                         |
| Select Top      | SELECT * FROM df LIMIT 5                                   | df.head()                                                    |
| Where           | SELECT * FROM df WHERE a = 1                               | df[df['a'] == 1]                                             |
| And             | SELECT * FROM df WHERE a = 1 AND b = 2                     | df[(df['a'] == 1) & (df['b'] == 2)]                          |
| Or              | SELECT * FROM df WHERE a = 1 OR b = 2                      | df[(df['a'] == 1) <code>&#124;</code> (df['b'] == 2)]        |
| Not             | SELECT * FROM df WHERE a != 1                              | df[df['a'] != 1]                                             |
| Order By        | SELECT * FROM df ORDER BY a                                | df.sort_values(by=['a'], ascending=True)                     |
| Null            | SELECT * FROM df WHERE a IS NULL                           | df[df['a'].isna()]                                           |
| Not Null        | SELECT * FROM df WHERE a IS NOT NULL                       | df[df['a'].notnull()]                                        |
| Min             | SELECT MIN(a) FROM df                                      | df['a'].min()                                                |
| Max             | SELECT MAX(a) FROM df                                      | df['a'].max()                                                |
| Count           | SELECT COUNT(*) FROM df                                    | df.shape[0]                                                  |
| Average         | SELECT AVG(a) FROM df                                      | df['a'].mean()                                               |
| Sum             | SELECT SUM(a) FROM df                                      | df['a'].sum()                                                |
| In              | SELECT * FROM df WHERE a IN (1,2,3)                        | df[df['a'].isin([1,2,3])                                     |
| Between         | SELECT * FROM df WHERE a BETWEEN 1 AND 5                   | df[(df['a'] >= 1) & (df['a'] <= 5)]                          |
| Inner Join      | SELECT * FROM df JOIN df_two ON df_two.a = df.a            | pd.merge(df, df_two, how='inner', on='a')                    |
| Left Join       | SELECT * FROM df LEFT JOIN df_two ON df_two.a = df.a       | pd.merge(df, df_two, how='left', left_on='a', right_on='a')  |
| Right Join      | SELECT * FROM df RIGHT JOIN df_two ON df_two.a = df.a      | pd.merge(df, df_two, how='right', left_on='a', right_on='a') |
| Full Outer Join | SELECT * FROM df FULL OUTER JOIN df_two ON df_two.a = df.a | pd.merge(df, df_two, how='outer', on='a')                    |
| Union All       | SELECT a,b,c FROM df UNION ALL SELECT d,e,f FROM df_two    | pd.concat([df, df_two])                                      |
| Union           | SELECT a,b,c FROM df UNION SELECT d,e,f FROM df_two        | pd.concat([df, df_two]).drop_duplicates()                    |

#### SQL

Interview Prep: https://www.w3schools.com/sql/

Practice Problems: https://www.richardtwatson.com/dm6e/Reader/ClassicModels.html


#### Pandas

Interview Prep:

Practice Problems:
