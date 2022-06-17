## DockerにおけるNginxコンテナの作成

- Nginxコンテナの作成・起動
```console
$ docker run --name nginx000ex1 -d nginx
```
- Nginxコンテナの停止
```conole
$ docker stop nginx000ex1
```

- Nginxコンテナの解除
```conole
$ docker rm nginx000ex1
```

- ポートを指定してNginxコンテナの作成・起動
```conole
$ docker run --name nginx000ex2 -d -p 8080:80 nginx
```

- コンテナを起動したらいかにアクセス可能

[http://localhost:8080/](http://localhost:8080/)

- Nginxコンテナの解除
```conole
$ docker rm nginx000ex2
```

- ドキュメントルート
```
/usr/share/nginx/html