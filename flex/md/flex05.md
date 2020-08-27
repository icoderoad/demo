
flex container属性（4）：

justify-content
flex 容器里的 flex 子元素有时不能充满整个容器，所以我们需要告诉 CSS 如何以特定方案排列和调整 flex 子元素。幸运的是，我们有justify-content属性处理这个问题。但在介绍justify-content的可选值之前，我们要先理解一些重要术语。

这张图片的元素横着排列，很好地描述了下面的概念。

回忆一下，把 flex 容器设为一个行，它的子元素会从左到右逐个排列，把 flex 容器设为一个列，它的子元素会从上到下逐个排列。子元素排列的方向被称为 main axis（主轴）。对于行，主轴水平贯穿每一个项目；对于列，主轴垂直贯穿每一个项目。

关于 flex 子元素在主轴排列方式，可以选择以下值：其中一个很常用的是justify-content: center;，可以让 flex 子元素排列在 flex 容器中间。其他可选值还有：

flex-start：从 flex 容器的前端开始排列项目。对行来说是把项目都靠左放，对于列是把项目都靠顶部放。
flex-end：从 flex 容器的后端开始排列项目。对行来说是把项目都靠右放，对于列是把项目都靠底部放。
space-between：项目间保留一定间距地在主轴排列。第一个和最后一个项目会被挤到容器边沿。例如，在行中第一个项目会紧贴着容器左侧，最后一个项目会紧贴着容器右侧，然后其他项目均匀排布。
space-around：与space-between相似，但头尾两个项目不会紧贴容器边缘，空间会均匀分布在所有项目两边


这个例子可以帮助你理解这个属性，在#box-container元素添加 CSS 属性justify-content，其值为 center

![](http://qfbeps0qh.hb-bkt.clouddn.com/go/justify-content.svg)