<!-- COUNT -->
```sql
SELECT COUNT(*) , COUNT(STUDENT_ID)
  FROM SAMPLE_4_2 ;
```

<!-- SUM, AVG, MAX, MIN -->
```sql
SELECT SUM(POINT) ,
       AVG(POINT) ,
       MAX(POINT) ,
       MIN(POINT)
  FROM SAMPLE_4_1 ;
```

<!-- DISTINCT -->
重複を除いたデータを取得する
```sql
SELECT DISTINCT GENDER
  FROM SAMPLE_4_1 ;
-- 男・女とだけ抽出される
```

<!-- COUNT & DISTINCT -->
重複を除いたデータの、データ数をカウントする
```sql
SELECT COUNT( DISTINCT GENDER )
  FROM SAMPLE_4_1 ;
-- 「2」（男・女）が出力される
```