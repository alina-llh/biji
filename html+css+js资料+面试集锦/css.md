# css课程
## 一、CSS 概念
### 01.什么是css
>层叠样式表(英文全称：Cascading Style Sheets)是一种用来表现HTML（标准通用标记语言的一个应用）或XML（标准通用标记语言的一个子集）等文件样式的计算机语言。CSS不仅可以静态地修饰网页，还可以配合各种脚本语言动态地对网页各元素进行格式化。
CSS 能够对网页中元素位置的排版进行像素级精确控制，支持几乎所有的字体字号样式，拥有对网页对象和模型样式编辑的能力。 
<img src=https://upload-images.jianshu.io/upload_images/3532891-a78a2de5c5211630.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 02.css历史
>01.从HTML被发明开始，样式就以各种形式存在。不同的浏览器结合它们各自的样式语言为用户提供页面效果的控制。最初的HTML只包含很少的显示属性。
>02.随着HTML的成长，为了满足页面设计者的要求，HTML添加了很多显示功能。但是随着这些功能的增加，HTML变的越来越杂乱，而且HTML页面也越来越臃肿。于是CSS便诞生了
>03.1994年哈坤·利提出了CSS的最初建议。而当时伯特·波斯（Bert Bos）正在设计一个名为Argo的浏览器，于是他们决定一起设计CSS。
>04.其实当时在互联网界已经有过一些统一样式表语言的建议了，但CSS是第一个含有“层叠”丰意的样式表语言。在CSS中，一个文件的样式可以从其他的样式表中继承。读者在有些地方可以使用他自己更喜欢的样式，在其他地方则继承或“层叠”作者的样式。这种层叠的方式使作者和读者都可以灵活地加入自己的设计，混合每个人的爱好
>05.1995年初，W3C内组织了专门管CSS的工作组
>06.1996年12月，CSS1.0 发布
>07.1998年5月，CSS2.0 发布
>08.2001年5月，CSS3.0 发布

### 03.css的作用
>01.CSS可译为层叠样式表或级联样式表，是一组格式设置规则，主要用于控制 WEB 外观。通过 CSS 样式设置页面的风格。可以将页面的内容与表现形式相分离。
>02.层叠就是浏览器对多个样式来源进行叠加，最终确定结果的过程。CSS 之所以有“层叠”的概念，是因为有多个样式来源。

### 04.DIV+CSS布局
>01.DIV+CSS是WEB设计标准，它是一种网页的布局方法。
>02.与传统中通过表格（table）布局定位的方式不同，它可以实现网页页面内容与表现相分离。提起DIV+CSS组合，还要从XHTML说起。XHTML是一种在HTML（标准通用标记语言的子集）基础上优化和改进的新语言，目的是基于XML应用与强大的数据转换能力，适应未来网络应用更多的需求。
>03.“DIV+CSS”其实是错误的叫法，而标准的叫法应是XHTML+CSS。因为DIV与Table都是XHTML或HTML语言中的一个标记，而CSS只是一种表现形式。也许其提出者本意并没有错，但是跟风者从表现曲解了其意思，认为整个页面就应当是DIV+CSS文件的组合。

### 05.网页的组成方式
>01.html   结构。搭建页面的骨架
<img src=https://upload-images.jianshu.io/upload_images/3532891-4ee297b9ce8bef1f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

>02.css    样式。控制页面的外观  颜色、布局等等设置
<img src=https://upload-images.jianshu.io/upload_images/3532891-701e558876b38e7f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

>03.JavaScript  行为。让网页动起来，标签动起来，数据动起来
<img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1572926659739&di=37de5b299f2ca89d6a49cbfd36ac6332&imgtype=0&src=http%3A%2F%2Fbbsfiles.vivo.com.cn%2Fvivobbs%2Fattachment%2Fforum%2F201710%2F09%2F211023pzbbjpq3dpqybh44.gif">

### 06.浏览器渲染流程
>1、浏览器开始解析目标HTML文件，执行流的顺序为自上而下。
>2、HTML解析器将HTML结构转换为基础的DOM(文档对象模型)，构建DOM树完成后，触发DomContendLoaded事件。
>3、CSS解析器将CSS解析为CSSOM(层叠样式表对象模型)，一棵仅含有样式信息的树。
>4、CSSOM和DOM开始合并构成渲染树，每个节点开始包含具体的样式信息。
>5、计算渲染树中个各个节点的位置信息，即布局阶段。
>6、将布局后的渲染树显示到界面上。

### 07.css阻塞渲染
>1）根据浏览器的流程，当cssdom还没构建完成时，页面是不会渲染到浏览器界面的，这也是为什么当css下载过慢时，会出现白屏的现象
>2) CSS 被视为阻塞渲染的资源，这意味着浏览器将不会渲染任何已处理的内容，直至 CSSOM 构建完毕。请务必精简您的 CSS，尽快提供它，并利用媒体类型和查询来解除对渲染的阻塞。

## 二、css的引入方式
### 01.内联式、 行内引入：
>1.直接在html的标签中书写css。这是一种最为原始也是最容易理解的.
>2.样式内容书写在html标签的style属性中，多个css样式可以写在一起，使用分号隔开。`<标签名 style="具体样式属性: 属性值;">内容</标签名>`
>3.样式书写是   样式名:样式值; (注意全部是英文半角符号)

>内联式特点：
    1、冗余代码多，代码量大
    2、不利于维护和修改
    3、优先级相对来说较高，个别特殊的效果可以使用，但是不要滥用

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>内联式引入css</title>
</head>
<body>
    <ul>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
        <li style="background-color: green;width: 100px;height: 100px;float: left;margin: 10px;color: #fff;text-align: center;line-height: 100px;"></li>
    </ul>
</body>
</html>
```

### 02.嵌入式引入 头部引入
>01.使用css选择器选择你要控制的元素，然后书写样式
>02.可以把样式书写在style标签中
>03.然后把style标签放在head标签中

>样式书写格式：
    选择器{
        样式名1:样式值1;
        样式名2:样式值2;
    }

>嵌入式引入特点：
    1、统一放置在 style 标签当中，然后通过选择器，将规定样式和对应的标签建立联系，便于维护和修改
    2、CSS 样式修改时并不需要翻阅 HTML 代码，也不需要去针对每个 HTML 标签处理样式，只需要调整style 标签中的样式，就可以针对性修改，页面达到了样式与结构相分离
    3、代码量少

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>嵌入式引入css</title>

    <style>
        li{
            color:red;
            background-color: yellow;
        }
    </style>
</head>
<body>
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>

</body>
</html>
```

### 03.css外部式引入
>在外部新建一个css文件（后缀是.css），把样式写在外部的css文件中
<img src=https://upload-images.jianshu.io/upload_images/3532891-d0035e817f04be4a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
<img src=https://upload-images.jianshu.io/upload_images/3532891-5772de72d950e995.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

>当一个页面需要外部css的时候，可以使用link标签把css引入进来,把link标签书写在head标签中
`<link rel="stylesheet" type="text/css" href="./index.css">`

>link标签书写的位置应该和style是一样的
    href:相关联css的路径
    rel：stylesheet  link引入的css和当前的文档html进行关联
    type：text/css  引入的格式是text文本，是css文本

>特点：
    1、将html和css完全分离成两个文件
    2、一个css文件可以控制多个html文件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" type="text/css" href="./index.css">
</head>
<body>
    <div>

    </div>
</body>
</html>
```

### 04.style标签和link标签的书写位置
>如果书写到非head标签的位置可能会引起一些问题

>1.不便于维护:后期维护的时候需要花费时间去寻找代码书写位置
>2.会引起页面的回流（重排）和重绘
    1)网页是DOM tree 和 样式结构 结合以后构建的render tree（渲染树），浏览器就是根据render tree来绘制页面的
    2)回流（重排）：当render tree中的一部分或者是全部，因为元素的尺寸、布局、隐藏等等改变引起页面的重新渲染（重新构建绘制）
    3)重绘：当render tree中一些元素需要更新属性，这些更新的属性只会影响元素的外观、风格，不会影响元素的布局
>3.页面从上至下去解析，假设style标签写在body后边，读取这个style之前，整个网页的文档已经渲染的差不多了，发现还有style标签,页面就会重新计算页面的样式 然后重新渲染，所以会引起 重绘和重排，网页可能出现闪烁，并且加载变慢
>4.所以style标签应该书写在head标签中

### 05.@import引入
>使用@import方法，在style标签中引入
`@import "index.css";`
`@import url(index.css);`
`@import url("index.css");`

### 06.link引入和@import引入的对比
>1、**适用的范围**
    @import在style标签中引入，也可以在外部的css文件中书写
    而link只能在html中书写引入
>2、**功能范围不同**
    link属于html标签
    @import只是css提供的引入css的功能
>3、**加载顺序不同**
    页面在加载的时候，link引入的css会同时被加载
    @import引入的css只有等页面全部下载完成以后才进行加载，所以可能会出现闪烁
>4、**兼容性**
    link都支持
    @import低版本ie不支持
>5、**使用JS控制样式**
    JS只能控制link标签
    @import是不能够被JS控制的

## 三、css的基础选择器
### 01.什么是选择器
>要使用css对HTML页面中的元素实现一对一，一对多或者多对一的控制，这就需要用到CSS选择器。
>HTML页面中的元素就是通过CSS选择器进行控制的
### 02.id选择器
>我们可以给元素设置id属性，然后通过 #+id属性值 的方式来选择这个元素

>选择器命名：
    1、id就像我们的身份证号，是不允许重复的
    2、并且一个元素只能有一个id属性
    3、id命名规范建议（类名相同）：
        id或者class必须以字母开头，不能以数字或者下划线开头
        名字不能是汉字，必须是英文的小写
        不允许带有广告的英文单词出现：如：ad adv adver advertising (防止浏览器当成垃圾广告处理掉 过滤掉 )
        后边小写字母、数字、连字符（ _  -）
        名字不能是汉字，必须是英文的小写
        见名知意
        不要出现空格
        一定要有自己的含义

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>id选择器</title>
    <style>
        #three{
            background-color: green;
        }
    </style>
</head>
<body>
    <ul>
        <li id="three"></li>
        <li></li>
    </ul>
</body>
</html>
```
### 03.类选择器：
>1、可以给不同的元素，进行分组。
   所有类名相等的元素，是一组的，可以进行控制样式
>2、给要被分组的元素设置class属性   
    选择器中使用 .+ class属性值 来选择元素
>3、类名不一定是多个，也可以是一个
>4、一个class可以设置多个类名，但是只能有一个class属性
    class属性的值可以用空格隔开，就代表书写多个类名
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>id选择器</title>
    <style>
        li{
            background-color: red;
        }
        .show{
            background-color: green;
        }

        .active{
            background-color: yellow;
        }
        .con{
            width: 100px;
            height: 100px;
        }
    </style>
</head>
<body>
    <ul>
        <li class="show"></li>
        <li></li>
        <li class="show"></li>
    </ul>
    <div class="active con"></div>
</body>
</html>
```
### 04.标签名选择器：
>1)通过标签名来选择元素
>2)会选择页面中（控制条件中）所有的这个标签的元素
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>标签名选择器</title>
    <style>
        li{
            background-color: red;
        }
    </style>
</head>
<body>
    <ul>
        <li></li>
        <li></li>
        <li id="three"></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
    <ol>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ol>
</body>
</html>
```

### 05.基础选择器的优先级
##### 01）样式来源：
默认样式
继承的
通配符 *  匹配所有元素
标签名选择器
类名选择器
id名选择器
行内书写
!important
##### 02）多个样式来源的优先级确定
!important > 行内书写 > id > 类 > 标签名 > 通配符 > 默认样式 > 继承 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>优先级</title>
    <style>
        *{
            margin: 0;
            /*  *>默认样式  */
            color: pink;
        }
        p{
            margin: 10px;
            /*标签名选择器 >  通配符**/

            /*!important书写在某个样式的后边
            这条样式无论写在哪一个选择器中，这条样式永远优先级最大*/
            margin: 100px !important;

            /*color: green;*/
        }

        .con{
            margin: 20px;
            /*类名选择器>标签名选择器*/
        }
        #box{
            margin: 30px;
            /*id选择器>类名选择器*/

            /*行内书写>id选择器*/
        }

        div{
            color: red;
            font-style: normal;
        }
    </style>
</head>
<body>
    <div>
        我是div
        <p id="box" class="con" style="margin: 50px;">我是p标签</p>
        <i>hellow</i>
    </div>
</body>
</html>
```

## 三、css的复杂选择器
### 01.后代选择器：
>后代选择器使用 空格间隔开   （A B：在A元素中寻找后代（不一定是儿子）是B的元素）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>层次选择器</title>
    <style>
       /* .box li{
            background-color: red;
        }*/
        div li{
            background-color: pink;
        }
        .show{}
        .box .show{}
        .outer .show{}
        html body div .show{}
    </style>
</head>
<body>
    <div class="outer">
        <p>p1</p>
        <p>p2</p>
        <span>span1</span>
        <ul class="box">
            <li>111</li>
            <li class="show">222</li>
        </ul>
        <ol>
            <li>333</li>
            <li>444</li>
        </ol>
    </div>

</body>
</html>
```
### 02.子代选择器：
>子代选择器使用 > 间隔开   （A>B：在A元素中寻找儿子辈元素 是B的元素）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>子代选择器</title>
    <style>
        .box>.show{
            background-color: red;
        }
    </style>
