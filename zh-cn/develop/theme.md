# 主题开发文档

> Ho! 欢迎加入开发的组织. Hochat 因你而优秀!

你已经走到了这一步了,感谢你对 Hochat 的支持!

## 开始之前

请先想好您的主题名称,最好在站点内搜索一下有没有重复名称的主题.

主题名称 不宜过长,全部小写,4-10个字符为最佳. 主题名称中不能含有特殊符号(下划线除外),空格,非法字符(f**k)

## Link Start!

请先构件好您的目录结构,我们所支持的目录结构是(主题名称为name):

```
- name
|   |- name.html
|   |- tree.txt
|   
+---img
|   |-  optinal.png
|       
+---js
|   |-  1.js
|   |-  asfdsafa.js
|       
\---style
    |-  1.css
    |-  asdfa.css
```



> 提示: style和js下可以任意创建任何名字的文件,他们最终会合成一个文件



此后,您就可以在 `主题名`.html 中编辑你自己风格的文件了!

## 语言结构

我们采用了独特的输出结构,可以助您快速的使用前端.

### 输出变量

我们可以输出一些变量,只需要使用

```
<%= 变量名 =%>
```

即可输出此变量

### 循环语句

循环语句可以帮您对评论区的数据有个方便的操作:

```
<# loop comments as comment #>
```

这样你就可以用上面的语句来输出了

```
<%= comment.username =%>
```

这样会输出用户名

当然了,你还需要指明何处停止循环

```
<# endloop #>
```

## 示例文件

```html
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <title>HoChat</title>
    <link rel="stylesheet" href="https://cdn.hochat.space/theme/default/css/main.css">
</head>
<body>

<div style="height: 50px;"></div>


<!-- HoChat! -->
<!-- Base Example -->
<div class="hochat">
    <div class="hochat-login">
        <div class="hochat-login-title">发表评论</div>
        <form>
            <div class="hochat-login-input-group">
                <div class="hochat-login-input">
                    <label>昵称(必填)</label>
                    <input placeholder="输入您的昵称" type="text">
                </div>

                <div class="hochat-login-input">
                    <label>邮件(必填)</label>
                    <input placeholder="请输入您的邮箱地址" type="text">
                </div>

                <div class="hochat-login-input">
                    <label>网址</label>
                    <input placeholder="输入您的网站地址" type="text">
                </div>
            </div>
            <textarea placeholder="什么叫鸡巴话，都在这里说吧~" rows="3"></textarea>
            <button>发射</button>
        </form>

    </div>
	<# loop comments as comment #>
    <div class="ho-chat">
        <img src="https://cdn.v2ex.com/gravatar/<%=comment.mailmd5=%>">
        <div class="ho-content">
            <div class="ho-name"><%=comment.username=%></div>
            <div class="ho-info"><%=comment.website=%></div>
            <div class="ho-msg">
                <%=comment.comment=%>
                <div class="ho-time"><%=comment.time=%></div>
            </div>
        </div>
    </div>
    <# endloop #>
</div>
<!-- Base Example -->
<script>
    window.addEventListener('load', function () {
        window.parent.postMessage(document.body.offsetHeight, "*");
    });
</script>
</body>
</html>
```

