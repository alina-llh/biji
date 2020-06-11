# html课程
## 一、课程准备 

## 二、网页及浏览器
### 01.网站和网页
>网页是构成网站的基本元素，是承载各种网站应用的平台。
>通俗地说，您的网站就是由网页组成的，如果您只有域名和虚拟主机而没有制作任何网页的话，您的客户仍旧无法访问您的网站。
>网页是一个包含HTML标签的纯文本文件，它可以存放在世界某个角落的某一台计算机中，是万>维网中的一“页”，是超文本标记语言格式（标准通用标记语言的一个应用，文件扩展名为.html或.htm）。网页通常用图像档来提供图画。网页要通过网页浏览器来阅读。
### 02.常见浏览器
>浏览器是网页运行的平台，常见的浏览器有 IE 、火狐（Firefox）,谷歌（Chrome）,Safari和Opera等，我们平时称为五大浏览器，第六个是Edge浏览器，是微软改进IE新出的内置浏览器

- IE
IE是Trident内核,国内很多双核浏览器其中之一便是Trident,美其名曰“兼容模式”Window发布后，IE将其内置浏览器命名为Edge,Edge最显著的特点就是新内核EdgeHTML。
- Firefox(火狐)
Gecko内核，Gecko的特点是代码完全公开，因此开发程度很高，全世界的程序员都可以为其编写代码，增加功能，可惜这几年没落了，比如打开速度慢，升级频繁，猪一样的队友flash，神一样的对手chrome
- Safari
采用的是大名鼎鼎的WebKit。
现在很多人错误的把webkit叫做chrome（即使chrome内核已经是blink，之前采用的是webkit内核），苹果感觉像是被别人抢了媳妇，都哭晕在厕所了。
- chrome(谷歌)
Blink内核,在Chromium项目中研发Blink内核渲染引擎（即浏览器核心），内置于Chrome浏览器之中，Blink其实是Webkit的分支，大部分国产浏览器最新版用Blink内核
- Opera
Presto内核(已经废弃)是挪威产浏览器opera的“前任”内核，为何说是“前任”，因为最新的opera浏览器早已抛弃投入到谷歌的怀抱了，采用Blink。
- 移动端
移动端的浏览器内核主要说的是系统内置的浏览器内核。
Android手机而言，使用率最高的就是webkit内核，大部分国产浏览器宣称的自己的内核，基本上也是属于webkit二次开发。
IOS以及WP7平台上，由于系统原因，系统大部分自带浏览器内核，一般是Safari或者IE内核Trident。

- 扩展 
https://blog.csdn.net/yuyanjing123456789/article/details/78689595
### 03.pc端 浏览器 市场占有率
>Google的Chrome浏览器排名第一，其市场份额为45.74%；
>微软的IE浏览器排名第二，其份额为22.95%；（其中，IE9的份额为8.19%，IE8的份额为6.86%，IE11的份额为5.31%，IE7的份额为2.58%）
>QQ浏览器排名第三，其份额为6.70%；
>2345加速浏览器排名第四，其份额为6.06%；
>搜狗高速浏览器排名第五，其份额为4.22%；
>火狐浏览器排名第六，其份额为2.32%；
>其他浏览器的市场份额合计为12.00%。

## 三、web基础概念
### 01.万维网
>www其实是World Wide Web 的缩写，它是一个由许多互相链接的超文本组成的系统，通过互联网访问。在汉语中，www 被翻译成“万维网” （Wan Wei Wang）。
>由两部分构成：www客户端和www服务端。www客户端指的是个人设备（电脑、手机等）装的浏览器。www服务端指的是服务器（一台可以放许多文档的电脑）的程序。www经常被简称作web,所以www客户端、www服务端又叫web客户端、web服务端
>让web客户端访问web服务端，从而获得网页。
使用http协议传送数据，通过互联网通信。
### 02.http协议简要工作流程
>HTTP，又被称为超文本传输协议（http，hypertext transfer protocol)是互联网上应用最为广泛的一种网络协议。所有的WWW文件都必须遵守这个标准。设计HTTP最初的目的是为了提供一种发布和接收HTML页面的方法。
>浏览网页时在浏览器地址栏中输入的URL前面都是以"http://"开始的。HTTP定义了信息如何被格式化、如何被传输，以及在各种命令下服务器和浏览器所采取的响应。 
> 工作流程：
（1）建立连接：web客户端发送建立连接的请求，web服务端作出响应。
（2）发送请求：web客户端发送请求内容。
（3）作出应答：web服务端回复html文件。
（4）关闭连接：web客户端收到文件就关闭连接。

### 03.域名
>域名（英语：Domain Name），简称域名、网域，是由一串用点分隔的名字组成的Internet上某一台计算机或计算机组的名称，用于在数据传输时标识计算机的电子方位（有时也指地理位置）。
>网域名称系统（DNS，Domain Name System，将域名和IP地址相互映射的一个分布式数据库）是因特网的一项核心服务，它作为可以将域名和IP地址相互映射的一个分布式数据库，能够使人更方便地访问互联网，而不用去记住能够被机器直接读取的IP地址数串。
>www.wikipedia.org是一个域名，和IP地址208.80.152.2相对应。DNS就像是一个自动的电话号码簿，我们可以直接拨打wikipedia的名字来代替电话号码（IP地址）。我们直接调用网站的名字以后，DNS就会将便于人类使用的名字（如www.wikipedia.org）转化成便于机器识别的IP地址（如208.80.152.2）。

### 04.w3c
>w3c一般指万维网联盟
>万维网联盟创建于1994年，是Web技术领域最具权威和影响力的国际中立性技术标准机构。到目前为止，W3C已发布了200多项影响深远的Web技术标准及实施指南，如广为业界采用的超文本标记语言HTML（标准通用标记语言下的一个应用）、可扩展标记语言XML（标准通用标记语言下的一个子集）以及帮助残障人士有效获得Web信息的无障碍指南（WCAG）等，有效促进了Web技术的互相兼容，对互联网技术的发展和应用起到了基础性和根本性的支撑作用

### 05.WEB的组成
>Web标准是由W3C和其他标准化组织制定的一系列标准的集合。主要包括结构（Structure）、表现（Presentation）和行为（Behavior）三个方面。
>1.结构标准：结构用于对网页元素进行整理和分类，主要包括XML和XHTML两个部分。(决定你是否有个好天然身体)
>2.样式标准：表现用于设置网页元素的版式、颜色、大小等外观样式，主要指的是CSS。(决定你是否打扮的美丽外观)
>3.行为标准：行为是指网页模型的定义及交互的编写，主要包括DOM和ECMAScript两个部分(决定你是否有吸引人的行为)
*理想状态我们的源码： .HTML    .css   .js*

## 四、html概念
### 01.html的历史
>1982年，Tim Berners-Lee 建立 HTML
>1993年6月，HTML 由 IETF 工作小組发布草案
>1994年10月，W3C 成立， 网络应用发展的标准规范交由 W3C 协会制定及推广
>1995年11月，HTML 2.0，2000年6月被宣布已经过时
>1996年1月 ，HTML 3.2 由 W3C 推荐为标准规范
>1997年11月，HTML 4.0
>1999年12月，HTML 4.01 以 XML 语法重新构建，较为严格，W3C推荐标准
>2000年1月，XHTML 1.0，W3C推荐标准
>2001年5月，XHTML 1.1，W3C推荐标准
>2004年，WHATWG小组成立，由各大浏览器开发商组成，重拾HTML 4规格，开发 HTML 5规格
>2006年，W3C认输，承认 XHTML 2.0不会成功
>2007年，W3C重新成立 HTML工作小组，参考 WHATWG 的规格发展期HTML规格
>2009年，XHTML 2.0被放弃，全面投入 HTML 5 规格的发展
>2011年6月，Google宣布全面采用 HTML 5 技术
>2012年， HTML 5被选为候选标准
>2014年10月28日，HTML 5.0，W3C正式发布HTML 5.0推荐标准
### 02.html概念
- HTML是超文本标记语言（Hypertext  Markup Language）
- 超文本指用超链接的方法，将各种不同空间的文字信息组织在一起的网状文本，也指页面内可以包含图片、链接，甚至音乐、程序等非文字元素
- 标记语言是一种将文本以及文本相关的其他信息结合起来，展现出关于文档结构和数据处理细节的电脑文字编码
- 超文本标记语言就是描述文本、图形和包含其他信息的文件组织和链接在一起的方式的一种语言。
### 03.我的第一个html
1).在桌面新建一个txt文件
<img src='https://upload-images.jianshu.io/upload_images/3532891-a0363ebe93fa5f68.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240' width='150'>
2).输入内容
``` html
<html>
	<head>
		<title>01.我的第一个网页</title>
	</head>
	<body>
		今天天气真的好！！！！
	</body>
</html>
```
3).更改后缀名为 html
<img src='https://upload-images.jianshu.io/upload_images/3532891-4183f9938519d704.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240' width='150'>
4).用浏览器打开
<img src='https://upload-images.jianshu.io/upload_images/3532891-6e6c31771c16f9ab.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240' width='200'>
5).书写第一个网页成功

