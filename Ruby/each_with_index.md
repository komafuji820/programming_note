## each_with_index
```ruby
def search(target_num, input)
  input.each_with_index do |num, i|
  # この時点で|num, i|には、
  # [0]番目 num=3, [1]番目 num=5, [2]番目 num=9 ,,, のデータが格納される
    if target_num == num
      puts "#{i + 1}番目にあります"
      return
    end
  end
  puts "その数は含まれていません"
end

input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]
def search(3, input)
```