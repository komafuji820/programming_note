# for文

## 基本構造
```java
for(繰り返しの条件){
  繰り返し処理
}
```

### 繰り返し条件
```java
for(int i = 0; i < 4; i++)
// 初期設定
// カウンタ変数iを変数宣言する

// 実行条件
// i < 4 がtrueであれば、繰り返し処理を実行する

// 継続処理
// 処理完了後、iに1を加算する
// なお、前置（++i）でも結果は変わらない。通常は、後置(i++)を使用する
```

###  for文の処理手順
1. 最初の処理
  初期設定(カウンタ変数)を読み込む→条件式がtrueかどうかを判定する→処理を実行
2. 2回目以降
  継続処理(i++)を実行する→条件式がtrueかどうかを判定する→処理を実行

### 記述例1
```java
class test {
	public static void main (String[] args) {

    int count = 0;

    for(int i = 0; i < 4; i++){
      count += 1;
      System.out.println(count);
    }
  }
}
```

### 記述例2
```java
class test {
	public static void main (String[] args) {

    String[] animals = {"こぶた", "たぬき", "きつね"};

    for(int i = 0; i < animals.length; i++){
      System.out.println(animals[i]);
    }
  }
}
```