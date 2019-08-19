# HTML基础

# 一、WEB前端的标准

   网页制作的标准，是由一系列标准组成的，主要包含三个方面：结构（html），表现(css)，行为（JavaScript）。
![markdown](https://images2017.cnblogs.com/blog/1083924/201712/1083924-20171224144150975-1373575862.png)

>注：结构和表现的标准是由w3c制定，行为标准由ECMA制定。

# 二、HTML相关的概念

## 1.html——超文本标记语言

## 2.xhtml——可扩展的超文本标记语言

## 3.html的第五次重大修改

>注：html和xhtml的区别：xhtml规范：必须小写，有开始结束标签，属性也用双引号；html：不区分大小写，有开始和结束标签，也可把结束标签放在开始标签里，如：`<input type='text' />`。属性可用双引号、单引号（但是必须配对）。
 xhtml相对于html并没有增加新的标签，只是语法要求严格，比如：标签必须闭合，标记名称必须小写等等。

# 三、html基本结构

## 1.文档声明

   html5的文档声明语法：`<!DOCTYPE html>`
   作用：告知浏览器文档使用哪种html和xhtml规范。

## 2.html

   html是网页的根元素或跟标签，所有的网页内容和标签都放在html标签之间。
   语法：`<html></html>`

## 3.html包含两大部分

### （1） head部分

   一般设置meta头元素或引入一些外部的css文件，js文件等以及关键字，描述设置字符编码：
   `<meta charset="utf-8"/>` 防止网页出现乱码；
   其他编码格式：gb2312,gbk;

### （2）body部分

   所有在网页中显示的内容及放置内容的标签都应放在body部分；

#### 基本结构

```
     <!DOCTYPE html> 命名文档类型
     <html></html> 说明写的是标记语言
     <head></head> 文件头部
     <title></title> 文件标题（显示在状态栏上的内容）
     <meta charset="utf-8"/> 编码格式
     <body></body> 文件主体（所有要写的内容）
```

# 四、 html基本语法

## 1.常规标记

   语法：`<标记 属性="属性值" 属性="属性值"></标记>`
   eg:`<h1 class="text-xxl">hello world!</h1>`

## 2.空标记

   语法：`<标记 属性="属性值" />`
   eg:`<img src="1.jpg" />`

>注：1.属性和属性值用等号连接，属性值要放在双引号中（所有标点符号都必须英文状态的）；2. 标记名称全部使用小写（标准）；（3）属性和属性之间用空格隔开，是不区分先后顺序的；

# 五、 html常用标记

## 1.网页标题

   语法：`<hx>网页标题内容</hx>(x为1-6)`

   eg：`<h3>标题</h3>`

## 2.段落文本

   语法：`<p>段落文本内容</p>`

## 3.转义字符

   空格转义字符：&nbsp;
   其他常用转义字符：">"="&gt"; "<"="&lt"; 版权声明="&copy"；
   HTML转义字符表：<http://tool.oschina.net/commons?type=2>

## 4.强制换行

   语法：`<br/>`（空标记）

## 5.加粗

   语法：`<strong>加粗文本</strong>` `<b>加粗文本</b>`

## 6.倾斜

   语法：`<em>加粗文本</em>` `<i>加粗文本</i>`

## 7.水平分割线

   语法：`<hr/>`

eg:

    <hr align="left" size="3" width="50%"/>
    <hr align="center" size="3" width="50%"/>
    <hr align="right" size="3" width="50%"/>
    <hr noshade/>

效果：

![](G:\web开发\水平分割线.png)

 - align 左对齐 右对齐 居中
 - size 粗细 单位像素
 - color 颜色
 - width 宽度（就是这条线有多长） 50%表示的是父层宽度的50%
 - noshade (没有属性值的属性) 不要阴影 

## 8.上标和下标

语法：

   上标：`<sup></sup>`

   下标：`<sub></sub>`

## 9.无序列表

语法：

      <ul>
          <li>aa</li>
          <li>bb</li>
         ... 
       </ul>  
>ul:type有：circle(空心圆); disc(实心圆);square(实心正方形);none(前面无符号);

## 10.有序列表

语法：

      <ol type="a" start="2">
          <li>aaa</li>
          <li>bbb</li>
          ...
      </ol>
> 注：type用来设置序号的类型，可以设置A,a,i,Ⅰ,1；strat用来设置从几开始；

eg： 

    <ol type="a" start="2">
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
     </ol>
效果：（默认序号类型是数值，设置属性type="a"的作用，start是从2开始，因此是从b开始显示） 

<ol type="a" start="2">
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
        <li>今天天气不错，阳光明媚！适合敲代码！</li>
     </ol>

## 11. 自定义列表

   语法：

      <dl>
        <dt>A</dt>
        <dd>a1</dd>
        <dd>a2</dd>
        ...
        <dt>B</dt>
        <dd>b1</dd>
        <dd>b2</dd>
        ...
       </dl>
>注： dt和dd是并列关系；在dl中可以存在很多组dt,dd,每组中只能存在一个dt,可以存在多个dd。

## 12. 图片

   语法：`<img src="图片路径" width="数值" height="数值" alt="替换文本" title="提示文本"/>`

>注： alt和title的区别：title是当鼠标悬停在图片上时要显示的提示信息；alt是当图片由于某些原因无法正常加载时要显示的替换信息。


        <!--
          图片路径        src(相对路径)
          宽度            width
          高度            height
          边框粗细        border  
          水平对齐方式    align   left/center/right
          -->
        <!--如果想要等比例缩放，就只能给宽或高，二者中的一个-->
        <!--img align="center" 不可以实现图片居中的-->
        <!--div做桥,将图片放在div中，然后设置div中的内容居中-->

eg：
       
        <div style="text-align:center;">
           <img src="images/2.jpg" align="left">
        </div>

> 相对路径的三种写法：
>
  - 当当前文件和目标文件在同一目录下，写法如下：目标文件名+扩展名；
  - 当当前文件和目标文件所处文件夹在同一目录下，写法如下：目标文件所处文件夹名/目标文件名+扩展名；
  - 当当前文件所处文件夹和目标文件所处文件夹在同一目录下，写法如下：.../目标文件所处文件夹名/目标文件名+扩展名；

## 13. 超链接

   语法：`<a href="http://链接地址或链接文件" target="_blank" title="提示信息">链接文本或图片</a>`

>  - target属性用来设置超链接是否在新窗口打开；
>  - target="_blank"链接在新窗口打开；
>  - target="_self"默认值，在本窗口打开；

>注：空链接 `<a href="#">新闻</a>` (跳转到页面顶部)

## 14. 表格（显示数据（多用于后台管理））

      标签释义：
         <caption></caption>:表头信息；
         <tr></tr>:定义一个表格行；
         <th></th>:定义一个表格头：自带居中效果，若是纯文本，默认以粗体的样式展现；
         <tbody></tbody>：可以理解为表格的内容区域，在Chrome、FF浏览器通过DOM进行表格动态插入行的时候，要使用这个。如果不进行DOM操作，可不用添加。
         <td></td>：定义一个单元格；
语法：

      <table border=0 title="测试">
        <caption> 表格标题</caption>
        <tr>
            <th>姓名</th>
            <th>年龄</th>
        </tr>
        <tr>
            <td>张三</td>
            <td>22</td>
        </tr>
        <tr>
            <td><input type=text /></td>
            <td><input type=text /></td>
        </tr>
      </table>
效果：
<table border=0 title="测试">
   <caption> 表格标题</caption>
   <tr>
     <th>姓名</th>
     <th>年龄</th>
   </tr>
   <tr>
      <td>张三</td>
      <td>22</td>
   </tr>
   <tr>
      <td><input type=text /></td>
      <td><input type=text /></td>
   </tr>
</table>

>注：表格相关属性：
>
   - （1）border 设置边框的宽度；
   - （2）cellspacing 设置单元格之间的间距
   - （3）cellpadding 设置内容和单元格之间的空隙
   - （4）align="left|center|right" 设置单元格内容的对齐方式
   - （5）width 设置单元格的宽度
   - （6）height 设置单元格的高度或者tr的高度
   - （7）colspan="数值" 合并列（在td加）
   - （8）rowspan="数值" 合并行（在td加）

>高级属性：
>
   - （1）合并相邻单元格边框
      语法：border-collapse:collapse（合并相邻单元格边框）|separate（边框分开）；
      注：border-collapse（在table加）
>
>eg： 不设置border-collapse属性，默认值separate；
>
    <!doctype html>
    <html lang="en">
    <head>
       <meta charset="UTF-8">
       <title>表格高级属性</title>
       <style type="text/css">
       .tab{
           /*border: 1px solid black;*/
        }
       .tab td{
           border:1px solid black;
           padding:5px 10px;
           text-align: center;
        }
       </style>
    </head>
    <body>
       <table class="tab" cellpadding="0" cellspacing="5" >
            <caption>测试数据</caption>
          <tr>
              <td>测试数据</td>
              <td>测试数据</td>
              <td>测试数据</td>
              <td>测试数据</td>
           </tr>
           <tr>
              <td>测试数据</td>
              <td>测试数据</td>
              <td>测试数据</td>
              <td>测试数据</td>
           </tr>
           <tr>
              <td>测试数据</td>
              <td>测试数据</td>
              <td>测试数据</td>
              <td>测试数据</td>
           </tr>
         </table>
     </body>
     </html>

>效果： 
<!doctype html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <title>表格高级属性</title>
   <style type="text/css">
   .tab{
       /*border: 1px solid black;*/
    }
   .tab td{
       border:1px solid black;
       padding:5px 10px;
       text-align: center;
    }
   </style>
</head>
<body>
   <table class="tab" cellpadding="0" cellspacing="5" >
        <caption>测试数据</caption>
      <tr>
          <td>测试数据</td>
          <td>测试数据</td>
          <td>测试数据</td>
          <td>测试数据</td>
       </tr>
       <tr>
          <td>测试数据</td>
          <td>测试数据</td>
          <td>测试数据</td>
          <td>测试数据</td>
       </tr>
       <tr>
          <td>测试数据</td>
          <td>测试数据</td>
          <td>测试数据</td>
          <td>测试数据</td>
       </tr>
     </table>
 </body>
 </html>


>
> -   （2）定义表格标题的位置（在table加）
> 语法：caption-side:top|bottom|left|right;
> 注：left和right只有火狐识别；caption是一个块状元素；
>
> - （3）设置单元格的间距（在table加）
>   语法：border-spacing：数值+单位；
>   注：当设置了border-collapse：collapse时，border-spacing会失效；
>
> - （4）隐藏或显示无内容单元格（在table加）
>   语法：empty-cells：show（显示）|hide（隐藏）；
>
> - （5）表格布局算法（在table加）
>   语法：table-layout：fixed|auto；
>   注：当设置为fixed的时候，单元格宽度固定，不随内容多少发生变化；
>
>   代码：
>
>   ```
>   <html>
>           <head>
>             <meta charset="UTF-8">
>             <style type="text/css">
>               
>              .tab3{
>                table-layout:fixed;
>                }
>   
>             </style>
>           </head>
>           <body>
>             <table class="tab3" width="400" border="1" cellspacing="0" cellpadding="0">
>               <tr height="30">
>                 <td width="300">jjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjj</td>
>                 <td width="100">777777777777777777777777777777777</td>
>               </tr>
>             </table>
>           </body>
>   </html>
>   ```
>

效果：

   ![](G:\web开发\宽度固定.png)    

### 表格相关html属性

#### 1. 设置单元格内容水平对齐方式

   align="left|center|right"

#### 2. 设置单元格内容垂直对齐方式

   valign="top|middle|bottom"

#### 3. 设置表格分割线

   rules="rows|cols|all|groups|none"

>rows:行分割线；cols:列分割线；all:行分割线和列分割线；groups:组分割线；none:没有分割线；

#### 4. 表格行分组

 `<thead></thead>` `<tbody></tbody>` `<tfoot></tfoot>`

#### 5. 表格列分组

`<colgroup span="数值"></colgroup>` `<col span="数值"/>`

>注：推荐使用colgroup进行列分组
span的默认属性值为1，一列为一组，设置为几即为几列为一组；

>着重释义：colspan：表示横向合并单元格（![](https://images0.cnblogs.com/blog/153475/201306/08135520-74522fef3995483a81869fbc4494644e.jpg)）；rowspan：表示纵向合并单元格（![](https://images0.cnblogs.com/blog/153475/201306/08140216-277b6a1c53d94bfa9d7eb8aa87654e2d.jpg)）；

# 六、 表单

​    作用：用来搜集用户信息
​    语法：<form method="" action=""></form>
​    注：所有的表单控件都要放在form标签之间； 

## 1. 文本框

语法：`<input type="text" value="admin" name="username"/>`
>注：value 用来设置默认值；name属性主要供后端获取输入的内容或信息；

## 2. 密码框

语法：`<input type="password"/>`

## 3. 提交按钮

语法：`<input type="submit" value="登录"/>`

>注：提交按钮的默认value值为提交或提交查询，可重新设置需要的value值；

## 4. 重置按钮

语法：`<input type="reset"/>`

## 5. 单选按钮

语法：`<input type="radio" name="***" checked="checked"/>`

>注：使用单选按钮时，一组中的单选按钮必须添加一致的name属性，才能实现多选一的效果；设置checked属性可以实现页面加载完成后添加默认选中状态；当属性和属性值相同时，可以省略属性值，如checked="checked" 可以写成checked；

## 6. 复选框（复选按钮）

语法：`<input type="checkbox" checked disabled/>`

>注：checked属性主要应用在单选和复选按钮上；disabled属性用来设置input控件的禁用状态；

## 7. 下拉菜单

语法：

      <select>
        <option>b</option>
        <option selected>a</option>
       ...
      </select>
效果:

<select>
    <option>b</option>
    <option selected>a</option>
   ...
  </select>

>注：selected用来设置下拉列表的默认选中项；

## 8. 文本域

语法：`<textarea cols="字符宽度" rows="行数"></textarea>`

>注：禁止用户通过拖拽改变文本域的大小；`textarea{resize:none;}`;

## 9. 普通按钮

语法：`<input type="button" value="***"/>`

>注：普通按钮不具备提交的功能，通常结合js使用；普通按钮默认value值为空，可以重新设置value属性；

## 10. 提示信息

### a）可以将单选或复选按钮和文字进行关联，点击文字也可选中单选，复选按钮

eg:
> `<input type="radio" name="sex" id="boy"/><label for="boy">男</label>`
> `<input type="checkbox" id="ball"/><label for="ball">篮球</label>`

### b）将提示信息放置在label标签中可以设置用户想要的样式；

### c）label标签时内联元素；

## 11. 表单字段集及表单字段集标题

语法：

     <fieldset>
       <legend>用户注册</legend>
        ...
       </fieldset>
>注：将form中的表单控件进行分组，并添加一个标题；

## 12. 上传文件

语法： `<input type="file"/>`

## 13. 隐藏字段

语法：`<input type="hidden"/>`
>注：主要提供后端修改数据的时候使用；

## 14. 图像域

语法：`<input type="image" width="***" height="***" src="图片路径"/>`

>作用：使用图像作为提交按钮，具备提交功能；

### form标签上的相关属性解释

#### 1. method用来设置数据传送方式，一般为get和post方式；

get和post的区别：

##### 1. get是从服务器上获取数据，post是向服务器传送数据；

##### 2. get是把参数数据队列加到提交表单的ACTION属性所指的URL中，值和表单内各个字段一一对应，在URL中可以看到。post是通过http post机制，将表单内各个字段与其内容放置在html header内一起传送到action属性所指的URL地址。用户看不到这个过程。

##### 3. 对于get方式，服务器端用Request.QueryString获取变量的值，对于post方式，服务器端用Request.Form获取提交的数据。

##### 4. get传送的数据量较小，不能大于2KB。post传送的数据量较大，一般被默认为不受限制。但理论上，IIS4中最大量为80KB，IIS5中为100KB。

##### 5. get安全性非常低，post安全性较高。但是执行效率却比Post方法好。

#### 2. action 用来设置数据要发送到的位置，一般为后端文件;

>eg:  `<form method="get/post" action="http://www.qfedu.com/index.php"></form>`

# 七、 div

作用：在布局网页时用来划分板块；
语法：`<div></div>`

# 八、span

语法： 
`<span>`标签被用来组合文档中的行内元素。在行内定义一个区域，也就是一行内可以被`<span>`划分成好几个区域，从而实现某种特定效果。`<span>`本身没有任何属性。

在IE6下，`span`元素浮动时一定要把`span`元素放在a标签之前，不然，会出现浏览器兼容问题，IE6下，浮动过后的`span`元素会向下错位一行。

>提示和注释：
>提示：请使用<span>来组合行内元素，以便通过样式来格式化它们。
>
>注：`span`没有固定的表现格式，只有在对它应用样式时，才会产生视觉上的差异;`span`可以实现将文本的某一部分独立出来;

# 九、 iframe框架和`<frameset>`标签

## 1. iframe框架

语法：
`<iframe src="3.表单.html" width="500" frameborder="0" scrolling="auto"></iframe>`
      

      注：
       width：iframe框架的宽度
       height：iframe框架的高度
       frameborder：设置iframe框架的边框
       scrolling = "no"：隐藏（去掉）iframe的滚动条

## 2. frameset 定义一个框架集，包含多个框架，每个框架都有独立的文档

### 2.1 格式

      <frameset >
         <frame src="a.html" />
         <frame src="b.html" />
         <noframes>框架无效</noframes>
      </frameset>

### 2.2 子项说明

`<frame src="a.html" /> `：子框架

`<noframes></noframes>`：浏览器不支持此框架的时，显示的内容。

### 2.3 属性

#### frameset 属性：

rows ：表示子框架按行的样式布局(![](https://images0.cnblogs.com/blog/153475/201305/24173151-790b77bbe58b408a93119669f7426ff7.jpg))。以2个子框架为例：rows="30%,*" ，表示第一个框架占整个页面30%的高度，第二个占剩下的；

cols ：表示子框架按列的样式布局(![](https://images0.cnblogs.com/blog/153475/201305/24173222-4591291731484862ab3bb01be3c3e491.jpg))。以2个子框架为例：cols="30%,*" ，表示第一个框架占整个页面30%的长度，第二个占剩下的；

noresize="noresize" ：表示不调整子框架的范围。

#### frame 属性：

src ：指向一个资源(如页面、图片等)的URI；

name ：指定框架的名称，以便进行框架间的操作；

# 十、 html注释

语法：`<!--注释内容-->`