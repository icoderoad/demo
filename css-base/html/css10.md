上一篇文章我们介绍了通过 CSS3 的 border-radius 设置元素的圆角边框。 在 CSS2.1 中给元素添加圆角是是用背景图片实现，制作比较麻烦。CSS3 新增加的 border-radius 属性，使快速制作圆角效果得到完美的解决。利用这个属性，我们可以实现很多想要的图形效果。例如我们在微信中使用的小程序图标是一个圆形的图标效果，要实现类似圆形图标效果，我们通过 border-radius 属性如何实现呢？首先图片要设置为一个正文形，把圆角的半径设置为边长的一半，即可把正方形按圆形显示。

在文章 “「09」通过 CSS 在元素周围添加圆角边框” 代码基础上，将主内容区 “八月你好” 的样式类 img-solid-red-radius 调整为以下代码：

<style type="text/css">

    .img-solid-red-radius {
        width: 100px;
        border-radius: 50px;
    }

</style>

还有一种更灵活的设置方式设置圆角的半径，通过百分比的方式设置为元素尺寸的 50% ，这样方式的设置会使圆的半径随元素的尺寸变化自动调整。 将之前 50px 具体值的设置注释掉，改为百分比方式，调整后代码如下：

<style type="text/css">

    .img-solid-red-radius {
        width: 100px;
        /*border-radius: 50px; */
        border-radius: 50%; 
    }

</style>

设置半圆形跟设置圆形的方法相同，需要调整元素的宽度是高度的 2 倍，且圆角半径等于元素的高度值，就可以得到上半圆或下半圆。调整元素的高度是宽度的 2 倍，且圆角半径等于元素的宽度值，就可以左半圆或右半圆。在页面 style 区增加 4 个类设置，分别为上半圆、下半圆、左半圆和右半圆，增加的代码如下：


<style type="text/css">

    .semicircle-up {
      width: 100px;
      height: 50px;
      border-radius: 100px 100px 0 0;
    }

    .semicircle-down {
      width: 100px;
      height: 50px;
      border-radius: 0 0 100px 100px;
    }

    .semicircle-left {
      width: 50px;
      height: 100px;
      border-radius: 100px 0 0 100px;
    }

    .semicircle-right {
      width: 50px;
      height: 100px;
      border-radius: 0 100px 100px 0;
    }

</style>

将 “八月你好” 照片后面的 4 张图片的类 img-radius-one、 img-radius-two、 img-radius-three、img-radius-four分别调整为 semicircle-up、semicircle-down、semicircle-left、semicircle-right 。预览页面效果如下：




