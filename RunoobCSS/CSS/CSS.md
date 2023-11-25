# ID和Class选择器
1. 类名的第一个字符不能使用数字！它无法在 Mozilla 或 Firefox 中起作用。
# 多重样式优先级
1. （内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式
2. 选择器的优先级是从右到左的，优先级高的选择器将会覆盖优先级低的选择器。
# Backgrounds（背景）

### background-color

```css
h1 {
    background-color: #6495ed;
}

p {
    background-color: #e0ffff;
}

div {
    background-color: #b0c4de;
}
```

### background-image

```css
body {
    background-image: url('bgdesert.jpg');
}
```

### background-position

```css
div {
    /**
    第一个值是水平位置，第二个值是垂直。左上角是0％0％。右下角是100％100％。如果仅指定了一个值，其他值将是50％。 默认值为：0％0％ */
    background-position: x% y%;
}

div {
    background-color: left top | left center |...;
}

div {
    /**
    第一个值是水平位置，第二个值是垂直。左上角是0。单位可以是像素（0px0px）或任何其他 CSS单位。如果仅指定了一个值，其他值将是50％。你可以混合使用％和positions */
    background-color: xpos ypos;
}
```

### background-image

```css
div {
    /**
    背景图像将向垂直和水平方向重复。这是默认*/
    background-color: repeat;
}

div {
    /**
    只有水平位置会重复背景图像 */
    background-color: repeat-x;
}

div {
    /**
    只有垂直位置会重复背景图像 */
    background-color: repeat-y;
}

div {
    /**
    background-image 不会重复 */
    background-color: no-repeat;
}
```

# Text（文本）

### color

```css
body {
    color: red;
}

h1 {
    color: #00ff00;
}

h2 {
    color: rgb(255, 0, 0);
}
```

### text-align

文本的对齐方式

```html
<h1>CSS text-align 实例</h1>
<p class="date">2015 年 3 月 14 号</p>
<p class="main">“当我年轻的时候，我梦想改变这个世界；当我成熟以后，我发现我不能够改变这个世界，我将目光缩短了些，决定只改变我的国家；当我进入暮年以后，我发现我不能够改变我们的国家，我的最后愿望仅仅是改变一下我的家庭，但是，这也不可能。当我现在躺在床上，行将就木时，我突然意识到：如果一开始我仅仅去改变我自己，然后，我可能改变我的家庭；在家人的帮助和鼓励下，我可能为国家做一些事情；然后，谁知道呢?我甚至可能改变这个世界。”</p>
<p><b>注意：</b> 重置浏览器窗口大小查看 &quot;justify&quot; 是如何工作的。</p>
```

```css
h1 {
    text-align: center;
}

p.date {
    text-align: right;
}

p.main {
    /**
    当text-align设置为"justify"，每一行被展开为宽度相等，左，右外边距是对齐（如杂志和报纸）。 */
    text-align: justify;
}
```

### text-decoration

用来设置或删除文本的装饰

```css
a {
    /**
    从设计的角度看 text-decoration属性主要是用来删除链接的下划线 */
    text-decoration: none;
}

h1 {
    /**
    上划线 */
    text-decoration: overline;
}

h2 {
    /**
    删除线 */
    text-decoration: line-through;
}

h3 {
    /**
    下划线 */
    text-decoration: underline;
}
```

### text-transform

用来指定在一个文本中的大写和小写字母

```css
p.uppercase {
    /**
    全部大写 */
    text-transform: uppercase;
}

p.lowercase {
    /**
    全部小写 */
    text-transform: lowercase;
}

p.capitalize {
    /**
    首字母大写 */
    text-transform: capitalize;
}
```

### text-indent

首行缩进

```css
p {
    text-indent: 50px;
}
```

### letter-spacing 

```css
h1 {
    /**
    默认。规定字符间没有额外的空间。 */
    letter-spacing: normal;
}

h2 {
    /**
    定义字符间的固定空间（允许使用负值）。 */
    letter-spacing: -3px;
}
```

### line-heigh

```css
.normal {
    /**
    默认。设置合理的行间距。 */
    line-height: normal;
}

.number {
    /**
    设置数字，此数字会与当前的字体尺寸相乘来设置行间距。 */
    line-height: 5;
}

.length {
    /**
    设置固定的行间距 */
    line-height: 70px;
}

.percent {
    /**
    基于当前字体尺寸的百分比行间距。 */
    line-height: 200%;
}
```

