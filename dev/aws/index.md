# 

## AWS アカウントの使い方
- 一つをIAMユーザー管理のアカウントとして用意。あとは Assume Roleを使用するなどが良い

## SES
- 苦情、バウンスなどはちゃんと管理しないとアカウント全体でダメージ

## Cognito
- あまり大規模な構成には向いてなさそう。大規模に行う場合は、別のサービス使用した方が良さげ。
- 複数のユーザープールを使用しての認証認可はありか?
