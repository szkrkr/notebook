# チームの立ち上げ

## 立ち上げ時考慮すること
* 英語含めて単語帳作る（ユビキタス言語）

## ソースコード作成時
* 命名規則(リソースなど)
* 想定する環境 (Prod, Dev, RC, Stagingなど)
* ポート設計
* インフラの構築順序  
構築前準備(DB Admin PW, DB文字列, SSL証明書) -> インフラ構築（Azure PowerShell Script/ARM Template) -> [ Application Release (Web/API/Function only) | データ構築(DB/Storage/KeyVault) ] -> ドメイン登録

* できれば使うHTTPStatusの認識合わせ  
(DBないのEntityが見つからなかったときは、204 か 404 か、など)

* 簡単なコーディングルール 
Datetime or DatetimeOffset