
![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

使用 align-content 属性对齐项目,示意图片如下所示：
![](https://www.icoderoad.com/demo/flex/images/align-content.png)


align-content  属性定义了多根轴线的对齐方式。

注意：如果项目只有一根轴线，该属性不起作用。

align-content 属性语法示例如下所示：

<style type="text/css">

.container {
  align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline | first baseline | last baseline + ... safe | unsafe;
}

</style>

align-content 属性有多个属性值，属性值及描述如下所示：

	属性值 			描述
flex-start 		: 与交叉轴的起点对齐。

flex-end 		: 与交叉轴的终点对齐。

center 			: 与交叉轴的中点对齐。

space-between	: 与交叉轴两端对齐，轴线之间的间隔平均分布。

space-around	: 每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。

space-evenly	: 项目与项目的间隔相等，项目与容器边框之间也是同样长度的间隔。

stretch 		: （默认值）：轴线占满整个交叉轴。

调整页面框架模块 7 ，模块 8 内容。 模块 7 分为上中下三部分，每一部分显示 8 个项目， 通过容器类 .container-dashed 进行上中下三部分区分。为了查看容器的显示效果，增加了容器高度类 .container-height。 为了显示 7 种常用属性样式，增加了 .align-content-start、.align-content-end、.align-content-center、.align-content-between、.align-content-around、.align-content-evenly、.align-content-stretch 7 种样式类。第一部分显示 flex-start：交叉轴的起点对齐。容器元素增加样式类 .align-content-start 。 第二部分显示 flex-end：交叉轴的终点对齐。第三部分显示 center : 居中。 第二三部分项目样式设置详情请看 html 代码部分。模块 8 分为四部分，第一部分显示为 space-between: 项目的第一行与交叉轴两端对齐，第二部分显示为 space-around 每根轴线两侧的间隔都相等，第三部分显示为 space-evenly 项目与项目的间隔相等，第四部分显示为 stretch 轴线占满整个交叉轴。


调整 css 代码如下所示：

<style type="text/css">
	.container-height {
	height: 130px;
	}
	.align-content-start {
	align-content: flex-start;
	margin-top: 10px;
	}

	.align-content-end {
	align-content: flex-end;
	margin-top: 10px;
	}

	.align-content-center {
	align-content: center;
	margin-top: 10px;
	}

	.align-content-between {
	align-content: space-between;
	margin-top: 10px;
	}

	.align-content-around {
	align-content: space-around;
	margin-top: 10px;
	}

	.align-content-evenly {
	align-content: space-evenly;
	margin-top: 10px;
	}

	.align-content-stretch {
	align-content: stretch;
	margin-top: 10px;
	}
</style>

模块 7 html 代码调整如下所示：

<article class="article  ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
 <div class="card">
    <div class="container title justify-content-center">align-content 属性示例</div>
    <div class="container">flex-start：交叉轴的起点对齐</div>
    <div class="container-dashed container-height wrap align-content-start">
        <div class="box box-item1">1</div>
        <div class="box box-item2">2</div>
        <div class="box box-item3">3</div>
        <div class="box box-item4">4</div>
        <div class="box box-item5">5</div>
        <div class="box box-item6">6</div>
        <div class="box box-item7">7</div>
        <div class="box box-item8">8</div>
    </div>
    <div class="container">flex-end：交叉轴的终点对齐</div>
    <div class="container-dashed container-height wrap align-content-end">
        <div class="box box-item1">1</div>
        <div class="box box-item2">2</div>
        <div class="box box-item3">3</div>
        <div class="box box-item4">4</div>
        <div class="box box-item5">5</div>
        <div class="box box-item6">6</div>
        <div class="box box-item7">7</div>
        <div class="box box-item8">8</div>
    </div>
    <div class="container">center : 与交叉轴的中点对齐</div>
    <div class="container-dashed container-height wrap align-content-center">
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


模块 8 html 代码调整如下所示：

<article class="article  ant-col ant-col-xs-24 ant-col-sm-12 ant-col-md-12 ant-col-lg-12 ant-col-xl-6">
	<div class="card">
	    <div class="container title justify-content-center">align-content 属性示例</div>
	     <div class="container ft12 ">space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。</div>
	    <div class="container-dashed container-height wrap align-content-between">
	        <div class="box box-item1">1</div>
	        <div class="box box-item2">2</div>
	        <div class="box box-item3">3</div>
	        <div class="box box-item4">4</div>
	        <div class="box box-item5">5</div>
	        <div class="box box-item6">6</div>
	        <div class="box box-item7">7</div>
	        <div class="box box-item8">8</div>
	    </div>
	    <div class="container ft12 ">space-around：每根轴线两侧的间隔都相等。</div>
	    <div class="container-dashed container-height wrap align-content-around">
	        <div class="box box-item1">1</div>
	        <div class="box box-item2">2</div>
	        <div class="box box-item3">3</div>
	        <div class="box box-item4">4</div>
	        <div class="box box-item5">5</div>
	        <div class="box box-item6">6</div>
	        <div class="box box-item7">7</div>
	        <div class="box box-item8">8</div>
	    </div>
	     <div class="container ft12 ">space-evenly：项目与项目的间隔相等，项目与容器边框之间也是同样长度的间隔。</div>
	    <div class="container-dashed container-height wrap align-content-evenly">
	        <div class="box box-item1">1</div>
	        <div class="box box-item2">2</div>
	        <div class="box box-item3">3</div>
	        <div class="box box-item4">4</div>
	        <div class="box box-item5">5</div>
	        <div class="box box-item6">6</div>
	        <div class="box box-item7">7</div>
	        <div class="box box-item8">8</div>
	    </div>
	    <div class="container ft12 ">stretch（默认值）：轴线占满整个交叉轴。</div>
	    <div class="container-dashed container-height wrap align-content-stretch">
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

![](https://www.icoderoad.com/demo/flex/images/html06-show01.png)

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
