![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

Flex 容器 flex-wrap 属性可以包裹一行或一列 。示意如下图所示：

![](https://www.icoderoad.com/demo/flex/images/flex-warp.png)

CSS Flexbox 有一个把 flex 子元素拆分为多行（或多列）的特性。默认情况下，flex 容器会调整项目大小，把它们都塞到一起。如果是行的话，所有项目都会在一条直线上。

不过，使用 flex-wrap 属性可以使项目换行。这意味着多出来的项目会被移到新的行或列。换行发生的断点由项目和容器的大小决定。

flex-wrap 属性语法示例如下所示：

<style type="text/css">

.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}

</style>

此属性有 3 个属性值，属性值及描述如下所示：

属性值 				        描述
nowrap（默认值）：所有弹性项目都将在一行，不换行
wrap           ：弹性项目将从上到下排列在多行上，换行
wrap-reverse   ：弹性项目将从下到上排列在多行上，换行

为了更好的查看 flex-wrap 属性 3 个值的不同区别，调整页面框架模块 2 的内容。为了区分 3 个属性的效果，将模块 2 分为 3 部分，通过容器的灰色 1 像素、半径 5 像素的圆角边框进行区分，增加带虚线边框的容器类 .container-dashed 。 第一部分容器设置为样式类 .nowrap 为不换行, 第二部分容器设置为样式类 .wrap 为换行从上到下排列， 第三部分设置为样式类 .wrap-reverse 为换行从下到上排列。每个容器放至编号为 1-8 数字的 8 个项目。调整样式代码如下所示：

<style type="text/css">

	   .container-dashed {
          display:flex;
          border: 1px dashed #ccc;
          border-radius: 5px;
          margin-bottom: 20px;
      }

      .nowrap { 
        -webkit-flex-wrap: nowrap;
        flex-wrap: nowrap;
      }

      .wrap { 
        -webkit-flex-wrap: wrap;
        flex-wrap: wrap;
      }  

      .wrap-reverse { 
        -webkit-flex-wrap: wrap-reverse;
        flex-wrap: wrap-reverse;
      }  

</style>

调整 html 代码如下所示：

<article class="article  ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
  <div class="card">
     <div class="container-dashed nowrap">
        <div class="box box-item1">1</div>
        <div class="box box-item2">2</div>
        <div class="box box-item3">3</div>
        <div class="box box-item4">4</div>
        <div class="box box-item5">5</div>
        <div class="box box-item6">6</div>
        <div class="box box-item7">7</div>
        <div class="box box-item8">8</div>
    </div>
    <div class="container-dashed wrap">
        <div class="box box-item1">1</div>
        <div class="box box-item2">2</div>
        <div class="box box-item3">3</div>
        <div class="box box-item4">4</div>
        <div class="box box-item5">5</div>
        <div class="box box-item6">6</div>
        <div class="box box-item7">7</div>
        <div class="box box-item8">8</div>
    </div>
    <div class="container-dashed wrap-reverse">
        <div class="box box-item1">1</div>
        <div class="box box-item2">2</div>
        <div class="box box-item3">3</div>
        <div class="box box-item4">4</div>
        <div class="box box-item5">5</div>
        <div class="box box-item6">6</div>
        <div class="box box-item7">7</div>
        <div class="box box-item8">8</div>
    </div>
  </div>
</article>

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html04-show01.png)

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