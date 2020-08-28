
flex container属性（2）：

使用 flex-wrap 属性包裹一行或一列

CSS flexbox 有一个把 flex 子元素拆分为多行（或多列）的特性。默认情况下，flex 容器会调整项目大小，把它们都塞到一起。如果是行的话，所有项目都会在一条直线上。

不过，使用flex-wrap属性可以使项目换行。这意味着多出来的项目会被移到新的行或列。换行发生的断点由项目和容器的大小决定。

换行方向的可选值有这些：

nowrap：默认值，不换行。

wrap：行从上到下排，列从左到右排。

wrap-reverse：行从下到上排，列从右到左排

![](http://qfbeps0qh.hb-bkt.clouddn.com/go/flex-wrap.svg)