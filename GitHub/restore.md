## PCを初期化した場合に、github上のアプリを復元する方法
1. git cloneすることで、ローカルにコードを復元する。
```sh
% git clone https://github.com/komafuji820/programming_note.git
```

2. 必要に応じて、DBを再構築する。
```sh
# 復元したコードのフォルダに移動する
% cd programming_note

# gemfileの内容に従って、必要なgemをインストールする
% bundle install

# データベースの作成
% rails db:create

# データベースにテーブルを作成する（マイグレーションファイルの内容を反映させる）
% rails db:migrate
```

3. GitHubDesktopとの連携
通常通り、Add Existing Repositoryを選択すればOK