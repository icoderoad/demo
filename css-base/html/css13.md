今天我们要学习的内容是 CSS 盒模型的外边距(margin) 属性。margin 属性允许我们在元素外创建额外的空白区域，这个区域不能放置其他元素，颜色完全透明。外边距可用于帮助将元素定位在页面上的特定位置，提供元素间距离，使所有其他元素保持安全距离 。 margin 属性语法示例如下：
<style type="text/css">

div {
  margin: 20px;
}

</style>

注意： margin 属性作用在内联级元素时，上边和下边的垂直边距不起作用。块级和内联块元素上边和下边的垂直边距可以正常使用。当涉及到外边距和内边距时，内联级别元素的影响与块和内联块元素略有不同。外边距仅在内联级元素的水平方向起作用，垂直方向不起作用。内边距在内联级元素的所有四个边上都起作用。但是，内边距垂直方向的上边和下边可能会与相邻元素的上下行叠加。对于块元素和内联块元素，外边距和内边距使用方式相同。

外边距值设置方式与内边距类似，也可以混用长度值和百分比。如果希望一个元素各边上的外边距不同，同样遵循上、右、下、左的模式，也允许提供 1~4 个值，作用规则与 padding 属性相同。

<style type="text/css">

div {
  margin: 8px 6% 4em 12mm;
}

</style>

CSS 也为外边距提供了单边的属性，上、右、下、左方向的属性分别为：margin-top、margin-right、margin-bottom、margin-left。具体说明如下：

margin-top：		设置元素的上外边距，允许使用负值
margin-right：	设置元素的右外边距，允许使用负值
margin-bottom：	设置元素的下外边距，允许使用负值
margin-left：	设置元素的左外边距，允许使用负值

语法示例如下：

<style type="text/css">

	div {
		  margin-top: 8px;
		  margin-right: 6px;
		  margin-bottom: 4px;
		  margin-left: 12px;
	}

</style>

一个元素的外边距可以是正值，也可以是负值。当元素之间是父子关系时，通过设置子元素的外边距为负值，可以将子元素从父元素中分离出来。以简单用户注册应用的页面导航为例，将侧栏区无序列表第一个设置正值，第二个设置为负值。为了方便看出效果，将无序列表区域设置宽度为 50%, 无序列表容器及具体选项都设置了虚线边框。调整代码如下：

<style type="text/css">

	.aside ul {
	  width:50%;
	  border: 1px dashed #ccc;
	}

	.aside ul>li:nth-child(1) {  
	  border: 1px dashed #ccc;
	  margin: 3px;
	}

	.aside ul>li:nth-child(2) {    
	  border: 1px dashed #ccc;
	  margin: 3px -20px;
	}

</style>

注意： :nth-child(N) 为选择指定元素下对应第几个子元素，本示例为选择无序列表区域下的第一、第二个元素。

预览页面效果如下图：


由上图可以看出，负外边距导致第二个列表值超出了无序列表容器，跑到了无序列表容器外面。在把一个元素的 margin 属性设置为负值时，元素可能部分或完全脱离页面，或覆盖页面上的其他内容，使用时一定要特别小心。