</head>
<body>
    <div class="outer">
        <p>p1</p>
        <p>p2</p>
        <span>span1</span>
        <ul class="box">
            <li>111</li>
            <li class="show">222</li>
            <li>
                <span class="show"></span>
            </li>
        </ul>
        <ol>
            <li>333</li>
            <li class="show">444</li>
        </ol>
    </div>

</body>
</html>
```
### 03.相邻兄弟选择器：
>相邻兄弟选择器使用 + 间隔开   （A+B：在A元素的下边紧贴着A的元素 并且是B  才能被选中）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>相邻兄弟选择器</title>
    <style>
        .outer>.show+span{
            background-color: yellow;
        }
        .outer>.show+p{
            /*选不中状态*/
            background-color: blue;
        }
    </style>
</head>
<body>
    <div class="outer">
        <p>p1</p>
        <p class="show">p2</p>
        <span>span1</span>
        <p>p3</p>
        <span>span2</span>
    </div>
</body>
</html>
```
### 04.通用兄弟选择器：
>相邻兄弟选择器使用 ~ 间隔开   （A~B：在A元素的下边兄弟元素 并且是B  就能被选中）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>通用兄弟选择器</title>
    <style>
        .outer>.show~span{
            background-color: yellow;
        }
    </style>
</head>
<body>
    <div class="outer">
        <span>span0</span>
        <p>p1</p>
        <p class="show">p2</p>
        <span>span1</span>
        <p>p3</p>
        <span>span2</span>
    </div>
</body>
</html>
```
### 05.群组选择器：
>1)将多个选择器使用 ， 隔开  可以同时对多个选择器设置样式
>2)如果多个元素有相同的样式，方法有两种
    1、使用一个共同的类名
    2、使用群组选择器
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>群组选择器</title>
    <style>
        /*.con{
            width: 100px;
            height: 100px;
        }*/
        .con1,.con2,.con3,.con4{
            width: 100px;
            height: 100px;
        }
        .con1{

            background-color: red;
        }
        .con2{

            background-color: #c0ff8b;
        }
        .con3{

            background-color: #5e8fff;
        }
        .con4{

            background-color: #ff2a91;
        }

    </style>
</head>
<body>
<ul>
    <li class="con1 con"></li>
    <li class="con2 con"></li>
    <li class="con3 con"></li>
    <li class="con4 con"></li>
</ul>
</body>
</html>
```
### 06.选择器的优先级
#### 01）相同优先级的选择器生效方式
>当优先级相同的时候，在后边书写的样式优先级高
>link其实也是把样式关联上，选择器优先级相同的情况写，后写的生效
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选择器的优先级</title>

    <style>
        .box{
            width: 100px;
            height: 100px;
            background-color: pink;
        }
        .con{
            width: 100px;
            height: 100px;
            background-color: green;
        }
    </style>
    <link rel="stylesheet" href="./01.css">
</head>
<body>
    <!--
        相同优先级的选择器生效方式：
            当优先级相同的时候，在后边书写的样式优先级高
            link其实也是把样式关联上，选择器优先级相同的情况写，后写的生效
    -->
    <div class="box con show">
        box
    </div>
</body>
</html>
```
#### 02）选择器优先级的权重计算：
行内样式： 1000
id：100
类：10
标签名：1

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选择器优先级2</title>
    <style>
        #box p{
            /*1 --101*/
            background-color: red;
        }
        #box .con p{
            /*2 -- 111*/
            background-color: pink;
        }
        .box #con p{
            /*3--111*/
            background-color: green;
        }
        .box .show p{
            /*4--21*/
            background-color: yellow;
        }
        .box .con .show p{
            /*5 -- 31*/
            background-color: grey;
        }
        #box .show p {
            /*6 --111*/
            background-color: purple;
        }
        #box #con .show p{
            /*7 -- 211*/
            background-color: #5ab3f4;
        }
        #box #con #show p{
            /*8  -- 301*/
            background-color: #5df2ff;
        }
    </style>
</head>
<body>
<div id="box" class="box">
    <div id="con" class="con">
        <div class="show" id="show">
            <p>我是一个p标签</p>
        </div>
    </div>
</div>
</body>
</html>
```
#### 02）选择器优先级覆盖案例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>优先级覆盖案例</title>
    <style>
        .outer li{
            width: 100px;
            height: 100px;
            margin: 10px;
            background-color: grey;
            float: left;
        }

        .outer .active{
            background-color: red;
        }
    </style>
</head>
<body>
    <ul class="outer">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <!-- 将来使用js，哪一个li拥有样式，就给它active的类名 -->
        <li class="active"></li>
        <li></li>
    </ul>
</body>
</html>
```

## 四、css的高级选择器
### 01）属性选择器
>属性选择器：
    **ELE[attr]**:元素拥有attr属性 就会被选择
    **ELE[attr=val]**:元素拥有attr属性 并且属性值为val  才会被选择
    **ELE[attr^=val]**:元素拥有attr属性 并且属性值以val为开头的  才会被选择
    **ELE[attr$=val]**:元素拥有attr属性 并且属性值以val为结尾的  才会被选择
    **ELE[attr\*=val]**:元素拥有attr属性 并且属性值包含val的  才会被选择

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>属性选择器</title>
    <style>
        ul li[name]{}
        ul li[name=laowang]{}
        ul li[name^=xiao]{}
        ul li[name$=wang]{}
        ul li[name*=ao]{}


        form input[type=button]{
            background-color: red;
        }
    </style>
</head>
<body>
<ul>
    <li name="xiaowang"></li>
    <li></li>
    <li name="laowang"></li>
    <li></li>
    <li name="xiaozhang"></li>
    <li></li>
    <li name="ao"></li>
    <li></li>
    <li name="laowang"></li>
</ul>
<form action="###">
    <input type="text">
    <input type="password">
    <input type="button">
</form>
</body>
</html>
```
### 02.伪类选择器
#### 01)什么是伪类选择器
**伪类选择器存在的意义是为了通过选择器，格式化DOM树以外的信息,以及不能被常规选择器获取到的信息**
>1、a标签的4种状态（被访问前，被访问后，鼠标激活，鼠标悬浮），不存在于DOM树中
>2、不能被常规获取，想要获得第一个子元素，无法通过常规的css选择器获取，只能通过伪类选择器来获取

#### 02)表单伪类选择器
**:read-only** 选取不可被用户编辑的可输入表单
**:read-write** 选取可以被用户编辑的表单元素
**:checked**   选取任何被选中的单选和多选框
**:disabled**  选取被禁用的表单元素
**:enabled**    选取未被禁用的表单元素
**:focus**      选取获取焦点的表单元素

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表单伪类选择器</title>
    <style>
        input:read-only{
            background-color: yellow;
        }
        /*目前这个选择器在火狐还是私有的，所以需要添加火狐前缀*/
        input:-moz-read-only{
            background-color: yellow;
        }

        input:read-write{
            background-color: green;
        }
        input:-moz-read-write{
            background-color: green;
        }

        /*单选框多选框默认不能设置背景和背景颜色*/
        input[type=checkbox]{
            background-color: red;
        }

        input[type=checkbox]:checked+label{
            color: red;
        }

        input:disabled{
            background-color: #0D1635;
        }

        input:enabled{
            width: 300px;
            height: 60px;
        }

        input:focus{
            background-color: pink;
        }
    </style>
</head>
<body>
<form action="###">
    请输入用户名：
    <input type="text" readonly value="请输入啊">
    请输入姓名：
    <input type="text">
    请输入密码：
    <input type="password">
    请输入电话号码：
    <input type="tel" disabled>

    请选择你喜欢的水果：
    <input type="checkbox" id="foods1" name="foods">
    <label for="foods1">苹果</label>
    <input type="checkbox" id="foods2"name="foods">
    <label for="foods2">梨</label>
    <input type="checkbox" id="foods3"name="foods">
    <label for="foods3">香蕉</label>
</form>
</body>
</html>
```
#### 03)结构伪类选择器
**:first-child**选取一组兄弟元素中的第一个元素
                在选择器模块的level4版本中，前边可以不添加元素，代表通配符所有
                比如 ul:first-child(选择ul中后代元素中 是第一个的)

**:first-of-type**  选取一组元素中，同类型的的第一个元素

**:last-child**     选取一组兄弟元素中的第最后一个元素

**:last-of-type**   选取一组元素中，同类型的的最后一个元素

**:nth-child(an+b)** 先找到当前元素的所有兄弟元素，然后按照顺序依次从0开始排序，被选择到的结果就是符合小括号中的值
        2n+1 奇数
        2n   偶数
        odd  奇数
        even 偶数
        num  直接写数字
        -n+3  选取前3个

**:nth-last-child(an+b)**:在所有的兄弟节点中由后向前匹配 其他和nth-child一样

**:nth-of-type(an+b)**:先找到当前元素的所有同类型兄弟元素，然后按照顺序依次从0开始排序，被选择到的结果就是符合小括号中的值

**:nth-last-of-type(an+b)**:在所有的同类型的兄弟节点中由后向前匹配 其他和nth-of-type一样

**:only-child**     匹配没有任何兄弟元素的元素

**:only-of-type**    代表一个元素没有同类型的兄弟元素

**:not(X)** X是一个选择器  选择所有元素中 排除X所代表元素的元素,这个not伪类 它的权重计算完全是看X的权重

**:empty**  选取没有子元素的元素 子元素包括元素和文本（空格和回车都包含）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>结构的伪类选择器</title>
    <style>
        /*.box li:first-child{
            background-color: red;
        }*/
        /*.box :first-child{
            background-color: pink;
        }*/
       /* .box span:first-child{
            background-color: red;
        }*/
        /*.box span:first-of-type{
            background-color: red;
        }*/
       /* .box li:last-child{
            background-color: pink;
        }*/
        /*.box span:last-of-type{
            background-color: red;
        }*/


        /*.box li:nth-child(2){
            background-color: pink;
        }*/
       /* .box li:nth-child(2n+1){
            background-color: pink;
        }*/
        /*.box li:nth-child(2n){
            background-color: pink;
        }*/

        /*.box li:nth-child(-n+3){
            background-color: red;
        }*/
        /*.box li:nth-last-child(-n+3){
            background-color: red;
        }*/

        /*.box span:nth-child(2){
            background-color: pink;
        }*/

       /* .box span:nth-of-type(2n+1){
            background-color: red;
        }*/
        /*.box span:nth-last-of-type(1){
            background-color: red;
        }*/

       /* ul li:only-child{
            background-color: pink;
        }
        .box :only-of-type{
            background-color: pink;
        }*/
        /*.box :not(em){
            background-color: red;
        }*/
        .box li:empty{
            background-color: red;
        }
    </style>
</head>
<body>
    <ul class="box">
        <li>11</li>
        <li>22</li>
        <li>33</li>
        <li>44</li>
        <li>55</li>
        <li>

        </li>
        <li>66</li>
    </ul>
    <ul class="box">
        <li>77</li>
        <li>88</li>
        <li>99</li>
        <li>aa</li>
        <li>bb</li>
        <li>cc</li>
    </ul>

    <div class="box">
        <p>p1</p>
        <span>span2</span>
        <p>p2</p>
        <span>span1</span>
        <em>em</em>
        <p>p3</p>
        <span>span3</span>
        <p>p4</p>
    </div>

    <ul>
        <li></li>
    </ul>
</body>
</html>
```
## 五、css的基础样式设置
### 01.文本颜色的设置（color）
color: 设置文字颜色（可以继承的）
>1、**可以直接设置颜色的名字**（开发中很少使用，因为不精确）
    red green yellow pink blue grey purple orange lightblue lightgreen greenyellow  yellowgreen

>2、**设置为三原色**  红r  绿g  蓝b
    所有颜色都是由这三种颜色调制出来的
    每一个颜色的值都是 0-255之间
    rgb(30,120,200)
    颜色还可以设置不透明度 ,可以使用 rgba(20,111,111,.7)

>3、颜色还可以设置为**十六进制**（不能设置透明度）
    #加上16进制的颜色值  6位
    #112233--> 11代表red的十六进制值  22代表green颜色的十六进制值  33代表blue颜色十六进制值
    十六进制颜色提供简写：当12位一样并且34位一样并且56一样的时候 可以每一位简写一个
    #112233-->#123
    #aabb11-->#ab1
    #000000-->#000
    #111222-->#111222

>4、**HSL**设置颜色
    H代表Hue 色调 0和360代表红色  范围是[0,360] 120代表绿色 240代表蓝色
    S代表Saturation 饱和度  0-100%
    L代表Lightness 亮度 0-100%

    HSLA() 中 hsl代表的意思不变  a代表透明度  [1,0]

>5、**继承 inherit**

