# markdown 基础语法

## 二级标题

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题

Markdown Preview Enhanced 插件 可以再 vscode 预览 输出成 html 或者 pdf 等

## 代码块

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<meta http-equiv="X-UA-Compatible" content="ie=edge" />
		<link rel="stylesheet" href="font-awesome-4.7.0/css/font-awesome.min.css" />
		<title>Document</title>
		<style>
			.fa-camera-retro {
				color: red;
				font-size: 40px;
			}
		</style>
	</head>

	<body>
		<!-- 字体图标     把 图标 做成了  字体 -->

		<!-- 修改 图标 大小  颜色 -->
		<!-- http://fontawesome.dashgame.com/ -->
		<!-- 一套字体图标库 -->
		<!-- 下载图标库 -->
		<!-- 引入css 样式 -->
		<!-- camera-retro 图标名称  需要加fa 前缀 -->
		<!-- 像修改字体一样 修改  图标 -->

		<!-- 通过类名 控制样式 -->

		<i class="fa fa-camera-retro"></i> fa-camera-retro
		<i class="fa fa-automobile"></i>
	</body>
</html>
```

<!-- 使用时 标记和  内容之间 要用空格  隔开 -->

## 表格

| 属性     |         值 |
| :------- | ---------: |
| 背景图片 | background |
| 字体     |       font |

## 列表

1. 列表 1
2. 列表 2

-   liebiaosan
-   列表 4

*   列表 5
*   列表 6

*   缩进 列表嵌套

1. 列表
    - 项目 1
    - 项目 2

_斜体_

**加粗**
~~删除线~~

> 引用一段话

## 图片

-   中括号里 类似 alt 属性 内容
-   相对路径 和 绝对路径
    ![img](banner1.png)
    ![img](http://gcsblog.oss-cn-shanghai.aliyuncs.com/blog/2019-04-29-072758.jpg?gcssloop)

## 链接

-   a 标签

[百度](https://www.baidu.com/)

我是`行内代码`

```
结构标准：结构用于对网页元素进行整理和分类，主要指的是HTML。
样式标准：表现用于设置网页元素的版式、颜色、大小等外观样式，主要指的是CSS。
行为标准：行为是指网页模型的定义及交互的编写，主要包括DOM和ECMAScript两个部分(JavaScript)。
```
