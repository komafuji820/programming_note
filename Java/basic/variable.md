# 変数宣言と代入

## CPUとHDDとメモリの関係
CPU = 頭脳
HDD = 引き出し（保管場所）
メモリ = 机（作業場所）
*変数のデータは、メモリに一時的に保管される*

```java
int price = 1000;
// int => 変数という箱を用意し、データを一時保存するためのメモリを確保する
// 変数名 => 箱（メモリ領域）に名前をつける
```

## 定数の場合
変数（定数）宣言の際に、finalを使用する
```java
final int PRICE = 1000;
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

## リテラル（マジックナンバー）について
データのことをリテラルという。
**リテラルは、"名無しの変数"であり、暗黙的に型が決められている**点に注意。
```java
// 整数
1000          // int型として扱われる
10000000000L  // long型として扱われる
3.5           // double型として扱われる
3.5F          // float型として扱われる
'紫'          // char型として扱われる
"東京"        // String型として扱われる
```

### 自動型変換
リテラルの型と、変数の型が違っていても、自動で型を変換してくれる場合がある。
1. 数値（整数型または小数点数型）であること
2. 変数の型 > リテラルの型であること

### キャスト
```java
long x = 10;
int y = (int)x;
// 変数xはlong型だが、代入の瞬間はint型として扱う
```

### 文字と数値の型変換
``` java
// 文字列→数値
String x = "10";
int y = Integer.parseInt(x);

// 数値→文字列
int x = 10;
String y = String.valueOf(x);
```