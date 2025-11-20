


DDL :7.20[[CSS]]
#MDN
## [网站应该使用什么结构？](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Getting_started/Environment_setup/Dealing_with_files#%E7%BD%91%E7%AB%99%E5%BA%94%E8%AF%A5%E4%BD%BF%E7%94%A8%E4%BB%80%E4%B9%88%E7%BB%93%E6%9E%84%EF%BC%9F)

接下来，让我们看看测试网站应该使用什么结构。在我们创建的任何网站项目中，最常见的是一个主页 HTML 文件和包含图像、样式文件和脚本文件的文件夹。现在让我们创建这些：


>[!example]
1. **`index.html`**：这个文件一般包含==主页内容==，也就是用户第一次访问网站时看到的文字和图片。使用文本编辑器，创建一个名为 `index.html` 的新文件，并将其保存在 `test-site` 文件夹内。
2. **`images` 文件夹**：这个文件夹包含网站上使用的所有图片。在 `test-site` 文件夹内创建一个名为 `images` 的文件夹。
3. **`styles` 文件夹**：这个文件夹包含为内容提供样式的 ==CSS== 代码（例如，设置文本和背景的颜色）。在 `test-site` 文件夹内创建一个名为 `styles` 的文件夹。
4. **`scripts` 文件夹**：这个文件夹包含所有用于向网站添加交互功能的 ==JavaScript== 代码（例如，点击时加载数据的按钮）。在 `test-site` 文件夹内创建一个名为 `scripts` 的文件夹


```html
<!-- 文档类型 -->
<!DOCTYPE html>
<!-- <>:元素 -->
<html lang="en-US">
  <head>
    <!-- 我的文档使用UTF-8的字符编码 -->
    <meta charset="utf-8" />
    <!-- 视口元素 -->
    <meta name="viewport" content="width=device-width" />
    <!-- 页面标题,收藏可看 -->
    <title>My test page</title>

  </head>
  <body>
    <p>
      
      My dog is <strong>very </strong>stupit.
    
    </p>

    <!--src:路径, alt:图像描述,听障人士  -->
    <img src="images/hammer.jpg" alt="我的小狗" />

  </body>
</html>
```



---

# CSS 规则集（rule set）是用来规定“哪些 HTML 元素要应用什么样的样式”的一段代码。
```css
p{
color:red;
font-size ;16px;
}
```

>[!tip]

>- p 是**选择器**，表示所有 < p > 段落
>- { color: red; font-size: 16px; } 是**声明块**
>- color: red; 和 font-size: 16px; 都是**声明**，用来规定颜色和字体大小;



>[!   warning  ]
## 一个规则集的结构

- **选择器 Selector**：告诉浏览器“我要选中哪些标签”
    
- **大括号 {}**：包住所有的样式声明
    
- **声明 Declaration**：一对“属性:值”（如 color: red;）
    
- **每条声明后面要有分号 ;**
```css
p{

color: rgb(54, 149, 217);

width: 500px;

border: 1px solid black;

}

h2,li {

color: rgb(61, 221, 162);

}
```

---
# CSS字体:
**文档头部`<head>`和 `</head>` 之间的任意位置）添加 `<link>`元素。代码如下：**
**从google copy**

```css
<link href="https://fonts.googleapis.com/css2?family=Winky+Rough:ital,wght@0,300..900;1,300..900&display=swap" rel="stylesheet">
---------------------------
font-family: "Winky Rough", sans-serif;
```

### CSS 布局主要是基于_盒子模型_。每个在页面上占用空间的盒子都有类似的属性：
- `padding`（内边距）：是指内容周围的空间。在下面的例子中，它是段落文本周围的空间。
- `border`（边框）：是紧接着内边距的实线。
- `margin`（外边距）：是围绕元素边框外侧的空间。
```css
h1,
h2 {
  font-size: 60px;
  text-align: center;
  color: rgb(54, 149, 217);
}
p,
li {
  font-size: 16px;
  line-height: 2;
  letter-spacing: 1px;
  color: rgb(61, 221, 162);
}
body {
  width: 600px;
  margin: 0 auto;
  background-color: rgb(223, 116, 134);
  padding: 0 20px 20px 20px;
  border: 5px solid rgb(19, 84, 170);
}
```
- `width: 600px;` 强制文档体永远保持 600 像素宽。
- `margin: 0 auto;` 当你在 `margin` 或 `padding` 这样的属性上设置两个值时，第一个值影响元素的_上下_方向（在这个例子中设置为 `0`）；第二个值影响_左右_方向。（这里，`auto` 是一个特殊的值，它将可用的水平空间平均分配给左边和右边）。
- `background-color: #FF9500;` 如前文所述，指定元素的背景颜色。
- `padding: 0 20px 20px 20px;` 我们给内边距设置了四个值，目的是给内容四周留出一点空间。

#### ==主标题设置==

## 图片
```css
img{
  display: block;
  margin: 0 auto;
  width: 500px;
 
}

```
- `<img>` 元素 [`width`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/width) 属性的值设置为小于 600 像素的值。  否则溢出
- 图像居中让页面更美观一些。可以复用 body 的 `margin: 0 auto`
- - margin 表示“外边距”。
    
- 这个写法里，margin: 0 auto; 表示：
    
    - 上下外边距是 0
        
    - 左右外边距是 auto（自动）

----

