# jQuery Notes

## Downloading and Installing jQuery

- Install directly from the jQuery site [here](https://jquery.com/)
- or you can attach the link and use a third parties library

You can see the latest stable version of CDN jQuery [here](http://code.jquery.com/)

Typically, put the CDN in first because it is much faster.

```html
<script src="//code.jquery.com/jquery-2.1.4.min.js"></script>
```

If the CDN does not load, then this code will run

```html
<script>
  window.jQuery ||
    document.write('<script src="js/jquery-2.1.4.js"><\/script>');
</script>
```

## The Simple Syntax of jQuery

```js
$(function () {
  $(selector).action();
});
```

## jQuery Selectors

#### Grouping Selector

```js
$("h2,h3,h4").css("border", "solid 1px red");
```

#### Id Selector

```js
$("div#container").css("border", "solid 1px red");
```

#### Class Selector

```js
$("p.lead").css("border", "solid 1px red");
```

#### Pseudo-element selector - selects first element

```js

```

#### Pseudo-element selector - selects even P tags

```js
$("p:even").css("border", "solid 1px red");
```

#### Descendant selector

```js
$("div em").css("border", "solid 1px red");
```

#### Child selector

```js
$("div > p").css("border", "solid 1px red");
```

#### jQuery Header selector

```js
$(":header").css("border", "solid 1px red");
```

#### jQuery Contains selector

```js
$('div:contains("Brad")').css("border", "solid 1px red");
```

## jQuery Event Methods

```js
$("#box").click(function () {
  alert("you just clicked the box");
});

$("input").blur(function () {
  if ($(this).val() == "") {
    $(this).css("border", "solid 1px red");
    $("#box").text("Forgot to add text?");
  }
});

$("input").keydown(function () {
  if ($(this).val() !== "") {
    $(this).css("border", "solid 1px #777");
    $("#box").text("Thanks for that!");
  }
});

$("#box").hover(
  function () {
    $(this).text("you hovered in!");
  },
  function () {
    $(this).text("you hovered out!");
  }
);
```

## jQuery Chaining

```js
$(".notification-bar").delay(2000).slideDown().delay(3000).fadeOut();
```

## Hiding, Showing & Fading Content with jQuery

```js
$("h1").hide();

$("div.hidden").show();

$("div.hidden").fadeIn(8000);

$("#box1").click(function () {
  $(this).fadeTo(1000, 0.25, function () {
    // animation is complete

    $(this).slideUp();
  });
});

$("div.hidden").slideDown();

$("button").click(function () {
  $("#box1").slideToggle();
});
```