### text-shadow

```css
h1 {
    /**
    h-shadow	必需。水平阴影的位置。允许负值。
    v-shadow	必需。垂直阴影的位置。允许负值。
    blur	可选。模糊的距离。
    color	可选。阴影的颜色。 */
    text-shadow: h-shadow v-shadow blur color;
}
```

### vertical-align 

设置一个元素的垂直对齐方式。

```css
 img.top {
     vertical-align: text-top;
 }

 img.textbottom {
     vertical-align: text-bottom;
 }

 img.bottom {
     vertical-align: bottom;
 }

 img.middle {
     vertical-align: middle;
 }
```

```html
 <p>一个<img src="logo.png" alt="w3cschool" width="270" height="50" />默认对齐的图像。</p>
 <p>一个<img class="top" src="logo.png" alt="w3cschool" width="270" height="50" /> text-top 对齐的图像。</p>
 <p>一个<img class="textbottom" src="logo.png" alt="w3cschool" width="270" height="50" /> text-bottom 对齐的图像。</p>
 <p>一个<img class="bottom" src="logo.png" alt="w3cschool" width="270" height="50" /> bottom 对齐的图像。</p>
 <p>一个<img class="middle" src="logo.png" alt="w3cschool" width="270" height="50" /> middle 对齐的图像。</p>
```

### white-space

用于设置如何处理（空白字符是否合并，以及如何合并；是否换行，以及如何换行；）元素内的空白字符

```css
/* 
默认。空白会被浏览器忽略。*/
white-space: normal;

/*
文本不会换行，文本会在在同一行上继续，直到遇到 <br> 标签为止。 */
white-space: nowrap;

/*
空白会被浏览器保留。其行为方式类似 HTML 中的 <pre> 标签。*/
white-space: pre;

/*
保留空白符序列，但是正常地进行换行。 */
white-space: pre-wrap;

/*
合并空白符序列，但是保留换行符。 */
white-space: pre-line;

/*
与 pre-wrap 的行为相同，除了：

任何保留的空白序列总是占用空间，包括行末的。
每个保留的空白字符后（包括空白字符之间）都可以被截断。
这样保留的空间占用空间而不会挂起，从而影响盒子的固有尺寸（最小内容——min-content——大小和最大内容——max-content——大小）。*/
white-space: break-spaces;

/* 全局值 */
/*
规定应该从父元素继承 white-space 属性的值。*/
white-space: inherit;
white-space: initial;
white-space: revert;
white-space: revert-layer;
white-space: unset;
```

### word-spacing

用于指定单词（word）之间的空白大小，只对英文word有效（英文单词可以生效，中文单字是没有效果的）；相比之下，letter-spacing指定字母（letter）之间的空白大小，对英文字母和中文单字可以生效。

```css
p {
    word-spacing: 30px;
}
```

# Fonts（字体）
1. serif和sans-serif字体之间的区别

![serif和sans-serif字体之间的区别](./imgs/serif.gif)

在计算机屏幕上，sans-serif字体被认为是比serif字体容易阅读

2. CSS字形
在CSS中，有两种类型的字体系列名称：

* **通用字体系列** - 拥有相似外观的字体系统组合（如 "Serif" 或 "Monospace"）
* **特定字体系列** - 一个特定的字体系列（如 "Times" 或 "Courier"）

Serif：字体中字符在行的末端拥有额外的装饰
Sans-serif：这些字体在末端没有额外的装饰
Monospace：所有的等宽字符具有相同的宽度

### font-family 

font-family 属性设置文本的字体系列。font-family 属性应该设置几个字体名称作为一种"后备"机制，如果浏览器不支持第一种字体，他将尝试下一种字体。

**注意**: 如果字体系列的名称超过一个字，它必须用引号，如Font Family："宋体"。

多个字体系列是用一个逗号分隔指明：

```css
p {
    font-family: "Times New Roman", Times, serif;
}
```

### font-style

指定斜体文字的字体样式属性

```css
p.normal {
    /**
    正常显示文本 */
    font-style: normal;
}

p.italic {
    /**
    以斜体字显示的文字 */
    font-style: italic;
}

p.oblique {
    /**
    倾斜的文字 - 文字向一边倾斜（和斜体非常类似，但不太支持）
    tips:没看出和斜体有什么区别 */
    font-style: oblique;
}
```

