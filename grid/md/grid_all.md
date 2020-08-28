eg: 
https://css-tricks.com/snippets/css/complete-guide-grid/

## lesson1
通过将属性display的值设为grid，使 HTML 元素变为网格容器。通过前面的操作，你可以对该容器使用与 CSS 网格（CSS Grid）相关的属性。
简单地添加一个网格元素并不能取得很大的进展。你还需要明确网格的结构。在一个网格容器中使用grid-template-columns属性可以添加一些列，示例如下：

.container {
  display: grid;
  grid-template-columns: 50px 50px;
}
上面的代码可以在网格容器中添加两列，宽度均为 50px。

grid-template-columns属性值的个数表示网格的列数，而每个值表示对应列的宽度。
用grid-template-rows为网格设置行数。

使用 CSS 网格单位来更改列和行的大小
在 CSS 网格中，可以使用绝对定位和相对定位单位如px和em来确定行或列的大小。下面的单位也可以使用：

fr：设置列或行占剩余空间的一个比例，

auto：设置列宽或行高自动等于它的内容的宽度或高度，

%：将列或行调整为它的容器宽度或高度的百分比，

最右侧的预览区中的效果通过下面的代码实现：

grid-template-columns: auto 50px 10% 2fr 1fr;
这段代添加了五个列。第一列的宽与它的内容宽度相等；第二列宽 50px；第三列宽是它容器的 10%；最后两列，将剩余的宽度平均分成三份，第四列占两份，第五列占一份。

## lesson2
使用 grid-column-gap 创建多列之间的间距
到目前为止，在你所建立的网格中列都相互紧挨着。如果需要在列与列之间添加一些间隙，我们可以使用grid-column-gap：

grid-column-gap: 10px;
这会在我们创建的所有列之间添加 10px 的空白间隙。
和上个挑战在两列之间添加间隙一样，你可以用grid-row-gap在两行之间添加间隙。

grid-gap是grid-row-gap和grid-column-gap的简写，它更方便使用。如果grid-gap有一个值，行与行之间和列与列之间将添加等于该值的间隙。但是，如果有两个值，第一个值将作为行间隙的高度值，第二个值是列间隙的宽度值。

## lesson3
使用 grid-column 来控制剩余部分
到目前为止，所有的讨论都是围绕网格容器的。grid-column属性是第一个用于网格项本身的属性。

网格的假想水平线和垂直线被称为线（lines）。这些线在网格的左上角从 1 开始编号，垂直线向右、水平线向下累加计数。

这是一个 3x3 网格的线条：
![095fee2af580fac511684248ba414992.png](:/988674bdd57548269b4a88e1c75d57e5)

你可以用grid-column属性定义网格项开始和结束的位置，进而控制每个网格项占用的列数
示例如下：
grid-column: 1 / 3;
这会让网格项从左侧第一条线开始到第三条线结束，占用两列。

当然，你可以像列一样使网格项跨越多行。对于一个网格项，你可以用grid-row属性来确定开始和结束的水平线。

## lesson4
使用 justify-self 水平对齐项目
在 CSS 网格中，每个网格项的内容分别位于被称为单元格（cell）的框内。你可以使用网格项的justify-self属性，设置其内容的位置在单元格内沿行轴对齐的方式。默认情况下，这个属性的值是stretch，这将使内容占满整个单元格的宽度。该 CSS 网格属性也可以使用其他的值：
start：使内容在单元格左侧对齐，
center：使内容在单元格居中对齐，
end：使内容在单元格右侧对齐，

使用 align-self 垂直对齐项目
正如能设置网格项沿行轴对齐方式一样，也可以设置网格项沿列轴对齐方式：你可以对网格项使用align-self属性。对于该属性，你能使用在上一个挑战中可用于justify-self属性的任一个值。

使用 justify-items 水平对齐所有项目
有时你想让在 CSS 网格中的网格项共享对齐方式。你可以像之前学习的那样单独使他们对齐，也可以对网格容器使用justify-items使它们一次性沿行轴对齐。对于这个属性你能使用在之前的两个挑战中学到的所有值，与之前不同的是，它将使网格中所有的网格项按所设置的方式对齐。

使用 align-items 垂直对齐所有项目
对网格容器使用align-items属性可以给网格中所有的网格项设置沿列轴对齐的方式。

## lesson5
将网格划分为区域模板
你可以将网格中的一些网格单元格组合成一个区域（area），并为该区域指定一个自定义名称。你可以通过给容器加上grid-template-areas来实现：
grid-template-areas:
  "header header header"
  "advert content content"
  "footer footer footer";
