# 边框

### border-radius

内切圆的半径

### box-shadow

```css
div {
    box-shadow: 10px 10px 5px #88888;
}
```

### border-image

效果就是在整个border范围内都是背景图片（类似baground-clip: border-box; ），去除padding、content遮住的部分就是baoder-image的效果。
border-image是border-image-source、border-image-slice、border-image-width、border-image-outset、border-image-repeat的简写。

### box-shadow

```css
/* x 偏移量 | y 偏移量 | 阴影颜色 */
box-shadow: 60px -16px teal;

/* x 偏移量 | y 偏移量 | 阴影模糊半径 | 阴影颜色 */
box-shadow: 10px 5px 5px black;

/* x 偏移量 | y 偏移量 | 阴影模糊半径 | 阴影扩散半径 | 阴影颜色 */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

/* 插页 (阴影向内) | x 偏移量 | y 偏移量 | 阴影颜色 */
box-shadow: inset 5em 1em gold;

/* 任意数量的阴影，以逗号分隔 */
box-shadow: 3px 3px red,
-1em 0 0.4em olive;

/* 全局关键字 */
box-shadow: inherit;
box-shadow: initial;
box-shadow: unset;
```

# 圆角

```css
div {
    /**
    四个值：左上、右上、右下、左下 */
    border-radius: 10px 10px 10px 10px;
}

div {
    /**
    三个值： 左上 右上和左下 右下 */
    border-radius: 15px 50px 30px;
}

div {
    /**
    两个值：左上和右下 右上和左下 */
    border-radius: 15px 50px;
}

div {
    /**
    椭圆角：两个值分别是半长轴和半短轴 */
    border-radius: 15px/50px;
}
```

当然也可以分开写四个属性。

# 背景

### background-image

```css
/**
可以给一个backgroung-image属性添加不止一张图片
不同的背景图像和图像用逗号隔开，第一张显示在最顶端
同理也可以给每个背景图像单独设置 position 和 repeat 
给每个背景图像单独设置 position 和 repeat 也不止一种写法*/
#example1 {
    background-image: url(img_flwr.gif), url(paper.gif);
    background-position: right bottom, left top;
    background-repeat: no-repeat, repeat;
}

#example1 {
    background: url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;
}
```

### background-size

```css
/* 关键字 */
background-size: cover background-size: contain
/* 一个值：这个值指定图片的宽度，图片的高度隐式的为 auto */
background-size: 50% background-size: 3em background-size: 12px background-size: auto
/* 两个值 */
/* 第一个值指定图片的宽度，第二个值指定图片的高度 */
background-size: 50% auto background-size: 3em 25% background-size: auto 6px background-size: auto auto
/* 逗号分隔的多个值：设置多重背景 */
background-size: auto,
auto
/* 不同于 background-size: auto auto */
background-size: 50%,
25%,
25% background-size: 6px,
auto,
contain
/* 全局属性 */
background-size: inherit;
background-size: initial;
background-size: unset;
```

### background-origin

```css
div {
    background-origin: border-box | padding-box | content-box;
}
```

注意和 background-clip 的区别，如果背景是纯色的话，效果相同。

### background-clip

```css
div {
    background-clip: border-box | padding-box | content-box;
}
```

注意和 background-origin 的区别，如果背景是纯色的话，效果相同。

# 渐变（Gradients）
1. 线性渐变

```css
div {
    /**
    线性渐变：从上到下（默认情况） */
    background-image: linear-gradient(#e66465, #9198e5)
}

div {
    /**
    线性渐变：从左到右 */
    background-image：linear-gradient(to right, red, yellow)
}

div {
    /**
    线性渐变：对角 */
    background-image: linear-gradient(to bottom right, red, yellow)
}

div {
    /**
    线性渐变：使用角度 */
    background-image: linear-gradient(angle, color-stop1, color-stop2);
}

div {
    /**
    使用多个颜色节点 */
    background-image: linear-gradient(red, yellow, green);
}

div {
    /**
    使用透明度 */
    background-image: linear-gradient(to right, rgba(255, 0, 0, 0), rgba(255, 0, 0, 1));
}

div {
    /**
    重复的线性渐变 */
    background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
}
```

2. 径向渐变

```css
div {
    /**
    颜色节点均匀分布的径向渐变 */
    background-image: radial-gradient(red, yellow, green);
}

div {
    /**
    颜色节点不均匀分布的径向渐变 */
    background-image: radial-gradient(red 5%, yellow 15%, green 60%);
}

div {
    /**
    设置形状：circle（圆形） ellipse（椭圆形，默认值） */
    background-image: radial-gradient(circle, red, yellow, green);
}

div {
    /**
    不同尺寸大小关键字的使用
size 参数定义了渐变的大小。它可以是以下四个值：

closest-side
farthest-side
closest-corner
farthest-corner */
    background-image: radial-gradient(closest-side at 60% 55%, red, yellow, black);
}
```

3. 重复的径向渐变

```css
#grad {
    background-image: repeating-radial-gradient(red, yellow 10%, green 15%);
}
```

# 文本效果

### text-shadow

```css
/* offset-x | offset-y | blur-radius | color */
text-shadow: 1px 1px 2px black;

/* color | offset-x | offset-y | blur-radius */
text-shadow: #fc0 1px 0 10px;

/* offset-x | offset-y | color */
text-shadow: 5px 5px #558abb;

/* color | offset-x | offset-y */
text-shadow: white 2px 5px;

/* offset-x | offset-y
/* Use defaults for color and blur-radius */
text-shadow: 5px 10px;

/* Global values */
text-shadow: inherit;
text-shadow: initial;
text-shadow: unset;
```

