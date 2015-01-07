css3
====

## 1 CSS3介

### 1.1 概念

CSS即层叠样式表（Cascading StyleSheet）。 在网页制作时采用层叠样式表技术，可以有效地对页面的布局、字体、颜色、背景和其它效果实现更加精确的控制。 只要对相应的代码做一些简单的修改，就可以改变同一页面的不同部分，或者页数不同的网页的外观和格式。

CSS3是CSS技术的升级版本，CSS3语言开发是朝着模块化发展的。以前的规范作为一个模块实在是太庞大而且比较复杂，所以，把它分解为一些小的模块，更多新的模块也被加入进来。这些模块包括：盒子模型、列表模块、超链接方式、语言模块、背景和边框、文字特效、多栏布局等。

### 1.2优点

CSS3的优点远远不止于能让页面看起来酷炫异常--尽管这也是不可忽视的。

CSS3能创建很多十分炫目的效果，使网站设计锦上添花。

### 1.3发展史

**CSS1**

作为一项W3C推荐，CSS1发布于 1996年12月17 日。1999 年1月11日，此推荐被重新修订。

**CSS2**

作为一项 W3C 推荐，CSS2发布于 1999年1月11日。CSS2添加了对媒介（打印机和听觉设备）和可下载字体的支持。

**CSS3**

CSS3计划将CSS划分为更小的模块。

### 1.4 浏览器对CSS3的支持状况

