# Debianをインストールする

## １, DebianのイメージをDocker hubから取得する。
https://hub.docker.com/_/debian

上記のリンクから
~~~sh
$ docker pull debian
~~~
をコピーする。

## 2,Debianのコンテナを構築

先ほどコピーした　pull コマンドを実行し、Debianのイメージを取得します。

<span style="color: red; ">ーー実行結果ーー</span>
~~~sh
Using default tag: latest
latest: Pulling from library/debian
Digest: sha256:534da5794e770279c889daa891f46f5a530b0c5de8bfbc5e40394a0164d9fa87
Status: Image is up to date for debian:latest
docker.io/library/debian:latest
~~~

Debianのイメージを取得できたことが確認できます。
~~~sh
$ docker images
~~~

<span style="color: red; ">ーー実行結果ーー</span>
|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|-----|-----|---|---|---|
|debian   | latest |   5c8936e57a38 | 12 days ago  | 124MB

Debianのイメージを無事に取得できた。

## 3,コンテナの作成、起動。ログイン、停止

コンテナ作成
~~~sh
docker create --name debian-test -it debian /bin/sh
~~~
コンテナの起動
~~~sh
docker start debian-test
~~~
コンテナへのログイン
~~~sh
 docker exec -it debian-test bash
 ~~~
コンテナの停止
~~~sh
docker stop bebian-test
~~~
コンテナの保存
~~~sh
docker commit debian-test my_bebian-test
~~~