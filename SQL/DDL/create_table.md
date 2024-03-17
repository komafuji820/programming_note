## create_tableの記述例
```sql
CREATE TABLE SAMPLE (
  ID                INT          NOT NULL PRIMARY KEY                 COMMENT 'ID'       ,
  NAME              VARCHAR(30)  NOT NULL                             COMMENT '名前'      ,
  GENDER            CHAR(1)      NOT NULL                             COMMENT '性別'      ,
  BIRTHDAY          DATE         NOT NULL                             COMMENT '生年月日'   ,
  WEIGHT            DECIMAL(4,1)                                      COMMENT '体重'      ,
  REGIST_TIMESTAMP  DATETIME     NOT NULL DEFAULT CURRENT_TIMESTAMP   COMMENT '登録日時' 
);
```

- DEFAULTオプション
データの入力がない場合は、自動的にDEFAULTで設定した値が入力される。
上記の場合は、CURRENT_TIMESTAMPのデータが自動で設定される。