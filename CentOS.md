# CentOSをインストールする

## １, CentOSのイメージを取得する。
~~~sh
$ docker pull centos:centos7
~~~

## 2, CentOSのコンテナを構築

先ほどコピーした　pull コマンドを実行し、CentOSのイメージを取得します。

<span style="color: red; ">ーー実行結果ーー</span>
~~~sh
Using default tag: latest
latest: Pulling from library/debian
Digest: sha256:534da5794e770279c889daa891f46f5a530b0c5de8bfbc5e40394a0164d9fa87
Status: Image is up to date for debian:latest
docker.io/library/debian:latest
business12@2020business12noMacBook-Air ~ % docker pull centos:centos7
centos7: Pulling from library/centos
Digest: sha256:be65f488b7764ad3638f236b7b515b3678369a5124c47b8d32916d6487418ea4
Status: Image is up to date for centos:centos7
docker.io/library/centos:centos7

~~~

CentOSのイメージを取得できたことが確認できます。
~~~sh
$ docker images
~~~

<span style="color: red; ">ーー実行結果ーー</span>
|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|-----|-----|---|---|---|
|centos    | centos7 |   eeb6ee3f44bd | 16 months ago | 204MB

CentOSのイメージを無事に取得できた。

## 3,コンテナの作成
コンテナ作成を行なう。
docker createコマンドを使ってコンテナの作成を行う。
~~~sh
docker create --name status-test -it centos_test/bin/sh
~~~

## 4,起動。ログイン、停止
コンテナの起動
~~~sh
docker start centos-test
~~~
コンテナへのログイン
~~~sh
 docker exec -it centos-test bash
 ~~~
コンテナの停止
~~~sh
docker stop centos-test
~~~
以上でCentOSが使えるようになった。