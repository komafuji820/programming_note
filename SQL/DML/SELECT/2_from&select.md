## FROM句
```sql
SELECT ID , NAME , GENDER
  FROM SAMPLE_4_1 ;
-- SELECT 抽出したいカラム名 FROM テーブル名
```

<!-- AS -->
```sql
SELECT ID       AS STUDENT_ID       , -- ASによって、抽出後のカラム名を指定できる
       NAME     AS STUDENT_NAME
  FROM SAMPLE_4_1 ;
```