## 整体
```html
<!-- 文档类型 -->
<!DOCTYPE html>
<!-- <>:元素 -->
<html lang="en-US">


  <head>
    <!-link了google的在线字体 -->
‼️英文
    <link
      href="https://fonts.googleapis.com/css2?family=Winky+Rough:ital,wght@0,300..900;1,300..900&display=swap"
      rel="stylesheet"
    />
‼️中文
    <link
      href="https://fonts.googleapis.com/css2?family=Ma+Shan+Zheng&family=Noto+Sans+SC&family=Winky+Rough:ital,wght@0,300..900;1,300..900&display=swap"
      rel="stylesheet"
    />
和自己的CSSlink
    <link href="styles/hammer.css" rel="stylesheet" />
    <!-- 我的文档使用UTF-8的字符编码 -->
    <meta charset="utf-8" />
    <!-- 视口元素 -->
    <meta name="viewport" content="width=device-width" />
    <!-- 页面标题,收藏可看 -->
    <title>My test page</title>
    <!-- link CSS文件 -->
  </head>

内容
  <body>
    <h1>My dog is <strong>very</strong> STUPID.</h1>
    <h2>But cute</h2>

    <!--src:路径, alt:图像描述,听障人士  -->
    <img src="images/hammer.jpg" alt="我的小狗" />
    <p>这是我的样子,是不是笨笨的?</p>
无序
    <ul>
      <li>睡觉</li>

      <li>吃饭</li>

      <li>玩游戏</li>
    </ul>
    <p>
      而且我还爱捣蛋,我有自己的
      <a
        href="https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Getting_started/Your_first_website/Creating_the_content"
        >微信</a
      >,但是我从来没有用过.
    </p>
  </body>
</html>

```

## 字体的设置要注意
```css
/* <!-- link了google的在线字体 --> */
html {
  font-family: "Winky Rough","Ma Shan Zheng", cursive,
 serif;
}

h2 {
  font-size: 60px;
  text-align: center;
  color: rgb(54, 149, 217);
}
p,
li {
  font-size: 16px;
  line-height: 2;
  letter-spacing: 1px;
  color: rgb(61, 221, 162);
}
body {
  width: 600px;
  margin: 0 auto;
  background-color: rgb(223, 116, 134);
  padding: 0 20px 20px 20px;
  border: 5px solid rgb(19, 84, 170);
}

h1 {
  margin: 0;
  padding: 20px 0;
  font-size: 70px;
  text-align: center;
  color: rgba(46, 203, 230, 0.816);
  text-shadow: 3px 3px 2px blueviolet;
}

img{
  display: block;
  margin: 0 auto;
  width: 500px;
 
}

```

- margin 表示“外边距”。
- 这个写法里，margin: 0 auto; 表示：
    
    - 上下外边距是 0
        
    - 左右外边距是 auto（自动）

---

#菜鸟

```html
	<!DOCTYPE html>
	<html>
	<head>
	<meta> charset="utf-8">
	<title>XXXX </title>
	</head>
	
	(web可视化内容⬇️body区域)
	<body>:元素包含了可见的页面内容
	
	<h1> 第一个标题</h1>
	
	<p>第一个段落</p>
	
	<p>这是另一个段落</p>
	</body>

</html>
```


# 头
#html的头部,不会出现在浏览器内容,保留的页面的元数据,简短
```
<head>

<meta charset="utf-8" />

<title>铁锤是笨蛋</title>

</head>
```

# 换行br/斜体em/分隔符hr/粗体b
```html

<p>
    <h1>铁锤不太聪明</h1>

    <p>她现在躺在我的卧室里 睡大觉 !</p>
    <img src="14.jpg" width="302" height="403" />
    <!-- hr是分隔符 --> 
    <hr />

    <h2>铁锤贪吃</h2>
    
     <p>
      <b>铁锤</b>看到吃的<br />
      啥都想尝尝<br />
      最爱吃冰淇淋<br />
	  第二是<em>鸭子</em> 这是我的<a   href="nawang121.github.io">portal</a><br />
      我在学习&lt;字符串&gt;
    </p>
```

---
## 链接
 #链接
 ```html
 <a href="URL">链接文本</a>
 1、<a> 标签：定义了一个超链接（anchor）。
 2、href 属性：指定目标 URL，当点击链接时，浏览器将导航到此 URL。
 
```
`<a>` 是“跳转”链接，控制的是“用户行为”,一个页面一次只能有一个主视图
`<iframe>` 是“嵌套”页面，控制的是“网页行为”,可以多个 iframe 并排

---

# <mark class="hltr-purple">table</mark>

<mark class="hltr-blue">表格小语法</mark>
```html
HTML 表格由 <table> 标签来定义。

HTML 表格是一种用于展示结构化数据的标记语言元素。

每个表格均有若干行（由 <tr> 标签定义），每行被分割为若干单元格（由 <td> 标签定义），表格可以包含标题行（<th>）用于定义列的标题。

- th：th 是 table header的缩写，表示表格的表头单元格。
- tr：tr 是 table row 的缩写，表示表格的一行。
- td：td 是 table data 的缩写，表示表格的数据单元格。

```