### 04.什么是标签
- HTML 标记标签通常被称为 HTML 标签 (HTML tag)
- HTML 标签是由尖括号包围的关键词，比如 `<html>`
- HTML 标签通常是成对出现的，比如 `<body> `和 `</body>`，标签中的第一个标签是开始标签，第二个标签是结束标签（闭合标签）
- 也有单标签，比如`<br>`、`<input type=’text’ value=’’>`等
- 浏览器不会显示html标签，而是使用标签来解释页面的内容
### 05.注释
``` html
<!DOCTYPE html>
<!--
html注释就是html中 对某一块内容的解释，但是不会被浏览器编译
注释的快捷键  ctrl+/  或者 ctrl+shift+/
如果多行注释，可以全部选中然后按快捷键ctrl+shift+/
-->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

</body>
</html>
```
### 06.html结构及具体作用
``` html
<!DOcTyPE html>
<!--
    DOCTYPE（document type）： 文档类型
    1.版本声明。
    2.给浏览器声明，告诉浏览器应该按照html5的规范来解析当前的文档。
    3.如果不书写，那么按照什么规范解析，就看浏览器心情
    4.必须定义在 HTML 文档的第一行，在 HTML 标签之前
    5.<!DOCTYPE html> 不是html标签，他只是一条浏览器的指令，在所有版本中，这条指令对大小写都不敏感
-->
<html lang="en">
<!--
    1.HTML 标记标签通常被称为 HTML 标签 (HTML tag)
    2.这个标签告诉浏览器这个是HTML 文档的开始，最后一个标签是</html>，这个标签告诉浏览器这个是终止。
    3.html标签是网页结构的最外层 里边包含两个标签  body 和 head 
    4.lang是语言  en是英语  告诉浏览器本网页是英文网页  ch是中文
    5.lang是html的属性   en是lang属性的值
-->
<head>
    <!--
        1.head代表网页的头部，不会显示网页中
        2.只要包含网页的元信息，标题，引入外部文件等等
    -->
    <meta charset="UTF-8">
    <!--
        meta标签是控制网页的元信息
        元信息就是信息的信息（关于当前网页的信息）
        charset代表字符编码，utf-8是万国码
        补充：
            gb2312 简单中文  包括6763个汉字
            BIG5   繁体中文 港澳台等用
            GBK包含全部中文字符，是GB2312的扩展，加入对繁体字的支持，兼容GB2312

        UTF-8则包含全世界所有国家需要用到的字符，以后我们统统使用UTF-8 字符集, 这样就避免出现字符集不统一而引起乱码的情况了
    -->
    <meta name=“keywords” content=“”>
    <!--设置网页关键字，为搜索引擎提供的关键字列表，各关键词间用英文逗号“,”隔开-->
    <meta name=“description” content=“”>
    <!--设置网页描述,用来告诉搜索引擎你的网站主要内容-->
    <title>html的编码结构</title>
    <!--title是网页的标题,显示在浏览器标签页的标题中-->
</head>
<body>
    <!--在html中，所有我们能够看到的内容全部书写在body中-->
</body>
</html>
```
### 07.其他版本声明(已经弃用)
<img src='https://upload-images.jianshu.io/upload_images/3532891-c865a1089284a17f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240'>
<img src='https://upload-images.jianshu.io/upload_images/3532891-ee55fdf9d4a9199a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240'>
<img src='https://upload-images.jianshu.io/upload_images/3532891-f7e1f59252c8e86b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240'>

### 08.HTML标签及标签的分类
> 1.html标签又叫做html元素，它分为块级元素和内联元素（也可以叫做行内元素），都是html规范中的概念。
> 2.html标签还被分为 不可替换元素和替换元素
> 3.html还被分为 空元素（void） 和 非空元素

### 09.html标签的关系
标签的相互关系就分为两种：
1.嵌套关系

``` html
<!--
    div元素是p元素的父元素
    p元素是div元素的子元素
    div元素是span元素的祖宗元素
    span是div的后代与元素
-->
<div>
    <p> 
        <span></span >
    </p>  
</div>
```

2.并列关系(兄弟关系)

```html
<!--
    head是body的上一个兄弟元素
    body是head的下一个兄弟元素
-->
<head></head>
<body></body>
```
**如果两个标签之间的关系是嵌套关系，子元素最好缩进一个tab键的身位（为了多个代码统一管理，我们可以设置一个tab代表多少空格元素）。如果是并列关系，最好上下对齐。**

## 五、html部分块级元素（html5之前版本提出的元素）
### 01.div元素
>整体页面布局当中最重要的 HTML 元素
>没有任何具体的含义，主要用于网页的布局，通过一个一个的div将页面划分为不同的部分，之后在针对部分进行开发
案例：把下图的网页进行分块
<img src='https://upload-images.jianshu.io/upload_images/3532891-63e545aef6ca17fc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240' width='300'>
<img src='https://upload-images.jianshu.io/upload_images/3532891-113ea8a93469a245.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240' width='500'>
```html
<!DOCTYPE HTML>
<html>
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <!--div标签：没有任何具体的含义，主要用于网页的布局，
    通过一个一个的div将页面划分为不同的部分，之后在针对部分进行开发-->
    <!--网页分块要求：先分行 在分列-->

    <!--网页的最外层-->
    <div>
        <!--头部区域-->
        <div>
            我是头部
        </div>

        <!--导航区域-->
        <div>
            我是导航
        </div>

        <!--主要内容区域-->
        <div>
            <!--主要内容上部分-->
            <div>
                上部分
            </div>
            <!--主要内容下部分-->
            <div>
                <!--内容左-->
                <div>内容左</div>
                <!--内容右-->
                <div>内容右</div>
            </div>
        </div>

        <!--底部区域-->
        <div>
            底部区域
        </div>
    </div>
</body>
</html>
```

### 02.标题标签
> - h1～h6 标签分别表示不同级别的标题，`<h1>`定义最大的标题，`<h6>`定义最小的标题。
> - 在浏览器默认状态下，每种标题均为加粗效果，各自对应不同的文字大小

案例：
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>标题标签</title>
</head>
<body>
<div>
   <!-- ctrl+d 复制整个一行-->
    <h1>1级标题</h1>
    <h2>2级标题</h2>
    <h3>3级标题</h3>
    <h4>4级标题</h4>
    <h5>5级标题</h5>
    <h6>6级标题</h6>

    <!--标题样式 字号大小：由大到小  默认加粗状态
    默认上下有一定的间隙-->

    标题:
        1、不要因为标题的字号大小很小，而使用低级别的标题 字号大小可以通过css的font-size来控制
        2、尽量避免跳过某一级标题，依次使用
        3、需要避免在同一个网页中多次使用h1元素，h1经常用在网页的标题或者是logo上
</div>
</body>
</html>
```
<img src='https://upload-images.jianshu.io/upload_images/3532891-0d3f7c615d645df4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240' width=300>

### 03.段落标签和换行标签
> - p 标签用于定义一个段落 `<p></p>`
> - `<br>`标签表示换行，为单标签，通常出现在 p 标签中
> - 每个p标签表示一个段落，而使用 br 标签换行，通常被称为软换行，段落的文本从一个新行开始，但是这些文本依旧是一个段落
> - br不要来增加文本之间的间隙 我们可以使用css的margin来代替
> - br标签是一个单标签  也是一个空元素,早期版本 <br /> 但是在h5中，已经把/给省略了
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!--meta标签是一个空标签  单标签-->
    <title>p标签</title>
</head>
<body>
    <div>
        <h2>html5XXXXXXXXXX</h2>
        <p>
            html5是html语言的第五次重大修改。。。。 html5 <br>是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次
            <br>重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5
            <br>是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语 <br>言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。 html5是html语言的第五次重大修改。。。。
        </p>

        <p>html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀html5前端开发工程师很香呀</p>

    </div>
</body>
</html>
```
<img src='https://upload-images.jianshu.io/upload_images/3532891-b83d80606c9b3049.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240'>

### 04.小练习（气象新闻）
<img src='https://upload-images.jianshu.io/upload_images/3532891-fcd6aa793fad4507.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240'>
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>气象新闻练习</title>
</head>
<body>
    <div>
        <h1>40.6摄氏度： 上海创出140年气象史上高温新纪录</h1>
        <p>2013年07月27日</p>

        <!--hr标签代表一个横线-->
        <hr>

        <div>
            style属性是给某个标签添加样式，本案例为添加一个背景颜色（后期课程学习）
            <p style="background-color: #fffbb5;">新华网上海７月２６日电（记者李荣）２６日１３时３６分至４７分这一时间段，上海徐家汇气象观测站测得当日最高温达４０．６摄氏度。这是上海有气象记录以来１４０年的高温新纪录，打破了此前１９３４年创下的４０．２摄氏度的历史极值。</p>
            <p style="background-color: #655280;">上海已经连续２天发出了最高等级的红色高温警报。上海中心气象台首席服务官满莉萍说，今年副热带高压强度特别强，对上海及江南地区的控制“实在太稳定了”，整个７月份基本上都处在它的势力范围之内。２５日上海已出现了气象史上７月份“第四高”的高温值，这使得２６日的“基础”气温就很高，超过了３０摄氏度，然后不断地升温。此外，２６日白天风小，又吹的是西南风，特别是在中午之后这一个最易出现高温的时段，光照又比较强，所以气温“直线飙升”，一举冲破历史极值，出现了“创纪录”的极端酷暑天。</p>
            <p style="background-color: #ff6da2;">在上海历史上，出现４０摄氏度以上极端高温的几率并不大。根据相关资料，中心城区徐家汇观测站１４０年来仅出现了５次记录，除了这一次的新纪录，还有就是１９３４年７月１２日的４０．２摄氏度；１９３４年８月２５日、２００９年７月２０日、２０１０年８月１３日的４０摄氏度。</p>
            <p style="background-color: #5df2ff;">由于气温实在太高，上 海２ ６日下午不少地区出现了热对流天气。气象台说，首先是浦东地区，下起了热雷雨。到１５时０５分，全市大部分地区出现了分散性的雷电活动和热雷雨，中心城区徐家汇等地都响起了隆隆的雷声。</p>
        </div>
    </div>
