## SELECT文の構造
```sql
SELECT ID , NAME , GENDER
  FROM SAMPLE_4_1 ;
-- SELECT 抽出したいカラム名 FROM テーブル名
```

```sql
SELECT *
  FROM SAMPLE_4_1 ;
-- 全データを抽出するときは、*とする。
```

```sql
SELECT ID       AS STUDENT_ID       , 
       NAME     AS STUDENT_NAME
  FROM SAMPLE_4_1 ;
-- ASによって、抽出後のカラム名を指定できる
```
