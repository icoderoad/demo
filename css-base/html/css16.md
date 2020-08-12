今天我们要学习的内容是基于 body 元素的 CSS 样式声明及覆盖。 到目前为止，我们之前文章里介绍的页面里都包含 body 元素。 你可以像任何其他 HTML 元素一样通过 CSS 设置 body 元素的样式，并且所有页面里的其他元素都将继承 body 元素的样式。

我们可以用 Cornsilk 的背景色来证明页面 body 元素的存在。设置页面背景颜色代码示例如下：

<style type="text/css">

    body {
      background-color: Cornsilk;
    }

</style>

以上代码将页面背景色设置为 Cornsilk ，预览页面查看效果，页面的背景颜色由白色变成比较浅的褐色。整个页面的 body 区域被 Cornsilk 颜色填充。

在介绍 ID 选择器时，我们在 body 元素上增加 id="pageBody" 的属性，在页面 style 区对页面的字体颜色设置了黄色。为了查看元素样式的继承效果，现将 style 区将 #pageBody 删除， 在 body 元素选择器增加 color : white , 将页面正文的颜色设置为白色。 调整后的代码如下：

<style type="text/css">

    body {
      background-color: Cornsilk;
      color: white;
    }

</style>

预览页面，可以看到页面字体默认颜色由黄色变成了白色。大家可以看下侧栏区的有序列表和用户注册部分的字体颜色都变成了白色。

有时 HTML 元素会被设置多个样式，多个样式之间样式相互冲突。例如， h3 元素不能同时被设置白色和金色。让我们看下当我们创建一个金色的样式类，然后将其应用于 h2 元素时会发生什么。我们的类会覆盖 body 元素的 color: white CSS 属性吗？

<style type="text/css">

    body {
      background-color: Cornsilk;
      color: white;
    }

    .text-gold {
        color: Gold;
    }

</style>

以上代码在 style 区增加金色样式类， 在主内容区第二个 “嘿，你好，欢迎来到路条编程公众号！” 的 h3 元素增加样式类 text-gold ，预览页面查看相应的页面效果，我们的 text-gold 类的金色文体覆盖了 body 元素的白色文本。

刚刚我们证明我了金色文本类将覆盖 body 元素的 CSS 样式。接下来我们要做的是如何覆盖刚才设置的金色文本类呢？创建一个名为 text-lime 文本样式类，该类为元素提供浅绿色，确保它在你的金色文本样式类声明下面。除了金色文本类之外，还将浅绿色文本类应用于 h3 元素，让我们看看最终 h3 元素显示什么颜色的文本。

将多个类应用到一个 HTML 元素中，代码示例如下：

class=“text-gold text-lime”


注意：类在 HTML 元素中的顺序并不重要。然而，<style> 部分中类声明的顺序才是重要的。第二个声明总是优先于第一个声明。因为 .text-lime 被声明在 .text-gold 下面，所以它重写 .text-gold 的属性。在 <style> 区增加 .text-lime 类，在主内容区 h3 元素上增加 text-lime 类 调整后代码如下：


<style type="text/css">

    body {
      background-color: Cornsilk;
      color: white;
    }

    .text-gold {
        color: Gold;
    }

    .text-lime {
      color: lime;
    }

</style>


<h3 class="text-gold text-lime" >嘿，你好，欢迎来到路条编程公众号！</h3>


以上代码我们只是证明了浏览器按照声明的顺序从上到下读取 CSS 。这意味着，在发生冲突时，浏览器将使用最后一个 CSS 声明替换前端的 CSS 声明。

注意，如果我们在 h3 元素的类中把浅绿色文本放在金色文本之前，它仍然会查看声明顺序，而不是它们的使用顺序！

但我们还没说完。还有其他方法可以覆盖CSS。你还记得id属性吗？
让我们重写金色文本和浅绿色文本类，并使 h3 元素变为橙色，方法是给 h3 元素一个 id，然后设置该 id 的样式。给 h3 元素设置一个橙色文本的 id 属性。记住，id 样式如下所示：

<h3 id="text-orange">

在 h3 元素上保留金色文本和浅绿色文本类，在 <style> 部分添加橙色文本 id 声明。代码示例如下：


<style type="text/css">

    body {
      background-color: Cornsilk;
      color: white;
    }

    .text-gold {
        color: Gold;
    }

    .text-lime {
      color: lime;
    }

    #text-orange {
      color: orange;
    }

</style>

注意：不管橙色文本类在声明在什么位置， h3 元素总是优先使用 #text-orange 样式，因为 id 属性权重最高。


上面示例我们已经证明了不管 id 声明在样式表的什么位置， id 声明都会覆盖类声明。还有其他方法可以覆盖 CSS ID 声明。你还记得内联样式吗？使用内联样式尝试使 h3 元素变为深粉色 DeepPink 。在 h3 元素上保留橙色 ID 类、浅绿色文本和金色文本类。内联样式定义代码如下所示：

<h3 id="text-orange" class="text-lime text-gold" style="color:DeepPink">


以上代码我们证明了内联样式将覆盖 style 元素中的所有 CSS 声明。下面我们要介绍一种优先级最高的 CSS 声明，这是最有力的覆盖方法。在我们开始之前，我们先来谈谈为什么要覆盖 CSS 声明。在许多情况下，你可以使用 CSS 库。这些库里的 CSS 声明可能会意外地覆盖你自己定义的 CSS 声明。因此，当你需要确保一个元素具有特定的 CSS 时，你可以使用 !important 声明。
让我们回到浅绿色文本类声明。请记住，浅绿色文本类被后续的类声明、id 声明和内联样式覆盖。我们在浅绿色文本类的颜色声明添加关键字 !important ，以确保你的 h3 元素将是浅绿色的。 调整后的代码如下所示：

<style type="text/css">

    body {
      background-color: Cornsilk;
      color: white;
    }

    .text-gold {
        color: Gold;
    }

    .text-lime {
      color: lime !important;
    }

    #text-orange {
      color: orange;
    }

</style>

大家可以按以上文章介绍的顺序进行 CSS 声明，并按相应顺序进行相关的 CSS 声明覆盖操作，预览页面查看每次覆盖后的页面效果，页面最终保持在设置完 !important 的效果，具体效果如下：


