# Cheatsheet  
## 接続  
パスワード利用 `mysql -u <username> -h <mysql hostname> -D <database name> -p`  
## ユーザ関連  
ユーザ一覧を取得 `select Host, User, Password from mysql.user;`  
ユーザの権限を表示 `show grants for '<username>';`  
外から接続できるようにするにはパスワードを暗号化する必要がある `SET PASSWORD for '<username>'@'<hostname>' = PASSWORD('<password>');`  
ユーザ作成 `CREATE USER '<username>'@'<hostname>' IDENTIFIED BY '<password>'`  
ユーザを削除 `DROP USER <user name>;`  
## データベース関連  
データベース一覧を表示 `show databases;`  
使用するデータベースを選択 `use <database name>;`  
データベース作成　`CREATE DATABASE <database name>;`  
データベースを削除 `DROP DATABASE <database name>;`  
## テーブル関連
テーブル一覧を表示 `show tables;`  
テーブルを削除 `DROP TABLE <table name>`  
テーブルのデータを更新 `UPDATE <table name> SET <column name> = <value> WHERE <条件>`  
テーブルのデータを削除 `DELETE FROM <table name> WHERE <削除する条件>`  
## その他  
`select * from <tablename> \G` で見やすく出力  
