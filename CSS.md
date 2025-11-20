##### <mark class="hltr-pink">语法</mark>

  <span style="font-size: 40px ;border:10px solid blue ;color:darkblue">h1 { color: blue; font-size:12px}</span>
选择器      属性     冒号    值   (分号)

##### <mark class="hltr-pink">css运行：</mark>
1. 浏览器载入HTML 文件.
2. 将 HTML 文件转化成一个 DOM（Document Object Model）
3. 接下来，浏览器会拉取该 HTML 相关的大部分资源，比如嵌入到页面的图片、视频和 CSS 样式。JavaScript 则会稍后进行处理.
4. 浏览器拉取到 CSS 之后会进行解析，根据选择器的不同类型（比如 element、class、id 等等）把他们分到不同的“桶”中,将不同的规则（基于选择器的规则，如元素选择器、类选择器、id 选择器等）应用在对应的 DOM 的节点中.
5. 上述的规则应用于渲染树.
6. 着色.

----
<mark class="hltr-pink">PreKnow:</mark>
# 层叠、优先级与继承

#### 冲突规则,CSS 代表**层叠样式表**

- 样式表层叠,写在后面的就是实际使用的规则
- 浏览器是根据优先级来决定不同选择器,需要使用哪个规则
- 继承
     <mark class="hltr-pink">这三个概念一起来控制 CSS 规则应用于哪个元素</mark>


# 继承
 #继承 
 
 ```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
------------------------------------------------------------------
<style>
.main{
    color: rebeccapurple;
    border: 2px solid #ccc;
    padding: 1em;
}

.special{
    color:rgb(125, 200, 175);
    font-weight: bold;
}
</style>
--------------------------------------------------------------------
</head>

<body>
    <ul class="main">
        <li>吃烧烤</li>
        <li>吃蔬果
            <ul>
                <li>土豆</li>
                <li>西瓜</li>
            </ul>
        </li>
        <li>
            吃雪糕
            <ul class="special">
                <li>
                    奶油和糖
                    <ul>
                        <li>变成🍫</li>
                        <li>变成🍰</li>
                    </ul>
                </li>
                <li>牛奶和糖</li>    
            </ul>
        </li>
</body>
</html>
```

# <mark class="hltr-pink">控制继承</mark>

- inherit
    “开启继承”。
- initial
	选定元素为该属性的初始值。
- revert
	浏览器的默认样式
- revert-layer
	上一个层叠层中建立的值。
- unset自然值,如果属性是自然继承那么就是 inherit，否则和 initial 一样

```html
<!DOCTYPE html>
<html>
    <head>
    <style>
        /* 默认(链接蓝色,字体是黄色) */
        body{
            color:rgb(235, 172, 95);
        }
        /* 继承 */
        .class-1 a {
            color:inherit;
        }
        /* 重制(链接黑色,字体黄) */
        .class-2 a{
            color:initial;
        }
        /* 取消了(链接字体全是黄色),和inherit一样 */
        .class-3 a{
            color:unset;
        }
    </style>
    </head>
    <body>
        <ul>
            <li>默认<a href="#">链接</a>颜色</li>
            <li class="class-1">继承<a href="#">链接</a>颜色</li>
            <li class="class-2">重制<a href="#">链接</a>颜色</li>
            <li class="class-3">取消<a href="#">链接</a>颜色的设置</li>
        </ul>
    </body>
</html>
```

# <mark class="hltr-pink">重设所有属性值</mark>

<mark class="hltr-pink">all</mark>
```html
<style>
      blockquote{
        background-color: rgb(141, 225, 99);
        border: 2px dotted blue;
      }

      .fix-this{
        all:unset;
      }

    </style>
    </head>

    <body>
        
            <blockquote>
                <p>有点东西</p>
            </blockquote>
        
            <blockquote class="fix-this">
                <p>没啥东西</p>
            </blockquote>
    </body>
```


<span style="font-size:  25px;">类选择器的权重大于元素选择器</span>
#优先级
- 类选择器的权重大于元素选择器，因此类上定义的属性将覆盖应用于元素上的属性。
```html
    <style>
    h2{
        font-size: 2em;
        color: #222;
        font-family: Geogia,"Time New Roman", Times, serif;
    }

    .small{
        font-size: 1em;
    }

    .bright{
        color: rgb(195, 151, 238);
    }

    </style>
    </head>

    <body>
        <h2>啥也咩呦,就是普通的h2标志</h2>

        <h2 class="small">是small的css</h2>
        
        <h2 class="bright">是bright的css</h2>
    </body>
</html>
```

<mark class="hltr-pink">选择器的优先级</mark>
- **ID**：选择器中包含<mark class="hltr-pink"> ID </mark>选择器则百位得一分。
- **类**：选择器中包含<mark class="hltr-pink">类</mark>选择器、<mark class="hltr-pink">属性</mark>选择器或者<mark class="hltr-pink">伪类</mark>则十位得一分。
- **元素**：选择器中包含<mark class="hltr-pink">元素、伪元素</mark>选择器则个位得一分。
- ---
## HTML 怎么转化成 DOM

```html

<p>
  Let's use:
  <span>Cascading</span>
  <span>Style</span>
  <span>Sheets</span>
</p>

DOM:
P
├─ "Let's use:"
├─ SPAN
|  └─ "Cascading"
├─ SPAN
|  └─ "Style"
└─ SPAN
    └─ "Sheets"

<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<style>
    span{
        border: 1px dashed greenyellow;
        background-color: lightsalmon;
    }
</style>
<body>
    <p>
        我们来看看铁锤在干嘛:
        <span>铁锤</span>
        <span>躺在我脚边</span>
        <span>呼呼大睡</span>
    </p>
</body>
</head>
</html>
```
![[Pasted image 20250723152555.png]]
- 一个**浏览器在解析CSS** 规则遇到了**无法理解**的属性或者值，会**忽略**这些**并继续解析**下面的 CSS 声明。**直接忽略**
---
 
# HTML + CSS
 
最普遍:在文档的开头链接 CSS
- HTML 文档的相同目录创建一个文件(.css)
```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="PracFirst.css"/>
<meta charset="utf-8">
<title>铁锤在挣扎CSS</title>
</head>

<body>
    <h1>这是一号大狗头</h1>```

```css
/* <title>铁锤在挣扎CSS</title> */
h1{
    color:red;
}
```

### 样式化 HTML 元素
- 直接匹配 HTML 元素的选择器

```css
/* <title>铁锤在挣扎CSS</title> */
h1{
    color:rgb(245, 113, 43);
}

p,
li{
    color :lab(59.58% 71.26 -23.25)
}
```

## 改变元素的默认行为
 - 比如:项目符号
	` list-style-type`
```css
p,
li{
    color :lab(59.58% 71.26 -23.25);
    list-style-type: square;
}
```
![[Pasted image 20250723160338.png]]![[Pasted image 20250723161036.png]]

## class
```html
<li>今天</li>
        <li class="special">好乖</li>
        <li>我的<em>饭呢</em></li>
```

```css
.special{
    color:rgb(157, 170, 134);
    font-weight: bold;
}
```
## 根据元素在文档中的位置确定样式
- < li>内部的任何< em>元素
- < p>元素没有变化
```
css
li em{
    color:rgb(38, 142, 35)
}

html
<ul>
        <li>今天</li>
        <li class="special">好乖</li>
        <li>我的<em>饭呢</em></li>
    </ul>
```
![[Pasted image 20250723164859.png]]

### 根据状态确定样式
-  < a> （锚）标签。取决于是否是**未访问**的、**访问过**的、**被鼠标悬停**的、**被键盘定位的**，亦或是**正在被点击当中**的状态，这个标签有着不同的状态。
```css
/* 未访问 */
a:link{
    color: rgb(247, 177, 189);
}
/* 已经访问 */
a:visited{
    color:rgb(101, 142, 178)
}

/* 悬浮(没有下划线) */
a:hover{
    text-decoration: none;
}
```

---
# html和CSS分开
```html
<!DOCTYPE html> 
<html>
<head>
<link rel="stylesheet" href="PracFirst.css">
<meta charset="utf-8"/>
<meta name="nora" content="width=device-width"/>
<title>考研的铁锤</title>
</head>

<body>
<h1>狗生哲学</h1>

<!-- 视觉像标题，但不是真标题，就可以用 <div>，更灵活，非h2 -->
<div class="job-title">讨好专家</div>
    <p>“讨好专家”是狗狗考研的一门核心课程，  
    以狗狗基本活动为主题而编制的课程系统，  
    跨越各狗类学科领域的一些生活上的问题。
    </p>

    <p>这门学科帮助狗狗理解他们的上帝和其创造的狗学、  
    军事学以及狗类历史之间微妙而复杂的关系和总体真理。
    </p>
    <ul>

    <h2>非紧急勿联系</h2>
    <ul>
        <li>Email:
            <a href="mailto:铁锤@gmail.com">铁锤@gmail.com</a>
        </li>
        <li>Web:
            <a href="http://啥也没有.ac.cn">http://啥也没有.ac.cn</a>
        </li>
        <li>Tel:000 1111336</li>
    </ul>
</body>
</html>
```

