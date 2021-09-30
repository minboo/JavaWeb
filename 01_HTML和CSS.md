# HTML和CSS

## 1、B/S 软件的结构

| C/S  | Client Server  |
| ---- | -------------- |
| B/S  | Browser Server |

![image](https://user-images.githubusercontent.com/69302396/135295841-40cf9e79-f1ff-48b0-adcd-6ef264c489b7.png)


## 2、前端的开发流程 

![image](https://user-images.githubusercontent.com/69302396/135295709-71a06633-159b-44c6-acc6-5db198abb26f.png)


## 3、网页的组成部分

页面由三部分内容组成!

>分别是内容（结构)、表现、行为。

>内容（结构)，是我们在页面中可以看到的数据。我们称之为内容。一般内容我们使用html技术来展示。

>表现，指的是这些内容在页面上的展示形式。比如说。布局，颜色，大小等等。一般使用cSS 技术实现行为，指的是页面中元素与输入设备交互的响应。一般使用 javascript 技术实现

## 4、HTML 简介

Hyper Text Markup Language （超文本标记语言） 简写：HTML HTML 

通过标签来标记要显示的网页中的各个部分。网页文件本身是一种文本文件， 通过在文本文件中添加标记符，可以告诉浏览器如何显示其中的内容（如：文字如何处理，画 面如何安排，图片如何显示等）

第一个 html 示例：

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>标题</title>
    </head>
    <body>
        hello
    </body>
</html>
```

注：Java 文件是需要先编译，再由 java 虚拟机跑起来。但 HTML 文件它不需要编译，直接由浏览器进行解析执行。

## 5、HTML 文件的书写规范

```html
<html> 表示整个 html 页面的开始
    <head> 头信息
    	<title>标题</title> 标题
    </head>
	<body> body 是页面的主体内容
        页面主体内容
    </body>
</html> 表示整个 html 页面的结
```

Html 的代码注释 :

```html
<!-- 这是 html 注释，可以在页面右键查看源代码中看到 -->
```

## 6、HTML 标签介绍

	1.标签的格式:
		<标签名>封装的数据</标签名>
	2.标签名大小写不敏感。
	3.标签拥有自己的属性。
		i. 分为基本属性：bgcolor="red" 可以修改简单的样式效果
		ii. 事件属性： onclick="alert('你好！');" 可以直接设置事件响应后的代码。
	4.标签又分为，单标签和双标签。
		i. 单标签格式： <标签名 /> br 换行 hr 水平线
		ii. 双标签格式: <标签名> ...封装的数据...</标签名
![image](https://user-images.githubusercontent.com/69302396/135295950-c9dedd87-f397-4924-a10a-aeb144789f18.png)

## 7、常用标签介绍 文档：w3cschool.CHM
### 7.1、font 字体标签
需求 1：在网页上显示 我是字体标签 ，并修改字体为 宋体，颜色为红色。
```html
<body>
<!-- 字体标签
需求 1：在网页上显示 我是字体标签 ，并修改字体为 宋体，颜色为红色。
font 标签是字体标签,它可以用来修改文本的字体,颜色,大小(尺寸)
color 属性修改颜色
face 属性修改字体
size 属性修改文本大小
-->
<font color="red" face="宋体" size="7">我是字体标签</font>
</body>
```
### 7.2、超链接 （ **** 重 点 ，必 须 掌 握 * ）

需求1：普通的超链接
```html
<body>
	<!-- a 标签是 超链接
	href 属性设置连接的地址
	target 属性设置哪个目标进行跳转
	_self 表示当前页面(默认值)
	_blank 表示打开新页面来进行跳转
	-->
	<a href="http://localhost:8080">百度</a><br/>
	<a href="http://localhost:8080" target="_self">百度_self</a><br/>
	<a href="http://localhost:8080" target="_blank">百度_blank</a><br/>
</body>
```
### 7.3、列表标签
无序列表 、 有序列表

需求 1：使用无序，列表方式，把东北 F4，赵四，刘能，小沈阳，宋小宝，展示出来
```html
<body>
<!--需求 1：使用无序，列表方式，把东北 F4，赵四，刘能，小沈阳，宋小宝，展示出来
	ul 是无序列表
	type 属性可以修改列表项前面的符号
	li 是列表项
-->
	<ul type="none">
		<li>赵四</li>
		<li>刘能</li>
		<li>小沈阳</li>
		<li>宋小宝</li>
	</ul>
</body>

```

### 7.4、img 标签
img 标签可以在 html 页面上显示图片。

需求 1：使用 img 标签显示一张美女的照片。并修改宽高，和边框属性

```html
<body>
	<!--需求 1：使用 img 标签显示一张美女的照片。并修改宽高，和边框属性
	img 标签是图片标签,用来显示图片
	src 属性可以设置图片的路径
	width 属性设置图片的宽度
	height 属性设置图片的高度
	border 属性设置图片边框大小
	alt 属性设置当指定路径找不到图片时,用来代替显示的文本内容
	在 JavaSE 中路径也分为相对路径和绝对路径. 相对路径:从工程名开始算
	绝对路径:盘符:/目录/文件名
	在 web 中路径分为相对路径和绝对路径两种

	相对路径:
	. 表示当前文件所在的目录
	.. 表示当前文件所在的上一级目录
	文件名 表示当前文件所在目录的文件,相当于 ./文件名 ./ 可以省略

	绝对路径:
	正确格式是: http://ip:port/工程名/资源路径
	错误格式是: 盘符:/目录/文件名
-->
	<img src="1.jpg" width="200" height="260" border="1" alt="美女找不到"/>
	<img src="../2.jpg" width="200" height="260" />
	<img src="../imgs/3.jpg" width="200" height="260" />
	<img src="../imgs/4.jpg" width="200" height="260" />
	<img src="../imgs/5.jpg" width="200" height="260" />
	<img src="../imgs/6.jpg" width="200" height="260" />
</body>

```
### 7.5、表格标签（ **** 重点，必须掌握 * )

需求 1：做一个 带表头的 ，三行，三列的表格，并显示边框

需求 2：修改表格的宽度，高度，表格的对齐方式，单元格间距。
```html
<body>
	<!--需求 1：做一个 带表头的 ，三行，三列的表格，并显示边框
	需求 2：修改表格的宽度，高度，表格的对齐方式，单元格间距。
	table 标签是表格标签
	border 设置表格标签
	width 设置表格宽度
	height 设置表格高度
	align 设置表格相对于页面的对齐方式
	cellspacing 设置单元格间距
	tr 是行标签
	th 是表头标签
	td 是单元格标签
	align 设置单元格文本对齐方式
	b 是加粗标签
-->
<table align="center" border="1" width="300" height="300" cellspacing="0">
	<tr>
		<th>1.1</th>
		<th>1.2</th>
		<th>1.3</th>
	</tr>
	<tr>
		<td>2.1</td>
		<td>2.2</td>
		<td>2.3</td>
	</tr>
	<tr>
		<td>3.1</td>
		<td>3.2</td>
		<td>3.3</td>
	</tr>
	</table>
</body>
```
