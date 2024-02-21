## slice(slice!)メソッド

### 基本
```ruby
value.slice(1) 
# 戻り値はa。valueの1番目（先頭は0）の文字を返す

value.slice(1, 3)
# 戻り値はalu。valueの1番目の文字から数え始めて3文字を返す

value.slice(-4, 3)
# 戻り値はalu。valueの最後尾から4文字目を起点に、3文字を返す
# 右から左に数えるのではない。例えばueを取得したい場合、value.slice(-1, 2)ではなく、value.slice(-2, 2)とする
```