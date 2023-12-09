# align-content
* 默认值：stetch
* 继承：否
* 可动画化：否

```css
align-content: stretch|center|flex-start|flex-end|space-between|space-around|initial|inherit;
```

#### stretch	

默认值。元素被拉伸以适应容器。

各行将会伸展以占用剩余的空间。如果剩余的空间是负数，该值等效于'flex-start'。在其它情况下，剩余空间被所有行平分，以扩大它们的侧轴尺寸。

#### center	

元素位于容器的中心。

各行向弹性盒容器的中间位置堆叠。各行两两紧靠住同时在弹性盒容器中居中对齐，保持弹性盒容器的侧轴起始内容边界和第一行之间的距离与该容器的侧轴结束内容边界与第最后一行之间的距离相等。（如果剩下的空间是负数，则各行会向两个方向溢出的相等距离。）

#### flex-start	

元素位于容器的开头。

各行向弹性盒容器的起始位置堆叠。弹性盒容器中第一行的侧轴起始边界紧靠住该弹性盒容器的侧轴起始边界，之后的每一行都紧靠住前面一行。

#### flex-end	

元素位于容器的结尾。

各行向弹性盒容器的结束位置堆叠。弹性盒容器中最后一行的侧轴起结束界紧靠住该弹性盒容器的侧轴结束边界，之后的每一行都紧靠住前面一行。

#### space-between	

元素位于各行之间留有空白的容器内。

各行在弹性盒容器中平均分布。如果剩余的空间是负数或弹性盒容器中只有一行，该值等效于'flex-start'。在其它情况下，第一行的侧轴起始边界紧靠住弹性盒容器的侧轴起始内容边界，最后一行的侧轴结束边界紧靠住弹性盒容器的侧轴结束内容边界，剩余的行则按一定方式在弹性盒窗口中排列，以保持两两之间的空间相等。

#### space-around	

元素位于各行之前、之间、之后都留有空白的容器内。

各行在弹性盒容器中平均分布，两端保留子元素与子元素之间间距大小的一半。如果剩余的空间是负数或弹性盒容器中只有一行，该值等效于'center'。在其它情况下，各行会按一定方式在弹性盒容器中排列，以保持两两之间的空间相等，同时第一行前面及最后一行后面的空间是其他空间的一半。

#### initial	

设置该属性为它的默认值。请参阅 initial。

#### inherit	

从父元素继承该属性。请参阅 inherit。

# align-items
* 默认值：stetch
* 继承：否
* 可动画化：否

```css
align-items: stretch|center|flex-start|flex-end|baseline|initial|inherit;
```

#### stretch	

默认值。元素被拉伸以适应容器。

如果指定侧轴大小的属性值为'auto'，则其值会使项目的边距盒的尺寸尽可能接近所在行的尺寸，但同时会遵照'min/max-width/height'属性的限制。

#### center	

元素位于容器的中心。

弹性盒子元素在该行的侧轴（纵轴）上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）。

#### flex-start	

元素位于容器的开头。

弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴起始边界。

#### flex-end	

元素位于容器的结尾。

弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴结束边界。

#### baseline	

元素位于容器的基线上。

如弹性盒子元素的行内轴与侧轴为同一条，则该值与'flex-start'等效。其它情况下，该值将参与基线对齐。

#### initial	

设置该属性为它的默认值。请参阅 initial。

#### inherit	

从父元素继承该属性。请参阅 inherit。

# align-self
* 默认值：auto
* 继承：否
* 可动画化：否

```css
align-self: auto|stretch|center|flex-start|flex-end|baseline|initial|inherit;
```

#### auto	

默认值。元素继承了它的父容器的 align-items 属性。如果没有父容器则为 "stretch"。	

#### stretch	

元素被拉伸以适应容器。

如果指定侧轴大小的属性值为'auto'，则其值会使项目的边距盒的尺寸尽可能接近所在行的尺寸，但同时会遵照'min/max-width/height'属性的限制。

#### center	

元素位于容器的中心。

弹性盒子元素在该行的侧轴（纵轴）上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）。

#### flex-start	

元素位于容器的开头。

弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴起始边界。

#### flex-end	

元素位于容器的结尾。

弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴结束边界。

#### baseline	

元素位于容器的基线上。

如弹性盒子元素的行内轴与侧轴为同一条，则该值与'flex-start'等效。其它情况下，该值将参与基线对齐。

#### initial	

设置该属性为它的默认值。请参阅 initial。	

#### inherit	

从父元素继承该属性。请参阅 inherit。

# all

> 一个都没理解是啥意思。🤔

all 属性用于重置所有属性，除了 unicode-bidi 和 direction。

```css
all: initial|inherit|unset;
```

#### initial	

该关键字代表改变该元素或其父元素的所有属性至初始值。

#### inherit	

该关键字代表改变该元素或其父元素的所有属性的值至他们的父元素属性的值。

#### unset	

该关键字代表如果该元素的属性的值是可继承的，则改变该元素或该元素的父元素的所有属性的值为他们父元素的属性值，反之则改变为初始值。

# animation

animation 属性是 animation-name，animation-duration, animation-timing-function，animation-delay，animation-iteration-count，animation-direction，animation-fill-mode 和 animation-play-state 属性的一个简写属性形式。

```css
animation: name duration timing-function delay iteration-count direction fill-mode play-state;
```

# animation-delay

定义动画什么时候开始，单位可以是秒（s）或毫秒（ms）。

```css
animation-delay:time;
```

# animation-direction

定义是否循环交替反向播放动画。如果动画被设置为只播放一次，该属性将不起作用。

```css
animation-direction: normal|reverse|alternate|alternate-reverse|initial|inherit;
```

#### normal 

默认值，动画按正常播放。

#### reverse

动画反向播放。

#### alternate

动画在奇数次（1、3、5...）正向播放，在偶数次（2、4、6...）反向播放。

#### alternate-reverse

动画奇数次（1、3、5...）反向播放，在偶数次（2、4、6...）正向播放。

#### initial

设置该属性为它的默认值。

#### inherit

从父元素继承该属性。

# animation-duration

定义动画完成一个周期需要多少秒或毫秒。默认值为 0，意味着没有动画效果。

# animation-fill-mode

规定当动画不播放时（当动画完成时，或当动画有一个延迟未开始播放时），要应用到元素的样式。
默认情况下，CSS 动画在第一个关键帧播放完之前不会影响元素，在最后一个关键帧完成后停止影响元素。animation-fill-mode 属性可重写该行为。

```css
animation-fill-mode: none|forwards|backwards|both|initial|inherit;
```

#### none	

默认值。动画在动画执行之前和之后不会应用任何样式到目标元素。

#### forwards	

在动画结束后（由 animation-iteration-count 决定），动画将应用该属性值。

#### backwards	

动画将应用在 animation-delay 定义期间启动动画的第一次迭代的关键帧中定义的属性值。这些都是 from 关键帧中的值（当 animation-direction 为 "normal" 或 "alternate" 时）或 to 关键帧中的值（当 animation-direction 为 "reverse" 或 "alternate-reverse" 时）。

#### both	

动画遵循 forwards 和 backwards 的规则。也就是说，动画会在两个方向上扩展动画属性。

#### initial	

设置该属性为它的默认值。请参阅 initial。

#### inherit	

从父元素继承该属性。请参阅 inherit。

# animation-iteration-count

定义动画应该播放多少次。

#### n	

一个数字，定义应该播放多少次动画

#### infinite	

指定动画应该播放无限次（永远）

# animation-name

为 @keyframes 动画指定名称。

```css
animation-name: keyframename|none;
```

# animation-play-state

指定动画是否正在运行或已暂停。

```css
animation-play-state: paused|running;
```

#### paused

指定暂停动画

#### running

指定正在运行的动画

# animation-timing-function

指定动画将如何完成一个周期。速度曲线定义动画从一套 CSS 样式变为另一套所用的时间。速度曲线用于使变化更为平滑。

```css
animation-timing-function: value;
```

#### linear	

动画从头到尾的速度是相同的。

#### ease	

默认。动画以低速开始，然后加快，在结束前变慢。

