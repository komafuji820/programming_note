## ifを使わない条件分岐
条件文が、if A == Bである場合、if文よりもcase文を用いた方が可読性が増す。

```ruby
puts '1または2を入力してください'
value = gets.to_i

case value
when 1
  puts 'one'
  # 1のときは、oneを返す
when 2
  puts 'two'
  # 2のときは、twoを返す
else
  puts "error"
  # それ以外のときは、errorを返す
end
```

## これをif文にすると、次の通り
```ruby
puts '1または2を入力してください'
value = gets.to_i

if value == 1
  puts 'one'
elsif value == 2
  puts 'two'
else
  puts "error"
end
```