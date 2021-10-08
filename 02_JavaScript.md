# 1、JavaScript 介绍

Javascript 语言诞生主要是完成页面的数据验证。因此它运行在客户端，需要运行浏览器来解析执行 JavaScript 代码。

JS 是 Netscape 网景公司的产品，最早取名为 LiveScript;为了吸引更多 java 程序员。更名为 JavaScript。

JS 是弱类型，Java 是强类型。

  特点：
  1. 交互性（它可以做的就是信息的动态交互）
  2. 安全性（不允许直接访问本地硬盘）
  3. 跨平台性（只要是可以解释 JS 的浏览器都可以执行，和平台无关）
# 2、JavaScript 和 html 代码的结合方式
## 2.1、第一种方式
只需要在 head 标签中，或者在 body 标签中， 使用 script 标签 来书写 JavaScript 代码

示例代码：
```javascript
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Title</title>
  <script type="text/javascript">
    // alert 是 JavaScript 语言提供的一个警告框函数。
    // 它可以接收任意类型的参数，这个参数就是警告框的提示信息
    alert("hello javaScript!");
  </script>
</head>
<body>
</body>
</html>
```
## 2.2、第二种方式
使用 script 标签引入 单独的 JavaScript 代码文件

文件目录：
![image](https://user-images.githubusercontent.com/69302396/136585120-acdee94f-bd7c-44cb-9cb3-3f3019d9b9b8.png)


html 代码内容：
```javascript
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Title</title>
  <!--现在需要使用 script 引入外部的 js 文件来执行
  src 属性专门用来引入 js 文件路径（可以是相对路径，也可以是绝对路径）
  script 标签可以用来定义 js 代码，也可以用来引入 js 文件
  但是，两个功能二选一使用。不能同时使用两个功能
  -->
  <script type="text/javascript" src="1.js"></script>
  <script type="text/javascript">
  alert("javascript");
  </script>
</head>
<body>
</body>
</html>
```
