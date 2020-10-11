
![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

使用 flex-shrink 属性收缩项目

目前为止，前面文章里的提到的属性都应用于 flex 容器（flex 子元素的父元素）。除此之外，flex 子元素也有很多实用属性。

首先介绍的是 flex-shrink 属性。使用之后，如果 flex 容器太小，该项目会自动缩小。当容器的宽度小于里面所有项目的宽度，项目就会自动压缩。

flex-shrink 属性接受 number 类型的值。数值越大，与其他项目相比会被压缩得更厉害。例如，如果一个项目的 flex-shrink 为 1 ，另一个项目 flex-shrink 为 3，那么 3 的那个与另一个相比会受到 3 倍压缩。如果所有项目的 flex-shrink 属性都为 1，当空间不足时，都将等比例缩小。如果一个项目的 flex-shrink 属性为 0，其他项目都为 1，则空间不足时，前者不缩小。

注意：负值对该属性无效。

flex-shrink 属性语法示例如下所示：

<style type="text/css">

.item {
  flex-shrink: 3; /* 默认值 1 */
}

</style>

调整页面框架模块 10 内容， 增加样式类 .shrink, flex-shrink 属性值为 0 。在容器内放置 4 个项目，将项目 3 增加样式类 .shrink 。

调整样式代码如下所示：

<style type="text/css">

.shrink {
	flex-shrink: 1;
}

.shrink0 {
	flex-shrink: 0;
}

</style>

调整的 html 代码如下所示：

<article class="article  ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
	<div class="card">
	    <div class="container title justify-content-center">flex-shrink 属性示例</div>
	    <div class="container ft12 ">flex-shrink：如果一个项目的 flex-shrink 属性为0，其他项目都为1，则空间不足时，前者不缩小。</div>
	    <div class="container-dashed wrap align-content-between">
	        <div class="box box-item1 shrink">1</div>
	        <div class="box box-item2 shrink">2</div>
	        <div class="box box-item3 shrink0">3<div>(flex-shrink:0)</div></div>
	        <div class="box box-item4 shrink">4</div>
	    </div>
	</div>
</article>

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html09-show01.png)

<p style="color:red;">
	<b>
	重要提示：示例效果预览，请访问 <a href="https://www.icoderoad.com/demo/" target="_blank">在线示例代码</a>, 完整代码查看及下载，请访问 <a href="https://github.com/icoderoad/demo" target="_blank"> https://github.com/icoderoad/demo</a>。
	</b>
</p>

<p>今天就讲到这里，如果有问题需要咨询，大家可以直接留言或扫下方二维码关注公众号。也可以添加 happyzjp 微信受邀加入学习社群，我们会尽力为你解答。</p>

![](https://www.icoderoad.com/upload/2020/09/icoderoad-41b3e8fe1caa4990b529c875f055e507.png)<br/>
![](https://www.icoderoad.com/upload/2020/09/xy-dc4752b6b7d34ba6b2de3c152c1d2961.png)<br/>
![](https://www.icoderoad.com/upload/2020/09/end-e22f055734c84115a28f03ca03df589a.png)<br/>

<center>
	<b>作者：路条编程（转载请获本网站授权，并注明作者与出处）</b>
</center>