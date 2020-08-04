今天我们要介绍的内容是通过 CSS 样式表改变文本颜色。通过 CSS 改变页面文本的颜色有3种方式，下面我们分别介绍3种方式的具体方法。

第1种内联方式：

通过在指定页面标签上设置 style属性，改变文本颜色的样式为 color 属性。以下为如何改变侧栏区无序列表标题颜色为蓝色的示例。

<p style="color: blue;">无序列表</p>

注意：输写样式时以一个“ ; ”结尾是一个好的编码习惯。

第2种嵌入方式：

第1种方案虽然可以改变页面元素的文本颜色，但它有一个很明显的缺点。只能改变页面当前标签的样式，如果想要页面里多个标签都使用同一种样式，每个元素都要添加 style 属性，这样不仅导致HTML代码冗长难以阅读，而且后期维护起来也非常困难。 所以我们一般不会大量使用这种方式添加样式，因而有了第2种内嵌方式。
第2种方式是通过在页面 <head> 元素中增加 style 方式实现。代码示例如下：

<!DOCTYPE html>
<html>
	<head>
	    <style type="text/css">
	         .aside p{
		          color: white;
		        }
	    </style>
	</head>
	<body></body>
</html>

该方式指定了侧栏区所有 p 元素文本颜色为白色，注意：第1种方式指定了侧栏区无序列表标题颜色为蓝色，由于内联方式优化级高于嵌入方式，所以侧栏区无序列表标题颜色仍为蓝色。

该方法虽然解决了第1种内联方式带来的多元素不能重用同一个样式的问题，但是同时又暴露出了另一个问题，没有办法和其他页面共用，只能本页面使用。所以当多个页面需要引入相同的 CSS 代码时，这样写会导致代码冗余，也不利于维护。

第3种外部方式：

通过在 <head> 元素中使用 <link> 元素来引入外部样式表文件，代码示例如下：

<!DOCTYPE html>
<html>
	<head>
    	<link rel="stylesheet" type="text/css" href="./css/style.css">
	</head>
	<body></body>
</html>

这是我们网页开发中最常见的也是最推荐的引入 CSS 的方式，具备良好的可维护性。如果多个页面共用一个 CSS 文件的话，一般只在第一次加载时需要下载，再次打开页面时根本不需要加载该文件，直接从本地浏览器缓存获取，加快了页面打开速度。

注意：3种方式的优先级为：内联式 > 嵌入式 > 外部式，但是嵌入式 >外部式有一个前提：嵌入式css样式的位置一定在外部式的后面。

在原有简单用户注册代码基础上，我们将之前嵌入方式的 CSS 代码调整至外部 CSS 样式表文件 style.css 中，在 html02.html 页面所在目录创建 css 目录，将 style.css文件放至 css 目录，引用当前目录下的文件为 ./目录名/样式表文件名.css。

代码结构如下图：

如果你想在本机查看示例效果，只需要将 style.css 文件代码复制到本地 style.css文件中。 html02.html代码复制至本地 html02.html 文件中。具体页面结构如上图。

style.css 文件完整代码如下：


*{
    margin: 0;
    padding: 0;
}

a{
    text-decoration: none;
}
.clears {
    clear: both;
    height: 0;
    line-height: 0;
    font-size: 0;
    overflow: hidden;
}
body {
    margin: 0 auto;
}

.layout{
    widht: 1920px;
    height: 740px;
    background-color:white;
    padding-top: 20px;
}
.header {
    height: 50px;
    width: 1300px;
    background-color: #90c840;
    color: white;
    margin: 20px auto 30px;
    text-align: center;
    line-height: 50px;
    font-size: 30px;
    cursor: pointer;
}


.nav {
    background-color:#edad21;
    height: 60px;
    width: 1300px;
    margin-bottom: 40px;
    margin-left: auto;
    margin-right: auto;
    line-height: 30px;
}
.menu{
    width: 1300px;
    height: 60px;
    display: inline-block;
}
.menu ul{
    list-style:none;
    display: inline-block;
}
.menu{
    vertical-align: middle;
}

.menu li{
    vertical-align: middle;
    display: inline-block;
    width: 250px;
    height: 50px;
    margin-top: 5px;
    text-align: center;
    margin-left: 5px;
    line-height: 50px;
    font-size: 25px;
    background-color:dimgrey;
}
a:link{
    color:greenyellow;
}
a:hover{
    color: darkorange;
}
.content {
    height: 450px;
    width: 1300px;
    margin-bottom: 20px;
    margin-left: auto;
    margin-right: auto;
}

.aside {
    height: 450px;
    background-color: #ec1f85;
    text-align: center;
    line-height: 50px;
    font-size: 25px;
    width: 350px;
    float: left;
}
.aside ul, .aside ol{
    text-align: left;
    line-height: 30px;
    font-size: 15px;
    width: 270px;
    margin-left: 50px
}
.aside p{
  margin-left: 10px
  text-align: left;
}
.aside .row span{
  font-size: 15px;
}

.main {
    height: 440px;
    background-color:#009dda;
    width: 935px;
    float: left;
    text-align: center;
    line-height: 35px;
    position: relative;
    left: 15px;
    margin-bottom: 20px;
    font-size: 25px;
    padding-top: 10px;
}
.main p a:link{
    color: blue;
    size: 15px;
}
.main p a:hover{
    color: red;
    size: 15px;
}
.footer {
    height: 80px;
    background-color:#dbdb00;
    width: 1300px;
    text-align: center;
    margin-top: 15px;
    margin-left: auto;
    margin-right: auto;
    line-height: 80px;
    font-size: 25px;
}

