# helmfile

## How to read

https://helm.sh/docs/ 


### values.yamlの意味

変数を扱うファイル

https://helm.sh/docs/chart_template_guide/values_files/

sample

```
# values.yaml
image:
  repository: https://example.com/
```

```
# chart
.Values.image.repository // https://example.com/ として扱われる
```

上記のようなものを builtin_objects と呼ぶ.

.Chart.AppVersion なども同様

https://helm.sh/docs/chart_template_guide/builtin_objects/


## name: {{ include "xxx" . -}} の意味

xxx は、テンプレート名

. は渡す変数.?　→違うかも

“-” は　[ここ](https://helm.sh/docs/chart_template_guide/control_structures/#:~:text=First%2C%20the%20curly,Newlines%20are%20whitespace!) 参照

> First, the curly brace syntax of template declarations can be modified with special characters to tell the template engine to chomp whitespace. {{- (with the dash and space added) indicates that whitespace should be chomped left, while -}} means whitespace to the right should be consumed. Be careful! Newlines are whitespace!
> 中括弧内側の前後にダッシュ {{- -}} をつけることができ、前に付けた場合はその部分より前の半角スペースを、後ろにつけた場合は改行コードを取り除くことができます

## _helpers.tplとは


テンプレートは _helpers.tpl で定義されている。

```
{{- define "xxx" -}}
```

> Chart内で共通で使うことのできるテンプレートスニペットを定義します、これは「名前付きテンプレート」と呼ばれます

https://qiita.com/keiSunagawa/items/db0db26579d918c81457#_helperstpl

> Named Templatee

https://helm.sh/docs/chart_template_guide/named_templates/

### with

```
{{- with .Values.yyy }}
imagePullSecrets: {{- toYaml . | nindent 12 }}
{{- end }} 
```

.Values.yyy オブジェクトをルートオブジェクトとしてendまで展開

つまり . は　.Values.yyy 

toYaml で . をオブジェクトをyaml形式で展開

| はチェイン

nindent 12 -> 12文字分indent インデント調整用


### 文字列操作関数

quote: “で囲む

b64enc: 多分base64エンコーディング

https://www.skyarch.net/blog/?p=16660#25