### font-size

```css
div {
    /**
    基于用户默认字体大小（medium）的绝对大小关键字。 */
    font-size: xx-small | x-small | small | medium | large | x-large | xx-large | xxx-large;
}

div {
    /**
    字体大小将相对于父元素的字体大小变大或变小 */
    font-size: larger | smaller;
}

p {
    /**
    一个固定的值 */
    font-size: 2em;
}

p {
    /**
    基于父元素字体大小的一个百分比值 */
    font-size: 100%;
}
```

### font-variant

```css
p.normal {
    font-variant: normal;
}

p.small {
    /**
    浏览器会显示小型大写字母的字体 */
    font-variant: small-caps;
}
```

### font-weight

```css
p.normal {
    /**
    默认值。定义标准的字符。 */
    font-weight: normal;
}

p.lighter {
    /**
    定义更细的字符。 */
    font-weight: lighter;
}

p.bold {
    /**
    定义粗体字符。 */
    font-weight: bold;
}

p.bolder {
    /**
    定义更粗的字符。 */
    font-weight: bolder;
}

p.number {
    /**
    定义由细到粗的字符。400 等同于 normal，而 700 等同于 bold。 
    数值采取离散式定义（使用 100 的整倍数）。数值为实数，非 100 的整数倍的值将被四舍五入转换为 100 的整倍数，遇到 *50 时，将向上转换，如 150 将转换为 200。
    说人话：只能会是100 - 900九个值，非100的倍数四舍五入向上取整 */
    font-weight: 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900;
}
```

# 链接（link）

顺序需要遵循爱恨（ `L` O `V` E- `H`  `A` TE）原则

```css
/**
正常，未访问过的链接 */
a:link {
    color: #000000;
}

/**
用户已访问过的链接 */
a:visited {
    color: #00FF00;
}

/**
当用户鼠标放在链接上时 */
a:hover {
    color: #FF00FF;
}

/**
链接被点击的那一刻 */
a:active {
    color: #0000FF;
}
```

# 列表

### list-style-type

```css
none 无标记。 disc 默认。标记是实心圆。 circle 标记是空心圆。 square 标记是实心方块。 decimal 标记是数字。 decimal-leading-zero 0开头的数字标记。(01, 02, 03, 等。) lower-roman 小写罗马数字(i, ii, iii, iv, v, 等。) upper-roman 大写罗马数字(I, II, III, IV, V, 等。) lower-alpha 小写英文字母The marker is lower-alpha (a, b, c, d, e, 等。) upper-alpha 大写英文字母The marker is upper-alpha (A, B, C, D, E, 等。) lower-greek 小写希腊字母(alpha, beta, gamma, 等。) lower-latin 小写拉丁字母(a, b, c, d, e, 等。) upper-latin 大写拉丁字母(A, B, C, D, E, 等。) hebrew 传统的希伯来编号方式 armenian 传统的亚美尼亚编号方式 georgian 传统的乔治亚编号方式(an, ban, gan, 等。) cjk-ideographic 简单的表意数字 hiragana 标记是：a,
i,
u,
e,
o,
ka,
ki,
等。（日文平假名字符） katakana 标记是：A,
I,
U,
E,
O,
KA,
KI,
等。（日文片假名字符） hiragana-iroha 标记是：i,
ro,
ha,
ni,
ho,
he,
to,
等。 （日文平假名序号） katakana-iroha 标记是：I,
RO,
HA,
NI,
HO,
HE,
TO,
等。（日文片假名序号）
```

### list-style-position

规定列表中列表项目标记的位置

```css
ul {
    /**
    列表项目标记放置在文本以内，且环绕文本根据标记对齐。 */
    list-style-position: inside;
}

ul {
    /**
    默认值。保持标记位于文本的左侧。列表项目标记放置在文本以外，且环绕文本不根据标记对齐。 */
    list-style-position: outside;
}
```

### list-style-image 

指定列表中的列表项标记的图像

```css
ul {
    list-style-image: url('filename.gif')
}
```

# Table（表格）

### border-collapse

```css
table {
    border-collapse: collapse;
}
```

### text-align & vertical-align

```css
td {
    /**
    水平对齐方式*/
    text-align: center | left | right;
    /**
    垂直对齐方式 */
    vertical-align: baseline | bottom | sub | super | text-bottom | middle;
}
```