```html
<h4>一列:</h4>
    <table border ="1">
    <tr>
        <td>100</td>
    </tr>
    </table>
      
    <h4>一行三列:</h4>
    <table border ="1">
    <tr>
        <td>100</td>
        <td>200</td>
        <td>300</td>       
    </tr>
    </table>

    <h4>二行三列</h4>
    <table border ="3">
    <tr>
        <td>100</td>
        <td>200</td>
        <td>300</td>
    </tr>
    <tr>
        <td>400</td>
        <td>500</td>
        <td>600</td>
    </tr>
    </table>
```

<mark class="hltr-orange">带th(thead) 和 tbody的表格,一共是两部分</mark>
==表格表头==
```html
 
    <h4>一行三列:</h4>
    <table border ="1">
     <thead>
        <tr>
            <th>笨蛋</th>
            <th>小狗</th>
            <th>铁锤</th>
        </tr>
    </thead>
    <tbody>
        <tr> 
        <td>100</td>
        <td>200</td>
        <td>300</td>       
    </tr>
    </tbody>
    </table>
```

 < thead> 表头
 < tbody> 表体
  < tfoot> 表尾

----
#列表
<mark class="hltr-pink">有序ol和无序ul</mark>

```html
<!-- 无序列表,小黑点 -->

<ul>
	<li>铁锤</li>
	<li>笨蛋</li>
	<li>小狗</li>
</ul>

<!-- ?有序列表始于 <ol> 标签 -->

<ol>
	<li>豆豆眼</li>
	<li>豆豆眉</li>
	<li>贪吃嘴</li>
</ol>

<!-- 加一个start -->

<ol start="10">
	<li>豆豆眼</li>
	<li>豆豆眉</li>
	<li>贪吃嘴</li>
</ol>
```

 ==< li> 是 列表项（list item）:它可以装文字，也可以**再嵌套一个 < ul>**，形成**多级菜单/树状结构**。< li> 既可以是“叶子”，也可以是“分支”==
 
==< ul> 是 无序列表（unordered list）,它是一个“列表的容器”，不能单独使用，必须配合 < li>（列表项）使用。==

```html
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
--------------------------------------
	•	<ul> 装的是一个列表
	•	<li> 既可以是“叶子”，也可以是“分支”
	•	如果一个 <li> 里有 文字 + 嵌套 <ul>，就表示这个选项下还有细项,是一个 三层嵌套的多级菜单：
	
	•	一级：吃烧烤、吃蔬果、吃雪糕
	•	二级：吃蔬果 ➝ 土豆 / 西瓜；吃雪糕 ➝ 奶油和糖 / 牛奶和糖
	•	三级：奶油和糖 ➝ 变成🍫 / 变成🍰
					吃烧烤
					吃蔬果
					└── 土豆
					└── 西瓜
					
					吃雪糕
					└── 奶油和糖
					    ├── 变成🍫
					    └── 变成🍰
					└── 牛奶和糖
```




#自定义列表
<mark class="hltr-pink">自定义列表</mark>
<mark class="hltr-pink">dl是definition lists的英文缩写 (列表开始)</mark>
<mark class="hltr-pink">dt是definition term的缩写 (列表项目)</mark>
<mark class="hltr-pink">dd是definition description的缩写(项目解释)</mark>

```html
 <dl>
      <dt>铁锤狗头
      <dd>-狗👀</dd>
      <dd>-狗👃</dd>
      <dd>-狗👂</dd>
      <dd>-狗👄</dd>
 </dt>
```

---
#容器类标签
 ==< div> 块级容器==
==< span>行内容器==
<mark class="hltr-pink">大的blocks的布局“div”</mark>
```html
    <hr />
    <div id="container" style = "width:500px">
    <div id ="header" style= "background-color:rgba(246, 198, 234, 0.643)">
    <h1 style="margin-bottom: 0;">铁锤的标题</h1>
    
    <div id="menu" style="background-color:
    rgb(160, 244, 250);height:200px ; width: 100px ;float: left;">
    <b>点菜</b><br>
    面包<br/>
    雪糕<br>
    大炸鸡</div>

    <div id="content" style="background-color:
    rgb(244, 229, 199) ; height: 200px;  width:400px ; float: left;">
    不知道今晚吃啥</div>

    <div id="footer" style="background-color: rgb(13, 249, 233); clear:both; 
    text-align: center;">
    铁锤无版权</div>
    </div>
    <hr/>
```

---
<mark class="hltr-pink">表单和输入:表单用于收集用户的输入信息。</mark>
# form,label,input,select
 #form,
 #label
 #input,
 #select
  #action

```html
<form action ="/" method = "post">
    <!-- 文本输入框 -->
     <label for="name">用户名:</label>
     <input type="text" id="name" name="name" required>
     
     <br>
     <!-- 密码输入框 -->
     <label for="password">输密码:</label>
     <input type="password" id="password" name="password" required><br/>
     
     <!-- 两个输入框 -->
     First Name:<input type="text" name="firstname"><br/>
     Last Name:<input type="text" name="lastname"><br/> 
     Username:<input type="text" name="username"><br/>
     password:<input type="password" name="password"><br/>



      <br>
      <!-- 单选按钮 -->
    <label> 性别:</label><br/>
    <input type="radio" id="male" name="gender" value="male" checked>
    <label for="male">男</label><br/>
    <input type="radio" id="female" name="gender" value="female">
    <label for ="female">女</label><br/>

    <br/>
    <!-- 复选框 -->
    <input type="checkbox" id="奶茶" name="奶茶" checked>
    <label for ="奶茶">奖励一杯奶茶</label><br/>
    <br/>
    <!--  [] 字段的值是一个“数组”，可以提交多个值给服务器。-->
    <input type="checkbox" name="零食[]" value="薯片"> 铁锤喜欢原味薯片<br/>
    <input type="checkbox" name="零食[]" value="西瓜"> 铁锤喜欢散步回家,来块西瓜<br/> 


    <br/>
    <!-- 下拉列表 -->
    <label for="country">选择国家:</label>
    <select id="country" name="country">
        <option value="china">中国</option>
        <option value="usa">美国</option>
        <option value="japan">日本</option>
    </select>

    <br/>
    <!-- 提交按钮 -->
    <input type="Submit" value="Submit">

</form>
```

