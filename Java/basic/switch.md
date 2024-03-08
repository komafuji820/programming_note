## switch文

### 記述例
```java
int num = Integer.parseInt(args[0]);
// コマンドライン引数を受け取る
switch (num){

  case 1:
    System.out.println("おいしい");
    break;
  // コマンドライン引数が1の場合

  case 2:
    System.out.println("普通");
    break;

  case 3:
    System.out.println("まずい");
    break;

  default:
    System.out.println("不正な値です");
    break;
  // 上記に当てはまらない場合
}
```

### なぜbreakと書くのか？
breakを書かないと、該当するcaseが呼び出されたあと、次以降のcaseが順次処理される。
上の例でコマンドライン引数に3を指定すると、3とdefaultが実行される。