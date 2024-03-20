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
  WHERE GENDER = 'M'
    AND AGE > 20 ;
-- WHEREで条件を指定する。
```

```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE NAME IN ('TARO','JIRO','HANAKO') ;
-- INで、いずれかを含むという意味になる。
/* WHERE NAME = 'TARO'
      OR NAME = 'JIRO'
      OR NAME = 'HANAKO';と同義 */
```

```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE NAME NOT IN ('TARO','JIRO','HANAKO') ;
-- TARO, JIRO, HANAKO "以外"が抽出される。
```

```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE NAME LIKE '%O%';
-- 名前に'O'を含むデータが抽出される。%はワイルドカード。
```

```sql
SELECT *
  FROM SAMPLE_4_1
 WHERE AGE BETWEEN 18 AND 20 ;
-- AGEが18以上20以下のデータが抽出される。
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