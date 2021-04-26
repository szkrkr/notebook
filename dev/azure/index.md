
## MEMO
### デプロイに関してGit pushとWeb Deploy型の比較
* Git push型
・極論VSいらない。
・PubXmlいらない。
・Azureリソース側にLocalGitを設定しとかないといけない。
・そのままだとビルドはシンプルなmsbuildが走る。カスタムはできるらしい。ConfigurationはAppServiceの環境変数依存。
・ソリューションに複数プロジェクトの場合、ビルドしたいcsprojはAppServiceの環境変数依存。
・リモートビルドなので、ビルド失敗を検出するのが目検。
* Web Deploy型
・デプロイ環境にVSとnugetとWeb Deployがいる。
・PubXmlがいる。
・msbuildの引数のカスタマイズはこちらのがやりやすい。
・ローカルビルドなので、ビルドのログ取ったりエラーハンドリングはしやすい。

### Azure WebAppsの WarmUpに関して

Azureは一定期間のアクセスが無いと、その次のアクセス時に起動処理が実行されてしまう。
このため、定期的にアプリケーションを実行しておく必要がある。
定期的にアクセスするFunctionや、自動テストなどを用意して回避する。

### SQL DB Server - FailoverGroup

* フェイルオーバー構成を組んだが、正副切り替え後にアプリケーションが上手く切り替え後に接続できないという事象が発生した。

* 原因
アプリケーション側で保持しているコネクションプールが消えないままになっており、何時まで経っても古い SQLDB へ接続を試みようとしていた。

* 対応
以下2点のどちらかを実装する。
(1) アプリケーションに SQLDB への接続エラーが発生した後にコネクションプールを破棄するメソッドを呼ぶよう、実装を変更する
(2) SQLDBの死活監視を行う仕組みを別途実装し、フェイルオーバーが発生したら AppService を再起動する (再起動により、コネクションプールを強制的に破棄する)
