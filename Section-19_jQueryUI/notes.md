# jQuery UI

## Draggable

```js
// https://jqueryui.com/draggable/
// go to this site for more, draggable plus sort is pretty good

$(".box").draggable();
$("#box1").draggable({ scroll: true, revert: "invalid" });
$("#box2").draggable({ axis: "x" });
$("#box3").draggable({ axis: "y" });
$("#box4").draggable({ containment: ".container", revert: "invalid" });
```
