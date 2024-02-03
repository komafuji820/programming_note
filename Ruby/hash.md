# ハッシュとは
一つの変数で複数の値を管理するもの。複数の値は、キーとバリューで管理する。

# ハッシュの生成
```ruby
# ハッシュロケット型
student = {:name => '太郎', :height => '170cm', :weight => '65kg'}
# シンボル型
student = {name: '太郎', height: '170cm', weight: '65kg'}
```

# 値の追加
```ruby
student[:age] = '20歳'
# 太郎, 170cm, 65kg, 20歳
```

# 値の取得
```ruby
puts student[:name]
# 太郎が出力される
```

# 値の上書き
```ruby
student[:name] = '次郎'
puts student[:name]
# 次郎が出力される
```