上面的代码将顶部三个单元格合并成一个名为header的区域，将底部三个单元格合并为一个名为footer的区域，并在中间行生成两个区域————advert和content。
注意：
在代码中，每个单词代表一个网格单元格，每对引号代表一行。
除了自定义标签，你还能使用句点（.）来表示一个空单元格

使用 grid-area 属性将项目放置在网格区域中
像上一个挑战那样，在为网格容添加区域模板后，你可以通过添加你定义的名称将网格项放入自定义区域。为此，你需要对网格项使用grid-area：
.item1 { grid-area: header; }
这样，类名为item1的网格项就被放到了header区域里。这种情况下，网格项将使用整个顶行，因为这一行被名为 header 区域。

使用 grid-area 创建区域模板
你在上一次挑战中学到的grid-area属性有另一种使用方式。如果网格中没有定义区域模板，你也可以像这样为它添加一个模板：
item1 { grid-area: 1/1/2/4; }
这里使用了你之前学习的线号来定义网格项的区域。上例中数字代表这些值：
grid-area: 起始水平线 / 起始垂直线 / 末尾水平线 / 终止垂直线 ;
因此，示例中的网格项将占用第 1 条和第 2 条水平线之间的行及第 1 条和第 4 条垂直线之间的列。

## lesson6
使用 repeat 函数减少重复
当使用grid-template-columns和grid-template-rows定义网格结构时，你需要为添加的每一行和每一列都输入一个值。

如果要添加带 100 行高度相同的网格，单独放入 100 个值不太实际。幸运的是，有一种更好的方法——使用repeat方法指定行或列的重复次数，后面加上逗号以及需要重复的值。

这里有一个添加 100 行网格的例子，使每行高度均为 50px：

grid-template-rows: repeat(100, 50px);
你还可以用 repeat 方法重复多个值，并在定义网格结构时与其他值一起使用。举个例子：

grid-template-columns: repeat(2, 1fr 50px) 20px;
效果相当于：

grid-template-columns: 1fr 50px 1fr 50px 20px;
注意：
1fr 50px重复了两次，后面跟着 20px。

## lesson7
使用 minmax 函数限制项目大小
此外，内置函数minmax也可以可用于设置grid-template-columns和grid-template-rows的值。它的作用是在网格容器改变大小时限制网格项的大小。为此，你需要指定网格项允许的尺寸范围。例如：
grid-template-columns: 100px minmax(50px, 200px);
在上面的代码中，grid-template-columns被设置为添加两列，第一列 100px 宽，第二列宽度最小值是 50px，最大值是 200px。

## lesson8
使用 auto-fill 创建弹性布局
重复方法带有一个名为自动填充（auto-fill）的功能。它的功能是根据容器的大小，尽可能多地放入指定大小的行或列。你可以通过结合auto-fill和minmax来更灵活地布局。
在最右侧的预览区中，grid-template-columns被设置为：
repeat(auto-fill, minmax(60px, 1fr));
上面的代码效果：列的宽度会随容器大小改变，在可以插入一个 60px 宽的列之前，当前行的所有列会一直拉伸（译者注：动手试一下你就明白了）。
注意：
如果容器无法使所有网格项放在同一行，余下的网格项将移至新的一行。

使用 auto-fit 创建弹性布局
auto-fit效果几乎和auto-fill一样。不同点仅在于，当容器的大小大于各网格项之和时，auto-fill将会持续地在一端放入空行或空列，这样就会使所有网格项挤到另一边；而auto-fit则不会在一端放入空行或空列，而是会将所有网格项拉伸至合适的大小。
注意：
如果容器无法使所有网格项放在同一行，余下的网格项将移至新的一行。

## lesson9
使用媒体查询创建响应式布局
通过使用媒体查询重新排列网格区域，更改网格尺寸以及重新排列网格项位置，CSS 网格能轻松地使网站更具响应性。
在最右侧的预览区中，当网页可视区域的宽不小于 300px 时，列数从 1 变为 2。并且，广告（advertisement）区域完全占据左列。
当网页可视区域的宽不小于400px时，使 header 区域完全占据最顶行，footer 区域完全占据最底行。
```
 @media (min-width: 300px){
    .container{
      grid-template-columns: auto 1fr;
      grid-template-rows: auto 1fr auto;
      grid-template-areas:
        "advert header"
        "advert content"
        "advert footer";
    }
  }
  
  @media (min-width: 400px){
    .container{
      /* 请修改本行以下的代码 */
    
      grid-template-areas:
        "header header"
        "advert content"
        "footer footer";
    
    /* 请修改本行以上的代码*/
    }
  }
```

## lesson10
在网格中创建网格
将元素转换为网格只会影响其子代元素。因此，在把某个子代元素设置为网格后，就会得到一个嵌套的网格。

例如，设置类为item3的元素的display和grid-template-columns属性，就会得到一个嵌套的网格。
