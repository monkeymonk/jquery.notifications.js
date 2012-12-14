jQuery.notifications Plugin - v 1.0
==================

Notifications System inspired by Growl


## Usage

### Basic

``` javascript
$(document).ready(function() {
    $.notifications({content: '<b>Lorem ipdum</b> dolor sit amet...'});
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

#### `add` ($.notification('add', params) is the same as $.notifications(params))

jQuery.notifications use a tiny template system that let you an easy way to customize your notifications.

``` javascript
$.notifications('add', {
    title: 'Lorem ipsum',
    content: '<b>Lorem ipsum</b> dolor sit amet...',

    className: 'simple',

    tpl: '<div class="{className}"><h1>{title}</h1><p>{content}</p></div>'
});

```

#### `remove`

``` javascript
$.notifications('remove');

// or

$.notifications('remove', identifier);

```


## Browsers: Tested and Working In

- IE 6, 7, 8, 9, 10
- Firefox 3+
- Opera 10+
- Safari 4+