```css
/* <title>考研的铁锤 */
body{
    background-color: rgb(242, 201, 181);
    color: rgb(111, 97, 168);
    font-family: Arial, Helvetica, sans-serif;
    padding: 1em;
    margin: 0;
}

h1{
    color:rgb(246, 79, 163);
    font-size:  2em;
    font-family: Georgia, 'Times New Roman', Times, serif;
    border-bottom:  10px dotted rgb(157, 74, 209);
}

h2{
    color:#d86639;
    font-style: italic ;
    font-weight: bold;
    font-size: 1.5em;
}

.job-title{
    color:#4588e6;
    font-weight: bold;
}

a:link,
a:visited{
    color:#026770;
}
a:hover{
    color:#e38622;
    text-decoration:none;
}

```

---
#CSS菜鸟教程： 
## 多重样式优先级
- （内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式
- 内联样式
	`<p style="color:sienna;margin-left:20px">这是一个段落。</p>`
- ==注意：==如果外部样式放在内部样式的后面，则外部样式将覆盖内部样式 
		
```html
<head>
    <!-- 设置：h3{color:blue;} -->
    <style type="text/css">
      /* 内部样式 */
      h3{color:green;}
    </style>
    <!-- 外部样式 style.css -->
    <link rel="stylesheet" type="text/css" href="style.css"/>
</head>
<body>
    <h3>显示蓝色，是外部样式</h3>
</body>
```

| **类型**         | **举例**                             | **优先级/权重** | **顺序有无影响** |
| -------------- | ---------------------------------- | ---------- | ---------- |
| **JS** 操控的样式   | element. style.color <br>= "green" | ✅ 最大       | 无视顺序       |
| **内联** CSS     | < div style="color: red">          | 高          | 无视顺序       |
| **< style> 块** | < style>p { color: blue }< /style> | 中          | 后写的覆盖前写的   |
| < link> 外部表    | <  link href="x.css">              | 低          | 后引入的覆盖前引入的 |
- 浏览器加载 HTML 时，从上往下执行，如果多个规则“权重一样”，那么**谁在后面写谁生效**。

#### 背景
#背景
<mark class="hltr-pink">css的背景，不是html的img</mark>
- background-color
- background-image
- background-repeat
- background-attachment
- background-position
 <mark class="hltr-pink">可以分开写或者合并</mark>
 - 简写属性，作用是将背景属性设置在一个声明中。
```css
body{
    /* background-color: #fae6e1;
    background-image: url('豆铁.jpg');
    background-repeat: no-repeat;
    background-position: right top ; */

    background:#fae6e1 url('豆铁.jpg') no-repeat right top;
}
```

#### 字体
 #用em来设置字体大小
 - px/16=em
	 `font-size: 2em;`

