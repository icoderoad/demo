
![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

使用 align-self 属性设置单个项目对齐方式。

使用 align-self 属性设置项目对齐方式,示意图片如下所示：

![](https://www.icoderoad.com/demo/flex/images/align-self.png)

align-self 属性语法示例如下所示：

<style type="text/css">

.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}

</style>

flex 子元素的最后一个属性是 align-self。这个属性允许你调整每个项目自己的对齐方式，而不是一次性设置全部项目。

因为 float、clear 和 vertical-align 等调整使用的属性都不能应用在 flex 子元素，所以这个属性显得十分有用。

align-self 的允许值与 align-items 一样，并且它会覆盖 align-items 的值。align-self 属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。

调整模块 14， 增加样式类 .self-start,  align-self 属性值为 lex-start; , 样式类 .self-end， 属性 align-self 值为 flex-end; 。容器中增加样式类 .container-height 设置容器高度，在容器中增加 4 个项目，项目 3 样式类设置为 .self-end, 其他项目都设置为样式类 .self-start。调整的样式类如下所示：

<style type="text/css">
      .self-start {
        align-self: flex-start;
      }

      .self-end {
        align-self: flex-end;
      }
 </style>

调整 html 代码如下所示：

<article class="article  ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
	<div class="card">
	    <div class="container title justify-content-center">self-align 属性示例</div>
	    <div class="container ft12 ">align-self:允许单个项目有与其他项目不一样的对齐方式，可覆盖 align-items 属性。默认值为auto，表示继承父元素的 align-items 属性，如果没有父元素，则等同于stretch。</div>
	    <div class="container-dashed wrap container-height">
	        <div class="box box-item1 self-start">1</div>
	        <div class="box box-item2 self-start">2</div>
	        <div class="box box-item3 self-end">3</div>
	        <div class="box box-item4 self-start">4</div>
	    </div>                 
	</div>
</article>

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html13-show01.png)

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

