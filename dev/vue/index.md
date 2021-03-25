## Vue 3.0 で、 Vuex をインストールする。 - "Could not resolve dependency:peer vue@"^2.0.0" from vuex@3.6.2 node_modules/vuex vuex@"*" from the root project"

`npm i vuex --save` ができなかった。謎の `vue add vuex` でできた。
https://stackoverflow.com/questions/66652577/how-can-i-install-vuex-in-a-vue-cli-project

## .vue で　tsにするには

`<script>` -> `<script lang="ts">` にする。


## ts ファイルにしたら $stateが効かない。　- "ERROR in src/components/FlashMessages.vue:28:25 TS2339: Property '$store' does not exist on type 'ComponentPublicInstance<{}, {}, {}, { getAllFlashMessages(): Word; }, {}, EmitsOptions, {}, {}, false, ComponentOptionsBase<{}, {}, {}, { getAllFlashMessages(): Word; }, {}, ComponentOptionsMixin, ComponentOptionsMixin, EmitsOptions, string, {}>>'."

https://stackoverflow.com/questions/64412243/vue-js-3-and-typescript-property-store-does-not-exist-on-type-componentpub

## ことはじめ

* [チュートリアル](https://v3.ja.vuejs.org/guide/introduction.html#%E3%82%B3%E3%83%B3%E3%83%9B%E3%82%9A%E3%83%BC%E3%83%8D%E3%83%B3%E3%83%88%E3%81%AB%E3%82%88%E3%82%8B%E6%A7%8B%E6%88%90)にある、HTMLをどうすれば良いのかわからないよ！！

というか Vue3とVu2でだいぶ違うみたい。

