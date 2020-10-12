
![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

使用 flex-grow 属性扩展项目,示意图片如下所示：

![](https://www.icoderoad.com/demo/flex/images/flex-grow.png)

与 flex-shrink 相对的是 flex-grow。你应该还记得，flex-shrink 会在容器太小时对元素作出调整。相应地，flex-grow 会在容器太大时对元素作出调整。

例子与前篇文章相似，如果一个项目 flex-grow 属性的值为 1，另一个 flex-grow 为 3，那么 3 的会比 1 的扩大三倍。

flex-grow 属性语法示例如下所示：

<style type="text/css">

.item {
  flex-grow: 4; /* 默认值 0 */
}

</style>


调整页面框架模块 11 内容， 增加样式类 .grow, flex-grow 属性值为 1 。在容器内放置 4 个项目，将项目 3 增加样式类 .grow3 ，flex-grow 属性值为 3。

调整样式代码如下所示：

<style type="text/css">

  .grow {
    flex-grow: 1;
  }

  .grow3 {
    flex-grow: 3;
  }


</style>

调整的 html 代码如下所示：

<article class="article  ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
	<div class="card">
	    <div class="container title justify-content-center">flex-grow 属性示例</div>
	    <div class="container ft12 ">flex-grow: 如果所有项目的 flex-grow 属性都为 1，则它们将等分剩余空间（如果有的话）。如果一个项目的flex-grow属性为 3，其他项目都为 1，则前者占据的剩余空间将比其他项多两倍。</div>
	    <div class="container-dashed wrap align-content-between">
	        <div class="box box-item1 grow">1</div>
	        <div class="box box-item2 grow">2</div>
	        <div class="box box-item3 grow3">3<div>(flex-grow:3)</div></div>
	        <div class="box box-item4 grow">4</div>
	    </div>
	</div>
</article>

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html10-show01.png)

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