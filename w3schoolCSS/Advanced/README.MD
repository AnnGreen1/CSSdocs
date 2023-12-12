# 清除浮动

如果一个元素比包含它的元素高，并且它是浮动的，它将“溢出”到其容器之外：

然后我们可以向包含元素添加 overflow: auto; ，来解决此问题：

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        div {
            border: 3px solid #4CAF50;
            padding: 5px;
        }

        .img1 {
            float: right;
        }

        .clearfix {
            overflow: auto;
        }

        .img2 {
            float: right;
        }
    </style>
</head>

<body>

    <h1>Clearfix</h1>

    <p>在本例中，图像高于包含它的元素，然而它被浮动了，所以它会在容器之外溢出：</p>

    <div>
        <img class="img1" src="/i/logo/w3logo-3.png" alt="W3School" width="180" height="167">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum...
    </div>

    <p style="clear:right">请为包含元素添加一个带有 overflow: auto; 的 clearfix 类，以解决此问题：</p>

    <div class="clearfix">
        <img class="img2" src="/i/logo/w3logo-3.png" alt="W3School" width="180" height="167">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum...
    </div>

</body>

</html>
```

只要您能够控制外边距和内边距（否则您可能会看到滚动条），overflow: auto clearfix 就会很好地工作。但是，新的现代 clearfix hack 技术使用起来更安全，以下代码被应用于多数网站：

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        div {
            border: 3px solid #4CAF50;
            padding: 5px;
        }

        .img1 {
            float: right;
        }

        .clearfix::after {
            content: "";
            clear: both;
            display: table;
        }

        .img2 {
            float: right;
        }
    </style>
</head>

<body>

    <p>在本例中，图像高于包含它的元素，然而它被浮动了，所以它会在容器之外溢出：</p>

    <div>
        <h1>Without Clearfix</h1>
        <img class="img1" src="/i/logo/w3logo-3.png" alt="W3School" width="180" height="167">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum...
    </div>

    <p style="clear:right">请为包含元素添加 clearfix hack，以解决此问题：</p>

    <div class="clearfix">
        <h1>With Clearfix</h1>
        <img class="img2" src="/i/logo/w3logo-3.png" alt="W3School" width="180" height="167">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum...
    </div>

</body>

</html>
```

# 变量
var() CSS 函数可以插入一个自定义属性（有时也被称为“CSS 变量”）的值，用来代替非自定义属性中值的任何部分。

var() 函数不能作为属性名、选择器或者其他除了属性值之外的值。（这样做通常会产生无效的语法或者一个没有关联到变量的值。）

函数的第一个参数是要替换的自定义属性的名称。函数的第二个参数是可选的，用作回退值。如果第一个参数引用的自定义属性无效，则该函数将使用第二个值。

tips：在实际应用中变量被定义为以两个破折号开始的任何有效标识符。自定义属性仅供作者和用户使用; CSS 将永远不会给他们超出这里表达的意义（因为 CSS 规范中规定只有官方定义的属性才能以单个连字符开头）。