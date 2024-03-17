## 削除の比較

### レコード(横行)の削除
```sql
DELETE FROM SAMPLE_3_1_1
  WHERE ID = 2 ;
-- ID=2のデータ(レコード)を削除する
```

### カラム(縦列)の削除
```sql
ALTER TABLE SAMPLE_3_1_1
  DROP BIRTH_PLACE ;
-- BIRTH_PLACEというカラムを削除する
```

### すべてのデータの削除（テーブルは残る）
```sql
TRUNCATE SAMPLE_3_1_1 ;
-- SAMPLE_3_1_1 というテーブル内のデータを全て削除する
```

### テーブル自体の削除
```sql
DROP TABLE SAMPLE_3_1_1 ;
-- SAMPLE_3_1_1 というテーブルを削除する
```