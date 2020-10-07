![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

flex 容器里的 flex 子元素有时不能充满整个容器，所以我们需要告诉 CSS 如何以特定方案排列和调整 flex 子元素。幸运的是，我们有 justify-content 属性处理这个问题。但在介绍 justify-content 的可选值之前，我们要先理解一些重要术语。

![](https://www.icoderoad.com/demo/flex/images/justify-content.png)

这张图片的元素横着排列，很好地描述了下面的概念。

回忆一下，把 flex 容器设为行排列时，它的子元素会从左到右逐个排列，把 flex 容器设为列排列时，它的子元素会从上到下逐个排列。子元素排列的方向被称为 main axis（主轴）。对于行，主轴水平贯穿每一个项目；对于列，主轴垂直贯穿每一个项目。

关于 flex 子元素在主轴排列方式，可以选择以下值：其中一个很常用的是 justify-content: center;，可以让 flex 子元素沿水平主轴排列在 flex 容器中间。

justify-content属性有 5 个属性值，属性值及描述如下所示：

属性值 				        描述
flex-start		：从 flex 容器的前端开始排列项目。对行来说是把项目都靠左放，对于列是把项目都靠顶部放。
flex-end		：从 flex 容器的后端开始排列项目。对行来说是把项目都靠右放，对于列是把项目都靠底部放。
center 			: 居中对齐，可以让 flex 子元素排列在 flex 容器中间。
space-between 	：项目间保留一定间距地在主轴排列。第一个和最后一个项目会被挤到容器边沿。
space-around 	：与space-between相似，但头尾两个项目不会紧贴容器边缘，空间会均匀分布在所有项目两边


调整页面框架模块 3 及 模块 4 的内容， 模块 3 放左对齐、右对齐和居中对齐的 4 个项目， 在两个模块顶部增加浅蓝色居中显示文字 “justify-content 属性示例”， 每个容器上面增加相应的排列属性值及中文描述 ，容器通过带边框来区分不同属性的显示效果。调整样式代码如下所示：

<style type="text/css">
      .ft12 {
        font-size: 12px;
      }
      .title {
        color: #1890ff;
        font-weight: 500;
        text-align: center;
        margin-bottom: 20px;
      }
      .justify-content-start, .justify-content-end, .justify-content-center,
      .justify-content-between, .justify-content-around{
        margin-top: 10px;
      }

      .justify-content-start{
        justify-content: flex-start ;
      }

      .justify-content-end{
        justify-content: flex-end; 
      }

      .justify-content-center{
        justify-content: center;
      }

      .justify-content-between{
        justify-content: space-between;
      }

      .justify-content-around{
        justify-content: space-around;
      }
</style>

模块 3 调整 html 代码如下所示：

<article class="article ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
	<div class="card">
	     <div class="container justify-content-center">
		      <div class="box box-item1">1</div>
		      <div class="box box-item2">2</div>
		      <div class="box box-item3">3</div>
		      <div class="box box-item4">4</div>
	    </div>
	    <div class="container justify-content-center">
	         <img src="../images/arrow1.png" width="60%" class="img1"/>
	    </div>
	    <div class="container container-direction-row-reverse justify-content-center">
		      <div class="box box-item5">5</div>
		      <div class="box box-item6">6</div>
		      <div class="box box-item7">7</div>
		      <div class="box box-item8">8</div>
	    </div>
	    <div class="container container-direction-row-reverse justify-content-center">
	        <img src="../images/arrow2.png" width="60%" class="img2"/>
	    </div>
	    <div class="container justify-content-center">
		       	<div class=" container-direction-column">
		        <div class="box box-item1" >1</div>
		        <div class="box box-item2">2</div>
		        <div class="box box-item3">3</div>
		        <div class="box box-item4">4</div>
	      </div>
	      <div class="box-img"> <img src="../images/arrow3.png" width="60%" class="img3"/></div>
	       <div class=" container-direction-column-reverse">
		        <div class="box box-item5">5</div>
		        <div class="box box-item6">6</div>
		        <div class="box box-item7">7</div>
		        <div class="box box-item8">8</div>
	      </div>
	      <div class="box-img"> <img src="../images/arrow4.png" width="60%" class="img4"/></div>
	    </div>
	</div>
</article>

模块 4 调整 html 代码如下所示：

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

![](https://www.icoderoad.com/demo/flex/images/html05-show01.png)

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