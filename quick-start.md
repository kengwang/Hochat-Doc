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

and then create a container. Hochat will be in this container. You can just simply add

```HTML
<div id="hochat_container"></div>
```

You can customize the id of the container, but it will be use next

The most important is insert JS

```html
<script>
    new Hochat("the_key", "#hochat_container");
</script>
```

Well, you can replace `the_key` with the key you get from the Hochat Console. `#hochat_container` is the CSS Selector for the container.

Ho! Now you can see Hochat in your webpage.

Enjoy~