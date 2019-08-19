CSS样式只有应用到HTML元素中，样式才会产生效果。有三种方式可以把CSS样式应用到HTML元素。一种方式是利用HTML元素的style属性，样式表作为style属性的值，该方式也称为行内样式；一种方式是将样式表放置在HTML网页文档head标签内，每个样式表赋予一个名称，然后在HTML元素中通过class属性引入样式表，该方式也称为内部样式；再一种方式是单独将样式表写入到一个文件，文件的扩展名为css，然后通过HTML的link标签链接外部样式表文件，在HTML元素中通过class属性引入样式表文件中的样式表，该方式也称为外部样式。

案例一：

# 1.行内样式

行内样式是利用HTML元素的style属性引入样式表，行内样式的优先级最高，行内样式会覆盖元素引入的内部样式或外部样式。

eg:

     <html>
     <head>
     <title>送杜少府之任蜀州</title>
     <meta charset="utf-8"/>
     </head>
     <body style="text-align:center;margin-top:20px;font-size:12px;">
     <p style="font-size:22px;font-family:楷体；font-weight:bolder;">送杜少府之任蜀州</p>
     <p>作者  王勃</p>
     <p style="font-size:18px;margin-top:30px；">城阙辅三秦，风烟望五津</p>
     <p style="font-size:18px;">与君离别意，同是宦游人</p>
     <p style="font-size:18px;">海内存知己，天涯若比邻</p>
     <p style="font-size:18px;">无为在歧路，儿女共沾巾</p>
     </body>
     </html>

>在上面的代码中，body元素引入了字体尺寸样式font-size，字体尺寸是12像素，body元素引入的样式会影响到body标签内所有的元素，当body标签内的元素引入自身样式后，其引入的自身样式将会覆盖body标签引入的样式。
>
>下面是浏览器显示效果:
>
>     <p style="font-size:22px;font-family:楷体；font-weight:bolder;">送杜少府之任蜀州</p>
>     <p>作者 王勃</p>
>     <p style="font-size:18px;margin-top:30px；">城阙辅三秦，风烟望五津</p>
>     <p style="font-size:18px;">与君离别意，同是宦游人</p>
>     <p style="font-size:18px;">海内存知己，天涯若比邻</p>
>     <p style="font-size:18px;">无为在歧路，儿女共沾巾</p>

# 2.内部样式

内部样式是在HTML的head标签内放置样式表，每个样式表赋予一个名称，用于标识一个样式。在HTML元素使用class属性引入已定义的样式名称。内部样式的优先级要低于行内样式，但高于外部样式。

eg：

    <html>
    <head>
    <title>送杜少府之任蜀州</title>
    <meta charset="utf-8"/>
    <style type="text/css">
    	.body_style{text-align: center;margin-top: 20px;font-size: 12px;}
    	.p_style{font-size: 18px;}
    	.p_title_style{font-size: 22px;font-family: 宋体;font-weight: bolder;}
    </style>
    </head>
    <body>
    <p class="p_title_style">送杜少府之任蜀州</p>
    <p>作者 王勃</p>
    <p style="margin-top: 30px;">城阙辅三秦，风烟望五津</p>
    <p>与君离别意，同是宦游人</p>
    <p>海内存知己，天涯若比邻</p>
    <p>无为在歧路，儿女共沾巾</p>
    </body>
    </html>

>在上面的网页代码中，样式表被放置在head标签中的style标签内，style标签属性type的值为text/css。放置在style标签内的每个样式表都被赋予一个有意义的名称，起到见名知义的作用。HTML元素利用class属性引入已定义的样式名称。从代码的简洁性和可维护性可以看出，使用内部样式明显要优于行内样式。

>下面是浏览器显示效果：

<p class="p_title_style">送杜少府之任蜀州</p>
	<p>作者 王勃</p>
	<p style="margin-top: 30px;">城阙辅三秦，风烟望五津</p>
	<p>与君离别意，同是宦游人</p>
	<p>海内存知己，天涯若比邻</p>
	<p>无为在歧路，儿女共沾巾</p>


