## 戻り値はどこに格納されるか？
戻り値は、メソッドを呼び出す記述に格納される。
```ruby
def calc(num1, num2)
  return num1 + num2
end

sum = calc(10, 25)
# 戻り値(35)は、"calc(10, 25)"に格納され、変数sumに代入されている。
puts("合計 = " + sum.to_s)
# 戻り値を再度変数に代入することで、スコープ外で戻り値を使うことができる。
```

## 戻り値を複数設定する場合
変数を複数用意する。このとき、returnで戻り値を明示しないと、最後の戻り値しか返されない点に注意。
```ruby
def slice_num(input)
  tens_place = input / 10 % 10
  ones_place = input % 10
  return tens_place, ones_place
  # 二つの戻り値を明示
end

tens_place, ones_place = slice_num(input)
```