## DockerにおけるWordPressコンテナの作成

WordPressにはMySQLとネットワークの起動必須

- ネットワークの作成
```sh
$ docker network create wordpress000net1
```

- MySQLコンテナの作成・起動
```sh
$ docker run --name mysql000ex1 -dit --net=wordpress000net1 -e MYSQL_ROOT_PASSWORD=myrootpass -e MYSQL_DATABASE=wordpress000db -e MYSQL_USER=wordpress000kun -e MYSQL_PASSWORD=wkunpass mysql --character-set-server=utf8 --collation-server=utf8_general_ci --default-authentication-plugin=mysql_native_password 
```

- WordPressコンテナの作成・起動
```sh
$ docker run --name wordpress000ex1 -dit --net=wordpress000net1 -p 8080:80 -e WORDPRESS_DB_HOST=mysql000ex1 -e WORDPRESS_DB_NAME=wordpress000db -e WORDPRESS_DB_USER=wordpress000kun -e WORDPRESS_DB_PASSWORD=wkunpass wordpress
```

- コンテナの停止
```sh
docker stop wordpress000ex1
docker stop mysql000ex1
```

- コンテナの解除
```sh
docker rm wordpress000ex1
docker rm mysql000ex1
```
- イメージの解除
```sh
docker image rm wordpress
docker image rm mysql
```
- ネットワークの解除
```sh
$ docker network rm wordpress000net1
```