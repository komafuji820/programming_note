## リモートリポジトリからデータをコピーする
```sh
% git clone https://github.com/komafuji820/programming_note.git

# 復元したコードのフォルダに移動する
% cd programming_note

# gemfileの内容に従って、必要なgemをインストールする
% bundle install

# データベースの作成
% rails db:create

# データベースにテーブルを作成する（マイグレーションファイルの内容を反映させる）
% rails db:migrate
```

## 新規作成との比較
```sh
# 新規作成コマンド
% rails _7.0.0_ new APPNAME -d mysql

# データベースを作成
% rails db:create

# マイグレーションファイルの編集
  t.string :title, null: false
  t.references :user, null: false, foreign_key: true
  # references型は、新規作成するカラムに、既存のテーブルを使用する場合に使う

# データベースにテーブルを作成
  rails db:migrate
```