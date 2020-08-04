今天我们继续介绍通过 CSS 类选择器改变元素样式。我们在 “CSS 基础知识：「03」通过样式表简单选择器修改页面元素样式” 文章中介绍了类选择器，类选择器是可以添加到 HTML 元素中的可重用样式。我们可以定义一个经常使用的文本颜色类。

在“CSS 基础知识：「03」通过样式表简单选择器修改页面元素样式”文章代码基础上，在页面 style 中增加一个文本颜色为古董白的 CSS 类 .text-antiquewhite 声明，代码如下：

<style type="text/css">
    /*CSS 基础知识：「04」文章中增加*/
    .text-antiquewhite {
            color:  antiquewhite;
    }

    h2 {
        color: red;
    }

    #pageBody {
        color: yellow;
    }

    .aside p{
      color: white;
    }

</style>

类选择器定义好后，你可以将类选择器应用到页面标题栏上，代码如下：

<header class="header text-antiquewhite">页面标题-HTML5新标签简介</header>

注意：一个元素上应用多个类时，多个类需要使用空格进行分开。style 中定义的类名以 . 开头。页面代码使用类名时不包含 . 符号。

类选择器允许对多个 HTML 元素使用相同的 CSS 样式。你可以将古董白文本类选择器再次应用于主内容区 p 元素上，实现一个类在同一页面中重复使用的效果。

以下为今天讲述内容的完整代码：

<!DOCTYPE html>
<html>
  <!--注释   页头   -->
  <head> 
    <!--注释   页头标题   -->
    <title> CSS 基础知识：「04」使用 class 类选择器设置元素样式 </title> 
    <link rel="stylesheet" type="text/css" href="./css/style.css">
    <style type="text/css">
        .text-antiquewhite {
            color:  antiquewhite;
        }

        #pageBody {
            color: yellow;
        }

        .aside p{
          color: white;
        }
    </style>
  </head>
<body id="pageBody">
  <span id="pageTop" name="pageTop"></span>
  <div class="layout">
     <!--页面标题-->
      <header class="header text-antiquewhite">页面标题-HTML5新标签简介</header>
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
            <p class="text-antiquewhite"> 主内容区 </p>
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

为了方便大家比较应用类选择器的前后效果，将两张图片放到此页面，效果图片如下：
应该前效果图：

应用后效果图：




