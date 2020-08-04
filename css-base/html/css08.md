今天我们要介绍的内容是通过 CSS 在元素周围添加边框。在元素周围添加边框最简单的办法是通过 border 属性实现。border 属性的语法为

border: 边框样式（border-style） | 边框宽度（border-width） | 边框颜色（border-color）

border 属性是一个复合属性，可以分解为边框样式（border-style）、边框宽度（border-width）、边框颜色（border-color）这 3 个属性，也可以单独设置相应的属性为元素添加边框。具体语法介绍如下：

border-style：边框样式

border-style 属性是用来设置元素的边框样式，如果没有显式定义 border-style 属性，或把 border-style 属性设置为 none，元素将没有边框，并忽略 border-color 属性 和 border-width 属性。

border-style 属性的取值为预定义关键字，CSS内置了 10 种不同的边框样式，每个样式都由一个预定义关键字来定义。以下为具体样式的关键字值及描述：

none    无边框
hidden  隐藏边框
dotted  点状线
dashed  虚线
solid   实线
double  双线
groove  3D凹槽
ridge   3D凸槽
inset   3D凹边
outset  3D凸边

border-width：边框宽度

border-width 属性用来设置元素边框的粗细程度，可以使用长度值表示具体的数值，如2px 或 0.5em，不允许负值。 也可以使用预定义关键字 thin | medium | thick，默认值为 medium。如果未显式声明 border-width 属性，则边框的宽度或者为零，或者为浏览器的默认值。border-width 属性需要 4 个参数值，也采用 top-right-bottom-left 的顺序。语法示例如下：

border-width: 1px 3px 1px 2px;

上述规则就表示上边框的宽度为 1px、右边框的宽度为 3px、下边框的宽度为 1px、左边框的宽度为 2px。

也可以使用单边属性，按上、右、下、左的顺序，border-width 对应的属性依次为 border-top-width、border-right-width、border-bottom-width、border-left-width 4 个属性。语法示例如下：

border-top-width: 1px; /*设置元素上边框宽度*/
border-right-width: 3px; /*设置元素右边框宽度*/
border-bottom-width: 1px; /*设置元素下边框宽度*/
border-left-width: 2px; /*设置元素左边框宽度*/

上述规则实现效果与 border-width 属性设置效果一样。

border-color：边框颜色

border-color 属性用来设置元素边框的颜色，其值可以是任意合法CSS的颜色，如预定义的颜色名、十六进制数值、RGB等。border-color 属性需要 4 个参数值，也采用 top-right-bottom-left 的顺序，语法示例如下：

border-color: blue black green red;

上述规则就表示上边框的颜色为蓝色、右边框的样式为黑色、下边框的样式为绿色、左边框的样式为红色。


我们在定义上边框单边属性时，每次都要使用类似 border-top-style、 border-top-width、border-top-color 这样的属性，代码写起来比较繁琐。于是，CSS 增加了单边定义的复合属性，同样按上、右、下、左的顺序，对应的单边属性依次为 border-top、border- right、border-bottom、border-left，它们的语法相同，语法示例如下：

border-top: 边框样式（border-style>）| 边框宽度（border-width）| 边框颜色（border-color）

有了这些属性，就可以创建出一些复杂的边框效果。

在文章 “CSS 层叠样式表基础知识：「07」通过 CSS 控制图片大小” 代码基础上， 我们增加两个图片元素的边框定义，在页面 style 区增加如下代码：

<style type="text/css">

    .img-dotted-red{
        border: dotted 3px red;
    }

    .img-complex{
        border-top: 8px dashed pink;
        border-right: 8px solid #da4f49;
        border-bottom: 8px dotted greenyellow;
        border-left: 8px double #faa732;
    }

</style>

在页面主内容区的第一张图片增加 class="img-dotted-red" ， 第二张图片增加 class="img-complex"，代码如下所示：


 <p>
  <img src="./images/html07-show01.jpg" alt="八月你好" class="img-dotted-red" >
  <a href="#">
  <img src="./images/sun.jpg" alt="迄今为止拍摄到的最接近太阳的照片"  title="迄今为止拍摄到的最接近太阳的照片" class="img-complex">
  </a>
</p>

根据上面的说明及示例，大家可以修改代码中对应 CSS 类的边框样式、宽度或颜色，重新预览查看对应的边框效果。

注意：边框样式只能从预定义关键字列表选择，如果关键字输入错误，将不显示对应的元素边框。