</body>
</html>
```

### 05.有序列表和无序列表
> - ul 表示无序列表，示出是带有项目符号列表
> - ul元素前边的符号可以是任何的形式 ,我们可以通过css的list-style-type属性控制
> - 没有规定ul和li嵌套的深度

> - ol 表示有序列表，显示出是带有编号的列表
> - ol元素前边的编号可以是任何的形式  我们可以通过css的list-style-type属性控制
> - 没有规定ul和li嵌套的深度

> - 无论是 ul 还是 ol ，列表中每个具体的列表项都使用的是 li 标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>ol标签和ul标签</title>
</head>
<body>
<div>
    <!--ol元素表示多个有序的列表项  显示出是带有编号的列表
        ol元素前边的编号可以是任何的形式  我们可以通过css的list-style-type属性控制
        没有规定ol和li嵌套的深度
    ul元素表示多个无序的列表项  显示出是带有项目符号列表
        ul元素前边的符号可以是任何的形式  我们可以通过css的list-style-type属性控制
        没有规定ul和li嵌套的深度

    无论是ol还是ul 里边的每一项都是一个li标签-->

    <div style="background-color: red;font-size: 30px;">
        <h2>尚硅谷校区时间排名</h2>
        <ol>
            <li>北京校区</li>
            <li>深圳校区</li>
            <li>上海校区</li>
            <li>武汉校区</li>
            <li>郑州校区</li>
        </ol>
    </div>


    <div>
        <h2>你喜欢吃的东西有哪些</h2>
        <ul>
            <li>上海红烧肉</li>
            <li>北京卤煮</li>
            <li>北京豆汁</li>
            <li>柳州螺蛳粉</li>
        </ul>
    </div>
</div>
</body>
</html>
```
<img src=https://upload-images.jianshu.io/upload_images/3532891-f986dc45f7e7ecec.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=800>

### 06.ul和ol的其他用法
> ul和ol也可以用于**重复结构**的 大块内容布局

>比如下图的案例：
><img src=https://upload-images.jianshu.io/upload_images/3532891-827cbf46e16b95af.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=400>
><img src=https://upload-images.jianshu.io/upload_images/3532891-fa95c84b24bedad2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=400>

>案例：完成下图结构
><img src=https://upload-images.jianshu.io/upload_images/3532891-32ca2dd57cdf62be.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=200>
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>ul和ol的用法</title>
</head>
<body>
    <!--
        ul、ol和li的使用规范：
        1、ul li   ol li  是组合标签
        2、ol或ul的子元素 必须只能是li
        3、li的父元素只能是ol或ul
        4、根据规范，不建议在ul和li嵌套的中间 书写其他元素
        5、li中可以嵌套任何元素
    -->
    <div>
        <h1>前端工程师招聘列表</h1>
        <ul>
            <li>
                <h2>UI前端工程师</h2>
                <p>
                    <span>20K-30K</span>
                    <span>深圳-南山区</span>
                </p>
                <p>求贤若渴</p>
            </li>
            <li>
                <h2>UI前端工程师</h2>
                <p>
                    <span>20K-30K</span>
                    <span>深圳-南山区</span>
                </p>
                <p>求贤若渴</p>
            </li>
            <li>
                <h2>UI前端工程师</h2>
                <p>
                    <span>20K-30K</span>
                    <span>深圳-南山区</span>
                </p>
                <p>求贤若渴</p>
            </li>
            <li>
                <h2>UI前端工程师</h2>
                <p>
                    <span>20K-30K</span>
                    <span>深圳-南山区</span>
                </p>
                <p>求贤若渴</p>
            </li>
            <li>
                <h2>UI前端工程师</h2>
                <p>
                    <span>20K-30K</span>
                    <span>深圳-南山区</span>
                </p>
                <p>求贤若渴</p>
            </li>
        </ul>
    </div>
</body>
</html>
```

### 07.自定义列表
> - 定义列表包括 dl 、dt 、dd 三种标签
> - 自定义列表是包含 术语 和 对术语描述 的列表 ，通常用来展示词汇表或者是对内容的解释
> - 其中 dl 标签表示定义列表，dt标签表示定义列表的标题，dd 标签定义了列表的内容
> - dl dt dd是组合标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>定义列表dl</title>
</head>
<body>
    <div>
        <dl>
            <dt>html5</dt>
            <dd>html5是在2014年10月29日宣布完成</dd>
        </dl>
    </div>
</body>
</html>
```
<img src=https://upload-images.jianshu.io/upload_images/3532891-7a1e9677d60e43e2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 08.自定义列表的用法
> - 1、单条解析和描述
> - 2、多条术语的描述
> - 3、对一个术语 进行多次描述
> - 4、在一个dl中 可以有多个 术语-解析  这样的格式（类似键值对）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>定义列表dl的用法</title>
</head>
<body>
    <div>
        <!-- dl dt  dd的组合用法
            dt和dd是兄弟关系，父元素只能是dl
            dl的子元素只能是 dt和dd  
        -->


        <!--单条解析和描述-->
        <dl>
            <dt>html5</dt>
            <dd>html5是在2014年10月29日宣布完成</dd>
        </dl>

        <!--多条术语的描述-->
        <dl>
            <dt>html5</dt>
            <dt>css3</dt>
            <dt>js</dt>
            <dd>
                他们仨结合起来就是传说中的网页三剑客
            </dd>
        </dl>


        <!--对一个术语 进行多次描述-->
        <dl>
            <dt>html5</dt>
            <dd>html是真的好啊</dd>
            <dd>学了html5  每天天气真的好</dd>
        </dl>

        <!--在一个dl中 可以有多个 术语-解析  这样的格式（类似键值对）-->
        <dl>
            <dt>html5</dt>
            <dd>html5 好啊</dd>

            <dt>css3</dt>
            <dd>css3 真好啊</dd>

            <dt>js</dt>
            <dd>js 真的很简单</dd>
        </dl>
    </div>
</body>
</html>
```

### 09.hr标签
1、h5规范：语义表示段落之间的主题转换，并不仅仅用在表现层上
2、旧版本中：他仅仅就是一个横线 只是表现层  没有什么语义
3、横线默认和父级一样宽
4、其实hr标签的表现是一个高度为0  宽度和父级一样宽的元素  拥有上下左右各1像素的边框
5、所以默认hr的线高度是2px
6、我们可以通过css来控制hr的样式
注意：
    在实际开发中，一条线常用的写法是  边框  或者是  一个空的div标签 设置高度和背景颜色即可

```html
<hr>
```
<img src=https://upload-images.jianshu.io/upload_images/3532891-37ce15a5f2d6b071.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=150>

### 10.一条线的其他做法
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>一条线</title>
</head>
<body>
    <!--第一种：空标签-->
    <div style="height: 1px;background-color: red;"></div>

    <!--第二种：边框-->
    <div style="border-bottom: 1px solid pink;margin-top: 100px;"></div>
</body>
</html>
```
<img src=https://upload-images.jianshu.io/upload_images/3532891-87d71600cb8f3960.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=400> 

### 11.块标签的特性
> 1.独占一行，换行显示
> 2.可以设置宽高
> 3.在不手动设置宽度的情况下，宽度默认为所在容器的100%（即容器宽度）
> 4.可以容纳行内元素和其他块元素(p标签、h标签都只能嵌套行元素或行内块元素)


## 六、html部分内联元素（html5之前版本提出）
### 01.span元素
- 没有任何特殊的含义
- 主要是为了增加额外的结构，方便我们控制样式或者是数据
- 并且使用要求：在其他语义化标签不适用的情况下再使用
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>span</title>
</head>
<body>
    <div>
        <h1>夏威夷三日游</h1>
        <!-- 增加了额外的结构 -->
        <p>价格<span style="color:red;">382</span>元</p>
    </div>
</body>
</html>
```
### 02.b、i、u元素
> - b标签呈现加粗状态
> - i标签呈现倾斜状态
> - u标签呈现下划线状态

> - 这三个标签是吸引读者到需要注意的内容上
> - 这些仅仅是添加了一些样式而已，只是表现层
> - 尽管如此，我们也不必为了加粗倾斜等元素 而去使用b i u等标签，替代的方法是使用css

> - 在目前使用最多的是i标签-通常在开发过程中，小图标之类的元素我们习惯用i标签来表示
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>b i u</title>
</head>
<body>
    
    <div>
        <b>我是小b</b>
        <i>我是小i</i>
        <u>我是小u</u>
    </div>
</body>
</html>
```
### 03.em、strong、var元素
> - em标签-强调作用：标出用户着重需要阅读的内容，但是主要也给SEO（搜索引擎优化）强调，呈现的是倾斜的状态
> - strong-强调（更强的强调）作用：表示文本十分重要，主要也给SEO（搜索引擎优化）强调，呈现的是一个加粗

> - em对某一个关键词强调
> - strong代表更强:比如 对某一句话直接强调

> - var标签 并没有起到强调或提示用户注意的作用。默认倾斜。var的语义是 包含变量的
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>em strong var</title>
</head>
<body>
<div>
    <!--em对某一个关键词强调-->
    <span>我<em>喜欢</em>男的！！！</span>
    <span>我喜欢<em>男的</em>！！！</span>

    <!--strong代表更强:比如 对某一句话直接强调-->
    <strong>警告:你们老师喜欢男的!!!</strong>

    <!--var标签 -->
    <p>小明有<var>x</var>个苹果，一天吃一个，一天吃完，请问<var>x</var>等于几</p>
    <p><var>x</var>+<var>y</var>=12</p>
</div>
</body>
</html>
```
### 04.a标签
#### 01)路径
##### 绝对路径
>1.完整的描述文件位置的路径就是绝对路径，以web站点根目录为参考基础的目录路径。
>2.绝对路径名的指定是从树型目录结构顶部的根目录开始到某个目录或文件的路径，由一系列连续的目录组成，中间用斜线分隔，直到要指定的目录或文件，路径中的最后一个名称即为要指向的目录或文件。
>3.之所以称为绝对，意指当所有网页引用同一个文件时，所使用的路径都是一样的
>4.比如`file:///C:/Users/lipeihua/Desktop/code/01.html` 就是一个绝对路径
>5.**在前端开发中是不会使用绝对路径的**
##### 相对路径
>1.相对路径就是指由这个文件所在的路径引起的跟其它文件（或文件夹）的路径关系。使用相对路径可以为我们带来非常多的便利。

