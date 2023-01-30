# RHEL7をインストールする

## １, RedHat社の公式サイトでコンテナイメージを取得するDockerコマンドを確認

https://catalog.redhat.com/software/containers/rhel7/57ea8cee9c624c035f96f3af?container-tabs=gti&gti-tabs=unauthenticated

上記のリンクから
~~~sh
$ docker pull registry.access.redhat.com/rhel7
~~~
をコピーする。

## 2,CentOS7でRHEL7のコンテナを構築

先ほどコピーした　pull コマンドを実行し、RHEL7のイメージを取得します。

<span style="color: red; ">ーー実行結果ーー</span>
~~~sh
Using default tag: latest
latest: Pulling from rhel7
Digest: sha256:42c7d8ef38a3be2578cad65a833e957f1821012d9f1208654ace4b44b3e3e305
Status: Image is up to date for registry.access.redhat.com/rhel7:latest
registry.access.redhat.com/rhel7:latest
~~~

RHEL7のイメージを取得できたことが確認できます。
~~~sh
$ docker images
~~~

<span style="color: red; ">ーー実行結果ーー</span>
|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|-----|-----|---|---|---|
|registry.access.redhat.com/rhel7 | latest | 71f49ae778de | 5 weeks ago | 208MB

RHEL7のイメージを無事に取得できた。

## 3,コンテナの作成、起動。ログイン、停止

コンテナ作成
~~~sh
docker create --name status-test -it stoic_ritchie
 /bin/sh
~~~
コンテナの起動
~~~sh
docker start stoic_ritchie
~~~
コンテナへのログイン
~~~sh
 docker exec -it stoic_ritchie bash
~~~
コンテナの停止
~~~sh
docker stop stoic_ritchie
~~~
コンテナの保存
~~~sh
docker commit stoic_ritchie my_stoic_ritchie
~~~



