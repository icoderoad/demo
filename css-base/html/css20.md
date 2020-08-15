之前的文章里我们介绍了 CSS 变量的使用方法。今天我们继续介绍 CSS 变量作用域、浏览器兼容性及变量重载问题。创建变量时，可以在创建变量的选择器中使用它。也可以在该选择器的任何后代中使用。继承特性是由 CSS 的"层叠"（cascade）规则决定的。

为了利用继承，CSS 变量通常在 :root 元素中定义。:root 是一个伪类选择器，它与文档的根元素（通常是 html 元素）匹配。通过在 :root 伪类选择器中创建变量，它们将在页面的全局范围内可用，并且可以从样式表的任何其他选择器进行访问。在 :root 伪类选择器中定义一个名为 --bg-color 的变量，并为其指定 SlateGray 值。然后，你可以看到该变量是继承的，并且使用该变量的所有子元素都具有青灰色背景。

在页面代码中增加 :root 伪类变量定义， 将页面导航区第 2、4 个元素的背景色设置为变量 --bg-color， 调整代码如下所示：

<style type="text/css">
    
    :root {
      --bg-color: SlateGray;
    }

    .menu li:nth-child(2) {  
      background-color: var(--bg-color);
    }

    .menu li:nth-child(4) {  
      background-color: var(--bg-color);
    }


</style>       

使用 CSS 时，大家都会遇到浏览器兼容性问题。这就是为什么提供变量备用属性设置以避免浏览器兼容性问题的重要性。

当浏览器解析网页的 CSS 时，它将忽略它无法识别或不支持的任何属性。例如，如果你使用 CSS 变量在网站上分配背景色，则 Internet Explorer 将忽略背景色，因为它不支持 CSS 变量。在这种情况下，如果找不到为该属性设置的任何其他值，它将恢复为浏览器的默认值，通常效果不理想。为了解决上述问题，可以通过设置备用值的方式来实现。设置背景色时设置一个备用颜色属性，在样式表的下面通过变量的方式设置新的值。较旧的浏览器将使用上面不支持变量设置的备用属性值，而较新的浏览器使用通过变量设置的属性值。页面代码调整如下：


<style type="text/css">
    
    :root {
      --bg-color: SlateGray;
    }

    .menu li:nth-child(2) {  
      background-color: SlateGray;
      background-color: var(--bg-color);
    }

    .menu li:nth-child(4) { 
      background-color: SlateGray; 
      background-color: var(--bg-color);
    }

</style>   

以上代码在老的浏览器会执行 background-color: SlateGray; 设置的背景色，新版本浏览器使用 background-color: var(--bg-color); 设置的背景色。

当你在 :root 伪类选择器中创建变量时，该变量的作用域为整个页面，在页面内所有选择器都可以使用该变量。然而，可以通过在特定元素或选择器中再次设置它们来重写这些变量的值。
在导航栏选项第 2 个元素中将 --bg-color 的值设置为 DarkViolet， 第 2 个元素将显示 DarkViolet 颜色的背景色。 调整后的代码如下

<style type="text/css">

    :root {
      --bg-color: SlateGray;
    }

    .menu li:nth-child(2) { 
      --bg-color: DarkViolet;
      background-color: SlateGray; 
      background-color: var(--bg-color);
    }

    .menu li:nth-child(4) {  
      background-color: SlateGray;
      background-color: var(--bg-color);
    }

</style>   

可以使用媒体查询重新设置 CSS 变量的值 。例如，当你的屏幕小于或大于你的媒体查询设置条件时，你可以更改一个变量的值，将在使用它的任何位置应用其修改后的样式。设置新的媒体查询方式，在最大宽度为 1400px 时，在 :root 伪类选择器中将变量 --bg-color 颜色设置为 Purple 。保存页面，预览页面，手工调整页面宽度到小于 1400px 。观察导航区第 4 个元素背景颜色的变化。页面宽度大于 1400px 时，背景颜色为 SlateGray ，小于 1400px时，背景颜色为 Purple。 最终小于 1400px 宽度时的页面效果如下所示：



