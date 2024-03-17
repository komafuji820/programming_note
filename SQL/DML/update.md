## UPDATE文

### 記述例
```sql
UPDATE SAMPLE_3_1_1         -- テーブル名
    SET NAME   = 'AIKO' ,   -- データを更新するカラム名・更新後のデータ
      GENDER = 'F'
  WHERE ID     = 1 ;        -- どのデータを更新するかを指定
```