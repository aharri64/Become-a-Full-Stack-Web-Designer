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

## Droppable

```js
// https://jqueryui.com/droppable/
$("#droppable").droppable({
  accept: "#box1",
  drop: function () {
    $(this).text("when a box got attitude, drop it like it's hot!");
  },
});
```

## sortable

```js
// https://jqueryui.com/sortable/

$("#sortable").sortable({
  connectWith: "#sortableToo",
  placeholder: "placeholderBox",
});
$("#sortableToo").sortable({
  connectWith: "#sortable",
  placeholder: "placeholderBox",
});
```
