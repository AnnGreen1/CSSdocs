# Viewport

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

* width：控制 viewport 的大小，可以指定的一个值，如 600，或者特殊的值，如 device-width 为设备的宽度（单位为缩放为 100% 时的 CSS 的像素）。
* height：和 width 相对应，指定高度。
* initial-scale：初始缩放比例，也即是当页面第一次 load 的时候缩放比例。
* maximum-scale：允许用户缩放到的最大比例。
* minimum-scale：允许用户缩放到的最小比例。
* user-scalable：用户是否可以手动缩放。
# 媒体查询

### 媒体查询区分横屏/竖屏

竖屏判断依据：可视区域宽度小于高度；
横屏判断依据：可视区域高度小于宽度。

```css
orientation：portrait | landscape
```

* portrait：指定输出设备中的页面可见区域高度大于或等于宽度
* landscape： 除portrait值情况外，都是landscape

```css
/**
当文档的宽度大于高度时（横屏），背景会变为浅蓝色。否则（竖屏）为浅绿色。 */
body {
    background-color: lightgreen;
}

@media only screen and (orientation: landscape) {
    body {
        background-color: lightblue;
    }
}
```

# 图片

### img

1. 使用width属性
如果 width 属性设置为 100%，图片会根据上下范围实现响应式功能

```css
img {
    width: 100%;
    height: auto;
}
```

2. 使用max-width属性
如果 max-width 属性设置为 100%, 图片永远不会大于其原始大小

```css
img {
    max-width: 100%;
    heigh: auto;
}
```

### 背景图片

背景图片可以响应调整大小或缩放。
tips: 一般第一种是最合理的，也基本够用了
1. 如果 background-size 属性设置为 "contain", 背景图片将按比例自适应内容区域。图片保持其比例不变

```css
div {
    width: 100%;
    height: 400px;
    background-image: url('/wp-content/uploads/2015/06/img_flowers.jpg');
    background-repeat: no-repeat;
    background-size: contain;
    border: 1px solid red;
}
```

2. 如果 background-size 属性设置为 "100% 100%" ，背景图片将延展覆盖整个区域

```css
div {
    width: 100%;
    height: 400px;
    background-image: url('/wp-content/uploads/2015/06/img_flowers.jpg');
    background-size: 100% 100%;
    border: 1px solid red;
}
```

3. 如果 background-size 属性设置为 "cover"，则会把背景图像扩展至足够大，以使背景图像完全覆盖背景区域。注意该属性保持了图片的比例因此 背景图像的某些部分无法显示在背景定位区域中。

```css
div {
    width: 100%;
    height: 400px;
    background-image: url('img_flowers.jpg');
    background-size: cover;
    border: 1px solid red;
}
```

##### 不同设备显示不同图片

大尺寸图片可以显示在大屏幕上，但在小屏幕上却不能很好显示。我们没有必要在小屏幕上去加载大图片，这样很影响加载速度。所以我们可以使用媒体查询，根据不同的设备显示不同的图片。

```css
/* For width smaller than 400px: */
body {
    background-image: url('img_smallflower.jpg');
}

/* For width 400px and larger: */
@media only screen and (min-width: 400px) {
    body {
        background-image: url('img_flowers.jpg');
    }
}
```

### html5 picture

```html
<picture>
    <source srcset="/wp-content/uploads/2015/06/img_smallflower.jpg" media="(max-width: 400px)">
    <source srcset="/wp-content/uploads/2015/06/img_flowers.jpg">
    <img src="/wp-content/uploads/2015/06/img_flowers.jpg" alt="Flowers" style="width:auto;">
</picture>
```

# 视频（Video）

width 属性设置为 100%，视频播放器会根据屏幕大小自动调整比例

```css
video {
    width: 100%;
    height: auto;
}
```

# 框架