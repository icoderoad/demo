今天我们要学习的内容是 CSS 盒模型介绍。页面上的每个元素都可以看作一个盒子，每个盒子都有内容、内边距（padding）、边框（border）、外边距（margin）这 4 个区域组成。内边距、边框、外边距是可选的，并且，都被分解为上、右、下、左 4 个部分。

每个元素有几个属性可以确定该框的大小。盒模型的核心内容区部分由元素的宽度和高度定义，CSS 中通过设置 width 和 height 属性确定。由元素的内容区从内向外扩展依次是 内边距（padding）、边框（border） 和 外边距（margin）。盒子模型的每个部分都对应一个CSS属性：宽度，高度，内边距，边框和外边距。以下面代码为例，查看下元素 div 中定义的相应属性：

<style type="text/css">

div {
  border: 8px solid #949599;
  height: 100px;
  margin: 20px;
  padding: 20px;
  width: 400px;
}

</style>

根据盒子模型的定义，我们可以使用以下公式计算元素的总宽度：

margin-right + border-right + padding-right + width + padding-left + border-left + margin-left

同时，可以使用以下公式计算元素的总高度：

margin-top + border-top + padding-top + height + padding-bottom + border-bottom + margin-bottom




上图片为分解后的盒子模型，包括基本高度和宽度以及内边距，边框和外边距。


使用上面这些公式，我们可以计算出上面示例代码的总高度和宽度。

宽度： 496px = 20px + 8px + 20px + 400px + 20px + 8px + 20px
高度： 196px = 20px + 8px + 20px + 100px + 20px + 8px + 20px

毫无疑问，盒子模型是 CSS 中比较难理解的部分之一。上面示例中，我们设置的 width 属性值 400px ，但是元素的实际宽度是 496px。默认情况下，盒子模型是通过相加的值获得的；因此，要确定盒子的实际尺寸，我们需要考虑盒子所有四个侧面的内边距、边框和外边距。我们的宽度不仅包括 width 属性值，还包括左侧和右侧内边距的大小，左侧和右侧边框以及左侧和右侧外边距。

到目前为止，我们只学习了其中的部分属性。接下来，让我们依次学习组成盒模型的 padding 和 margin 属性。


padding 属性是元素的边框和内容之间的空白区域，用来控制元素边框和内容之间的距离。示例代码如下：


<style type="text/css">

div {
  padding: 20px;
}

</style>

CSS 为 padding 属性提供 1~4 个值，让浏览器根据提供的参数值个数来决定作用对象。规则如下：

一个值：将用于全部的四4个方向

两个值：第一个用于上边、下边，第二个用于左、右边

三个值：第一个用于上边，第二个用于左边、右边，第三个用于下边

四个值：将按上、右、下、左的顺序作用于四边

在文章 “CSS 层叠样式表基础知识：「11」通过 CSS 设置元素背景颜色” 代码基础上， 修改主内容区 h2、h3、h4 元素的 padding属性，调整代码如下：


<style type="text/css">

.main h2 {
  padding: 6px 8px;
}

.main h3 {
  padding: 8px 4px 4px;
}


.main h4 {
  padding: 10px 5px 6px 2px;
}

</style>