## 公式リファレンス
  https://docs.ruby-lang.org/ja/latest/doc/index.html

## absメソッド
  計算結果に対して、常に正の整数を返す

## caseメソッド
  一つの値に対して、複数の値をチェックする場合に使用する。
  if文で書くと、**if value == 1, elsif value == 2, elsif value == 3...** となるケースで使用する。

## 記述例
```ruby
puts '1または2を入力してください'
value = gets.to_i

case value
when 1
  puts 'one'
  <!-- 1のときは、oneを返す -->
when 2
  puts 'two'
  <!-- 2のときは、twoを返す -->
else
  puts "error"
  <!-- それ以外のときは、errorを返す -->
end
```

## if文との違い
if文は、条件に対して**true/false**を返す場合や、比較をする場合に用いる。
if文で**if value == 1, elsif value == 2...** と記述するケースでは、caseの方が可読性が高い。