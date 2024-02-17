# クラスとインスタンス

## クラス
設計図のようなもの

## インスタンス
クラスを元にして作られる実体のこと

## クラス変数
クラスから作成されたすべてのインスタンスで共有される変数のこと

### 記述例
```ruby
class Dog
  @@type = '犬'
  # def ~ endで囲む必要がない
  # 一番最初に定義する
end
```

## インスタンス変数
インスタンスが持つ属性を定義する変数

## クラスメソッド
クラス自身が使用できるメソッド

### 記述例
```ruby
class Dog
  def self.say
    puts 'ワンワン'
  end
end
```

## インスタンスメソッド
「インスタンスメソッドを定義したクラス」から生成されるインスタンスが使用できるメソッド
インスタンス変数はもちろん、クラス変数も使用できる。

## 記述例
```ruby
class Dog
  @@type = "犬" 
  # クラス変数の定義

  def initialize
    @name = "マロン"
    @dog_type = "トイプードル"
  end
  # インスタンス変数の定義

  def self.say
    puts "ワンワン"
  end
  # クラスメソッドの定義

  def say_type
    puts "わたしは#{@@type}です"
  end
  # インスタンスメソッドの定義
  # クラス変数が使える

  def self_introduction
    puts "わたしの名前は#{@name}で種類は#{@dog_type}"
  end
  # インスタンスメソッドの定義
  # インスタンス変数が使える
end

dog = Dog.new
# インスタンスの生成
Dog.say
# クラスメソッドの実行
dog.say_type
dog.self_introduction
# インスタンスメソッドの実行
```