>./ ：代表文件所在的目录（可以省略不写）
>../ ：代表文件所在的父级目录
>../../ ：代表文件所在的父级目录的父级目录
>/ ：代表文件所在的根目录,可以理解成项目内部的绝对路径。
##### 相对路径练习：
>01.html和outer是同级兄弟关系，02.html和inner是同级兄弟关系，03.html和content是同级兄弟关系
<img src=https://upload-images.jianshu.io/upload_images/3532891-b825cf2a45a4ba43.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=200>
```html
<!-- 01.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <h1>01.html</h1>
    <a href="./outer/02.html">02</a>
    <a href="./outer/inner/03.html">03</a>
</body>
</html>
```

```html
<!-- 02.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <h1>02</h1>
    <a href="../01.html">01</a>
    <a href="./inner/03.html">03</a>
</body>
</html>
```

```html
<!-- 03.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <h1>03</h1>
    <a href="../../01.html">01</a>
    <a href="../02.html">02</a>
</body>
</html>
```
##### 网络路径
> 如果需要链接网络上的资源的时候，可以使用网络路径
`http://www.baidu.com`

#### 02).a标签的基础用法
>1.a标签用来做跳转
>2.a标签就是超链接：可以创建通向其他网页  文件 同一个页面的位置 邮件地址 或者其他url链接 链接电话  链接短信
>3.a标签的href属性，用来写地址:如果是网络地址 需要写全`http://`或者`https://`协议。如果写本地地址，使用相对路径即可
>4.title属性：是鼠标悬浮在a链接上的时候，对当前链接的提示信息，弹窗显示
>5.target属性：`_self`:在当前标签页跳转; `_blank`:在新的标签页打开跳转
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>a标签</title>
</head>
<body>
    <div>

        <a href="http://www.baidu.com" title="" >百度一百下你也不知道</a>

        <a href="###" title="尚硅谷前端就业连续9期百分百就业 666666">尚硅谷大数据就业连续9期...</a>

        <a href="http://www.baidu.com" target="_blank">百度一百下你也不知道</a>
    </div>
</body>
</html>
```
<img src=https://upload-images.jianshu.io/upload_images/3532891-f3636c2d26a4c794.gif?imageMogr2/auto-orient/strip>

#### 03).a标签的锚链接
>锚链接的两种效果：
>1.在当前页面中跳转.：通过元素的ID进行跳转 `<a href="#name"></a>`
>在a标签的href中书写 #+名字(自由命名，注意规范)
>在相对应的跳转点标签 书写id属性  值为 锚链接中的名字
>这样点击锚链接就能跳转到相对应的位置
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>a标签的锚链接</title>
</head>
<body>
<div>
    <!--position: fixed;相对浏览器窗口定位 无论滚动条是否滚动，此元素位置不改变
    right是距离浏览器窗口右边为0
    top是距离浏览器窗口顶部为100px-->
    <div style="position: fixed;right: 0;top: 100px;">
        <p><a href="#news">新闻</a></p>
        <p><a href="#yule">娱乐</a></p>
        <p><a href="#smile">搞笑</a></p>
        <p><a href="#tiyu">体育</a></p>
        <p><a href="#my">我的</a></p>
    </div>
    <ul>
        <li style="height: 600px;background-color: red;" id="news">新闻</li>
        <li style="height: 600px;background-color: #ffca71;" id="yule">娱乐</li>
        <li style="height: 600px;background-color: #6559ff;" id="smile">搞笑</li>
        <li style="height: 600px;background-color: #beffbd;" id="tiyu">体育</li>
        <li style="height: 600px;background-color: #d0ffb9;" id="my">我的</li>
    </ul>
</div>
</body>
</html>
```
<img src=https://upload-images.jianshu.io/upload_images/3532891-f6b93bc56f1c82c9.gif?imageMogr2/auto-orient/strip>
>2.网页中的返回顶部效果：`<a href="#"></a>`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>回到顶部</title>
</head>
<body>
<div>
    <div class="con" style='height: 1000px;background-color: red;'>我很高，生成滚动条了</div>
	<a href="#">点击我回到顶部</a>
</div>
</body>
</html>
```
<img src=https://upload-images.jianshu.io/upload_images/3532891-9851005fdc97b9d5.gif?imageMogr2/auto-orient/strip>
#### 04).a标签的其他功能
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>a标签的其他功能</title>
</head>
<body>
<!--a标签下载：
    1.当连接的文件能够使用浏览器打开，那么可以进行打开，否则将直接下载
    2.也可以给a标签一个download属性 书写下载文件的路径，那么可以直接下载
    3.a标签必须书写href属性，哪怕为空都可以执行download下载，否则a标签不具有任何功能
 -->
<a href="" download="../images/01.png">点击下载图片</a>
<a href="../note/9.10_html02.pptx">点击下载图片</a>

<!--a标签对电话短信email的支持 主要针对移动端
    1.a标签的打电话是在href属性中书写   tel:电话号码  这样的格式
    2.a标签的发短信是在href属性中书写   sms:电话号码  这样的格式
    3.a标签的发送邮件是在href属性中书写 mailto:邮箱地址 这样的格式
-->
<a href="tel:15701665563">给李沛华打电话</a>
<a href="sms:15701665563">给李沛华发短信</a>
<a href="mailto:lipeihua@atguigu.com">给李沛华发邮件</a>
</body>
</html>
```

### 05.行内元素的属性
>1.在一行中如有剩余空间，允许同其他 行内/行内块 标签公用一行
>2.不可以直接设置宽高（宽高无效）,默认的宽高由内容决定
>3.内容过多时允许换行并断开（一般都是用于处理文字样式）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>行标签属性</title>
</head>
<body>
    <div>
        <!-- 宽度无效 -->
        <span style="width: 20000000px;height: 100px;background-color: red;">span111</span>
        <b>b111</b>
        <i> i1111</i>
        <var>var111</var>
    </div>
</body>
</html>
```
## 七、表单元素
### 01.form元素
> - 为用户创建html表单
    表单可以向服务器发送数据
    form标签中可以包含很多表单元素
``` html
<form action="http://www.baidu.com" method="get">
```
>- action属性：
    表单提交的地址
> - method属性：
    表单提交的方式  数据传输的方式
    常见的两种方式是 get和post

    ~~~(简单了解)理解：get可以当成小汽车：数据少   数据直接在地址栏上显示（不安全）
    post可以当成大货车：数据多  数据发送相对于get安全一点
    ~~~

### 02.表单的提交
> - 表单提交需要在表单中书写`提交按钮`。
> - 提交按钮可以是 
`<button type=submit></button>` 或
`<input type=submit value='' >`
> - 提交按钮只会提交当前按钮所在的form表单中的内容
    如果没有form标签，表单提交失效
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>form标签</title>
</head>
<body>
    <form action="http://www.baidu.com" method="get">
        <!--表单元素-->

        <!--input标签的type类型是submit代表提交  value是按钮显示的内容-->
        <!-- 本次提交为空 -->
        <input type="submit" value="提交">
    </form>
</body>
</html>

```
### 03.html4表单的类型
>input：
>type类型的值不一样，呈现的状态也是不一样的

    text：
        单行文本输入框（文本域）
        没有长度和内容限制，只能输入一行，明文显示
        表单提交都是以键值对的形式提交的  比如  user = lipeihua
    
        name属性就是给表单起一个名字（自己命名，一般是后台提供）
        value属性就是表单的值，可以预定义 也可以等待用户输入
        name和value就构成了一个键值对
        如果构不成一个键值对，就不会进行提交
    
    password：
        密码输入框
        默认吧输入的内容呈现出小黑点
    
    radio：
        单选框
        书写name属性后，可以进行单选
        应该书写value值，是向后台提供的数据
        在input前写的内容，和input没有任何关系，只不过让用户视觉上觉得有关联
    
    checkbox：
        多选框
        其他同单选框
    
    file:
        上传文件按钮
    
    hidden：
        提交隐藏内容
        在表单提交过程中有的数据需要提交，但是不需要用户输入或者是修改，那么直接使用隐藏域提交


    button:
        单纯的按钮，没有任何作用和功能，只是长了按钮的样子
        如果需要添加功能，可以使用js
        value值是按钮中的文字


    reset:
        重置按钮
        当重置按钮被点击，就会重置当前reset所在的表单，变成默认的状态
    
    submit：
        提交按钮
        input标签的type类型是submit代表提交  value是按钮显示的内容
        提交按钮只会提交当前按钮所在的form表单中的内容
        如果没有form标签，表单提交失效  

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>form标签</title>
</head>
<body>
    <form action="http://www.baidu.com" method="get">
        请输入用户名：
        <input type="text" name="user" value="lipeihua">
        <br>
        
        请输入密码：
        <input type="password" name="pass" value="">
        <br>

        请选择性别：
        男：<input type="radio" name="sex" value="男">
        女：<input type="radio" name="sex" value="女">
        未知：<input type="radio" name="sex" value="未知">
        <br>
        
        选择你最喜欢的语言：
        PHP：<input type="checkbox" name="lang" value="PHP">
        JAVA：<input type="checkbox" name="lang" value="JAVA">
        JS：<input type="checkbox" name="lang" value="JS">
        HTML：<input type="checkbox" name="lang" value="HTML">
        <br>

        请上传你的照片：
        <input type="file" name="photo">
        <br>

        <input type="hidden" name="id" value="00000000001">

        <input type="button" value="点我啊" id="btn">

        <br>

        <input type="reset" value="重置啊">

        
        <input type="submit" value="提交">
    </form>
    <script>
        var oBtn = document.getElementById("btn");
        oBtn.onclick = function () {
            alert("hello world");
        }
    </script>