#### ease-in	

动画以低速开始。

#### ease-out	

动画以低速结束。

#### ease-in-out	

动画以低速开始和结束。

#### steps(int, start|end)	

指定了时间函数中的间隔数量（步长）。有两个参数，第一个参数指定函数的间隔数，该参数是一个正整数（大于 0）。 第二个参数是可选的，表示动画是从时间段的开头连续还是末尾连续。含义分别如下：
* start：表示直接开始。
* end：默认值，表示戛然而止。

#### cubic-bezier(n, n, n, n)	

在 cubic-bezier 函数中自己的值。可能的值是从 0 到 1 的数值。
参考：https://cubic-bezier.com

# appearance 

> 最好别用，基本没有浏览器支持且没必要。

允许您使元素看上去像标准的用户界面元素。

```css
appearance: normal|icon|window|button|menu|field;
```

# backface-visibility 

> 真的就是字面意思，背向屏幕时。😮

定义当元素背面向屏幕时是否可见。

```css
backface-visibility: visible|hidden;
```

#### visible	

背面是可见的。

#### hidden	

背面是不可见的。

# background

```css
background:bg-color bg-image position/bg-size bg-repeat bg-origin bg-clip bg-attachment initial|inherit;
```

# background-attachment 

设置背景图像是否固定或者随着页面的其余部分滚动。

#### scroll	

背景图片随着页面的滚动而滚动，这是默认的。

#### fixed	

背景图片不会随着页面的滚动而滚动。

#### local	

背景图片会随着元素内容的滚动而滚动。

#### initial	

设置该属性的默认值。 阅读关于 initial 内容

#### inherit	

指定 background-attachment 的设置应该从父元素继承。

# background-blend-mode 

定义了背景层的混合模式（图片与颜色）。
tips: 这个属性如果能够用好在特定场景还是很方便的🤔

```css
background-blend-mode: normal|multiply|screen|overlay|darken|lighten|color-dodge|saturation|color|luminosity;
```

#### normal

默认值。设置正常的混合模式

#### multiply

正片叠底模式。

#### screen

滤色模式。

#### overlay

叠加模式。

#### darken

变暗模式。

#### lighten

变亮模式。

#### color-dodge

颜色减淡模式。

#### saturation

饱和度模式。

#### color

颜色模式。

#### luminosity

亮度模式。

# background-clip

注意和background-origin的区别。

#### border-box

默认值。背景绘制在边框方框内（剪切成边框方框）。

#### padding-box

背景绘制在衬距方框内（剪切成衬距方框）。

#### content-box

背景绘制在内容方框内（剪切成内容方框）。

# background-color

设置一个元素的背景颜色。

#### color

指定背景颜色。合法的颜色值。

#### transparent	

指定背景颜色应该是透明的。这是默认。

#### inherit	

指定背景颜色，应该从父元素继承

# background-image 

#### url('URL')	

图像的URL

#### none	

无图像背景会显示。这是默认

#### linear-gradient()	

创建一个线性渐变的 "图像"(从上到下)

#### radial-gradient()	

用径向渐变创建 "图像"。 (center to edges)

#### repeating-linear-gradient()	

创建重复的线性渐变 "图像"。

#### repeating-radial-gradient()	

创建重复的径向渐变 "图像"

#### inherit	

指定背景图像应该从父元素继承

#  background-origin

background-Origin属性指定background-position属性应该是相对位置。

注意如果背景图像background-attachment是"固定"，这个属性没有任何效果。

#### padding-box	

背景图像填充框的相对位置

#### border-box	

背景图像边界框的相对位置

#### content-box	

背景图像的相对位置的内容框

# background-position 

设置背景图像的起始位置。
注意对于这个工作在Firefox和Opera，background-attachment必须设置为 "fixed（固定）".

#### left|top|right|bottom|center left|top|right|bottom|center

如果仅指定一个关键字，其他值将会是"center" 

#### x% y%

第一个值是水平位置，第二个值是垂直。左上角是0％0％。右下角是100％100％。如果仅指定了一个值，其他值将是50％。 默认值为：0％0％。

# background-repeat

#### repeat	

