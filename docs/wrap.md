# wrap()

`wrap`メソッドに関する処理

## wrap

jQuery:
```js
$('#target').wrap('<span />');
```

VanillaJS:
```js
const target = document.getElementById("target");
const wrapper = document.createElement("span");

target.parentNode.insertBefore(wrapper, target);
wrapper.appendChild(target);
```