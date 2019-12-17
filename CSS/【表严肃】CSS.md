### CSS

学习与【表严肃】

#### 引入CSS样式方式

```
1：外部样式链接 Link
2：导入 @import url()--不建议，要将此定义在文件最开始，否则会失效
3：Head中样式 Style
4：行内样式 <p style="color:red"></p>-不灵活
   ！important，压倒性的样式，正常不建议使用，优先级最高
```

#### 注释

##### HTML注释

```html
<!-- 我是注释-->
```

##### CSS注释

```css
/*我是注释*/
.a{
    color：red;
}
```

#### 选择器

##### 元素选择器

```
单个元素
元素组，使用逗号隔开

使用场景，优缺点，限制？？
```

##### 类选择器

定义页面中一组元素的样式，给页面添加标签的

```html

普通形式
.red{
  color:red;
}
.green{
  background:green;  
}
<p class="red"></p>
<p class="green"></p>

作用多个类

<p class="red green"></p>

类组合
一：无空格，代表元素上同时有red,green样式的元素，再增加新的样式
.red.green{
    font-size:20px;
}
二：有空格,有一种继承的感觉，代表red样式下，还具有green样式的元素，再增加新的样式
.red .green{
    font-size:20px;
}
.red .green .black{# 有一种继承的感觉，red下的green下的black的元素，再增加新的样式
    font-size:30px;
}

```

##### ID选择器

定位页面中的单个元素，确定页面元素唯一性
id建议保证唯一性，虽然可以定义同一个id，浏览器依旧可以解析，但建议唯一性

```html

#logo{
color:green;
}

<p id="logo"></p>
```

##### 属性选择器

```html
使用方括号包裹属性

适用场景：？？？

html元素的属性
[title]:{
   color:green;
}

# 完全匹配
[title="点击我"]：{
    color:green;
}
# 包含有点击文字的
[title*="点击"]{
    color:green;
}
# 以点击两个字开始的
[title^="点击"]{
    color:green;
}
# 以点击两个字结束的
[title$="点击"]{
    color:green;
}


要注意css样式的顺序

先定义通用的样式，在编写自定义的样式，这样自定义的样式就会覆盖通用样式


<button title="点击我">按钮</button>
<button title="你来点击我">按钮</button>
<button title="快点点击">按钮</button>
<button title="点击我一下">按钮</button>

```

##### 后代选择器

```
后代选择器非常灵活，只要是后代，无论层级多深都会覆盖样式

爷爷（a）-爸爸（b）-儿子（c）-孙子（d）

所有后代
.a *{

}
a的b后代
.a .b{

}
a的c后代（先找a，再找b，再找c）
.a .b .c {

}
a的c后代(如果c后代还包含一个类名为c的也会更改，会将a的所有c后代样式进行更改)
.a .c{

}

```

##### 相邻选择器

```html
特性：从上往下


# 与a同级的相邻div样式
.a + div{
   background:red;
}
# 与a同级的之后所有的div样式
.a ~ div{
   background:red;
}

假如把a改为了b，则仅c的样式会更改
# 与b同级的相邻div样式
.b + div{
   background:red;
}
# 与b同级的之后所有的div样式
.b ~ div{
   background:red;
}

<body>
<div class="a"></div>
<div class="b"></div>
<div class="c"></div>
</body>
```

##### 伪类选择器

:冒号，想类选择器又不是类

常用伪类选择器：:link,.visited,:hover,:active,:focus

```css
a:link{
color:red;
}
a:visited{
color:bule;
}
button:hover{
background:blue;
}
button:active{
background:red;
}
input:focus{
color:red;
}
```

```html

<body>
<a href="http://www.baidu.com"></a>
<button>点我</button>
</body>


```

##### 伪元素选择器

元素实际不存在，仅有其逻辑意义

可以使用单冒号，也可以双冒号，建议使用单冒号，兼容性好一些

常用伪元素选择器：:before,:after,:first-letter,:first-child,:last-child,:ntn-child(2)

```css
文章段落首字母字体放大效果
 
p:first-letter{
    font-size:50px;
}
<p>Limte is yong peple</p>
```

```
在元素前面或后面添加补充内容
例如：网页中经常会有在问题后面有一个帮助文档的小图标，提示用户可以查看帮助文档

p:after{
content:"[?]";
color:blue;
}

p.before{
content:"[!]";
color:blue;
}

所有p标签后面均会添加帮助图标
所有p标签前面均会添加感叹号图标

<p>什么是物流信息</p>
<p>什么是行政信息</p>
<p>什么是邮政信息</p>

```



```css
想要实现的效果：希望div中某个子元素背景样式进行修改
/*第一个元素*/
parent:first-child{
    background:red;
}
/*最后一个元素*/
parent:last-child{
     background:green;
}
/*第二个元素*/
parent:nhn-child(2){
     background:blue;
}


<div class="parent">
<div class="a"></div>
<div class="b"></div>
<div class="c"></div>
</div>
```

##### 选择器权重

```css
styles属性(内联)>ID选择器>类选择器/属性选择器/伪类选择器>元素选择器
```



##### 字体属性

```css
font-family 
font-weight 100-900之间
font-size
```

##### 文字属性

```css
text-align:left,right,center,justify
line-heigh:行高，line-heigh与font-size的关系
text-decoration:文字装饰，underline,overline,line-through,none
```

##### display

```css
display:block(块级元素)/inline(行内元素)/inline-block(行内块元素)/none（不显示）-隐藏元素

行内元素：margin，padding仅左右有效，上下无效
行内块元素，margin，padding上下左右均有效
```

##### 框

```

content-内容

padding-内边距

border-边框

margin-外边距
```

