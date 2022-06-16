# docker-command
## Docker Desktop 4.9.0

1. apache000ex1

<p>docker-compose.ymlのみの作成</p>
<p>httpdのみで作成</p>

- サービス用のコンテナを構築、作成、起動、アタッチの実行
```console
docker compose up -d
```
- コンテナを停止し、 `up`で作成したコンテナ、ネットワーク、ボリューム、イメージを削除
```console
docker compose down --rmi all
```

2. apache000ex2

<p>docker-compose.ymlとDockerfileを組み合わせての作成</p>
<p>httpdのみで作成</p>
- サービス用のコンテナを構築、作成、起動、アタッチの実行
```console
docker compose up -d
```
- コンテナを停止し、 `up`で作成したコンテナ、ネットワーク、ボリューム、イメージを削除
```console
docker compose down --rmi all
```
