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
顺序需要遵循爱恨（`L`O`V`E-`H` `A`TE）原则
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