![Image of CSS3]
(http://a1.jikexueyuan.com/home/201501/07/63b5/54acae5b78c84.png)

### 1.5 CSS3的发展状况及未来趋势

CSS3无疑对Web前端开发带来质的飞跃。虽然目前CSS3还没有完全普及，而且浏览器也不完全支持，但对于我们积极地去学习和实践并不矛盾，掌握和学习CSS3将是大势所趋。CSS3将是引导我们进入编写网页精彩世界的先驱技术。

开发人员能够更轻松地创建功能强大、易于维护网站。随着旧版浏览器所占市场份额逐渐减少，学习CSS3技术将更有价值。这是作为一位优秀前端开发人员所必须掌握的技术之一，也是前端开发人员的大势所趋。当然，学习一门新技术不能跟风，需要理性思考，这种理性思考并不表示对新技术的畏缩，同时也应该明白学习新技术可能会遇到的困难和风险。只有这样，才能更好地驾驭CSS3。

## 2 CSS3选择器

### 2.1 概念

每一条css样式定义由两部分组成，形式如下：

```
[code] 选择器{样式} [/code] 
```

在{}之前的部分就是“选择器”。 “选择器”指明了{}中的“样式”的作用对象，也就是“样式”作用于网页中的哪些元素。

### 2.2属性选择器：E[attr]

为CSS3属性选择器中最简单的一种，只使用属性名，不确定任何属性值。

例：为带有target属性的链接添加红色背景

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
a[target]
{
background-color:red;
}
</style>
</head>
<body>

<p>带有 target 属性的链接会得到红色背景：</p>

<a href="http://www.jikexueyuan.com">www.jikexueyuan.com</a>
<a href="www.jikexueyuan.com/resources/" target="_blank">http://www.jikexueyuan.com/resources/</a>
<a href="www.jikexueyuan.com/vip/" target="_top">http://www.jikexueyuan.com/vip/</a>

</body>
</html>
```

> 注：对于 IE8 及更早版本的浏览器中的 [<i>attribute</i>]，必须声明 <!DOCTYPE>。

### 2.3 属性选择器：E[attr="value"]

指定属性的值，可以更精确的获得自己需要的元素。

例：为带有target=“blank"的链接添加红色背景

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
a[target=_blank]
{
background-color:red;
}
</style>
</head>
<body>

<p>target="_blank" 的链接会得到红色背景：</p>

<a href="http://www.w3school.com.cn">www.jikexueyuan.com</a>
<a href="http://www.disney.com" target="_blank">http://www.jikexueyuan.com/resources/</a>
<a href="http://www.wikipedia.org" target="_top">http://www.jikexueyuan.com/vip/</a>

</body>
</html>
```

> 注：对于 IE8 及更早版本的浏览器中的 [<i>attribute</i>]，必须声明 <!DOCTYPE>。

### 2.4 属性选择器：E[attr~="value"]

可根据属性值中的词列表的某个词来进行选择元素，选择器是属性值是一个或多个词列表，如果是列表时，他们需要用空格隔开，只要属性值中有一个value相匹配就可以选中该元素，而我们前面所讲的`E[attr="value"]`是属性值需要完全匹配才会被选中，两者区别就是一个有“〜”号，一个没有“〜”号。

例：
```javascript
<!DOCTYPE html>
<html>
<head>
<style>
[title~=jike]
{
border:5px solid red;
}
</style>
</head>
<body>

<p>title 属性中包含单词 "jike" 的图片会获得红色边框。</p>

<img src="http://a1.jikexueyuan.com/home/201412/21/21df/5496e376f33c7.jpg" title="jike xueyuan" />
<br />
<img src="http://a1.jikexueyuan.com/home/201412/21/21df/5496e376f33c7.jpg" title="egret" />

</body>
</html>
```

> 注：对于 IE8 及更早版本的浏览器中的 [attribute~=value]，必须声明 <!DOCTYPE>。


### 2.5 属性选择器：E[attr^="value"]

指选择attr属性值以“value”开头的所有元素，换句话说，选择的属性其以对应的属性值是以“value”开始的

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
<style type="text/css">
p[title^="val"] {color:#FF0000;}
</style>
</head>
<body>
<div style="width:733px; border: 1px solid #666; padding:5px;">
<p title="value">匹配具有att属性、且值以val开头的E元素</p>
</div>
</body>
</html>
```

### 2.6 属性选择器：E[attr$="value"]

匹配具有att属性、且值以val结尾的E元素

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style type="text/css">
p[title$="val"] {font-weight:bold;}
</style>
</head>
<body>
<div style="width:733px; border: 1px solid #666; padding:5px;">
<p title="this is val">匹配具有att属性、且值以val结尾的E元素</p>
</div>
</body>
</html>
```

### 2.7 属性选择器：E[attr*="value"]

匹配具有att属性、且值中含有val的E元素

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style type="text/css">
p[title*="val"] {text-decoration:underline;}
</style>
</head>
<body>
<div style="width:733px; border: 1px solid #666; padding:5px;">
<p title="have val word">匹配具有att属性、且值中含有val的E元素</p>
</div>
</body>
</html>
```

### 2.8 伪类选择器：E:root

匹配文档的根元素，在HTML中，根元素永远是HTML。

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
:root
{
background:#35b558;
}
</style>
</head>
<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p>第二行</p>
<p>第三行。</p>

</body>
</html>
```

### 2.9  伪类选择器：E:nth-child(n)

匹配父元素中的第n个子元素E

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:nth-child(2)
{
background:#35b558;
}
</style>
</head>
<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p>第二行</p>
<p>第三行</p>

</body>
</html>
```

> 注：</b>Internet Explorer 不支持 :nth-child() 选择器。

### 2.10 伪类选择器：nth-last-child()

规定属于其父元素的第二个子元素的每个 p 元素，从最后一个子元素开始计数。

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:nth-last-child(2)
{
background:#35b558;
}
</style>
</head>
<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p>第二行</p>
<p>第三行</p>

</body>
</html>
```

### 2.11 伪类选择器：E:nth-of-type(n)

匹配同类型中的第n个同级兄弟元素E

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:nth-of-type(2)
{
background:#35b558;
}
</style>
</head>
<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p>第二行</p>
<p>第三行</p>

</body>
</html>
```

### 2.12 伪类选择器：E:nth-last-of-type(n)

匹配同类型中的倒数第n个同级兄弟元素E

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:nth-last-of-type(2)
{
background:#35b558;
}
</style>
</head>
<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p>第二行</p>
<p>第三行</p>

</body>
</html>
```

### 2.13 结构性伪类选择器：E:last-child

匹配父元素中最后一个E元素

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:last-child
{
background:#35b558;
}
</style>
</head>
<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p>第二行</p>
<p>第三行</p>

</body>
</html>
```

### 2.14 结构性伪类选择器：E:first-of-type

匹配同级兄弟元素中的第一个E元素

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:first-of-type
{
background:#35b558;
}
</style>
</head>

<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p>第二行</p>
<p>第三行</p>

</body>
</html>
```

### 2.15 结构性伪类选择器：E:only-child

匹配属于父元素中唯一子元素的E

例：
```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:last-child
{
background:#35b558;
}
</style>
</head>
<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p>第二行</p>
<p>第三行</p>

</body>
</html>
```

### 2.16 结构性伪类选择器：E:only-of-type

匹配属于同类型中唯一兄弟元素的E

例：
```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:only-of-type
{
background:#35b558;
}
</style>
</head>

<body>

<div>
<p>第一行</p>
</div>

<div>
<p>第二行</p>
<p>第三行</p>
</div>

</body>
</html>
```

### 2.17 结构性伪类选择器：E:empty

匹配没有任何子元素（包括text节点）的元素E

例：
```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p:empty
{
width:100px;
height:20px;
background:#35b558;
}
</style>
</head>
<body>

<h1>标题-极客学院</h1>
<p>第一行</p>
<p></p>
<p>第二行</p>
<p>第三行</p>
<p>第四行</p>

</body>
</html>
```

### 2.18 UI元素状态伪类选择器：E:checked

匹配所有用户界面（form表单）中处于选中状态的元素E

例：
```javascript
<!DOCTYPE html>
<html>
<head>
<style>
input:checked
{
background:#ff0000;
}
</style>
</head>
<body>

<form action="">
<input type="radio" checked="checked" value="male" name="gender" /> Male<br>
<input type="radio" value="female" name="gender" /> Female<br>
<input type="checkbox" checked="checked" value="Bike" /> I have a bike<br>
<input type="checkbox" value="Car" /> I have a car
</form>

</body>
</html>
```

> 注：由于只有Opera支持，本例只在 Opera 中正确工作。

### 2.19 UI元素状态伪类选择器：E:enabled

匹配所有用户界面（form表单）中处于可用状态的E元素

例：
```javascript
<!DOCTYPE html>
<html>
<head>
<style>
input[type="text"]:enabled
{
background:#ffff00;
}
input[type="text"]:disabled
{
background:#dddddd;
}
</style>
</head>
<body>

<form action="">
First name: <input type="text" value="jike" /><br>
Last name: <input type="text" value="xueyuan" /><br>
Country: <input type="text" disabled="disabled" value="Disneyland" /><br>
</form>

</body>
</html>
```

### 2.20 UI元素状态伪类选择器：E:enabled

匹配所有用户界面（form表单）中处于不可用状态的E元素

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
input[type="text"]:enabled
{
background:#ffff00;
}
input[type="text"]:disabled
{
background:#dddddd;
}
</style>
</head>
<body>

<form action="">
First name: <input type="text" value="jike" /><br>
Last name: <input type="text" value="xueyuan" /><br>
Country: <input type="text" disabled="disabled" value="Disneyland" /><br>
</form>

</body>
</html>
```

### 2.21 UI元素状态伪类选择器：E::selection

匹配E元素中被用户选中或处于高亮状态的部分

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
::selection
{
color:#ff0000;
}
::-moz-selection
{
color:#ff0000;
}
</style>
</head>
<body>

<h1>请试着选取页面上的文本</h1>

<p>一行文字一行文字</p>

<div>这是 div 元素中的文本。</div>

<br>

<a href="http://www.jikexueyuan.com" target="_blank">访问 极客学院</a>

</body>
</html>
```

### 2.22 目标伪类： E:target

匹配相关URL指向的E元素

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
:target
{
border: 2px solid #D4D4D4;
background-color: #e5eecc;
}
</style>
</head>
<body>

<h1>这是标题</h1>

<p><a href="#news1">显示第一行</a></p>
<p><a href="#news2">显示第二行</a></p>

<p>请点击上面的链接，:target 选择器会突出显示当前活动的 HTML 锚点。</p>

<p id="news1"><b>第一行...</b></p>
<p id="news2"><b>第二行...</b></p>

</body>
</html>
```

> 注：</b> Internet Explorer 8 以及更早的版本不支持 :target 选择器。

### 2.23 否定伪类： E:not(s)

匹配所有不匹配简单选择符s的元素E

例：

```javascript
<!DOCTYPE html>
<html>
<head>
<style>
p
{
color:#000000;
}
:not(p)
{
color:#ff0000;
}
</style>
</head>
<body>

<h1>这是标题</h1>

<p>第一行</p>

<p>第二行</p>

<div>这是 div 元素中的文本。</div>

<br>

<a href="http://www.jikexueyuan.com" target="_blank">访问 极客学院</a>

</body>
</html>
```



