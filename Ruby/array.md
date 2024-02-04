# 配列とは
一つの変数で複数の値を管理するもの。複数の値は、順番（添え字）で管理する。

# 配列の生成
```ruby
pencil_case = ['ペン', '消しゴム', '定規']
```

# 値の追加
```ruby
pencil_case << 'えんぴつ'
# ペン、消しゴム、定規、えんぴつ
```

# 値の取得
```ruby
puts pencil_case[0]
# ペンが出力される
```

# 値の上書き
```ruby
pencil_case[0] = '修正テープ'
puts pencil_case[0]
# 修正テープが出力される
```