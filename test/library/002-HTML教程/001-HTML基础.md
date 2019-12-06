## html（hyper text markup language）超文本标记语言
html 是一种规范，一种标准，它通过**标记符号**来标记要显示的网页中的各个部分。可以告诉浏览器如何显示其中的内容，他是一种由浏览器解释执行的语言。（如：文字如何处理，画面如何安排，图片如何显示等）

• 可以使用.html与.htm做为html文件的扩展名。<br>
• HTML由于比较简单，是一种描述性的语言，没有逻辑性。<br>
• 可以使用任意文本编辑器创建HTML所以使用起来非常容易。<br>

## HTML常用标签
HTML由标签组成，标记符中的标记元素用尖括号括起来，带斜杠的元素表示该标记说明结束;大多数标记符必须成对使用，以表示作用的起始和结束。 结束标记一定要以"/"结束，引号必须使用""，标签之间不能交叉嵌套。


[点击可查看标签详细介绍](http://wangqifan.coding.me/html_css_doc/?file=001-html、css初识/01-html简介标签)

提前说明，HTML标签分为三类，有不同布局特性：

标签类型 | 布局特性
---|---
**行标签`inline`**| 不能设置大小，默认水平排列。常见文字标签
**行内块标签`inline-block`** | 可以设置大小，默认水平排列。常见图片、表单标签
**块标签`block`** | 可以设置大小，默认垂直排列。

### 基本标签 （最常用）

标签名 | 功能 | 标签类型 | 特点 | 写法
---|---|---|---|---
div | 划定页面区域 | block | 没有任何默认样式 | `<div></div>` 
span | 普通文本 | inline | 没有任何默认样式 | `<span></span>`
p | 段落文字 | block | 自带下间距 | `<p></p>`
a | 超链接 | inline | 可链接到任意格式的本地、远程文件或get接口 | `<a href=""></a>`
img | 图片 | inline-block | 可链接到本地、远程图片文件 | `<img src="">`

<script async src="//jsfiddle.net/Red_Sign/h9g5043f/1/embed/html,result/dark/"></script>

### 字体效果标签

标签名 | 功能 | 标签类型 | 特点 | 写法
---|---|---|---|---
h1 | 一级标题（最大） | block | 加粗、字号较大、自带上下间距 | `<h1></h1>` 
h6 | 六级标题（最小） | block | 加粗、字号较大、自带上下间距 | `<h6></h6>` 
b | 文字加粗 | inline |  | `<b></b>` 

<script async src="//jsfiddle.net/Red_Sign/pq35sx92/1/embed/html,result/dark/"></script>

### 区段标签
> 和上下的内容进行区分和隔离

标签名 | 功能 | 标签类型 | 特点 | 写法
---|---|---|---|---
hr | 水平线分隔线 | block | 自带上下间距，调整颜色需使用`border-color` | `<hr/>` 
br | 换行 | block | 常用于段落中文字换行 | `<br/>` 

<script async src="//jsfiddle.net/Red_Sign/wuLnf3ob/8/embed/html,result/dark/"></script>

### 列表标签
> 用来表示多个有关联的内容，如商品列表、菜单等

标签名 | 功能 | 标签类型  | 特点 
---|---|--- | ---
ul | 列表容器 | block | 自带间距、列表前标记
li | 列表内容 | block | 

```html
<ul>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

<script async src="//jsfiddle.net/Red_Sign/qpf9e65a/1/embed/html,result/dark/"></script>

### 表格标签
> 常用于数据展示

标签名 | 功能 | 特点 
---|--- | --- 
table | 表格容器  
tr | 表格行  | tr内有几个th\td表示一行有几个单元格
th | 单元格（表头）| 大写、文字居中
td | 单元格 

<script async src="//jsfiddle.net/Red_Sign/yz8wpjge/1/embed/html,result/dark/"></script>

### 表单
> 用于发送请求，其中表单元素也可不依赖表单单独使用

标签名 | 功能 | 标签类型  | 写法
---|---|--- | ---
form | 表单容器 | block | `<form action=""></form>`
input | 表单控件（type属性控制其具体功能） | inline-block | `<input type="">`
textarea | 多行文本输入框 | inline-block | `<textarea></textarea>`
label | 自动聚焦标签 | inline  
select > option | 下拉框 | inline-block 


表单元素有很多属性，用来设置表单元素的值、特征等。如：
```html
<!-- 输入框默认值张三，禁用不可修改 -->
<input type="text" value="张三" disabled>
```

属性 | 描述 
---- |---
type           | 控件类型      
name           | 用于提交的数据名称       
value          | 指定默认值      
disabled       | 用来设置控件是否可用      
readOnly       | 用来设置控件的只读属性      


#### 不同类型的input
> 通过修改`input`标签的`type`属性可以改变控件类型 

```html
<input type="text">
```

控件类型   |  type值  
--- | ---- |
单行文本   | text    
密码       | password   
单选按钮   | radio    
复选按钮     | checkbox 
文件上传     | file    
按钮         | button     
重置按钮     | reset     
提交按钮     | submit   
 
#### 下拉框
```html
<select name="uek" size="1" multiple>
　　<option value="webui" selected="selected">前端工程师</option>
　　<option value="ui" selected="selected">ui设计师</option>
　　<option value="php" selected="selected">php工程师</option>
</select>
```
#### 自动聚焦 label
```html
<input type='radio' id='man'>
<label for='man'>男</label>
```
<script async src="//jsfiddle.net/Red_Sign/6pzgfv93/6/embed/html,result/dark/"></script>

### 实体
> 用特殊字符表示的符号，相当于普通的文字，防止与HTML自身的符号冲突

实体名 | 功能   
---|---
`&nbsp;` | 空格，想输入连续空格时只能用该实体  
`&lt;`| 小于号 <  
`&gt;`| 大于号 >  
`&copy;` | 版权符号 ©

<script async src="//jsfiddle.net/Red_Sign/hsfr27pu/1/embed/html,result/dark/"></script>

## JavaScript cookie 与 本地存储
> 客户端存储主要方便一些APP离线使用或数据跨页面使用,目前常见的客户端存储方式有cookie、localStorage和sessionStorage

浏览器查看三种存储：
![浏览器查看客户端存储](http://wangqifan.coding.me/JavaScript/new/amWiki/images/%E6%9C%AC%E5%9C%B0%E5%AD%98%E5%82%A8.png)


功能：  

* 记录保存用户的登录信息，这样用户在下次登录的时候就不用再次输入账号密码了。
* 保存一些简单的页面设置，比如说页面的背景，文字属性等。
* 统计用户访问该网站的习惯，比如什么时间访问，访问了哪些页面，在每个网页的停留时间等。


### cookie
#### 简介

* `cookie` 就是存储在浏览器中的一个字符串，用户访问某个网页时，可以通过`cookie`给访问者电脑存储一些简单数据
* 每当同一台计算机通过浏览器请求某个页面时，就会发送这个cookie。可以使用 `JavaScript` 来创建和取回 `cookie` 的值。

#### 用法
浏览器中可直接查看、修改cookie，双击对应的内容即可修改它的值：
![浏览器中查看cookied](http://wangqifan.coding.me/testDoc/assets/001/cookie.png)

> 扩展：使用JavaScript**访问cookie：**`document.cookie`、**设置cookie：** `document.cookie="key=val"`   （cookie的数据存储的结构是键/值对形式）


### `localStorage` 和 `sessionStorage`
> 新版本的HTML5提供了客户端存储`localStorage` 和 `sessionStorage`，是web存储的一种更为强大的版本，可提供更多的安全性、速度和易用性。存储数据量更大（5MB ——10MB）。并且此数据并不会在每次出现服务器请求时都被加载。

#### 基本概念：
* `localStorage` 负责存储长期的数据。当Web页面或浏览器关闭时，仍会保持数据的存储。
* `sessionStorage` 负责存储一个临时的数据。如果用户关闭了页面或浏览器，则会销毁数据。
* `sessionStorage` 和 `localStorage` 具有完全相同的使用语法。
* **不同浏览器、不同域名、不同端口号 存储的数据不能共用**
* `sessionStorage` 和 `localStorage`只能保存**字符串**类型的数据。

#### 用法

同样，在浏览器的`Application`栏中可对本地存储进行查看、双击修改、删除等操作：
![浏览器中查看cookied](http://wangqifan.coding.me/testDoc/assets/001/004-1573115328819.png)

使用案例：

* localStorage
    * 用户登录信息：用户名、token等
    * 未登录即可使用的购物车
* sessionStorage
    * 存储网页跳转时的数据：例如订单id、商品id
    * 记录网页状态：例如上一页停留在哪个选项卡

> 扩展：使用JavaScript **设置数据：**`localStorage.key=value;`，**获取数据：**`localStorage.key;`，**删除数据：**`localStorage.removeItem(key);`，**清空全部数据：**`localStorage.clear();`

****