.life{
    color: white;
    line-height: 50px;
    font-size: 30px;
}
.mt-10{margin-top: 10px;}

.row {
  display: grid;
  grid-template-columns: 50% 50%;
  grid-template-rows: 50% 50%;
}

.row  .item {
  line-height: 15px;
  justify-items: start;
  justify-content: start;
}

html02.html文件完整代码如下：

<!DOCTYPE html>
<html>
  <!--注释   页头   -->
  <head> 
    <!--注释   页头标题   -->
    <title> CSS 基础知识：「02」通过样式表修改页面文本颜色 </title> 
    <link rel="stylesheet" type="text/css" href="./css/style.css">
    <style type="text/css">
        .aside p{
          color: white;
        }
    </style>
  </head>
<body>
  <span id="pageTop" name="pageTop"></span>
  <div class="layout">
     <!--页面标题-->
      <header class="header">页面标题-HTML5新标签简介</header>
       <!--页面导航-->
      <nav class="nav">
        <ul class="menu">
              <li><a href="#">页面导航-header标签</a></li>
              <li><a href="#">nav标签</a></li>
              <li><a href="#">aside标签</a></li>
              <li><a href="#">main标签</a></li>
              <li><a href="#">footer标签</a></li>
          </ul>
      </nav>
      <article class="content">
          <!--侧栏区-->
          <aside class="aside">

            侧栏区
            <div class="row">
              <div>
              <p style="color: blue;" >无序列表</p>
              <ul>
                <li>飞机</li>
                <li>战斗机</li>
                <li>无人机</li>
              </ul>
            </div>
            <div>
              <p>有序列表</p>

              <ol>
                <li>飞机</li>
                <li>战斗机</li>
                <li>无人机</li>
              </ol>
            </div>
            </div>

             <p>用户注册</p>

            <form action="#" method="post">
                <div class="row mt-10">
                    <span class="item">用户名：</span>
                    <span class="item">
                      <input type="text" value="" placeholder="请输入用户名" required="required" >                 
                    </span>
                </div>
                <div class="row mt-10">
                    <span class="item">性别：</span>
                    <span class="item">
                      <label for="male"><input type="radio" value="male" id="male" placeholder="男" name="sex" required="required" checked="checked"> 男 </label>
                       <label for="female"><input type="radio" name="sex"  value="female" id="female" placeholder="女" required="required" > 女 </label>          
                    </span>
                </div>
                <div class="row mt-10">
                    <span class="item">爱好：</span>
                    <span class="item">
                       <label for="dushu"><input type="checkbox" name="hobby" value="dushu"   id="dushu" checked="checked">读书</label>
                       <label for="tiyu"><input type="checkbox"  name="hobby" value="tiyu"    id="tiyu"  >体育</label>
                       <label for="yinyue"><input type="checkbox" name="hobby" value="yinyue" id="yinyue">音乐</label>
                       <label for="youxi"><input type="checkbox" name="hobby" value="youxi"   id="youxi">游戏</label>
                       <label for="bagua"><input type="checkbox" name="hobby" value="bagua"   id="bagua">八卦</label>
                       <label for="tucao"><input type="checkbox" name="hobby" value="tucao"   id="tucao">吐槽</label>        
                    </span>
                </div>

                <div class="mt-10"><input type="submit" value="注册" ></div>
             </form>
          </aside>
          <!--主内容区-->
          <main class="main">
            <p> 主内容区 </p>
                <p> &nbsp; </p>
            <!-- <h1>嘿，你好，欢迎来到路条编程公众号！</h1> -->
          <h2>嘿，你好，欢迎来到路条编程公众号！</h2>
          <h3>嘿，你好，欢迎来到路条编程公众号！</h3>
          <h4>嘿，你好，欢迎来到路条编程公众号！</h4>
          <br>
          <!-- 
          <h5>嘿，你好，欢迎来到路条编程公众号！</h5>
          <h6>嘿，你好，欢迎来到路条编程公众号！</h6>
          -->
          <p class="life">生活不仅是眼前的苟且，还有<a href="https://baike.baidu.com/item/%E8%AF%97%E5%92%8C%E8%BF%9C%E6%96%B9/19483889" target="_blank">诗和远方</a>。</p> 

          <a href="#">
          <img src="https://mmbiz.qpic.cn/mmbiz_jpg/iciaYydulQQ938RSBlZICkZcFgBDbnN9LicG0Vib2H8iarZsgmPeCibyg4fhEcFcHlicO3EyH2ds6Qrc4NFyA8BbPohuQ/0?wx_fmt=jpeg" alt="迄今为止拍摄到的最接近太阳的照片"  width="200" title="迄今为止拍摄到的最接近太阳的照片">
          </a>

          <br/>
          <a href="https://www.taobao.com" >淘宝网(当前页打开)</a> <a href="https://www.taobao.com" target="_blank">淘宝网(新页面打开)</a> &nbsp; &nbsp; <a href="#pageTop">返回顶部</a>

          </main>
      </article>
       <!--页脚-->
      <footer class="footer">页脚-&copy;路条编程版权所有</footer>
      <div class="clears"></div>
  </div>
</body>
</html>

页面最终效果图如下：