```html
<form action="/" method="post">
method:提交方式：post 或 get
-----------------------------
<label for="name"> 用户名：</label>
<input type="text" id="name" name="name" required>

:::<label>` 是表单标签描述，应与其对应的 input 通过 `for` 属性形成绑定.
:::for="name"`：表示该标签对应的是 id="name" 的输入框
:::id="name"`：(给前端用的)允许 JS 或 CSS 给该元素唯一标识，也为 label 属性服务
:::name="name"`：(给后端用的)表示输入数据被提交时所使用的字段名，是提交给服务器的 key
:::required`：表示此输入框为必填，否则提交会报错
------------------------------------
checked:默认选中该项
-----------------------------
name="snack[]"：表示同一名称多值，服务器接收时会把数据同时作为数组处理

```
- **< form action="...">，指定当用户 提交表单时，数据要发送到哪一个服务器地址（或处理脚本）去处理。**
`<form action="/action_page.php">`
- 把用户填好的数据，提交给服务器的 /action_page.php 页面去处理。


---

<mark class="hltr-pink">整个表格的大标题</mark> #caption <mark class="hltr-pink">和td 有所不同,td是表头</mark>

```
<body>
    <table >
        <!-- 整个表格的大标题 -->
        <caption>nowcoder</caption>
            <tr>
              <td>1</td>
              <td>1</td>
              <td>1</td>
            </tr>
            <tr>
                <td>1</td>
                <td>1</td>
                <td>1</td>
            </tr>
        </body>
    </table>
</body>

```

---
### iframe语法:
```
<iframe src="URL"></iframe>
该URL指向不同的网页。

height 和 width 属性用来定义iframe标签的高度与宽度。

frameborder 属性用于定义iframe表示是否显示边框。
设置属性值为 "0" 移除iframe的边框:
```

```html
<!-- iframe -->
 <iframe src = "https://www.runoob.com/html/html-iframes.html" 
  name = "runboo"
  width = "100" height="50" frameborder = "10"></iframe>
<iframe src="https://labuladong.online/algo/intro/data-structure-basic/" 
name ="DMO" 
width = "100" height = "50"></iframe>
<p><a href ="https://developer.mozilla.org/" 
  target="DMO" rel="noop">铁锤.COM</a></p>

```
`<a>` 是“跳转”链接，控制的是“用户行为”,一个页面一次只能有一个主视图
`<iframe>` 是“嵌套”页面，控制的是“网页行为”,可以多个 iframe 并排

---

#### 直接插入js 
#### &nbsp; character entities,实体符号
```html
<!-- 直接插入js -->
 <!DOCTYPE html>
 <html>
  <head>
  <meta charset="utf-8">
  </head>
  <body>
  <script>
    // &nbsp;character entities,实体符号
    document.write('<span style="color:rgb(123,2,3)">铁&nbsp;锤天天找零食</span>')
  </script>
  </body>
 </html>
```

---
#### Uniform Resource Locators
#URL
<mark class="hltr-pink">URL可以由字母组成( 网站域名)，如"runoob.com"，或互联网协议（IP）地址： 192.68.20.50。</mark>

#### URL Scheme，也叫 **协议名称**（Protocol Scheme）:https://
<mark class="hltr-pink">URL 想象成一个地址，而 scheme 就是访问方式
</mark>


---
# HTML 速查列表

 #HTML基本文档
```html
<!DOCTYPE html>
<html>
<head>
<title>文档标题</title>
</head>
<body>
可见文本...
</body>
</html>
```

 #基本标签（Basic/Tags）
```html
<h1>最大的标题</h1>
<h2> . . . </h2>
<h3> . . . </h3>
<h4> . . . </h4>
<h5> . . . </h5>
<h6>最小的标题</h6>
 
<p>这是一个段落。</p>
<br> （换行）
<hr> （水平线）
<!-- 这是注释 -->
```

 #文本格式化（Formatting）
```html
<b>粗体文本</b>
<code>计算机代码</code>
<em>强调文本</em>
<i>斜体文本</i>
<kbd>键盘输入</kbd> 
<pre>预格式化文本</pre>
<small>更小的文本</small>
<strong>重要的文本</strong>
 
<abbr> （缩写）
<address> （联系信息）
<bdo> （文字方向）
<blockquote> （从另一个源引用的部分）
<cite> （工作的名称）
<del> （删除的文本）
<ins> （插入的文本）
<sub> （下标文本）
<sup> （上标文本）
```

 #链接（Links）
```html
普通的链接：<a href="http://www.example.com/">链接文本</a>
图像链接： <a href="http://www.example.com/"><img src="URL" alt="替换文本"></a>
邮件链接： <a href="mailto:webmaster@example.com">发送e-mail</a>
书签：
<a id="tips">提示部分</a>
<a href="#tips">跳到提示部分</a>
```

 #图片（Images）
```html
<img src="URL" alt="替换文本" height="42" width="42">
//带有title的
<img scr=" "  title = "" alt="" >
```

 #样式/区块（Styles/Sections）
```html
<style type="text/css">
h1 {color:red;}
p {color:blue;}
</style>
<div>文档中的块级元素</div>
<span>文档中的内联元素</span>
```

 #列表
```html
无序列表
<ul>
    <li>项目</li>
    <li>项目</li>
