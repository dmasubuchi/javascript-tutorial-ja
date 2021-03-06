importance: 5

---

# Spy デコレータ

その `calls` プロパティにすべての関数呼び出しを保存するラッパーを返すデコレータ `spy(func)` を作成してください。

すべての呼び出しは引数の配列として格納されます。

For instance:

```js
function work(a, b) {
  alert( a + b ); // work は任意の関数またはメソッド
}

*!*
work = spy(work);
*/!*

work(1, 2); // 3
work(4, 5); // 9

for (let args of work.calls) {
  alert( 'call:' + args.join() ); // "call:1,2", "call:4,5"
}
```

P.S. このデコレータはユニットテストで役立つ場合があります。その高度な形は [Sinon.JS](http://sinonjs.org/) ライブラリの `sinon.spy` です。