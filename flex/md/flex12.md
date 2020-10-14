
![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。


使用 flex 简写属性设置项目显示方式。

之前文章介绍的几个 flex 属性有一个简写方式。flex-grow、flex-shrink 和 flex-basis 属性可以在 flex 中一同设置。

例如，flex: 1 0 10px; 会把项目属性设为 flex-grow: 1 ，flex-shrink: 0 以及 flex-basis: 10px 。

属性的默认设置是 flex: 0 1 auto;。

flex 属性语法示例如下所示：

<style type="text/css">

.item {
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
}

</style>

flex 属性是 flex-grow, flex-shrink 和 flex-basis 的简写，默认值为 0 1 auto 。后两个属性可选。该属性有两个快捷值：auto (1 1 auto) 和 none (0 0 auto)。

建议您使用此速记属性，而不是设置各个属性。速记属性可以智能地设置其他属性值。

调整模块 13， 增加样式类 .flex-grow,  flex 属性值为 3 1 auto; , 样式类.flex-shrink， 属性 flex 值为 1 2 auto; ，样式类 .flex-basis ，属性 flex 值为 flex: 0 1 10px; 。在容器中增加 3 个项目，项目 1 至 3 的样式类分别为 .flex-grow、.flex-shrink 、.flex-basis。调整的样式类如下所示：

<style type="text/css">
  .flex-grow {
    flex: 3 1 auto;
  }

  .flex-shrink {
    flex: 0 2 auto;
  }

  .flex-basis {
    flex: 0 1 10px;
  }
</style>

调整的 html 代码如下所示：

<article class="article  ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
	 <div class="card">
	    <div class="container title justify-content-center">flex 属性示例</div>
	    <div class="container ft12 ">flex: 是flex-grow, flex-shrink 和 flex-basis的简写</div>
	    <div class="container-dashed wrap align-content-between">
	        <div class="box box-item1 flex-grow">1</div>
	        <div class="box box-item2 flex-shrink">2</div>
	        <div class="box box-item3 flex-basis">3</div>
	    </div>
	</div>
</article>

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html12-show01.png)

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

