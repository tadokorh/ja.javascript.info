最初の2つのチェックは2つの `case` になります。3つ目のチェックは2つのケースに分割されます。:

```js run
let a = +prompt('a?', '');

switch (a) {
  case 0:
    alert( 0 );
    break;

  case 1:
    alert( 1 );
    break;

  case 2:
  case 3:
    alert( '2,3' );
*!*
    break;
*/!*
}
```

注意してください: 末尾の `break` は必須ではありませんが、将来のためにそれを置く方がよいです。

将来、たとえば `case 4` のような `case` を追加したい機会があります。そして、以前に break を置くのを忘れていた場合、 `case 3` の終わりでエラーが発生します。なので、これは一種の自己保険です。