</ul>
有序列表
<ol>
    <li>第一项</li>
    <li>第二项</li>
</ol>
```

 #定义列表
```html
<dl>
  <dt>项目 1</dt>
    <dd>描述项目 1</dd>
  <dt>项目 2</dt>
    <dd>描述项目 2</dd>
</dl>
```
 
 #表格（Tables）
```html
<table border="1">
  <tr>
    <th>表格标题</th>
    <th>表格标题</th>
  </tr>
  <tr>
    <td>表格数据</td>
    <td>表格数据</td>
  </tr>
</table>
```

 #框架（Iframe）
```html
<iframe src="demo_iframe.htm"></iframe>
```

 #表单（Forms）
```html
<form action="demo_form.php" method="post/get">
<input type="text" name="email" size="40" maxlength="50">
<input type="password">
<input type="checkbox" checked="checked">
<input type="radio" checked="checked">
<input type="submit" value="Send">
<input type="reset">
<input type="hidden">
<select>
<option>苹果</option>
<option selected="selected">香蕉</option>
<option>樱桃</option>
</select>
<textarea name="comment" rows="60" cols="20"></textarea>
 
</form>
```

#实体（Entities）
```html
&lt; 等同于 <
&gt; 等同于 >
&#169; 等同于 ©
```

-----
# html5
 #html5
 ```html
整体使用了 HTML5 的语义化标签
       <header> 表示站点标题
	•	<nav> 表示导航栏（含 <ul> 和搜索栏）
	•	<main> 是核心内容区域
	•	<article> 是一段独立内容（你写的主人遛狗故事）
	•	<aside> 是右侧推荐内容或补充内容
	•	<footer> 是站点统一页脚
-----------
<!DOCTYPE html>
<html> 
<head>
<meta charset="utf-8">
<title>铁锤搏击俱乐部</title>
</head>

<body>
    <header>
        <!-- <该web页面统一的标题> -->
         <h1>铁锤知音</h1>
    </header>

    <nav>
        <!-- 该web统一的导航栏 -->
         <ul>
            <li><a href="#">狗头主页</a></li>
            <li><a href="#">拉猪交流论坛</a></li>
            <li><a href="#">炸厨房教学</a></li>
            <li><a href="#">主人培养中心</a></li>
            <li><a href="#">养人分享心得</a></li>
            <!-- 共有n个导航栏“项目” -->
            </ul>
        
        <form action="#" method="get">
            <!-- 搜索栏是站点内导航的一个非线性的方式 -->
            <input type="search" name="q" placeholder="找一个毛茸茸的狗头"/>
            <input type="submit" value="找找看"/>
        </form>    
    </nav>

    <main>
        <!-- 网页主体的内容 -->
         <article>
            <!-- 此处包含一个article -->
             今天主人掉毛了，医生说是因为没遛够。<br>
             我立刻拉他出门狂奔三圈。<br>
             他还想反抗？汪！<br>
             不听话的主人都要送去再教育营！<br>
         </article>

         <img src="14.jpg" title="铁锤美照" width="302" height="403" />

         <aside>
            <!-- 侧边栏在主内容的右侧 -->
             <h2>狗头为什么总是毛茸茸</h2>
             <ul>
                <li><a href ="#">拉布拉多为什么叫拉布拉猪?--BBZ非严谨报导</a></li>
                <li><a href ="#">小狗为什么爱睡觉?--BBX非严谨报导</a></li>
                <li><a href ="#">柴犬总是咬人的背后故事!--BBT非严谨报导</a></li>
                <li><a href ="#">小狗乐园预约真相5🐱--BBU非严谨报导</a></li>
                <!--  -->
             </ul>
         </aside>
    </main>

    <footer>
        <!-- 本站有所网页的统一footer -->
        <p>© 2025 本站无任何使用版权</p>
    </footer>
</body>
</html> 
```
---
# Canvas
#Canvas
`<canvas id="myCanvas" width="200" height="100"></canvas>`

```js
// 找到 <canvas> 元素
// 创建context对象
// 设置fillStyle属性可以是CSS颜色，渐变，或图案。
// fillStyle 默认设置是#000000（黑色）。
//fillRect(x,y,width,height) 方法定义了矩形当前的填充方式。
//ctx.moveTo(0, 0,把画笔“移动到”起点 (0, 0)，不画任何东西
//ctx.lineTo(100, 50),从当前位置“规划一条线”到 (100, 50)，仍不画
//stroke(),真正执行画线动作，把上面的线段描边出来,根据你之前定义的“路径”，用当前的笔触样式描边绘制出来
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
ctx.fillStyle="#ffc99fff";
ctx.fillRect(0,0,150,75);
ctx.moveTo(0,0);
ctx.lineTo(100,50);
ctx.stroke();

