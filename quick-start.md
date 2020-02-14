# Quick Start

> Ho! This is a small step for you, but it is also a big step for you towards succeed

## Register

You can register your own Hochat account in [Hochat Console](https://console.hochat.space).

This section is going to be finish, Now you can contact [atkengwang@qq.com](mailto:atkengwang@qq.com) to add your site.

Then you can get your own key.

## Include Hochat

First, find the pages you wanted to add. Simply, you can add it to your footer.

You can include Hochat by our CDN:

```html
<script src="https://cdn.hochat.space/hochat.js"></script>
```

### Method 1 (Recommend)

Find the Element you wanted to add, For example

```html
<div id="main"></div>
    
    window.onload = function () {
        new Hochat("document", "#main");
    }
```

Hochat will append to main in your website

### Method 2:

 create a container. Hochat will be in this container. You can just simply add

```HTML
<div id="hochat_container"></div>
```

### Method 3:

 Find the element that you want to append at the end.

```html
<body class="hochat_container">
    ...
</body>
```

You can customize the id and class of the container, but it will be use next

The most important is insert JS

```html
<script>
    new Hochat("the_key", "#hochat_container");
</script>
```

Well, you can replace `the_key` with the key you get from the Hochat Console. `#hochat_container` is the CSS Selector for the container. For Method 1 is `#hochat_container`, For Method 2 is `.hochat_container`

Ho! Now you can see Hochat in your webpage.

Enjoy~