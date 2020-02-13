# 快速开始

> Ho! 这是你的一小步,但这也是你迈向成功的一大步

## Register

你可以在 [Hochat Console](https://console.hochat.space) 注册你的账户.

由于当前未发布,此内容有待更新,如需注册请链接 [atkengwang@qq.com](mailto:atkengwang@qq.com) ,我们会提前帮您注册.



之后,你就得到了一个独一无二的Key

## 引用 Hochat

首先,找到你想要放置的位置. 你一般可以将他放在Footer文件里

从我们的CDN引用 Hochat 的主文件:

(欢迎大家赞助CDN,有意愿联系 [atkengwang@qq.com](mailto:atkengwang@qq.com))

```html
<script src="https://cdn.hochat.space/hochat.js"></script>
```

然后新建一个容器. Hochat 会生成在这个容器中. 你可以添加代码:

```HTML
<div id="hochat_container"></div>
```

你可以自定义他的ID以及Style属性,但是一会儿我们会用到这个ID

最重要的环节

```html
<script>
    new Hochat("the_key", "#hochat_container");
</script>
```

你可以将 `the_key` 替换成你从控制台的到的key  `#hochat_container` 是容器的css选择标签

Ho! 现在你可以看见你的页面中有Hochat了

享受吧~