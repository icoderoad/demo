之前的文章里我们介绍了通过关键字、十六进制和 RGB 值修改元素的颜色值。从今天开始，我们要学习 CSS 变量（自定义属性）相关的内容。CSS 变量（自定义属性）就像任何编程语言的简单变量。这些变量（自定义属性）用于存储具体的数值，并且有一个变量（自定义属性）可以使用的范围。变量（自定义属性）是通过在开头使用 --，然后使用区分大小写的名称来定义的。变量（自定义属性）的好处是，通过给变量（自定义属性）起一个对你来说在项目中有意义的名字，你能更容易的管理和维护你的代码。例如，当你为项目的主色调设置一个变量名 --primary-color，那么后面再修改这个主色调时，只需要改动一处，而不需要在不同位置的多个 CSS 文件中去手动修改多次值。

CSS 变量语法如下所示：

--my-var-color: #fff;

在变量前加上双横线前缀，然后像给普通 CSS 属性一样设置属性值。在上面的代码中，我们定义了一个 --my-var-color 的变量并设置了一个颜色值。

注意：变量名大小写敏感，--my-var-color 和 --My-Var-Color 是两个不同变量。

变量定义完成后，通过 val() 函数来使用你的变量，调用变量方式如下所示：

a {
  color: var(--my-var-color);
}

var()函数还可以使用第二个参数，表示变量的默认值。如果该变量不存在，就会使用这个默认值。



a {
  color: var(--my-var-color, #F00);
}

第二个参数不处理内部的逗号或空格，都视作参数的一部分。


var(--my-font, "SimSun", "SimHei");
var(--my-padding, 8px 12px 14px 7px);


注意，变量值只能用作属性值，不能用作属性名。

.text-margin-top {
  --text-margin: margin-top;
  /* 无效 */
  var(--text-margin): 6px;
}

以上代码中，变量 --text-margin 用作属性名是无效的。


在之前文章代码的基础，在页面 style 创建两个 CSS 变量，一个变量为主色调背景色，另一个为主色调字体颜色。并将 body 元素的背景色和字体颜色通过变量方式设置。同时将返回顶部文本颜色设置为变量 --primary-text-color。如果要改变这两处理的文本颜色， 直接修改变量 --primary-text-color 值即可。达到一次修改多个元素值的目的。调整代码如下：

<style type="text/css">

    body {

      --primary-bg-color: #FFF8DC;
      --primary-text-color: #FFF;

      background-color: var(--primary-bg-color);
      color: var(--primary-text-color);
    }
    
    [href~="#pageTop"] {
        color: var(--primary-text-color) !important;
        background: #F00;
    }

</style>


本次文章主要进行了页面代码的修改，页面预览效果与之前文章没有变化。大家可以通过 www.icoderoad.com 域名查看对应文档的效果。这几篇文章效果没有太大变化，主要的变化是页面的代码部分增加了变量的定义及使用。预览效果页面如下：




