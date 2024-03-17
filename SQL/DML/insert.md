## INSERT文

### 記述例
```sql
INSERT INTO SAMPLE_3_1_1 (ID , NAME     , GENDER , BIRTHDAY     , REGIST_TIMESTAMP      )
                  VALUES (1  , 'TARO'   , 'M'    , '2000-01-01' , '2020-08-01 00:00:00' ) ;
```
- not null制約があるカラムを記述していないとエラーになる。
- nullを許容するカラムは、記述していなくてもよい。
- DEFAULTオプションを指定しているカラムは、データが自動設定されるので、記述しなくてもエラーにはならない。

### 複数のデータをinsertするときの注意
```sql
INSERT INTO SAMPLE_3_1_1 (ID , NAME     , GENDER , BIRTHDAY     , REGIST_TIMESTAMP      )
                  VALUES (1  , 'TARO'   , 'M'    , '2000-01-01' ,                       ) 
                  VALUES (2  , 'HANAKO' , 'F'    , '2005-01-01' ,                       ) ;
```
↑複数のデータを1つのinsert文で処理することはできない。
↓必ず、insertとvaluesをセットにする。
```sql
INSERT INTO SAMPLE_3_1_1 (ID , NAME     , GENDER , BIRTHDAY     , REGIST_TIMESTAMP      )
                  VALUES (1  , 'TARO'   , 'M'    , '2000-01-01' ,                       ) ;
INSERT INTO SAMPLE_3_1_1 (ID , NAME     , GENDER , BIRTHDAY     , REGIST_TIMESTAMP      )
                  VALUES (2  , 'HANAKO' , 'F'    , '2005-01-01' ,                       ) ;
```