# 盒子模型

box-sizing:content-box; （默认值，width/height只包含内容区）
box-sizing:border-box; （width/height包含内容区、内边距、边框，不包含外边距，不包含外边距的意思只是外边距不在模型的范围内，不是外边距不能设置）
* Margin(外边距) - 清除边框外的区域，外边距是透明的。
* Border(边框) - 围绕在内边距和内容外的边框。
* Padding(内边距) - 清除内容周围的区域，内边距是透明的。
* Content(内容) - 盒子的内容，显示文本和图像。
# Border（边框）

### border-style

```css
div {
    /**
    默认无边框 */
    border-styel: none;
}

div {
    /**
    定义一个点线边框 */
    border-style: dotted;
}

div {
    /**
    定义虚线边框 */
    border-style: dashed;
}

div {
    /**
    定义实线边框 */
    border-style: solid;
}

div {
    /**
    定义两个边框 */
    border-style: double;
}

div {
    /**
    定义3D沟槽边框 */
    border-style: groove;
}

div {
    /**
    定义3D脊边框 */
    border-style: ridge;
}

div {
    /**
    定义3D嵌入边框 */
    border-style: inset;
}

div {
    /**
    定义3D突出边框 */
    border-style: outset;
}
```

### border-width

```css
div {
    /**
    明确指定宽度值 */
    border-width: 5px | 1.5em | 1.5cm | 4rem;
}

div {
    /**
    使用border-width关键字
    规范并没有规定关键字的实际值故在不同浏览器效果是不一样的，但显然 thin≤medium≤thick，并且值在单个文档中是恒定 */
    border-width: thin | medium | thick;
}
```

### border-color

border-color 单独使用是不起作用的，必需先试用 border-style 来设置边框样式

```css
div {
    border-color: red | rgb(red, green, blue) | #ffffff | transparent;
}
```

### border

通过 border 属性设置边框必需设置 border-style

```css
div {
    border: 5px solid red;
}
```

### border-radius

```css
div {
    border-radius: 5px;
}
```

# 轮廓（outline）

轮廓（outline）是绘制于元素周围的一条线，位于**边框边缘的外围**，可起到突出元素的作用。

```css
div {
    /**
    颜色、样式、宽度 */
    outline: #00FF00 dotted thick;
}

div {
    /**
    轮廓的颜色
    coloe-name、hex-number、rgb-numbe */
    outline-color: #00ff00;
}

div {
    /**
    轮廓的样式 */
    outline-stye: none | dotted | dashed | solid | double | groove | ridge | inset | outset | inherit;
}

div {
    /**
    轮廓的宽度 */
    outline-width； thin | medium |thick | inherit;
}
```

# margin（外边距）

margin(外边距)属性定义元素周围的空间。margin 没有背景颜色，是完全透明的。

# padding（填充）

padding（填充）是一个简写属性，定义元素边框与元素内容之间的空间，即上下左右的内边距。

# 分组和嵌套

`elemnt,element` ： `div,p` 选择所有 `<div>` 和 `<p>` 元素；
`element element` ： `div p` 选择 `<div>` 内所有的 `p` 元素。
`element.class` ： `p.hometown` 选择所有 `class="hometown` 的 `<p>` 元素。

# 尺寸（Dimension）

```css
div {
    /**
    设置元素的高度 */
    height: 100px;

    /**
    设置行高 */
    line-height: 90%;

    /**
    设置元素的最大高度 */
    max-height: 100px;

    /**
    设置元素的最大宽度 */
    max-width: 100px;

    /**
    设置元素的最小高度 */
    min-height: 100px;

    /**
    设置元素最小宽度 */
    min-width: 100px;
    /**
    设置元素的宽度 */
    width: 100px;
}
```

# Display（显示）

`display:none;` 不占局空间，隐藏某个元素，在dom结构中；
`visibility:hidden;` 占据空间，隐藏某个元素，在dom结构中。

```css
span {
    /**
    显示为块级元素 */
    display: block;
}

div {
    /**
    显示为内联元素 */
    display: inline;
}
```

# Position（定位）

position属性的五个值：static、relative、fixed、absolute、sticky，设置了 position 属性之后，元素可以使用顶部、底部、左侧、右侧属性定位。

### position

