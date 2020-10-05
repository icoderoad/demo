![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

Flex 容器 flex-direction 属性决定了主轴的方向，即项目的排列方向。方向如下图所示：

![](https://www.icoderoad.com/demo/flex/images/flex-direction.png)

这样就建立了 Flex 布局的主轴，从而确定了项目在容器中的方向。可以将 Flex 项目理解为主要分布在水平行或垂直列中。

flex-direction 属性语法示例如下所示：

<style type="text/css">

.container {
  flex-direction: row | row-reverse | column | column-reverse;
}

</style>

此属性有 4 个属性值，属性值及描述如下所示：

属性值 				描述
row（默认值）：主轴为水平方向，起点在左端。 如上图 1 所示
row-reverse：主轴为水平方向，起点在右端。 如上图 2 所示
column：主轴为垂直方向，起点在顶端。如上图 3 所示
column-reverse：主轴为垂直方向，起点在底端。如上图 4 所示

调整模块1 的样式和代码，为了更好的查看 flex 布局项目的效果，增加项目至 8 个，定义每个项目的背景色为绿、蓝、紫、黑、黄、金、红、灰 8 种颜色。上下两部分设置按行( row )及按列( column )方向排列项目。上部第一行按水平轴方向正向排列， 第二行按水平轴逆向排列。下部第一列按垂直轴方向正向排列，第二列按垂直轴方向逆向排列。大家可以根据箭头标识的方向进行正反向区分。调整样式代码如下所示:

<style type="text/css">

	  .container {
          display:flex;
      }

      .justify-content-center{
        justify-content: center;
      }
      .container-direction-row-reverse {
          flex-direction: row-reverse;
      }

       .container-direction-column {
          flex-direction: column;
          width:25%;
      }

      .container-direction-column-reverse {
          flex-direction: column-reverse;
           width:25%;
      }

      .container .img1 {
        margin-left: 8px;
      }

      .container .img2 {
        margin-right: 8px;
      }

      .container .img3 {
        margin-top: 42px;
      }

      .container .img4 {
        margin-top: 42px;
      }


      .box {
        color:white;
        font-size: 26px;
        text-align: center;
        text-shadow:4px 4px 0 rgba(0,0,0,0.1);
        padding:10px;
        vertical-align: middle;
        margin: 5px;
        color: white;
        line-height: 20px;
      }

      .box-img {
        text-align: center;
        vertical-align: middle;
      }

      .box-item1 {background:#1abc9c;}
      .box-item2 {background:#3498db;}
      .box-item3 {background:#9b59b6;}
      .box-item4 { background:#34495e;}
      .box-item5 { background:#f1c40f;}
      .box-item6 { background:#e67e22;}
      .box-item7 { background:#e74c3c;}
      .box-item8 { background:#bdc3c7;}

</style>

调整 html 代码如下所示：

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

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html03-show01.png)

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