```

# 画圆 
#arc(x,y,r,start,stop)
 ```js
   ctx.beginPath();
        ctx.arc(45,20,10,0,2*Math.PI);
        ctx.stroke();
```

# #文字
- strokeText(text, x, y) —— 描边文字(空心)
- fillText(text, x, y) —— 填充文字
```js
ctx.font="30px Arial";
ctx.strokeText("Hello World",10,50);
```


#   #拖放（ #Drag 和  #Drop）

```html
<script>
            // drop and drag
        function allowDrop(ev)
        {
            ev.preventDefault();
        }

    
        //dataTransfersetData方法设置被拖数据的数据类型和值
        
        function drag(ev)
        {
            ev.dataTransfer.setData("Text",ev.target.id);
        }

        function drop(ev)
        {
            ev.preventDefault();
            var data=ev.dataTransfer.getData("Text");
            ev.target.appendChild(document.getElementById(data));
        }
</script>

<body>
        <!-- drag and drop -->
        <p>狗头可以拖动:</p>
        放到何处 - ondragover
        进行放置 - ondrop
	        <div id ="div1" ondrop="drop(event)"
	        ondragover="allowDrop(event)"></div>
        <br>



        使元素可拖动,把 draggable 属性设置为 true ：
	    拖动什么 - ondragstart 和 setData()
	    ondragstart 属性调用了一个函数，drag(event)，它规定了被拖动的数据。
	    
        <img id="drag1" src="14.jpg" draggable="true"
        ondragstart="drag(event)"title="铁锤美照" width="120"
        height="160">
</body>
```

# Geolocation（地理 #定位）

```html
<body>

        <!-- <location> -->
        <p id="demo">你爱点不点:</p>
        <button onclick="getLocation()">leave me alone</button>
        <script>
        // location
        // 找页面上 id="demo" 的那个元素，把它存在变量 x 里，
        // 以便后面用 x.innerHTML = "..." 往这个元素里写文字。
        // 在js搞处对象,需要在HTML添加元素.
        var x=document.getElementById("demo");
        function getLocation()
        {
            if (navigator.geolocation)
            {
                navigator.geolocation.getCurrentPosition(showPosition);
            }
            else{
            x.innerHTML="你的浏览器该升级了.";
            }
        }

        function showPosition(position)
        {
            x.innerHTML="纬度: "+position.coords.latitude+"<br>经度: "+position.coords.longitude;
        }

```

# Video(视频)
 #Video视频 

<mark class="hltr-pink">DOM</mark> 全称：Document Object Model
DOM 是浏览器把 HTML 网页“变成 JavaScript 能操作的对象”的一种方式。
DOM 就是 JavaScript 和 HTML 之间的“桥梁”
浏览器收到代码后，会把它“翻译成”一个结构化的树状模型（DOM Tree）：
```html
<p>你好</p>

DOM:....

Document
└── html
    └── body
        └── p
            └── 文本节点：“你好”

         JavaScript 就可以通过 DOM 来：
	•	找到这个 <p> 标签；
	•	读它的内容；
	•	改它的内容；
	•	增加或删除节点……


```


# Video(视频)/Audio(音频)
 #Video视频/Audio音频
 
- JavaScript 里的函数就像 Java 里void 方法()
- div style="text-align: center" 
   类似Java Swing 中的按钮绑定了事件监听器

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>铁锤发火续集</title>
</head>
<body>

<div style="text-align: center">
    <!-- 类似Java Swing 中的按钮绑定了事件监听器 -->
    <button onclick="playPause()">播放/暂停</button>
    <button onclick="makeBig()">放大</button>
    <button onclick="makeSmall()">缩小</button>
    <button onclick="makeNormal()">普通</button>
    <br>
    <video id="video1" width="100" height="250">
        <!-- type 属性用来告诉浏览器：这个视频文件的格式/编码类型是什么。 -->
        <source src="VideoTT.mp4" type="video/mp4">
    </video>
</div>

<script>
//JavaScript 里的函数就像 Java 里void 方法()
var Hammer=document.getElementById("video1");

function playPause()
{
    if(Hammer.paused){
        Hammer.play();
    }else{
        Hammer.pause();
    }
}

function makeBig(){
    Hammer.width=300;
    Hammer.height=500;
}

function makeSmall(){
    Hammer.width=70;
    Hammer.height=180;
}

function makeNormal(){
    Hammer.width=100;
    Hammer.height=250;
}
</script>
</body>
</html>

----------------------
视频的媒体数据加载期间发生错误时执行的方法
??
```

<mark class="hltr-pink">控件功能的音频媒体标签</mark>
```html
<body>
    <audio controls>
        
    </audio>
</body>
```

# Web SQL 数据库
 #WebSQL数据库
 
 ## <mark class="hltr-pink"> 核心方法</mark>
以下是规范中定义的三个核心方法：

1. **openDatabase**：这个方法使用现有的数据库或者新建的数据库创建一个数据库对象。
2. **transaction**：这个方法让我们能够控制一个事务，以及基于这种情况执行提交或者回滚。
3. **executeSql**：这个方法用于执行实际的 SQL 查询。

```js
// 打开数据库
//            (数据库名称,版本号,描述文本, 数据库大小,创建回调)
var db =openDatabase('mybd','10','Test DB',2*1024*1024);
```

---
# 基本语法
#MDN

