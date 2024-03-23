## SELECT文の構造

### 例文
```sql
SELECT SCHOOL_NAME AS SCHOOL_NAME   ,
       MAX(SCORE)  AS HIGH_SCORE    ,
       AVG(SCORE)  AS AVERAGE_SCORE
  FROM SAMPLE_4_4
WHERE SCHOOL_NAME IS NOT NULL
GROUP BY SCHOOL_NAME
HAVING COUNT(*) >= 3
ORDER BY HIGH_SCORE DESC , AVERAGE_SCORE DESC , SCHOOL_NAME ;
```

*関数について*
GROUP BYで絞り込んだデータに対して関数を適用する。
例えば、MAX(SCORE)は、①groupAの中での最高点、②groupBの中での最高点、③groupCの中での最高点を計算する。
同様に、COUNT(*)も、①groupAのレコード数、②groupBのレコード数、③groupCのレコード数を計算する。
そのため、groupAの生徒数が5人、Bが2人、Cが3人だった場合、レコード数は5,2,3となるため、count(*) >=3 の結果は、A・Cとなる。

### SELECT文の処理順序
FROM → WHERE → GROUP BY → 関数(COUNT, MAX, AVG...) → HAVING → SELECT → ORDER BY

### 処理順序が与える影響
- ASで指定したカラム名は、ORDER BYでは使用できるが、WHEREでは使用できない。
- 関数を利用した絞り込みは、WHEREでは使用できない。（そのためにHAVINGがある）

### WHEREとHAVING
WHERE：FROM句のテーブルのレコードを絞り込む場所（不要なデータは先に排除する）
HAVING：GROUP BYで集約したデータを絞り込む場所