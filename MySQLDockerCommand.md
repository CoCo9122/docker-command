## DockerにおけるMySQLコンテナの作成

- MySQLコンテナの作成・起動
```sh
$ docker run --name mysql000ex1 -dit -e MYSQL_ROOT_PASSWORD=myrootpass mysql
```
- MySQLコンテナの停止
```sh
$ dcoker stop mysql000ex1
```

- MySQLコンテナの削除
```sh
$ docker rm mysql000ex1
```

- MySQLコンテナの作成・起動（実際の場合）
```sh
$ docker run --name コンテナ名 -dit --net=ネットワーク名 -e MYSQL_ROOT_PASSWORD=MySQLのrootパスワード -e MYSQL_DATABASE=データベース領域 -e MYSQL_USER=MySQLのユーザー名 -e MYSQL_PASSWORD=MySQLのパスワード mysql --character-set-server=文字コード --collation-server=照合順序 --default-authentication-plugin=認証方式 
```