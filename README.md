### 開発環境の作成
1.プロジェクトが格納されているディレクトリに移動<br>
2.mysqlのイメージをdocker hubより取得<br>
docker pull mysql:latest<br>
3.expressをインストールする<br>
cd backend_node<br>
npm install express --save-dev<br>
4.dockerイメージの作成
docker-compose build
5.コンテナの生成
docker-compose up
6.expressの疎通確認
下記URLにブラウザよりアクセスした際、app.jsにてexpressを使用した処理が実行され、HelloWorldが表示される。
http://localhost:3000
7.mysqlの疎通確認
mysqlのコンテナ名を確認
docker ps
mysqlのコンテナに接続
docker exec -it mysqlのコンテナ名 bash
ログイン（パスワードはdocker-compose.ymlの環境変数MYSQL_ROOT_PASSWORDに記載）
mysql -u root -p
