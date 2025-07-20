# 黑马程序员前端JavaScript入门到精通全套视频教程，javascript核心进阶ES6语法、API、js高级等基础知识和实战教程
 [视频链接](https://www.bilibili.com/video/BV1Y84y1L7Nn/?spm_id_from=333.337.search-card.all.click&vd_source=0a0dd058ef849bffba564af91a70780d)

百度网盘链接：https://pan.baidu.com/s/1MxueOHXGQtmE-ypRq1kELA&pwd=9987

2025年7月13号
## 1 入门篇

### 1.1 JavaScript 介绍

**1 什么是 JavaScript 语言？**

> 是一种运行在客户端（浏览器）的编程语言，实现人机交互效果

2 JavaScript的组成（有什么？）

>  1）ECMAScript： 规定了js基础语法核心知识。
>
> 2）DOM： 操作文档，比如对页面元素进行移动、大小、添加删除等操作
>
> 3）BOM：操作浏览器，比如页面弹窗，检测窗口宽度、存储数据到浏览器等等

3 实现页面中点击按钮，显示粉色，其他不显示。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Title</title>
  <style>
    .pink {
      color: pink;
    }
  </style>
</head>
<body>
<button> 按钮1</button>
<button> 按钮2</button>
<button> 按钮3</button>
<button> 按钮4</button>
<script>
  const buttonList = document.querySelectorAll('button');
  buttonList.forEach(button => {
    button.addEventListener('click', (event) => {
      document.querySelector('.pink') && (document.querySelector('.pink').className = '');
      const ele = event.target;
      ele.className = 'pink';
    });
  });
</script>
</body>
</html>
```

