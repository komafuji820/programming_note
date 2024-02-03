# ブランチの名前を修正する

## ローカルブランチ
```sh
# 基本
git branch -m 古いブランチ名 新しいブランチ名

# 現在のブランチ名を変更するだけなら、下記だけでも良い。
git branch -m 新しいブランチ名
```

## リモートブランチ
- ローカルのブランチ名を変更後、下記を実行
```sh
# 変更後のローカルブランチをpush(Git Hub Desktopではなく、コマンドから行うこと)
git push -u origin 現在のブランチ名


# pushしようとして、パスワード不正エラーが出た場合は次へ
Invalid username or password.

# 変更前のリモートブランチを削除
git push origin :リモートのブランチ名
```

## Invalid username or password.について
- 対処法
1. アクセストークンを発行
Setting → Developer Settings → Personal access tokens → Tokens(classic)
2. ローカルブランチをpush
```sh
git push -u origin 現在のブランチ名
```
3. ユーザー名とトークンを入力を求められるので、入力
4. 新しいリモートブランチが作成される