## 変数宣言と代入

## CPUとHDDとメモリの関係
CPU = 頭脳
HDD = 引き出し（保管場所）
メモリ = 机（作業場所）
*変数のデータは、メモリに一時的に保管される*

```java
int price = 1000
// int => 変数という箱を用意し、データを一時保存するためのメモリを確保する
// 変数名 => 箱（メモリ領域）に名前をつける
```

## 定数の場合
変数（定数）宣言の際に、finalを使用する
```java
final int PRICE = 1000
// finalを使用し、すべて大文字で記述する
```

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