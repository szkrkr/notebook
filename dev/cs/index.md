


* DBに対し参照しかしないデータをとるときは、 AsNoTracking() は、つけたほうがパフォーマンスが良い.
* Asyncに対しては、.ConfigureAwait(false)をする。できないときは、同一スレッドの内容をつけたいときだけ。