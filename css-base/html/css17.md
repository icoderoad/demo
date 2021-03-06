今天我们要学习的内容是使用十六进制颜色设置样式。 在前面文章中，我们文章里多次使用了字体颜色，大部分字体颜色都是通过关键字方式设置的。你知道在 CSS 中还有其他表示颜色的方法吗？其中一种方法被称为十六进制颜色，简称十六进制。我们通常使用十进制，或者以 10 为底的数字，每个数字用 0 到 9 来表示。十六进制是以 16 为基数的数字。这意味着它使用 16 个不同的数字。和小数一样，数字 0-9 代表 0 到 9 的值。那么 A，B，C，D，E，F 代表 10 到 15 的值。总之，0 到 F 可以代表十六进制的一个数字，给我们 16 个可能的值。

在 CSS 中，我们可以使用 # + 红色（R）、绿色（G）和蓝色（B）各两个数字共计 6 个十六进制数字来表示颜色。例如，#000000表示黑色。在文章 “ CSS 层叠样式表基础知识：「16」基于 body 元素的 CSS 样式声明及覆盖 ”代码的基础上，将正文背景色从关键字 Cornsilk 调整为 #FFF8DC 十六进制颜色，调整代码如下：

<style type="text/css">

    body {
      background-color: #FFF8DC;
    }

</style>

预览页面与之前关键字设置时效果一样。

十六进制使用红色（R）、绿色（G）和蓝色（B）各两个 共 6 个十六进制数字来表示颜色。从这三种纯色（红、绿、蓝）我们可以改变每种颜色的数值，创造出超过 1600 万种其他颜色！
例如，橙色是纯红色混合了一些绿色，没有蓝色。在十六进制中 ，使用 #FFA500 表示。数字 0 是十六进制码中最低位的数字，表示完全没有颜色。数字 F 是十六进制代码中的最高位数字，代表最大可能的亮度。


使用下面示例中十六进制替换页面 style 部分元素中的颜色关键字。

颜色            十六进制码
Gold            #FFD700
lime            #00FF00
Orange          #FFA500
white           #FFFFFF

调整部分代码如下：

<style type="text/css">
    #text-orange {
      color: #FFA500;
    }

    .text-gold {
        color: #FFD700;
    }

    .text-lime {
      color: #00FF00 !important;
    }

    body {
      background-color: #FFF8DC;
      color: #FFFFFF;
    }
</style>       

代码调整后保存预览页面，与 “ CSS 层叠样式表基础知识：「16」基于 body 元素的 CSS 样式声明及覆盖 ” 文章预览效果进行比较，页面效果没有变化。说明十六进制码与关键字效果一致。

许多人对超过1600万种颜色的可能性感到不知所措。而且很难记住十六进制代码。幸运的是，你可以缩短它。例如，red 的十六进制代码 #FF0000 可以缩短为 #F00。这个缩写形式给出一个数字表示红色，一个数字表示绿色，一个数字表示蓝色。这将可能的颜色总数减少到4000种左右。浏览器会将 #FF0000 和 #F00 解析为完全相同的颜色。接下来我们尝试使用缩写的十六进制颜色码为元素设置颜色。

颜色            十六进制码
lime            #0F0
white           #FFF
red             #F00

<style type="text/css">
 .text-lime {
    color: #0F0 !important;
  }

  body {
    background-color: #FFF8DC;
    color: #FFF;
  }


  [href~="#pageTop"] {
      color: #fff !important;
      background: #F00;
  }
</style>  

以上主要介绍了颜色的十六进制码 6 位及3位颜色值设置元素样式， 浏览页面效果和 “ CSS 层叠样式表基础知识：「16」基于 body 元素的 CSS 样式声明及覆盖 ”文章的预览效果没有变化。大家可以在示例预览效果域名对比下，主要区别是代码中 color 及 background-color 属性值的变化。调整后最终的页面效果如下：

