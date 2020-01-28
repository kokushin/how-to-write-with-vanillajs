# on()

`on`メソッドに関する処理

## クラスに対してイベントを登録する

jQuery:
```js
$('.js-button').on('click', e => {
  // 処理
});
```

VanillaJS:
```js
document.querySelectorAll('.js-button').forEach(element => {
  element.addEventListener('click', e => {
    // 処理
  });
});
```

## 動的に生成された要素にイベントを登録する

jQuery:
```js
$(document).on('click', '.js-button', e => {
  // 処理
});
```

VanillaJS:
```js
document.addEventListener('click', e => {
  if (!e.target || !e.target.classList.contains('js-button')) {
    return;
  }
  // 処理
});
```