# 3. 外部样式

外部样式是将样式表写入到一个外部文件，外部文件的扩展名为css，样式表的写法和内部样式的写法相同。外部样式文件可以通过HTML的link标签链接到网页文档，样式表文件链接到网页文档后，HTML元素可以通过class属性引入样式文件中的样式表。外部样式的优先级最低。样式表文件同HTML文件一样，也是文本文件，可以使用任何文本编辑器编辑，也可以使用高级一点的编辑工具，如EditPlus、UltraEdit、Dreamweaver等软件。样式表文件的写法同内部样式的写法相同。下面是样式表文件代码，和网页文件在同一目录下。

     .body_style{text-align: center;margin-top: 20px;font-size: 12px;}
     .p_style{font-size: 18px;}
     .p_title_style{font-size: 22px;font-family: 宋体;font-weight: bolder;}


在网页文件中使用link标签链接前面写好的CSS文件，在link标签的href属性设置CSS文件的路径，路径可以是绝对路径，也可以是相对路径，HTML元素引入样式表的方法同内部样式相同。网页文件代码如下。

    <html>
    <head>
     <title>送杜少府之任蜀州</title>
     <meta http-equiv="Content-Type";content="text/html";charset="utf-8"/>
     <link rel="stylesheet" type="text/css" href="style.css"/>
    </head>
    <body>
     <p class="p_title_style">送杜少府之任蜀州</p>
     <p>作者 王勃</p>
     <p style="margin-top: 30px;">城阙辅三秦，风烟望五津</p>
     <p>与君离别意，同是宦游人</p>
     <p>海内存知己，天涯若比邻</p>
     <p>无为在歧路，儿女共沾巾</p>
    </body>
    </html>

>效果如下：

	<p class="p_title_style">送杜少府之任蜀州</p>
	<p>作者 王勃</p>
	<p style="margin-top: 30px;">城阙辅三秦，风烟望五津</p>
	<p>与君离别意，同是宦游人</p>
	<p>海内存知己，天涯若比邻</p>
	<p>无为在歧路，儿女共沾巾</p>
# 案例二：

# 一、内联样式

　　内联样式通过style属性来设置，属性值可以任意的CSS样式。

代码：

     <!DOCTYPE html>
     <html lang="en">
     <head>
       <meta charset="UTF-8">
       <title>内联样式</title>
     </head>
     <body>
       <p style="background: red"> I  love  China!</p>
     </body>
     </html>

显示效果：

