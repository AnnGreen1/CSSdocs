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