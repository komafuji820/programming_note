# クラスとインスタンス

## インスタンス
クラスを元にして作られるデータのこと

## インスタンスメソッド
「インスタンスメソッドを定義したクラス」から生成されるインスタンスが使用できるメソッド

## インスタンス変数
インスタンスが持つ属性を定義する変数

## クラスメソッド
クラス自身が使用できるメソッド

## 記述例
```ruby
class Fruit

  # クラスメソッドの定義
  def self.flesh
    puts '採れたて新鮮な果実です'
  end
 
  # インスタンス変数の定義
  def initialize(name, price)
    @name = name
    @price = price
  end
 
  # インスタンスメソッドの定義
  def introduce
    puts "#{@name}は#{@price}円です"
  end
end

# インスタンスの生成
apple = Fruit.new('リンゴ', 120)
orange = Fruit.new('オレンジ', 200)
strawbery = Fruit.new('いちご', 60)

# クラスメソッドの呼び出し
Fruit.flesh

# インスタンスメソッドの呼び出し
apple.introduce
orange.introduce
strawbery.introduce
```