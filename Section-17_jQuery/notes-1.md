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
<script>window.jQuery || document.write('<script src="js/jquery-2.1.4.js"><\/script>');</script>
```

## The Simple Syntax of jQuery
```js
$(function() {
    $(selector).action();
})
```

## jQuery Selectors

#### Grouping Selector
```js
$('h2,h3,h4').css('border','solid 1px red');
```
#### Id Selector
```js
$('div#container').css('border','solid 1px red');
```
#### Class Selector
```js
$('p.lead').css('border','solid 1px red');
```
#### Pseudo-element selector - selects first element
```js

```
#### Pseudo-element selector - selects even P tags
```js
$('p:even').css('border','solid 1px red');
```
#### Descendant selector
```js
$('div em').css('border','solid 1px red');
```
#### Child selector
```js
$('div > p').css('border','solid 1px red');
```
#### jQuery Header selector
```js
$(':header').css('border','solid 1px red');
```
#### jQuery Contains selector
```js
$('div:contains("Brad")').css('border','solid 1px red');
```
