
flex item（3）：

flex-shrink

使用 flex-shrink 属性收缩项目
目前为止，挑战里的提到的属性都应用于 flex 容器（flex 子元素的父元素）。除此之外，flex 子元素也有很多实用属性。

首先介绍的是flex-shrink属性。使用之后，如果 flex 容器太小，该项目会自动缩小。当容器的宽度小于里面所有项目的宽度，项目就会自动压缩。

flex-shrink属性接受 number 类型的值。数值越大，与其他项目相比会被压缩得更厉害。例如，如果一个项目的flex-shrink为 1 ，另一个项目flex-shrink为 3，那么 3 的那个与另一个相比会受到 3 倍压缩。
