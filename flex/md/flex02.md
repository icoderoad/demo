
![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

Flex 容器是通过 display 属性设置的，要创建一个 Flex 容器，必须将父容器样式中的 display 属性设置为 flex 或 inline-flex 。

容器图片如下所示：

![](https://www.icoderoad.com/demo/flex/images/container.png)

任何一个容器都可以指定为 Flex 布局。

<style type="text/css">

.container {
  display: flex; 
}

</style>

行内元素也可以使用 Flex 布局。

<style type="text/css">

.container{
  display: inline-flex;
}

</style>

调整页面框架的模块 1 的内容， 增加一个 Flex 容器，容器样式设置为 flex, 容器内增加 3 个项目 ，样式类分别为.box .box-item1 、box-item2、box-item3, 样式类 .box 设置盒子整体样式， 项目1、2、3 设置背景色分别为绿、蓝色、紫色，外边距设置为 5px , 文本设置水平垂直居中显示，宽度设置 27% ,文本颜色设置白色。调整的样式类代码如下所示：

<style type="text/css">

	  .container {
          display:flex;
      }

      .box {
        color:white;
        font-size: 30px;
        text-align: center;
        text-shadow:4px 4px 0 rgba(0,0,0,0.1);
        padding:10px;
      }

      .box-item1 {
          vertical-align: middle;
          margin: 5px;
          background:#1abc9c;
          color: white;
          text-align: center;
          width: 27%;
      }

      .box-item2 {
          vertical-align: middle;
          margin: 5px;
          background:#3498db;
          color: white;
          text-align: center;
           width: 27%;
      }

      .box-item3 {
          vertical-align: middle;
          margin: 5px;
          background:#9b59b6;
          color: white;
          text-align: center;
          width: 27%;
      }

</style>

调整 html 代码如下所示：

<article class="article ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
	<div class="card">
	     <div class="container">
	      <div class="box box-item1">1</div>
	      <div class="box box-item2">2</div>
	      <div class="box box-item3">3</div>
	    </div>
	</div>
</article>

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html02-show01.png)

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