### box-shadow

```css
/* x 偏移量 | y 偏移量 | 阴影颜色 */
box-shadow: 60px -16px teal;

/* x 偏移量 | y 偏移量 | 阴影模糊半径 | 阴影颜色 */
box-shadow: 10px 5px 5px black;

/* x 偏移量 | y 偏移量 | 阴影模糊半径 | 阴影扩散半径 | 阴影颜色 */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

/* 插页 (阴影向内) | x 偏移量 | y 偏移量 | 阴影颜色 */
box-shadow: inset 5em 1em gold;

/* 任意数量的阴影，以逗号分隔 */
box-shadow: 3px 3px red,
-1em 0 0.4em olive;

/* 全局关键字 */
box-shadow: inherit;
box-shadow: initial;
box-shadow: unset;
```

### text-overflow

```css
/**
用一个省略号（'…'、U+2026 HORIZONTAL ELLIPSIS）来表示被截断的文本 */
text-overflow: ellipsis;
/**
在内容区域的极限处截断文本 */
text-overflow: clip;
```

### word-wrap

已更名为 overflow-wrap，应用于行级元素，用来设置浏览器是否应该在一个本来不能断开的字符串中插入换行符，以防止文本溢出其行向盒。

##### anywhere

为防止溢出，如果行中没有其他可接受的断点，则不可断的字符串（如长词或 URL）可能会在任何时候换行。在断点处不会插入连字符。在计算最小内容内在大小时，会考虑由单词换行引入的软换行机会。

##### break-word

与 anywhere 值相同，如果行中没有其他可接受的断点，则允许在任意点将通常不可断的单词换行，但在计算最小内容内在大小时不考虑断字引入的软换行机会。

### word-break

#### normal

使用默认的断行规则。

#### break-all

对于 non-CJK (CJK 指中文/日文/韩文) 文本，可在任意字符间断行。

#### keep-all

CJK 文本不断行。Non-CJK 文本表现同 normal。

### hanging-punctuation 

定一个标点符号是否会在启动或在结束时文本行框以外。

```css
div {
    /**
    none	不在文本整行的开头还是结尾的行框之外放置标签符号。
    first	标点附着在首行开始边缘之外。
    last	标点附着在首行结尾边缘之外。
    allow-end	
    force-end */
    hanging-punctuation: none|first|last|allow-end|force-end;
}
```

### text-emphasis

将强调标记应用于文本（空格和控制字符除外）。它是text-emphasis-color和text-emphasis-style的简写。

```css
/* Initial value */
text-emphasis: none;
/* No emphasis marks */

/* <string> value */
text-emphasis: "x";
text-emphasis: "点";
text-emphasis: "\25B2";
text-emphasis: "*"#555;
text-emphasis: "foo";
/* Should NOT use. It may be computed to or rendered as 'f' only */

/* Keywords value */
text-emphasis: filled;
text-emphasis: open;
text-emphasis: filled sesame;
text-emphasis: open sesame;

/* Keywords value combined with a color */
text-emphasis: filled sesame #555;

/* Global values */
text-emphasis: inherit;
text-emphasis: initial;
text-emphasis: revert;
text-emphasis: revert-layer;
text-emphasis: unset;
```

# 字体

```css
@font-face {
    /**
    必需。规定字体的名称。 */
    font-family: myFirstFont;

    /**
    必需。定义字体文件的 URL。 */
    src: utl(xxx.ttf)
        /**
    可选。定义如何拉伸字体。默认是 "normal" */
        font-stretch: normal | condensed | ultra-condensed | extra-condensed | semi-condensed | expanded | semi-expanded | extra-expanded | ultra-expanded;

    /**
    定义字体的样式，默认是 "normal" */
    font-style: normal | italic | oblique;

    /**
    定义由细到粗的字符。400 等同于 normal，而 700 等同于 bold。 
    数值采取离散式定义（使用 100 的整倍数）。数值为实数，非 100 的整数倍的值将被四舍五入转换为 100 的整倍数，遇到 *50 时，将向上转换，如 150 将转换为 200。
    说人话：只能会是100 - 900九个值，非100的倍数四舍五入向上取整 */
    font-weight: 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900;

    /**
    可选。定义字体支持的 UNICODE 字符范围。默认是 "U+0-10FFFF"。 */
    unicode-range: U+26;
}
```

# 2D转换

### translate()

根据左(X轴)和顶部(Y轴)位置给定的参数，从当前元素位置移动。

```css
div {
    transform: translate(50px, 100px);
}
```

### rotate()
在一个给定度数顺时针旋转的元素。负值是允许的，这样是元素逆时针旋转。
```css
div {
    transform: rotate(30deg);
}
```

### scale()
用于修改元素的大小。可以通过向量形式定义的缩放值来放大或缩小元素，同时可以在不同的方向设置不同的缩放值。
```css
/**
x和y方向缩放相同 */
transform: scale(0.7);

/**
x轴方向缩放1.3倍，y轴方向缩放0.4倍 */
transform: scale(1.3, 0.4);
```

### skew()
包含两个参数值，分别表示X轴和Y轴倾斜的角度，如果第二个参数为空，则默认为0，参数为负表示向相反方向倾斜。
```css
transform: skew(30deg,20deg);
```

### matrix()
matrix 方法有六个参数，包含旋转，缩放，移动（平移）和倾斜功能。