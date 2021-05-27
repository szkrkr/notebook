# firebase project関連

## multiple project
1. 環境別に分けたプロジェクトにそれぞれデプロイする方法。
   https://firebase.googleblog.com/2016/07/deploy-to-multiple-environments-with.html
2. 一つのプロジェクトで、デプロイターゲットを複数登録する。
   https://firebase.google.com/docs/hosting/multisites

→プロジェクトごとに、本番環境、開発環境を分けたい。さらに、Hostingの名前も変えたい！とするときは、上記2つを混ぜ合わせる。  
  
firebase.json
```
{
  "hosting": [
    {
      "target": "development",
      "public": "build",
      "ignore": ["firebase.json", "**/.*", "**/node_modules/**"],
      "rewrites": [
        {
          "source": "**",
          "destination": "/index.html"
        }
      ]
    },
    {
      "target": "production",
      "public": "build",
      "ignore": ["firebase.json", "**/.*", "**/node_modules/**"],
      "rewrites": [
        {
          "source": "**",
          "destination": "/index.html"
        }
      ]
    }
  ]
}
```
.firebaserc
```

{
  "projects": {
    "default": "projectid-01",
    "production": "projectid-02"
  },
  "targets": {
    "projectid-01": {
      "hosting": {
        "development": [
          "hosting-name-01"
        ]
      }
    },
    "projectid-02": {
      "hosting": {
        "production": [
          "hosting-name-02"
        ]
      }
    }
  }
}

```

## firebaseでさきリージョン設定するとstorageが使えなくなる。

Qiitaに記事にした。  
[Firebase: SDK経由で画像をStorageにアップロードできない。デフォルトのGCPリソースロケーションを最初に設定して困った話。](https://qiita.com/szkrkr/items/fe32a02708e461c3ca20)