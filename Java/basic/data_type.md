## 変数の型
メモリの容量に応じて型が用意されている。
基本的に、整数はint, 小数点数はdoubleを使用する。

### 整数
- byte
- short
- int（21億まで）
- long（21億以上）

### 小数点数
- float
- double

### 文字
- char（1文字）
- string（文字列）

### 論理値
- boolean（true/false）

### 記述例
```java
int itIndustrylifetimeWage = 276000000;

long itIndustryMarketSize = 1355000000000L;
// longは21億以上の場合に、"L"とセットで使用する

char favoriteKanji = '紫';
// charはシングルクオテーションとセットで使用する

String dreamJob = "エンジニア";
// Stringはダブルクオテーションとセットで使用する

boolean ispreviousGraduate = true;
// booleanは、変数名にisを付ける
```