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