背景图像将向垂直和水平方向重复。这是默认

#### repeat-x	

只有水平位置会重复背景图像

#### repeat-y	

只有垂直位置会重复背景图像

#### no-repeat	

background-image 不会重复

# background-size 

#### length	

设置背景图片高度和宽度。第一个值设置宽度，第二个值设置的高度。如果只给出一个值，第二个是设置为 auto(自动)

#### percentage	

将计算相对于背景定位区域的百分比。第一个值设置宽度，第二个值设置的高度，各个值之间以空格 隔开指定高和宽，以逗号 , 隔开指定多重背景。如果只给出一个值，第二个是设置为"auto(自动)"

#### cover	

此时会保持图像的纵横比并将图像缩放成将完全覆盖背景定位区域的最小大小。

#### contain	

此时会保持图像的纵横比并将图像缩放成将适合背景定位区域的最大大小。

tips: 注意cover和contain的微妙区别。

# border-collapse

#### collapse

如果可能，边框会合并为一个单一的边框。会忽略 border-spacing 和 empty-cells 属性

#### separate	

默认值。边框会被分开。不会忽略 border-spacing 和 empty-cells 属性

tips: table会默认外面还有一层边框就是这个原因。

#  border-color 

# border-image 

# border-image-outset

定义边框图像可超出边框盒的大小。

# border-image-repeat

#### stretch	

默认值。拉伸图像来填充区域

#### repeat	

平铺（repeated）图像来填充区域。	

#### round	

类似 repeat 值。如果无法完整平铺所有图像，则对图像进行缩放以适应区域。	

#### space

类似 repeat 值。如果无法完整平铺所有图像，扩展空间会分布在图像周围

# border-image-slice

border-image-slice 属性可以用四个指定的 <number-percentage> 值来表示每一个图像切片的位置。负数是无效的，而大于其相应的最大尺寸的值则会被限制为 100%。

border-image-slice 和 border-width 是用于定义边框样式的 CSS 属性，它们有不同的作用和效果。

border-width: 用于定义边框的宽度。可以通过设置 border-width 属性来指定边框的厚度，可以是一个值（如 1px）或者是四个值（如 1px 2px 3px 4px，分别表示上、右、下、左四个边的宽度）。

border-image-slice: 用于定义边框图片的裁剪区域。border-image-slice 属性指定了用于边框的图片裁剪区域的大小。它可以接受一个值，也可以是四个值，分别表示裁剪区域的上、右、下、左四个边的大小。

这两个属性的作用不同，border-width 主要用于定义边框的宽度，而 border-image-slice 则用于定义边框图片的裁剪区域。它们通常用于不同的场景。

虽然它们都涉及到边框的样式，但是不能完全实现相同的效果。border-width 用于定义纯色边框的宽度，而 border-image-slice 用于定义基于图片的边框效果。通过结合使用这两个属性，可以实现更加丰富和复杂的边框样式。

# border-image-source

指定要使用的图像，而不是由border-style属性设置的边框样式。

# border-image-width

指定图像边界的宽度。

# border-left

# border-left-color 

# border-left-style

# border-left-width 

# border-radius

# border-right 

# border-right-color

# border-right-style 

# border-right-width

# border-spacing
设置相邻单元格的边框间的距离（仅用于"边框分离"模式）。
`border-spacing` 属性是用于设置表格元素中的单元格之间的边框间距的。它可以用于表格元素（ `<table>` ）以及具有 `display: table` 或 `display: inline-table` 样式的元素。

虽然 `border-spacing` 属性最常用于表格元素，但它并不是只能用于表格。任何具有 `display: table` 或 `display: inline-table` 样式的元素都可以使用 `border-spacing` 属性来设置单元格之间的边框间距。

另外，对于普通的块级元素，我们也可以使用 `margin` 属性来实现类似的效果，用于设置元素之间的外边距，但它并不是专门用于表格或表格样式的元素。

# border-style

# border-top 

# border-top-color 

# border-top-left-radius

# border-top-right-radius

# border-top-style

# border-top-width

# border-width 

# bottom 

# box-align 

> 前提条件：display设置为box

