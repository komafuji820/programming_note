## 部分テンプレートの呼び出し

### 基本的な書き方
```ruby
# { tweet: tweet } => {部分テンプレート内での変数: 代入したいデータ}
render partial: 'tweet', locals:{ tweet: tweet }
```

### each.doメソッドと一体化した書き方
```ruby
render partial: 'hoge', collection: @hoges

# 次の記載と同じ意味
@hoges.each do |hoge|
  render partial: 'hoge', locals: {hoge: hoge}
end
```

## コントローラーで使用する場合

### redirect_toの代わりに使用する。入力データは、そのまま保持される。
```ruby
render :edit, status: :unprocessable_entity
# unprocessable_entity = 何らかの処理に失敗した場合
```
<!-- 注意 -->
renderを使用する場合、コントローラーのアクションを経由しない。（上記の場合、editコントローラーは呼び出されない）
そのため、render先（views/edit）にデータを渡すには、インスタンス変数を使用しなければならない。