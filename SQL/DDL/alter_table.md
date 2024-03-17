## alter_tableの記述例

### 修正
```sql
-- カラムの追加
ALTER TABLE SAMPLE_3_1_1
  ADD PLACE VARCHAR(15) NOT NULL DEFAULT 'JAPAN' COMMENT '出生地' AFTER WEIGHT ;
```
- AFTERを書かない場合、最後尾に追加する
- AFTERではなく、FIRSTにすると、先頭に追加する

```sql
-- カラム名の変更(MySQL@8.0以降のみ)
ALTER TABLE SAMPLE_3_1_1
  RENAME COLUMN PLACE TO BIRTH_PLACE ;

-- カラム名以外のデータを変更できる(modify)
ALTER TABLE SAMPLE_3_1_1
  MODIFY FUR_COLOR VARCHAR(30) DEFAULT 'BROWN' ;

-- 全てのデータを変更できる(change)
ALTER TABLE SAMPLE_3_1_1
  CHANGE PLACE BIRTH_PLACE VARCHAR(15) NOT NULL DEFAULT 'JAPAN' COMMENT '出生地' ;
```
- MODIFYやCHANGEでは、*変更しない箇所も含めて*記述が必要。記述しなかった箇所はNULLとなってしまう。
- そのため、たとえ変更がなくても、型の指定が必須。

### 削除
```sql
ALTER TABLE SAMPLE_3_1_1
  DROP BIRTH_PLACE ;
```