```css
div {
    /**
    默认值，及没有定位，遵循正常的文档流对象 */
    position: static;
}

div {
    /**
    相对于浏览器窗口位置固定定位 */
    position: fixed;
    top: 30px;
    right: 50px;
}

div {
    /**
    相对于定位元素正常位置定位 */
    position: relative;
    left: 20px;
}

div {
    /**
    相对于最近的已定位父元素定位，如果没有已定位的父元素，则相对于 html 定位 */
    position: absolute;
    left: 100px;
    top: 150px;
}

div {
    /**
    依赖于用户的滚动，在 position:relative; 与 position:fixed; 定位之间切换
    它的行为就像 position:relative; 而当页面滚动超出目标区域时，它的表现就像 position:fixed;，它会固定在目标位置。
    元素定位表现为在跨越特定阈值前为相对定位，之后为固定定位。
    这个特定阈值指的是 top, right, bottom 或 left 之一，换言之，指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。 */
    position: sticky;
    top: 0;
}
```

### z-index

元素的定位与文档流无关，所以它们可以覆盖页面上的其它元素。z-index属性指定了一个元素的堆叠顺序（哪个元素应该放在前面，或后面）。
一个元素可以有正数或负数的堆叠顺序。具有更高堆叠顺序的元素总是在较低的堆叠顺序元素的前面。

注意： 如果两个定位元素重叠，没有指定z - index，最后定位在HTML代码中的元素将被显示在最前面。

# Overflow

overflow 属性用于控制内容溢出元素框时显示的方式。
`overflow: auto;` 和 `overflow: scroll;` 的主要区别在于当内容不超出容器尺寸时是否显示滚动条， `overflow: auto;` 只在需要时才会显示滚动条，而· `overflow: scrol;` 则无论是否需要都会显示滚动条。

```css
div {
    /**
    默认值，内容不会被修剪，会呈现在元素框之外 */
    overflow: visible;
}

div {
    /**
    内容会被修剪，并且内容是不可见的 */
    overflow: hidden;
}

div {
    /**
    内容会被修剪，但是浏览器会显示滚动条以便查看剩余内容 */
    overflow: scroll;
}

div {
    /**
    如果内容会被修剪 ，这浏览器会显示滚动条以便查看剩余内容 */
}
```

# Float（浮动）

```css
img {
    float: left | right | both | none | inherit;
}
```

元素浮动之后，周围的元素会重新排列，为了避免这种情况，使用clear属性清除浮动，clear属性指定元素两侧不能出现浮动元素。

```css
div {
    /**
    清除左浮动 */
    clear: left;
}

div {
    /**
    清除两侧浮动 */
    clear: both;
}

div {
    /**
    清除右浮动 */
    clear: right;
}
```

tips：clear的作用就是“清除浮动”，所谓清除浮动不是指清除自己的浮动，是指清除被设置了clear属性的元素的左右元素的浮动，也就是使其float属性“失效”，即时设置了float属性也相当于没有设置的效果。

# 对齐
1. 元素居中对齐
要水平居中一个（块级）元素，可以使用过 `margin: auto;` ，如果没有设置 `width` 属性（或者设置100%），居中对齐将不起作用。
```css 
 .container {

    width: 80vw;
    height: 80vh;
    border: 1px solid pink;

}
.content {

    width: 100px;
    height: 200px; 
    margin: auto;
    border: 1px solid hotpink;

}

```
```html
<div class="container">
    <div class="content"></div>
</div>
```

2. 图片居中对齐
可以通过display设置图片为块级元素，使其居中对齐。

```css
div {
    width: 700px;
}

img {
    display: block;
    margin: auto;
}
```

```html
<div class="container">
    <img src="../imgs/serif.gif" alt="">
</div>
```

3. 垂直居中对齐 - 使用padding
tips: 几乎不会有人用吧？局限性太大了，能否算的上是一种方法都很难说（不过对于行内元素确实可以）

```html
 <style>
     .container {
         padding: 90px 0;
         height: 50px;
     }
 </style>
 <div class="container">
     期望此段文本是垂直居中对齐的
 </div>
```

4. 垂直居中 - 使用line-height
通过使line-height等于height来实现垂直居中对齐（仅单行文本有效）

5. 垂直居中 - 使用position和transform

```css
.center {
    height: 200px;
    position: relative;
    border: 3px solid green;
}

.center p {
    margin: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

# 导航栏