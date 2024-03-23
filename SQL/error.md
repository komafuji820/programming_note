## エラー文まとめ

- 一度実行したスクリプトに、SQL文を*書き足して*実行すると、元々存在していたSQLが再度実行されるため、エラーが発生する。
```sql
Duplicate entry '1' for key 
'PRIMARY'
-- 主キー'1'が重複している
```

- グループ化した場合に、グループ化できないデータをSELECTしようとすると、エラーが発生する。
```sql
Expression #4 of SELECT list is not in GROUP BY clause and contains nonaggregated column 'test_db.SAMPLE_4_4.STUDENT_NAME' which is not functionally dependent on columns in GROUP BY clause; this is incompatible with sql_mode=only_full_group_by
```