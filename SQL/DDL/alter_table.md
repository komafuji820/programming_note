## alter_tableの記述例

### 修正
<!-- カラムの追加 -->
```sql
ALTER TABLE SAMPLE_3_1_1
  ADD PLACE VARCHAR(15) NOT NULL DEFAULT 'JAPAN' COMMENT '出生地' AFTER WEIGHT ;
-- カラム「PLACE」を「WEIGHT」カラムの後に追加する。空欄不可で、初期値はJAPAN。
-- AFTERで、カラムを追加する場所を指定する。指定しなければ、最後尾に追加される。
-- FIRSTにすると、先頭に追加する。
```

<!-- カラム名の変更(MySQL@8.0以降のみ) -->
```sql
ALTER TABLE SAMPLE_3_1_1
  RENAME COLUMN PLACE TO BIRTH_PLACE ;
-- カラム名をPLACEからBIRTH_PLACEに修正
```

<!-- データの変更(modify)※カラム名を除く -->
```sql
ALTER TABLE SAMPLE_3_1_1
  MODIFY FUR_COLOR VARCHAR(30) DEFAULT 'BROWN' ;
```

<!-- データの変更(change)※カラム名を含む、全てのデータの変更に使用できる -->
```sql
ALTER TABLE SAMPLE_3_1_1
  CHANGE PLACE BIRTH_PLACE VARCHAR(15) NOT NULL DEFAULT 'JAPAN' COMMENT '出生地' ;
-- カラム「PLACE」を「BIRTH_PLACE」に修正する。空欄不可で、初期値はJAPAN。
-- MODIFYやCHANGEでは、*変更しない箇所も含めて記述が必要な点に注意* 記述しないと、NULLで上書きされる。
-- そのため、型の指定は常に必須。
```

### 削除
<!-- カラムの削除 -->
```sql
ALTER TABLE SAMPLE_3_1_1
  DROP BIRTH_PLACE ;
```