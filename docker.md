___Dockerのイメージ作成とコンテナの作成を行う___

___イメージの確認___


~~~sh
$ docker images
~~~


<span style="color: red; ">ーー実行結果ーー</span>

|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|-----|-----|---|---|---|
| ubuntu | latest | 3c2df5585507 | 5 weeks ago | 77.8MB
| httpd  | latest | d16a51d08814 | 2 months ago| 145MB
| nginx  | latest | 891bc8b449d4 | 4 months ago| 142MB


___イメージの取得___
~~~sh
$ docker pull ubuntu 
~~~

___再度イメージの確認をする___
~~~sh
$ docker images
~~~

<span style="color: red; ">ーー実行結果ーー</span>

|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|-----|-----|---|---|---|
| ubuntu | latest | 6b7dfa7e8fdb | 3 days ago  | 77.8MB
| ubuntu | <none> | a8780b506fa4 | 5 weeks ago | 77.8MB
| httpd  | latest | d16a51d08814 | 2 months ago| 145MB



___取得したイメージからコンテナ作成___

___下記のコマンドで現在のコンテナの稼働状況を確認します。___
~~~sh
$ docker ps
~~~

___下記のコマンドを実行すると作成と同時にコンテナも起動し、そのタイミングで自動的にログインします。___
~~~sh
$ docker run -it ubuntu
root@098a42730d74:/# 
~~~

___コンテナの起動___
~~~sh
$ docker start ubuntu-test
~~~

___コンテナへのログイン___
~~~sh
$ docker exec -it ubuntu-test bash
~~~

___コンテナの停止___
~~~sh
$ docker stop ubuntu-test
~~~

___コンテナの保存___
~~~sh
$ docker commit ubuntu-test my_ubuntu-test
~~~
