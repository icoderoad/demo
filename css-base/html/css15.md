今天我们要学习的内容是使用 CSS 的绝对单位与相对单位表示元素长度和尺寸。CSS有多种不同的单位来表示元素的长度和尺寸，CSS 单位需要在样式表中指定长度单位，比如 padding：5px。CSS 中主要有绝对长度和相对长度两种类型的单位。

绝对长度：绝对长度单位是一个固定的值，它反应一个真实的物理尺寸。绝对长度单位视输出介质而定，不依赖于环境（显示器、分辨率、操作系统等）。

相对长度：CSS 相对长度单位中的 “相对” 二字，表明了其长度会随着它的参考值的变化而变化，不是固定的。

常用的绝对长度单位有pt（点）、mm（毫米）、cm（厘米）、in（英寸），pt是一个标准印刷度量单位，一英寸是72 点，即 1pt = 1/72inmm、cm、in 这几个长度单位。在日常网页开发中，绝对长度单位的使用场景很少，我们在本文章中不作详细介绍，简单了解即可。

网页开发中相对长度单位有 px（像素）、em、 rem、%（百分比）、vw、vh、vmin、vmcx、ex、ch 等。今天我们主要介绍 px、 em、 rem 及 % 4种，其他的长度单位在以后文章中使用到再详细介绍。

px（像素）
浏览器内的一切长度都是以 CSS 像素为单位的，CSS 像素的单位是 px，px 是一个相对单位，相对的是设备像素，也就是物理像素，其相对性体现在在同一个设备上或在不同设备之间每 1 个 px 所代表的物理像素是可以变化的。由于我们在之前示例中使用的 px 比较多，今天就不再举例进行演示。

em
em 用来适应用户所使用的字体，1em 与当前的字体尺寸（font-size属性）大小一致，2em 相对于当前字体尺寸的2倍。

1、如果当前元素的父元素设置了 font-size，则 em 参考元素为其父元素
2、如果当前元素的父元素没有设置 font-size，则逐级向上查找有设置 font-size 属性的元素，直到 <html> 根元素
3、如果当前元素的父元素向上所有父元素均没有设置 font-size ，则 em 其参考大小为浏览器默认大小 16px

以侧栏区有序列表为例，将元素的字体大小设置为 14px,行高设置为当前元素的 3 倍，示例代码如下：

<style type="text/css">

    .aside ol {
        font-size: 14px;
        line-height: 3em;
    }

</style>


rem

rem 即 root em，其参考元素为文档的根元素 <html> 中 font-size 属性。

如果文档根元素 <html> 没有设置 font-size 属性，那么当前元素rem相对于浏览器默认字体大小 16px
如果文档根元素 <html style="font-size: 22px"> 设置了 font-size 属性，那么当前元素 rem 相对于文档的根元素 <html>

以侧栏区用户注册表单为例，在文档根元素上增加 style="font-size: 22px" ，将每行的描述文字设置为 1rem, 行高设置为根文档字体大小的 1.1 倍 , 为了使每行显示两个爱好，将每个爱好宽度设置为 80px, 显示方式调整为内联，不然设置宽度不起作用，示例代码如下：

<style type="text/css">

    .aside label {
        display:inline-block;
        width: 80px;
    }

    .aside span {
        font-size: 1rem;
        line-height: 1.1rem;
    }

</style>


% 百分比：
在定义 CSS 样式的时候经常会用的 “%” 这个长度单位，但是这个百分比到底是相对于谁的百分比呢？
块级元素的默认宽度 100% 是相对其父元素的宽度，父元素的宽度相对更上一级元素的宽度. 更准确的说是相对于父元素内容的宽度(不包括内边距)

以侧栏区用户注册表单为例，由于注册表单是通过 grid 方式排版，控件描述及输入控件各占每行的50%。具体 regForm 类的定义，请自行查看 style.css文件。 为了方便查看设置百分比效果，将每列添加相应的边框。

<style type="text/css">

    .regForm .item {
         border: 1px dashed #ccc;
    }

     [title="hobby"]{
        height:3.5em !important;
    }

    .aside label {
        display:inline-block;
        width: 80px;
        line-height: 1.2em;
    }

    .aside span {
        font-size: 1rem;
        line-height: 1.1rem;
    }

    .aside ol {
        font-size: 14px;
        line-height: 3em;
    }

</style>

以上代码增加了 em , rem 及 % 的长度设置方式， 具体效果如下：

