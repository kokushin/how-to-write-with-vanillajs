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

## unwrap

jQuery:
```js
$('#target').unwrap();
```

VanillaJS:
```js
const target = document.querySelector('#target');

while(target.firstChild) {
  target.parentNode.insertBefore(target.firstChild, target);
}
target.remove();
```