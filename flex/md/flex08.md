
![](https://www.icoderoad.com/demo/flex/images/flexbox.png)

欢迎关注路条编程网站，通过学习 CSS Flexbox 弹性布局这一系列文章，你将会逐步掌握 Flex 布局相关的知识。

使用 order 属性设置项目排列顺序,示意图片如下所示：

![](https://www.icoderoad.com/demo/flex/images/order.png)

order 属性可以控制 CSS flex 容器里项目的顺序。默认情况下，项目排列顺序与源 HTML 文件中顺序相同。这个属性接受数字作为参数，可以使用负数。数值越小，排列越靠前，默认为0。

order 属性语法示例如下所示：

<style type="text/css">

.item {
  order: 5; /* 默认值为 0 */
}

</style>

调整页面框架模块 9 内容， 增加容器类 .container-dashed ,在容器内放置 4 个项目，调整项目 3，4 的排列顺序，增加两个排序样式类 .order1, .order2，设置样式类 .order1 的 order 属性为 -2, .order2 的 order 属性为 -1。调整排序后的项目排列为 4、3、1 、2。

保存页面代码，预览页面，整体效果图如下所示：

![](https://www.icoderoad.com/demo/flex/images/html08-show01.png)

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