</body>
</html>
```
### 04.其他表单元素
    select&option
        下拉列表
        option代表列表的每一项
            显示出来的值应该放在option标签中
            提交的内容是放在option的value属性中
       select是列表的外层
            表单的name是在select中书写
    
    textarea：
       多行文本输入框
       右下角可以放大缩小
       cols和rows用来控制宽和高
            cols代表一行有几个字符（一个汉字算两个字符）
            rows代表总共几行，超出是要生成滚动条的
            但是：我们很少这样控制，主要通过css的width和height控制
        textarea没有value属性，输入的值直接就是textarea标签中的内容
    
    button：
        HTML <button> 元素表示一个可点击的按钮，可以用在表单或文档其它需要使用简单标准按钮的地方。 默认情况下，HTML按钮的显示样式接近于 user agent 所在的宿主系统平台（用户操作系统）的按钮， 但你可以使用 CSS 来改变按钮的样貌。
    
        type：button的类型。可选值：
            submit:  此按钮将表单数据提交给服务器。如果未指定属性，或者属性动态更改为空值或无效值，则此值为默认值。
            reset:  此按钮重置所有组件为初始值。
            button: 此按钮没有默认行为。它可以有与元素事件相关的客户端脚本，当事件出现时可触发。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>其他表单元素</title>
</head>
<body>
<form action="###" method="get">
    请选择你喜欢的城市
    <select name="city" >
        <option value="北京">北京</option>
        <option value="上海">上海</option>
        <option value="深圳">深圳</option>
        <option value="草围">草围</option>
    </select>

    <br>
    
    请说出你对我们的留言：
    <textarea name="message" cols="30" rows="10" ></textarea>

    <button></button>
    <input type="submit" value="提交">
</form>
</body>
</html>
```

### 05.button和input的区别
    在 button 元素内部，可以放置文本或图像。这是<button>与使用 input 元素创建的按钮的不同之处。
    
    二者相比较， <button> 控件提供了更为强大的功能和更丰富的内容。
    <button> 与 </button> 标签之间的所有内容都是按钮的内容，其中包括任何可接受的正文内容，比如文本或多媒体内容。
    例如，我们可以在按钮中包括一个图像和相关的文本，用它们在按钮中创建一个吸引人的标记图像。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>button</title>
</head>
<body>
<form action="###" method="get">
    <input type="text" name="user" value="">

    <button type="button">点击我呀</button>
    <button type="button">
        <img src="../images/06.png" alt="">
    </button>
</form>
</body>
</html>
```
### 06.获取焦点和失去焦点
`获取焦点`：
    当表单元素变成一个可以输入的状态的时候，被称作为获取焦点
`失去焦点`：
    当表单元素失去可以输入状态的时候，被称作为失去焦点
    

### 07.label标签
    label元素：
        为表单元素定义标注（点击标注的信息，可以让表单元素获取焦点）
    
    两种使用方法：
        一、
            label标签包含住标注元素，
            让label标签的for属性 和 被标注的表单元素的id属性 值相等
    
        二、
            label标签包住整个 标注元素 和 相对应的表单元素
            label不能出现for属性

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>button</title>
</head>
<body>
<form action="###" method="get">

    <label for="user">请输入用户名：</label>
    <input type="text" name="user" value="" id="user">


    <label>
        男 <input type="radio">
    </label>


    <button type="submit">点击我呀</button>

</form>
</body>
</html>
```
### 08.label标签包含其他元素
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>button</title>
</head>
<body>
    <!--

        label元素：
            可以标注input表单元素

            对select来说 只能获取焦点，但是不能把列表下拉出来

    -->
<form action="###" method="get">

    <label for="city">选择城市</label>
    <select name="city" id="city">
        <option value="北京">北京</option>
        <option value="上海">上海</option>
        <option value="广州">广州</option>
    </select>

    <label for="mes">留言</label>
    <textarea name="mes" id="mes" cols="30" rows="10"></textarea>
    

    <button type="submit">点击我呀</button>

</form>
</body>
</html>
```
## 八、table元素
### 01.table元素的基础元素
    HTML的 table 元素表示表格数据 — 即通过二维数据表表示的信息
    一个可选的 <caption> 元素
    一个可选的 <thead> 元素
    下列任意一个:
        零个或多个 <tbody>
        零个或多个 <tr>
        零个或多个 <th>
        零个或多个 <td>
        一个可选的 <tfoot> 元素
### 02.table的基础使用
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>table</title>
</head>
<body>
    <!--
        表格书写：
            table是表格的最外层
            caption：HTML <caption> 元素 (or HTML 表格标题元素) 展示一个表格的标题， 它常常作为 <table> 的第一个子元素出现，同时显示在表格内容的最前面
            tr就是表格的每一行
            th表示表头单元格  默认居中和加粗
            td表示普通单元格
    -->

    <table>
        <caption>1108班就业表</caption>
        <tr>
            <th>姓名</th>
            <th>就业薪资</th>
            <th>备注</th>
        </tr>
        <tr>
            <td>小王</td>
            <td>12</td>
            <td></td>
        </tr>
        <tr>
            <td>老王</td>
            <td>13</td>
            <td></td>
        </tr>
        <tr>
            <td>王中王</td>
            <td>14</td>
            <td></td>
        </tr>
        <tr>
            <td>大王</td>
            <td>15</td>
            <td></td>
        </tr>
    </table>
</body>
</html>w
```
### 03.table的常用属性
    border：（废弃） 
    这个整型元素使用像素，定义了表格边框的大小。
    如果设置为1，表示表格具有1px大小的边框。
    
    cellpadding ：（废弃）
    这个属性定义了表格单元的内容和边框之间的空间。如果它是一个像素长度单位，这个像素将被应用到所有的四个侧边
    
    cellspacing ：（废弃）
    这个属性（使用百分比或像素）定义了两个单元格之间空间的大小（从水平和垂直方向上）
    
    width ：（废弃）
    该属性定义了表格的宽度。宽度可能是一个像素或者是一个百分比值，宽度的百分比值将被定义为表格容器的宽度。
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>table</title>
</head>
<body>
    <table width="400" border="1" style="" cellpadding="10" cellspacing="10">
        <caption>0225班就业表</caption>
        <tr>
            <th>姓名</th>
            <th>就业薪资</th>
            <th>备注</th>
        </tr>
        <tr>
            <td>小王</td>
            <td>12</td>
            <td></td>
        </tr>
        <tr>
            <td>老王</td>
            <td>13</td>
            <td></td>
        </tr>
        <tr>
            <td>王中王</td>
            <td>14</td>
            <td></td>
        </tr>
        <tr>
            <td>大王</td>
            <td>15</td>
            <td></td>
        </tr>
    </table>
</body>
</html>
```

### 04.合并单元格
    合并单元格：
            colspan:设置跨列，谁合并，给谁设置
    
            rowspan：设置跨行,谁合并，给谁设置
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>table</title>
</head>
<body>
    <table width="400" border="1" style="border-collapse:collapse;" cellpadding="10" cellspacing="0">
        <caption>0225班就业表</caption>
        <tr>
            <th colspan="2">学生就业就业薪资</th>
            <th>备注</th>
        </tr>
        <tr>
            <td>小王</td>
            <td>12</td>
            <td></td>
        </tr>
        <tr>
            <td>老王</td>
            <td rowspan="2">13</td>
            <td></td>
        </tr>
        <tr>
            <td>王中王</td>
            <td></td>
        </tr>
        <tr>
            <td>大王</td>
            <td>15</td>
            <td></td>
        </tr>
    </table>
</body>
</html>
```
### 05.表格的优化
    thead　表格的头        用来放标题之类的东西
    tbody　表格的身体    放数据本体 
    tfoot　 表格的脚       放表格的脚注之类
    
    为了让大表格(table)在下载的时候可以分段的显示,就是说在浏览器解析HTML时，
    table是作为一个整体解释的，使用TBODY可以优化显示。如果表格很长，用tbody分段，
    可以一部分一部分地显示，不用等整个表格都下载完成
    
    TBODY包含行的内容下载完优先显示，不必等待表格结束.另外，还需要注意一个地方。表格行本来是从上向下显示的。但是，应用了thead/tbody/tfoot以后，就“从头到脚”显示，不管你的行代码顺序如何。也就是说如果thead写在了tbody的后面，html显示时，还是以先thead后tbody显示。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表格的优化</title>
</head>
<body>
    <!--
        表格的优化
            thead
            tbody
            tfoot
    -->
    <table>
        <thead>
            <tr>
                <td>
                    1
                </td>
            </tr>
            <tr></tr>
            <tr></tr>
        </thead>
        <tbody>
            <tr>
                <td>2</td>
            </tr>
            <tr></tr>
            <tr></tr>
            <tr></tr>
        </tbody>
        <tbody>
            <tr></tr>
            <tr></tr>
            <tr></tr>
            <tr></tr>
            <tr></tr>
        </tbody>

        <tfoot>
            <tr></tr>
            <tr></tr>
            <tr></tr>
        </tfoot>

    </table>