>6、**透明颜色**：transparent
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .outer{
            color: red;
            color: rgb(30,120,200);
            color: rgba(20,111,111,.7);
            color: #ae43ea;
            color: hsl(0,100%,50%);
            color: hsla(0,100%,50%,.3);
        }
    </style>
</head>
<body>
    <div class="outer">
        今天天气真好
        <span>对，真的好</span>
    </div>
</body>
</html>

```
### 02.关于a标签颜色的继承
>01).a标签比较特殊，如果a标签没有href属性，a标签没有默认样式，那么继承颜色生效
>02).但是如果a标签拥有href属性，a标签链接的自带样色会盖过继承
   a的4个状态（有链接、被点击后、点击中、鼠标悬浮）是有自己的样式的，只能通过伪类来控制这4中样式
>03).所以在开发中给a标签设置颜色，需要直接对a标签进行设置
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>关于a标签颜色的继承</title>
    <style>
        .box{
            color: red;
        }
    </style>
</head>
<body>
    <div class="box">
        哈哈哈哈
        <a>笑个鸡哦</a>
    </div>
</body>
</html>
```
### 03.font-famliy：设置字体(可以继承)
>1、常见中文字体："Microsoft YaHei"、"SimHei"、"SimSun"

>2、但是我们设置的字体用户可能没有，我们需要设置备用字体
    在font-famliy后书写多个字体，使用逗号隔开，浏览器会依次检测支持为止，否则将执行默认字体

>3、目前常用的字体可以分为5大类
    serif：衬线字体族  衬线指的是字母结构笔画之外的装饰性笔画 宋体
    sans-serif：无衬线字体族 黑题
    cursive:手写体族 楷体
    monospace：等宽字体族  中易宋体 幼圆
    fantasy：梦幻字体族
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>font-famliy</title>
    <style>
        .box{
            font-family: "Microsoft YaHei";
            font-family: "SimSun";
            font-family: "SimHei";
            font-family: "SimHei","SimSun","Microsoft YaHei";


            /*字体的五大类*/
            font-family: Serif;
            font-family: sans-serif;
            font-family: cursive;
            font-family: Monospace;
            font-family: fantasy;
        }
    </style>
</head>
<body>
    <div class="box">
        哈哈哈哈
        <span>笑个鬼</span>
    </div>
</body>
</html>
```
### 04.外部引入字体包
>1、外部引入的字体包和某一个元素没有任何关系，而是本页面都可以使用这个字体
>2、 原来我们页面自带的字体包都有自己的名字，我们首先给引进来的字体包起一个名字
>3、在css中使用@font-face来引入外部字体包
    font-face中有一个font-famliy属性 是给字体包起名字的
    还要使用src：url（）来引入字体包
>4、根据你起得名字，来使用字体包
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>外部引入字体包</title>
    <style>
        @font-face {
            font-family: "jier";
            src:url("../images/abc.ttf");
        }
        .outer{
            font-family: "jier";
        }
    </style>
</head>
<body>
    <div class="outer">
        看我的表演 我是非主流子
    </div>
</body>
</html>
```
### 05.font-size
>1、常用的单位是px、em、rem  当然也有不用的 cm in等等
>2、可以设置小数（低版本ie不支持）
>3、字号最好不要设置为奇数
>4、一般来说汉字是正方形的，宽高就等于字号大小
>5、但是实际文字占用的高度要大于字号大小，根据字体的不同，文字上下有一定的不能控制的间隙
    因为文字的大小是基于4线格的（顶线 中线 基线 底线） 汉字并不能完整的填充满四线格
>6、浏览器都有自己的默认字号大小和最小字号
    谷歌浏览器默认字号大小是16px
    谷歌浏览器支持的最小字号 多数是12px
    如果设置12以下，字体不支持
    但是如果设置字号为0 那么文字高度为0  消失
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>字号设置</title>
    <style>
        .box{
            font-size: 30px;

            font-family: "Microsoft YaHei";

            font-family: "SimSun";

            font-family: "SimHei";
        }
    </style>
</head>
<body>
    <div class="box">
        哈哈哈哈哈
        <span>我也哈哈gj哈</span>
    </div>
</body>
</html>
```
### 06.字体风格：font-style（可以继承）
>1、normal：正常
    多数元素的默认值
    对于默认倾斜或斜体的元素  i   var  em 可以调整成正常非倾斜样式

>2、italic 让元素呈现斜体  一般指的是一个字体
    在字体设计的过程中，会对一个文字设计 正常体  斜体 粗体 等状态
    而italic只是选择让使用斜体显示

>3、oblique 让常规字体进行倾斜（强行让当前文字变倾斜）
    oblique 后可以跟一个旋转角度  以deg为单位
    谷歌只支持0deg
    火狐只支持汉字和-90  -90度的设置

> 4、对于上边两种倾斜版本，使用上没有什么区别（italic会占用高度较小）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>字体风格</title>
    <style>
        em,i,var{
            font-style: normal;
        }
        .outer{
            font-style: italic;
            font-style: oblique 0deg;
        }
    </style>
</head>
<body>
    <div>
        <em>em啊</em>
        <i>i啊</i>
        <var>哈哈哈啊</var>
    </div>
    <div class="outer">
        outer中
        <span>span里</span>
    </div>
</body>
</html>
```
### 07.font-weight:(继承)
>用来定义字体的粗细 其实目前浏览器只支持3个级别  细 正常 粗
>normal：正常粗细  可以将默认加粗的字体进行改变为正常 比如 b strong

>bold：加粗

>bolder:相对父级来说的，比父级要粗一个级别

>lighter：相对父级来说，比父级细一个级别

>100-900 整除100的整数：
    因为浏览器只支持 细 粗 正常3个 所以
    100-300 是细
    400-500 正常
    600-900 加粗
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>font-weight 字体粗细</title>
    <style>
        .outer b,.outer strong{
            font-weight: normal;
        }
        .box{
            font-weight: bold;
        }
        .box span{
            font-weight: lighter;
        }
        .box span em{
            /*font-weight: lighter;*/
            font-weight: bolder;
        }

        .con{
            font-weight: 100;
        }

    </style>
</head>
<body>
    <div class="outer">
        <b>我是小b</b>
        <strong>我是小s</strong>
    </div>
    <div class="box">
        我是一个box
        <span>我是一个span <em>我是em</em></span>
    </div>
    <div class="con">
        我是con
    </div>
</body>
</html>
```
### 07.font合写：
>font-style  font-weight font-size/line-height  font-famliy

>font合写必须要书写 font-size 和font-famliy  否则合写不生效

>font合写其实在实际项目中使用的很少，一般我们要分开设置

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>font合写</title>
    <style>
        .font{
            line-height: 1.8;
            font:italic bold 40px "Microsoft YaHei";
        }
    </style>
</head>
<body>
<div class="font">
    看我的合写 你记不记得住
</div>
</body>
</html>
```
### 08.字母x和css的基线、四线格
>x在css中扮演了极其重要的角色
>在垂直方向排版的或对齐的，都离不开基线（baseline）的支持
基线分为多种，比如 字母基线，悬挂基线 表意基线等等
在英文中，字母x的下边缘就是我们的基线
x-height就是代表基线和等分线（中线）的距离

### 09.line-height：(继承)
>1、用来控制行高，一行文的高度。规范来说就是两行文字基线之间的距离

>2、line-height和内联元素连接非常紧密，行高直接决定了内联元素占用的高度（不包括替换元素）

>3：值：(不支持负值)
    ·normal：执行浏览器默认值，在各个浏览器中不同，并且还受字体的影响
    ·数字：没有单位，比如1.5  就是当前元素文字大小的1.5倍
    ·百分比：也是相对于当前元素的文字大小计算的，很少使用
    ·长度：带单位，直接设置行高

>4、行距与半行距
    行距是 上边一行文字的底线和下边一行文字的顶线之间的距离
    半行距  就是行距的一半; 让行高减去一行文字的高度，得到的值除以2，就是半行距
    一行文字的上边和下边分别是两个半行距
    半行距高度*2 + 文字的字号  = 行高

>5、使用line-height对单行文字（也可以是内联元素）做垂直居中

>6、em方框：对于一个字，用户代理先生成一个方框（即em框），这个框有底线，基线，中线和顶线四个构成
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>line-height</title>
    <style>
        .con1{
            width: 200px;
            background-color: red;
            color: #fff;

            /*line-height: 1.8;*/
            /*line-height: 100%;*/
            /*line-height: 16px;*/
        }

        .con2{
            background-color: red;
            line-height: normal;
        }

        .con3_outer{
            background-color: red;
            line-height: 16px;
        }
    </style>
</head>
<body>

    <p class="con1">
        用来控制行高，一行文的高度。规范来说就是两行文字基线之间的距离用来控制行高，一行文的高度。规范来说就是两行文字基线之间的距离用来控制行高，一行文的高度。规范来说就是两行文字基线之间的距离用来控制行高，一行文的高度。规范来说就是两行文字基线之间的距离用来控制行高，一行文的高度。规范来说就是两行文字基线之间的距离用来控制行高，一行文的高度。规范来说就是两行文字基线之间的距离用来控制行高，一行文的高度。规范来说就是两行文字基线之间的距离
    </p>
    <div>
        <span class="con2">我是一个spanpan</span>
    </div>
    <br>
    <div class="con3_outer">
        <span class="con3">看我居中</span>
    </div>

</body>
</html>
```
### 10.单行文字做垂直居中
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>单行文字做垂直居中</title>
    <style>
        .box{
            /*line-height的设置 可以让元素在line-height的值里边垂直居中，不一定非要设置高度*/
            background-color: red;
            /*height: 100px;*/
            line-height: 100px;
        }

        .con{
            background-color: pink;
            line-height: 100px;
            /*span在con中垂直居中，主要是看父元素的line-height*/
        }
        .con span{
            line-height: normal;
        }
    </style>
</head>
<body>
    <div class="box">
        今天天气知道你好
    </div>


    <div class="con">
        <span>你好</span>
    </div>
</body>
</html>
```
### 11.line-height的继承
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>line-height的继承</title>
    <style>
        .nav>li{
            width: 200px;
            height: 60px;
            line-height: 60px;
            background-color: red;
            position: relative;
        }
        .con{
            position: absolute;
            top: 60px;
            left: 0;
            background-color: pink;
            line-height: 20px;
            display: none;
        }
        .nav>li:hover .con{
            display: block;
        }
    </style>
</head>
<body>
    <ul class="nav">
       <li>
           今日头条
           <ul class="con">
                <li>头条1</li>
                <li>头条2</li>
                <li>头条3</li>
                <li>头条4</li>
                <li>头条5</li>
                <li>头条6</li>
           </ul>
       </li>
    </ul>
</body>
</html>
```
### 12.em方框和行内框
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        span{
            line-height: 40px;
            vertical-align: baseline;
        }
        em{
            line-height: 60px;
            vertical-align: baseline;
        }
        var{
            line-height: 80px;
            vertical-align: baseline;
        }
    </style>
</head>
<body>
<div>
    <span>span1</span>
    <em>em1</em>
    <var>var1</var>
</div>
</body>
</html>
```
### 13.vertical-align:
>1、默认情况下，在一个行框中，所有内容都是基线对齐
>2、但是图片没有基线，所以就把图片的底部当成了基线对了
>3、vertical-align 可以设置让一个元素以自身的哪一个位置对齐

>值：
    1、baseline 基线对齐
    2、top  让元素顶部与整行的顶部对齐
    3、bottom 让元素底部与整行的底部对齐
    4.middle 让元素的中间在行框的x-height中间对齐
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>06.vertical-align</title>
    <style>
        .box{
            background-color: red;
            font-size: 100px;
            height: 400px;

        }
        .box img{
            height: 50px;
            vertical-align: baseline;
            vertical-align: top;
            vertical-align: bottom;
            vertical-align: middle;
            vertical-align: text-top;

        }
    </style>
</head>
<body>
    <div class="box">
        <img src="../images/05.jpg" alt="">
        <span>hehehe</span>
        哈
    </div>
</body>
</html>
```
### 14.多行元素的水平垂直居中
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>多行文字居中</title>
    <style>
        .outer{
            width: 200px;
            background-color: green;
            /*color: #fff;*/
            height: 400px;
            line-height: 400px;
        }
        .outer span{
            /*对于span换行来说，设置display为inline-block 再设置vertical-align:middle，垂直居中才生效*/
            line-height: 1.2;
            display: inline-block;/*将元素设置为行内块*/
            vertical-align: middle;/*让元素自身的中线进行lineheight对齐*/
        }
    </style>
</head>
<body>
    <div class="outer">
        <span>今天天气真好啊 假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了今天天气真好啊 明天就放假了</span>
    </div>
</body>
</html>
```
### 15.让图片在父级垂直居中
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>让图片在父级垂直居中</title>
    <style>
        .box{
            height: 500px;
            background-color: red;
            line-height: 500px;
        }
        .box img{
            height: 200px;
            vertical-align: middle;

        }
    </style>
</head>
<body>
<div class="box">
    <img src="../images/05.jpg" alt="">
