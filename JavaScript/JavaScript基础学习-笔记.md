# 一、JavaScript高级程序设计

[JavaScript高级程序设计](https://github.com/yanminxing/project_doc/blob/main/JavaScript/books/JavaScript%E9%AB%98%E7%BA%A7%E7%A8%8B%E5%BA%8F%E8%AE%BE%E8%AE%A1%EF%BC%88%E7%AC%AC4%E7%89%88%EF%BC%89.pdf)

## 1 什么是 JavaScript

1 的JavaScript 包含以下几个部分

> (1)**核心（ECMAScript）:** 由 ECMA-262 定义并提供核心功能。
>
> ECMAScript，即 ECMA-262 定义的语言，并不局限于 Web 浏览器。事实上，这门语言没有输入和输出之类的方法。ECMA-262 将这门语言作为一个基准来定义，以便在它之上再构建更稳健的脚本语言.
>
> **(2)文档对象模型（DOM）**: 提供与网页内容交互的方法和接口。
>
> 文档对象模型（DOM，Document Object Model）是一个应用编程接口（API），用于在 HTML 中使 用扩展的 XML。DOM 将整个页面抽象为一组分层节点（已：抽象为一棵DOM树）。HTML 或 XML 页面的每个组成部分都是一种节点，包含不同的数据。  注意：DOM 并非只能通过 JavaScript 访问，而且确实被其他很多语言实现了。
>
> **(3)浏览器对象模型（BOM）**：提供与浏览器交互的方法和接口

## 2 HTML 中的 JavaScript

# 二、JavaScript教程--阮一峰

[文档链接](https://wangdoc.com/javascript/basic/introduction)

## 1 入门篇

### 1.1 导论

1 什么是 JavaScript 语言？

> (1) **轻量级的脚本语言**：JavaScript 是一种轻量级的脚本语言。所谓“脚本语言”（script language），指的是它不具备开发操作系统的能力，而是只用来编写控制其他大型应用程序（比如浏览器）的“脚本”。
>
> (2) **嵌入式（embedded）语言**: JavaScript 也是一种嵌入式（embedded）语言。它本身提供的核心语法不算很多，只能用来做一些数学和逻辑运算。JavaScript 本身不提供任何与 I/O（输入/输出）相关的 API，都要靠宿主环境（host）提供，所以 JavaScript 只合适嵌入更大型的应用程序环境，去调用宿主环境提供的底层 API。

>备注：
>
>(1) 目前，已经嵌入 JavaScript 的宿主环境有多种，最常见的环境就是**浏览器**，另外还有**服务器环境**，也就是 Node 项目。
>
>(2) JavaScript 的核心语法部分相当精简，只包括两个部分：**基本的语法**构造（比如操作符、控制结构、语句）和**标准库**（就是一系列具有各种功能的对象比如`Array`、`Date`、`Math`等）。除此之外，各种**宿主环境提供额外的 API（**即只能在该环境使用的接口），以便 JavaScript 调用。以浏览器为例，它提供的额外 API 可以分成三大类。
>
>- **浏览器控制类：操作浏览器**
>- **DOM 类：操作网页的各种元素**
>- **Web 类：实现互联网的各种功能**
>
>如果宿主环境是服务器，则会提供各种操作系统的 API，比如文件操作 API、网络通信 API等等。这些你都可以在 Node 环境中找到。
>
>(3) JavaScript 的发明目的，就是作为浏览器的内置脚本语言，为网页开发者提供操控浏览器的能力



2 强大的性能

> **（1）灵活的语法，表达力强。**
>
> JavaScript 既支持类似 C 语言清晰的**过程式编程**，也支持灵活的**函数式编程**，可以用来写并发处理（concurrent）。
>
> **（2）支持编译运行。**
>
> JavaScript 语言本身，虽然是一种解释型语言，但是在现代浏览器中，JavaScript 都是编译后运行。程序会被高度优化，运行效率接近二进制程序。
>
> **（3）事件驱动和非阻塞式设计。**
>
> JavaScript 程序可以采用事件驱动（event-driven）和非阻塞式（non-blocking）设计，在服务器端适合高并发环境，普通的硬件就可以承受很大的访问量。

3 实验环境

> 进入 Chrome 浏览器的“控制台”
>
> - 直接进入：按下`Option + Command + J`（Mac）或者`Ctrl + Shift + J`（Windows / Linux）
> - 开发者工具进入：开发者工具的快捷键是 F12，或者`Option + Command + I`（Mac）以及`Ctrl + Shift + I`（Windows / Linux），然后选择 Console 面板

### 1.2  JavaScript 的基本语法

[ JavaScript 的基本语法](https://wangdoc.com/javascript/basic/grammar#%E8%AF%AD%E5%8F%A5)

1 语句

> 概念：语句（statement）是为了完成某种任务而进行的操作。JavaScript 程序的执行单位为行（line），也就是一行一行地执行。一般情况下，每一行就是一个语句。语句以分号结尾，一个分号就表示一个语句结束。多个语句可以写在一行内。
>
> 备注：
>
> (1)  表达式：指一个为了得到返回值的计算式。
>
> (2) 语句和表达式的区别: 前者主要为了进行某种操作，一般情况下不需要返回值；后者则是为了得到返回值，一定会返回一个值。
>
> 表达式不需要分号结尾。一旦在表达式后面添加分号，则 JavaScript 引擎就将表达式视为语句，这样会产生一些没有任何意义的语句。
>
> （3）空语句：分号前面可以没有任何内容，JavaScript 引擎将其视为空语句。



# 三、你不知道的JavaScript

## 1 