</body>
</html>
```
## 九、iframe元素
### 01.iframe元素概念
>HTML内联框架元素 (`<iframe>`)它能够将另一个HTML页面嵌入到当前页面中。
>
>每个嵌入的浏览上下文（embedded browsing context）都有自己的会话历史记录(session history)和DOM树。包含嵌入内容的浏览上下文称为 **父级浏览上下文**。
>
>**顶级浏览上下文**（没有父级）通常是由 Window 对象表示的浏览器窗口。

>页面上每个`<iframe>`都会需要包括内存在内的额外计算资源，这是因为每个浏览上下文都拥有完整的文档环境。虽然理论上来说你能够在代码中写出来无限多的`<iframe>`，但是你最好还是先看看这么做会不会导致某些性能问题。
### 02.iframe元素使用
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset=UTF-8>
    <tItle>Title</tItle>
</head>
<body>
    <!--
        iframe标签：
            1、src是嵌入html的地址  可以是网络  也可以是本地服务器
            2、width和height属性来设置内联框架的宽高
     -->
    <div>
        <h1>学习iframe标签</h1>
        <div>
            哈哈哈哈
            <iframe src="http://www.baidu.com" width="300"></iframe>
            <iframe src="./01.html" width="300"></iframe>
        </div>
    </div>

</body>
</html>
```

## 十、html书写规范
### 01.标签换行写法
```html
<div>
    <p>
        今天的天
        <span>真的好啊</span>
    </p>
</div>
```
### 02.标签需要关闭
```html
<p>
    <span>哈哈哈哈哈</span>
    <em>呵呵呵呵</em>
</p>
```
### 03.代码缩进使用tab键
>tab每次缩进空格数量一样，我们可以设置。也为了方便代码合并
>shift+tab是向前缩进
### 04.标签的正确嵌套
```html
<ul>
    <li></li>
    <li></li>
</ul>
<dl>
    <dt></dt>
    <dd>

    </dd>
</dl>
```
### 05.合理加注释
### 06.a标签不能嵌套a标签
```html
<a href="">
    <a href=""></a>
</a>
```
### 07.特殊符号的实体
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>特殊符号的实体</title>
</head>
<body>
    <!--
        使用实体
        在html中，会把一个或多个空格或回车解析成一个空格显示
        在html中 特殊符号，一般不会直接书写，而是使用代表这个符号的实体（编码）

        空格： &nbsp;
        大于：&gt;
        小于：&lt;
        版权：&copy;
        双引号：&quot;
    -->
    <p>今天天&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;气好晴朗</p>
    &gt;&lt;&copy;&quot;

</body>
</html>
```

## 十一、html标签的语义化
>1、语义化标签更具有可读性，便于团队的开发和维护
>2、没有css的情况下，网页也能很好的呈现出内容结构和代码结构
>3、关于SEO，搜索引擎更能理解到网页中各部分之间的关系，更准确更快速搜索信息

## 十二、html5语义化标签
### 01.header标签：
>1、用来定义文档（网页或者是某一个段落）的页眉（头部）
>2、可能包含一些标题元素，也可能包含其他元素，比如logo、搜索框、作者信息等等
>3、`<header>` 元素不是分段内容，而是属于独立分块的头部.因此不会往 大纲 中引入新的段落。也就是说，<header> 元素通常用于包含周围部分的标题（h1 至 h6 元素），但这不是必需的。
>4、完成的网页或者是完整的块（网页的一个独立区域）是头部、内容、 尾部组成的（并不是强制）
>5、整个页面没有header限制个数，可以使用多个
>6、`<header>` 元素不能作为 `<address>`、`<footer>` 或另一个 `<header>` 元素的子元素。
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>header标签</title>
</head>
<body>
    <div>
        <!--头部区域-->
        <header>
            <h1>你看我像不像logo</h1>
            <nav>
                <a href="###">news</a>
                <a href="###">my</a>
                <a href="###">tiyu</a>
            </nav>
        </header>
        <!--内容区域-->
    </div>
</body>
</html>
```
### 02.footer标签：
>footer标签：
>1、footer标签代表一个网页或者章节内容的底部区域（页脚）
>2、footer通常包含章节的作者，版权数据和文章的其他链接
>3、其他和header同理，比如不是独立的区域，应该是隶属于一个章节或者是网页
>4、`<footer>` 元素不能作为 `<address>`、`<header>` 或另一个 `<footer>` 元素的子元素。
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>footer</title>
</head>
<body>
    <div>
        <!--头部区域-->
        <header>
            <h1>你看我像不像logo</h1>
            <nav>
                <a href="###">news</a>
                <a href="###">my</a>
                <a href="###">tiyu</a>
            </nav>
        </header>
        <!--内容区域-->

        <!--底部区域-->
        <footer>
            <div>
                <h3>友情链接</h3>
                <a href="###">百度</a>
                <a href="###">阿里巴巴</a>
                <a href="###">阿里妈妈</a>
            </div>
        </footer>
    </div>
</body>
</html>
```
### 03.nav标签：
>1.`<nav>`元素表示页面的一部分，其目的是在当前文档或其他文档中提供导航链接。
>2.导航部分的常见示例是菜单，目录和索引
>3.并不是所有的导航都需要用nav标签，只是当前页面中比较重要的热门的可以使用nav，比如在底部导航，就没有必要加入链接
>4.一个网页可能会有多个导航，比如整个网页的导航，也可以是某一块区域的导航

**注意**
nav使用有两种方法：
    1、当nav中的导航列表是静态的
        nav中直接嵌套a标签使用即可

    2、当nav中的导航是动态的（需要滑动查看更多，主要出现在移动端）
        nav中最好嵌套ul>li>a标签
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>nav标签</title>
</head>
<body>
    <div>
        <!--头部区域-->
        <header>
            <h1>你看我像不像logo</h1>
            <nav>
                <a href="###">news</a>
                <a href="###">my</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
            </nav>
            <!--
            <nav>
                <ul>
                    <li><a href="###">news</a></li>
                    <li><a href="###">news</a></li>
                    <li><a href="###">news</a></li>
                    <li><a href="###">news</a></li>
                    <li><a href="###">news</a></li>
                    <li><a href="###">news</a></li>
                    <li><a href="###">news</a></li>
                    <li><a href="###">news</a></li>
                    <li><a href="###">news</a></li>
                </ul>
            </nav>-->
        </header>
        <!--内容区域-->

        <!--底部区域-->
        <footer>
            <div>
                <h3>友情链接</h3>
                <a href="###">百度</a>
                <a href="###">阿里巴巴</a>
                <a href="###">阿里妈妈</a>
            </div>
        </footer>
    </div>


</body>
</html>
```
### 04.section标签：
>1、section是html中一个独立的区域（主要针对网页分块），没有其他语义，一般会包含一个独立的标题
>2、假设有一个效果，上边是nav导航栏，导航栏一般对对应一个区域，用来显示这个导航到的内容，这个区域我们就可以使用section
>3、section主要是对网页进行分块，也可以对网页中的某块内容进行分块
>4、通常一个完整的section是有标题和内容组成的，不推荐给没有标题的区域设置section
>5、如果想要给一个内容设置有个容器用来书写样式，那么还是推荐使用div
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>section标签</title>
</head>
<body>
    <div>
        <!--头部区域-->
        <header>
            <h1>你看我像不像logo</h1>
            <nav>
                <a href="###">news</a>
                <a href="###">my</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
            </nav>
        </header>
        <!--内容区域-->
        <section>
            <h2>我是section元素的头部啊啊啊啊啊</h2>

        </section>
        <!--底部区域-->
        <footer>
            <div>
                <h3>友情链接</h3>
                <a href="###">百度</a>
                <a href="###">阿里巴巴</a>
                <a href="###">阿里妈妈</a>
            </div>
        </footer>
    </div>
</body>
</html>
```
### 05.article标签
>1、代表文档、页面、或程序中，可以独立的完整的被外部引用的内容
>2、比如一篇博客、一篇文章、一段用户的评论、一个日历插件，或者是其他独立内容
>3、一般来说 一个article也有自己的头部header，或者是footer
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>article</title>
</head>
<body>
    <div>
        <!--头部区域-->
        <header>
            <h1>你看我像不像logo</h1>
            <nav>
                <a href="###">news</a>
                <a href="###">my</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
            </nav>
        </header>
        <!--内容区域-->
        <section>
            <h2>这里是评论区域</h2>
            <article>
                <h3>评论人：张三</h3>
                <p>今天天气真好</p>
            </article>
            <article>
                <h3>评论人：李四</h3>
                <p>今天天气真好</p>
            </article>
            <article>
                <h3>评论人：王五</h3>
                <p>今天天气真好</p>
            </article>
        </section>
        <!--底部区域-->
        <footer>
            <div>
                <h3>友情链接</h3>
                <a href="###">百度</a>
                <a href="###">阿里巴巴</a>
                <a href="###">阿里妈妈</a>
            </div>
        </footer>
    </div>

</body>
</html>
```
### 06.div、article和section
**article和section**
>1、article元素可以看做是特殊的section，但是强调独立性比section更强
>2、section主要强调分段分块，article是强调很强的独立性
>3、原则上来说能用article的时候，也可以使用section，但是假设用article更合适，请使用article

**div、article和section**
>div、section、article语义依次递增
>div没有任何的语义，仅仅是用作样式，可以用在任何场景，但是我们容易看不清上下文关系
>对于主题性的区域，我们可以使用section
>加入这个区域可以脱离上下文，作为完整独立的内容存在，使用article