目前所有主流浏览器都不支持 box-align 属性。

Internet Explorer 10 通过私有属性 -ms-flex-align 支持.

Firefox通过私有属性- MOZ-box-align支持。

Safari和Chrome通过私有属性-WebKit-box-align支持。

#### start	

对于正常方向的boxes，每个子元素的顶部边缘放在沿box的顶部。反向箱，每个子元素的底边放在沿box的底部

#### end	

对于正常方向的boxes，每个子元素的顶部边缘放在沿box的底部。反向箱，每个子元素的底边放在沿box的顶部

#### center	

任何多余的空间被划分均匀，一半以上的子元素放在上面，剩下的子元素放在另一半

#### baseline	

如果box-orient是内嵌单轴或横向，所有的子元素都置于他们的基线对齐

#### stretch	

子元素拉伸以填充包含区块

# box-direction

#### normal	

以默认方向显示子元素。

#### reverse	

以反方向显示子元素。

#### inherit	

应该从子元素继承 box-direction 属性的值

# box-flex

# box-flex-group

# box-lines

# box-ordinal-group 

# box-orient

# box-pack

> 前提条件：display设置为box

#### start	

对于普通方向的boxes，左边缘的第一个子元素被放置在左侧（所有额外的空间放置后的最后一个子元素）。对于反向
boxes，右边缘最后一个子元素放置在右侧（所有额外的空间放置前的第一个子元素）

#### end	

对于正常的方向的boxes，最后一个子元素的右边缘放置在右侧（所有额外的空间放置前的第一个子元素）。对于反向boxes，第一个孩子的左边缘放置在左侧（所有额外的空间放置后的最后一个子元素）

#### center	

额外的空间划分均匀的两半，前一半放置第一个子元素，另一半放置最后一个子元素

#### justify	

额外的空间平均分配给每个子元素

# box-shadow 

# box-sizing

# caption-side 

#### top	

默认值。把表格标题定位在表格之上。

#### bottom	

把表格标题定位在表格之下。

#### inherit	

规定应该从父元素继承 caption-side 属性的值。

# clear

指定段落的左侧或右侧不允许浮动的元素。

# clip

#### shape	

设置元素的形状。唯一合法的形状值是：rect (top, right, bottom, left)

#### auto	

默认值。不应用任何剪裁。

#### inherit	

规定应该从父元素继承 clip 属性的值。

# color

指定**文本**的颜色。

# column-count

#### number	

列的最佳数目将其中的元素的内容无法流出

#### auto	

列数将取决于其他属性，例如："column-width"

# column-fill

> 几乎没有浏览器支持

#### balance	

列长短平衡。浏览器应尽量减少改变列的长度

#### auto	

列顺序填充，他们将有不同的长度

# column-gap

# column-rule 

# column-rule-color 

# column-rule-style

# column-rule-width

# column-span 

# column-width 

# columns 

```css
columns: column-width column-count;
```

# content

```css
content: normal|none|counter|attr|string|open-quote|close-quote|no-open-quote|no-close-quote|url|initial|inherit;
```

#### none	

设置 content 为空值。	尝试一下 »

#### normal	

在 :before 和 :after 伪类元素中会被视为 none，即也是空值。

#### counter	

设定计数器，格式可以是 counter(name) 或 counter(name, style) 。产生的内容是该伪类元素指定名称的最小范围的计数；格式由style指定（默认是'decimal'——十进制数字）

#### attr(attribute)	将元素的 attribute 属性以字符串形式返回。

#### string

设置文本内容

#### open-quote	

设置前引号

#### close-quote	

设置后引号

#### no-open-quote	

移除内容的开始引号

#### no-close-quote	

移除内容的闭合引号	尝试一下 »

#### url(url)	

设置某种媒体（图像，声音，视频等内容）的链接地址	

#### inherit	

指定的 content 属性的值，应该从父元素继承

# counter-increment 

递增一个或多个计数器值。

# counter-reset 

创建或重置一个或多个计数器。

# cursor

#### url	

需使用的自定义光标的 URL。

注释：请在此列表的末端始终定义一种普通的光标，以防没有由 URL 定义的可用光标。

