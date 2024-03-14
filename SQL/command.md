## コマンド集
```sh
# バージョンの確認
% mysql --version

# 起動
% mysql.server start

# 管理者ユーザーでログイン
% mysql -u root         # 管理者ユーザーはパスワードなし

# ユーザーの作成＆確認（管理者ユーザーでログインしている場合）
% create user 新ユーザー名@localhost identified by ‘新パスワード’;
% select Host,User from mysql.user;

# データベース（スキーマ）の作成＆確認（管理者ユーザーでログインしている場合）
% create database データベース名 default character set utf8;
% show databases;

# ユーザーへのアクセス権限の付与＆アクセス権限の確認（管理者ユーザーでログインしている場合）
% grant all privileges on データベース名.* to ユーザー名@localhost ;
% show grants for ユーザー名@localhost;

# 認証プラグインの変更＆確認（管理者ユーザーでログインしている場合）
% alter user ユーザー名@localhost identified with mysql_native_password by 'パスワード';
% select User,Plugin from mysql.user;

# ログアウト
% quit
```

## 認証プラグインについて
今までの認証プラグインは、"mysql_native_password" だったが、MySQL8.0から"caching_sha2_password"に変更された。
ただし、MySQLに接続するツールの多くがこれをサポートしていない。
これを"mysql_native_password"に戻るコマンドが、
```sh
# 認証プラグインの変更
% alter user ユーザー名@localhost identified with mysql_native_password by 'パスワード';
```