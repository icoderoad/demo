今天我们要学习的内容是 CSS 属性选择器。在前面文章中，我们学到了 HTML 元素的多种属性 ，通过元素属性设置对应元素的样式。如通过 width 属性，可以指定元素的宽度；通过 id 属性，可以区分不同的元素等。

在前面文章中，简单用户应用页面大部分使用类选择器来定义样式。由于类选择器并不能说明什么样式服务于什么元素。因此，对于一个大型网站，CSS 代码比较庞大，若要修改某个样式，就成为非常头疼的事情。

我们通过使用 CSS 属性选择器解决以上问题。CSS 属性选择器提供了一种简单而强大的方法，可以根据特定属性或属性值是否存在将样式应用到 HTML 元素。

你可以通过将属性（可选地带值）放在一对方括号中来创建属性选择器，也可以在其前面放置一个元素类型选择器。

[属性] 这是属性选择器的最简单形式，如果给定属性存在，则将样式规则应用到此元素。例如，我们可以设置带有 title 属性属性的元素的样式为以下代码：

<style type="text/css">

[title] {
 color: white;
}

</style>

如果指定元素设置了类选择器，由于类选择器与属性选择器权重相等，相等权重的按位置覆盖，不同权重的选择器，位置变了也不会覆盖。权重计算规则如下：

1、内联样式，如: style="..."，权重值为1000。
2、ID选择器，如：#content，权重值为 100。
3、类，伪类、属性选择器，如 .content，权重值为 10。
4、元素选择器、伪元素选择器，如 div p，权重值为 1。
5、通配符、子选择器、相邻选择器等。如* > +，权重值为 0。
6、继承的样式没有权值

还可以通过将属性选择器放置在元素选择器之后，将选择范围限制为特定的 HTML 元素，示例代码如下：

<style type="text/css">

a[title] {
 color: white;
}

</style>

选择器 a[title] 仅匹配具有 title 属性的 a 元素，因此它匹配 a 元素，但不匹配具有属性的 p 元素。


使用 = 运算符选择属性值与给定值完全相等的任何元素：

<style type="text/css">

input[type="submit"] {
    border: 1px solid green;
}

</style>

以上示例中的选择器匹配 <input> 具有 type 属性值等于 submit 的所有元素。


使用 ~= 运算符选择包含属性值或以空格分隔的值（例如 href~="#pageTop" ）的元素，其中一个值等于指定的值，示例代码如下：

<style type="text/css">

[href~="#pageTop"] {
    color: #fff !important;
    background: red;
}

</style>


该选择器将匹配任何具有 href 属性且包含 #pageTop 属性值的 a 元素。例如，它匹配具有属性值为 #pageTop或 #pageTop warning 的 a 元素。


使用 |= 运算选择与属性具有以指定的值开头且包含连字符分隔值的任何元素，示例代码如下：

<style type="text/css">

[lang|=en] {
    color: #fff;
    background: blue;
}

</style>

该选择器匹配具有 lang 属性且包含以 en 开头，无论该值后面是否带有连字符和更多字符的所有元素。换句话说，它匹配具有属性值 en、en-US、en-GB 等的 lang 元素，但不匹配属性值为 US-en、GB-en 等的 lang 元素。

使用 ^= 运算符选择指定值开头的元素，它可以是一个完整的词，也可以是属性值开头包含指定值。示例代码如下：

<style type="text/css">

a[href^="http://"] {
    background: url("external.png") 100% 50% no-repeat;
    padding-right: 15px;
}

</style>

该选择器将匹配所有 href 属性值以 http:// 开头的超链接，在超连接上添加一个小图标，指示它们将在新的选项卡或窗口中打开。


使用 $= 运算符选择拥有属性 href ，且属性值以 val 结尾的元素，val 为完整的单词或单词的一部分。示例代码如下：

<style type="text/css">

a[href$=".doc"] {
    background: url("doc.png") 0 50% no-repeat;
    padding-left: 20px;
}

</style>

该选择器将匹配所有包含属性 href 且属性值以 doc 结尾的所有超链接元素，并添加一个小的 doc 图标，向用户提供相关链接文件类型。

使用 *= 运算符选择拥有属性 attribute，且属性的值包含 val 子字符串的所有元素。示例代码如下：


<style type="text/css">

[class*="warning"] {
    color: #fff;
    background: red;
}

</style>

该选择器将选择所有 class 属性值包含 warning 的元素。例如，该选择器将匹配具有类值为 warning、alert warning、alert-warning或alert_warning 的元素。


以简单用户注册应用页面为例，在导航第一个超链接增加属性 title="header标签" ， 页面 style 代码区增加 3 个属性选择器，调整代码如下：
<style type="text/css">

 	[href~="#pageTop"] {
	    color: #fff !important;
	    background: red;
	}

	input[type="submit"] {
	    width: 33%;
	    border: 2px dotted green;
	}


	a[title] {
	    color:white;
	}

</style>

以上代码属性选择器对导航区第一个链接、侧栏区注册按钮及主内容区返回顶部起作用，具体效果如下图:


