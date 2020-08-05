上一篇文章我们介绍了通过 CSS 在元素周围添加边框，默认添加的边框都是矩形边框。今天我们要介绍的内容是通过 CSS 在元素周围添加圆角边框。在现在的网页设计中，为了美化网页，不让页面展示的那么生硬，为了实现设计的曲线之美，在页面设计中增加了很多圆角设计效果。在 CSS 中我们如何实现相应的圆角效果呢？在 CSS3 中，通过  border-radius 属性实现元素的圆角效果。

定义 border-radius 后，元素 4 个角上对应的圆角属性分别是 border-top-left-radius、border-top-right-radius、border-bottom-right-radius、border-bottom-left-radius，属性的语法格式为：

border-*-*-radius : [ 长度 | 百分比 ]{1,2}


定义 border-*-*-radius 属性时，需要提供一至两个参数值，第一个参数用于椭圆的横轴半径，第二个参数用于椭圆的纵轴半径。如果只提供1个值，表示横轴半径与纵轴半径相等。如果某个值为0，则使用方角，不使用圆角。使用百分比时，横轴半径根据元素的 width 计算得到，纵轴半径根据元素的 height 计算得到。

border-*-*-radius 具体属性描述如下：


border-top-left-radius      左上角的弧度
border-top-right-radius     右上角的弧度
border-bottom-left-radius   左下角的弧度
border-bottom-right-radius  右下角的弧度

通过以上 4 个属性在页面的 style 部分增加图片红色实线圆角样式，修改后的代码如下：


<style type="text/css">

    .img-solid-red-radius{
          border: solid 3px red;
          border-top-left-radius : 15px;
          border-top-right-radius: 10px;
          border-bottom-right-radius: 21px;
          border-bottom-left-radius: 7px;
    }

</style>

将主内容区图片 “八月你好” 类调整为 img-solid-red-radius，具体效果见最终效果图。


通过以上代码给元素设置圆角效果，编码时输写过于繁琐，后期代码维护困难，也容易出错。CSS 提供了一个复合属性 border-radius，来实现与前面 4 个属性相同的效果。属性语法格式为：

border-radius : 长度{1,4} [/ 长度{1,4} ]?

该属性支持一至四个长度值的设置，具体描述如下：

一个值:  四个圆角值相同
两个值:  第一个值为左上角与右下角，第二个值为右上角与左下角
三个值:  第一个值为左上角, 第二个值为右上角和左下角，第三个值为右下角
四个值:  第一个值为左上角，第二个值为右上角，第三个值为右下角，第四个值为左下角


在上面代码基础上，增加 4 个样式圆角的定义如下：

<style type="text/css">

    .img-radius-one{
        border-radius: 10px;
    }

    .img-radius-two{
        border-radius: 10px 20px;
    }

     .img-radius-three{
        border-radius: 10px 20px 15px;
    }

     .img-radius-four{
        border-radius: 10px 20px 15px 8px;
    }

    .img-solid-red-radius{
          border: solid 3px red;
          border-top-left-radius : 15px;
          border-top-right-radius: 10px;
          border-bottom-right-radius: 21px;
          border-bottom-left-radius: 7px;
    }

    .img-solid-red {
        border: solid 3px red;
    }

</style>

在主内容区 “迄今为止拍摄到的最接近太阳的照片” 后面复制3个相同的图片，将每个图片的 class 分别设置为 img-dotted-red img-radius-one 、img-solid-red img-radius-two、 img-dotted-red img-radius-three 、img-solid-red img-radius-four ，按每隔一个图片是虚线、实线的方式设置边框样式。具体效果如下图：


从今天开始，文章中就不再放完整的示例代码了，完整代码过长，影响大家阅读文章内容。为了方便大家可以拿到最新的完整的代码，现将代码放到 github 网站上，具体网址为： https://github.com/icoderoad/demo 。大家可以直接在线查看代码，也可以从对应页面的 code 处选择 Download ZIP 进行文件下载。

示例效果预览，请访问 https://www.icoderoad.com , 完整代码查看及下载，请访问  https://github.com/icoderoad/demo。






