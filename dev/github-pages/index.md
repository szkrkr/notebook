# Github Page

## Github Pageでポートフォリオサイトを作る。

### Motivation

ここをみてたら、良いなぁーって気持ちになったのと、自分から発信する土壌を作りたかった。
https://github.com/azer/notebook

### 完成品　

[Szrkrk's Portfolio](http://szkrkr.github.io/)

### 構成

* Portfolioサイト: Jekyll による静的サイト
  szkrkr.github.io/ にリンクされる。
* Portfolioから派生したnotebookのサイト: HonKitから作成した静的サイト
  szkrkr.github.io/notebook にリンクされる。
  githubのレポジトリ自体は分かれているが、レポジトリ名がそのままリンクされることになる。

### 参考URL

* [GitHub.com/GitHub Pages/Jekyll を使用して GitHub Pages サイトを設定する](https://docs.github.com/ja/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll)
* [jekyll homepage](http://jekyllrb-ja.github.io/)
* [jekyll/minima](https://github.com/jekyll/minima)
* [GitBookでWebサイトを作ってGitHub Pagesで公開する方法](https://r-ngtm.hatenablog.com/entry/2020/06/18/193235)
* [GitBook がしれっと HonKit になってた件](https://qiita.com/sugurutakahashi12345/items/9e0d47b74ce257b31006)
* [honkit/honkit](https://github.com/honkit/honkit)

### trouble shooting

* bundle exec jekyll X.X.0 new . とかやろうとしたら、"Could not locate Gemfile or .bundle/ directory”  
  -> 最初は、jekyll からで良い。なぜなら、bundleファイルがないから。  
  [Ref](https://talk.jekyllrb.com/t/trouble-creating-a-new-jekyll-site-could-not-locate-gemfile-or-bundle-directory/4399)

* jekyllができない。  
-> [jekyllのサイト](https://jekyllrb.com/docs/installation/macos/)　にある ```gem install --user-install bundler jekyll```　ではなく、　``` gem install bundler jekyll``` で良い。
使いたいRubyのverisonと間違えないようにする。

* jekyll相対ぱすはどうするの  
`[any](any.md)` や `[any](any.html)` でもなく、    
`[any](any)` でOK    
[Ref](https://stackoverflow.com/questions/7653483/github-relative-link-in-markdown-file)

* markdownで新しいタブで開くはどうやるの  
→　html tagで記載する。  
[Ref](https://stackoverflow.com/questions/4425198/can-i-create-links-with-target-blank-in-markdown)

* GitHub PagesのminimaテンプレートでGAのデータが送信されない  
-> [GitHub PagesのminimaテンプレートでGAのデータが送信されない](https://qiita.com/mitsuaki1229/items/fea653029ce09ebce858)

### Future
* favicon.ico の設定
* custom domain

### 構築までかかった時間
* 6時間程度

### 所感
* Rubyは全然触らないので、gem コマンドを本当に久しぶりに打った。
* サーバーの管理がなくて良いなと思った。

### その他
* Github Contoribution Graph
https://grass-graph.moshimo.works/

* Code Activitly/ Languages
[WakaTime](https://wakatime.com/)