</div>
</body>
</html>
```
### 16.去除图片默认间隙
>1、因为图片底部默认和行框的文字基线对齐，所以图片和行框底部有一定的间隙
>2、就算行框只有一个图片，间隙也存在。是因为在当前行框内，如果存在一个行内块元素的时候，就会渲染一个看不见摸不着的节点
    这个节点拥有当前元素的字号大小，行高等信息。这个节点被称作为“幽灵空白节点”

>3、去除间隙：
    1、  display:block;
        图片底部能够和文字的基线对齐，是因为图片默认的vertical-align为baseline
        但是verticle-align这个属性只有行内元素和行内块元素支持，块级元素是失效的
        所以将img设置为块元素属性 就可以不用基线对齐了
        也可以理解为：因为改成块，解决了幽灵空白节点的问题
                        并且没有元素和他在个行框

    2、设置verticle-align不为baseline 比如 top bottom middle都可以


    3、空白是文字有字号大小，撑开了当前的em方框
        直接让字号大小变成0   文字就没有大小了  也就是幽灵空白节点文字大小变成0了  也不会撑开间隙了
        主要针对于没有文字的行框
    
    4、改变文字的高度  文字的高度可以由line-height来控制
        让line-height：0 也可以解决问题
        
    5、浮动
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>06.vertical-align</title>
    <style>
        .box{
            background-color: red;
            /*font-size: 0px;*/
            /*line-height: 0;*/

        }
        .box span{
            font-size: 50px;
        }
        .box img{
            height: 150px;

            /*display: block;*/

            /*vertical-align: middle;
            vertical-align: top;
            vertical-align: bottom;*/

            float: left;
        }
    </style>
</head>
<body>
    <div class="box">
        <img src="../images/05.jpg" alt="">
        <span>hahahagh</span>

    </div>

<div>
    <span></span>
</div>
</body>
</html>
```
### 17.text-decoration：文本修饰（不继承）
>虽然不继承，但是延伸到后代元素，因为后代元素属于这个元素的下划线范围

none：取消下划线
underline:下划线
overline:上划线
line-through：删除线

text-decoration其实是一个简写的属性。
    text-decoration-line：上划线 下划线 删除线
    text-decoration-color：颜色
    text-decoration-style：实线solid  虚线dashed 点线dotted 波浪线wavy

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>text-decoration</title>
    <style>
        a,u{
            text-decoration: none;
        }
        .outer{
            text-decoration: underline;
            /*text-decoration: overline;*/
            /*text-decoration: line-through;*/
        }
        .outer span{
            text-decoration: overline red wavy;

        }
    </style>
</head>
<body>
    <div>
        <a href="###">a</a>
        <u>u</u>
    </div>
    <div class="outer">
        <span>你好</span>
        世界
    </div>
