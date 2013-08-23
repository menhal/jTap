jTap
=============

**jTap** - дополнительное событие для jQuery обрабатывающее прикосновение к экрану на сенсорных устройствах.

Те, кто сталкивался с адаптацией веб-приложений под мобильные устройства, знают что событие "click" срабатывает с
задержкой в 300ms, наблюдать которую не совсем приятно. Помимо этого, клик по не дерегированной области документа не
будет зафиксирован. Для решения этих задач и был разработан **jQuery Tap Event**.

Использование
-------

Подключите файл плагина на странице:
```html
<script src="jquery.tap.min.js"></script>
```
и затем, после инициализации, можно устанавливать обработчики следующим образом:
```javascript
$('selector').tap(handler);
$('selector').on('tap', handler);
```

**Заметка**: при использовании метода "tap", можно проверить его сщуествование таким образом:
```javascript
$.isFunction($.fn.tap);
```
и даже обезопасить себя поступив так:
```javascript
var clickEvent = $.isFunction($.fn.tap) ? 'tap' : 'click';

$('selector')[clickEvent](handler);
```
Но, конечно же, лучше просто использовать делегирование события при помощи стандартного метода `.on('tap', handler)`

**Заметка**: Примечательная особенность плагина - универсальность. Не важно где вы используете событие "tap":
на девайсе с сенсорным экраном или на настольном компьютере - обработчик будет выполнятся одинаково повсюду.

Changelog
-------
**Версия [0.2.0](https://github.com/BR0kEN-/jTap/tree/v0.2.0)**:
- дебютная публичная версия.

Лицензия
-------
**jTap** находится под действием [MIT license](http://opensource.org/licenses/mit-license.html).

Демонстрация
-------
http://firstvector.org/jTap
