<!-- ORDER BY -->
```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE GENDER = 'M'
 ORDER BY BIRTHDAY DESC;  -- ORDER BY で、データの並び替えを行う。DESC=降順。特に指定しなければ昇順となる。
```

*昇順と降順*
昇順 = 0→10, A→Z, あ→ん
降順 = 10→0, Z→A, ん→あ
なお、新しい日付＝大きい数なので、最新の日付順＝降順