# Chrome
* How to import lodash to Chrome console?
```
fetch('https://cdn.jsdelivr.net/npm/lodash@4.17.4/lodash.min.js')
    .then(response => response.text())
    .then(text => eval(text))
```
https://medium.com/@matt.leo/how-to-import-lodash-to-chrome-console-3e5e30b4933e


# Makrdown
* use `<details>` tag to collapse
<details>
  <summary> open </summary>
  <p>
  collpased!
  </p>
</details>

* use `%28` instead of `(`, `%29` instead of `)` when you use `()` link syntax.

# Raspberry-Pi
* https://eikihaya.hatenablog.com/entry/20170727/1501121212

# 環境変数
`vi ~/.zshrc`で編集すること。
コマンドライン上だと、再起動すると、消える。
https://qiita.com/yakumomutsuki/items/d2fd9f103df7f728c20b

ちなみに npm へのpathは `npm bin -g`で確認可能。
adsf内の場合は、｀.asdf/installs/nodejs/15.10.0/.npm/bin｀ とかになる。

(vueを入れる時に困った。)

# Terminal
* % clear
  -> clear screen but previous command is remmaining if you scroll.
* % reset
  -> clear screen with previous command.

# 参考文献に関して

https://www.komazawa-u.ac.jp/~kazov/Nis/lecture/seminar/references.html

