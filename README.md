# README
<!-- 
This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ... -->

① dockerをインストールしておく。<br>
② Railsアプリを置く作業用ディレクトリを作成し移動する
```
mkdir <ディレクトリ名> && cd <ディレクトリ名>
```
③ $ git cloneでリポジトリを自分の手元のローカルに複製する
```
$ git clone https://github.com/TomoXiang710/rails-docker.git
```
④ 
```
$ docker compose up -d 
```
でRailsとpostgreSQLそれぞれのコンテナを起動する<br>
⑤
```
$ docker compose exec web bash
``` 
を実行して
```
root@~~~~~~:/rails-docker
```
でコンテナの中のシェルに入る。<br>
⑥ 
```
$ rails db:create
$ rails db:migrate
```
を実行し、
```
$ exit 
```
でコンテナから抜ける。<br>
⑦ 
```
http://localhost:3000/
```
でブラウザにアクセスできる。