![](https://images2017.cnblogs.com/blog/1252860/201802/1252860-20180201215245171-1078506528.png)
　　

# 二、内部样式

　　内部样式定义在文档的head部分，通过style标签来设置。需要使用元素选择器（p）来关联样式和要设置样式的标签（p标签）。

代码：
     
     <!DOCTYPE html>
     <html lang="en">
     <head>
       <meta charset="UTF-8">
       <title>内联样式</title>
       <style type="text/css">
          .p{ 
             background: green;
          }
    </style>
    </head>
    <body>
        <p> I  love  China!</p>
    </body>
    </html>

效果：

![](https://images2017.cnblogs.com/blog/1252860/201802/1252860-20180201215627046-8500019.png)

# 三、外部样式

　　在文档外的*.css定义css样式，然后在文档的head部分通过link元素引入。　　

代码:

       <!DOCTYPE html>
       <html lang="en">
       <head>
          <meta charset="UTF-8">
          <title>内联样式</title>
          <link rel="stylesheet" href="style.css">
       </head>
       <body>
           <p> I  love  China!</p>
       </body>
       </html>

style.css文件内容：

       p{ 
             background: yellow;
         }

显示效果：

![](https://images2017.cnblogs.com/blog/1252860/201802/1252860-20180201220344218-1222052546.png)

## a.在一个外部样式表中导入其他样式表的样式

eg:

combine.css文件中导入上面的style.css

     @import "style.css";
     body{
        background: red;
      }
HTML文件中引入combine.css文件:

代码:

     <!DOCTYPE html>
     <html lang="en">
     <head>
          <meta charset="UTF-8">
          <title>document</title>
          <link rel="stylesheet" href="combine.css">
     </head>
     <body>
          <p> I  <span>love</span>  China!</p>
     </body>
     </html>　　

显示效果：

![](https://images2017.cnblogs.com/blog/1252860/201802/1252860-20180201231633125-1386362545.png)

## b、声明样式表的字符编码　

    @charset "utf-8"
    p{ 
             background: yellow !important;
         }　

# 四、元素样式的层叠和继承

## 1、样式层叠

　　样式表允许以多种方式规定样式信息。样式可以规定在单个的 HTML 元素中，在 HTML 页的头元素中，或在一个外部的 CSS 文件中。甚至可以在同一个 HTML 文档内部引用多个外部样式表。一般而言，所有的样式会根据下面的规则层叠于一个新的虚拟样式表中，其中数字 4 拥有最高的优先权。　　

### 1.浏览器缺省设置（浏览器的默认样式）

### 2.外部样式表

### 3.内部样式表（位于 <head> 标签内部）

### 4.内联样式（在 HTML 元素内部）

### 5.同一样式表中，CSS选择器越准确的，优先级越高。


   不同优先级的样式表定义元素的不同css属性都会作用在元素上，相同的css属性只有优先级最高的会对元素起作用。相同优先级样式表中css选择器准确的样式起作用，同一样式表中css选择器一样的后边会覆盖前边的样式。

用重要样式（！important）可以调整层叠次序:　

代码:

      <!DOCTYPE html>
      <html lang="en">
      <head>
         <meta charset="UTF-8">
         <title>内联样式</title>
         <link rel="stylesheet" href="style.css">
      </head>
      <body>
          <p  style="background: red"> I  love  China!</p>
      </body>
      </html>

style.css文件:　　

       p{ 
             background: yellow !important;
          }

important标记的样式会有最高的优先级:

![](https://images2017.cnblogs.com/blog/1252860/201802/1252860-20180201224533531-2105071833.png)

　　在谷歌浏览器的开发者工具中我们可以查看元素的优先级，同一个元素的最上面的样式的优先级最高。

![](https://img2018.cnblogs.com/blog/1252860/201901/1252860-20190127015043697-121344092.png)

## 2、样式继承

代码:

     <!DOCTYPE html>
     <html lang="en">
     <head>
        <meta charset="UTF-8">
        <title>document</title>
        <style type="text/css">
            .p{
                color: white;
                background: grey;
                border: 2px solid black; 
               }
        </style>
     </head>
     <body>
         <p> I  <span>love</span>  China!</p>
     </body>
     </html>
显示效果：

![](https://images2017.cnblogs.com/blog/1252860/201802/1252860-20180201225240812-1126097364.png)

- span元素并没设置字体颜色，但是却是用前景色white,这个值有父元素p继承来。可以从一个元素的祖先元素继承样式，继承来的样式的优先级是最低的（比浏览器的默认样式的优先级都低）。

- 并非所有的css属性均可继承，只有与元素外观相关的元素会继承。元素在页面布局相关的样式不会继承，css中可以使用inherit强行实行继承。　　

代码:

     <!DOCTYPE html>
     <html lang="en">
     <head>
         <meta charset="UTF-8">
         <title>document</title>
         <style type="text/css">
             .p{
                 color: white;
                 background: grey;
                 border: 2px solid black; 
               }
             span{
                 border: inherit;
         }
     </style>
     </head>
     <body>
          <p> I  <span>love</span>  China!</p>
     </body>
     </html>


　　　　　　

## 3.继承属性和通用元素选择器

　　我们有时候给所有元素的设置某个样式，如字体等，我们一般会使用通用选择器来设置。但是对所有元素都起作用，效率较低，这个时候我们可以考虑给body元素设置字体，body的子元素会默认继承字体。