1、 #html:元素组成
2、 #属性:元素也可以有属性。属性包含关于元素的额外信息，这些信息不会出现在内容中。(空格, 属性名, ”属性值“)
<mark class="hltr-pink">始终包含属性引号,不要混合使用单引号和双引号</mark>

- < head> 元素。这个元素充当一个容器，用于存放你想包含在 HTML 页面中但<mark class="hltr-pink">不</mark>向页面浏览者<mark class="hltr-pink">显示</mark>的内容。这包括会出现在搜索结果中的关键字和页面描述、用于样式化内容的 CSS、字符集声明等等。
- < title > 元素。它设置了页面的标题，这个标题会出现在加载该页面的浏览器标签页中。当页面被收藏为书签时，页面标题也用于描述该页面。
- < body> 元素。它包含了在页面上显示的所有内容，包括文本、图像、视频、游戏、可播放的音轨或其他任何东西。
- HTML 解析器在渲染代码时都会将每个空白序列减少为<mark class="hltr-pink">单个空格</mark>。使用多个空白呢增加可读性。

---
# 头元素-元信息

- < title> 元素是一项元数据，用于表示整个 HTML 文档的标题

- < meta> 元素包含了 name 和 content 属性：
		name 指定了 meta 元素的类型；说明该元素包含了什么类型的信息。
		content 指定了实际的元数据内容。
		name="description"(搜索引擎优化)
- 可以在元数据中添加对自定义图标,在浏览器的“收藏夹”及“书签”列表中显示

-  ==CSS== (< link>)并使用 ==JavaScript== (< script>)
	- < link> 元素经常位于文档的头部，它有 2 个属性，rel="stylesheet" 表明这是文档的样式表，而 href 包含了样式表文件的路径
            ==`<link rel="stylesheet" href="my-css-file.css" />`==
	- < script> 元素也应当放在文档的头部，并包含 src 属性来指向需要加载的 JavaScript 文件路径，同时最好加上 defer 以告诉浏览器在解析完成 HTML 后再加载 JavaScript。
	        ==`<script src="my-js-file.js" defer></script>

- 为站点设定语言，这个可以通过添加==lang== 属性到 HTML  
				   ==`<html lang="zh-CN"> </html>` ==

---
# 文档的基本组成部分


<mark class="hltr-pink">HTML 的语义（HTML semantics）是指：
使用标签本身的“含义”来描述内容的结构和用途，而不仅仅是为了视觉效果。
</mark>

```html
<header>：页眉。
<nav>：导航栏。
<main>：主内容。主内容中还可以有各种子内容区段，可用<article>、<section> 和 <div> 等元素表示。
<aside>：侧边栏，经常嵌套在 <main> 中。
<footer>：页脚。
```
- < aside> 包含一些间接信息（术语条目、作者简介、相关链接，等等 
 ==< div> 和 < span> ==
 - < span>内联的（inline）无语义元素
 - < div> 是一个块级无语义元素
 - ---
# 超链接

**Uniform Resource Locator，URL**

 - #URL 可以指向 HTML 文件、文本文件、图像、文本文档、视频和音频文件以及可以在网络上保存的任何其他内容,**使用路径查找文件**。
 <mark class="hltr-pink">href 和 src,rel 的区别</mark>
  -  href 是 跳转或引用外部链
	 - href Hypertext Reference（超文本引用）--< a>、< link>-表示链接到另一个资源的位置，浏览器会跳转或引用它
  - 而 src 是 加载和嵌入资源
	 - Source（来源）-<img>、< script>、< iframe>、< audio>、< video>-表示嵌入资源的地址，浏览器会下载并使用它-加载图片、脚本、音频等资源
 - rel 是relationship（关系）-当前文档与所链接资源之间的关系类型。

**需要将以下四页的本地副本放在同一目录**
- index.html
- projects.html
- pictures.html
- social.html

**给图片增加 `title` 属性来提供更多的信息,(alt="") 可以是空**
```html
<img
  src="images/dinosaur.jpg"
  alt="The head and torso of a dinosaur skeleton;
          it has a large head with long sharp teeth"
  width="400"
  height="341"
  title="A T-Rex on display in the Manchester University Museum" />

```


**为图片提供一个语义容器-< figure> 和 < figcaption > 元素**
```html
<figure>
  <img
    src="images/dinosaur.jpg"
    alt="The head and torso of a dinosaur skeleton;
            it has a large head with long sharp teeth"
    width="400"
    height="341" />

  <figcaption>
    A T-Rex on display in the Manchester University Museum.
  </figcaption>
</figure>

```

- < figure> 是什么？语义： 表示一段独立的“媒体内容”或“配图区域”。一般用于：图片、图表、代码示例、音视频等的“容器”。它本身不会显示任何视觉样式，但有语义意义  

- < figcaption> 表示 figure 内部的 说明文字，就是“这张图说了啥”或“图注”。必须写在 < figure> 元素内部。通常作为 < figure> 的第一个或最后一个子元素。

   <mark class="hltr-pink">显示视频文本</mark>
**使用 WebVTT 文件格式和 < track> 元素**
---  
# 媒体嵌入
#火狐测试 

<mark class="hltr-pink">为主 article 添加一个视频</mark>
（贴靠开放标签下侧），嵌入一个 Bilibili 视频,使用 Bilibili 生成嵌入代码。视频的宽度应该是 400px。
```html
<iframe src="//player.bilibili.com/player.html?isOutside=true&aid=3303261&bvid=BV1rs411d7hC&cid=5221343&p=2" 
        width="300"
        scrolling="no" 
        border="0" 
        frameborder="no" 
        framespacing="0" 
        allowfullscreen="true">
        </iframe>
