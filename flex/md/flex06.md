
flex container属性（5）：

align-items
使用 align-items 属性对齐元素:
align-items属性与justify-content类似。回忆一下，justify-content属性使 flex 子元素沿主轴排列。行的主轴是水平线，列的主轴是垂直线。

Flex 容器中，与主轴垂直的叫做 cross axis（交叉轴）。行的交叉轴是垂直的，列的交叉轴是水平的。

CSS 提供了align-items属性，可以用于在交叉轴调整 flex 子元素。对于行，它规定了项目在容器中应该靠上还是靠下，而对于列，就是靠左或靠右。

align-items的可选值包括：

flex-start：从 flex 容器的前端开始排列项目。对行来说是把项目都靠顶部放，对于列是把项目都靠左放。

flex-end：从 flex 容器的后端开始排列项目。对行来说是把项目都靠底部放，对于列是把项目都靠右放。

center：把项目的位置调整到中间。对于行，垂直居中（项目上下方空间相等）。对于列，水平居中（项目左右方空间相等）。

stretch：拉伸项目，填满 flex 容器。例如，排成行的项目从容器顶部拉伸到底部。

baseline：基线对齐地排列。基线是字体相关的概念，可以认为字体坐落在基线上。

![](http://qfbeps0qh.hb-bkt.clouddn.com/go/align-items.svg)