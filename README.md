jQuery.notifications Plugin - v 1.0
==================

Notifications System inspired by Growl


## Usage

### Basic

First of all, include `jquery.notifications.js` and `jquery.notifications.css` in your HTML then start to use jQuery.notifications.

``` javascript
$(document).ready(function() {
    $.notifications({
        text: 'Lorem ipsum',
        content: '<b>Lorem ipdum</b> dolor sit amet...',
        image: 'http://lorempixel.com/40/40/abstract/'
    });
});
```

### Options

``` javascript
{
    className: 'notification',

    alive: 4000,
    fadeIn: 600,
    fadeOut: 800,
    sticky: false,

    // Template
    tpl: '<div class="{className}"><div class="{className}-img"><img src="{image}" alt="" /></div><div class="{className}-content"><div class="{className}-title">{title}</div>{content}</div></div>',

    // Callback
    onShow: function () {},
    onHide: function () {}
}
```

### Methods

#### jQuery.notifications('add');

jQuery.notifications use a tiny template system that let you an easy way to customize your notifications.

``` javascript
$.notifications('add', {
    title: 'Lorem ipsum',
    content: '<b>Lorem ipsum</b> dolor sit amet...',

    className: 'simple',

    tpl: '<div class="{className}"><h1>{title}</h1><p>{content}</p></div>'
});

// same as $.notifications(params);

```

#### jQuery.notifications('remove');

By default, that remove the last notification that was added.
You can pass an identifier to targetting a specific one.
You can also pass a callback, if not the `onHide` will be used (if is set).

``` javascript
$.notifications('remove', callback);

// or

$.notifications('remove', 3, callback);

```

#### jQuery.notifications('removeAll');

Remove all notifications.
You can pass a callback, if not the `onHide` will be used (if is set).

``` javascript
$.notifications('removeAll', callback);

```


## Browsers: Tested and Working In

- IE 6, 7, 8, 9, 10
- Firefox 3+
- Opera 10+
- Safari 4+

