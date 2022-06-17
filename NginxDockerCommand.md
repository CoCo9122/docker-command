## DockerにおけるNginxコンテナの作成

- Nginxコンテナの作成・起動
```sh
$ docker run --name nginx000ex1 -d nginx
```
- Nginxコンテナの停止
```sh
$ docker stop nginx000ex1
```

- Nginxコンテナの解除
```sh
$ docker rm nginx000ex1
```

- ポートを指定してNginxコンテナの作成・起動
```sh
$ docker run --name nginx000ex2 -d -p 8080:80 nginx
```

- コンテナを起動したらいかにアクセス可能

[http://localhost:8080/](http://localhost:8080/)

- Nginxコンテナの解除
```sh
$ docker rm nginx000ex2
```

- ドキュメントルート
```sh
/usr/share/nginx/html