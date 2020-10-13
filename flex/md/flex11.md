
![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

使用 flex-basis 属性设置项目的初始大小

flex-basis 属性指定了项目在 CSS 进行 flex-shrink 或 flex-grow 调整前项目占据的主轴空间（main size）的初始大小。

flex-basis 属性的单位与其他 size 属性一致（px、em、%等），也可以是关键字。如果值为 auto，项目的大小依赖于自身内容。

flex-basis 属性语法示例如下所示：

<style type="text/css">

.item {
  flex-basis:  | auto; /* 默认值 auto */
}

</style>

如果设置为 0，则不考虑内容周围的多余空间。如果设置为 auto，则多余空间将根据其 flex-grow 值进行分配。


调整模块 12， 增加样式类 .basis,  flex-basis 属性值为 60px, .basis-auto 属性  flex-basis 值为 auto。在容器中增加 3 个项目，增加项目 2 样式类 .basis-auto, 项目 1、项目 3 样式类为 .basis。调整的样式类如下所示：


<style type="text/css">
      .basis {
        flex-basis: 60px;
      }

      .basis-auto{
        flex-basis: auto;
      }
</style>

调整的html 代码如下所示：

<article class="article  ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
 <div class="card">=
    <div class="container title justify-content-center">flex-basis 属性示例</div>
    <div class="container ft12 ">flex-basis: 如果所有项目的属性定义了在分配多余空间之前，项目占据的主轴空间（main size）</div>
    <div class="container-dashed wrap align-content-between">
        <div class="box box-item1 grow basis">1</div>
        <div class="box box-item2 grow3 basis-auto">2</div>
        <div class="box box-item3 grow basis">3</div>
    </div>
  </div>
</article>

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html11-show01.png)

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

