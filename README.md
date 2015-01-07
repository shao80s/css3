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