### 07.aside元素：
>1、表示一个和其余页面内容几乎无关的区域
>2、被认为是独立于内容的一部分，并且可以拆出来而不会使整体收到影响，通常表现为侧边栏
>3、这个里边的内容和其他元素内容关联性不强
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>aside元素</title>
</head>
<body>
    <div>
        <!--头部区域-->
        <header>
            <h1>你看我像不像logo</h1>
            <nav>
                <a href="###">news</a>
                <a href="###">my</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
                <a href="###">tiyu</a>
            </nav>
        </header>
        <!--内容区域-->

        <div>
            <!-- 主题区域-->
            <section>
                <h2>这里是评论区域</h2>
                <article>
                    <h3>评论人：张三</h3>
                    <p>今天天气真好</p>
                </article>
                <article>
                    <h3>评论人：李四</h3>
                    <p>今天天气真好</p>
                </article>
                <article>
                    <h3>评论人：王五</h3>
                    <p>今天天气真好</p>
                </article>
            </section>
            <!--侧边栏-->
            <aside>
                我是侧边栏内容
            </aside>
        </div>

        <!--底部区域-->
        <footer>
            <div>
                <h3>友情链接</h3>
                <a href="###">百度</a>
                <a href="###">阿里巴巴</a>
                <a href="###">阿里妈妈</a>
            </div>
        </footer>
    </div>

</body>
</html>
```
### 08.figure元素
>1、代表一块独立的内容，是一个独立的引用单元
>2、这个标签在主文中用来引用 图片、插画、表格、代码段等等信息
>3、一般会在figure元素中插入figcaption元素（标题元素），将figcaption代表的标题与figure内容相关联
>4、如果是单独一张图片 或者 单独的表格等等，那么直接使用相应的标签即可，如果存在图片和标题，那么请使用figure标签
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>figure</title>
</head>
<body>
    <figure>
        <figcaption>海贼王的图片</figcaption>
        <img src="../images/05.jpg" alt="" width="300">
    </figure>
</body>
</html>
```
### 09.mark元素：
>1、为引用的内容进行标记或突出显示文本，用来表示和上下文之间的关联性
>2、突出显示的文本通常可能和用户当前的活动等有一定的关联性
>3、比如，用户搜索的时候，它可以显示搜索之后的关键字
>4、不要把mark和 em、strong进行混淆。em、strong都是表示文本在上下文的重要性，而mark只是为了表示关联性
>5、mark标签是行内标签，默认黄色背景颜色
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>mark元素</title>
</head>
<body>
    <input type="text" value="下雨">
    <p>今天晚上可能会<mark>下雨</mark>，明天中秋节晴朗</p>
</body>
</html>
```
### 10.time元素：
>1、用来表示24小时制 或者是 一个公历时间
>2、作用：以机器可读的格式去表示日期和时间，安排日程表的应用就可以使用这个time标签
>3、通用时间格式  XXXX-XX-XX XX:XX:XX

>两种用法：
>1、time标签直接包含时间
>2、使用datetime属性来表示时间
```html
<!--内容区域-->
    <div>
        <!-- 主题区域-->
        <section>
            <h2>这里是评论区域</h2>
            <article>
                <h3>评论人：张三</h3>
                <p>今天天气真好</p>
                <p><time>2019-9-12 19:00:00</time></p>
            </article>
            <article>
                <h3>评论人：李四</h3>
                <p>今天天气真好</p>
                <p><time datetime="2019-9-12 18:00:00">一小时之前</time></p>
            </article>
            <article>
                <h3>评论人：王五</h3>
                <p>今天天气真好</p>
            </article>
        </section>
        <!--侧边栏-->
        <aside>
            我是侧边栏内容
        </aside>
    </div>

```
### 11.datalist 元素：
>1、包含了一组option元素，代表是列表可选的值
>2、和input进行相关联，用来配套使用
>3、input中的list属性 == datalist的id属性
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>datalist元素</title>
</head>
<body>
    <input list="city" type="text">
    <datalist id="city">
        <option value="河南">河南</option>
        <option value="河北">河北</option>
        <option value="湖北">湖北</option>
        <option value="湖南">湖南</option>
        <option value="胡建">胡建</option>
    </datalist>
</body>
</html>
```
### 12.progress元素：
>1、主要用来显示一项任务的完成程度
>2、规范没有规定默认的样式，所以各个浏览器默认的样式不一定相同

>属性:
>    value：是当前进度的值
>    max：是总进度的长度
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>progress元素</title>
</head>
<body>
    <progress max="100" value="80"></progress>
</body>
</html>
```
### 13.ruby元素
>HTML <ruby> 元素 被用来展示东亚文字注音或字符注释
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>注释标签</title>
</head>
<body>
    <p>
        <ruby>蠡<rt>li</rt></ruby>
    </p>
</body>
</html>
```
## 十三、表单的新增功能
### 01.表单的新属性
                    h5规范允许 当属性名和属性值相等的时候  可以直接书写属性名即可
                                        在js中，h5允许以布尔值的形式控制属性开启或关闭
                        也就是在js中 给autofocus属性设置值为true（真，打开） 或者是 false（假，关闭）
                        但是在元素的属性中 不允许使用true或者是false来控制开启或关闭
    
                    如果多个表单书写autofocus，那么以第一个书写的为准

>placeholder：     占位符

>autocomplete： 是否提示用户曾经输入过的值  默认是on  关闭是off

>autofocus：        默认自动获取焦点
                    			    他有唯一一个值是autofocus

>required：         必填项，当提交的时候，此表单必须填写

>disabled：         禁用任何表单元素，这个元素就被禁止输入或选择等等操作
                    				使用disabled禁用表单，表单元素是不会在被提交了

>checked：          单选框或多选框 默认被选中

>readonly：         对于可编辑的表单来说 表示不能再次被编辑  但是是可以被提交的
                    				对单选多选按钮不支持

>form：             	如果input存在form属性，表示当前的input属于某一个表单
                   				 此时form表单的id的值 就是这个input的值
                    				那么form表单 和当前的input就进行关联了
                    				无论input书写在哪里，都能随着表单发送数据
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表单元素的新属性</title>
</head>
<body>
<form action="###" method="get" id="form1">
    请输入用户名：
    <input type="text" name="user" placeholder="请输入用户名" autofocus autocomplete="off">
    <br>

    请输入密码：
    <input type="text" name="pass" value="123456" autofocus required>
    <br>

    请确认性别：
    男：<input type="radio" name="sex" value="男" disabled checked>
    女：<input type="radio" name="sex" value="女" disabled>
    <br>


    请确认年龄：
    大于30岁：<input type="radio" name="age" value="30-" checked readonly>
    小于30岁：<input type="radio" name="age" value="30+" readonly>

    请输入邮箱：
    <input type="email" name="email" value="lipeihua@atguigu.com" readonly>

    <br>
    <button>提交</button>
</form>

<!--在form表单外有一个input，但是想点击form中的提交按钮的时候，把这个input也给提交了，form属性就这样使用-->
<input type="hidden" name="id" form="form1" value="12587">
</body>
</html>
```

### 02.表单的新类型
>input：（如果input的新类型不被浏览器所支持，那么他会默认显示成text文本框）
        大多数都被谷歌浏览器支持，如果开发移动端，只要谷歌支持即可，因为所有安卓系统内置浏览器都是chrome

>type类型：
    text：       文本框
    password：   密码框
    radio：      单选框
    checkbox：   多选框
    hidden：     隐藏域
    file：       文件域
    button：     按钮
    reset：      重置按钮
    submit：     提交按钮

    color：      用来引入或者打开指定颜色的控件
    date：       日期的控件（年月日）
    week：       日期的控件（年周）（火狐不支持）
    month：      日期的控件（年月）（火狐不支持）
    
    email：      编辑email的字段
                    1、自带验证，但是验证不完整，一般还是自己书写
                    2、在移动端上 有相对应的自动弹出键盘包含 @ .com 等按键
    number：     用来输入数字的控件
                    1、多了一个上下的按键，可以增加和降低数字大小
                    2、验证必须是数字
                    3、其他属性
                        min：最少数量
                        max：最大数量
                        value：当前数量
                        step：每次累加累减数量
    
    search：     用来搜索框，当用户输入内容后，在末尾有一个删除按钮，单击可以删除输入好的文字
    tel：        电话号码输入框
    url：        url地址
    
    range：      输入一个拖拽的控件
                属性：
                    max：最大值
                    min：最小值
                    step：每次走的最小单位
                    value：当前值
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>新type类型-input</title>
</head>
<body>
    <form action="###" method="get">
        请选择你喜欢的颜色：
        <input type="color" name="color">
        <br>

        请选择你的出生日期：
        <input type="date" name="brithday">
        <br>

        请输入当前的周数：
        <input type="week" name="week">
        <br>

        请输入你几月生日：
        <input type="month" name="month">
        <br>

        请输入您的邮箱地址：
        <input type="email" name="email">
        <br>

        请选择您购买的数量：
        <input type="number" name="num" min="2" max="10" step="2">
        <br>

        请在本框中进行检索：
        <input type="search" name="sear">
        <br>

        请输入您的电话号码：
        <input type="tel" name="tel">
        <br>

        请输入你的个人博客的网址：
        <input type="url" name="url">
        <br>

        请选择：
        <input type="range" name="range" min="30" max="100" value="50">
        <br>
        <br>
        <button>提交</button>
    </form>

</body>
</html>
```
### 03.select元素的新属性
>selected： 默认选中项
>multiple： 让select可以进行多选（按住ctrl键进行多选）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>select元素的属性</title>
</head>
<body>
<form action="###" method="get">
    请选择你喜欢的食物：
    <select name="food" id="" multiple>
        <option value="肉">肉</option>
        <option value="鸡蛋">鸡蛋</option>
        <option value="水果" selected>水果</option>
        <option value="骨头">骨头</option>
    </select>
    <button>提交</button>