| Property                                                                | 描述                 |
| :---------------------------------------------------------------------- | :----------------- |
| [font](https://www.runoob.com/cssref/pr-font-font.html)                 | 在一个声明中设置所有的字体属性    |
| [font-family](https://www.runoob.com/cssref/pr-font-font-family.html)   | 指定文本的字体系列          |
| [font-size](https://www.runoob.com/cssref/pr-font-font-size.html)       | 指定文本的字体大小          |
| [font-style](https://www.runoob.com/cssref/pr-font-font-style.html)     | 指定文本的字体样式          |
| [font-variant](https://www.runoob.com/cssref/pr-font-font-variant.html) | 以小型大写字体或者正常字体显示文本。 |
| [font-weight](https://www.runoob.com/cssref/pr-font-weight.html)        | 	指定字体的粗细。          |
#### 链接
 #链接 
```css
a:link,
a:visited{
    color:#026770;
}
a:hover{
    color:#e38622;
    text-decoration:none;
}
```

#### CSS 盒子模型(Box Model)
 #CSS盒子模型BoxModel 
- 所有HTML元素可以看作盒子，在CSS中，"box model"这一术语是用来设计和布局时使用。
- CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：边距，边框，填充，和实际内容。
- 盒模型允许我们在其它元素和周围元素边框之间的空间放置元素。
	- **Margin(外边距)** - 清除边框外的区域，外边距是透明的。
	- **Border(边框)** - 围绕在内边距和内容外的边框。
	- **Padding(内边距)** - 清除内容周围的区域，内边距是透明的。
	- **Content(内容)** - 盒子的内容，显示文本和图像。
	          <img src="Pasted image 20250725140836.png"  width="400" >

#### CSS 边框
 #边框
 
- dotted：定义点状边框。
- dashed：定义虚线边框。
- solid：定义实线边框。
- double：定义双线边框。
- groove：定义三维沟槽边框。效果取决于 border-color 的值。
- ridge：定义三维脊状边框。效果取决于 border-color 的值。
- inset：定义三维嵌入边框。效果取决于 border-color 的值。
- outset：定义三维突出边框。效果取决于 border-color 的值。
- none：定义无边框。
- hidden：定义隐藏边框。
```css
border-color: violet;
    border-style: ridge ;
    border-width: 0.3em;
```


#### 轮廓（outline）
 #轮廓outline
```css
   outline-color: rgb(241, 51, 17);
    outline-style: dotted;
```

- **border** 是**元素盒子的一部分**，会占据空间，会推动周围布局。
- **outline** 是**元素盒子外的一圈线**，**不占空间**，不会影响布局。
	- border 是装饰，outline 是提示。


#### 文本的对齐
#文本的对齐
```css
h1 {text-align:center;}
p.date {text-align:right;}
p.main {text-align:justify;}
```

```html
    <h1>测试image页面</h1>
    <p class="first">铁锤今天拿到了心仪的offer</p>
    <p style="text-align:center;">女子狗院</p>   
    <p class="third">努力没有白费哦。</p>
    
```
```css
p{
    outline: 5px ridge red ; 
    color: blue;
    
}
p.first{
        text-align: right;
}

p.third{
    letter-spacing: 30px;
}
```
<img src="Pasted image 20250725145357.png" width="400px" height="80px">

| 属性                                                                            | 描述           |
| :---------------------------------------------------------------------------- | :----------- |
| [color](https://www.runoob.com/cssref/pr-text-color.html)                     | 设置文本颜色       |
| [direction](https://www.runoob.com/cssref/pr-text-direction.html)             | 设置文本方向。      |
| [letter-spacing](https://www.runoob.com/cssref/pr-text-letter-spacing.html)   | 设置字符间距       |
| [line-height](https://www.runoob.com/cssref/pr-dim-line-height.html)          | 设置行高         |
| [text-align](https://www.runoob.com/cssref/pr-text-text-align.html)           | 对齐元素中的文本     |
| [text-decoration](https://www.runoob.com/cssref/pr-text-text-decoration.html) | 向文本添加修饰      |
| [text-indent](https://www.runoob.com/cssref/pr-text-text-indent.html)         | 缩进元素中文本的首行   |
| [text-shadow](https://www.runoob.com/cssref/css3-pr-text-shadow.html)         | 设置文本阴影       |
| [text-transform](https://www.runoob.com/cssref/pr-text-text-transform.html)   | 控制元素中的字母     |
| [unicode-bidi](https://www.runoob.com/cssref/pr-text-unicode-bidi.html)       | 设置或返回文本是否被重写 |
| [vertical-align](https://www.runoob.com/cssref/pr-pos-vertical-align.html)    | 设置元素的垂直对齐    |
| [white-space](https://www.runoob.com/cssref/pr-text-white-space.html)         | 设置元素中空白的处理方式 |
| [word-spacing](https://www.runoob.com/cssref/pr-text-word-spacing.html)       | 设置字间距        |

#### padding / margin(外边距)
 #margin(外边距)
 #padding 

| **名称**  | **中文** | **用途**     | **说明**            |
| ------- | ------ | ---------- | ----------------- |
| content | 内容     | 放文本、图片、表格等 | 就是你写的内容，比如一段文字、图片 |
| padding | 内边距    | 内容和边框之间的空隙 | 会撑大背景色            |
| border  | 边框     | 元素本身的边界线   | 可以加颜色、粗细样式        |
| margin  | 外边距    | 元素之间的距离    | 不会撑背景，只是留白        |

```
|<-- margin -->|         外部留白
+--------------+         border
|   padding    |         内边距，填充物
|  content区   |         放的内容，比如书、狗粮
|   padding    |
+--------------+
|<-- margin -->|
```


#### Overflow
 #Overflow
- overflow 属性可以控制内容溢出元素框时在对应的元素区间内添加<mark class="hltr-pink">滚动条</mark>。

| 值       | 描述                           |
| ------- | ---------------------------- |
| visible | 默认值。内容不会被修剪，会呈现在元素框之外。       |
| hidden  | 内容会被修剪，并且其余内容是不可见的。          |
| scroll  | 内容会被修剪，但是浏览器会显示滚动条以便查看其余的内容。 |
| auto    | 如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。 |
| inherit | 规定应该从父元素继承 overflow 属性的值     |

###### <mark class="hltr-lightsalmon-">问题</mark>
- <mark class="hltr-pink"> 如何不让 p 的 CSS 内容影响 # d 中的 < p></mark>
     - 让 # d 内的 < p> 不继承或被通用规则覆盖
```css
css:
p {
    outline: 5px ridge red ; 
    color: blue;
}
html:
<div id="d">辛苦的汗水背后是,吃了很多辣翅.
    <p>炸鸡是高盐高脂肪食物，<br>会加重狗狗肝肾负担，<br>甚至会诱发胰腺炎.</p>
    </div>

```
<mark class="hltr-pink">用更具体的选择器覆盖通用规则</mark>
```css
#d p{
    outline: none;
    color:inherit;
    background: #f0bfd9;
    color: rgb(7, 129, 129);
    padding: 15px;
    width: 100px;
    height: 100px;
    border: 3px  dashed orange;
    overflow: auto;
}
```

<img src="Pasted image 20250725160354.png" height="150px" ><img src="Pasted image 20250725160635.png" height="150">

#### 图片居中对齐
 #图片居中对齐
 - 让图片居中对齐, 可以使用 margin: auto; 并将它放到 **块** 元素中:
```css
img{
    display: block;
    margin:auto;
    width: 150px;
}
html:
<img src="豆铁.jpg" alt="doutie">
```

#### 组合选择符
 #组合选择符
- 后代选择器(以空格     分隔)
	- 选取所有 < p> 元素插入到 < div> 元素中:
- 子元素选择器(以大于 > 号分隔）更远的后代则不会匹配
- 相邻兄弟选择器（以加号 + 分隔）紧挨
- 普通兄弟选择器（以波浪号 ～ 分隔）即使它们不直接相邻


#### html和css的父类子类
- HTML 和 CSS 中的「父类 / 子类」是 结构上的包含关系
- 作用
	- ：CSS 会根据HTML 元素的父子层级来决定哪些规则生效。
```html
css:
<style>
ul li {
  color: red;
}
</style>
HTML:
<ul>
  <li>苹果</li>
  <li>香蕉</li>
</ul>
```
- < ul> 是父元素（parent）
- 每个 < li> 是它的子元素（child）
- 这种是结构上的“包裹”关系
- css:所有出现在 < ul> 里的 < li> 都变红。


#### 伪类
  <span style="font-size: 50px">:</span>
- 用冒号 ==:== 开头的 CSS 语法，用来选择元素的某种“状态”或“特殊情况”。
- 浏览器自动判断的状态，自动触发（假装的class，程序员没法预知）

```css
a:link {color:#FF0000;} /* 未访问的链接 */
a:visited {color:#00FF00;} /* 已访问的链接 */
a:hover {color:#FF00FF;} /* 鼠标划过链接 */
a:active {color:#0000FF;} /* 已选中的链接 */
```
- a:hover 必须被置于 a:link 和 a:visited 之后，才是有效的。
- a:active 必须被置于 a:hover 之后，才是有效的。


#### 伪元素
   <span style="font-size:50px">::</span> 
- 常用的 CSS 伪元素有 ==::==before、::after、::first-line、::first-letter
<mark class="hltr-pink">语法：</mark>
```css
<style>
p:first-line 
{
color:#ff0000;
font-variant:small-caps;
}


p:first-letter 
{
	color:#ff0000;
	font-size:xx-large;
}

</style>

<body>
<p>你可以使用 "first-line" 伪元素向文本的首行设置特殊样式。</p>
</body>
```

```css
h1::before {content: url('豆铁.gif');}
```
<img src="Pasted image 20250726105449.png"width="250px">

####  伪类和为元素组合 
```html
<style>
article p:first-child::first-line{
    font-size:120%;
    font-weight:bold;
}
</style>
html:
<article>
    <p>
       “国际院校”这个词可以指两种类型的学校：
       一类是“国际学校”，通常指以外国教育体系为教学标准，
       招收一定比例外籍学生的学校；另一类是“国际化大学”，
       通常指在全球范围内享有较高声誉，
       且在国际上有广泛合作和交流的大学。 
    </p>
    <p>
        2025QS世界大学排名，麻省理工学院连续十三年排名第一
        ，帝国理工和牛津位居第二、三位，而剑桥大学排位第五。
    </p>
</article>
```

<img src="Pasted image 20250727160448.png"style="width:50%">


#### 导航栏

| **排列方式** | **样式关键**                                            | **常见属性**            | **说明**         |
| -------- | --------------------------------------------------- | ------------------- | -------------- |
| 垂直排列     | 默认行为                                                | < ul>< li>、block 元素 | < li> 默认是纵向排列的 |
| 水平排列     | ✅ display: flex✅ float: left✅ display: inline-block | 控制元素在一行排列           |                |

**垂直导航栏**
<img src="Pasted image 20250726113229.png" height=100px>
- 建立一个垂直的导航栏
- 在鼠标移动到选项时，修改背景颜色(hover)
- 激活/当前导航条(active)
```css
  ul{
        list-style-type:none;
        margin: 0%;
        padding: 0%;
        background-color: rgb(248, 212, 212);
    }
    li a{
        display: block;
        width: 60px;
        color: rgb(13, 132, 114);
       text-decoration: none;
       text-align: center;
    }

    li a:hover{
        background-color: rgb(175, 230, 230);
        color: rgb(243, 183, 105);
    }
    li a:active{
        background-color: black;
        color: aliceblue;
    }
html:
 <ul>
        <li><a href="#home">home</a></li>
        <li><a href="#news">news</a></li>
        <li><a href="#contact">contact</a></li>
        <li><a href="#about">about</a></li> 
    </ul>
```

**水平**
```html
<style>
    ul{
        list-style-type: none;
        margin:0;
        padding:0;
        overflow: hidden;
        background-color: bisque;
    }
    
    li
    {
        float :left;
    }

    li a{
        display: flex;
        color: brown;
        text-align: center;
        padding: 14px 16px;
        width: 60px;
        text-decoration: none;
    }

    li a:hover{
        background-color: aqua;
    }
```

####  下拉菜单

```html
<style>
    /* 下拉按钮样式 */
    .dropbutton{
        background-color: aquamarine;
        color:rgb(156, 106, 41);
        padding: 16px;
        font-size: 16px;
        border:none;
        cursor:pointer;
    }
/* 让 .dropdown 这个元素成为定位上下文。 */
/* 子元素(dropdown-content)设置了 position: absolute; 
以这个 .dropdown 为参考点(相对定位)来定位*/
.dropdown{
    position:relative;
    display: inline-block;
}

/* 下拉内容 (默认隐藏) */ 
.dropdown-content{
    display: none;
    position: absolute;
    background-color: rgb(207, 207, 246);
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(239, 120, 120, 0.2);;
}

/* 下拉菜单的链接  */
.dropdown-content a{
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

.dropdown-content a:hover{
    background-color: brown;
}
/* 注意，hover后有空格， .dropdown-content 是 .dropdown 的 子元素*/
.dropdown:hover .dropdown-content{
    display: block;
}

.dropdown:hover .dropbtn {
    background-color: #3e8e41;
}
</style>
</head>

<body>
<div class="dropdown">
    <button class="dropbutton">点我下啦</button>
    <div class="dropdown-content">
        <a href="#">猪肉</a>
        <a href="#">牛肉</a>
        <a href="#">肌肉</a>

    </div>
</div>
</body>
</html>
```
<img src="Pasted image 20250726123502.png" height=150px>

#### 提示工具(Tooltip)
- 提示工具 Tooltip 本质上就是一个文字块（text 或 element），在用户 hover（悬停）或 focus（聚焦）时显示出来。
-  一个原本隐藏的文本 div，在特定事件发生时（例如 hover）设置为 visible 或 display: block。
- 提示工具显示在头部和底部。我们需要使用 **margin-left** 属性，并设置为 -60px。
-  ::after 及 content 属性为提示工具创建一个**小箭头标志**，箭头是由边框组成的
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
</head>
<style>
.tooltip {
    position: relative;
    display: inline-block;
    border-bottom: 1px dotted black;
}

.tooltip .tooltiptext {
    visibility: hidden;
    width: 120px;
    background-color: black;
    color: #fff;
    text-align: center;
    border-radius: 6px;
    padding: 5px 0;
    position: absolute;
    z-index: 1;
    bottom: 150%;
    left: 50%;
    margin-left: -60px;
}

.tooltip .tooltiptext::after {
    content: "";
    position: absolute;
    top: 100%;
    left: 50%;
    margin-left: -5px;
    border-width: 5px;
    border-style: solid;
    border-color: black transparent transparent transparent;
}

.tooltip:hover .tooltiptext {
    visibility: visible;
}
</style>
<body style="text-align:center;">

<h2>顶部提示框/底部箭头</h2>

<div class="tooltip">鼠标移动到我这
  <span class="tooltiptext">提示文本</span>
</div>

</body>
</html>
```

#### CSS 属性选择器
-  **属性选择器 = 用属性来定位元素**

  <span style="font-size: 40px ;border:10px solid blue ;color:darkblue">h1 {color:blue;font-size:12px}</span>
选择器      属性     冒号    值   (分号)

- **"value 是完整单词"** 类型的比较符号: ~=, |=
- **"拼接字符串**" 类型的比较符号: * =, ^ =, $ =

| **用法**            | **选择的元素**                           | **对应的 HTML 示例**          |
| ----------------- | ----------------------------------- | ------------------------ |
| [type]            | 所有有 type 属性的 < input> 元素            | < input type="text">     |
| [type="password"] | 所有密码框                               | < input type="password"> |
| [type^="p"]       | 所有 type 以 p 开头的 input（如 password）   | < input type="password"> |
| [type$="t"]       | 所有 type 结尾是 t 的 input（如 text）       | < input type="text">     |
| [type*="ass"]     | type 中包含 "ass" 的 input（例如 password） | < input type="password"> |

#### 使用 CSS 来渲染 HTML 的表单元素
- **HTML** 的 < input> 是“内容结构”，它属于 HTML 的标签，是用于构建网页表单输入的
```html
<form>
  <input type="text" placeholder="输入名字">
</form>
```
	- 这是“结构”和“内容”。
	- 负责“能输入东西”，比如文本、密码、日期、单选框、复选框等。
	- 是页面上的“功能”元素。

- **CSS** 作用于 < input>，是“外观样式”
```css
input {
  border: 2px solid red;
  background-color: lightyellow;
}
```
	这段 CSS 会让所有 input：
	•	边框变红
	•	背景变浅黄

| **HTML 的 input** | **CSS 的 input** |
| ---------------- | --------------- |
| 是“表单输入框”本身       | 是“给输入框加样式”      |
| 定义“能不能输入”、“输入类型” | 定义“长什么样”、“漂不漂亮” |
| 是功能              | 是外观             |
```html
<style>
input[type=text],select{
width: 100px;
padding: 12px 20px;
margin: 8px 0;
display: inline;
border: 2px dotted rgb(130, 237, 237);
border-radius: 10px;
box-sizing: border-box;
}

input[type=submit]{
    width: 100px;
    background-color: #bceda1;
    border:none;
    border-radius: 8px;
    padding: 14px 20px;
    margin:8px 0;
    cursor: pointer;
}

input[type=submit]:hover{
    background-color: #249517;
}

div{
    border-radius: 5px;
    background-color: #fbd1d1;
     padding: 20px;
}
</style>
</head>
<body>
<h3>使用 css 来渲染 html 的form元素</h3>

<div>
    <form>
        <form action="/" method="post">
        <label for="fname">First Name</label>
        <input type="text" id="fname"
         name="firstname" placeholder="你姓个啥？">
        
        <label for="lname">Last Name</label>
        <input type="text" id="lname" 
        name="lastname" placeholder="名字是啥？">

        <label for="country">Country</label>
        <select id="country" name="country">
            <option value="aaa">aaa</option>
            <option value="bbb">bbb</option>
            <option value="ccc">ccc</option>
        </select>

        <input type="submit" value="submit">
    </form>
</div>
</body>
```

#### 媒介@
**基础完成**
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>整体网页css渲染</title>
<style>
    *{
        box-sizing: border-box;
    }
body{
        font-family: Arial;
        padding: 10px;
        background: #c3d0d2;
}
.header{
        padding: 30px;
        text-align: center;
        background: rgb(210, 241, 231);   
}

.header h1{
    font-size: 50px;
}

.topnav {
    overflow: hidden;
    background-color: #f9d4d4;
}

.topnav a {
        float: left;
        display: block;
        color: #0d7624;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        }

.topnav a:hover {
        background-color: #eeabab;
        color: rgb(191, 75, 75);
        }

/* 创建两列 */
/* Left column */
.leftcolumn {   
  float: left;
  width: 75%;
}
 
/* 右侧栏 */
.rightcolumn {
  float: left;
  width: 25%;
  background-color: #f29494;
  padding-left: 20px;
}

/* 图像部分 */
.trueimg {
  background-color: #5b4e4e;
  width: 100%;
  padding: 20px;
}
/* 文章卡片效果 */
.card {
  background-color: rgb(221, 242, 202);
  padding: 20px;
  margin-top: 20px;
}

/* 列后面清除浮动 */
.row:after {
  content: "";
  display: table;
  clear: both;
}
 
/* 底部 */
.footer {
  padding: 20px;
  text-align: center;
  background: #f1b1df;
  margin-top: 20px;
}



/* 响应式布局 - 屏幕尺寸小于 800px 时，两列布局改为上下布局 */
@media screen and (max-width:800px) {
    .leftcolumn, .rightcolumn{
        width: 100%;
        padding: 0;
    }
}

/* 响应式布局 -屏幕尺寸小于 400px 时，导航等布局改为上下布局 */
@media screen and (max-width:400px) {
    .topnav a{
        float: none;
        width: 100%;
    }
}
</style>
</head>


<body>

<div class="header">
    <h1>铁锤大学</h1>
    <p>铁锤院长工作好辛苦</p>
</div>

<div class="topnav">
    <a href="#">11</a>
    <a href="#">22</a>
    <a href="#">33</a>
    <a href="#" style="float:right">44</a>
</div>

<div class="row">
    <div class="leftcolumn">
        <div class="card">
            <h2> 竞选标题</h2>
            <h5>2050 年 8 月 3 号</h5>
            <div class="trueimg" style="height:200px">美照</div>
            <p>竞选感言.....</p>
            <p>铁锤学院坐落于犬岛CBD，其美名响彻高等教育系统，以培养技术及应用型人才为主要目标。</p>
        </div>
        <div class="card">
            <h2> 竞选标题</h2>
            <h5>2050 年 8 月 3 号</h5>
            <div class="trueimg" style="height:200px">美照</div>
            <p>竞选感言.....</p>
            <p>铁锤学院坐落于犬岛CBD，其美名响彻高等教育系统，以培养技术及应用型人才为主要目标。</p>
        </div>
    </div>
    <div class="rightcolumn">
        <div class="card">
            <h2> 关于铁锤院长的信息</h2>
            <div class="trueimg" style="height:200px">美照</div>
            <p>看看铁锤院长每天都犯什么嫌吧</p>
        </div>
        <div class="card">
            <h3>热点绯闻</h3>
            <div class="trueimg"><p>美照</p></div>
            <div class="trueimg"><p>美照</p></div>
            <div class="trueimg"><p>美照</p></div>
        </div>
        <div class="card">
            <h3>别管我</h3>
            <p>不久前，黑山大学的一群生物学家以那位美艳性感的柴犬裔女星命名他们发现的新物种，一种生活在菠萝咬苹果海峡水域的幼犬。</p>
        </div>
</div>
</div>
<div class="footer">
    <h2>不要错过的重要底部信息</h2>
</div>
</body>
</html>

```

## CSS3
#### 2D 转换
- translate()
- rotate()
- scale()
- skew()
- matrix():使用六个值的矩阵matrix(包含旋转，缩放，移动（平移）,倾斜功能。)
- <mark class="hltr-pink">-webkit-, -ms- 或 -moz- </mark>**浏览器前缀**
	- 一样的code，需要加上浏览器的前缀<mark class="hltr-pink">再写一遍</mark>：比如  
	    transform: rotate(30deg);
	    -ms-transform: rotate(30deg);
	    -webkit-transform: rotate(30deg);

|**前缀**|**代表的浏览器**|**举例**|
|---|---|---|
|-webkit-|Chrome、Safari、Edge 新版|-webkit-transform|
|-moz-|Firefox|-moz-transition|
|-ms-|Internet Explorer（IE）|-ms-transform|
|-o-|Opera（老版本）|-o-transition

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<style>
div{
    width:200px;
    height:100px;
    background-color: pink;
    border: 1px solid lightsalmon;
}
div#div2{
    transition: transform 1s ease;
    transform: translate(0px,0px);
    /* -ms-transform: translate(50px,100px);
    -webkit-transform:translate(50px,100px); */
    /* transform: rotate(30deg);
    -ms-transform: rotate(30deg);
    -webkit-transform: rotate(30deg); */
}

div#div2:hover{
    transform: translate(50px,100px);
}
</style>
</head>

<body>
    <div>铁锤国际技校</div>
    <div id="div2">铁锤院长</div>
</body>
</html>
```

#### 3D 转换
- rotateX()
- rotateY()

#### 过渡属性
| 属性                                                                                                                                       | 描述                      | CSS |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ----------------------- | --- |
| [transition](https://www.runoob.com/cssref/css3-pr-transition.html "CSS3 transition 属性")                                                 | 简写属性，用于在一个属性中设置四个过渡属性。  | 3   |
| [transition-property](https://www.runoob.com/cssref/css3-pr-transition-property.html "CSS3 transition-property 属性")                      | 规定应用过渡的 CSS 属性的名称。      | 3   |
| [transition-duration](https://www.runoob.com/cssref/css3-pr-transition-duration.html "CSS3 transition-duration 属性")                      | 定义过渡效果花费的时间。默认是 0。      | 3   |
| [transition-timing-function](https://www.runoob.com/cssref/css3-pr-transition-timing-function.html "CSS3 transition-timing-function 属性") | 规定过渡效果的时间曲线。默认是 "ease"。 | 3   |
| [transition-delay](https://www.runoob.com/cssref/css3-pr-transition-delay.html "CSS3 transition-delay 属性")                               | 规定过渡效果何时开始。默认是 0。       | 3   |
```html
<style>
div{
    width:100px;
    height:100px;
    background-color: pink;
    border: 1px solid lightsalmon;
    transition-property:width;
    transition-duration:1s;
    transition-timing-function:linear;
    transition-delay:2s;

    -webkit-transition-property:width;
    -webkit-transition-duration:1s;
    -webkit-transition-timing-function:linear;
    -webkit-transition-delay:2s;
}

div:hover{
    width:200px;
}
</style>
<body>
    <div>铁锤国际技校</div>
    <div id="div2">铁锤院长</div>
</body>
```
<img src="Pasted image 20250727101657.png" style="height:150px;border:2px dotted blue" >
# 分页(pagination)
- 为每个页面做导航
<img src="Pasted image 20250727105738.png" style="width:300px">

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<style>
ul.pagination{
    display: inline-block;
    padding:0;
    margin:0;
}

ul.pagination li{display: inline}

/*  */
ul.pagination li a{
    color:rgb(241, 136, 136);
    float:left;
    padding:8px 16px;
    text-decoration: none;
    /* 当 background-color 发生变化时，
    效果会在 0.3 秒内平滑地过渡完成，而不是立刻生效。 */
    transition:background-color .3s;
}

ul.pagination li a.active{
    background-color: blueviolet;
    color:white;
}

/* 当鼠标悬停在分页组件（ul.pagination）中 ，
不是 .active 的链接 <a> 元素 上时，
    将它的背景颜色变为 aquamarine（浅绿色）。 */
ul.pagination li a:hover:not(.active){background-color: aquamarine;}

</style>
</head>

<body>

<h2>分页，鼠标悬停效果</h2>
<p>看看是个什么</p>
<ul class="pagination">
<li><a href="#">«</a></li>
<li><a href="#">1</a></li>
<li><a class="active" href="#">2</a></li>
<li><a href="#">3</a></li>
<li><a href="#">4</a></li>
<li><a href="#">5</a></li>
<li><a href="#">6</a></li>
<li><a href="#">7</a></li>
<li><a href="#">»</a></li>
</body>
</html>
```
解释**嵌套结构和分页代码**
- ==`ul.pagination li a.{`==
	•	找到一个 < ul> 元素，它有类名 pagination
	•	在它里面的每一个 < li> 元素
	•	再在 < li> 里面的 < a> 元素
👉 结构关系是父 > 子 > 子（严格来说，是“后代”选择器）：

```html
<ul class="pagination">        ← 外层祖先（父辈）
  <li>                          ← 中间父辈
    <a href="#">链接</a>       ← 最终目标：这个 <a>
  </li>
</ul>
```

- ul .pagination li a.active
	在 .pagination 的 < ul> 里，某个 < li> 里的 < a> 元素，同时这个 < a> 元素拥有类名 active
	✅ 作用：设置“当前页按钮”的样式。

-  ul. pagination li a:hover:not(.active)
鼠标悬停在 不是 active 的 < a> 链接上时，改变它的样式（比如背景变色）a
```css
ul.pagination        ← 最外层父元素
└── li               ← 每个子项
    └── a            ← 里面的链接（我们想加样式的对象）
         ├── a.active              ← 当前页
         └── a:hover:not(.active) ← 鼠标悬停 + 非当前页
```

#### 弹性盒子(Flex Box)
- 弹性盒子由**弹性容器**(Flex container)和**弹性子元素**(Flex item)组成。
- 当页面需要适应不同的屏幕大小以及设备类型时确保元素拥有恰当的行为的布局方式。
- Flex 弹性盒子和 @media 媒体查询不重复，功能不同，常常配合使用
- **flex**：是“弹性布局”，**专门为复杂的横向或纵向排列设计的现代方案**，它自动处理对齐、间距、换行，比 inline 强大很多。
- 弹性容器通过设置 display 属性的值为 flex 或 inline-flex将其定义为弹性容器
- 弹性容器内包含了一个或多个弹性子元素

|**功能**|flex **弹性盒子**|@media **媒体查询**|
|---|---|---|
|**作用**|自动排列子元素|根据“屏幕尺寸”改变样式|
|**触发条件**|由容器属性决定，如 display: flex|由“设备宽度”等媒体特征决定|
|**使用目的**|子元素自动换行、对齐、分布|为不同屏幕指定不同的布局规则|
|**灵活性**|更偏向**布局结构本身**的适应|更偏向**整体外观**的调整|

---
###  MDN
#### 盒模型
- 是关于「一个盒子内部尺寸组成」的规则，描述盒子的尺寸结构（content + padding + border + margin），是“内部构造”。
`|<--margin-->[border[padding[  content  ]padding]border]<--margin-->|`

#### display外部显示（Outer Display Type）vs 内部显示（Inner Display Type）
- 这是控制这些“盒子”之间 **怎么排列**，以及**盒子里面的内容怎么排列** 的机制
###### 1、外部显示类型（Outer Display Type）
- 决定这个盒子在页面中是 block 还是 inline。这个盒子在页面上的位置行为。
	•	block：这个盒子是一个区块，独占一行。
	•	inline：这个盒子是一个行内元素，多个可并排。
	•	none：这个盒子不显示（不会参与布局）。
######  1、内部显示类型（Inner Display Type）
- 决定这个盒子里面的子元素如何布局（是 Flex、Grid、Table 还是正常 Flow）。盒子里面的内容如何排列

#### 区块盒子与行内盒子
###### ➤ 区块盒子（block-level box）
- 像“砖头”一样占据整行。
###### ➤ 行内盒子（inline-level box）
- 像“字”一样在一行中排列。

| **特性**                  | **🧱 区块盒子** block                 | **✒️ 行内盒子** inline                |
| ----------------------- | --------------------------------- | --------------------------------- |
| **是否换行**                | ✅ 每个元素独占一行（自动换行）                  | ❌ 不换行（多个 inline 元素排成一行）           |
| **默认宽度**                | 撑满父容器的整行（100%）                    | 内容多宽就多宽                           |
| **能否设置宽 / 高**           | ✅ 可以 width / height               | ❌ 无效，width 和 height 设置了也不生效       |
| **常见元素**                | < div>, < p>, < h1>, < section> 等 | < span>, < a>, < strong>, < em> 等 |
| **是否可以嵌套 block 元素**     | ✅ 可以放其他 block 或 inline            | ❌ 不能嵌套 block 元素                   |
| **padding / margin 支持** | ✅ 上下左右都能生效                        | ⚠️ 左右有效，上下可能不生效（浏览器不同）            |

---
#### <mark class="hltr-lightsalmon-">牛客做题：</mark>

<mark class="hltr-lightsalmon-">题目</mark>
将html模块中ul列表的第2个li标签和第4个li标签的背景颜色设置成"rgb(255, 0, 0)"。
  : nth-child(n)匹配属于其父元素的第n个子元素
```html
<head>
    <meta charset="UTF-8">
    <style>
       /* 填写样式 */
       li:nth-child(2),
       li:nth-child(4){
        background-color:rgb(255,0,0);
       }
    </style>
</head>

<body>
  <ul>
	<li>1</li>
	<li>2</li>
	<li>3</li>
	<li>4</li>
</ul> 
    <script type="text/javascript">
        /* 填写JavaScript */
        
    </script>
</body>
```

<mark class="hltr-lightsalmon-">题目</mark>
请给html模块的div元素加一个后伪元素，且后伪元素的宽度和高度都是20px，背景颜色为"rgb(255, 0, 0)"。
-  ::after 后伪元素真正显示出来，还需要两点：
- ✅ 必须补上的两个关键点：
		1.	设置 content：伪元素必须有 content 才能出现，即使是空字符串 ""
		2.	设置 display：默认是 inline，而你希望的是有宽高，所以要设成 block 或 inline-block
```css
<style>
       /* 填写样式 */
       div::after{
        content:"";
        display:inline-block;
        height:20px;
        width:20px;
        background-color:rgb(255,0,0);
       }
    </style>
```


#### 根元素（Root Element和父元素（Parent Element）
-  **定义**：HTML 中的根元素是 < html> 标签。
	- 所有 CSS 的 rem 单位，都是相对于 < html> 的 font-size 来计算的。
-  父元素就是你当前元素的直接上一级包裹元素。
	- 所有 CSS 的 em 单位，是相对于“父元素的字体大小” 来计算的（如果自己设置了字体大小，就相对于自己）。
<mark class="hltr-orange">举例子：</mark>
- **`em` 单位在用于 `font-size` 时表示“父元素的字体大小**,而在用于其他属性时则表示“自身的字体大小”）。
	- 每一层嵌套都会<mark class="hltr-pink">逐渐变大</mark>，因为每个元素的字体大小都被设置为 `1.3em` —— 即其父元素字体大小的 1.3 倍。
- **rem 单位的意思是“根元素的字体大小”**
	- 字体大小取决于根元素（`<html>`）。这意味着每层嵌套<mark class="hltr-pink">不会让字体越变越大</mark>。

- **`lh`** 是相对于元素自身的行高。
- 和 **`rlh`** 的区别在于，而后者是相对于根元素（通常是 `<html>`）的行高。

- **百分比**的问题在于，它们总是**相对于其他值**设置的。例如，如果将元素的字体大小设置为百分比，那么它将是元素父元素字体大小的百分比。如果使用百分比作为宽度值，那么它将是父值宽度的百分比。

- **（`opacity`）**，它控制元素的不透明度（它有多透明）。此属性接受 **`0`（完全透明）** 和 **`1`（完全不透明）之间的数字。**



#### <mark class="hltr-lightsalmon-">题目</mark>
```
挑战：基本的 CSS 理解
上一页
概述：CSS 构建
下一页
你已经在这个模块中了解到了很多内容，所以当你达到这个模块的最后一篇文章的时候，感觉一定非常不错吧！在你继续之前的最后一步，就是完成对于这个模块的测验。本次测验涉及到几个相关的练习，你必须按顺序完成，这样你才能设计出最终的成品：一张名片/游戏玩家卡片/社交媒体的简介。

起点
在开始测验之前，你应该：

将 HTML file for the exercise, 和 associated image file,拷贝到你的本地环境中。如果你想使用自己的图片文件以及把你的名字写进资料里面的话，也没有问题，不过需要保证你提供的图像是正方形的。
下载 CSS resources text file 到你的本地环境，这个文件包含了一组原始选择器和规则集。你需要学习并将他们组合，这是测验的一部分。
备注： 另外，你可以使用一个网站比如 JSBin 或 Glitch 来做你的测验。你可以复制 HTML 和 CSS 到其中一个在线编辑器中，以及使用这个 this URL 来让 <img> 显示图片。如果你使用的在线编辑器无法让你链接 CSS 文件 (没有单独的 CSS 面板)，你也可以将 CSS 直接放入<style> 元素中。

项目概要
我们已经为你提供了一些原始的 HTML 和一张图片，然后需要编写必要的 CSS 来让其成为一个漂亮的网上小名片，可能大小是游戏玩家卡片或社交媒体简介的两倍。下面的段落描述了你需要做的事情。

基本设置：

首先，在你放 HTML 文件和图像文件的目录下，创建一个新的文件，把它命名为类似style.css。
通过 <link> 元素来将你的 CSS 链接到 HTML 文件中。
我们为你提供的 CSS 资源文本文件中，前两项规则集是我们设置好的，你可以直接使用，所以将他们复制粘贴到你的新 CSS 文件的顶部。同时也可以将这个作为测验，用来确认你是否正确链接了你的 CSS 文件到 HTML 中。
在以上的两条规则中添加一条 CSS 注释，注释中要包含一些文本来表明这是整体页面的一般样式。你可以在 CSS 文件底部添加 3 个或以上的注释，来明确地表明该样式是应用到卡片的容器，应用到标题和页脚的样式，和名片主要内容的样式。从现在开始，随后在样式表添加的样式都应该有组织地放置在合适的地方。
关注我们为你提供的选择器和规则集：

接下来，我们希望你观察四个选择器，并计算每一个的专用性。将它们写在稍后可以找到的地方，例如在 CSS 顶部的注释中。

现在是时候把正确的选择器放在正确的规则集上了！你的 CSS 资源中有四对选择器和规则集需要匹配，现在就开始匹配，并将它们添加到你的 CSS 文件。你需要：

为整体卡片的容器提供一个固定的宽/高，背景颜色，边框，以及边框圆角等等。
为 header 提供一个渐变的背景颜色，从更暗到更亮，加上圆角，配合在卡片容器上设置的圆角。
为 footer 提供一个渐变的背景颜色，从更亮到更暗，加上圆角，配合在卡片容器上设置的圆角。
将图像向右浮动，使其粘贴在名片主要内容的右边，然后把它的 max-height 设置为 100% (一个聪明的技巧，来确保它将放大/缩小，与父容器保持同样的高度，不管它变成什么高度。)
注意！提供的规则集中有两个错误。使用你知道的任何技术找到这些错误并修复，然后再继续。

你需要写的新规则：

编写一个同时面向 card head 和 card footer 的规则集，使它们计算的总高度为 50px（包括 30px 的内容高度和 10px 的 padding）但用 em 来表示。
浏览器会为<h2> 和 <p>元素应用默认的 margin，这会影响我们的设计，所以编写一个规则集：margin 设置为 0。
为了阻止图像溢出名片的主要内容 ( <article> 元素)，我们需要给它设置一个明确的高度。设置 <article>的高度为 120px，但是使用 em来表示。还要给它一个半透明黑色的背景颜色，产生一个稍暗一点的阴影，能让红色的背景稍微透过。
编写一个规则集，使 <h2> 有效的字体大小为 20px (使用 em表达) 以及一个适当的行高将其放置在标题的内容框的中央。回想起来，内容框高度应该是 30px，你所有需要的数字都已经给你了，所以可以计算出行高。
为页脚中的 <p> 编写一个规则集，使它的有效字体大小为 15px (使用 em表达) 以及一个适当的行高将其放置在页面的内容框的中央。回想起来，内容框高度应该是 30px，你所有需要的数字都已经给你了，所以可以计算出行高。
最为最后一步，为 <article> 中的段落设置一个合适的 padding 值，让它和 <h2> 以及页脚的段落左边缘对齐，并将其颜色设置得便于阅读。
备注： 记住第二条规则集会将 font-size: 10px; 设置在 <html> 元素上 — 这意味着 <html> 的任何后代中，一个 em 将会等于 10px 而不是默认的 16px。(这是当然的，如果在层次结构中，有不同的 font-size 设置于其上，问题中的后代没有任何的祖先位于 em 元素和 <html> 之间。这可能会影响你所需要的值，尽管在这个简单的示例中，这不是问题。)

其他事情要考虑：

如果你编写的 CSS 有比较好的可读性，并在每行上单独声明，你将得到奖励。
你应该在所有规则的选择器中都用 .card 作为开头，这样的好处是：如果将名片放在带有其他内容的页面的情况下，这些规则不会干扰其他元素的样式。
注意和提示
你不需要以任何方式编辑 HTML，除了将 CSS 应用于你的 HTML。
当使用 em 值代表一些你需要的像素长度的时候，想想 (<html>) 元素的基本字体大小，以及需要乘以什么才能获得所需的值。这将给你 em 的值，至少在这样一个简单的情况下。
```

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Fundamental CSS comprehension</title>
    <link rel="stylesheet" href="style.css"/>
  </head>
  <body>

  <section class="card">
    <header>
      <h2>LiangTieChui</h2>
    </header>
    <article>
      <img src="tie.jpg" alt="铁锤这个笨蛋，偷偷去阳台翻垃圾，还自作聪明的意味我发现不了。">
      <p>柴女 古舍 基地中心<br>
         大聪明街道<br>
         小笨蛋社区<br>
         柴山<br>
         CA 3020A<br>
        <strong>Tel</strong>: 01234 567 890<br>
        <strong>Mail</strong>: tiechui@nothere.com</p>
    </article>
    <footer>
      <p>铁锤国际院校：提供高等教育，包你生气</p>
    </footer>
  </section>

  </body>
</html>

```

```css
body {
  margin: 0;
}

html {
  font-family: 'Helvetica neue', Arial, 'sans serif';
  font-size: 10px;
  background-color: #fdcbcb;
}
/* 整体样式 */

.card{
  width: 35em;
  height: 22em;
  margin: 5em auto;
  background-color: rgb(242, 185, 185);
  border: 0.2em solid black;
  border-radius: 1.5em;

}

.card img{
    float:right;
    max-height:100%;
    margin-left: 1em;
}



.card p{
    margin:0;
}

.card h2{
    font-size:2em;
    color:rgb(64, 95, 3);
    line-height: 0.1em;
    text-align: left;
}


.card article{
height: 10em;
background-color:rgba(237, 95, 95, 0.2);
padding-left:0.2em;
color:rgb(255, 255, 255);
align-items: flex-start;

}

.card article p {
    padding-left: 1em;
    color:rgb(246, 246, 209)
}


.card footer p {
    font-size: 1.5em;
    line-height: 3em;
}



.card header,
.card footer{
    padding: 1em;
    height:5em;
    border-radius: 1.5em 1.5em 0 0;
}

.card header{
    background-image: linear-gradient(
     90deg,
    rgba(226, 251, 0, 0.39),
    rgb(105, 230, 255)
    );
}

.card footer{
    font-size:0.7em;
    background-image: linear-gradient(
     to right,
    rgba(69, 255, 76, 0.39),
    rgb(105, 230, 255)
    );
    border-radius: 0 0 1.5em 1.5em ;
    color:rgb(60, 87, 5);
    text-align: left;
}

```
<img src="Pasted image 20250729150024.png" style="width: 20em; border-radius:1.5em 1.5em 1.5em 1.5em">


### <mark class="hltr-lightsalmon-">题目</mark>
```
挑战：排版社区大学首页
上一页
概述：为文本添加样式（样式化文本）
下一页
在本测评中，通过对社区学校主页的文本样式化，我们会测试你对所有本模块涉及到的文本样式化技术的理解。你或许也会从中获得乐趣。

开始
在本测评开始前，你应该：

获取本次练习的 HTML 和 CSS 文件以及提供的 external link icon。
在本地计算机中拷贝一份上述文件。
备注： 或者，你可以使用像 JSBin 或 Glitch 的网站完成你的测评。你可以把 HTML 和 CSS 粘贴到在线编辑器中，并使用this URL指定背景图像。如果你使用的在线编辑器没有单独的 CSS 面板，你可以将其放在 HTML 文件的<style>元素中。

项目简介
你有一个虚构的社区大学主页的未处理 HTML 文件和一些 CSS 文件。这些 CSS 文件把网页分成两栏布局，提供了一些简单的样式化。你将在 CSS 文件底部的 comment 下写你的 CSS，这样可以方便地标出你的工作。不要担心选择器一直重复；我们会帮你跳过这个问题。

字体：

首先，下载一些免费的字体。因为这是一所大学，字体应该严肃，正式，给人信任的感觉——主体使用 serif 字体，对标题结合使用 sans-serif 或者 slab serif 会是不错的选择。
使用合适的服务对着两种字体生成无死角的@font-face代码。
将你的 body 字体应用到 body，heading 字体应用到 heading。
文本样式化基础：

设置全站网页 font-size 为 10px。
使用相对单位（relative unit）为标题和其他元素的 font-sizes 设置合适的值。
为 body 文本设置合适的line-height。
居中页面顶级标题。
为标题设置 letter-spacing 避免字间太过拥挤。
为 body 文本设置合适的 letter-spacing 和 word-spacing。
在<section>元素中，每个标题后的第一段文字设置 20px 的文本缩进。
链接：

设置 link, visited, focus, 和 hover 状态设置颜色，与页面顶部和底部的水平线颜色相匹配。
设置链接默认带下划线，但 hover 和 focus 时下划线消失。
取消页面中所有链接 focus 时默认的外边线。
设置 active 时有显著不同的样式，使其又突出又与整体页面设计和谐。
在外部链接右侧插入外部链接图标。
列表：

确保列表和列表项与页面整体样式和谐。每个列表项应该有同样的与段落行相同的line-height 。每个列表上下间距应该与段落间距相同。
使用与页面设计匹配的 bullet 列表项符号。你可以选择自定义的 bullet 图像或者其他的喜欢的 bullet 符号。
导航栏菜单：

样式化你的导航栏菜单，使它拥有与页面整体相匹配的外观。
提示与技巧
本练习中你不需要编辑 HTML 文件。
你不需要使导航栏菜单看起来像按钮，但它需要有一定的高度才不至于在页面侧边看起来很别扭；同时记得，你需要的是一个垂直导航栏菜单。
实例
下图展示了其中一种设计完成后的例子。
```

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>St Huxley's Community College</title>
    <link href="style.css" type="text/css" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
  </head>
  <body>

  <header>
    <h1>St Huxley's Community College</h1>
  </header>

  <section>
      <h2>Brave new world</h2>

      <p>It's a brave new world out there. Our children are being put in increasing more competitive situations, both during recreation, and as they start to move into the adult world of <a href="https://en.wikipedia.org/wiki/Examination">examinations</a>, <a href="https://en.wikipedia.org/wiki/Jobs">jobs</a>, <a href="https://en.wikipedia.org/wiki/Career">careers</a>, and other life choices. Having the wrong mindset, becoming <a href="https://en.wikipedia.org/wiki/Emotion">too emotional</a>, or making the wrong choices can contribute to them experiencing difficulty in taking their rightful place in today's ideal society.</p>

      <p>As concerned parents, guardians or carers, you will no doubt want to give your children the best possible start in life — and you've come to the right place.</p>

      <h2>The best start in life</h2>

      <p>At St. Huxley's, we pride ourselves in not only giving our students a top quality education, but also giving them the societal and emotional intelligence they need to win big in the coming utopia. We not only excel at subjects such as genetics, data mining, and chemistry, but we also include compulsory lessons in:</p>

      <ul>
        <li>Emotional control</li>
        <li>Judgement</li>
        <li>Assertion</li>
        <li>Focus and resolve</li>
      </ul>

      <p>If you are interested, then you next steps will likely be to:</p>
      
      <ol>
        <li><a href="#">Call us</a> for more information</li>
        <li><a href="#">Ask for a brochure</a>, which includes signup form</li>
        <li><a href="#">Book a visit</a>!</li>
      </ol>
  </section>

  <aside>

    <h2>Top course choices</h2>

    <ul>
      <li><a href="#">Genetic engineering</a></li>
      <li><a href="#">Genetic mutation</a></li>
      <li><a href="#">Organic Chemistry</a></li>
      <li><a href="#">Pharmaceuticals</a></li>
      <li><a href="#">Biochemistry with behaviour</a></li>
      <li><a href="#">Pure biochemistry</a></li>
      <li><a href="#">Data mining</a></li>
      <li><a href="#">Computer security</a></li>
      <li><a href="#">Bioinformatics</a></li>
      <li><a href="#">Cybernetics</a></li>
    </ul>

    <p><a href="#">See more</a></p>

  </aside>

  <nav>

    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Finding us</a></li>
      <li><a href="#">Courses</a></li>
      <li><a href="#">Staff</a></li>
      <li><a href="#">Media</a></li>
      <li><a href="#">Prospectus</a></li>
    </ul>

  </nav>

  <footer>

    <p>&copy; 2016 St Huxley's Community College</p>

  </footer>

  </body>
</html>
```

```css
/* General setup */
/* General setup */

* {
  box-sizing: border-box;
}

body {
  margin: 0 auto;
  min-width: 1000px;
  max-width: 1400px;
  font-family: "Kaisei Opti", serif;
  font-weight: 400;
  font-style: normal;
  font-size:10px;
}

/* Layout */

section {
  float: left;
  width: 50%;
  
}

aside {
  float: left;
  width: 30%;
}

nav {
  float: left;
  width: 20%;
}

footer {
  clear: both;
}

header, section, aside, nav, footer {
  padding: 20px;
}

/* header and footer */

header, footer {
  border-top: 5px solid #a66;
  border-bottom: 5px solid #a66;
}


/* WRITE YOUR CODE BELOW HERE */body header{
    font-size:1.1em;
  font-family: "Kaisei Opti",  sans-serif;
  font-weight: 400;
  font-style: normal;
}
 body footer{
     font-size:1.1em;
 }
 
 section h2{
     font-size: 2em;
 }

 header{
    text-align: center;
    color: rgb(63, 168, 242);
    letter-spacing:0.05em ;
    word-spacing:0%;
 }

 section p{
    text-indent: 20px;
    line-height: 1em;
 }

a:link{
    color: #a66;
    text-decoration: underline;
}
a:visited{
    color: #a66;
}
a:focus{
    color: #a66;
    text-decoration: none;
    outline:none;
}
a:hover{
    color: #a66;
    text-decoration: none;
}
a:active{
    color: blueviolet;
}
/* 在所有 <a> 链接后面添加一个
固定大小的小图标（比如外链图标） */
section a::after{
    content: " ";
    display: inline-block;
    width:10px;
    height:10px;
    margin-left: 4px;
    background-image: url('external-link-52.png');
    background-size: contain;
    background-repeat: no-repeat;
}
section > p:nth-of-type(1) a::after{
    content: " ";
    display: inline-block;
    width:10px;
    height:10px;
    margin-left: 4px;
    background-image: url('external-link-52.png');
    background-size: contain;
    background-repeat: no-repeat;
}

section ul li{
    line-height: 1em;
    list-style-type:square;
}
aside ul li{
    line-height: 1em;
    list-style-type:square;
}
/* 补充nav的单独none样式 */
nav a::after{
    content: none;
}

nav a:link,
nav a:visited{
    text-decoration: none;
    display: block;
    text-align: center;
    padding: 10px;
    border:1px solid  rgb(164, 93, 93);
    font-weight: bold;
}
nav a:hover,
nav a:focus{
    background-color:  rgb(243, 208, 208);
    color:white;
    outline:none;
}
nav a:active{
    background-color: rgb(180, 76, 76);
    color:antiquewhite
}

nav ul li{
    list-style-type:none;
}
```
<img src="Pasted image 20250729182532.png" style="width:90em">

#### 布局
 出现在另一个元素下面的元素被描述为**块**元素，**内联元素**就像段落中的单个单词一样。
		- **块元素**内容的布局方向：**块方向**，垂直运行。
		- **内联方向**是内联内容：（如句子）的运行方向。
			- `display:block`，列表项显示为一个在另一个之下。
			- 如果将显示值更改为`inline`，它们现在将显示在彼此旁边

- 页面上的多数元素，**正常布局流**将完全可以创建你所需要的布局，可以按照**默认**的方式来搭建页面
- 下列布局技术会**覆盖默认**的布局行为：
	- **[`display`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/display)** 属性 — 标准的 value，比如`block`, `inline` 或者 `inline-block` 元素在正常布局流中的表现形式 (见 [Types of CSS boxes](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/Box_model#types_of_css_boxes)). 接着是全新的布局方式，通过设置`display`的值，比如 [CSS Grid](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/CSS_layout/Grids) 和 [Flexbox](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/CSS_layout/Flexbox).
	- **浮动**——应用 **[`float`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/float)** 值，诸如 `left` 能够让块级元素互相并排成一行，而不是一个堆叠在另一个上面。
	- **[`position`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/position)** 属性 — 允许你精准设置盒子中的盒子的位置，正常布局流中，默认为 `static` ，使用其他值会引起元素不同的布局方式，例如将元素固定到浏览器视口的左上角。
	- **表格布局**— 表格的布局方式可以用在非表格内容上，可以使用`display: table`和相关属性在非表元素上使用。
	- **多列布局**— 这个 [Multi-column layout](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_multicol_layout) 属性可以让块按列布局，比如报纸的内容就是一列一列排布的。
#### `display: flex` 和 `display: grid`

<mark class="hltr-lightsalmon-">题目</mark>
- 不是很好
```
目标
你需要实现你自己的布局。下面是你应该完成的目标：

在一行中显示导航选项，并且选项之间拥有相同的空间。
导航条应随着内容一起滚动并且在触碰到视口顶部之后于顶部固定。
文章内的图片应该被文本包围。
<article> 与 <aside> 元素应该为双列布局。它们的列尺寸应该是弹性的，以便在浏览器窗口收缩得更小的时候能够变窄。
照片应显示为两列网格，图像之间有 1 像素的间隙。
提示和小技巧
在实现布局的过程中你不需要修改 HTML，下面是你应该使用的技术：

弹性盒
栅格
浮动
定位

```

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Layout Task</title>
    <link href="styles.css" rel="stylesheet" type="text/css">
  </head>

<body>

  <div class="logo">
    My exciting website!
  </div>

  <nav>
    <ul>
      <li>
        <a href="">Home</a>
      </li>
      <li>
        <a href="">Blog</a>
      </li>
      <li>
        <a href="">About us</a>
      </li>
      <li>
        <a href="">Our history</a>
      </li>
      <li>
        <a href="">Contacts</a>
      </li>
    </ul>
  </nav>

  <main class="grid">
    <article>
      <h1>
        An Exciting Blog Post
      </h1>
      <img src="balloon-sq6.jpg" alt="placeholder" class="feature">
      <p>Veggies es bonus vobis, proinde vos postulo essum magis kohlrabi welsh onion daikon amaranth tatsoi tomatillo melon
        azuki bean garlic.</p>

      <p>Gumbo beet greens corn soko endive gumbo gourd. Parsley shallot courgette tatsoi pea sprouts fava bean collard greens
        dandelion okra wakame tomato. Dandelion cucumber earthnut pea peanut soko zucchini.</p>

      <p>Turnip greens yarrow ricebean rutabaga endive cauliflower sea lettuce kohlrabi amaranth water spinach avocado daikon
        napa cabbage asparagus winter purslane kale. Celery potato scallion desert raisin horseradish spinach carrot soko.
        Lotus root water spinach fennel kombu maize bamboo shoot green bean swiss chard seakale pumpkin onion chickpea gram
        corn pea. Brussels sprout coriander water chestnut gourd swiss chard wakame kohlrabi beetroot carrot watercress.
        Corn amaranth salsify bunya nuts nori azuki bean chickweed potato bell pepper artichoke.</p>

      <p>Nori grape silver beet broccoli kombu beet greens fava bean potato quandong celery. Bunya nuts black-eyed pea prairie
        turnip leek lentil turnip greens parsnip. Sea lettuce lettuce water chestnut eggplant winter purslane fennel azuki
        bean earthnut pea sierra leone bologi leek soko chicory celtuce parsley jícama salsify.</p>

      <p>Celery quandong swiss chard chicory earthnut pea potato. Salsify taro catsear garlic gram celery bitterleaf wattle
        seed collard greens nori. Grape wattle seed kombu beetroot horseradish carrot squash brussels sprout chard.</p>

    </article>

    <aside>
      <h2>
        Photography
      </h2>
      <ul class="photos">
        <li>
          <img src="balloon-sq1.jpg" alt="placeholder">
        </li>
        <li>
          <img src="balloon-sq2.jpg" alt="placeholder">
        </li>
        <li>
          <img src="balloon-sq3.jpg" alt="placeholder">
        </li>
        <li>
          <img src="balloon-sq4.jpg" alt="placeholder">
        </li>
        <li>
          <img src="balloon-sq5.jpg" alt="placeholder">
        </li>
      </ul>

    </aside>
  </main>

</body>

</html>
```

```css
body {
    background-color: #fff;
    color: #ea6161;
    margin: 0;
    font: 1.2em / 1.2 Arial, Helvetica, sans-serif;
  }

  img {
      max-width: 100%;
      display: block;
  }
  
  .logo {
    font-size: 200%;
    padding: 50px 20px;
    margin: 0 auto;
    max-width: 980px;
  }
  
  .grid {
    margin: 0 auto;
    padding: 0 20px;
    max-width: 980px;
  }
  
  nav {
    background-color: #f5c2c2;
    padding: .5em;
    position:sticky;
    top:0;
    z-index: 1;
    max-width: 980px;
    padding-left: 20px;
    padding-right: 20px;
    margin: 0 auto;
  }
  
  
  nav ul {
    margin: 0;
    padding: 0;
    list-style: none;
    display: flex;
    justify-content: space-between;
    
  }
  
  nav a {
    display: block;
    color: #7a2121;
    text-decoration: none;
    padding: .5em 1em;
  
  }
  
  .photos {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .feature {
      width: 200px;
  }


  /* ----------- */
  .grid{
    display: flex;
    gap:20px;
  }
  article, aside{
    flex:1;
  }


  
  .photos{
    display: flex;
    justify-content: space-between;

  }

  .feature{
    float:left;
    margin:0 1em 1em 0;
  }
nav li{
  flex:1;
  text-align: center;
  border:#ea6161 solid .2em;
  font-size: 1.3em;;
}


```

<img src="Pasted image 20250730133359.png" style="height: 20em">
