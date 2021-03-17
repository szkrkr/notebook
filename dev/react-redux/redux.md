
# reduxの説明

## データの流れのイメージ
画面 => Operation = ( Action ) => Reducer => Store => Selector => 画面

1. Operationで、どのようなケースで、どのように値を更新したいかを設定して、Reducerに伝える(Dispatchする）。
  * ※「どのようなケースで、どのように値を」がAction
  * ※「どのようなケースで」が、FETCH_APPLICATION_REQUESTEDとかの定数
  * ※「どのように値を」が、payloadのなかみ
2.	Reducerは、Actionを受け取って、ケースに対して、それぞれStoreの値を更新する。
3.	Storeは、アプリケーション全体の値を保存しておく場所で、Reducerの要求で値を更新する。（逆にReducer以外からは、Storeを更新してはいけない）
4.	Selectorは、監視しているStoreの値が更新されると、Selectorが反応して、その値を欲している画面のみに伝える。
5.	画面は、Selectorが更新されたことを受け、再度レンダリングする。


* ※ ちなみに最小の構成であれば、
画面 = ( Action ) => Reducer => Store => 画面
画面から、Reducerを読んで、更新されたStoreから読み取って、画面が再レンダリングされるというのもできます。