</form>
</body>
</html>
```
### 05.调用相册和摄像头
>input的file补充：
>`<input type="file" accept="image/*" capture="camera">`
>`<input type="file" accept="image/*" capture="photo">`
>文件域 的 accept属性书写 image/*  代表接受任何格式的图片
    capture=camera  代表从相机拍照接收
    capture=photo  代表从相册选取照片
>但是在pc端的表现都是选取文件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>调用本地相册和相机</title>
</head>
<body>

    <input type="file" accept="image/*" capture="camera">

    <input type="file" accept="image/*" capture="photo">
</body>
</html>
```
## 十四.音视频
### 01.音视频历史
>大家都有在网页中浏览视频的经历，但在HTML5之前，对视频乃至音频都还没有一个标准
因此在网页中看到的视频，都是通过第三插件的方式嵌入的，可能是QuickTime，也可能是RealPlayer 或者 Flash。浏览器很好的整合了这些插件，你完全意识不到它们的存在
<img src=https://upload-images.jianshu.io/upload_images/3532891-71eca012693b1cd3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=150 > 
<img src=https://upload-images.jianshu.io/upload_images/3532891-a8866b38473ee8e4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=150>
<img src=https://upload-images.jianshu.io/upload_images/3532891-82f479c3b2669025.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 width=150>

### 02.音视频格式
>大多数人会认为视频文件就是 .avi .mp4,但事实上 avi和mp4仅仅是容器的格式，它只决定怎么将视频存储起来，而不关系存储的内容。有点类似于.zip
>不管是音频文件或视频文件，实际上都只是一个容器文件。这点类似于压缩了一组文件的ZIP文件，视频文件（视频容器）包含了音频轨道、视频轨道和其他一些元数据。
>视频播放的时候，音频轨道和视频轨道是绑定在一起的。
>**元数据包含了视频的封面、标题、子标题、字幕、时间等相关信息**

<img src=https://upload-images.jianshu.io/upload_images/3532891-3467fbc4c1027a02.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 03.编解码器
>音频和视频编码/解码是一组算法，用来对一段特定音频或视频进行解码和编码，以便音频和视频能够播放。
>原始的媒体文件体积非常巨大，如果不对其进行编码，那么数据量是非常惊人的，在互联网上传播则要耗费无法忍受的时间；
>如果不对其进行解码，就无法将编码后的数据重组为原始的媒体数据

<img src=https://upload-images.jianshu.io/upload_images/3532891-467142d4c36c9382.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

>H.264： 别名 MPEG-4的第十部分,由MPEG研发并于2003年标准化
它的目的支持一切设备，无论是低带宽低cpu，还是高带宽高cpu 或者是两者之间。
要做到这一点，H.264标准被分成不同的几种配置。高配置使用了更多特性，
这会导致在解码过程中更加消耗CPU，但视频文件本身会更小，视频效果也更好							  
>苹果iphone手机		基本配置(BaseLine)
正常的电视机支持        	基本配置(BaseLine) 和 主配置(Main)两种
正常的电脑支持  	           基本配置(BaseLine) 和 主配置(Main) 高级配置(high)三种

>当然有一些编解码器受专利的保护，有一些则是免费的，例如Ogg的Vorbis音频编解码器。
Ogg的Theora视频编解码器也是可以免费使用的。而想使用H.264的话就需要支付相关的费用了
现在的视频编解码器会使用各种技巧减少从一帧到另一帧过程中传递的信息数量，它们不会存储每一帧的所有信息，而只是存储两帧之间的差异信息。
编码器也分有损和无损，无损视频文件一般太大，在网页中没有优势，所以我们重点研究有损编解码器。
有损编解码器中，信息在编码过程中丢失是无法避免的，反复的对视频编码会导致其画面不均匀。

###04.不同浏览器对音视频的兼容性
目前还没有一种编解码和容器的组合能应用于所有的浏览器中！！！
<img src=https://upload-images.jianshu.io/upload_images/3532891-9d265619a691b13e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
<img src=https://upload-images.jianshu.io/upload_images/3532891-7dc1c7dbe20e88e3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 05.音视频格式的转换
**使用ffmpeg工具**
>1.安装，并找到bin目录
>2.在计算机图标上右键
>3.选择属性
>4.更改设置
>5.高级
>6.环境变量
>7.找到系统变量的 path
>8.把ffmpeg 的 bin的路径添到后边
>9.一直点确定完成

**测试是否安装成功**
>1.window+r
>2.输入CMD
>3.打开命令行窗口 输入ffmpeg 检测是否安装成功

**ffmpeg的使用**
>用 FFmpeg 制作MP4 视频
ffmpeg -i test.mp4 -c:v libx264 -s 1280x720 -b:v 1500k -profile:v high -level 3.1 -c:a aac -ac 2 -b:a 160k -movflags faststart OUTPUT.mp4

>用 FFmpeg 制作 WebM 视频
ffmpeg -i test.mp4 -c:v libvpx -s 1280x720 -b:v 1500k -c:a libvorbis -ac 2 -b:a 160k OUTPUT.webm   

>FFmpeg 制作 Ogg 视频
ffmpeg -i test.mp4 -c:v libtheora -s 1280x720 -b:v 1500k -c:a libvorbis -ac 2 -b:a 160k OUTPUT.ogv

>FFmpeg 制作Mp3音频
ffmpeg -i tt.mp3 -c:a libmp3lame -ac 2 -b:a 160k OUTPUT.mp3

>FFmpeg 制作Ogg音频
ffmpeg -i tt.mp3 -c:a libvorbis -ac 2 -b:a 160k OUTPUT.ogg

>FFmpeg 制作ACC音频	
ffmpeg -i tt.mp3 -c:a aac -ac 2 -b:a 160k OUTPUT.aac

### 06.音视频旧格式
>`<object>` 标签的作用是在 HTML 页面中嵌入多媒体元素
`<object data="1.swf" width="400"></object>`

>`<embed>` 标签的作用是在 HTML 页面中嵌入多媒体元素
`<embed src="1.swf" width="400">`

**为什么淘汰：**
>`<object>`缺点：
需要flash，效率低
如果浏览器不支持 Flash，那么视频将无法播放
iPad 和 iPhone 不能显示 Flash 视频
将视频转换为其他格式，仍然不能在所有浏览器中播放
目前安卓4.4也抛弃了flash......

### 07.html5的新音视频标签
>视频基本标签用法 ：
`<video width=" " height="" src=""> </video>`
	src 属性：指定播放文件的URL。
	width、height属性：
		设置媒体元素的大小，单位为像素；
		省略该属性，则使用播放源文件的大小；
		仅设置宽度值，将根据播放源文件的长宽比例自动生成一个与之对应的高度值。
>音频基本格式 ：
`<audio  src="" controls> </audio>`
src 属性：指定播放文件的URL。
其他和视频一样。

>指定一种视频格式，不能播就提示：
`<video src="examp.mp4" >您的浏览器不支持</video>`

>给定多个source标签，给定多种视频格式，浏览器根据自身支持程度选择播放哪一种
`<source src=”1.mp4” type=”video/mp4” />`

### 08.音视频标签的属性
<img src=https://upload-images.jianshu.io/upload_images/3532891-c015210c8510148e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
<img src=https://upload-images.jianshu.io/upload_images/3532891-8f1f9c805bc8e7eb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

>preload：
    该属性旨在告诉浏览器作者认为达到最佳的用户体验的方式是什么
    1.none: 提示作者认为用户不需要查看该视频，服务器也想要最小化访问流量；换句话说就是提示浏览器该视频不需要缓存。
    2.metadata: 提示尽管我们认为用户不需要查看该视频，不过抓取元数据（比如：长度）还是很合理的。
    3.auto: 用户需要这个视频优先加载；换句话说就是提示：如果需要的话，可以下载整个视频，即使用户并不一定会用它。
    4.空字符串：也就代指 auto 值。

### 十五.SEO
### 01.基本概念
>1.**搜索引擎优化（SearchEngine Optimization，简称SEO）**，指在了解搜索引擎自然搜索机制的基础之上，对网站进行内部及外部的调整优化，改进网站在搜索引擎中关键字的自然排名，获得更多的展现量，吸引更多目标客户点击访问网站，从而达到互联网营销及品牌建设的目标
>
>2.**SEO**可以帮助将网站中的高质量内容更好的呈现给搜索引擎，SEO和搜索引擎，是良性的共生关系
<img src=https://upload-images.jianshu.io/upload_images/3532891-55960db49c4a875f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 02.喂养爬虫
>1.让爬虫抓取自己网站更多的网页，往往能够提高网站整体的质量和排名。让爬虫抓的更多，有两个方法：
>2.爬虫通常通过链接来发现更多的网页。通过建立更多链接到自己网站的链接，来留住爬虫，提高网站排名。
>3.提高网站加载速度，让爬虫在一定时间内能够访问更多网页

### 03.内链与外链：
>1.内链指的是链接到网站内部的链接，内链能有效的提高排名
>2.外链指的是连接到网站外部的链接，外链能比内链更好的提高排名
>3.外链不可控制，但是内链可以自己建立许多，保证网站内部的页面能够互相连接。
>4.内链的锚文本一定要真实,锚文本填写不真实，最严重会导致搜索引擎视为欺骗，删除所有排名
### 04.SEO与SEM：
>1.**SEO**：搜索引擎优化，通过优化网站质量提高网站在搜索引擎中的排名，是SEM的一种常用方式
>2.**SEM**：搜索引擎营销，除了免费的SEO，还有PPC等付费模式
>3.**关键词**指的是在搜索引擎中搜索的词，通常在搜索结果中会被标成红色
<img src=https://upload-images.jianshu.io/upload_images/3532891-32f83a596e1e9dee.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
>4.排名越靠前，网站被点击量越高，越容易产生收益。第一名的点击量远远比第二名大得多
<img src=https://upload-images.jianshu.io/upload_images/3532891-7a55ab08e6e747c5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 05.HTML代码SEO优化：
>1.标签语义化：根据标签的语义合理使用
>1.图片alt一定要合理书写
>2.a标签内部的文本（锚文本）对关键词排名影响非常大
>3.合理利用搜索引擎重视的标签(title，strong，h1-h3，a，em，img&alt）