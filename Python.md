___Ubuntuに最新バージョンのPythonをインストールする___

___Pythonバージョン確認___
~~~sh
$ python3 -V
~~~

___実行結果___
~~~sh
Python 3.8.2
~~~

___ビルド環境の準備___

___Pythonに必要なツールをインストールします___
~~~
$ apt update
$ apt install build-essential libbz2-dev libdb-dev \
  libreadline-dev libffi-dev libgdbm-dev liblzma-dev \
  libncursesw5-dev libsqlite3-dev libssl-dev \
  zlib1g-dev uuid-dev tk-dev
  ~~~

  ___ソースコードのダウンロード___
  ~~~sh
  $ wget https://www.python.org/ftp/python/3.9.2/Python-3.9.2.tar.xz<br>
  ~~~

  ___ダウンロードしたファイルは、次のコマンドで解凍しておきます。___
  ~~~sh
  $ tar xJf Python-3.9.2.tar.xz
  ~~~

___ビルド___
~~~sh
$ cd Python-3.9.2
$ ./configure
$ make
$ make install
~~~

___最後に次のような表示で終われば成功です。___
~~~sh
Installing collected packages: setuptools, pip
Successfully installed pip-20.2.3 setuptools-49.2.1
~~~

___インストールできたかを確認しましょう。___
~~~sh
$ python3 -V
~~~

___実行結果___
~~~sh
Python 3.9.2
~~~