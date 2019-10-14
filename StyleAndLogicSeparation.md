# 样式与逻辑分离

在前端发展到今天，工程化的开发模式已经必不可少。

现代化的开发模式，是一个多人合作的模式，必须使得每一个开发成本降低。因此，规范的代码结构，使保证每个成员能快速接入的基本要求。

不同的内容，使用不同的文件承载，保证开发与维护的方便性。

示例：

```html
<div class='container'>
    <div class='header'>
        头部
    </div>
    <div class='body'>
        内容
    </div>
    <div class='footer'>
        底部
    </div>
</div>
```

> 注：该代码由 HTML 编写

该内容写在独立文件中，标签上只有属性名称，没有样式内容，样式内容单独编辑。

```css
.container{
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
}
.container .header,.container .footer{
    height: 200px;
    background-color: red;
}
.containe .body {
    flex-grow: 1;
    background-color: blue;
}
```

> 注：该代码由 css3 编写

该内容写在对应的样式文件中，保持两者的独立性，对开发而言，是一个不错的进步。