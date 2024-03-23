## SELECT文の構造
<!-- 基本の形 -->
```sql
SELECT ID , NAME , GENDER
  FROM SAMPLE_4_1 ;
-- SELECT 抽出したいカラム名 FROM テーブル名
```

<!-- 条件WHERE -->
```sql
SELECT *                -- 全データを抽出するときは、*とする。
  FROM SAMPLE_4_1 ;
  WHERE GENDER = 'M'    -- WHEREで条件を指定する。
    AND AGE > 20 ;
```

<!-- WHERE IN -->
```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE NAME IN ('TARO','JIRO','HANAKO') ;   -- INで、いずれかを含むという意味になる。
/* WHERE NAME = 'TARO'
      OR NAME = 'JIRO'
      OR NAME = 'HANAKO';と同義 */
```

<!-- WHERE NOT IN -->
```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE NAME NOT IN ('TARO','JIRO','HANAKO') ; -- TARO, JIRO, HANAKO "以外"が抽出される。
```

<!-- LIKE -->
```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE NAME LIKE '%O%';  -- 名前に'O'を含むデータが抽出される。%はワイルドカード。
```

<!-- BETWEEN AND -->
```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE AGE BETWEEN 18 AND 20 ;  -- AGEが18以上20以下のデータが抽出される。
```

<!-- IS -->
```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE AGE IS NULL ;  -- NULLのデータを抽出する際には、ISを使用する。
```

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
なお、新しい日付＝大きい数となるため、最新の日付順は降順となる。

<!-- AS -->
```sql
SELECT ID       AS STUDENT_ID       , -- ASによって、抽出後のカラム名を指定できる
       NAME     AS STUDENT_NAME
  FROM SAMPLE_4_1 ;
```

## WHEREで用いる演算子について
NOT > AND > ORの順に見ること。
```sql
SELECT *
  FROM SAMPLE_4_1;
  WHERE GENDER = 'F' AND NOT WEIGHT > 6 OR NOT GENDER = 'F' AND BIRTHDAY > '20120101';
```
これは、次の記述と同義
```sql
SELECT *
  FROM SAMPLE_4_1;
  WHERE (GENDER = 'F' AND ( NOT WEIGHT > 6 )) OR (( NOT GENDER = 'F') AND BIRTHDAY > '20120101');
```