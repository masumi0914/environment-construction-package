# 概要
PHP及びNginx用のDocker開発環境構築パッケージ

# 使い方
1. cloneする
2. 次のコマンドを実行
  $docker-compose up -d # コンテナを作成して起動

# 備忘録
* dockerコマンド
1. docker ps # 動いているコンテナの確認 
2. docker rm {コンテナID} # コンテナの削除
3. docker images # イメージ一覧
4. docker rmi {イメージID} # イメージの削除

* docker-compose コマンド
1. docker-compose ps # プロセス状況確認
2. docker-compose down # コンテナ停止

* dockerの開発環境構築方法<br>
下記の2パターン
1. app,web,dbを一つずつ作成する
2. docker-compose.ymlファイルに記載してまとめてインストールする(今回)

* docker-composeについて
1. 複数のコンテナ(今回だとapp,web)を同時にインストールしたり起動させたりするツール
2. docker-compose.ymlにアーキテクチャの仕様を記載する

* nginxとphp-fpmの通信方式
1. TCPで通信する(今回)
2. UNIXドメインソケット<br>
    →通信のためにソケットを指定する<br>
    →niginx側からソケットを参照できるようにする

