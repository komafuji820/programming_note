## 演算子

### ++について
1. 変数名++
```java
int number5 = 5;
int answer = number5++;
// 1 まずanswerに5が代入される
// 2 その後、number5に1が加算される
System.out.println(answer);
// よって、answerの値は5
System.out.println(number5);
// number5の値は6
```

2. ++変数名
```java
int number5 = 5;
int answer = ++number5;
// 1 まずnumber5に1が加算される
// 2 その後、answerにnumber5が代入される
System.out.println(answer);
// よって、answerの値は6
System.out.println(number5);
// number5の値も6
```

*++が前にあれば変数への加算を先に行い、++があとにあれば、変数への加算を後から行う！*

3. +1との違い
```java
int number5 = 5;
int answer = ++number5;
// こちらは、number5の値が6になった上で代入されている ＝> number5の中身が置き換わっている

int number5 = 5;
int answer = number5 + 1;
// こちらは、number5の値は5のままで、+1された数字が代入されている ＝> number5は5のまま
```

4. 代入演算子との違い
```java
int number5 = 5;
number5 += 10;
System.out.println(number5);
// number5の値は15
```