#### default	

默认光标（通常是一个箭头）

#### auto	

默认。浏览器设置的光标。

#### crosshair	

光标呈现为十字线。

#### pointer	

光标呈现为指示链接的指针（一只手）

#### move	

此光标指示某对象可被移动。

#### e-resize	

此光标指示矩形框的边缘可被向右（东）移动。

#### ne-resize	

此光标指示矩形框的边缘可被向上及向右移动（北/东）。

#### nw-resize	

此光标指示矩形框的边缘可被向上及向左移动（北/西）。

#### n-resize	

此光标指示矩形框的边缘可被向上（北）移动。

#### se-resize	

此光标指示矩形框的边缘可被向下及向右移动（南/东）。

#### sw-resize	

此光标指示矩形框的边缘可被向下及向左移动（南/西）。

#### s-resize	

此光标指示矩形框的边缘可被向下移动（南）。

#### w-resize	

此光标指示矩形框的边缘可被向左移动（西）。

#### text	

此光标指示文本。

#### wait	

此光标指示程序正忙（通常是一只表或沙漏）。

#### help	

此光标指示可用的帮助（通常是一个问号或一个气球）。

# direction

指定文本方向/书写方向。

#### ltr	

默认。文本方向从左到右。

#### rtl	

文本方向从右到左。

#### inherit	

规定应该从父元素继承 direction 属性的值。

# display

设置元素的内部和外部的显示类型。

#### none	

此元素不会被显示。

#### block	

此元素将显示为块级元素，此元素前后会带有换行符。

#### inline	

默认。此元素会被显示为内联元素，元素前后没有换行符。

#### inline-block	

行内块元素。（CSS2.1 新增的值）

#### list-item	

此元素会作为列表显示。

#### run-in	

此元素会根据上下文作为块级元素或内联元素显示。

#### compact	

CSS 中有值 compact，不过由于缺乏广泛支持，已经从 CSS2.1 中删除。

#### marker	

CSS 中有值 marker，不过由于缺乏广泛支持，已经从 CSS2.1 中删除。

#### table	

此元素会作为块级表格来显示（类似 <table>），表格前后带有换行符。

#### inline-table	

此元素会作为内联表格来显示（类似 <table>），表格前后没有换行符。

#### table-row-group	

此元素会作为一个或多个行的分组来显示（类似 `<tbody>` ）。

#### table-header-group	

此元素会作为一个或多个行的分组来显示（类似 `<thead>` ）。

#### table-footer-group	

此元素会作为一个或多个行的分组来显示（类似 `<tfoot>` ）。

#### flow-root	

生成一个块级元素盒，其会建立一个新的块级格式化上下文，定义格式化上下文的根元素。

#### table-row	

此元素会作为一个表格行显示（类似 `<tr>` ）。

#### table-column-group	

此元素会作为一个或多个列的分组来显示（类似 `<colgroup>` ）。

#### table-column	

此元素会作为一个单元格列显示（类似 `<col>` ）

#### table-cell	

此元素会作为一个表格单元格显示（类似 `<td>` 和 `<th>` ）

#### table-caption	

此元素会作为一个表格标题显示（类似 `<caption>` ）

#### inherit	

规定应该从父元素继承 display 属性的值。

# empty-cells

定义了应该怎么来渲染表格 `<table>` 中没有可见内容的单元格的边框和背景。

#### show

边框和背景正常渲染。与普通元素一样。

#### hide

边框和背景被隐藏。

# filter

```css
filter: none | blur() | brightness() | contrast() | drop-shadow() | grayscale() | hue-rotate() | invert() | opacity() | saturate() | sepia() | url();
```

# flex

# flex-basis

#  flex-direction

# flex-flow 
 flex-direction 和 flex-wrap 的简写。

```css
lex-flow: flex-direction flex-wrap;
```

# flex-grow 

设置或检索弹性盒子的扩展比率。

```css
flex-grow: number|initial|inherit;
```
tips：所有元素都设置为`flex-grow:0;`或`flex-grow:1`还是有区别的，前者不会占据其他空间，后者会占据其他空间。