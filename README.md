### 開発環境の作成
1.プロジェクトが格納されているディレクトリに移動  
2.mysqlのイメージをdocker hubより取得  
&emsp;docker pull mysql:latest  
3.expressをインストールする  
&emsp;cd backend_node  
&emsp;npm install express --save-dev  
4.dockerイメージの作成  
&emsp;docker-compose build  
5.コンテナの生成  
&emsp;docker-compose up  
6.expressの疎通確認  
&emsp;下記URLにブラウザよりアクセスした際、app.jsにてexpressを使用した処理が実行され、HelloWorldが表示される。  
&emsp;http://localhost:3000  
7.mysqlの疎通確認  
&emsp;mysqlのコンテナ名を確認  
&emsp;&emsp;docker ps  
&emsp;mysqlのコンテナに接続  
&emsp;&emsp;docker exec -it mysqlのコンテナ名 bash  
&emsp;ログイン（パスワードはdocker-compose.ymlの環境変数MYSQL_ROOT_PASSWORDに記載）  
&emsp;&emsp;mysql -u root -p
