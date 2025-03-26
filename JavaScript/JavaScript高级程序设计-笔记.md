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

### 2.1 基本的输出[视频p2]

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



### 2.2 js代码位置[视频p3]

>1 将代码写在标签的属性中，但是这属于结构与行为耦合，不推荐
>
>2 代码写到script标签中，如果有多个script标签中存在相同的函数，会执行只有一个标签的
>
>3 js代码写在外部js里面，通过script标签引入。写到外部文件中的代码可以在不同的页面中同时使用，也可以利用浏览器的缓存机制，推荐使用 
>
>​	注意点：当script标签一旦引入了外部文件，就不能中间写代码了，因为写了，浏览器也会忽略。如果需要将代码写在script标签内，重新再加一个便是

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Title</title>
  <!--4 js代码写在外部js里面，通过script标签引入，
        写到外部文件中的代码可以在不同的页面中同时使用，也可以利用浏览器的缓存机制，推荐使用
  -->
  <script type="text/javascript" src="../js/02_learn_js.js"></script>
  <script type="text/javascript">
    //3  代码写到script标签中，并添加type="text/javascript"属性
   function myAlert () {
     alert('Hello World!');
   }
  </script>
</head>
<body>
 <!--1 代码写到标签的onclick属性中，点击时候会执行。-->
 <!--可以将代码写在标签的属性中，但是这属于结构与行为耦合，不推荐-->
 <button onclick="alert('Hello World!')">点我</button>
 <!--2 代码写到超链接标签的href属性中，并以javascript:开头，点击时候会执行，-->
 <a href="javascript:alert('Hello World!')">点我</a>
 <!--点击超链接，不会跳转-->
 <a href="javascript:;">点我</a>
 <!--3 代码写到script标签中-->
 <!--有同名时候，会执行最后一个-->
 <button onclick="myAlert()">点我11</button>
 <button onclick="myFun()">点我222</button>

 <script type="text/javascript">
   //3  代码写到script标签中，这里会执行
   function myAlert () {
     alert('H!1111');
   }
 </script>
</body>
</html>
```

### 2.3 基本上语法[视频p4]

1  注释

> ```
> /**/ 多行注释
> // 单行注释
> ```

2  JS中严格区分大小写

3  JS中每一条语句以分号结尾。如果不写，浏览器会自动加上，但是会消耗点儿性能，而且有时候，浏览器会加错分号

4  JS会忽略多个空格和换行，所以我们可以利用这个来美化代码
