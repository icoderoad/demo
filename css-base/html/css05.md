前面的文章中我们介绍了通过 CSS 选择器控制元素的样式，默认情况下都是修改页面文本的字体颜色。如果要改变元素中文本的字体大小怎么操作呢，在 CSS 中，是通过 font-size 属性来设置元素中所含文本的字体大小。

通过 CSS 定义 font-size 属性时，可以使用预定义关键字、绝对尺寸、相对尺寸三种方式实现。我们今天要介绍的是现在网页中使用最多的绝对尺寸方式，绝对尺寸包含 px（像素）、pt（点，1pt 相当于 1/72in）、in（英寸）、cm（厘米）、mm（毫米）等。页面中使用比较多的是像素方式，今天的文章主要介绍像素方式。像素类选择器方式的代码示例如下：

<style type="text/css">

    .font-px-30 {
        font-size:30px;
    }

</style>

注意：如果以 px 为单位设置字体大小，使用 IE 浏览器的用户，就不能在浏览器上通过设置“文字大小”来对文本进行放大或缩小。

CSS 定义了 5 种通用字体，分别是 serif、sans-serif、cursive、fantasy、monospace，font-family ，可用使用其中的任何一种。一般中文网站页面默认情况下使用的字体为宋体，如果想改变页面字体为其他字体，CSS 通过 font-family 属性来设置。在类 font-px-30 增加 font-family 属性，将字体设置为华文仿宋，代码如下：

<style type="text/css">

    .font-px-30 {
        font-size:30px;
        font-family: STFangsong;
    }

</style>


为了容易区分设置的文本字号及字体，在“ CSS 层叠样式表基础知识：「04」使用 class 类选择器设置元素样式 ” 文章代码基础上，将主内容区中 “生活不仅是眼前的苟且，还有诗和远方。” 文本的字号设置为 18px, 在“诗和远方”链接上增加类 font-px-30, 字号设置为 30px, 字体设置为华文仿宋， 在 style区，覆盖样式表 style.css 文件中的 life 类，调整后代码如下：

<style type="text/css">

    .font-px-30 {
        font-size:30px;
        font-family: STFangsong;
        color:greenyellow;
    }

    .life {
      line-height: 30px;
      font-size:18px;
    }

</style>

注意：在设置字体时，如果字体名称中包含空格或中文或其他特殊字符，则要把整个字体名称用放在引号中，可以使用单引号，也可以使用双引号。并且，字体名称不区分大小写。

由于我们大部分页面使用的是中文，对于中文，有三种指定字体的方法：
1、直接使用中文字体名称
2、使用英文字体名称
3、使用字体的 unicode 码
但是，在 CSS 文档中定义字体时，如果直接书写中文，经常会出现乱码，或者在某些浏览器下字体不生效。一个常用的解决办法，是把中文字体名称转换为对应的英文字体名称或 unicode 码。如，宋体的英文字体名称为 SimSun、unicode 码为 \5B8B\4F53。

以下为今天讲述内容的完整代码：

<!DOCTYPE html>
<html>
  <!--注释   页头   -->
  <head> 
    <!--注释   页头标题   -->
    <title> CSS 基础知识：「05」使用类选择器设置元素包含文本字号及字体 </title> 
    <link rel="stylesheet" type="text/css" href="./css/style.css">
    <style type="text/css">
         .font-px-30 {
            font-size:30px;
            font-family: STFangsong;
            color:greenyellow;
        }

        .life {
          line-height: 30px;
          font-size:18px;
        }

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
  </head>
<body id="pageBody">
  <span id="pageTop" name="pageTop"></span>
  <div class="layout">
     <!--页面标题-->
      <header class="header text-antiquewhite">页面标题-CSS 基础知识</header>
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
          <p class="life">生活不仅是眼前的苟且，还有<a href="https://baike.baidu.com/item/%E8%AF%97%E5%92%8C%E8%BF%9C%E6%96%B9/19483889" target="_blank" class="font-px-30">诗和远方</a>。</p> 

          <a href="#">
          <img src="https://mmbiz.qpic.cn/mmbiz_jpg/iciaYydulQQ938RSBlZICkZcFgBDbnN9LicG0Vib2H8iarZsgmPeCibyg4fhEcFcHlicO3EyH2ds6Qrc4NFyA8BbPohuQ/0?wx_fmt=jpeg" alt="迄今为止拍摄到的最接近太阳的照片"  width="200" title="迄今为止拍摄到的最接近太阳的照片">
          </a>

          <br/>
          <a href="https://www.taobao.com" >淘宝网(当前页打开)</a> <a href="https://www.taobao.com" target="_blank">淘宝网(新页面打开)</a> &nbsp; &nbsp; <a href="#pageTop">返回顶部</a>

          </main>
          <div class="clears"></div>
      </article>

       <!--页脚-->
      <footer class="footer">页脚-&copy;路条编程版权所有</footer>
      <div class="clears"></div>
  </div>
</body>
</html>


页面效果图如下：

为了方便大家查看之前文章的示例效果，已经将示例文件更新至网站: https://www.icoderoad.com , 目录索引如下图：



