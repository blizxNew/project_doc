# JavaScript高级程序设计-笔记  

1 参考

> JavaScript高级程序设计-第四版
>
> [尚硅谷JavaScript基础&实战丨JS入门到精通全套完整版](https://www.bilibili.com/video/BV1YW411T7GX/?spm_id_from=333.1387.favlist.content.click&vd_source=0a0dd058ef849bffba564af91a70780d)
>
> [阮一峰--网道JavaScript](https://wangdoc.com/javascript/basic/introduction)

2025年3月9号

## 1 入门篇
1 什么是 JavaScript 语言？

>

 

## 2 基础篇

### 2.1 基本的输出

> alert: 浏览器弹出警告框
>
> document.write:向网页写入内容，在源代码body里面没有该元素，但是元素审查的时候有
>
> console.log：向控制台输出内容
>
> 
>
> 注意项： 使用 `alert` 可能会破坏用户体验，因为它会中断用户的操作。因此，应该谨慎使用。

```html
<!--声明文档类型，告知浏览器这是一个HTML5文档。-->
<!DOCTYPE html>
<!--开始HTML文档，lang="en"属性指定了文档的语言为英语。-->
<html lang="en">
<!--定义HTML文档的头部，包含文档的元数据，如字符集、标题和脚本等。-->
<head>
  <!--设置文档的字符编码为UTF-8，这是一种普遍支持的编码，可以显示几乎所有的字符。-->
  <meta charset="UTF-8">
  <!--设置网页的标题，此处的标题是“Title”。这个标题会出现在浏览器的标签页上。-->
  <title>Title</title>
  <!--开始一个JavaScript脚本段，type="text/javascript"属性指定了脚本的类型为JavaScript，
   类型可选，默认为text/javascript。-->
  <script type="text/javascript">
    // 浏览器弹出警告框
    alert("Hello, World!");
    // 向网页写入内容
    document.write("Hello, World!");
    // 向控制台输出内容
    console.log("Hello, World!");
    /**
     * 注意事项：JavaScript代码，从上到下依次执行，一行一行得执行。
     * 在这里，会先弹出警告框，点击警告框的“确定”按钮后，才会向网页写入内容，最后向控制台输出内容。
     * */
  </script>
</head>
<!--开始HTML文档的主体部分，这里可以放置网页的主要内容。-->
<body></body>
</html>
```

