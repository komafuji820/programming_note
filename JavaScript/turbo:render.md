# renderメソッドによって再読み込みしたときの問題点
  renderメソッドにより、入力情報を保持したまま元にページに戻ったときは、
  ```js
  window.addEventListener('turbo:load', post);
  ```
  の記述だけでは、render後にJSが読み込まれなくなるエラーが発生する。その場合、
  ```js
  window.addEventListener('turbo:render', post);
  ```
  を追記する。