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

## Accordion

```js
// https://jqueryui.com/accordion/

$("#accordion").accordion({ collapsible: true, heightStyle: "content" });
```

## Datepicker

```js
// DATEPICKER
// https://jqueryui.com/datepicker/

$(".date").datepicker({
  showOtherMonths: true,
  selectOtherMonths: true,
  showButtonPanel: true,
  changeMonth: false,
  changeYear: false,
  numberOfMonths: 2,
  minDate: -1,
  maxDate: "+1W +5D",
});
```

## Todo List

```js
$("#todoList ul").sortable({
  items: "li:not('.listTitle, .addItem')",
  connectWith: "ul",
  dropOnEmpty: true,
  placeholder: "emptySpace",
});

$("input").keydown(function (e) {
  if (e.keyCode == 13) {
    var item = $(this).val();

    $(this)
      .parent()
      .parent()
      .append("<li>" + item + "</li>");
    $(this).val("");
  }
});

$("#trash").droppable({
  drop: function (event, ui) {
    ui.draggable.remove();
  },
});
```
