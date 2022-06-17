## DockerにおけるRedmineコンテナの作成

RedmineにはMariaDBとネットワークの起動必須

- ネットワークの作成
```sh
$ docker network create redmine000net1 
```

- MariaDBコンテナの作成・起動
```sh
docker run --name mariadb000ex1 -dit --net=redmine000net1 -e MYSQL_ROOT_PASSWORD=mariarootpass -e MYSQL_DATABASE=redmine000db -e MYSQL_USER=redmine000kun -e MYSQL_PASSWORD=rkunpass mariadb --character-set-server=utf8 --collation-server=utf8_general_ci --default-authentication-plugin=mysql_native_password
```

- Redmineコンテナの作成・起動
```sh
docker run --name redmine000ex1 --net=redmine000net1 -dit -p 8080:3000 -e REDMINE_DB_MYSQL=mariadb000ex1 -e REDMINE_DB_DATABASE=redmine000db -e REDMINE_DB_USERNAME=redmine000kun -e REDMINE_DB_PASSWORD=rkunpass redmine
```

- コンテナの停止
```sh
docker stop redmine000ex1
docker stop mariadb000ex1
```

- コンテナおよびボリュームの削除
```sh
docker rm redmine000ex1 -v
docker rm mariadb000ex1 -v
```

- イメージの削除
```sh
docker image rm redmine
docker image rm mariadb
```
- ネットワークの削除
```sh
$ docker network rm redmine000net1
```