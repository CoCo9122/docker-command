## DockerにおけるApacheコンテナの作成

- Apacheコンテナの作成・起動
```console
$ docker run --name apa000ex1 -d httpd
```
- Apacheコンテナの停止
```conole
$ docker stop apa000ex1
```

- Apacheコンテナの解除
```conole
$ docker rm apa000ex1
```

- ポートを指定してApacheコンテナの作成・起動
```conole
$ docker run --name apa000ex2 -d -p 8080:80 httpd
```

- コンテナを起動したらいかにアクセス可能

[http://localhost:8080/](http://localhost:8080/)

- Apacheコンテナの解除
```conole
$ docker rm apa000ex2
```

- ドキュメントルート
```
/usr/local/apache2/htdocs/
```