</body>
</html>
```
### 18.text-indent首行文本缩进
1、单位是px  缩进的像素  固定的单位，字号大小改变 还需要重新书写px

2、em单位  em是一个相对单位，1em=当前文字的字号大小  如果缩进两个文字 那么2em

3、只针对块级元素生效

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>10.text-indent首行文本缩进</title>
    <style>
        p{
            width: 200px;
            background-color: yellow;
            font-size:16px;
            /*text-indent: 32px;*/
            text-indent: 2em;
        }
        span{
            text-indent: 2em;
        }
    </style>
</head>
<body>
    <p>
        今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好
        <br>
        <span>
            真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊真的好呀啊
        </span>
    </p>
</body>
</html>
```
### 19.text-align:(继承)
1、规定行内的内容如何相对于它的块级父元素水平方向对齐
2、并不是控制元素自己的对齐，只是控制它里边的行内容水平方向对齐
3、
    left：默认 左对齐
    center：居中
    right：右对齐

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>文本对齐</title>
    <style>
        .outer{
            width: 600px;
            height: 200px;
            background-color: red;
            text-align: center;
        }
        .con{
            width: 300px;
            height: 100px;
            background-color: yellow;

            text-align: center;
            text-align: right;
            line-height: 100px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="con">
            hello world <span>span</span>
        </div>
    </div>
</body>
</html>
```
### 20.text-align:justify;
        两端对齐只针对于英文等字母语言 其他语言无效
        英文在一行书写的时候，最后位置可能放不下一整个单词，那么整体的单词就会换行
        导致每一行文本末尾参差不齐，所以需要两端对齐
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>文本对齐</title>
    <style>
        .outer{
            width: 600px;
            height: 200px;
            background-color: red;
            /*text-align: center;*/
        }
        .con{
            width: 300px;
            background-color: yellow;
            text-align: justify;

        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="con">
            hello world span sadkas asasdasfasf asd de dasdasf hello world span sadkas asasdasfasf asd de dasdasf hello world span sadkas asasdasfasf asd de dasdasf hello world span sadkas asasdasfasf asd de dasdasf
        </div>
    </div>
</body>
</html>
```
### 21.字符和词间距：
1、在html中，英文数字的组合 只要没有空格都会被当做是一个单词
    在汉字中，虽然不会把多个汉字连在一起当做是一个单词
    但是仍然词间距的时候 ，只改变空格隔开的间距
2、letter-spacing:控制字符间距
3、word-spacing:控制词间距

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>字符和词间距</title>
    <style>
        .show{
            /*width: 100px;*/
            background-color: red;
            letter-spacing: 0px;
            word-spacing: 0px;

        }
    </style>
</head>
<body>
    <div class="show">
        how are you i'm fine thank you
        <br>
        今天天气 真的好
    </div>
</body>
</html>
```
### 22.背景类的设置：
背景颜色设置：
    background-color:颜色值（和color的颜色一致 十六进制 rgba hsl 颜色单词）
背景图的设置：
    background-image:url(路径) 背景图引入后 默认原点在元素的左上角
    在html中，由左至右 是x轴方向    由上至下 是y轴方向  x和y的交叉是原点
背景图定位：
    background-position：x轴方向位置  y轴方向位置
        值的写法：
            1、px
            2、百分比  百分比是参照于 容器的总宽度-图片的总宽度
            3、其他写法
                x：center left right
                y: center top  bottom
    background-repeat:控制背景图片是否平铺
        no-repeat：不平铺
        repeat：x和y都平铺（默认）
        repeat-x：只有x轴平铺
        repeat-y：只有y轴平铺

背景图提供了合写（一般我们都使用合写）
    background：color image position repeat；
    都可以进行省略

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>背景类的设置</title>
    <style>
        .box{
            width: 1000px;
            height: 600px;
            /*background-color: #5df2ff;
            background-image: url(../images/05.jpg);

            background-position: 50px 50px;
            background-position: 50% 50%;
            background-position: right 50%;


            background-repeat: no-repeat;
            background-repeat: repeat-x;
            background-repeat: repeat-y;*/

            /*background: #5df2ff url("../images/05.jpg") center center no-repeat;*/

            /*background-color: red;
            background: url("../images/05.jpg") center center no-repeat;*/
        }
    </style>
</head>
<body>
    <div class="box">
        我是一个box元素
    </div>
</body>
</html>
```
### 23.overflow属性
1、元素超出父级，不会影响父级的兄弟元素位置
2、overflow属性定义一个内容太大无法适应容器的时候应该怎么做
3、  设置给被超出的元素
    visible：默认，内容不会被修剪，而是显示在元素的框外
    hidden:超出内容被修剪，修剪掉的内容不可见，并且没有滚动条
    scroll：超出内容被修剪，浏览器显示滚动条方便查看被修剪的内容
    auto：浏览器定夺，如果内容超出就生成滚动掉，否则不生成

4、overflow：auto和scroll的区别：
    auto:是自动生成滚动条，不超出不生成 超出才生成
    scroll：无论是否超出都会生成滚动条

5、overflow-x：
    overflow-y：
    只控制x和y的超出情况

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>overflow属性</title>
    <style>
        .outer{
            width: 200px;
            height: 100px;
            background-color: red;

            /*overflow: visible;
            overflow: hidden;
            overflow: scroll;
            overflow: auto;*/
            overflow-x: hidden;
            overflow-y: hidden;
        }
        .con{
            width: 400px;
            height: 200px;
            background-color: pink;
        }
        .bottom{
            height: 400px;
            background-color: green;
        }
    </style>
</head>
<body>

    <div class="outer">
        <div class="con">
            今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好今天天气真好
        </div>
    </div>
    <div class="bottom">

    </div>
</body>
</html>
```
### 24.visibility属性：
控制元素显示或者隐藏

hidden:控制元素隐藏
    1、保留原来的位置，其他元素的布局没有发生改变
    2、相当于此元素变透明
    3、visibility属性是继承的，里边的子元素也全部都继承属性，并且隐藏了
    4、如果给子元素设置visible覆盖，那么子元素可以进行显示

visible：让visibility：hidden隐藏的元素显示
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>visibility属性</title>
    <style>
        .box{
            width: 600px;
            height: 400px;
            background: yellow;
        }
        .con1{
            width: 300px;
            height: 100px;
            background-color: pink;
            visibility: hidden;
        }
        .con1 .inner{
            width: 100px;
            height: 50px;
            background-color: #5ab3f4;
            visibility: visible;
        }
        .con2{
            width: 300px;
            height: 100px;
            background-color: green;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="con1">
            <div class="inner"></div>
        </div>
        <div class="con2"></div>
    </div>
</body>
</html>
```
### 25.display属性：
指定了元素的显示类型，包含两种基础特征，用于规定元素生成什么样子的盒模型
    1、外部显示类型：定义元素怎么样参加流体布局
    2、内部显示类型：定义了元素内 子元素的布局方式

1、block：
    让元素以块标签属性显示（block-block）
2、inline
    让元素以行元素属性显示（inline-inline）
3、inline-block
    让元素以行内块的属性显示
    inline控制行内显示
    block控制可以设置宽高
4、none:
    让元素隐藏，包含子孙元素全部隐藏，并且不会占用任何位置，在DOM也访问不到可视化宽高（就算设置了宽高，使用js的offsetWidth和offsetHeight都获取不到宽高）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>display属性</title>
    <style>
        .con1{
            display: block;
            width: 400px;
            height: 100px;
            background-color: pink;
        }
        .con3{
            display: inline;
            width: 100px;
            height: 100px;
            background-color: red;

        }
        .con4{
            display: inline-block;
            width: 100px;
            height: 100px;
            background-color: #5df2ff;
        }
        .con5{
            display: none;
        }
    </style>
</head>
<body>
    <span class="con1">hello</span>
    <em class="con2">world</em>
    <div class="con3">那哈哈哈</div>
    <div class="con4">con44</div>
    <div class="con5">
        222
        <span>333</span>
    </div>

</body>
</html>
```
### 26.display和visibility隐藏的区别
1、visibility可以继承，子元素是因为继承了才隐藏
            可以覆盖继承，子元素即可显示
            display不能被继承，而是直接带着所有内部元素直接隐藏

2、visibility隐藏，原来空间仍然保留
    display隐藏，原来空间消失被占用

3、js可以获取到visibility隐藏元素的可视化宽高
    js不可以获取到display隐藏元素的可视化宽高
###  27.opacity透明度：
指定了一个元素的透明度
当opacity作用在某一个元素上的时候，把这个元素和里边的内容当成一个整体看待
即使里边的元素没有继承opacity。它也和父级有一样的透明度

opacity的取值是 1-0
    1代表完全不透明
    0代表完全透明

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>opacity透明度</title>
    <style>
        .box{
            width: 200px;
            height: 200px;
            background-color: deeppink;
            font-size: 30px;
            text-align: center;
            line-height: 200px;
            opacity: .6;
        }
    </style>
</head>
<body>
    <div class="box" id="box">
        <span>你好</span>
    </div>
    <script>
        var oBox = document.querySelector("#box");
        var timer = null;
        var i = 1;
        timer = setInterval(function () {
            i -= 0.01;
            oBox.style.opacity = i;
        },1000/60)
    </script>
</body>
</html>
```
### 28.opacity和rgba和hsla透明的区别：
1、rgba和hsla只是一个颜色，是属性的取值，比如color  background-color，所以只是对颜色的一个处理
2、opacity是一个属性，透明是直接设置给元素的，并不会对元素的某部分进行控制
f

## 六、盒子模型
### 01.盒子模型的概念：
1、在html中，把每一个元素都当做成一个盒子，拥有盒子的平面外形和空间
2、盒模型由内容（content）+内边距（padding）+边框（border）+外边距（margin）4部分构成

内容区域：你书写的内容或者子元素能够显示的区域
内边距：撑开内容与边框的距离
边框：元素的边框
外边距：撑开元素和其他元素之间的距离

### 02.盒子模型-内容区域（在标准盒子模型下）：
标准盒子模型下设置的width和height都是content（内容）区域的宽高

width：
    默认是auto。auto分为4种情况：
        1.fill-available：充分利用可使用空间（块标签）
        2.fit-content:收缩到合适（浮动，定位）
        3.min-content:收缩到最小（表格中常见）
        4.max-content:超出容器限制（英文单词较长，或者设置了不换行，就会超出容器限制）

height：
    auto：其高度由内部元素堆叠而成，也就是内部元素撑起来的

### 03.设置宽度的坑
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设置宽度的坑</title>
    <style>
        .box{
            /*假设一个元素 内容区域加上左右各50的margin  正好撑满父级
            以下设置是错误的*/
            width: 100%;/*把内容区域设置成了和父级一样宽 再加上margin 就超出父级了*/
            margin: 0 50px;
            height: 100px;
            background-color: red;

            /*解决以上问题很简单，不写width，或者设置width为auto*/
            width: auto;
        }
        input{
            /*input元素：
                占用的宽是200px 高是50px
                边框是1px
                padding是左右各10px

                    所以设置的宽度应该是 200-2-20=178
                */
            width:178px;
            height: 48px;
            padding: 0 10px;
            border: 1px solid #000;
        }
    </style>
</head>
<body>
    <!--

    -->
    <div class="box">
dd
    </div>
    <input type="text">
</body>
</html>
```
### 04.设置高度的坑
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设置高度的坑</title>
    <style>
        /*想让con元素和屏幕一样高*/
        /*想要让高度的百分比生效，需要给父级也要设置高度（不能是auto）*/
        html{
            height: 100%;
        }
        body{
            height: 100%;
        }
        .outer{
            height: 100%;
        }
        .con{
            height: 100%;
            background-color: red;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="con"></div>
    </div>
</body>
</html>
```
### 05.margin基础
设置一个元素外边距的宽度。外边距可以理解为当前元素与父级或其他兄弟级元素的距离。
值可以是一个单位，也可以是一个百分比

值是单位
    分4个方向
        margin-left、margin-right、margin-top、margin-bottom
        每个方向的值都可以单独的设置
        margin-left、margin-top是让自身元素靠右 靠下
        margin-bottom、margin-right是让其他元素 靠右  靠下

    margin的简写：
        margin后跟4个值： 分别代表  上 右  下  左
        margin后跟3个值： 分别代表  上   左右   下
        margin后跟2个值： 分别代表  上下     左右
            margin后跟1个值： 分别代表  上下左右
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>margin基础</title>
    <style>
        .con1,.con2{
            width: 200px;
            height: 200px;
        }
        .con1{
            background-color: #5df2ff;
            /*margin-left: 100px;
            margin-top: 80px;
            margin-right: 30px;
            margin-bottom: 40px;*/

            /*margin: 80px 30px 40px 100px;*/
            /*margin: 80px 50px 40px;*/
            margin: 80px 50px;
            margin: 50px;
        }
        .con2{
            background-color: yellow;
        }
    </style>
</head>
<body>
    <div class="con1"></div>
    <div class="con2"></div>
</body>
</html>
```
### 06.margin 0 auto居中:
在正常的布局中，块级元素具有满屏的属性，也就是在水平方向上占满父级的宽度
    满屏以后，内部元素的内容+内边距+边框+外边距 刚好是等于 父级的 内容区域的大小
    所以当水平方向上的 宽度 边框  内边距都是固定值的时候
    在水平方向上margin设置auto的时候，默认左右平分剩余空间，达到水平居中效果

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>margin 0 auto居中</title>
    <style>
        .outer{

        }
        header{
            width: 1000px;
            height: 100px;
            background-color: pink;
            margin: 0 auto;
            margin: 30px auto 50px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <header></header>
        <section></section>
        <footer></footer>
    </div>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>水平方向auto小练习</title>
    <style>
        .con{
            width: 400px;
            height: 100px;
            background-color: red;
            margin-left: auto;
            margin-right: 0;
        }
    </style>
</head>
<body>
    <!--
        水平方向auto小练习:
            当水平方向出现auto的时候，剩余空间会进行分配
             当右边不要  左边出现auto 剩余空间就会直接给左边
    -->

    <div class="con">

    </div>
</body>
</html>
```
### 07.垂直方向上的 margin ： auto 0 为什么不行
垂直方向上的 margin ： auto 0 为什么不行？
    相对于水平方向来说，块元素在垂直方向上并没有满屏的属性，margin默认在上下的值都是0
    无论是否设置垂直方向的auto，表现出来的都是元素多高就占用多少，并没有剩余空间去平分

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>margin 0 auto居中</title>
    <style>
        .outer{
            height: 400px;
            background-color: #b51d1a;
        }
        header{
            width: 1000px;
            height: 100px;
            background-color: pink;
            margin: auto 0;
        }
    </style>
</head>
<body>
    <div class="outer">
        <header></header>
    </div>
</body>
</html>
```
### 08.margin的父级塌陷：
当一个父级中 第一个元素的margin-top会塌陷给父级
    最后一个元素的margin-bottom会塌陷给父级

    防止父级和其他元素之间的间隙过大，当第一个和最后一个子元素的margn塌陷给父级以后
    父级就可以和兄弟元素在垂直方向上进行叠加
避免父级塌陷：
    1、给父级设置一个边框  边框的宽度不能为0
        防止影响视觉，可以设置透明（transparent）颜色
    2、开启BFC（块级格式化上下文）
        很多种方法，后边讲解
        overflow：hidden 可以开启 。。。。。。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>margin基础</title>
    <style>
        .con1,.con2{
            width: 200px;
            height: 200px;
        }
        .con1{
            background-color: #5df2ff;
            margin-top: 50px;
        }
        .con2{
            margin-top: 40px;
            background-color: yellow;
            margin-bottom: 40px;
        }
        .outer{
            background-color: pink;

            /*border:1px solid transparent;*/
            overflow: hidden;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="con1"></div>
        <div class="con2"></div>
    </div>

</body>
</html>
```
### 09.margin对元素的影响和支持性：（margin都为正值的时候）
对块标签来说：
    margin-left：元素右移动
    margin-top：元素下移动
    margin-right：如果右边有元素  后边的元素右移动
    margin-bottom：如果下边有元素  后边的元素下移动
    margin垂直方向叠加
    父级塌陷

对行标签：
    margin在垂直方向上不生效
    水平方向
        margin-left：元素右移动
        margin-right：如果右边有元素  后边的元素右移动

对行内块:
    上下左右全支持
    其他和块元素一样

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>margin对元素的影响和支持性</title>
    <style>
        .con2{
            margin: 40px;
        }
        .ipt{
            margin: 30px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="con1">div</div>
        <span class="con2">我是span1</span>
        <span class="con2">我是span1</span>
        <input type="text" class="ipt">
    </div>
</body>
</html>
```
### 10.负margin的基础用法：
margin-left为负：
    元素向左移动，并且原来的位置不保留（后边元素会紧跟上一起移动），
    元素向左移动，并不会挤到前边的兄弟元素，而是覆盖前边的兄弟元素
margin-right为负：
    元素视觉大小不发生变化
    但是元素实际所占用的空间变小，后边元素会跟上来 或者是撑不开父级宽度
    假如元素width为100px  设置marginright为-20  元素实际大小是80px
margin-top为负：
    元素向上移动，并且原来的位置不保留（下边元素会紧跟上一起移动），
    元素向上移动，并不会挤到上边的兄弟元素，而是覆盖上边的兄弟元素
margin-bottom为负：
    元素视觉大小不发生变化
    但是元素实际所占用的空间变小，下边元素会跟上来 或者是撑不开父级高度
    假如元素height为100px  设置marginbottom为-20  元素实际大小是80px

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>负margin的基础用法</title>
    <style>
        .outer{
            background-color: red;
            /*overflow: hidden;*/
        }
        .con1{
            width: 200px;
            height: 200px;
            background-color: deeppink;
            /*float: left;*/

            margin-left: 0px;
            margin-right: 0px;
        }
        .con2{
            width: 200px;
            height: 200px;
            background-color: yellow;
            /*float: left;*/

            margin-top: 0px;
            margin-bottom: -0px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="con1"></div>
        <div class="con2"></div>
    </div>
</body>
</html>
```
### 11.负margin练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>负margin练习1</title>
    <style>
        header{
            width: 1000px;
            height: 100px;
            background-color: red;
            margin: 0 auto;
        }
        section{
            width: 800px;
            height: 400px;
            background-color: yellow;
            /*margin: 0 auto;
            margin-top: -50px;*/

            margin: -50px auto 0;
        }
    </style>
</head>
<body>
    <div class="outer">
        <header>

        </header>
        <section>

        </section>
    </div>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>负margin练习1</title>
    <style>
        .outer{
            /*width: 1000px;*/
            height: 250px;
            border: 1px solid #000;
            float: left;
        }
        .inner{
            width: 1068px;
            overflow: hidden;
            margin-right: -68px;
        }
        .outer .inner div{
            width: 199px;
            height: 200px;
            background-color: pink;
            float: left;
            margin-right: 68px;
        }

        /*方法1  最后一个设置为0 覆盖*/
        /*.outer .active{
            margin-right: 0;
        }*/


        /*方法二： 直接使用选择器选择前3个*/
       /* .outer div:nth-child(-n+3){
            margin-right: 68px;
        }*/
    </style>
</head>
<body>
    <div class="outer">
        <div class="inner">
            <div></div>
            <div></div>
            <div></div>
            <div class="active"></div>
        </div>
    </div>
</body>
</html>
```
### 12.边框的设置:
border-width:边框宽度
border-style:边框样式  solid 实现   dashed  虚线    dotted  点线
border-color：边框颜色

合写：border：border-width  border-style border-color

注意：
    边框是在margin里边
    背景颜色在边框中显示（实线的时候，我们看不到）
    背景图片原点没有从边框开始  而是从padding开始的，但是可能会平铺到边框中

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>边框的设置</title>
    <style>
        .box{
            width: 100px;
            height: 100px;
            border: 10px dotted #000;
            margin: 10px;
            background-color: red;
            background: url("../images/05.jpg") 0 0 no-repeat;
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```
### 12.边框的应用
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>边框的应用</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }

        .head_out{
            width: 100%;
            border-bottom: 4px solid #55a5ff;
        }
        .head_out .head{
            width: 1000px;
            height: 100px;
            background-color: orangered;
            margin: 0 auto;
        }
        .head a{
            text-decoration: none;
            color: #3c3c3c;
            font-size: 12px;
        }
        .head .head_login{
            border-right: 3px solid #3c3c3c;
            border-left:3px solid #3c3c3c;
            padding: 10px 20px;
            margin-left: 20px;
        }
        .head .head_regist{
            border-right: 3px solid #3c3c3c;
            padding: 10px 20px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="head_out">
            <header class="head">
                <div class="head_top">
                    <a href="###" class="head_login">登录</a>
                    <a href="###" class="head_regist">注册</a>
                </div>
            </header>
        </div>
    </div>
</body>
</html>
```
### 13.边框画三角形
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>边框画三角形</title>
    <style>
        body{
            background-color: #ccc;
        }
        .box{
            width: 0;
            height: 0;
            border: 100px solid #000;
            border-top-color: transparent;
            border-bottom-color: #ff8d9e;
            border-left-color: transparent;
            border-right-color:transparent;

            transform: rotate(0deg);
        }
    </style>
</head>
<body>
    <!--
        当内容非常小的时候，
        上下左右边框重合，重合部分就会平分为两半，
        这个时候，整个边框就分为了4个三角形
    -->
    <div class="box"></div>
</body>
</html>
```
### 14.padding：
1、padding的写法和margin基本一摸一样
2、padding主要撑开内容之间的距离
3、背景颜色可以显示在padding中，也可以显示在border中
4、背景图片的原点，其实默认在 padding的左上角

padding的支持性：
    块标签：
        四个方向都支持
    行标签：
        水平方向直接支持
        垂直方向也支持设置，但是不能撑开元素的距离

padding不支持负值
padding也不去设置auto 不支持

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>padding的设置</title>
    <style>
        .box{
            width: 800px;
            height: 400px;
            background-color: #b51d1a;
        }
        .con{
            width: 200px;
            height: 200px;
            background-color: #5df2ff;
            padding: 10px 20px;
            background: url("../images/05.jpg");
        }
        .con span{
            padding: 20px;
            color: #fff;
            background-color: yellow;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="con">
            今天天气真好
            <span>哈哈哈</span>
        </div>

    </div>
</body>
</html>
```
### 15.padding扩大点击区域
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .con1{
            width: 100px;
            height: 100px;
            background-color: red;
        }
        a{
            font-size: 12px;
            padding: 20px 0;
        }
    </style>
</head>
<body>
    <div>
        <div class="con1"></div>
        <a href="###">百度两下你就直到</a>
        <div class="con1"></div>

    </div>
</body>
</html>
```
### 16.标准盒模型和怪异盒模型：
默认情况基本都是标准盒模型

怪异盒模型：ie6  或者是 没有正确书写版本声明  或者是设置了box-sizing

标准盒模型：
    元素占用的空间大小为：内容区域（content）+内边距（padding）+边框（border）+外边距（margin）
    ex：
        一个元素    margin：20px 30px;
                    padding:10px 5px;
                    border: 2px solid #000;
                    width:300px;
            求这个元素所占用的宽度空间大小是：374px

    怪异盒模型：
    元素所占用的空间大小为：内容（content+padding+border）+外边距（margin）
        怪异盒模型设置的width是 content+padding+border整体的宽度
        ex：
            一个元素    margin：20px 30px;
                        padding:10px 5px;
                        border: 2px solid #000;
                        width:300px;
                求这个元素所占用的宽度空间大小是：360px
                求这个元素内容（content）区域的宽度是286px

### 17.生成怪异盒模型
 一个盒子模型中，每一个属性盒子都有自己的名字
由内向外分别是  content-box 、 padding-box、border-box、margin-box（没有官方说明）

将一个元素设置盒模型显示
    box-sizing属性：
        content-box:标准盒模型
        border-box:怪异盒模型

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>怪异盒模型</title>
    <style>
        .box{
            width: 100px;
            height: 100px;
            background-color: red;
            padding: 10px;
            margin: 15px;
            border: 2px solid #000;
            box-sizing: content-box;/*标准盒模型*/
            box-sizing: border-box;/*怪异盒模型*/
        }
    </style>
</head>
<body>
    <div class="box">

    </div>
</body>
</html>
```

### 18.盒子模型概念总结
1、在html中，把每一个元素都当做成一个盒子，拥有盒子的平面外形和空间
2、盒子模型由 内容（content）、内边距（padding）、边框（border）、外边距（margin）四个构成
3、盒子模型分为怪异盒子模型和标准盒子模型
4、标准盒子模型的所占用空间的计算方式是 content+padding+border+margin
    怪异盒子模型所占的的空间计算方式是 content+margin（content内容是包含内容内边距和边框的）
5、使用box-sizing属性可以切换盒子模型的方式

### 19.padding和margin的使用场景
padding和margin的使用场景
padding：撑开内容与边框的距离 padding中会显示背景颜色和背景图片

margin：撑开元素之间距离

日常使用过程中，可以按照下边方式来使用：
    padding和margin都可以撑开元素之间的距离。
    padding主要用来撑开父子之间的距离
    margin主要用来撑开兄弟之间的距离

## 七、浮动
### 01.浮动的来历
正常页面流：
    在css中，是存在流的概念的，正常情况下，页面总是由左至右，由上至下布局，我们把这种情况称作为正常页面流
    但是，在很多情况下，正常页面流有很多效果实现不了，所以需要一些手段来破坏流
    而浮动（float）就是破坏流的一种手段

浮动的来历：
    在目前开发中，很多的元素都是一个个的float堆叠起来的，但是这种布局及其容易崩溃，
    只要高度和宽度发生一点变化，页面都可能发生错乱
    float设计的初始想法仅仅是为了做文字环绕图片

    左浮动：让元素沿着容器左侧放置，允许文本和内联元素环绕它，它从正常的页面中移除，虽然还保持一点流动性


浮动以后元素出现重叠，但是行框盒子和浮动元素有不可重叠性

### 02.浮动解决一行显示块标签问题
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动解决一行显示块标签问题</title>
    <style>
        .box1{
            width: 100px;
            height: 100px;
            background-color: red;
            margin: 5px;
            /*float: left;*/
            float: right;
        }
        .box2{
            width: 150px;
            height: 150px;
            background-color: yellow;
            margin: 5px;
            /*float: left;*/
            float: right;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="box1"></div>
        <div class="box2">aa</div>
    </div>
</body>
</html>
```
### 03.可能被阻挡的浮动
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>可能被阻挡的浮动</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        ul{
            width: 960px;
            margin: 0 auto;
            background-color: #5df2ff;
        }
        ul li{
            width: 300px;
            height: 200px;
            margin: 10px;
            background-color: red;
            float: left;
        }
    </style>
</head>
<body>
    <ul>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
</body>
</html>
```
### 04.浮动对元素的影响
浮动对元素的影响:
    块标签：
        不再独占一行
        仍然可以设置宽和高
        构成了BFC，不再进行父级塌陷
        完美支持margin和padding

    行标签：
        可以设置宽高
        完美支持padding和margin

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动对元素的影响</title>
    <style>
        .box{
            width: 100px;
            height: 100px;
            background-color: red;
            margin: 10px;
            padding: 10px;

            /*float: left;*/
        }

        .span1{
            width: 100px;
            height: 30px;
            background-color: #5df2ff;
            margin: 40px;
            padding: 20px;

            float: left;
        }
    </style>
</head>
<body>
    <div class="box">

    </div>
    <span class="span1">span1</span>
</body>
</html>
```
### 05.浮动练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动练习</title>
    <style>
        .outer{
            width: 1000px;
            margin: 0 auto;
        }
        .header{
            /*width: 1000px;*/
            height: 100px;
            /*margin: 0 auto;*/
            background-color: #ffdd65;
        }
        .box{
            /*width: 1000px;*/
            /*margin: 20px auto 0;*/
            margin-top: 20px;
            /*清除浮动方式1：给浮动元素的父级书写overflow：hidden*/
            overflow: hidden;
        }
        .box .left{
            width: 200px;
            height: 400px;
            background-color: deeppink;
            float: left;
            /*margin-right: 50px;*/
        }
        .box .right{
            width: 750px;
            height: 400px;
            background-color: #da90ff;
            float: right;
        }
        .footer{
            /*width: 1000px;*/
            height: 100px;
            /*margin: 30px auto 0;*/
            margin-top: 30px;
            background-color: #bdbaff;
        }
    </style>
</head>
<body>
    <div class="outer">
        <header class="header"></header>
        <div class="box">
            <div class="left"></div>
            <div class="right"></div>
        </div>
        <footer class="footer"></footer>
    </div>
</body>
</html>
```
### 06.清除浮动：
浮动的概念：让元素脱离文档流，按照指定的方向发生移动，遇到父级的边界或者是上一个浮动元素或者是上一个不浮动兄弟元素就停下来

高度塌陷：浮动元素以后，脱离父级内容区域，父级没有内容撑开自身的高度
        父级的兄弟元素是 按照父级的位置进行布局的，所以页面会乱掉

清除浮动：清除浮动不是不让元素浮动，而是清除浮动对父级带来的影响

清除浮动的方法：
    1、给浮动元素的父级设置高度height（不推荐使用）
        缺点：很多情况下 高度都是不缺定的  所有不适用

    2、以浮制浮，给浮动元素的父元素设置浮动，原理是开启BFC（不推荐使用）
        缺点：只有在父级需要浮动的时候，可以这么清除，否则父级的浮动会影响布局
    
    3、overflow：hidden；给父级设置，原理也是开启BFC（可以使用）
        优点：简单快捷
        缺点：元素超出的时候，会隐藏超出部分
    
    4、br清除浮动：在浮动元素的后边书写一个br。br中书写clear属性，值为both
        缺点：增加不必要的元素，不符合样式与结构相分离的要求
    
    5、clear清浮动法：给浮动元素的下边添加一个块元素，书写样式clear:both
        缺点：增加额外的结构，不符合语义化标准
    
    6、after伪元素清浮动（推荐）
        可以给所有浮动元素的父级一个  clearFix的类名
        当一个元素需要清除浮动的时候  直接设置clearFix类名即可
    
        .clearFix:after{
            content:"\200B";  必须拥有content属性   内容为空
            display: block;   必须块标签才能清浮动
            height: 0;          高度为0 不占用空间
            clear: both;        清除浮动
        }
    
        .clearFix{  //兼容ie
            *zoom:1;    //*是css  hack 只有ie6.7 认识
                            ie6、7 不支持伪元素，所以需要开启元素的haslayout来清除浮动
        }
### 07.伪元素
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>伪元素</title>
    <style>
        .box:after{
            content:"嗯，好";
        }
        .box:before{
            content:"啊";
        }
    </style>
</head>
<body>
    <div class="box">
        <p>今天天气真好</p>
    </div>
</body>
</html>
```
## 八、定位
### 01.定位的概念：
1、除非专门指定，否则所有框都在普通流中定位。
2、也就是说，普通流中的元素的位置由元素在 HTML 中的位置决定。
3、定位的基本思想很简单，它允许你定义元素框相对于其正常位置应该出现的位置，或者相对于父元素甚至浏览器窗口本身的位置
4、通过使用 position 属性，我们可以选择 4 种不同类型的定位
    position属性是把元素放置到一个静态的、相对的、绝对的、或固定的位置中
    position属性的四个值分别对应static、relative、absolute、fixed

left、right、top、bottom
    单位为 px 或 百分比都可以
    left 和 right 同时设置时只有left有效
    top 和bottom一起设置时只有top有效
### 02.相对定位
position:relative;
让元素相对定位：
    元素先放置在未添加定位时候的区域
    然后再不改变页面布局的情况下（
            1、其他元素没有受到任何影响
            2、自身原来的位置也保留
            3、和浮动可以一起使用
        ）


    left:   设置元素 左边缘 到 原来左边缘位置 的距离
    right:   设置元素 右边缘 到 原来右边缘位置 的距离
    top:   设置元素 上边缘 到 原来上边缘位置 的距离
    bottom:   设置元素 下边缘 到 原来下边缘位置 的距离
    
    在相对定位中：left为正 元素向右走
    在相对定位中：top为正 元素向下走
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>相对定位</title>
    <style>
        .outer div{
            width: 200px;
            height: 200px;
        }
        .con1{
            background-color: orangered;
            position: relative;
            left: 0px;
            right: 0px;
            float: left;
        }
        .con2{
            background-color: #5df2ff;
            float: left;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="con1"></div>
        <div class="con2"></div>
    </div>
</body>
</html>
```
### 03.包含块：
绝对定位的元素 相对于它的包含块进行定位.
如何确定一个元素的包含块，完全取决于它自身的position属性：
    1、如果一个元素自身的position属性是 static或者是relative：
        它的包含块就是离他最近的祖先元素或者是格式化上下文。

    2、如果一个元素自身的position属性是absolute，
        它的包含块就是离他最近的 拥有定位属性（值不为static）的元素
    
    3、如果一个元素自身的position属性是fixed
        它的包含块就是viewport（视口）
    
    4、补充：如果一个元素的position属性是absolute 或者是 fixed 在下边几种情况下，包含块会发生改变
        1、当祖先元素的 拥有 transform 或 perspective 属性 并且值不为none的时候  它也是被当做包含块
        2、当祖先元素 拥有 filter属性的时候（值不为none）  它也可以被当做包含块
    
    5、如果由内向外找不到包含块条件的元素，那么html（根元素）被称作为初始包含块

### 04.绝对定位：
1、不预留任何的空间（脱离页面流）
2、通过指定当前元素 相对于其包含块偏移的量 来确定当前元素的位置
3、绝对定位以后，浮动失效。margin padding仍然可以使用

left: 0; 让定位元素的左边距离包含块左边为0
top: 0;让定位元素的上边距离包含块上边为0

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>绝对定位</title>
    <style>
        .outer{
            width: 800px;
            height: 500px;
            background-color: red;
            margin: 0 auto;
            overflow: hidden;

            /*transform: rotateX(0deg);*/
            /*perspective: 300px;*/
            position: relative;
        }
        .inner{
            width: 600px;
            height: 300px;
            background-color: deeppink;
            margin: 50px;
            overflow: hidden;
            position: relative;
        }
        .con{
            width: 300px;
            height: 200px;
            background-color: greenyellow;
            margin: 30px;
            position: relative;

        }
        .box{
            width: 100px;
            height: 100px;
            background-color: yellow;
            position: absolute;

            right: 0;
            bottom: 0;
        }
    </style>
</head>
<body>
 <div class="outer">
        <div class="inner">
            <div class="con">
                con
                <div class="box"></div>
            </div>
        </div>
    </div>
</body>
</html>
```

### 05.固定定位
固定定位：
    1、不为元素预留空间（脱离页面流）
    2、相对于视口（viewport）的位置来定位元素的
    3、滚动页面滚动条的时候，视口不发生改变，元素位置也不会改变

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>固定定位</title>
    <style>
        .con{
            height: 4000px;
            background-color: #3c3c3c;
        }
        .left{
            position: fixed;
            width: 150px;
            height: 300px;
            left: 0;
            top: 100px;
            background-color: red;
            text-align: center;
            line-height: 100px;
            font-size: 30px;
            color: #fff;

            animation: change .2s linear infinite;

        }
        .right{
            position: fixed;
            width: 150px;
            height: 300px;
            right: 0;
            top: 100px;
            background-color: red;
            text-align: center;
            line-height: 100px;
            font-size: 30px;
            color: #fff;
            animation: change .2s linear infinite;
        }

        @keyframes change {
            0%{
                background-color: red;
            }
            20%{
                background-color: green;
            }
            40%{
                background-color: pink;
            }
            60%{
                background-color: yellowgreen;
            }
            80%{
                background-color: grey;
            }
            100%{
                background-color: red;
            }
        }
    </style>
</head>
<body>
    
    <div class="con"></div>
    <div class="gg">
        <div class="left">
            开局一条狗
            <br>
            装备全靠爆
        </div>
        <div class="right">
            我是砸砸辉
            <br>
            是兄弟就来
            <br>
            砍我吧
        </div>
    </div>
</body>
</html>
```
### 06.定位位置的设置
定位位置是通过 left  right  top  bottom来设置的

值可以是
    1、像素
    2、百分比
        left 和 right 的百分比相对于参考物的width
        top和botton的百分比是相对于参考物的height

补充：
        无论任何方向的padding或margin都是参照元素的width来计算的

### 07.轮播图布局练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>图片轮播布局</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        .outer{
            width: 520px;
            border: 1px solid #5df2ff;
            margin: 100px auto 0;
            position: relative;
        }
        .inner{
            width: 520px;
            overflow-x: scroll;
        }
        .con{
            width: 2600px;
            overflow: hidden;
        }
        .con img{
            width: 520px;
            height: 280px;
            float: left;
        }
        .left{
            width: 30px;
            height: 30px;
            font-size: 24px;
            line-height: 30px;
            text-align: center;
            background-color: rgba(0,0,0,.5);
            color: #fff;
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
        }
        .right{
            width: 30px;
            height: 30px;
            font-size: 24px;
            line-height: 30px;
            text-align: center;
            background-color: rgba(0,0,0,.5);
            color: #fff;
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
        }
        .page{
            position: absolute;
            bottom: 20px;
            left: 50%;
            /*让元素向左移动自身的一半*/
            transform: translateX(-50%);
        }
        .page li{
            width: 20px;
            height: 20px;
            background-color: rgba(255,255,255,.4);
            border-radius: 50%;
            float: left;
            margin: 3px;
        }
        .page .active{
            background-color: rgba(255,255,255,1);
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="inner">
            <div class="con">
                <img src="../images/01.jpg" alt="">
                <img src="../images/02.jpg" alt="">
                <img src="../images/03.jpg" alt="">
                <img src="../images/04.jpg" alt="">
                <img src="../images/05.jpg" alt="">
            </div>
            <p class="left">&lt;</p>
            <p class="right">&gt;</p>
            <ul class="page">
                <li class="active"></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul>
        </div>
    </div>

</body>
</html>
```
### 08.z-index属性：
1、指定了一个定位属性的元素 及其后代 的层叠顺序
2、只有定位元素（非static值）拥有 z-index属性
3、z-index的值没有单位  理论上来说 z-index的值大的元素 会覆盖小的元素
4、定位元素默认的z-index 的值 是  auto

5、如果一个拥有z-index属性的定位元素中 子元素也设置了z-index
    那么子元素会重新创建一个层叠上下文，子元素的z-index只能在当前的层叠上下文中对比排列

元素层叠顺序：
    z-index为负< background< border< 块级元素 <浮动元素 <内联元素 <没有设置z-index的定位元素 < z-index为正

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>z-index属性</title>
    <style>
        .outer{
            width: 500px;
            height: 300px;
            background-color: rgba(34,45,124,.5);
            position: absolute;
            z-index: 1;
        }
        .outer .con{
            width: 300px;
            height: 200px;
            background-color: rgba(111,43,21,.5);
            position: absolute;
            z-index: 1000;
        }
        .inner{
            width: 300px;
            height: 200px;
            background-color: rgba(234,124,35,1);
            position: absolute;
            top: 180px;
            z-index: 4;
        }
    </style>
</head>
<body>
<div class="outer">
        <div class="con">

        </div>
    </div>
    <div class="inner"></div>
</body>
</html>
```

### 09.z-index练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>z-index练习</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        .outer{
            overflow: hidden;
            background-color: #ccc;
        }
        .outer li{
            float: left;
            width: 300px;
            height: 200px;

            margin: 100px;
            position: relative;
        }
        .outer li .con{
            width: 300px;
            height: 200px;
            background-color: pink;
            position: relative;
            z-index: 4;
        }
        .outer li .show{
            width: 300px;
            height: 50px;
            background-color: #5df2ff;
            position: absolute;
            bottom: -25px;
            right: -25px;
            z-index: 3;
        }
    </style>
</head>
<body>
    <!--
        如果想让一个元素拥有z-index属性，并且还不想影响它的其他正常布局
        我们可以给这个元素一个 position：relative;
    -->
    <ul class="outer">
        <li>
            <div class="con"></div>
            <div class="show"></div>
        </li>
        <li>
            <div class="con"></div>
            <div class="show"></div>
        </li>
        <li>
            <div class="con"></div>
            <div class="show"></div>
        </li>
        <li>
            <div class="con"></div>
            <div class="show"></div>
        </li>
        <li>
            <div class="con"></div>
            <div class="show"></div>
        </li>
        <li>
            <div class="con"></div>
            <div class="show"></div>
        </li>
    </ul>
</body>
</html>
```
### 10.定位练习2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>定位练习</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        .outer{

        }
        .outer li{
            position: relative;
            float: left;
        }
        .outer li img{
            display: block;
            width: 313px;
            height: 220px;
        }
        .outer li p{
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 30px;
            line-height: 30px;
            text-align: center;
            color: #fff;
            /*背景半透明解决方案1：*/
            /*background-color: rgba(0,0,0,.5);*/


            /*背景半透明解决方案2:opacity*/
            /*opacity: .5;
            background-color: black;*/

            /*背景半透明解决方案3:*/
            background: url("../images/black.png") 0 0 repeat;
        }
    </style>
</head>
<body>
    <ul class="outer">
        <li>
            <img src="../images/01.jpg" alt="">
            <p>今天天气真好啊啊</p>
        </li>
    </ul>
</body>
</html>
```
## 九、css2其他
### 01.a标签的4个伪类：
link：当有链接属性时
visited:当连接被访问过以后
hover：当连接被鼠标悬浮的时候
active:当连接在激活状态的时候

位置不能互换：
    这4个选择器 优先级是一样的。
    顺序改变就可能后边覆盖前边的
    比如visited写在最后，那么当连接北方问过后，访问过后的颜色就会覆盖hover和active

    记忆：爱恨法则   love-hate


    ！！！
    hover适用于多数其他元素
    并且伪元素也可以使用
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>a标签的4个伪类</title>
    <style>
        a{
            color: pink;
        }
        .a1:link{
            color: yellow;
        }
        .a2:visited{
            color: blueviolet;
        }
        .a3:hover{
            color:red;
        }
        .a4:active{
            color: #2ba5eb;
        }

    </style>
</head>
<body>

<a href="###" class="a1">link 当有链接属性时</a>
<a href="####" class="a2">visited 当连接被访问过之后</a>
<a href="####" class="a3">hover 当连接被鼠标悬浮的时候</a>
<a href="####" class="a4">active:当连接在激活状态的时候</a>


<a href="##" class="a1 a2 a3 a4">同时设置4个伪类</a>

</body>
</html>
```
### 02.hover的下拉效果
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>hover的下拉效果</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        .outer{
            width: 300px;
            border: 1px solid #ffa000;
            position: relative;
        }
        .outer p{
            width: 300px;
            height: 50px;
            line-height: 50px;
            text-align: center;
            color: #fff;
            background-color: #ccc;
        }
        .outer .con{
            position: absolute;
            width: 400px;
            left: 0;
            top:50px;
            background-color: #2ba5eb;

            display: none;
        }
        .con li{
            line-height: 30px;
        }

        .outer:hover>.con{
            display: block;
        }
        .outer:hover>p{
            background-color: red;
        }
        .outer .con li:hover{
            background-color: deeppink;
        }
    </style>
</head>
<body>
    <div class="outer">
        <p>我是一个标题</p>
        <ul class="con">
            <li>新闻</li>
            <li>娱乐</li>
            <li>我的</li>
            <li>天气</li>
            <li>真好</li>
        </ul>
    </div>
</body>
</html>
```
### 03.下拉效果2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>hover的下拉效果</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        .outer_fathor{
            overflow: hidden;
        }
        .outer{
            width: 300px;
            border: 1px solid #ffa000;
            position: relative;
            float: left;
        }
        .outer p{
            width: 300px;
            height: 50px;
            line-height: 50px;
            text-align: center;
            color: #fff;
            background-color: #ccc;
        }
        .outer .con{
            position: absolute;
            width: 400px;
            left: 0;
            top:50px;
            background-color: #2ba5eb;

            display: none;
        }
        .con li{
            line-height: 30px;
        }

        .outer:hover>.con{
            display: block;
        }
        .outer:hover>p{
            background-color: red;
        }
        .outer .con li:hover{
            background-color: deeppink;
        }
    </style>
</head>
<body>
    <ul class="outer_fathor">
        <li class="outer">
            <p>我是一个标题</p>
            <ul class="con">
                <li>新闻</li>
                <li>娱乐</li>
                <li>我的</li>
                <li>天气</li>
                <li>真好</li>
            </ul>
        </li>
        <li class="outer">
            <p>我是一个标题</p>
            <ul class="con">
                <li>新闻</li>
                <li>娱乐</li>
                <li>我的</li>
                <li>天气</li>
                <li>真好</li>
            </ul>
        </li>
        <li class="outer">
            <p>我是一个标题</p>
            <ul class="con">
                <li>新闻</li>
                <li>娱乐</li>
                <li>我的</li>
                <li>天气</li>
                <li>真好</li>
            </ul>
        </li>
        <li class="outer">
            <p>我是一个标题</p>
            <ul class="con">
                <li>新闻</li>
                <li>娱乐</li>
                <li>我的</li>
                <li>天气</li>
                <li>真好</li>
            </ul>
        </li>
    </ul>

</body>
</html>
```
### 04.精灵图
精灵图（雪碧图、css sprites）:
    是一种网页图片的应用处理方式，允许将一个页面中很多零星的小图片包含到一张大图中去，
    当访问页面的时候，就不会一张张的去请求显示图片
    对于当前的网络来说，小于200k的文件加载速度是一样的
    通过background-position属性 将图片定位到需要的位置即可、

优点：
    1、减少图片大小
    2、减少服务器请求次数

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>精灵图</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        .outer{
            width: 101px;
            overflow: hidden;
            border: 1px solid #3c3c3c;
            margin: 100px auto 0;
        }
        .box{
            overflow: hidden;
            width: 102px;
            margin-top: -1px;
        }
        .box li{
            width: 50px;
            height: 80px;
            border-right: 1px solid #3c3c3c;
            border-top: 1px solid #3c3c3c;
            float: left;
        }
        .box li i{
            width: 45px;
            height: 40px;
            display: block;
            margin: 10px auto 0;
            background: url("../images/jd_2.png") 0 0 no-repeat;
        }
        .box li:nth-child(1) i{
            background-position: -1px -3px;
        }
        .box li:nth-child(2) i{
            background-position: -70px -5px;
        }
        .box li:nth-child(3) i{
            background-position: -2px -73px;
        }
        .box li:nth-child(4) i{
            background-position: -70px -73px;
        }

        .box li p{
            text-align: center;
            margin-top: 5px;
        }
    </style>
</head>
<body>
<div class="outer">


    <ul class="box">
        <li>
            <i></i>
            <p>加油卡</p>
        </li>
        <li>
            <i></i>
            <p>白条</p>
        </li>
        <li>
            <i></i>
            <p>机票</p>
        </li>
        <li>
            <i></i>
            <p>电影票</p>
        </li>
    </ul>
</div>
</body>
</html>
```

### 05.精灵图2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>精灵图</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        .outer{
            width: 161px;
            overflow: hidden;
            border: 1px solid #3c3c3c;
            margin: 100px auto 0;
        }
        .box{
            overflow: hidden;
            width: 162px;
            margin-top: -1px;
        }
        .box li{
            width: 80px;
            height: 100px;
            border-right: 1px solid #3c3c3c;
            border-top: 1px solid #3c3c3c;
            float: left;
            background: #ccc;
            color: #fff;
        }
        .box li:hover{
            background-color: red;
        }
        .outer .box li:hover i{
            background-position-y: -53px;
        }
        .box li i{
            width: 45px;
            height: 40px;
            display: block;
            margin: 10px auto 0;
            background: url("../images/i-nav.png") 0 0 no-repeat;
        }
        .box li:nth-child(1) i{
            background-position: 3px 0px;
        }
        .box li:nth-child(2) i{
            background-position: -61px 0px;
        }

        .box li p{
            text-align: center;
            margin-top: 5px;
        }
    </style>
</head>
<body>

<div class="outer">


    <ul class="box">
        <li>
            <i></i>
            <p>加油卡</p>
        </li>
        <li>
            <i></i>
            <p>白条</p>
        </li>
    </ul>
</div>
</body>
</html>
```
### 06.最小高度
使用 min-height 来设置最小高度
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>最小高度</title>
    <style>
        .outer{
            width: 200px;
            border: 1px solid #000;
        }
        header,footer{
            text-align: center;
            height:40px;
            line-height: 40px;
        }
        .con{
            border: 1px solid red;
            line-height: 1.7;
            min-height: 100px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <header>
            头部
        </header>
        <div class="con">
            文章1 <br>
            文章1 <br>
            文章1 <br>
            文章1 <br>
            文章1 <br>
            文章1 <br>
            文章1 <br>
            文章1 <br>
            文章1 <br>
        </div>
        <footer>
            底部
        </footer>
    </div>
</body>
</html>
```
### 07.最小宽度
min-width设置最小宽度
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>最小宽度</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .head_out{
            width: 100%;
            border-bottom: 4px solid #5ab3f4;
            min-width: 1000px;
        }
        .head{
            width: 1000px;
            margin:0 auto;
            height: 100px;
            background-color: #ffa000;
        }
    </style>
</head>
<body>
<!--
    案例中，当浏览器缩小窗口，生成横向滚动条的时候，
    head_out  width：100%的宽度  是屏幕的宽度，当滑动横向滚动条的时候，这个元素的宽度没有达到主要内容1000px的要求
    所以可以给head_out设置最小宽度  min-width
-->
    <div class="head_out">
        <div class="head"></div>
    </div>
</body>
</html>
```
### 08.最大宽度和最大高度

宽度：width    min-width  max-width
高度：height   min-height   max-height

当3个冲突后怎么办：
    1、当min-width和max-width 冲突的时候，min-width是优先的

    2、当width和  min或max冲突以后，min或者max直接无视width的存在（无论是否添加 ！important）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            height: 100px;
            background-color: red;
            min-width: 800px;
            max-width: 700px;
            width: 400px !important;
        }
    </style>
</head>
<body>

<div class="box">

</div>
</body>
</html>
```
### 09.伪元素
1、伪元素可以理解为“虚假的元素”，
2、他们虽然会在内容元素的前后插入额外的元素，但并不会在文档中生成，在文档的源代码当中并不能够找到它们。
3、虽然在结构上是虚假元素，但是在表现上和普通元素没有什么区别，能为它们添加任何样式，比如改变文字颜色、添加背景、调整字体大小等等

after:
    在当前元素的最后边插入一个伪元素
before：
    在当前元素的最前边插入一个伪元素

4、伪元素必须拥有content属性 ，才能生效
5、伪元素默认是一个行内元素
6、伪元素对其他属性基本都是支持的

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>伪元素</title>
    <style>
        .box{
            width: 200px;
            height: 50px;
            background-color: red;
            position: relative;
        }
        .box:after{
            content:"没有我你是不行的";
            display: block;
            width: 100px;
            height: 100px;
            background-color: pink;
        }
        .box:before{
            content:"hahahah";
            display: block;
            width: 100px;
            height: 100px;
            background-color: pink;
            position: absolute;
            left: 300px;
            top: 80px;
        }
    </style>
</head>
<body>

    <div class="box">我是一个box</div>
</body>
</html>
```
### 10.其他伪元素
first-letter伪元素：
    把一个块级元素的第一个文字选中，可以单独进行控制
first-line伪元素
    把一个块级元素的第一行选中，单独进行控制

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>其他伪元素</title>
    <style>
        p{
            width: 300px;
            line-height: 1.6;
            background-color: red;
        }
        p:first-letter{
            font-size: 30px;
            color: #fff;
        }
        p:first-line{
            font-size: 24px;
            color: yellow;
        }
    </style>
</head>
<body>
    <p>今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好今天天气真的好</p>
</body>
</html>
```
### 11.css hack
由于不同的厂商的浏览器，或者是同一个浏览器不同的版本（ie），对css的解析和认识不完全一样
可能会导致不同浏览器显示的效果不相同
那么我们需要针对某个浏览器，去写不同的样式，让代码能够兼容所有的浏览器
比如：
    after伪元素清浮动，只有ie8及以上支持，所以要针对ie6、7书写一个开启haslayout
    *代表ie6,7  zoom代表开启haslayout  所以可以书写  *zoom：1；
    那么这个代码只有ie 6 7 认识

为什么使用css hack
第一种理解：
    让我们css 的代码兼容不同的浏览器

第二种理解：
    我们可以为不同的浏览器定制不同的样式

css hack有3种表现方式：
1、css属性前缀法  2、选择器前缀法   3、IE条件注释法

1、IE条件注释法
    主要针对IE的版本
        gt ：大于
        lt：小于
        gte：大于等于
        lte：小于等于
        ！：非当前
        目前条件注释只支持到ie9及以下  其他浏览器不支持条件注释

2、css属性前缀法
    *color：ie 5,6,7
    +color：ie 5,6,7
    #color：ie 5,6,7
    -color：ie 5、6
    color\0:ie 9 10 11
    color\9:ie 6 7 8 9 10
    color\9\0:ie 8 9 10

3、选择器前缀法
    将前缀写在选择器前边，控制选择器是否针对当前浏览器有效
    *html  ie 5 6
    *+html ie7
    :root  ie9 10 11


### 12.粘连布局方法1：
又称作  stick footer布局
如果页面不够长的话  footer粘在视窗的底部
如果页面内容长度超出，footer就会被页面向下推送出去

给inner最小高度是 100%
让footer给margin-top：-50 上去  （main元素和footer重叠）
给main元素一个padding-bottom 50px   就算重叠  文字也显示不到padding中
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>粘连布局</title>
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        html,body{
            height: 100%;
        }
        .outer{
            height: 100%;
        }
        .inner{
            min-height: 100%;
        }
        .main{
            padding-bottom: 50px;
        }
        footer{
            height: 50px;
            background-color: #5ab3f4;

            margin-top: -50px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="inner">
            <div class="main">
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                
            </div>
        </div>
        <footer></footer>
    </div>
</body>
</html>
```
### 13.粘连布局方法2
给inner设置最小高度是100%
给inner设置padding-bottom是50px
给inner设置为 怪异盒子模型：box-sizing：border-box
让footermargin-top为负 上来
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>粘连布局</title>
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        html,body{
            height: 100%;
        }
        .outer{
            height: 100%;
        }
        .inner{
            min-height: 100%;
            padding-bottom: 50px;
            /*设置为怪异盒子模型的方式：
            高度就包含了padding  总共加起来是百分百  并且main不会显示在inner的padding中*/
            box-sizing: border-box;
        }
        .main{

        }
        footer{
            height: 50px;
            background-color: #5ab3f4;

            margin-top: -50px;
        }
    </style>
</head>
<body>

    <div class="outer">
        <div class="inner">
            <div class="main">
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
            </div>
        </div>
        <footer></footer>
    </div>
</body>
</html>
```
### 14.calc方法：
calc()
    我们可以把它当做一个函数，其实他是calculate（计算）缩写。
    是css3提供的一个新功能，主要用来计算长度
    我们可以用它来给padding  margin width height font-size等等计算大小值 值是一个动态的


1、使用+ - * /进行运算
2、可以使用百分比  px  em  rem等单位
3、可以单位混合计算
4、在使用的时候，尽量在 +  -  * / 前后添加一个空格
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>calc方法</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .box{
            width: calc(100% - 200px);
            height: calc(100px / 2 + 100px);
            margin: 0 auto;
            background-color: red;
        }
    </style>
</head>
<body>
    <!--书写一个效果，让div永远距离两边都是100px
    计算div的宽度-->
    <div class="box"></div>
</body>
</html>
```
### 14.粘连布局方法3
直接计算inner的最小高度是  100% - 50px
footer在main元素小的时候，刚好跟着inner  在最下边。否则就被inner撑下去
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>粘连布局</title>
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        html,body{
            height: 100%;
        }
        .outer{
            height: 100%;
        }
        .inner{
            min-height: calc(100% - 50px);
            /*padding-bottom: 50px;*/
        }
        .main{

        }
        footer{
            height: 50px;
            background-color: #5ab3f4;

            /*margin-top: -50px;*/
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="inner">
            <div class="main">
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
                main区域 <br>
            </div>
        </div>
        <footer></footer>
    </div>
</body>
</html>

```
### 15.样式重置
什么是样式重置（css reset）：
    1、将html的默认样式全部去掉，需要的时候我们自行添加。
    2、统一页面风格

为什么是使用样式重置：
    1、多数元素拥有自己的默认样式，并且我们很多都不需要
    2、默认样式在不同浏览器中呈现的也不一定相同，就会导致浏览器展示页面不相同的现象
    3、整个页面中 固定的风格代码，可以在样式重置中直接书写，不用每一个都设置

为什么不适用 *{margin：0；padding:0;}
    1、样式重置简单，不够完整  一些demo可以使用，真正项目不推荐使用，请使用css reset
    2、* 通配符 匹配所有的标签，影响很大 效率很低

normalize.css是什么？
    normalize觉得，存在即合理。保留了应该存在的默认样式，并且把每一个默认样式在浏览器中中统一了


```css
/* 清除内外边距 */
body, h1, h2, h3, h4, h5, h6, hr, p, blockquote,
dl, dt, dd, ul, ol, li,
pre,
fieldset, lengend, button, input, textarea,
th, td {
    margin: 0;
    padding: 0;
}

/* 设置默认字体 */
body,
button, input, select, textarea { /* for ie */
    /*font: 12px/1 Tahoma, Helvetica, Arial, "宋体", sans-serif;*/
    font: 16px/1.3 "Microsoft YaHei",Tahoma, Helvetica, Arial, "\5b8b\4f53", sans-serif; /* 用 ascii 字符表示，使得在任何编码下都无问题 */
}

h1 { font-size: 18px; /* 18px / 12px = 1.5 */ }
h2 { font-size: 16px; }
h3 { font-size: 14px; }
h4, h5, h6 { font-size: 100%; }

address, cite, dfn, em, var, i{ font-style: normal; } /* 将斜体扶正 */
b, strong{ font-weight: normal; } /* 将粗体扶细 */
code, kbd, pre, samp, tt { font-family: "Courier New", Courier, monospace; } /* 统一等宽字体 */
small { font-size: 12px; } /* 小于 12px 的中文很难阅读，让 small 正常化 */

/* 重置列表元素 */
ul, ol { list-style: none; }

/* 重置文本格式元素 */
a { text-decoration: none; }


/* 重置表单元素 */
legend { color: #000; } /* for ie6 */
fieldset, img { border: none; }
button, input, select, textarea {
    font-size: 100%; /* 使得表单元素在 ie 下能继承字体大小 */
}

/* 重置表格元素 */
table {
    border-collapse: collapse;
    border-spacing: 0;
}

/* 重置 hr */
hr {
    border: none;
    height: 1px;
}

/* 让非ie浏览器默认也显示垂直滚动条，防止因滚动条引起的闪烁 */
html { overflow-y: scroll; }
```
### 16.空元素和替换元素
空元素：
    在html中 ，一个不可能存在子节点（注释节点，文本节点，元素节点）的元素就叫做空元素
    通常在空元素上使用 闭合标签 是无效的
    `<input type="text"></input>` =======>闭合标签无效

    br、hr、img、input、link、meta、source

替换元素：
    浏览器根据元素的标签和属性，来决定元素具体显示的内容
    img、input、textarea、select、video、iframe是替换元素
    audio、canvas标签在某些时候也是替换元素
### 17.BFC：（Block Formatting Content）
块级格式化上下文
是页面可视化css渲染的一部分，是块盒子布局的一块区域
这个区域是相对外界独立的

构成BFC的条件：
    1、根元素（html）
    2、浮动元素（float属性不是none的）
    3、绝对定位和固定定位元素（position属性s是fixed 和 absolute的时候）
    4、行内块标签（display属性是inline-block）
    5、overflow属性不是visible的时候
    6、display其他属性（flex、gird、flow-root、table-cell、table-caption、table、table-row、table-row-group、table-header-group、table-footer-group）

BFC主要解决的问题：
    1、清除浮动：BFC区域的高度计算会把浮动元素计算在内
    2、解决父级塌陷：BFC构成独立的区域，里外的元素应该互补影响
    3、识别浮动的兄弟元素

### 18.BFC清除浮动
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .con{
            width: 100px;
            height: 100px;
            background-color: red;
            float: left;
        }

        .outer{
            border:1px solid yellow;

            /*2、overflow属性*/
            /*overflow: hidden;
            overflow: scroll;
            overflow: auto;*/

            /*3、display属性*/
            /*display: inline-block;*/

            /*4、float*/
            /*float: left;*/
            
            /*5、定位元素*/
            position: absolute;
            position: fixed;
        }
        .box{
            width: 100px;
            height: 100px;
            background-color: red;
            float: left;
        }
    </style>
</head>
<body>
<!--1、html元素构成BFC  可以包含浮动元素-->
<!--<div class="con"></div>-->

<div class="outer">
    <div class="box"></div>
</div>
</body>
</html>
```
### 19.BFC解决父级塌陷
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>

        .outer{
            /*border:1px solid yellow;*/
            background-color: yellow;

            /*1、overflow属性*/
            /*overflow: hidden;*/
            /*overflow: scroll;*/
            /*overflow: auto;*/

            /*q、display属性*/
            /*display: inline-block;*/

            /*3、float*/
            /*float: left;*/
            
            /*4、定位元素*/
            /*position: absolute;*/
            /*position: fixed;*/
        }
        .box{
            width: 100px;
            height: 100px;
            background-color: red;
            margin-top: 100px;
        }
    </style>
</head>
<body>


<div class="outer">
    <div class="box"></div>
</div>
</body>
</html>
```
### 20.BFC识别浮动元素
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .con{
            width: 100px;
            height: 40px;
            background-color: pink;
            float: left;
        }
        .outer{
            border:1px solid yellow;
        }
        .box{
            height: 100px;
            background-color: red;

            /*当一个元素被设置成BFC以后，能后识别前边的兄弟浮动元素。并且可以让自己不被浮动元素覆盖*/
            /*overflow: hidden;*/

        }
    </style>
</head>
<body>


<div class="outer">
    <div class="con">con</div>
    <div class="box">box</div>
</div>
</body>
</html>
```