``` 
  
  
  <mark class="hltr-pink">为 further info 的链接添加响应式图片</mark>  
  
   **srcset**:  #srcset,告诉浏览器有哪些不同尺寸的图片可以选.
-  一个宽度描述符（一个正整数，后面紧跟 w 符号）
  **sizes**：   #sizes,告诉浏览器你预计图片在不同屏幕上显示的大小（用 CSS 像素描述）
- 浏览器的视口的宽度小于等于 500px 时使用的 120px 宽的图片，其他情况下选择 400px 宽的版本

```html
<a href="https://www.mozilla.org/en-US/firefox/new/">
<img src="imageB/120firefox_logo-only_RGB.png" alt="firefox logo" 
      srcset="imageB/120firefox_logo-only_RGB.png 120w,imageB/400firefox_logo-only_RGB.png 400w" 
      sizes="(max-width: 500px) 120px">
</a>
```


<mark class="hltr-pink">picture 元素</mark>
- 包含零或多个 <source> 元素和一个 <img> 元素来为不同的显示/设备场景提供图像版本
```html
<picture>
          <source 
            srcset="600red-panda.png 600w,1200red-panda.png 1200w"
            sizes="(max-width:600px) 600px">
          <img src="600red-panda.png" alt="猫">
         </picture>
```


<span style="font-size: 25px; color :purple;">整体的codes</span>
```html
<body>
    <header>
      <h1>铁锤时报</h1>
      <!-- insert <img> element, link to the small
          version of the Firefox logo -->
      <img src="imageB/120firefox_logo-only_RGB.png" alt="firefox logo">

    </header>

    <main>
      <article>

        <!-- insert iframe from Bilibili -->
        <iframe src="//player.bilibili.com/player.html?isOutside=true&aid=3303261&bvid=BV1rs411d7hC&cid=5221343&p=2" 
        width="300"
        scrolling="no" 
        border="0" 
        frameborder="no" 
        framespacing="0" 
        allowfullscreen="true">
        </iframe>

        <h2>Rocking the free web</h2>

        <p>Mozilla are a global community of technologists, thinkers, and builders, working together to keep the Internet alive and accessible, so people worldwide can be informed contributors and creators of the Web. We believe this act of human collaboration across an open platform is essential to individual growth and our collective future.</p>

        <p>Click on the images below to find more information about the cool stuff Mozilla does. <a href="https://www.flickr.com/photos/mathiasappel/21675551065/">Red panda picture</a> by Mathias Appel.</p>
      </article>

      <div class="further-info">
        <!-- insert images with srcsets and sizes -->
        <a href="https://www.mozilla.org/en-US/firefox/new/">
          <img src="imageB/120firefox_logo-only_RGB.png" alt="firefox logo" 
          srcset="imageB/120firefox_logo-only_RGB.png 120w,imageB/400firefox_logo-only_RGB.png 400w" 
          sizes="(max-width: 500px) 120px">
        </a>
        <a href="https://www.mozilla.org/">
          <img src="imageB/400mozilla-dinosaur-head.png'" alt="恐龙" 
          srcset="imageB/120mozilla-dinosaur-head.png 120w,imageB/400mozilla-dinosaur-head.png 400w" 
          sizes="(max-width: 500px) 120px">
        </a>
        <a href="https://addons.mozilla.org/">
          <img src="imageB/120firefox-addons.jpg" alt="脆片"
          srcset="imageB/120firefox-addons.jpg 120w,imageB/400firefox-addons.jpg 400w"
          sizes="(max-width: 500px) 120px">
        </a>
        <a href="https://developer.mozilla.org/en-US/">
          <img src="imageA/mdn.svg" alt="一只马" 
        >
        </a>
        <div class="clearfix"></div>
      </div>

      <div class="red-panda">
        <!-- insert picture element -->
         <picture>
          <source 
            srcset="600red-panda.png 600w,1200red-panda.png 1200w"
            sizes="(max-width:600px) 600px">
          <img src="600red-panda.png" alt="猫">
         </picture>
      </div>

    </main>
  </body>
</html>

```

----
#### 用rel href src
#用rel/href/src

| **属性名** | **中文意思**                  | **通常用于哪个标签**                     | **作用**               |
| ------- | ------------------------- | -------------------------------- | -------------------- |
| rel     | relationship<br>（关系）      | < link>                          | 描述**当前页面与链接资源的关系**   |
| href    | hyper reference <br>（超链接） | < link>、< a>、<br>< base>         | 提供**目标地址**，即“链接到哪”   |
| src     | source<br>（来源）            | < img>、< script>、<br>< iframe> 等 | 提供**资源地址**，即“加载什么内容” |



# html和http的关系
-  **HTML 是内容，HTTP 是传输协议。**


| **概念** | **HTML（HyperText Markup Language）** | **HTTP（HyperText Transfer Protocol）** |
| ------ | ----------------------------------- | ------------------------------------- |
| 是什么    | 一种超文本标记语言，用来**编写网页内容和结构**           | 一种**应用层协议**，用于**客户端和服务器之间传输网页数据**     |
| 用来做    | 组织文本、链接、图像、视频等内容                    | 浏览器向服务器请求网页、图片、CSS、JS 等内容             |

