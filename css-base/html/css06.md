通过 CSS 对页面元素内文本内容进行字体设置，除了指定大多数操作系统上常见的字体外，我们还可以指定非标准的、自定义的 web 免费字体，以便在我们的网站上页面使用，达到美化页面的目的。现在联系网上有许多网页字体的来源。由于使用版权的问题，我们一般使用网上免费的字体，本次示例教程使用阿里巴巴普惠体进行配置。
阿里巴巴普惠体是阿里巴巴发布的字体，它将开放商业授权给所有个人和商家，让所有用户可以免费使用。你可以通过引用字体的 URL 或本地文件在 CSS 中使用。本次示例我们通过引用本地文件方式引入字体。现在让我们开始进行阿里巴巴普惠体引入工作吧。
首先从网址 https://alibabafont.taobao.com/wow/alibabafont/act/alifont 下载最新版本的字体文件，将对应的文件放至示例 fonts 目录下。在 style.css 中增加字体引用代码如下：

@font-face {
    font-family: 'AlibabaPuHuiTi-Heavy';
    src: url('../fonts/Alibaba-PuHuiTi-Heavy.otf');
    font-weight: 800;
    font-style: normal;
}

在页面 style 部分增加类 .font-puhuiti-heavy ,  页面使用字体名称必须与 style.css 文件中定义的名称一致。 代码配置如下：

<style type="text/css">

.text-puhuiti-heavy {
   font-family: AlibabaPuHuiTi-Heavy;
   color: white;
}

</style>

在页面标题部分 header 元素类将之前的 text-antiquewhite 改为 text-puhuiti-heavy， 标题部分会显示为普惠体样式，具体样式见效果图片。

一般情况下，有几种默认字体可在所有浏览器中使用。这些通用字体包括 monospace, serif 和 sans-serif。当一种字体不可用时，你可以告诉浏览器“降级”为另一种字体。

例如，如果希望某个元素使用阿里巴巴普惠体字体，但在阿里巴巴普惠体不可用时降级为华文仿宋字体，请按如下方式指定：


<style type="text/css">

.text-puhuiti-heavy {
   font-family: AlibabaPuHuiTi-Heavy STFangsong;
   color: white;
}

</style>

多个字体之间使用空格分开，浏览器会根据这个列表，按顺序查找这些字体，如果访问者的计算机上安装了第一种字体，就可以正确显示。如果没有安装第一种字体，就自动切换到第二种、第三种字体，以此类推。如果所有字体都没有找到，就会从 sans-serif 字体中选择一种可用的字体。

利用这个特性，还可以实现英文和中文使用不同字体的效果。通常的做法是，把英文字体写在前面，中文字体写在后面。如：


<style type="text/css">

.text-antiquewhite {
  font-family: Arial, STFangsong;
}

</style>


这样，浏览器会优先使用 Arial 字体显示文本，由于中文字符不识别 Arial 字体，就会在后面的字体中继续查找，找到 STFangsong  字体后，便对中文应用该字体，这样，就达到了中文和英文使用不同字体的效果。在页面主内容区标题段落文本中增加了字母 A,可以看出中文和字母字体的区别。

注意：通用字体名称不区分大小写。而且它们不需要引号，因为它们是 CSS 关键字。

以下为今天讲述内容的完整代码：

<!DOCTYPE html>
<html>
  <!--注释   页头   -->
  <head> 
    <meta charset="utf-8">
    <!--注释   页头标题   -->
    <title> CSS 层叠样式表基础知识：「06」导入外部字体进行页面元素美化 </title> 
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

        .text-puhuiti-heavy {
           font-family: AlibabaPuHuiTi-Heavy;
           color: white;
        }

        .text-antiquewhite {
            color:  antiquewhite;
            font-family: Arial, STFangsong
        }

        h2 {
          color: red;
        }
        
        #pageBody {
            color: yellow;
        }

    </style>
  </head>
<body id="pageBody">
  <span id="pageTop" name="pageTop"></span>
  <div class="layout">
     <!--页面标题-->
      <header class="header puhuiti-heavy">页面标题-CSS 基础知识</header>
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

            <p >侧栏区</p>
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
            <p class="text-antiquewhite"> 主内容区 A </p>
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
